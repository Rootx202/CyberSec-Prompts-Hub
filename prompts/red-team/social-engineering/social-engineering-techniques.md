# Social Engineering Techniques - Red Team Prompts

This document contains 5 detailed bilingual (English/Arabic) prompts for authorized red team social engineering assessments.

---

## Prompt 1: Phishing Campaign Planning

### Description
A comprehensive prompt for designing authorized phishing simulation campaigns to test organizational security awareness and incident response capabilities.

### Tags
`phishing` `simulation` `awareness-testing` `email-security`

---

## 🇬🇧 English Prompt

```
You are a certified red team operator conducting an authorized phishing simulation for a client organization. Design a comprehensive phishing campaign framework that includes:

**Campaign Objectives:**
- Define measurable goals (click rates, credential capture rates, reporting rates)
- Establish success criteria and key performance indicators
- Document scope limitations and boundaries

**Target Audience Analysis:**
- Identify high-risk departments and roles
- Analyze communication patterns and trusted sender relationships
- Map potential psychological triggers and urgency factors

**Email Craftsmanship:**
- Develop 3 realistic lure scenarios (e.g., IT support, HR notification, vendor update)
- Create subject lines with appropriate urgency without triggering spam filters
- Design email body content that passes technical and visual inspection
- Include placeholder tracking mechanisms

**Landing Page Development:**
- Design credential capture pages that mirror legitimate services
- Implement detection evasion techniques for security awareness training
- Create realistic form fields and error handling

**Technical Infrastructure:**
- Recommend email delivery infrastructure requirements
- Suggest domain selection and DMARC/DKIM/SPF considerations
- Outline tracking and analytics implementation

**Ethical Considerations & Defensive Measures:**
- Document proper authorization and legal requirements
- Include immediate remediation steps for compromised credentials
- Provide recommendations for improving organizational phishing defenses
- Suggest security awareness training enhancements based on results

**Reporting Template:**
- Executive summary format
- Technical findings breakdown
- Metrics and comparison with industry benchmarks

Ensure all recommendations align with PTES (Penetration Testing Execution Standard) and NIST SP 800-115 guidelines.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت مشغل فريق أحمر معتمد تقوم بإجراء محاكاة تصيد احتيالية مصرح بها لمنظمة عميل. صمم إطار حملة تصيد شامل يتضمن:

**أهداف الحملة:**
- تحديد أهداف قابلة للقياس (معدلات النقر، معدلات التقاط بيانات الاعتماد، معدلات الإبلاغ)
-确立 معايير النجاح ومؤشرات الأداء الرئيسية
- توثيق حدود النطاق والقيود

**تحليل الجمهور المستهدف:**
- تحديد الأقسام والأدوار عالية المخاطر
- تحليل أنماط الاتصال وعلاقات المرسلين الموثوقين
- رسم محفزات نفسية محتملة وعوامل الاستعجال

**صناعة رسائل البريد الإلكتروني:**
- تطوير 3 سيناريوهات طعم واقعية (مثل: دعم تقني، إشعار موارد بشرية، تحديث مورد)
- إنشاء سطور موضوع بدرجة استعجال مناسبة دون تفعيل فلاتر البريد المزعج
- تصميم محتوى نص البريد الذي يجتاز الفحص الفني والبصري
- تضمين آليات تتبع نائبة

**تطوير صفحة الهبوط:**
- تصميم صفحات التقاط بيانات الاعتماد التي تحاكي الخدمات الشرعية
- تنفيذ تقنيات التهرب من الكشف لتدريب الوعي الأمني
- إنشاء حقول نموذج واقعية ومعالجة الأخطاء

**البنية التحتية التقنية:**
- توصية بمتطلبات بنية تحتية لتوصيل البريد الإلكتروني
- اقتراح اعتبارات اختيار النطاق و DMARC/DKIM/SPF
- توضيح تنفيذ التتبع والتحليلات

**الاعتبارات الأخلاقية والتدابير الدفاعية:**
- توثيق الترخيص المناسب والمتطلبات القانونية
- تضمين خطوات المعالجة الفورية لبيانات الاعتماد المخترقة
- تقديم توصيات لتحسين دفاعات التصيد التنظيمية
- اقتراح تحسينات تدريب الوعي الأمني بناءً على النتائج

**قالب إعداد التقارير:**
- تنسيق ملخص تنفيذي
- تفصيل النتائج التقنية
- المقاييس والمقارنة مع معايير الصناعة

تأكد من توافق جميع التوصيات مع معيار تنفيذ اختبار الاختراق (PTES) وإرشادات NIST SP 800-115.
```

---

## Example Output Preview

```
# Phishing Campaign Framework - ABC Corporation

## Campaign Objectives
- Target click rate: <15% (industry benchmark: 20-25%)
- Credential capture rate: <5%
- Reporting rate: >70% within 2 hours

## Lure Scenarios
1. IT Support: "Urgent: Password Expiration Notice"
2. HR Notification: "Updated Benefits Enrollment"
3. Vendor Update: "Invoice Payment Confirmation"

## Recommended Defenses
- Implement DMARC with p=reject policy
- Deploy advanced email gateway with ML-based detection
- Conduct quarterly phishing simulations with progressive difficulty
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 2: Pretexting Scenarios

### Description
A detailed prompt for developing realistic pretexting scenarios to test an organization's vulnerability to social engineering attacks through fabricated situations and impersonation.

### Tags
`pretexting` `impersonation` `social-engineering` `red-team`

---

## 🇬🇧 English Prompt

```
You are an authorized social engineering assessor developing pretexting scenarios for a controlled engagement. Create a comprehensive pretexting framework covering:

**Scenario Development Methodology:**
- Research-based approach to understanding organizational context
- Identification of trusted entities and authority figures
- Analysis of communication channels and verification procedures

**Pretexting Categories:**
1. **Authority-Based Pretexting:**
   - IT administrator conducting "emergency maintenance"
   - Executive requiring urgent assistance
   - Compliance officer performing audit verification

2. **Urgency-Based Pretexting:**
   - Time-sensitive business transaction
   - System outage requiring immediate action
   - Legal or regulatory deadline pressure

3. **Helpfulness-Based Pretexting:**
   - Technical support offering assistance
   - Vendor providing service updates
   - Colleague requesting collaboration

**Character Development:**
- Create detailed backstories with verifiable details
- Develop communication style guides for each persona
- Document potential inconsistencies to avoid

**Information Gathering Techniques:**
- OSINT sources for organizational intelligence
- LinkedIn and professional network analysis
- Public records and regulatory filings review
- Social media reconnaissance methodology

**Communication Scripts:**
- Phone conversation frameworks with branching logic
- Email correspondence templates
- In-person interaction guidelines

**Verification Bypass Techniques:**
- Common organizational weaknesses in identity verification
- Methods to establish quick credibility
- Handling challenging questions and callbacks

**Ethical Considerations & Defensive Measures:**
- Authorization documentation requirements
- Legal boundaries and prohibited actions
- Immediate disclosure protocols if genuine harm detected
- Organizational controls to prevent pretexting attacks
- Employee verification training recommendations
- Multi-channel confirmation procedures

**Documentation Standards:**
- Evidence collection methodology
- Recording and logging procedures (where legally permitted)
- Post-engagement disclosure requirements
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت مقيم هندسة اجتماعية مصرح له تقوم بتطوير سيناريوهات الذرائع لعملية خاضعة للرقابة. أنشئ إطار عمل شامل للذرائع يغطي:

**منهجية تطوير السيناريو:**
- نهج قائم على البحث لفهم السياق التنظيمي
- تحديد الكيانات الموثوقة وشخصيات السلطة
- تحليل قنوات الاتصال وإجراءات التحقق

**فئات الذرائع:**
1. **ذرائع قائمة على السلطة:**
   - مسؤول تقني يقوم بـ "صيانة طارئة"
   - تنفيذي يحتاج مساعدة عاجلة
   - مسؤول امتثال يقوم بالتحقق من التدقيق

2. **ذرائع قائمة على الاستعجال:**
   - معاملة تجارية حساسة للوقت
   - انقطاع النظام يتطلب إجراءً فوريًا
   - ضغط موعد قانوني أو تنظيمي

3. **ذرائع قائمة على المساعدة:**
   - دعم تقني يعرض المساعدة
   - مورد يقدم تحديثات الخدمة
   - زميل يطلب التعاون

**تطوير الشخصية:**
- إنشاء قصص خلفية مفصلة بتفاصيل قابلة للتحقق
- تطوير أدلة أسلوب الاتصال لكل شخصية
- توثيق التناقضات المحتملة التي يجب تجنبها

**تقنيات جمع المعلومات:**
- مصادر OSINT للاستخبارات التنظيمية
- تحليل LinkedIn وشبكة المحترفين
- مراجعة السجلات العامة والإيداعات التنظيمية
- منهجية استطلاع وسائل التواصل الاجتماعي

**نصوص الاتصال:**
- أطر المحادثات الهاتفية بمنطق متفرع
- قوالب مراسلات البريد الإلكتروني
- إرشادات التفاعل الشخصي

**تقنيات تجاوز التحقق:**
- نقاط الضعف التنظيمية الشائعة في التحقق من الهوية
- طرق إنشاء مصداقية سريعة
- التعامل مع الأسئلة الصعبة وعمليات إعادة الاتصال

**الاعتبارات الأخلاقية والتدابير الدفاعية:**
- متطلبات توثيق الترخيص
- الحدود القانونية والإجراءات المحظورة
- بروتوكولات الإفصاح الفوري إذا تم اكتشاف ضرر حقيقي
- الضوابط التنظيمية لمنع هجمات الذرائع
- توصيات تدريب التحقق للموظفين
- إجراءات التأكيد متعددة القنوات

**معايير التوثيق:**
- منهجية جمع الأدلة
- إجراءات التسجيل والتوثيق (حيثما يسمح القانون)
- متطلبات الإفصاح بعد العملية
```

---

## Example Output Preview

```
# Pretexting Scenario: IT Emergency Maintenance

## Persona Profile
- Name: Michael Chen, Senior Systems Administrator
- Department: IT Infrastructure
- Tenure: 5 years (fabricated based on org research)
- Communication Style: Technical, urgent but professional

## Script Framework
"Hi [Target], this is Michael from IT Infrastructure. We're experiencing 
an issue with the authentication server that's affecting remote access. 
I need to verify your credentials are properly synced before we apply 
the emergency patch. Can you confirm you're able to access your email?"

## Red Flags for Training
- Unscheduled maintenance calls should be verified
- Legitimate IT staff never ask for credentials
- Always call back using official numbers
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 3: Vishing (Voice Phishing) Techniques

### Description
A comprehensive prompt for planning and executing authorized vishing assessments to test voice-based social engineering vulnerabilities.

### Tags
`vishing` `voice-phishing` `phone-security` `social-engineering`

---

## 🇬🇧 English Prompt

```
You are an authorized red team operator planning a vishing (voice phishing) assessment. Develop a comprehensive vishing testing framework including:

**Pre-Engagement Requirements:**
- Legal authorization documentation
- Call recording consent requirements by jurisdiction
- Scope boundaries and prohibited targets
- Callback verification procedures

**Target Reconnaissance:**
- Phone number enumeration techniques
- Organizational directory mapping
- Help desk and support line analysis
- Executive assistant identification

**Vishing Attack Vectors:**
1. **Help Desk Impersonation:**
   - Password reset request scenarios
   - Account verification calls
   - Technical support fraud

2. **Authority Figure Impersonation:**
   - Executive urgent request
   - Legal department inquiry
   - Compliance audit call

3. **Vendor/Partner Impersonation:**
   - Service provider verification
   - Contract renewal discussion
   - Technical integration support

**Call Script Development:**
- Opening statements that establish credibility
- Question sequences with clear objectives
- Objection handling and redirection techniques
- Natural conversation flow patterns
- Exit strategies for various scenarios

**Voice and Delivery Techniques:**
- Tone and pacing considerations
- Professional terminology usage
- Background noise and environment simulation
- Accent and language considerations

**Information Extraction Methods:**
- Gradual information gathering approach
- Confirmation and verification tactics
- Creating false sense of urgency
- Leveraging reciprocity principles

**Technical Considerations:**
- Caller ID spoofing (where legally permitted)
- VoIP and call routing infrastructure
- Call recording and logging setup
- Counter-surveillance awareness

**Ethical Considerations & Defensive Measures:**
- Prohibition on threats or intimidation
- Limits on information requested
- Immediate callback requirements for sensitive requests
- Organizational vishing defense protocols
- Employee verification training programs
- Technical controls (call authentication, STIR/SHAKEN)

**Post-Assessment Activities:**
- Evidence documentation and chain of custody
- Target notification and debriefing procedures
- Success metrics and analysis
- Recommendations for voice security improvements
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت مشغل فريق أحمر مصرح له تخطط لتقييم الفيشينغ (التصيد الصوتي). طور إطار اختبار فيشينغ شامل يتضمن:

**متطلبات ما قبل العملية:**
- وثائق الترخيص القانوني
- متطلبات موافقة تسجيل المكالمات حسب الولاية القضائية
- حدود النطاق والأهداف المحظورة
- إجراءات التحقق من إعادة الاتصال

**استطلاع الهدف:**
- تقنيات تعداد أرقام الهواتف
- رسم خريطة الدليل التنظيمي
- تحليل خطوط المساعدة والدعم
- تحديد مساعدي التنفيذيين

**متجهات هجوم الفيشينغ:**
1. **انتحال شخصية مكتب المساعدة:**
   - سيناريوهات طلب إعادة تعيين كلمة المرور
   - مكالمات التحقق من الحساب
   - احتيال الدعم التقني

2. **انتحال شخصية شخصية ذات سلطة:**
   - طلب تنفيذي عاجل
   - استفسار قسم الشؤون القانونية
   - مكالمة تدقيق الامتثال

3. **انتحال شخصية مورد/شريك:**
   - التحقق من مزود الخدمة
   - مناقشة تجديد العقد
   - دعم التكامل التقني

**تطوير نص المكالمة:**
- تصريحات افتتاحية تؤسس المصداقية
- تسلسلات أسئلة بأهداف واضحة
- تقنيات التعامل مع الاعتراضات وإعادة التوجيه
- أنماط تدفق المحادثة الطبيعية
- استراتيجيات الخروج لمختلف السيناريوهات

**تقنيات الصوت والتسليم:**
- اعتبارات النبرة والإيقاع
- استخدام المصطلحات المهنية
- محاكاة الضوضاء المحيطة والبيئة
- اعتبارات اللهجة واللغة

**طرق استخراج المعلومات:**
- نهج جمع المعلومات التدريجي
- تكتيكات التأكيد والتحقق
- خلق شعور زائف بالاستعجال
- الاستفادة من مبادئ المعاملة بالمثل

**الاعتبارات التقنية:**
- تزييف معرف المتصل (حيثما يسمح القانون)
- البنية التحتية للـ VoIP وتوجيه المكالمات
- إعداد تسجيل المكالمات وتسجيلها
- الوعي بالمراقبة المضادة

**الاعتبارات الأخلاقية والتدابير الدفاعية:**
- حظر التهديد أو الترهيب
- حدود المعلومات المطلوبة
- متطلبات إعادة الاتصال الفورية للطلبات الحساسة
- بروتوكولات الدفاع التنظيمية ضد الفيشينغ
- برامج تدريب التحقق للموظفين
- الضوابط التقنية (مصادقة المكالمات، STIR/SHAKEN)

**أنشطة ما بعد التقييم:**
- توثيق الأدلة وسلسلة الحيازة
- إجراءات إخطار الهدف وإحاطته
- مقاييس النجاح والتحليل
- توصيات لتحسين أمن الصوت
```

---

## Example Output Preview

```
# Vishing Assessment - Technical Support Scenario

## Pre-Call Preparation
- Target: IT Help Desk (x4355)
- Cover Story: Remote employee with VPN issues
- Objective: Obtain VPN configuration credentials

## Call Script Flow
[Opening] "Hi, this is Sarah from Marketing. I'm working remotely 
and can't connect to the VPN. I have a client presentation in 30 
minutes and really need help getting connected quickly."

[Building Rapport] "I know you guys are probably swamped. I really 
appreciate you helping me out here. What information do you need?"

[Objective Pursuit] "Okay, so I need to use the mobile token? 
Can you walk me through the setup? I have the serial number from 
my laptop sticker ready..."

## Defensive Measures Identified
- Implement callback verification for all password resets
- Deploy STIR/SHAKEN caller ID authentication
- Create verification code system for IT support calls
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 4: Physical Social Engineering

### Description
A detailed prompt for planning authorized physical social engineering assessments to test an organization's physical security controls and employee vigilance.

### Tags
`physical-security` `tailgating` `impersonation` `facility-access`

---

## 🇬🇧 English Prompt

```
You are a certified physical security assessor conducting an authorized social engineering engagement. Design a comprehensive physical social engineering assessment framework:

**Pre-Assessment Planning:**
- Site reconnaissance methodology (perimeter, entrances, smoking areas)
- Building access point identification
- Security personnel observation protocols
- Badge and access control system analysis
- Camera and surveillance mapping

**Attack Methodologies:**

1. **Tailgating/Piggybacking:**
   - Timing analysis for optimal approach
   - Target selection criteria (helpful employees, distracted personnel)
   - Social scripts for gaining entry
   - Props and visual cues (heavy boxes, lanyards, clipboards)

2. **Impersonation Scenarios:**
   - Delivery personnel (food, packages, equipment)
   - Maintenance/contractor worker
   - IT support technician
   - Vendor or partner visitor
   - Interview candidate

3. **Access Control Manipulation:**
   - Held door exploitation
   - Emergency exit abuse
   - Loading dock infiltration
   - Conference room access

4. **Badge and Credential Attacks:**
   - Visual badge cloning opportunities
   - Social engineering badge acquisition
   - Visitor pass manipulation

**Prop and Equipment Preparation:**
- Realistic uniforms and attire selection
- Props that support cover story
- Hidden recording devices (where legally permitted)
- Emergency exit tools and considerations

**Behavioral Techniques:**
- Confidence and posture projection
- Busy professional appearance
- Familiarity with facility operations
- Handling security challenges

**Target Employee Analysis:**
- Identifying high-risk personnel behaviors
- Common cognitive biases to exploit
- Department-specific vulnerabilities
- Shift change exploitation windows

**Ethical Considerations & Defensive Measures:**
- Never bypass active intrusion alarms
- Legal limitations on forced entry
- Prohibition on damaging property
- Immediate surrender if confronted
- Physical security control recommendations
- Employee awareness training content
- Access control hardening measures
- Visitor management improvements

**Documentation Requirements:**
- Photographic evidence guidelines
- Timestamp and location logging
- Witness interaction notes
- Security control effectiveness assessment

**Post-Assessment Reporting:**
- Executive vulnerability summary
- Technical findings with evidence
- Remediation prioritization matrix
- ROI analysis for security improvements
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت مقيم أمن مادي معتمد تقوم بإجراء عملية هندسة اجتماعية مصرح بها. صمم إطار تقييم هندسة اجتماعية مادية شامل:

**تخطيط ما قبل التقييم:**
- منهجية استطلاع الموقع (المحيط، المداخل، مناطق التدخين)
- تحديد نقاط الوصول إلى المبنى
- بروتوكولات مراقبة أفراد الأمن
- تحليل نظام الشارات والتحكم في الوصول
- رسم خريطة الكاميرات والمراقبة

**منهجيات الهجوم:**

1. **التسلل/الركوب:**
   - تحليل التوقيت للنهج الأمثل
   - معايير اختيار الهدف (موظفون متعاونون، موظفون مشتتون)
   - نصوص اجتماعية لدخول
   - الدعائم والإشارات البصرية (صناديق ثقيلة، بطاقات عنق، حافظات أوراق)

2. **سيناريوهات انتحال الشخصية:**
   - موظفو التوصيل (طعام، طرود، معدات)
   - عامل صيانة/مقاول
   - فني دعم تقني
   - زائر مورد أو شريك
   - مرشح مقابلة

3. **التلاعب بوسائل التحكم في الوصول:**
   - استغلال الأبواب المفتوكة
   - إساءة استخدام مخرج الطوارئ
   - التسلل عبر رصيف التحميل
   - الوصول إلى قاعة الاجتماعات

4. **هجمات الشارات وبيانات الاعتماد:**
   - فرص استنساخ الشارات البصرية
   - الحصول على شارة الهندسة الاجتماعية
   - التلاعب بتصريح الزائر

**إعداد الدعائم والمعدات:**
- اختيار الزي الرسمي والملابس الواقعية
- الدعائم التي تدعم القصة الغلافية
- أجهزة التسجيل المخفية (حيثما يسمح القانون)
- أدوات مخرج الطوارئ والاعتبارات

**التقنيات السلوكية:**
- إسقاط الثقة والوقفة
- مظهر المهني المشغول
- المعرفة بعمليات المنشأة
- التعامل مع التحديات الأمنية

**تحليل الموظفين المستهدفين:**
- تحديد سلوكيات الموظفين عالية المخاطر
- التحيزات المعرفية الشائعة للاستغلال
- نقاط الضعف الخاصة بكل قسم
- نوافذ استغلال تغيير الوردية

**الاعتبارات الأخلاقية والتدابير الدفاعية:**
- عدم تجاوز أجهزة إنذار الاقتحام النشطة
- القيود القانونية على الدخول القسري
- حظر إتلاف الممتلكات
- الاستسلام الفوري عند المواجهة
- توصيات ضوابط الأمن المادي
- محتوى تدريب الوعي للموظفين
- تدابير تقوية التحكم في الوصول
- تحسينات إدارة الزوار

**متطلبات التوثيق:**
- إرشادات الأدلة الفوتوغرافية
- تسجيل الطابع الزمني والموقع
- ملاحظات تفاعل الشهود
- تقييم فعالية الضوابط الأمنية

**إعداد التقارير بعد التقييم:**
- ملخص الثغرات التنفيذي
- النتائج التقنية مع الأدلة
- مصفوفة أولويات المعالجة
- تحليل العائد على الاستثمار لتحسينات الأمان
```

---

## Example Output Preview

```
# Physical Security Assessment - ACME Headquarters

## Assessment Summary
- Date: [REDACTED]
- Location: Main Campus, Building A
- Assessment Type: Tailgating & Impersonation

## Findings

### Tailgating Test
- Attempts: 5
- Successful Entry: 4 (80%)
- Challenge Rate: 20%

### Impersonation Results
| Scenario          | Access Level | Notes                          |
|-------------------|--------------|--------------------------------|
| IT Support        | Full floor   | No badge verification required |
| Delivery          | Reception    | Escorted after 2 min wait      |
| Maintenance       | Server room  | Badge given without ID check   |

## Recommendations
1. Implement mandatory badge check at all entrances
2. Install anti-tailgating turnstiles at main lobby
3. Deploy security awareness training for reception staff
4. Implement visitor escort policy enforcement
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 5: Security Awareness Testing

### Description
A comprehensive prompt for designing and evaluating security awareness programs through simulated social engineering attacks and measuring organizational resilience.

### Tags
`security-awareness` `training` `simulation` `metrics`

---

## 🇬🇧 English Prompt

```
You are a security awareness specialist designing a comprehensive assessment program to measure and improve organizational resilience against social engineering attacks. Develop a detailed framework including:

**Program Foundation:**
- Risk assessment methodology for awareness gaps
- Stakeholder alignment and executive sponsorship
- Baseline metrics establishment
- Industry benchmark comparison

**Assessment Categories:**

1. **Phishing Simulation Program:**
   - Campaign frequency and complexity progression
   - Template realism grading system
   - Target group segmentation (executives, IT, general staff)
   - Multi-stage attack simulations

2. **Vishing Assessment Integration:**
   - Phone-based simulation scenarios
   - Help desk and reception vulnerability testing
   - Executive assistant targeted assessments

3. **Physical Security Drills:**
   - Tailgating prevention exercises
   - Visitor policy compliance checks
   - Clean desk policy audits
   - Sensitive document handling tests

4. **USB Drop Exercises:**
   - Safe USB device deployment methodology
   - Tracking and measurement systems
   - Alternative approaches for high-security environments

**Metrics Framework:**
- Click rates and trend analysis
- Report rates and response times
- Credential submission rates
- Phishing recognition accuracy
- Post-training knowledge retention scores

**Simulation Design Principles:**
- Realistic scenario development based on current threats
- Progressive difficulty scaling
- Department-specific targeting
- Seasonal and event-based relevance
- Industry-specific threat emulation

**Training Content Development:**
- Micro-learning module topics
- Interactive scenario-based training
- Gamification elements for engagement
- Executive-focused awareness content
- New hire onboarding integration

**Reporting and Analytics:**
- Individual performance dashboards
- Department comparison reports
- Trend analysis visualizations
- Executive scorecards
- Risk scoring methodology

**Ethical Considerations & Defensive Measures:**
- Fair treatment of employees who fail simulations
- No punitive actions for simulation failures
- Psychological safety in reporting
- Privacy considerations for tracking data
- Positive reinforcement approaches
- Building reporting culture without blame

**Continuous Improvement Cycle:**
- Quarterly program reviews
- Threat landscape adaptation
- Training content updates
- Metrics benchmark adjustments
- Feedback integration mechanisms

**Program Success Criteria:**
- Target metrics for program maturity
- Industry best practice alignment
- Regulatory compliance requirements
- ROI measurement methodology
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت متخصص في الوعي الأمني تصمم برنامج تقييم شامل لقياس وتحسين المرونة التنظيمية ضد هجمات الهندسة الاجتماعية. طور إطارًا مفصلاً يتضمن:

**أساس البرنامج:**
- منهجية تقييم المخاطر لفجوات الوعي
- التوافق مع أصحاب المصلحة والرعاية التنفيذية
- إنشاء مقاييس خط الأساس
- مقارنة معايير الصناعة

**فئات التقييم:**

1. **برنامج محاكاة التصيد:**
   - تكرار الحملة وتدرج التعقيد
   - نظام تصنيف واقعية القوالب
   - تجزئة المجموعة المستهدفة (تنفيذيون، تقنيون، موظفون عامون)
   - محاكاة هجمات متعددة المراحل

2. **تكامل تقييم الفيشينغ:**
   - سيناريوهات المحاكاة عبر الهاتف
   - اختبار ثغرات مكتب المساعدة والاستقبال
   - تقييمات موجهة لمساعدي التنفيذيين

3. **تدريبات الأمن المادي:**
   - تمارين منع التسلل
   - فحوصات امتثال سياسة الزوار
   - تدقيقات سياسة المكتب النظيف
   - اختبارات التعامل مع المستندات الحساسة

4. **تمارين إسقاط USB:**
   - منهجية نشر أجهزة USB الآمنة
   - أنظمة التتبع والقياس
   - مناهج بديلة للبيئات عالية الأمان

**إطار المقاييس:**
- معدلات النقر وتحليل الاتجاهات
- معدلات الإبلاغ وأوقات الاستجابة
- معدلات إرسال بيانات الاعتماد
- دقة التعرف على التصيد
- درجات الاحتفاظ بالمعرفة بعد التدريب

**مبادئ تصميم المحاكاة:**
- تطوير سيناريوهات واقعية بناءً على التهديدات الحالية
- تحجيم الصعوبة التدريجي
- الاستهداف الخاص بكل قسم
- الصلة الموسمية والحدثية
- محاكاة التهديدات الخاصة بالصناعة

**تطوير محتوى التدريب:**
- مواضيع وحدات التعلم المصغر
- التدريب التفاعلي القائم على السيناريو
- عناصر التنمية للتفاعل
- محتوى الوعي المركز على التنفيذيين
- تكامل إعداد الموظفين الجدد

**إعداد التقارير والتحليلات:**
- لوحات أداء الأفراد
- تقارير مقارنة الأقسام
- تصورات تحليل الاتجاهات
- بطاقات أداء تنفيذية
- منهجية تسجيل المخاطر

**الاعتبارات الأخلاقية والتدابير الدفاعية:**
- المعاملة العادلة للموظفين الذين يفشلون في المحاكاة
- عدم اتخاذ إجراءات عقابية لفشل المحاكاة
- الأمان النفسي في الإبلاغ
- اعتبارات الخصوصية لبيانات التتبع
- مناهج التعزيز الإيجابي
- بناء ثقافة الإبلاغ دون لوم

**دورة التحسين المستمر:**
- مراجعات البرنامج الفصلية
- التكيف مع مشهد التهديدات
- تحديثات محتوى التدريب
- تعديلات معايير المقاييس
- آليات تكامل التغذية الراجعة

**معايير نجاح البرنامج:**
- المقاييس المستهدفة لنضج البرنامج
- التوافق مع أفضل ممارسات الصناعة
- متطلبات الامتثال التنظيمي
- منهجية قياس العائد على الاستثمار
```

---

## Example Output Preview

```
# Security Awareness Program Assessment - Quarterly Report

## Executive Summary
- Overall Phishing Resilience Score: 78/100 (+12 from Q1)
- Report Rate: 82% (+15% improvement)
- Average Response Time: 4.2 minutes (-2.1 min from Q1)

## Department Performance Matrix

| Department      | Click Rate | Report Rate | Training Complete |
|-----------------|------------|-------------|-------------------|
| Finance         | 8%         | 91%         | 100%              |
| Engineering     | 12%        | 78%         | 95%               |
| Sales           | 18%        | 72%         | 88%               |
| Executive Team  | 5%         | 88%         | 100%              |

## Simulation Campaign Results
- Campaigns Run: 6
- Total Emails Sent: 4,250
- Unique Clicks: 412 (9.7%)
- Reports Received: 3,485 (82%)
- Credentials Captured: 23 (0.5%)

## Recommendations
1. Increase simulation complexity for Finance team (high performers)
2. Targeted training for Sales department (lowest metrics)
3. Implement quarterly vishing simulations
4. Deploy USB drop exercise in Engineering area
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team
