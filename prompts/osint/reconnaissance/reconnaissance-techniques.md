# Reconnaissance Techniques - OSINT Prompts

> A comprehensive collection of bilingual (English/Arabic) prompts for target profiling, domain enumeration, email harvesting, and reconnaissance methodologies.

---

## Prompt 1: Target Profiling & Footprinting

### Description
Conduct comprehensive target profiling and footprinting for authorized security assessments including organizational structure analysis, technology stack identification, and attack surface mapping.

### Tags
`target-profiling` `footprinting` `attack-surface` `organization-analysis` `reconnaissance`

---

## 🇬🇧 English Prompt

```
You are a security researcher conducting authorized reconnaissance for a penetration testing engagement. Develop a comprehensive target profiling framework:

**Phase 1: Organization Intelligence**

**Corporate Structure:**
- Company hierarchy and key personnel
- Subsidiaries and acquisitions
- Partner and vendor relationships
- Geographic presence and office locations
- Business lines and revenue streams

**Employee Intelligence:**
- Key personnel identification (executives, IT admins, developers)
- Employee count and growth patterns
- Technology skills and certifications
- Social media presence analysis
- Recruitment and job posting intelligence

**Phase 2: Technical Infrastructure**

**External Infrastructure:**
- Domain portfolio and acquisitions
- DNS infrastructure analysis
- Mail server configuration (SPF, DKIM, DMARC)
- SSL/TLS certificate analysis
- Hosting provider identification

**Cloud & SaaS Footprint:**
- Cloud provider identification (AWS, Azure, GCP)
- SaaS application usage
- Collaboration platform identification
- Development infrastructure (GitHub, GitLab)
- Third-party service dependencies

**Technology Stack:**
- Web framework and CMS identification
- Programming languages and frameworks
- Database technologies
- Server operating systems
- Third-party libraries and versions

**Phase 3: Attack Surface Mapping**

**Internet-Facing Assets:**
- Web applications and portals
- API endpoints and documentation
- Remote access infrastructure (VPN, RDP)
- Email and collaboration services
- Customer-facing applications

**Shadow IT Discovery:**
- Unsanctioned cloud services
- Employee-developed applications
- Test and development environments
- Forgotten or legacy systems

**Phase 4: Vulnerability Intelligence**

**Historical Data:**
- Previous breach history
- CVE database for identified technologies
- Bug bounty program findings (if public)
- Security disclosure history

**Configuration Issues:**
- Misconfigured services
- Information disclosure
- Default credentials
- Outdated software versions

**OSINT Tools Reference:**
- WHOIS, DNSDumpster, Sublist3r
- Shodan, Censys, BinaryEdge
- BuiltWith, Wappalyzer, WhatRuns
- TheHarvester, SpiderFoot, Maltego
- LinkedIn, job boards, annual reports

**Output Requirements:**
- Executive summary report
- Detailed infrastructure map
- Attack surface diagram
- Key personnel list
- Technology inventory
- Risk prioritization matrix
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت باحث أمني تجري استطلاعاً مصرحاً لعملية اختبار الاختراق. طور إطاراً شاملاً لتوصيف الهدف:

**المرحلة 1: استخبارات المنظمة**

**الهيكل المؤسسي:**
- التسلسل الهرمي للشركة والأشخاص الرئيسيين
- الشركات التابعة والاستحواذات
- علاقات الشركاء والموردين
- الوجود الجغرافي ومواقع المكاتب
- خطوط الأعمال وتدفقات الإيرادات

**استخبارات الموظفين:**
- تحديد الأشخاص الرئيسيين (التنفيذيين، مسؤولي IT، المطورين)
- عدد الموظفين وأنماط النمو
- المهارات التقنية والشهادات
- تحليل الوجود على وسائل التواصل الاجتماعي
- استخبارات التوظيف وإعلانات الوظائف

**المرحلة 2: البنية التحتية التقنية**

**البنية التحتية الخارجية:**
- محفظة النطاقات والاستحواذات
- تحليل البنية التحتية DNS
- تكوين خادم البريد (SPF, DKIM, DMARC)
- تحليل شهادات SSL/TLS
- تحديد مزود الاستضافة

**البصمة السحابية و SaaS:**
- تحديد مزود الخدمة السحابية (AWS, Azure, GCP)
- استخدام تطبيقات SaaS
- تحديد منصة التعاون
- البنية التحتية للتطوير (GitHub, GitLab)
- تبعيات الخدمات الخارجية

**مجموعة التقنيات:**
- تحديد إطار الويب ونظام إدارة المحتوى
- لغات البرمجة والأطر
- تقنيات قواعد البيانات
- أنظمة تشغيل الخوادم
- المكتبات الخارجية والإصدارات

**المرحلة 3: رسم خريطة سطح الهجوم**

**الأصول المواجهة للإنترنت:**
- تطبيقات الويب والبوابات
- نقاط نهاية API والوثائق
- البنية التحتية للوصول عن بعد (VPN, RDP)
- خدمات البريد والتعاون
- التطبيقات المواجهة للعملاء

**اكتشاف تكنولوجيا المعلومات الظلية:**
- الخدمات السحابية غير المعتمدة
- التطبيقات التي طورها الموظفون
- بيئات الاختبار والتطوير
- الأنظمة المنسية أو القديمة

**المرحلة 4: استخبارات الثغرات**

**البيانات التاريخية:**
- تاريخ الاختراقات السابقة
- قاعدة بيانات CVE للتقنيات المحددة
- نتائج برنامج مكافآت الأخطاء (إن وجدت)
- تاريخ الإفصاح الأمني

**مشاكل التكوين:**
- الخدمات غير المكوّنة بشكل صحيح
- كشف المعلومات
- بيانات الاعتماد الافتراضية
- إصدارات البرامج القديمة

**أدوات OSINT المرجعية:**
- WHOIS, DNSDumpster, Sublist3r
- Shodan, Censys, BinaryEdge
- BuiltWith, Wappalyzer, WhatRuns
- TheHarvester, SpiderFoot, Maltego
- LinkedIn, لوحات الوظائف، التقارير السنوية

**متطلبات المخرجات:**
- تقرير الملخص التنفيذي
- خريطة البنية التحتية المفصلة
- مخطط سطح الهجوم
- قائمة الأشخاص الرئيسيين
- جرد التقنيات
- مصفوفة أولويات المخاطر
```

---

## Example Output Preview

```
# Target Profile Report - Acme Corporation

## Executive Summary
**Target:** Acme Corporation (acmecorp.com)
**Assessment Date:** January 2024
**Risk Level:** Medium-High

## Organization Intelligence

### Corporate Structure
- **Headquarters:** San Francisco, CA
- **Employees:** 2,500+ (LinkedIn analysis)
- **Subsidiaries:** 3 identified (TechStartup Inc, DataCo, CloudServ)
- **Key Executives:**
  - CEO: John Smith (@jsmithCEO)
  - CTO: Jane Doe (@jdoeCTO)
  - CISO: Mike Johnson (@mjohnsonCISO)

### Technology Stack Identified
| Category | Technology | Version | Risk Level |
|----------|------------|---------|------------|
| Web Server | nginx | 1.18.0 | Medium |
| Framework | React | 17.x | Low |
| CMS | WordPress | 5.9 | High |
| Database | PostgreSQL | 13.x | Low |
| Cloud | AWS | N/A | Low |

## Infrastructure Summary
- **Domains:** 47 identified
- **Subdomains:** 234 identified
- **Public IPs:** 12 ranges
- **Cloud Services:** AWS (primary), Azure (secondary)

## Attack Surface Map
```
[Internet]
    ├── www.acmecorp.com (WordPress 5.9) ⚠️
    ├── api.acmecorp.com (REST API)
    ├── mail.acmecorp.com (O365)
    ├── vpn.acmecorp.com (Cisco AnyConnect)
    ├── dev.acmecorp.com (Exposed) ⚠️⚠️
    ├── jira.acmecorp.com (Jira Cloud)
    └── github.com/acmecorp (Public repos)
```

## Key Findings
1. **Critical:** Development environment exposed (dev.acmecorp.com)
2. **High:** WordPress version outdated with known CVEs
3. **Medium:** SPF record too permissive
4. **Low:** Server version disclosure in headers

## Recommendations
1. Immediately secure or take down development environment
2. Update WordPress to latest version
3. Implement stricter SPF policy
4. Remove server version headers
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 2: Domain Enumeration & Subdomain Discovery

### Description
Perform comprehensive domain enumeration and subdomain discovery using passive and active techniques for attack surface identification.

### Tags
`domain-enumeration` `subdomain-discovery` `dns-analysis` `attack-surface` `infrastructure-mapping`

---

## 🇬🇧 English Prompt

```
You are a penetration tester conducting authorized domain enumeration. Develop a comprehensive subdomain discovery methodology:

**Section 1: Passive Enumeration Techniques**

**Certificate Transparency Logs:**
- Query CT logs for SSL certificates
- Tools: crt.sh, Censys, Google CT logs
- Identify subdomains from SAN fields
- Track certificate issuance history

**Search Engine Discovery:**
- Google dorking for subdomains
- Site: operator variations
- File type searches for internal references
- Cached and archived content analysis

**Third-Party Data Sources:**
- DNS aggregation services (SecurityTrails, DNSDB)
- Historical DNS records
- WHOIS database correlation
- Passive DNS replication services

**Section 2: Active Enumeration Techniques**

**DNS Bruteforce:**
- Wordlist-based enumeration
- Tools: Sublist3r, Gobuster, DNSRecon
- Recursive subdomain discovery
- Permutation generation

**DNS Records Analysis:**
- Zone transfer attempts (AXFR)
- Record type enumeration (A, AAAA, CNAME, MX, TXT, NS, SOA)
- Wildcard detection methodology
- DNSSEC analysis

**Virtual Host Discovery:**
- Host header manipulation
- Mass virtual host scanning
- Tools: VHostScan, gobuster vhost mode

**Section 3: Cloud & SaaS Discovery**

**Cloud Storage:**
- AWS S3 bucket discovery
- Azure Blob storage enumeration
- Google Cloud Storage identification
- DigitalOcean Spaces discovery

**SaaS Applications:**
- Office 365 tenant identification
- Google Workspace enumeration
- Salesforce org discovery
- Slack workspace identification

**Section 4: Subdomain Takeover Assessment**

**Vulnerable Services:**
- Identify dangling DNS records
- Cloud service verification
- GitHub Pages, Heroku, AWS S3
- Azure services, Google Cloud

**Takeover Verification:**
- HTTP response analysis
- Service fingerprinting
- False positive reduction

**Section 5: Analysis & Prioritization**

**Asset Classification:**
- Production vs. development vs. staging
- Business criticality assessment
- Technology stack identification
- Data sensitivity indicators

**Output Requirements:**
- Complete subdomain inventory
- DNS record enumeration
- Takeover vulnerability report
- Asset classification matrix
- Recommended scope for testing
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت مختبر اختراق تجري تعداد نطاقات مصرحاً به. طور منهجية شاملة لاكتشاف النطاقات الفرعية:

**القسم 1: تقنيات التعداد السلبي**

**سجلات شفافية الشهادات:**
- استعلام سجلات CT لشهادات SSL
- الأدوات: crt.sh, Censys, سجلات Google CT
- تحديد النطاقات الفرعية من حقول SAN
- تتبع تاريخ إصدار الشهادات

**اكتشاف محركات البحث:**
- Google dorking للنطاقات الفرعية
- تباينات مشغل site:
- عمليات بحث نوع الملف للمراجع الداخلية
- تحليل المحتوى المؤرشف والمخزن

**مصادر البيانات الخارجية:**
- خدمات تجميع DNS (SecurityTrails, DNSDB)
- سجلات DNS التاريخية
- ارتباط قاعدة بيانات WHOIS
- خدمات نسخ DNS السلبي

**القسم 2: تقنيات التعداد النشط**

**القوة الغاشمة DNS:**
- التعداد القائم على قوائم الكلمات
- الأدوات: Sublist3r, Gobuster, DNSRecon
- اكتشاف النطاقات الفرعية المتكرر
- توليد التباديل

**تحليل سجلات DNS:**
- محاولات نقل المنطقة (AXFR)
- تعداد أنواع السجلات (A, AAAA, CNAME, MX, TXT, NS, SOA)
- منهجية كشف البدائل
- تحليل DNSSEC

**اكتشاف المضيف الافتراضي:**
- التلاعب برأس المضيف
- فحص المضيف الافتراضي الجماعي
- الأدوات: VHostScan, gobuster وضع vhost

**القسم 3: اكتشاف السحابة و SaaS**

**التخزين السحابي:**
- اكتشاف حاويات AWS S3
- تعداد تخزين Azure Blob
- تحديد Google Cloud Storage
- اكتشاف DigitalOcean Spaces

**تطبيقات SaaS:**
- تحديد مستأجر Office 365
- تعداد Google Workspace
- اكتشاف منظمة Salesforce
- تحديد مساحة عمل Slack

**القسم 4: تقييم الاستيلاء على النطاق الفرعي**

**الخدمات الضعيفة:**
- تحديد سجلات DNS المعلقة
- التحقق من الخدمات السحابية
- GitHub Pages, Heroku, AWS S3
- خدمات Azure, Google Cloud

**التحقق من الاستيلاء:**
- تحليل استجابة HTTP
- البصمة الخدمية
- تقليل الإيجابيات الكاذبة

**القسم 5: التحليل والأولويات**

**تصنيف الأصول:**
- الإنتاج مقابل التطوير مقابل التدريج
- تقييم الأهمية التجارية
- تحديد مجموعة التقنيات
- مؤشرات حساسية البيانات

**متطلبات المخرجات:**
- جرد النطاقات الفرعية الكامل
- تعداد سجلات DNS
- تقرق ثغرات الاستيلاء
- مصفوفة تصنيف الأصول
- النطاق الموصى به للاختبار
```

---

## Example Output Preview

```
# Domain Enumeration Report - target.com

## Summary Statistics
- **Root Domains:** 3
- **Total Subdomains:** 847
- **Alive Hosts:** 623
- **Takeover Vulnerable:** 12
- **Cloud Assets:** 156

## Enumeration Methodology Results

| Technique | Subdomains Found | Unique |
|-----------|------------------|--------|
| CT Logs (crt.sh) | 523 | 412 |
| DNS Bruteforce | 289 | 156 |
| Search Engines | 178 | 89 |
| Historical DNS | 134 | 67 |
| Virtual Hosts | 45 | 23 |

## Subdomain Inventory (Sample)

| Subdomain | IP Address | Service | Risk |
|-----------|------------|---------|------|
| www.target.com | 104.18.32.7 | Cloudflare | Low |
| api.target.com | 10.0.0.1 | Internal | Medium |
| dev.target.com | 52.14.23.11 | AWS EC2 | High |
| staging.target.com | 40.76.12.89 | Azure | Medium |
| mail.target.com | 23.45.67.89 | O365 | Low |
| vpn.target.com | 12.34.56.78 | Cisco VPN | Medium |
| old.target.com | 192.0.2.1 | **TAKEOVER** | Critical |
| ftp.target.com | 198.51.100.1 | File Server | High |

## Subdomain Takeover Assessment

### Confirmed Vulnerable
| Subdomain | Service | Status | Exploitable |
|-----------|---------|--------|-------------|
| old.target.com | GitHub Pages | CNAME points to deleted repo | Yes |
| blog.target.com | Heroku | App not found | Yes |
| staging-app.target.com | AWS S3 | Bucket does not exist | Yes |

### DNS Records Analysis
```
target.com.      IN  SOA   ns1.target.com. admin.target.com.
target.com.      IN  A     104.18.32.7
target.com.      IN  MX    10 target-com.mail.protection.outlook.com.
target.com.      IN  TXT   "v=spf1 include:_spf.google.com ~all"
target.com.      IN  TXT   "MS=ms12345678"
api.target.com.  IN  A     10.0.0.1 (Private IP - Internal)
www.target.com.  IN  CNAME target.com.
```

## Cloud Assets Discovered
- **AWS:** 23 S3 buckets, 12 EC2 instances
- **Azure:** 8 VMs, 3 Storage accounts
- **GCP:** 2 Compute instances

## Recommendations
1. **Critical:** Remediate 12 subdomain takeover vulnerabilities immediately
2. **High:** Review exposed internal IP references in DNS
3. **Medium:** Implement subdomain monitoring program
4. **Low:** Clean up unused DNS records
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 3: Email Harvesting & Analysis

### Description
Conduct comprehensive email harvesting and analysis for authorized security assessments including email format discovery, credential exposure monitoring, and social engineering risk assessment.

### Tags
`email-harvesting` `email-intelligence` `credential-exposure` `social-engineering` `communication-analysis`

---

## 🇬🇧 English Prompt

```
You are a security researcher conducting authorized email intelligence gathering. Develop a comprehensive email harvesting and analysis framework:

**Section 1: Email Discovery Techniques**

**Public Sources:**
- Search engine harvesting (Google, Bing, DuckDuckGo)
- Social media profile extraction
- Professional networks (LinkedIn, business directories)
- Public documents and PDF metadata
- Code repositories (GitHub, GitLab)
- Mailing list archives
- Conference speaker bios

**Email Format Analysis:**
- Pattern identification (firstname.lastname, firstlast, f.lastname)
- Format verification through validation
- Organization-wide format inference
- Historical format changes

**Technical Discovery:**
- DNS MX record analysis
- Email server enumeration
- SPF/DKIM/DMARC record analysis
- Autodiscover service probing

**Section 2: Email Validation & Verification**

**Validation Techniques:**
- SMTP verification (VRFY, RCPT TO)
- Catch-all detection methodology
- Disposable email identification
- Role account identification

**Tools Integration:**
- TheHarvester, Hunter.io, EmailRep
- GHunt, Holehe, EmailHarvester
- Custom SMTP validation scripts

**Section 3: Credential Exposure Analysis**

**Breach Intelligence:**
- Have I Been Pwned API integration
- DeHashed, LeakCheck queries
- Paste site monitoring
- Dark web credential exposure
- Historical breach correlation

**Password Pattern Analysis:**
- Password reuse indicators
- Organizational password patterns
- Seasonal/organizational password themes

**Section 4: Social Engineering Risk Assessment**

**Target Prioritization:**
- Executive and high-value targets
- IT administrator identification
- New employee vulnerability
- Department-based targeting

**Contact Intelligence:**
- Phone number correlation
- Social media linkage
- Job role and responsibilities
- Organizational relationships

**Section 5: Email Infrastructure Security**

**Security Posture:**
- SPF record effectiveness
- DKIM implementation status
- DMARC policy enforcement
- STARTTLS support
- Anti-phishing measures

**Risk Metrics:**
- Email spoofing vulnerability
- Domain reputation score
- Blacklist status
- Configuration issues

**Output Requirements:**
- Email inventory with metadata
- Format pattern documentation
- Credential exposure report
- Social engineering risk assessment
- Security posture analysis
- Remediation recommendations
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت باحث أمني تجري جمع معلومات البريد الإلكتروني مصرحاً به. طور إطاراً شاملاً لحصاد وتحليل البريد الإلكتروني:

**القسم 1: تقنيات اكتشاف البريد الإلكتروني**

**المصادر العامة:**
- الحصاد من محركات البحث (Google, Bing, DuckDuckGo)
- استخراج ملفات التواصل الاجتماعي
- الشبكات المهنية (LinkedIn، أدلة الأعمال)
- المستندات العامة وبيانات PDF الوصفية
- مستودعات الكود (GitHub, GitLab)
- أرشيفات القوائم البريدية
- السير الذاتية للمتحدثين في المؤتمرات

**تحليل تنسيق البريد الإلكتروني:**
- تحديد الأنماط (الاسم.اللقب، الاسمالأخير، ا.اللقب)
- التحقق من التنسيق عبر التحقق
- استنتاج التنسيق على مستوى المنظمة
- التغييرات التاريخية في التنسيق

**الاكتشاف التقني:**
- تحليل سجل DNS MX
- تعداد خادم البريد الإلكتروني
- تحليل سجلات SPF/DKIM/DMARC
- استكشاف خدمة الاكتشاف التلقائي

**القسم 2: التحقق من البريد الإلكتروني**

**تقنيات التحقق:**
- التحقق من SMTP (VRFY, RCPT TO)
- منهجية كشف catch-all
- تحديد البريد الإلكتروني المؤقت
- تحديد حسابات الأدوار

**تكامل الأدوات:**
- TheHarvester, Hunter.io, EmailRep
- GHunt, Holehe, EmailHarvester
- نصوص التحقق من SMTP المخصصة

**القسم 3: تحليل كشف بيانات الاعتماد**

**استخبارات الاختراقات:**
- تكامل API مع Have I Been Pwned
- استعلامات DeHashed, LeakCheck
- مراقبة مواقع اللصق
- كشف بيانات الاعتماد على الويب المظلم
- ارتباط الاختراقات التاريخية

**تحليل أنماط كلمات المرور:**
- مؤشرات إعادة استخدام كلمات المرور
- أنماط كلمات المرور التنظيمية
- سمات كلمات المرور الموسمية/التنظيمية

**القسم 4: تقييم مخاطر الهندسة الاجتماعية**

**أولوية الأهداف:**
- التنفيذيون والأهداف عالية القيمة
- تحديد مسؤولي IT
- ضعف الموظفين الجدد
- الاستهداف القائم على القسم

**استخبارات جهات الاتصال:**
- ارتباط أرقام الهواتف
- الربط بوسائل التواصل الاجتماعي
- الدور الوظيفي والمسؤوليات
- العلاقات التنظيمية

**القسم 5: أمن البنية التحتية للبريد الإلكتروني**

**الوضع الأمني:**
- فعالية سجل SPF
- حالة تنفيذ DKIM
- إنفاذ سياسة DMARC
- دعم STARTTLS
- تدابير مكافحة التصيد

**مقاييس المخاطر:**
- ضعف انتحال البريد الإلكتروني
- درجة سمعة النطاق
- حالة القائمة السوداء
- مشاكل التكوين

**متطلبات المخرجات:**
- جرد البريد الإلكتروني مع البيانات الوصفية
- توثيق أنماط التنسيق
- تقرق كشف بيانات الاعتماد
- تقييم مخاطر الهندسة الاجتماعية
- تحليل الوضع الأمني
- توصيات المعالجة
```

---

## Example Output Preview

```
# Email Intelligence Report - target.com

## Email Format Analysis

### Discovered Formats
| Format | Pattern | Confidence | Examples Found |
|--------|---------|------------|----------------|
| Primary | first.last@target.com | 85% | john.smith@target.com |
| Secondary | flast@target.com | 12% | jsmith@target.com |
| Legacy | firstlast@target.com | 3% | johnsmith@target.com |

### Validation Results
- **Total Discovered:** 2,347 emails
- **Verified Active:** 1,892 (80.6%)
- **Catch-all Domain:** Yes
- **Role Accounts:** 45 identified

## Email Inventory by Department

| Department | Count | Key Contacts |
|------------|-------|--------------|
| Executive | 23 | CEO, CFO, CTO, CISO |
| IT/Security | 156 | SysAdmins, DevOps, Security |
| Finance | 89 | Accounting, Payroll |
| HR | 34 | Recruiting, Benefits |
| Sales | 423 | Sales Representatives |
| Engineering | 567 | Developers, QA |

## Credential Exposure Analysis

### Breach Exposure Summary
| Email Domain | Total Exposed | Breach Sources |
|--------------|---------------|----------------|
| target.com | 347 | LinkedIn (2016), Collection #1 |
| subsidiary.com | 89 | Adobe (2013), Dropbox (2012) |

### High-Risk Exposures
| Email | Breach | Password Pattern | Risk Level |
|-------|--------|------------------|------------|
| admin@target.com | Collection #1 | Summer2020! | Critical |
| it-admin@target.com | LinkedIn 2016 | Target123! | Critical |
| cfo@target.com | Multiple | Company@2021 | High |

## Email Security Posture

### DNS Configuration
```
target.com. IN TXT "v=spf1 include:_spf.google.com include:spf.protection.outlook.com ~all"
target.com. IN TXT "MS=ms12345678"
_dmarc.target.com. IN TXT "v=DMARC1; p=none; rua=mailto:dmarc@target.com"
```

### Security Assessment
| Control | Status | Risk |
|---------|--------|------|
| SPF | Present (~all) | Medium |
| DKIM | Enabled | Low |
| DMARC | p=none | High |
| STARTTLS | Enabled | Low |
| Blacklisted | No | Low |

## Social Engineering Risk Assessment

### High-Value Targets
1. **admin@target.com** - IT Administrator, credentials exposed
2. **cfo@target.com** - CFO, public profile, password reused
3. **hr@target.com** - HR Department, role account

### Attack Vectors
- Credential stuffing (347 valid emails with known passwords)
- Spear phishing to executives (23 high-profile targets)
- Password reset attacks (format patterns documented)

## Recommendations
1. **Critical:** Enable DMARC enforcement (p=reject)
2. **Critical:** Force password reset for exposed accounts
3. **High:** Implement MFA for all accounts
4. **Medium:** Conduct security awareness training for exposed users
5. **Low:** Standardize email format and document policy
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 4: Network Infrastructure Mapping

### Description
Map and analyze network infrastructure through passive and active reconnaissance including IP enumeration, service identification, and network topology discovery.

### Tags
`network-mapping` `infrastructure-reconnaissance` `service-enumeration` `topology-discovery` `asset-discovery`

---

## 🇬🇧 English Prompt

```
You are a network security analyst conducting authorized infrastructure reconnaissance. Develop a comprehensive network mapping framework:

**Section 1: IP Range Discovery**

**Public IP Identification:**
- WHOIS database queries for netblocks
- ASN enumeration and BGP analysis
- Regional Internet Registry (RIR) data
- Historical IP allocation records
- Cloud provider IP range correlation

**IP Range Expansion:**
- Adjacent IP space analysis
- Subnet inference from known hosts
- CDN and load balancer mapping
- Anycast IP identification

**Section 2: Service Enumeration**

**Port Scanning Methodology:**
- TCP SYN scanning techniques
- UDP service discovery
- Service version detection
- Operating system fingerprinting
- Script-based vulnerability detection

**Service Identification:**
- Banner grabbing and analysis
- Protocol fingerprinting
- SSL/TLS certificate analysis
- HTTP header analysis
- Service-specific probing

**Section 3: Infrastructure Analysis**

**Load Balancer Detection:**
- DNS round-robin identification
- HTTP load balancer headers
- SSL certificate variations
- IP diversity analysis

**CDN Identification:**
- IP ownership analysis
- HTTP headers (CF-Ray, X-CDN)
- DNS CNAME patterns
- Geographic distribution

**Cloud Provider Mapping:**
- AWS, Azure, GCP IP range matching
- Service-specific endpoint identification
- Multi-cloud architecture detection
- Container orchestration indicators

**Section 4: Network Topology Discovery**

**Routing Analysis:**
- Traceroute path mapping
- MPLS and VPN detection
- Firewall and IDS positioning
- Network segmentation identification

**Internal Network Inference:**
- Private IP disclosure in headers
- Internal DNS names in certificates
- Email header analysis
- Error message leakage

**Section 5: Vulnerability Assessment**

**Service Vulnerabilities:**
- CVE correlation for identified services
- Default credential testing
- Misconfiguration detection
- Outdated service identification

**Network Security Analysis:**
- Firewall rule inference
- Network segmentation gaps
- Exposure of sensitive services
- Remote access security

**Tools & Techniques:**
- Nmap, Masscan, Rustscan
- Shodan, Censys, BinaryEdge
- Traceroute, mtr, tracepath
- SSL analysis tools

**Output Requirements:**
- Network topology diagram
- Service inventory matrix
- IP allocation summary
- Cloud infrastructure map
- Vulnerability assessment report
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت محلل أمن شبكي تجري استطلاع البنية التحتية مصرحاً به. طور إطاراً شاملاً لرسم خرائط الشبكة:

**القسم 1: اكتشاف نطاقات IP**

**تحديد IP العام:**
- استعلامات قاعدة بيانات WHOIS للكتل الشبكية
- تعداد ASN وتحليل BGP
- بيانات سجلات الإنترنت الإقليمية (RIR)
- سجلات تخصيص IP التاريخية
- ارتباط نطاقات IP لمزود السحابة

**توسيع نطاق IP:**
- تحليل مساحة IP المجاورة
- استنتاج الشبكة الفرعية من المضيفات المعروفة
- رسم خرائط CDN وموازنات الحمل
- تحديد IPAnycast

**القسم 2: تعداد الخدمات**

**منهجية فحص المنافذ:**
- تقنيات فحص TCP SYN
- اكتشاف خدمات UDP
- كشف إصدار الخدمة
- البصمة لنظام التشغيل
- الكشف عن الثغرات القائم على النصوص

**تحديد الخدمة:**
- استيلاء الشعارات وتحليلها
- البصمة البروتوكولية
- تحليل شهادات SSL/TLS
- تحليل رؤوس HTTP
- التحقيق الخاص بالخدمة

**القسم 3: تحليل البنية التحتية**

**كشف موازن الحمل:**
- تحديد DNS round-robin
- رؤوس موازن حمل HTTP
- تباينات شهادات SSL
- تحليل تنوع IP

**تحديد CDN:**
- تحليل ملكية IP
- رؤوس HTTP (CF-Ray, X-CDN)
- أنماط DNS CNAME
- التوزيع الجغرافي

**رسم خرائط مزود السحابة:**
- مطابقة نطاقات IP لـ AWS, Azure, GCP
- تحديد نقاط النهاية الخاصة بالخدمة
- كشف بنية السحابة المتعددة
- مؤشرات تنسيق الحاويات

**القسم 4: اكتشاف طبولوجيا الشبكة**

**تحليل التوجيه:**
- رسم خريطة مسار Traceroute
- كشف MPLS و VPN
- تحديد موضع جدار الحماية و IDS
- تحديد تقسيم الشبكة

**استنتاج الشبكة الداخلية:**
- كشف IP الخاص في الرؤوس
- أسماء DNS الداخلية في الشهادات
- تحليل رؤوس البريد الإلكتروني
- تسريب رسائل الخطأ

**القسم 5: تقييم الثغرات**

**ثغرات الخدمة:**
- ارتباط CVE للخدمات المحددة
- اختبار بيانات الاعتماد الافتراضية
- كشف التكوين الخاطئ
- تحديد الخدمات القديمة

**تحليل أمن الشبكة:**
- استنتاج قواعد جدار الحماية
- فجوات تقسيم الشبكة
- كشف الخدمات الحساسة
- أمن الوصول عن بعد

**الأدوات والتقنيات:**
- Nmap, Masscan, Rustscan
- Shodan, Censys, BinaryEdge
- Traceroute, mtr, tracepath
- أدوات تحليل SSL

**متطلبات المخرجات:**
- مخطط طبولوجيا الشبكة
- مصفوفة جرد الخدمات
- ملخص تخصيص IP
- خريطة البنية التحتية السحابية
- تقرق تقييم الثغرات
```

---

## Example Output Preview

```
# Network Infrastructure Report - target.com

## IP Allocation Summary

### Public IP Ranges
| CIDR | Owner | Type | Services |
|------|-------|------|----------|
| 104.18.32.0/24 | Cloudflare | CDN | Web Traffic |
| 52.14.0.0/16 | AWS | Cloud | EC2, S3 |
| 40.76.0.0/14 | Azure | Cloud | VMs, Storage |
| 198.51.100.0/24 | Target Corp | Own | Mail, VPN |

### IP Inventory
- **Total Public IPs:** 127
- **Cloud-hosted:** 89 (70%)
- **On-premises:** 38 (30%)

## Service Enumeration Results

### Port Distribution
| Port | Service | Count | Risk Level |
|------|---------|-------|------------|
| 443 | HTTPS | 45 | Low |
| 80 | HTTP | 32 | Medium |
| 22 | SSH | 8 | Medium |
| 3389 | RDP | 4 | High |
| 25 | SMTP | 3 | Medium |
| 3306 | MySQL | 2 | High |

### High-Risk Services Exposed
| IP Address | Port | Service | Version | CVEs |
|------------|------|---------|---------|------|
| 198.51.100.15 | 3389 | RDP | Windows 2016 | CVE-2019-0708 |
| 198.51.100.20 | 3306 | MySQL | 5.7.12 | CVE-2016-6662 |
| 52.14.23.11 | 22 | SSH | OpenSSH 7.4 | Medium |

## Network Topology Map

```
Internet
    │
    ├── Cloudflare (CDN/WAF)
    │       ├── www.target.com (104.18.32.7)
    │       └── api.target.com (104.18.32.8)
    │
    ├── AWS Infrastructure
    │       ├── dev.target.com (52.14.23.11) [EC2]
    │       ├── staging.target.com (52.14.23.12) [EC2]
    │       └── storage.target.com (S3 Bucket)
    │
    └── On-Premises
            ├── mail.target.com (198.51.100.10)
            ├── vpn.target.com (198.51.100.20)
            └── rdp.target.com (198.51.100.15) ⚠️
```

## Cloud Infrastructure Analysis

### AWS Services Identified
| Service | Endpoint | Purpose |
|---------|----------|---------|
| EC2 | 3 instances | Web servers |
| S3 | 5 buckets | Static content |
| RDS | 1 instance | Database |
| CloudFront | 2 distributions | CDN |

### Security Groups Analysis
- **Overly Permissive:** 2 security groups allow 0.0.0.0/0
- **SSH Open:** 3 instances exposed to internet
- **Database Exposed:** 1 RDS instance public

## Vulnerability Summary

| Severity | Count | Examples |
|----------|-------|----------|
| Critical | 2 | BlueKeep RDP, Exposed MySQL |
| High | 5 | Outdated SSH, Public database |
| Medium | 12 | Missing security headers |
| Low | 23 | Information disclosure |

## Recommendations
1. **Critical:** Patch or disable RDP exposure (BlueKeep vulnerability)
2. **Critical:** Restrict MySQL to internal access only
3. **High:** Implement VPN requirement for SSH access
4. **Medium:** Review AWS security group rules
5. **Low:** Implement security headers on all web services
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 5: Google Dorking & Advanced Search Techniques

### Description
Utilize advanced Google search operators and dorking techniques for targeted information discovery, sensitive file identification, and reconnaissance automation.

### Tags
`google-dorking` `advanced-search` `information-disclosure` `file-discovery` `search-operators`

---

## 🇬🇧 English Prompt

```
You are an OSINT specialist utilizing advanced search techniques for authorized reconnaissance. Develop a comprehensive Google dorking framework:

**Section 1: Search Operator Fundamentals**

**Basic Operators:**
- site: - Domain and subdomain restriction
- inurl: - URL pattern matching
- intitle: - Title text matching
- intext: - Body content matching
- filetype: - Document type filtering
- ext: - File extension filtering
- cache: - Cached version retrieval

**Advanced Operators:**
- "exact phrase" - Exact match
- OR / | - Boolean OR
- - (minus) - Exclusion
- * (asterisk) - Wildcard
- .. (range) - Number range
- related: - Similar sites
- info: - Site information

**Section 2: Reconnaissance Dork Categories**

**Directory & File Discovery:**
```
site:target.com intitle:"index of" /admin
site:target.com intitle:"index of" /backup
site:target.com intitle:"index of" /config
site:target.com filetype:sql "insert into"
site:target.com ext:log | ext:txt | ext:conf
```

**Sensitive Document Discovery:**
```
site:target.com filetype:pdf "confidential"
site:target.com filetype:docx "internal use only"
site:target.com filetype:xlsx "salary" OR "payroll"
site:target.com filetype:pptx "roadmap" OR "strategy"
site:target.com filetype:pdf "password" OR "credential"
```

**Login & Admin Pages:**
```
site:target.com inurl:admin intitle:login
site:target.com inurl:wp-admin
site:target.com inurl:cpanel
site:target.com inurl:phpmyadmin
site:target.com inurl:administrator
```

**Configuration & Credentials:**
```
site:target.com filetype:env "DB_PASSWORD"
site:target.com filetype:yaml "password"
site:target.com filetype:xml "password"
site:target.com "jdbc:mysql://" filetype:java
site:target.com "api_key" OR "apikey" filetype:json
```

**Section 3: Technology-Specific Dorks**

**WordPress:**
```
site:target.com inurl:wp-content/uploads
site:target.com filetype:sql "WordPress"
site:target.com "Powered by WordPress" inurl:readme
```

**Apache/Nginx:**
```
site:target.com intitle:"Apache Status"
site:target.com inurl:server-status
site:target.com intitle:"nginx status"
```

**Cloud Services:**
```
site:s3.amazonaws.com "target.com"
site:blob.core.windows.net "target"
site:storage.googleapis.com "target"
site:drive.google.com "target.com confidential"
```

**Section 4: Automation & Tooling**

**Dork Automation Tools:**
- GoogleDorks, DorkMe, Dork-Scanner
- Pagodo (Passive Google Dork)
- Custom Python scripts with Google API
- Browser automation for complex queries

**Rate Limiting & Detection Avoidance:**
- Query throttling strategies
- Proxy rotation implementation
- User-agent variation
- CAPTCHA handling procedures

**Section 5: Analysis & Documentation**

**Result Classification:**
- Sensitivity rating (Public/Internal/Confidential)
- Exposure risk assessment
- Remediation priority
- False positive identification

**Report Structure:**
- Dork query used
- Results summary
- Sensitive data identified
- Recommended remediation
- Evidence screenshots

**Output Requirements:**
- Comprehensive dork list
- Query execution log
- Findings documentation
- Risk assessment matrix
- Remediation recommendations
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت متخصص OSINT تستخدم تقنيات بحث متقدمة للاستطلاع المصرح به. طور إطاراً شاملاً لـ Google Dorking:

**القسم 1: أساسيات مشغلات البحث**

**المشغلات الأساسية:**
- site: - تقييد النطاق والنطاق الفرعي
- inurl: - مطابقة نمط URL
- intitle: - مطابقة نص العنوان
- intext: - مطابقة محتوى النص
- filetype: - تصفية نوع المستند
- ext: - تصفية امتداد الملف
- cache: - استرجاع النسخة المخزنة

**المشغلات المتقدمة:**
- "عبارة دقيقة" - مطابقة تامة
- OR / | - أو المنطقية
- - (ناقص) - الاستبعاد
- * (نجمة) - البدل
- .. (نطاق) - نطاق الأرقام
- related: - مواقع مشابهة
- info: - معلومات الموقع

**القسم 2: فئات Dork للاستطلاع**

**اكتشاف الأدلة والملفات:**
```
site:target.com intitle:"index of" /admin
site:target.com intitle:"index of" /backup
site:target.com intitle:"index of" /config
site:target.com filetype:sql "insert into"
site:target.com ext:log | ext:txt | ext:conf
```

**اكتشاف المستندات الحساسة:**
```
site:target.com filetype:pdf "confidential"
site:target.com filetype:docx "internal use only"
site:target.com filetype:xlsx "salary" OR "payroll"
site:target.com filetype:pptx "roadmap" OR "strategy"
site:target.com filetype:pdf "password" OR "credential"
```

**صفحات تسجيل الدخول والمسؤول:**
```
site:target.com inurl:admin intitle:login
site:target.com inurl:wp-admin
site:target.com inurl:cpanel
site:target.com inurl:phpmyadmin
site:target.com inurl:administrator
```

**التكوينات وبيانات الاعتماد:**
```
site:target.com filetype:env "DB_PASSWORD"
site:target.com filetype:yaml "password"
site:target.com filetype:xml "password"
site:target.com "jdbc:mysql://" filetype:java
site:target.com "api_key" OR "apikey" filetype:json
```

**القسم 3: Dorks الخاصة بالتقنيات**

**WordPress:**
```
site:target.com inurl:wp-content/uploads
site:target.com filetype:sql "WordPress"
site:target.com "Powered by WordPress" inurl:readme
```

**Apache/Nginx:**
```
site:target.com intitle:"Apache Status"
site:target.com inurl:server-status
site:target.com intitle:"nginx status"
```

**الخدمات السحابية:**
```
site:s3.amazonaws.com "target.com"
site:blob.core.windows.net "target"
site:storage.googleapis.com "target"
site:drive.google.com "target.com confidential"
```

**القسم 4: الأتمتة والأدوات**

**أدوات أتمتة Dork:**
- GoogleDorks, DorkMe, Dork-Scanner
- Pagodo (Passive Google Dork)
- نصوص Python مخصصة مع Google API
- أتمتة المتصفح للاستعلامات المعقدة

**تحديد المعدل وتجنب الكشف:**
- استراتيجيات اختناق الاستعلام
- تنفيذ تدوير الوكيل
- تباين وكيل المستخدم
- إجراءات التعامل مع CAPTCHA

**القسم 5: التحليل والتوثيق**

**تصنيف النتائج:**
- تصنيف الحساسية (عام/داخلي/سري)
- تقييم مخاطر الكشف
- أولوية المعالجة
- تحديد الإيجابيات الكاذبة

**هيكل التقرير:**
- استعلام Dork المستخدم
- ملخص النتائج
- البيانات الحساسة المحددة
- المعالجة الموصى بها
- لقطات شاشة للأدلة

**متطلبات المخرجات:**
- قائمة dorks شاملة
- سجل تنفيذ الاستعلام
- توثيق النتائج
- مصفوفة تقييم المخاطر
- توصيات المعالجة
```

---

## Example Output Preview

```
# Google Dorking Reconnaissance Report - target.com

## Execution Summary
- **Total Queries Executed:** 127
- **Unique Findings:** 89
- **Critical Exposures:** 12
- **High-Risk Findings:** 34

## Critical Findings

### 1. Exposed Database Backup
**Query:** `site:target.com filetype:sql "insert into"`

**Result:** https://target.com/backup/database_backup_2024.sql
**Content:** Full database dump with user credentials (hashed)
**Risk:** Critical - Credential exposure, data breach

### 2. Configuration File Exposure
**Query:** `site:target.com filetype:env "DB_PASSWORD"`

**Result:** https://dev.target.com/.env
**Content:**
```
DB_HOST=internal-db.target.com
DB_PASSWORD=Sup3rS3cr3tP@ss!
AWS_ACCESS_KEY=AKIAIOSFODNN7EXAMPLE
AWS_SECRET_KEY=wJalrXUtnFEMI/K7MDENG
```
**Risk:** Critical - Database and AWS credentials exposed

### 3. Employee Directory Leaked
**Query:** `site:target.com filetype:xlsx "employee" "contact"`

**Result:** https://target.com/docs/Employee_Directory_2024.xlsx
**Content:** 500+ employee names, emails, phone numbers, departments
**Risk:** High - Social engineering attack vector

## Findings by Category

| Category | Findings | Critical | High | Medium |
|----------|----------|----------|------|--------|
| Config Files | 23 | 4 | 8 | 11 |
| Database Dumps | 5 | 3 | 2 | 0 |
| Employee Data | 12 | 2 | 5 | 5 |
| Admin Panels | 8 | 1 | 4 | 3 |
| Sensitive Documents | 41 | 2 | 15 | 24 |

## Sensitive Documents Found

| File | Type | Exposure | Remediation |
|------|------|----------|-------------|
| /backup/db.sql | Database | Credentials | Remove immediately |
| /.env | Config | API Keys | Move to secrets manager |
| /Employee_Directory.xlsx | Spreadsheet | PII | Restrict access |
| /financial_report_q4.pdf | PDF | Financial Data | Add authentication |
| /password_policy.docx | Document | Security info | Remove from public |

## Dork Query Reference

### Most Effective Queries
1. `site:target.com filetype:sql` - 3 critical database exposures
2. `site:target.com filetype:env "password"` - 2 config file exposures
3. `site:target.com intitle:"index of" /backup` - 5 backup directories
4. `site:s3.amazonaws.com "target.com"` - 2 public S3 buckets
5. `site:target.com inurl:admin` - 4 admin interfaces

## Recommendations
1. **Critical:** Remove all exposed credential files immediately
2. **Critical:** Rotate all compromised passwords and API keys
3. **High:** Implement access controls on sensitive documents
4. **High:** Review and secure backup directories
5. **Medium:** Conduct regular Google dork audits
6. **Low:** Add robots.txt entries for sensitive paths
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team
