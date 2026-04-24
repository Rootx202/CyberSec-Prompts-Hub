# Penetration Test Report Prompts | مطالب تقارير اختبار الاختراق

---

## Prompt 1: Penetration Test Report Structure

### Description
Create comprehensive penetration test report structure and content.

### Tags
`penetration-testing` `reporting` `documentation` `security-assessment`

---

## 🇬🇧 English Prompt

```
Create a professional penetration test report for the following engagement:

Engagement Details:
[PROVIDE ENGAGEMENT DETAILS]

Report should include:

1. Executive Summary
   - Assessment overview
   - Key findings summary
   - Risk rating summary
   - Business impact
   - Recommendations overview

2. Scope and Methodology
   - Testing scope
   - Testing methodology (PTES, OSSTMM, etc.)
   - Tools used
   - Timeline
   - Limitations

3. Findings and Analysis
   - Detailed findings
   - Vulnerability description
   - Evidence and screenshots
   - Risk rating (CVSS)
   - Affected systems
   - Reproduction steps

4. Remediation Recommendations
   - Prioritized recommendations
   - Implementation guidance
   - Resource requirements

5. Technical Appendices
   - Scan results
   - Tool outputs
   - Exploit code (if applicable)
   - Timeline of activities

Provide report template and sample content.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنشئ تقرير اختبار اختراق احترافي للمشروع التالي:

تفاصيل المشروع:
[قدم تفاصيل المشروع]

يجب أن يتضمن التقرير:

1. الملخص التنفيذي
   - نظرة عامة على التقييم
   - ملخص النتائج الرئيسية
   - ملخص تصنيف المخاطر
   - تأثير الأعمال
   - نظرة عامة على التوصيات

2. النطاق والمنهجية
   - نطاق الاختبار
   - منهجية الاختبار (PTES, OSSTMM, إلخ)
   - الأدوات المستخدمة
   - الجدول الزمني
   - القيود

3. النتائج والتحليل
   - النتائج التفصيلية
   - وصف الثغرة
   - الأدلة ولقطات الشاشة
   - تصنيف المخاطر (CVSS)
   - الأنظمة المتأثرة
   - خطوات الإعادة

4. توصيات المعالجة
   - توصيات مرتبة حسب الأولوية
   - إرشادات التنفيذ
   - متطلبات الموارد

5. الملاحق الفنية
   - نتائج الفحص
   - مخرجات الأدوات
   - كود الاستغلال (إن وجد)
   - جدول زمني للأنشطة

قدم قالب التقرير ومحتوى نموذجي.
```

---

## Example Output Preview

```
=== PENETRATION TEST REPORT ===

CLIENT: Example Corp
ENGAGEMENT: Annual Penetration Test
DATE: January 15, 2024
REPORT ID: PT-2024-001

─────────────────────────────────────────────────────
EXECUTIVE SUMMARY
─────────────────────────────────────────────────────

Assessment Overview:
A comprehensive penetration test was conducted against
Example Corp's external and internal infrastructure from
January 10-14, 2024.

Key Statistics:
├─ Total Findings: 15
├─ Critical: 2
├─ High: 4
├─ Medium: 6
└─ Low: 3

Critical Findings Summary:
1. SQL Injection in Customer Portal (CVSS 9.8)
2. Remote Code Execution on Web Server (CVSS 10.0)

Risk Rating: HIGH
Immediate remediation required for critical findings.

Business Impact:
- Potential data breach affecting 100,000+ customers
- Regulatory compliance violations (PCI DSS, GDPR)
- Reputational damage risk

─────────────────────────────────────────────────────
FINDING #1: SQL Injection
─────────────────────────────────────────────────────

Severity: CRITICAL (CVSS 9.8)
Affected System: customer.example.com
CWE Reference: CWE-89

Description:
The login form is vulnerable to SQL injection attacks,
allowing authentication bypass and database access.

Evidence:
Request: POST /login HTTP/1.1
Parameter: username
Payload: ' OR '1'='1'--

Response: Authentication successful
Data extracted: User credentials table

Reproduction Steps:
1. Navigate to https://customer.example.com/login
2. Enter payload in username field
3. Submit form
4. Observe successful authentication

Remediation:
- Implement parameterized queries
- Apply input validation
- Use prepared statements
- Deploy WAF rules

─────────────────────────────────────────────────────
REMEDIATION PRIORITY MATRIX
─────────────────────────────────────────────────────

┌──────────┬───────────────────────────────┬──────┬────────┐
│ Priority │ Finding                       │ Risk │ Due    │
├──────────┼───────────────────────────────┼──────┼────────┤
│ 1        │ SQL Injection                 │ Crit │ 24h    │
│ 2        │ Remote Code Execution         │ Crit │ 24h    │
│ 3        │ Privilege Escalation          │ High │ 7d     │
│ 4        │ Cross-Site Scripting          │ High │ 14d    │
└──────────┴───────────────────────────────┴──────┴────────┘
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 2: Vulnerability Finding Documentation

### Description
Document individual vulnerability findings with proper structure.

### Tags
`vulnerability` `documentation` `finding` `reporting` `cvss`

---

## 🇬🇧 English Prompt

```
Document a security vulnerability finding:

Vulnerability Details:
[PROVIDE VULNERABILITY DETAILS]

Include in documentation:

1. Finding Identification
   - Finding ID
   - Title
   - Category (OWASP, CWE)
   - CVSS score and vector

2. Technical Description
   - Vulnerability explanation
   - Attack vector
   - Prerequisites

3. Affected Components
   - System/application name
   - Version
   - Location (URL, endpoint)
   - Dependencies

4. Proof of Concept
   - Step-by-step reproduction
   - Screenshots
   - Request/response examples
   - Tool commands used

5. Impact Analysis
   - Confidentiality impact
   - Integrity impact
   - Availability impact
   - Business impact

6. Remediation Guidance
   - Specific fix recommendations
   - Code examples if applicable
   - Workarounds
   - References

Provide complete finding documentation.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
وثّق نتيجة ثغرة أمنية:

تفاصيل الثغرة:
[قدم تفاصيل الثغرة]

ضمّن في التوثيق:

1. تحديد النتيجة
   - معرف النتيجة
   - العنوان
   - الفئة (OWASP, CWE)
   - درجة CVSS والمتجه

2. الوصف التقني
   - شرح الثغرة
   - متجه الهجوم
   - المتطلبات الأساسية

3. المكونات المتأثرة
   - اسم النظام/التطبيق
   - الإصدار
   - الموقع (URL, نقطة النهاية)
   - التبعيات

4. إثبات المفهوم
   - خطوات الإعادة خطوة بخطوة
   - لقطات الشاشة
   - أمثلة الطلب/الاستجابة
   - أوامر الأدوات المستخدمة

5. تحليل التأثير
   - تأثير السرية
   - تأثير النزاهة
   - تأثير التوفر
   - تأثير الأعمال

6. إرشادات المعالجة
   - توصيات إصلاح محددة
   - أمثلة برمجية إن وجدت
   - حلول بديلة
   - المراجع

قدم توثيق نتيجة كامل.
```

---

## Example Output Preview

```
=== VULNERABILITY FINDING DOCUMENTATION ===

FINDING ID: FIND-2024-001
TITLE: Authenticated Remote Code Execution via File Upload
CATEGORY: CWE-434 (Unrestricted Upload of File with Dangerous Type)

CVSS v3.1 SCORE: 8.8 (HIGH)
Vector: CVSS:3.1/AV:N/AC:L/PR:L/UI:N/S:U/C:H/I:H/A:H

─────────────────────────────────────────────────────
TECHNICAL DESCRIPTION
─────────────────────────────────────────────────────

The application allows authenticated users to upload files
without proper validation of file type or content. This
enables uploading malicious files (e.g., PHP, ASPX) that
can be executed on the server.

Attack Vector: Network (AV:N)
- Attackable from any network location
- No special access required beyond authentication

Attack Complexity: Low (AC:L)
- No special conditions required
- Reliable exploitation

Privileges Required: Low (PR:L)
- Authenticated user access required
- Standard user privileges sufficient

─────────────────────────────────────────────────────
AFFECTED COMPONENTS
─────────────────────────────────────────────────────

Application: Content Management System
Version: 3.2.1
Endpoint: /admin/upload.php
Location: https://target.com/admin/upload.php

─────────────────────────────────────────────────────
PROOF OF CONCEPT
─────────────────────────────────────────────────────

Step 1: Authenticate to the application
POST /login HTTP/1.1
username=admin&password=password

Step 2: Upload malicious file
POST /admin/upload.php HTTP/1.1
Content-Type: multipart/form-data

------Boundary
Content-Disposition: form-data; name="file"; filename="shell.php"
Content-Type: application/x-php

<?php system($_GET['cmd']); ?>
------Boundary--

Step 3: Execute uploaded file
GET /uploads/shell.php?cmd=whoami
Response: www-data

─────────────────────────────────────────────────────
IMPACT ANALYSIS
─────────────────────────────────────────────────────

Confidentiality: HIGH
- Full access to server files
- Database credentials exposed
- Customer data at risk

Integrity: HIGH
- Ability to modify any file
- Database manipulation possible
- Defacement risk

Availability: HIGH
- Server can be taken offline
- Ransomware deployment possible

Business Impact:
- Data breach notification required
- Regulatory fines (GDPR, PCI)
- Reputational damage

─────────────────────────────────────────────────────
REMEDIATION GUIDANCE
─────────────────────────────────────────────────────

Primary Fix:
Implement strict file type validation:

// Allowlist approach
$allowed_types = ['image/jpeg', 'image/png', 'application/pdf'];
if (!in_array($_FILES['file']['type'], $allowed_types)) {
    die('Invalid file type');
}

// Validate file content
$finfo = new finfo(FILEINFO_MIME_TYPE);
$mime = $finfo->file($_FILES['file']['tmp_name']);
if (!in_array($mime, $allowed_types)) {
    die('Invalid file type');
}

// Store outside webroot
$upload_dir = '/var/uploads/';
move_uploaded_file($tmp, $upload_dir . $safe_name);

Additional Measures:
- Rename files with random names
- Implement file size limits
- Scan uploads for malware
- Set proper file permissions
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 3: Risk Prioritization Report

### Description
Create risk prioritization report for vulnerability management.

### Tags
`risk-prioritization` `vulnerability-management` `reporting` `risk`

---

## 🇬🇧 English Prompt

```
Create a risk prioritization report for identified vulnerabilities:

Vulnerability List:
[PROVIDE LIST OF VULNERABILITIES]

Develop prioritization including:

1. Risk Scoring Methodology
   - CVSS scoring
   - Business context weighting
   - Asset criticality
   - Threat intelligence factors

2. Prioritization Criteria
   - Exploitability assessment
   - Asset exposure
   - Data sensitivity
   - Compliance requirements

3. Priority Tiers
   - Critical (immediate action)
   - High (within 7 days)
   - Medium (within 30 days)
   - Low (within 90 days)

4. Remediation Roadmap
   - Resource allocation
   - Timeline planning
   - Dependency mapping

5. Metrics and Tracking
   - SLA compliance
   - Mean time to remediate
   - Risk reduction metrics

Provide prioritization matrix and roadmap.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنشئ تقرير أولويات المخاطر للثغرات المحددة:

قائمة الثغرات:
[قدم قائمة الثغرات]

طوّر الأولوية متضمنة:

1. منهجية تسجيل المخاطر
   - تسجيل CVSS
   - وزن سياق الأعمال
   - أهمية الأصول
   - عوامل استخبارات التهديدات

2. معايير الأولوية
   - تقييم قابلية الاستغلال
   - تعرض الأصول
   - حساسية البيانات
   - متطلبات الامتثال

3. مستويات الأولوية
   - حرج (إجراء فوري)
   - عالي (خلال 7 أيام)
   - متوسط (خلال 30 يوماً)
   - منخفض (خلال 90 يوماً)

4. خارطة طريق المعالجة
   - تخصيص الموارد
   - تخطيط الجدول الزمني
   - تعيين التبعيات

5. المقاييس والتتبع
   - امتثال SLA
   - متوسط وقت المعالجة
   - مقاييس تقليل المخاطر

قدم مصفوفة الأولويات وخارطة الطريق.
```

---

## Example Output Preview

```
=== RISK PRIORITIZATION REPORT ===

REPORT DATE: January 15, 2024
SCOPE: Q1 2024 Vulnerability Assessment

RISK SCORING METHODOLOGY:
Risk Score = CVSS × Asset Criticality × Threat Factor × Exposure

SCORING FACTORS:
┌──────────────────┬────────────────────────────────────┐
│ Factor           │ Values                             │
├──────────────────┼────────────────────────────────────┤
│ Asset Criticality│ Critical=1.5, High=1.2, Med=1.0   │
│ Threat Factor    │ Active exploit=2.0, PoC=1.5, None=1.0│
│ Exposure         │ Internet=2.0, Internal=1.0        │
└──────────────────┴────────────────────────────────────┘

PRIORITIZED VULNERABILITY LIST:
┌──────┬─────────────────────┬───────┬─────┬──────┬─────┬──────────┐
│ Rank │ Vulnerability       │ CVSS  │ AC  │ TF   │ Exp │ Priority │
├──────┼─────────────────────┼───────┼─────┼──────┼─────┼──────────┤
│ 1    │ RCE on Web Server   │ 10.0  │ 1.5 │ 2.0  │ 2.0 │ CRITICAL │
│ 2    │ SQL Injection       │ 9.8   │ 1.5 │ 2.0  │ 2.0 │ CRITICAL │
│ 3    │ Priv Escalation     │ 8.8   │ 1.5 │ 1.5  │ 1.0 │ HIGH     │
│ 4    │ XSS (Stored)        │ 8.1   │ 1.2 │ 1.5  │ 2.0 │ HIGH     │
│ 5    │ SSRF                │ 7.5   │ 1.2 │ 1.5  │ 1.0 │ HIGH     │
│ 6    │ Info Disclosure     │ 5.3   │ 1.5 │ 1.0  │ 1.0 │ MEDIUM   │
│ 7    │ Missing Headers     │ 5.0   │ 1.0 │ 1.0  │ 1.0 │ LOW      │
└──────┴─────────────────────┴───────┴─────┴──────┴─────┴──────────┘

REMEDIATION ROADMAP:
┌────────────────────────────────────────────────────────────┐
│ WEEK 1: CRITICAL VULNERABILITIES                          │
├────────────────────────────────────────────────────────────┤
│ □ RCE on Web Server - Patch + WAF rules                   │
│ □ SQL Injection - Parameterized queries                    │
│ Resources: 2 developers, 1 security engineer               │
└────────────────────────────────────────────────────────────┘

┌────────────────────────────────────────────────────────────┐
│ WEEK 2-3: HIGH VULNERABILITIES                            │
├────────────────────────────────────────────────────────────┤
│ □ Privilege Escalation - Fix sudo configuration           │
│ □ XSS (Stored) - Output encoding                          │
│ □ SSRF - URL validation                                    │
│ Resources: 2 developers                                     │
└────────────────────────────────────────────────────────────┘

METRICS TRACKING:
├─ Total vulnerabilities: 45
├─ Critical remediated: 0/2 (0%)
├─ High remediated: 0/4 (0%)
├─ Mean time to remediate: N/A
├─ SLA compliance rate: N/A
└─ Risk reduction target: 80% in 30 days
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 4: Technical Security Assessment Report

### Description
Create comprehensive technical security assessment report.

### Tags
`security-assessment` `technical-report` `documentation` `audit`

---

## 🇬🇧 English Prompt

```
Create a technical security assessment report:

Assessment Details:
[PROVIDE ASSESSMENT DETAILS]

Include:

1. Technical Executive Summary
   - Technical findings overview
   - Architecture observations
   - Key technical risks

2. Infrastructure Assessment
   - Network architecture review
   - Server configuration analysis
   - Network security controls

3. Application Security Assessment
   - Web application findings
   - API security analysis
   - Authentication mechanisms

4. Security Controls Assessment
   - Access controls review
   - Encryption implementation
   - Logging and monitoring

5. Technical Recommendations
   - Specific technical fixes
   - Configuration changes
   - Architecture improvements

Provide detailed technical report.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنشئ تقرير تقييم أمني تقني:

تفاصيل التقييم:
[قدم تفاصيل التقييم]

ضمّن:

1. الملخص التنفيذي التقني
   - نظرة عامة على النتائج التقنية
   - ملاحظات البنية
   - المخاطر التقنية الرئيسية

2. تقييم البنية التحتية
   - مراجعة بنية الشبكة
   - تحليل تكوين الخوادم
   - ضوابط أمن الشبكة

3. تقييم أمن التطبيقات
   - نتائج تطبيقات الويب
   - تحليل أمن API
   - آليات المصادقة

4. تقييم الضوابط الأمنية
   - مراجعة ضوابط الوصول
   - تنفيذ التشفير
   - التسجيل والمراقبة

5. التوصيات التقنية
   - إصلاحات تقنية محددة
   - تغييرات التكوين
   - تحسينات البنية

قدم تقريراً تقنياً مفصلاً.
```

---

## Example Output Preview

```
=== TECHNICAL SECURITY ASSESSMENT REPORT ===

ASSESSMENT ID: TSA-2024-001
DATE: January 15, 2024
SCOPE: Production Infrastructure

══════════════════════════════════════════════════════
INFRASTRUCTURE ASSESSMENT
══════════════════════════════════════════════════════

NETWORK ARCHITECTURE FINDINGS:
┌─────────────────────────────────────────────────────┐
│ Finding: Excessive Network Segmentation             │
│ Severity: Medium                                    │
│ Details: 15 network segments, complex ACLs         │
│ Risk: Management overhead, potential misconfig     │
│ Recommendation: Consolidate to 5-7 segments        │
└─────────────────────────────────────────────────────┘

FIREWALL RULE ANALYSIS:
├─ Total rules: 2,450
├─ Unused rules: 340 (14%)
├─ Overly permissive: 89
├─ Shadowed rules: 23
└─ Recommendation: Rule cleanup required

SERVER CONFIGURATION REVIEW:
┌──────────┬──────────────┬──────────────────────┐
│ Server   │ Issues Found │ Severity Distribution│
├──────────┼──────────────┼──────────────────────┤
│ WEB-01   │ 12           │ 2H, 5M, 5L          │
│ WEB-02   │ 8            │ 1H, 4M, 3L          │
│ DB-01    │ 15           │ 3H, 7M, 5L          │
│ APP-01   │ 6            │ 0H, 4M, 2L          │
└──────────┴──────────────┴──────────────────────┘

══════════════════════════════════════════════════════
APPLICATION SECURITY ASSESSMENT
══════════════════════════════════════════════════════

AUTHENTICATION MECHANISM REVIEW:
├─ MFA: Implemented ✓
├─ Password Policy: Strong ✓
├─ Session Management: Issues found ⚠️
│   └─ Session timeout: 8 hours (recommended: 1 hour)
├─ Account Lockout: Implemented ✓
└─ Certificate Validation: Issues found ⚠️
    └─ Certificate pinning not implemented

API SECURITY FINDINGS:
┌─────────────────────┬──────────┬──────────────────────┐
│ Finding             │ Severity │ API Endpoint         │
├─────────────────────┼──────────┼──────────────────────┤
│ Missing rate limit  │ Medium   │ /api/v1/auth        │
│ No input validation │ High     │ /api/v1/users       │
│ Excessive data      │ Low      │ /api/v1/products    │
│ CORS misconfig      │ Medium   │ /api/v1/*           │
└─────────────────────┴──────────┴──────────────────────┘

══════════════════════════════════════════════════════
SECURITY CONTROLS ASSESSMENT
══════════════════════════════════════════════════════

ACCESS CONTROL MATRIX:
┌───────────────┬──────────┬───────────┬──────────────┐
│ Control Area  │ Status   │ Gap Count │ Risk Level   │
├───────────────┼──────────┼───────────┼──────────────┤
│ PAM           │ Partial  │ 3         │ High         │
│ Role-Based    │ Complete │ 0         │ Low          │
│ Privileged    │ Partial  │ 2         │ Medium       │
│ Service Accts │ Gap      │ 5         │ High         │
└───────────────┴──────────┴───────────┴──────────────┘

ENCRYPTION IMPLEMENTATION:
├─ Data at Rest: AES-256 ✓
├─ Data in Transit: TLS 1.3 ✓
├─ Key Management: Issues ⚠️
│   └─ Keys not rotated
└─ Certificate Management: Gaps
    └─ No automated renewal
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 5: Remediation Tracking Report

### Description
Create remediation tracking and progress report.

### Tags
`remediation` `tracking` `reporting` `vulnerability-management`

---

## 🇬🇧 English Prompt

```
Create a remediation tracking and progress report:

Remediation Data:
[PROVIDE REMEDIATION DATA]

Include:

1. Executive Summary
   - Overall progress
   - Key achievements
   - Blockers and risks

2. Remediation Status by Severity
   - Critical findings status
   - High findings status
   - Medium findings status
   - Low findings status

3. Team Performance
   - Remediation by team
   - SLA compliance
   - Mean time to remediate

4. Trend Analysis
   - Remediation velocity
   - New findings vs. remediated
   - Backlog analysis

5. Recommendations
   - Process improvements
   - Resource needs
   - Risk acceptance decisions

Provide tracking dashboard and metrics.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنشئ تقرير تتبع وتقدم المعالجة:

بيانات المعالجة:
[قدم بيانات المعالجة]

ضمّن:

1. الملخص التنفيذي
   - التقدم الإجمالي
   - الإنجازات الرئيسية
   - العوائق والمخاطر

2. حالة المعالجة حسب الخطورة
   - حالة النتائج الحرجة
   - حالة النتائج العالية
   - حالة النتائج المتوسطة
   - حالة النتائج المنخفضة

3. أداء الفريق
   - المعالجة حسب الفريق
   - امتثال SLA
   - متوسط وقت المعالجة

4. تحليل الاتجاهات
   - سرعة المعالجة
   - النتائج الجديدة مقابل المعالجة
   - تحليل backlog

5. التوصيات
   - تحسينات العملية
   - احتياجات الموارد
   - قرارات قبول المخاطر

قدم لوحة التتبع والمقاييس.
```

---

## Example Output Preview

```
=== REMEDIATION TRACKING REPORT ===

REPORT PERIOD: January 1-15, 2024
LAST UPDATED: January 15, 2024

══════════════════════════════════════════════════════
EXECUTIVE SUMMARY
══════════════════════════════════════════════════════

Overall Progress:
┌────────────────────────────────────────────────────┐
│ ████████████████████░░░░░░░░░░ 67% Complete       │
└────────────────────────────────────────────────────┘

Key Statistics:
├─ Total Findings: 45
├─ Remediated: 30 (67%)
├─ In Progress: 8 (18%)
├─ Not Started: 5 (11%)
├─ Risk Accepted: 2 (4%)

Achievements This Period:
✓ Critical RCE vulnerability remediated
✓ SQL Injection fixed in customer portal
✓ 15 medium findings closed

Blockers:
⚠ 2 high findings pending vendor patch
⚠ Resource constraints on network team

══════════════════════════════════════════════════════
REMEDIATION BY SEVERITY
══════════════════════════════════════════════════════

CRITICAL FINDINGS:
┌──────────┬─────────────────────┬──────────┬────────┐
│ ID       │ Finding             │ Status   │ Due    │
├──────────┼─────────────────────┼──────────┼────────┤
│ CRIT-001 │ RCE Web Server      │ ✓ Closed │ Jan 10 │
│ CRIT-002 │ SQL Injection       │ ✓ Closed │ Jan 12 │
└──────────┴─────────────────────┴──────────┴────────┘
SLA Compliance: 100% (2/2 within 24 hours)

HIGH FINDINGS:
┌──────────┬─────────────────────┬──────────┬────────┐
│ ID       │ Finding             │ Status   │ Due    │
├──────────┼─────────────────────┼──────────┼────────┤
│ HIGH-001 │ Priv Escalation     │ ✓ Closed │ Jan 14 │
│ HIGH-002 │ XSS Stored          │ In Prog  │ Jan 20 │
│ HIGH-003 │ SSRF                │ In Prog  │ Jan 21 │
│ HIGH-004 │ Auth Bypass         │ Blocked  │ Jan 25 │
└──────────┴─────────────────────┴──────────┴────────┘
SLA Compliance: 75% (3/4 on track)

══════════════════════════════════════════════════════
TEAM PERFORMANCE
══════════════════════════════════════════════════════

┌─────────────┬───────────┬───────────┬───────────────┐
│ Team        │ Assigned  │ Remediated│ Avg MTTR      │
├─────────────┼───────────┼───────────┼───────────────┤
│ App Dev     │ 15        │ 12 (80%)  │ 4.2 days      │
│ Infra       │ 12        │ 8 (67%)   │ 7.5 days      │
│ Network     │ 10        │ 5 (50%)   │ 9.3 days      │
│ Security    │ 8         │ 5 (63%)   │ 3.1 days      │
└─────────────┴───────────┴───────────┴───────────────┘

══════════════════════════════════════════════════════
TREND ANALYSIS
══════════════════════════════════════════════════════

Remediation Velocity (Last 30 days):
Week 1: ████████ 8 findings
Week 2: ██████████████ 14 findings
Week 3: ██████████ 10 findings
Week 4: ████████████ 12 findings

New vs. Remediated Trend:
├─ Week 1: New 5, Fixed 8 (+3)
├─ Week 2: New 3, Fixed 14 (+11)
├─ Week 3: New 2, Fixed 10 (+8)
└─ Week 4: New 4, Fixed 12 (+8)
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team
