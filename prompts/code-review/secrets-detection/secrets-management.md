# Secrets Detection and Management Prompts

A comprehensive collection of bilingual (English/Arabic) prompts for secrets detection and management, covering hardcoded secrets, API key exposure, and credential scanning.

---

## Prompt 1: Hardcoded Secrets Detection

### Description
Comprehensive methodology for detecting hardcoded secrets, credentials, and sensitive data in source code repositories.

### Tags
`secrets-detection` `hardcoded-credentials` `credential-scanning` `git-secrets`

---

## 🇬🇧 English Prompt

```
You are a security specialist conducting comprehensive secrets detection in source code. Analyze the codebase for hardcoded secrets and provide remediation guidance.

CODEBASE CONTEXT:
[Insert: programming language(s), repository size, number of files, sensitive services (AWS/GCP/Azure/Databases), compliance requirements, CI/CD platform]

Following OWASP and secrets management best practices, provide:

1. **Secrets Pattern Detection**
   - API keys and tokens (AWS, Azure, GCP, GitHub)
   - Database connection strings
   - Password and username combinations
   - Private keys (RSA, SSH, PGP)
   - OAuth client secrets
   - Encryption keys and salts

2. **Detection Techniques**
   - Regular expression pattern matching
   - Entropy analysis for high-randomness strings
   - Context-aware detection (variable names, comments)
   - Configuration file analysis
   - Environment variable leakage
   - Log file sensitive data exposure

3. **High-Risk Locations**
   - Source code files (all languages)
   - Configuration files (.env, config.yml, settings.py)
   - Infrastructure as Code (Terraform, CloudFormation)
   - Container definitions (Dockerfile, docker-compose)
   - CI/CD configuration files
   - Documentation and README files

4. **False Positive Management**
   - Test fixture identification
   - Placeholder value detection
   - Public key vs private key distinction
   - Example code patterns
   - Documentation patterns

5. **Remediation Strategies**
   - Secret removal from history (BFG, git-filter-repo)
   - Secret rotation procedures
   - Environment variable implementation
   - Secrets manager integration (Vault, AWS Secrets Manager)
   - Pre-commit hook implementation

6. **Prevention Measures**
   - Pre-commit scanning tools (git-secrets, detect-secrets)
   - CI/CD pipeline integration
   - Developer training requirements
   - Code review checklist items
   - Security policy enforcement

Provide detection regex patterns and remediation scripts.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت متخصص أمن تجري اكتشاف شامل للأسرار في الكود المصدري. حلل قاعدة الكود للأسرار المضمنة وقدم إرشادات المعالجة.

سياق قاعدة الكود:
[أدخل: لغة/لغات البرمجة، حجم المستودع، عدد الملفات، الخدمات الحساسة (AWS/GCP/Azure/قواعد البيانات)، متطلبات الامتثال، منصة CI/CD]

وفقاً لـ OWASP وأفضل ممارسات إدارة الأسرار، قدم:

1. **اكتشاف أنماط الأسرار**
   - مفاتيح ورموز API (AWS، Azure، GCP، GitHub)
   - سلاسل اتصال قواعد البيانات
   - مجموعات كلمات المرور وأسماء المستخدمين
   - المفاتيح الخاصة (RSA، SSH، PGP)
   - أسرار عميل OAuth
   - مفاتيح وأملاح التشفير

2. **تقنيات الاكتشاف**
   - مطابقة أنماط التعبيرات النمطية
   - تحليل الإنتروبي للسلاسل عالية العشوائية
   - الاكتشاف الواعي بالسياق (أسماء المتغيرات، التعليقات)
   - تحليل ملفات التكوين
   - تسريب متغيرات البيئة
   - كشف البيانات الحساسة في ملفات السجل

3. **المواقع عالية المخاطر**
   - ملفات الكود المصدري (جميع اللغات)
   - ملفات التكوين (.env، config.yml، settings.py)
   - البنية التحتية ككود (Terraform، CloudFormation)
   - تعريفات الحاويات (Dockerfile، docker-compose)
   - ملفات تكوين CI/CD
   - التوثيق وملفات README

4. **إدارة الإيجابيات الكاذبة**
   - تحديد أدوات الاختبار
   - اكتشاف القيم النائبة
   - التمييز بين المفتاح العام والخاص
   - أنماط الكود المثال
   - أنماط التوثيق

5. **استراتيجيات المعالجة**
   - إزالة السر من السجل (BFG، git-filter-repo)
   - إجراءات تدوير السر
   - تنفيذ متغيرات البيئة
   - تكامل مدير الأسرار (Vault، AWS Secrets Manager)
   - تنفيذ خطاف ما قبل الالتزام

6. **تدابير الوقاية**
   - أدوات المسح قبل الالتزام (git-secrets، detect-secrets)
   - التكامل مع خط أنابيب CI/CD
   - متطلبات تدريب المطورين
   - عناصر قائمة التحقق من مراجعة الكود
   - إنفاذ سياسة الأمان

قدم أنماط regex للاكتشاف ونصوص المعالجة.
```

---

## Example Output Preview

```
═══════════════════════════════════════════════════════
 SECRETS DETECTION REPORT | تقرير اكتشاف الأسرار
═══════════════════════════════════════════════════════

EXECUTIVE SUMMARY:
┌─────────────────────────────────────────────────────┐
│ Total Files Scanned:       12,456                   │
│ Secrets Detected:          23                       │
│ Critical:                   8                       │
│ High:                       7                       │
│ Medium:                     5                       │
│ Low:                        3                       │
│ Files Requiring Remediation: 15                     │
└─────────────────────────────────────────────────────┘

CRITICAL FINDING - AWS ACCESS KEY:
┌─────────────────────────────────────────────────────┐
│ File: src/config/database.js:23                     │
│ Type: AWS Access Key ID                              │
│ Severity: CRITICAL                                   │
│ Entropy Score: 4.23 (High)                          │
│                                                     │
│ ❌ VULNERABLE CODE:                                 │
│ const AWS = require('aws-sdk');                    │
│ AWS.config.update({                                 │
│   accessKeyId: 'AKIAIOSFODNN7EXAMPLE',            │
│   secretAccessKey: 'wJalrXUtnFEMI/K7MDENG/        │
│     bPxRfiCYEXAMPLEKEY',                            │
│   region: 'us-east-1'                               │
│ });                                                 │
│                                                     │
│ ✅ SECURE CODE:                                     │
│ const AWS = require('aws-sdk');                    │
│ AWS.config.update({                                 │
│   accessKeyId: process.env.AWS_ACCESS_KEY_ID,     │
│   secretAccessKey: process.env.AWS_SECRET_ACCESS_KEY,│
│   region: process.env.AWS_REGION                   │
│ });                                                 │
│                                                     │
│ REMEDIATION STEPS:                                  │
│ 1. Rotate AWS credentials immediately              │
│ 2. Remove from git history:                         │
│    git filter-branch --force --index-filter \      │
│      'git rm --cached --ignore-unmatch \           │
│       src/config/database.js' HEAD                 │
│ 3. Force push to overwrite remote                  │
│ 4. Add to .gitignore: *.env, secrets/              │
└─────────────────────────────────────────────────────┘

DETECTION PATTERNS:
┌─────────────────────────────────────────────────────┐
│ Pattern Name          │ Regex                           │ Matches │
│───────────────────────│─────────────────────────────────│─────────│
│ AWS Access Key ID     │ AKIA[0-9A-Z]{16}               │    3    │
│ AWS Secret Key        │ [A-Za-z0-9/+=]{40}             │    2    │
│ GitHub Token          │ ghp_[a-zA-Z0-9]{36}            │    1    │
│ Slack Token           │ xox[baprs]-[0-9]{10,13}        │    2    │
│ Private SSH Key       │ -----BEGIN RSA PRIVATE KEY-----│    1    │
│ Database URL          │ postgresql://[^:]+:[^@]+@      │    4    │
│ JWT Secret            │ (jwt|token).*=.*['"][^'" ]{20,}│    3    │
│ Generic API Key       │ (api[_-]?key|apikey).*=.*['"][^'" ]{10,}│ 7 │
└─────────────────────────────────────────────────────┘

PRE-COMMIT HOOK CONFIGURATION:
┌─────────────────────────────────────────────────────┐
│ # .pre-commit-config.yaml                           │
│ repos:                                              │
│   - repo: https://github.com/gitleaks/gitleaks     │
│     rev: v8.18.0                                    │
│     hooks:                                          │
│       - id: gitleaks                                │
│                                                     │
│   - repo: https://github.com/Yelp/detect-secrets   │
│     rev: v1.4.0                                     │
│     hooks:                                          │
│       - id: detect-secrets                          │
│         args: ['--baseline', '.secrets.baseline']  │
│                                                     │
│   - repo: https://github.com/pre-commit/pre-commit-hooks│
│     rev: v4.5.0                                     │
│     hooks:                                          │
│       - id: detect-private-key                     │
│       - id: detect-aws-credentials                  │
│         args: ['--allow-missing-credentials']      │
└─────────────────────────────────────────────────────┘

GIT HISTORY CLEANUP:
┌─────────────────────────────────────────────────────┐
│ # Using BFG Repo-Cleaner                            │
│                                                     │
│ # 1. Clone fresh copy                               │
│ git clone --mirror git@github.com:org/repo.git     │
│                                                     │
│ # 2. Create file with secrets to remove            │
│ echo 'AKIAIOSFODNN7EXAMPLE' > secrets.txt          │
│ echo 'wJalrXUtnFEMI/K7MDENG/bPxRfiCYEXAMPLEKEY' >> secrets.txt│
│                                                     │
│ # 3. Run BFG                                        │
│ java -jar bfg.jar --replace-text secrets.txt repo.git│
│                                                     │
│ # 4. Clean up                                       │
│ cd repo.git                                         │
│ git reflog expire --expire=now --all               │
│ git gc --prune=now --aggressive                    │
│                                                     │
│ # 5. Force push                                     │
│ git push --force                                    │
│                                                     │
│ # 6. Rotate all exposed credentials                 │
└─────────────────────────────────────────────────────┘

SECRETS BASELINE FILE:
┌─────────────────────────────────────────────────────┐
│ {                                                   │
│   "version": "1.4.0",                              │
│   "plugins_used": [{                                │
│     "name": "AWSKeyDetector"                       │
│   }],                                               │
│   "filters_used": [{                                │
│     "path": "spec/**"                              │
│   }],                                               │
│   "results": [{                                     │
│     "filename": "tests/fixtures/mock_credentials.json",│
│     "is_verified": false,                          │
│     "line_number": 5,                               │
│     "type": "AWS Access Key",                       │
│     "is_secret": false                              │
│   }]                                                │
│ }                                                   │
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

## Prompt 2: API Key and Token Exposure

### Description
Comprehensive guide to detecting and preventing API key and token exposure across various platforms and services.

### Tags
`api-keys` `token-exposure` `credential-leakage` `oauth-security`

---

## 🇬🇧 English Prompt

```
You are a security analyst specializing in API security and credential exposure. Analyze the codebase and infrastructure for API key and token vulnerabilities.

SERVICE CONTEXT:
[Insert: external services used (Stripe, Twilio, SendGrid, GitHub), API management platform, authentication methods, rate limiting, compliance requirements]

Following API security best practices, provide:

1. **API Key Pattern Detection**
   - REST API keys (Stripe, Twilio, SendGrid)
   - OAuth tokens and client secrets
   - Bearer tokens and JWT secrets
   - Service account keys
   - Webhook signing secrets
   - Integration tokens

2. **Exposure Vectors Analysis**
   - Source code repositories
   - Client-side JavaScript exposure
   - Mobile application decompilation risks
   - Log file leakage
   - Error message exposure
   - Documentation and help files

3. **Platform-Specific Patterns**
   - AWS (Access Key ID, Secret Key, Session Token)
   - GCP (Service Account JSON, API Keys)
   - Azure (Connection Strings, SAS Tokens)
   - GitHub (Personal Access Tokens, App Tokens)
   - Slack (Bot Tokens, Webhook URLs)
   - Stripe (Secret Keys, Publishable Keys)

4. **Detection Methodology**
   - Static code analysis
   - Dynamic analysis (network traffic)
   - Repository scanning
   - Log analysis
   - Browser dev tools analysis
   - Mobile app security testing

5. **Mitigation Strategies**
   - API key rotation automation
   - Scoped token implementation
   - IP whitelisting
   - Referrer restrictions
   - Key usage monitoring
   - Anomaly detection

6. **Incident Response**
   - Immediate key revocation
   - Key rotation procedures
   - Impact assessment
   - Logging and forensic analysis
   - Stakeholder notification
   - Preventive measures implementation

Provide detection rules and mitigation configurations.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت محلل أمن متخصص في أمن API والتعرض لبيانات الاعتماد. حلل قاعدة الكود والبنية التحتية للثغرات المتعلقة بمفاتيح API ورموز الوصول.

سياق الخدمة:
[أدخل: الخدمات الخارجية المستخدمة (Stripe، Twilio، SendGrid، GitHub)، منصة إدارة API، طرق المصادقة، الحد من المعدل، متطلبات الامتثال]

وفقاً لأفضل ممارسات أمن API، قدم:

1. **اكتشاف أنماط مفاتيح API**
   - مفاتيح REST API (Stripe، Twilio، SendGrid)
   - رموز OAuth وأسرار العميل
   - رموز Bearer وأسرار JWT
   - مفاتيح حسابات الخدمة
   - أسرار توقيع Webhook
   - رموز التكامل

2. **تحليل متجهات التعرض**
   - مستودعات الكود المصدري
   - التعرض في JavaScript من جانب العميل
   - مخاطر فك تجميع تطبيقات الهاتف
   - تسريب ملفات السجل
   - كشف رسائل الخطأ
   - التوثيق وملفات المساعدة

3. **الأنماط الخاصة بكل منصة**
   - AWS (معرف مفتاح الوصول، المفتاح السري، رمز الجلسة)
   - GCP (JSON حساب الخدمة، مفاتيح API)
   - Azure (سلاسل الاتصال، رموز SAS)
   - GitHub (رموز الوصول الشخصية، رموز التطبيق)
   - Slack (رموز البوت، عناوين URL للـ Webhook)
   - Stripe (المفاتيح السرية، المفاتيح القابلة للنشر)

4. **منهجية الاكتشاف**
   - التحليل الثابت للكود
   - التحليل الديناميكي (حركة مرور الشبكة)
   - مسح المستودعات
   - تحليل السجلات
   - تحليل أدوات المطور في المتصفح
   - اختبار أمن تطبيقات الهاتف

5. **استراتيجيات التخفيف**
   - أتمتة تدوير مفاتيح API
   - تنفيذ الرموز المحددة النطاق
   - القائمة البيضاء للـ IP
   - قيود المُحيل
   - مراقبة استخدام المفاتيح
   - اكتشاف الشذوذ

6. **الاستجابة للحوادث**
   - إلغاء المفتاح الفوري
   - إجراءات تدوير المفتاح
   - تقييم التأثير
   - التسجيل والتحليل الجنائي
   - إشعار أصحاب المصلحة
   - تنفيذ التدابير الوقائية

قدم قواعد الاكتشاف وتكوينات التخفيف.
```

---

## Example Output Preview

```
═══════════════════════════════════════════════════════
 API KEY EXPOSURE REPORT | تقرير تعرض مفاتيح API
═══════════════════════════════════════════════════════

EXPOSED CREDENTIALS SUMMARY:
┌─────────────────────────────────────────────────────┐
│ Service          │ Type         │ Severity │ Status │
│──────────────────│──────────────│──────────│────────│
│ Stripe           │ Secret Key   │ Critical │ Rotated│
│ GitHub           │ Personal Token│ High    │ Rotated│
│ Slack            │ Bot Token    │ High     │ Rotated│
│ AWS              │ Access Key   │ Critical │ Pending│
│ SendGrid         │ API Key      │ High     │ Rotated│
│ Twilio           │ Auth Token   │ Critical │ Rotated│
└─────────────────────────────────────────────────────┘

API KEY PATTERN LIBRARY:
┌─────────────────────────────────────────────────────┐
│ Service   │ Key Pattern                    │ Example Prefix │
│───────────│────────────────────────────────│────────────────│
│ Stripe    │ sk_live_[a-zA-Z0-9]{24}       │ sk_live_       │
│ Stripe    │ sk_test_[a-zA-Z0-9]{24}       │ sk_test_       │
│ GitHub    │ ghp_[a-zA-Z0-9]{36}           │ ghp_           │
│ GitHub    │ github_pat_[a-zA-Z0-9]{22}    │ github_pat_    │
│ Slack     │ xoxb-[0-9]{10,13}-[a-zA-Z0-9]{24}│ xoxb-      │
│ AWS       │ AKIA[A-Z0-9]{16}              │ AKIA           │
│ Twilio    │ AC[a-f0-9]{32}                │ AC             │
│ SendGrid  │ SG.[a-zA-Z0-9_-]{22}\.[a-zA-Z0-9_-]{43}│ SG.    │
│ GCP       │ AIza[a-zA-Z0-9_-]{35}         │ AIza           │
│ Azure     │ [a-zA-Z0-9]{8}-[a-zA-Z0-9]{4}-[a-zA-Z0-9]{4}│ Various │
└─────────────────────────────────────────────────────┘

CLIENT-SIDE EXPOSURE DETECTION:
┌─────────────────────────────────────────────────────┐
│ ❌ VULNERABLE:                                      │
│ // frontend/src/api/payment.js                     │
│ const stripe = Stripe('sk_live_example_redacted_key');│
│ // Secret key exposed in client-side code!        │
│                                                     │
│ ✅ SECURE:                                          │
│ // frontend/src/api/payment.js                     │
│ const stripe = Stripe(process.env.STRIPE_PUBLIC_KEY);│
│ // Only use publishable keys client-side          │
│                                                     │
│ // backend/src/routes/payment.js                   │
│ const stripe = require('stripe')(process.env.STRIPE_SECRET_KEY);│
└─────────────────────────────────────────────────────┘

LOG EXPOSURE DETECTION:
┌─────────────────────────────────────────────────────┐
│ ❌ VULNERABLE LOG OUTPUT:                           │
│ [INFO] Payment processed with card token: tok_visa │
│ [DEBUG] API Request: Authorization: Bearer ghp_xxx │
│ [ERROR] Database connection: postgresql://user:pass│
│                                                     │
│ ✅ SECURE LOG OUTPUT:                               │
│ [INFO] Payment processed: txn_12345                │
│ [DEBUG] API Request: Authorization: [REDACTED]     │
│ [ERROR] Database connection: [CONNECTION_FAILED]   │
└─────────────────────────────────────────────────────┘

API KEY SCOPING RECOMMENDATIONS:
┌─────────────────────────────────────────────────────┐
│ Service   │ Recommended Scope                 │ Actions│
│───────────│───────────────────────────────────│────────│
│ GitHub    │ Read-only for CI/CD               │ Pull   │
│ Stripe    │ Read + Write (no delete)          │ Charges│
│ AWS       │ Least privilege IAM role          │ S3, EC2│
│ Slack     │ Specific channels only            │ Post   │
│ SendGrid  │ Specific sender domain            │ Send   │
│ Twilio    │ Specific phone numbers            │ SMS    │
└─────────────────────────────────────────────────────┘

KEY ROTATION AUTOMATION:
┌─────────────────────────────────────────────────────┐
│ #!/bin/bash                                         │
│ # Automated key rotation script                     │
│                                                     │
│ # Rotate Stripe key                                 │
│ NEW_KEY=$(curl -s -X POST \                        │
│   "https://api.stripe.com/v1/api_keys" \           │
│   -u "$STRIPE_SECRET_KEY:" \                       │
│   -d "name=Production Key $(date +%Y%m%d)" \       │
│   -d "type=secret" | jq -r '.secret_key')          │
│                                                     │
│ # Update secrets manager                            │
│ aws secretsmanager update-secret \                  │
│   --secret-id prod/stripe/secret-key \             │
│   --secret-string "$NEW_KEY"                       │
│                                                     │
│ # Trigger application restart                       │
│ kubectl rollout restart deployment/api-server      │
│                                                     │
│ # Verify new key works                              │
│ curl -s -X GET "https://api.stripe.com/v1/charges" \│
│   -u "$NEW_KEY:" | jq -r '.object'                 │
└─────────────────────────────────────────────────────┘

MONITORING CONFIGURATION:
┌─────────────────────────────────────────────────────┐
│ # CloudWatch Alarm for unusual API key usage       │
│ {                                                   │
│   "AlarmName": "API-Key-Anomaly-Detection",        │
│   "MetricName": "APIRequestCount",                 │
│   "Threshold": 1000,                               │
│   "EvaluationPeriods": 1,                          │
│   "DatapointsToAlarm": 1,                          │
│   "ComparisonOperator": "GreaterThanThreshold",   │
│   "TreatMissingData": "breaching",                 │
│   "AlarmActions": ["arn:aws:sns:security-alerts"] │
│ }                                                   │
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

## Prompt 3: Credential Scanning Automation

### Description
Comprehensive framework for implementing automated credential scanning across the software development lifecycle.

### Tags
`credential-scanning` `automation` `ci-cd-security` `gitleaks`

---

## 🇬🇧 English Prompt

```
You are a DevSecOps engineer implementing automated credential scanning infrastructure. Design a comprehensive credential scanning automation system.

INFRASTRUCTURE CONTEXT:
[Insert: repository count, CI/CD platform, secret management tool, compliance requirements, alerting systems, development workflow]

Following security automation best practices, provide:

1. **Scanning Tool Selection**
   - Gitleaks configuration and deployment
   - TruffleHog integration patterns
   - Git-secrets implementation
   - Detect-secrets baseline management
   - Commercial tool comparison (GitGuardian, Snyk)

2. **Pre-Commit Integration**
   - Git hooks implementation
   - IDE plugin recommendations
   - Local scanning workflow
   - Developer experience optimization
   - False positive handling

3. **CI/CD Pipeline Integration**
   - Pull request scanning
   - Branch protection integration
   - Pipeline stage configuration
   - Failure handling policies
   - Remediation workflow

4. **Historical Scanning**
   - Full repository history scan
   - Incremental scan optimization
   - Large repository handling
   - Multi-repository scanning
   - Scan result aggregation

5. **Alert and Response Automation**
   - Alert routing configuration
   - Severity-based escalation
   - JIRA/ticket integration
   - Slack/Teams notifications
   - On-call integration

6. **Metrics and Reporting**
   - Scan coverage metrics
   - Time-to-remediation tracking
   - False positive rate
   - Trend analysis
   - Compliance reporting

Provide complete configuration files and integration scripts.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت مهندس DevSecOps تنفذ بنية تحتية للمسح الآلي لبيانات الاعتماد. صمم نظام أتمتة مسح بيانات الاعتماد الشامل.

سياق البنية التحتية:
[أدخل: عدد المستودعات، منصة CI/CD، أداة إدارة الأسرار، متطلبات الامتثال، أنظمة التنبيه، سير عمل التطوير]

وفقاً لأفضل ممارسات أتمتة الأمان، قدم:

1. **اختيار أداة المسح**
   - تكوين ونشر Gitleaks
   - أنماط تكامل TruffleHog
   - تنفيذ Git-secrets
   - إدارة خط أساس Detect-secrets
   - مقارنة الأدوات التجارية (GitGuardian، Snyk)

2. **التكامل قبل الالتزام**
   - تنفيذ خطافات Git
   - توصيات إضافات IDE
   - سير عمل المسح المحلي
   - تحسين تجربة المطور
   - التعامل مع الإيجابيات الكاذبة

3. **التكامل مع خط أنابيب CI/CD**
   - مسح طلبات السحب
   - تكامل حماية الفروع
   - تكوين مرحلة خط الأنابيب
   - سياسات التعامل مع الفشل
   - سير عمل المعالجة

4. **المسح التاريخي**
   - مسح السجل الكامل للمستودع
   - تحسين المسح التزايدي
   - التعامل مع المستودعات الكبيرة
   - مسح المستودعات المتعددة
   - تجميع نتائج المسح

5. **أتمتة التنبيه والاستجابة**
   - تكوين توجيه التنبيهات
   - التصعيد بناءً على الخطورة
   - تكامل JIRA/التذاكر
   - إشعارات Slack/Teams
   - تكامل نظام المناوبات

6. **المقاييس والتقارير**
   - مقاييس تغطية المسح
   - تتبع الوقت للمعالجة
   - معدل الإيجابيات الكاذبة
   - تحليل الاتجاهات
   - تقارير الامتثال

قدم ملفات تكوين كاملة ونصوص التكامل.
```

---

## Example Output Preview

```
═══════════════════════════════════════════════════════
 CREDENTIAL SCANNING AUTOMATION | أتمتة مسح بيانات الاعتماد
═══════════════════════════════════════════════════════

SCANNING ARCHITECTURE:
┌─────────────────────────────────────────────────────┐
│                                                     │
│  [Developer Workstation]                            │
│       │                                             │
│       │ git commit                                  │
│       ▼                                             │
│  ┌─────────────────────────────────────────────┐   │
│  │ Pre-commit Hook                              │   │
│  │ • Gitleaks scan                             │   │
│  │ • Custom regex patterns                     │   │
│  │ • Block on secret detection                 │   │
│  └─────────────────────────────────────────────┘   │
│       │ Pass                                        │
│       ▼                                             │
│  [Push to Repository]                               │
│       │                                             │
│       ▼                                             │
│  ┌─────────────────────────────────────────────┐   │
│  │ CI/CD Pipeline                               │   │
│  │ • Full repository scan                      │   │
│  │ • Historical commit analysis                │   │
│  │ • Generate report                           │   │
│  └─────────────────────────────────────────────┘   │
│       │                                             │
│       ├─ Pass ─▶ [Merge Allowed]                   │
│       │                                             │
│       └─ Fail ─▶ [Alert & Block]                   │
│                    │                                │
│                    ▼                                │
│           ┌─────────────────┐                      │
│           │ Security Team   │                      │
│           │ JIRA Ticket     │                      │
│           │ Slack Alert     │                      │
│           └─────────────────┘                      │
│                                                     │
└─────────────────────────────────────────────────────┘

GITLEAKS CONFIGURATION:
┌─────────────────────────────────────────────────────┐
│ # .gitleaks.toml                                    │
│ title = "Custom Gitleaks Configuration"            │
│                                                     │
│ [extend]                                            │
│ useDefault = true                                   │
│                                                     │
│ [[rules]]                                           │
│ id = "custom-api-key"                               │
│ description = "Custom API Key Pattern"             │
│ regex = '''(?i)(api[_-]?key|apikey)[\s:=]+['"]?[a-zA-Z0-9]{20,}['"]?'''│
│ tags = ["api", "key"]                              │
│                                                     │
│ [[rules]]                                           │
│ id = "internal-secret"                              │
│ description = "Internal Secret Pattern"            │
│ regex = '''COMPANY_SECRET_[A-Z0-9]{32}'''          │
│ tags = ["internal", "secret"]                      │
│                                                     │
│ [allowlist]                                         │
│ description = "Global allowlist"                   │
│ paths = [                                           │
│   '''^tests/''',                                   │
│   '''^fixtures/''',                                │
│   '''\.example$''',                                │
│ ]                                                   │
│ regexes = [                                         │
│   '''AKIAIOSFODNN7EXAMPLE''',  # AWS example key  │
│   '''sk_test_example_redacted_key''', # Stripe test│
│ ]                                                   │
└─────────────────────────────────────────────────────┘

GITHUB ACTIONS WORKFLOW:
┌─────────────────────────────────────────────────────┐
│ name: Secret Scanning                               │
│ on:                                                 │
│   push:                                             │
│     branches: [main, develop]                       │
│   pull_request:                                     │
│     branches: [main]                                │
│                                                     │
│ jobs:                                               │
│   gitleaks:                                         │
│     runs-on: ubuntu-latest                          │
│     steps:                                          │
│       - uses: actions/checkout@v3                   │
│         with:                                       │
│           fetch-depth: 0  # Full history           │
│                                                     │
│       - name: Run Gitleaks                          │
│         uses: gitleaks/gitleaks-action@v2          │
│         env:                                        │
│           GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}│
│           GITLEAKS_LICENSE: ${{ secrets.GITLEAKS_LICENSE }}│
│         with:                                       │
│           config-path: .gitleaks.toml              │
│           report-format: sarif                      │
│           report-path: results.sarif               │
│                                                     │
│       - name: Upload SARIF results                  │
│         uses: github/codeql-action/upload-sarif@v2 │
│         with:                                       │
│           sarif_file: results.sarif                │
│                                                     │
│   trufflehog:                                       │
│     runs-on: ubuntu-latest                          │
│     steps:                                          │
│       - uses: actions/checkout@v3                   │
│         with:                                       │
│           fetch-depth: 0                            │
│                                                     │
│       - name: TruffleHog Scan                       │
│         uses: trufflesecurity/trufflehog@main      │
│         with:                                       │
│           path: ./                                  │
│           base: ${{ github.event.repository.default_branch }}│
│           extra_args: --only-verified              │
└─────────────────────────────────────────────────────┘

PRE-COMMIT HOOK SCRIPT:
┌─────────────────────────────────────────────────────┐
│ #!/bin/bash                                         │
│ # .git/hooks/pre-commit                             │
│                                                     │
│ echo "Running secret scan..."                       │
│                                                     │
│ # Run gitleaks on staged files                     │
│ gitleaks protect --staged --config=.gitleaks.toml  │
│                                                     │
│ if [ $? -eq 1 ]; then                               │
│     echo "❌ Secrets detected in staged files!"    │
│     echo "Please remove secrets before committing."│
│     echo ""                                         │
│     echo "If this is a false positive, add to:"   │
│     echo "  .gitleaks.toml [allowlist] section"   │
│     exit 1                                          │
│ fi                                                  │
│                                                     │
│ echo "✅ No secrets detected"                       │
│ exit 0                                              │
└─────────────────────────────────────────────────────┘

ALERT NOTIFICATION:
┌─────────────────────────────────────────────────────┐
│ 🔐 SECRET DETECTED - IMMEDIATE ACTION REQUIRED      │
│                                                     │
│ Repository: company/api-gateway                     │
│ Branch: feature/payment-integration                 │
│ Commit: abc123def                                   │
│ Author: developer@company.com                       │
│                                                     │
│ Finding:                                            │
│ • Type: AWS Secret Access Key                       │
│ • File: src/config/aws.js:45                        │
│ • Severity: CRITICAL                                │
│                                                     │
│ Actions Required:                                   │
│ 1. Do NOT merge this PR                            │
│ 2. Rotate the exposed credential                   │
│ 3. Remove secret from code and git history         │
│ 4. Update secret in vault                          │
│                                                     │
│ JIRA: https://company.atlassian.net/browse/SEC-123 │
│ Slack: #security-alerts                             │
│                                                     │
│ Runbook: https://wiki.company.com/secret-response  │
└─────────────────────────────────────────────────────┘

METRICS DASHBOARD:
┌─────────────────────────────────────────────────────┐
│ Credential Scanning Metrics - Last 30 Days         │
├─────────────────────────────────────────────────────┤
│ Scans Completed:       1,245                        │
│ Secrets Detected:      23                           │
│ Critical:              5                            │
│ High:                  8                            │
│ Medium:                10                           │
│ Avg Time to Remediate: 4.2 hours                    │
│ False Positive Rate:   12%                          │
│ Coverage:              98% of repositories          │
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

## Prompt 4: Secrets Manager Integration

### Description
Comprehensive guide to integrating secrets management solutions with applications for secure credential handling.

### Tags
`secrets-manager` `vault` `aws-secrets-manager` `credential-management`

---

## 🇬🇧 English Prompt

```
You are a platform security engineer implementing secrets management integration. Design a comprehensive secrets manager integration strategy.

SECRETS MANAGEMENT CONTEXT:
[Insert: secrets manager platform (Vault/AWS Secrets Manager/Azure Key Vault), application architecture, deployment environment, programming languages, compliance requirements]

Following HashiCorp Vault and cloud-native security best practices, provide:

1. **Architecture Design**
   - Secrets manager selection criteria
   - High availability configuration
   - Multi-region considerations
   - Network security requirements
   - Access control architecture

2. **Application Integration**
   - SDK integration patterns
   - Environment variable injection
   - Container integration (sidecar, init container)
   - Kubernetes secrets integration
   - Serverless function integration

3. **Authentication Methods**
   - AppRole authentication
   - Kubernetes authentication
   - Cloud IAM authentication
   - Certificate-based authentication
   - Token management strategies

4. **Secrets Lifecycle Management**
   - Secret versioning
   - Automated rotation
   - Lease and renewal handling
   - Secret revocation procedures
   - Audit logging

5. **Development Workflow**
   - Local development setup
   - Development secrets management
   - CI/CD pipeline integration
   - Secret injection methods
   - Testing strategies

6. **Security Controls**
   - Encryption at rest/transit
   - Access policy design
   - Audit logging configuration
   - Monitoring and alerting
   - Incident response procedures

Provide integration code examples and policy configurations.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت مهندس أمن المنصة تنفذ تكامل إدارة الأسرار. صمم استراتيجية تكامل مدير الأسرار الشاملة.

سياق إدارة الأسرار:
[أدخل: منصة مدير الأسرار (Vault/AWS Secrets Manager/Azure Key Vault)، بنية التطبيق، بيئة النشر، لغات البرمجة، متطلبات الامتثال]

وفقاً لأفضل ممارسات HashiCorp Vault وأمن السحابة الأصلية، قدم:

1. **تصميم البنية**
   - معايير اختيار مدير الأسرار
   - تكوين التوفر العالي
   - اعتبارات المناطق المتعددة
   - متطلبات أمن الشبكة
   - بنية التحكم في الوصول

2. **تكامل التطبيق**
   - أنماط تكامل SDK
   - حقن متغيرات البيئة
   - تكامل الحاويات (sidecar، init container)
   - تكامل أسرار Kubernetes
   - تكامل الدوال السيرفرلية

3. **طرق المصادقة**
   - مصادقة AppRole
   - مصادقة Kubernetes
   - مصادقة IAM السحابية
   - المصادقة القائمة على الشهادات
   - استراتيجيات إدارة الرموز

4. **إدارة دورة حياة الأسرار**
   - إصدار الأسرار
   - التدوير الآلي
   - التعامل مع الإيجار والتجديد
   - إجراءات إبطال الأسرار
   - تسجيل التدقيق

5. **سير عمل التطوير**
   - إعداد التطوير المحلي
   - إدارة أسرار التطوير
   - تكامل خط أنابيب CI/CD
   - طرق حقن الأسرار
   - استراتيجيات الاختبار

6. **ضوابط الأمان**
   - التشفير أثناء السكون/النقل
   - تصميم سياسة الوصول
   - تكوين تسجيل التدقيق
   - المراقبة والتنبيه
   - إجراءات الاستجابة للحوادث

قدم أمثلة كود التكامل وتكوينات السياسات.
```

---

## Example Output Preview

```
═══════════════════════════════════════════════════════
 SECRETS MANAGER INTEGRATION | تكامل مدير الأسرار
═══════════════════════════════════════════════════════

ARCHITECTURE DIAGRAM:
┌─────────────────────────────────────────────────────┐
│                                                     │
│  ┌─────────────────────────────────────────────┐   │
│  │           HashiCorp Vault Cluster            │   │
│  │    ┌─────────┐ ┌─────────┐ ┌─────────┐     │   │
│  │    │ Vault 1 │ │ Vault 2 │ │ Vault 3 │     │   │
│  │    └─────────┘ └─────────┘ └─────────┘     │   │
│  │              │                              │   │
│  │         Consul Backend                       │   │
│  └─────────────────────────────────────────────┘   │
│                      │                              │
│                      ▼                              │
│  ┌─────────────────────────────────────────────┐   │
│  │           Application Layer                  │   │
│  │                                              │   │
│  │  ┌──────────┐  ┌──────────┐  ┌──────────┐  │   │
│  │  │ App Pod  │  │ App Pod  │  │ App Pod  │  │   │
│  │  │ ┌──────┐ │  │ ┌──────┐ │  │ ┌──────┐ │  │   │
│  │  │ │Vault │ │  │ │Vault │ │  │ │Vault │ │  │   │
│  │  │ │Agent │ │  │ │Agent │ │  │ │Agent │ │  │   │
│  │  │ └──────┘ │  │ └──────┘ │  │ └──────┘ │  │   │
│  │  └──────────┘  └──────────┘  └──────────┘  │   │
│  │                                              │   │
│  │              Kubernetes Cluster              │   │
│  └─────────────────────────────────────────────┘   │
│                                                     │
└─────────────────────────────────────────────────────┘

VAULT POLICY CONFIGURATION:
┌─────────────────────────────────────────────────────┐
│ # vault policy: app-policy.hcl                      │
│                                                     │
│ # Read-only access to application secrets          │
│ path "secret/data/app/{{identity.entity.aliases.auth_kubernetes_123.metadata.service_account}}/*" {│
│   capabilities = ["read"]                          │
│ }                                                   │
│                                                     │
│ # Database credentials with lease                  │
│ path "database/creds/app-readonly" {               │
│   capabilities = ["read"]                          │
│ }                                                   │
│                                                     │
│ # Encryption keys for data encryption              │
│ path "transit/encrypt/app-key" {                   │
│   capabilities = ["update"]                        │
│ }                                                   │
│                                                     │
│ path "transit/decrypt/app-key" {                   │
│   capabilities = ["update"]                        │
│ }                                                   │
│                                                     │
│ # PKI for certificate generation                   │
│ path "pki/issue/app-dot-company" {                │
│   capabilities = ["update"]                        │
│ }                                                   │
└─────────────────────────────────────────────────────┘

KUBERNETES AUTHENTICATION:
┌─────────────────────────────────────────────────────┐
│ # Enable Kubernetes auth method                     │
│ vault auth enable kubernetes                        │
│                                                     │
│ # Configure Kubernetes auth                         │
│ vault write auth/kubernetes/config \               │
│   kubernetes_host="https://kubernetes.default.svc:443" \│
│   kubernetes_ca_cert=@/var/run/secrets/           │
│     kubernetes.io/serviceaccount/ca.crt \          │
│   token_reviewer_jwt=@/var/run/secrets/           │
│     kubernetes.io/serviceaccount/token             │
│                                                     │
│ # Create role for application                       │
│ vault write auth/kubernetes/role/app-role \        │
│   bound_service_account_names=app-sa \             │
│   bound_service_account_namespaces=production \    │
│   policies=app-policy \                            │
│   ttl=1h                                            │
└─────────────────────────────────────────────────────┘

APPLICATION INTEGRATION (NODE.JS):
┌─────────────────────────────────────────────────────┐
│ // vault-client.js                                  │
│ const vault = require('node-vault')({              │
│   endpoint: process.env.VAULT_ADDR,                │
│   token: process.env.VAULT_TOKEN                   │
│ });                                                 │
│                                                     │
│ class VaultSecretManager {                          │
│   constructor() {                                   │
│     this.cache = new Map();                        │
│     this.leaseTimers = new Map();                  │
│   }                                                 │
│                                                     │
│   async getSecret(path) {                          │
│     // Check cache first                           │
│     if (this.cache.has(path)) {                    │
│       return this.cache.get(path);                 │
│     }                                               │
│                                                     │
│     // Fetch from Vault                             │
│     const result = await vault.read(path);         │
│     const secret = result.data;                    │
│                                                     │
│     // Cache with auto-renewal                     │
│     this.cache.set(path, secret);                  │
│     this.scheduleRenewal(path, result.lease_id,   │
│       result.lease_duration);                      │
│                                                     │
│     return secret;                                  │
│   }                                                 │
│                                                     │
│   scheduleRenewal(path, leaseId, duration) {       │
│     const renewTime = (duration * 0.8) * 1000;    │
│     const timer = setTimeout(async () => {        │
│       await vault.renew({ lease_id: leaseId });   │
│       this.scheduleRenewal(path, leaseId, duration);│
│     }, renewTime);                                  │
│     this.leaseTimers.set(path, timer);            │
│   }                                                 │
│ }                                                   │
│                                                     │
│ module.exports = new VaultSecretManager();         │
└─────────────────────────────────────────────────────┘

VAULT AGENT SIDEcar CONFIGURATION:
┌─────────────────────────────────────────────────────┐
│ # vault-agent-config.hcl                            │
│ pid_file = "/tmp/vault-agent.pid"                  │
│                                                     │
│ auto_auth {                                         │
│   method "kubernetes" {                             │
│     mount_path = "auth/kubernetes"                  │
│     config = {                                      │
│       role = "app-role"                            │
│     }                                               │
│   }                                                 │
│                                                     │
│   sink "file" {                                     │
│     config = {                                      │
│       path = "/tmp/vault-token"                    │
│     }                                               │
│   }                                                 │
│ }                                                   │
│                                                     │
│ template {                                          │
│   source      = "/etc/vault/templates/db.tmpl"     │
│   destination = "/etc/secrets/db-credentials"      │
│   error_on_missing_key = true                      │
│ }                                                   │
│                                                     │
│ # db.tmpl                                           │
│ {{ with secret "database/creds/app-readonly" }}   │
│ DB_USER={{ .Data.username }}                       │
│ DB_PASS={{ .Data.password }}                       │
│ {{ end }}                                           │
└─────────────────────────────────────────────────────┘

SECRET ROTATION CONFIGURATION:
┌─────────────────────────────────────────────────────┐
│ # Database secrets engine with rotation            │
│ vault secrets enable database                       │
│                                                     │
│ vault write database/config/postgresql \           │
│   plugin_name=postgresql-database-plugin \         │
│   allowed_roles="app-readonly,app-readwrite" \     │
│   connection_url="postgresql://{{username}}:{{password}}@db:5432/app?sslmode=disable" \│
│   username="vault-admin" \                         │
│   password="initial-admin-password"                │
│                                                     │
│ # Create rotating credentials                       │
│ vault write database/roles/app-readonly \          │
│   db_name=postgresql \                             │
│   creation_statements="CREATE ROLE \"{{name}}\" WITH LOGIN PASSWORD '{{password}}' VALID UNTIL '{{expiration}}'; GRANT SELECT ON ALL TABLES IN SCHEMA public TO \"{{name}}\";" \│
│   default_ttl="1h" \                               │
│   max_ttl="24h"                                     │
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

## Prompt 5: Environment Variables Security

### Description
Comprehensive guide to securing environment variables and preventing sensitive data leakage through environment configuration.

### Tags
`environment-variables` `configuration-security` `dotenv` `container-security`

---

## 🇬🇧 English Prompt

```
You are a security engineer specializing in configuration security. Conduct a comprehensive assessment of environment variable security practices.

APPLICATION CONTEXT:
[Insert: deployment environment (containers, serverless, VMs), configuration management tools, container orchestration, CI/CD platform, secret exposure requirements]

Following security configuration best practices, provide:

1. **Environment Variable Security Assessment**
   - Sensitive data in .env files
   - Docker environment variable exposure
   - Kubernetes ConfigMap/Secret risks
   - CI/CD variable security
   - Cloud provider environment configuration

2. **Container Environment Security**
   - Dockerfile ENV instruction risks
   - docker-compose.yml exposure
   - Container orchestration secrets
   - Environment variable inheritance
   - Container inspection vulnerabilities

3. **CI/CD Pipeline Security**
   - Pipeline variable configuration
   - Masking effectiveness
   - Variable inheritance risks
   - Build log exposure
   - Artifact contamination

4. **Runtime Protection**
   - Process environment inspection
   - Memory dump risks
   - Log file contamination
   - Debug endpoint exposure
   - Error message leakage

5. **Secure Configuration Patterns**
   - Secrets manager integration
   - Configuration service implementation
   - Environment-specific configuration
   - Just-in-time secret injection
   - Configuration encryption

6. **Monitoring and Detection**
   - Environment variable monitoring
   - Anomaly detection
   - Compliance verification
   - Audit logging
   - Incident response procedures

Provide security configurations and hardening scripts.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت مهندس أمن متخصص في أمن التكوين. أجرِ تقييماً شاملاً لممارسات أمن متغيرات البيئة.

سياق التطبيق:
[أدخل: بيئة النشر (حاويات، سيرفرلس، أجهزة افتراضية)، أدوات إدارة التكوين، تنسيق الحاويات، منصة CI/CD، متطلبات كشف الأسرار]

وفقاً لأفضل ممارسات التكوين الأمني، قدم:

1. **تقييم أمن متغيرات البيئة**
   - البيانات الحساسة في ملفات .env
   - تعرض متغيرات بيئة Docker
   - مخاطر ConfigMap/Secret في Kubernetes
   - أمن متغيرات CI/CD
   - تكوين البيئة لمزود الخدمة السحابية

2. **أمن بيئة الحاويات**
   - مخاطر تعليمة ENV في Dockerfile
   - التعرض في docker-compose.yml
   - أسرار تنسيق الحاويات
   - وراثة متغيرات البيئة
   - ثغرات فحص الحاويات

3. **أمن خط أنابيب CI/CD**
   - تكوين متغيرات خط الأنابيب
   - فعالية الإخفاء
   - مخاطر وراثة المتغيرات
   - كشف سجلات البناء
   - تلوث التحف

4. **الحماية أثناء التشغيل**
   - فحص بيئة العملية
   - مخاطر تفريغ الذاكرة
   - تلوث ملفات السجل
   - كشف نقاط نهاية التصحيح
   - تسريب رسائل الخطأ

5. **أنماط التكوين الآمن**
   - تكامل مدير الأسرار
   - تنفيذ خدمة التكوين
   - التكوين الخاص بكل بيئة
   - حقن الأسرار في الوقت المناسب
   - تشفير التكوين

6. **المراقبة والاكتشاف**
   - مراقبة متغيرات البيئة
   - اكتشاف الشذوذ
   - التحقق من الامتثال
   - تسجيل التدقيق
   - إجراءات الاستجابة للحوادث

قدم تكوينات أمنية ونصوص تقوية.
```

---

## Example Output Preview

```
═══════════════════════════════════════════════════════
 ENVIRONMENT VARIABLES SECURITY | أمن متغيرات البيئة
═══════════════════════════════════════════════════════

SECURITY ASSESSMENT MATRIX:
┌─────────────────────────────────────────────────────┐
│ Configuration Source      │ Risk Level │ Finding   │
│───────────────────────────│────────────│───────────│
│ .env files in repo        │ Critical   │ Exposed   │
│ Dockerfile ENV            │ High       │ Leaked    │
│ docker-compose.yml        │ Critical   │ Plaintext │
│ CI/CD Variables           │ Medium     │ Unmasked  │
│ Kubernetes ConfigMaps     │ High       │ Unencoded │
│ Application logs          │ Medium     │ Logged    │
└─────────────────────────────────────────────────────┘

DOCKERFILE SECURITY ISSUES:
┌─────────────────────────────────────────────────────┐
│ ❌ INSECURE DOCKERFILE:                             │
│ FROM node:18-alpine                                 │
│ ENV DATABASE_URL=postgresql://admin:password@db:5432│
│ ENV API_KEY=sk_live_abc123                         │
│ ENV JWT_SECRET=my-super-secret-key                 │
│ COPY . .                                            │
│ CMD ["node", "server.js"]                          │
│                                                     │
│ Issues:                                             │
│ • Secrets in image layers (visible in docker history)│
│ • Inspectable via `docker inspect`                  │
│ • Visible in CI/CD logs                            │
│                                                     │
│ ✅ SECURE DOCKERFILE:                               │
│ FROM node:18-alpine                                 │
│ # No ENV for secrets                               │
│ COPY package*.json ./                               │
│ RUN npm ci --only=production                       │
│ COPY . .                                            │
│ # Secrets injected at runtime                       │
│ CMD ["node", "server.js"]                          │
│                                                     │
│ Runtime:                                            │
│ docker run -e DATABASE_URL=$DB_URL \               │
│   -e API_KEY=$API_KEY \                            │
│   -e JWT_SECRET=$JWT_SECRET \                      │
│   myapp:latest                                      │
└─────────────────────────────────────────────────────┘

KUBERNETES SECRETS CONFIGURATION:
┌─────────────────────────────────────────────────────┐
│ # Secure Kubernetes Secret                          │
│ apiVersion: v1                                      │
│ kind: Secret                                        │
│ metadata:                                           │
│   name: app-secrets                                 │
│   namespace: production                             │
│ type: Opaque                                        │
│ stringData:                                         │
│   database-url: "postgresql://..."                 │
│   api-key: "sk_live_..."                            │
│ ---                                                 │
│ apiVersion: apps/v1                                 │
│ kind: Deployment                                    │
│ metadata:                                           │
│   name: app                                         │
│ spec:                                               │
│   template:                                         │
│     spec:                                           │
│       containers:                                   │
│       - name: app                                   │
│         envFrom:                                    │
│         - secretRef:                                │
│             name: app-secrets                       │
│         env:                                        │
│         - name: POD_NAME                           │
│           valueFrom:                                │
│             fieldRef:                               │
│               fieldPath: metadata.name              │
└─────────────────────────────────────────────────────┘

CI/CD VARIABLE SECURITY:
┌─────────────────────────────────────────────────────┐
│ # GitHub Actions - Secure variable usage            │
│ env:                                                │
│   # ❌ NEVER do this:                               │
│   # API_KEY: sk_live_abc123                        │
│                                                     │
│   # ✅ Use secrets                                  │
│   API_KEY: ${{ secrets.API_KEY }}                  │
│                                                     │
│ jobs:                                               │
│   build:                                            │
│     runs-on: ubuntu-latest                          │
│     steps:                                          │
│       - name: Deploy                                │
│         run: |                                      │
│           # Variables are masked in logs           │
│           echo "Deploying with key: ***"           │
│           # Secret passed securely                 │
│           curl -H "Authorization: Bearer $API_KEY" │
│                                                     │
│       - name: Debug (Disabled in production)        │
│         if: ${{ env.DEBUG == 'true' }}             │
│         run: |                                      │
│           # Never log secrets                       │
│           echo "Environment: ${{ env.NODE_ENV }}"  │
│                                                     │
│ # Masking verification                              │
│ - name: Verify masking                              │
│   run: |                                            │
│     if echo "$API_KEY" | grep -q "sk_live"; then  │
│       echo "ERROR: Secret not masked!"             │
│       exit 1                                        │
│     fi                                              │
└─────────────────────────────────────────────────────┘

RUNTIME PROTECTION SCRIPT:
┌─────────────────────────────────────────────────────┐
│ #!/bin/bash                                         │
│ # env-security-check.sh                             │
│                                                     │
│ echo "Checking for exposed secrets in environment"│
│                                                     │
│ # Check for common secret patterns                 │
│ PATTERNS=(                                          │
│   "AKIA[A-Z0-9]{16}"        # AWS Access Key       │
│   "sk_live_[a-zA-Z0-9]{24}" # Stripe Live Key      │
│   "xoxb-[0-9]+-[0-9A-Za-z]+" # Slack Token         │
│   "ghp_[a-zA-Z0-9]{36}"     # GitHub Token         │
│ )                                                   │
│                                                     │
│ for pattern in "${PATTERNS[@]}"; do                │
│   if env | grep -E "$pattern" > /dev/null 2>&1; then│
│     echo "CRITICAL: Secret pattern detected in environment!"│
│     # Alert but don't expose the secret           │
│     exit 1                                          │
│   fi                                                │
│ done                                                │
│                                                     │
│ # Check for sensitive variable names               │
│ SENSITIVE_VARS=(PASSWORD SECRET KEY TOKEN API_KEY)│
│ for var in "${SENSITIVE_VARS[@]}"; do             │
│   if [ -n "${!var}" ]; then                        │
│     echo "WARNING: Sensitive variable $var is set"│
│   fi                                                │
│ done                                                │
│                                                     │
│ echo "Environment security check passed"           │
└─────────────────────────────────────────────────────┘

LOGGING SECURITY CONFIGURATION:
┌─────────────────────────────────────────────────────┐
│ // Secure logging configuration                     │
│ const SENSITIVE_KEYS = [                            │
│   'password', 'secret', 'token', 'api_key',        │
│   'authorization', 'cookie', 'session'             │
│ ];                                                  │
│                                                     │
│ function sanitizeForLogging(obj) {                 │
│   const sanitized = { ...obj };                    │
│   for (const key of Object.keys(sanitized)) {      │
│     const lowerKey = key.toLowerCase();            │
│     if (SENSITIVE_KEYS.some(s => lowerKey.includes(s))) {│
│       sanitized[key] = '[REDACTED]';               │
│     }                                               │
│   }                                                 │
│   return sanitized;                                 │
│ }                                                   │
│                                                     │
│ // Usage                                            │
│ logger.info('Request received', {                  │
│   path: req.path,                                   │
│   headers: sanitizeForLogging(req.headers),        │
│   body: sanitizeForLogging(req.body)               │
│ });                                                 │
│                                                     │
│ // Output:                                          │
│ // {"level":"info","message":"Request received",   │
│ //  "headers":{"authorization":"[REDACTED]",...}}  │
└─────────────────────────────────────────────────────┘

SECURITY CHECKLIST:
┌─────────────────────────────────────────────────────┐
│ Item                              │ Status │ Action │
│───────────────────────────────────│────────│────────│
│ .env in .gitignore               │ ✓      │ Done   │
│ No secrets in Dockerfile          │ ✓      │ Done   │
│ CI/CD secrets properly masked     │ ✓      │ Done   │
│ Kubernetes secrets encrypted      │ ✓      │ Done   │
│ Log sanitization implemented      │ ✓      │ Done   │
│ Runtime secret scanning           │ ✓      │ Done   │
│ Secret rotation automated         │ ✓      │ Done   │
│ Debug endpoints disabled          │ ✓      │ Done   │
│ Error messages sanitized          │ ✓      │ Done   │
│ Environment audit logging         │ ✓      │ Done   │
└─────────────────────────────────────────────────────┘
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team
