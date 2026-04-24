# Using CyberSec Prompts with ChatGPT | استخدام مطالب الأمن السيبراني مع ChatGPT

---

## Quick Start Guide | دليل البدء السريع

### English

This guide shows you how to effectively use the cybersecurity prompts from this repository with ChatGPT.

#### Step 1: Choose Your Prompt
Browse the `prompts/` directory and select a prompt that matches your needs.

#### Step 2: Copy the Prompt
Copy either the English or Arabic version of the prompt.

#### Step 3: Customize
Replace placeholder text like `[PROVIDE TARGET]` or `[PASTE OUTPUT]` with your actual data.

#### Step 4: Submit
Paste the customized prompt into ChatGPT and review the response.

---

### العربية

يوضح لك هذا الدليل كيفية استخدام مطالب الأمن السيبراني من هذا المستودع مع ChatGPT بفعالية.

#### الخطوة 1: اختر المطلب الخاص بك
تصفح مجلد `prompts/` واختر مطلباً يتناسب مع احتياجاتك.

#### الخطوة 2: انسخ المطلب
انسخ النسخة الإنجليزية أو العربية من المطلب.

#### الخطوة 3: التخصيص
استبدل النص البديل مثل `[قدم الهدف]` أو `[الصق المخرجات]` ببياناتك الفعلية.

#### الخطوة 4: الإرسال
الصق المطلب المخصص في ChatGPT وراجع الرد.

---

## Example Usage | مثال على الاستخدام

### Scenario: Analyzing Nmap Scan Results
### السيناريو: تحليل نتائج فحص Nmap

**Original Prompt (from prompts/pentesting/network-scanning/):**

```
You are a penetration tester analyzing Nmap scan results. I will provide you with the output of an Nmap scan...

Scan Output:
[PASTE YOUR NMAP OUTPUT HERE]
```

**Customized Prompt:**

```
You are a penetration tester analyzing Nmap scan results. I will provide you with the output of an Nmap scan, and you need to:

1. Identify all open ports and their associated services
2. Determine service versions and potential vulnerabilities
3. Suggest CVEs that might apply to each identified service
4. Recommend next steps for further enumeration
5. Provide specific Nmap scripts that could be used for additional reconnaissance

Scan Output:
Starting Nmap 7.94 ( https://nmap.org )
Nmap scan report for 192.168.1.100
Host is up (0.001s latency).

PORT     STATE SERVICE     VERSION
22/tcp   open  ssh         OpenSSH 8.2p1 Ubuntu
80/tcp   open  http        Apache httpd 2.4.41
443/tcp  open  ssl/http    nginx 1.18.0
3306/tcp open  mysql       MySQL 5.7.38

Service detection performed. Please report any incorrect results.
```

**Expected Response Structure:**
- Port analysis with service identification
- CVE recommendations for each service
- Specific enumeration commands
- Risk assessment
- Next steps

---

## Tips for Best Results | نصائح لأفضل النتائج

### English

1. **Be Specific**: Provide detailed information when prompted
2. **Use Real Data**: Replace all placeholders with actual data
3. **Follow Up**: Ask clarifying questions based on the response
4. **Iterate**: Refine prompts based on initial results
5. **Verify**: Always verify AI suggestions before implementation

### العربية

1. **كن محدداً**: قدم معلومات تفصيلية عند طلبها
2. **استخدم بيانات حقيقية**: استبدل جميع البدائل ببيانات فعلية
3. **تابع**: اطرح أسئلة توضيحية بناءً على الرد
4. **كرر**: حسّن المطالب بناءً على النتائج الأولية
5. **تحقق**: تحقق دائماً من اقتراحات الذكاء الاصطناعي قبل التنفيذ

---

## Recommended GPT-4 Settings | إعدادات GPT-4 الموصى بها

- **Model**: GPT-4 or GPT-4 Turbo
- **Temperature**: 0.7 for balanced responses
- **Max Tokens**: 4096 for detailed responses
- **System Prompt**: "You are a cybersecurity expert with deep knowledge of penetration testing, incident response, and security analysis."

---

## Disclaimer | تنصل

⚠️ **Important**: These prompts are for educational and authorized testing purposes only. Always obtain proper authorization before performing any security testing. The authors are not responsible for misuse of this content.

⚠️ **مهم**: هذه المطالب للأغراض التعليمية والاختبار المصرح به فقط. احصل دائماً على إذن مناسب قبل إجراء أي اختبارات أمنية. المؤلفون غير مسؤولين عن سوء استخدام هذا المحتوى.
