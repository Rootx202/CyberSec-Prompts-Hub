# Incident Reporting Prompts

A comprehensive collection of bilingual (English/Arabic) prompts for incident documentation and reporting, aligned with NIST SP 800-61 and SANS incident handling guidelines.

---

## Prompt 1: Incident Documentation Template

### Description
Comprehensive incident documentation template for capturing all relevant details during security incident response, ensuring consistency and completeness of incident records.

### Tags
`incident-documentation` `incident-response` `record-keeping` `NIST-800-61`

---

## 🇬🇧 English Prompt

```
You are a security incident handler documenting a security incident. Create a comprehensive incident documentation record for the following incident.

INCIDENT INFORMATION:
[Insert: incident detection details, initial indicators, affected systems, current status, assigned personnel]

Following NIST SP 800-61 and incident handling best practices, provide:

1. **Incident Identification**
   - Unique incident identifier (INC-YYYY-NNNN)
   - Incident detection date and time
   - Date/time of initial compromise (if known)
   - Detection source (SIEM, user report, external notification)
   - Incident reporter and contact information
   - Current incident status (Open/In Progress/Contained/Resolved/Closed)

2. **Incident Classification**
   - Incident category (malware, unauthorized access, DoS, etc.)
   - Incident type and subtype
   - Threat actor classification (if known)
   - Attack vector identification
   - MITRE ATT&CK techniques observed
   - Kill chain phase at detection

3. **Affected Assets Inventory**
   - Systems affected (hostname, IP, OS, function)
   - Network segments impacted
   - Data/systems at risk
   - User accounts potentially compromised
   - Third-party systems affected
   - Business services impacted

4. **Incident Timeline**
   - Chronological event reconstruction
   - Initial compromise indicators
   - Discovery and detection events
   - Response actions taken with timestamps
   - Current status and next steps

5. **Impact Assessment**
   - Confidentiality impact (data exposed)
   - Integrity impact (data/system modified)
   - Availability impact (service disruption)
   - Business impact (financial, operational, reputational)
   - Regulatory impact (breach notification requirements)

6. **Response Actions Log**
   - Containment actions with timestamps
   - Eradication steps performed
   - Recovery actions initiated
   - Evidence collected and secured
   - Communications sent (internal/external)

7. **Evidence Inventory**
   - Evidence items collected
   - Chain of custody documentation
   - Storage location and access controls
   - Retention requirements

8. **Stakeholder Information**
   - Incident response team members
   - Management notifications
   - Legal/HR involvement
   - External parties notified (customers, regulators, vendors)

Output Format: Structured incident record document with all required fields.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت معالج حوادث أمنية توثق حادثاً أمنياً. أنشئ سجل توثيق حادث شامل للحادث التالي.

معلومات الحادث:
[أدخل: تفاصيل اكتشاف الحادث، المؤشرات الأولية، الأنظمة المتأثرة، الحالة الحالية، الموظفين المعينين]

وفقاً لـ NIST SP 800-61 وأفضل ممارسات معالجة الحوادث، قدم:

1. **تحديد الحادث**
   - معرف الحادث الفريد (INC-YYYY-NNNN)
   - تاريخ ووقت اكتشاف الحادث
   - تاريخ/وقت الاختراق الأولي (إن كان معروفاً)
   - مصدر الاكتشاف (SIEM، تقرير مستخدم، إشعار خارجي)
   - مُبلغ الحادث ومعلومات الاتصال
   - حالة الحادث الحالية (مفتوح/قيد التقدم/محتوم/محلول/مغلق)

2. **تصنيف الحادث**
   - فئة الحادث (برمجيات خبيثة، وصول غير مصرح، حرمان من الخدمة، إلخ)
   - نوع الحادث والنوع الفرعي
   - تصنيف الفاعل المهدد (إن كان معروفاً)
   - تحديد متجه الهجوم
   - تقنيات MITRE ATT&CK المُلاحظة
   - مرحلة سلسلة القتل عند الاكتشاف

3. **جرد الأصول المتأثرة**
   - الأنظمة المتأثرة (اسم المضيف، IP، نظام التشغيل، الوظيفة)
   - مقاطع الشبكة المتأثرة
   - البيانات/الأنظمة المعرضة للخطر
   - حسابات المستخدمين المنتهكة المحتملة
   - أنظمة الطرف الثالث المتأثرة
   - خدمات الأعمال المتأثرة

4. **الجدول الزمني للحادث**
   - إعادة بناء الأحداث الزمنية
   - مؤشرات الاختراق الأولي
   - أحداث الاكتشاف والكشف
   - إجراءات الاستجابة المتخذة مع الطوابع الزمنية
   - الحالة الحالية والخطوات التالية

5. **تقييم التأثير**
   - تأثير السرية (البيانات المكشوفة)
   - تأثير النزاهة (البيانات/النظام المعدل)
   - تأثير التوفر (تعطيل الخدمة)
   - تأثير الأعمال (مالي، تشغيلي، سمعة)
   - التأثير التنظيمي (متطلبات إشعار الخرق)

6. **سجل إجراءات الاستجابة**
   - إجراءات الاحتواء مع الطوابع الزمنية
   - خطوات الاستئصال المنفذة
   - إجراءات الاستعادة المبدوءة
   - الأدلة المجمعة والمؤمنة
   - الاتصالات المرسلة (داخلية/خارجية)

7. **جرد الأدلة**
   - عناصر الأدلة المجمعة
   - توثيق سلسلة الحيازة
   - موقع التخزين وضوابط الوصول
   - متطلبات الاحتفاظ

8. **معلومات أصحاب المصلحة**
   - أعضاء فريق الاستجابة للحوادث
   - إشعارات الإدارة
   - مشاركة القانون/الموارد البشرية
   - الأطراف الخارجية المُعلمة (العملاء، المنظمون، البائعون)

تنسيق المخرجات: وثيقة سجل حادث منظمة مع جميع الحقول المطلوبة.
```

---

## Example Output Preview

```
═══════════════════════════════════════════════════════
 INCIDENT DOCUMENTATION RECORD | سجل توثيق الحادث
═══════════════════════════════════════════════════════

┌─────────────────────────────────────────────────────┐
│ INCIDENT IDENTIFICATION                              │
├─────────────────────────────────────────────────────┤
│ Incident ID:        INC-2024-0892                   │
│ Detection Date:     March 15, 2024 14:23 UTC        │
│ Compromise Date:    March 14, 2024 (estimated)      │
│ Detection Source:   SIEM Alert - Behavioral Anomaly │
│ Reporter:           SOC Analyst - Ahmed Hassan      │
│ Status:             🔴 IN PROGRESS - Containment    │
└─────────────────────────────────────────────────────┘

INCIDENT CLASSIFICATION:
┌─────────────────────────────────────────────────────┐
│ Category:           Ransomware Attack               │
│ Type:              Encryption Ransomware            │
│ Threat Actor:      Unknown (under investigation)    │
│ Attack Vector:     Phishing Email → Macro Download  │
│ MITRE ATT&CK:      T1566.001, T1059, T1486         │
│ Kill Chain Phase:  Actions on Objectives            │
└─────────────────────────────────────────────────────┘

AFFECTED ASSETS:
┌────────────┬─────────────────┬──────────────────────┐
│ Hostname   │ IP Address      │ Impact               │
├────────────┼─────────────────┼──────────────────────┤
│ WS-FIN-01  │ 192.168.1.50    │ Encrypted - Offline  │
│ WS-FIN-02  │ 192.168.1.51    │ Encrypted - Offline  │
│ FS-SHARE-01│ 192.168.1.100   │ Shares encrypted     │
│ DB-FIN-01  │ 192.168.1.200   │ Database encrypted   │
└────────────┴─────────────────┴──────────────────────┘

IMPACT ASSESSMENT:
┌─────────────────────────────────────────────────────┐
│ Confidentiality: HIGH - Financial data accessed     │
│ Integrity:        CRITICAL - Data encrypted         │
│ Availability:     HIGH - Services unavailable       │
│ Business Impact:  $250K/day estimated loss          │
│ Regulatory:       GDPR breach notification required │
└─────────────────────────────────────────────────────┘
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 2: Incident Timeline Creation

### Description
Systematic incident timeline creation methodology for reconstructing events, establishing causality, and understanding the complete picture of a security incident.

### Tags
`incident-timeline` `event-reconstruction` `forensic-analysis` `chronological-analysis`

---

## 🇬🇧 English Prompt

```
You are a security analyst tasked with creating a comprehensive incident timeline. Develop a detailed chronological reconstruction of events for the following security incident.

INCIDENT DATA:
[Insert: available logs, timestamps, system artifacts, witness reports, detection alerts, IOCs]

LOG SOURCES AVAILABLE:
[Insert: SIEM logs, endpoint logs, network captures, email logs, authentication logs, application logs]

Following forensic analysis best practices, provide:

1. **Timeline Methodology**
   - Data sources and their reliability rating
   - Time zone standardization approach
   - Clock synchronization verification
   - Gap identification methodology

2. **Pre-Incident Phase (Reconnaissance/Initial Access)**
   - First observed malicious activity
   - Reconnaissance events detected
   - Initial access attempt indicators
   - Phishing or social engineering events
   - Vulnerability exploitation attempts

3. **Compromise Phase**
   - Successful initial compromise timestamp
   - Exploitation events and techniques
   - First malicious code execution
   - Initial persistence establishment
   - Credential theft/acquisition events

4. **Post-Compromise Phase**
   - Privilege escalation events
   - Lateral movement activities
   - Additional system compromises
   - Data collection/staging events
   - Exfiltration indicators

5. **Detection & Response Phase**
   - Alert generation timestamps
   - Investigation activities
   - Containment actions taken
   - Eradication steps performed
   - Recovery initiation

6. **Timeline Visualization**
   - ASCII-based timeline diagram
   - Key events highlighting
   - Duration calculations
   - Dwell time analysis

7. **Critical Events Analysis**
   - Most significant events identified
   - Attack decision points
   - Opportunities for earlier detection
   - Control failures at each phase

8. **Timeline Gaps & Uncertainties**
   - Periods with insufficient data
   - Events with low confidence
   - Assumptions made
   - Additional data needed

Output Format: Comprehensive timeline with UTC timestamps, confidence levels, and evidence references.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت محلل أمني مكلف بإنشاء جدول زمني شامل للحادث. طور إعادة بناء زمنية مفصلة للأحداث للحادث الأمني التالي.

بيانات الحادث:
[أدخل: السجلات المتاحة، الطوابع الزمنية، آثار النظام، تقارير الشهود، تنبيهات الكشف، مؤشرات الاختراق]

مصادر السجلات المتاحة:
[أدخل: سجلات SIEM، سجلات نقاط النهاية، لقطات الشبكة، سجلات البريد الإلكتروني، سجلات المصادقة، سجلات التطبيقات]

وفقاً لأفضل ممارسات التحليل الجنائي، قدم:

1. **منهجية الجدول الزمني**
   - مصادر البيانات وتقييم موثوقيتها
   - نهج توحيد المنطقة الزمنية
   - التحقق من مزامنة الساعة
   - منهجية تحديد الفجوات

2. **مرحلة ما قبل الحادث (الاستطلاع/الوصول الأولي)**
   - أول نشاط خبيث مُلاحظ
   - أحداث الاستطلاع المكتشفة
   - مؤشرات محاولة الوصول الأولي
   - أحداث التصيد الاحتيالي أو الهندسة الاجتماعية
   - محاولات استغلال الثغرات

3. **مرحلة الاختراق**
   - الطابع الزمني للاختراق الأولي الناجح
   - أحداث وتقنيات الاستغلال
   - أول تنفيذ كود خبيث
   - إنشاء الاستمرار الأولي
   - أحداث سرقة/اكتساب بيانات الاعتماد

4. **مرحلة ما بعد الاختراق**
   - أحداث تصعيد الامتيازات
   - أنشطة الحركة الجانبية
   - اختراقات الأنظمة الإضافية
   - أحداث جمع/تحضير البيانات
   - مؤشرات التهريب

5. **مرحلة الكشف والاستجابة**
   - الطوابع الزمنية لتوليد التنبيهات
   - أنشطة التحقيق
   - إجراءات الاحتواء المتخذة
   - خطوات الاستئصال المنفذة
   - بدء الاستعادة

6. **تصور الجدول الزمني**
   - مخطط الجدول الزمني القائم على ASCII
   - إبراز الأحداث الرئيسية
   - حسابات المدة
   - تحليل وقت البقاء

7. **تحليل الأحداث الحرجة**
   - أهم الأحداث المحددة
   - نقاط قرارات الهجوم
   - فرص الكشف المبكر
   - فشل الضوابط في كل مرحلة

8. **فجوات وشكوك الجدول الزمني**
   - فترات عدم كفاية البيانات
   - أحداث بمستوى ثقة منخفض
   - الافتراضات الموضوعة
   - بيانات إضافية مطلوبة

تنسيق المخرجات: جدول زمني شامل مع طوابع زمنية UTC، مستويات الثقة، ومراجع الأدلة.
```

---

## Example Output Preview

```
═══════════════════════════════════════════════════════
 INCIDENT TIMELINE | الجدول الزمني للحادث
═══════════════════════════════════════════════════════

TIMELINE OVERVIEW:
┌─────────────────────────────────────────────────────┐
│ Total Incident Duration: 72 hours 34 minutes        │
│ Dwell Time (Initial Access → Detection): 14h 23m   │
│ Detection to Containment: 2h 45m                    │
│ Containment to Recovery: 55h 26m                   │
└─────────────────────────────────────────────────────┘

CHRONOLOGICAL TIMELINE:
┌─────────────────────────────────────────────────────┐
│ PRE-INCIDENT PHASE                                   │
├─────────────────────────────────────────────────────┤
│ T-18:00  Mar 14, 06:23 UTC                         │
│   [HIGH CONF] Phishing email sent to victim        │
│   Source: Email Gateway Logs                       │
│   Subject: "Urgent: Invoice Review Required"       │
│                                                     │
│ T-14:00  Mar 14, 10:23 UTC                         │
│   [HIGH CONF] Victim opens phishing email          │
│   Source: O365 Audit Logs                          │
│   Action: Clicked link, downloaded macro doc       │
│                                                     │
│ T-13:55  Mar 14, 10:28 UTC                         │
│   [HIGH CONF] Macro execution - malware dropped    │
│   Source: EDR Alert                                │
│   File: C:\Users\victim\AppData\svchost.exe        │
└─────────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────────┐
│ COMPROMISE PHASE                                     │
├─────────────────────────────────────────────────────┤
│ T+0:00   Mar 14, 10:28 UTC - COMPROMISE TIME       │
│   [HIGH CONF] Initial code execution               │
│   Technique: T1059.003 - Windows Command Shell     │
│                                                     │
│ T+0:05   Mar 14, 10:33 UTC                         │
│   [MED CONF] C2 beacon established                 │
│   Source: Network Flow Logs                        │
│   Destination: 185[.]234[.]72[.]91:443            │
│                                                     │
│ T+2:15   Mar 14, 12:43 UTC                         │
│   [HIGH CONF] Credential dumping performed         │
│   Source: EDR Detection                            │
│   Technique: T1003.001 - LSASS access              │
└─────────────────────────────────────────────────────┘

VISUAL TIMELINE:
     Mar 14                Mar 15                Mar 16
  ─────┬─────────────────┬─────────────────┬──────────▶
       │                 │                 │
       ▼ Initial         ▼ Detection       ▼ Recovery
       Compromise        T+14h 23m         T+72h 34m
       │                 │                 │
   [███▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓███▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒]
       │    Lateral     │   Containment   │ Recovery
            Movement         Eradication
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 3: Impact Assessment Report

### Description
Comprehensive impact assessment methodology for quantifying and qualifying the business, operational, and regulatory impact of security incidents.

### Tags
`impact-assessment` `business-impact` `risk-quantification` `regulatory-impact`

---

## 🇬🇧 English Prompt

```
You are a risk analyst conducting an impact assessment for a security incident. Develop a comprehensive impact assessment report for the following incident.

INCIDENT DETAILS:
[Insert: incident type, affected systems, data involved, duration, current status, initial impact estimates]

BUSINESS CONTEXT:
[Insert: industry sector, regulatory requirements, business criticality of affected systems, customer impact]

Following risk assessment best practices and regulatory guidelines, provide:

1. **Executive Impact Summary**
   - Overall severity rating (Critical/High/Medium/Low)
   - Key impact areas identified
   - Immediate business concerns
   - Recommended priority actions

2. **Technical Impact Assessment**
   - CIA Triad Analysis:
     * Confidentiality Impact (data exposure level)
     * Integrity Impact (data/system modification)
     * Availability Impact (service disruption)
   - Systems and infrastructure affected
   - Data sensitivity classification of affected data
   - Technical recovery requirements

3. **Business Impact Assessment**
   - Financial Impact:
     * Direct costs (response, recovery, remediation)
     * Indirect costs (productivity loss, opportunity cost)
     * Projected annual financial impact
   - Operational Impact:
     * Business process disruption
     * Service degradation/outage
     * Supply chain impact
   - Reputational Impact:
     * Customer trust implications
     * Brand damage assessment
     * Market position effects

4. **Regulatory & Compliance Impact**
   - Applicable regulations (GDPR, HIPAA, PCI-DSS, SOX, etc.)
   - Breach notification requirements
   - Potential fines and penalties
   - Regulatory reporting deadlines
   - Audit implications

5. **Data Impact Assessment**
   - Types of data affected (PII, PHI, financial, intellectual property)
   - Number of records/data subjects impacted
   - Data classification levels compromised
   - Data exfiltration likelihood assessment
   - Data recovery potential

6. **Stakeholder Impact**
   - Customer impact and notification needs
   - Employee impact assessment
   - Partner/vendor impact
   - Investor/shareholder considerations

7. **Impact Quantification**
   - Financial impact scoring matrix
   - Risk score calculation methodology
   - Comparable incident benchmarks
   - Insurance coverage implications

8. **Remediation Cost Estimation**
   - Immediate response costs
   - System recovery costs
   - Security improvement costs
   - Legal and compliance costs
   - Total estimated remediation investment

Output Format: Comprehensive impact assessment report with quantified metrics and risk ratings.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت محلل مخاطر تجري تقييم التأثير لحادث أمني. طور تقرير تقييم تأثير شامل للحادث التالي.

تفاصيل الحادث:
[أدخل: نوع الحادث، الأنظمة المتأثرة، البيانات المعنية، المدة، الحالة الحالية، تقديرات التأثير الأولية]

سياق الأعمال:
[أدخل: القطاع الصناعي، المتطلبات التنظيمية، أهمية الأنظمة المتأثرة للأعمال، تأثير العملاء]

وفقاً لأفضل ممارسات تقييم المخاطر والإرشادات التنظيمية، قدم:

1. **ملخص التأثير التنفيذي**
   - تقييم الخطورة العام (حرج/عالي/متوسط/منخفض)
   - مجالات التأثير الرئيسية المحددة
   - المخاوف التجارية الفورية
   - الإجراءات ذات الأولوية الموصى بها

2. **تقييم التأثير التقني**
   - تحليل ثلاثية CIA:
     * تأثير السرية (مستوى كشف البيانات)
     * تأثير النزاهة (تعديل البيانات/النظام)
     * تأثير التوفر (تعطيل الخدمة)
   - الأنظمة والبنية التحتية المتأثرة
   - تصنيف حساسية البيانات المتأثرة
   - متطلبات الاستعادة التقنية

3. **تقييم تأثير الأعمال**
   - التأثير المالي:
     * التكاليف المباشرة (الاستجابة، الاستعادة، المعالجة)
     * التكاليف غير المباشرة (فقدان الإنتاجية، تكلفة الفرصة)
     * التأثير المالي السنوي المتوقع
   - التأثير التشغيلي:
     * تعطيل عمليات الأعمال
     * تدهور/انقطاع الخدمة
     * تأثير سلسلة التوريد
   - التأثير على السمعة:
     * آثار ثقة العملاء
     * تقييم ضرر العلامة التجارية
     * آثار الموقع في السوق

4. **التأثير التنظيمي والامتثال**
   - اللوائح المعمول بها (GDPR، HIPAA، PCI-DSS، SOX، إلخ)
   - متطلبات إشعار الخرق
   - الغرامات والعقوبات المحتملة
   - مواعيد الإبلاغ التنظيمي
   - آثار التدقيق

5. **تقييم تأثير البيانات**
   - أنواع البيانات المتأثرة (PII، PHI، مالية، ملكية فكرية)
   - عدد السجلات/أصحاب البيانات المتأثرين
   - مستويات تصنيف البيانات المنتهكة
   - تقييم احتمالية تهريب البيانات
   - إمكانية استعادة البيانات

6. **تأثير أصحاب المصلحة**
   - تأثير العملاء واحتياجات الإشعار
   - تقييم تأثير الموظفين
   - تأثير الشركاء/البائعين
   - اعتبارات المستثمرين/المساهمين

7. **تحديد كمية التأثير**
   - مصفوفة تسجيل التأثير المالي
   - منهجية حساب درجة المخاطر
   - معايير الحوادث المماثلة
   - آثار تغطية التأمين

8. **تقدير تكلفة المعالجة**
   - تكاليف الاستجابة الفورية
   - تكاليف استعادة الأنظمة
   - تكاليف تحسين الأمان
   - التكاليف القانونية والامتثال
   - إجمالي الاستثمار المقدر للمعالجة

تنسيق المخرجات: تقرير تقييم تأثير شامل مع مقاييس محددة كمياً وتقييمات مخاطر.
```

---

## Example Output Preview

```
═══════════════════════════════════════════════════════
 IMPACT ASSESSMENT REPORT | تقرير تقييم التأثير
═══════════════════════════════════════════════════════

┌─────────────────────────────────────────────────────┐
│ EXECUTIVE IMPACT SUMMARY                             │
├─────────────────────────────────────────────────────┤
│ Overall Severity:  🔴 CRITICAL                      │
│ Incident Type:     Ransomware with Data Exfiltration│
│ Key Impact Areas:  Operations, Financial, Regulatory│
│ Immediate Actions: Containment, Customer Notification│
└─────────────────────────────────────────────────────┘

CIA TRIAD IMPACT:
┌─────────────────────────────────────────────────────┐
│ Confidentiality: 🔴 HIGH                            │
│   - 250,000 customer records potentially exposed   │
│   - Financial data: SSN, account numbers at risk   │
│   - Trade secrets: Product roadmap accessed        │
│                                                     │
│ Integrity:       🔴 CRITICAL                        │
│   - Database encrypted (integrity compromised)     │
│   - Backup integrity under investigation           │
│   - Configuration files modified                   │
│                                                     │
│ Availability:    🟠 HIGH                            │
│   - Core systems offline: 72+ hours                │
│   - Customer portal unavailable                    │
│   - Internal operations degraded                   │
└─────────────────────────────────────────────────────┘

FINANCIAL IMPACT SUMMARY:
┌─────────────────────────────────────────────────────┐
│ Category                    │ Estimated Cost        │
├─────────────────────────────┼───────────────────────┤
│ Response & Recovery         │ $850,000              │
│ Business Interruption       │ $1,200,000            │
│ Legal & Regulatory          │ $500,000 (potential)  │
│ Customer Remediation        │ $350,000              │
│ Security Improvements       │ $600,000              │
│ Reputational Impact         │ $2,000,000 (est.)     │
├─────────────────────────────┼───────────────────────┤
│ TOTAL ESTIMATED IMPACT      │ $5,500,000            │
└─────────────────────────────┴───────────────────────┘

REGULATORY IMPACT:
┌─────────────────────────────────────────────────────┐
│ GDPR:     72-hour notification REQUIRED             │
│           Potential fine: €20M or 4% global revenue│
│ PCI-DSS:  Breach notification to card brands       │
│           Potential fine: $500K-$1M per month      │
│ SOX:      Material incident disclosure required    │
│ SEC:      8-K filing within 4 business days        │
└─────────────────────────────────────────────────────┘
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 4: Regulatory Breach Notification

### Description
Comprehensive regulatory breach notification documentation ensuring compliance with various data protection regulations and timely stakeholder communication.

### Tags
`breach-notification` `regulatory-compliance` `GDPR` `data-protection`

---

## 🇬🇧 English Prompt

```
You are a data protection officer preparing breach notification documentation. Create comprehensive breach notification materials for the following data breach incident.

BREACH DETAILS:
[Insert: breach type, data categories affected, number of data subjects, cause of breach, containment status, discovery date]

REGULATORY CONTEXT:
[Insert: applicable regulations (GDPR, HIPAA, CCPA, etc.), jurisdictions affected, data subject locations, organization size]

Following regulatory requirements and data protection best practices, provide:

1. **Notification Requirements Assessment**
   - Applicable regulations and their thresholds
   - Notification triggers and timelines
   - Required recipients (supervisory authorities, data subjects)
   - Exemptions assessment (if any)

2. **Supervisory Authority Notification**
   - GDPR Article 33 notification template (72-hour requirement)
   - Required information elements:
     * Nature of breach and categories/numbers affected
     * DPO contact details
     * Likely consequences of breach
     * Measures taken/proposed
   - HIPAA breach notification (60-day requirement)
   - Other regulatory notification formats

3. **Data Subject Notification**
   - Clear and plain language communication
   - Required elements per regulation:
     * What happened
     * What data was involved
     * What we are doing
     * What you can do
   - Notification method and timing
   - Multi-language requirements (if applicable)

4. **Incident Description Template**
   - Date and time of breach
   - Date of discovery
   - Description of breach circumstances
   - Categories of personal data affected
   - Categories of data subjects affected
   - Approximate number affected

5. **Risk Assessment Documentation**
   - Risk to rights and freedoms analysis
   - Likelihood vs. severity matrix
   - Factors considered in risk assessment
   - Determination of notification necessity

6. **Mitigation Measures Documentation**
   - Immediate actions taken
   - Preventive measures implemented
   - Remediation actions planned
   - Third-party involvement

7. **Communication Templates**
   - Press release template (if required)
   - Customer FAQ document
   - Call center script
   - Social media response guidance

8. **Documentation & Record Keeping**
   - Article 33(5) GDPR documentation requirements
   - Timeline of notifications sent
   - Proof of notification delivery
   - Post-notification monitoring requirements

Output Format: Complete notification package with templates and compliance checklist.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت مسؤول حماية البيانات تعد وثائق إشعار الخرق. أنشئ مواد إشعار خرق شاملة لحادث خرق البيانات التالي.

تفاصيل الخرق:
[أدخل: نوع الخرق، فئات البيانات المتأثرة، عدد أصحاب البيانات، سبب الخرق، حالة الاحتواء، تاريخ الاكتشاف]

السياق التنظيمي:
[أدخل: اللوائح المعمول بها (GDPR، HIPAA، CCPA، إلخ)، الولايات القضائية المتأثرة، مواقع أصحاب البيانات، حجم المنظمة]

وفقاً للمتطلبات التنظيمية وأفضل ممارسات حماية البيانات، قدم:

1. **تقييم متطلبات الإشعار**
   - اللوائح المعمول بها وعتباتها
   - محفزات الإشعار والجدول الزمني
   - المستلمين المطلوبين (السلطات الإشرافية، أصحاب البيانات)
   - تقييم الإعفاءات (إن وجدت)

2. **إشعار السلطة الإشرافية**
   - قالب إشعار المادة 33 من GDPR (متطلب 72 ساعة)
   - عناصر المعلومات المطلوبة:
     * طبيعة الخرق وفئات/أعداد المتأثرين
     * تفاصيل اتصال مسؤول حماية البيانات
     * العواقب المحتملة للخرق
     * التدابير المتخذة/المقترحة
   - إشعار خرق HIPAA (متطلب 60 يوم)
   - تنسيقات الإشعار التنظيمي الأخرى

3. **إشعار صاحب البيانات**
   - تواصل واضح وبسيط باللغة العادية
   - العناصر المطلوبة حسب اللائحة:
     * ماذا حدث
     * ما البيانات المعنية
     * ماذا نفعل
     * ماذا يمكنك أن تفعل
   - طريقة وتوقيت الإشعار
   - متطلبات متعددة اللغات (إن وجدت)

4. **قالب وصف الحادث**
   - تاريخ ووقت الخرق
   - تاريخ الاكتشاف
   - وصف ظروف الخرق
   - فئات البيانات الشخصية المتأثرة
   - فئات أصحاب البيانات المتأثرين
   - العدد التقريبي للمتأثرين

5. **توثيق تقييم المخاطر**
   - تحليل المخاطر على الحقوق والحريات
   - مصفوفة الاحتمالية مقابل الخطورة
   - العوامل المعتبرة في تقييم المخاطر
   - تحديد ضرورة الإشعار

6. **توثيق تدابير التخفيف**
   - الإجراءات الفورية المتخذة
   - التدابير الوقائية المنفذة
   - إجراءات المعالجة المخططة
   - مشاركة الأطراف الثالثة

7. **قوالب التواصل**
   - قالب البيان الصحفي (إذا كان مطلوباً)
   - وثيقة الأسئلة الشائعة للعملاء
   - نص مركز الاتصال
   - إرشادات الاستجابة على وسائل التواصل الاجتماعي

8. **التوثيق وحفظ السجلات**
   - متطلبات توثيق المادة 33(5) من GDPR
   - الجدول الزمني للإشعارات المرسلة
   - إثبات تسليم الإشعار
   - متطلبات المراقبة بعد الإشعار

تنسيق المخرجات: حزمة إشعار كاملة مع قوالب وقائمة التحقق من الامتثال.
```

---

## Example Output Preview

```
═══════════════════════════════════════════════════════
 BREACH NOTIFICATION PACKAGE | حزمة إشعار الخرق
═══════════════════════════════════════════════════════

┌─────────────────────────────────────────────────────┐
│ NOTIFICATION REQUIREMENTS MATRIX                     │
├─────────────────┬─────────────┬──────────────────────┤
│ Regulation      │ Deadline    │ Recipient           │
├─────────────────┼─────────────┼──────────────────────┤
│ GDPR Art. 33    │ 72 hours    │ Supervisory Authority│
│ GDPR Art. 34    │ Without delay│ Data Subjects      │
│ HIPAA           │ 60 days     │ HHS, Media, Patients │
│ CCPA            │ Without delay│ Affected Consumers │
│ State Laws      │ Varies      │ AG, Consumers       │
└─────────────────┴─────────────┴──────────────────────┘

GDPR ARTICLE 33 NOTIFICATION TEMPLATE:
┌─────────────────────────────────────────────────────┐
│ To: [Supervisory Authority Name]                    │
│ From: [Organization Name]                           │
│ Date: [Date]                                        │
│ Re: Personal Data Breach Notification              │
│                                                     │
│ 1. Nature of Breach:                                │
│    Ransomware attack resulting in unauthorized     │
│    access to customer database                     │
│                                                     │
│ 2. Categories of Personal Data:                     │
│    - Names and contact details                     │
│    - Financial account information                 │
│    - Government ID numbers (SSN equivalent)        │
│                                                     │
│ 3. Approximate Numbers:                             │
│    - Data subjects: 250,000                        │
│    - Records: 2.5 million                          │
│                                                     │
│ 4. DPO Contact:                                     │
│    Name: [DPO Name]                                │
│    Email: dpo@company.com                          │
│    Phone: +XX-XXX-XXXX                             │
│                                                     │
│ 5. Likely Consequences:                             │
│    Identity theft, financial fraud risk            │
│                                                     │
│ 6. Measures Taken:                                  │
│    - Systems isolated and secured                  │
│    - Law enforcement notified                      │
│    - Enhanced monitoring deployed                  │
│    - Customer notification in progress             │
└─────────────────────────────────────────────────────┘

DATA SUBJECT NOTIFICATION LETTER:
┌─────────────────────────────────────────────────────┐
│ Subject: Important Notice About Data Security      │
│                                                     │
│ Dear [Customer Name],                               │
│                                                     │
│ We are writing to inform you of a security        │
│ incident that may have affected your personal     │
│ information.                                        │
│                                                     │
│ WHAT HAPPENED:                                      │
│ On [date], we discovered unauthorized access to   │
│ our systems. An attacker may have accessed your   │
│ personal information.                              │
│                                                     │
│ WHAT INFORMATION WAS INVOLVED:                      │
│ - Your name and email address                      │
│ - Account number                                   │
│ - [Other affected data]                            │
│                                                     │
│ WHAT WE ARE DOING:                                  │
│ • Notified law enforcement                         │
│ • Engaged cybersecurity experts                    │
│ • Enhanced security measures                       │
│                                                     │
│ WHAT YOU CAN DO:                                    │
│ • Monitor your accounts                            │
│ • Enable two-factor authentication                 │
│ • Report suspicious activity                       │
│                                                     │
│ For questions: 1-800-XXX-XXXX or security@xxx.com │
└─────────────────────────────────────────────────────┘
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 5: Post-Incident Lessons Learned

### Description
Comprehensive lessons learned documentation capturing insights, improvements, and action items following a security incident to strengthen future response capabilities.

### Tags
`lessons-learned` `post-incident` `continuous-improvement` `security-enhancement`

---

## 🇬🇧 English Prompt

```
You are a security manager facilitating a post-incident lessons learned session. Create comprehensive documentation capturing insights and improvements from the following security incident.

INCIDENT SUMMARY:
[Insert: incident type, timeline, response actions, outcome, total impact, resolution status]

RESPONSE TEAM:
[Insert: teams involved, external resources used, key personnel, stakeholder communications]

Following incident response best practices and continuous improvement principles, provide:

1. **Incident Retrospective Overview**
   - Meeting participants and roles
   - Incident timeline summary
   - Response effectiveness summary
   - Key metrics (TTD, TTR, TTI)

2. **What Worked Well (Positives)**
   - Detection capabilities that functioned effectively
   - Response procedures that proved valuable
   - Team coordination successes
   - Communication effectiveness
   - Tool and technology performance
   - Training that proved effective
   - Decisions that positively impacted outcome

3. **What Could Be Improved (Gaps)**
   - Detection gaps or delays
   - Response procedure failures or gaps
   - Communication breakdowns
   - Tool limitations or failures
   - Resource constraints
   - Training gaps identified
   - Process inefficiencies
   - Decision-making delays

4. **Root Cause Analysis Summary**
   - Technical root cause(s)
   - Process root cause(s)
   - Human factors
   - Organizational factors
   - Control failures

5. **Comparative Analysis**
   - Comparison with previous similar incidents
   - Industry benchmark comparison
   - Response capability maturity assessment
   - Progress since last lessons learned

6. **Actionable Recommendations**
   - Short-term improvements (0-30 days)
     * Immediate fixes needed
     * Quick wins identified
   - Medium-term enhancements (30-90 days)
     * Process improvements
     * Tool implementations
   - Long-term strategic changes (90+ days)
     * Architecture changes
     * Organizational changes
     * Major investments

7. **Action Item Register**
   - Specific action items with:
     * Unique identifier
     * Description
     * Owner/Responsible party
     * Priority level
     * Due date
     * Success criteria
     * Status tracking

8. **Knowledge Base Updates**
   - Runbook updates needed
   - Playbook revisions required
   - Training materials to develop
   - Documentation updates needed
   - Detection rule additions

9. **Metrics and KPI Updates**
   - Current metric performance
   - Target metric values
   - New metrics to track
   - Reporting requirements

10. **Follow-up Schedule**
    - Action item review meetings
    - Remediation verification timeline
    - Next lessons learned review

Output Format: Comprehensive lessons learned document with actionable items and ownership.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت مدير أمن تيسر جلسة الدروس المستفادة بعد الحادث. أنشئ توثيقاً شاملاً يلتقط الرؤى والتحسينات من الحادث الأمني التالي.

ملخص الحادث:
[أدخل: نوع الحادث، الجدول الزمني، إجراءات الاستجابة، النتيجة، التأثير الإجمالي، حالة الحل]

فريق الاستجابة:
[أدخل: الفرق المعنية، الموارد الخارجية المستخدمة، الموظفون الرئيسيون، اتصالات أصحاب المصلحة]

وفقاً لأفضل ممارسات الاستجابة للحوادث ومبادئ التحسين المستمر، قدم:

1. **نظرة عامة استعادية الحادث**
   - المشاركون في الاجتماع والأدوار
   - ملخص الجدول الزمني للحادث
   - ملخص فعالية الاستجابة
   - المقاييس الرئيسية (TTD، TTR، TTI)

2. **ما عمل بشكل جيد (الإيجابيات)**
   - قدرات الكشف التي عملت بفعالية
   - إجراءات الاستجابة التي أثبتت قيمتها
   - نجاحات تنسيق الفريق
   - فعالية التواصل
   - أداء الأدوات والتكنولوجيا
   - التدريب الذي أثبت فعاليته
   - القرارات التي أثرت إيجاباً على النتيجة

3. **ما يمكن تحسينه (الفجوات)**
   - فجوات أو تأخيرات الكشف
   - فشل أو فجوات إجراءات الاستجابة
   - انهيارات التواصل
   - قيود أو فشل الأدوات
   - قيود الموارد
   - فجوات التدريب المحددة
   - عدم كفاءة العمليات
   - تأخيرات اتخاذ القرار

4. **ملخص تحليل السبب الجذري**
   - السبب الجذري التقني
   - السبب الجذري للعملية
   - العوامل البشرية
   - العوامل التنظيمية
   - فشل الضوابط

5. **التحليل المقارن**
   - المقارنة مع حوادث مماثلة سابقة
   - مقارنة معيار الصناعة
   - تقييم نضج قدرة الاستجابة
   - التقدم منذ آخر دروس مستفادة

6. **توصيات قابلة للتنفيذ**
   - تحسينات قصيرة المدى (0-30 يوم)
     * إصلاحات فورية مطلوبة
     * مكاسب سريعة محددة
   - تعزيزات متوسطة المدى (30-90 يوم)
     * تحسينات العمليات
     * تنفيذ الأدوات
   - تغييرات استراتيجية طويلة المدى (90+ يوم)
     * تغييرات الهيكل
     * التغييرات التنظيمية
     * الاستثمارات الكبرى

7. **سجل عناصر العمل**
   - عناصر عمل محددة مع:
     * معرف فريد
     * الوصف
     * المالك/الطرف المسؤول
     * مستوى الأولوية
     * تاريخ الاستحقاق
     * معايير النجاح
     * تتبع الحالة

8. **تحديثات قاعدة المعرفة**
   - تحديثات دليل التشغيل المطلوبة
   - مراجعات كتيب العمليات المطلوبة
   - مواد التدريب للتطوير
   - تحديثات التوثيق المطلوبة
   * إضافات قواعد الكشف

9. **تحديثات المقاييس والمؤشرات**
   - أداء المقياس الحالي
   - قيم المقياس المستهدفة
   - مقاييس جديدة للتتبع
   - متطلبات الإبلاغ

10. **جدول المتابعة**
    - اجتماعات مراجعة عناصر العمل
    - الجدول الزمني للتحقق من المعالجة
    - مراجعة الدروس المستفادة التالية

تنسيق المخرجات: وثيقة دروس مستفادة شاملة مع عناصر قابلة للتنفيذ وملكية.
```

---

## Example Output Preview

```
═══════════════════════════════════════════════════════
 LESSONS LEARNED DOCUMENT | وثيقة الدروس المستفادة
═══════════════════════════════════════════════════════

┌─────────────────────────────────────────────────────┐
│ INCIDENT RETROSPECTIVE                               │
├─────────────────────────────────────────────────────┤
│ Incident ID:     INC-2024-0892                      │
│ Date:           March 15-18, 2024                   │
│ Meeting Date:    March 20, 2024                     │
│ Participants:    12 (SOC, IT, Legal, HR, Exec)      │
│ Facilitator:     Security Manager                   │
└─────────────────────────────────────────────────────┘

RESPONSE METRICS:
┌─────────────────────────────────────────────────────┐
│ Time to Detect (TTD):    2h 34m    │ Target: <1h   │
│ Time to Respond (TTR):   4h 12m    │ Target: <2h   │
│ Time to Contain:         45m       │ Target: <1h ✓ │
│ Time to Recover:         68h       │ Target: <24h  │
│ Detection Source:        User Report│ Target: SIEM │
└─────────────────────────────────────────────────────┘

WHAT WORKED WELL ✓:
┌─────────────────────────────────────────────────────┐
│ • IR team activated within 15 minutes of alert     │
│ • Communication with leadership was effective      │
│ • Backup systems remained uncompromised            │
│ • Forensic evidence preserved properly             │
│ • External IR firm engagement was swift            │
│ • Customer notification completed within 48 hours  │
└─────────────────────────────────────────────────────┘

GAPS IDENTIFIED ✗:
┌─────────────────────────────────────────────────────┐
│ • Initial phishing email not detected by email GW  │
│ • No EDR alert on initial malware execution        │
│ • MFA not enforced on privileged accounts          │
│ • Network segmentation gaps allowed spread         │
│ • Incident playbooks outdated (last update: 2022)  │
│ • No 24/7 SOC coverage (incident occurred at night)│
└─────────────────────────────────────────────────────┘

ACTION ITEM REGISTER:
┌──────┬──────────────────────────┬────────┬──────────┤
│ ID   │ Action                   │ Owner  │ Due      │
├──────┼──────────────────────────┼────────┼──────────┤
│ LL-01│ Deploy advanced email GW │ IT Ops │ Apr 15   │
│ LL-02│ Implement MFA for admin  │ IAM    │ Apr 1    │
│ LL-03│ Update IR playbooks      │ SecOps │ Apr 30   │
│ LL-04│ Implement 24/7 SOC       │ CISO   │ Q2       │
│ LL-05│ Network segmentation     │ NetOps │ Q3       │
│ LL-06│ EDR tuning project       │ SOC    │ May 15   │
└──────┴──────────────────────────┴────────┴──────────┘

FOLLOW-UP SCHEDULE:
• Weekly action review: Every Monday 10:00
• Remediation verification: April 30, 2024
• Next lessons learned: July 2024 (or next incident)
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---
