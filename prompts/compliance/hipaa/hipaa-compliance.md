# HIPAA Compliance Prompts | مطالب امتثال HIPAA

---

## Prompt 1: HIPAA Security Rule Assessment

### Description
Assess compliance with HIPAA Security Rule requirements.

### Tags
`hipaa` `compliance` `healthcare` `phi` `security-rule`

---

## 🇬🇧 English Prompt

```
As a HIPAA compliance consultant, assess the organization's Security Rule compliance:

Organization Profile:
[PROVIDE ORGANIZATION DETAILS]

Evaluate Security Rule standards:

ADMINISTRATIVE SAFEGUARDS (45 CFR § 164.308):
1. Security Management Process
2. Assigned Security Responsibility
3. Workforce Security
4. Information Access Management
5. Security Awareness and Training
6. Security Incident Procedures
7. Contingency Plan
8. Evaluation
9. Business Associate Contracts

PHYSICAL SAFEGUARDS (45 CFR § 164.310):
1. Facility Access Controls
2. Workstation Use
3. Workstation Security
4. Device and Media Controls

TECHNICAL SAFEGUARDS (45 CFR § 164.312):
1. Access Control
2. Audit Controls
3. Integrity
4. Person or Entity Authentication
5. Transmission Security

For each standard:
- Implementation status (Required/Addressable)
- Current controls
- Gaps identified
- Remediation recommendations
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
كمستشار امتثال HIPAA، قيّم امتثال المنظمة لقاعدة الأمان:

ملف المنظمة:
[قدم تفاصيل المنظمة]

قيّم معايير قاعدة الأمان:

الضمانات الإدارية (45 CFR § 164.308):
1. عملية إدارة الأمان
2. تعيين مسؤولية الأمان
3. أمن القوى العاملة
4. إدارة الوصول للمعلومات
5. الوعي والتدريب الأمني
6. إجراءات الحوادث الأمنية
7. خطة الطوارئ
8. التقييم
9. عقود شركاء الأعمال

الضمانات المادية (45 CFR § 164.310):
1. ضوابط الوصول للمنشأة
2. استخدام محطة العمل
3. أمن محطة العمل
4. ضوابط الأجهزة والوسائط

الضمانات التقنية (45 CFR § 164.312):
1. التحكم في الوصول
2. ضوابط التدقيق
3. النزاهة
4. مصادقة الشخص أو الكيان
5. أمن النقل

لكل معيار:
- حالة التنفيذ (مطلوب/قابل للمعالجة)
- الضوابط الحالية
- الفجوات المحددة
- توصيات المعالجة
```

---

## Example Output Preview

```
=== HIPAA Security Rule Assessment Report ===

COVERED ENTITY: Example Healthcare Provider
ASSESSMENT DATE: 2024-01-15
ASSESSOR: Compliance Team

ADMINISTRATIVE SAFEGUARDS:
┌──────────────────────────┬──────────┬──────────┬────────┐
│ Standard                 │ Type     │ Status   │ Score  │
├──────────────────────────┼──────────┼──────────┼────────┤
│ 164.308(a)(1) Security   │ Required │ Compliant│ 100%   │
│ Management               │          │          │        │
│ 164.308(a)(2) Assigned   │ Required │ Compliant│ 100%   │
│ Responsibility           │          │          │        │
│ 164.308(a)(3) Workforce  │ Required │ Partial  │ 85%    │
│ Security                 │          │          │        │
│ 164.308(a)(4) Access     │ Required │ Compliant│ 100%   │
│ Management               │          │          │        │
│ 164.308(a)(5) Training   │ Required │ Partial  │ 75%    │
│ 164.308(a)(6) Incident   │ Required │ Compliant│ 100%   │
│ Procedures               │          │          │        │
│ 164.308(a)(7) Contingency│ Required │ Partial  │ 80%    │
│ 164.308(a)(8) Evaluation │ Required │ Compliant│ 100%   │
└──────────────────────────┴──────────┴──────────┴────────┘

PHYSICAL SAFEGUARDS:
┌──────────────────────────┬──────────┬──────────┬────────┐
│ Standard                 │ Type     │ Status   │ Score  │
├──────────────────────────┼──────────┼──────────┼────────┤
│ 164.310(a)(1) Facility   │ Address. │ Compliant│ 100%   │
│ Access                   │          │          │        │
│ 164.310(b) Workstation   │ Required │ Compliant│ 100%   │
│ Use                      │          │          │        │
│ 164.310(c) Workstation   │ Required │ Partial  │ 90%    │
│ Security                 │          │          │        │
│ 164.310(d)(1) Device     │ Required │ Compliant│ 100%   │
│ Media Controls           │          │          │        │
└──────────────────────────┴──────────┴──────────┴────────┘

TECHNICAL SAFEGUARDS:
┌──────────────────────────┬──────────┬──────────┬────────┐
│ Standard                 │ Type     │ Status   │ Score  │
├──────────────────────────┼──────────┼──────────┼────────┤
│ 164.312(a)(1) Access     │ Required │ Compliant│ 100%   │
│ Control                  │          │          │        │
│ 164.312(b) Audit         │ Required │ Partial  │ 70%    │
│ Controls                 │          │          │        │
│ 164.312(c)(1) Integrity  │ Address. │ Compliant│ 100%   │
│ 164.312(d) Auth          │ Required │ Compliant│ 100%   │
│ 164.312(e)(1) Trans      │ Required │ Compliant│ 100%   │
│ Security                 │          │          │        │
└──────────────────────────┴──────────┴──────────┴────────┘

OVERALL COMPLIANCE: 92%

CRITICAL GAPS:
1. Audit log retention insufficient (6 months vs 6 years)
2. Security training not completed for 15% of staff
3. Contingency plan testing overdue

REMEDIATION PRIORITY:
├─ HIGH: Implement audit log retention
├─ HIGH: Complete staff training
└─ MEDIUM: Update contingency testing
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 2: HIPAA Privacy Rule Implementation

### Description
Implement HIPAA Privacy Rule requirements for PHI protection.

### Tags
`hipaa` `privacy` `phi` `compliance` `healthcare`

---

## 🇬🇧 English Prompt

```
Design HIPAA Privacy Rule implementation program:

Organization Details:
[PROVIDE ORGANIZATION DETAILS]

Address key Privacy Rule requirements:

1. Notice of Privacy Practices
   - Content requirements
   - Distribution methods
   - Acknowledgment procedures

2. Patient Rights
   - Access to PHI
   - Amendment requests
   - Accounting of disclosures
   - Restriction requests
   - Confidential communications

3. Uses and Disclosures
   - Treatment, Payment, Operations (TPO)
   - Authorization requirements
   - Minimum necessary standard
   - Business associate disclosures

4. Administrative Requirements
   - Privacy Officer designation
   - Workforce training
   - Policies and procedures
   - Documentation requirements

5. Breach Notification
   - Breach definition
   - Risk assessment
   - Notification requirements
   - Documentation

Provide implementation procedures and templates.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
صمم برنامج تنفيذ قاعدة الخصوصية في HIPAA:

تفاصيل المنظمة:
[قدم تفاصيل المنظمة]

عالج متطلبات قاعدة الخصوصية الرئيسية:

1. إشعار ممارسات الخصوصية
   - متطلبات المحتوى
   - طرق التوزيع
   - إجراءات الإقرار

2. حقوق المريض
   - الوصول إلى المعلومات الصحية المحمية
   - طلبات التعديل
   - محاسبة الإفصاحات
   - طلبات التقييد
   - الاتصالات السرية

3. الاستخدامات والإفصاحات
   - المعالجة والدفع والعمليات
   - متطلبات التفويض
   - معيار الحد الأدنى الضروري
   - إفصاحات شركاء الأعمال

4. المتطلبات الإدارية
   - تعيين مسؤول الخصوصية
   - تدريب القوى العاملة
   - السياسات والإجراءات
   - متطلبات التوثيق

5. إخطار الخرق
   - تعريف الخرق
   - تقييم المخاطر
   - متطلبات الإخطار
   - التوثيق

قدم إجراءات التنفيذ والقوالب.
```

---

## Example Output Preview

```
=== HIPAA Privacy Rule Implementation Guide ===

NOTICE OF PRIVACY PRACTICES (NPP):
Content Requirements:
├─ Uses and disclosures permitted
├─ Patient rights description
├─ Covered entity's legal duties
├─ Contact information
└─ Effective date

Distribution Methods:
├─ Initial visit (paper copy)
├─ Website posting
├─ Email upon request
└─ Posted in facility

PATIENT RIGHTS PROCEDURES:

Access Request Process:
├─ Timeline: 30 days (extendable 30 days)
├─ Form: Standard access request form
├─ Verification: Photo ID + DOB
├─ Format: Paper or electronic
└─ Fee: Reasonable cost-based fee

Amendment Request Process:
├─ Timeline: 60 days (extendable 30 days)
├─ Form: Amendment request form
├─ Review: Privacy Officer + provider
├─ Decision: Accept or deny in writing
└─ Appeal: Patient may submit statement

AUTHORIZATION REQUIREMENTS:
┌─────────────────────────────────────────────────┐
│ DISCLOSURES REQUIRING AUTHORIZATION:            │
├─────────────────────────────────────────────────┤
│ □ Marketing communications                      │
│ □ Sale of PHI                                   │
│ □ Psychotherapy notes                           │
│ □ Research (in most cases)                      │
│ □ Uses beyond TPO                               │
└─────────────────────────────────────────────────┘

MINIMUM NECESSARY STANDARD:
├─ Define job roles and access needs
├─ Limit access to minimum required
├─ Audit access patterns
└─ Train staff on requirement

BREACH NOTIFICATION TIMELINE:
├─ T+0: Breach discovered
├─ T+24h: Risk assessment initiated
├─ T+72h: Determine notification required
├─ T+60 days: Individual notification
├─ Annual: HHS submission if >500 affected
└─ Immediate: Media notice if >500 in state
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 3: HIPAA Breach Notification

### Description
Develop HIPAA breach notification procedures and assessment process.

### Tags
`hipaa` `breach-notification` `phi` `incident-response` `healthcare`

---

## 🇬🇧 English Prompt

```
Develop comprehensive HIPAA breach notification procedures:

Organization Profile:
[PROVIDE ORGANIZATION DETAILS]

Create procedures for:

1. Breach Definition and Identification
   - What constitutes a breach
   - Exceptions to breach definition
   - Detection mechanisms

2. Risk Assessment Process
   - Four-factor risk assessment
   - Probability assessment
   - Harm assessment
   - Documentation requirements

3. Notification Requirements
   - Individual notification (60 days)
   - HHS notification (annual/immediate)
   - Media notification (500+ in state)
   - Business associate notification

4. Notification Content
   - Required elements
   - Template letters
   - Substitute notice procedures

5. Documentation Requirements
   - Breach log maintenance
   - Risk assessment documentation
   - Notification documentation
   - Timeline documentation

Provide decision trees and templates.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
طوّر إجراءات إخطار خرق HIPAA الشاملة:

ملف المنظمة:
[قدم تفاصيل المنظمة]

أنشئ إجراءات لـ:

1. تعريف الخرق وتحديده
   - ما يشكل خرقاً
   - استثناءات من تعريف الخرق
   - آليات الكشف

2. عملية تقييم المخاطر
   - تقييم المخاطر ذو العوامل الأربعة
   - تقييم الاحتمالية
   - تقييم الضرر
   - متطلبات التوثيق

3. متطلبات الإخطار
   - إخطار الأفراد (60 يوماً)
   - إخطار HHS (سنوي/فوري)
   - إخطار وسائل الإعلام (500+ في الولاية)
   - إخطار شريك الأعمال

4. محتوى الإخطار
   - العناصر المطلوبة
   - نماذج الرسائل
   - إجراءات الإخطار البديل

5. متطلبات التوثيق
   - صيانة سجل الخروقات
   - توثيق تقييم المخاطر
   - توثيق الإخطارات
   - توثيق الجدول الزمني

قدم أشجار القرار والقوالب.
```

---

## Example Output Preview

```
=== HIPAA Breach Notification Procedures ===

BREACH DEFINITION:
A breach is the acquisition, access, use, or disclosure of PHI
in a manner not permitted under the Privacy Rule which
compromises the security or privacy of the PHI.

EXCEPTIONS:
├─ Unintentional acquisition by workforce member
├─ Inadvertent disclosure to authorized person
└─ Good faith belief that unauthorized person could not retain

FOUR-FACTOR RISK ASSESSMENT:
┌──────────────────────────────────────────────────────────┐
│ Factor 1: Nature and extent of PHI involved              │
│ ├─ Types of identifiers                                  │
│ ├─ Financial information                                 │
│ └─ Sensitivity level                                     │
│                                                          │
│ Factor 2: Unauthorized person who used/received PHI     │
│ ├─ Known vs unknown recipient                           │
│ └─ Ability to retain information                        │
│                                                          │
│ Factor 3: Whether PHI was actually acquired or viewed   │
│ ├─ Physical access                                      │
│ └─ Electronic access logs                               │
│                                                          │
│ Factor 4: Extent of risk mitigation                     │
│ ├─ Encryption status                                    │
│ ├─ Data destruction confirmation                        │
│ └─ Assurances obtained                                  │
└──────────────────────────────────────────────────────────┘

NOTIFICATION DECISION TREE:
                    ┌──────────────────┐
                    │ Breach Discovered│
                    └────────┬─────────┘
                             ▼
              ┌──────────────────────────┐
              │ Exception Applies?       │
              └───────────┬──────────────┘
                    ┌─────┴─────┐
                   YES           NO
                    │            │
                    ▼            ▼
              ┌──────────┐ ┌──────────────┐
              │ Document │ │ Risk         │
              │ Only     │ │ Assessment   │
              └──────────┘ └──────┬───────┘
                                  ▼
                    ┌──────────────────────┐
                    │ Low Risk of Harm?    │
                    └───────────┬──────────┘
                          ┌─────┴─────┐
                         YES           NO
                          │            │
                          ▼            ▼
                    ┌──────────┐ ┌──────────────┐
                    │ Document │ │ NOTIFY       │
                    │ Decision │ │ (60 days)    │
                    └──────────┘ └──────────────┘

NOTIFICATION TEMPLATE:
Dear [Patient Name],
We are writing to inform you of a breach of your protected
health information that occurred on [DATE].

Description of breach: [DESCRIBE]
Types of information involved: [LIST]
Steps we are taking: [DESCRIBE]
Steps you can take: [DESCRIBE]

Contact: [NAME] at [PHONE] or [EMAIL]

TIMELINE TRACKING:
├─ Day 0: Discovery
├─ Day 1: Investigation initiated
├─ Day 7: Risk assessment complete
├─ Day 14: Notification decision
├─ Day 30: Letters prepared
└─ Day 60: Deadline for individual notification
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 4: HIPAA Business Associate Management

### Description
Establish HIPAA business associate compliance program.

### Tags
`hipaa` `business-associate` `compliance` `contracts` `vendor`

---

## 🇬🇧 English Prompt

```
Develop a HIPAA business associate compliance program:

Organization Details:
[PROVIDE ORGANIZATION DETAILS]

Create program for:

1. Business Associate Identification
   - Definition and criteria
   - Inventory methodology
   - Classification framework

2. Business Associate Agreements (BAA)
   - Required provisions
   - Template development
   - Negotiation points
   - Review process

3. Due Diligence
   - Security assessment
   - Compliance verification
   - Risk evaluation
   - Ongoing monitoring

4. Subcontractor Management
   - Flow-down requirements
   - Verification procedures
   - Contract requirements

5. Termination Procedures
   - Data return/destruction
   - Certification requirements
   - Transition procedures

Provide BAA template and management procedures.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
طوّر برنامج امتثال شركاء الأعمال في HIPAA:

تفاصيل المنظمة:
[قدم تفاصيل المنظمة]

أنشئ برنامجاً لـ:

1. تحديد شريك الأعمال
   - التعريف والمعايير
   - منهجية الجرد
   - إطار التصنيف

2. اتفاقيات شريك الأعمال (BAA)
   - الأحكام المطلوبة
   - تطوير القالب
   - نقاط التفاوض
   - عملية المراجعة

3. العناية الواجبة
   - تقييم الأمان
   - التحقق من الامتثال
   - تقييم المخاطر
   - المراقبة المستمرة

4. إدارة المقاولين من الباطن
   - متطلبات الانتقال للأسفل
   - إجراءات التحقق
   - متطلبات العقد

5. إجراءات الإنهاء
   - إرجاع/تدمير البيانات
   - متطلبات الشهادة
   - إجراءات الانتقال

قدم قالب BAA وإجراءات الإدارة.
```

---

## Example Output Preview

```
=== HIPAA Business Associate Management Program ===

BUSINESS ASSOCIATE DEFINITION:
A person or entity that performs functions or activities
on behalf of a covered entity involving the use or
disclosure of PHI.

BA IDENTIFICATION CATEGORIES:
┌─────────────────┬────────────────────────────────────┐
│ Category        │ Examples                           │
├─────────────────┼────────────────────────────────────┤
│ IT Services     │ EHR vendors, cloud providers       │
│ Claims          │ Billing services, clearinghouses   │
│ Legal           │ Attorneys handling PHI             │
│ Administrative  │ Third-party administrators         │
│ Consulting      │ Quality improvement consultants    │
└─────────────────┴────────────────────────────────────┘

BA INVENTORY:
├─ Total BAs identified: 47
├─ High-risk BAs: 12
├─ BAAs in place: 45
└─ BAAs missing: 2

BAA REQUIRED PROVISIONS:
┌────────────────────────────────────────────────────┐
│ 1. Permitted uses and disclosures of PHI          │
│ 2. Prohibition on further use/disclosure         │
│ 3. Appropriate safeguards                        │
│ 4. Report breaches and violations                │
│ 5. Ensure subcontractor compliance               │
│ 6. Make PHI available for access requests        │
│ 7. Make PHI available for amendment              │
│ 8. Provide accounting of disclosures             │
│ 9. Allow HHS compliance investigation            │
│ 10. Return or destroy PHI at termination         │
└────────────────────────────────────────────────────┘

DUE DILIGENCE CHECKLIST:
├─ Security policies review
├─ SOC 2 Type II report
├─ HIPAA compliance attestation
├─ Security questionnaire completed
├─ References from healthcare clients
└─ Insurance coverage verified

ONGOING MONITORING:
├─ Annual security attestation
├─ Incident notification review
├─ Subcontractor verification
└─ Contract compliance audit

BA RISK SCORING:
┌─────────────┬──────────────────────────────────────┐
│ Risk Factor │ Weight                               │
├─────────────┼──────────────────────────────────────┤
│ PHI Volume  │ High (40%)                           │
│ PHI Type    │ High (30%)                           │
│ Access Level│ Medium (20%)                         │
│ Track Record│ Low (10%)                            │
└─────────────┴──────────────────────────────────────┘

TERMINATION PROCEDURES:
1. 30-day notice requirement
2. PHI return/destruction certification
3. Subcontractor notification
4. Audit verification
5. Documentation retention (6 years)
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 5: HIPAA Security Training Program

### Description
Develop comprehensive HIPAA security awareness training program.

### Tags
`hipaa` `training` `security-awareness` `compliance` `workforce`

---

## 🇬🇧 English Prompt

```
Design a HIPAA security awareness training program:

Organization Profile:
[PROVIDE ORGANIZATION DETAILS]

Create training program covering:

1. Training Requirements
   - Initial training (new hires)
   - Refresher training (annual)
   - Role-specific training
   - Remedial training

2. Core Training Topics
   - HIPAA overview
   - Privacy Rule fundamentals
   - Security Rule basics
   - PHI handling procedures
   - Patient rights
   - Breach reporting

3. Role-Specific Training
   - Clinical staff
   - Administrative staff
   - IT personnel
   - Management
   - Volunteers/contractors

4. Training Delivery Methods
   - Online modules
   - In-person sessions
   - Simulations
   - Quick reference guides

5. Compliance Tracking
   - Attendance tracking
   - Assessment scores
   - Completion certificates
   - Remediation for non-compliance

Provide training curriculum and materials outline.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
صمم برنامج تدريب الوعي الأمني لـ HIPAA:

ملف المنظمة:
[قدم تفاصيل المنظمة]

أنشئ برنامج تدريب يغطي:

1. متطلبات التدريب
   - التدريب الأولي (الموظفون الجدد)
   - التدريب التنشيطي (سنوي)
   - التدريب الخاص بالدور
   - التدريب العلاجي

2. مواضيع التدريب الأساسية
   - نظرة عامة على HIPAA
   - أساسيات قاعدة الخصوصية
   - أساسيات قاعدة الأمان
   - إجراءات التعامل مع المعلومات الصحية المحمية
   - حقوق المرضى
   - الإبلاغ عن الخروقات

3. التدريب الخاص بالدور
   - الطاقم السريري
   - الطاقم الإداري
   - موظفو تكنولوجيا المعلومات
   - الإدارة
   - المتطوعون/المقاولون

4. طرق توصيل التدريب
   - الوحدات عبر الإنترنت
   - الجلسات الشخصية
   - المحاكاة
   - أدلة المرجع السريع

5. تتبع الامتثال
   - تتبع الحضور
   - درجات التقييم
   - شهادات الإتمام
   - المعالجة لعدم الامتثال

قدم منهج التدريب ومخطط المواد.
```

---

## Example Output Preview

```
=== HIPAA Security Training Program ===

TRAINING SCHEDULE:
┌─────────────────┬────────────────┬────────────┬──────────┐
│ Training Type   │ Audience       │ Frequency  │ Duration │
├─────────────────┼────────────────┼────────────┼──────────┤
│ Initial         │ New hires      │ At hire    │ 2 hours  │
│ Refresher       │ All staff      │ Annual     │ 1 hour   │
│ Role-specific   │ By role        │ Annual     │ 1 hour   │
│ Remedial        │ Non-compliant  │ As needed  │ 30 min   │
└─────────────────┴────────────────┴────────────┴──────────┘

CORE TRAINING CURRICULUM:

Module 1: HIPAA Overview (20 min)
├─ What is HIPAA?
├─ Covered entities and BAs
├─ PHI definition and examples
└─ Penalties for non-compliance

Module 2: Privacy Rule (20 min)
├─ Patient rights
├─ Minimum necessary standard
├─ Authorization requirements
└─ Common privacy violations

Module 3: Security Rule (20 min)
├─ Administrative safeguards
├─ Physical safeguards
├─ Technical safeguards
└─ Your role in security

Module 4: PHI Handling (20 min)
├─ Proper PHI access
├─ Secure transmission
├─ Disposal procedures
└─ Mobile device security

Module 5: Incident Reporting (20 min)
├─ What is a breach?
├─ Reporting procedures
├─ Timeline requirements
└─ Your responsibilities

ROLE-SPECIFIC MODULES:

IT Personnel (Additional 1 hour):
├─ Access control management
├─ Audit log monitoring
├─ Encryption requirements
└─ Security incident response

Management (Additional 30 min):
├─ Policy enforcement
├─ Audit responsibilities
└─ Breach management

DELIVERY METHODS:
├─ Online LMS platform
├─ Interactive scenarios
├─ Video modules
├─ Quizzes (80% pass required)
└─ Certificates upon completion

COMPLIANCE TRACKING:
┌──────────────────────────────────────────────────┐
│ Training Dashboard                                │
├──────────────────────────────────────────────────┤
│ Total Staff: 500                                  │
│ Completed Initial: 485 (97%)                      │
│ Completed Annual: 470 (94%)                       │
│ Average Score: 87%                                │
│ Non-compliant: 15 (3%)                            │
└──────────────────────────────────────────────────┘

REMEDIATION PROCESS:
1. Reminder email (Day 1)
2. Manager notification (Day 7)
3. Mandatory in-person training (Day 14)
4. Access restriction (Day 30)
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team
