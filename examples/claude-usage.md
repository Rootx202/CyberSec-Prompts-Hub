# Using CyberSec Prompts with Claude | استخدام مطالب الأمن السيبراني مع Claude

---

## Quick Start Guide | دليل البدء السريع

### English

Claude excels at complex reasoning and detailed technical analysis, making it ideal for cybersecurity prompts requiring deep analysis.

#### Why Claude for Cybersecurity?
- Strong code analysis capabilities
- Excellent at explaining complex concepts
- Good at following structured formats
- Handles long context windows effectively

#### Step-by-Step Usage:
1. Select a prompt from the repository
2. Copy and customize with your data
3. Submit to Claude (claude.ai)
4. Request follow-up analysis as needed

---

### العربية

يتفوق Claude في الاستدلال المعقد والتحليل التقني المفصل، مما يجعله مثالياً للمطالب الأمنية التي تتطلب تحليلاً عميقاً.

#### لماذا Claude للأمن السيبراني؟
- قدرات قوية في تحليل الكود
- ممتاز في شرح المفاهيم المعقدة
- جيد في اتباع التنسيقات المنظمة
- يتعامل مع نوافذ السياق الطويلة بفعالية

---

## Example: Malware Analysis with Claude
## مثال: تحليل البرمجيات الخبيثة مع Claude

**Prompt:**

```
Analyze the following malware sample indicators and provide:
1. Malware family classification
2. Behavior analysis
3. Indicators of Compromise (IOCs)
4. Detection and mitigation recommendations

Sample Details:
MD5: a1b2c3d4e5f6g7h8i9j0
File Type: PE32 executable
Size: 245KB
Imported DLLs: kernel32.dll, user32.dll, ws2_32.dll
Strings: "C2Server", "keylog", "screenshot", "%APPDATA%"
Network: Connects to 192.168.1.100:4444
Registry: HKCU\Software\Microsoft\Windows\CurrentVersion\Run
```

**Expected Claude Response:**
- Detailed malware family analysis
- MITRE ATT&CK mapping
- Network and host-based IOCs
- YARA rules for detection
- Removal recommendations

---

## Best Practices for Claude | أفضل الممارسات لـ Claude

### English

1. **Provide Context**: Claude benefits from detailed context
2. **Request Structured Output**: Ask for specific formats
3. **Iterative Analysis**: Build on previous responses
4. **Code Review**: Claude excels at code security review
5. **Documentation**: Request comprehensive documentation

### العربية

1. **قدم السياق**: Claude يستفيد من السياق المفصل
2. **اطلب مخرجات منظمة**: اطلب تنسيقات محددة
3. **التحليل التكراري**: ابنِ على الردود السابقة
4. **مراجعة الكود**: Claude يتفوق في مراجعة أمان الكود
5. **التوثيق**: اطلب توثيقاً شاملاً

---

## Recommended Claude Settings | إعدادات Claude الموصى بها

- **Model**: Claude 3 Opus or Claude 3.5 Sonnet
- **Temperature**: 0.5-0.7 for technical accuracy
- **Max Output**: 4096 tokens for detailed responses
- **System Prompt**: "You are a cybersecurity expert specializing in threat analysis, penetration testing, and incident response. Provide detailed, technical, and actionable insights."

---

## Advanced Usage: Multi-Turn Analysis
## الاستخدام المتقدم: التحليل متعدد الأدوار

```
Turn 1: Submit initial prompt with scan results
Turn 2: Request specific exploitation techniques
Turn 3: Ask for remediation recommendations
Turn 4: Request executive summary
```

This approach leverages Claude's context retention for comprehensive analysis.

هذا النهج يستفيد من قدرة Claude على الاحتفاظ بالسياق للتحليل الشامل.
