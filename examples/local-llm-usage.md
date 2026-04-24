# Using CyberSec Prompts with Local LLMs | استخدام مطالب الأمن السيبراني مع النماذج المحلية

---

## Overview | نظرة عامة

### English

Local Large Language Models (LLMs) provide privacy and security benefits for sensitive cybersecurity work. This guide covers using prompts with popular local LLMs.

Benefits of Local LLMs:
- Complete data privacy
- No internet required
- Customizable models
- No usage limits
- Compliance-friendly

---

### العربية

توفر النماذج اللغوية الكبيرة المحلية (LLMs) فوائد الخصوصية والأمان للعمل الأمني الحساس. يغطي هذا الدليل استخدام المطالب مع النماذج المحلية الشائعة.

فوائد النماذج المحلية:
- خصوصية كاملة للبيانات
- لا يحتاج إنترنت
- نماذج قابلة للتخصيص
- لا حدود للاستخدام
- متوافق مع الامتثال

---

## Supported Local LLMs | النماذج المحلية المدعومة

| Model | Size | Best For | الحجم الأفضل لـ |
|-------|------|----------|-----------------|
| Llama 3 | 8B-70B | General security tasks | المهام الأمنية العامة |
| Mistral | 7B | Fast analysis | التحليل السريع |
| CodeLlama | 7B-34B | Code review | مراجعة الكود |
| DeepSeek Coder | 6.7B-33B | Secure coding | البرمجة الآمنة |
| WizardLM | 7B-13B | Instruction following | اتباع التعليمات |

---

## Setup Guide | دليل الإعداد

### Using Ollama

```bash
# Install Ollama
curl -fsSL https://ollama.com/install.sh | sh

# Pull a security-focused model
ollama pull llama3:70b

# Run interactive session
ollama run llama3:70b

# Or use API
curl http://localhost:11434/api/generate -d '{
  "model": "llama3:70b",
  "prompt": "Analyze this nmap scan..."
}'
```

### Using LM Studio

1. Download LM Studio from lmstudio.ai
2. Search for security-capable models
3. Download Llama 3 70B or Mistral Large
4. Load model and start chat
5. Copy prompts from repository

---

## Optimizing Prompts for Local LLMs
## تحسين المطالب للنماذج المحلية

### English

Local LLMs may require prompt adjustments:

1. **Simplify Complex Prompts**: Break into smaller parts
2. **Clear Instructions**: Be explicit about format
3. **Provide Examples**: Few-shot learning helps
4. **Iterative Refinement**: Build responses step by step

### العربية

قد تتطلب النماذج المحلية تعديلات المطالب:

1. **بسّط المطالب المعقدة**: قسمها إلى أجزاء أصغر
2. **تعليمات واضحة**: كن صريحاً حول التنسيق
3. **قدم أمثلة**: التعلم من الأمثلة القليلة يساعد
4. **التحسين التكراري**: ابنِ الردود خطوة بخطوة

---

## Example: Adjusted Prompt for Local LLM
## مثال: مطلب معدل للنموذج المحلي

**Original Prompt (GPT-4 Optimized):**
```
Analyze this Nmap scan comprehensively and provide:
1. Service identification
2. CVE mapping
3. Exploitation recommendations
4. Remediation steps
```

**Local LLM Optimized:**
```
Task: Analyze Nmap scan results

Step 1: Identify each open port and its service
Step 2: For each service, list known CVEs
Step 3: Suggest exploitation tools for each vulnerability
Step 4: Provide specific remediation commands

Nmap Output:
[scan results]

Format your response as:
PORT | SERVICE | CVEs | TOOLS | REMEDIATION
```

---

## Performance Tips | نصائح الأداء

### English

1. **GPU Acceleration**: Use CUDA for faster inference
2. **Quantization**: Use 4-bit/8-bit for memory efficiency
3. **Context Window**: Monitor token limits
4. **Batch Processing**: Process multiple prompts together

### العربية

1. **تسريع GPU**: استخدم CUDA لاستدلال أسرع
2. **التكميم**: استخدم 4-bit/8-bit لكفاءة الذاكرة
3. **نافذة السياق**: راقب حدود الرموز
4. **المعالجة الدفعية**: عالج مطالب متعددة معاً

---

## Security Considerations | اعتبارات أمنية

⚠️ **Important**: 
- Keep models updated for security patches
- Isolate local LLM from production systems
- Review outputs before acting on recommendations
- Validate all security suggestions

⚠️ **مهم**:
- حافظ على تحديث النماذج لترقيعات الأمان
- اعزل النموذج المحلي عن أنظمة الإنتاج
- راجع المخرجات قبل التصرف على التوصيات
- تحقق من جميع الاقتراحات الأمنية
