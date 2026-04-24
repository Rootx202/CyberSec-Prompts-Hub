# NIST Cybersecurity Framework Prompts | مطالب إطار NIST للأمن السيبراني

---

## Prompt 1: NIST CSF Implementation Assessment

### Description
Assess organization's NIST Cybersecurity Framework implementation maturity.

### Tags
`nist` `compliance` `framework` `maturity-assessment` `cybersecurity`

---

## 🇬🇧 English Prompt

```
As a compliance consultant, assess the NIST Cybersecurity Framework implementation for the following organization:

Organization Profile:
[PROVIDE ORGANIZATION DETAILS]

Evaluate each CSF function:
1. IDENTIFY (ID)
   - Asset Management (ID.AM)
   - Business Environment (ID.BE)
   - Governance (ID.GV)
   - Risk Assessment (ID.RA)
   - Risk Management Strategy (ID.RM)
   - Supply Chain Risk Management (ID.SC)

2. PROTECT (PR)
   - Identity Management and Access Control (PR.AC)
   - Awareness and Training (PR.AT)
   - Data Security (PR.DS)
   - Information Protection Processes (PR.IP)
   - Protective Technology (PR.PT)

3. DETECT (DE)
   - Anomalies and Events (DE.AE)
   - Security Continuous Monitoring (DE.CM)
   - Detection Processes (DE.DP)

4. RESPOND (RS)
   - Response Planning (RS.RP)
   - Communications (RS.CO)
   - Analysis (RS.AN)
   - Mitigation (RS.MI)
   - Improvements (RS.IM)

5. RECOVER (RC)
   - Recovery Planning (RC.RP)
   - Improvements (RC.IM)
   - Communications (RC.CO)

Provide maturity scores (1-5) and improvement recommendations for each category.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
كمستشار امتثال، قيّم تنفيذ إطار NIST للأمن السيبراني للمنظمة التالية:

ملف المنظمة:
[قدم تفاصيل المنظمة]

قيّم كل وظيفة من وظائف CSF:
1. التحديد (ID)
   - إدارة الأصول (ID.AM)
   - بيئة الأعمال (ID.BE)
   - الحوكمة (ID.GV)
   - تقييم المخاطر (ID.RA)
   - استراتيجية إدارة المخاطر (ID.RM)
   - إدارة مخاطر سلسلة التوريد (ID.SC)

2. الحماية (PR)
   - إدارة الهوية والتحكم في الوصول (PR.AC)
   - الوعي والتدريب (PR.AT)
   - أمن البيانات (PR.DS)
   - عمليات حماية المعلومات (PR.IP)
   - تقنيات الحماية (PR.PT)

3. الكشف (DE)
   - الحالات الشاذة والأحداث (DE.AE)
   - المراقبة المستمرة للأمن (DE.CM)
   - عمليات الكشف (DE.DP)

4. الاستجابة (RS)
   - تخطيط الاستجابة (RS.RP)
   - الاتصالات (RS.CO)
   - التحليل (RS.AN)
   - التخفيف (RS.MI)
   - التحسينات (RS.IM)

5. التعافي (RC)
   - تخطيط التعافي (RC.RP)
   - التحسينات (RC.IM)
   - الاتصالات (RC.CO)

قدم درجات النضج (1-5) وتوصيات التحسين لكل فئة.
```

---

## Example Output Preview

```
=== NIST CSF Maturity Assessment Report ===

ORGANIZATION: Example Corp
ASSESSMENT DATE: 2024-01-15
ASSESSOR: Security Team

MATURITY LEVELS:
Level 1: Partial | Level 2: Risk Informed | Level 3: Repeatable | Level 4: Adaptive | Level 5: Optimized

IDENTIFY FUNCTION - Overall Score: 2.8
├─ ID.AM Asset Management: 3.0 ✓
├─ ID.BE Business Environment: 2.5 ⚠️
├─ ID.GV Governance: 3.0 ✓
├─ ID.RA Risk Assessment: 2.0 ⚠️
├─ ID.RM Risk Management: 3.0 ✓
└─ ID.SC Supply Chain: 2.0 ⚠️

PROTECT FUNCTION - Overall Score: 3.2
├─ PR.AC Access Control: 3.5 ✓
├─ PR.AT Awareness Training: 2.5 ⚠️
├─ PR.DS Data Security: 3.5 ✓
├─ PR.IP Protection Processes: 3.0 ✓
└─ PR.PT Protective Technology: 3.5 ✓

DETECT FUNCTION - Overall Score: 2.5
├─ DE.AE Anomalies: 2.5 ⚠️
├─ DE.CM Continuous Monitoring: 2.5 ⚠️
└─ DE.DP Detection Processes: 2.5 ⚠️

RESPOND FUNCTION - Overall Score: 2.3
├─ RS.RP Response Planning: 2.5 ⚠️
├─ RS.CO Communications: 2.0 ⚠️
├─ RS.AN Analysis: 2.5 ⚠️
├─ RS.MI Mitigation: 2.0 ⚠️
└─ RS.IM Improvements: 2.5 ⚠️

RECOVER FUNCTION - Overall Score: 2.0
├─ RC.RP Recovery Planning: 2.0 ⚠️
├─ RC.IM Improvements: 2.0 ⚠️
└─ RC.CO Communications: 2.0 ⚠️

OVERALL MATURITY: 2.6 (Risk Informed)

PRIORITY RECOMMENDATIONS:
1. Implement comprehensive risk assessment program
2. Develop incident response playbooks
3. Establish recovery procedures and testing
4. Enhance supply chain risk management
5. Improve security monitoring capabilities
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 2: NIST CSF Gap Analysis

### Description
Perform gap analysis between current state and NIST CSF requirements.

### Tags
`nist` `gap-analysis` `compliance` `assessment` `framework`

---

## 🇬🇧 English Prompt

```
Conduct a NIST Cybersecurity Framework gap analysis:

Current State Assessment:
[PROVIDE CURRENT SECURITY CONTROLS]

For each NIST CSF subcategory:
1. Identify current implementation status
2. Compare against NIST requirements
3. Document gaps and deficiencies
4. Assess risk of each gap
5. Provide remediation roadmap

Output format:
- Gap ID and description
- CSF reference (e.g., ID.AM-1)
- Current state vs. desired state
- Risk level (High/Medium/Low)
- Remediation steps
- Timeline and resources needed
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أجرِ تحليل فجوات إطار NIST للأمن السيبراني:

تقييم الحالة الحالية:
[قدم ضوابط الأمان الحالية]

لكل فئة فرعية من NIST CSF:
1. حدد حالة التنفيذ الحالية
2. قارن بمتطلبات NIST
3. وثق الفجوات والنواقص
4. قيّم مخاطر كل فجوة
5. قدم خارطة طريق للمعالجة

تنسيق المخرجات:
- معرف الفجوة والوصف
- مرجع CSF (مثل ID.AM-1)
- الحالة الحالية مقابل الحالة المطلوبة
- مستوى المخاطر (عالي/متوسط/منخفض)
- خطوات المعالجة
- الجدول الزمني والموارد المطلوبة
```

---

## Example Output Preview

```
=== NIST CSF Gap Analysis Report ===

GAP-001: Incomplete Asset Inventory
CSF Reference: ID.AM-1
Current State: Partial asset inventory (servers only)
Desired State: Comprehensive asset inventory including hardware, software, data
Risk Level: HIGH
Remediation: Deploy asset discovery tools, implement CMDB
Timeline: 3 months | Resources: $50K

GAP-002: No Formal Risk Assessment Process
CSF Reference: ID.RA-1
Current State: Ad-hoc risk discussions
Desired State: Documented risk assessment methodology
Risk Level: HIGH
Remediation: Develop risk assessment framework, train staff
Timeline: 2 months | Resources: $25K

GAP-003: Insufficient Security Monitoring
CSF Reference: DE.CM-1
Current State: Basic log collection
Desired State: 24/7 SIEM with correlation rules
Risk Level: MEDIUM
Remediation: Deploy SIEM solution, develop use cases
Timeline: 6 months | Resources: $150K

GAP SUMMARY:
┌────────────┬───────┬────────────┐
│ Risk Level │ Count │ Priority   │
├────────────┼───────┼────────────┤
│ High       │ 5     │ Immediate  │
│ Medium     │ 12    │ 60 days    │
│ Low        │ 8     │ 180 days   │
└────────────┴───────┴────────────┘

REMEDIATION ROADMAP:
Phase 1 (0-3 months): Address High-risk gaps
Phase 2 (3-6 months): Address Medium-risk gaps
Phase 3 (6-12 months): Address Low-risk gaps
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 3: NIST CSF Control Mapping

### Description
Map existing controls to NIST CSF framework categories.

### Tags
`nist` `control-mapping` `compliance` `framework` `controls`

---

## 🇬🇧 English Prompt

```
Map the following security controls to NIST CSF categories:

Existing Controls:
[PROVIDE LIST OF SECURITY CONTROLS]

For each control:
1. Identify applicable NIST CSF subcategory
2. Determine control effectiveness
3. Identify any control gaps
4. Suggest additional controls needed
5. Document mapping rationale

Create a control mapping matrix showing:
- Control ID and name
- NIST CSF reference
- Implementation status
- Coverage level (Full/Partial/None)
- Notes and recommendations
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
قم بتعيين ضوابط الأمان التالية إلى فئات إطار NIST CSF:

الضوابط الموجودة:
[قدم قائمة ضوابط الأمان]

لكل ضابط:
1. حدد الفئة الفرعية المطبقة من NIST CSF
2. حدد فعالية الضابط
3. حدد أي فجوات في الضوابط
4. اقترح ضوابط إضافية مطلوبة
5. وثق سبب التعيين

أنشئ مصفوفة تعيين الضوابط توضح:
- معرف الضابط واسمه
- مرجع NIST CSF
- حالة التنفيذ
- مستوى التغطية (كامل/جزئي/لا شيء)
- ملاحظات وتوصيات
```

---

## Example Output Preview

```
=== NIST CSF Control Mapping Matrix ===

IDENTIFY FUNCTION:
┌────────────────┬──────────┬──────────┬──────────┬─────────────────┐
│ Control        │ CSF Ref  │ Status   │ Coverage │ Notes           │
├────────────────┼──────────┼──────────┼──────────┼─────────────────┤
│ Asset Mgmt     │ ID.AM-1  │ Active   │ Full     │ CMDB deployed   │
│ Risk Assess    │ ID.RA-1  │ Partial  │ Partial  │ Annual only     │
│ Vendor Assess  │ ID.SC-1  │ Active   │ Partial  │ Critical only   │
└────────────────┴──────────┴──────────┴──────────┴─────────────────┘

PROTECT FUNCTION:
┌────────────────┬──────────┬──────────┬──────────┬─────────────────┐
│ Control        │ CSF Ref  │ Status   │ Coverage │ Notes           │
├────────────────┼──────────┼──────────┼──────────┼─────────────────┤
│ Access Control │ PR.AC-1  │ Active   │ Full     │ PAM implemented │
│ Encryption     │ PR.DS-1  │ Active   │ Partial  │ Data at rest    │
│ Training       │ PR.AT-1  │ Active   │ Partial  │ Annual only     │
└────────────────┴──────────┴──────────┴──────────┴─────────────────┘

DETECT FUNCTION:
┌────────────────┬──────────┬──────────┬──────────┬─────────────────┐
│ Control        │ CSF Ref  │ Status   │ Coverage │ Notes           │
├────────────────┼──────────┼──────────┼──────────┼─────────────────┤
│ SIEM           │ DE.CM-1  │ Active   │ Full     │ 24/7 monitoring │
│ IDS/IPS        │ DE.CM-7  │ Active   │ Full     │ Network-wide    │
│ Vulnerability  │ DE.CM-8  │ Active   │ Partial  │ Monthly scans   │
└────────────────┴──────────┴──────────┴──────────┴─────────────────┘

COVERAGE SUMMARY:
├─ Total Controls Mapped: 45
├─ Full Coverage: 28 (62%)
├─ Partial Coverage: 15 (33%)
└─ No Coverage: 2 (5%)

RECOMMENDED ADDITIONS:
1. DE.DP-4: Event detection testing procedures
2. RS.CO-2: Incident notification procedures
3. RC.RP-1: Recovery plan documentation
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 4: NIST CSF Risk Assessment

### Description
Conduct risk assessment aligned with NIST CSF requirements.

### Tags
`nist` `risk-assessment` `compliance` `framework` `risk-management`

---

## 🇬🇧 English Prompt

```
Conduct a comprehensive risk assessment following NIST CSF guidelines:

Scope:
[DEFINE ASSESSMENT SCOPE]

Perform risk assessment including:
1. Asset identification and valuation
2. Threat identification and analysis
3. Vulnerability assessment
4. Control effectiveness evaluation
5. Risk calculation and prioritization

Output should include:
- Risk register with all identified risks
- Risk scoring methodology (Likelihood x Impact)
- Risk treatment recommendations
- Residual risk assessment
- Risk acceptance criteria

Follow NIST SP 800-30 methodology for risk assessment.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أجرِ تقييم مخاطر شامل يتبع إرشادات إطار NIST CSF:

النطاق:
[حدد نطاق التقييم]

قم بإجراء تقييم المخاطر بما يشمل:
1. تحديد وتقييم الأصول
2. تحديد وتحليل التهديدات
3. تقييم الثغرات
4. تقييم فعالية الضوابط
5. حساب وتحديد أولويات المخاطر

يجب أن تشمل المخرجات:
- سجل المخاطر مع جميع المخاطر المحددة
- منهجية تسجيل المخاطر (الاحتمالية × التأثير)
- توصيات معالجة المخاطر
- تقييم المخاطر المتبقية
- معايير قبول المخاطر

اتبع منهجية NIST SP 800-30 لتقييم المخاطر.
```

---

## Example Output Preview

```
=== NIST CSF Risk Assessment Report ===

ASSESSMENT SCOPE: Enterprise IT Infrastructure
METHODOLOGY: NIST SP 800-30 Rev. 1
RISK SCORING: Likelihood (1-5) × Impact (1-5)

RISK REGISTER:
┌──────┬─────────────────────────┬──────┬────────┬────────┬──────┬──────────┐
│ ID   │ Risk Description        │ Like │ Impact │ Score  │ Level│ Treatment│
├──────┼─────────────────────────┼──────┼────────┼────────┼──────┼──────────┤
│ R001 │ Ransomware attack       │ 4    │ 5      │ 20     │ Crit │ Mitigate │
│ R002 │ Data breach (external)  │ 3    │ 5      │ 15     │ High │ Mitigate │
│ R003 │ Insider threat          │ 3    │ 4      │ 12     │ High │ Mitigate │
│ R004 │ DDoS attack             │ 3    │ 3      │ 9      │ Med  │ Accept   │
│ R005 │ Cloud misconfiguration  │ 4    │ 3      │ 12     │ High │ Mitigate │
│ R006 │ Phishing success        │ 4    │ 4      │ 16     │ High │ Mitigate │
│ R007 │ Supply chain compromise │ 2    │ 5      │ 10     │ Med  │ Transfer │
│ R008 │ Physical security breach│ 2    │ 4      │ 8      │ Med  │ Mitigate │
└──────┴─────────────────────────┴──────┴────────┴────────┴──────┴──────────┘

RISK DISTRIBUTION:
├─ Critical: 1 (12.5%)
├─ High: 4 (50%)
├─ Medium: 3 (37.5%)
└─ Low: 0 (0%)

RISK TREATMENT PLAN:
R001 - Ransomware:
├─ Implement EDR solution
├─ Enhance backup procedures
├─ Conduct tabletop exercises
└─ Review insurance coverage

RISK MATRIX:
         │ 1   2   3   4   5  (Impact)
    ─────┼────────────────────
      5  │     │     │     │ R001
      4  │     │     │ R006│ R003
      3  │     │ R008│ R004│ R005
(Lik) 2  │     │     │ R007│
      1  │     │     │     │

RESIDUAL RISK:
After treatment, all Critical and High risks reduced to Medium or below.
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 5: NIST CSF Incident Response Alignment

### Description
Align incident response procedures with NIST CSF Respond function.

### Tags
`nist` `incident-response` `compliance` `framework` `response`

---

## 🇬🇧 English Prompt

```
Align incident response program with NIST CSF Respond function:

Current IR Program:
[DESCRIBE CURRENT INCIDENT RESPONSE PROCEDURES]

Ensure alignment with:
1. RS.RP - Response Planning
   - Incident response plan development
   - Response procedures documentation
   - Roles and responsibilities

2. RS.CO - Communications
   - Internal communications
   - External communications
   - Reporting requirements

3. RS.AN - Analysis
   - Incident categorization
   - Impact analysis
   - Forensics procedures

4. RS.MI - Mitigation
   - Containment procedures
   - Eradication procedures
   - Recovery procedures

5. RS.IM - Improvements
   - Lessons learned process
   - Plan updates
   - Metrics tracking

Provide gap analysis and implementation roadmap.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
قم بمواءمة برنامج الاستجابة للحوادث مع وظيفة الاستجابة في إطار NIST CSF:

برنامج الاستجابة الحالي:
[صف إجراءات الاستجابة للحوادث الحالية]

تأكد من المواءمة مع:
1. RS.RP - تخطيط الاستجابة
   - تطوير خطة الاستجابة للحوادث
   - توثيق إجراءات الاستجابة
   - الأدوار والمسؤوليات

2. RS.CO - الاتصالات
   - الاتصالات الداخلية
   - الاتصالات الخارجية
   - متطلبات الإبلاغ

3. RS.AN - التحليل
   - تصنيف الحوادث
   - تحليل التأثير
   - إجراءات الطب الشرعي

4. RS.MI - التخفيف
   - إجراءات الاحتواء
   - إجراءات الإزالة
   - إجراءات التعافي

5. RS.IM - التحسينات
   - عملية الدروس المستفادة
   - تحديثات الخطة
   - تتبع المقاييس

قدم تحليل الفجوات وخارطة طريق التنفيذ.
```

---

## Example Output Preview

```
=== NIST CSF Incident Response Alignment Report ===

RS.RP - RESPONSE PLANNING:
├─ RS.RP-1: IR Plan exists ✓
├─ RS.RP-2: Roles defined ✓
└─ RS.RP-3: Procedures documented ⚠️ PARTIAL
    Gap: Missing cloud incident procedures
    Action: Develop cloud IR runbook

RS.CO - COMMUNICATIONS:
├─ RS.CO-1: Personnel notified ✓
├─ RS.CO-2: External reporting ⚠️ PARTIAL
    Gap: No regulatory notification playbook
├─ RS.CO-3: Stakeholder comms ⚠️ PARTIAL
    Gap: No customer notification templates
├─ RS.CO-4: Coordination with 3rd parties ✓
└─ RS.CO-5: Voluntary sharing ⚠️ GAPS
    Gap: No ISAC membership

RS.AN - ANALYSIS:
├─ RS.AN-1: Notifications from detection ✓
├─ RS.AN-2: Impact understood ✓
├─ RS.AN-3: Forensics performed ⚠️ PARTIAL
    Gap: Limited forensic capabilities
├─ RS.AN-4: New incidents categorized ✓
└─ RS.AN-5: Prioritization ✓

RS.MI - MITIGATION:
├─ RS.MI-1: Containment executed ✓
├─ RS.MI-2: Eradication performed ✓
└─ RS.MI-3: Evidence preserved ⚠️ PARTIAL
    Gap: No formal chain of custody

RS.IM - IMPROVEMENTS:
├─ RS.IM-1: Lessons learned ✓
├─ RS.IM-2: Response plan updated ✓
└─ RS.IM-3: Effectiveness reviewed ⚠️ GAPS
    Gap: No metrics tracking

ALIGNMENT SCORE: 72%

IMPLEMENTATION ROADMAP:
Month 1-2: Address critical gaps (forensics, chain of custody)
Month 3-4: Develop notification playbooks
Month 5-6: Implement metrics program
Month 7-12: Join ISAC, enhance sharing
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team
