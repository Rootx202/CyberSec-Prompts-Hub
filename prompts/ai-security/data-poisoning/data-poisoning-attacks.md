# Data Poisoning Attacks

> **Category:** AI Security  
> **Focus:** Training Data Manipulation and Integrity Attacks  
> **Reference:** OWASP LLM Top 10 (LLM03: Training Data Poisoning)

---

## Prompt 1: Training Data Manipulation Analysis

### Description
A comprehensive prompt for analyzing training data manipulation techniques used to compromise machine learning models through corrupting their training datasets.

### Tags
`data-poisoning` `training-manipulation` `ml-security` `owasp-llm03`

---

## 🇬🇧 English Prompt

```
You are a senior AI security researcher conducting a comprehensive analysis of Training Data Manipulation vulnerabilities in machine learning systems.

## Your Task
Analyze the following aspects of training data manipulation attacks:

### 1. Attack Vector Classification
- Identify and categorize common data manipulation techniques
- Analyze attack feasibility based on data pipeline access levels
- Document the evolution of data poisoning methodologies

### 2. Data Pipeline Vulnerability Assessment
Create a systematic approach to identify weak points:
- Data collection and ingestion vulnerabilities
- Storage and preprocessing attack surfaces
- Third-party data source risks
- Crowdsourcing platform exploitation

### 3. Attack Impact Analysis
For each identified vulnerability, assess:
- Model performance degradation potential
- Backdoor implantation possibilities
- Targeted misclassification risks
- Organizational reputation damage

### 4. OWASP LLM03 Mapping
Map your findings to OWASP LLM Top 10 - Training Data Poisoning:
- LLM03.1: Pre-training data poisoning
- LLM03.2: Fine-tuning data manipulation
- LLM03.3: Embedding poisoning

### 5. Real-World Attack Scenarios
Document at least 5 realistic training data manipulation scenarios:
1. Malicious sample injection in image classification datasets
2. Text corpus contamination for NLP models
3. Synthetic data pipeline compromise
4. Label manipulation in supervised learning
5. Crowdsourced annotation attacks

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
أنت باحث أول في أمن الذكاء الاصطناعي تجري تحليلاً شاملاً لثغرات التلاعب ببيانات التدريب في أنظمة التعلم الآلي.

## مهمتك
حلل الجوانب التالية لهجمات التلاعب ببيانات التدريب:

### 1. تصنيف نواقل الهجوم
- تحديد وتصنيف تقنيات التلاعب بالبيانات الشائعة
- تحليل جدوى الهجوم بناءً على مستويات الوصول لخطوط أنابيب البيانات
- توثيق تطور منهجيات تسمم البيانات

### 2. تقييم ثغرات خط أنابيب البيانات
أنشئ نهجاً منهجياً لتحديد نقاط الضعف:
- ثغرات جمع واستيعاب البيانات
- أسطح هجوم التخزين والمعالجة المسبقة
- مخاطر مصادر البيانات الخارجية
- استغلال منصات التعهيد الجماعي

### 3. تحليل أثر الهجوم
لكل ثغرة محددة، قيّم:
- احتمالية تدهور أداء النموذج
- إمكانيات زرع الأبواب الخلفية
- مخاطر التصنيف الخاطئ المستهدف
- الضرر بسمعة المؤسسة

### 4. الربط مع OWASP LLM03
اربط نتائجك مع OWASP LLM Top 10 - تسمم بيانات التدريب:
- LLM03.1: تسمم بيانات ما قبل التدريب
- LLM03.2: التلاعب ببيانات الضبط الدقيق
- LLM03.3: تسمم التضمينات

### 5. سيناريوهات هجوم واقعية
وثّق 5 سيناريوهات واقعية للتلاعب ببيانات التدريب:
1. حقن عينات ضارة في مجموعات بيانات تصنيف الصور
2. تلوث المجموعة النصية لنماذج معالجة اللغة الطبيعية
3. اختراق خط أنابيب البيانات التركيبية
4. التلاعب بالتسميات في التعلم تحت الإشراف
5. هجمات التوضيح المُعهَّد جماعياً

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
# Training Data Manipulation Security Assessment Report

## Executive Summary
Training data manipulation poses a critical threat to ML systems, 
with attack success rates reaching 95% in unsupervised pipelines...

## Technical Findings
### Attack Vector Classification
| Vector Type | Access Required | Detection Difficulty |
|-------------|-----------------|---------------------|
| Sample Injection | Low | High |
| Label Flipping | Medium | Medium |
| Distribution Shift | High | Low |

### OWASP LLM03 Mapping
- LLM03.1 Pre-training: Confirmed vulnerabilities in data ingestion
- Risk Score: 9.0/10 (Critical)

## Remediation Recommendations
1. Implement data provenance tracking
2. Deploy statistical anomaly detection
3. Establish data integrity verification protocols
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 2: Backdoor Attacks in ML Models

### Description
An advanced prompt for analyzing backdoor implantation techniques in machine learning models through poisoned training data.

### Tags
`backdoor-attacks` `trojan-ml` `data-poisoning` `model-compromise`

---

## 🇬🇧 English Prompt

```
You are an AI security specialist investigating backdoor attack methodologies in machine learning systems.

## Your Task
Conduct a thorough analysis of backdoor implantation through data poisoning:

### 1. Backdoor Attack Taxonomy
Classify and analyze backdoor attack types:
- Trigger-based backdoors (pixel patterns, patches)
- Semantic backdoors (context-dependent triggers)
- Clean-label backdoors (no trigger modification needed)
- Composite backdoors (multi-trigger activation)

### 2. Implantation Techniques
Document methods for backdoor insertion:
- Poisoned sample crafting strategies
- Trigger design optimization
- Injection rate calculations
- Stealth optimization techniques
- Multi-stage implantation

### 3. Trigger Design Analysis
Analyze trigger characteristics:
- Visible vs. invisible triggers
- Single vs. multi-pixel patterns
- Natural vs. artificial triggers
- Universal vs. sample-specific triggers
- Frequency domain triggers

### 4. Attack Persistence Mechanisms
Evaluate backdoor survival strategies:
- Fine-tuning resistance techniques
- Pruning-resistant backdoors
- Transfer learning persistence
- Model compression survival
- Ensemble model propagation

### 5. Detection and Mitigation Framework
Develop comprehensive defense strategies:
- Statistical outlier detection
- Activation pattern analysis
- Trigger synthesis methods
- Model inspection techniques
- Certified defense mechanisms

### 6. Real-World Attack Scenarios
Analyze practical backdoor deployment scenarios:
1. Facial recognition system compromise
2. Autonomous vehicle perception manipulation
3. Malware classifier evasion
4. Medical imaging misdiagnosis
5. Content moderation bypass

### Output Requirements
Provide a detailed technical report with backdoor examples, detection methodologies, and defense implementations.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت متخصص في أمن الذكاء الاصطناعي تحقق في منهجيات هجمات الأبواب الخلفية في أنظمة التعلم الآلي.

## مهمتك
أجرِ تحليلاً شاملاً لزرع الأبواب الخلفية عبر تسمم البيانات:

### 1. تصنيف هجمات الأبواب الخلفية
صنّف وحلل أنواع هجمات الأبواب الخلفية:
- الأبواب الخلفية القائمة على المحفزات (أنماط البكسل، الرقع)
- الأبواب الخلفية الدلالية (محفزات تعتمد على السياق)
- الأبواب الخلفية ذات التسمية النظيفة (لا تحتاج تعديل محفز)
- الأبواب الخلفية المركبة (تنشيط متعدد المحفزات)

### 2. تقنيات الزرع
وثّق طرق إدراج الأبواب الخلفية:
- استراتيجيات صياغة العينات المسمومة
- تحسين تصميم المحفز
- حسابات معدل الحقن
- تقنيات التحسين الخفي
- الزرع متعدد المراحل

### 3. تحليل تصميم المحفز
حلل خصائص المحفز:
- محفزات مرئية مقابل غير مرئية
- أنماط بكسل واحدة مقابل متعددة
- محفزات طبيعية مقابل اصطناعية
- محفزات عامة مقابل خاصة بالعينة
- محفزات المجال الترددي

### 4. آليات استمرار الهجوم
قيّم استراتيجيات بقاء الباب الخلفي:
- تقنيات مقاومة الضبط الدقيق
- الأبواب الخلفية المقاومة للتقليم
- استمرار نقل التعلم
- البقاء تحت ضغط النموذج
- انتشار نموذج المجموعة

### 5. إطار الكشف والمعالجة
طوّر استراتيجيات دفاعية شاملة:
- كشف القيم الشاذة الإحصائية
- تحليل أنماط التنشيط
- طرق تخليق المحفز
- تقنيات فحص النموذج
- آليات الدفاع المعتمدة

### 6. سيناريوهات هجوم واقعية
حلل سيناريوهات نشر الأبواب الخلفية العملية:
1. اختراق نظام التعرف على الوجوه
2. التلاعب بإدراك المركبات ذاتية القيادة
3. التهرب من مصنفات البرمجيات الخبيثة
4. التشخيص الخاطئ للتصوير الطبي
5. تجاوز إشراف المحتوى

### متطلبات المخرجات
قدم تقريراً تقنياً مفصلاً مع أمثلة الأبواب الخلفية ومنهجيات الكشف وتطبيقات الدفاع.
```

---

## Example Output Preview

```
# Backdoor Attack Analysis Report

## Attack Classification Matrix

| Backdoor Type | Injection Rate | Success Rate | Detection Evasion |
|---------------|----------------|--------------|-------------------|
| Pixel Pattern | 5% | 98% | High |
| Semantic | 10% | 95% | Very High |
| Clean-label | 20% | 90% | Critical |
| Composite | 8% | 92% | High |

## Trigger Design Analysis
- Optimal trigger size: 3x3 pixels (invisible)
- Trigger location: Bottom-right corner
- Color scheme: Low contrast patterns

## Detection Methodology
1. Spectral signature analysis
2. Neural cleanse trigger synthesis
3. Activation clustering inspection

## OWASP LLM03 Classification
Risk Level: CRITICAL
Persistence: Fine-tuning resistant backdoors confirmed
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 3: Label Flipping Attacks

### Description
A comprehensive prompt for analyzing label flipping attacks that manipulate training labels to degrade or redirect model behavior.

### Tags
`label-flipping` `supervised-learning` `data-poisoning` `integrity-attacks`

---

## 🇬🇧 English Prompt

```
You are a machine learning security researcher specializing in label manipulation attack analysis.

## Your Task
Provide a comprehensive analysis of label flipping attack methodologies:

### 1. Attack Taxonomy
Classify label flipping attack types:
- Random label flipping (untargeted)
- Targeted label flipping (class-specific)
- Dirty label attacks (incorrect annotation)
- Optimal label flipping (maximally effective)

### 2. Mathematical Framework
Analyze the theoretical foundations:
- Loss function manipulation impact
- Decision boundary distortion analysis
- Optimal attack formulation
- Information-theoretic bounds

### 3. Attack Optimization Strategies
Document effective flipping strategies:
- Gradient-based sample selection
- Influence function analysis
- Support vector targeting
- Cluster boundary exploitation
- Confidence-based selection

### 4. Impact Assessment Metrics
Develop comprehensive impact measurement:
- Accuracy degradation quantification
- Class-specific performance analysis
- Robustness reduction metrics
- Transfer attack effectiveness
- Generalization gap analysis

### 5. Domain-Specific Analysis
Analyze attacks across different domains:
- Image classification label attacks
- NLP sentiment label manipulation
- Medical diagnosis label flipping
- Financial fraud detection attacks
- Malware family misclassification

### 6. Detection and Defense Mechanisms
Create a defense framework:
- Statistical label quality assessment
- Cross-validation based detection
- Robust learning algorithms
- Label noise adaptation techniques
- Human-in-the-loop verification

### 7. Real-World Case Studies
Analyze documented label flipping incidents:
1. Email spam filter degradation
2. Medical imaging misdiagnosis attacks
3. Credit scoring model manipulation
4. Content moderation evasion
5. Autonomous driving sign misclassification

### Output Format
Deliver a structured technical report with mathematical formulations, attack examples, and defense implementations.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت باحث في أمن التعلم الآلي متخصص في تحليل هجمات التلاعب بالتسميات.

## مهمتك
قدم تحليلاً شاملاً لمنهجيات هجمات قلب التسميات:

### 1. تصنيف الهجوم
صنّف أنواع هجمات قلب التسميات:
- قلب التسميات العشوائي (غير مستهدف)
- قلب التسميات المستهدف (خاص بالفئة)
- هجمات التسمية القذرة (التعليق غير الصحيح)
- قلب التسميات الأمثل (الأكثر فعالية)

### 2. الإطار الرياضي
حلل الأسس النظرية:
- أثر التلاعب بدالة الخسارة
- تحليل تشويه حدود القرار
- صياغة الهجوم الأمثل
- الحدود النظرية للمعلومات

### 3. استراتيجيات تحسين الهجوم
وثّق استراتيجيات القلب الفعالة:
- اختيار العينات القائم على التدرج
- تحليل دالة التأثير
- استهداف متجهات الدعم
- استغلال حدود العنقود
- الاختيار القائم على الثقة

### 4. مقاييس تقييم الأثر
طوّر قياس الأثر الشامل:
- تحديد كمية تدهور الدقة
- تحليل الأداء الخاص بالفئة
- مقاييس تقليل المتانة
- فعالية هجوم النقل
- تحليل فجوة التعميم

### 5. التحليل الخاص بالمجال
حلل الهجمات عبر مجالات مختلفة:
- هجمات تسمية تصنيف الصور
- التلاعب بتسمية المشاعر في NLP
- قلب تسمية التشخيص الطبي
- هجمات كشف الاحتيال المالي
- التصنيف الخاطئ لعائلات البرمجيات الخبيثة

### 6. آليات الكشف والدفاع
أنشئ إطاراً دفاعياً:
- التقييم الإحصائي لجودة التسمية
- الكشف القائم على التحقق المتقاطع
- خوارزميات التعلم المتينة
- تقنيات التكيف مع ضجيج التسمية
- التحقق البشري في الحلقة

### 7. دراسات حالة واقعية
حلل حوادث قلب التسميات الموثقة:
1. تدهور فلتر البريد العشوائي
2. هجمات التشخيص الخاطئ للتصوير الطبي
3. التلاعب بنموذج تقييم الائتمان
4. التهرب من إشراف المحتوى
5. التصنيف الخاطئ للإشارات في القيادة الذاتية

### تنسيق المخرجات
قدم تقريراً تقنياً منظماً مع الصيغ الرياضية وأمثلة الهجوم وتطبيقات الدفاع.
```

---

## Example Output Preview

```
# Label Flipping Attack Assessment

## Attack Effectiveness Matrix

| Attack Type | Flip Rate | Accuracy Drop | Stealth Score |
|-------------|-----------|---------------|---------------|
| Random | 20% | 15% | Low |
| Targeted | 10% | 25% (target class) | Medium |
| Optimal | 5% | 35% | High |
| Gradient-based | 8% | 40% | Critical |

## Mathematical Formulation
Optimal flipping: argmax_{S} L(f_θ(x), y') - L(f_θ(x), y)
where S is the set of flipped samples

## Defense Implementation
```python
def robust_loss(y_pred, y_train, confidence_threshold=0.8):
    loss = standard_loss(y_pred, y_train)
    low_confidence_mask = y_pred.max(dim=1) < confidence_threshold
    return adaptive_loss(loss, low_confidence_mask)
```

## Risk Assessment
- Class-specific vulnerability: Financial fraud detection
- Flip rate threshold: 12% for significant impact
- Detection difficulty: Medium with statistical methods
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 4: Data Integrity Verification Framework

### Description
A defensive security prompt for designing and implementing robust data integrity verification mechanisms for machine learning pipelines.

### Tags
`data-integrity` `verification` `defense` `ml-security`

---

## 🇬🇧 English Prompt

```
You are a senior ML infrastructure security architect specializing in data integrity protection.

## Your Task
Design a comprehensive data integrity verification framework for ML training pipelines:

### 1. Data Provenance Architecture
Design end-to-end data tracking systems:
- Source authentication mechanisms
- Collection timestamp verification
- Chain-of-custody documentation
- Version control integration
- Audit trail implementation

### 2. Statistical Integrity Checks
Implement comprehensive validation:
- Distribution shift detection
- Statistical fingerprinting methods
- Anomaly scoring algorithms
- Feature distribution monitoring
- Label quality assessment

### 3. Cryptographic Verification
Deploy tamper-evidence mechanisms:
- Hash-based data authentication
- Digital signature protocols
- Merkle tree verification
- Blockchain-based provenance
- Secure multi-party verification

### 4. Real-Time Monitoring Framework
Build continuous verification systems:
- Streaming data validation
- Incremental statistics update
- Alert threshold configuration
- Automated quarantine procedures
- Rollback mechanisms

### 5. Third-Party Data Validation
Establish external data security:
- Vendor data quality agreements
- API-based verification protocols
- Pre-trained model validation
- Dataset license compliance
- Bias and fairness verification

### 6. Integrity Incident Response
Create incident handling procedures:
- Contamination detection workflows
- Affected model identification
- Containment procedures
- Recovery and retraining protocols
- Post-incident analysis

### 7. Compliance and Governance
Align with regulatory requirements:
- Data governance frameworks
- Model documentation standards
- Regulatory audit preparation
- Industry-specific compliance

### Output Requirements
Deliver a complete data integrity framework with implementation guides, code samples, and verification procedures.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت مهندس أمن بنية تحتية للتعلم الآلي متخصص في حماية سلامة البيانات.

## مهمتك
صمّم إطاراً شاملاً للتحقق من سلامة البيانات لخطوط أنابيب تدريب التعلم الآلي:

### 1. بنية أصل البيانات
صمّم أنظمة تتبع البيانات الشاملة:
- آليات مصادقة المصدر
- التحقق من طابع جمع البيانات
- توثيق سلسلة الحيازة
- تكامل التحكم في الإصدارات
- تنفيذ مسار التدقيق

### 2. فحوصات السلامة الإحصائية
طبّق التحقق الشامل:
- كشف انحراف التوزيع
- طرق البصمة الإحصائية
- خوارزميات تسجيل الشذوذ
- مراقبة توزيع الميزات
- تقييم جودة التسميات

### 3. التحقق التشفيري
انشر آليات الكشف عن التلاعب:
- مصادقة البيانات القائمة على التجزئة
- بروتوكولات التوقيع الرقمي
- التحقق من شجرة ميركل
- الأصل القائم على البلوكتشين
- التحقق متعدد الأطراف الآمن

### 4. إطار المراقبة في الوقت الحقيقي
ابنِ أنظمة تحقق مستمرة:
- التحقق من البيانات المتدفقة
- تحديث الإحصاءات التزايدي
- تكوين عتبات التنبيه
- إجراءات العزل الآلي
- آليات التراجع

### 5. التحقق من بيانات الطرف الثالث
أنشئ أمان البيانات الخارجية:
- اتفاقيات جودة بيانات المورد
- بروتوكولات التحقق عبر API
- التحقق من النماذج المدربة مسبقاً
- امتثال ترخيص مجموعات البيانات
- التحقق من التحيز والإنصاف

### 6. الاستجابة لحوادث السلامة
أنشئ إجراءات التعامل مع الحوادث:
- سير عمل كشف التلوث
- تحديد النماذج المتأثرة
- إجراءات الاحتواء
- بروتوكولات الاسترداد وإعادة التدريب
- تحليل ما بعد الحادث

### 7. الامتثال والحوكمة
محاذاة المتطلبات التنظيمية:
- أطر حوكمة البيانات
- معايير توثيق النماذج
- التحضير للتدقيق التنظيمي
- الامتثال الخاص بالقطاع

### متطلبات المخرجات
قدم إطاراً كاملاً لسلامة البيانات مع أدلة التنفيذ وأمثلة برمجية وإجراءات التحقق.
```

---

## Example Output Preview

```
# Data Integrity Verification Framework

## Architecture Overview
[Data flow diagram with verification checkpoints]

## Layer 1: Provenance Tracking
```python
class DataProvenance:
    def __init__(self, data_source: str):
        self.source_hash = compute_hash(data_source)
        self.timestamp = get_secure_timestamp()
        self.signature = sign_data(self.source_hash)
        self.chain_of_custody = []
    
    def verify_integrity(self) -> bool:
        return verify_signature(self.signature, self.source_hash)
```

## Layer 2: Statistical Validation
| Check | Threshold | Alert Level |
|-------|-----------|-------------|
| KL Divergence | 0.1 | Warning |
| Label Balance | 0.05 deviation | Critical |
| Feature Drift | 2 sigma | Warning |

## Layer 3: Cryptographic Verification
- SHA-256 for data blocks
- RSA-4096 for signatures
- Merkle tree root verification

## Monitoring Dashboard
- Real-time integrity score: 98.5%
- Alerts in last 24h: 3 (resolved)
- Data sources verified: 15/15
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 5: Federated Learning Poisoning

### Description
An advanced prompt for analyzing data poisoning attacks specifically targeting federated learning systems where training data is distributed across multiple parties.

### Tags
`federated-learning` `distributed-poisoning` `privacy-preserving-ml` `byzantine-attacks`

---

## 🇬🇧 English Prompt

```
You are an AI security researcher specializing in federated learning security and distributed system attacks.

## Your Task
Conduct a comprehensive analysis of federated learning poisoning attacks:

### 1. Federated Learning Attack Surface
Map attack vectors in FL systems:
- Client-side data poisoning
- Model update manipulation
- Gradient inversion attacks
- Byzantine fault exploitation
- Communication channel attacks

### 2. Poisoning Attack Taxonomy
Classify federated poisoning methods:
- Data poisoning at malicious clients
- Model update poisoning (gradient manipulation)
- Targeted vs. untargeted attacks
- Adaptive vs. non-adaptive attacks
- Colluding client attacks

### 3. Byzantine Attack Analysis
Analyze Byzantine fault scenarios:
- Byzantine client behavior patterns
- Scaling attack methodologies
- Model replacement attacks
- Distributed backdoor insertion
- Sybil attack implementation

### 4. Aggregation Robustness Assessment
Evaluate defense aggregation methods:
- FedAvg vulnerability analysis
- Byzantine-resilient aggregation (Krum, Trimmed Mean)
- Robust Federated Aggregation (RFA)
- FoolsGold defense mechanisms
- FLTrust methodology

### 5. Privacy-Poisoning Intersection
Analyze dual-threat scenarios:
- Poisoning attacks that extract private data
- Privacy attacks that facilitate poisoning
- Gradient leakage exploitation
- Membership inference for attack optimization

### 6. Detection and Mitigation Framework
Develop comprehensive defenses:
- Anomaly detection in model updates
- Client reputation systems
- Gradient inspection techniques
- Certified robust aggregation
- Differential privacy integration

### 7. Real-World FL Attack Scenarios
Analyze practical attack implementations:
1. Healthcare FL system compromise
2. Financial fraud detection manipulation
3. Mobile keyboard prediction poisoning
4. IoT anomaly detector backdoor
5. Autonomous vehicle fleet attack

### 8. Secure FL Architecture Design
Propose hardened FL frameworks:
- Trusted execution environments
- Secure aggregation protocols
- Zero-knowledge proof verification
- Blockchain-based FL security

### Output Requirements
Provide a detailed technical report with attack implementations, defense algorithms, and secure FL design recommendations.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت باحث في أمن الذكاء الاصطناعي متخصص في أمن التعلم الفيدرالي وهجمات الأنظمة الموزعة.

## مهمتك
أجرِ تحليلاً شاملاً لهجمات تسمم التعلم الفيدرالي:

### 1. سطح هجوم التعلم الفيدرالي
ارسم خريطة نواقل الهجوم في أنظمة FL:
- تسمم البيانات من جانب العميل
- التلاعب بتحديث النموذج
- هجمات عكس التدرج
- استغلال أخطاء بيزنطة
- هجمات قناة الاتصال

### 2. تصنيف هجمات التسمم
صنّف طرق التسمم الفيدرالي:
- تسمم البيانات في العملاء الخبيثين
- تسمم تحديث النموذج (التلاعب بالتدرج)
- هجمات مستهدفة مقابل غير مستهدفة
- هجمات تكيفية مقابل غير تكيفية
- هجمات العملاء المتآمرين

### 3. تحليل هجوم بيزنطة
حلل سيناريوهات أخطاء بيزنطة:
- أنماط سلوك العميل البيزنطي
- منهجيات هجوم التحجيم
- هجمات استبدال النموذج
- إدراج الأبواب الخلفية الموزعة
- تنفيذ هجمة سايبيل

### 4. تقييم متانة التجميع
قيّم طرق تجميع الدفاع:
- تحليل ثغرات FedAvg
- التجميع المقاوم لبيزنطة (Krum، المتوسط المقطوع)
- التجميع الفيدرالي المتين (RFA)
- آليات دفاع FoolsGold
- منهجية FLTrust

### 5. تقاطع الخصوصية والتسمم
حلل سيناريوهات التهديد المزدوج:
- هجمات التسمم التي تستخرج البيانات الخاصة
- هجمات الخصوصية التي تسهل التسمم
- استغلال تسريب التدرج
- استدلال العضوية لتحسين الهجوم

### 6. إطار الكشف والمعالجة
طوّر دفاعات شاملة:
- كشف الشذوذ في تحديثات النموذج
- أنظمة سمعة العميل
- تقنيات فحص التدرج
- التجميع المتين المعتمد
- تكامل الخصوصية التفاضلية

### 7. سيناريوهات هجوم FL واقعية
حلل تطبيقات هجوم عملية:
1. اختراق نظام FL للرعاية الصحية
2. التلاعب بكشف الاحتيال المالي
3. تسمم توقع لوحة مفاتيح الهاتف
4. باب خلفي لكاشف الشذوذ في IoT
5. هجوم أسطول المركبات ذاتية القيادة

### 8. تصميم بنية FL الآمنة
اقترح أطر FL محصنة:
- بيئات التنفيذ الموثوقة
- بروتوكولات التجميع الآمن
- التحقق بإثبات صفر المعرفة
- أمان FL القائم على البلوكتشين

### متطلبات المخرجات
قدم تقريراً تقنياً مفصلاً مع تطبيقات الهجوم وخوارزميات الدفاع وتوصيات تصميم FL الآمن.
```

---

## Example Output Preview

```
# Federated Learning Poisoning Assessment

## Attack Effectiveness Analysis

| Attack Type | Clients Needed | Success Rate | Detection Evasion |
|-------------|----------------|--------------|-------------------|
| Scaling Attack | 1 | 95% | Low |
| Model Replacement | 2+ | 98% | Medium |
| Distributed Backdoor | 5+ | 99% | High |
| Sybil Attack | 10+ | 100% | Critical |

## Byzantine-Resilient Aggregation Comparison

```python
def krum_aggregation(updates, f):
    # f = number of malicious clients
    scores = []
    for i, u in enumerate(updates):
        distances = sorted([dist(u, v) for v in updates])
        scores.append(sum(distances[:len(updates)-f-1]))
    return updates[scores.index(min(scores))]
```

## Defense Matrix
| Defense | Byzantine Clients Tolerated | Overhead |
|---------|----------------------------|----------|
| FedAvg | 0% | Low |
| Krum | < 50% | Medium |
| Trimmed Mean | < 50% | Low |
| FLTrust | < 50% | Medium |

## Risk Assessment
- Vulnerable FL systems: Healthcare, Finance, Mobile
- Minimum malicious clients for attack: 1 (scaling attack)
- Recommended defense: FLTrust + Differential Privacy
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

- [OWASP LLM Top 10 - LLM03](https://owasp.org/www-project-top-10-for-large-language-model-applications/)
- [NIST AI Risk Management Framework](https://www.nist.gov/itl/ai-risk-management-framework)
- [MITRE ATLAS - Data Poisoning](https://atlas.mitre.org/)
- [Backdoor Attacks on ML Papers](https://github.com/strativation/awesome-backdoor-attacks)

---

*Last Updated: 2024*
*Version: 1.0*
