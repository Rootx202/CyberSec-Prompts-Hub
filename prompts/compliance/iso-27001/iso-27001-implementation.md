# ISO 27001 Implementation Prompts | مطالب تنفيذ ISO 27001

---

## Prompt 1: ISO 27001 Gap Analysis

### Description
Conduct gap analysis between current state and ISO 27001 requirements.

### Tags
`iso-27001` `gap-analysis` `isms` `compliance` `information-security`

---

## 🇬🇧 English Prompt

```
Conduct an ISO 27001:2022 gap analysis:

Organization Profile:
[PROVIDE ORGANIZATION DETAILS]

Evaluate all ISO 27001:2022 Annex A controls:

ORGANIZATIONAL CONTROLS (Clause 5):
- 5.1 Policies for information security
- 5.2 Information security roles and responsibilities
- 5.3 Segregation of duties
[... continue for all controls]

PEOPLE CONTROLS (Clause 6):
- 6.1 Screening
- 6.2 Terms and conditions of employment
- 6.3 Information security awareness, education, training
[... continue for all controls]

PHYSICAL CONTROLS (Clause 7):
- 7.1 Physical security perimeters
- 7.2 Physical entry
- 7.3 Securing offices, rooms and facilities
[... continue for all controls]

TECHNOLOGICAL CONTROLS (Clause 8):
- 8.1 User endpoint devices
- 8.2 Privileged access rights
- 8.3 Information access restriction
[... continue for all controls]

For each control:
- Implementation status
- Evidence available
- Gaps identified
- Remediation required
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أجرِ تحليل فجوات ISO 27001:2022:

ملف المنظمة:
[قدم تفاصيل المنظمة]

قيّم جميع ضوابط المرفق أ من ISO 27001:2022:

الضوابط التنظيمية (البند 5):
- 5.1 سياسات أمن المعلومات
- 5.2 أدوار ومسؤوليات أمن المعلومات
- 5.3 الفصل بين المهام
[... استمر لجميع الضوابط]

ضوابط الأفراد (البند 6):
- 6.1 الفحص
- 6.2 شروط وأحكام التوظيف
- 6.3 الوعي والتثقيف والتدريب الأمني
[... استمر لجميع الضوابط]

الضوابط المادية (البند 7):
- 7.1 حدود أمنية مادية
- 7.2 الدخول المادي
- 7.3 تأمين المكاتب والغرف والمرافق
[... استمر لجميع الضوابط]

الضوابط التقنية (البند 8):
- 8.1 أجهزة المستخدم النهائية
- 8.2 حقوق الوصول المميزة
- 8.3 تقييد الوصول للمعلومات
[... استمر لجميع الضوابط]

لكل ضابط:
- حالة التنفيذ
- الأدلة المتاحة
- الفجوات المحددة
- المعالجة المطلوبة
```

---

## Example Output Preview

```
=== ISO 27001:2022 Gap Analysis Report ===

ORGANIZATION: Example Corp
SCOPE: Entire organization
ANALYSIS DATE: 2024-01-15

SUMMARY:
┌─────────────────┬─────────┬─────────┬─────────┬─────────┐
│ Control Clause  │ Total   │ Compliant│ Partial │ Gap     │
├─────────────────┼─────────┼─────────┼─────────┼─────────┤
│ 5. Organizational│ 37     │ 25      │ 8       │ 4       │
│ 6. People       │ 8       │ 6       │ 1       │ 1       │
│ 7. Physical     │ 14      │ 10      │ 3       │ 1       │
│ 8. Technological│ 34      │ 22      │ 7       │ 5       │
├─────────────────┼─────────┼─────────┼─────────┼─────────┤
│ TOTAL           │ 93      │ 63 (68%)│ 19 (20%)│ 11 (12%)│
└─────────────────┴─────────┴─────────┴─────────┴─────────┘

CRITICAL GAPS:
┌──────────┬────────────────────────────────────────────┐
│ Control  │ Gap Description                            │
├──────────┼────────────────────────────────────────────┤
│ 5.15     │ No formal supplier relationship management│
│ 5.36     │ Incident management process incomplete    │
│ 8.8      │ Vulnerability management gaps             │
│ 8.24     │ Cryptography usage not standardized       │
│ 8.28     │ Secure coding practices not documented    │
└──────────┴────────────────────────────────────────────┘

PARTIAL IMPLEMENTATIONS:
┌──────────┬────────────────────────────────────────────┐
│ Control  │ Partial Implementation                     │
├──────────┼────────────────────────────────────────────┤
│ 5.7      │ Threat intelligence - limited sources     │
│ 5.14     │ Information transfer - some channels only │
│ 8.12     │ Data leakage prevention - partial coverage│
└──────────┴────────────────────────────────────────────┘

REMEDIATION PRIORITY:
├─ HIGH: 11 controls requiring full implementation
├─ MEDIUM: 19 controls requiring enhancement
└─ LOW: Ongoing monitoring of compliant controls

TIMELINE TO COMPLIANCE:
├─ Phase 1 (0-3 months): Address critical gaps
├─ Phase 2 (3-6 months): Address partial implementations
├─ Phase 3 (6-9 months): Internal audit preparation
└─ Phase 4 (9-12 months): Certification audit
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 2: ISO 27001 Statement of Applicability

### Description
Develop Statement of Applicability (SoA) for ISO 27001 certification.

### Tags
`iso-27001` `soa` `statement-of-applicability` `isms` `certification`

---

## 🇬🇧 English Prompt

```
Develop the Statement of Applicability (SoA) for ISO 27001 certification:

Organization Scope:
[PROVIDE SCOPE DETAILS]

Create SoA including:

1. Scope Definition
   - Organizational boundaries
   - Business processes included
   - Locations covered
   - Exclusions and justifications

2. Control Selection Process
   - Risk assessment methodology
   - Control selection criteria
   - Exclusion criteria
   - Documentation requirements

3. Control Implementation Status
   - Control ID and name
   - Applicability (Yes/No)
   - Justification for exclusions
   - Implementation status
   - Evidence reference

4. Control Objectives
   - Link controls to objectives
   - Risk treatment mapping
   - Control dependencies

5. Document Control
   - Version control
   - Approval process
   - Review schedule
   - Change management

Provide complete SoA template and guidance.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
طوّر بيان قابلية التطبيق (SoA) لشهادة ISO 27001:

نطاق المنظمة:
[قدم تفاصيل النطاق]

أنشئ بيان قابلية التطبيق متضمناً:

1. تعريف النطاق
   - الحدود التنظيمية
   - العمليات التجارية المشمولة
   - المواقع المغطاة
   - الاستثناءات ومبرراتها

2. عملية اختيار الضوابط
   - منهجية تقييم المخاطر
   - معايير اختيار الضوابط
   - معايير الاستثناء
   - متطلبات التوثيق

3. حالة تنفيذ الضوابط
   - معرف واسم الضابط
   - قابلية التطبيق (نعم/لا)
   - تبرير الاستثناءات
   - حالة التنفيذ
   - مرجع الدليل

4. أهداف الضوابط
   - ربط الضوابط بالأهداف
   - تعيين معالجة المخاطر
   - تبعيات الضوابط

5. التحكم في المستندات
   - التحكم في الإصدارات
   - عملية الاعتماد
   - جدول المراجعة
   - إدارة التغيير

قدم قالب بيان قابلية التطبيق الكامل والإرشادات.
```

---

## Example Output Preview

```
=== Statement of Applicability (SoA) ===

DOCUMENT: SoA-001
VERSION: 1.0
DATE: 2024-01-15
STATUS: Approved

SCOPE DEFINITION:
┌────────────────────────────────────────────────────────┐
│ Organization: Example Corp                             │
│ Boundaries: Headquarters, Data Center, Remote Workers  │
│ Business Processes:                                    │
│   - Customer data management                           │
│   - Financial operations                               │
│   - Software development                               │
│ Exclusions: Retail stores (separate ISMS)              │
└────────────────────────────────────────────────────────┘

CONTROL SELECTION MATRIX (Sample):
┌───────┬─────────────────────────┬──────┬──────────────┬──────────┬─────────┐
│ Ctrl │ Control Name            │ Appl │ Justification│ Status   │ Evidence│
├───────┼─────────────────────────┼──────┼──────────────┼──────────┼─────────┤
│ 5.1   │ Policies for IS         │ Yes  │ -            │ Impl     │ POL-001 │
│ 5.2   │ IS Roles                │ Yes  │ -            │ Impl     │ HR-005  │
│ 5.3   │ Segregation of duties   │ Yes  │ -            │ Partial  │ ACC-002 │
│ 5.4   │ Management responsibilities│ Yes│ -           │ Impl     │ POL-001 │
│ 5.5   │ Contact with authorities│ Yes  │ -            │ Impl     │ INC-001 │
│ 5.6   │ Contact with special interest│ Yes│ -         │ Impl     │ COM-001 │
│ 5.7   │ Threat intelligence     │ Yes  │ -            │ Partial  │ SEC-003 │
│ 5.8   │ Information security in project│ Yes│ -       │ Impl     │ PM-001  │
│ 5.9   │ Inventory of information│ Yes  │ -            │ Impl     │ INV-001 │
│ 5.10  │ Acceptable use          │ Yes  │ -            │ Impl     │ POL-002 │
└───────┴─────────────────────────┴──────┴──────────────┴──────────┴─────────┘

EXCLUSIONS:
┌───────┬─────────────────────────┬──────────────────────────────────────┐
│ Ctrl │ Control Name            │ Justification for Exclusion          │
├───────┼─────────────────────────┼──────────────────────────────────────┤
│ 7.7   │ Clear desk and screen   │ Remote-only workforce, not applicable│
│ 7.9   │ Security of assets off- │ No off-site assets in scope          │
│       │ premises                │                                      │
└───────┴─────────────────────────┴──────────────────────────────────────┘

CONTROL IMPLEMENTATION SUMMARY:
├─ Total controls in Annex A: 93
├─ Controls applicable: 85 (91%)
├─ Controls excluded: 8 (9%)
├─ Implemented: 70 (82%)
├─ Partially implemented: 10 (12%)
└─ Not implemented: 5 (6%)

RISK TREATMENT MAPPING:
Each control is linked to:
├─ Risk ID from Risk Assessment
├─ Treatment option (Apply/Accept/Transfer/Avoid)
└─ Residual risk level
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 3: ISO 27001 Risk Assessment

### Description
Conduct risk assessment aligned with ISO 27001 requirements.

### Tags
`iso-27001` `risk-assessment` `isms` `risk-management` `information-security`

---

## 🇬🇧 English Prompt

```
Conduct ISO 27001-aligned information security risk assessment:

Organization Context:
[PROVIDE ORGANIZATION CONTEXT]

Perform risk assessment:

1. Context Establishment
   - Internal context
   - External context
   - ISMS scope definition

2. Asset Identification
   - Primary assets (information, processes)
   - Supporting assets (hardware, software, people)
   - Asset valuation

3. Threat Identification
   - Threat sources
   - Threat actors
   - Threat scenarios

4. Vulnerability Identification
   - Technical vulnerabilities
   - Organizational weaknesses
   - Process gaps

5. Risk Analysis
   - Likelihood assessment
   - Impact assessment
   - Risk calculation

6. Risk Evaluation
   - Risk comparison with criteria
   - Risk prioritization
   - Risk treatment decisions

7. Risk Treatment
   - Treatment options (apply/accept/transfer/avoid)
   - Control selection
   - Residual risk assessment

Provide risk register and treatment plan.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أجرِ تقييم مخاطر أمن المعلومات المتوافق مع ISO 27001:

سياق المنظمة:
[قدم سياق المنظمة]

أجرِ تقييم المخاطر:

1. إنشاء السياق
   - السياق الداخلي
   - السياق الخارجي
   - تعريف نطاق نظام إدارة أمن المعلومات

2. تحديد الأصول
   - الأصول الأساسية (المعلومات، العمليات)
   - الأصول الداعمة (الأجهزة، البرمجيات، الأشخاص)
   - تقييم الأصول

3. تحديد التهديدات
   - مصادر التهديد
   - الجهات المهددة
   - سيناريوهات التهديد

4. تحديد الثغرات
   - الثغرات التقنية
   - نقاط الضعف التنظيمية
   - فجوات العمليات

5. تحليل المخاطر
   - تقييم الاحتمالية
   - تقييم التأثير
   - حساب المخاطر

6. تقييم المخاطر
   - مقارنة المخاطر بالمعايير
   - ترتيب أولويات المخاطر
   - قرارات معالجة المخاطر

7. معالجة المخاطر
   - خيارات المعالجة (تطبيق/قبول/نقل/تجنب)
   - اختيار الضوابط
   - تقييم المخاطر المتبقية

قدم سجل المخاطر وخطة المعالجة.
```

---

## Example Output Preview

```
=== ISO 27001 Risk Assessment Report ===

ASSESSMENT DATE: 2024-01-15
METHODOLOGY: ISO 27005-aligned

CONTEXT SUMMARY:
├─ Business: Technology services
├─ Scope: HQ + Data Center
├─ Assets: 245 identified
└─ Threat landscape: Medium-high

ASSET VALUATION:
┌─────────────────┬────────────┬───────────────────────┐
│ Asset Category  │ Count      │ Critical Assets       │
├─────────────────┼────────────┼───────────────────────┤
│ Information     │ 45         │ Customer DB, IP       │
│ Software        │ 78         │ Core applications     │
│ Hardware        │ 67         │ Servers, network      │
│ People          │ 35         │ Key personnel         │
│ Services        │ 20         │ Critical services     │
└─────────────────┴────────────┴───────────────────────┘

RISK REGISTER:
┌──────┬────────────────────┬──────────┬──────────┬────────┬──────┬─────────┐
│ ID   │ Risk Description   │ Asset    │ Threat   │ Vuln   │ Score│ Treatment│
├──────┼────────────────────┼──────────┼──────────┼────────┼──────┼─────────┤
│ R001 │ Data breach        │ Customer │ External │ Weak   │ 20   │ Apply    │
│      │ (external)         │ DB       │ attacker │ auth   │      │ controls │
│ R002 │ Ransomware         │ Servers  │ Cyber-   │ Missing│ 16   │ Apply    │
│      │                    │          │ criminal │ EDR    │      │ controls │
│ R003 │ Insider threat     │ Customer │ Employee│ Excess │ 12   │ Apply    │
│      │                    │ data     │         │ access │      │ controls │
│ R004 │ DDoS attack        │ Web      │ External │ No DDoS│ 9    │ Transfer │
│      │                    │ services │ attacker│ protec │      │ (CDN)    │
│ R005 │ Physical breach    │ Data     │ Intruder │ Weak   │ 12   │ Apply    │
│      │                    │ center   │         │ access │      │ controls │
└──────┴────────────────────┴──────────┴──────────┴────────┴──────┴─────────┘

RISK SCORING MATRIX:
         │ 1   2   3   4   5  (Impact)
    ─────┼────────────────────
      5  │     │     │ R001│
      4  │     │     │ R002│ R003
      3  │     │ R004│ R005│
(Lik) 2  │     │     │     │
      1  │     │     │     │

RISK TREATMENT PLAN:
R001 - Data Breach:
├─ Treatment: Apply controls
├─ Controls: 8.2, 8.3, 8.5, 8.24
├─ Owner: Security Team
├─ Due Date: 2024-03-01
└─ Residual Risk: Low

RISK SUMMARY:
├─ Critical risks: 2
├─ High risks: 5
├─ Medium risks: 12
├─ Low risks: 8
└─ Total risks: 27
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 4: ISO 27001 Internal Audit

### Description
Plan and conduct ISO 27001 internal audit.

### Tags
`iso-27001` `internal-audit` `isms` `audit` `certification`

---

## 🇬🇧 English Prompt

```
Plan and document ISO 27001 internal audit:

ISMS Scope:
[PROVIDE ISMS SCOPE DETAILS]

Develop audit program:

1. Audit Planning
   - Audit objectives
   - Audit criteria
   - Audit scope
   - Audit team selection

2. Audit Schedule
   - Areas to be audited
   - Timeline
   - Resource allocation
   - Document review

3. Audit Checklist Development
   - Clause 4: Context of the organization
   - Clause 5: Leadership
   - Clause 6: Planning
   - Clause 7: Support
   - Clause 8: Operation
   - Clause 9: Performance evaluation
   - Clause 10: Improvement
   - Annex A controls

4. Audit Execution
   - Opening meeting
   - Document review
   - Interviews
   - Evidence collection
   - Nonconformity identification

5. Audit Reporting
   - Findings summary
   - Nonconformities
   - Observations
   - Recommendations

Provide audit checklist and report template.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
خطط وثق التدقيق الداخلي لـ ISO 27001:

نطاق نظام إدارة أمن المعلومات:
[قدم تفاصيل نطاق ISMS]

طوّر برنامج التدقيق:

1. تخطيط التدقيق
   - أهداف التدقيق
   - معايير التدقيق
   - نطاق التدقيق
   - اختيار فريق التدقيق

2. جدول التدقيق
   - المجالات التي سيتم تدقيقها
   - الجدول الزمني
   - تخصيص الموارد
   - مراجعة المستندات

3. تطوير قائمة تحقق التدقيق
   - البند 4: سياق المنظمة
   - البند 5: القيادة
   - البند 6: التخطيط
   - البند 7: الدعم
   - البند 8: التشغيل
   - البند 9: تقييم الأداء
   - البند 10: التحسين
   - ضوابط المرفق أ

4. تنفيذ التدقيق
   - اجتماع الافتتاح
   - مراجعة المستندات
   - المقابلات
   - جمع الأدلة
   - تحديد حالات عدم المطابقة

5. إعداد تقرير التدقيق
   - ملخص النتائج
   - حالات عدم المطابقة
   - الملاحظات
   - التوصيات

قدم قائمة تحقق التدقيق وقالب التقرير.
```

---

## Example Output Preview

```
=== ISO 27001 Internal Audit Plan ===

AUDIT REFERENCE: IA-2024-001
AUDIT TYPE: Internal ISMS Audit
AUDIT DATE: 2024-01-15 to 2024-01-17

AUDIT TEAM:
├─ Lead Auditor: John Smith (ISO 27001 LA certified)
├─ Auditor 1: Jane Doe (Security Specialist)
└─ Auditor 2: Bob Wilson (IT Manager)

AUDIT SCHEDULE:
Day 1 (Jan 15):
├─ 09:00-10:00: Opening meeting
├─ 10:00-12:00: Document review (Clauses 4-6)
├─ 13:00-15:00: Interview - Management
└─ 15:00-17:00: Interview - Security Team

Day 2 (Jan 16):
├─ 09:00-12:00: Annex A controls review
├─ 13:00-15:00: Technical controls verification
└─ 15:00-17:00: Physical security review

Day 3 (Jan 17):
├─ 09:00-12:00: Remaining controls
├─ 13:00-15:00: Findings compilation
└─ 15:00-16:00: Closing meeting

AUDIT CHECKLIST (Sample):
┌──────────┬────────────────────────────┬──────┬────────────┐
│ Clause   │ Requirement               │ Conf │ Findings   │
├──────────┼────────────────────────────┼──────┼────────────┤
│ 4.1      │ External/Internal context │ Y    │ Documented │
│ 4.2      │ Needs of interested parties│ Y   │ Documented │
│ 4.3      │ ISMS scope                │ Y    │ Defined    │
│ 4.4      │ ISMS establishment        │ Y    │ Complete   │
│ 5.1      │ Leadership commitment     │ Y    │ Evidenced  │
│ 5.2      │ Policy                    │ Y    │ Approved   │
│ 5.3      │ Roles and responsibilities│ Y    │ Defined    │
│ 6.1.1    │ Risk assessment           │ Y    │ Documented │
│ 6.1.2    │ Risk treatment            │ Y    │ Plan exists│
│ 6.2      │ Objectives                │ Y    │ Defined    │
└──────────┴────────────────────────────┴──────┴────────────┘

NONCONFORMITIES IDENTIFIED:
┌──────────┬──────────────────────────────────────────────┐
│ NC-001   │ Clause 8.8 - Vulnerability management       │
│ Type     │ Minor                                        │
│ Finding  │ Quarterly scans not consistently performed   │
│ Evidence │ Missing scan reports for Q2 and Q3           │
│ Action   │ Implement automated scanning schedule        │
│ Due      │ 2024-02-15                                   │
└──────────┴──────────────────────────────────────────────┘

AUDIT SUMMARY:
├─ Clauses audited: 7 main + Annex A
├─ Controls reviewed: 85 applicable
├─ Major NCs: 0
├─ Minor NCs: 3
├─ Observations: 7
└─ Overall effectiveness: 95%
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 5: ISO 27001 Certification Preparation

### Description
Prepare organization for ISO 27001 certification audit.

### Tags
`iso-27001` `certification` `isms` `preparation` `audit`

---

## 🇬🇧 English Prompt

```
Prepare organization for ISO 27001 certification audit:

Organization Details:
[PROVIDE ORGANIZATION DETAILS]

Create preparation plan:

1. Pre-Audit Readiness Assessment
   - Internal audit completion
   - Management review status
   - Corrective actions closure
   - Documentation completeness

2. Documentation Review
   - Mandatory documents check
   - Policy and procedure review
   - Records and evidence
   - Document control compliance

3. Stage 1 Audit Preparation
   - Documentation review readiness
   - Scope verification
   - Management commitment evidence
   - Risk assessment review

4. Stage 2 Audit Preparation
   - Control implementation evidence
   - Process effectiveness demonstration
   - Staff awareness
   - Interview preparation

5. Certification Body Coordination
   - CB selection criteria
   - Audit logistics
   - Communication protocols
   - Post-audit activities

Provide preparation checklist and timeline.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
حضّر المنظمة لتدقيق شهادة ISO 27001:

تفاصيل المنظمة:
[قدم تفاصيل المنظمة]

أنشئ خطة التحضير:

1. تقييم الجاهزية قبل التدقيق
   - إكمال التدقيق الداخلي
   - حالة مراجعة الإدارة
   - إغلاق الإجراءات التصحيحية
   - اكتمال التوثيق

2. مراجعة التوثيق
   - فحص المستندات الإلزامية
   - مراجعة السياسات والإجراءات
   - السجلات والأدلة
   - امتثال التحكم في المستندات

3. التحضير لتدقيق المرحلة 1
   - جاهزية مراجعة المستندات
   - التحقق من النطاق
   - دليل التزام الإدارة
   - مراجعة تقييم المخاطر

4. التحضير لتدقيق المرحلة 2
   - دليل تنفيذ الضوابط
   - إثبات فعالية العمليات
   - وعي الموظفين
   - التحضير للمقابلات

5. التنسيق مع جهة المنح
   - معايير اختيار جهة المنح
   - لوجستيات التدقيق
   - بروتوكولات الاتصال
   - أنشطة ما بعد التدقيق

قدم قائمة تحقق التحضير والجدول الزمني.
```

---

## Example Output Preview

```
=== ISO 27001 Certification Preparation Checklist ===

PRE-AUDIT READINESS:
┌─────────────────────────────────────────┬────────┬────────┐
│ Item                                    │ Status │ Date   │
├─────────────────────────────────────────┼────────┼────────┤
│ Internal audit completed                │ ✓      │ Dec 15 │
│ Management review conducted             │ ✓      │ Dec 20 │
│ Corrective actions closed               │ ✓      │ Jan 05 │
│ Internal audit NCs resolved             │ ✓      │ Jan 10 │
│ Document review complete                │ ✓      │ Jan 12 │
└─────────────────────────────────────────┴────────┴────────┘

MANDATORY DOCUMENTS CHECKLIST:
┌─────────────────────────────────────────┬────────┬────────┐
│ Document                                │ Status │ Ref    │
├─────────────────────────────────────────┼────────┼────────┤
│ ISMS Scope (Clause 4.3)                 │ ✓      │ DOC-001│
│ Information Security Policy (Clause 5.2)│ ✓      │ POL-001│
│ Risk Assessment Methodology (Clause 6.1)│ ✓      │ MET-001│
│ Risk Assessment Report                  │ ✓      │ RA-001 │
│ Risk Treatment Plan                     │ ✓      │ RT-001 │
│ Statement of Applicability              │ ✓      │ SoA-001│
│ Objectives and Plans (Clause 6.2)       │ ✓      │ OBJ-001│
│ Competence Records (Clause 7.2)         │ ✓      │ HR-001 │
│ Awareness Records (Clause 7.3)          │ ✓      │ TRN-001│
│ Communication Evidence (Clause 7.4)     │ ✓      │ COM-001│
│ Document Control Records (Clause 7.5)   │ ✓      │ DOC-CTR│
│ Operational Planning Records            │ ✓      │ OP-001 │
│ Monitoring Evidence (Clause 9.1)        │ ✓      │ MON-001│
│ Internal Audit Records (Clause 9.2)     │ ✓      │ IA-001 │
│ Management Review Records (Clause 9.3)  │ ✓      │ MR-001 │
│ Corrective Action Records (Clause 10.1) │ ✓      │ CA-001 │
└─────────────────────────────────────────┴────────┴────────┘

STAGE 1 AUDIT PREPARATION:
├─ Duration: 1-2 days
├─ Focus: Documentation review
├─ Key topics:
│   ├─ Scope definition clarity
│   ├─ Risk assessment methodology
│   ├─ SoA completeness
│   └─ Management commitment
└─ Expected outcome: Ready for Stage 2

STAGE 2 AUDIT PREPARATION:
├─ Duration: 3-5 days
├─ Focus: Implementation verification
├─ Key activities:
│   ├─ Control implementation evidence
│   ├─ Staff interviews
│   ├─ Process observation
│   └─ Record sampling
└─ Key personnel to prepare:
    ├─ Top management
    ├─ ISMS Manager
    ├─ IT Security
    ├─ HR
    └─ Process owners

STAFF INTERVIEW PREPARATION:
┌─────────────────┬────────────────────────────────────┐
│ Audience        │ Key Topics to Review               │
├─────────────────┼────────────────────────────────────┤
│ Top Management  │ Policy, objectives, commitment     │
│ ISMS Manager    │ Risk, controls, improvements       │
│ IT Staff        │ Technical controls, incidents      │
│ HR              │ Training, screening, termination   │
│ All Staff       │ Policy awareness, reporting        │
└─────────────────┴────────────────────────────────────┘

TIMELINE TO CERTIFICATION:
├─ Week 1-2: Final preparation
├─ Week 3: Stage 1 audit
├─ Week 4: Address Stage 1 findings
├─ Week 5-6: Stage 2 audit
├─ Week 7: Certification decision
└─ Week 8: Certificate issued
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team
