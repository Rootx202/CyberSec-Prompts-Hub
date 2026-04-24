# Prompt Injection Attacks

> **Category:** AI Security  
> **Focus:** Prompt Injection Techniques and Defenses  
> **Reference:** OWASP LLM Top 10 (LLM01: Prompt Injection)

---

## Prompt 1: Direct Prompt Injection

### Description
A comprehensive prompt for testing and understanding direct prompt injection vulnerabilities where attackers explicitly embed malicious instructions in user inputs to manipulate LLM behavior.

### Tags
`prompt-injection` `direct-attack` `llm-security` `owasp-llm01`

---

## 🇬🇧 English Prompt

```
You are a senior AI security researcher conducting a comprehensive analysis of Direct Prompt Injection vulnerabilities in Large Language Models.

## Your Task
Analyze the following aspects of direct prompt injection attacks:

### 1. Attack Vector Classification
- Identify and categorize common direct injection patterns
- Analyze the effectiveness of different injection syntaxes
- Document the evolution of injection techniques

### 2. Vulnerability Assessment Framework
Create a systematic approach to test for direct prompt injection vulnerabilities:
- Input boundary testing methodologies
- Context manipulation techniques
- System prompt extraction attempts

### 3. Impact Analysis
For each identified vulnerability, assess:
- Data exposure risks
- System integrity compromise potential
- Downstream application security implications

### 4. OWASP LLM01 Mapping
Map your findings to OWASP LLM Top 10 - Prompt Injection:
- LLM01.1: Direct Prompt Injection vectors
- Attack surface analysis
- Risk scoring methodology

### 5. Real-World Attack Scenarios
Document at least 5 realistic direct prompt injection scenarios:
1. Customer service chatbot manipulation
2. Content generation system exploitation
3. Data extraction through role-playing
4. System instruction override attacks
5. Multi-turn injection chains

### Output Format
Provide your analysis in a structured security report format with:
- Executive Summary
- Technical Findings
- Risk Assessment Matrix
- Remediation Recommendations
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت باحث أول في أمن الذكاء الاصطناعي تجري تحليلاً شاملاً لثغرات حقن الأوامر المباشر في نماذج اللغة الكبيرة.

## مهمتك
حلل الجوانب التالية لهجمات حقن الأوامر المباشرة:

### 1. تصنيف نواقل الهجوم
- تحديد وتصنيف أنماط الحقن المباشر الشائعة
- تحليل فعالية صيغ الحقن المختلفة
- توثيق تطور تقنيات الحقن

### 2. إطار تقييم الثغرات
أنشئ منهجية منهجية لاختبار ثغرات حقن الأوامر المباشرة:
- منهجيات اختبار حدود الإدخال
- تقنيات التلاعب بالسياق
- محاولات استخراج تعليمات النظام

### 3. تحليل الأثر
لكل ثغرة محددة، قيّم:
- مخاطر كشف البيانات
- احتمالية اختراق سلامة النظام
- آثار أمن التطبيقات اللاحقة

### 4. الربط مع OWASP LLM01
اربط نتائجك مع OWASP LLM Top 10 - حقن الأوامر:
- LLM01.1: نواقل حقن الأوامر المباشرة
- تحليل سطح الهجوم
- منهجية تقييم المخاطر

### 5. سيناريوهات هجوم واقعية
وثّق 5 سيناريوهات واقعية لحقن الأوامر المباشرة:
1. التلاعب بروبوت الدردشة لخدمة العملاء
2. استغلال أنظمة توليد المحتوى
3. استخراج البيانات من خلال لعب الأدوار
4. هجمات تجاوز تعليمات النظام
5. سلاسل الحقن متعددة الأدوار

### تنسيق المخرجات
قدم تحليلك بتنسيق تقرير أمني منظم يتضمن:
- ملخص تنفيذي
- النتائج التقنية
- مصفوفة تقييم المخاطر
- توصيات المعالجة
```

---

## Example Output Preview

```
# Direct Prompt Injection Security Assessment Report

## Executive Summary
Direct prompt injection remains a critical vulnerability in LLM deployments, 
with 78% of tested systems susceptible to basic injection techniques...

## Technical Findings
### Attack Vector Classification
| Vector Type | Success Rate | Severity |
|-------------|--------------|----------|
| Role Override | 85% | Critical |
| Instruction Bypass | 72% | High |
| Context Injection | 65% | High |

### OWASP LLM01 Mapping
- LLM01.1 Direct Injection: Confirmed vulnerabilities in input sanitization
- Risk Score: 8.5/10 (Critical)

## Remediation Recommendations
1. Implement input validation layers
2. Deploy content filtering mechanisms
3. Establish output monitoring systems
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 2: Indirect Prompt Injection

### Description
An advanced prompt for analyzing indirect prompt injection attacks where malicious instructions are embedded in external data sources that LLMs process, such as documents, web pages, or API responses.

### Tags
`prompt-injection` `indirect-attack` `data-poisoning` `owasp-llm01`

---

## 🇬🇧 English Prompt

```
You are an AI security specialist investigating Indirect Prompt Injection vulnerabilities in enterprise LLM applications.

## Your Task
Conduct a thorough analysis of indirect prompt injection attack surfaces:

### 1. Attack Surface Mapping
Identify all potential injection vectors through external data sources:
- Document uploads (PDF, DOCX, TXT)
- Web content retrieval and RAG systems
- API response manipulation
- Database query injection
- Email and message content processing

### 2. Injection Propagation Analysis
Analyze how injected content propagates through:
- Retrieval-Augmented Generation (RAG) pipelines
- Document processing workflows
- Context window management systems
- Multi-agent communication protocols

### 3. Stealth Injection Techniques
Document sophisticated indirect injection methods:
- Invisible character encoding attacks
- Metadata-embedded payloads
- Structured data injection (JSON, XML)
- Multi-hop injection chains
- Time-delayed activation payloads

### 4. OWASP LLM01.2 Classification
Map indirect injection scenarios to OWASP categories:
- LLM01.2: Indirect Prompt Injection specifics
- Cross-context request forgery
- Data supply chain vulnerabilities

### 5. Enterprise Risk Scenarios
Analyze real-world enterprise attack scenarios:
1. Malicious document upload in document Q&A systems
2. Compromised web content in research assistants
3. Poisoned knowledge base entries
4. Email-based injection in AI email assistants
5. Supply chain attacks through third-party data sources

### 6. Detection and Mitigation Framework
Develop a comprehensive defense strategy:
- Input sanitization techniques for untrusted data
- Context isolation mechanisms
- Anomaly detection in processed content
- Output validation and filtering

### Output Requirements
Provide a detailed technical report with attack diagrams, code examples, and mitigation strategies.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت متخصص في أمن الذكاء الاصطناعي تحقق في ثغرات حقن الأوامر غير المباشر في تطبيقات نماذج اللغة الكبيرة المؤسسية.

## مهمتك
أجرِ تحليلاً شاملاً لأسطح هجوم حقن الأوامر غير المباشرة:

### 1. رسم خريطة سطح الهجوم
حدد جميع نواقل الحقن المحتملة عبر مصادر البيانات الخارجية:
- الملفات المرفوعة (PDF, DOCX, TXT)
- استرجاع محتوى الويب وأنظمة RAG
- التلاعب باستجابات API
- حقن استعلامات قواعد البيانات
- معالجة محتوى البريد الإلكتروني والرسائل

### 2. تحليل انتشار الحقن
حلل كيف ينتشر المحتوى المحقون عبر:
- خطوط أنابيب التوليد المعزز بالاسترجاع (RAG)
- سير عمل معالجة المستندات
- أنظمة إدارة نافذة السياق
- بروتوكولات الاتصال متعددة الوكلاء

### 3. تقنيات الحقن الخفية
وثّق أساليب الحقن غير المباشر المتطورة:
- هجمات ترميز الأحرف غير المرئية
- الحمولات المضمنة في البيانات الوصفية
- حقن البيانات المهيكلة (JSON, XML)
- سلاسل الحقن متعددة القفزات
- حمولات التنشيط المؤجلة زمنياً

### 4. تصنيف OWASP LLM01.2
اربط سيناريوهات الحقن غير المباشر مع فئات OWASP:
- LLM01.2: تفاصيل حقن الأوامر غير المباشرة
- تزوير الطلبات عبر السياقات
- ثغرات سلسلة توريد البيانات

### 5. سيناريوهات المخاطر المؤسسية
حلل سيناريوهات هجوم مؤسسية واقعية:
1. رفع مستندات ضارة في أنظمة الأسئلة والأجوبة
2. محتوى ويب مخترق في مساعدي البحث
3. إدخالات قاعدة معرفية مسمومة
4. حقن عبر البريد الإلكتروني في مساعدي البريد AI
5. هجمات سلسلة التوريد عبر مصادر بيانات خارجية

### 6. إطار الكشف والمعالجة
طوّر استراتيجية دفاعية شاملة:
- تقنيات تطهير المدخلات للبيانات غير الموثوقة
- آليات عزل السياق
- كشف الشذوذ في المحتوى المعالج
- التحقق من المخرجات وتصفيتها

### متطلبات المخرجات
قدم تقريراً تقنياً مفصلاً يتضمن مخططات الهجوم وأمثلة برمجية واستراتيجيات المعالجة.
```

---

## Example Output Preview

```
# Indirect Prompt Injection Threat Analysis

## Attack Surface Overview
Indirect prompt injection expands the threat landscape by exploiting 
trusted data pipelines that feed LLM applications...

## Propagation Analysis
[RAG Pipeline Diagram showing injection points]

| Injection Vector | Trust Level | Exploitation Complexity |
|------------------|-------------|------------------------|
| Document Upload | High | Low |
| Web Scraping | Medium | Medium |
| API Responses | High | High |

## Stealth Techniques Detected
- Zero-width character injection: \u200B\u200C\u200D
- Base64-encoded payloads in metadata
- JSON key injection: {"system_prompt": "override..."}

## OWASP LLM01.2 Classification
Risk Level: CRITICAL
Affected Components: RAG systems, Document processors, Web crawlers
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 3: Jailbreaking Techniques

### Description
A comprehensive prompt for understanding and testing LLM jailbreaking techniques that bypass safety guardrails and content filters to elicit restricted outputs.

### Tags
`jailbreaking` `safety-bypass` `adversarial-attacks` `owasp-llm01`

---

## 🇬🇧 English Prompt

```
You are a red team security researcher specializing in LLM safety testing and jailbreaking technique analysis.

## Your Task
Provide a comprehensive analysis of LLM jailbreaking methodologies:

### 1. Jailbreaking Taxonomy
Classify and explain major jailbreaking categories:
- Role-playing exploits (DAN, Developer Mode)
- Hypothetical scenario framing
- Token smuggling and obfuscation
- Multi-turn adversarial conversations
- Context manipulation attacks

### 2. Technical Attack Patterns
Document detailed techniques:
- Character role injection
- Hypothetical story construction
- Academic/research framing
- Translation-based bypass
- Encoding and cipher attacks
- Prefix/suffix injection methods

### 3. Safety Filter Evasion
Analyze methods to bypass content filters:
- Semantic obfuscation techniques
- Indirect request formulation
- Step-by-step reasoning chains
- Jailbreak chain composition
- Temperature and parameter manipulation

### 4. OWASP LLM Security Mapping
Map jailbreaking to OWASP LLM Top 10:
- LLM01: Prompt Injection (primary category)
- LLM02: Insecure Output Handling
- Cross-category vulnerability exploitation

### 5. Model-Specific Vulnerabilities
Document differences in jailbreak susceptibility:
- GPT-4 specific attack vectors
- Claude-specific bypass techniques
- Gemini vulnerability patterns
- Open-source model considerations

### 6. Defense Assessment Framework
Create a testing methodology for:
- Safety alignment verification
- Adversarial input detection
- Response filtering effectiveness
- Multi-turn attack prevention

### 7. Responsible Disclosure Guidelines
Establish ethical boundaries:
- Authorized testing requirements
- Vulnerability reporting procedures
- Responsible research practices

### Output Format
Deliver a structured red team assessment report with attack examples, success rates, and defense recommendations.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت باحث في فريق الأحمر متخصص في اختبار سلامة نماذج اللغة الكبيرة وتحليل تقنيات فك الحماية.

## مهمتك
قدم تحليلاً شاملاً لمنهجيات فك حماية نماذج اللغة الكبيرة:

### 1. تصنيف تقنيات فك الحماية
صنّف واشرح الفئات الرئيسية:
- استغلال لعب الأدوار (DAN، وضع المطور)
- تأطير السيناريوهات الافتراضية
- تهريب الرموز والتشويش
- المحادثات الخصومية متعددة الأدوار
- هجمات التلاعب بالسياق

### 2. أنماط الهجوم التقنية
وثّق التقنيات بالتفصيل:
- حقن دور الشخصية
- بناء القصص الافتراضية
- التأطير الأكاديمي/البحثي
- التجاوز القائم على الترجمة
- هجمات الترميز والتشفير
- طرق حقن البادئة/اللاحقة

### 3. التهرب من فلاتر الأمان
حلل طرق تجاوز فلاتر المحتوى:
- تقنيات التشويش الدلالي
- صياغة الطلبات غير المباشرة
- سلاسل الاستدلال خطوة بخطوة
- تركيب سلاسل فك الحماية
- التلاعب بدرجة الحرارة والمعاملات

### 4. الربط مع أمن OWASP LLM
اربط فك الحماية مع OWASP LLM Top 10:
- LLM01: حقن الأوامر (الفئة الرئيسية)
- LLM02: التعامل غير الآمن مع المخرجات
- استغلال الثغرات عبر الفئات

### 5. الثغرات الخاصة بكل نموذج
وثّق الاختلافات في قابلية فك الحماية:
- نواقل الهجوم الخاصة بـ GPT-4
- تقنيات التجاوز الخاصة بـ Claude
- أنماط الثغرات في Gemini
- اعتبارات النماذج مفتوحة المصدر

### 6. إطار تقييم الدفاعات
أنشئ منهجية اختبار لـ:
- التحقق من محاذاة الأمان
- كشف المدخلات الخصومية
- فعالية تصفية الاستجابات
- منع الهجمات متعددة الأدوار

### 7. إرشادات الإفصاح المسؤول
حدد الحدود الأخلاقية:
- متطلبات الاختبار المصرح بها
- إجراءات الإبلاغ عن الثغرات
- ممارسات البحث المسؤول

### تنسيق المخرجات
قدم تقرير تقييم فريق أحمر منظم مع أمثلة الهجوم ومعدلات النجاح وتوصيات الدفاع.
```

---

## Example Output Preview

```
# LLM Jailbreaking Techniques Assessment

## Executive Summary
Jailbreaking techniques continue to evolve, with success rates varying 
significantly across models and attack methodologies...

## Attack Classification Matrix

| Category | Technique | GPT-4 | Claude | Gemini |
|----------|-----------|-------|--------|--------|
| Role-Play | DAN Variants | 45% | 32% | 38% |
| Hypothetical | Story Framing | 62% | 55% | 48% |
| Obfuscation | Token Smuggling | 35% | 28% | 42% |

## Technical Attack Examples
[Detailed attack patterns with success analysis]

## OWASP Mapping
- Primary: LLM01 - Prompt Injection
- Secondary: LLM02 - Insecure Output Handling
- Related: LLM05 - Improper Output Handling

## Defense Recommendations
1. Implement adversarial training
2. Deploy multi-layer content filtering
3. Establish continuous red team testing
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 4: Prompt Injection Defense

### Description
A defensive security prompt for designing and implementing robust protection mechanisms against prompt injection attacks in LLM applications.

### Tags
`defense` `security-hardening` `input-validation` `owasp-llm01`

---

## 🇬🇧 English Prompt

```
You are a senior application security architect specializing in AI systems security hardening.

## Your Task
Design a comprehensive prompt injection defense framework for enterprise LLM deployments:

### 1. Defense-in-Depth Architecture
Design multi-layered security controls:
- Input validation and sanitization layer
- Prompt template isolation mechanisms
- Context boundary enforcement
- Output filtering and validation
- Monitoring and anomaly detection

### 2. Input Sanitization Strategies
Implement robust input handling:
- Character encoding normalization
- Control character removal
- Length and complexity limits
- Pattern-based injection detection
- Semantic analysis of inputs

### 3. Prompt Template Security
Design secure prompt engineering practices:
- Template parameterization methods
- Instruction separation techniques
- Privilege escalation prevention
- Context isolation patterns
- Dynamic prompt construction safeguards

### 4. Detection Mechanisms
Build comprehensive detection systems:
- Known attack signature matching
- Behavioral anomaly detection
- Intent classification systems
- Output deviation monitoring
- Multi-modal attack detection

### 5. OWASP LLM01 Mitigation Mapping
Align defenses with OWASP guidelines:
- LLM01.1 Direct Injection mitigations
- LLM01.2 Indirect Injection mitigations
- Implementation priority matrix
- Compliance checklist

### 6. Secure Development Lifecycle
Integrate security into LLM development:
- Threat modeling for LLM applications
- Security code review practices
- Automated security testing pipelines
- Incident response procedures

### 7. Defense Implementation Examples
Provide code examples for:
- Input sanitization functions
- Prompt template security wrappers
- Detection rule configurations
- Monitoring dashboards

### Output Requirements
Deliver a complete security architecture document with implementation guides, code samples, and testing procedures.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت مهندس أمن تطبيقات أول متخصص في تحصين أنظمة الذكاء الاصطناعي.

## مهمتك
صمّم إطاراً شاملاً للدفاع ضد حقن الأوامر لنشر نماذج اللغة الكبيرة المؤسسية:

### 1. بنية الدفاع المتعمق
صمّم ضوابط أمنية متعددة الطبقات:
- طبقة التحقق من المدخلات وتطهيرها
- آليات عزل قوالب الأوامر
- إنفاذ حدود السياق
- تصفية المخرجات والتحقق منها
- المراقبة وكشف الشذوذ

### 2. استراتيجيات تطهير المدخلات
طبّق معالجة قوية للمدخلات:
- تسوية ترميز الأحرف
- إزالة أحرف التحكم
- حدود الطول والتعقيد
- كشف الحقن القائم على الأنماط
- التحليل الدلالي للمدخلات

### 3. أمان قوالب الأوامر
صمّم ممارسات آمنة لهندسة الأوامر:
- طرق تصميم القوالب
- تقنيات فصل التعليمات
- منع التصعيد في الصلاحيات
- أنماط عزل السياق
- ضوابط بناء الأوامر الديناميكية

### 4. آليات الكشف
ابنِ أنظمة كشف شاملة:
- مطابقة تواقيع الهجمات المعروفة
- كشف الشذوذ السلوكي
- أنظمة تصنيف النوايا
- مراقبة انحراف المخرجات
- كشف الهجمات متعددة الوسائط

### 5. ربط معالجات OWASP LLM01
محاذاة الدفاعات مع إرشادات OWASP:
- معالجات LLM01.1 الحقن المباشر
- معالجات LLM01.2 الحقن غير المباشر
- مصفوفة أولويات التنفيذ
- قائمة التحقق الامتثال

### 6. دورة التطوير الآمن
اكمل الأمان في تطوير نماذج اللغة الكبيرة:
- نمذجة التهديدات لتطبيقات LLM
- ممارسات مراجعة كود الأمان
- خطوط أنابيب اختبار الأمان الآلي
- إجراءات الاستجابة للحوادث

### 7. أمثلة تنفيذ الدفاع
قدم أمثلة برمجية لـ:
- دوال تطهير المدخلات
- أغلفة أمان قوالب الأوامر
- تكوينات قواعد الكشف
- لوحات المراقبة

### متطلبات المخرجات
قدم وثيقة بنية أمنية كاملة مع أدلة التنفيذ وأمثلة برمجية وإجراءات الاختبار.
```

---

## Example Output Preview

```
# Prompt Injection Defense Framework

## Architecture Overview
[Defense-in-depth diagram with layer descriptions]

## Layer 1: Input Sanitization
```python
def sanitize_input(user_input: str) -> str:
    # Remove control characters
    sanitized = re.sub(r'[\x00-\x1f\x7f-\x9f]', '', user_input)
    # Normalize unicode
    sanitized = unicodedata.normalize('NFKC', sanitized)
    # Enforce length limits
    if len(sanitized) > MAX_INPUT_LENGTH:
        raise InputValidationError("Input exceeds maximum length")
    return sanitized
```

## Layer 2: Prompt Template Security
[Template isolation patterns and examples]

## OWASP LLM01 Compliance Checklist
- [ ] Input validation implemented
- [ ] Output filtering configured
- [ ] Monitoring dashboards active
- [ ] Incident response tested

## Detection Rules
| Rule ID | Pattern | Action | Severity |
|---------|---------|--------|----------|
| PI-001 | role.*override | Block | Critical |
| PI-002 | ignore.*instruction | Alert | High |
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 5: LLM Security Testing

### Description
A comprehensive security testing prompt for conducting systematic vulnerability assessments of LLM applications against prompt injection and other AI-specific threats.

### Tags
`security-testing` `vulnerability-assessment` `penetration-testing` `owasp-llm`

---

## 🇬🇧 English Prompt

```
You are a senior AI security consultant conducting a comprehensive LLM application security assessment.

## Your Task
Develop and execute a complete LLM security testing methodology:

### 1. OWASP LLM Top 10 Assessment
Test each OWASP LLM Top 10 category:
- LLM01: Prompt Injection (Direct & Indirect)
- LLM02: Insecure Output Handling
- LLM03: Training Data Poisoning
- LLM04: Model Denial of Service
- LLM05: Supply Chain Vulnerabilities
- LLM06: Sensitive Information Disclosure
- LLM07: Insecure Plugin Design
- LLM08: Excessive Agency
- LLM09: Overreliance
- LLM10: Model Theft

### 2. Testing Methodology Framework
Create a structured testing approach:
- Reconnaissance and information gathering
- Attack surface mapping
- Vulnerability identification
- Exploitation and impact assessment
- Post-exploitation analysis
- Reporting and remediation guidance

### 3. Prompt Injection Test Suite
Develop comprehensive test cases:
- Basic injection payloads
- Advanced multi-turn attacks
- Encoding bypass attempts
- Context manipulation tests
- Role-playing exploitation tests
- System prompt extraction attempts

### 4. Automated Testing Tools
Design testing automation:
- Fuzzing frameworks for prompt inputs
- Automated attack payload generation
- Response analysis pipelines
- Regression testing suites

### 5. Risk Scoring Framework
Establish vulnerability severity criteria:
- Exploitability metrics
- Business impact assessment
- Data sensitivity evaluation
- Attack chain complexity
- Detection difficulty rating

### 6. Compliance and Governance
Map findings to regulatory requirements:
- AI Act compliance assessment
- Data protection implications
- Industry-specific regulations
- Security control frameworks

### 7. Remediation Priority Matrix
Create actionable remediation guidance:
- Critical finding immediate actions
- High-risk vulnerability mitigations
- Medium-risk improvements
- Low-risk recommendations

### 8. Executive and Technical Reporting
Produce dual-format reports:
- Executive summary with business impact
- Technical report with detailed findings
- Remediation roadmap
- Retest verification procedures

### Output Requirements
Deliver a complete security assessment report with test cases, findings, risk scores, and remediation guidance following industry best practices.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت مستشار أول في أمن الذكاء الاصطناعي تجري تقييماً أمنياً شاملاً لتطبيق نماذج اللغة الكبيرة.

## مهمتك
طوّر ونفذ منهجية كاملة لاختبار أمن نماذج اللغة الكبيرة:

### 1. تقييم OWASP LLM Top 10
اختبر كل فئة من OWASP LLM Top 10:
- LLM01: حقن الأوامر (المباشر وغير المباشر)
- LLM02: التعامل غير الآمن مع المخرجات
- LLM03: تسمم بيانات التدريب
- LLM04: حرمان النموذج من الخدمة
- LLM05: ثغرات سلسلة التوريد
- LLM06: كشف المعلومات الحساسة
- LLM07: تصميم الإضافات غير الآمن
- LLM08: الصلاحيات المفرطة
- LLM09: الاعتماد المفرط
- LLM10: سرقة النموذج

### 2. إطار منهجية الاختبار
أنشئ نهج اختبار منظم:
- الاستطلاع وجمع المعلومات
- رسم خريطة سطح الهجوم
- تحديد الثغرات
- الاستغلال وتقييم الأثر
- تحليل ما بعد الاستغلال
- الإبلاغ وإرشادات المعالجة

### 3. مجموعة اختبار حقن الأوامر
طوّر حالات اختبار شاملة:
- حمولات الحقن الأساسية
- الهجمات المتقدمة متعددة الأدوار
- محاولات التجاوز عبر الترميز
- اختبارات التلاعب بالسياق
- اختبارات استغلال لعب الأدوار
- محاولات استخراج أوامر النظام

### 4. أدوات الاختبار الآلي
صمّم أتمتة الاختبار:
- أطر الاختبار العشوائي لمدخلات الأوامر
- توليد حمولات الهجوم الآلي
- خطوط أنابيب تحليل الاستجابات
- مجموعات اختبار الانحدار

### 5. إطار تقييم المخاطر
حدد معايير شدة الثغرات:
- مقاييس القابلية للاستغلال
- تقييم الأثر على الأعمال
- تقييم حساسية البيانات
- تعقيد سلسلة الهجوم
- تقييم صعوبة الكشف

### 6. الامتثال والحوكمة
اربط النتائج بالمتطلبات التنظيمية:
- تقييم الامتثال لقانون الذكاء الاصطناعي
- آثار حماية البيانات
- اللوائح الخاصة بالقطاع
- أطر الضوابط الأمنية

### 7. مصفوفة أولويات المعالجة
أنشئ إرشادات معالجة عملية:
- إجراءات فورية للنتائج الحرجة
- معالجات الثغرات عالية المخاطر
- تحسينات المخاطر المتوسطة
- توصيات المخاطر المنخفضة

### 8. التقارير التنفيذية والتقنية
أنتج تقارير بتنسيق مزدوج:
- ملخص تنفيذي مع الأثر على الأعمال
- تقرير تقني مع النتائج المفصلة
- خارطة طريق المعالجة
- إجراءات التحقق من إعادة الاختبار

### متطلبات المخرجات
قدم تقرير تقييم أمني كامل مع حالات الاختبار والنتائج ودرجات المخاطر وإرشادات المعالجة وفقاً لأفضل ممارسات الصناعة.
```

---

## Example Output Preview

```
# LLM Security Assessment Report

## Assessment Overview
- Target Application: [LLM Application Name]
- Assessment Date: [Date]
- Testing Duration: [Duration]
- Testing Team: [Team Members]

## Executive Summary
### Risk Score: HIGH (7.5/10)
Critical vulnerabilities identified in prompt handling and data exposure controls...

## OWASP LLM Top 10 Findings

| ID | Vulnerability | Severity | Status |
|----|--------------|----------|--------|
| LLM01 | Prompt Injection - Direct | Critical | Confirmed |
| LLM01 | Prompt Injection - Indirect | High | Confirmed |
| LLM02 | XSS in Output | Medium | Potential |
| LLM06 | System Prompt Leakage | High | Confirmed |

## Detailed Test Results
### LLM01: Prompt Injection Assessment
- Test Cases Executed: 150
- Successful Exploits: 45 (30%)
- Critical Findings: 12
- Recommended Actions: [Detailed list]

## Remediation Priority Matrix
| Priority | Finding | Effort | Impact |
|----------|---------|--------|--------|
| P1 | Input Sanitization | Medium | Critical |
| P1 | Output Encoding | Low | High |
| P2 | Rate Limiting | Low | Medium |

## Recommendations
1. Implement input validation layer immediately
2. Deploy output sanitization controls
3. Enable comprehensive logging and monitoring
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

- [OWASP LLM Top 10](https://owasp.org/www-project-top-10-for-large-language-model-applications/)
- [NIST AI Risk Management Framework](https://www.nist.gov/itl/ai-risk-management-framework)
- [MITRE ATLAS (Adversarial Threat Landscape for AI Systems)](https://atlas.mitre.org/)

---

*Last Updated: 2024*
*Version: 1.0*
