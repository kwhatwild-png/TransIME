# TransIME - 中英/中越实时翻译输入法 (Android + Jetpack Compose)

基于 **Kotlin + Jetpack Compose** 构建的专用实时翻译输入法应用。

## 🌟 核心特性
- **系统输入法服务**：继承 `InputMethodService`，支持在微信、WhatsApp、浏览器等任意 App 中调起。
- **一键切换翻译模式**：工具栏双向快速切换 `中 ⇄ 英` 与 `中 ⇄ 越`。
- **中文九宫格与全拼**：支持经典 T9 九宫格拼音输入，拼音智能候选，亦支持 26 键全拼。
- **越南语原生键盘**：集成 `Ư, Ơ, Đ, Ê, Ă, Â, Ô` 键位与 `sắc, huyền, hỏi, ngã, nặng` 声调，全面支持 Telex 自动连打合成。
- **超全符号库 (?123)**：收录越南盾 `₫`、人民币 `¥`、数学、括号、特殊箭头与即时 Emoji。
- **双模输入**：软键盘即打即译 + 麦克风原生 `SpeechRecognizer` 三语实时语音转文字。
- **Gemini Flash 智能互译引擎**：语种自动探测，母语级地道口语表达，专为越南语日常称谓（Anh, Em, Chị, Bạn）及语气助词（ạ, dạ, nhé, nha）调优。
- **双栏预览与一键上屏**：上栏显示原文与语言标识，下栏显示 AI 译文，点击“上屏”通过 `InputConnection.commitText` 自动填入宿主应用。
- **主配置页 (Activity)**：包含系统输入法启用引导、Gemini API Key 填写入库与称谓偏好管理。

## 🚀 快速生成 APK
详情请参阅工程根目录下的 **`APK-BUILD-GUIDE.md`**。
