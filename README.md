Quick Start Commands
bash
# Clone repository
git clone https://github.com/shayaanalqua/jarvis

# Navigate to directory
cd jarvis

# Install dependencies
pip install -r requirements.txt

# Create .env file
echo "OPENAI_API_KEY=your_key_here" > .env

# Run application
python test_jarvis.py

Overview
J.A.R.V.I.S (Just A Rather Very Intelligent System) is a desktop AI assistant that combines voice control, system automation, and natural language processing. It features a holographic-inspired UI with real-time system monitoring, voice commands, and integration with multiple services.

Features
🎤 Voice Control
Wake word detection ("Jarvis")

Real-time speech-to-text transcription (Whisper)

Text-to-speech output (ElevenLabs / pyttsx3)

Voice command execution

🖥️ System Control
Screenshot Capture - Instant screen capture with timestamp

Volume Control - Increase, decrease, and mute

Brightness Control - Adjust screen brightness (0-100%)

App Launcher - Open/close applications

System Status - Real-time CPU, RAM, disk, and battery monitoring

System Power - Lock, shutdown, and restart PC

📧 Communication
Email - Open Gmail inbox/compose in browser

Calendar - Google Calendar integration

🌐 Web Integration
Web Search - Google search queries

YouTube - Search and open videos

Weather - Current weather by location

News - Google News feed

📋 Productivity
Clipboard Management - Copy/paste with voice

Memory - Long-term fact storage and recall

Alarms & Reminders - Set time-based notifications

File Management - Create, search, and organize files

🤖 AI Capabilities
Natural Language Processing - OpenAI GPT-4o-mini

Voice Synthesis - ElevenLabs / TTS-1

Speech Recognition - Whisper / Windows Speech Recognition

Function Calling - Execute system commands via AI

Technology Stack
Core Technologies
Technology	Version	Purpose
Python	3.8+	Programming Language
PyQt5	5.15.9	GUI Framework
OpenAI API	2.53.0	NLP & AI Processing
ElevenLabs API	Latest	Text-to-Speech
pyttsx3	2.90	Offline TTS Fallback
WebSockets	12.0	Real-time Communication
SoundDevice	0.5.5	Audio I/O Processing
System Control Libraries
Library	Purpose
pyautogui	Screenshot capture
psutil	System monitoring
pyperclip	Clipboard operations
ctypes	Windows system calls
wmi	Windows Management
AI & ML Libraries
Library	Purpose
openai	GPT-4o-mini / Whisper / TTS-1
elevenlabs	High-quality TTS
speech_recognition	Local speech recognition
numpy	Audio data processing
Audio Processing
Library	Purpose
sounddevice	Microphone capture
pyaudio	Audio I/O
simpleaudio	Audio playback
pygame	Audio playback
Utilities
Library	Purpose
python-dotenv	Environment configuration
requests	HTTP requests
schedule	Task scheduling
threading	Concurrent operations
asyncio	Asynchronous I/O
System Architecture
text
┌─────────────────────────────────────────────────────────────────┐
│                     J.A.R.V.I.S System                         │
├─────────────────────────────────────────────────────────────────┤
│                                                                 │
│  ┌─────────────────────────────────────────────────────────┐   │
│  │                    User Interface                       │   │
│  │  ┌──────────┐  ┌──────────┐  ┌────────────────────┐   │   │
│  │  │  Header  │  │  Status  │  │    Chat Display     │   │   │
│  │  └──────────┘  └──────────┘  └────────────────────┘   │   │
│  │  ┌──────────┐  ┌──────────┐  ┌────────────────────┐   │   │
│  │  │  Input   │  │  Voice   │  │  Quick Actions     │   │   │
│  │  └──────────┘  └──────────┘  └────────────────────┘   │   │
│  └─────────────────────────────────────────────────────────┘   │
│                              │                                  │
│                              ▼                                  │
│  ┌─────────────────────────────────────────────────────────┐   │
│  │                    Core Engine                         │   │
│  └─────────────────────────────────────────────────────────┘   │
│                              │                                  │
│         ┌────────────────────┼────────────────────┐           │
│         ▼                    ▼                    ▼           │
│  ┌─────────────┐    ┌─────────────┐    ┌─────────────┐      │
│  │  Command    │    │    AI       │    │   System    │      │
│  │  Processor  │◄───│  Engine     │───►│   Tools     │      │
│  └─────────────┘    └─────────────┘    └─────────────┘      │
│         │                    │                    │           │
│         ▼                    ▼                    ▼           │
│  ┌─────────────────────────────────────────────────────────┐   │
│  │              External Services                         │   │
│  │  ┌────────┐  ┌────────┐  ┌────────┐  ┌────────┐      │   │
│  │  │ OpenAI │  │Eleven- │  │ Gmail  │  │Calendar│      │   │
│  │  │  API   │  │  Labs  │  │        │  │        │      │   │
│  │  └────────┘  └────────┘  └────────┘  └────────┘      │   │
│  └─────────────────────────────────────────────────────────┘   │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
Data Flow Diagram
text
User Input → Command Processor → Command Router
                                       │
                ┌──────────────────────┼──────────────────────┐
                ▼                      ▼                      ▼
         Local Command           AI Processing          Web Search
                │                      │                      │
                ▼                      ▼                      ▼
         System Action          OpenAI GPT-4o          Browser Open
                │                      │                      │
                ▼                      ▼                      ▼
         Result Display         TTS Output             Results Display
Installation
Prerequisites
Python 3.8 or higher

pip (Python package manager)

Windows 10/11 (Primary support) / macOS / Linux

Step-by-Step Installation
1. Clone or Download
bash
git clone https://github.com/shayaanalqua/jarvis
cd jarvis-assistant
2. Create Virtual Environment (Recommended)
bash
python -m venv venv
source venv/bin/activate  # Linux/Mac
venv\Scripts\activate     # Windows
3. Install Dependencies
bash
pip install -r requirements.txt
4. Configure API Keys
Create a .env file in the project root:

env
OPENAI_API_KEY=your_openai_api_key_here
ELEVENLABS_API_KEY=your_elevenlabs_api_key_here
5. Run the Application
bash
python test_jarvis.py
Configuration
Environment Variables (.env)
Variable	Description	Required
OPENAI_API_KEY	OpenAI API key for GPT-4o-mini	✅ Yes
ELEVENLABS_API_KEY	ElevenLabs API key for TTS	❌ Optional
API Keys Setup
OpenAI API Key
Go to OpenAI Platform

Navigate to API Keys

Create new secret key

Copy and paste into .env

ElevenLabs API Key
Go to ElevenLabs

Navigate to Account → API Keys

Create new API key

Copy and paste into .env

Usage
Launching the Application
bash
python test_jarvis.py
Quick Actions
Button	Function
📷 Screenshot	Capture screen
🔊 Vol Up	Increase volume
🔉 Vol Down	Decrease volume
🔇 Mute	Toggle mute
📧 Email	Open Gmail
📅 Calendar	Open Google Calendar
▶ YouTube	Open YouTube
🌤 Weather	Show weather
📰 News	Open Google News
💻 Status	Show system stats
Voice Commands
Method 1: AI Voice Button
Click 🎙 AI VOICE

Wait for "Voice Assistant ready"

Speak naturally into your microphone

Method 2: Windows Speech Recognition
Click 🎤 LISTEN

Press Windows Key + H

Speak your command

Press Enter to execute

Method 3: Text Input
Type your command in the input box

Press Enter or click SEND

Commands Reference
System Commands
Command	Description
screenshot	Capture screenshot
volume up	Increase volume
volume down	Decrease volume
mute	Toggle mute
brightness 50	Set brightness to 50%
status	Show system status
lock pc	Lock computer
shutdown pc	Shutdown computer
restart pc	Restart computer
Application Commands
Command	Description
open chrome	Open Google Chrome
open notepad	Open Notepad
open vscode	Open VS Code
open spotify	Open Spotify
open calculator	Open Calculator
Web Commands
Command	Description
search for [query]	Google search
search youtube [query]	YouTube search
weather	Show weather
weather in [city]	Weather by city
news	Open Google News
Communication Commands
Command	Description
check email	Open Gmail inbox
send email	Open Gmail compose
calendar	Open Google Calendar
Productivity Commands
Command	Description
remember that [fact]	Store memory
what do you know	Recall memories
copy [text] to clipboard	Copy text
paste	Show clipboard content
set alarm at 14:30 to [msg]	Set reminder
alarms	Show all alarms
clear alarms	Clear all alarms
Misc Commands
Command	Description
help	Show all commands
hello	Greeting
shutdown	Close JARVIS
Project Structure
text
JARVIS_App/
├── test_jarvis.py              # Main application
├── jarvis_realtime.py          # Voice assistant engine
├── .env                        # Environment variables
├── .gitignore                  # Git ignore file
├── requirements.txt            # Dependencies
│
├── scripts/                    # Custom automation scripts
│   └── example_script.py       # Template script
│
├── assets/                     # Resources
│   └── icon.png               # App icon
│
└── docs/                       # Documentation
    ├── README.md              # This file
    └── api_reference.md       # API documentation
API Reference
Core Classes
JarvisTestApp
Main application class managing UI and command routing.

python
class JarvisTestApp:
    def __init__(self):
        # Initialize PyQt5 UI
        # Setup voice assistant
        # Start system monitoring
        
    def execute(self, command: str) -> str:
        """Route and execute commands"""
        
    def speak(self, text: str) -> None:
        """Text-to-speech output"""
VoiceAssistant
Handles voice processing, AI chat, and TTS.

python
class VoiceAssistant:
    def __init__(self, system_prompt, on_response):
        # Initialize OpenAI and ElevenLabs
        
    def process_text(self, text: str) -> str:
        """Process text and return response"""
        
    def speak(self, text: str) -> None:
        """Convert text to speech"""
RealtimeVoiceAssistant
Compatibility wrapper for VoiceAssistant.

Troubleshooting
Common Issues
1. "OPENAI_API_KEY not found in .env file"
Solution: Create .env file with your API key.

2. "Could not find PyAudio"
Solution:

bash
pip install pipwin
pipwin install pyaudio
3. "sounddevice or websockets not installed"
Solution:

bash
pip install sounddevice websockets numpy
4. "SpeechRecognition not installed"
Solution:

bash
pip install SpeechRecognition
5. "ElevenLabs not installed"
Solution:

bash
pip install elevenlabs
Logging
Check the terminal output for detailed logs:

Connection status

Error messages

API responses

Performance Optimization
Memory Management
Conversation history limited to 10 turns

Audio buffers cleared after playback

Screenshot files saved to Desktop

CPU Usage
System monitoring updates every 3 seconds

Asynchronous operations for voice processing

Threaded operations for UI responsiveness

Network Usage
OpenAI API calls optimized with max_tokens=200

ElevenLabs streaming for efficient audio

Contact
Developer: Shayaan Alqua Abdi

Email: shayaanalqua@gmail.com

GitHub: https://github.com/shayaanalqua/

Acknowledgments
OpenAI - GPT-4o-mini, Whisper, TTS-1

ElevenLabs - Text-to-Speech
