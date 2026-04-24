# Dependency Security Prompts

A comprehensive collection of bilingual (English/Arabic) prompts for dependency security analysis, covering supply chain security, vulnerable dependencies, and SBOM management.

---

## Prompt 1: Supply Chain Security Assessment

### Description
Comprehensive methodology for assessing and securing the software supply chain, including dependency verification, integrity checking, and supply chain attack prevention.

### Tags
`supply-chain` `dependency-security` `software-integrity` `sbom`

---

## 🇬🇧 English Prompt

```
You are a supply chain security specialist conducting a comprehensive assessment of software supply chain security. Analyze the dependency management practices and provide security recommendations.

PROJECT CONTEXT:
[Insert: programming language(s), package managers used, deployment pipeline, CI/CD platform, registry usage (npm/PyPI/Maven), third-party services, compliance requirements]

Following SLSA framework and supply chain security best practices, provide:

1. **Dependency Source Verification**
   - Package registry security assessment
   - Private registry implementation recommendations
   - Package provenance verification
   - Namespace squatting detection
   - Typosquatting vulnerability assessment

2. **Integrity Verification**
   - Lockfile integrity validation
   - Checksum verification implementation
   - GPG signing verification
   - SRI (Subresource Integrity) for web assets
   - Sigstore/cosign for container images

3. **Supply Chain Attack Vectors**
   - Dependency confusion attack prevention
   - Compromised maintainer scenario
   - Malicious package detection
   - Build pipeline injection prevention
   - Dependency hijacking mitigation

4. **SLSA Framework Implementation**
   - Build provenance requirements
   - Source integrity verification
   - Build process attestation
   - Software artifact verification
   - Supply chain levels assessment

5. **Vendor and Third-Party Risk**
   - Third-party library risk assessment
   - License compliance verification
   - End-of-life dependency identification
   - Security SLA requirements
   - Vendor security assessment criteria

6. **Monitoring and Response**
   - Dependency vulnerability monitoring
   - Security advisory subscription
   - Incident response for supply chain attacks
   - Dependency freeze procedures
   - Emergency patching workflow

Provide implementation checklists and configuration examples.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت متخصص في أمن سلسلة التوريد تجري تقييماً شاملاً لأمن سلسلة توريد البرمجيات. حلل ممارسات إدارة التبعيات وقدم توصيات أمنية.

سياق المشروع:
[أدخل: لغة/لغات البرمجة، مديرو الحزم المستخدمون، خط أنابيب النشر، منصة CI/CD، استخدام السجل (npm/PyPI/Maven)، خدمات الطرف الثالث، متطلبات الامتثال]

وفقاً لإطار SLSA وأفضل ممارسات أمن سلسلة التوريد، قدم:

1. **التحقق من مصدر التبعية**
   - تقييم أمن سجل الحزم
   - توصيات تنفيذ السجل الخاص
   - التحقق من مصدر الحزمة
   - اكتشاف احتلال مساحة الاسم
   - تقييم ثغرة انتحال الكتابة

2. **التحقق من السلامة**
   - التحقق من سلامة ملف القفل
   - تنفيذ التحقق من البصمة
   - التحقق من توقيع GPG
   - SRI (سلامة المورد الفرعي) لأصول الويب
   - Sigstore/cosign لصور الحاويات

3. **متجهات هجوم سلسلة التوريد**
   - منع هجوم الخلط بين التبعيات
   - سيناريو المشرف المخترق
   - اكتشاف الحزم الضارة
   - منع حقن خط أنابيب البناء
   - التخفيف من اختطاف التبعية

4. **تنفيذ إطار SLSA**
   - متطلبات مصدر البناء
   - التحقق من سلامة المصدر
   - شهادة عملية البناء
   - التحقق من التحف البرمجية
   - تقييم مستويات سلسلة التوريد

5. **مخاطر البائعين والطرف الثالث**
   - تقييم مخاطر مكتبات الطرف الثالث
   - التحقق من الامتثال للترخيص
   - تحديد التبعيات منتهية العمر
   - متطلبات اتفاقية مستوى الخدمة الأمنية
   - معايير تقييم أمن البائع

6. **المراقبة والاستجابة**
   - مراقبة ثغرات التبعيات
   - اشتراكات النشرات الأمنية
   - الاستجابة للحوادث لهجمات سلسلة التوريد
   - إجراءات تجميد التبعيات
   - سير عمل الترقيع الطارئ

قدم قوائم تحقق للتنفيذ وأمثلة التكوين.
```

---

## Example Output Preview

```
═══════════════════════════════════════════════════════
 SUPPLY CHAIN SECURITY ASSESSMENT | تقييم أمن سلسلة التوريد
═══════════════════════════════════════════════════════

SLSA COMPLIANCE MATRIX:
┌─────────────────────────────────────────────────────┐
│ Requirement                      │ Current │ Target │
│─────────────────────────────────│─────────│────────│
│ Source - Provenance             │ Level 1 │ Level 3│
│ Build - Hermetic                │ No      │ Yes    │
│ Build - Reproducible            │ Partial │ Yes    │
│ Provenance - Generation         │ Manual  │ Auto   │
│ Provenance - Verification       │ No      │ Yes    │
│─────────────────────────────────│─────────│────────│
│ Overall SLSA Level              │ Level 1 │ Level 3│
└─────────────────────────────────────────────────────┘

DEPENDENCY CONFUSION ATTACK PREVENTION:
┌─────────────────────────────────────────────────────┐
│ ❌ VULNERABLE CONFIGURATION:                        │
│ # .npmrc - Mixed registries                        │
│ registry=https://registry.npmjs.org                │
│ @company:registry=https://npm.company.com         │
│ # Attackers can register @company packages        │
│ # on public npm with newer versions               │
│                                                     │
│ ✅ SECURE CONFIGURATION:                            │
│ # .npmrc - Scoped registry with authentication    │
│ @company:registry=https://npm.company.com         │
│ //npm.company.com/:_authToken=${NPM_TOKEN}        │
│                                                     │
│ # Prevent public registry fallback                 │
│ registry=https://npm.company.com                   │
│ always-auth=true                                   │
│ strict-ssl=true                                    │
└─────────────────────────────────────────────────────┘

PACKAGE VERIFICATION WORKFLOW:
┌─────────────────────────────────────────────────────┐
│                                                     │
│  [Developer]                                        │
│      │                                              │
│      ▼                                              │
│  ┌─────────────┐                                   │
│  │ Commit Code │                                   │
│  └─────────────┘                                   │
│      │                                              │
│      ▼                                              │
│  ┌─────────────────────────────────────────────┐   │
│  │ CI Pipeline                                  │   │
│  ├─────────────────────────────────────────────┤   │
│  │ 1. Verify lockfile integrity                 │   │
│  │    npm ci --ignore-scripts                  │   │
│  │    sha256sum package-lock.json              │   │
│  │                                              │   │
│  │ 2. Scan for vulnerabilities                  │   │
│  │    npm audit --audit-level=high             │   │
│  │    trivy fs .                               │   │
│  │                                              │   │
│  │ 3. Verify package signatures                 │   │
│  │    cosign verify $IMAGE                     │   │
│  │                                              │   │
│  │ 4. Generate SBOM                             │   │
│  │    syft packages dir:. -o spdx-json         │   │
│  │                                              │   │
│  │ 5. Build with provenance                    │   │
│  │    goreleaser --rm-dist                     │   │
│  └─────────────────────────────────────────────┘   │
│      │                                              │
│      ▼                                              │
│  ┌─────────────┐                                   │
│  │  Artifact   │                                   │
│  │  Registry   │                                   │
│  └─────────────┘                                   │
│                                                     │
└─────────────────────────────────────────────────────┘

MALICIOUS PACKAGE INDICATORS:
┌─────────────────────────────────────────────────────┐
│ Indicator                  │ Risk Level │ Action    │
│────────────────────────────│────────────│───────────│
│ New maintainer ( < 7 days) │ High       │ Review    │
│ Version bump + code change │ Medium     │ Diff check│
│ Install scripts            │ Critical   │ Block     │
│ Network calls in code      │ Critical   │ Block     │
│ eval/Function usage        │ High       │ Review    │
│ Minified code in package   │ Medium     │ Inspect   │
│ Typosquatting similarity   │ Critical   │ Block     │
│ Postinstall scripts        │ High       │ Review    │
└─────────────────────────────────────────────────────┘

GITHUB ACTIONS SUPPLY CHAIN SECURITY:
┌─────────────────────────────────────────────────────┐
│ name: Supply Chain Security                         │
│ on: [push, pull_request]                            │
│                                                     │
│ jobs:                                               │
│   verify:                                           │
│     runs-on: ubuntu-latest                          │
│     permissions:                                    │
│       id-token: write                               │
│       contents: read                                │
│     steps:                                          │
│       - uses: actions/checkout@v3                   │
│                                                     │
│       - name: Verify Dependencies                   │
│         uses: actions/dependency-review-action@v3  │
│                                                     │
│       - name: Generate SBOM                         │
│         uses: anchore/sbom-action@v0               │
│         with:                                       │
│           format: spdx-json                         │
│           output-file: sbom.spdx.json              │
│                                                     │
│       - name: Sign Artifact                         │
│         uses: sigstore/cosign-installer@v3         │
│         run: |                                      │
│           cosign sign --yes ${{ env.IMAGE }}       │
│                                                     │
│       - name: Verify SLSA Provenance               │
│         uses: slsa-framework/slsa-verifier@v2      │
│         with:                                       │
│           attestation: provenance.json             │
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

## Prompt 2: Vulnerable Dependency Detection

### Description
Comprehensive approach to detecting and managing vulnerable dependencies, including automated scanning, vulnerability databases, and remediation strategies.

### Tags
`vulnerability-scanning` `dependency-audit` `cve` `security-advisory`

---

## 🇬🇧 English Prompt

```
You are a security engineer responsible for dependency vulnerability management. Conduct a comprehensive analysis of vulnerable dependencies and provide remediation guidance.

PROJECT CONTEXT:
[Insert: language/framework, dependency count, package manager, vulnerability scanner used, risk tolerance, SLA requirements, deployment frequency]

Following NIST and industry best practices for vulnerability management, provide:

1. **Vulnerability Scanning Strategy**
   - Automated scanning tool selection (Snyk, Dependabot, OWASP DC)
   - Scan frequency and triggers
   - CI/CD pipeline integration
   - False positive management
   - Severity threshold configuration

2. **Vulnerability Prioritization**
   - CVSS score interpretation
   - Exploitability assessment
   - Business context prioritization
   - Reachability analysis
   - Environmental factors consideration

3. **Remediation Strategies**
   - Patch vs upgrade decisions
   - Backport security fixes
   - Alternative package evaluation
   - Breaking change assessment
   - Risk acceptance criteria

4. **Vulnerability Intelligence**
   - CVE database monitoring
   - Security advisory tracking
   - Exploit database monitoring
   - Threat intelligence integration
   - Zero-day vulnerability handling

5. **Compliance and Reporting**
   - Vulnerability metrics tracking
   - SLA compliance monitoring
   - Regulatory compliance (PCI, SOC2)
   - Executive reporting formats
   - Audit trail documentation

6. **Emergency Response**
   - Critical vulnerability workflow
   - Emergency patching procedures
   - Mitigation when patch unavailable
   - Communication protocols
   - Post-incident review

Provide scanning configurations and remediation workflow examples.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت مهندس أمن مسؤول عن إدارة ثغرات التبعيات. أجرِ تحليلاً شاملاً للتبعيات الضعيفة وقدم إرشادات المعالجة.

سياق المشروع:
[أدخل: اللغة/الإطار، عدد التبعيات، مدير الحزم، الماسح الضوئي للثغرات المستخدم، التسامح مع المخاطر، متطلبات SLA، تكرار النشر]

وفقاً لـ NIST وأفضل الممارسات الصناعية لإدارة الثغرات، قدم:

1. **استراتيجية المسح الضوئي للثغرات**
   - اختيار أداة المسح الآلي (Snyk، Dependabot، OWASP DC)
   - تكرار ومحفزات المسح
   - التكامل مع خط أنابيب CI/CD
   - إدارة الإيجابيات الكاذبة
   - تكوين عتبة الخطورة

2. **أولوية الثغرات**
   - تفسير درجة CVSS
   - تقييم القابلية للاستغلال
   - أولوية سياق الأعمال
   - تحليل قابلية الوصول
   - مراعاة العوامل البيئية

3. **استراتيجيات المعالجة**
   - قرارات الترقيع مقابل الترقية
   - إصلاحات أمنية للإصدارات السابقة
   - تقييم الحزم البديلة
   - تقييم التغييرات الجذرية
   - معايير قبول المخاطر

4. **استخبارات الثغرات**
   - مراقبة قاعدة بيانات CVE
   - تتبع النشرات الأمنية
   - مراقبة قاعدة بيانات الاستغلال
   - تكامل استخبارات التهديدات
   - التعامل مع الثغرات اليوم الصفري

5. **الامتثال والتقارير**
   - تتبع مقاييس الثغرات
   - مراقبة الامتثال لـ SLA
   - الامتثال التنظيمي (PCI، SOC2)
   - تنسيقات التقارير التنفيذية
   - توثيق مسار التدقيق

6. **الاستجابة الطارئة**
   - سير عمل الثغرات الحرجة
   - إجراءات الترقيع الطارئ
   - التخفيف عندما لا يتوفر ترقيع
   - بروتوكولات التواصل
   - مراجعة ما بعد الحادث

قدم تكوينات المسح وأمثلة سير عمل المعالجة.
```

---

## Example Output Preview

```
═══════════════════════════════════════════════════════
 VULNERABLE DEPENDENCY REPORT | تقرير التبعيات الضعيفة
═══════════════════════════════════════════════════════

EXECUTIVE SUMMARY:
┌─────────────────────────────────────────────────────┐
│ Total Dependencies:        847                      │
│ Direct Dependencies:       156                      │
│ Vulnerable Packages:       23                       │
│ Critical Vulnerabilities:   3                       │
│ High Vulnerabilities:       7                       │
│ Medium Vulnerabilities:     8                       │
│ Low Vulnerabilities:        5                       │
└─────────────────────────────────────────────────────┘

CRITICAL VULNERABILITIES:
┌─────────────────────────────────────────────────────┐
│ CVE-2024-21626 | CVSS: 9.8 | CRITICAL               │
├─────────────────────────────────────────────────────┤
│ Package:       com.example:logging-lib:1.2.3       │
│ Vulnerability: Remote Code Execution               │
│ Fixed In:      1.2.5                               │
│ Dependency:    Direct                              │
│ Reachability:  Reachable                           │
│                                                     │
│ Description:                                        │
│ Deserialization vulnerability allows RCE when      │
│ processing untrusted log messages.                 │
│                                                     │
│ Affected Paths:                                     │
│ src/main/java/com/app/Logger.java → logging-lib   │
│                                                     │
│ Exploit Status: PoC Available                      │
│                                                     │
│ Remediation:                                        │
│ mvn versions:use-next-releases -Dincludes=        │
│   com.example:logging-lib                          │
│                                                     │
│ SLA Due Date:  24 hours (Critical)                 │
│ Assigned To:   security-team                       │
└─────────────────────────────────────────────────────┘

VULNERABILITY SEVERITY BREAKDOWN:
┌─────────────────────────────────────────────────────┐
│ Package               │ CVE          │ CVSS │ Fix   │
│───────────────────────│──────────────│──────│───────│
│ lodash@4.17.15        │ CVE-2021-23337│ 7.2 │ 4.17.21│
│ axios@0.21.1          │ CVE-2021-3749│ 7.5 │ 0.21.4│
│ moment@2.29.0         │ CVE-2022-31129│ 7.5 │ 2.29.4│
│ minimist@1.2.5        │ CVE-2021-44906│ 9.8 │ 1.2.8│
│ jsonwebtoken@8.5.1    │ CVE-2022-23529│ 9.8 │ 9.0.0│
│ node-fetch@2.6.0      │ CVE-2022-0235│ 8.1 │ 2.6.7│
└─────────────────────────────────────────────────────┘

REMEDIATION WORKFLOW:
┌─────────────────────────────────────────────────────┐
│                                                     │
│  ┌─────────────┐                                   │
│  │ Vulnerability│                                   │
│  │  Detected   │                                   │
│  └─────────────┘                                   │
│        │                                            │
│        ▼                                            │
│  ┌─────────────────────────────────────────────┐   │
│  │ Severity Assessment                          │   │
│  │ ├─ CVSS Score: 9.8                          │   │
│  │ ├─ Exploit Available: Yes                   │   │
│  │ ├─ Reachable: Yes                           │   │
│  │ └─ Business Impact: High                    │   │
│  └─────────────────────────────────────────────┘   │
│        │                                            │
│        ▼                                            │
│  ┌─────────────┐     ┌─────────────┐              │
│  │ Critical/   │────▶│ 24h SLA     │              │
│  │ High        │     │ Escalate    │              │
│  └─────────────┘     └─────────────┘              │
│        │                                            │
│        ▼                                            │
│  ┌─────────────────────────────────────────────┐   │
│  │ Remediation Decision                         │   │
│  │ ├─ Upgrade available? → Test & Deploy       │   │
│  │ ├─ No upgrade? → Mitigate/Alternative       │   │
│  │ └─ Breaking change? → Risk assessment       │   │
│  └─────────────────────────────────────────────┘   │
│                                                     │
└─────────────────────────────────────────────────────┘

DEPENDABOT CONFIGURATION:
┌─────────────────────────────────────────────────────┐
│ # .github/dependabot.yml                            │
│ version: 2                                          │
│ updates:                                            │
│   - package-ecosystem: "npm"                        │
│     directory: "/"                                  │
│     schedule:                                       │
│       interval: "daily"                             │
│       time: "06:00"                                 │
│     open-pull-requests-limit: 10                   │
│     reviewers:                                      │
│       - "security-team"                            │
│     labels:                                         │
│       - "security"                                  │
│       - "dependencies"                             │
│     commit-message:                                 │
│       prefix: "security"                           │
│     ignore:                                         │
│       - dependency-name: "lodash"                  │
│         versions: ["4.17.16", "4.17.17"]          │
│                                                     │
│   - package-ecosystem: "maven"                     │
│     directory: "/"                                  │
│     schedule:                                       │
│       interval: "weekly"                           │
│     groups:                                         │
│       spring-security:                             │
│         patterns:                                  │
│           - "org.springframework.security:*"      │
└─────────────────────────────────────────────────────┘

SLA COMPLIANCE METRICS:
┌─────────────────────────────────────────────────────┐
│ Severity │ SLA Target │ Avg Time │ Compliance Rate │
│──────────│────────────│──────────│─────────────────│
│ Critical │ 24 hours   │ 18 hrs   │      95%        │
│ High     │ 7 days     │ 4.2 days │      88%        │
│ Medium   │ 30 days    │ 12 days  │      92%        │
│ Low      │ 90 days    │ 45 days  │      78%        │
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

## Prompt 3: Software Bill of Materials (SBOM)

### Description
Comprehensive guide to implementing and managing Software Bill of Materials for improved supply chain visibility and security compliance.

### Tags
`sbom` `spdx` `cyclonedx` `software-transparency` `compliance`

---

## 🇬🇧 English Prompt

```
You are a software supply chain specialist implementing SBOM (Software Bill of Materials) practices. Design a comprehensive SBOM implementation strategy.

PROJECT CONTEXT:
[Insert: project size, regulatory requirements (NTIA/EO 14028), distribution model, customer requirements, build system, artifact storage, CI/CD platform]

Following NTIA minimum elements and industry standards, provide:

1. **SBOM Standards and Formats**
   - SPDX (Software Package Data Exchange) implementation
   - CycloneDX format usage
   - Format selection criteria
   - Required fields and attributes
   - Extension mechanisms

2. **SBOM Generation**
   - Build-time generation tools (Syft, Trivy, sbom-tool)
   - Package manager integration
   - Container image SBOM generation
   - Dependency tree completeness
   - VEX (Vulnerability Exploitability eXchange) integration

3. **SBOM Distribution**
   - Artifact registry integration
   - Consumer distribution methods
   - API access patterns
   - Signature and verification
   - Version control considerations

4. **SBOM Quality and Accuracy**
   - Completeness validation
   - Automated verification
   - Dependency relationship accuracy
   - License identification
   - Supplier information capture

5. **Operational Workflows**
   - SBOM update triggers
   - Change management processes
   - Vulnerability correlation
   - License compliance workflow
   - Audit preparation procedures

6. **Tool Integration**
   - CI/CD pipeline integration
   - Registry integration (Artifactory, Nexus)
   - Security tool integration
   - Dashboard and reporting
   - API automation

Provide SBOM examples, tool configurations, and workflow diagrams.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت متخصص في سلسلة توريد البرمجيات تنفذ ممارسات SBOM (قائمة مكونات البرمجيات). صمم استراتيجية تنفيذ SBOM شاملة.

سياق المشروع:
[أدخل: حجم المشروع، المتطلبات التنظيمية (NTIA/EO 14028)، نموذج التوزيع، متطلبات العملاء، نظام البناء، تخزين التحف، منصة CI/CD]

وفقاً للحد الأدنى لعناصر NTIA ومعايير الصناعة، قدم:

1. **معايير وتنسيقات SBOM**
   - تنفيذ SPDX (تبادل بيانات حزمة البرمجيات)
   - استخدام تنسيق CycloneDX
   - معايير اختيار التنسيق
   - الحقول والسمات المطلوبة
   - آليات التمديد

2. **توليد SBOM**
   - أدوات التوليد وقت البناء (Syft، Trivy، sbom-tool)
   - تكامل مدير الحزم
   - توليد SBOM لصور الحاويات
   - اكتمال شجرة التبعيات
   - تكامل VEX (تبادل قابلية استغلال الثغرات)

3. **توزيع SBOM**
   - تكامل سجل التحف
   - طرق توزيع المستهلكين
   - أنماط الوصول عبر API
   - التوقيع والتحقق
   - اعتبارات التحكم في الإصدار

4. **جودة ودقة SBOM**
   - التحقق من الاكتمال
   - التحقق الآلي
   - دقة علاقة التبعيات
   - تحديد الترخيص
   - التقاط معلومات المورد

5. **سير العمل التشغيلي**
   - محفزات تحديث SBOM
   - عمليات إدارة التغيير
   - ربط الثغرات
   - سير عمل الامتثال للترخيص
   - إجراءات التحضير للتدقيق

6. **تكامل الأدوات**
   - التكامل مع خط أنابيب CI/CD
   - تكامل السجل (Artifactory، Nexus)
   - تكامل أدوات الأمان
   - لوحة المعلومات وإعداد التقارير
   - أتمتة API

قدم أمثلة SBOM وتكوينات الأدوات ومخططات سير العمل.
```

---

## Example Output Preview

```
═══════════════════════════════════════════════════════
 SBOM IMPLEMENTATION GUIDE | دليل تنفيذ SBOM
═══════════════════════════════════════════════════════

NTIA MINIMUM ELEMENTS CHECKLIST:
┌─────────────────────────────────────────────────────┐
│ Element                        │ Status  │ Source   │
│───────────────────────────────│─────────│──────────│
│ Supplier Name                 │ ✓       │ Package  │
│ Component Name                │ ✓       │ Package  │
│ Component Version             │ ✓       │ Package  │
│ Unique Identifier             │ ✓       │ PURL     │
│ Dependency Relationship       │ ✓       │ Analysis │
│ Author of SBOM Data           │ ✓       │ Tool     │
│ Timestamp                     │ ✓       │ Build    │
│───────────────────────────────│─────────│──────────│
│ NTIA Compliance               │ 100%    │          │
└─────────────────────────────────────────────────────┘

SPDX SBOM EXAMPLE:
┌─────────────────────────────────────────────────────┐
│ SPDXVersion: SPDX-2.3                               │
│ DataLicense: CC0-1.0                                │
│ SPDXID: SPDXRef-DOCUMENT                            │
│ DocumentName: MyApp-1.0.0                           │
│ DocumentNamespace: https://company.com/sbom/       │
│   myapp-1.0.0                                       │
│ Creator: Tool: syft-0.84.0                          │
│ Created: 2024-01-15T10:30:00Z                       │
│                                                     │
│ ##### Package: logging-lib                          │
│                                                     │
│ PackageName: logging-lib                            │
│ SPDXID: SPDXRef-logging-lib-123                     │
│ PackageVersion: 1.2.5                               │
│ PackageDownloadLocation: https://repo1.maven.org/  │
│   maven2/com/example/logging-lib/1.2.5/            │
│ FilesAnalyzed: false                                │
│ PackageVerificationCode: d6a770ba38583ed4bb4525f   │
│   9678199f96c0a4d35e                                │
│ PackageLicenseConcluded: Apache-2.0                │
│ PackageLicenseDeclared: Apache-2.0                 │
│ PackageCopyrightText: NOASSERTION                  │
│ ExternalRef: PACKAGE-MANAGER purl pkg:maven/       │
│   com.example/logging-lib@1.2.5                    │
│                                                     │
│ ##### Relationship                                  │
│                                                     │
│ Relationship: SPDXRef-DOCUMENT DEPENDS_ON          │
│   SPDXRef-logging-lib-123                          │
│ Relationship: SPDXRef-logging-lib-123 DEPENDS_ON   │
│   SPDXRef-jackson-core-456                         │
└─────────────────────────────────────────────────────┘

CYCLONEDX SBOM EXAMPLE:
┌─────────────────────────────────────────────────────┐
│ {                                                   │
│   "bomFormat": "CycloneDX",                        │
│   "specVersion": "1.5",                            │
│   "serialNumber": "urn:uuid:3e671687-395b-41f5",   │
│   "version": 1,                                     │
│   "metadata": {                                     │
│     "timestamp": "2024-01-15T10:30:00Z",           │
│     "component": {                                  │
│       "type": "application",                       │
│       "name": "MyApp",                              │
│       "version": "1.0.0"                           │
│     },                                              │
│     "tools": [{                                     │
│       "vendor": "anchore",                          │
│       "name": "syft",                               │
│       "version": "0.84.0"                          │
│     }]                                              │
│   },                                                │
│   "components": [{                                  │
│     "type": "library",                              │
│     "bom-ref": "pkg:maven/com.example/logging@1.2.5",│
│     "name": "logging-lib",                          │
│     "version": "1.2.5",                            │
│     "purl": "pkg:maven/com.example/logging@1.2.5", │
│     "licenses": [{                                  │
│       "license": {                                  │
│         "id": "Apache-2.0"                         │
│       }                                             │
│     }],                                             │
│     "supplier": {                                   │
│       "name": "Example Corp"                       │
│     }                                               │
│   }]                                                │
│ }                                                   │
└─────────────────────────────────────────────────────┘

SBOM GENERATION WORKFLOW:
┌─────────────────────────────────────────────────────┐
│                                                     │
│  [Source Code]                                      │
│       │                                             │
│       ▼                                             │
│  ┌─────────────────────────────────────────────┐   │
│  │ Build Pipeline                               │   │
│  ├─────────────────────────────────────────────┤   │
│  │ 1. Checkout code                             │   │
│  │ 2. Restore dependencies                      │   │
│  │ 3. Build application                         │   │
│  │                                              │   │
│  │ # Generate SBOM                              │   │
│  │ syft packages dir:. \                        │   │
│  │   -o spdx-json=sbom.spdx.json \              │   │
│  │   -o cyclonedx-json=sbom.cdx.json           │   │
│  │                                              │   │
│  │ # Sign SBOM                                  │   │
│  │ cosign sign-blob sbom.spdx.json \           │   │
│  │   --output-signature sbom.sig               │   │
│  │                                              │   │
│  │ # Upload to registry                         │   │
│  │ curl -X PUT -H "Authorization: Bearer $TOKEN"│   │
│  │   -T sbom.spdx.json \                        │   │
│  │   $REGISTRY/sboms/myapp/1.0.0/              │   │
│  └─────────────────────────────────────────────┘   │
│       │                                             │
│       ▼                                             │
│  ┌─────────────┐                                   │
│  │ SBOM        │                                   │
│  │ Registry    │                                   │
│  └─────────────┘                                   │
│                                                     │
└─────────────────────────────────────────────────────┘

TOOL COMPARISON:
┌─────────────────────────────────────────────────────┐
│ Tool     │ Format  │ Container │ CI/CD │ VEX      │
│──────────│─────────│───────────│───────│──────────│
│ Syft     │ Both    │ ✓         │ ✓     │ Via Grype│
│ Trivy    │ Both    │ ✓         │ ✓     │ ✓        │
│ sbom-tool│ SPDX    │ ✓         │ ✓     │ ✓        │
│ CycloneDX│ CycloneDX│ ✓        │ ✓     │ ✓        │
│ Tern     │ SPDX    │ ✓         │ ✓     │ ✗        │
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

## Prompt 4: Dependency Update Management

### Description
Strategic approach to managing dependency updates including version pinning, update policies, and automated dependency management workflows.

### Tags
`dependency-update` `version-management` `renovate` `dependabot`

---

## 🇬🇧 English Prompt

```
You are a DevOps engineer responsible for dependency management strategy. Design a comprehensive dependency update management system.

PROJECT CONTEXT:
[Insert: number of repositories, team size, release frequency, risk tolerance, testing coverage, deployment model, maintenance windows]

Following semantic versioning and dependency management best practices, provide:

1. **Version Management Policy**
   - Semantic versioning interpretation
   - Version pinning vs floating versions
   - Range specification guidelines
   - Pre-release version handling
   - Lockfile management strategy

2. **Update Strategy Design**
   - Automatic vs manual update decisions
   - Update grouping strategies
   - Major version upgrade procedures
   - Security update priority
   - Maintenance window scheduling

3. **Automation Tools**
   - Dependabot configuration
   - Renovate bot setup
   - Custom automation scripts
   - Testing automation integration
   - Approval workflow automation

4. **Risk Mitigation**
   - Breaking change detection
   - Automated testing requirements
   - Staged rollout procedures
   - Rollback procedures
   - Monitoring and alerting

5. **Team Workflow**
   - PR review process for updates
   - Testing responsibilities
   - Approval matrix
   - Communication protocols
   - Documentation requirements

6. **Metrics and Monitoring**
   - Dependency freshness metrics
   - Technical debt tracking
   - Security update lag time
   - Update success rate
   - Team velocity impact

Provide configuration examples and workflow diagrams.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت مهندس DevOps مسؤول عن استراتيجية إدارة التبعيات. صمم نظام إدارة تحديث التبعيات الشامل.

سياق المشروع:
[أدخل: عدد المستودعات، حجم الفريق، تكرار الإصدار، التسامح مع المخاطر، تغطية الاختبارات، نموذج النشر، نوافذ الصيانة]

وفقاً للإصدار الدلالي وأفضل ممارسات إدارة التبعيات، قدم:

1. **سياسة إدارة الإصدارات**
   - تفسير الإصدار الدلالي
   - تثبيت الإصدار مقابل الإصدارات العائمة
   - إرشادات تحديد النطاق
   - التعامل مع إصدارات ما قبل الإصدار
   - استراتيجية إدارة ملف القفل

2. **تصميم استراتيجية التحديث**
   - قرارات التحديث التلقائي مقابل اليدوي
   - استراتيجيات تجميع التحديثات
   - إجراءات ترقية الإصدار الرئيسي
   - أولوية تحديثات الأمان
   - جدولة نافذة الصيانة

3. **أدوات الأتمتة**
   - تكوين Dependabot
   - إعداد Renovate bot
   - نصوص الأتمتة المخصصة
   - تكامل أتمتة الاختبارات
   - أتمتة سير عمل الموافقة

4. **التخفيف من المخاطر**
   - اكتشاف التغييرات الجذرية
   - متطلبات الاختبار الآلي
   - إجراءات الطرح المرحلي
   - إجراءات التراجع
   - المراقبة والتنبيه

5. **سير عمل الفريق**
   - عملية مراجعة PR للتحديثات
   - مسؤوليات الاختبار
   - مصفوفة الموافقة
   - بروتوكولات التواصل
   - متطلبات التوثيق

6. **المقاييس والمراقبة**
   - مقاييس حداثة التبعيات
   - تتبع الديون التقنية
   - وقت تأخر تحديث الأمان
   - معدل نجاح التحديث
   - تأثير سرعة الفريق

قدم أمثلة التكوين ومخططات سير العمل.
```

---

## Example Output Preview

```
═══════════════════════════════════════════════════════
 DEPENDENCY UPDATE MANAGEMENT | إدارة تحديث التبعيات
═══════════════════════════════════════════════════════

VERSION MANAGEMENT POLICY:
┌─────────────────────────────────────────────────────┐
│ Update Type │ Action      │ Testing │ Approval     │
│─────────────│─────────────│─────────│──────────────│
│ Patch       │ Auto-merge  │ Unit    │ None         │
│ Minor       │ Auto-PR     │ Full    │ 1 reviewer   │
│ Major       │ Manual PR   │ Full+Int│ 2 reviewers  │
│ Security    │ Auto-PR     │ Full    │ Security team│
│ Pre-release │ Block       │ N/A     │ Manual       │
└─────────────────────────────────────────────────────┘

RENOVATE CONFIGURATION:
┌─────────────────────────────────────────────────────┐
│ // renovate.json                                    │
│ {                                                   │
│   "extends": [                                      │
│     "config:base",                                 │
│     "group:allNonMajor"                           │
│   ],                                               │
│   "schedule": ["every weekday before 10am"],      │
│   "timezone": "America/New_York",                  │
│   "prConcurrentLimit": 5,                          │
│   "prHourlyLimit": 2,                              │
│   "rangeStrategy": "bump",                         │
│   "semanticCommits": "enabled",                    │
│   "packageRules": [                                │
│     {                                              │
│       "matchPackagePatterns": ["*"],               │
│       "matchUpdateTypes": ["minor", "patch"],     │
│       "groupName": "non-major dependencies",      │
│       "groupSlug": "all-minor-patch",             │
│       "automerge": true,                           │
│       "automergeType": "pr"                       │
│     },                                             │
│     {                                              │
│       "matchUpdateTypes": ["major"],               │
│       "bumpVersion": null,                         │
│       "labels": ["major-update", "needs-review"], │
│       "reviewers": ["team:security"],             │
│       "schedule": ["on the first day of the month"]│
│     },                                             │
│     {                                              │
│       "matchDatasources": ["npm"],                 │
│       "matchPackagePatterns": ["^@types/"],        │
│       "enabled": false                             │
│     },                                             │
│     {                                              │
│       "matchPackageNames": ["lodash"],             │
│       "allowedVersions": "<5.0.0"                  │
│     }                                              │
│   ],                                               │
│   "vulnerabilityAlerts": {                        │
│     "labels": ["security"],                        │
│     "assignees": ["security-team"],               │
│     "prPriority": 10                               │
│   }                                                │
│ }                                                  │
└─────────────────────────────────────────────────────┘

UPDATE WORKFLOW DIAGRAM:
┌─────────────────────────────────────────────────────┐
│                                                     │
│  [Renovate Bot]                                     │
│       │                                             │
│       ▼                                             │
│  ┌─────────────────────────────────────────────┐   │
│  │ PR Created                                   │   │
│  │ ├─ Grouped: Minor/Patch updates             │   │
│  │ └─ Individual: Major/Security updates       │   │
│  └─────────────────────────────────────────────┘   │
│       │                                             │
│       ▼                                             │
│  ┌─────────────────────────────────────────────┐   │
│  │ CI Pipeline                                  │   │
│  │ ├─ Unit tests                               │   │
│  │ ├─ Integration tests                        │   │
│  │ ├─ Security scan                            │   │
│  │ └─ Build verification                       │   │
│  └─────────────────────────────────────────────┘   │
│       │                                             │
│       ▼                                             │
│  ┌──────────┬────────────────────┐                 │
│  │  Tests   │       Result       │                 │
│  ├──────────┼────────────────────┤                 │
│  │  Pass    │ Auto-merge (patch) │                 │
│  │  Pass    │ Ready for review   │                 │
│  │  Fail    │ Notify & block     │                 │
│  └──────────┴────────────────────┘                 │
│       │                                             │
│       ▼                                             │
│  ┌─────────────────────────────────────────────┐   │
│  │ Approval & Merge                             │   │
│  │ ├─ Minor: 1 reviewer required               │   │
│  │ ├─ Major: 2 reviewers + testing             │   │
│  │ └─ Security: Security team approval         │   │
│  └─────────────────────────────────────────────┘   │
│                                                     │
└─────────────────────────────────────────────────────┘

DEPENDENCY FRESHNESS METRICS:
┌─────────────────────────────────────────────────────┐
│ Package          │ Current │ Latest │ Age (days)  │
│──────────────────│─────────│────────│─────────────│
│ react            │ 18.2.0  │ 18.2.0 │ 0           │
│ lodash           │ 4.17.21 │ 4.17.21│ 0           │
│ express          │ 4.18.1  │ 4.18.2 │ 45          │
│ typescript       │ 5.0.0   │ 5.3.3  │ 180         │
│──────────────────│─────────│────────│─────────────│
│ Average Age      │         │        │ 56 days     │
│ Freshness Score  │         │        │ 87%         │
└─────────────────────────────────────────────────────┘

ROLLBACK PROCEDURE:
┌─────────────────────────────────────────────────────┐
│ # Immediate Rollback Script                        │
│                                                     │
│ #!/bin/bash                                         │
│                                                     │
│ # Revert package-lock.json to previous version     │
│ git checkout HEAD~1 -- package-lock.json           │
│                                                     │
│ # Clean and reinstall                               │
│ rm -rf node_modules                                 │
│ npm ci                                              │
│                                                     │
│ # Verify application starts                         │
│ npm run health-check                                │
│                                                     │
│ # Deploy reverted version                           │
│ npm run deploy:production                           │
│                                                     │
│ # Notify team                                       │
│ slack-cli send "#dev-alerts" "Dependency rollback  │
│   completed - investigate root cause"              │
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

## Prompt 5: Private Registry Security

### Description
Comprehensive guide to implementing and securing private package registries for enterprise dependency management.

### Tags
`private-registry` `artifact-management` `npm-registry` `repository-security`

---

## 🇬🇧 English Prompt

```
You are an infrastructure security engineer implementing private package registry security. Design a comprehensive private registry security architecture.

REGISTRY CONTEXT:
[Insert: package ecosystems, registry platform (Artifactory/Nexus/Verdaccio), user count, geographic distribution, compliance requirements, existing identity provider]

Following enterprise security best practices, provide:

1. **Registry Architecture**
   - High availability design
   - Geographic distribution strategy
   - Caching and proxy configuration
   - Storage and retention policies
   - Backup and disaster recovery

2. **Access Control**
   - Authentication integration (SSO/SAML/LDAP)
   - Role-based access control design
   - Package-level permissions
   - API token management
   - Service account governance

3. **Security Controls**
   - Package scanning integration
   - Malware detection
   - License compliance checking
   - Package signing and verification
   - Repudiation prevention

4. **Proxy and Caching**
   - Upstream registry configuration
   - Cache invalidation strategy
   - Offline mode capabilities
   - Bandwidth optimization
   - Rate limiting configuration

5. **Compliance and Auditing**
   - Audit logging requirements
   - Compliance reporting
   - Retention policies
   - Data residency considerations
   - Regulatory alignment (FedRAMP, SOC2)

6. **Operational Procedures**
   - Onboarding new packages
   - Package deprecation process
   - Vulnerability response workflow
   - Maintenance procedures
   - Incident response playbook

Provide architecture diagrams, configuration examples, and security checklists.
```

---

## 🇸🇦 Arabic Prompt | بالعربية

```
أنت مهندس أمن البنية التحتية تنفذ أمن سجل الحزم الخاص. صمم بنية أمنية شاملة للسجل الخاص.

سياق السجل:
[أدخل: أنظمة الحزم، منصة السجل (Artifactory/Nexus/Verdaccio)، عدد المستخدمين، التوزيع الجغرافي، متطلبات الامتثال، مزود الهوية الموجود]

وفقاً لأفضل ممارسات أمن المؤسسات، قدم:

1. **بنية السجل**
   - تصميم التوفر العالي
   - استراتيجية التوزيع الجغرافي
   - تكوين التخزين المؤقت والوكيل
   - سياسات التخزين والاحتفاظ
   - النسخ الاحتياطي واستعادة الكوارث

2. **التحكم في الوصول**
   - تكامل المصادقة (SSO/SAML/LDAP)
   - تصميم التحكم في الوصول القائم على الأدوار
   - أذونات مستوى الحزمة
   - إدارة رموز API
   - حوكمة حسابات الخدمة

3. **ضوابط الأمان**
   - تكامل فحص الحزم
   - اكتشاف البرمجيات الخبيثة
   - فحص الامتثال للترخيص
   - توقيع والتحقق من الحزم
   - منع الإنكار

4. **الوكيل والتخزين المؤقت**
   - تكوين سجل المنبع
   - استراتيجية إبطال ذاكرة التخزين المؤقت
   - قدرات وضع عدم الاتصال
   - تحسين عرض النطاق الترددي
   - تكوين الحد من المعدل

5. **الامتثال والتدقيق**
   - متطلبات تسجيل التدقيق
   - تقارير الامتثال
   - سياسات الاحتفاظ
   - اعتبارات إقامة البيانات
   - التوافق التنظيمي (FedRAMP، SOC2)

6. **الإجراءات التشغيلية**
   - إضافة حزم جديدة
   - عملية إهمال الحزم
   - سير عمل الاستجابة للثغرات
   - إجراءات الصيانة
   - دليل الاستجابة للحوادث

قدم مخططات البنية وأمثلة التكوين وقوائم التحقق الأمنية.
```

---

## Example Output Preview

```
═══════════════════════════════════════════════════════
 PRIVATE REGISTRY SECURITY | أمن السجل الخاص
═══════════════════════════════════════════════════════

REGISTRY ARCHITECTURE:
┌─────────────────────────────────────────────────────┐
│                                                     │
│  [Developers]         [CI/CD Systems]              │
│       │                      │                      │
│       └──────────┬───────────┘                      │
│                  │                                  │
│                  ▼                                  │
│  ┌─────────────────────────────────────────────┐   │
│  │           Load Balancer (HA)                 │   │
│  └─────────────────────────────────────────────┘   │
│                  │                                  │
│       ┌──────────┼──────────┐                      │
│       ▼          ▼          ▼                      │
│  ┌─────────┐ ┌─────────┐ ┌─────────┐              │
│  │ Registry│ │ Registry│ │ Registry│              │
│  │ Node 1  │ │ Node 2  │ │ Node 3  │              │
│  └─────────┘ └─────────┘ └─────────┘              │
│       │          │          │                      │
│       └──────────┼──────────┘                      │
│                  │                                  │
│                  ▼                                  │
│  ┌─────────────────────────────────────────────┐   │
│  │         Shared Storage (S3/NFS)             │   │
│  │    ┌─────────────────────────────────┐      │   │
│  │    │ • Internal Packages              │      │   │
│  │    │ • Cached Public Packages        │      │   │
│  │    │ • Security Scan Results         │      │   │
│  │    └─────────────────────────────────┘      │   │
│  └─────────────────────────────────────────────┘   │
│                  │                                  │
│                  ▼                                  │
│  ┌─────────────────────────────────────────────┐   │
│  │         Upstream Registries                  │   │
│  │  npmjs.org │ pypi.org │ maven.central       │   │
│  └─────────────────────────────────────────────┘   │
│                                                     │
└─────────────────────────────────────────────────────┘

NEXUS REPOSITORY CONFIGURATION:
┌─────────────────────────────────────────────────────┐
│ # docker-compose.yml                                │
│ version: '3'                                        │
│ services:                                           │
│   nexus:                                            │
│     image: sonatype/nexus3:3.59.0                  │
│     environment:                                    │
│       - NEXUS_SECURITY_RANDOMPASSWORD=false        │
│       - INSTALL4J_ADD_VM_PARAMS=-Xms2g -Xmx4g     │
│       - NEXUS_SECURITY_INITIAL_PASSWORD=${NEXUS_PWD}│
│     volumes:                                        │
│       - nexus-data:/nexus-data                     │
│       - ./nexus.properties:/nexus-data/etc/nexus.properties│
│     labels:                                         │
│       - "traefik.enable=true"                      │
│       - "traefik.http.routers.nexus.rule=Host(`nexus.company.com`)"│
│     healthcheck:                                    │
│       test: ["CMD", "curl", "-f", "http://localhost:8081"]│
│       interval: 30s                                 │
│       timeout: 10s                                  │
│       retries: 3                                    │
│                                                     │
│ volumes:                                            │
│   nexus-data:                                       │
└─────────────────────────────────────────────────────┘

ACCESS CONTROL MATRIX:
┌─────────────────────────────────────────────────────┐
│ Role          │ Read │ Write │ Delete │ Admin     │
│───────────────│──────│───────│────────│────────────│
│ Developer     │  ✓   │   ✓   │   ✗    │    ✗      │
│ Team Lead     │  ✓   │   ✓   │   ✓    │    ✗      │
│ CI/CD System  │  ✓   │   ✓   │   ✗    │    ✗      │
│ Security Team │  ✓   │   ✗   │   ✓    │    ✓      │
│ Admin         │  ✓   │   ✓   │   ✓    │    ✓      │
└─────────────────────────────────────────────────────┘

PACKAGE SCANNING INTEGRATION:
┌─────────────────────────────────────────────────────┐
│ # Webhook Configuration for Scanning               │
│ {                                                   │
│   "webhooks": {                                     │
│     "package-upload": {                            │
│       "url": "https://scanner.company.com/scan",   │
│       "method": "POST",                            │
│       "headers": {                                  │
│         "Authorization": "Bearer ${WEBHOOK_TOKEN}" │
│       },                                            │
│       "onFailure": "block"                         │
│     }                                               │
│   },                                                │
│   "scanning": {                                     │
│     "enabled": true,                               │
│     "blockOnCritical": true,                       │
│     "blockOnHigh": false,                          │
│     "scanTimeout": 300,                            │
│     "reportStorage": "s3://scan-reports/"          │
│   }                                                 │
│ }                                                   │
└─────────────────────────────────────────────────────┘

AUDIT LOG EXAMPLE:
┌─────────────────────────────────────────────────────┐
│ Timestamp           │ User      │ Action │ Package │
│─────────────────────│───────────│────────│─────────│
│ 2024-01-15 10:23:45 │ jsmith    │ upload │@company/ui@2.1.0│
│ 2024-01-15 10:24:12 │ scanner   │ scan   │@company/ui@2.1.0│
│ 2024-01-15 10:24:15 │ scanner   │ approve│@company/ui@2.1.0│
│ 2024-01-15 10:30:00 │ ci-system │ download│@company/ui@2.1.0│
│ 2024-01-15 11:00:00 │ admin     │ delete │@company/old-pkg│
└─────────────────────────────────────────────────────┘

SECURITY CHECKLIST:
┌─────────────────────────────────────────────────────┐
│ Control                         │ Status │ Priority │
│─────────────────────────────────│────────│──────────│
│ SSO/SAML Integration            │ ✓      │ Critical │
│ TLS 1.3 Enforcement             │ ✓      │ Critical │
│ Package Signing Required        │ ✓      │ High     │
│ Vulnerability Scanning          │ ✓      │ High     │
│ License Compliance Check        │ ✓      │ Medium   │
│ Audit Logging Enabled           │ ✓      │ Critical │
│ Backup Configured (3-2-1)       │ ✓      │ High     │
│ Rate Limiting                   │ ✓      │ Medium   │
│ Geo-replication                 │ ✓      │ Medium   │
│ Disaster Recovery Tested        │ ✓      │ High     │
└─────────────────────────────────────────────────────┘
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team
