# Code Audit Techniques Prompts

A comprehensive collection of bilingual (English/Arabic) prompts for code audit techniques, covering manual review, automated scanning, and systematic code review methodologies.

---

## Prompt 1: Manual Code Review Methodology

### Description
A systematic approach to manual code review focusing on identifying security vulnerabilities through structured analysis, design pattern review, and security-focused inspection techniques.

### Tags
`manual-review` `code-audit` `security-review` `static-analysis`

---

## 🇬🇧 English Prompt

```
You are a senior security code auditor conducting a comprehensive manual code review. Apply systematic review methodology to identify security vulnerabilities in the following codebase.

CODEBASE INFORMATION:
[Insert: programming language, application type, framework, lines of code, critical functionality, authentication mechanism, data flow description]

Following OWASP Code Review Guide and industry best practices, provide:

1. **Pre-Review Analysis**
   - Architecture understanding and threat modeling
   - Entry point identification (user inputs, APIs, files)
   - Trust boundary mapping
   - High-risk component identification
   - Previous vulnerability analysis

2. **Authentication and Session Review**
   - Authentication mechanism analysis
   - Password storage and handling
   - Session management implementation
   - Multi-factor authentication integration
   - Account lockout and recovery mechanisms

3. **Access Control Review**
   - Authorization logic examination
   - Role-based access control validation
   - Insecure direct object reference detection
   - Privilege escalation possibilities
   - API endpoint access verification

4. **Input/Output Data Flow**
   - Input validation coverage analysis
   - Output encoding verification
   - Data transformation security
   - File handling operations review
   - Third-party integration security

5. **Cryptographic Implementation**
   - Encryption algorithm appropriateness
   - Key management practices
   - Random number generation security
   - Certificate validation
   - Sensitive data handling in memory

6. **Error Handling and Logging**
   - Exception handling patterns
   - Information disclosure in errors
   - Logging adequacy for security events
   - Debug information exposure
   - Fail-secure mechanism verification

Provide detailed findings with severity ratings, code locations, and remediation recommendations.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت مدقق كود أمني أول تجري مراجعة كود يدوية شاملة. طبق منهجية المراجعة المنظمة لتحديد الثغرات الأمنية في قاعدة الكود التالية.

معلومات قاعدة الكود:
[أدخل: لغة البرمجة، نوع التطبيق، الإطار، أسطر الكود، الوظائف الحرجة، آلية المصادقة، وصف تدفق البيانات]

وفقاً لدليل مراجعة الكود من OWASP وأفضل الممارسات الصناعية، قدم:

1. **تحليل ما قبل المراجعة**
   - فهم البنية ونمذجة التهديدات
   - تحديد نقاط الدخول (مدخلات المستخدم، APIs، الملفات)
   - رسم حدود الثقة
   - تحديد المكونات عالية المخاطر
   - تحليل الثغرات السابقة

2. **مراجعة المصادقة والجلسات**
   - تحليل آلية المصادقة
   - تخزين ومعالجة كلمات المرور
   - تنفيذ إدارة الجلسات
   - تكامل المصادقة متعددة العوامل
   - آليات قفل الحساب والاسترداد

3. **مراجعة التحكم في الوصول**
   - فحص منطق التفويض
   - التحقق من التحكم في الوصول القائم على الأدوار
   - اكتشاف الإشارة المباشرة غير الآمنة للكائنات
   - إمكانيات تصعيد الامتيازات
   - التحقق من الوصول لنقاط نهاية API

4. **تدفق بيانات الإدخال/الإخراج**
   - تحليل تغطية التحقق من المدخلات
   - التحقق من ترميز المخرجات
   - أمن تحويل البيانات
   - مراجعة عمليات التعامل مع الملفات
   - أمن التكاملات الخارجية

5. **التنفيذ التشفيري**
   - ملاءمة خوارزميات التشفير
   - ممارسات إدارة المفاتيح
   - أمن توليد الأرقام العشوائية
   - التحقق من الشهادات
   - التعامل مع البيانات الحساسة في الذاكرة

6. **معالجة الأخطاء والتسجيل**
   - أنماط معالجة الاستثناءات
   - كشف المعلومات في الأخطاء
   - كفاية التسجيل للأحداث الأمنية
   - كشف معلومات التصحيح
   - التحقق من آلية الفشل الآمن

قدم نتائج مفصلة مع تصنيفات الخطورة ومواقع الكود وتوصيات المعالجة.
```

---

## Example Output Preview

```
═══════════════════════════════════════════════════════
 MANUAL CODE REVIEW REPORT | تقرير مراجعة الكود اليدوية
═══════════════════════════════════════════════════════

EXECUTIVE SUMMARY
┌─────────────────────────────────────────────────────┐
│ Total Files Reviewed:     127                       │
│ Lines of Code:            45,230                    │
│ Findings:                 23                        │
│ Critical:                 3                         │
│ High:                     7                         │
│ Medium:                   8                         │
│ Low:                      5                         │
└─────────────────────────────────────────────────────┘

CRITICAL FINDINGS:
┌─────────────────────────────────────────────────────┐
│ [CRITICAL-001] SQL Injection in User Search        │
├─────────────────────────────────────────────────────┤
│ Location:    src/services/UserService.java:142     │
│ Severity:    CRITICAL                               │
│ CVSS Score:  9.8                                    │
│                                                     │
│ Vulnerable Code:                                    │
│ String query = "SELECT * FROM users WHERE name    │
│   LIKE '%" + searchTerm + "%'";                    │
│                                                     │
│ Impact:                                              │
│ - Full database access                              │
│ - Data exfiltration possible                        │
│ - Potential authentication bypass                   │
│                                                     │
│ Remediation:                                         │
│ Use parameterized queries:                          │
│ String query = "SELECT * FROM users WHERE name    │
│   LIKE ?";                                          │
│ stmt.setString(1, "%" + searchTerm + "%");         │
└─────────────────────────────────────────────────────┘

AUTHENTICATION REVIEW FINDINGS:
┌─────────────────────────────────────────────────────┐
│ [HIGH-002] Weak Password Policy                     │
│ Location:    src/controllers/AuthController.java:67│
│ Issue:       Minimum password length of 6 chars    │
│ Remediation: Implement minimum 12 chars with       │
│              complexity requirements               │
│                                                     │
│ [MEDIUM-005] Session Not Invalidated on Logout     │
│ Location:    src/filters/AuthFilter.java:89        │
│ Issue:       Session token remains valid after    │
│              logout                                 │
│ Remediation: Implement proper session destruction  │
└─────────────────────────────────────────────────────┘

TRUST BOUNDARY MAP:
┌─────────────────────────────────────────────────────┐
│                                                     │
│  [Internet] ──▶ [WAF] ──▶ [Load Balancer]          │
│                          │                          │
│                          ▼                          │
│              [API Gateway] ──▶ [Auth Service]      │
│                          │                          │
│                          ▼                          │
│                 [Application Servers]               │
│                          │                          │
│                          ▼                          │
│              [Database] ◀── [Cache]                │
│                                                     │
│  Trust Boundaries: ── ── ──                         │
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

## Prompt 2: Automated Static Analysis

### Description
Comprehensive guide to automated static application security testing (SAST), tool configuration, result interpretation, and false positive management.

### Tags
`sast` `static-analysis` `automated-scanning` `code-scanner`

---

## 🇬🇧 English Prompt

```
You are a DevSecOps engineer configuring and managing automated static analysis tools for a secure software development pipeline. Design and implement a comprehensive SAST strategy.

APPLICATION CONTEXT:
[Insert: programming language(s), build system, CI/CD platform, repository size, existing security tools, compliance requirements]

Following industry best practices for SAST implementation, provide:

1. **Tool Selection and Configuration**
   - Language-specific SAST tool recommendations
   - Commercial vs open-source tool comparison
   - Rule set customization and tuning
   - Baseline configuration establishment
   - Integration with IDE and CI/CD

2. **Scan Configuration**
   - Scan scope and exclusion patterns
   - Severity threshold configuration
   - Custom rule development for application-specific risks
   - Framework-specific security rules
   - Performance optimization settings

3. **CI/CD Pipeline Integration**
   - Pre-commit hook implementation
   - Pull request scanning automation
   - Branch protection policy integration
   - Build pipeline stages for SAST
   - Quality gate implementation

4. **Result Management and Triage**
   - False positive identification and suppression
   - Vulnerability prioritization framework
   - Result correlation across tools
   - Historical trend analysis
   - Risk acceptance workflow

5. **Remediation Workflow**
   - Developer notification mechanisms
   - Ticket creation automation
   - Remediation tracking and verification
   - Security champion program integration
   - Training recommendations based on findings

6. **Reporting and Metrics**
   - Executive dashboard design
   - Team-level security metrics
   - Vulnerability density calculations
   - Time-to-remediation tracking
   - Coverage and adoption metrics

Provide configuration examples for SonarQube, Semgrep, CodeQL, or language-specific tools.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت مهندس DevSecOps تقوم بتكوين وإدارة أدوات التحليل الثابت الآمن للتطبيقات لخط أنابيب تطوير برمجي آمن. صمم ونفذ استراتيجية SAST شاملة.

سياق التطبيق:
[أدخل: لغة/لغات البرمجة، نظام البناء، منصة CI/CD، حجم المستودع، أدوات الأمان الموجودة، متطلبات الامتثال]

وفقاً لأفضل الممارسات الصناعية لتنفيذ SAST، قدم:

1. **اختيار وتكوين الأداة**
   - توصيات أدوات SAST الخاصة بكل لغة
   - مقارنة الأدوات التجارية مقابل مفتوحة المصدر
   - تخصيص وضبط مجموعة القواعد
   - إنشاء تكوين خط الأساس
   - التكامل مع IDE و CI/CD

2. **تكوين الفحص**
   - نطاق الفحص وأنماط الاستبعاد
   - تكوين عتبة الخطورة
   - تطوير قواعد مخصصة للمخاطر الخاصة بالتطبيق
   - قواعد الأمان الخاصة بالإطار
   - إعدادات تحسين الأداء

3. **التكامل مع خط أنابيب CI/CD**
   - تنفيذ خطاف ما قبل الالتزام
   - أتمتة فحص طلبات السحب
   - تكامل سياسة حماية الفروع
   - مراحل خط الأناء للـ SAST
   - تنفيذ بوابة الجودة

4. **إدارة النتائج والفرز**
   - تحديد وكبت الإيجابيات الكاذبة
   - إطار أولوية الثغرات
   - ربط النتائج عبر الأدوات
   - تحليل الاتجاهات التاريخية
   - سير عمل قبول المخاطر

5. **سير عمل المعالجة**
   - آليات إشعار المطورين
   - أتمتة إنشاء التذاكر
   - تتبع المعالجة والتحقق
   - تكامل برنامج بطل الأمان
   - توصيات التدريب بناءً على النتائج

6. **إعداد التقارير والمقاييس**
   - تصميم لوحة التنفيذيين
   - مقاييس الأمان على مستوى الفريق
   - حسابات كثافة الثغرات
   - تتبع الوقت للمعالجة
   - مقاييس التغطية والاعتماد

قدم أمثلة تكوين لـ SonarQube، Semgrep، CodeQL، أو الأدوات الخاصة بكل لغة.
```

---

## Example Output Preview

```
═══════════════════════════════════════════════════════
 SAST CONFIGURATION GUIDE | دليل تكوين SAST
═══════════════════════════════════════════════════════

TOOL COMPARISON MATRIX:
┌─────────────────────────────────────────────────────┐
│ Tool        │ Languages │ License  │ CI/CD │ IDE   │
│─────────────│───────────│──────────│───────│───────│
│ SonarQube   │ 29+       │ Com/CE   │ ✓     │ ✓     │
│ Semgrep     │ 30+       │ MIT      │ ✓     │ ✓     │
│ CodeQL      │ 7+        │ GitHub   │ ✓     │ ✓     │
│ Checkmarx   │ 25+       │ Com      │ ✓     │ ✓     │
│ Snyk Code   │ 15+       │ Com      │ ✓     │ ✓     │
└─────────────────────────────────────────────────────┘

SEMGREP CONFIGURATION:
┌─────────────────────────────────────────────────────┐
│ # .semgrepconfig.yml                                │
│ rules:                                              │
│   - id: java-sql-injection                          │
│     patterns:                                       │
│       - pattern: $STMT.executeQuery($VAR)          │
│       - pattern-not: $STMT.executeQuery("...")     │
│     message: "Potential SQL injection"             │
│     severity: ERROR                                 │
│     languages: [java]                               │
│                                                     │
│   - id: python-hardcoded-secret                     │
│     patterns:                                       │
│       - pattern: $VAR = "..."                       │
│       - metavariable-regex:                         │
│           metavariable: $VAR                        │
│           regex: '(?i)(password|api_key|secret)'   │
│     message: "Hardcoded secret detected"           │
│     severity: WARNING                               │
│     languages: [python]                             │
└─────────────────────────────────────────────────────┘

GITHUB ACTIONS CI/CD INTEGRATION:
┌─────────────────────────────────────────────────────┐
│ name: Security Scan                                 │
│ on: [push, pull_request]                            │
│                                                     │
│ jobs:                                               │
│   semgrep:                                          │
│     runs-on: ubuntu-latest                          │
│     steps:                                          │
│       - uses: actions/checkout@v3                   │
│       - uses: returntocorp/semgrep-action@v1       │
│         with:                                       │
│           config: >-                                │
│             p/security-audit                        │
│             p/secrets                               │
│             p/owasp-top-ten                         │
│                                                     │
│   sonarqube:                                        │
│     runs-on: ubuntu-latest                          │
│     steps:                                          │
│       - uses: actions/checkout@v3                   │
│       - name: SonarQube Scan                        │
│         uses: sonarsource/sonarqube-scan-action    │
│         with:                                       │
│           args: >                                   │
│             -Dsonar.qualitygate.wait=true          │
│             -Dsonar.security.hotspots=true         │
└─────────────────────────────────────────────────────┘

QUALITY GATE THRESHOLDS:
┌─────────────────────────────────────────────────────┐
│ Metric                    │ Threshold │ Action      │
│───────────────────────────│───────────│─────────────│
│ Critical Vulnerabilities  │ 0         │ Block       │
│ High Vulnerabilities      │ 0         │ Block       │
│ Medium Vulnerabilities    │ <5        │ Warn        │
│ Coverage on New Code      │ >80%      │ Block       │
│ Duplicated Lines          │ <3%       │ Warn        │
│ Security Hotspots         │ 0         │ Block       │
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

## Prompt 3: Code Review for DevOps Pipeline

### Description
Comprehensive security code review methodology for CI/CD pipelines, infrastructure-as-code, and DevOps tooling with focus on pipeline security.

### Tags
`devops-security` `cicd-security` `pipeline-security` `infrastructure-as-code`

---

## 🇬🇧 English Prompt

```
You are a DevSecOps architect conducting a security review of CI/CD pipelines and DevOps infrastructure. Analyze the pipeline configuration and provide comprehensive security recommendations.

DEVOPS ENVIRONMENT:
[Insert: CI/CD platform (Jenkins/GitLab/GitHub Actions/Azure DevOps), deployment targets, infrastructure type, secrets management tool, container platform]

Following CIS Controls and DevSecOps best practices, provide:

1. **Pipeline Access Control**
   - Role-based access control for pipelines
   - Service account security
   - API token management
   - Webhook security configuration
   - Multi-approval requirements for sensitive operations

2. **Source Code Security**
   - Branch protection rules
   - Code review requirements
   - Signed commit enforcement
   - Merge request security
   - Repository access controls

3. **Build Process Security**
   - Build environment hardening
   - Dependency verification (SRI, checksums)
   - Build secret management
   - Artifact signing and verification
   - Reproducible builds

4. **Infrastructure-as-Code Security**
   - Terraform/CloudFormation security review
   - Kubernetes manifest security analysis
   - Dockerfile security best practices
   - Helm chart security review
   - Ansible playbook security

5. **Deployment Security**
   - Deployment approval workflows
   - Environment promotion security
   - Blue-green/canary deployment security
   - Rollback procedures
   - Production access controls

6. **Secrets Management**
   - Secret scanning in repositories
   - Vault integration patterns
   - Environment variable security
   - Secret rotation automation
   - Runtime secret injection

Provide pipeline configuration examples with security controls implemented.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت مهندس DevSecOps تجري مراجعة أمنية لخطوط أنابيب CI/CD والبنية التحتية DevOps. حلل تكوين خط الأنابيب وقدم توصيات أمنية شاملة.

بيئة DevOps:
[أدخل: منصة CI/CD (Jenkins/GitLab/GitHub Actions/Azure DevOps)، أهداف النشر، نوع البنية التحتية، أداة إدارة الأسرار، منصة الحاويات]

وفقاً لضوابط CIS وأفضل ممارسات DevSecOps، قدم:

1. **التحكم في الوصول لخط الأنابيب**
   - التحكم في الوصول القائم على الأدوار لخطوط الأنابيب
   - أمان حسابات الخدمة
   - إدارة رموز API
   - تكوين أمان Webhook
   - متطلبات الموافقة المتعددة للعمليات الحساسة

2. **أمن الكود المصدري**
   - قواعد حماية الفروع
   - متطلبات مراجعة الكود
   - إنفاذ الالتزامات الموقعة
   - أمان طلبات الدمج
   - ضوابط الوصول للمستودع

3. **أمن عملية البناء**
   - تقوية بيئة البناء
   - التحقق من التبعيات (SRI، البصمات)
   - إدارة أسرار البناء
   - توقيع والتحقق من التحف
   - البنيات القابلة للتكرار

4. **أمن البنية التحتية ككود**
   - مراجعة أمن Terraform/CloudFormation
   - تحليل أمن بيانات Kubernetes
   - أفضل ممارسات أمن Dockerfile
   - مراجعة أمن مخططات Helm
   - أمن playbooks لـ Ansible

5. **أمن النشر**
   - سير عمل موافقة النشر
   - أمن ترقية البيئات
   - أمن النشر الأزرق-الأخضر/الكناري
   - إجراءات التراجع
   - ضوابط الوصول للإنتاج

6. **إدارة الأسرار**
   - فحص الأسرار في المستودعات
   - أنماط التكامل مع Vault
   - أمان متغيرات البيئة
   - أتمتة تدوير الأسرار
   - حقن الأسرار أثناء التشغيل

قدم أمثلة تكوين خط الأنابيب مع ضوابط أمنية مطبقة.
```

---

## Example Output Preview

```
═══════════════════════════════════════════════════════
 DEVOPS SECURITY REVIEW | مراجعة أمن DevOps
═══════════════════════════════════════════════════════

PIPELINE SECURITY ARCHITECTURE:
┌─────────────────────────────────────────────────────┐
│                                                     │
│  [Developer] ──▶ [Git Repo] ──▶ [CI Pipeline]     │
│       │              │               │              │
│       │         Branch Prot    Security Scan       │
│       │         Signed Comm    Secret Scan         │
│       │                                              │
│       ▼              ▼               ▼              │
│  [Code Review] ──▶ [Build] ──▶ [Artifact Store]   │
│                          │               │          │
│                     SAST/SAST       Sign & Verify  │
│                     Image Scan                      │
│                          │                          │
│                          ▼                          │
│              [CD Pipeline] ──▶ [Production]        │
│                    │                                │
│              Approval Gate                          │
│              Config Validation                      │
│                                                     │
└─────────────────────────────────────────────────────┘

GITHUB ACTIONS SECURITY CONFIGURATION:
┌─────────────────────────────────────────────────────┐
│ name: Secure CI/CD Pipeline                         │
│                                                     │
│ on:                                                 │
│   pull_request:                                     │
│     branches: [main, production]                    │
│                                                     │
│ jobs:                                               │
│   security-gates:                                   │
│     runs-on: ubuntu-latest                          │
│     steps:                                          │
│       - name: Checkout with SHA pinning            │
│         uses: actions/checkout@b4ffde65f46336ab    │
│           88eb4be6c9d92eb29078a66b28d2d24           │
│                                                     │
│       - name: Secret Scanning                       │
│         uses: trufflesecurity/trufflehog@main      │
│                                                     │
│       - name: SAST Scan                             │
│         uses: github/codeql-action/analyze@v2      │
│         with:                                       │
│           config-file: .github/codeql-config.yml   │
│                                                     │
│       - name: Container Security                    │
│         uses: aquasecurity/trivy-action@master     │
│         with:                                       │
│           scan-type: 'fs'                           │
│           severity: 'CRITICAL,HIGH'                 │
│           exit-code: '1'                            │
│                                                     │
│   deploy:                                           │
│     needs: security-gates                           │
│     environment: production                         │
│     steps:                                          │
│       - name: Deploy with Approval                  │
│         run: ./deploy.sh                            │
└─────────────────────────────────────────────────────┘

BRANCH PROTECTION RULES:
┌─────────────────────────────────────────────────────┐
│ Rule                          │ Enforced │ Bypass   │
│───────────────────────────────│──────────│──────────│
│ Require PR before merge       │ ✓        │ Admin    │
│ Require approved PRs          │ ✓ (2)    │ None     │
│ Dismiss stale approvals       │ ✓        │ -        │
│ Require signed commits        │ ✓        │ None     │
│ Require status checks         │ ✓        │ None     │
│ Require linear history        │ ✓        │ -        │
│ Include administrators        │ ✓        │ -        │
└─────────────────────────────────────────────────────┘

DOCKERFILE SECURITY:
┌─────────────────────────────────────────────────────┐
│ # Secure Dockerfile Example                         │
│ FROM node:18-alpine AS builder                      │
│                                                     │
│ # Run as non-root                                   │
│ RUN addgroup -g 1001 appgroup && \                 │
│     adduser -u 1001 -G appgroup -D appuser         │
│                                                     │
│ # Copy with ownership                               │
│ COPY --chown=appuser:appgroup . /app               │
│                                                     │
│ # No secrets in build                               │
│ ARG NPM_TOKEN                                       │
│ RUN --mount=type=secret,id=npm_token \             │
│     npm ci                                          │
│                                                     │
│ # Minimal final image                               │
│ FROM gcr.io/distroless/nodejs18                    │
│ COPY --from=builder /app /app                      │
│ USER 1001                                           │
│ CMD ["server.js"]                                   │
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

## Prompt 4: Threat Modeling Code Review

### Description
Integration of threat modeling methodology into code review processes, focusing on STRIDE analysis and identifying architectural security weaknesses.

### Tags
`threat-modeling` `stride` `architecture-security` `risk-analysis`

---

## 🇬🇧 English Prompt

```
You are a security architect conducting threat model-driven code review. Apply STRIDE methodology to systematically identify security threats in the application architecture and implementation.

APPLICATION CONTEXT:
[Insert: application architecture, data flow diagram, trust boundaries, authentication methods, external integrations, sensitive data types, deployment topology]

Following Microsoft STRIDE threat modeling methodology, provide:

1. **Spoofing Threat Analysis**
   - Authentication mechanism review
   - Identity verification weaknesses
   - Session token security
   - Certificate validation issues
   - API authentication gaps

2. **Tampering Threat Analysis**
   - Data integrity verification
   - Input validation completeness
   - Database transaction security
   - File integrity monitoring
   - Configuration tampering risks

3. **Repudiation Threat Analysis**
   - Audit logging adequacy
   - Non-repudiation mechanisms
   - Transaction logging completeness
   - Log tampering prevention
   - User activity attribution

4. **Information Disclosure Analysis**
   - Data exposure paths
   - Error message leakage
   - Log sensitivity
   - Cache security
   - Memory dump vulnerabilities

5. **Denial of Service Analysis**
   - Resource exhaustion vectors
   - Input size limitations
   - Rate limiting implementation
   - Connection handling
   - Query optimization

6. **Elevation of Privilege Analysis**
   - Authorization bypass possibilities
   - Role escalation vulnerabilities
   - Insecure direct object references
   - Parameter tampering
   - Feature toggle abuse

Provide threat scenarios with likelihood/impact ratings and code-level mitigations.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت مهندس أمن معماري تجري مراجعة كود مدفوعة بنمذجة التهديدات. طبق منهجية STRIDE لتحديد التهديدات الأمنية بشكل منهجي في بنية التطبيق والتنفيذ.

سياق التطبيق:
[أدخل: بنية التطبيق، مخطط تدفق البيانات، حدود الثقة، طرق المصادقة، التكاملات الخارجية، أنواع البيانات الحساسة، طوبولوجيا النشر]

وفقاً لمنهجية نمذجة التهديدات STRIDE من Microsoft، قدم:

1. **تحليل تهديدات الانتحال (Spoofing)**
   - مراجعة آلية المصادقة
   - نقاط ضعف التحقق من الهوية
   - أمان رموز الجلسة
   - مشاكل التحقق من الشهادات
   - فجوات مصادقة API

2. **تحليل تهديدات التلاعب (Tampering)**
   - التحقق من سلامة البيانات
   - اكتمال التحقق من المدخلات
   - أمان معاملات قاعدة البيانات
   - مراقبة سلامة الملفات
   - مخاطر التلاعب بالتكوين

3. **تحليل تهديدات الإنكار (Repudiation)**
   - كفاية سجلات التدقيق
   - آليات عدم الإنكار
   - اكتمال تسجيل المعاملات
   - منع التلاعب بالسجلات
   - نسبة نشاط المستخدم

4. **تحليل كشف المعلومات (Information Disclosure)**
   - مسارات كشف البيانات
   - تسريب رسائل الخطأ
   - حساسية السجلات
   - أمان ذاكرة التخزين المؤقت
   - ثغرات تفريغ الذاكرة

5. **تحليل حرمان الخدمة (Denial of Service)**
   - متجهات استنزاف الموارد
   - قيود حجم المدخلات
   - تنفيذ الحد من المعدل
   - معالجة الاتصالات
   - تحسين الاستعلامات

6. **تحليل رفع الامتيازات (Elevation of Privilege)**
   - إمكانيات تجاوز التفويض
   - ثغرات تصعيد الأدوار
   - الإشارات المباشرة غير الآمنة للكائنات
   - التلاعب بالمعاملات
   - إساءة استخدام مفاتيح الميزات

قدم سيناريوهات التهديد مع تصنيفات الاحتمالية/التأثير والتخفيفات على مستوى الكود.
```

---

## Example Output Preview

```
═══════════════════════════════════════════════════════
 THREAT MODEL ANALYSIS | تحليل نمذجة التهديدات
═══════════════════════════════════════════════════════

DATA FLOW DIAGRAM:
┌─────────────────────────────────────────────────────┐
│                                                     │
│  ┌──────────┐     ┌──────────┐     ┌──────────┐   │
│  │  User    │────▶│   Web    │────▶│   API    │   │
│  │  Browser │     │  Server  │     │ Gateway  │   │
│  └──────────┘     └──────────┘     └──────────┘   │
│       │                │                │          │
│       │    [T1]        │    [T2]        │          │
│       │    Spoofing    │    Tampering   │          │
│       ▼                ▼                ▼          │
│  ┌──────────┐     ┌──────────┐     ┌──────────┐   │
│  │   Auth   │     │  Session │     │ Database │   │
│  │  Service │     │  Store   │     │  Server  │   │
│  └──────────┘     └──────────┘     └──────────┘   │
│       │                                  │          │
│       │         [T3] Info Disclosure     │          │
│       ▼                                  ▼          │
│  ┌──────────────────────────────────────────────┐  │
│  │              External API                    │  │
│  │         [T4] Elevation of Privilege          │  │
│  └──────────────────────────────────────────────┘  │
│                                                     │
│  Trust Boundary: ═══════════════════════════════    │
└─────────────────────────────────────────────────────┘

STRIDE THREAT MATRIX:
┌─────────────────────────────────────────────────────┐
│ Threat ID │ Type    │ Component   │ Likelihood │ Impact │ Risk │
│───────────│─────────│─────────────│────────────│────────│──────│
│ T001      │ Spoofing│ Auth API    │ High       │ High   │ Crit │
│ T002      │ Tamper  │ User Input  │ High       │ Med    │ High │
│ T003      │ Repud   │ Audit Log   │ Med        │ High   │ Med  │
│ T004      │ Info    │ Error Msg   │ Med        │ Med    │ Med  │
│ T005      │ DoS     │ API Gateway │ Low        │ High   │ Med  │
│ T006      │ Elev    │ Admin Panel │ Med        │ High   │ High │
└─────────────────────────────────────────────────────┘

DETAILED THREAT SCENARIO:
┌─────────────────────────────────────────────────────┐
│ T001 - Authentication Bypass (Spoofing)             │
├─────────────────────────────────────────────────────┤
│ Description:                                        │
│ JWT token validation accepts "none" algorithm,     │
│ allowing attackers to forge valid tokens.          │
│                                                     │
│ Attack Vector:                                      │
│ 1. Attacker creates JWT with alg: "none"           │
│ 2. Sets payload with admin privileges              │
│ 3. Server accepts token without signature check    │
│                                                     │
│ Affected Code:                                      │
│ // Vulnerable: No algorithm validation             │
│ const decoded = jwt.verify(token, secret, {        │
│   algorithms: ['HS256', 'RS256', 'none']  // BUG! │
│ });                                                 │
│                                                     │
│ Mitigation:                                         │
│ const decoded = jwt.verify(token, secret, {        │
│   algorithms: ['RS256'],  // Explicit allowlist    │
│   issuer: 'https://auth.example.com'               │
│ });                                                 │
│                                                     │
│ Risk Rating: CRITICAL                               │
│ Remediation Priority: P1                            │
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

## Prompt 5: Code Review Reporting and Documentation

### Description
Comprehensive framework for documenting code review findings, creating actionable reports, and tracking remediation progress.

### Tags
`code-review-report` `documentation` `remediation-tracking` `security-reporting`

---

## 🇬🇧 English Prompt

```
You are a security team lead responsible for code review documentation and reporting. Create comprehensive documentation standards and templates for security code review findings.

REVIEW CONTEXT:
[Insert: project name, review scope, team structure, stakeholder requirements, compliance obligations, timeline, previous findings]

Following industry standards for security documentation, provide:

1. **Finding Documentation Standards**
   - Severity classification criteria (CVSS integration)
   - Evidence capture requirements
   - Code snippet formatting
   - Proof-of-concept guidelines
   - Business impact articulation

2. **Technical Report Structure**
   - Executive summary format
   - Technical findings template
   - Remediation guidance format
   - Risk acceptance documentation
   - False positive justification template

3. **Remediation Tracking**
   - Issue tracking integration (JIRA, GitHub Issues)
   - SLA definitions by severity
   - Progress dashboard requirements
   - Escalation procedures
   - Verification checklist

4. **Metrics and KPIs**
   - Vulnerability density calculation
   - Time-to-remediation tracking
   - False positive rate measurement
   - Coverage metrics
   - Trend analysis methodology

5. **Communication Templates**
   - Developer notification format
   - Management escalation template
   - Compliance report format
   - Third-party audit support
   - Release blocking criteria

6. **Knowledge Base Development**
   - Secure coding pattern library
   - Vulnerability pattern documentation
   - Training material integration
   - Historical finding analysis
   - Team learning resources

Provide complete templates and examples for immediate use.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت قائد فريق أمن مسؤول عن توثيق وإعداد تقارير مراجعة الكود. أنشئ معايير توثيق وقوالب شاملة لنتائج مراجعة الكود الأمنية.

سياق المراجعة:
[أدخل: اسم المشروع، نطاق المراجعة، هيكل الفريق، متطلبات أصحاب المصلحة، الالتزامات التنظيمية، الجدول الزمني، النتائج السابقة]

وفقاً لمعايير الصناعة لتوثيق الأمان، قدم:

1. **معايير توثيق النتائج**
   - معايير تصنيف الخطورة (تكامل CVSS)
   - متطلبات التقاط الأدلة
   - تنسيق مقتطفات الكود
   - إرشادات إثبات المفهوم
   - صياغة تأثير الأعمال

2. **هيكل التقرير الفني**
   - تنسيق الملخص التنفيذي
   - قالب النتائج الفنية
   - تنسيق إرشادات المعالجة
   - توثيق قبول المخاطر
   - قالب تبرير الإيجابيات الكاذبة

3. **تتبع المعالجة**
   - تكامل تتبع المشكلات (JIRA، GitHub Issues)
   - تعريفات SLA حسب الخطورة
   - متطلبات لوحة التقدم
   - إجراءات التصعيد
   - قائمة التحقق من التحقق

4. **المقاييس والمؤشرات الرئيسية**
   - حساب كثافة الثغرات
   - تتبع الوقت للمعالجة
   - قياس معدل الإيجابيات الكاذبة
   - مقاييس التغطية
   - منهجية تحليل الاتجاهات

5. **قوالب التواصل**
   - تنسيق إشعار المطورين
   - قالب تصعيد الإدارة
   - تنسيق تقرير الامتثال
   - دعم التدقيق الخارجي
   - معايير حظر الإصدار

6. **تطوير قاعدة المعرفة**
   - مكتبة أنماط البرمجة الآمنة
   - توثيق أنماط الثغرات
   - تكامل مواد التدريب
   - تحليل النتائج التاريخية
   - موارد تعلم الفريق

قدم قوالب كاملة وأمثلة للاستخدام الفوري.
```

---

## Example Output Preview

```
═══════════════════════════════════════════════════════
 CODE REVIEW REPORT TEMPLATE | قالب تقرير مراجعة الكود
═══════════════════════════════════════════════════════

SECURITY CODE REVIEW REPORT
═══════════════════════════════════════════════════════

EXECUTIVE SUMMARY
┌─────────────────────────────────────────────────────┐
│ Project:          E-Commerce Platform               │
│ Review Period:    2024-01-15 to 2024-01-19         │
│ Reviewer:         Security Team Alpha              │
│ Report Version:   1.0                               │
│ Classification:   Confidential                      │
└─────────────────────────────────────────────────────┘

FINDINGS OVERVIEW:
┌─────────────────────────────────────────────────────┐
│ Severity    │ Count │ % Remediated │ Avg Fix Time  │
│─────────────│───────│──────────────│───────────────│
│ Critical    │   3   │     67%      │   2.3 days    │
│ High        │   7   │     43%      │   5.1 days    │
│ Medium      │  12   │     25%      │   8.7 days    │
│ Low         │   8   │     12%      │  14.2 days    │
│─────────────│───────│──────────────│───────────────│
│ TOTAL       │  30   │     33%      │   6.8 days    │
└─────────────────────────────────────────────────────┘

DETAILED FINDING TEMPLATE:
┌─────────────────────────────────────────────────────┐
│ FINDING: SEC-2024-001                               │
├─────────────────────────────────────────────────────┤
│ Title:          SQL Injection in Search Function    │
│ Severity:       CRITICAL                            │
│ CVSS Score:     9.8 (AV:N/AC:L/PR:N/UI:N/S:C       │
│                       /C:H/I:H/A:H)                │
│ Status:         Open                                │
│ Discovered:     2024-01-15                          │
│ Assigned To:    dev-team-backend                    │
│ SLA Due Date:   2024-01-17                          │
│                                                     │
│ AFFECTED COMPONENTS:                                │
│ - src/api/search.js:45-52                           │
│ - src/services/SearchService.js:78-91              │
│                                                     │
│ DESCRIPTION:                                        │
│ The search functionality accepts user input and    │
│ directly concatenates it into SQL queries without  │
│ proper sanitization, allowing attackers to        │
│ execute arbitrary SQL commands.                    │
│                                                     │
│ VULNERABLE CODE:                                    │
│ const query = `SELECT * FROM products              │
│   WHERE name LIKE '%${searchTerm}%'`;              │
│ const results = await db.execute(query);           │
│                                                     │
│ PROOF OF CONCEPT:                                   │
│ Input: "'; DROP TABLE products; --"                │
│ Impact: Complete database compromise                │
│                                                     │
│ REMEDIATION:                                        │
│ Use parameterized queries:                          │
│ const query = `SELECT * FROM products              │
│   WHERE name LIKE ?`;                              │
│ const results = await db.execute(query,            │
│   [`%${searchTerm}%`]);                            │
│                                                     │
│ BUSINESS IMPACT:                                    │
│ - Potential data breach affecting 500K+ users      │
│ - Regulatory fines under GDPR: up to €20M         │
│ - Reputational damage and customer trust loss      │
│                                                     │
│ REFERENCES:                                         │
│ - OWASP A03:2021 – Injection                        │
│ - CWE-89: SQL Injection                             │
│ - https://cheatsheetseries.owasp.org/...          │
└─────────────────────────────────────────────────────┘

REMEDIATION TRACKING DASHBOARD:
┌─────────────────────────────────────────────────────┐
│ Week 3 Summary - January 2024                       │
├─────────────────────────────────────────────────────┤
│                                                     │
│ Critical Issues: ████░░░░ 3/3 Open (2 overdue)     │
│ High Issues:     ████████░ 7/7 Open (5 in progress)│
│ Medium Issues:   ████████░░░░ 12/12 (3 fixed)     │
│ Low Issues:      ████████░░░░░░ 8/8 (1 fixed)     │
│                                                     │
│ Time to Remediation:                                │
│ - Critical: 2.3 days (Target: 1 day) - OVERDUE     │
│ - High:     5.1 days (Target: 3 days) - OVERDUE    │
│ - Medium:   8.7 days (Target: 7 days) - ON TRACK   │
│                                                     │
│ Top Finding Categories:                             │
│ 1. Injection Vulnerabilities: 12                    │
│ 2. Authentication Issues: 8                         │
│ 3. Access Control: 6                                │
│ 4. Cryptography: 4                                  │
└─────────────────────────────────────────────────────┘
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team
