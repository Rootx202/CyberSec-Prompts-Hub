# PCI DSS Compliance Prompts | مطالب امتثال PCI DSS

---

## Prompt 1: PCI DSS Scope Assessment

### Description
Determine PCI DSS scope and cardholder data environment boundaries.

### Tags
`pci-dss` `compliance` `scope` `cardholder-data` `payment`

---

## 🇬🇧 English Prompt

```
As a PCI DSS Qualified Security Assessor (QSA), determine the scope of PCI DSS compliance:

Organization Profile:
[PROVIDE ORGANIZATION DETAILS]

Perform scope assessment:

1. Cardholder Data Identification
   - Where is CHD received, processed, stored, transmitted?
   - What data elements are stored (PAN, CVV, expiry)?
   - Data flow diagrams

2. System Component Identification
   - Systems involved in CHD processing
   - Network segmentation assessment
   - Connected systems and third parties

3. Scope Determination
   - Cardholder Data Environment (CDE) boundaries
   - Systems that connect to CDE
   - Segmentation effectiveness

4. Sampling Strategy
   - Sample selection methodology
   - Sample size determination
   - Coverage requirements

5. Third-Party Service Providers
   - Service provider inventory
   - PCI DSS compliance status
   - Contractual obligations

Provide scope definition and recommendations for scope reduction.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
كمقيم أمني مؤهل لـ PCI DSS، حدد نطاق امتثال PCI DSS:

ملف المنظمة:
[قدم تفاصيل المنظمة]

أجرِ تقييم النطاق:

1. تحديد بيانات حامل البطاقة
   - أين يتم استلام ومعالجة وتخزين ونقل بيانات البطاقة؟
   - ما عناصر البيانات المخزنة (رقم البطاقة، رمز التحقق، تاريخ الانتهاء)؟
   - رسوم تدفق البيانات

2. تحديد مكونات النظام
   - الأنظمة المشاركة في معالجة بيانات البطاقة
   - تقييم تجزئة الشبكة
   - الأنظمة المتصلة والأطراف الثالثة

3. تحديد النطاق
   - حدود بيئة بيانات حامل البطاقة
   - الأنظمة المتصلة ببيئة البيانات
   - فعالية التجزئة

4. استراتيجية العينات
   - منهجية اختيار العينات
   - تحديد حجم العينة
   - متطلبات التغطية

5. مقدمو الخدمات من الأطراف الثالثة
   - جرد مقدمي الخدمات
   - حالة امتثال PCI DSS
   - الالتزامات التعاقدية

قدم تعريف النطاق وتوصيات لتقليل النطاق.
```

---

## Example Output Preview

```
=== PCI DSS Scope Assessment Report ===

ORGANIZATION: Example Merchant Inc.
ASSESSMENT TYPE: PCI DSS v4.0
LEVEL: Level 1 ( >6M transactions/year)

CARDHOLDER DATA LOCATIONS:
┌─────────────────┬──────────┬──────────┬──────────┬──────────┐
│ Location        │ Received │ Processed│ Stored   │ Transmitted│
├─────────────────┼──────────┼──────────┼──────────┼──────────┤
│ POS Terminals   │ ✓        │ ✓        │ ✗        │ ✓        │
│ E-commerce Web  │ ✓        │ ✓        │ ✗        │ ✓        │
│ Payment Gateway │ ✓        │ ✓        │ ✗        │ ✓        │
│ Call Center     │ ✓        │ ✓        │ ✓ (temp) │ ✓        │
└─────────────────┴──────────┴──────────┴──────────┴──────────┘

DATA ELEMENTS STORED:
├─ PAN: Yes (tokenized) ✓
├─ CVV/CVC: No ✓
├─ Expiry Date: Yes
├─ Cardholder Name: No
└─ Service Code: No

CARDHOLDER DATA ENVIRONMENT (CDE):
┌─────────────────────────────────────────────────────┐
│                    CDE BOUNDARY                     │
│  ┌─────────┐  ┌─────────┐  ┌─────────┐            │
│  │POS Sys  │  │Web App  │  │Payment  │            │
│  │         │  │Server   │  │Gateway  │            │
│  └────┬────┘  └────┬────┘  └────┬────┘            │
│       │            │            │                  │
│       └────────────┼────────────┘                  │
│                    ▼                               │
│              ┌───────────┐                         │
│              │ Firewall  │                         │
│              └───────────┘                         │
└─────────────────────────────────────────────────────┘

SEGMENTATION ASSESSMENT:
├─ Status: EFFECTIVE
├─ Method: Network segmentation via firewall
├─ Testing: Penetration test passed
└─ Recommendation: Maintain current segmentation

THIRD-PARTY SERVICE PROVIDERS:
├─ Payment Gateway: PCI DSS Level 1 ✓
├─ Web Host: PCI DSS compliant ✓
└─ POS Vendor: PCI DSS validated ✓

SCOPE REDUCTION OPPORTUNITIES:
1. Implement tokenization for all channels
2. Remove CHD storage from call center
3. Use P2PE terminals

SAMPLE SELECTION:
├─ POS Systems: 25 of 100 (25%)
├─ Servers: All in-scope systems (100%)
├─ Workstations: 10 of 50 (20%)
└─ Network devices: All (100%)
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 2: PCI DSS Requirement Assessment

### Description
Assess compliance with all 12 PCI DSS requirements.

### Tags
`pci-dss` `compliance` `requirements` `assessment` `security`

---

## 🇬🇧 English Prompt

```
Conduct a comprehensive PCI DSS requirements assessment:

Organization Scope:
[PROVIDE SCOPE DETAILS]

Assess all 12 PCI DSS requirements:

Requirement 1: Install and maintain network security controls
Requirement 2: Apply secure configurations to all system components
Requirement 3: Protect stored account data
Requirement 4: Protect cardholder data with strong cryptography
Requirement 5: Protect all systems and networks from malicious software
Requirement 6: Develop and maintain secure systems and software
Requirement 7: Restrict access to system components and cardholder data
Requirement 8: Identify users and authenticate access to system components
Requirement 9: Restrict physical access to cardholder data
Requirement 10: Log and monitor all access to system components
Requirement 11: Test security of systems and networks regularly
Requirement 12: Support information security with organizational policies

For each requirement:
- Implementation status
- Evidence reviewed
- Gaps identified
- Remediation recommendations
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أجرِ تقييماً شاملاً لمتطلبات PCI DSS:

نطاق المنظمة:
[قدم تفاصيل النطاق]

قيّم جميع متطلبات PCI DSS الـ 12:

المتطلب 1: تثبيت وصيانة ضوابط أمن الشبكة
المتطلب 2: تطبيق تكوينات آمنة على جميع مكونات النظام
المتطلب 3: حماية بيانات الحساب المخزنة
المتطلب 4: حماية بيانات حامل البطاقة بتشفير قوي
المتطلب 5: حماية جميع الأنظمة والشبكات من البرمجيات الخبيثة
المتطلب 6: تطوير وصيانة أنظمة وبرمجيات آمنة
المتطلب 7: تقييد الوصول إلى مكونات النظام وبيانات حامل البطاقة
المتطلب 8: تحديد المستخدمين والمصادقة على الوصول إلى مكونات النظام
المتطلب 9: تقييد الوصول المادي إلى بيانات حامل البطاقة
المتطلب 10: تسجيل ومراقبة جميع الوصول إلى مكونات النظام
المتطلب 11: اختبار أمن الأنظمة والشبكات بانتظام
المتطلب 12: دعم أمن المعلومات بسياسات تنظيمية

لكل متطلب:
- حالة التنفيذ
- الأدلة المراجعة
- الفجوات المحددة
- توصيات المعالجة
```

---

## Example Output Preview

```
=== PCI DSS Requirements Assessment Summary ===

ASSESSMENT STATUS:
┌────┬───────────────────────────────┬────────────┬────────┐
│ Req│ Requirement Name              │ Status     │ Score  │
├────┼───────────────────────────────┼────────────┼────────┤
│ 1  │ Network Security Controls     │ COMPLIANT  │ 100%   │
│ 2  │ Secure Configurations         │ PARTIAL    │ 85%    │
│ 3  │ Protect Stored Data           │ COMPLIANT  │ 100%   │
│ 4  │ Encrypt Transmission          │ COMPLIANT  │ 100%   │
│ 5  │ Malware Protection            │ COMPLIANT  │ 100%   │
│ 6  │ Secure Systems Development    │ PARTIAL    │ 75%    │
│ 7  │ Restrict Access               │ COMPLIANT  │ 100%   │
│ 8  │ Identify & Authenticate       │ PARTIAL    │ 90%    │
│ 9  │ Restrict Physical Access      │ COMPLIANT  │ 100%  
│ 10 │ Log & Monitor Access          │ PARTIAL    │ 80%    │
│ 11 │ Regular Security Testing      │ COMPLIANT  │ 100%   │
│ 12 │ Information Security Policies │ COMPLIANT  │ 100%   │
└────┴───────────────────────────────┴────────────┴────────┘

OVERALL COMPLIANCE: 94%

DETAILED FINDINGS:

Req 2 - Secure Configurations (85%):
├─ 2.2.1: Default passwords changed ✓
├─ 2.2.2: Unnecessary services disabled ✓
└─ 2.2.4: Vendor defaults not changed ⚠️
    Gap: SNMP community string default
    Fix: Change to complex string

Req 6 - Secure Development (75%):
├─ 6.2: Security patches applied ✓
├─ 6.3: Secure coding practices ⚠️
├─ 6.4: Change control procedures ⚠️
└─ 6.5: Common coding vulnerabilities ⚠️
    Gaps: No formal SDLC, missing code review
    Fix: Implement SDLC with security gates

Req 10 - Log & Monitor (80%):
├─ 10.1: Audit logs enabled ✓
├─ 10.2: Log events defined ✓
├─ 10.3: Log details captured ✓
├─ 10.4: Time synchronization ✓
└─ 10.7: Log retention ⚠️
    Gap: Only 90 days online, 1 year required
    Fix: Implement long-term log storage

REMEDIATION PRIORITY:
1. HIGH: SDLC implementation (Req 6)
2. MEDIUM: Log retention (Req 10)
3. LOW: SNMP configuration (Req 2)
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 3: PCI DSS Penetration Testing

### Description
Plan and conduct PCI DSS-compliant penetration testing.

### Tags
`pci-dss` `penetration-testing` `compliance` `security-testing` `assessment`

---

## 🇬🇧 English Prompt

```
Plan and document PCI DSS penetration testing requirements:

Scope:
[PROVIDE SCOPE DETAILS]

Develop penetration testing plan:

1. Scope Definition
   - CDE boundary testing
   - Segmentation testing
   - Application testing
   - Network testing

2. Testing Methodology
   - Reconnaissance
   - Vulnerability scanning
   - Exploitation
   - Post-exploitation
   - Reporting

3. Testing Requirements (Req 11.3)
   - 11.3.1: Internal network testing
   - 11.3.2: External network testing
   - 11.3.3: Application testing
   - 11.3.4: Segmentation testing

4. Tester Qualifications
   - Independence requirements
   - Certification requirements
   - Experience requirements

5. Reporting Requirements
   - Executive summary
   - Technical findings
   - Remediation timeline
   - Retesting schedule

Provide testing plan and report template.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
خطط ووثق متطلبات اختبار الاختراق المتوافق مع PCI DSS:

النطاق:
[قدم تفاصيل النطاق]

طوّر خطة اختبار الاختراق:

1. تعريف النطاق
   - اختبار حدود بيئة بيانات حامل البطاقة
   - اختبار التجزئة
   - اختبار التطبيقات
   - اختبار الشبكة

2. منهجية الاختبار
   - الاستطلاع
   - فحص الثغرات
   - الاستغلال
   - ما بعد الاستغلال
   - التقارير

3. متطلبات الاختبار (المتطلب 11.3)
   - 11.3.1: اختبار الشبكة الداخلية
   - 11.3.2: اختبار الشبكة الخارجية
   - 11.3.3: اختبار التطبيقات
   - 11.3.4: اختبار التجزئة

4. مؤهلات المختبر
   - متطلبات الاستقلالية
   - متطلبات الشهادات
   - متطلبات الخبرة

5. متطلبات التقارير
   - الملخص التنفيذي
   - النتائج الفنية
   - الجدول الزمني للمعالجة
   - جدولة إعادة الاختبار

قدم خطة الاختبار وقالب التقرير.
```

---

## Example Output Preview

```
=== PCI DSS Penetration Testing Plan ===

TESTING SCOPE:
├─ Internal CDE: 10.0.0.0/24
├─ External: public-facing web servers
├─ Applications: E-commerce platform
└─ Segmentation: CDE to corporate network

METHODOLOGY:
Phase 1: Reconnaissance (2 days)
├─ OSINT gathering
├─ Network mapping
└─ Service enumeration

Phase 2: Vulnerability Assessment (3 days)
├─ Automated scanning
├─ Manual verification
└─ False positive elimination

Phase 3: Exploitation (3 days)
├─ Network attacks
├─ Web application attacks
├─ Social engineering (if approved)
└─ Segmentation bypass attempts

Phase 4: Post-Exploitation (2 days)
├─ Privilege escalation
├─ Lateral movement
└─ Data access verification

Phase 5: Reporting (2 days)
├─ Findings documentation
├─ Risk assessment
└─ Remediation recommendations

PCI DSS REQUIREMENTS MATRIX:
┌───────────────┬──────────────────────────────────────┐
│ Requirement   │ Testing Scope                        │
├───────────────┼──────────────────────────────────────┤
│ 11.3.1        │ Internal network exploitation        │
│ 11.3.2        │ External perimeter testing           │
│ 11.3.3        │ Web app penetration test             │
│ 11.3.4        │ Segmentation verification            │
└───────────────┴──────────────────────────────────────┘

TESTER QUALIFICATIONS:
├─ Independence: No conflict of interest
├─ Certifications: OSCP, GPEN, or CEH
├─ Experience: 3+ years penetration testing
└─ PCI DSS: Previous PCI assessment experience

SCHEDULE:
├─ Start Date: [DATE]
├─ Duration: 12 days
├─ Report Delivery: [DATE + 5 days]
└─ Retest: Within 6 months or after changes
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 4: PCI DSS Vulnerability Management

### Description
Implement PCI DSS-compliant vulnerability management program.

### Tags
`pci-dss` `vulnerability-management` `compliance` `patching` `security`

---

## 🇬🇧 English Prompt

```
Design a PCI DSS-compliant vulnerability management program:

Organization Details:
[PROVIDE ORGANIZATION DETAILS]

Address PCI DSS requirements:

1. Vulnerability Scanning (Req 11.3.2)
   - External scanning requirements
   - Approved Scanning Vendor (ASV)
   - Scan frequency
   - Reporting requirements

2. Internal Vulnerability Assessments (Req 11.3.1)
   - Scan frequency
   - Scope coverage
   - Remediation timelines

3. Patch Management (Req 6.2)
   - Critical patches: within 1 month
   - Security patches: risk-based approach
   - Change control process

4. Risk Assessment Process
   - Vulnerability prioritization
   - Business impact consideration
   - Exception process

5. Metrics and Reporting
   - KPIs for vulnerability management
   - Trend analysis
   - Compliance reporting

Provide program framework and procedures.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
صمم برنامج إدارة الثغرات المتوافق مع PCI DSS:

تفاصيل المنظمة:
[قدم تفاصيل المنظمة]

عالج متطلبات PCI DSS:

1. فحص الثغرات (المتطلب 11.3.2)
   - متطلبات الفحص الخارجي
   - مقدم خدمات الفحص المعتمد (ASV)
   - تكرار الفحص
   - متطلبات التقارير

2. تقييمات الثغرات الداخلية (المتطلب 11.3.1)
   - تكرار الفحص
   - تغطية النطاق
   - جداول المعالجة

3. إدارة التصحيحات (المتطلب 6.2)
   - التصحيحات الحرجة: خلال شهر واحد
   - تصحيحات الأمان: نهج قائم على المخاطر
   - عملية التحكم في التغيير

4. عملية تقييم المخاطر
   - أولويات الثغرات
   - اعتبار التأثير على الأعمال
   - عملية الاستثناء

5. المقاييس والتقارير
   - مؤشرات الأداء الرئيسية لإدارة الثغرات
   - تحليل الاتجاهات
   - تقارير الامتثال

قدم إطار البرنامج والإجراءات.
```

---

## Example Output Preview

```
=== PCI DSS Vulnerability Management Program ===

PROGRAM FRAMEWORK:
┌─────────────────────────────────────────────────────┐
│          VULNERABILITY MANAGEMENT LIFECYCLE         │
├─────────────────────────────────────────────────────┤
│ 1. Discovery    → Asset inventory, scanning         │
│ 2. Assessment   → Risk scoring, prioritization      │
│ 3. Remediation  → Patching, mitigations             │
│ 4. Verification → Rescanning, testing               │
│ 5. Reporting    → Metrics, compliance               │
└─────────────────────────────────────────────────────┘

ASV SCANNING SCHEDULE:
├─ Frequency: Quarterly + after significant changes
├─ ASV Provider: [Approved Vendor Name]
├─ Scope: All external IP addresses
└─ Compliance Target: PASS on all scans

INTERNAL VULNERABILITY SCANNING:
├─ Frequency: Monthly minimum
├─ Scope: All in-scope systems
├─ Authenticated: Required for accurate results
└─ Tools: Nessus, Qualys, or OpenVAS

REMEDIATION TIMELINES (PCI DSS):
┌──────────────┬─────────────┬────────────────────┐
│ Severity     │ Timeline    │ Examples           │
├──────────────┼─────────────┼────────────────────┤
│ Critical     │ 30 days     │ RCE, SQLi          │
│ High         │ 30 days     │ Privilege escalation│
│ Medium       │ 90 days     │ Information disclosure│
│ Low          │ 180 days    │ Minor misconfig    │
└──────────────┴─────────────┴────────────────────┘

PATCH MANAGEMENT PROCESS:
1. Vendor releases security patch
2. Security team assesses criticality
3. Patch tested in non-production
4. Change request submitted
5. Patch deployed during maintenance window
6. Verification scan performed

KPIs AND METRICS:
├─ Average time to remediate: Target <25 days
├─ Scan compliance rate: Target 100%
├─ Critical vulns open >30 days: Target 0
├─ ASV pass rate: Target 100%
└─ Exception rate: Target <5%

REPORTING CADENCE:
├─ Weekly: Operational metrics
├─ Monthly: Management dashboard
├─ Quarterly: Compliance report
└─ Annually: Program assessment
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 5: PCI DSS Incident Response

### Description
Develop PCI DSS-compliant incident response plan for payment card breaches.

### Tags
`pci-dss` `incident-response` `compliance` `breach` `payment`

---

## 🇬🇧 English Prompt

```
Develop a PCI DSS-compliant incident response plan for payment card data breaches:

Organization Details:
[PROVIDE ORGANIZATION DETAILS]

Include:

1. Incident Response Team
   - Team composition and roles
   - Contact information
   - Escalation procedures

2. Incident Classification
   - Severity levels
   - Payment card breach indicators
   - Classification criteria

3. Response Procedures
   - Detection and analysis
   - Containment strategies
   - Eradication procedures
   - Recovery process

4. Notification Requirements
   - Card brand notification
   - Acquiring bank notification
   - Regulatory notifications
   - Customer notification

5. Forensic Investigation
   - Evidence preservation
   - Forensic analysis requirements
   - Third-party engagement

6. Post-Incident Activities
   - Lessons learned
   - Policy updates
   - Training updates

Provide complete incident response plan.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
طوّر خطة استجابة للحوادث متوافقة مع PCI DSS لخرقات بيانات بطاقات الدفع:

تفاصيل المنظمة:
[قدم تفاصيل المنظمة]

ضمّن:

1. فريق الاستجابة للحوادث
   - تكوين الفريق والأدوار
   - معلومات الاتصال
   - إجراءات التصعيد

2. تصنيف الحوادث
   - مستويات الخطورة
   - مؤشرات خرق بطاقات الدفع
   - معايير التصنيف

3. إجراءات الاستجابة
   - الكشف والتحليل
   - استراتيجيات الاحتواء
   - إجراءات الإزالة
   - عملية التعافي

4. متطلبات الإخطار
   - إخطار علامة البطاقة
   - إخطار البنك المكتسب
   - الإخطارات التنظيمية
   - إخطار العملاء

5. التحقيق الجنائي
   - حفظ الأدلة
   - متطلبات التحليل الجنائي
   - التعاقد مع أطراف ثالثة

6. أنشطة ما بعد الحادث
   - الدروس المستفادة
   - تحديثات السياسات
   - تحديثات التدريب

قدم خطة استجابة كاملة للحوادث.
```

---

## Example Output Preview

```
=== PCI DSS Incident Response Plan ===

INCIDENT RESPONSE TEAM:
┌─────────────────┬────────────────┬────────────────────┐
│ Role            │ Primary        │ Backup             │
├─────────────────┼────────────────┼────────────────────┤
│ IR Lead         │ CISO           │ Security Manager   │
│ Technical Lead  │ Security Eng   │ Network Admin      │
│ Legal Counsel   │ General Counsel│ External Counsel   │
│ Communications  │ PR Director    │ Marketing VP       │
│ Card Brand Liaison│ Compliance  │ CFO                │
└─────────────────┴────────────────┴────────────────────┘

SEVERITY CLASSIFICATION:
┌──────────┬─────────────────────────────────────────────┐
│ Level    │ Criteria                                    │
├──────────┼─────────────────────────────────────────────┤
│ Critical │ Confirmed CHD breach, active exfiltration   │
│ High     │ Suspected breach, systems compromised       │
│ Medium   │ Possible breach, investigation needed       │
│ Low      │ Policy violation, no CHD impact             │
└──────────┴─────────────────────────────────────────────┘

BREACH INDICATORS:
├─ Unusual network traffic to CDE
├─ Unauthorized access attempts
├─ Malware detection in CDE
├─ Database anomalies
├─ Physical security incidents
└─ Third-party compromise notification

NOTIFICATION TIMELINE:
├─ T+0: Incident detected
├─ T+4h: Initial assessment complete
├─ T+24h: Determine if breach confirmed
├─ T+48h: Notify acquiring bank
├─ T+72h: Notify card brands (if required)
└─ Ongoing: Customer notification (as directed)

CARD BRAND CONTACTS:
├─ Visa: visa.com/merchantsecurity
├─ Mastercard: mastercard.us/compromise
├─ Amex: americanexpress.com/fraud
└─ Discover: discover.com/datarisk

FORENSIC REQUIREMENTS:
├─ Engage PCI Forensic Investigator (PFI)
├─ Preserve all logs and evidence
├─ Image affected systems
├─ Document chain of custody
└─ Timeline reconstruction

POST-INCIDENT CHECKLIST:
□ Complete root cause analysis
□ Update security controls
□ Revise incident response plan
□ Conduct team training
□ Submit compliance update
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team
