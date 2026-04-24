# Persistence Techniques Prompts

> **Collection:** Red Team Operations  
> **Category:** Persistence  
> **Language:** Bilingual (English/Arabic)  
> **Last Updated:** 2024

---

## Prompt 1: Registry Persistence

### Description
A comprehensive prompt for analyzing and detecting Windows Registry-based persistence mechanisms used by threat actors to maintain access to compromised systems.

### Tags
`persistence` `registry` `windows` `red-team` `T1547`

---

## 🇬🇧 English Prompt

```
You are a senior red team operator and malware analyst specializing in Windows persistence mechanisms. Provide a comprehensive technical analysis of Registry-based persistence techniques.

Please cover the following areas:

1. **Common Registry Persistence Locations:**
   - Run and RunOnce keys (HKLM/HKCU)
   - Winlogon Helper DLL
   - Services registry entries
   - Browser Helper Objects (BHOs)
   - Shell Extensions and ContextMenuHandlers
   - Boot Execute entries
   - Image File Execution Options (IFEO)

2. **Technical Implementation Examples:**
   - PowerShell commands for establishing persistence
   - Batch script implementations
   - C/C++ code snippets for programmatic registry manipulation
   - LOLBAS (Living Off The Land Binaries) techniques

3. **Stealth Considerations:**
   - Avoiding detection by AV/EDR solutions
   - Registry key obfuscation techniques
   - Legitimate-looking registry entry naming conventions

4. **Detection & Hunting:**
   - Sigma/YARA rule examples for registry persistence
   - PowerShell detection queries
   - Event ID monitoring (4657, 13)
   - Baseline comparison methodologies

5. **MITRE ATT&CK Mapping:**
   - T1547.001: Boot or Logon Autostart Execution: Registry Run Keys
   - T1546.003: Event Triggered Execution: Windows Management Instrumentation Event Subscription

Provide actionable detection queries and mitigation strategies for blue team defenders.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت خبير في فريق الهجوم الأحمر ومحلل برمجيات خبيثة متخصص في آليات الثبات في نظام Windows. قدم تحليلاً تقنياً شاملاً لتقنيات الثبات عبر سجل النظام (Registry).

يرجى تغطية المجالات التالية:

1. **مواقع الثبات الشائعة في السجل:**
   - مفاتيح Run و RunOnce (HKLM/HKCU)
   - Winlogon Helper DLL
   - إدخالات سجل الخدمات
   - كائنات مساعد المتصفح (BHOs)
   - ملحقات Shell ومعالجات القائمة السياقية
   - إدخالات Boot Execute
   - خيارات تنفيذ ملف الصورة (IFEO)

2. **أمثلة التنفيذ التقني:**
   - أوامر PowerShell لإنشاء الثبات
   - تطبيقات Batch Script
   - مقتطفات كود C/C++ للتعامل البرمجي مع السجل
   - تقنيات LOLBAS (الاستفادة من الأدوات الشرعية)

3. **اعتبارات التخفي:**
   - تجنب الكشف من حلول AV/EDR
   - تقنيات تشويش مفاتيح السجل
   - اصطلاحات التسمية التي تبدو شرعية

4. **الكشف والبحث:**
   - أمثلة قواعد Sigma/YARA للثبات في السجل
   - استعلامات PowerShell للكشف
   - مراقبة معرّفات الأحداث (4657, 13)
   - منهجيات مقارنة خط الأساس

5. **ربط إطار MITRE ATT&CK:**
   - T1547.001: التنفيذ التلقائي عند التمهيد أو تسجيل الدخول: مفاتيح Run
   - T1546.003: التنفيذ المُفعّل بالأحداث: اشتراكات WMI

قدم استعلامات كشف قابلة للتنفيذ واستراتيجيات التخفيف لفرق الدفاع الأزرق.
```

---

## Example Output Preview

```
# Registry Persistence Analysis

## 1. Run Keys Persistence

### HKLM\Software\Microsoft\Windows\CurrentVersion\Run
```powershell
# Establish persistence via PowerShell
Set-ItemProperty -Path "HKLM:\Software\Microsoft\Windows\CurrentVersion\Run" `
    -Name "SecurityUpdate" -Value "C:\ProgramData\update.exe"
```

### Detection - Sigma Rule
```yaml
title: Registry Run Key Persistence
status: experimental
logsource:
  category: registry_event
detection:
  selection:
    TargetObject|contains:
      - '\CurrentVersion\Run'
      - '\CurrentVersion\RunOnce'
  condition: selection
```

## 2. Winlogon Helper DLL
```powershell
Set-ItemProperty -Path "HKLM:\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Winlogon" `
    -Name "Shell" -Value "explorer.exe, C:\temp\malicious.dll"
```
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 2: Scheduled Tasks Persistence

### Description
An in-depth prompt for understanding and detecting persistence through Windows Task Scheduler, covering creation methods, stealth techniques, and detection strategies.

### Tags
`persistence` `scheduled-tasks` `windows` `red-team` `T1053`

---

## 🇬🇧 English Prompt

```
You are an advanced red team specialist focusing on Windows Task Scheduler persistence mechanisms. Provide a detailed technical guide on Scheduled Tasks persistence.

Please address the following comprehensive topics:

1. **Scheduled Tasks Creation Methods:**
   - schtasks.exe command-line usage
   - PowerShell Scheduled Tasks module
   - XML task definition files
   - COM interface manipulation (ITaskService)
   - Direct Task Scheduler API calls

2. **Advanced Task Configuration:**
   - Trigger types (boot, logon, idle, event-based)
   - Execution with elevated privileges
   - Running as SYSTEM or specific users
   - Multiple actions per task
   - Task repetition and interval settings

3. **Persistence Scenarios:**
   - At-logon payload execution
   - Boot-time persistence
   - Event-triggered execution (e.g., on specific Event ID)
   - Idle-state task execution
   - User session-based triggers

4. **Evasion Techniques:**
   - Task naming conventions mimicking legitimate Windows tasks
   - Binary path obfuscation
   - Arguments encoding and hiding
   - Disabling task history logging
   - Time-based execution to avoid business hours monitoring

5. **Detection & Forensics:**
   - Event IDs to monitor (4698, 4699, 4700, 4701, 4702)
   - PowerShell hunting queries
   - Task folder enumeration and analysis
   - Baseline comparison for unauthorized tasks
   - Sigma rules and Splunk queries

6. **MITRE ATT&CK Reference:**
   - T1053.005: Scheduled Task/Job: Scheduled Task
   - Related techniques for lateral movement via scheduled tasks

Include practical command examples and complete detection rule sets.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت خبير متقدم في فريق الهجوم الأحمر متخصص في آليات الثبات عبر مجدول مهام Windows. قدم دليلاً تقنياً مفصلاً عن الثبات من خلال المهام المجدولة.

يرجى معالجة المواضيع الشاملة التالية:

1. **طرق إنشاء المهام المجدولة:**
   - استخدام سطر الأوامر schtasks.exe
   - وحدة PowerShell للمهام المجدولة
   - ملفات تعريف المهام بتنسيق XML
   - التعامل مع واجهة COM (ITaskService)
   - استدعاءات API مباشرة لمجدول المهام

2. **تكوين المهام المتقدم:**
   - أنواع المحفزات (التمهيد، تسجيل الدخول، الخمول، المستندة للأحداث)
   - التنفيذ بصلاحيات مرتفعة
   - التشغيل كـ SYSTEM أو مستخدمين محددين
   - إجراءات متعددة لكل مهمة
   - إعدادات التكرار والفواصل الزمنية

3. **سيناريوهات الثبات:**
   - تنفيذ الحمولة عند تسجيل الدخول
   - الثبات عند وقت التمهيد
   - التنفيذ المُفعّل بالأحداث (مثلاً عند معرّف حدث محدد)
   - تنفيذ المهام في حالة الخمول
   - محفزات مستندة إلى جلسة المستخدم

4. **تقنيات التخفي:**
   - اصطلاحات تسمية المهام التي تحاكي مهام Windows الشرعية
   - تشويش مسار الملف التنفيذي
   - ترميز وإخفاء الوسائط
   - تعطيل تسجيل تاريخ المهام
   - التنفيذ المستند إلى الوقت لتجنب المراقبة خلال ساعات العمل

5. **الكشف والطب الشرعي:**
   - معرّفات الأحداث للمراقبة (4698، 4699، 4700، 4701، 4702)
   - استعلامات PowerShell للبحث
   - تعداد وتحليل مجلدات المهام
   - مقارنة خط الأساس للمهام غير المصرح بها
   - قواعد Sigma واستعلامات Splunk

6. **مرجع MITRE ATT&CK:**
   - T1053.005: مهمة مجدولة/وظيفة: مهمة مجدولة
   - التقنيات ذات الصلة للحركة الجانبية عبر المهام المجدولة

أمثلة أوامر عملية ومجموعات قواعد كشف كاملة.
```

---

## Example Output Preview

```
# Scheduled Tasks Persistence Analysis

## 1. Basic Task Creation
```cmd
schtasks /create /tn "Microsoft\Windows\UpdateHelper" /tr "C:\ProgramData\update.exe" /sc onlogon /rl HIGHEST
```

## 2. PowerShell Task Creation
```powershell
$trigger = New-ScheduledTaskTrigger -AtLogon
$action = New-ScheduledTaskAction -Execute "C:\temp\payload.exe"
$settings = New-ScheduledTaskSettingsSet -Hidden -AllowStartIfOnBatteries
Register-ScheduledTask -TaskName "SecurityMaintenance" -Trigger $trigger -Action $action -Settings $settings -RunLevel Highest
```

## 3. Detection - Event Log Query
```powershell
Get-WinEvent -FilterHashtable @{LogName='Security'; ID=4698,4702} | 
    Where-Object {$_.Message -match "suspicious_task_name"}
```

## 4. Sigma Rule
```yaml
title: Suspicious Scheduled Task Creation
detection:
  selection:
    EventID: 4698
    TaskContent|contains:
      - 'cmd.exe'
      - 'powershell'
      - 'wscript'
      - 'mshta'
  condition: selection
```
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 3: WMI Event Subscriptions

### Description
A technical prompt for understanding Windows Management Instrumentation (WMI) event subscriptions as a sophisticated persistence mechanism, including creation methods and detection approaches.

### Tags
`persistence` `wmi` `event-subscription` `windows` `T1546`

---

## 🇬🇧 English Prompt

```
You are a senior red team operator and WMI specialist. Provide an exhaustive technical analysis of WMI Event Subscriptions for persistence purposes.

Cover the following comprehensive areas:

1. **WMI Event Subscription Components:**
   - __EventFilter: Defining the trigger conditions
   - __EventConsumer: Defining the action to execute
   - __FilterToConsumerBinding: Linking filter to consumer
   - Consumer types: CommandLineEventConsumer, ActiveScriptEventConsumer, LogFileEventConsumer, SMTPEventConsumer

2. **Technical Implementation:**
   - PowerShell WMI class creation scripts
   - MOF (Managed Object Format) file deployment
   - mofcomp.exe compilation methods
   - WMI permanent vs. temporary event subscriptions
   - VBScript/JScript payload embedding in ActiveScriptEventConsumer

3. **Common Persistence Patterns:**
   - New process creation triggers
   - File system modification monitoring
   - Registry change detection
   - User logon event triggers
   - Time-based execution via WMI

4. **Stealth and OPSEC Considerations:**
   - Legitimate-looking WMI namespace usage
   - Obfuscating the CommandLineTemplate
   - Using trusted script hosts
   - Cleaning up MOF files after deployment
   - Avoiding common detection signatures

5. **Detection Methodologies:**
   - WMI repository analysis (objects.data)
   - PowerShell enumeration commands
   - WMI activity event log monitoring (Event ID 5861)
   - Sysmon configuration for WMI monitoring
   - YARA rules for MOF file detection

6. **Remediation & Forensics:**
   - Identifying malicious subscriptions
   - Proper removal procedures
   - WMI repository corruption recovery
   - Timeline analysis for forensic investigation

7. **MITRE ATT&CK Mapping:**
   - T1546.003: Event Triggered Execution: Windows Management Instrumentation Event Subscription

Provide complete PowerShell scripts for creation and detection, along with forensic analysis procedures.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت خبير متقدم في فريق الهجوم الأحمر ومتخصص في WMI. قدم تحليلاً تقنياً شاملاً لاشتراكات أحداث WMI لأغراض الثبات.

قم بتغطية المجالات الشاملة التالية:

1. **مكونات اشتراك أحداث WMI:**
   - __EventFilter: تحديد شروط المحفز
   - __EventConsumer: تحديد الإجراء للتنفيذ
   - __FilterToConsumerBinding: ربط المصفى بالمستهلك
   - أنواع المستهلك: CommandLineEventConsumer، ActiveScriptEventConsumer، LogFileEventConsumer، SMTPEventConsumer

2. **التنفيذ التقني:**
   - نصوص PowerShell لإنشاء فئات WMI
   - نشر ملفات MOF (تنسيق الكائنات المُدارة)
   - طرق تجميع mofcomp.exe
   - اشتراكات أحداث WMI الدائمة مقابل المؤقتة
   - تضمين الحمولة بـ VBScript/JScript في ActiveScriptEventConsumer

3. **أنماط الثبات الشائعة:**
   - محفزات إنشاء عملية جديدة
   - مراقبة تعديلات نظام الملفات
   - كشف تغييرات السجل
   - محفزات أحداث تسجيل دخول المستخدم
   - التنفيذ المستند إلى الوقت عبر WMI

4. **اعتبارات التخفي والأمن العملياتي:**
   - استخدام مساحة اسم WMI ذات مظهر شرعي
   - تشويش CommandLineTemplate
   - استخدام مضيفات البرمجة الموثوقة
   - تنظيف ملفات MOF بعد النشر
   - تجنب تواقيع الكشف الشائعة

5. **منهجيات الكشف:**
   - تحليل مستودع WMI (objects.data)
   - أوامر تعداد PowerShell
   - مراقبة سجل نشاط WMI (معرّف الحدث 5861)
   - تكوين Sysmon لمراقبة WMI
   - قواعد YARA للكشف عن ملفات MOF

6. **المعالجة والطب الشرعي:**
   - تحديد الاشتراكات الخبيثة
   - إجراءات الإزالة الصحيحة
   - استعادة تلف مستودع WMI
   - تحليل الجدول الزمني للتحقيق الجنائي

7. **ربط إطار MITRE ATT&CK:**
   - T1546.003: التنفيذ المُفعّل بالأحداث: اشتراك حدث Windows Management Instrumentation

قدم نصوص PowerShell كاملة للإنشاء والكشف، بالإضافة إلى إجراءات التحليل الجنائي.
```

---

## Example Output Preview

```
# WMI Event Subscription Persistence

## 1. Complete PowerShell Implementation
```powershell
# Create Event Filter
$filterName = "SecurityUpdateFilter"
$query = "SELECT * FROM __InstanceCreationEvent WITHIN 5 WHERE TargetInstance ISA 'Win32_Process'"
$filter = Set-WmiInstance -Class __EventFilter -Namespace "root\subscription" -Arguments @{
    Name = $filterName
    EventNamespace = "root\cimv2"
    Query = $query
    QueryLanguage = "WQL"
}

# Create Event Consumer
$consumerName = "SecurityUpdateConsumer"
$consumer = Set-WmiInstance -Class CommandLineEventConsumer -Namespace "root\subscription" -Arguments @{
    Name = $consumerName
    CommandLineTemplate = "C:\Windows\System32\cmd.exe /c C:\temp\payload.exe"
    WorkingDirectory = "C:\Windows\System32"
}

# Bind Filter to Consumer
Set-WmiInstance -Class __FilterToConsumerBinding -Namespace "root\subscription" -Arguments @{
    Filter = $filter
    Consumer = $consumer
}
```

## 2. Detection Commands
```powershell
# Enumerate all event filters
Get-WmiObject -Class __EventFilter -Namespace "root\subscription"

# Enumerate all event consumers
Get-WmiObject -Class __EventConsumer -Namespace "root\subscription"

# Enumerate bindings
Get-WmiObject -Class __FilterToConsumerBinding -Namespace "root\subscription"
```

## 3. MOF File Example
```mof
#pragma namespace("\\\\.\\root\\subscription")
instance of __EventFilter as $FILTER {
    Name = "PersistenceFilter";
    Query = "SELECT * FROM __InstanceCreationEvent WITHIN 60 WHERE TargetInstance ISA 'Win32_Process'";
    QueryLanguage = "WQL";
};
```
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 4: Service Creation Persistence

### Description
A comprehensive prompt for analyzing Windows Service-based persistence mechanisms, covering service creation, manipulation, and detection strategies.

### Tags
`persistence` `windows-service` `privilege-escalation` `red-team` `T1543`

---

## 🇬🇧 English Prompt

```
You are an expert red team operator specializing in Windows service manipulation and persistence. Provide a detailed technical guide on Service Creation Persistence.

Please comprehensively address the following topics:

1. **Service Creation Methods:**
   - sc.exe command-line utility usage
   - PowerShell New-Service cmdlet
   - Service Control Manager API (CreateService)
   - WMI Win32_Service class manipulation
   - Registry-based service creation

2. **Service Configuration Options:**
   - Service types (OWN_PROCESS, SHARE_PROCESS, INTERACTIVE_PROCESS)
   - Start types (AUTO, DEMAND, DISABLED, BOOT)
   - Service failure actions and recovery
   - Service privileges and required permissions
   - Service SID and service isolation

3. **Persistence Scenarios:**
   - Creating new malicious services
   - Modifying existing legitimate services
   - Service binary path manipulation
   - Service DLL hijacking (svchost.exe)
   - Service recovery actions for persistence

4. **Advanced Techniques:**
   - Evasive service naming conventions
   - Service binary path obfuscation
   - Using legitimate Windows binaries (LOLBAS)
   - Service trigger configuration
   - PPL (Protected Process Light) considerations

5. **Privilege Escalation Integration:**
   - SERVICE_ALL_ACCESS requirements
   - Unquoted service path exploitation
   - Weak service permission exploitation
   - Service registry ACL weaknesses
   - Token manipulation for service creation

6. **Detection & Monitoring:**
   - Event ID monitoring (7045, 4697, 7040)
   - PowerShell detection queries
   - Service baseline comparison
   - Sysmon service creation monitoring
   - Sigma rules and SIEM queries

7. **Mitigation Strategies:**
   - Service permission auditing
   - Application whitelisting
   - Service hardening configurations
   - Monitoring privileged service creation

8. **MITRE ATT&CK Reference:**
   - T1543.003: Create or Modify System Process: Windows Service
   - T1574.011: Hijack Execution Flow: Services Registry Permissions Weakness

Include practical attack examples, complete detection rules, and defensive recommendations.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت خبير في فريق الهجوم الأحمر متخصص في التعامل مع خدمات Windows والثبات. قدم دليلاً تقنياً مفصلاً عن الثبات عبر إنشاء الخدمات.

يرجى معالجة المواضيع التالية بشكل شامل:

1. **طرق إنشاء الخدمات:**
   - استخدام أداة سطر الأوامر sc.exe
   - أمر PowerShell New-Service
   - واجهة برمجة Service Control Manager API (CreateService)
   - التعامل مع فئة WMI Win32_Service
   - إنشاء الخدمات عبر السجل

2. **خيارات تكوين الخدمة:**
   - أنواع الخدمات (OWN_PROCESS، SHARE_PROCESS، INTERACTIVE_PROCESS)
   - أنواع البدء (AUTO، DEMAND، DISABLED، BOOT)
   - إجراءات فشل الخدمة والاسترداد
   - امتيازات الخدمة والأذونات المطلوبة
   - SID الخدمة وعزل الخدمة

3. **سيناريوهات الثبات:**
   - إنشاء خدمات خبيثة جديدة
   - تعديل الخدمات الشرعية الموجودة
   - التلاعب بمسار الملف التنفيذي للخدمة
   - اختطاف DLL للخدمة (svchost.exe)
   - إجراءات استرداد الخدمة للثبات

4. **التقنيات المتقدمة:**
   - اصطلاحات تسمية الخدمات الخفية
   - تشويش مسار الملف التنفيذي للخدمة
   - استخدام الملفات التنفيذية الشرعية لـ Windows (LOLBAS)
   - تكوين محفزات الخدمة
   - اعتبارات العمليات المحمية (PPL)

5. **تكامل التصعيد إلى الامتيازات:**
   - متطلبات SERVICE_ALL_ACCESS
   - استغلال مسار الخدمة غير المقتبس
   - استغلال أذونات الخدمة الضعيفة
   - ضعف ACL لسجل الخدمة
   - التلاعب بالرمز لإنشاء الخدمة

6. **الكشف والمراقبة:**
   - مراقبة معرّفات الأحداث (7045، 4697، 7040)
   - استعلامات PowerShell للكشف
   - مقارنة خط الأساس للخدمات
   - مراقبة Sysmon لإنشاء الخدمات
   - قواعد Sigma واستعلامات SIEM

7. **استراتيجيات التخفيف:**
   - تدقيق أذونات الخدمات
   - القائمة البيضاء للتطبيقات
   - تكوينات تقوية الخدمات
   - مراقبة إنشاء الخدمات المميزة

8. **مرجع MITRE ATT&CK:**
   - T1543.003: إنشاء أو تعديل عملية النظام: خدمة Windows
   - T1574.011: اختطاف تدفق التنفيذ: ضعف أذونات سجل الخدمات

أمثلة هجوم عملية وقواعد كشف كاملة وتوصيات دفاعية.
```

---

## Example Output Preview

```
# Windows Service Persistence Analysis

## 1. Basic Service Creation
```cmd
sc.exe create "SecurityUpdateService" binPath= "C:\ProgramData\update.exe" start= auto DisplayName= "Security Update Service"
sc.exe description "SecurityUpdateService" "Provides security updates for Windows components."
sc.exe start "SecurityUpdateService"
```

## 2. PowerShell Service Creation
```powershell
New-Service -Name "SecurityMaintenance" -BinaryPathName "C:\temp\payload.exe" -DisplayName "Security Maintenance" -StartupType Automatic
```

## 3. Service Recovery Configuration
```cmd
sc.exe failure "SecurityUpdateService" reset= 86400 actions= restart/5000/restart/5000/run/5000
sc.exe failureflag "SecurityUpdateService" 1
```

## 4. Detection - PowerShell Query
```powershell
Get-CimInstance -ClassName Win32_Service | Where-Object {
    $_.PathName -notmatch "C:\\Windows\\System32" -and 
    $_.PathName -notmatch "C:\\Program Files"
} | Select-Object Name, PathName, StartMode
```

## 5. Sigma Detection Rule
```yaml
title: Suspicious Service Creation
status: experimental
logsource:
  product: windows
  service: system
detection:
  selection:
    EventID: 7045
    ServiceFileName|contains:
      - 'cmd.exe'
      - 'powershell'
      - 'wscript'
      - 'mshta'
      - 'regsvr32'
  condition: selection
fields:
  - ServiceName
  - ServiceFileName
  - ServiceType
```
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 5: DLL Search Order Hijacking

### Description
A technical prompt for understanding DLL Search Order Hijacking as a persistence and privilege escalation technique, covering exploitation methods, vulnerable applications, and detection strategies.

### Tags
`persistence` `dll-hijacking` `privilege-escalation` `red-team` `T1574`

---

## 🇬🇧 English Prompt

```
You are a senior red team operator and malware analyst specializing in DLL hijacking techniques. Provide an exhaustive technical analysis of DLL Search Order Hijacking for persistence.

Comprehensively cover the following areas:

1. **DLL Search Order Fundamentals:**
   - Windows DLL search sequence
   - KnownDLLs registry key
   - SafeDllSearchMode impact
   - Application directory priority
   - Side-by-side (SxS) manifest considerations

2. **Types of DLL Hijacking:**
   - DLL Search Order Hijacking
   - DLL Side-loading (phantom DLL)
   - DLL Planting/Preloading
   - DLL Proxying (forwarding exports)
   - COM DLL hijacking

3. **Technical Implementation:**
   - Identifying vulnerable applications (Process Monitor usage)
   - Creating proxy DLLs with forwarded exports
   - DLL export table manipulation
   - Reflective DLL injection basics
   - Tools: Koppelinging, SharpDllProxy, Spartan

4. **Persistence Opportunities:**
   - Targeting system startup applications
   - Service executable DLL hijacking
   - Scheduled task binary hijacking
   - Browser extension DLL hijacking
   - Common vulnerable applications list

5. **Attack Chain Integration:**
   - Initial access via DLL planting
   - Privilege escalation scenarios
   - Lateral movement considerations
   - Combining with other persistence mechanisms

6. **Proxy DLL Development:**
   - Creating forwarding exports
   - Maintaining original functionality
   - Cross-architecture considerations (x86/x64)
   - Handling different calling conventions

7. **Detection & Hunting:**
   - Process Monitor analysis techniques
   - Event ID monitoring (7, 8, 9 - Sysmon)
   - Image File Execution Options monitoring
   - DLL signature verification
   - Baselining application DLL loads

8. **Mitigation Strategies:**
   - Application hardening
   - DLL signature enforcement
   - SafeDllSearchMode configuration
   - Application whitelisting (AppLocker/WDAC)

9. **MITRE ATT&CK Mapping:**
   - T1574.001: Hijack Execution Flow: DLL Search Order Hijacking
   - T1574.002: Hijack Execution Flow: DLL Side-Loading

Provide practical examples, proxy DLL code snippets, and comprehensive detection methodologies.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت خبير متقدم في فريق الهجوم الأحمر ومحلل برمجيات خبيثة متخصص في تقنيات اختطاف DLL. قدم تحليلاً تقنياً شاملاً لاختيطاف ترتيب بحث DLL للثبات.

قم بتغطية المجالات الشاملة التالية:

1. **أساسيات ترتيب بحث DLL:**
   - تسلسل بحث Windows عن DLL
   - مفتاح سجل KnownDLLs
   - تأثير SafeDllSearchMode
   - أولوية دليل التطبيق
   - اعتبارات بيان SxS (Side-by-side)

2. **أنواع اختطاف DLL:**
   - اختطاف ترتيب بحث DLL
   - التحميل الجانبي لـ DLL (DLL الوهمي)
   - زرع/تحميل مسبق لـ DLL
   - وكالة DLL (إعادة توجيه الصادرات)
   - اختطاف DLL لـ COM

3. **التنفيذ التقني:**
   - تحديد التطبيقات الضعيفة (استخدام Process Monitor)
   - إنشاء DLLs وكيلة مع الصادرات المُعادة توجيهها
   - التلاعب بجدول تصدير DLL
   - أساسيات حقن DLL الانعكاسي
   - الأدوات: Koppelinging، SharpDllProxy، Spartan

4. **فرص الثبات:**
   - استهداف تطبيقات بدء تشغيل النظام
   - اختطاف DLL للملفات التنفيذية للخدمات
   - اختطاف الملف التنفيذي للمهام المجدولة
   - اختطاف DLL لإضافات المتصفح
   - قائمة التطبيقات الضعيفة الشائعة

5. **تكامل سلسلة الهجوم:**
   - الوصول الأولي عبر زرع DLL
   - سيناريوهات التصعيد إلى الامتيازات
   - اعتبارات الحركة الجانبية
   - الجمع مع آليات الثبات الأخرى

6. **تطوير DLL الوكيل:**
   - إنشاء الصادرات المُعادة توجيهها
   - الحفاظ على الوظائف الأصلية
   - اعتبارات البنية المتقاطعة (x86/x64)
   - التعامل مع اصطلاحات الاستدعاء المختلفة

7. **الكشف والبحث:**
   - تقنيات تحليل Process Monitor
   - مراقبة معرّفات الأحداث (7، 8، 9 - Sysmon)
   - مراقبة خيارات تنفيذ ملف الصورة
   - التحقق من توقيع DLL
   - إنشاء خط أساس لتحميلات DLL للتطبيقات

8. **استراتيجيات التخفيف:**
   - تقوية التطبيقات
   - إنفاذ توقيع DLL
   - تكوين SafeDllSearchMode
   - القائمة البيضاء للتطبيقات (AppLocker/WDAC)

9. **ربط إطار MITRE ATT&CK:**
   - T1574.001: اختطاف تدفق التنفيذ: اختطاف ترتيب بحث DLL
   - T1574.002: اختطاف تدفق التنفيذ: التحميل الجانبي لـ DLL

أمثلة عملية ومقتطفات كود DLL وكيل ومنهجيات كشف شاملة.
```

---

## Example Output Preview

```
# DLL Search Order Hijacking Analysis

## 1. Windows DLL Search Order
```
1. Application directory
2. System directory (C:\Windows\System32)
3. 16-bit system directory (C:\Windows\System)
4. Windows directory (C:\Windows)
5. Current directory
6. Directories in PATH environment variable
```

## 2. Identifying Vulnerable Applications
```
Process Monitor Filter:
- Operation is CreateFile
- Path ends with .dll
- Result is NAME NOT FOUND
```

## 3. Proxy DLL Creation (C++)
```cpp
// Forward exports to legitimate DLL
#pragma comment(linker, "/export:OriginalFunction=legitimate.OriginalFunction")

BOOL APIENTRY DllMain(HMODULE hModule, DWORD ul_reason_for_call, LPVOID lpReserved) {
    switch (ul_reason_for_call) {
        case DLL_PROCESS_ATTACH:
            // Malicious payload execution
            system("C:\\temp\\payload.exe");
            break;
    }
    return TRUE;
}
```

## 4. SharpDllProxy Usage
```powershell
# Generate proxy DLL
SharpDllProxy.exe --dll legitimate.dll --payload shellcode.bin

# Output: proxy DLL with forwarded exports
```

## 5. Common Vulnerable Applications
| Application | Vulnerable DLL | Context |
|-------------|----------------|---------|
| explorer.exe | OneDriveCore.dll | User login |
| svchost.exe | Various | Service start |
| outlook.exe | mso.dll | Application start |

## 6. Detection - Sysmon Event ID 7
```xml
<Sysmon schemaversion="4.82">
  <EventFiltering>
    <ImageLoad onmatch="exclude">
      <Rule groupRelation="and">
        <Image condition="contains">suspicious_app.exe</Image>
        <ImageLoaded condition="contains">user_writable_path</ImageLoaded>
      </Rule>
    </ImageLoad>
  </EventFiltering>
</Sysmon>
```

## 7. Sigma Detection Rule
```yaml
title: DLL Loaded from Suspicious Location
status: experimental
logsource:
  category: image_load
  product: windows
detection:
  selection:
    ImageLoaded|contains:
      - '\Users\'
      - '\AppData\'
      - '\Temp\'
    Signed: 'false'
  condition: selection
```
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## References & Resources

### MITRE ATT&CK Techniques Covered
| Technique ID | Name |
|--------------|------|
| T1547.001 | Boot or Logon Autostart Execution: Registry Run Keys |
| T1053.005 | Scheduled Task/Job: Scheduled Task |
| T1546.003 | Event Triggered Execution: WMI Event Subscription |
| T1543.003 | Create or Modify System Process: Windows Service |
| T1574.001 | Hijack Execution Flow: DLL Search Order Hijacking |

### Additional Resources
- [MITRE ATT&CK Framework](https://attack.mitre.org/)
- [Atomic Red Team](https://github.com/redcanaryco/atomic-red-team)
- [Sigma Rules Repository](https://github.com/SigmaHQ/sigma)

---

*This document is part of the CyberSec-Prompts-Hub collection for red team operations and defensive security research.*
