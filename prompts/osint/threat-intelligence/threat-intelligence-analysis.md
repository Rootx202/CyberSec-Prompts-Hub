# Threat Intelligence Analysis - OSINT Prompts

> A comprehensive collection of bilingual (English/Arabic) prompts for threat intelligence platforms, IOC analysis, threat feeds, and intelligence methodologies.

---

## Prompt 1: Threat Intelligence Platform Integration

### Description
Design and implement threat intelligence platform (TIP) integrations for centralized intelligence management, automation, and distribution across security operations.

### Tags
`threat-intelligence-platform` `tip` `intelligence-management` `automation` `misp`

---

## 🇬🇧 English Prompt

```
You are a threat intelligence architect designing platform integrations. Develop a comprehensive TIP implementation framework:

**Section 1: Platform Selection & Architecture**

**Platform Evaluation Criteria:**
- Open source vs. commercial considerations
- Scalability and performance requirements
- Integration capabilities assessment
- Data model and STIX/TAXII support
- Multi-tenancy and access control

**Popular Platforms:**
- MISP (Open Source)
- OpenCTI (Open Source)
- ThreatConnect (Commercial)
- Anomali ThreatStream (Commercial)
- Recorded Future (Commercial)

**Architecture Design:**
- Single vs. distributed deployment
- High availability configuration
- Data storage considerations
- API gateway design
- Authentication and authorization

**Section 2: Data Ingestion Framework**

**Internal Sources:**
- SIEM integration (Splunk, Elastic, QRadar)
- EDR feeds (CrowdStrike, SentinelOne, Defender)
- Email security gateways
- Firewall and proxy logs
- Vulnerability scanners

**External Sources:**
- Commercial threat feeds
- Open source intelligence feeds
- Information sharing communities (ISACs)
- Government feeds (CISA, NCSC)
- Research organization feeds

**Ingestion Methods:**
- STIX/TAXII protocol
- REST API integration
- File-based import (CSV, JSON, STIX)
- Real-time streaming (Kafka, webhook)
- Email parsing for reports

**Section 3: Data Processing & Enrichment**

**Normalization Pipeline:**
- Indicator format standardization
- De-duplication logic
- Confidence scoring assignment
- TLP marking application
- Relationship mapping

**Enrichment Services:**
- WHOIS and DNS enrichment
- Geolocation services
- Malware analysis sandbox integration
- URL and domain reputation
- Hash lookup services

**Quality Assurance:**
- Feed reliability scoring
- False positive identification
- Stale indicator management
- Confidence level adjustment
- Source reputation tracking

**Section 4: Intelligence Distribution**

**Downstream Integration:**
- SIEM detection rule generation
- Firewall block list updates
- DNS sinkhole configuration
- Email gateway rules
- EDR IOC deployment

**Sharing Mechanisms:**
- TAXII server configuration
- MISP feed distribution
- STIX bundle export
- PDF report generation
- API endpoint provisioning

**Access Control:**
- Role-based access control (RBAC)
- TLP-based sharing restrictions
- Organization-level isolation
- API key management
- Audit logging

**Section 5: Automation & Orchestration**

**Automation Use Cases:**
- New IOC automatic enrichment
- Alert triage automation
- Feed quality monitoring
- Expiration and rotation
- Report generation scheduling

**SOAR Integration:**
- Playbook trigger points
- Bi-directional sync design
- Case management integration
- Response automation handoff

**Output Requirements:**
- Platform architecture diagram
- Integration configuration guide
- Data flow documentation
- Automation playbook library
- Operational procedures
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت مهندس استخبارات تهديدات تصمم تكامل المنصات. طور إطاراً شاملاً لتنفيذ منصة استخبارات التهديدات:

**القسم 1: اختيار المنصة والبنية**

**معايير تقييم المنصة:**
- اعتبارات المصدر المفتوح مقابل التجاري
- متطلبات القابلية للتوسع والأداء
- تقييم قدرات التكامل
- دعم نموذج البيانات و STIX/TAXII
- تعدد المستأجرين والتحكم في الوصول

**المنصات الشائعة:**
- MISP (مفتوح المصدر)
- OpenCTI (مفتوح المصدر)
- ThreatConnect (تجاري)
- Anomali ThreatStream (تجاري)
- Recorded Future (تجاري)

**تصميم البنية:**
- النشر الفردي مقابل الموزع
- تكوين التوافر العالي
- اعتبارات تخزين البيانات
- تصميم بوابة API
- المصادقة والتفويض

**القسم 2: إطار استيعاب البيانات**

**المصادر الداخلية:**
- تكامل SIEM (Splunk, Elastic, QRadar)
- تغذيات EDR (CrowdStrike, SentinelOne, Defender)
- بوابات أمن البريد الإلكتروني
- سجلات جدار الحماية والوكيل
- ماسحات الثغرات

**المصادر الخارجية:**
- تغذيات التهديدات التجارية
- تغذيات الاستخبارات مفتوحة المصدر
- مجتمعات مشاركة المعلومات (ISACs)
- التغذيات الحكومية (CISA, NCSC)
- تغذيات منظمات البحث

**طرق الاستيعاب:**
- بروتوكول STIX/TAXII
- تكامل REST API
- استيراد قائم على الملفات (CSV, JSON, STIX)
- البث في الوقت الحقيقي (Kafka, webhook)
- تحليل البريد الإلكتروني للتقارير

**القسم 3: معالجة البيانات والإثراء**

**خط أنابيب التطبيع:**
- توحيد تنسيق المؤشر
- منطق إزالة التكرار
- تعيين درجة الثقة
- تطبيق علامات TLP
- رسم خريطة العلاقات

**خدمات الإثراء:**
- إثراء WHOIS و DNS
- خدمات تحديد الموقع الجغرافي
- تكامل صندوق رمل تحليل البرمجيات الخبيثة
- سمعة URL والنطاق
- خدمات البحث عن التجزئة

**ضمان الجودة:**
- تسجيل موثوقية التغذية
- تحديد الإيجابيات الكاذبة
- إدارة المؤشرات القديمة
- تعديل مستوى الثقة
- تتبع سمعة المصدر

**القسم 4: توزيع الاستخبارات**

**التكامل النهائي:**
- توليد قواعد كشف SIEM
- تحديثات قائمة حظر جدار الحماية
- تكوين حفرة DNS
- قواعد بوابة البريد الإلكتروني
- نشر IOC لـ EDR

**آليات المشاركة:**
- تكوين خادم TAXII
- توزيع تغذية MISP
- تصدير حزمة STIX
- توليد تقارير PDF
- توفير نقاط نهاية API

**التحكم في الوصول:**
- التحكم في الوصول القائم على الدور (RBAC)
- قيود المشاركة القائمة على TLP
- عزل مستوى المنظمة
- إدارة مفاتيح API
- تسجيل التدقيق

**القسم 5: الأتمتة والتنسيق**

**حالات استخدام الأتمتة:**
- الإثراء التلقائي لـ IOC الجديد
- أتمتة فرز التنبيهات
- مراقبة جودة التغذية
- انتهاء الصلاحية والتبديل
- جدولة توليد التقارير

**تكامل SOAR:**
- نقاط تشغيل دليل التشغيل
- تصميم المزامنة ثنائية الاتجاه
- تكامل إدارة الحالات
- تسليم أتمتة الاستجابة

**متطلبات المخرجات:**
- مخطط بنية المنصة
- دليل تكوين التكامل
- توثيق تدفق البيانات
- مكتبة أدلة تشغيل الأتمتة
- الإجراءات التشغيلية
```

---

## Example Output Preview

```
# Threat Intelligence Platform Architecture

## Platform Architecture Diagram

```
┌─────────────────────────────────────────────────────────────────┐
│                    THREAT INTELLIGENCE PLATFORM                  │
│  ┌─────────────────────────────────────────────────────────────┐│
│  │                     Ingestion Layer                          ││
│  │  ┌─────────┐ ┌─────────┐ ┌─────────┐ ┌─────────┐           ││
│  │  │ STIX/   │ │ REST    │ │ TAXII   │ │ File    │           ││
│  │  │ TAXII   │ │ API     │ │ Server  │ │ Import  │           ││
│  │  └────┬────┘ └────┬────┘ └────┬────┘ └────┬────┘           ││
│  └───────┼──────────┼──────────┼──────────┼───────────────────┘│
│          └──────────┼──────────┼──────────┘                     │
│  ┌──────────────────▼──────────▼───────────────────────────────┐│
│  │                  Processing Layer                            ││
│  │  ┌───────────┐ ┌───────────┐ ┌───────────┐ ┌─────────────┐ ││
│  │  │ Normalize │ │Enrichment │ │ De-dup    │ │ Score       │ ││
│  │  └───────────┘ └───────────┘ └───────────┘ └─────────────┘ ││
│  └─────────────────────────────────────────────────────────────┘│
│  ┌─────────────────────────────────────────────────────────────┐│
│  │                   Storage Layer                              ││
│  │  ┌──────────────┐ ┌──────────────┐ ┌──────────────────────┐ ││
│  │  │ Indicators   │ │ Relationships│ │ Reports/Analysis     │ ││
│  │  │ (Elastic)    │ │ (Graph DB)   │ │ (PostgreSQL)         │ ││
│  │  └──────────────┘ └──────────────┘ └──────────────────────┘ ││
│  └─────────────────────────────────────────────────────────────┘│
│  ┌─────────────────────────────────────────────────────────────┐│
│  │                  Distribution Layer                          ││
│  │  ┌─────────┐ ┌─────────┐ ┌─────────┐ ┌─────────┐           ││
│  │  │ SIEM    │ │ Firewall│ │ EDR     │ │ SOAR    │           ││
│  │  │ Export  │ │ Blocks  │ │ IOC     │ │ Trigger │           ││
│  │  └─────────┘ └─────────┘ └─────────┘ └─────────┘           ││
│  └─────────────────────────────────────────────────────────────┘│
└─────────────────────────────────────────────────────────────────┘
```

## Integration Configuration

### Source Connectors
| Source | Type | Method | Frequency | Format |
|--------|------|--------|-----------|--------|
| AlienVault OTX | External | API | 15 min | STIX 2.1 |
| MISP Community | Community | TAXII | 5 min | MISP JSON |
| Internal SIEM | Internal | API | Real-time | JSON |
| CISA Advisories | Government | RSS | Hourly | STIX 2.0 |
| Vendor Feed A | Commercial | API | 30 min | CSV |

### Enrichment Pipeline
```yaml
enrichment_pipeline:
  - step: whois_lookup
    service: whois_api
    timeout: 5s
    
  - step: dns_resolution
    service: internal_dns
    timeout: 3s
    
  - step: geolocation
    service: maxmind
    timeout: 2s
    
  - step: reputation_check
    services:
      - virusTotal
      - hybrid_analysis
    timeout: 10s
    
  - step: malware_analysis
    service: cuckoo_sandbox
    condition: is_file_hash
    timeout: 60s
```

## Distribution Configuration

### SIEM Export (Splunk)
```python
# IOC Export to Splunk Lookup
def export_to_splunk(indicators, lookup_name="threat_intel.csv"):
    """
    Export indicators to Splunk lookup table
    """
    output = []
    for indicator in indicators:
        output.append({
            'indicator': indicator.value,
            'type': indicator.type,
            'confidence': indicator.confidence,
            'severity': indicator.severity,
            'first_seen': indicator.first_seen,
            'last_seen': indicator.last_seen,
            'tags': ','.join(indicator.tags),
            'tlp': indicator.tlp
        })
    
    # Write to Splunk lookup path
    write_csv(f"/opt/splunk/etc/apps/TA-threat-intel/lookups/{lookup_name}", output)
```

### Firewall Block List
```
# Firewall Block List Generation
# Generated: 2024-01-15 10:00:00 UTC
# Total IPs: 1,247
# TLP: AMBER

# High Confidence Malicious IPs
deny 192.0.2.1  # C2 Server - APT Group A - Confidence: 95
deny 198.51.100.1  # Malware Distribution - Confidence: 90
deny 203.0.113.1  # Phishing Infrastructure - Confidence: 85
...
```

## Automation Playbook: New IOC Processing
```yaml
playbook: new_ioc_processing
trigger: indicator_created
steps:
  - name: enrich_indicator
    actions:
      - whois_lookup
      - dns_resolution
      - geolocate
      - reputation_check
      
  - name: score_indicator
    condition: enrichment_complete
    actions:
      - calculate_confidence_score
      - assign_severity
      
  - name: distribute_indicator
    condition: confidence > 70
    actions:
      - push_to_siem
      - update_firewall_blocks
      - create_detection_rule
      
  - name: notify_analysts
    condition: severity == "critical"
    actions:
      - create_case_in_soar
      - notify_on_call_analyst
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

## Prompt 2: IOC Analysis & Enrichment

### Description
Perform comprehensive indicator of compromise (IOC) analysis including contextual enrichment, confidence scoring, and actionable intelligence derivation.

### Tags
`ioc-analysis` `indicator-enrichment` `confidence-scoring` `threat-indicators` `contextual-analysis`

---

## 🇬🇧 English Prompt

```
You are a threat intelligence analyst conducting IOC analysis. Develop a comprehensive indicator analysis framework:

**Section 1: Indicator Classification**

**Indicator Types:**
- Network indicators (IP, domain, URL, email)
- File indicators (hash, filename, path)
- Host indicators (registry, mutex, service)
- Behavioral indicators (pattern, TTP)
- Cryptographic indicators (certificate, key)

**Classification Criteria:**
- Threat type categorization
- Actor attribution indicators
- Campaign association
- Malware family linkage
- Infrastructure classification

**Section 2: Contextual Enrichment**

**Network Indicators:**
- WHOIS registration data
- DNS resolution history
- SSL certificate analysis
- ASN and network allocation
- Historical passive DNS
- Port and service scanning
- Geographic location

**File Indicators:**
- Static analysis results
- Dynamic analysis sandbox reports
- Import table analysis
- String extraction
- Packer identification
- Compilation timestamps
- Digital signature validation

**Behavioral Indicators:**
- MITRE ATT&CK technique mapping
- Kill chain phase identification
- Tool classification
- Detection rule correlation

**Section 3: Confidence Scoring**

**Scoring Factors:**
- Source reliability (1-5 scale)
- Corroboration from multiple sources
- Age of indicator
- Context specificity
- False positive history

**Confidence Levels:**
- High (80-100): Confirmed malicious
- Medium (50-79): Likely malicious
- Low (20-49): Suspicious
- Unknown (0-19): Insufficient data

**Scoring Algorithm:**
```
Confidence = (Source_Reliability × 0.25) +
             (Corroboration × 0.30) +
             (Context_Match × 0.25) +
             (Recency × 0.10) +
             (Low_FP_Rate × 0.10)
```

**Section 4: Relationship Mapping**

**Entity Relationships:**
- Indicator-to-indicator relationships
- Indicator-to-malware relationships
- Indicator-to-actor relationships
- Indicator-to-campaign relationships
- Infrastructure relationships

**Graph Analysis:**
- Pivot point identification
- Connected component analysis
- Temporal relationship tracking
- Infrastructure clustering

**Section 5: Actionable Output**

**Detection Rules:**
- SIEM query generation
- YARA rule creation
- Sigma rule development
- Snort/Suricata rules
- Custom detection logic

**Blocking Recommendations:**
- Firewall block recommendations
- DNS sinkhole configurations
- Email gateway rules
- Proxy block lists

**Intelligence Reports:**
- Executive summary format
- Technical analysis detail
- MITRE ATT&CK mapping
- Timeline construction
- Remediation guidance

**Output Requirements:**
- Enriched indicator report
- Confidence score documentation
- Relationship graph
- Detection rule set
- Actionable recommendations
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت محلل استخبارات تهديدات تجري تحليل IOC. طور إطاراً شاملاً لتحليل المؤشرات:

**القسم 1: تصنيف المؤشرات**

**أنواع المؤشرات:**
- مؤشرات الشبكة (IP، نطاق، URL، بريد إلكتروني)
- مؤشرات الملفات (تجزئة، اسم ملف، مسار)
- مؤشرات المضيف (سجل، mutex، خدمة)
- مؤشرات سلوكية (نمط، TTP)
- مؤشرات تشفير (شهادة، مفتاح)

**معايير التصنيف:**
- تصنيف نوع التهديد
- مؤشرات إسناد الجهة
- ارتباط الحملة
- ربط عائلة البرمجيات الخبيثة
- تصنيف البنية التحتية

**القسم 2: الإثراء السياقي**

**مؤشرات الشبكة:**
- بيانات تسجيل WHOIS
- تاريخ تحليل DNS
- تحليل شهادات SSL
- ASN وتخصيص الشبكة
- DNS السلبي التاريخي
- فحص المنافذ والخدمات
- الموقع الجغرافي

**مؤشرات الملفات:**
- نتائج التحليل الثابت
- تقارير صندوق رمل التحليل الديناميكي
- تحليل جدول الاستيراد
- استخراج النصوص
- تحديد أداة التغليف
- طوابع وقت الترجمة
- التحقق من التوقيع الرقمي

**المؤشرات السلوكية:**
- ربط تقنيات MITRE ATT&CK
- تحديد مرحلة سلسلة القتل
- تصنيف الأدوات
- ارتباط قواعد الكشف

**القسم 3: تسجيل الثقة**

**عوامل التسجيل:**
- موثوقية المصدر (مقياس 1-5)
- التأكيد من مصادر متعددة
- عمر المؤشر
- خصوصية السياق
- تاريخ الإيجابيات الكاذبة

**مستويات الثقة:**
- عالي (80-100): مؤكد ضار
- متوسط (50-79): محتمل ضار
- منخفض (20-49): مشبوه
- غير معروف (0-19): بيانات غير كافية

**خوارزمية التسجيل:**
```
الثقة = (موثوقية_المصدر × 0.25) +
        (التأكيد × 0.30) +
        (مطابقة_السياق × 0.25) +
        (الحداثة × 0.10) +
        (معدل_إيجابيات_كاذبة_منخفض × 0.10)
```

**القسم 4: رسم خريطة العلاقات**

**علاقات الكيانات:**
- علاقات المؤشر بالمؤشر
- علاقات المؤشر بالبرمجيات الخبيثة
- علاقات المؤشر بالجهة
- علاقات المؤشر بالحملة
- علاقات البنية التحتية

**تحليل الرسم البياني:**
- تحديد نقطة التحول
- تحليل المكون المتصل
- تتبع العلاقات الزمنية
- تجميع البنية التحتية

**القسم 5: المخرجات القابلة للتنفيذ**

**قواعد الكشف:**
- توليد استعلام SIEM
- إنشاء قواعد YARA
- تطوير قواعد Sigma
- قواعد Snort/Suricata
- منطق كشف مخصص

**توصيات الحظر:**
- توصيات حظر جدار الحماية
- تكوينات حفرة DNS
- قواعد بوابة البريد الإلكتروني
- قوائم حظر الوكيل

**تقارير الاستخبارات:**
- تنسيق الملخص التنفيذي
- تفاصيل التحليل التقني
- ربط MITRE ATT&CK
- بناء الجدول الزمني
- إرشادات المعالجة

**متطلبات المخرجات:**
- تقرق المؤشر المُثرى
- توثيق درجة الثقة
- رسم بياني للعلاقات
- مجموعة قواعد الكشف
- توصيات قابلة للتنفيذ
```

---

## Example Output Preview

```
# IOC Analysis Report

## Indicator Overview
**Indicator:** 192.0.2.1
**Type:** IPv4 Address
**First Seen:** 2024-01-10
**Last Seen:** 2024-01-15
**Confidence Score:** 92/100 (High)

## Enrichment Results

### WHOIS Data
| Field | Value |
|-------|-------|
| Organization | Unknown Hosting Provider |
| Country | [REDACTED] |
| ASN | AS12345 |
| Allocation Date | 2023-06-15 |
| Abuse Contact | abuse@unknownhost.example |

### DNS Resolution History
| Date | Resolution | Type |
|------|------------|------|
| 2024-01-15 | malicious-domain.com | A |
| 2024-01-14 | c2-server.net | A |
| 2024-01-12 | update-service.xyz | A |

### SSL Certificates
```
Subject: CN=update-service.xyz
Issuer: Let's Encrypt
Valid From: 2024-01-01
Valid To: 2024-04-01
SHA256: a1b2c3d4e5f6...
```

### Threat Intelligence Correlation
| Source | Verdict | Confidence | Context |
|--------|---------|------------|---------|
| VirusTotal | Malicious | 15/72 vendors | C2 detected |
| AlienVault | Malicious | High | APT campaign |
| MISP | Malicious | High | Actor: APT-X |
| Internal | Malicious | Confirmed | Active incident |

## Confidence Score Breakdown

| Factor | Weight | Score | Weighted |
|--------|--------|-------|----------|
| Source Reliability | 25% | 4/5 | 20% |
| Corroboration | 30% | 4 sources | 28% |
| Context Match | 25% | High | 24% |
| Recency | 10% | <7 days | 10% |
| Low FP Rate | 10% | None | 10% |
| **Total** | **100%** | | **92%** |

## Relationship Graph

```
192.0.2.1 (IP)
├── Resolves to ──► malicious-domain.com (Domain)
│   └── SSL Cert ──► CN=update-service.xyz
├── Communicated from ──► Hash:a1b2c3d4 (Malware)
│   └── Dropped by ──► Phishing Campaign Q1-2024
├── Related to ──► 198.51.100.1 (Same ASN)
│   └── Used by ──► APT Group X
└── Part of ──► Campaign: Operation Stealth
```

## MITRE ATT&CK Mapping
| Technique | ID | Use |
|-----------|-----|-----|
| Command and Control | T1071 | HTTPS C2 communication |
| Application Layer Protocol | T1071.001 | Web protocols |
| Standard Application Layer Protocol | T1071.001 | HTTPS |

## Detection Rules

### YARA Rule
```yara
rule APT_X_C2_IP {
    meta:
        author = "Threat Intel Team"
        date = "2024-01-15"
        threat_actor = "APT-X"
        confidence = "High"
        
    strings:
        $ip1 = "192.0.2.1" wide
        $domain1 = "malicious-domain.com" wide
        $domain2 = "c2-server.net" wide
        
    condition:
        any of them
}
```

### Sigma Rule
```yaml
title: APT-X C2 Communication
id: a1b2c3d4-5678-90ab-cdef-1234567890ab
status: stable
description: Detects communication with APT-X C2 infrastructure
author: Threat Intel Team
date: 2024/01/15
logsource:
    category: network_connection
    product: firewall
detection:
    selection:
        dst_ip:
            - 192.0.2.1
            - 198.51.100.1
        dst_port:
            - 443
            - 8443
    condition: selection
fields:
    - src_ip
    - dst_ip
    - dst_port
    - bytes_sent
    - bytes_received
level: critical
tags:
    - attack.command_and_control
    - attack.t1071.001
```

## Actionable Recommendations

### Immediate Actions
1. **Block** IP 192.0.2.1 at perimeter firewall
2. **Alert** on any internal communication to this IP
3. **Hunt** for associated domains in DNS logs
4. **Review** any endpoint with historical connections

### SIEM Query (Splunk)
```splunk
index=firewall OR index=proxy dest_ip=192.0.2.1 
| stats count by src_ip, dest_port, _time
| table _time, src_ip, dest_port, count
```

### Blocking Configuration
```
# Firewall Block Rule
access-list threat_intel extended deny ip any host 192.0.2.1 log
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

## Prompt 3: Threat Feed Management

### Description
Manage and optimize threat intelligence feeds including source evaluation, feed processing, quality monitoring, and feed lifecycle management.

### Tags
`threat-feeds` `feed-management` `source-evaluation` `quality-monitoring` `intelligence-feeds`

---

## 🇬🇧 English Prompt

```
You are a threat intelligence manager responsible for feed management. Develop a comprehensive threat feed management framework:

**Section 1: Feed Source Evaluation**

**Evaluation Criteria:**
- Source reliability and reputation
- Data freshness and update frequency
- Indicator types and coverage
- Geographic and sector relevance
- False positive rate history
- Cost vs. value assessment

**Source Categories:**
- Open source feeds (free, community-driven)
- Commercial feeds (paid, curated)
- Government feeds (CISA, NCSC, ENISA)
- Industry feeds (ISACs, sector-specific)
- Internal feeds (from security operations)

**Evaluation Matrix:**
| Criteria | Weight | Score (1-5) | Weighted |
|----------|--------|-------------|----------|
| Accuracy | 30% | - | - |
| Timeliness | 20% | - | - |
| Coverage | 20% | - | - |
| Relevance | 15% | - | - |
| Integration | 15% | - | - |

**Section 2: Feed Processing Pipeline**

**Ingestion Configuration:**
- Pull vs. push mechanisms
- Authentication requirements
- Rate limiting handling
- Error handling and retry logic
- Schema validation

**Normalization Process:**
- Indicator format standardization
- Timestamp normalization (UTC)
- Confidence score mapping
- TLP marking assignment
- Tag harmonization

**De-duplication Logic:**
- Exact match detection
- Fuzzy matching for domains
- Hash collision handling
- Cross-feed deduplication
- Historical overlap analysis

**Section 3: Quality Monitoring**

**Metrics Collection:**
- Daily indicator volume
- Unique vs. duplicate ratio
- False positive reports
- Mean time to detection
- Indicator overlap with other feeds

**Quality Indicators:**
- Freshness score (age distribution)
- Actionability rate
- Detection hit rate
- Analyst feedback score
- Alert-to-incident ratio

**Alerting Thresholds:**
- Volume spike detection
- Stale feed detection
- Error rate monitoring
- Latency alerts

**Section 4: Feed Lifecycle Management**

**Onboarding Process:**
- Trial period evaluation
- Integration testing
- False positive baseline
- Documentation requirements
- Stakeholder approval

**Operational Management:**
- Daily health checks
- Weekly quality reviews
- Monthly performance reports
- Quarterly source reviews
- Annual contract renewals

**Deprecation Process:**
- Performance degradation triggers
- Alternative source identification
- Stakeholder notification
- Graceful removal
- Historical data retention

**Section 5: Optimization Strategies**

**Feed Prioritization:**
- Tiered importance classification
- Processing order optimization
- Resource allocation
- Critical feed redundancy

**Cost Optimization:**
- Overlap analysis for consolidation
- Free vs. paid evaluation
- Usage-based pricing analysis
- Bulk indicator purchases

**Performance Tuning:**
- Parallel processing optimization
- Caching strategies
- Incremental updates
- Query optimization

**Output Requirements:**
- Feed evaluation template
- Processing pipeline documentation
- Quality dashboard specifications
- Lifecycle management procedures
- Optimization recommendations
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت مدير استخبارات تهديدات مسؤول عن إدارة التغذيات. طور إطاراً شاملاً لإدارة تغذيات التهديدات:

**القسم 1: تقييم مصادر التغذية**

**معايير التقييم:**
- موثوقية وسمعة المصدر
- حداثة البيانات وتكرار التحديث
- أنواع المؤشرات والتغطية
- الصلة الجغرافية والقطاعية
- تاريخ معدل الإيجابيات الكاذبة
- تقييم التكلفة مقابل القيمة

**فئات المصادر:**
- تغذيات مفتوحة المصدر (مجانية، يقودها المجتمع)
- تغذيات تجارية (مدفوعة، منسقة)
- تغذيات حكومية (CISA, NCSC, ENISA)
- تغذيات صناعية (ISACs، خاصة بالقطاع)
- تغذيات داخلية (من عمليات الأمن)

**مصفوفة التقييم:**
| المعيار | الوزن | الدرجة (1-5) | المرجح |
|---------|-------|--------------|--------|
| الدقة | 30% | - | - |
| الحداثة | 20% | - | - |
| التغطية | 20% | - | - |
| الصلة | 15% | - | - |
| التكامل | 15% | - | - |

**القسم 2: خط أنابيب معالجة التغذية**

**تكوين الاستيعاب:**
- آليات السحب مقابل الدفع
- متطلبات المصادقة
- التعامل مع تحديد المعدل
- معالجة الأخطاء ومنطق إعادة المحاولة
| التحقق من المخطط

**عملية التطبيع:**
- توحيد تنسيق المؤشر
| تطبيع الطابع الزمني (UTC)
| تعيين درجة الثقة
| تعيين علامات TLP
| تنسيق العلامات

**منطق إزالة التكرار:**
- كشف المطابقة التامة
- المطابقة الغامضة للنطاقات
- التعامل مع تصادم التجزئة
- إزالة التكرار عبر التغذيات
- تحليل التداخل التاريخي

**القسم 3: مراقبة الجودة**

**جمع المقاييس:**
- حجم المؤشرات اليومي
- نسبة الفريد مقابل المكرر
- تقارير الإيجابيات الكاذبة
- متوسط وقت الكشف
- تداخل المؤشر مع تغذيات أخرى

**مؤشرات الجودة:**
- درجة الحداثة (توزيع العمر)
- معدل القابلية للتنفيذ
- معدل إصابة الكشف
- درجة تغذية المحلل الراجعة
- نسبة التنبيه إلى الحادث

**عتبات التنبيه:**
- كشف ارتفاع الحجم
- كشف التغذية القديمة
- مراقبة معدل الخطأ
| تنبيهات زمن الانتقال

**القسم 4: إدارة دورة حياة التغذية**

**عملية الإدخال:**
- تقييم فترة التجربة
- اختبار التكامل
- خط أساس الإيجابيات الكاذبة
- متطلبات التوثيق
| موافقة أصحاب المصلحة

**الإدارة التشغيلية:**
- فحوصات الصحة اليومية
| مراجعات الجودة الأسبوعية
| تقارير الأداء الشهرية
| مراجعات المصدر الفصلية
| تجديدات العقود السنوية

**عملية الإلغاء:**
| محفزات تدهور الأداء
| تحديد المصادر البديلة
| إشعار أصحاب المصلحة
| الإزالة السلسة
| الاحتفاظ بالبيانات التاريخية

**القسم 5: استراتيجيات التحسين**

**أولوية التغذية:**
| تصنيف الأهمية المتدرجة
| تحسين ترتيب المعالجة
| تخصيص الموارد
| تكرار التغذية الحرجة

**تحسين التكلفة:**
| تحليل التداخل للدمج
| تقييم المجاني مقابل المدفوع
| تحليل التسعير القائم على الاستخدام
| مشتريات المؤشرات بالجملة

**ضبط الأداء:**
| تحسين المعالجة المتوازية
| استراتيجيات التخزين المؤقت
| التحديثات التزايدية
| تحسين الاستعلام

**متطلبات المخرجات:**
| قالب تقييم التغذية
| توثيق خط أنابيب المعالجة
| مواصفات لوحة جودة المعلومات
| إجراءات إدارة دورة الحياة
| توصيات التحسين
```

---

## Example Output Preview

```
# Threat Feed Management Report

## Feed Inventory Summary

### Active Feeds by Category
| Category | Count | Daily Volume | Coverage |
|----------|-------|--------------|----------|
| Commercial | 5 | 15,000 | Global |
| Government | 3 | 2,500 | US/EU |
| ISAC | 2 | 1,200 | Sector |
| Open Source | 8 | 25,000 | Global |
| Internal | 3 | 500 | Custom |
| **Total** | **21** | **44,200** | - |

## Feed Quality Dashboard

### Performance Metrics (Last 30 Days)
| Feed Name | Volume | Unique % | FP Rate | Age (hrs) | Score |
|-----------|--------|----------|---------|-----------|-------|
| Commercial-A | 5,200 | 78% | 2.1% | 4.2 | 4.5/5 |
| Commercial-B | 4,800 | 82% | 1.8% | 6.1 | 4.6/5 |
| Open-OTX | 8,500 | 65% | 5.2% | 12.3 | 3.8/5 |
| CISA-Feed | 800 | 91% | 0.9% | 2.5 | 4.8/5 |
| ISAC-Financial | 600 | 88% | 1.2% | 3.8 | 4.7/5 |

### Quality Trend Analysis
```
Feed Quality Score (Last 90 Days)
Month    | Commercial | Open Source | Government
---------|------------|-------------|------------
Oct 2023 | 4.4        | 3.9         | 4.6
Nov 2023 | 4.5        | 3.7         | 4.7
Dec 2023 | 4.6        | 3.8         | 4.8
Jan 2024 | 4.5        | 3.8         | 4.8
```

## Feed Overlap Analysis

### Indicator Overlap Matrix
| Feed | A | B | C | D | E |
|------|---|---|---|---|---|
| A | - | 45% | 32% | 18% | 12% |
| B | 45% | - | 28% | 22% | 15% |
| C | 32% | 28% | - | 35% | 20% |
| D | 18% | 22% | 35% | - | 25% |
| E | 12% | 15% | 20% | 25% | - |

### Consolidation Opportunity
- Feeds B and C have 45% overlap - consider consolidation
- Feed D provides unique 25% not covered elsewhere
- Open source feeds overlap significantly with commercial

## Processing Pipeline Status

### Pipeline Health
| Stage | Status | Latency | Errors |
|-------|--------|---------|--------|
| Ingestion | ✅ Healthy | 2.3s | 0.1% |
| Normalization | ✅ Healthy | 1.5s | 0.2% |
| Enrichment | ⚠️ Warning | 8.2s | 1.2% |
| De-duplication | ✅ Healthy | 3.1s | 0.0% |
| Distribution | ✅ Healthy | 1.8s | 0.0% |

### Recent Alerts
```
[2024-01-15 10:23] WARNING: Enrichment latency above threshold (8.2s > 5s)
[2024-01-15 08:45] INFO: Feed Commercial-C volume spike detected (+150%)
[2024-01-14 23:00] ALERT: Open-Source-D feed stale (no update in 48h)
```

## Feed Lifecycle Actions

### Recommended Actions
| Feed | Action | Reason | Priority |
|------|--------|--------|----------|
| Open-Source-D | Investigate | Stale for 48 hours | High |
| Commercial-B | Renew | Contract expires Feb 2024 | Medium |
| Open-OTX | Tune | High FP rate (5.2%) | Medium |
| New-Feed-X | Trial | Evaluate for coverage gaps | Low |

### Cost Optimization
| Optimization | Current Cost | Projected Savings |
|--------------|--------------|-------------------|
| Consolidate B+C | $50K/year | $15K/year |
| Reduce open source | $0 | 20% processing |
| Negotiate volume | - | $8K/year |

## Feed Evaluation Template

### New Feed Assessment: [Feed Name]
| Criteria | Weight | Score | Weighted | Notes |
|----------|--------|-------|----------|-------|
| Accuracy | 30% | 4 | 1.2 | Low FP rate |
| Timeliness | 20% | 5 | 1.0 | <1hr latency |
| Coverage | 20% | 4 | 0.8 | Good sector focus |
| Relevance | 15% | 5 | 0.75 | Highly relevant |
| Integration | 15% | 4 | 0.6 | Standard API |
| **Total** | **100%** | - | **4.35/5** | **Recommend** |
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 4: Threat Actor Profiling

### Description
Create comprehensive threat actor profiles including capability assessment, motivation analysis, and predictive threat modeling.

### Tags
`threat-actor` `actor-profiling` `capability-assessment` `motivation-analysis` `threat-modeling`

---

## 🇬🇧 English Prompt

```
You are a threat intelligence analyst developing threat actor profiles. Create a comprehensive actor profiling framework:

**Section 1: Actor Identification**

**Naming & Tracking:**
- Actor naming conventions
- Alias and cluster tracking
- Attribution chain documentation
- Naming conflicts resolution
- Historical name changes

**Identification Indicators:**
- Unique TTP combinations
- Infrastructure fingerprints
- Tool signatures
- Linguistic markers
- Operational patterns

**Section 2: Capability Assessment**

**Technical Capabilities:**
- Exploit development capability
- Zero-day acquisition/development
- Malware development sophistication
- OPSEC practices
- Infrastructure management

**Operational Capabilities:**
- Target selection methodology
- Campaign planning sophistication
- Persistence duration
- Data exfiltration techniques
- Financial laundering methods

**Capability Maturity Model:**
| Level | Description | Characteristics |
|-------|-------------|-----------------|
| 1 | Script Kiddie | Uses existing tools only |
| 2 | Opportunistic | Modifies existing tools |
| 3 | Advanced | Custom tools, good OPSEC |
| 4 | APT | Zero-days, nation-state |
| 5 | Elite | Novel techniques, persistent |

**Section 3: Motivation Analysis**

**Motivation Categories:**
- Financial (cybercrime, ransomware)
- Espionage (corporate, state)
- Hacktivism (political, social)
- Destruction (sabotage, warfare)
- Thrill-seeking (challenge, recognition)

**Behavioral Indicators:**
- Target selection patterns
- Timing of operations
- Public statements/releases
- Negotiation behavior
| Data handling practices

**Section 4: Targeting Analysis**

**Victim Selection:**
- Geographic preferences
- Industry sector targeting
| Organization size preference
| Technology stack preferences
| High-value asset identification

**Attack Patterns:**
- Initial access methods
| Lateral movement preferences
| Data exfiltration timing
| Persistence mechanisms
| Impact delivery methods

**Section 5: Predictive Modeling**

**Behavioral Prediction:**
- Operational cycle analysis
| Seasonal activity patterns
| Response to exposure
| Adaptation capabilities
| Likely future targets

**Risk Assessment:**
- Threat level to organization
| Exposure probability
| Impact potential
| Defense gap analysis
| Prioritized mitigation

**Output Requirements:**
- Actor profile document
| Capability matrix
| Motivation assessment
| Targeting pattern analysis
| Predictive threat model
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت محلل استخبارات تهديدات تطور ملفات تعريف جهات التهديد. أنشئ إطاراً شاملاً لتنميط الجهات:

**القسم 1: تحديد الجهة**

**التسمية والتتبع:**
- اصطلاحات تسمية الجهات
| تتبع الأسماء المستعارة والمجموعات
| توثيق سلسلة الإسناد
| حل تضاربات التسمية
| التغييرات التاريخية للأسماء

**مؤشرات التحديد:**
- مجموعات TTP الفريدة
| بصمات البنية التحتية
| تواقيع الأدوات
| العلامات اللغوية
| الأنماط التشغيلية

**القسم 2: تقييم القدرات**

**القدرات التقنية:**
- قدرة تطوير الاستغلال
| الحصول على/تطوير ثغرات اليوم الصفري
| تطور تطوير البرمجيات الخبيثة
| ممارسات OPSEC
| إدارة البنية التحتية

**القدرات التشغيلية:**
- منهجية اختيار الهدف
| تطور تخطيط الحملات
| مدة الاستمرار
| تقنيات نشر البيانات
| طرق غسيل الأموال

**نموذج نضج القدرات:**
| المستوى | الوصف | الخصائص |
|---------|-------|---------|
| 1 | هاوي | يستخدم الأدوات الموجودة فقط |
| 2 | انتهازي | يعدل الأدوات الموجودة |
| 3 | متقدم | أدوات مخصصة، OPSEC جيد |
| 4 | APT | ثغرات يوم صفري، حكومي |
| 5 | نخبة | تقنيات جديدة، مستمر |

**القسم 3: تحليل الدوافع**

**فئات الدوافع:**
- مالي (جرائم إلكترونية، فدية)
| تجسس (شركات، دول)
| ناشط إلكتروني (سياسي، اجتماعي)
| تدمير (تخريب، حرب)
| البحث عن الإثارة (تحدي، شهرة)

**المؤشرات السلوكية:**
- أنماط اختيار الهدف
| توقيت العمليات
| التصريحات/الإصدارات العامة
| سلوك التفاوض
| ممارسات التعامل مع البيانات

**القسم 4: تحليل الاستهداف**

**اختيار الضحية:**
- التفضيلات الجغرافية
| استهداف القطاع الصناعي
| تفضيل حجم المنظمة
| تفضيلات مجموعة التقنيات
| تحديد الأصول عالية القيمة

**أنماط الهجوم:**
- طرق الوصول الأولي
| تفضيلات الحركة الجانبية
| توقيت نشر البيانات
| آليات الاستمرار
| طرق تسليم التأثير

**القسم 5: النمذجة التنبؤية**

**التنبؤ السلوكي:**
- تحليل الدورة التشغيلية
| الأنماط الموسمية للنشاط
| الاستجابة للكشف
| قدرات التكيف
| الأهداف المستقبلية المحتملة

**تقييم المخاطر:**
- مستوى التهديد للمنظمة
| احتمالية التعرض
| الأثر المحتمل
| تحليل فجوات الدفاع
| التخفيف ذو الأولوية

**متطلبات المخرجات:**
- وثيقة ملف الجهة
| مصفوفة القدرات
| تقييم الدوافع
| تحليل أنماط الاستهداف
| نموذج التهديد التنبؤي
```

---

## Example Output Preview

```
# Threat Actor Profile

## Actor Overview
**Designation:** APT-X (Also known as: Group Alpha, Stealth Panda)
**First Observed:** 2018
**Last Activity:** January 2024
**Threat Level:** Critical

## Identification Summary
| Attribute | Details |
|-----------|---------|
| Primary Alias | APT-X |
| Secondary Aliases | Group Alpha, Stealth Panda, TA-001 |
| Suspected Attribution | Nation-State (Region: [REDACTED]) |
| Confidence | Medium (72%) |

## Capability Assessment

### Technical Capabilities
| Capability | Level | Evidence |
|------------|-------|----------|
| Exploit Development | Advanced | 3 zero-days used (2020-2023) |
| Malware Development | Advanced | Custom RATs, rootkits |
| OPSEC | High | Infrastructure rotation, encryption |
| Tool Sophistication | Advanced | Custom tooling, minimal reuse |
| Persistence | Advanced | Firmware implants, supply chain |

### Capability Matrix
```
Technical Sophistication: ████████░░ (80%)
Operational Security:     ███████░░░ (70%)
Resource Level:           █████████░ (90%)
Adaptability:             ████████░░ (80%)
Persistence:              █████████░ (90%)
```

### Capability Maturity: Level 4 (APT)

## Motivation Analysis

### Primary Motivation: Cyber Espionage
- Government and diplomatic target focus
- Long-term persistence in networks
- Intellectual property theft
- Strategic intelligence collection

### Secondary Motivation: Financial Intelligence
- Banking sector targeting
- Cryptocurrency exchange operations
- Payment processor infiltration

### Behavioral Indicators
| Indicator | Observed | Pattern |
|-----------|----------|---------|
| Target Selection | Strategic | Government, Defense, Tech |
| Timing | Business Hours | UTC+8 timezone aligned |
| Public Statements | Minimal | No claimed operations |
| Data Handling | Exfil Only | No destructive operations |
| Adaptation | Moderate | Tool updates after exposure |

## Targeting Analysis

### Geographic Preferences
| Region | Activity Level | Sectors |
|--------|---------------|---------|
| North America | High | Defense, Tech, Finance |
| Europe | Medium | Government, Energy |
| Asia-Pacific | High | Manufacturing, Tech |
| Middle East | Medium | Energy, Government |

### Industry Targeting
```
Defense/Aerospace  ████████████ (35%)
Technology         ██████████░░ (28%)
Financial          ██████░░░░░ (18%)
Government         ████░░░░░░░ (12%)
Energy             ██░░░░░░░░░ (7%)
```

### Attack Pattern Summary
| Phase | Techniques | Notes |
|-------|------------|-------|
| Initial Access | Supply chain, Watering hole, Phishing | |
| Execution | Custom backdoor, PowerShell | |
| Persistence | Registry, Scheduled tasks, Bootkit | |
| Lateral Movement | RDP, PsExec, Pass-the-Hash | |
| Exfiltration | Custom protocol over HTTPS | Slow and steady |

## Predictive Modeling

### Operational Cycle Analysis
```
Average Campaign Duration: 14 months
Reconnaissance Phase: 2-3 months
Initial Access: 1 week
Persistence Establishment: 1 month
Data Collection: 6-8 months
Exfiltration: 2-3 months
Cool-down Period: 2-4 months
```

### Seasonal Activity Patterns
- Increased activity Q1 (January-March)
- Major operations aligned with geopolitical events
- Reduced activity during regional holidays

### Likely Future Targets
1. **High Probability:** Emerging technology companies (AI/ML)
2. **Medium Probability:** Healthcare research organizations
3. **Elevated Risk:** Critical infrastructure operators

## Risk Assessment for Organization

| Factor | Score | Assessment |
|--------|-------|------------|
| Threat Level | Critical | In targeting profile |
| Exposure Probability | High | Industry match |
| Impact Potential | Severe | IP at risk |
| Current Defense | Moderate | Gap in supply chain |

### Recommended Priorities
1. Enhance supply chain security monitoring
2. Implement additional network segmentation
3. Deploy advanced threat detection for custom backdoors
4. Conduct threat hunting for known TTPs
5. Enhance logging for lateral movement detection
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 5: Strategic Intelligence Reporting

### Description
Develop strategic threat intelligence reports for executive leadership including trend analysis, risk assessment, and strategic recommendations.

### Tags
`strategic-intelligence` `executive-reporting` `trend-analysis` `risk-assessment` `strategic-recommendations`

---

## 🇬🇧 English Prompt

```
You are a strategic threat intelligence analyst preparing executive-level reports. Develop a comprehensive strategic reporting framework:

**Section 1: Executive Summary Development**

**Key Components:**
- Threat landscape overview (1-2 paragraphs)
- Critical findings summary (bullet points)
| Risk level assessment (color-coded)
| Key trends and patterns
| Recommended actions (prioritized)

**Communication Style:**
- Business-focused language
| Quantified impact where possible
| Clear and concise messaging
| Visual aids (charts, graphs)
| Actionable recommendations

**Section 2: Threat Trend Analysis**

**Temporal Trends:**
- Year-over-year comparison
| Quarterly trend analysis
| Seasonal pattern identification
| Emerging vs. declining threats

**Threat Category Trends:**
- Ransomware evolution
| Supply chain attacks
| Cloud security threats
| Identity-based attacks
| IoT/OT security threats

**Geographic Trends:**
- Regional threat actor activity
| Geographic targeting shifts
| Regulatory landscape changes
| Cross-border threat patterns

**Section 3: Industry-Specific Analysis**

**Sector Threat Profiles:**
- Threat actors targeting sector
| Common attack vectors
| Notable incidents in industry
| Regulatory implications

**Competitive Intelligence:**
- Peer organization incidents
| Industry-wide vulnerabilities
| Shared infrastructure risks

**Section 4: Risk Assessment Framework**

**Risk Matrix Development:**
| Probability | Impact | Risk Score |
|-------------|--------|------------|
| High (3) | High (3) | Critical (9) |
| High (3) | Medium (2) | High (6) |
| Medium (2) | High (3) | High (6) |
| Medium (2) | Medium (2) | Medium (4) |
| Low (1) | Any | Low (1-3) |

**Risk Factors:**
- Industry exposure level
| Geographic presence
| Technology stack vulnerabilities
| Partner/supply chain dependencies
| Regulatory requirements

**Section 5: Strategic Recommendations**

**Investment Priorities:**
- Security control gaps
| Technology investments
| People and training needs
| Process improvements

**Strategic Initiatives:**
- Multi-year roadmap items
| Industry collaboration opportunities
| Regulatory compliance enhancements
| Security culture improvements

**Metrics & KPIs:**
- Risk reduction metrics
| Security maturity indicators
| Incident trend measurements
| Investment ROI indicators

**Output Requirements:**
- Executive summary (1 page)
| Detailed trend analysis
| Industry threat profile
| Risk assessment matrix
| Strategic recommendations
| Appendix with technical details
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت محلل استخبارات تهديدات استراتيجية تعد تقارير على المستوى التنفيذي. طور إطاراً شاملاً للتقارير الاستراتيجية:

**القسم 1: تطوير الملخص التنفيذي**

**المكونات الرئيسية:**
- نظرة عامة على مشهد التهديدات (1-2 فقرة)
| ملخص النتائج الحرجة (نقاط نقطية)
| تقييم مستوى المخاطر (مُرمز بالألوان)
| الاتجاهات والأنماط الرئيسية
| الإجراءات الموصى بها (مُرتبة حسب الأولوية)

**أسلوب الاتصال:**
- لغة تركز على الأعمال
| تأثير كمي حيثما أمكن
| رسائل واضحة وموجزة
| وسائل مساعدة بصرية (مخططات، رسوم بيانية)
| توصيات قابلة للتنفيذ

**القسم 2: تحليل اتجاهات التهديدات**

**الاتجاهات الزمنية:**
- مقارنة سنة بسنة
| تحليل الاتجاهات الفصلية
| تحديد الأنماط الموسمية
| التهديدات الناشئة مقابل المتدهورة

**اتجاهات فئات التهديدات:**
- تطور برمجيات الفدية
| هجمات سلسلة التوريد
| تهديدات أمن السحابة
| هجمات قائمة على الهوية
| تهديدات أمن IoT/OT

**الاتجاهات الجغرافية:**
- نشاط جهات التهديد الإقليمية
| تحولات الاستهداف الجغرافي
| تغييرات المشهد التنظيمي
| أنماط التهديدات عبر الحدود

**القسم 3: تحليل خاص بالصناعة**

**ملفات تهديدات القطاع:**
- جهات التهديد التي تستهدف القطاع
| نواقل الهجوم الشائعة
| الحوادث البارزة في الصناعة
| الآثار التنظيمية

**الاستخبارات التنافسية:**
- حوادث المنظمات النظيرة
| نقاط الضعف على مستوى الصناعة
| مخاطر البنية التحتية المشتركة

**القسم 4: إطار تقييم المخاطر**

**تطوير مصفوفة المخاطر:**
| الاحتمالية | الأثر | درجة المخاطرة |
|------------|-------|---------------|
| عالية (3) | عالية (3) | حرجة (9) |
| عالية (3) | متوسطة (2) | عالية (6) |
| متوسطة (2) | عالية (3) | عالية (6) |
| متوسطة (2) | متوسطة (2) | متوسطة (4) |
| منخفضة (1) | أي | منخفضة (1-3) |

**عوامل المخاطر:**
- مستوى التعرض الصناعي
| الوجود الجغرافي
| نقاط ضعف مجموعة التقنيات
| تبعات الشركاء/سلسلة التوريد
| المتطلبات التنظيمية

**القسم 5: التوصيات الاستراتيجية**

**أولويات الاستثمار:**
- فجوات الضوابط الأمنية
| الاستثمارات التقنية
| احتياجات الأفراد والتدريب
| تحسينات العمليات

**المبادرات الاستراتيجية:**
- بنود خارطة الطريق متعددة السنوات
| فرص التعاون الصناعي
| تعزيزات الامتثال التنظيمي
| تحسينات ثقافة الأمن

**المقاييس ومؤشرات الأداء الرئيسية:**
- مقاييس تقليل المخاطر
| مؤشرات نضج الأمن
| قياسات اتجاهات الحوادث
| مؤشرات العائد على الاستثمار

**متطلبات المخرجات:**
- ملخص تنفيذي (صفحة واحدة)
| تحليل تفصيلي للاتجاهات
| ملف تهديدات الصناعة
| مصفوفة تقييم المخاطر
| توصيات استراتيجية
| ملحق بالتفاصيل التقنية
```

---

## Example Output Preview

```
# Strategic Threat Intelligence Report - Q1 2024

## Executive Summary

The global threat landscape in Q1 2024 demonstrates continued sophistication among nation-state actors and an evolution in ransomware-as-a-service (RaaS) operations. Our analysis indicates a 23% increase in targeted attacks against organizations in our sector, with supply chain compromises emerging as the primary attack vector. Critical vulnerabilities in enterprise software remain a significant risk, with an average of 12 days to weaponization after disclosure.

**Key Findings:**
- Ransomware attacks increased 23% YoY; average ransom demand up 45%
- Supply chain attacks account for 31% of initial access (up from 18%)
- Zero-day exploitation timeline shortened to 12 days average
- Identity-based attacks bypassing traditional perimeter defenses

**Risk Assessment:** 🔴 HIGH (Increased from Medium in Q4 2023)

**Priority Actions:**
1. Implement supply chain security program (30-day initiative)
2. Accelerate identity and access management modernization
3. Enhance vulnerability management SLAs for critical systems

---

## Threat Trend Analysis

### Ransomware Evolution
| Metric | Q4 2023 | Q1 2024 | Change |
|--------|---------|---------|--------|
| Attack Frequency | 156/week | 192/week | +23% |
| Avg Ransom | $1.8M | $2.6M | +45% |
| Dwell Time | 21 days | 14 days | -33% |
| Data Exfil Rate | 78% | 91% | +17% |

```
Ransomware Attack Trend (12 months)
Jan ████████░░░░ 120
Feb █████████░░░ 135
Mar █████████░░░ 140
Apr ██████████░░ 158
May ██████████░░ 162
Jun ███████████░ 175
Jul ███████████░ 178
Aug ████████████ 185
Sep ████████████ 188
Oct ████████████ 190
Nov ████████████ 192
Dec ████████████ 195
```

### Attack Vector Distribution
```
Phishing           ████████░░░░ 28%
Supply Chain       ████████░░░░ 31%
Vulnerability      ██████░░░░░░ 22%
Credential Theft   ████░░░░░░░░ 15%
Other              ██░░░░░░░░░░ 4%
```

---

## Industry Threat Profile

### Sector-Specific Threats
| Threat Actor | Activity Level | Target Focus | Risk |
|--------------|---------------|--------------|------|
| APT-X | High | IP Theft | Critical |
| RaaS-Alpha | Very High | Financial | Critical |
| Cybercrime-Beta | Medium | Data Theft | High |

### Notable Industry Incidents (Q1 2024)
1. **Company A** - Ransomware attack, $4.5M ransom paid
2. **Company B** - Supply chain compromise, 6-month dwell time
3. **Company C** - Data breach, 2M customer records exposed

### Regulatory Landscape
- New SEC cyber disclosure rules effective
- GDPR enforcement actions increased 40%
- Industry-specific regulations pending

---

## Risk Assessment Matrix

### Organizational Risk Profile
| Risk Category | Probability | Impact | Score | Priority |
|---------------|-------------|--------|-------|----------|
| Ransomware | High (3) | Severe (3) | 🔴 9 | 1 |
| Supply Chain | High (3) | High (2) | 🟠 6 | 2 |
| Insider Threat | Medium (2) | High (2) | 🟡 4 | 3 |
| Cloud Misconfig | Medium (2) | Medium (2) | 🟡 4 | 4 |

### Risk Trend Analysis
```
Overall Risk Score Trend
Q1 2023: ████████░░ 8.2 (High)
Q2 2023: ███████░░░ 7.5 (High)
Q3 2023: ██████░░░░ 6.8 (Medium-High)
Q4 2023: ███████░░░ 7.2 (High)
Q1 2024: █████████░ 8.9 (High)
```

---

## Strategic Recommendations

### Investment Priorities (FY2024)
| Initiative | Investment | Risk Reduction | ROI Period |
|------------|------------|----------------|------------|
| Supply Chain Security | $450K | -35% | 12 months |
| Identity Modernization | $800K | -28% | 18 months |
| EDR Enhancement | $200K | -15% | 6 months |
| Security Training | $150K | -12% | Ongoing |

### Strategic Initiatives Roadmap
```
Q2 2024: Supply chain assessment and vendor security program
Q3 2024: Zero-trust architecture phase 1 implementation
Q4 2024: SOC modernization and automation enhancement
Q1 2025: Cloud security posture management deployment
```

### Key Performance Indicators
| KPI | Current | Target | Timeline |
|-----|---------|--------|----------|
| Mean Time to Detect | 72 hrs | 24 hrs | Q4 2024 |
| Vulnerability Remediation (Critical) | 15 days | 3 days | Q3 2024 |
| Phishing Click Rate | 12% | 5% | Q4 2024 |
| MFA Coverage | 78% | 100% | Q2 2024 |

---

## Appendix: Technical Details
*[Detailed technical indicators, IOCs, and TTP mappings available in classified attachment]*
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team
