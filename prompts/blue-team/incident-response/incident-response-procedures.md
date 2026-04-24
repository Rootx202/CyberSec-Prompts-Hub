# Incident Response Procedures Prompts

A comprehensive collection of bilingual (English/Arabic) prompts for incident response procedures, aligned with NIST SP 800-61 and SANS Incident Handler's Handbook frameworks.

---

## Prompt 1: Incident Triage Process

### Description
A structured approach to triaging security incidents, determining severity levels, and establishing initial response priorities based on impact assessment.

### Tags
`incident-triage` `severity-assessment` `priority-classification` `NIST-800-61`

---

## 🇬🇧 English Prompt

```
You are a senior incident response analyst conducting initial incident triage. Analyze the following incident details and provide a comprehensive triage assessment.

INCIDENT DETAILS:
[Insert incident information including: detection source, affected systems, initial indicators, timeline, user reports]

Provide your triage assessment following NIST SP 800-61 Rev. 2 guidelines:

1. **Incident Classification**
   - Incident type (malware, unauthorized access, denial of service, etc.)
   - Attack vector identification
   - Threat actor category (if determinable)

2. **Severity Assessment** (Critical/High/Medium/Low)
   - Business impact score (1-10)
   - Data sensitivity impact
   - System criticality rating
   - Regulatory compliance implications

3. **Scope Determination**
   - Number of affected hosts/users
   - Network segments impacted
   - Data exposure potential
   - Lateral movement indicators

4. **Priority Matrix**
   - Response urgency level
   - Resource allocation recommendation
   - Escalation requirements
   - Communication plan

5. **Initial Response Actions**
   - Immediate containment needs
   - Evidence preservation priorities
   - Stakeholder notification list

Output Format: Structured report with severity badge and action timeline.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت محلل استجابة للحوادث أول تقوم بإجراء الفرز الأولي للحوادث الأمنية. حلل تفاصيل الحادث التالية وقدم تقييم فرز شامل.

تفاصيل الحادث:
[أدخل معلومات الحادث بما في ذلك: مصدر الاكتشاف، الأنظمة المتأثرة، المؤشرات الأولية، الجدول الزمني، تقارير المستخدمين]

قدم تقييم الفرز الخاص بك وفقاً لإرشادات NIST SP 800-61 Rev. 2:

1. **تصنيف الحادث**
   - نوع الحادث (برمجيات خبيثة، وصول غير مصرح، حرمان من الخدمة، إلخ)
   - تحديد متجه الهجوم
   - فئة الفاعل المهدد (إن أمكن تحديده)

2. **تقييم الخطورة** (حرجة/عالية/متوسطة/منخفضة)
   - درجة تأثير الأعمال (1-10)
   - تأثير حساسية البيانات
   - تصنيف أهمية النظام
   - الآثار المترتبة على الامتثال التنظيمي

3. **تحديد النطاق**
   - عدد المضيفين/المستخدمين المتأثرين
   - مقاطع الشبكة المتضررة
   - احتمالية تسريب البيانات
   - مؤشرات الحركة الجانبية

4. **مصفوفة الأولويات**
   - مستوى الإلحاح في الاستجابة
   - توصية تخصيص الموارد
   - متطلبات التصعيد
   - خطة التواصل

5. **إجراءات الاستجابة الأولية**
   - احتياجات الاحتواء الفورية
   - أولويات حفظ الأدلة
   - قائمة إشعار أصحاب المصلحة

تنسيق المخرجات: تقرير منظم مع شارة الخطورة والجدول الزمني للإجراءات.
```

---

## Example Output Preview

```
═══════════════════════════════════════════════════════
 INCIDENT TRIAGE REPORT | تقرير فرز الحادث
═══════════════════════════════════════════════════════

Incident ID: INC-2024-0892
Severity: 🔴 CRITICAL
Classification: Ransomware Attack

┌─────────────────────────────────────────────────────┐
│ SEVERITY ASSESSMENT                                  │
├─────────────────────────────────────────────────────┤
│ Business Impact:    9/10                            │
│ Data Sensitivity:   HIGH (PII/Financial)            │
│ System Criticality: Production Database             │
│ Regulatory Impact:  GDPR, PCI-DSS breach            │
└─────────────────────────────────────────────────────┘

Scope: 47 hosts affected, Finance department segment
Response Priority: IMMEDIATE - Activate CSIRT
Escalation: CISO, Legal, PR team notified
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 2: Containment Strategies

### Description
Comprehensive containment strategy development including short-term and long-term containment approaches, network segmentation, and isolation procedures.

### Tags
`containment` `network-isolation` `malware-containment` `SANS-Handler`

---

## 🇬🇧 English Prompt

```
You are a cybersecurity incident handler specializing in containment operations. Develop a comprehensive containment strategy for the following security incident.

INCIDENT CONTEXT:
[Insert: incident type, affected infrastructure, current spread status, business criticality]

Following SANS Incident Handler's Handbook methodology, provide:

1. **Short-Term Containment Plan**
   - Immediate isolation actions (first 1-4 hours)
   - Network segmentation emergency procedures
   - System quarantine protocols
   - Service suspension decisions
   - Temporary rule implementations (firewall, IPS/IDS)

2. **Long-Term Containment Strategy**
   - Sustainable containment measures
   - System hardening requirements
   - Enhanced monitoring deployment
   - Backup verification and isolation
   - Business continuity adjustments

3. **Containment Validation**
   - Verification procedures for containment effectiveness
   - Monitoring checkpoints and alerts
   - Rollback procedures if containment fails

4. **Business Impact Mitigation**
   - Critical service maintenance plans
   - Alternative workflow implementations
   - Stakeholder communication protocols

5. **Technical Implementation Commands**
   - Platform-specific isolation commands
   - Network ACL configurations
   - Endpoint protection updates

Provide execution timeline with RACI matrix for each action.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت معالج حوادث أمنية متخصص في عمليات الاحتواء. طور استراتيجية احتواء شاملة للحادث الأمني التالي.

سياق الحادث:
[أدخل: نوع الحادث، البنية التحتية المتأثرة، حالة الانتشار الحالية، أهمية الأعمال]

وفقاً لمنهجية دليل معالج الحوادث من SANS، قدم:

1. **خطة الاحتواء قصيرة المدى**
   - إجراءات العزل الفورية (الساعات 1-4 الأولى)
   - إجراءات الطوارئ لتقسيم الشبكة
   - بروتوكولات عزل الأنظمة
   - قرارات تعليق الخدمات
   - تنفيذ القواعد المؤقتة (جدار حماية، IPS/IDS)

2. **استراتيجية الاحتواء طويلة المدى**
   - تدابير الاحتواء المستدامة
   - متطلبات تقوية الأنظمة
   - نشر المراقبة المحسّنة
   - التحقق من النسخ الاحتياطية وعزلها
   - تعديلات استمرارية الأعمال

3. **التحقق من الاحتواء**
   - إجراءات التحقق من فعالية الاحتواء
   - نقاط المراقبة والتنبيهات
   - إجراءات التراجع في حال فشل الاحتواء

4. **تخفيف تأثير الأعمال**
   - خطط صيانة الخدمات الحرجة
   - تنفيذ سير العمل البديلة
   - بروتوكولات التواصل مع أصحاب المصلحة

5. **أوامر التنفيذ التقنية**
   - أوامر العزل الخاصة بكل منصة
   - تكوينات قوائم التحكم في الشبكة
   - تحديثات حماية نقاط النهاية

قدم الجدول الزمني للتنفيذ مع مصفوفة RACI لكل إجراء.
```

---

## Example Output Preview

```
═══════════════════════════════════════════════════════
 CONTAINMENT STRATEGY DOCUMENT | وثيقة استراتيجية الاحتواء
═══════════════════════════════════════════════════════

┌─────────────────────────────────────────────────────┐
│ SHORT-TERM CONTAINMENT (0-4 Hours)                   │
├─────────────────────────────────────────────────────┤
│ [T+0:00] Isolate affected VLANs: VLAN 100, 200      │
│ [T+0:30] Block C2 IPs at perimeter firewall         │
│ [T+1:00] Disable compromised service accounts       │
│ [T+2:00] Deploy emergency endpoint isolation        │
└─────────────────────────────────────────────────────┘

Network Isolation Commands:
┌─────────────────────────────────────────────────────┐
│ # Cisco IOS - Isolate VLAN                          │
│ conf t                                              │
│   interface Vlan100                                 │
│   shutdown                                          │
│ end                                                 │
│                                                     │
│ # Windows Firewall - Block outbound                 │
│ netsh advfirewall set allprofiles firewallpolicy   │
│   blockinbound,blockoutbound                       │
└─────────────────────────────────────────────────────┘

RACI Matrix:
| Action                | R      | A     | C        | I       |
|-----------------------|--------|-------|----------|---------|
| VLAN Isolation        | NetOps | CISO  | IncResp  | ExTeam  |
| Account Disable       | IdMgmt | CISO  | HR       | Users   |
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 3: Evidence Preservation

### Description
Systematic approach to digital evidence collection, chain of custody management, and forensic data preservation following legal and regulatory standards.

### Tags
`digital-forensics` `evidence-collection` `chain-of-custody` `legal-compliance`

---

## 🇬🇧 English Prompt

```
You are a digital forensics specialist responsible for evidence preservation during an active security incident. Guide the evidence collection process for the following scenario.

INCIDENT SCENARIO:
[Insert: incident type, affected systems, storage media, memory status, network logs availability]

Following NIST SP 800-86 and forensic best practices, provide:

1. **Evidence Identification Checklist**
   - Volatile data sources (RAM, network connections, running processes)
   - Non-volatile data sources (hard drives, logs, configurations)
   - Cloud and virtual environment artifacts
   - Mobile devices and IoT assets
   - Network traffic captures

2. **Collection Priority Matrix**
   - Order of volatility (most volatile first)
   - Collection window requirements
   - Resource requirements per evidence type
   - Risk of evidence degradation

3. **Acquisition Procedures**
   - Memory acquisition methods and tools
   - Disk imaging procedures (forensic vs. logical)
   - Network log collection steps
   - Cloud forensic acquisition
   - Hash verification protocols

4. **Chain of Custody Documentation**
   - Evidence labeling system
   - Transfer and handling procedures
   - Storage requirements
   - Access logging format

5. **Legal Considerations**
   - Warrant and authorization requirements
   - Privacy regulations compliance
   - Cross-border data considerations
   - Admissibility requirements

Provide step-by-step collection scripts and documentation templates.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت متخصص في الطب الشرعي الرقمي مسؤول عن حفظ الأدلة أثناء حادث أمني نشط. وجه عملية جمع الأدلة للسيناريو التالي.

سيناريو الحادث:
[أدخل: نوع الحادث، الأنظمة المتأثرة، وسائط التخزين، حالة الذاكرة، توفر سجلات الشبكة]

وفقاً لـ NIST SP 800-86 وأفضل الممارسات الجنائية، قدم:

1. **قائمة التحقق من تحديد الأدلة**
   - مصادر البيانات المتطايرة (الذاكرة العشوائية، الاتصالات الشبكية، العمليات الجارية)
   - مصادر البيانات غير المتطايرة (محركات الأقراص الصلبة، السجلات، التكوينات)
   - آثار البيئات السحابية والافتراضية
   - الأجهزة المحمولة وأصول إنترنت الأشياء
   - لقطات حركة مرور الشبكة

2. **مصفوفة أولويات الجمع**
   - ترتيب التطاير (الأكثر تطايراً أولاً)
   - متطلبات نافذة الجمع
   - متطلبات الموارد حسب نوع الدليل
   - خطر تدهور الأدلة

3. **إجراءات الاستحواذ**
   - طرق وأدوات استحواذ الذاكرة
   - إجراءات نسخ الأقراص (جنائية مقابل منطقية)
   - خطوات جمع سجلات الشبكة
   - الاستحواذ الجنائي السحابي
   - بروتوكولات التحقق من البصمة الرقمية

4. **توثيق سلسلة الحيازة**
   - نظام تسمية الأدلة
   - إجراءات النقل والتعامل
   - متطلبات التخزين
   - تنسيق تسجيل الوصول

5. **الاعتبارات القانونية**
   - متطلبات المذكرات والترخيص
   - الامتثال للوائح الخصوصية
   - الاعتبارات عبر الحدود
   - متطلبات القبول كدليل

قدم نصوص جمع خطوة بخطوة وقوالب التوثيق.
```

---

## Example Output Preview

```
═══════════════════════════════════════════════════════
 EVIDENCE PRESERVATION PLAN | خطة حفظ الأدلة
═══════════════════════════════════════════════════════

┌─────────────────────────────────────────────────────┐
│ ORDER OF VOLATILITY COLLECTION                       │
├────────────┬──────────────────────────┬─────────────┤
│ Priority   │ Evidence Type            │ Window      │
├────────────┼──────────────────────────┼─────────────┤
│ 1          │ CPU Registers/Cache      │ Seconds     │
│ 2          │ Memory (RAM)             │ Minutes     │
│ 3          │ Network State            │ Minutes     │
│ 4          │ Running Processes        │ Minutes     │
│ 5          │ Disk Data                │ Days        │
│ 6          │ Remote Logs              │ Weeks       │
│ 7          │ Archive Media            │ Years       │
└────────────┴──────────────────────────┴─────────────┘

Memory Acquisition Command (Linux):
┌─────────────────────────────────────────────────────┐
│ # Using LiME (Linux Memory Extractor)               │
│ sudo insmod lime.ko "path=/mnt/usb/mem.lime         │
│   format=raw"                                       │
│                                                     │
│ # Calculate hash for verification                   │
│ sha256sum /mnt/usb/mem.lime > mem.lime.sha256      │
└─────────────────────────────────────────────────────┘

CHAIN OF CUSTODY FORM
┌─────────────────────────────────────────────────────┐
│ Evidence ID: EVD-2024-0892-001                      │
│ Type: RAM Image                                     │
│ Source: srv-finance-01 (192.168.1.50)              │
│ Collected By: Ahmed Hassan                          │
│ Date/Time: 2024-03-15 14:32:17 UTC                  │
│ Hash (SHA256): a7f2c8...d4e9b1                      │
│ Location: Evidence Locker A-3                       │
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

## Prompt 4: Eradication Procedures

### Description
Methodical eradication of threats including malware removal, vulnerability remediation, and verification of threat elimination from the environment.

### Tags
`eradication` `malware-removal` `vulnerability-remediation` `threat-elimination`

---

## 🇬🇧 English Prompt

```
You are a senior security engineer responsible for threat eradication. Develop a comprehensive eradication plan for the following security incident.

THREAT DETAILS:
[Insert: malware type/exploit details, affected systems, persistence mechanisms, lateral movement scope, IOCs]

Following NIST SP 800-61 and SANS methodology, provide:

1. **Threat Analysis**
   - Malware/threat classification
   - Persistence mechanisms identified
   - Command and control infrastructure
   - Propagation methods
   - Associated vulnerabilities exploited

2. **Eradication Action Plan**
   - Malware removal procedures per system type
   - Registry/System configuration cleanup
   - Scheduled task/service removal
   - Backdoor and remote access elimination
   - Malicious account removal
   - C2 communication blocking

3. **Vulnerability Remediation**
   - Patching requirements and priority
   - Configuration changes needed
   - Security control updates
   - Third-party software updates

4. **Verification Procedures**
   - IOC scanning across environment
   - Persistence mechanism verification
   - C2 communication testing
   - Behavioral analysis confirmation
   - Clean baseline comparison

5. **Documentation Requirements**
   - Eradication timeline documentation
   - Systems remediated inventory
   - Outstanding issues tracking
   - Lessons learned notes

Provide platform-specific eradication commands and verification scripts.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت مهندس أمن أول مسؤول عن استئصال التهديدات. طور خطة استئصال شاملة للحادث الأمني التالي.

تفاصيل التهديد:
[أدخل: نوع البرمجيات الخبيثة/تفاصيل الاستغلال، الأنظمة المتأثرة، آليات الاستمرار، نطاق الحركة الجانبية، مؤشرات الاختراق]

وفقاً لمنهجية NIST SP 800-61 و SANS، قدم:

1. **تحليل التهديد**
   - تصنيف البرمجيات الخبيثة/التهديد
   - آليات الاستمرار المحددة
   - البنية التحتية للقيادة والتحكم
   - طرق الانتشار
   - الثغرات الأمنية المرتبطة المستغلة

2. **خطة إجراءات الاستئصال**
   - إجراءات إزالة البرمجيات الخبيثة حسب نوع النظام
   - تنظيف السجل/تكوين النظام
   - إزالة المهام المجدولة/الخدمات
   - القضاء على الأبواب الخلفية والوصول عن بعد
   - إزالة الحسابات الخبيثة
   - حظر اتصالات القيادة والتحكم

3. **معالجة الثغرات الأمنية**
   - متطلبات الترقيع والأولوية
   - تغييرات التكوين المطلوبة
   - تحديثات ضوابط الأمان
   - تحديثات برامج الطرف الثالث

4. **إجراءات التحقق**
   - فحص مؤشرات الاختراق عبر البيئة
   - التحقق من آليات الاستمرار
   - اختبار اتصالات القيادة والتحكم
   - تأكيد التحليل السلوكي
   - مقارنة خط الأساس النظيف

5. **متطلبات التوثيق**
   - توثيق الجدول الزمني للاستئصال
   - جرد الأنظمة المعالجة
   - تتبع القضايا المعلقة
   - ملاحظات الدروس المستفادة

قدم أوامر الاستئصال الخاصة بكل منصة ونصوص التحقق.
```

---

## Example Output Preview

```
═══════════════════════════════════════════════════════
 ERADICATION PROCEDURES DOCUMENT | وثيقة إجراءات الاستئصال
═══════════════════════════════════════════════════════

┌─────────────────────────────────────────────────────┐
│ THREAT PROFILE                                       │
├─────────────────────────────────────────────────────┤
│ Classification: APT29-derived backdoor              │
│ Persistence:  Registry Run Keys + Scheduled Task    │
│ C2 Domains:  mal-site[.]com, c2-net[.]biz          │
│ Propagation: SMB exploit + Credential theft         │
└─────────────────────────────────────────────────────┘

ERADICATION ACTIONS:
┌─────────────────────────────────────────────────────┐
│ Windows - Registry Cleanup                          │
│ reg delete "HKLM\SOFTWARE\Microsoft\Windows        │
│   \CurrentVersion\Run" /v "SecurityHealth" /f      │
│                                                     │
│ Windows - Scheduled Task Removal                    │
│ schtasks /delete /tn "SystemHealthCheck" /f        │
│                                                     │
│ Windows - Service Removal                           │
│ sc delete "WinSecurityService"                      │
│                                                     │
│ Firewall - Block C2                                 │
│ netsh advfirewall firewall add rule name="Block    │
│   C2" dir=out action=block remoteip=10.10.10.50    │
└─────────────────────────────────────────────────────┘

VERIFICATION SCRIPT OUTPUT:
┌─────────────────────────────────────────────────────┐
│ [✓] Registry persistence: REMOVED                   │
│ [✓] Scheduled tasks: CLEAN                          │
│ [✓] C2 connectivity: BLOCKED                        │
│ [✓] Malicious files: 0 FOUND                        │
│ [✓] Network connections: CLEAN                      │
│ [⚠] Pending: Patch MS17-010 on 3 servers           │
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

## Prompt 5: Recovery Planning

### Description
Strategic recovery planning including system restoration, service resumption, monitoring enhancement, and business continuity operations post-incident.

### Tags
`recovery-planning` `system-restoration` `business-continuity` `service-resumption`

---

## 🇬🇧 English Prompt

```
You are a disaster recovery specialist developing a recovery plan after a security incident. Create a comprehensive recovery strategy for the following situation.

INCIDENT RECOVERY CONTEXT:
[Insert: incident type, systems affected, backup status, business impact, regulatory requirements, downtime costs]

Following NIST SP 800-61 and business continuity best practices, provide:

1. **Recovery Objectives**
   - Recovery Time Objective (RTO) per system
   - Recovery Point Objective (RPO) assessment
   - Maximum Tolerable Downtime (MTD)
   - Critical system prioritization matrix

2. **System Restoration Plan**
   - Clean system rebuild procedures
   - Backup restoration sequence
   - Data integrity verification
   - Configuration restoration steps
   - Patch management before restoration

3. **Service Resumption Strategy**
   - Phased return-to-service approach
   - Dependency mapping for services
   - User access restoration
   - Network connectivity restoration
   - Third-party integration recovery

4. **Enhanced Monitoring Deployment**
   - Temporary heightened monitoring rules
   - IOC-based alerting deployment
   - Behavioral analytics tuning
   - Log retention adjustments
   - SIEM rule additions

5. **Validation and Testing**
   - Service functionality testing checklist
   - Security validation procedures
   - Performance baseline comparison
   - User acceptance criteria

6. **Communication Plan**
   - Internal stakeholder updates
   - Customer/user notification
   - Regulatory body reporting
   - Status reporting schedule

Provide detailed timeline with resource allocation and dependencies.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت متخصص في استعادة الكوارث تقوم بتطوير خطة استعادة بعد حادث أمني. أنشئ استراتيجية استعادة شاملة للوضع التالي.

سياق استعادة الحادث:
[أدخل: نوع الحادث، الأنظمة المتأثرة، حالة النسخ الاحتياطي، تأثير الأعمال، المتطلبات التنظيمية، تكاليف التوقف]

وفقاً لـ NIST SP 800-61 وأفضل ممارسات استمرارية الأعمال، قدم:

1. **أهداف الاستعادة**
   - هدف وقت الاستعادة (RTO) لكل نظام
   - تقييم هدف نقطة الاستعادة (RPO)
   - أقصى وقت توقف محتمل (MTD)
   - مصفوفة أولويات الأنظمة الحرجة

2. **خطة استعادة الأنظمة**
   - إجراءات إعادة بناء الأنظمة النظيفة
   - تسلسل استعادة النسخ الاحتياطية
   - التحقق من سلامة البيانات
   - خطوات استعادة التكوين
   - إدارة الترقيع قبل الاستعادة

3. **استراتيجية استئناف الخدمات**
   - نهج العودة التدريجية للخدمة
   - تخطيط التبعيات للخدمات
   - استعادة وصول المستخدمين
   - استعادة الاتصال الشبكي
   - استعادة تكاملات الطرف الثالث

4. **نشر المراقبة المحسّنة**
   - قواعد المراقبة المؤقتة المكثفة
   - نشر التنبيهات المستندة إلى مؤشرات الاختراق
   - ضبط التحليلات السلوكية
   - تعديلات الاحتفاظ بالسجلات
   - إضافات قواعد SIEM

5. **التحقق والاختبار**
   - قائمة التحقق من اختبار وظائف الخدمة
   - إجراءات التحقق الأمني
   - مقارنة خط الأساس للأداء
   - معايير قبول المستخدم

6. **خطة التواصل**
   - تحديثات أصحاب المصلحة الداخليين
   - إشعار العملاء/المستخدمين
   - الإبلاغ للهيئات التنظيمية
   - جدول تقارير الحالة

قدم جدولاً زمنياً مفصلاً مع تخصيص الموارد والتبعيات.
```

---

## Example Output Preview

```
═══════════════════════════════════════════════════════
 RECOVERY PLAN | خطة الاستعادة
═══════════════════════════════════════════════════════

┌─────────────────────────────────────────────────────┐
│ RECOVERY OBJECTIVES                                  │
├──────────────────┬──────────┬──────────┬────────────┤
│ System           │ RTO      │ RPO      │ Priority   │
├──────────────────┼──────────┼──────────┼────────────┤
│ AD Domain Ctrl   │ 2 hours  │ 1 hour   │ P1         │
│ Database Server  │ 4 hours  │ 15 min   │ P1         │
│ Web Servers      │ 6 hours  │ 1 hour   │ P2         │
│ File Servers     │ 12 hours │ 4 hours  │ P2         │
│ Workstations     │ 24 hours │ 24 hours │ P3         │
└──────────────────┴──────────┴──────────┴────────────┘

PHASED RECOVERY TIMELINE:
┌─────────────────────────────────────────────────────┐
│ Phase 1 (0-4h): Core Infrastructure                 │
│   ├─ Restore AD from clean backup                   │
│   ├─ Verify authentication services                 │
│   └─ Validate DNS/DHCP operations                   │
│                                                     │
│ Phase 2 (4-8h): Critical Services                   │
│   ├─ Database restoration & verification            │
│   ├─ Application server rebuild                     │
│   └─ Network segment re-enablement                  │
│                                                     │
│ Phase 3 (8-24h): Full Operations                    │
│   ├─ Workstation reimaging                         │
│   ├─ User access restoration                        │
│   └─ Service monitoring enhancement                 │
└─────────────────────────────────────────────────────┘

SERVICE VALIDATION CHECKLIST:
[✓] Database integrity: VERIFIED
[✓] Application functionality: TESTED
[✓] User authentication: OPERATIONAL
[✓] Network segmentation: ENFORCED
[✓] Backup verification: COMPLETED
[⏳] Performance baseline: IN PROGRESS
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 6: Post-Incident Analysis

### Description
Comprehensive post-incident analysis including root cause analysis, lessons learned documentation, and actionable recommendations for security improvement.

### Tags
`post-incident-analysis` `root-cause-analysis` `lessons-learned` `security-improvement`

---

## 🇬🇧 English Prompt

```
You are a senior security analyst conducting a post-incident analysis. Provide a comprehensive retrospective analysis for the following resolved incident.

INCIDENT SUMMARY:
[Insert: incident timeline, response actions taken, systems affected, data impact, resolution status, total cost]

Following NIST SP 800-61 and SANS post-incident review guidelines, provide:

1. **Executive Summary**
   - Incident overview in business terms
   - Business impact quantification
   - Response effectiveness rating
   - Key outcomes and decisions

2. **Root Cause Analysis**
   - Attack vector analysis
   - Contributing factors identification
   - Control failures analysis
   - Why-Why analysis or 5 Whys methodology
   - Timeline reconstruction

3. **Response Effectiveness Review**
   - Detection timeline analysis
   - Response speed assessment
   - Communication effectiveness
   - Tool and process gaps
   - Team coordination evaluation

4. **Lessons Learned**
   - What worked well (positives)
   - What could be improved (gaps)
   - Unexpected challenges faced
   - Resource adequacy assessment

5. **Recommendations**
   - Short-term improvements (0-30 days)
   - Medium-term enhancements (30-90 days)
   - Long-term strategic changes (90+ days)
   - Policy and procedure updates
   - Training and awareness needs

6. **Metrics and KPIs**
   - Time to detect (TTD)
   - Time to respond (TTR)
   - Time to recover (TTR)
   - Mean time between incidents (MTBI)
   - Cost per incident analysis

7. **Action Items**
   - Prioritized action list with owners
   - Due dates and milestones
   - Success criteria for each action
   - Follow-up review schedule

Provide structured report format suitable for executive and technical audiences.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت محلل أمن أول تجري تحليلاً بعد الحادث. قدم تحليلاً استعاديًا شاملاً للحادث المحلول التالي.

ملخص الحادث:
[أدخل: الجدول الزمني للحادث، إجراءات الاستجابة المتخذة، الأنظمة المتأثرة، تأثير البيانات، حالة الحل، التكلفة الإجمالية]

وفقاً لإرشادات مراجعة ما بعد الحادث من NIST SP 800-61 و SANS، قدم:

1. **الملخص التنفيذي**
   - نظرة عامة على الحادث بمصطلحات الأعمال
   - تحديد كمية تأثير الأعمال
   - تقييم فعالية الاستجابة
   - النتائج والقرارات الرئيسية

2. **تحليل السبب الجذري**
   - تحليل متجه الهجوم
   - تحديد العوامل المساهمة
   - تحليل فشل الضوابط
   - منهجية لماذا-لماذا أو 5 لماذا
   - إعادة بناء الجدول الزمني

3. **مراجعة فعالية الاستجابة**
   - تحليل الجدول الزمني للكشف
   - تقييم سرعة الاستجابة
   - فعالية التواصل
   - فجوات الأدوات والعمليات
   - تقييم تنسيق الفريق

4. **الدروس المستفادة**
   - ما عمل بشكل جيد (الإيجابيات)
   - ما يمكن تحسينه (الفجوات)
   - التحديات غير المتوقعة التي واجهت
   - تقييم كفاية الموارد

5. **التوصيات**
   - التحسينات قصيرة المدى (0-30 يوم)
   - التعزيزات متوسطة المدى (30-90 يوم)
   - التغييرات الاستراتيجية طويلة المدى (90+ يوم)
   - تحديثات السياسات والإجراءات
   - احتياجات التدريب والتوعية

6. **المقاييس والمؤشرات الرئيسية**
   - الوقت للكشف (TTD)
   - الوقت للاستجابة (TTR)
   - الوقت للاستعادة (TTR)
   - متوسط الوقت بين الحوادث (MTBI)
   - تحليل التكلفة لكل حادث

7. **عناصر العمل**
   - قائمة إجراءات مرتبة حسب الأولوية مع المالكين
   - تواريخ الاستحقاق والمعالم
   - معايير النجاح لكل إجراء
   - جدول مراجعة المتابعة

قدم تنسيق تقرير منظم مناسب للجماهير التنفيذية والتقنية.
```

---

## Example Output Preview

```
═══════════════════════════════════════════════════════
 POST-INCIDENT ANALYSIS REPORT | تقرير تحليل ما بعد الحادث
═══════════════════════════════════════════════════════

EXECUTIVE SUMMARY
┌─────────────────────────────────────────────────────┐
│ Incident ID: INC-2024-0892                          │
│ Classification: Ransomware Attack                   │
│ Duration: 72 hours total                            │
│ Business Impact: $2.4M (downtime + response)        │
│ Data Impact: No exfiltration confirmed              │
│ Response Rating: ★★★★☆ (4/5)                        │
└─────────────────────────────────────────────────────┘

ROOT CAUSE ANALYSIS (5 Whys):
┌─────────────────────────────────────────────────────┐
│ Why 1: Systems were encrypted by ransomware         │
│ Why 2: Attacker gained access via phishing          │
│ Why 3: Employee clicked malicious link              │
│ Why 4: Email filtering failed to detect threat      │
│ Why 5: Signature-based only, no sandbox analysis    │
│                                                     │
│ ROOT CAUSE: Inadequate email security controls      │
│ CONTRIBUTING: Outdated patching, lack of MFA        │
└─────────────────────────────────────────────────────┘

RESPONSE METRICS:
┌─────────────────────────────────────────────────────┐
│ Time to Detect (TTD):    2 hours 34 minutes        │
│ Time to Respond (TTR):   4 hours 12 minutes        │
│ Time to Recover (TTR):   68 hours                   │
│ Detection Source: User Report                       │
│ Initial Containment: 45 minutes                     │
│ Full Eradication: 36 hours                          │
└─────────────────────────────────────────────────────┘

LESSONS LEARNED:
┌─────────────────────────────────────────────────────┐
│ ✓ POSITIVES                                         │
│   • Incident response team activated within 15 min │
│   • Backup systems remained uncompromised          │
│   • Communication protocols followed effectively   │
│                                                     │
│ ✗ GAPS                                              │
│   • Detection relied on user reporting             │
│   • Network segmentation insufficient              │
│   • MFA not enforced for VPN access                │
└─────────────────────────────────────────────────────┘

ACTION ITEMS:
┌────┬──────────────────────────────┬────────┬──────────┐
│ #  │ Action                        │ Owner  │ Due Date │
├────┼──────────────────────────────┼────────┼──────────┤
│ 1  │ Deploy email sandboxing       │ SecOps │ 7 days   │
│ 2  │ Enforce MFA for VPN           │ IAM    │ 14 days  │
│ 3  │ Network segmentation review   │ NetOps │ 30 days  │
│ 4  │ EDR deployment all endpoints  │ SecOps │ 45 days  │
│ 5  │ Phishing awareness training   │ HR     │ 30 days  │
└────┴──────────────────────────────┴────────┴──────────┘
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team
