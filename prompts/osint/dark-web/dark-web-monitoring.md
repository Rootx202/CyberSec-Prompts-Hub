# Dark Web Monitoring - OSINT Prompts

> A comprehensive collection of bilingual (English/Arabic) prompts for dark web monitoring, threat actor tracking, credential leak detection, and underground intelligence gathering.

---

## Prompt 1: Dark Web Infrastructure & Access

### Description
Establish secure dark web monitoring infrastructure including Tor configuration, operational security measures, and safe navigation practices for intelligence gathering.

### Tags
`dark-web` `tor` `operational-security` `infrastructure` `safe-access`

---

## 🇬🇧 English Prompt

```
You are a dark web intelligence specialist setting up secure monitoring infrastructure. Develop a comprehensive dark web access and monitoring framework:

**Section 1: Infrastructure Setup**

**Tor Configuration:**
- Tor Browser hardening and security settings
- Tails OS vs. Whonix configuration
- Tor bridges and pluggable transports
- Entry/exit node selection considerations
- Circuit management and renewal

**Virtual Machine Architecture:**
- Isolated VM configuration (Whonix Gateway/Workstation)
- Network isolation best practices
- Snapshot and non-persistence setup
- Host system security measures
- Hardware isolation considerations

**Section 2: Operational Security (OpSec)**

**Identity Protection:**
- Separate monitoring identities
- Persona creation and management
- Avoiding correlation attacks
- Time zone and language considerations
- Behavioral pattern awareness

**Technical OpSec:**
- JavaScript and script blocking
- Canvas fingerprinting prevention
- WebRTC leak prevention
- DNS leak protection
- Time synchronization risks

**Section 3: Dark Web Navigation**

**Marketplace & Forum Identification:**
- Popular marketplaces and forums
- Onion directory resources
- Valid link verification
- Mirror and phishing site detection
- Invitation-only access methods

**Search & Discovery:**
- Dark web search engines (Ahmia, Torch, Haystak)
- Directory sites and link lists
- Forum search techniques
- Archive sites (Dark Fail)
- RSS feed monitoring

**Section 4: Intelligence Collection Methods**

**Passive Monitoring:**
- RSS feed aggregation
- Keyword alerting systems
- Paste site monitoring
- Marketplace listing scrapers
- Forum thread monitoring

**Active Collection:**
- Forum participation guidelines
- Vendor communication protocols
- Sample acquisition procedures
- Trust and reputation building
- Escrow and transaction safety

**Section 5: Evidence Preservation**

**Documentation Standards:**
- Screenshot procedures (metadata removal)
- Page archiving methods
- Timestamp verification
- Chain of custody maintenance
- Hash verification

**Legal Considerations:**
- Jurisdiction awareness
- Law enforcement liaison protocols
- Evidence admissibility requirements
- Privacy and data handling laws

**Output Requirements:**
- Infrastructure configuration guide
- OpSec checklist
- Resource directory
- Evidence collection procedures
- Legal compliance framework
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت متخصص في استخبارات الويب المظلم تقوم بإعداد بنية تحتية آمنة للمراقبة. طور إطاراً شاملاً للوصول إلى الويب المظلم والمراقبة:

**القسم 1: إعداد البنية التحتية**

**تكوين Tor:**
- تقوية متصفح Tor وإعدادات الأمان
- تكوين Tails OS مقابل Whonix
- جسور Tor والنقل القابل للتوصيل
- اعتبارات اختيار عقدة الدخول/الخروج
- إدارة الدائرة وتجديدها

**بنية الآلة الافتراضية:**
- تكوين VM معزول (بوابة Whonix/محطة العمل)
- أفضل ممارسات عزل الشبكة
- إعداد اللقطة وعدم الاستمرار
- تدابير أمن نظام المضيف
- اعتبارات عزل الأجهزة

**القسم 2: الأمن التشغيلي (OpSec)**

**حماية الهوية:**
- هويات مراقبة منفصلة
- إنشاء وإدارة الشخصية
- تجنب هجمات الارتباط
- اعتبارات المنطقة الزمنية واللغة
- الوعي بالأنماط السلوكية

**الأمن التقني التشغيلي:**
- حظر JavaScript والنصوص
- منع البصمة Canvas
- منع تسريب WebRTC
- حماية من تسريب DNS
- مخاطر مزامنة الوقت

**القسم 3: التنقل في الويب المظلم**

**تحديد الأسواق والمنتديات:**
- الأسواق والمنتديات الشائعة
- موارد دليل Onion
- التحقق من صحة الروابط
- كشف المواقع المرآة والتصيد
- طرق الوصول الحصري بالدعوة

**البحث والاكتشاف:**
- محركات بحث الويب المظلم (Ahmia, Torch, Haystak)
- مواقع الدليل وقوائم الروابط
- تقنيات البحث في المنتديات
- مواقع الأرشيف (Dark Fail)
- مراقبة خلاصات RSS

**القسم 4: طرق جمع الاستخبارات**

**المراقبة السلبية:**
- تجميع خلاصات RSS
- أنظمة تنبيه الكلمات الرئيسية
- مراقبة مواقع اللصق
- كاشفات قوائم السوق
- مراقبة خيوط المنتديات

**الجمع النشط:**
- إرشادات المشاركة في المنتديات
- بروتوكولات التواصل مع البائعين
- إجراءات الحصول على العينات
- بناء الثقة والسمعة
- أمان الإيداع والمعاملات

**القسم 5: حفظ الأدلة**

**معايير التوثيق:**
- إجراءات لقطة الشاشة (إزالة البيانات الوصفية)
- طرق أرشفة الصفحات
- التحقق من الطابع الزمني
- صيانة سلسلة الحيازة
- التحقق من التجزئة

**الاعتبارات القانونية:**
- الوعي بالاختصاص القضائي
- بروتوكولات الاتصال بإنفاذ القانون
- متطلبات قبول الأدلة
- قوانين الخصوصية ومعالجة البيانات

**متطلبات المخرجات:**
- دليل تكوين البنية التحتية
- قائمة تحقق OpSec
- دليل الموارد
- إجراءات جمع الأدلة
- إطار الامتثال القانوني
```

---

## Example Output Preview

```
# Dark Web Infrastructure Setup Guide

## Infrastructure Architecture

```
┌─────────────────────────────────────────────────┐
│                    Host OS                       │
│  ┌───────────────────────────────────────────┐  │
│  │          Whonix Gateway (VM)               │  │
│  │    ┌─────────────────────────────────┐    │  │
│  │    │    Tor Network Interface         │    │  │
│  │    │    - Entry Node: Random          │    │  │
│  │    │    - Middle: Random              │    │  │
│  │    │    - Exit: Country-filtered      │    │  │
│  │    └─────────────────────────────────┘    │  │
│  └───────────────────────────────────────────┘  │
│                      │                           │
│            Internal Virtual Network              │
│                      │                           │
│  ┌───────────────────────────────────────────┐  │
│  │        Whonix Workstation (VM)             │  │
│  │    ┌─────────────────────────────────┐    │  │
│  │    │  Tor Browser (Hardened)          │    │  │
│  │    │  - Security Level: Safest        │    │  │
│  │    │  - JavaScript: Disabled          │    │  │
│  │    │  - Canvas: Randomized            │    │  │
│  │    └─────────────────────────────────┘    │  │
│  └───────────────────────────────────────────┘  │
└─────────────────────────────────────────────────┘
```

## Tor Browser Configuration Checklist

### Security Settings (about:preferences#privacy)
- [ ] Security Level: Safest
- [ ] HTTPS-Only Mode: Enable
- [ ] Block dangerous content: Enable

### about:config Hardening
```
javascript.enabled = false
media.peerconnection.enabled = false
privacy.resistFingerprinting = true
webgl.disabled = true
network.websocket.enabled = false
```

## Operational Security Checklist

### Pre-Session
- [ ] Verify VM snapshot restoration
- [ ] Check for DNS leaks
- [ ] Verify Tor circuit (new identity)
- [ ] Set monitoring timezone
- [ ] Activate monitoring persona

### During Session
- [ ] Never access clearnet sites
- [ ] Block all scripts and media
- [ ] Avoid downloading files when possible
- [ ] Use separate personas per investigation
- [ ] Document all findings in real-time

### Post-Session
- [ ] Clear all session data
- [ ] Restore VM to clean snapshot
- [ ] Verify no persistence
- [ ] Secure evidence documentation
- [ ] Log session metadata

## Resource Directory

### Dark Web Search Engines
| Name | Onion Address | Purpose |
|------|--------------|---------|
| Ahmia | ahmia.fi | General search |
| Torch | xmh57jrzrnwtec... | Deep search |
| Haystak | haystak5njsmn... | Index search |

### Monitoring Targets
| Type | Examples | Priority |
|------|----------|----------|
| Data Leak Sites | HaveIBeenPwned DW, LeakCheck | High |
| Marketplaces | [Classified] | High |
| Forums | [Classified] | Medium |
| Paste Sites | Pastebin mirrors | Medium |

## Evidence Documentation Template

```
Case ID: [CASE-XXXX]
Date/Time: [UTC Timestamp]
Operator: [Anonymized ID]
Source URL: [Onion URL]
Circuit Path: [Entry-Middle-Exit countries]

### Screenshot Evidence
- File: [HASH].png
- SHA256: [hash value]
- Metadata: Removed

### Page Archive
- File: [HASH].html
- WARC: [HASH].warc

### Notes
[Detailed description of findings]
```
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 2: Threat Actor Tracking & Attribution

### Description
Track and analyze threat actors on dark web platforms including behavior analysis, TTP identification, and attribution methodology.

### Tags
`threat-actor` `attribution` `ttp-analysis` `behavioral-analysis` `threat-tracking`

---

## 🇬🇧 English Prompt

```
You are a threat intelligence analyst conducting dark web threat actor tracking. Develop a comprehensive actor tracking and attribution framework:

**Section 1: Actor Identification**

**Profile Building:**
- Username and alias tracking
- Historical account analysis
- Profile metadata extraction
- Avatar and image analysis
- Signature and bio patterns

**Activity Analysis:**
- Posting frequency and timing
- Forum sections of activity
- Interaction patterns
- Language and tone analysis
- Technical sophistication assessment

**Section 2: Technical Attribution**

**Linguistic Analysis:**
- Language patterns and native tongue indicators
- Regional spelling variations
- Idiomatic expressions
- Time zone inference from posting times
- Machine translation detection

**Technical Indicators:**
- Screenshot analysis (watermarks, system info)
- Code style and preferences
- Tool and malware usage patterns
- Infrastructure preferences
- OPSEC practices assessment

**Section 3: Behavioral Profiling**

**Motivation Assessment:**
- Financial vs. ideological drivers
- Target selection patterns
- Hacktivism indicators
- Nation-state affiliations
- Mercenary activity signs

**Skill Assessment:**
- Technical capability evaluation
- Tool development vs. usage
- Vulnerability discovery capability
- Operational security sophistication
- Social engineering aptitude

**Section 4: TTP Documentation**

**Attack Pattern Analysis:**
- MITRE ATT&CK mapping
- Unique TTP identification
- Tool and technique preferences
- Victim targeting patterns
- Operational tempo

**Infrastructure Tracking:**
- C2 server identification
- Domain registration patterns
- Hosting provider preferences
- Cryptocurrency wallet analysis
- Infrastructure reuse detection

**Section 5: Attribution Methodology**

**Evidence Weighting:**
- Primary indicators (high confidence)
- Secondary indicators (medium confidence)
- Behavioral indicators (contextual)
- Technical markers (supporting)

**Attribution Confidence:**
- High confidence criteria
- Medium confidence criteria
- Low confidence criteria
- Uncertainty documentation

**Cross-Referencing:**
- Internal threat actor database
- Public threat intelligence reports
- Industry sharing communities
- Government advisories

**Output Requirements:**
- Actor profile template
- TTP documentation matrix
- Attribution confidence report
- Timeline of activity
- Intelligence sharing format
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت محلل استخبارات تهديدات تجري تتبع جهات التهديد على الويب المظلم. طور إطاراً شاملاً لتتبع الجهات والإسناد:

**القسم 1: تحديد الجهة**

**بناء الملف الشخصي:**
- تتبع اسم المستخدم والأسماء المستعارة
- تحليل الحسابات التاريخية
- استخراج البيانات الوصفية للملف الشخصي
- تحليل الصورة الرمزية والصور
- أنماط التوقيع والسيرة الذاتية

**تحليل النشاط:**
- تكرار النشر والتوقيت
- أقسام النشاط في المنتديات
- أنماط التفاعل
- تحليل اللغة والنبرة
- تقييم التطور التقني

**القسم 2: الإسناد التقني**

**التحليل اللغوي:**
- أنماط اللغة ومؤشرات اللغة الأم
- تباينات التهجئة الإقليمية
- التعبيرات الاصطلاحية
- استنتاج المنطقة الزمنية من أوقات النشر
- كشف الترجمة الآلية

**المؤشرات التقنية:**
- تحليل لقطات الشاشة (علامات مائية، معلومات النظام)
- أسلوب الكود والتفضيلات
- أنماط استخدام الأدوات والبرمجيات الخبيثة
- تفضيلات البنية التحتية
- تقييم ممارسات OPSEC

**القسم 3: التنميط السلوكي**

**تقييم الدافع:**
- المحركات المالية مقابل الأيديولوجية
- أنماط اختيار الهدف
- مؤشرات القرصنة الناشطة
- الانتماءات الحكومية
- علامات النشاط المرتزق

**تقييم المهارات:**
- تقييم القدرة التقنية
- تطوير الأدوات مقابل الاستخدام
- قدرة اكتشاف الثغرات
- تطور الأمن التشغيلي
- الكفاءة في الهندسة الاجتماعية

**القسم 4: توثيق TTP**

**تحليل أنماط الهجوم:**
- ربط MITRE ATT&CK
- تحديد TTP الفريدة
- تفضيلات الأدوات والتقنيات
- أنماط استهداف الضحايا
- الوتيرة التشغيلية

**تتبع البنية التحتية:**
- تحديد خادم C2
- أنماط تسجيل النطاق
- تفضيلات مزود الاستضافة
- تحليل محافظ العملات المشفرة
- كشف إعادة استخدام البنية التحتية

**القسم 5: منهجية الإسناد**

**ترجيح الأدلة:**
- المؤشرات الأولية (ثقة عالية)
- المؤشرات الثانوية (ثقة متوسطة)
- المؤشرات السلوكية (سياقية)
- العلامات التقنية (داعمة)

**ثقة الإسناد:**
- معايير الثقة العالية
- معايير الثقة المتوسطة
- معايير الثقة المنخفضة
- توثيق عدم اليقين

**المرجعية المتقاطعة:**
- قاعدة بيانات جهات التهديد الداخلية
- تقارير استخبارات التهديدات العامة
- مجتمعات المشاركة الصناعية
- النصائح الحكومية

**متطلبات المخرجات:**
- قالب ملف الجهة
- مصفوفة توثيق TTP
- تقرق ثقة الإسناد
- الجدول الزمني للنشاط
- تنسيق مشاركة الاستخبارات
```

---

## Example Output Preview

```
# Threat Actor Profile Report

## Actor Overview
**Designation:** TA-2024-001 (ALPHA)
**Primary Alias:** "ShadowBroker_X"
**Active Period:** 2022 - Present
**Threat Level:** High

## Profile Summary

### Basic Information
| Attribute | Value | Confidence |
|-----------|-------|------------|
| Primary Language | Russian (native) | High |
| Time Zone | UTC+3 | High |
| Likely Origin | Eastern Europe | Medium |
| Motivation | Financial | High |
| Sophistication | Advanced | High |

### Associated Aliases
| Alias | Platform | First Seen | Status |
|-------|----------|------------|--------|
| ShadowBroker_X | Forum A | Jan 2022 | Active |
| DarkCoder_RU | Forum B | Mar 2022 | Banned |
| XShadowX | Marketplace C | Jun 2023 | Active |

## Technical Attribution

### Linguistic Indicators
- Native Russian speaker (grammar patterns)
- Uses Russian keyboard layout indicators
- Posts primarily during Moscow business hours
- Occasional machine-translated English content

### Technical Indicators
- Screenshot analysis: Windows 10, Cyrillic system language
- Preferred tools: Custom Cobalt Strike, Mimikatz
- Infrastructure: Bulletproof hosting in [REDACTED]
- Cryptocurrency: Bitcoin primary, Monero for high-value

## TTP Matrix (MITRE ATT&CK)

| Tactic | Technique | Observed Usage |
|--------|-----------|----------------|
| Initial Access | T1566.001 | Spearphishing with malicious docs |
| Execution | T1059.001 | PowerShell payloads |
| Persistence | T1053.005 | Scheduled tasks |
| Defense Evasion | T1027 | Obfuscated scripts |
| Credential Access | T1003.001 | LSASS dumping |
| Lateral Movement | T1021.001 | RDP with stolen creds |
| Exfiltration | T1048.003 | Exfiltration over HTTPS |
| Impact | T1486 | Data encryption |

## Activity Timeline

```
2024-01: Announced new ransomware variant on Forum A
2023-11: Released leaked database (Company X)
2023-09: Advertised initial access broker services
2023-06: Posted exploit for CVE-2023-XXXX
2023-03: New marketplace vendor account created
2022-01: First observed activity on Forum A
```

## Attribution Confidence Assessment

| Indicator Category | Findings | Confidence |
|-------------------|----------|------------|
| **Primary** | | |
| Language patterns | Native Russian | 95% |
| Infrastructure | Known Russian-hosted | 85% |
| **Secondary** | | |
| Timing patterns | UTC+3 timezone | 80% |
| Technical tools | Russian-language comments in code | 75% |
| **Behavioral** | | |
| Target selection | Western companies primarily | 70% |
| Ransom demands | Ruble-adjacent amounts | 60% |

**Overall Attribution Confidence: 75% - Eastern European Actor**

## Recommendations
1. Monitor all identified aliases for new activity
2. Add TTP signatures to detection systems
3. Block identified infrastructure IPs
4. Alert on linguistic indicators in phishing emails
5. Share intelligence with industry ISAC
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 3: Credential Leak Monitoring

### Description
Design comprehensive credential leak monitoring programs for detecting compromised credentials, data breach analysis, and credential exposure notification systems.

### Tags
`credential-leaks` `data-breach` `compromised-credentials` `breach-monitoring` `credential-exposure`

---

## 🇬🇧 English Prompt

```
You are a security analyst designing a credential leak monitoring program. Develop a comprehensive framework for detecting and responding to credential exposures:

**Section 1: Leak Source Identification**

**Dark Web Sources:**
- Data leak marketplaces
- Credential trading forums
- Paste sites and Telegram channels
- Ransomware leak sites
- Initial access broker postings

**Clear Web Sources:**
- Public code repositories (GitHub, GitLab)
- Document sharing platforms
- Social media exposure
- Job postings with sensitive data
- Academic and research publications

**Monitoring Infrastructure:**
- Automated scraping systems
- API integrations (Have I Been Pwned, DeHashed)
- Dark web alerting systems
- RSS feed monitoring
- Custom keyword alerts

**Section 2: Data Breach Analysis**

**Breach Assessment Framework:**
- Breach authenticity verification
- Data freshness assessment
- Affected population identification
- Data sensitivity classification
- Exposure scope determination

**Data Parsing & Normalization:**
- Format identification (CSV, SQL, JSON)
- Email validation and normalization
- Password hash identification
- Personal data extraction
- Duplicate detection and removal

**Section 3: Credential Intelligence**

**Password Analysis:**
- Hash type identification (MD5, SHA1, bcrypt)
- Cracking feasibility assessment
- Password pattern analysis
- Common password identification
- Organizational password policies inference

**Email Intelligence:**
- Corporate vs. personal email separation
- Role account identification
- Executive and high-value target flagging
- Service account detection
- Historical breach correlation

**Section 4: Impact Assessment**

**Risk Scoring:**
- Credential sensitivity weighting
- Account access level consideration
- Password strength factor
- Multi-factor authentication status
- Password age consideration

**Affected Party Identification:**
- Internal employee accounts
- Customer account exposure
- Third-party/vendor accounts
- Shared account detection
- Application-specific credentials

**Section 5: Response & Notification**

**Internal Response Protocol:**
- Severity classification
- Escalation procedures
- Immediate containment actions
- Forensic investigation triggers
- Legal notification requirements

**Notification Procedures:**
- Employee notification templates
- Customer communication guidelines
- Regulatory notification requirements
- Public disclosure decisions
- Support resource allocation

**Remediation Actions:**
- Forced password reset procedures
- Multi-factor authentication enforcement
- Session token revocation
- Account lockout protocols
- Security awareness training triggers

**Output Requirements:**
- Monitoring playbook
- Breach analysis template
- Risk assessment matrix
- Notification templates
- Response workflow documentation
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت محلل أمن تصمم برنامج مراقبة تسريب بيانات الاعتماد. طور إطاراً شاملاً للكشف عن ت عرضات بيانات الاعتماد والاستجابة لها:

**القسم 1: تحديد مصادر التسريب**

**مصادر الويب المظلم:**
- أسواق تسريب البيانات
- منتديات تداول بيانات الاعتماد
- مواقع اللصق وقنوات Telegram
- مواقع تسريب الفدية
- منشورات وسطاء الوصول الأولي

**مصادر الويب العام:**
- مستودعات الكود العامة (GitHub, GitLab)
- منصات مشاركة المستندات
- التعرض على وسائل التواصل الاجتماعي
- إعلانات الوظائف مع بيانات حساسة
- المنشورات الأكاديمية والبحثية

**البنية التحتية للمراقبة:**
- أنظمة الكشط الآلية
- تكاملات API (Have I Been Pwned, DeHashed)
- أنظمة تنبيه الويب المظلم
- مراقبة خلاصات RSS
- تنبيهات الكلمات الرئيسية المخصصة

**القسم 2: تحليل اختراق البيانات**

**إطار تقييم الاختراق:**
- التحقق من أصالة الاختراق
- تقييم حداثة البيانات
- تحديد السكان المتأثرين
- تصنيف حساسية البيانات
- تحديد نطاق التعرض

**تحليل البيانات وتطبيعها:**
- تحديد التنسيق (CSV, SQL, JSON)
- التحقق من البريد الإلكتروني وتطبيعه
- تحديد نوع تجزئة كلمة المرور
- استخراج البيانات الشخصية
- كشف التكرار وإزالته

**القسم 3: استخبارات بيانات الاعتماد**

**تحليل كلمات المرور:**
- تحديد نوع التجزئة (MD5, SHA1, bcrypt)
- تقييم جدوى الكسر
- تحليل أنماط كلمات المرور
- تحديد كلمات المرور الشائعة
- استنتاج سياسات كلمات المرور التنظيمية

**استخبارات البريد الإلكتروني:**
- فصل البريد المؤسسي عن الشخصي
- تحديد حسابات الأدوار
- وضع علامات على التنفيذيين والأهداف عالية القيمة
- كشف حسابات الخدمة
- ارتباط الاختراقات التاريخية

**القسم 4: تقييم التأثير**

**تسجيل المخاطر:**
- ترجيح حساسية بيانات الاعتماد
- اعتبار مستوى الوصول للحساب
- عامل قوة كلمة المرور
- حالة المصادقة متعددة العوامل
- اعتبار عمر كلمة المرور

**تحديد الأطراف المتأثرة:**
- حسابات الموظفين الداخليين
- تعرض حسابات العملاء
- حسابات الطرف الثالث/الموردين
- كشف الحسابات المشتركة
- بيانات الاعتماد الخاصة بالتطبيقات

**القسم 5: الاستجابة والإشعار**

**بروتوكول الاستجابة الداخلية:**
- تصنيف الخطورة
- إجراءات التصعيد
- إجراءات الاحتواء الفورية
- محفزات التحقيق الجنائي
- متطلبات الإشعار القانوني

**إجراءات الإشعار:**
- قوالب إشعار الموظفين
- إرشادات التواصل مع العملاء
- متطلبات الإشعار التنظيمي
- قرارات الإفصاح العام
- تخصيص موارد الدعم

**إجراءات المعالجة:**
- إجراءات إعادة تعيين كلمة المرور الإجبارية
- إنفاذ المصادقة متعددة العوامل
- إلغاء رمز الجلسة
- بروتوكولات قفل الحساب
- محفزات تدريب الوعي الأمني

**متطلبات المخرجات:**
- دليل التشغيل للمراقبة
- قالب تحليل الاختراق
- مصفوفة تقييم المخاطر
- قوالب الإشعار
- توثيق سير عمل الاستجابة
```

---

## Example Output Preview

```
# Credential Leak Monitoring Report

## Leak Summary
**Source:** Dark Web Marketplace
**Discovery Date:** 2024-01-15
**Original Breach Date:** 2023-12-20
**Total Records:** 2,347,891
**Affected Domains:** 127

## Breach Analysis

### Data Contents
| Field | Present | Sample Count |
|-------|---------|--------------|
| Email | Yes | 2,347,891 (100%) |
| Password Hash | Yes | 2,347,891 (100%) |
| Username | Yes | 1,892,456 (81%) |
| Full Name | Partial | 456,123 (19%) |
| Phone | Partial | 89,234 (4%) |
| Address | Partial | 34,567 (1%) |

### Password Hash Analysis
| Hash Type | Count | Cracking Difficulty |
|-----------|-------|---------------------|
| bcrypt | 1,234,567 | Hard |
| SHA-256 | 678,901 | Medium |
| MD5 | 234,567 | Easy |
| Plaintext | 199,856 | None |

## Organizational Impact

### Company Domain Analysis
**Target Domain:** company.com
**Affected Records:** 847

| Email Type | Count | Risk Level |
|------------|-------|------------|
| Corporate (@company.com) | 847 | Critical |
| Subsidiary (@sub.company.com) | 234 | High |
| Legacy (@oldcompany.com) | 89 | Medium |

### Affected Personnel Breakdown

| Department | Exposed | High-Value | Critical |
|------------|---------|------------|----------|
| Executive | 12 | 8 | 3 |
| IT/Admin | 45 | 23 | 15 |
| Finance | 67 | 12 | 5 |
| Engineering | 234 | 34 | 8 |
| Sales | 189 | 23 | 2 |
| Other | 300 | 45 | 0 |

### Critical Account Exposures

| Email | Role | Hash Type | Password Strength | MFA Status |
|-------|------|-----------|-------------------|------------|
| admin@company.com | IT Admin | MD5 | Weak | Disabled ⚠️ |
| ceo@company.com | Executive | bcrypt | Medium | Enabled ✓ |
| finance-director@company.com | Finance | SHA-256 | Weak | Disabled ⚠️ |
| dba@company.com | Database Admin | MD5 | Weak | Disabled ⚠️ |
| devops@company.com | DevOps | bcrypt | Strong | Enabled ✓ |

## Password Pattern Analysis

### Common Passwords Found
```
Company2023!     - 45 occurrences
Summer2023       - 38 occurrences
Company@123      - 34 occurrences
Welcome1         - 29 occurrences
Password123!     - 27 occurrences
```

### Policy Compliance
| Requirement | Compliant | Non-Compliant |
|-------------|-----------|---------------|
| Length ≥ 12 | 342 (40%) | 505 (60%) |
| Complexity | 289 (34%) | 558 (66%) |
| No common words | 567 (67%) | 280 (33%) |

## Response Actions

### Immediate Actions Taken
1. ✅ Verified breach authenticity with source
2. ✅ Identified all affected corporate accounts
3. ✅ Flagged 15 high-risk accounts for priority reset
4. ✅ Initiated forced password reset for all affected users
5. ✅ Enabled MFA enforcement for affected accounts

### Notification Timeline
| Action | Deadline | Status |
|--------|----------|--------|
| Executive notification | Immediate | Complete |
| IT team alert | +1 hour | Complete |
| Affected users | +4 hours | In Progress |
| Legal review | +24 hours | Pending |
| Customer notification (if applicable) | +72 hours | Pending |

### Recommended Long-term Actions
1. Implement passwordless authentication for executives
2. Deploy credential monitoring service (Have I Been Pwned API)
3. Conduct security awareness training for exposed users
4. Review and enforce password policy compliance
5. Implement breach monitoring automation
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 4: Ransomware & Extortion Monitoring

### Description
Monitor ransomware groups and extortion operations including leak site tracking, victim identification, and ransomware variant analysis.

### Tags
`ransomware` `extortion` `leak-sites` `ransomware-groups` `victim-monitoring`

---

## 🇬🇧 English Prompt

```
You are a threat intelligence analyst monitoring ransomware and extortion operations. Develop a comprehensive ransomware monitoring framework:

**Section 1: Ransomware Group Tracking**

**Group Intelligence:**
- Active ransomware groups identification
- Rebrand and spin-off tracking
- Leadership and key member identification
- Affiliate program analysis
- Historical activity timeline

**Infrastructure Tracking:**
- Leak site URL monitoring
- Tor hidden services tracking
- Payment portal identification
- Communication channels (Tox, Jabber, Session)
- Infrastructure changes and migrations

**Section 2: Leak Site Monitoring**

**Automated Monitoring:**
- New victim posting detection
- Site availability monitoring
- Content change tracking
- Countdown timer monitoring
- Archive and deletion tracking

**Victim Identification:**
- Company name extraction
- Geographic location determination
- Industry sector classification
- Revenue and size estimation
- Previous breach history

**Data Exfiltration Analysis:**
- Data type identification
- Volume estimation
- Sensitivity assessment
- Regulatory implications (GDPR, HIPAA)
- Competitive intelligence value

**Section 3: Ransomware Variant Analysis**

**Technical Analysis:**
- Malware family identification
- Encryption algorithm analysis
- File extension patterns
- Ransom note formatting
- Encryption speed and methodology

**Operational Analysis:**
- Attack vector preferences
- Lateral movement techniques
- Persistence mechanisms
- Data staging methods
- Exfiltration channels

**Section 4: Negotiation Intelligence**

**Communication Analysis:**
- Initial contact methods
- Ransom demand patterns
- Negotiation tactics
- Payment timeline expectations
- Decryption guarantee methods

**Payment Tracking:**
- Cryptocurrency wallet analysis
- Payment verification methods
- Decryptor delivery process
- Double extortion patterns
- Data deletion verification

**Section 5: Victim Support & Reporting**

**Threat Assessment:**
- Organization-specific risk evaluation
- Data exposure probability
- Regulatory notification requirements
- Reputational impact assessment
- Business continuity implications

**Intelligence Products:**
- Victim notification reports
- Industry threat advisories
- Quarterly trend analysis
- Annual ransomware landscape report
- Executive briefings

**Output Requirements:**
- Group tracking database
- Leak site monitoring playbook
- Victim identification workflow
- Variant analysis template
- Threat advisory format
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت محلل استخبارات تهديدات تراقب عمليات الفدية والابتزاز. طور إطاراً شاملاً لمراقبة الفدية:

**القسم 1: تتبع مجموعات الفدية**

**استخبارات المجموعات:**
- تحديد مجموعات الفدية النشطة
- تتبع إعادة العلامة التجارية والانفصال
- تحديد القيادة والأعضاء الرئيسيين
- تحليل برنامج الشركاء التابعين
- الجدول الزمني للنشاط التاريخي

**تتبع البنية التحتية:**
- مراقبة عنوان URL لموقع التسريب
- تتبع خدمات Tor المخفية
- تحديد بوابة الدفع
- قنوات الاتصال (Tox, Jabber, Session)
- تغييرات البنية التحتية والهجرات

**القسم 2: مراقبة موقع التسريب**

**المراقبة الآلية:**
- كشف نشر الضحايا الجدد
- مراقبة توفر الموقع
- تتبع تغييرات المحتوى
- مراقبة مؤقت العد التنازلي
- تتبع الأرشفة والحذف

**تحديد الضحية:**
- استخراج اسم الشركة
- تحديد الموقع الجغرافي
- تصنيف القطاع الصناعي
- تقدير الإيرادات والحجم
- تاريخ الاختراق السابق

**تحليل نشر البيانات:**
- تحديد نوع البيانات
- تقدير الحجم
- تقييم الحساسية
- الآثار التنظيمية (GDPR, HIPAA)
- قيمة الاستخبارات التنافسية

**القسم 3: تحليل متغير الفدية**

**التحليل التقني:**
- تحديد عائلة البرمجيات الخبيثة
- تحليل خوارزمية التشفير
- أنماط امتداد الملف
- تنسيق ملاحظة الفدية
- سرعة ومنهجية التشفير

**التحليل التشغيلي:**
- تفضيلات متجه الهجوم
- تقنيات الحركة الجانبية
- آليات الاستمرار
- طرق تجهيز البيانات
- قنوات النشر

**القسم 4: استخبارات التفاوض**

**تحليل الاتصالات:**
- طرق الاتصال الأولي
- أنماط مطالب الفدية
- تكتيكات التفاوض
- توقعات الجدول الزمني للدفع
- طرق ضمان فك التشفير

**تتبع الدفع:**
- تحليل محافظ العملات المشفرة
- طرق التحقق من الدفع
- عملية تسليم أداة فك التشفير
- أنماط الابتزاز المزدوج
- التحقق من حذف البيانات

**القسم 5: دعم الضحية وإعداد التقارير**

**تقييم التهديد:**
- تقييم المخاطر الخاص بالمنظمة
- احتمالية كشف البيانات
- متطلبات الإشعار التنظيمي
- تقييم التأثير على السمعة
- الآثار على استمرارية الأعمال

**منتجات الاستخبارات:**
- تقارير إشعار الضحية
- تحذيرات تهديدات الصناعة
- تحليل الاتجاهات الفصلية
- تقرق مشهد الفدية السنوي
- إحاطات تنفيذية

**متطلبات المخرجات:**
- قاعدة بيانات تتبع المجموعات
- دليل تشغيل مراقبة موقع التسريب
- سير عمل تحديد الضحية
- قالب تحليل المتغيرات
- تنسيق التحذيرات التهديدية
```

---

## Example Output Preview

```
# Ransomware Threat Intelligence Report

## Active Ransomware Groups - Q1 2024

### Group Activity Summary
| Group | New Victims | Average Ransom | Payment Rate | Trend |
|-------|-------------|----------------|--------------|-------|
| LockBit 3.0 | 234 | $2.1M | 28% | ↑ |
| ALPHV/BlackCat | 189 | $1.8M | 32% | ↑ |
| Royal | 156 | $1.5M | 24% | → |
| Black Basta | 123 | $1.2M | 22% | ↓ |
| Clop | 89 | $3.2M | 35% | ↑ |

## Leak Site Monitoring - Recent Additions

### New Victim Notifications (Last 7 Days)

**Victim 1: Manufacturing Company**
- **Group:** LockBit 3.0
- **Posted:** 2024-01-15
- **Company:** [REDACTED] Manufacturing Inc.
- **Location:** United States, Ohio
- **Industry:** Automotive Parts Manufacturing
- **Revenue:** $150M estimated
- **Data Claimed:** 1.2TB (Financial records, CAD files, employee data)
- **Countdown:** 6 days remaining
- **Previous Breaches:** None identified

**Victim 2: Healthcare Provider**
- **Group:** ALPHV/BlackCat
- **Posted:** 2024-01-14
- **Company:** [REDACTED] Medical Group
- **Location:** United Kingdom
- **Industry:** Healthcare
- **Regulatory Impact:** GDPR, NHS requirements
- **Data Claimed:** 850GB (Patient records, medical imaging)
- **Countdown:** 3 days remaining
- **Criticality:** HIGH - Protected Health Information

## Ransomware Variant Analysis

### LockBit 3.0 (LockBit Black) Technical Profile
| Attribute | Details |
|-----------|---------|
| **Encryption** | AES-256 + RSA-2048 |
| **Extensions** | .lockbit, .lb3 |
| **Ransom Note** | RESTORE_FILES.txt |
| **Detection Rate** | 45/72 vendors |
| **First Seen** | July 2022 |
| **Affiliate Program** | Yes (80/20 split) |

### Attack Chain
```
Initial Access → Phishing/Purchased Access
Execution → PowerShell/Cobalt Strike
Persistence → Scheduled Tasks, Registry
Defense Evasion → Disable AV, Clear Logs
Lateral Movement → RDP, SMB, PsExec
Data Exfiltration → Rclone, Mega.nz
Encryption → LockBit encryptor
Extortion → Leak site + Payment portal
```

## Negotiation Intelligence

### Observed Ransom Demands (Last 30 Days)
| Group | Min Demand | Max Demand | Median |
|-------|------------|------------|--------|
| LockBit 3.0 | $500K | $15M | $2.1M |
| ALPHV | $400K | $12M | $1.8M |
| Royal | $250K | $8M | $1.5M |
| Clop | $1M | $25M | $3.2M |

### Negotiation Tactics
- Initial demand typically 3-5x settlement amount
- Countdown timer creates urgency
- "Discount" offered for early payment
- Data sample provided as proof
- Separate decryptor price vs. data deletion price

## Threat Advisory

### Sector Alert: Healthcare Organizations
**Threat Level:** HIGH

**Rationale:**
- 45% increase in healthcare targeting (Q4 2023)
- Regulatory pressure increases payment likelihood
- Patient data has high black market value
- Operational disruption can be life-threatening

**Recommended Actions:**
1. Review and test backup procedures
2. Implement network segmentation
3. Enable enhanced logging and monitoring
4. Conduct tabletop exercise for ransomware
5. Review cyber insurance coverage
6. Establish law enforcement contacts
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 5: Underground Marketplace Intelligence

### Description
Monitor and analyze underground marketplaces for illicit goods, services, and data sales including vendor tracking and pricing intelligence.

### Tags
`underground-marketplaces` `illicit-trade` `vendor-tracking` `pricing-intelligence` `dark-markets`

---

## 🇬🇧 English Prompt

```
You are a dark web intelligence analyst monitoring underground marketplaces. Develop a comprehensive marketplace monitoring framework:

**Section 1: Marketplace Landscape**

**Marketplace Classification:**
- General-purpose markets
- Specialized markets (drugs, credentials, malware)
- Carding shops
- Identity document markets
- Weapons and contraband markets

**Market Lifecycle Tracking:**
- New market emergence
- Market growth and decline
- Exit scam detection
- Law enforcement takedowns
- Market migrations and replacements

**Section 2: Vendor Intelligence**

**Vendor Profiling:**
- Vendor name and aliases
- Product categories offered
- Reputation and feedback analysis
- Transaction volume estimation
- Geographic indicators

**Trust & Reputation Systems:**
- Feedback score analysis
- Verified vendor programs
- Escrow usage patterns
- Dispute history review
- Longevity indicators

**Pricing Intelligence:**
- Product pricing trends
- Bulk discount structures
- Payment method preferences
- Cryptocurrency preferences
- Price comparison across markets

**Section 3: Product Monitoring**

**Data & Credentials:**
- Corporate credential sales
- Personal identity packages
- Financial account sales
- Government document sales
- Educational credential fraud

**Malware & Tools:**
- Exploit sales and rentals
- Malware-as-a-Service (MaaS)
- Ransomware affiliate programs
- Initial access sales
- Botnet rentals

**Physical Goods:**
- Counterfeit products
- Controlled substances
- Weapons trafficking
- Stolen merchandise
- Counterfeit documents

**Section 4: Transaction Analysis**

**Payment Methods:**
- Cryptocurrency tracking
- Monetization techniques
- Mixing service usage
- Exchange patterns
- Cash-out methods

**Escrow & Dispute:**
- Escrow service analysis
- Dispute resolution patterns
- Admin intervention cases
- Refund and compensation
- Fraud prevention measures

**Section 5: Threat Intelligence Integration**

**Attribution Support:**
- Vendor behavior correlation
- Infrastructure overlap analysis
- Cross-market vendor tracking
- Law enforcement cooperation
- Attribution confidence factors

**Risk Assessment:**
- Market stability assessment
- Exit scam probability
- Law enforcement risk
- Vendor reliability scoring
- Transaction risk factors

**Output Requirements:**
- Marketplace landscape report
- Vendor tracking database
- Pricing intelligence summary
- Product category analysis
- Risk assessment framework
```

---

## 🇸🇦 Arabic Prompt | بالعربية

```
أنت محلل استخبارات الويب المظلم تراقب الأسواق السرية. طور إطاراً شاملاً لمراقبة الأسواق:

**القسم 1: مشهد الأسواق**

**تصنيف الأسواق:**
- الأسواق متعددة الأغراض
- الأسواق المتخصصة (مخدرات، بيانات اعتماد، برمجيات خبيثة)
- متاجر البطاقات
- أسواق وثائق الهوية
- أسواق الأسلحة والممنوعات

**تتبع دورة حياة السوق:**
- ظهور سوق جديدة
- نمو السوق وانحساره
- كشف عمليات الاحتيال عند الانسحاب
- عمليات الإغلاق من قبل إنفاذ القانون
- هجرات السوق والبدائل

**القسم 2: استخبارات البائعين**

**التنميط البائع:**
- اسم البائع والأسماء المستعارة
- فئات المنتجات المعروضة
- تحليل السمعة والتغذية الراجعة
- تقدير حجم المعاملات
- المؤشرات الجغرافية

**أنظمة الثقة والسمعة:**
- تحليل نقاط التغذية الراجعة
- برامج البائعين المعتمدين
- أنماط استخدام الإيداع
- مراجعة تاريخ النزاعات
- مؤشرات طول العمر

**استخبارات التسعير:**
- اتجاهات أسعار المنتجات
- هياكل خصم الجملة
- تفضيلات طريقة الدفع
- تفضيلات العملات المشفرة
- مقارنة الأسعار عبر الأسواق

**القسم 3: مراقبة المنتجات**

**البيانات وبيانات الاعتماد:**
- مبيعات بيانات الاعتماد المؤسسية
- حزم الهوية الشخصية
- مبيعات الحسابات المالية
- مبيعات الوثائق الحكومية
- احتيال بيانات الاعتماد التعليمية

**البرمجيات الخبيثة والأدوات:**
- مبيعات وإيجارات الاستغلال
- البرمجيات الخبيثة كخدمة (MaaS)
- برامج الشركاء التابعين للفدية
- مبيعات الوصول الأولي
- إيجارات شبكات البوت

**السلع المادية:**
- المنتجات المقلدة
- المواد الخاضعة للرقابة
- الاتجار بالأسلحة
- البضائع المسروقة
- المستندات المزورة

**القسم 4: تحليل المعاملات**

**طرق الدفع:**
- تتبع العملات المشفرة
- تقنيات تحويل الأموال
- استخدام خدمات الخلط
- أنماط التبادل
- طرق صرف النقود

**الإيداع والنزاعات:**
- تحليل خدمة الإيداع
- أنماط حل النزاعات
- حالات تدخل المسؤول
- الاسترداد والتعويض
- تدابير منع الاحتيال

**القسم 5: تكامل استخبارات التهديدات**

**دعم الإسناد:**
- ارتباط سلوك البائع
- تحليل تداخل البنية التحتية
- تتبع البائع عبر الأسواق
- التعاون مع إنفاذ القانون
- عوامل ثقة الإسناد

**تقييم المخاطر:**
- تقييم استقرار السوق
- احتمالية الاحتيال عند الانسحاب
- مخاطر إنفاذ القانون
- تسجيل موثوقية البائع
- عوامل مخاطر المعاملات

**متطلبات المخرجات:**
- تقرق مشهد الأسواق
- قاعدة بيانات تتبع البائعين
- ملخص استخبارات التسعير
- تحليل فئات المنتجات
- إطار تقييم المخاطر
```

---

## Example Output Preview

```
# Underground Marketplace Intelligence Report

## Marketplace Landscape - January 2024

### Active Markets Summary
| Market | Category | Est. Users | Est. Listings | Status |
|--------|----------|------------|---------------|--------|
| Market A | General | 500K+ | 85,000 | Active |
| Market B | Credentials | 150K+ | 23,000 | Active |
| Market C | Drugs | 300K+ | 120,000 | Active |
| Market D | Cards | 80K+ | 15,000 | Active |
| Market E | General | 200K+ | 45,000 | Exit Scam Watch |

### Recent Market Events
- **Market X:** Exit scam detected (Jan 10) - Estimated $15M stolen
- **Market Y:** Law enforcement takedown (Dec 2023)
- **Market Z:** Rebranded from previous market

## Vendor Intelligence

### Top Credential Vendors
| Vendor | Rating | Transactions | Join Date | Products |
|--------|--------|--------------|-----------|----------|
| DataKing | 4.9/5 | 12,345 | 2021-03 | Corporate creds, RDP |
| AccessBroker | 4.8/5 | 8,901 | 2022-01 | Initial access |
| CredMaster | 4.7/5 | 6,789 | 2022-06 | Fullz, combos |
| CorpHunter | 4.9/5 | 5,432 | 2021-11 | Corp email access |
| DB_Leak_Seller | 4.6/5 | 4,567 | 2022-09 | Database dumps |

### Vendor Trust Indicators
| Indicator | Weight | Description |
|-----------|--------|-------------|
| Verified status | High | Admin-verified vendor |
| Transaction history | Medium | 1,000+ completed |
| Longevity | Medium | 1+ year active |
| Dispute rate | High | <2% dispute rate |
| Finalize early | Low | Offers FE to trusted |

## Pricing Intelligence

### Credential Pricing (USD)
| Product Type | Price Range | Median | Trend |
|--------------|-------------|--------|-------|
| Corporate email access | $50-500 | $150 | ↑ |
| RDP access | $10-100 | $35 | → |
| Full identity package | $15-50 | $25 | ↓ |
| Credit card (valid) | $15-100 | $35 | → |
| Bank account access | $100-1,000 | $350 | ↑ |
| VPN credentials | $5-25 | $12 | → |

### Bulk Pricing Examples
| Product | 1x | 10x | 100x |
|---------|-----|-----|------|
| Fullz (US) | $25 | $200 | $1,500 |
| Credit card | $35 | $280 | $2,000 |
| RDP access | $35 | $280 | $2,200 |

### Malware-as-a-Service Pricing
| Service | Setup Fee | Monthly | Features |
|---------|-----------|---------|----------|
| Ransomware Kit | $1,000 | $500 | Support, updates |
| Stealer | $500 | $200 | Panel included |
| Botnet rental | N/A | $200/1K bots | C2 included |
| Exploit kit | $5,000 | $1,000 | Zero-day included |

## Transaction Analysis

### Payment Method Distribution
| Currency | Percentage | Trend |
|----------|------------|-------|
| Bitcoin (BTC) | 45% | ↓ |
| Monero (XMR) | 40% | ↑ |
| Litecoin (LTC) | 10% | → |
| Other | 5% | → |

### Escrow Usage
| Escrow Type | Usage Rate | Avg. Transaction |
|-------------|------------|------------------|
| Full escrow | 65% | $500+ |
| Partial escrow | 20% | $100-500 |
| Finalize early | 15% | <$100 |

## Risk Assessment

### Market Stability Scores
| Market | Stability | Exit Scam Risk | LE Risk |
|--------|-----------|----------------|---------|
| Market A | High | Low | Medium |
| Market B | Medium | Medium | High |
| Market C | High | Low | Medium |
| Market D | Medium | Medium | High |
| Market E | Low | High | Medium |

### Recommendations
1. Monitor Market E closely - exit scam indicators present
2. Track DataKing vendor - high volume corporate access
3. Alert on corporate credential sales targeting client domains
4. Review pricing trends for budget forecasting
5. Maintain relationships with law enforcement for takedown intel
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team
