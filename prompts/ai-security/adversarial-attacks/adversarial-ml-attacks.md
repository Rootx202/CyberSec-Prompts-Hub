# Adversarial Machine Learning Attacks

> **Category:** AI Security  
> **Focus:** Adversarial ML Fundamentals and Attack Methodologies  
> **Reference:** MITRE ATLAS, NIST AI RMF

---

## Prompt 1: Adversarial ML Fundamentals

### Description
A comprehensive prompt for understanding the foundational concepts of adversarial machine learning, including attack taxonomies, theoretical frameworks, and fundamental principles.

### Tags
`adversarial-ml` `fundamentals` `attack-taxonomy` `ml-security`

---

## 🇬🇧 English Prompt

```
You are a senior AI security researcher conducting a comprehensive study of adversarial machine learning fundamentals.

## Your Task
Provide a thorough analysis of adversarial ML foundational concepts:

### 1. Adversarial ML Taxonomy
Classify and explain attack categories:
- Evasion attacks (test-time attacks)
- Poisoning attacks (training-time attacks)
- Exploratory attacks (model extraction)
- Inference attacks (privacy violations)
- Model inversion attacks

### 2. Theoretical Foundations
Analyze the mathematical underpinnings:
- Adversarial example existence proofs
- Decision boundary vulnerability analysis
- Gradient-based vulnerability theory
- High-dimensional space fragility
- Linear behavior in neural networks

### 3. Attack Surface Analysis
Map vulnerabilities across ML pipeline:
- Input space vulnerabilities
- Model architecture weaknesses
- Training data susceptibility
- Inference pipeline exposure
- Deployment environment risks

### 4. Adversarial Example Generation
Document primary attack methods:
- Fast Gradient Sign Method (FGSM)
- Projected Gradient Descent (PGD)
- Carlini & Wagner (C&W) attacks
- DeepFool algorithm
- Jacobian-based Saliency Map Attack (JSMA)

### 5. Transferability Analysis
Analyze attack transfer properties:
- Transfer between model architectures
- Cross-model vulnerability exploitation
- Black-box transfer attack strategies
- Ensemble-based transfer improvement
- Domain-specific transfer considerations

### 6. Threat Model Framework
Establish comprehensive threat modeling:
- Attacker knowledge levels (white/gray/black box)
- Attacker capabilities and access
- Attack goals (targeted vs. untargeted)
- Resource constraints analysis
- Realistic threat scenarios

### 7. Defense Landscape Overview
Map the defense ecosystem:
- Adversarial training approaches
- Input transformation defenses
- Detection-based methods
- Certified defense mechanisms
- Practical deployment considerations

### Output Format
Provide a comprehensive educational document with theoretical foundations, mathematical formulations, and practical examples.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت باحث أول في أمن الذكاء الاصطناعي تجري دراسة شاملة لأساسيات التعلم الآلي الخصومي.

## مهمتك
قدم تحليلاً شاملاً للمفاهيم الأساسية للتعلم الآلي الخصومي:

### 1. تصنيف التعلم الآلي الخصومي
صنّف واشرح فئات الهجوم:
- هجمات التهرب (هجمات وقت الاختبار)
- هجمات التسمم (هجمات وقت التدريب)
- هجمات الاستكشاف (استخراج النموذج)
- هجمات الاستدلال (انتهاكات الخصوصية)
- هجمات عكس النموذج

### 2. الأسس النظرية
حلل الأسس الرياضية:
- براهين وجود الأمثلة الخصومية
- تحليل ثغرات حدود القرار
- نظرية الثغرات القائمة على التدرج
- هشاشة الفضاء عالي الأبعاد
- السلوك الخطي في الشبكات العصبية

### 3. تحليل سطح الهجوم
ارسم خريطة الثغرات عبر خط أنابيب التعلم الآلي:
- ثغرات فضاء الإدخال
- نقاط ضعف بنية النموذج
- قابلية بيانات التدريب
- تعرض خط أنابيب الاستدلال
- مخاطر بيئة النشر

### 4. توليد الأمثلة الخصومية
وثّق طرق الهجوم الأساسية:
- طريقة إشارة التدرج السريع (FGSM)
- هبوط التدرج المُسقط (PGD)
- هجمات Carlini & Wagner (C&W)
- خوارزمية DeepFool
- هجوم خريطة الأهمية القائم على اليعقوبي (JSMA)

### 5. تحليل القابلية للنقل
حلل خصائص نقل الهجوم:
- النقل بين بنى النماذج
- استغلال الثغرات عبر النماذج
- استراتيجيات هجوم النقل للصندوق الأسود
- تحسين النقل القائم على المجموعات
- اعتبارات النقل الخاصة بالمجال

### 6. إطار نمذجة التهديد
أنشئ نمذجة تهديد شاملة:
- مستويات معرفة المهاجم (صندوق أبيض/رمادي/أسود)
- قدرات المهاجم ووصوله
- أهداف الهجوم (مستهدفة مقابل غير مستهدفة)
- تحليل قيود الموارد
- سيناريوهات التهديد الواقعية

### 7. نظرة عامة على مشهد الدفاع
ارسم خريطة منظومة الدفاع:
- مناهج التدريب الخصومي
- دفاعات تحويل المدخلات
- الطرق القائمة على الكشف
- آليات الدفاع المعتمدة
- اعتبارات النشر العملي

### تنسيق المخرجات
قدم وثيقة تعليمية شاملة مع الأسس النظرية والصيغ الرياضية وأمثلة عملية.
```

---

## Example Output Preview

```
# Adversarial ML Fundamentals Guide

## Attack Taxonomy Overview

| Attack Type | Attack Phase | Knowledge Required | Primary Goal |
|-------------|--------------|-------------------|--------------|
| Evasion | Test-time | Model internals | Misclassification |
| Poisoning | Training-time | Data access | Model corruption |
| Extraction | Any | API access | Model stealing |
| Inference | Test-time | Model access | Privacy violation |

## Theoretical Foundation
```
FGSM Formula: x_adv = x + ε * sign(∇_x J(θ, x, y))
Where:
- x: original input
- ε: perturbation magnitude
- J: loss function
- θ: model parameters
```

## Transferability Matrix
| Source → Target | CNN | Transformer | RNN |
|-----------------|-----|-------------|-----|
| CNN | 85% | 65% | 60% |
| Transformer | 70% | 90% | 55% |
| RNN | 55% | 50% | 80% |

## Threat Model Summary
- White-box: Full model access, gradient computation possible
- Gray-box: Partial knowledge, architecture known
- Black-box: API access only, transfer attacks required
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 2: Model Extraction Attacks

### Description
An advanced prompt for analyzing model stealing and extraction attacks that aim to reconstruct or replicate machine learning models through query access.

### Tags
`model-extraction` `model-stealing` `intellectual-property` `api-security`

---

## 🇬🇧 English Prompt

```
You are an AI security specialist investigating model extraction and intellectual property theft in machine learning systems.

## Your Task
Conduct a comprehensive analysis of model extraction attacks:

### 1. Attack Motivation and Impact
Analyze the threat landscape:
- Intellectual property theft implications
- Competitive advantage erosion
- Model cloning for adversarial attacks
- Privacy violation through extracted models
- Economic impact assessment

### 2. Extraction Attack Taxonomy
Classify model stealing methods:
- Equation-solving attacks
- Path-finding attacks
- Model distillation attacks
- Active learning-based extraction
- Hyperparameter stealing techniques

### 3. Query-Based Extraction
Analyze API-based attack methods:
- Optimal query selection strategies
- Adaptive sampling techniques
- Decision boundary mapping
- Gradient estimation from outputs
- Efficiency optimization methods

### 4. Architecture-Specific Vulnerabilities
Document extraction approaches per model type:
- Neural network extraction methods
- Decision tree path extraction
- SVM hyperplane reconstruction
- Ensemble model decomposition
- Transformer model stealing

### 5. Extraction Attack Metrics
Develop effectiveness measurement:
- Fidelity (agreement with original)
- Accuracy preservation
- Query efficiency
- Computational cost analysis
- Information leakage quantification

### 6. Defense Mechanisms
Evaluate protection strategies:
- Query rate limiting
- Output perturbation
- Rounding and noise injection
- Watermarking techniques
- Differential privacy for APIs

### 7. Real-World Attack Scenarios
Analyze documented extraction cases:
1. MLaaS model stealing attacks
2. Computer vision API extraction
3. NLP model replication
4. Fraud detection model cloning
5. Recommendation system extraction

### 8. Legal and Ethical Considerations
Address regulatory aspects:
- IP protection frameworks
- Trade secret implications
- Terms of service violations
- Responsible disclosure guidelines
- Defensive research ethics

### Output Requirements
Provide a detailed technical report with attack implementations, defense strategies, and legal considerations.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت متخصص في أمن الذكاء الاصطناعي تحقق في استخراج النماذج وسرعة الملكية الفكرية في أنظمة التعلم الآلي.

## مهمتك
أجرِ تحليلاً شاملاً لهجمات استخراج النماذج:

### 1. دوافع الهجوم وأثره
حلل مشهد التهديدات:
- آثار سرقة الملكية الفكرية
- تآكل الميزة التنافسية
- استنساخ النماذج للهجمات الخصومية
- انتهاك الخصوصية عبر النماذج المستخرجة
- تقييم الأثر الاقتصادي

### 2. تصنيف هجمات الاستخراج
صنّف طرق سرقة النماذج:
- هجمات حل المعادلات
- هجمات إيجاد المسار
- هجمات تقطير النموذج
- الاستخراج القائم على التعلم النشط
- تقنيات سرقة المعاملات الفائقة

### 3. الاستخراج القائم على الاستعلام
حلل طرق الهجوم عبر API:
- استراتيجيات اختيار الاستعلام الأمثل
- تقنيات العينات التكيفية
- رسم خريطة حدود القرار
- تقدير التدرج من المخرجات
- طرق تحسين الكفاءة

### 4. الثغرات الخاصة بكل بنية
وثّق مناهج الاستخراج حسب نوع النموذج:
- طرق استخراج الشبكات العصبية
- استخراج مسار شجرة القرار
- إعادة بناء المستوي الفائق لـ SVM
- تفكيك نموذج المجموعة
- سرقة نماذج المحولات

### 5. مقاييس هجوم الاستخراج
طوّر قياس الفعالية:
- الدقة (الاتفاق مع الأصل)
- الحفاظ على الدقة
- كفاءة الاستعلام
- تحليل التكلفة الحسابية
- تحديد كمية تسريب المعلومات

### 6. آليات الدفاع
قيّم استراتيجيات الحماية:
- تحديد معدل الاستعلام
- اضطراب المخرجات
- التقريب وحقن الضوضاء
- تقنيات العلامة المائية
- الخصوصية التفاضلية لواجهات API

### 7. سيناريوهات هجوم واقعية
حلل حالات الاستخراج الموثقة:
1. هجمات سرقة نماذج MLaaS
2. استخراج API الرؤية الحاسوبية
3. تكرار نماذج معالجة اللغة الطبيعية
4. استنساخ نماذج كشف الاحتيال
5. استخراج أنظمة التوصية

### 8. الاعتبارات القانونية والأخلاقية
عالج الجوانب التنظيمية:
- أطر حماية الملكية الفكرية
- آثار الأسرار التجارية
- انتهاكات شروط الخدمة
- إرشادات الإفصاح المسؤول
- أخلاقيات البحث الدفاعي

### متطلبات المخرجات
قدم تقريراً تقنياً مفصلاً مع تطبيقات الهجوم واستراتيجيات الدفاع والاعتبارات القانونية.
```

---

## Example Output Preview

```
# Model Extraction Attack Assessment

## Attack Classification Matrix

| Attack Type | Queries Required | Fidelity Achieved | Detection Risk |
|-------------|------------------|-------------------|----------------|
| Equation-solving | O(d) | 100% | High |
| Path-finding | O(2^d) | 100% | Medium |
| Distillation | O(n) | 95% | Low |
| Active Learning | O(log n) | 90% | Low |

## Query Efficiency Analysis
```python
def optimal_query_selection(uncertainty_scores, budget):
    """Select queries maximizing information gain"""
    selected = sorted(uncertainty_scores, 
                     key=lambda x: x.entropy, 
                     reverse=True)[:budget]
    return selected
```

## Defense Effectiveness
| Defense | Fidelity Reduction | Accuracy Impact | Deployment Cost |
|---------|-------------------|-----------------|-----------------|
| Rate Limiting | 15% | 0% | Low |
| Output Rounding | 25% | 2% | Low |
| Noise Injection | 40% | 5% | Medium |
| Watermarking | N/A | 0% | Medium |

## Legal Framework
- Trade Secrets Act: Applicable to model parameters
- Copyright: May protect training data, not learned weights
- DMCA: API terms violation potential
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 3: Membership Inference Attacks

### Description
A comprehensive prompt for analyzing membership inference attacks that determine whether a specific data point was used in training a machine learning model.

### Tags
`membership-inference` `privacy-attacks` `data-protection` `ml-privacy`

---

## 🇬🇧 English Prompt

```
You are a privacy and AI security researcher specializing in membership inference attack analysis.

## Your Task
Provide a comprehensive analysis of membership inference vulnerabilities:

### 1. Attack Overview and Taxonomy
Define and classify membership inference:
- Binary membership inference
- Set membership inference
- Attribute inference attacks
- Property inference attacks
- Distribution inference

### 2. Attack Methodology Analysis
Document primary attack approaches:
- Shadow model training techniques
- Confidence-based inference
- Loss-based membership detection
- Metric-based attacks
- Neural network-based classifiers

### 3. Vulnerability Factors
Analyze what makes models susceptible:
- Model overfitting correlation
- Training data distribution effects
- Model architecture implications
- Regularization impact analysis
- Ensemble model vulnerabilities

### 4. Attack Implementation Framework
Create systematic attack methodology:
- Shadow model training protocol
- Attack classifier training
- Threshold optimization methods
- Evaluation metrics definition
- Cross-model attack transfer

### 5. Privacy Risk Assessment
Quantify privacy implications:
- True positive rate analysis
- False positive rate trade-offs
- Attack advantage metric
- Population-level privacy loss
- Individual privacy risk

### 6. Defense Mechanisms
Evaluate protection strategies:
- Differential privacy implementation
- Regularization techniques
- Model stacking approaches
- Output perturbation methods
- Confidence masking techniques

### 7. Domain-Specific Analysis
Analyze attacks across different domains:
- Medical data membership inference
- Financial record privacy risks
- Image dataset privacy leakage
- Text corpus membership detection
- Graph data privacy attacks

### 8. Regulatory Compliance
Map to privacy regulations:
- GDPR implications (Article 15, 22)
- CCPA privacy requirements
- HIPAA considerations for healthcare
- Industry-specific compliance

### 9. Real-World Attack Scenarios
Document practical attack cases:
1. Healthcare model patient identification
2. Financial service customer inference
3. Social media data leakage
4. Academic dataset privacy
5. Biometric system vulnerabilities

### Output Format
Deliver a comprehensive privacy risk assessment with attack implementations and defense recommendations.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت باحث في الخصوصية وأمن الذكاء الاصطناعي متخصص في تحليل هجمات استدلال العضوية.

## مهمتك
قدم تحليلاً شاملاً لثغرات استدلال العضوية:

### 1. نظرة عامة على الهجوم وتصنيفه
عرّف وصنّف استدلال العضوية:
- استدلال العضوية الثنائي
- استدلال العضوية المجموعاتي
- هجمات استدلال السمات
- هجمات استدلال الخصائص
- استدلال التوزيع

### 2. تحليل منهجية الهجوم
وثّق مناهج الهجوم الأساسية:
- تقنيات تدريب النموذج الظل
- الاستدلال القائم على الثقة
- كشف العضوية القائم على الخسارة
- الهجمات القائمة على المقاييس
- المصنفات القائمة على الشبكات العصبية

### 3. عوامل الثغرة
حلل ما يجعل النماذج عرضة:
- ارتباط فرط التخصيص للنموذج
- آثار توزيع بيانات التدريب
- آثار بنية النموذج
- تحليل أثر التنظيم
- ثغرات نموذج المجموعة

### 4. إطار تنفيذ الهجوم
أنشئ منهجية هجوم منهجية:
- بروتوكول تدريب النموذج الظل
- تدريب مصنف الهجوم
- طرق تحسين العتبة
- تعريف مقاييس التقييم
- نقل الهجوم عبر النماذج

### 5. تقييم مخاطر الخصوصية
حدد آثار الخصوصية:
- تحليل معدل الإيجابية الصحيحة
- المفاضلات في معدل الإيجابية الكاذبة
- مقياس ميزة الهجوم
- فقدان الخصوصية على مستوى السكان
- مخاطر الخصوصية الفردية

### 6. آليات الدفاع
قيّم استراتيجيات الحماية:
- تنفيذ الخصوصية التفاضلية
- تقنيات التنظيم
- مناهج تكديس النماذج
- طرق اضطراب المخرجات
- تقنيات إخفاء الثقة

### 7. التحليل الخاص بالمجال
حلل الهجمات عبر مجالات مختلفة:
- استدلال عضوية البيانات الطبية
- مخاطر خصوصية السجلات المالية
- تسريب خصوصية مجموعات البيانات المصورة
- كشف عضوية المجموعات النصية
- هجمات خصوصية بيانات الرسوم البيانية

### 8. الامتثال التنظيمي
اربط بلوائح الخصوصية:
- آثار GDPR (المادتان 15، 22)
- متطلبات خصوصية CCPA
- اعتبارات HIPAA للرعاية الصحية
- الامتثال الخاص بالقطاع

### 9. سيناريوهات هجوم واقعية
وثّق حالات هجوم عملية:
1. تحديد المرضى في نماذج الرعاية الصحية
2. استدلال عملاء الخدمات المالية
3. تسريب بيانات وسائل التواصل الاجتماعي
4. خصوصية مجموعات البيانات الأكاديمية
5. ثغرات أنظمة القياسات الحيوية

### تنسيق المخرجات
قدم تقييماً شاملاً لمخاطر الخصوصية مع تطبيقات الهجوم وتوصيات الدفاع.
```

---

## Example Output Preview

```
# Membership Inference Attack Assessment

## Attack Performance Matrix

| Model Type | Training Size | Attack Accuracy | AUC Score |
|------------|---------------|-----------------|-----------|
| ResNet-50 | 10K | 87% | 0.92 |
| BERT | 100K | 72% | 0.78 |
| XGBoost | 50K | 81% | 0.85 |
| MLP | 20K | 89% | 0.94 |

## Shadow Model Methodology
```python
class MembershipInferenceAttack:
    def __init__(self, target_model, shadow_models):
        self.target = target_model
        self.shadows = shadow_models
        self.attack_classifier = train_attack_model(shadow_models)
    
    def infer(self, sample, output):
        features = extract_features(output)
        return self.attack_classifier.predict(features)
```

## Privacy Risk Scoring
- High Risk: AUC > 0.85 (immediate remediation)
- Medium Risk: AUC 0.65-0.85 (monitoring required)
- Low Risk: AUC < 0.65 (acceptable)

## Defense Effectiveness
| Defense | AUC Reduction | Utility Loss |
|---------|---------------|--------------|
| DP (ε=1) | 0.35 | 5% |
| L2 Reg | 0.15 | 1% |
| Output Noise | 0.20 | 3% |

## GDPR Compliance Check
- [ ] Data minimization implemented
- [ ] Privacy impact assessment completed
- [ ] User consent for training data
- [ ] Right to erasure mechanism
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 4: Model Inversion Attacks

### Description
An advanced prompt for analyzing model inversion attacks that reconstruct training data or extract sensitive information from trained machine learning models.

### Tags
`model-inversion` `privacy-leakage` `training-data-extraction` `reconstruction-attacks`

---

## 🇬🇧 English Prompt

```
You are an AI security researcher specializing in model inversion and training data extraction attacks.

## Your Task
Conduct a comprehensive analysis of model inversion attack methodologies:

### 1. Attack Definition and Taxonomy
Classify model inversion attack types:
- Gradient-based inversion
- Confidence-based reconstruction
- GAN-assisted inversion
- Optimization-based attacks
- Feature reconstruction attacks

### 2. Theoretical Foundations
Analyze the mathematical basis:
- Information leakage from model outputs
- Confidence score exploitation
- Gradient information utilization
- Prior knowledge incorporation
- Optimization landscape analysis

### 3. Attack Implementation Methods
Document detailed attack approaches:
- White-box gradient inversion
- Black-box confidence inversion
- Active learning-based extraction
- Model API exploitation
- Side-channel information utilization

### 4. Neural Network Inversion
Focus on deep learning models:
- Layer-wise feature inversion
- Activation maximization techniques
- DeepDream-style reconstruction
- Intermediate representation extraction
- Feature space navigation

### 5. Privacy-Sensitive Data Recovery
Analyze reconstruction of:
- Facial image reconstruction
- Text data extraction
- Medical image recovery
- Financial data reconstruction
- Biometric template extraction

### 6. Attack Enhancement Techniques
Document optimization methods:
- Prior-based regularization
- GAN-based refinement
- Ensemble inversion approaches
- Multi-query optimization
- Auxiliary data exploitation

### 7. Vulnerability Assessment Framework
Develop evaluation methodology:
- Reconstruction quality metrics
- Semantic similarity evaluation
- Privacy loss quantification
- Attack success criteria
- Cross-model vulnerability comparison

### 8. Defense Mechanisms
Evaluate protection strategies:
- Differential privacy integration
- Output perturbation techniques
- Model architecture modifications
- Training data augmentation
- Confidence score manipulation

### 9. Real-World Attack Scenarios
Analyze practical inversion cases:
1. Face recognition model inversion
2. Medical diagnosis data extraction
3. Speech recognition inversion
4. Text model training data leakage
5. Recommendation system user profiling

### 10. Legal and Ethical Implications
Address regulatory concerns:
- Privacy law violations
- Biometric data protection
- Healthcare data regulations
- Responsible disclosure requirements

### Output Requirements
Provide a detailed technical analysis with reconstruction examples and defense recommendations.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت باحث في أمن الذكاء الاصطناعي متخصص في هجمات عكس النموذج واستخراج بيانات التدريب.

## مهمتك
أجرِ تحليلاً شاملاً لمنهجيات هجوم عكس النموذج:

### 1. تعريف الهجوم وتصنيفه
صنّف أنواع هجمات عكس النموذج:
- العكس القائم على التدرج
- إعادة البناء القائمة على الثقة
- العكس بمساعدة GAN
- الهجمات القائمة على التحسين
- هجمات إعادة بناء الميزات

### 2. الأسس النظرية
حلل الأساس الرياضي:
- تسريب المعلومات من مخرجات النموذج
- استغلال درجات الثقة
- استخدام معلومات التدرج
- دمج المعرفة المسبقة
- تحليل مشهد التحسين

### 3. طرق تنفيذ الهجوم
وثّق مناهج الهجوم المفصلة:
- عكس التدرج للصندوق الأبيض
- عكس الثقة للصندوق الأسود
- الاستخراج القائم على التعلم النشط
- استغلال API النموذج
- استخدام معلومات القناة الجانبية

### 4. عكس الشبكات العصبية
ركز على نماذج التعلم العميق:
- عكس الميزات طبقة تلو طبقة
- تقنيات تعظيم التنشيط
- إعادة البناء على طراز DeepDream
- استخراج التمثيل الوسيط
- التنقل في فضاء الميزات

### 5. استرداد البيانات الحساسة للخصوصية
حلل إعادة بناء:
- إعادة بناء صور الوجه
- استخراج البيانات النصية
- استرداد الصور الطبية
- إعادة بناء البيانات المالية
- استخراج قوالب القياسات الحيوية

### 6. تقنيات تعزيز الهجوم
وثّق طرق التحسين:
- التنظيم القائم على المسبق
- التنقيح القائم على GAN
- مناهج العكس الجماعية
- تحسين الاستعلامات المتعددة
- استغلال البيانات المساعدة

### 7. إطار تقييم الثغرات
طوّر منهجية التقييم:
- مقاييس جودة إعادة البناء
- تقييم التشابه الدلالي
- تحديد كمية فقدان الخصوصية
- معايير نجاح الهجوم
- مقارنة الثغرات عبر النماذج

### 8. آليات الدفاع
قيّم استراتيجيات الحماية:
- تكامل الخصوصية التفاضلية
- تقنيات اضطراب المخرجات
- تعديلات بنية النموذج
- تعزيز بيانات التدريب
- التلاعب بدرجات الثقة

### 9. سيناريوهات هجوم واقعية
حلل حالات العكس العملية:
1. عكس نموذج التعرف على الوجوه
2. استخراج بيانات التشخيص الطبي
3. عكس التعرف على الكلام
4. تسريب بيانات تدريب النموذج النصي
5. بناء ملفات المستخدمين في أنظمة التوصية

### 10. الآثار القانونية والأخلاقية
عالج المخاوف التنظيمية:
- انتهاكات قوانين الخصوصية
- حماية البيانات الحيوية
- لوائح بيانات الرعاية الصحية
- متطلبات الإفصاح المسؤول

### متطلبات المخرجات
قدم تحليلاً تقنياً مفصلاً مع أمثلة إعادة البناء وتوصيات الدفاع.
```

---

## Example Output Preview

```
# Model Inversion Attack Assessment

## Attack Success Rates by Data Type

| Data Type | Reconstruction Quality | Privacy Risk |
|-----------|----------------------|--------------|
| Face Images | 85% SSIM | Critical |
| Medical Images | 72% SSIM | Critical |
| Text Data | 65% BLEU | High |
| Tabular Data | 78% Accuracy | High |

## Gradient Inversion Implementation
```python
def gradient_inversion(model, target_gradient, iterations=1000):
    reconstructed = initialize_random_input()
    for i in range(iterations):
        gradient = compute_gradient(model, reconstructed)
        loss = mse_loss(gradient, target_gradient)
        reconstructed = optimize(reconstructed, loss)
    return reconstructed
```

## Defense Effectiveness Analysis
| Defense | SSIM Reduction | Accuracy Impact |
|---------|----------------|-----------------|
| DP (ε=0.1) | 45% | 12% |
| Noise σ=0.1 | 35% | 5% |
| Top-k Outputs | 25% | 3% |

## Privacy Risk Matrix
- Critical: Face/Biometric models with >80% reconstruction
- High: Medical/Financial models with >60% reconstruction
- Medium: General models with 40-60% reconstruction
- Low: Models with <40% reconstruction

## Legal Compliance Status
- Biometric Data: GDPR Article 9 violation risk
- Healthcare: HIPAA breach potential
- Cross-border: Data transfer implications
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 5: Adversarial Attack Detection and Defense

### Description
A comprehensive prompt for designing and implementing robust detection mechanisms and defense strategies against adversarial attacks in machine learning systems.

### Tags
`adversarial-defense` `detection` `robustness` `ml-security-hardening`

---

## 🇬🇧 English Prompt

```
You are a senior ML security architect specializing in adversarial defense and detection system design.

## Your Task
Design a comprehensive adversarial attack detection and defense framework:

### 1. Detection Methodology Framework
Create multi-layered detection systems:
- Statistical anomaly detection
- Model-based detection classifiers
- Input distribution analysis
- Reconstruction error detection
- Ensemble detection methods

### 2. Adversarial Training Strategies
Implement robust training approaches:
- PGD adversarial training
- TRADES training methodology
- Ensemble adversarial training
- Feature denoising approaches
- Adversarial logit pairing

### 3. Input Transformation Defenses
Design preprocessing defenses:
- JPEG compression defense
- Bit-depth reduction
- Input quantization methods
- Spatial smoothing techniques
- Randomization-based defenses

### 4. Certified Defense Mechanisms
Implement provable robustness:
- Randomized smoothing
- Interval bound propagation
- Convex relaxation methods
- Certified training approaches
- Formal verification integration

### 5. Runtime Detection Systems
Build production-ready detection:
- Confidence threshold monitoring
- Gradient norm analysis
- Feature space density estimation
- Subspace detection methods
- Real-time alerting systems

### 6. Defense Evaluation Framework
Establish comprehensive testing:
- AutoAttack benchmark evaluation
- Adaptive attack testing
- Transfer attack assessment
- Clean accuracy preservation
- Computational overhead analysis

### 7. Model Hardening Techniques
Apply architectural improvements:
- Robust architecture design
- Defense-aware training
- Ensemble diversity optimization
- Gradient masking avoidance
- Feature robustness enhancement

### 8. Production Deployment Considerations
Address operational challenges:
- Detection-defense pipeline integration
- Performance overhead management
- False positive mitigation
- Model update strategies
- Monitoring and alerting systems

### 9. Defense Against Specific Attacks
Target high-risk attack vectors:
- PGD attack defense strategies
- C&W attack mitigation
- AutoAttack resilience
- Transfer attack prevention
- Black-box attack defense

### 10. Continuous Security Assessment
Establish ongoing evaluation:
- Red team testing integration
- Automated attack generation
- Defense degradation monitoring
- Model drift detection
- Security update procedures

### Output Requirements
Deliver a complete defense architecture with implementation guides, code samples, and evaluation procedures.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت مهندس أمن تعلم آلي أول متخصص في تصميم الدفاع الخصومي وأنظمة الكشف.

## مهمتك
صمّم إطاراً شاملاً للكشف عن الهجمات الخصومية والدفاع ضدها:

### 1. إطار منهجية الكشف
أنشئ أنظمة كشف متعددة الطبقات:
- كشف الشذوذ الإحصائي
- مصنفات الكشف القائمة على النموذج
- تحليل توزيع المدخلات
- كشف خطأ إعادة البناء
- طرق الكشف الجماعية

### 2. استراتيجيات التدريب الخصومي
طبّق مناهج تدريب متينة:
- التدريب الخصومي PGD
- منهجية تدريب TRADES
- التدريب الخصومي الجماعي
- مناهج إزالة ضجيج الميزات
- اقتران اللوجيت الخصومي

### 3. دفاعات تحويل المدخلات
صمّم دفاعات المعالجة المسبقة:
- دفاع ضغط JPEG
- تقليل عمق البت
- طرق تقدير المدخلات
- تقنيات التمهيد المكاني
- الدفاعات القائمة على العشوائية

### 4. آليات الدفاع المعتمدة
طبّق المتانة المثبتة:
- التمهيد العشوائي
- انتشار حدود الفاصل
- طرق الاسترخاء المحدب
- مناهج التدريب المعتمد
- تكامل التحقق الرسمي

### 5. أنظمة الكشف في وقت التشغيل
ابنِ كشف جاهز للإنتاج:
- مراقبة عتبة الثقة
- تحليل معيار التدرج
- تقدير كثافة فضاء الميزات
- طرق الكشف في الفضاء الفرعي
- أنظمة التنبيه في الوقت الحقيقي

### 6. إطار تقييم الدفاع
أنشئ اختباراً شاملاً:
- تقييم معيار AutoAttack
- اختبار الهجوم التكيفي
- تقييم هجوم النقل
- الحفاظ على دقة البيانات النظيفة
- تحليل الحمل الحسابي

### 7. تقنيات تحصين النموذج
طبّق التحسينات المعمارية:
- تصميم بنية متينة
- تدريب واعي للدفاع
- تحسين تنوع المجموعات
- تجنب إخفاء التدرج
- تعزيز متانة الميزات

### 8. اعتبارات نشر الإنتاج
عالج التحديات التشغيلية:
- تكامل خط أنابيب الكشف-الدفاع
- إدارة الحمل الزائد للأداء
- معالجة الإيجابيات الكاذبة
- استراتيجيات تحديث النموذج
- أنظمة المراقبة والتنبيه

### 9. الدفاع ضد هجمات محددة
استهدف نواقل هجوم عالية المخاطر:
- استراتيجيات دفاع هجوم PGD
- معالجة هجوم C&W
- مقاومة AutoAttack
- منع هجوم النقل
- دفاع هجوم الصندوق الأسود

### 10. التقييم الأمني المستمر
أنشئ تقييماً مستمراً:
- تكامل اختبار الفريق الأحمر
- توليد هجوم آلي
- مراقبة تدهور الدفاع
- كشف انحراف النموذج
- إجراءات تحديث الأمان

### متطلبات المخرجات
قدم بنية دفاع كاملة مع أدلة التنفيذ وأمثلة برمجية وإجراءات التقييم.
```

---

## Example Output Preview

```
# Adversarial Defense Framework

## Detection Layer Architecture
[Multi-layer detection diagram]

## Layer 1: Statistical Detection
```python
def statistical_anomaly_detection(input_sample, threshold=3.0):
    features = extract_features(input_sample)
    z_scores = (features - mean) / std
    return np.any(np.abs(z_scores) > threshold)
```

## Layer 2: Adversarial Training
```python
def pgd_adversarial_train(model, x, y, epsilon=0.03, alpha=0.01, steps=10):
    x_adv = x.clone()
    for _ in range(steps):
        x_adv.requires_grad = True
        loss = criterion(model(x_adv), y)
        x_adv = x_adv + alpha * x_adv.grad.sign()
        x_adv = clamp(x_adv, x - epsilon, x + epsilon)
    return model(x_adv)
```

## Defense Evaluation Results

| Defense | Clean Acc | PGD-20 | AutoAttack | Overhead |
|---------|-----------|--------|------------|----------|
| Standard | 95.2% | 0.0% | 0.0% | 0ms |
| PGD Train | 87.5% | 45.2% | 42.1% | 15ms |
| TRADES | 84.3% | 53.8% | 51.2% | 12ms |
| Randomized Smoothing | 81.2% | 48.5% | 47.8% | 45ms |

## Production Deployment Checklist
- [ ] Detection threshold calibrated
- [ ] False positive rate < 1%
- [ ] Response time < 50ms
- [ ] Monitoring dashboards active
- [ ] Incident response procedures documented
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
- [NIST AI Risk Management Framework](https://www.nist.gov/itl/ai-risk-management-framework)
- [CleverHans Attack Library](https://github.com/cleverhans-lab/cleverhans)
- [Adversarial Robustness Toolbox (ART)](https://github.com/Trusted-AI/adversarial-robustness-toolbox)

---

*Last Updated: 2024*
*Version: 1.0*
