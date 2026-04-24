# Threat Detection Methods - Bilingual Prompts

> A comprehensive collection of bilingual (English/Arabic) prompts for threat detection methodologies, SIEM rule development, and security operations.

---

## Prompt 1: SIEM Rule Development

### Description
Develop comprehensive SIEM detection rules for various attack patterns using Splunk, Elastic, and Microsoft Sentinel with correlation logic and alert tuning.

### Tags
`siem` `detection-rules` `splunk` `elastic` `sentinel` `correlation`

---

## 🇬🇧 English Prompt

```
You are a senior SOC analyst specializing in SIEM rule development. Create a comprehensive set of detection rules for the following attack scenario:

**Attack Scenario:** Lateral movement detection in a Windows enterprise environment

**Requirements:**
1. Develop detection rules for the following SIEM platforms:
   - Splunk (SPL syntax)
   - Elastic Security (ES|QL or KQL)
   - Microsoft Sentinel (KQL)

2. For each rule, provide:
   - Rule name and description
   - Detection logic with full query syntax
   - Data source requirements (Windows Event IDs, Sysmon, etc.)
   - False positive rate estimation
   - Tuning recommendations
   - MITRE ATT&CK technique mapping

3. Focus on detecting these lateral movement techniques:
   - PSExec execution
   - WMI remote command execution
   - SMB session enumeration
   - Remote Desktop Protocol (RDP) anomalies
   - Pass-the-Hash attacks

4. Include correlation rules that combine multiple events:
   - Authentication followed by remote execution
   - Service creation with network connections
   - Process lineage analysis

5. Provide alert enrichment recommendations:
   - Threat intelligence integration
   - Asset criticality scoring
   - User risk profiling

**Output Format:**
- Organize by SIEM platform
- Include comments in code explaining logic
- Provide severity classification criteria
- Add runbook recommendations for each alert type
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت محلل SOC أول متخصص في تطوير قواعد SIEM. قم بإنشاء مجموعة شاملة من قواعد الكشف للسيناريو الهجومي التالي:

**سيناريو الهجوم:** كشف الحركة الجانبية في بيئة ويندوز المؤسسية

**المتطلبات:**
1. تطوير قواعد الكشف لمنصات SIEM التالية:
   - Splunk (بصيغة SPL)
   - Elastic Security (بصيغة ES|QL أو KQL)
   - Microsoft Sentinel (بصيغة KQL)

2. لكل قاعدة، قدم:
   - اسم القاعدة ووصفها
   - منطق الكشف مع صيغة الاستعلام الكاملة
   - متطلبات مصادر البيانات (معرفات أحداث ويندوز، Sysmon، إلخ)
   - تقدير معدل الإيجابيات الكاذبة
   - توصيات الضبط الدقيق
   - ربط تقنيات MITRE ATT&CK

3. التركيز على كشف تقنيات الحركة الجانبية التالية:
   - تنفيذ PSExec
   - تنفيذ الأوامر عن بعد عبر WMI
   - تعداد جلسات SMB
   - شذوذ بروتوكول سطح المكتب البعيد (RDP)
   - هجمات تمرير التجزئة (Pass-the-Hash)

4. تضمين قواعد الربط التي تجمع أحداث متعددة:
   - المصادقة متبوعة بالتنفيذ عن بعد
   - إنشاء الخدمة مع الاتصالات الشبكية
   - تحليل تسلسل العمليات

5. تقديم توصيات إثراء التنبيهات:
   - تكامل استخبارات التهديدات
   - تصنيف أهمية الأصول
   - ملف تعريف مخاطر المستخدم

**تنسيق المخرجات:**
- التنظيم حسب منصة SIEM
- تضمين تعليقات في الكود توضح المنطق
- تقديم معايير تصنيف الخطورة
- إضافة توصيات دفتر التشغيل لكل نوع تنبيه
```

---

## Example Output Preview

```
### Splunk Detection Rule - PSExec Execution

```splunk
index=wineventlog (EventCode=4688 OR EventCode=1)
| where (New_ProcessName="*psexec*" OR CommandLine="*psexec*")
| stats count by _time, Computer, User, New_ProcessName, CommandLine
| eval severity=if(count > 5, "high", "medium")
| table _time, Computer, User, New_ProcessName, CommandLine, severity
```

**MITRE ATT&CK:** T1021.002 (Remote Services: SMB/Windows Admin Shares)
**Data Sources:** Windows Security Event 4688, Sysmon Event 1
**False Positive Rate:** Low (tune for legitimate admin tools)

---

### Elastic Security - WMI Remote Execution

```sql
FROM winlogbeat-*
| WHERE winlog.event_id IN (1, 4688)
| WHERE process.command_line LIKE "*wmic*" AND process.command_line LIKE "*node*"
| STATS count = COUNT(*) BY host.name, user.name, process.command_line
```

**MITRE ATT&CK:** T1047 (Windows Management Instrumentation)
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 2: Threat Hunting Methodology

### Description
Establish systematic threat hunting methodologies with hypothesis-driven investigations, data analysis techniques, and hunt documentation frameworks.

### Tags
`threat-hunting` `hypothesis-driven` `investigation` `data-analysis` `methodology`

---

## 🇬🇧 English Prompt

```
You are a threat hunting lead for a Fortune 500 organization. Develop a comprehensive threat hunting program with the following components:

**Part 1: Hunting Hypothesis Framework**
Create 5 detailed hunting hypotheses covering:
- Living-off-the-Land (LotL) binary abuse
- Data exfiltration through covert channels
- Persistence mechanisms in cloud environments
- Insider threat indicators
- Supply chain compromise detection

For each hypothesis provide:
- Hypothesis statement
- Data sources required (with specific log types)
- Analytical techniques to apply
- Expected IOCs and behaviors
- Success metrics

**Part 2: Technical Hunt Procedures**
For each hypothesis, develop:
- Step-by-step hunting procedure
- KQL/SPL queries for investigation
- Statistical analysis methods (anomaly detection, baseline comparison)
- Visualization recommendations
- Pivot points for deeper investigation

**Part 3: Hunt Documentation Template**
Create a standardized format including:
- Executive summary section
- Technical findings
- Detection opportunities identified
- Gap analysis
- Recommendations for SOC improvement

**Part 4: Threat Hunting Maturity Model**
Define 5 levels of hunting maturity with:
- Skill requirements per level
- Tool capabilities needed
- Typical time-to-detection
- ROI metrics

**Deliverable:**
A complete threat hunting playbook with at least 3 full hypothesis investigations documented.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت قائد فريق البحث عن التهديدات في مؤسسة من فورتشين 500. قم بتطوير برنامج شامل للبحث عن التهديدات بالعناصر التالية:

**الجزء 1: إطار فرضيات البحث**
أنشئ 5 فرضيات بحثية مفصلة تغطي:
- إساءة استخدام الثنائيات المحلية (Living-off-the-Land)
- نشر البيانات عبر القنوات الخفية
- آليات الاستمرار في البيئات السحابية
- مؤشرات التهديد الداخلي
- كشف اختراق سلسلة التوريد

لكل فرضية قدم:
- صياغة الفرضية
- مصادر البيانات المطلوبة (مع أنواع السجلات المحددة)
- التقنيات التحليلية المطلوب تطبيقها
- مؤشرات الاختراق والسلوكيات المتوقعة
- مقاييس النجاح

**الجزء 2: إجراءات البحث التقنية**
لكل فرضية، طور:
- إجراء بحث خطوة بخطوة
- استعلامات KQL/SPL للتحقيق
- أساليب التحليل الإحصائي (كشف الشذوذ، مقارنة خط الأساس)
- توصيات التصور البياني
- نقاط التحول للتحقيق الأعمق

**الجزء 3: قالب توثيق عمليات البحث**
أنشئ تنسيقاً معيارياً يتضمن:
- قسم الملخص التنفيذي
- النتائج التقنية
- فرص الكشف المحددة
- تحليل الفجوات
- توصيات لتحسين SOC

**الجزء 4: نموذج نضج البحث عن التهديدات**
حدد 5 مستويات لنضج البحث مع:
- متطلبات المهارات لكل مستوى
- قدرات الأدوات المطلوبة
- الوقت المتوقع للكشف
- مقاييس العائد على الاستثمار

**المخرجات:**
دفتر تشغيل كامل للبحث عن التهديدات مع توثيق 3 فرضيات بحث كاملة على الأقل.
```

---

## Example Output Preview

```
### Hypothesis 1: Living-off-the-Land Binary Abuse

**Hypothesis Statement:**
"Adversaries are using LOLBins (certutil, mshta, regsvr32, etc.) to execute 
malicious code while evading traditional signature-based detection."

**Data Sources Required:**
- Windows Security Events (4688, 4689)
- Sysmon Events (1, 7, 11)
- PowerShell Operational Logs (4104)
- Command-line auditing logs

**Hunting Procedure - Step 1: Baseline LOLBin Usage**
```kql
DeviceProcessEvents
| where FileName in~ ("certutil.exe", "mshta.exe", "regsvr32.exe", 
                       "rundll32.exe", "wmic.exe", "powershell.exe")
| summarize Count=count(), Commands=make_set(ProcessCommandLine) 
  by FileName, DeviceName
| order by Count desc
```

**Analytical Techniques:**
1. Statistical outlier detection (z-score analysis)
2. Command-line pattern analysis
3. Network connection correlation
4. Parent process validation

**Expected Behaviors:**
- Unusual command-line arguments
- Network connections from LOLBins
- Script execution from remote sources
- Registry modifications

**Success Metrics:**
- True positive rate: >70%
- Time to detection: <24 hours
- Coverage: 95% of endpoints
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 3: Behavioral Analytics

### Description
Implement behavioral analytics for user and entity behavior analysis (UEBA), anomaly detection, and insider threat identification using machine learning and statistical methods.

### Tags
`behavioral-analytics` `ueba` `anomaly-detection` `machine-learning` `insider-threat`

---

## 🇬🇧 English Prompt

```
You are a security data scientist implementing behavioral analytics for an enterprise SOC. Design a comprehensive UEBA (User and Entity Behavior Analytics) solution:

**Section 1: Baseline Behavior Modeling**
Develop baselining approaches for:
1. User login patterns (time, location, device)
2. File access behaviors (volume, sensitivity, time)
3. Network activity patterns (destinations, protocols, data volume)
4. Cloud resource utilization patterns
5. Service account activity profiles

For each, provide:
- Data points to collect
- Statistical models to apply (Moving Average, ARIMA, Isolation Forest, etc.)
- Training period requirements
- Threshold calculation methodology

**Section 2: Anomaly Detection Framework**
Create detection logic for:
- Impossible travel detection
- Data exfiltration anomalies
- Privilege escalation behaviors
- After-hours sensitive data access
- Unusual process execution patterns

Include SIEM queries for:
- Splunk (with Machine Learning Toolkit)
- Elastic (with anomaly detection jobs)
- Microsoft Sentinel (with built-in UEBA)

**Section 3: Risk Scoring Model**
Design a multi-factor risk scoring system:
- Risk factors and weights
- Score aggregation methodology
- Dynamic threshold adjustment
- Risk decay algorithms
- Alert prioritization framework

**Section 4: Insider Threat Detection**
Develop specific use cases:
- Departing employee monitoring
- Flight risk indicators
- Data staging detection
- Communication pattern analysis
- Access pattern violations

**Technical Requirements:**
- Include Python code snippets for custom analytics
- Provide sample dashboards configuration
- Document data pipeline requirements
- Include model retraining procedures
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت عالم بيانات أمني تقوم بتطبيق التحليلات السلوكية لمركز عمليات أمن المؤسسات (SOC). صمم حلاً شاملاً لتحليل سلوك المستخدم والكيان (UEBA):

**القسم 1: نمذجة السلوك الأساسي**
طور مناهج التأسيس لـ:
1. أنماط تسجيل دخول المستخدم (الوقت، الموقع، الجهاز)
2. سلوكيات الوصول للملفات (الحجم، الحساسية، الوقت)
3. أنماط النشاط الشبكي (الوجهات، البروتوكولات، حجم البيانات)
4. أنماط استخدام الموارد السحابية
5. ملفات تعريف نشاط حسابات الخدمة

لكل منها، قدم:
- نقاط البيانات المراد جمعها
- النماذج الإحصائية المطلوب تطبيقها (المتوسط المتحرك، ARIMA، غابة العزل، إلخ)
- متطلبات فترة التدريب
- منهجية حساب العتبة

**القسم 2: إطار كشف الشذوذ**
أنشئ منطق الكشف لـ:
- كشف السفر المستحيل
- شذوذ نشر البيانات
- سلوكيات تصعيد الصلاحيات
- الوصول للبيانات الحساسة بعد ساعات العمل
- أنماط تنفيذ العمليات غير المعتادة

تضمين استعلامات SIEM لـ:
- Splunk (مع مجموعة أدوات التعلم الآلي)
- Elastic (مع مهام كشف الشذوذ)
- Microsoft Sentinel (مع UEBA المدمج)

**القسم 3: نموذج تقييم المخاطر**
صمم نظام تقييم مخاطر متعدد العوامل:
- عوامل الخطر والأوزان
- منهجية تجميع الدرجات
- الضبط الديناميكي للعتبات
- خوارزميات اضمحلال المخاطر
- إطار أولوية التنبيهات

**القسم 4: كشف التهديد الداخلي**
طور حالات استخدام محددة:
- مراقبة الموظفين المغادرين
- مؤشرات خطر الهروب
- كشف تجهيز البيانات
- تحليل أنماط الاتصال
- انتهاكات أنماط الوصول

**المتطلبات التقنية:**
- تضمين مقتطفات كود Python للتحليلات المخصصة
- تقديم تكوين لوحات المعلومات النموذجية
- توثيق متطلبات خط أنابيب البيانات
- تضمين إجراءات إعادة تدريب النموذج
```

---

## Example Output Preview

```
### User Login Baseline Modeling

**Statistical Model: Weighted Moving Average with Standard Deviation Bands**

```python
import pandas as pd
import numpy as np
from sklearn.ensemble import IsolationForest

def calculate_login_baseline(login_data, user_id, window_days=30):
    """
    Calculate baseline login patterns for a user
    
    Args:
        login_data: DataFrame with columns [timestamp, user_id, location, device]
        user_id: Target user for analysis
        window_days: Historical window for baseline calculation
    """
    user_logins = login_data[login_data['user_id'] == user_id]
    
    # Time-based features
    user_logins['hour'] = user_logins['timestamp'].dt.hour
    user_logins['day_of_week'] = user_logins['timestamp'].dt.dayofweek
    
    # Calculate statistical baseline
    baseline = {
        'avg_logins_per_day': user_logins.groupby(user_logins['timestamp'].dt.date).size().mean(),
        'std_logins_per_day': user_logins.groupby(user_logins['timestamp'].dt.date).size().std(),
        'typical_hours': user_logins['hour'].mode().tolist(),
        'typical_locations': user_logins['location'].mode().tolist(),
        'typical_devices': user_logins['device'].mode().tolist()
    }
    
    return baseline

def detect_anomalous_login(current_login, baseline, threshold=2.5):
    """
    Detect anomalous login using z-score analysis
    """
    anomalies = []
    
    # Check time anomaly
    if current_login['hour'] not in baseline['typical_hours']:
        anomalies.append(('time', 'high'))
    
    # Check location anomaly
    if current_login['location'] not in baseline['typical_locations']:
        anomalies.append(('location', 'critical'))
    
    return anomalies
```

---

### Splunk MLTK - Impossible Travel Detection

```splunk
| tstats count from datamodel=Authentication 
  where Authentication.action=success 
  by Authentication.user, Authentication.src, _time
| table _time, Authentication.user, Authentication.src
| streamstats window=2 current=f last(Authentication.src) as prev_src 
    last(_time) as prev_time by Authentication.user
| eval time_diff = _time - prev_time
| eval distance_km = geo_distance(src_lat, src_lon, prev_lat, prev_lon)
| eval speed_kmh = (distance_km / (time_diff / 3600))
| where speed_kmh > 800
| table _time, Authentication.user, Authentication.src, prev_src, speed_kmh
```

**Risk Score Calculation:**
| Factor | Weight | Trigger Condition |
|--------|--------|-------------------|
| Impossible Travel | 30 | Speed > 800 km/h |
| Unusual Time | 15 | Outside ±2 std hours |
| New Location | 20 | Never seen country |
| New Device | 25 | Unknown device ID |
| Failed Logins | 10 | >5 failures before success |
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 4: MITRE ATT&CK Mapping

### Description
Map security events, alerts, and detections to the MITRE ATT&CK framework with technique identification, coverage analysis, and detection engineering recommendations.

### Tags
`mitre-attack` `framework-mapping` `technique-identification` `coverage-analysis` `detection-engineering`

---

## 🇬🇧 English Prompt

```
You are a MITRE ATT&CK framework specialist working with an enterprise security team. Perform comprehensive ATT&CK mapping and analysis:

**Task 1: Event-to-Technique Mapping**
Map the following security events to MITRE ATT&CK techniques:

Event Category 1: Windows Security Events
- Event 4624 (Successful logon) with logon type variations
- Event 4688 (Process creation) with command-line analysis
- Event 4672 (Special privileges assigned)
- Event 4720 (User account created)
- Event 4728/4732/4756 (Group membership changes)

Event Category 2: Sysmon Events
- Event 1 (Process creation)
- Event 3 (Network connection)
- Event 7 (Image loaded)
- Event 11 (File created)
- Event 13 (Registry value set)

Event Category 3: Cloud Security Events
- AWS CloudTrail API calls
- Azure AD sign-in logs
- Microsoft 365 audit logs
- GCP Admin Activity logs

**Task 2: Detection Coverage Analysis**
Create a coverage matrix showing:
- Current detection capability per technique
- Data source availability assessment
- Gap identification and prioritization
- Recommended additional data sources

**Task 3: Technique-Specific Detection Rules**
Develop detection rules for high-priority techniques:
- T1059.001 (PowerShell)
- T1566.001 (Spearphishing Attachment)
- T1078 (Valid Accounts)
- T1486 (Data Encrypted for Impact)
- T1071.001 (Web Protocols C2)

For each technique provide:
- Attack chain analysis
- Detection opportunities at each phase
- SIEM detection rules (Splunk, Elastic, Sentinel)
- False positive mitigation strategies

**Task 4: Threat Intelligence Integration**
Show how to:
- Map threat actor TTPs to ATT&CK
- Create actor-specific detection rules
- Prioritize detections based on threat landscape
- Track technique evolution over time

**Output Format:**
Provide a structured ATT&CK Navigator layer file and detailed markdown documentation.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت متخصص في إطار عمل MITRE ATT&CK تعمل مع فريق أمن مؤسسي. قم بإجراء تحليل شامل لربط ATT&CK:

**المهمة 1: ربط الأحداث بالتقنيات**
اربط أحداث الأمان التالية بتقنيات MITRE ATT&CK:

فئة الأحداث 1: أحداث أمان ويندوز
- الحدث 4624 (تسجيل دخول ناجح) مع أنواع تسجيل الدخول المختلفة
- الحدث 4688 (إنشاء عملية) مع تحليل سطر الأوامر
- الحدث 4672 (تعيين صلاحيات خاصة)
- الحدث 4720 (إنشاء حساب مستخدم)
- الأحداث 4728/4732/4756 (تغييرات عضوية المجموعة)

فئة الأحداث 2: أحداث Sysmon
- الحدث 1 (إنشاء عملية)
- الحدث 3 (اتصال شبكي)
- الحدث 7 (تحميل الصورة/المكتبة)
- الحدث 11 (إنشاء ملف)
- الحدث 13 (تعيين قيمة السجل)

فئة الأحداث 3: أحداث الأمان السحابي
- استدعاءات AWS CloudTrail API
- سجلات تسجيل الدخول Azure AD
- سجلات تدقيق Microsoft 365
- سجلات نشاط المسؤول GCP

**المهمة 2: تحليل تغطية الكشف**
أنشئ مصفوفة تغطية تُظهر:
- قدرة الكشف الحالية لكل تقنية
- تقييم توفر مصادر البيانات
- تحديد الفجوات وأولوياتها
- مصادر البيانات الإضافية الموصى بها

**المهمة 3: قواعد الكشف الخاصة بالتقنيات**
طور قواعد كشف للتقنيات ذات الأولوية العالية:
- T1059.001 (PowerShell)
- T1566.001 (مرفق التصيد المستهدف)
- T1078 (حسابات صالحة)
- T1486 (تشفير البيانات للتأثير)
- T1071.001 (بروتوكولات الويب للقيادة والسيطرة)

لكل تقنية قدم:
- تحليل سلسلة الهجوم
- فرص الكشف في كل مرحلة
- قواعد كشف SIEM (Splunk, Elastic, Sentinel)
- استراتيجيات التخفيف من الإيجابيات الكاذبة

**المهمة 4: تكامل استخبارات التهديدات**
أظهر كيفية:
- ربط تكتيكات وتقنيات ومهارات المهاجمين بـ ATT&CK
- إنشاء قواعد كشف خاصة بكل جهة تهديد
- تحديد أولويات الكشف بناءً على مشهد التهديدات
- تتبع تطور التقنيات بمرور الوقت

**تنسيق المخرجات:**
قدم ملف طبقة ATT&CK Navigator منظم ووثائق markdown مفصلة.
```

---

## Example Output Preview

```
### Event-to-Technique Mapping Matrix

| Event Source | Event ID | ATT&CK Technique | Technique Name | Detection Quality |
|--------------|----------|------------------|----------------|-------------------|
| Windows Security | 4624 Type 2 | T1078 | Valid Accounts | Medium |
| Windows Security | 4624 Type 10 | T1021.001 | RDP | High |
| Windows Security | 4688 | T1059 | Command/Scripting | High |
| Windows Security | 4672 | T1136.001 | Create Account | High |
| Sysmon | 1 | T1059.001 | PowerShell | High |
| Sysmon | 3 | T1071 | Application Layer Protocol | Medium |

---

### Detection Rule - T1059.001 PowerShell

**Splunk Query:**
```splunk
index=sysmon EventCode=1 Image="*powershell.exe"
| eval suspicious=0
| rex field=CommandLine "(?<encoded>-[eE][nN][cC][oO]?[dD]?[eE]?[dD]?[cC]?[oO]?[mM]?[mM]?[aA]?[nN]?[dD]?)"
| eval suspicious=if(isnotnull(encoded), suspicious+1, suspicious)
| eval suspicious=if(match(CommandLine, "(DownloadString|DownloadFile|IEX|Invoke-)"), suspicious+1, suspicious)
| eval suspicious=if(match(CommandLine, "(Bypass|Hidden|ExecutionPolicy)"), suspicious+1, suspicious)
| where suspicious >= 2
| table _time, Computer, User, CommandLine, suspicious
```

**Elastic Query:**
```sql
FROM logs-windows.sysmon-*
| WHERE event.code == 1 AND process.name : "*powershell.exe"
| WHERE process.command_text LIKE ANY (
    "%downloadstring%", "%iex%", "%invoke-%",
    "%-encodedcommand%", "%-enc%", "%bypass%"
  )
| KEEP @timestamp, host.name, user.name, process.command_text
```

**Microsoft Sentinel (KQL):**
```kql
DeviceProcessEvents
| where FileName =~ "powershell.exe"
| where ProcessCommandLine has_any ("DownloadString", "IEX", "Invoke-", 
    "-EncodedCommand", "-enc", "bypass", "Hidden")
| extend SuspicionScore = 
    iif(ProcessCommandLine has "EncodedCommand", 2, 0) +
    iif(ProcessCommandLine has_any ("IEX", "Invoke-"), 2, 0) +
    iif(ProcessCommandLine has_any ("bypass", "Hidden"), 1, 0)
| where SuspicionScore >= 2
| project TimeGenerated, DeviceName, AccountName, ProcessCommandLine, SuspicionScore
```

---

### ATT&CK Navigator Layer (JSON Structure)
```json
{
  "version": "4.5",
  "name": "Detection Coverage",
  "domain": "enterprise-attack",
  "techniques": [
    {
      "techniqueID": "T1059.001",
      "color": "#00FF00",
      "comment": "High coverage - Multiple detection rules active"
    },
    {
      "techniqueID": "T1078",
      "color": "#FFFF00",
      "comment": "Medium coverage - Requires behavioral analytics"
    }
  ]
}
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

## Prompt 5: Indicator of Compromise (IOC) Development

### Description
Create comprehensive Indicators of Compromise (IOCs) including YARA rules, Sigma rules, STIX objects, and detection signatures with validation and lifecycle management.

### Tags
`ioc` `yara` `sigma` `stix` `indicators` `detection-signatures`

---

## 🇬🇧 English Prompt

```
You are a threat intelligence analyst specializing in IOC development and management. Create a comprehensive IOC package for the following threat scenario:

**Threat Scenario:**
A sophisticated APT group is conducting targeted attacks against financial institutions using custom malware with the following characteristics:
- Custom backdoor using HTTPS C2 with domain fronting
- Persistence via scheduled tasks and registry run keys
- Data exfiltration through cloud storage APIs (OneDrive, Google Drive)
- Lateral movement using modified PsExec and WMI
- Anti-analysis techniques including VM detection and sandbox evasion

**Deliverable 1: YARA Rules**
Develop YARA rules that detect:
- Main backdoor binary (provide logic for file characteristics)
- Loader/dropper components
- Persistence mechanism artifacts
- Memory-resident components

Include for each rule:
- Rule metadata (author, date, reference, hash examples)
- String patterns (with regex where appropriate)
- Condition logic with false positive handling
- Tuning recommendations

**Deliverable 2: Sigma Rules**
Create Sigma rules for detection across SIEM platforms:
- Process execution patterns
- Network connection characteristics
- Registry modifications
- Scheduled task creation
- File system artifacts

Convert Sigma rules to:
- Splunk SPL
- Elastic KQL
- Microsoft Sentinel KQL
- QRadar AQL

**Deliverable 3: STIX 2.1 Objects**
Create structured threat intelligence objects:
- Indicator objects (file hashes, domains, IPs, URLs)
- Malware objects with relationship mappings
- Attack Pattern objects (MITRE ATT&CK mapping)
- Intrusion Set objects for the APT group
- Relationship objects linking all components

**Deliverable 4: IOC Lifecycle Management**
Document:
- IOC validation procedures
- Confidence scoring methodology
- Expiration and rotation policies
- False positive feedback loop
- Integration with threat intelligence platforms (TIP)

**Deliverable 5: Network Detection Rules**
Create Snort/Suricata rules for:
- C2 communication patterns
- DNS query patterns
- SSL/TLS certificate anomalies
- Data exfiltration signatures

**Technical Standards:**
- Follow STIX 2.1 specification
- Use Sigma specification 2.0
- Include YARA rule validation commands
- Provide OpenCTI/MISP import formats
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت محلل استخبارات تهديدات متخصص في تطوير وإدارة مؤشرات الاختراق (IOCs). أنشئ حزمة IOC شاملة لسيناريو التهديد التالي:

**سيناريو التهديد:**
مجموعة APT متطورة تقوم بإجراء هجمات مستهدفة ضد المؤسسات المالية باستخدام برمجيات خبيثة مخصصة بالخصائص التالية:
- باب خلفي مخصص يستخدم C2 عبر HTTPS مع تمويه النطاق (Domain Fronting)
- الاستمرار عبر المهام المجدولة ومفاتيح تشغيل السجل
- نشر البيانات عبر واجهات برمجة التخزين السحابي (OneDrive, Google Drive)
- الحركة الجانبية باستخدام PsExec و WMI المعدلين
- تقنيات مكافحة التحليل تشمل كشف الآلات الافتراضية وتجاوز الصندوق الرملي

**المخرج 1: قواعد YARA**
طور قواعد YARA تكشف عن:
- الثنائي الرئيسي للباب الخلفي (قدم المنطق لخصائص الملف)
- مكونات المحمل/المسقط
- آثار آليات الاستمرار
- المكونات المقيمة في الذاكرة

تضمين لكل قاعدة:
- بيانات القاعدة الوصفية (المؤلف، التاريخ، المرجع، أمثلة التجزئة)
- أنماط النصوص (مع التعبيرات النمطية حيثما يكون ذلك مناسباً)
- منطق الشرط مع التعامل مع الإيجابيات الكاذبة
- توصيات الضبط الدقيق

**المخرج 2: قواعد Sigma**
أنشئ قواعد Sigma للكشف عبر منصات SIEM:
- أنماط تنفيذ العمليات
- خصائص الاتصال الشبكي
- تعديلات السجل
- إنشاء المهام المجدولة
- آثار نظام الملفات

حول قواعد Sigma إلى:
- Splunk SPL
- Elastic KQL
- Microsoft Sentinel KQL
- QRadar AQL

**المخرج 3: كائنات STIX 2.1**
أنشئ كائنات استخبارات تهديدات منظمة:
- كائنات المؤشر (تجزئات الملفات، النطاقات، IPs، عناوين URL)
- كائنات البرمجيات الخبيثة مع خرائط العلاقات
- كائنات نمط الهجوم (ربط MITRE ATT&CK)
- كائنات مجموعة الاختراق لمجموعة APT
- كائنات العلاقة التي تربط جميع المكونات

**المخرج 4: إدارة دورة حياة IOC**
وثّق:
- إجراءات التحقق من IOC
- منهجية تقييم الثقة
- سياسات انتهاء الصلاحية والتبديل
- حلقة التغذية الراجعة للإيجابيات الكاذبة
- التكامل مع منصات استخبارات التهديدات (TIP)

**المخرج 5: قواعد الكشف الشبكي**
أنشئ قواعد Snort/Suricata لـ:
- أنماط اتصالات C2
- أنماط استعلام DNS
- شذوذ شهادات SSL/TLS
- توقيعات نشر البيانات

**المعايير التقنية:**
- اتبع مواصفات STIX 2.1
- استخدم مواصفات Sigma 2.0
- تضمين أوامر التحقق من قواعد YARA
- تقديم تنسيقات استيراد OpenCTI/MISP
```

---

## Example Output Preview

```
### YARA Rule - Custom Backdoor Detection

```yara
rule APT_Financial_Backdoor : APT Backdoor Financial
{
    meta:
        author = "Threat Intel Team"
        date = "2024-01-15"
        version = "1.2"
        reference = "https://ti-platform/campaign/financial-apt-2024"
        hash = "a1b2c3d4e5f67890abcdef1234567890"
        tlp = "AMBER"
        confidence = "HIGH"
        
    strings:
        // C2 Configuration Pattern
        $c2_pattern = { 68 74 74 70 73 3A 2F 2F [10-50] 2F 61 70 69 2F 76 31 }
        
        // Domain Fronting Indicators
        $domain_front = /fronting\.[a-z]{4,10}\.(com|net|org)/ wide
        
        // API Key Pattern
        $api_key = /Bearer [A-Za-z0-9_-]{30,50}/
        
        // VM Detection Strings
        $vm_detect1 = "VMware" nocase
        $vm_detect2 = "VirtualBox" nocase
        $vm_detect3 = "sandbox" nocase
        $vm_detect4 = "analysis" nocase
        
        // Encoded Configuration
        $config_b64 = /config=[A-Za-z0-9+\/]{40,}={0,2}/
        
        // Mutex for singleton execution
        $mutex = "Global\\FinancialAPT_Mutex_2024" wide
        
    condition:
        uint16(0) == 0x5A4D and (
            (2 of ($vm_detect*) and 1 of ($c2_pattern, $domain_front, $api_key)) or
            ($mutex and 1 of ($c2_pattern, $config_b64)) or
            (3 of ($vm_detect*, $c2_pattern, $domain_front, $api_key, $config_b64))
        ) and filesize < 5MB
}
```

---

### Sigma Rule - Scheduled Task Persistence

```yaml
title: Suspicious Scheduled Task Creation by Unknown Process
id: a1b2c3d4-5678-90ab-cdef-1234567890ab
status: stable
description: Detects creation of scheduled tasks by unusual processes, 
  indicating potential persistence mechanism
references:
    - https://attack.mitre.org/techniques/T1053/005/
author: Threat Intel Team
date: 2024/01/15
tags:
    - attack.persistence
    - attack.t1053.005
logsource:
    category: process_creation
    product: windows
detection:
    selection:
        Image|endswith: 
            - '\schtasks.exe'
            - '\taskschd.msc'
        CommandLine|contains:
            - '/create'
            - '-create'
    filter_legitimate:
        ParentImage|endswith:
            - '\explorer.exe'
            - '\mmc.exe'
            - '\svchost.exe'
    condition: selection and not filter_legitimate
fields:
    - Image
    - CommandLine
    - ParentImage
    - User
falsepositives:
    - Legitimate administrative scripts
    - Software installation processes
level: medium
```

**Splunk Conversion:**
```splunk
index=wineventlog EventCode=4688 
  (New_ProcessName="*schtasks.exe" OR New_ProcessName="*taskschd.msc")
  CommandLine="*create*"
  NOT (ParentProcessName="*explorer.exe" OR ParentProcessName="*mmc.exe" OR ParentProcessName="*svchost.exe")
| table _time, Computer, User, New_ProcessName, CommandLine, ParentProcessName
```

---

### STIX 2.1 Indicator Objects

```json
{
  "type": "bundle",
  "id": "bundle--a1b2c3d4-5678-90ab-cdef-1234567890ab",
  "objects": [
    {
      "type": "indicator",
      "spec_version": "2.1",
      "id": "indicator--e1f2a3b4-c5d6-7890-abcd-ef1234567890",
      "created": "2024-01-15T10:30:00.000Z",
      "modified": "2024-01-15T10:30:00.000Z",
      "name": "APT Financial Backdoor Hash",
      "description": "SHA256 hash of custom backdoor used in financial sector attacks",
      "indicator_types": ["malicious-activity"],
      "pattern": "[file:hashes.'SHA-256' = 'a1b2c3d4e5f67890abcdef1234567890abcdef1234567890abcdef1234567890']",
      "pattern_type": "stix",
      "valid_from": "2024-01-15T10:30:00.000Z",
      "kill_chain_phases": [
        {
          "kill_chain_name": "mitre-attack",
          "phase_name": "execution"
        }
      ]
    },
    {
      "type": "indicator",
      "spec_version": "2.1",
      "id": "indicator--f2g3h4i5-j6k7-8901-bcde-f23456789012",
      "created": "2024-01-15T10:35:00.000Z",
      "modified": "2024-01-15T10:35:00.000Z",
      "name": "APT C2 Domain",
      "description": "Domain fronting C2 domain used by APT group",
      "indicator_types": ["malicious-activity", "attribution"],
      "pattern": "[domain-name:value = 'fronting.valid-domain.com']",
      "pattern_type": "stix",
      "valid_from": "2024-01-15T10:35:00.000Z"
    }
  ]
}
```

---

### Snort Rule - C2 Detection

```
alert tcp $HOME_NET any -> $EXTERNAL_NET $HTTP_PORTS (msg:"APT Financial C2 Domain Fronting Detected"; flow:to_server,established; content:"Host|3A|"; content:"fronting."; nocase; distance:0; content:"/api/v1"; http_uri; metadata:ruleset custom, service http; reference:url,ti-platform/campaign/financial-apt-2024; classtype:trojan-activity; sid:1000001; rev:1;)
```

---

### IOC Lifecycle Management Framework

| Phase | Action | Timeline | Confidence Threshold |
|-------|--------|----------|---------------------|
| Collection | Gather raw indicators | Immediate | N/A |
| Validation | Test against known FP | 24-48 hrs | >80% |
| Production | Deploy to detection | 48-72 hrs | >90% |
| Monitoring | Track FP rate | Ongoing | <5% FP |
| Expiration | Review and retire | 90-180 days | N/A |
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team
