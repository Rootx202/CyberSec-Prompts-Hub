# Secure Coding Practices Prompts

A comprehensive collection of bilingual (English/Arabic) prompts for secure coding practices, aligned with OWASP Secure Coding Practices and industry standards.

---

## Prompt 1: OWASP Secure Coding Principles

### Description
A structured approach to implementing OWASP secure coding principles across the software development lifecycle, focusing on defense-in-depth and security-by-design methodologies.

### Tags
`owasp` `secure-coding` `defense-in-depth` `security-by-design`

---

## 🇬🇧 English Prompt

```
You are a senior application security architect conducting a secure code review and implementing OWASP secure coding principles. Analyze the following codebase and provide comprehensive security recommendations.

CODEBASE CONTEXT:
[Insert: programming language, framework, application type, sensitive data handling requirements, deployment environment]

Following OWASP Secure Coding Practices Quick Reference Guide, provide:

1. **Input Validation Assessment**
   - Allowlist vs blocklist validation strategies
   - Input sanitization requirements per data type
   - Canonicalization attack prevention
   - Character encoding handling
   - File upload validation criteria

2. **Output Encoding Implementation**
   - Context-specific encoding (HTML, JavaScript, URL, CSS)
   - Template engine security configuration
   - JSON serialization protection
   - XML output encoding requirements
   - CSV injection prevention

3. **Authentication Security**
   - Secure password storage mechanisms (bcrypt, Argon2)
   - Multi-factor authentication integration
   - Session management best practices
   - Account lockout and rate limiting
   - Password policy implementation

4. **Access Control Design**
   - Role-based access control (RBAC) implementation
   - Attribute-based access control (ABAC) considerations
   - Principle of least privilege enforcement
   - Insecure direct object reference prevention
   - Horizontal and vertical privilege escalation mitigation

5. **Cryptographic Practices**
   - Encryption algorithm selection (AES-256-GCM, ChaCha20)
   - Key management lifecycle
   - Secure random number generation
   - TLS/SSL configuration requirements
   - Cryptographic key rotation procedures

6. **Error Handling and Logging**
   - Secure error message design
   - Stack trace protection in production
   - Security event logging requirements
   - Log injection prevention
   - Sensitive data exclusion from logs

Provide code examples in the target language with security annotations and unit test requirements.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت مهندس أمن تطبيقات أول تجري مراجعة كود آمن وتنفذ مبادئ OWASP للبرمجة الآمنة. حلل قاعدة الكود التالية وقدم توصيات أمنية شاملة.

سياق قاعدة الكود:
[أدخل: لغة البرمجة، الإطار، نوع التطبيق، متطلبات التعامل مع البيانات الحساسة، بيئة النشر]

وفقاً لدليل OWASP السريع لممارسات البرمجة الآمنة، قدم:

1. **تقييم التحقق من المدخلات**
   - استراتيجيات التحقق بالقائمة البيضاء مقابل القائمة السوداء
   - متطلبات تنقية المدخلات حسب نوع البيانات
   - منع هجمات التوحيد القياسي
   - معالجة ترميز الأحرف
   - معايير التحقق من رفع الملفات

2. **تنفيذ ترميز المخرجات**
   - الترميز الخاص بالسياق (HTML، JavaScript، URL، CSS)
   - تكوين أمان محرك القوالب
   - حماية تسلسل JSON
   - متطلبات ترميز مخرجات XML
   - منع حقن CSV

3. **أمن المصادقة**
   - آليات التخزين الآمن لكلمات المرور (bcrypt، Argon2)
   - تكامل المصادقة متعددة العوامل
   - أفضل ممارسات إدارة الجلسات
   - قفل الحساب والحد من المعدل
   - تنفيذ سياسة كلمات المرور

4. **تصميم التحكم في الوصول**
   - تنفيذ التحكم في الوصول القائم على الأدوار (RBAC)
   - اعتبارات التحكم في الوصول القائم على السمات (ABAC)
   - إنفاذ مبدأ الامتياز الأقل
   - منع الإشارة المباشرة غير الآمنة للكائنات
   - التخفيف من التصعيد الأفقي والعمودي للامتيازات

5. **الممارسات التشفيرية**
   - اختيار خوارزميات التشفير (AES-256-GCM، ChaCha20)
   - دورة حياة إدارة المفاتيح
   - توليد الأرقام العشوائية الآمن
   - متطلبات تكوين TLS/SSL
   - إجراءات تدوير المفاتيح التشفيرية

6. **معالجة الأخطاء والتسجيل**
   - تصميم رسائل الخطأ الآمنة
   - حماية تتبع المكدس في الإنتاج
   - متطلبات تسجيل أحداث الأمان
   - منع حقن السجلات
   - استبعاد البيانات الحساسة من السجلات

قدم أمثلة برمجية باللغة المستهدفة مع تعليقات أمنية ومتطلبات اختبارات الوحدة.
```

---

## Example Output Preview

```
═══════════════════════════════════════════════════════
 SECURE CODING ASSESSMENT | تقييم البرمجة الآمنة
═══════════════════════════════════════════════════════

┌─────────────────────────────────────────────────────┐
│ INPUT VALIDATION FINDINGS                            │
├─────────────────────────────────────────────────────┤
│ [HIGH] Missing allowlist validation on user input   │
│ Location: src/controllers/UserController.java:45    │
│                                                     │
│ Vulnerable Code:                                    │
│ String username = request.getParameter("user");    │
│                                                     │
│ Secure Implementation:                              │
│ private static final Pattern USERNAME_PATTERN =    │
│   Pattern.compile("^[a-zA-Z0-9_]{3,20}$");         │
│ if (!USERNAME_PATTERN.matcher(username).matches()) │
│   throw new ValidationException("Invalid format"); │
└─────────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────────┐
│ CRYPTOGRAPHIC RECOMMENDATIONS                        │
├─────────────────────────────────────────────────────┤
│ Password Hashing: BCrypt with cost factor 12        │
│ Encryption: AES-256-GCM for data at rest            │
│ Key Derivation: PBKDF2 with 310,000 iterations     │
│ Random Generation: SecureRandom.getInstanceStrong()│
└─────────────────────────────────────────────────────┘

SECURITY CONTROLS MATRIX:
| Control Category    | Current | Target | Gap    |
|---------------------|---------|--------|--------|
| Input Validation    | 65%     | 95%    | -30%   |
| Output Encoding     | 70%     | 100%   | -30%   |
| Authentication      | 80%     | 100%   | -20%   |
| Access Control      | 75%     | 95%    | -20%   |
| Cryptography        | 60%     | 100%   | -40%   |
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 2: Language-Specific Security (Python)

### Description
Comprehensive Python secure coding guidelines covering common vulnerability patterns, secure library usage, and Python-specific security considerations.

### Tags
`python` `secure-coding` `language-security` `python-security`

---

## 🇬🇧 English Prompt

```
You are a Python security specialist conducting a secure code review. Analyze the Python application code for security vulnerabilities and provide language-specific remediation guidance.

PYTHON APPLICATION CONTEXT:
[Insert: application type, Python version, frameworks used (Django/Flask/FastAPI), data sensitivity level, deployment environment]

Following Python security best practices and OWASP guidelines, provide:

1. **Injection Vulnerability Assessment**
   - SQL injection prevention (parameterized queries, ORM security)
   - OS command injection risks (subprocess security)
   - Code injection vulnerabilities (eval, exec, compile)
   - Template injection (Jinja2, Mako security)
   - LDAP and NoSQL injection patterns

2. **Deserialization Security**
   - Pickle deserialization risks and alternatives
   - YAML safe loading practices
   - JSON parsing security considerations
   - Marshal and shelve module risks
   - Custom deserialization validation

3. **Cryptographic Implementation**
   - secrets module usage for cryptographic operations
   - hashlib secure algorithm selection
   - cryptography library best practices
   - SSL/TLS configuration with ssl module
   - Key derivation function implementation

4. **File System Security**
   - Path traversal prevention (os.path security)
   - Temporary file handling (tempfile module)
   - File permission management
   - Symlink attack prevention
   - Race condition mitigation

5. **Memory and Resource Management**
   - Memory exhaustion vulnerabilities
   - Resource leak prevention
   - Integer overflow handling
   - Regex denial of service (ReDoS)
   - Generator expression security

6. **Framework-Specific Security**
   - Django security middleware configuration
   - Flask-WTF CSRF protection
   - FastAPI dependency injection security
   - SQLAlchemy security best practices
   - Celery task security

Provide secure code examples with bandit static analysis compliance.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت متخصص في أمن Python تجري مراجعة كود آمن. حلل كود تطبيق Python للثغرات الأمنية وقدم إرشادات معالجة خاصة باللغة.

سياق تطبيق Python:
[أدخل: نوع التطبيق، إصدار Python، الأطر المستخدمة (Django/Flask/FastAPI)، مستوى حساسية البيانات، بيئة النشر]

وفقاً لأفضل ممارسات أمن Python وإرشادات OWASP، قدم:

1. **تقييم ثغرات الحقن**
   - منع حقن SQL (الاستعلامات المُعلمّة، أمان ORM)
   - مخاطر حقن أوامر نظام التشغيل (أمان subprocess)
   - ثغرات حقن الكود (eval، exec، compile)
   - حقن القوالب (أمان Jinja2، Mako)
   - أنماط حقن LDAP و NoSQL

2. **أمن إزالة التسلسل**
   - مخاطر إزالة تسلسل Pickle والبدائل
   - ممارسات التحميل الآمن لـ YAML
   - اعتبارات أمن تحليل JSON
   - مخاطر وحدتي marshal و shelve
   - التحقق من إزالة التسلسل المخصص

3. **التنفيذ التشفيري**
   - استخدام وحدة secrets للعمليات التشفيرية
   - اختيار خوارزمية hashlib الآمنة
   - أفضل ممارسات مكتبة cryptography
   - تكوين SSL/TLS مع وحدة ssl
   - تنفيذ وظيفة اشتقاق المفتاح

4. **أمن نظام الملفات**
   - منع اجتياز المسار (أمان os.path)
   - التعامل مع الملفات المؤقتة (وحدة tempfile)
   - إدارة أذونات الملفات
   - منع هجمات الروابط الرمزية
   - التخفيف من حالات السباق

5. **إدارة الذاكرة والموارد**
   - ثغرات استنزاف الذاكرة
   - منع تسرب الموارد
   - التعامل مع تجاوز الأعداد الصحيحة
   - حرمان الخدمة بالتعبير النمطي (ReDoS)
   - أمن تعابير المولد

6. **الأمان الخاص بالإطار**
   - تكوين البرمجيات الوسيطة الأمنية في Django
   - حماية CSRF في Flask-WTF
   - أمن حقن التبعية في FastAPI
   - أفضل ممارسات أمن SQLAlchemy
   - أمن مهام Celery

قدم أمثلة كود آمنة متوافقة مع التحليل الثابت bandit.
```

---

## Example Output Preview

```
═══════════════════════════════════════════════════════
 PYTHON SECURITY ASSESSMENT | تقييم أمن Python
═══════════════════════════════════════════════════════

┌─────────────────────────────────────────────────────┐
│ INJECTION VULNERABILITIES DETECTED                   │
├─────────────────────────────────────────────────────┤
│ [CRITICAL] SQL Injection in user query              │
│ File: app/database/queries.py:67                    │
│                                                     │
│ ❌ Vulnerable:                                      │
│ query = f"SELECT * FROM users WHERE id = {user_id}"│
│ cursor.execute(query)                               │
│                                                     │
│ ✅ Secure:                                          │
│ query = "SELECT * FROM users WHERE id = %s"        │
│ cursor.execute(query, (user_id,))                   │
└─────────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────────┐
│ DESERIALIZATION RISKS                               │
├─────────────────────────────────────────────────────┤
│ [HIGH] Unsafe pickle.load() usage                   │
│ File: app/utils/cache.py:23                         │
│                                                     │
│ ❌ Vulnerable:                                      │
│ data = pickle.loads(cached_data)                   │
│                                                     │
│ ✅ Secure Alternative:                              │
│ import json                                         │
│ data = json.loads(cached_data)                      │
│                                                     │
│ # If pickle required, use restricted unpickler:    │
│ class SafeUnpickler(pickle.Unpickler):             │
│     def find_class(self, module, name):            │
│         if module == 'builtins' and name in        │
│            safe_builtins:                          │
│             return getattr(builtins, name)         │
│         raise pickle.UnpicklingError()             │
└─────────────────────────────────────────────────────┘

BANDIT SCAN COMPLIANCE:
| Test ID  | Severity | Issue                     | Status   |
|----------|----------|---------------------------|----------|
| B101     | Low      | assert statement usage    | Pass     |
| B601     | High     | paramiko call             | Fixed    |
| B602     | High     | subprocess shell=True     | Fixed    |
| B303     | Medium   | MD5 usage                 | Fixed    |
| B310     | High     | urllib urlopen            | Fixed    |
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 3: Language-Specific Security (JavaScript/Node.js)

### Description
Comprehensive JavaScript and Node.js secure coding guidelines covering frontend and backend security patterns, npm security, and JavaScript-specific vulnerabilities.

### Tags
`javascript` `nodejs` `secure-coding` `frontend-security` `npm-security`

---

## 🇬🇧 English Prompt

```
You are a JavaScript security specialist conducting a comprehensive security review of a JavaScript/Node.js application. Analyze the codebase for vulnerabilities and provide secure coding recommendations.

JAVASCRIPT APPLICATION CONTEXT:
[Insert: application type (frontend/backend/full-stack), Node.js version, frameworks (Express/Nest/React/Angular), npm packages used, deployment environment]

Following OWASP and Node.js Security best practices, provide:

1. **Injection Prevention**
   - NoSQL injection prevention (MongoDB, Mongoose security)
   - Command injection mitigation (child_process security)
   - Server-Side Prototype Pollution detection and prevention
   - Regular expression denial of service (ReDoS)
   - Expression Language injection

2. **Authentication and Session Security**
   - JWT implementation security (algorithm confusion, weak secrets)
   - Session management best practices (express-session, cookie-session)
   - Passport.js security configuration
   - OAuth/OIDC implementation security
   - CORS and CSRF protection

3. **Frontend Security**
   - XSS prevention strategies (DOM-based, reflected, stored)
   - Content Security Policy (CSP) implementation
   - Secure cookie configuration (HttpOnly, Secure, SameSite)
   - LocalStorage and SessionStorage security considerations
   - Third-party script security management

4. **Node.js Runtime Security**
   - Event loop blocking prevention
   - Unhandled promise rejection risks
   - Error handling security (stack trace exposure)
   - Process environment variable protection
   - Cluster mode and child process security

5. **Dependency Security**
   - npm audit analysis and remediation
   - Supply chain attack prevention
   - Package.json security configuration
   - Lockfile integrity verification
   - Dependency update strategies

6. **Express.js and Framework Security**
   - Helmet.js middleware configuration
   - Rate limiting implementation (express-rate-limit)
   - Input validation (Joi, express-validator)
   - Helmet security headers
   - HPP (HTTP Parameter Pollution) protection

Provide secure code examples with ESLint security plugin compliance.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت متخصص في أمن JavaScript تجري مراجعة أمنية شاملة لتطبيق JavaScript/Node.js. حلل قاعدة الكود للثغرات وقدم توصيات برمجة آمنة.

سياق تطبيق JavaScript:
[أدخل: نوع التطبيق (واجهة أمامية/خلفية/كامل)، إصدار Node.js، الأطر (Express/Nest/React/Angular)، حزم npm المستخدمة، بيئة النشر]

وفقاً لـ OWASP وأفضل ممارسات أمن Node.js، قدم:

1. **منع الحقن**
   - منع حقن NoSQL (أمان MongoDB، Mongoose)
   - التخفيف من حقن الأوامر (أمان child_process)
   - اكتشاف ومنع تلوث النموذج الأولي من جانب الخادم
   - حرمان الخدمة بالتعبير النمطي (ReDoS)
   - حقن لغة التعبير

2. **أمن المصادقة والجلسات**
   - أمان تنفيذ JWT (الارتباك في الخوارزمية، الأسرار الضعيفة)
   - أفضل ممارسات إدارة الجلسات (express-session، cookie-session)
   - تكوين أمن Passport.js
   - أمان تنفيذ OAuth/OIDC
   - حماية CORS و CSRF

3. **أمن الواجهة الأمامية**
   - استراتيجيات منع XSS (قائم على DOM، منعكس، مخزن)
   - تنفيذ سياسة أمن المحتوى (CSP)
   - تكوين ملفات تعريف الارتباط الآمنة (HttpOnly، Secure، SameSite)
   - اعتبارات أمن LocalStorage و SessionStorage
   - إدارة أمن النصوص البرمجية الخارجية

4. **أمن بيئة تشغيل Node.js**
   - منع حجب حلقة الأحداث
   - مخاطر رفض الوعود غير المعالجة
   - أمن معالجة الأخطاء (كشف تتبع المكدس)
   - حماية متغيرات بيئة العملية
   - أمن الوضع العنقودي والعمليات الفرعية

5. **أمن التبعيات**
   - تحليل ومعالجة npm audit
   - منع هجمات سلسلة التوريد
   - تكوين أمن Package.json
   - التحقق من سلامة ملف القفل
   - استراتيجيات تحديث التبعيات

6. **أمن Express.js والأطر**
   - تكوين البرمجيات الوسيطة Helmet.js
   - تنفيذ الحد من المعدل (express-rate-limit)
   - التحقق من المدخلات (Joi، express-validator)
   - ترويسات أمان Helmet
   - حماية HPP (تلوث معامل HTTP)

قدم أمثلة كود آمنة متوافقة مع إضافة ESLint الأمنية.
```

---

## Example Output Preview

```
═══════════════════════════════════════════════════════
 JAVASCRIPT SECURITY ASSESSMENT | تقييم أمن JavaScript
═══════════════════════════════════════════════════════

┌─────────────────────────────────────────────────────┐
│ PROTOTYPE POLLUTION DETECTED                         │
├─────────────────────────────────────────────────────┤
│ [CRITICAL] Unsafe object merge                      │
│ File: src/utils/helpers.js:45                       │
│                                                     │
│ ❌ Vulnerable:                                      │
│ function merge(target, source) {                    │
│   for (let key in source) {                         │
│     target[key] = source[key];                      │
│   }                                                 │
│ }                                                   │
│                                                     │
│ ✅ Secure:                                          │
│ function merge(target, source) {                    │
│   for (let key in source) {                         │
│     if (key === '__proto__' || key === 'constructor'│
│         || key === 'prototype') continue;           │
│     target[key] = source[key];                      │
│   }                                                 │
│ }                                                   │
│                                                     │
│ // Or use safe libraries:                           │
│ import { merge } from 'lodash';                     │
└─────────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────────┐
│ JWT SECURITY CONFIGURATION                           │
├─────────────────────────────────────────────────────┤
│ ❌ Vulnerable:                                      │
│ jwt.verify(token, publicKey);  // Algorithm confusion│
│                                                     │
│ ✅ Secure:                                          │
│ jwt.verify(token, publicKey, {                      │
│   algorithms: ['RS256'],  // Explicitly specify     │
│   issuer: 'https://auth.example.com',               │
│   audience: 'https://api.example.com',              │
│   clockTolerance: 10,                               │
│   maxAge: '2h'                                      │
│ });                                                 │
└─────────────────────────────────────────────────────┘

EXPRESS SECURITY MIDDLEWARE:
┌─────────────────────────────────────────────────────┐
│ const helmet = require('helmet');                   │
│ const rateLimit = require('express-rate-limit');    │
│                                                     │
│ app.use(helmet({                                    │
│   contentSecurityPolicy: {                          │
│     directives: {                                   │
│       defaultSrc: ["'self'"],                       │
│       scriptSrc: ["'self'", "trusted.cdn.com"],    │
│       styleSrc: ["'self'", "'unsafe-inline'"],     │
│       imgSrc: ["'self'", "data:", "cdn.example.com"]│
│     }                                               │
│   },                                                │
│   hsts: { maxAge: 31536000, includeSubDomains: true}│
│ }));                                                │
│                                                     │
│ const limiter = rateLimit({                         │
│   windowMs: 15 * 60 * 1000,  // 15 minutes          │
│   max: 100,  // limit each IP to 100 requests       │
│   standardHeaders: true,                            │
│   legacyHeaders: false                              │
│ });                                                 │
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

## Prompt 4: Secure API Development

### Description
Comprehensive secure API development guidelines covering REST and GraphQL security, authentication mechanisms, and API-specific vulnerability patterns.

### Tags
`api-security` `rest-api` `graphql` `authentication` `api-design`

---

## 🇬🇧 English Prompt

```
You are an API security architect designing and reviewing secure API implementations. Analyze the API architecture and provide comprehensive security recommendations.

API CONTEXT:
[Insert: API type (REST/GraphQL/gRPC), authentication mechanism, data sensitivity, rate limiting requirements, client types, deployment environment]

Following OWASP API Security Top 10 and industry best practices, provide:

1. **Authentication and Authorization**
   - OAuth 2.0 / OpenID Connect implementation security
   - API key management best practices
   - JWT security configuration and validation
   - Mutual TLS (mTLS) implementation
   - API gateway authentication patterns

2. **API Security Controls**
   - Rate limiting and throttling strategies
   - Input validation and sanitization
   - Output filtering and data minimization
   - Request/Response size limits
   - Timeout configurations

3. **REST API Security**
   - HTTP method security (GET, POST, PUT, DELETE, PATCH)
   - Resource-based access control
   - Proper use of HTTP status codes
   - Content-Type validation
   - Idempotency key implementation

4. **GraphQL Security**
   - Query depth limiting
   - Query complexity analysis
   - Field-level authorization
   - Introspection disabling in production
   - Batching attack prevention
   - Persisted queries implementation

5. **Data Protection**
   - Sensitive data exposure prevention
   - Response filtering strategies
   - Pagination security (cursor vs offset)
   - Bulk operation security
   - Audit logging requirements

6. **API Documentation Security**
   - OpenAPI/Swagger security specifications
   - Authentication documentation
   - Error message sanitization
   - Version deprecation security
   - Security contact information

Provide security architecture diagrams and code implementation examples.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت مهندس أمن واجهات برمجة التطبيقات تقوم بتصميم ومراجعة تنفيذات API الآمنة. حلل بنية API وقدم توصيات أمنية شاملة.

سياق API:
[أدخل: نوع API (REST/GraphQL/gRPC)، آلية المصادقة، حساسية البيانات، متطلبات الحد من المعدل، أنواع العملاء، بيئة النشر]

وفقاً لأهم 10 مخاطر أمنية لواجهات برمجة التطبيقات من OWASP وأفضل الممارسات الصناعية، قدم:

1. **المصادقة والتفويض**
   - أمان تنفيذ OAuth 2.0 / OpenID Connect
   - أفضل ممارسات إدارة مفاتيح API
   - تكوين والتحقق من أمان JWT
   - تنفيذ TLS المتبادل (mTLS)
   - أنماط مصادقة بوابة API

2. **ضوابط أمن API**
   - استراتيجيات الحد من المعدل والاختناق
   - التحقق من المدخلات وتنقيتها
   - تصفية المخرجات وتقليل البيانات
   - حدود حجم الطلب/الاستجابة
   - تكوينات المهلة

3. **أمن REST API**
   - أمان طرق HTTP (GET، POST، PUT، DELETE، PATCH)
   - التحكم في الوصول القائم على الموارد
   - الاستخدام الصحيح لرموز حالة HTTP
   - التحقق من Content-Type
   - تنفيذ مفتاح Idempotency

4. **أمن GraphQL**
   - تحديد عمق الاستعلام
   - تحليل تعقيد الاستعلام
   - التفويض على مستوى الحقل
   - تعطيل الاستبطان في الإنتاج
   - منع هجمات التجميع
   - تنفيذ الاستعلامات المستمرة

5. **حماية البيانات**
   - منع كشف البيانات الحساسة
   - استراتيجيات تصفية الاستجابة
   - أمن التقسيم إلى صفحات (cursor مقابل offset)
   - أمن العمليات المجمعة
   - متطلبات تسجيل التدقيق

6. **أمن توثيق API**
   - مواصفات أمن OpenAPI/Swagger
   - توثيق المصادقة
   - تنقية رسائل الخطأ
   - أمن إهمال الإصدار
   - معلومات جهة الاتصال الأمنية

قدم مخططات بنية أمنية وأمثلة تنفيذ برمجي.
```

---

## Example Output Preview

```
═══════════════════════════════════════════════════════
 API SECURITY ARCHITECTURE | بنية أمن API
═══════════════════════════════════════════════════════

┌─────────────────────────────────────────────────────┐
│ AUTHENTICATION FLOW                                  │
├─────────────────────────────────────────────────────┤
│                                                     │
│  ┌─────────┐    ┌──────────────┐    ┌───────────┐  │
│  │ Client  │───▶│ API Gateway  │───▶│ Auth      │  │
│  │         │    │              │    │ Service   │  │
│  └─────────┘    └──────────────┘    └───────────┘  │
│       │               │                    │        │
│       │         Rate Limit         JWT Validation   │
│       │         Input Valid        Token Refresh    │
│       │         mTLS Term                          │
│       ▼               ▼                    ▼        │
│  ┌─────────┐    ┌──────────────┐    ┌───────────┐  │
│  │ API Key │    │ Access Token │    │ Refresh   │  │
│  │ + Secret│    │ (JWT RS256)  │    │ Token     │  │
│  └─────────┘    └──────────────┘    └───────────┘  │
│                                                     │
└─────────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────────┐
│ GRAPHQL SECURITY CONFIGURATION                       │
├─────────────────────────────────────────────────────┤
│ const { ApolloServer } = require('@apollo/server');│
│ const { depthLimit } = require('graphql-depth-limit');│
│                                                     │
│ const server = new ApolloServer({                   │
│   typeDefs,                                         │
│   resolvers,                                        │
│   validationRules: [                                │
│     depthLimit(5),  // Max query depth              │
│     createComplexityLimitRule(1000)                 │
│   ],                                                │
│   introspection: process.env.NODE_ENV !== 'prod',  │
│   debug: false,                                     │
│   context: ({ req }) => {                           │
│     const user = verifyToken(req.headers.auth);    │
│     return { user, isAuthenticated: !!user };      │
│   }                                                 │
│ });                                                 │
└─────────────────────────────────────────────────────┘

RATE LIMITING CONFIGURATION:
┌─────────────────────────────────────────────────────┐
│ Endpoint              │ Rate Limit │ Window         │
│───────────────────────│────────────│────────────────│
│ /api/auth/login       │ 5          │ 15 minutes     │
│ /api/auth/refresh     │ 30         │ 15 minutes     │
│ /api/graphql          │ 100        │ 1 minute       │
│ /api/public/*         │ 1000       │ 1 minute       │
│ /api/admin/*          │ 50         │ 1 minute       │
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

## Prompt 5: Secure Database Operations

### Description
Comprehensive secure database operations guidelines covering SQL and NoSQL security, connection management, and data protection at the database layer.

### Tags
`database-security` `sql-security` `nosql-security` `data-protection` `encryption`

---

## 🇬🇧 English Prompt

```
You are a database security specialist conducting a comprehensive security review of database operations. Analyze the database architecture and provide security recommendations.

DATABASE CONTEXT:
[Insert: database type (PostgreSQL/MySQL/MongoDB/Redis/Elasticsearch), ORM used, data sensitivity classification, compliance requirements, deployment environment]

Following database security best practices and compliance requirements, provide:

1. **Query Security**
   - SQL injection prevention strategies
   - Parameterized query implementation
   - ORM security configuration (Sequelize, TypeORM, Prisma)
   - Stored procedure security
   - Dynamic SQL mitigation

2. **Access Control**
   - Database user permission design (principle of least privilege)
   - Role-based access control implementation
   - Row-level security configuration
   - View-based data access patterns
   - Connection pooling security

3. **Connection Security**
   - TLS/SSL configuration for database connections
   - Connection string security (no hardcoded credentials)
   - Connection pooling best practices
   - Database credential rotation
   - Network segmentation requirements

4. **Data Protection**
   - Column-level encryption implementation
   - Transparent Data Encryption (TDE) configuration
   - Data masking strategies
   - Backup encryption requirements
   - Data retention and deletion policies

5. **NoSQL Security Considerations**
   - MongoDB security configuration
   - Redis authentication and ACL
   - Elasticsearch security features
   - Document-level security
   - Aggregation pipeline injection prevention

6. **Monitoring and Auditing**
   - Query logging and analysis
   - Anomaly detection in database access
   - Audit trail implementation
   - Performance monitoring security implications
   - Alert configuration for suspicious activities

Provide security configuration examples and migration scripts for remediation.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت متخصص في أمن قواعد البيانات تجري مراجعة أمنية شاملة لعمليات قاعدة البيانات. حلل بنية قاعدة البيانات وقدم توصيات أمنية.

سياق قاعدة البيانات:
[أدخل: نوع قاعدة البيانات (PostgreSQL/MySQL/MongoDB/Redis/Elasticsearch)، ORM المستخدم، تصنيف حساسية البيانات، متطلبات الامتثال، بيئة النشر]

وفقاً لأفضل ممارسات أمن قواعد البيانات ومتطلبات الامتثال، قدم:

1. **أمن الاستعلامات**
   - استراتيجيات منع حقن SQL
   - تنفيذ الاستعلامات المُعلمّة
   - تكوين أمان ORM (Sequelize، TypeORM، Prisma)
   - أمان الإجراءات المخزنة
   - التخفيف من SQL الديناميكي

2. **التحكم في الوصول**
   - تصميم أذونات مستخدم قاعدة البيانات (مبدأ الامتياز الأقل)
   - تنفيذ التحكم في الوصول القائم على الأدوار
   - تكوين أمن مستوى الصف
   - أنماط الوصول للبيانات القائمة على العرض
   - أمان تجميع الاتصالات

3. **أمن الاتصال**
   - تكوين TLS/SSL لاتصالات قاعدة البيانات
   - أمان سلسلة الاتصال (عدم وجود بيانات اعتماد مشفرة)
   - أفضل ممارسات تجميع الاتصالات
   - تدوير بيانات اعتماد قاعدة البيانات
   - متطلبات تقسيم الشبكة

4. **حماية البيانات**
   - تنفيذ التشفير على مستوى العمود
   - تكوين تشفير البيانات الشامل (TDE)
   - استراتيجيات إخفاء البيانات
   - متطلبات تشفير النسخ الاحتياطية
   - سياسات الاحتفاظ بالبيانات وحذفها

5. **اعتبارات أمن NoSQL**
   - تكوين أمن MongoDB
   - المصادقة وقوائم التحكم في Redis
   - ميزات أمن Elasticsearch
   - الأمان على مستوى المستند
   - منع حقن خط أنابيب التجميع

6. **المراقبة والتدقيق**
   - تسجيل وتحليل الاستعلامات
   - اكتشاف الشذوذ في الوصول لقاعدة البيانات
   - تنفيذ مسار التدقيق
   - الآثار الأمنية لمراقبة الأداء
   - تكوين التنبيهات للأنشطة المشبوهة

قدم أمثلة تكوين أمنية ونصوص ترحيل للمعالجة.
```

---

## Example Output Preview

```
═══════════════════════════════════════════════════════
 DATABASE SECURITY ASSESSMENT | تقييم أمن قاعدة البيانات
═══════════════════════════════════════════════════════

┌─────────────────────────────────────────────────────┐
│ SQL INJECTION PREVENTION                             │
├─────────────────────────────────────────────────────┤
│ ❌ Vulnerable (Raw Query):                          │
│ const query = `SELECT * FROM users WHERE id = ${userId}`;│
│                                                     │
│ ✅ Secure (Parameterized):                          │
│ const query = 'SELECT * FROM users WHERE id = $1'; │
│ const result = await db.query(query, [userId]);    │
│                                                     │
│ ✅ Secure (ORM - Prisma):                           │
│ const user = await prisma.user.findUnique({        │
│   where: { id: userId }                            │
│ });                                                 │
│                                                     │
│ ✅ Secure (ORM - TypeORM):                          │
│ const user = await userRepository.findOne({        │
│   where: { id: Equal(userId) }                     │
│ });                                                 │
└─────────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────────┐
│ ROW-LEVEL SECURITY (PostgreSQL)                      │
├─────────────────────────────────────────────────────┤
│ -- Enable RLS on sensitive table                    │
│ ALTER TABLE sensitive_data ENABLE ROW LEVEL SECURITY;│
│                                                     │
│ -- Create policy for tenant isolation               │
│ CREATE POLICY tenant_isolation ON sensitive_data    │
│   USING (tenant_id = current_setting('app.tenant_id')::uuid);│
│                                                     │
│ -- Grant access to application role                 │
│ GRANT SELECT, INSERT, UPDATE ON sensitive_data      │
│   TO app_role;                                      │
└─────────────────────────────────────────────────────┘

DATABASE USER PERMISSIONS MATRIX:
┌─────────────────────────────────────────────────────┐
│ Role           │ Tables      │ Operations │ Notes   │
│────────────────│─────────────│────────────│─────────│
│ app_readonly   │ All         │ SELECT     │ Reports │
│ app_readwrite  │ business_*  │ CRUD       │ App API │
│ app_admin      │ All         │ ALL        │ Mgmt    │
│ migration_user │ All         │ DDL        │ Deploy  │
└─────────────────────────────────────────────────────┘

CONNECTION STRING SECURITY:
┌─────────────────────────────────────────────────────┐
│ # Environment Variables (Recommended)               │
│ DATABASE_URL=postgresql://user:pass@host:5432/db   │
│                                                     │
│ # Kubernetes Secret                                 │
│ apiVersion: v1                                      │
│ kind: Secret                                        │
│ metadata:                                           │
│   name: db-credentials                              │
│ type: Opaque                                        │
│ stringData:                                         │
│   DATABASE_URL: "postgresql://..."                  │
│                                                     │
│ # Prisma Schema                                     │
│ datasource db {                                     │
│   provider = "postgresql"                           │
│   url      = env("DATABASE_URL")                    │
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
