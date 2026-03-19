<img width="1299" height="424" alt="cd (1)" src="https://github.com/user-attachments/assets/b25fff4d-043d-4f38-9985-f832ae0d0f6e" />

## Recall.ai - API for desktop recording

If you’re looking for a hosted desktop recording API, consider checking out [Recall.ai](https://www.recall.ai/product/desktop-recording-sdk/?utm_source=github&utm_medium=sponsorship&utm_campaign=sohzm-cheating-daddy), an API that records Zoom, Google Meet, Microsoft Teams, in-person meetings, and more.

This project is sponsored by Recall.ai.

---

> [!NOTE]  
> Use latest MacOS and Windows version, older versions have limited support

> [!NOTE]  
> During testing it wont answer if you ask something, you need to simulate interviewer asking question, which it will answer

A real-time AI assistant that provides contextual help during video calls, interviews, presentations, and meetings using screen capture and audio analysis.

## Features

- **Live AI Assistance**: Real-time help powered by Google Gemini 2.0 Flash Live
- **Screen & Audio Capture**: Analyzes what you see and hear for contextual responses
- **Multiple Profiles**: Interview, Sales Call, Business Meeting, Presentation, Negotiation
- **Transparent Overlay**: Always-on-top window that can be positioned anywhere
- **Click-through Mode**: Make window transparent to clicks when needed
- **Cross-platform**: Works on macOS, Windows, and Linux (kinda, dont use, just for testing rn)

## Setup

1. **Get a Gemini API Key**: Visit [Google AI Studio](https://aistudio.google.com/apikey)
2. **Install Dependencies**: `npm install`
3. **Run the App**: `npm start`

## Usage

1. Enter your Gemini API key in the main window
2. Choose your profile and language in settings
3. Click "Start Session" to begin
4. Position the window using keyboard shortcuts
5. The AI will provide real-time assistance based on your screen and what interview asks

## Keyboard Shortcuts

- **Window Movement**: `Ctrl/Cmd + Arrow Keys` - Move window
- **Click-through**: `Ctrl/Cmd + M` - Toggle mouse events
- **Close/Back**: `Ctrl/Cmd + \` - Close window or go back
- **Send Message**: `Enter` - Send text to AI

## Audio Capture

- **macOS**: [SystemAudioDump](https://github.com/Mohammed-Yasin-Mulla/Sound) for system audio
- **Windows**: Loopback audio capture
- **Linux**: Microphone input

## Telegram（可选）：把手动截图转发到 Telegram

当你在应用里触发**手动截图**（例如快捷键截图用于分析）时，可以选择把同一张截图同步发送到 Telegram。

### 配置方式 A：环境变量（推荐）

启动前设置：

- `TELEGRAM_BOT_TOKEN`
- `TELEGRAM_CHAT_ID`

并把偏好开关打开（见下方“开启开关”）。

### 配置方式 B：写入本地 credentials

编辑配置目录里的 `credentials.json`，增加/填写：

- `telegramBotToken`
- `telegramChatId`

配置目录位置：

- **macOS**: `~/Library/Application Support/cheating-daddy-config/`
- **Windows**: `~/AppData/Roaming/cheating-daddy-config/`
- **Linux**: `~/.config/cheating-daddy-config/`

### 开启开关

编辑同一目录下的 `preferences.json`：

- `sendScreenshotToTelegram`: 设为 `true`

## Requirements

- Electron-compatible OS (macOS, Windows, Linux)
- Gemini API key
- Screen recording permissions
- Microphone/audio permissions
