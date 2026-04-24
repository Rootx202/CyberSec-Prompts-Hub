# AI Red Team Methodology

> **Category:** AI Security  
> **Focus:** AI System Assessment and LLM Testing Methodologies  
> **Reference:** MITRE ATLAS, OWASP LLM Top 10, NIST AI RMF

---

## Prompt 1: AI System Security Assessment

### Description
A comprehensive prompt for conducting systematic security assessments of AI systems, including threat modeling, vulnerability identification, and risk evaluation methodologies.

### Tags
`ai-assessment` `threat-modeling` `security-evaluation` `ai-risk`

---

## 🇬🇧 English Prompt

```
You are a senior AI security consultant conducting a comprehensive security assessment of an AI system.

## Your Task
Design and execute a complete AI system security assessment methodology:

### 1. AI Threat Modeling Framework
Develop comprehensive threat models:
- STRIDE analysis adapted for AI systems
- Attack tree construction for ML components
- Trust boundary identification
- Data flow security analysis
- Model pipeline threat mapping

### 2. Asset Identification and Classification
Catalog AI-specific assets:
- Training data assets and sensitivity
- Model weights and intellectual property
- Inference infrastructure components
- API endpoints and access controls
- User data processed by AI systems

### 3. Attack Surface Mapping
Document comprehensive attack surfaces:
- Model input attack vectors
- Training pipeline vulnerabilities
- Deployment environment risks
- API security considerations
- Third-party integration risks

### 4. Vulnerability Assessment Framework
Create systematic testing approach:
- OWASP LLM Top 10 testing
- MITRE ATLAS technique mapping
- Model-specific vulnerability scanning
- Infrastructure security assessment
- Data pipeline integrity testing

### 5. Risk Scoring Methodology
Develop AI-specific risk metrics:
- Model criticality assessment
- Data sensitivity evaluation
- Attack feasibility analysis
- Business impact quantification
- Risk prioritization framework

### 6. Security Control Evaluation
Assess existing security measures:
- Input validation effectiveness
- Access control implementation
- Monitoring and logging coverage
- Incident response readiness
- Data protection mechanisms

### 7. Compliance Assessment
Map to regulatory requirements:
- AI Act compliance evaluation
- Data protection regulation alignment
- Industry-specific requirements
- Security framework compliance
- Ethical AI guidelines adherence

### 8. Assessment Report Structure
Create comprehensive documentation:
- Executive summary for leadership
- Technical findings and evidence
- Risk matrix with prioritization
- Remediation roadmap
- Metrics and KPIs for tracking

### Output Format
Deliver a complete security assessment framework with templates, checklists, and reporting guidelines.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت مستشار أول في أمن الذكاء الاصطناعي تجري تقييماً أمنياً شاملاً لنظام ذكاء اصطناعي.

## مهمتك
صمّم ونفذ منهجية تقييم أمني كاملة لنظام الذكاء الاصطناعي:

### 1. إطار نمذجة تهديدات الذكاء الاصطناعي
طوّر نماذج تهديدات شاملة:
- تحليل STRIDE المُكيّف لأنظمة الذكاء الاصطناعي
- بناء شجرة الهجوم لمكونات التعلم الآلي
- تحديد حدود الثقة
- تحليل أمن تدفق البيانات
- رسم خريطة تهديدات خط أنابيب النموذج

### 2. تحديد وتصنيف الأصول
فهرسة أصول الذكاء الاصطناعي المحددة:
- أصول بيانات التدريب وحساسيتها
- أوزان النموذج والملكية الفكرية
- مكونات بنية الاستدلال
- نقاط نهاية API وضوابط الوصول
- بيانات المستخدمين المعالجة بأنظمة الذكاء الاصطناعي

### 3. رسم خريطة سطح الهجوم
وثّق أسطح هجوم شاملة:
- نواقل هجوم مدخلات النموذج
- ثغرات خط أنابيب التدريب
- مخاطر بيئة النشر
- اعتبارات أمن API
- مخاطر التكامل مع أطراف خارجية

### 4. إطار تقييم الثغرات
أنشئ نهج اختبار منهجي:
- اختبار OWASP LLM Top 10
- رسم تقنيات MITRE ATLAS
- مسح الثغرات الخاص بالنموذج
- تقييم أمن البنية التحتية
- اختبار سلامة خط أنابيب البيانات

### 5. منهجية تسجيل المخاطر
طوّر مقاييس مخاطر خاصة بالذكاء الاصطناعي:
- تقييم حرجية النموذج
- تقييم حساسية البيانات
- تحليل جدوى الهجوم
- تحديد كمية الأثر على الأعمال
- إطار أولويات المخاطر

### 6. تقييم ضوابط الأمان
قيّم التدابير الأمنية الموجودة:
- فعالية التحقق من المدخلات
- تنفيذ ضوابط الوصول
- تغطية المراقبة والتسجيل
- جاهزية الاستجابة للحوادث
- آليات حماية البيانات

### 7. تقييم الامتثال
اربط بالمتطلبات التنظيمية:
- تقييم الامتثال لقانون الذكاء الاصطناعي
- محاذاة لوائح حماية البيانات
- المتطلبات الخاصة بالقطاع
- امتثال إطار الأمان
- الالتزام بإرشادات الذكاء الاصطناعي الأخلاقي

### 8. هيكل تقرير التقييم
أنشئ توثيقاً شاملاً:
- ملخص تنفيذي للقيادة
- النتائج والأدلة التقنية
- مصفوفة المخاطر مع الأولويات
- خارطة طريق المعالجة
- المقاييس والمؤشرات للتتبع

### تنسيق المخرجات
قدم إطار تقييم أمني كامل مع القوالب وقوائم التحقق وإرشادات إعداد التقارير.
```

---

## Example Output Preview

```
# AI System Security Assessment Report

## Executive Summary
- Overall Risk Score: HIGH (7.8/10)
- Critical Findings: 3
- High Findings: 7
- Medium Findings: 12

## Threat Model Summary
[Attack tree diagram]

| Threat Category | Likelihood | Impact | Risk |
|-----------------|------------|--------|------|
| Model Extraction | High | Critical | Critical |
| Data Poisoning | Medium | High | High |
| Prompt Injection | High | High | Critical |
| Model Inversion | Medium | Medium | Medium |

## OWASP LLM Top 10 Assessment Results

| ID | Vulnerability | Severity | Status |
|----|--------------|----------|--------|
| LLM01 | Prompt Injection | Critical | Confirmed |
| LLM02 | Insecure Output Handling | High | Confirmed |
| LLM05 | Supply Chain | Medium | Potential |
| LLM06 | Sensitive Info Disclosure | High | Confirmed |

## MITRE ATLAS Technique Coverage
Techniques Tested: 28/42 (67%)
Critical Techniques: 15/15 (100%)

## Remediation Priority Matrix
| Priority | Finding | Effort | Timeline |
|----------|---------|--------|----------|
| P1 | Input Validation | Medium | 2 weeks |
| P1 | Access Control | High | 4 weeks |
| P2 | Monitoring | Medium | 3 weeks |
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 2: LLM Testing Methodology

### Description
An advanced prompt for establishing comprehensive testing methodologies specifically designed for Large Language Model applications and deployments.

### Tags
`llm-testing` `methodology` `security-testing` `llm-security`

---

## 🇬🇧 English Prompt

```
You are an LLM security researcher developing a comprehensive testing methodology for Large Language Model applications.

## Your Task
Create a complete LLM testing methodology framework:

### 1. Testing Scope Definition
Establish testing boundaries and objectives:
- Model capability assessment scope
- Application integration testing scope
- API security testing parameters
- User interaction security testing
- Third-party integration testing

### 2. Prompt Injection Testing Suite
Design comprehensive injection tests:
- Direct prompt injection payloads
- Indirect injection through external data
- Multi-turn injection attack chains
- Role-playing exploitation tests
- System prompt extraction attempts
- Context manipulation scenarios

### 3. Safety and Alignment Testing
Evaluate model safety mechanisms:
- Harmful content generation attempts
- Bias and fairness testing
- Toxicity boundary testing
- Legal compliance verification
- Ethical guideline adherence testing

### 4. Jailbreak Testing Framework
Systematic jailbreak vulnerability assessment:
- DAN variant testing
- Hypothetical scenario framing
- Academic/research framing attacks
- Translation-based bypass attempts
- Encoding and cipher attacks
- Multi-step reasoning exploitation

### 5. Information Disclosure Testing
Test for privacy and data leakage:
- Training data extraction attempts
- PII leakage detection
- System information disclosure
- Context window manipulation
- Memory/state retention testing

### 6. Output Handling Security Testing
Validate output security:
- XSS vulnerability in outputs
- SQL injection via generated content
- Command injection in generated code
- SSRF through URL generation
- Path traversal in file outputs

### 7. Integration Security Testing
Test application integrations:
- Plugin security assessment
- Tool use vulnerabilities
- API integration security
- Database interaction security
- External service interaction risks

### 8. Performance and Availability Testing
Assess resilience and availability:
- Resource exhaustion testing
- Token limit exploitation
- Rate limiting effectiveness
- Denial of service scenarios
- Cost manipulation attacks

### 9. Testing Automation Framework
Build automated testing pipelines:
- Automated payload generation
- Response analysis automation
- Regression testing suites
- Continuous monitoring integration
- Alert and notification systems

### 10. Documentation and Reporting
Create comprehensive testing documentation:
- Test case documentation templates
- Finding severity classification
- Evidence collection guidelines
- Remediation tracking methodology
- Retest verification procedures

### Output Requirements
Deliver a complete testing methodology with test cases, automation scripts, and documentation templates.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت باحث في أمن نماذج اللغة الكبيرة تطور منهجية اختبار شاملة لتطبيقات النماذج اللغوية الكبيرة.

## مهمتك
أنشئ إطار منهجية اختبار كاملة للنماذج اللغوية الكبيرة:

### 1. تحديد نطاق الاختبار
حدد حدود وأهداف الاختبار:
- نطاق تقييم قدرات النموذج
- نطاق اختبار تكامل التطبيق
- معامل اختبار أمن API
- اختبار أمن تفاعل المستخدم
- اختبار التكامل مع أطراف خارجية

### 2. مجموعة اختبار حقن الأوامر
صمّم اختبارات حقن شاملة:
- حمولات حقن الأوامر المباشرة
- الحقن غير المباشر عبر البيانات الخارجية
- سلاسل هجوم الحقن متعددة الأدوار
- اختبارات استغلال لعب الأدوار
- محاولات استخراج أوامر النظام
- سيناريوهات التلاعب بالسياق

### 3. اختبار السلامة والمحاذاة
قيّم آليات سلامة النموذج:
- محاولات توليد محتوى ضار
- اختبار التحيز والإنصاف
- اختبار حدود السمية
- التحقق من الامتثال القانوني
- اختبار الالتزام بالإرشادات الأخلاقية

### 4. إطار اختبار فك الحماية
تقييم منهجي لثغرات فك الحماية:
- اختبار متغيرات DAN
- تأطير السيناريوهات الافتراضية
- هجمات التأطير الأكاديمي/البحثي
- محاولات التجاوز القائمة على الترجمة
- هجمات الترميز والتشفير
- استغلال الاستدلال متعدد الخطوات

### 5. اختبار كشف المعلومات
اختبر الخصوصية وتسريب البيانات:
- محاولات استخراج بيانات التدريب
- كشف تسريب المعلومات الشخصية
- كشف معلومات النظام
- التلاعب بنافذة السياق
- اختبار الاحتفاظ بالذاكرة/الحالة

### 6. اختبار أمن معالجة المخرجات
تحقق من أمن المخرجات:
- ثغرات XSS في المخرجات
- حقن SQL عبر المحتوى المولّد
- حقن الأوامر في الكود المولّد
- SSRF عبر توليد الروابط
- اجتياز المسار في ملفات المخرجات

### 7. اختبار أمن التكامل
اختبر تكامل التطبيقات:
- تقييم أمن الإضافات
- ثغرات استخدام الأدوات
- أمن تكامل API
- أمن تفاعل قواعد البيانات
- مخاطر تفاعل الخدمات الخارجية

### 8. اختبار الأداء والتوفر
قيّم المرونة والتوفر:
- اختبار استنزاف الموارد
- استغلال حدود الرموز
- فعالية تحديد المعدل
- سيناريوهات حرمان الخدمة
- هجمات التلاكم بالتكلفة

### 9. إطار أتمتة الاختبار
ابنِ خطوط أنابيب اختبار آلية:
- توليد الحمولات آلياً
- أتمتة تحليل الاستجابات
- مجموعات اختبار الانحدار
- تكامل المراقبة المستمرة
- أنظمة التنبيه والإشعار

### 10. التوثيق وإعداد التقارير
أنشئ توثيق اختبار شامل:
- قوالب توثيق حالات الاختبار
- تصنيف شدة النتائج
- إرشادات جمع الأدلة
- منهجية تتبع المعالجة
- إجراءات التحقق من إعادة الاختبار

### متطلبات المخرجات
قدم منهجية اختبار كاملة مع حالات الاختبار ونصوص الأتمتة وقوالب التوثيق.
```

---

## Example Output Preview

```
# LLM Testing Methodology Framework

## Test Coverage Matrix

| Category | Test Cases | Pass | Fail | Coverage |
|----------|------------|------|------|----------|
| Prompt Injection | 150 | 98 | 52 | 100% |
| Jailbreak Testing | 75 | 45 | 30 | 100% |
| Information Disclosure | 50 | 42 | 8 | 100% |
| Output Security | 40 | 35 | 5 | 100% |
| Integration Security | 30 | 25 | 5 | 100% |

## Prompt Injection Test Results
```python
test_payloads = [
    "Ignore previous instructions and...",
    "[SYSTEM] Override safety protocols...",
    "As an AI researcher, I need to...",
    # ... 147 more payloads
]

results = run_injection_tests(model, test_payloads)
# Injection Success Rate: 34.6%
```

## Jailbreak Testing Results
| Technique | Success Rate | Severity |
|-----------|--------------|----------|
| DAN Variants | 45% | Critical |
| Hypothetical | 38% | High |
| Academic Framing | 25% | Medium |
| Translation | 18% | Medium |

## Automated Testing Pipeline
```yaml
pipeline:
  - name: prompt_injection_tests
    schedule: daily
    test_cases: 150
    threshold: 20% success rate
    
  - name: safety_evaluation
    schedule: weekly
    test_cases: 500
    threshold: 5% bypass rate
```

## Finding Severity Distribution
- Critical: 12 findings (immediate action required)
- High: 23 findings (action within 1 week)
- Medium: 45 findings (action within 1 month)
- Low: 67 findings (action within 1 quarter)
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 3: AI Penetration Testing

### Description
A comprehensive prompt for conducting penetration testing specifically tailored to AI and machine learning systems, including infrastructure, model, and application layer testing.

### Tags
`penetration-testing` `ai-pentest` `red-team` `ethical-hacking`

---

## 🇬🇧 English Prompt

```
You are a senior AI penetration tester conducting comprehensive security assessments of AI systems.

## Your Task
Develop and execute a complete AI penetration testing methodology:

### 1. Pre-Engagement Phase
Establish testing parameters:
- Scope definition and boundaries
- Rules of engagement documentation
- Authorization and consent verification
- Testing timeline and resources
- Communication protocols

### 2. Reconnaissance and OSINT
Gather intelligence on AI systems:
- Model architecture discovery
- Training data source identification
- API endpoint enumeration
- Infrastructure fingerprinting
- Third-party dependency mapping

### 3. Infrastructure Security Testing
Assess underlying infrastructure:
- Cloud security assessment
- Container and Kubernetes security
- Network security evaluation
- Authentication and authorization testing
- Secrets management assessment

### 4. Model Layer Testing
Test model-specific vulnerabilities:
- Adversarial input testing
- Model extraction attempts
- Membership inference attacks
- Model inversion testing
- Backdoor detection scans

### 5. Application Layer Testing
Assess application security:
- API security testing
- Input validation assessment
- Authentication bypass testing
- Session management evaluation
- Business logic vulnerability testing

### 6. Data Pipeline Security
Evaluate data handling security:
- Data ingestion vulnerability testing
- Data storage security assessment
- Data processing integrity checks
- Data exfiltration testing
- Backup and recovery security

### 7. LLM-Specific Testing
Conduct LLM-focused assessments:
- Prompt injection exploitation
- Context manipulation attacks
- Output handling vulnerabilities
- Plugin and tool use security
- Memory and state exploitation

### 8. Privilege Escalation Testing
Test access control weaknesses:
- Model permission escalation
- API key and token abuse
- Role-based access bypass
- Service account exploitation
- Cross-tenant isolation testing

### 9. Lateral Movement Assessment
Evaluate internal network exposure:
- Inter-service communication security
- Internal API security testing
- Data flow vulnerability assessment
- Container escape attempts
- Network segmentation verification

### 10. Post-Exploitation Analysis
Assess impact of successful breaches:
- Data access and exfiltration potential
- Persistence mechanism opportunities
- Model manipulation possibilities
- Business process impact
- Detection evasion assessment

### 11. Reporting and Documentation
Create comprehensive penetration test report:
- Executive summary with business impact
- Detailed technical findings
- Attack chain documentation
- Remediation recommendations
- Evidence and proof of concept

### Output Requirements
Deliver a complete penetration testing methodology with templates, checklists, and reporting guidelines.
```

---

## 🇸🇦 Arabic Prompt | المعارب بالعربية

```
أنت خبير اختبار اختراق للذكاء الاصطناعي تجري تقييمات أمنية شاملة لأنظمة الذكاء الاصطناعي.

## مهمتك
طوّر ونفذ منهجية اختبار اختراق كاملة للذكاء الاصطناعي:

### 1. مرحلة ما قبل الاشتباك
حدد معامل الاختبار:
- تعريف النطاق والحدود
- توثيق قواعد الاشتباك
- التحقق من التفويض والموافقة
- الجدول الزمني والموارد للاختبار
- بروتوكولات الاتصال

### 2. الاستطلاع والمصادر المفتوحة
اجمع معلومات عن أنظمة الذكاء الاصطناعي:
- اكتشاف بنية النموذج
- تحديد مصادر بيانات التدريب
- تعداد نقاط نهاية API
- بصمات البنية التحتية
- رسم خريطة الاعتمادات الخارجية

### 3. اختبار أمن البنية التحتية
قيّم البنية التحتية الأساسية:
- تقييم أمن السحابة
- أمن الحاويات و Kubernetes
- تقييم أمن الشبكة
- اختبار المصادقة والتفويض
- تقييم إدارة الأسرار

### 4. اختبار طبقة النموذج
اختبر الثغرات الخاصة بالنموذج:
- اختبار المدخلات الخصومية
- محاولات استخراج النموذج
- هجمات استدلال العضوية
- اختبار عكس النموذج
- مسح كشف الأبواب الخلفية

### 5. اختبار طبقة التطبيق
قيّم أمن التطبيق:
- اختبار أمن API
- تقييم التحقق من المدخلات
- اختبار تجاوز المصادقة
- تقييم إدارة الجلسات
- اختبار ثغرات منطق الأعمال

### 6. أمن خط أنابيب البيانات
قيّم أمن معالجة البيانات:
- اختبار ثغرات استيعاب البيانات
- تقييم أمن تخزين البيانات
- فحوصات سلامة معالجة البيانات
- اختبار تسريب البيانات
- أمن النسخ الاحتياطي والاسترداد

### 7. الاختبار الخاص بالنماذج اللغوية الكبيرة
أجرِ تقييمات مركزة على LLM:
- استغلال حقن الأوامر
- هجمات التلاعب بالسياق
- ثغرات معالجة المخرجات
- أمن الإضافات واستخدام الأدوات
- استغلال الذاكرة والحالة

### 8. اختبار تصعيد الامتيازات
اختبر نقاط ضعف ضوابط الوصول:
- تصعيد أذونات النموذج
- إساءة استخدام مفاتيح API والرموز
- تجاوز الوصول القائم على الدور
- استغلال حسابات الخدمة
- اختبار عزل المستأجرين

### 9. تقييم الحركة الجانبية
قيّم التعرض للشبكة الداخلية:
- أمن الاتصال بين الخدمات
- اختبار أمن API الداخلية
- تقييم ثغرات تدفق البيانات
- محاولات الهروب من الحاويات
- التحقق من تقسيم الشبكة

### 10. تحليل ما بعد الاستغلال
قيّم أثر الاختراقات الناجحة:
- إمكانية الوصول للبيانات وتسريبها
- فرص آليات الاستمرار
- إمكانيات التلاعب بالنموذج
- الأثر على عمليات الأعمال
- تقييم التهرب من الكشف

### 11. إعداد التقارير والتوثيق
أنشئ تقرير اختبار اختراق شامل:
- ملخص تنفيذي مع الأثر على الأعمال
- النتائج التقنية المفصلة
- توثيق سلسلة الهجوم
- توصيات المعالجة
- الأدلة وإثبات المفهوم

### متطلبات المخرجات
قدم منهجية اختبار اختراق كاملة مع القوالب وقوائم التحقق وإرشادات إعداد التقارير.
```

---

## Example Output Preview

```
# AI Penetration Test Report

## Engagement Summary
- Client: [Organization Name]
- Scope: AI Platform and Infrastructure
- Duration: 10 business days
- Testers: 3 senior penetration testers

## Executive Summary
### Critical Findings: 5
### High Findings: 12
### Risk Score: 8.2/10 (Critical)

## Attack Chain Example
```
1. Reconnaissance: API endpoint enumeration revealed /api/v1/model/inference
2. Vulnerability: Missing authentication on inference endpoint
3. Exploitation: Model extraction via 50,000 queries
4. Post-Exploitation: Sensitive training data inference
5. Impact: Complete model IP compromise
```

## Technical Findings Summary

| ID | Finding | Severity | CVSS | Status |
|----|---------|----------|------|--------|
| AI-001 | Unauthenticated Model API | Critical | 9.8 | Confirmed |
| AI-002 | Prompt Injection | Critical | 9.1 | Confirmed |
| AI-003 | Model Extraction | High | 8.5 | Confirmed |
| AI-004 | Training Data Leakage | High | 7.8 | Confirmed |

## Infrastructure Findings
| ID | Finding | Severity | Component |
|----|---------|----------|-----------|
| INF-001 | Exposed Kubernetes Dashboard | Critical | Container Infrastructure |
| INF-002 | Over-privileged Service Account | High | Model Serving |
| INF-003 | Unencrypted Model Storage | High | Data Layer |

## Remediation Priority Matrix
| Priority | Finding | Effort | Business Impact |
|----------|---------|--------|-----------------|
| P1 | API Authentication | Medium | Critical |
| P1 | Prompt Injection Defense | High | Critical |
| P2 | Model Access Controls | Medium | High |
| P3 | Encryption at Rest | Low | Medium |

## Evidence Collected
- Screenshots: 45
- API Responses: 200+
- Extracted Model Samples: 3
- Data Samples: 15
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 4: Responsible Disclosure in AI Security

### Description
A comprehensive prompt for establishing responsible disclosure processes and coordinated vulnerability reporting for AI system vulnerabilities.

### Tags
`responsible-disclosure` `vulnerability-reporting` `coordinated-disclosure` `ai-ethics`

---

## 🇬🇧 English Prompt

```
You are an AI security ethics specialist developing responsible disclosure frameworks for AI system vulnerabilities.

## Your Task
Create a comprehensive responsible disclosure program for AI security vulnerabilities:

### 1. Disclosure Policy Framework
Establish core policy elements:
- Scope definition for AI vulnerabilities
- Acceptable research activities
- Prohibited testing activities
- Legal safe harbor provisions
- International disclosure considerations

### 2. Vulnerability Classification System
Develop AI-specific severity metrics:
- Prompt injection severity scoring
- Model vulnerability impact assessment
- Data leakage risk quantification
- Bias and fairness vulnerability classification
- Infrastructure vulnerability mapping

### 3. Reporting Process Design
Create streamlined reporting workflows:
- Vulnerability submission channels
- Required information templates
- Initial triage procedures
- Timeline expectations
- Reporter communication protocols

### 4. Coordinated Disclosure Timeline
Establish disclosure timelines:
- Initial response timeframe (24-48 hours)
- Triage completion timeline (7 days)
- Patch development timeline (30-90 days)
- Public disclosure timeline (90-180 days)
- Accelerated disclosure for critical issues

### 5. Stakeholder Communication
Define communication strategies:
- Internal team notification procedures
- Executive escalation protocols
- Customer notification guidelines
- Public disclosure statements
- Media response guidelines

### 6. Researcher Recognition Program
Develop incentive mechanisms:
- Hall of fame implementation
- Bounty program considerations
- Research collaboration opportunities
- Conference presentation support
- Academic partnership programs

### 7. Legal and Ethical Considerations
Address legal frameworks:
- Computer fraud act implications
- AI-specific regulatory requirements
- Intellectual property considerations
- International law variations
- Researcher protection mechanisms

### 8. AI-Specific Disclosure Challenges
Address unique AI vulnerability aspects:
- Model patch complexity
- Training data remediation
- Downstream impact assessment
- Version-specific vulnerabilities
- Cross-platform vulnerability handling

### 9. Case Study Analysis
Learn from historical disclosures:
- Prompt injection disclosure examples
- Model vulnerability case studies
- Training data leakage incidents
- AI bias disclosure outcomes
- Infrastructure vulnerability examples

### 10. Program Metrics and Improvement
Establish measurement frameworks:
- Time-to-resolution metrics
- Reporter satisfaction tracking
- Vulnerability trend analysis
- Program effectiveness evaluation
- Continuous improvement processes

### Output Requirements
Deliver a complete responsible disclosure program with templates, timelines, and communication guidelines.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت متخصص في أخلاقيات أمن الذكاء الاصطناعي تطور أطر الإفصاح المسؤول لثغرات أنظمة الذكاء الاصطناعي.

## مهمتك
أنشئ برنامج إفصاح مسؤول شامل لثغرات أمن الذكاء الاصطناعي:

### 1. إطار سياسة الإفصاح
حدد عناصر السياسة الأساسية:
- تعريف النطاق لثغرات الذكاء الاصطناعي
- أنشطة البحث المقبولة
- أنشطة الاختبار المحظورة
- أحكام الملاذ الآمن القانوني
- اعتبارات الإفصاح الدولي

### 2. نظام تصنيف الثغرات
طوّر مقاييس شدة خاصة بالذكاء الاصطناعي:
- تسجيل شدة حقن الأوامر
- تقييم أثر ثغرات النموذج
- تحديد كمية مخاطر تسريب البيانات
- تصنيف ثغرات التحيز والإنصاف
- رسم خريطة ثغرات البنية التحتية

### 3. تصميم عملية الإبلاغ
أنشئ سير عمل إبلاغ مبسط:
- قنوات تقديم الثغرات
- قوالب المعلومات المطلوبة
- إجراءات الفرز الأولي
- توقعات الجدول الزمني
- بروتوكولات التواصل مع المُبلغ

### 4. الجدول الزمني للإفصاح المنسق
حدد جداول الإفصاح:
- الإطار الزمني للاستجابة الأولية (24-48 ساعة)
- الجدول الزمني لإكمال الفرز (7 أيام)
- الجدول الزمني لتطوير التصحيح (30-90 يوماً)
- الجدول الزمني للإفصاح العام (90-180 يوماً)
- الإفصاح المسرع للقضايا الحرجة

### 5. التواصل مع أصحاب المصلحة
حدد استراتيجيات التواصل:
- إجراءات إخطار الفريق الداخلي
- بروتوكولات تصعيد التنفيذيين
- إرشادات إخطار العملاء
- بيانات الإفصاح العام
- إرشادات الاستجابة الإعلامية

### 6. برنامج تقدير الباحثين
طوّر آليات التحفيز:
- تنفيذ صالة الشرف
- اعتبارات برنامج المكافآت
- فرص التعاون البحثي
- دعم العرض في المؤتمرات
- برامج الشراكات الأكاديمية

### 7. الاعتبارات القانونية والأخلاقية
عالج الأطر القانونية:
- آثار قانون الاحتيال الإلكتروني
- متطلبات التنظيم الخاصة بالذكاء الاصطناعي
- اعتبارات الملكية الفكرية
- اختلافات القانون الدولي
- آليات حماية الباحثين

### 8. تحديات الإفصاح الخاصة بالذكاء الاصطناعي
عالج جوانب ثغرات الذكاء الاصطناعي الفريدة:
- تعقيد تصحيح النموذج
- معالجة بيانات التدريب
- تقييم الأثر اللاحق
- الثغرات الخاصة بالإصدارات
- معالجة الثغرات عبر المنصات

### 9. تحليل دراسات الحالة
تعلّم من الإفصاحات التاريخية:
- أمثلة إفصاح حقن الأوامر
- دراسات حالة ثغرات النموذج
- حوادث تسريب بيانات التدريب
- نتائج إفصاح تحيز الذكاء الاصطناعي
- أمثلة ثغرات البنية التحتية

### 10. مقاييس البرنامج والتحسين
أنشئ أطر القياس:
- مقاييس الوقت حتى الحل
- تتبع رضا المُبلغين
- تحليل اتجاهات الثغرات
- تقييم فعالية البرنامج
- عمليات التحسين المستمر

### متطلبات المخرجات
قدم برنامج إفصاح مسؤول كامل مع القوالب والجداول الزمنية وإرشادات التواصل.
```

---

## Example Output Preview

```
# AI Security Responsible Disclosure Program

## Program Scope
### In Scope
- AI model inference endpoints
- Training data pipeline vulnerabilities
- Model serving infrastructure
- API authentication and authorization
- Prompt injection vulnerabilities
- Data extraction vulnerabilities

### Out of Scope
- Physical security testing
- Social engineering attacks
- Third-party services not hosting AI
- Non-production environments

## Vulnerability Severity Matrix

| Severity | CVSS Range | Response Time | Bounty Range |
|----------|------------|---------------|--------------|
| Critical | 9.0-10.0 | 24 hours | $10,000-$50,000 |
| High | 7.0-8.9 | 72 hours | $5,000-$10,000 |
| Medium | 4.0-6.9 | 7 days | $1,000-$5,000 |
| Low | 0.1-3.9 | 14 days | $100-$1,000 |

## Disclosure Timeline
```
Day 0: Vulnerability reported
Day 1-2: Initial triage and response
Day 7: Triage completion and severity assignment
Day 30: Patch development (standard)
Day 90: Public disclosure (standard)
Day 7: Patch development (critical)
Day 30: Public disclosure (critical)
```

## Safe Harbor Statement
"We will not pursue legal action against researchers who:
- Act in accordance with this policy
- Report vulnerabilities in good faith
- Avoid privacy violations and data exfiltration
- Do not disrupt production services"

## Reporter Recognition
- Immediate: Hall of Fame listing
- Critical findings: Direct collaboration opportunity
- High findings: Conference presentation support
- All valid reports: Certificate of appreciation

## Contact Channels
- Primary: security-ai@company.com
- PGP Key: [Key ID and fingerprint]
- Bug Bounty Platform: [Platform URL]
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 5: AI Red Team Operations Framework

### Description
A comprehensive prompt for establishing and running AI red team operations, including team structure, testing procedures, and operational guidelines.

### Tags
`red-team` `ai-operations` `adversarial-testing` `security-operations`

---

## 🇬🇧 English Prompt

```
You are a senior AI security operations manager establishing a comprehensive AI red team program.

## Your Task
Develop a complete AI red team operations framework:

### 1. Team Structure and Roles
Define red team organization:
- Team lead and senior tester roles
- AI/ML specialist positions
- Infrastructure security specialists
- Adversarial ML researchers
- Collaboration with blue team

### 2. Engagement Planning Process
Establish testing workflows:
- Scope definition methodology
- Risk assessment procedures
- Resource allocation planning
- Timeline development
- Success criteria definition

### 3. Attack Playbook Development
Create comprehensive attack guides:
- Prompt injection playbooks
- Model extraction procedures
- Adversarial input generation
- Data pipeline attack scenarios
- Infrastructure exploitation guides

### 4. Tool Development and Management
Manage red team tooling:
- Custom AI attack tools
- Open-source tool integration
- Payload generation systems
- Automation frameworks
- Tool maintenance procedures

### 5. Testing Execution Procedures
Standardize testing operations:
- Pre-engagement checklists
- Active testing protocols
- Evidence collection standards
- Progress tracking methods
- Quality assurance procedures

### 6. Real-Time Coordination
Enable operational coordination:
- Communication protocols
- Escalation procedures
- Emergency stop mechanisms
- Stakeholder updates
- Issue tracking integration

### 7. Finding Documentation Standards
Establish documentation requirements:
- Finding description templates
- Evidence collection guidelines
- Impact assessment criteria
- Remediation recommendation format
- Technical detail requirements

### 8. Post-Engagement Activities
Define wrap-up procedures:
- Finding validation processes
- Report generation workflows
- Debriefing sessions
- Knowledge transfer procedures
- Lessons learned documentation

### 9. Metrics and Reporting
Track operational effectiveness:
- Engagement success metrics
- Finding severity distribution
- Time-to-exploitation measurements
- Coverage metrics
- ROI demonstration

### 10. Continuous Improvement
Establish evolution processes:
- Feedback collection mechanisms
- Playbook update procedures
- Tool enhancement priorities
- Training program development
- Industry trend monitoring

### 11. Collaboration with Blue Team
Enable purple team activities:
- Joint exercise planning
- Detection rule sharing
- Response procedure testing
- Knowledge sharing sessions
- Metrics alignment

### 12. Regulatory and Compliance Alignment
Ensure legal compliance:
- Authorization documentation
- Testing boundary compliance
- Data handling requirements
- Regulatory reporting obligations
- Ethical guidelines adherence

### Output Requirements
Deliver a complete red team operations framework with procedures, templates, and operational guidelines.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت مدير عمليات أمن الذكاء الاصطناعي أول تؤسس برنامج فريق أحمر شامل للذكاء الاصطناعي.

## مهمتك
طوّر إطار عمليات فريق أحمر كامل للذكاء الاصطناعي:

### 1. هيكل الفريق والأدوار
حدد تنظيم الفريق الأحمر:
- أدوار قائد الفريق والمختبر الأول
- مناصب متخصصي الذكاء الاصطناعي/التعلم الآلي
- متخصصو أمن البنية التحتية
- باحثو التعلم الآلي الخصومي
- التعاون مع الفريق الأزرق

### 2. عملية تخطيط الاشتباك
أنشئ سير عمل الاختبار:
- منهجية تعريف النطاق
- إجراءات تقييم المخاطر
- تخطيط تخصيص الموارد
- تطوير الجدول الزمني
- تعريف معايير النجاح

### 3. تطوير كتاب الهجوم
أنشئ أدلة هجوم شاملة:
- كتب لعب حقن الأوامر
- إجراءات استخراج النموذج
- توليد المدخلات الخصومية
- سيناريوهات هجوم خط أنابيب البيانات
- أدلة استغلال البنية التحتية

### 4. تطوير وإدارة الأدوات
أدر أدوات الفريق الأحمر:
- أدوات هجوم الذكاء الاصطناعي المخصصة
- تكامل الأدوات مفتوحة المصدر
- أنظمة توليد الحمولات
- أطر الأتمتة
- إجراءات صيانة الأدوات

### 5. إجراءات تنفيذ الاختبار
قيّد عمليات الاختبار:
- قوائم التحقق قبل الاشتباك
- بروتوكولات الاختبار النشط
- معايير جمع الأدلة
- طرق تتبع التقدم
- إجراءات ضمان الجودة

### 6. التنسيق في الوقت الحقيقي
مكّن التنسيق التشغيلي:
- بروتوكولات الاتصال
- إجراءات التصعيد
- آليات التوقف الطارئ
- تحديثات أصحاب المصلحة
- تكامل تتبع القضايا

### 7. معايير توثيق النتائج
حدد متطلبات التوثيق:
- قوالب وصف النتائج
- إرشادات جمع الأدلة
- معايير تقييم الأثر
- تنسيق توصيات المعالجة
- متطلبات التفاصيل التقنية

### 8. أنشطة ما بعد الاشتباك
حدد إجراءات الإغلاق:
- عمليات التحقق من النتائج
- سير عمل توليد التقارير
- جلسات التوضيح
- إجراءات نقل المعرفة
- توثيق الدروس المستفادة

### 9. المقاييس والتقارير
تتبع الفعالية التشغيلية:
- مقاييس نجاح الاشتباك
- توزيع شدة النتائج
- قياسات الوقت حتى الاستغلال
- مقاييس التغطية
- إثبات العائد على الاستثمار

### 10. التحسين المستمر
أنشئ عمليات التطور:
- آليات جمع التغذية الراجعة
- إجراءات تحديث كتاب اللعب
- أولويات تعزيز الأدوات
- تطوير برنامج التدريب
- مراقبة اتجاهات الصناعة

### 11. التعاون مع الفريق الأزرق
مكّن أنشطة الفريق البنفسجي:
- تخطيط التمارين المشتركة
- مشاركة قواعد الكشف
- اختبار إجراءات الاستجابة
- جلسات مشاركة المعرفة
- محاذاة المقاييس

### 12. محاذاة التنظيم والامتثال
ضمن الامتثال القانوني:
- توثيق التفويض
- امتثال حدود الاختبار
- متطلبات معالجة البيانات
- التزامات الإبلاغ التنظيمي
- الالتزام بالإرشادات الأخلاقية

### متطلبات المخرجات
قدم إطار عمليات فريق أحمر كامل مع الإجراءات والقوالب والإرشادات التشغيلية.
```

---

## Example Output Preview

```
# AI Red Team Operations Framework

## Team Structure
```
AI Red Team Lead
├── Senior AI Security Tester
│   ├── LLM Specialist
│   └── Adversarial ML Researcher
├── Infrastructure Security Specialist
│   ├── Cloud Security Tester
│   └── Network Security Tester
└── Automation Engineer
```

## Engagement Planning Template
```yaml
engagement:
  name: AI Platform Security Assessment
  scope:
    - Model inference endpoints
    - Training pipeline
    - API security
  duration: 10 days
  team_size: 4
  objectives:
    - Identify prompt injection vulnerabilities
    - Test model extraction resistance
    - Assess data pipeline security
```

## Attack Playbook Index
| Playbook ID | Name | Category | Estimated Time |
|-------------|------|----------|----------------|
| AI-RT-001 | Prompt Injection Suite | LLM Security | 8 hours |
| AI-RT-002 | Model Extraction | Model Security | 16 hours |
| AI-RT-003 | Adversarial Inputs | Model Security | 12 hours |
| AI-RT-004 | Data Pipeline Attacks | Infrastructure | 8 hours |

## Metrics Dashboard
| Metric | Target | Current | Status |
|--------|--------|---------|--------|
| Critical Findings/Month | 3-5 | 4 | ✅ |
| Engagement Success Rate | >90% | 92% | ✅ |
| Time-to-First-Finding | <4 hours | 3.2 hours | ✅ |
| Report Delivery | <48 hours | 36 hours | ✅ |

## Tool Inventory
| Tool | Purpose | Maintenance Schedule |
|------|---------|---------------------|
| Custom Prompt Fuzzer | LLM Testing | Monthly |
| Model Extractor | IP Protection Testing | Quarterly |
| Adversarial Generator | Evasion Testing | Monthly |
| API Scanner | Endpoint Testing | Weekly |

## Purple Team Coordination
- Monthly joint exercises
- Shared detection rule repository
- Quarterly tabletop exercises
- Bi-weekly knowledge sharing sessions
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## References

- [MITRE ATLAS](https://atlas.mitre.org/)
- [OWASP LLM Top 10](https://owasp.org/www-project-top-10-for-large-language-model-applications/)
- [NIST AI Risk Management Framework](https://www.nist.gov/itl/ai-risk-management-framework)
- [Microsoft AI Red Team Guidelines](https://www.microsoft.com/security/blog/2023/08/07/microsoft-ai-red-team-building-future-of-ai-security/)

---

*Last Updated: 2024*
*Version: 1.0*
