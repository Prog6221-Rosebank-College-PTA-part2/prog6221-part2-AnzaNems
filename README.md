[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/Apa4hIya)
ST10480934
🔒 CyberGuard — Cybersecurity Awareness Chatbot
Show Image
A WPF-based cybersecurity awareness chatbot built in C# for the PROG6221 Programming 2A module at The Independent Institute of Education (IIE).

📋 Project Overview
CyberGuard is a Graphical User Interface (GUI) chatbot that educates users on cybersecurity topics in a conversational manner. The bot covers phishing, password safety, malware, firewalls, VPNs, MFA, and social engineering — all while detecting the user's sentiment and personalising responses.

✅ Features Implemented
Part 1 (Console App — preserved in git history)

Voice greeting using SpeechSynthesizer
ASCII art logo displayed on startup
Personalised greeting asking for the user's name
Basic response system for cybersecurity topics
Input validation with graceful error handling
Coloured console output with typewriter effect

Part 2 (WPF GUI — current version)

Full WPF window with dark cybersecurity theme
All Part 1 features migrated to the GUI
Keyword recognition — detects phishing, password, mfa, malware, firewall, vpn, social engineering, privacy
Random responses — multiple responses per topic selected randomly
Conversation flow — follow-up phrases like "tell me more" continue the current topic
Memory and recall — remembers the user's name and favourite topic
Sentiment detection — detects worried, curious, and frustrated and adjusts responses
Quick topic buttons — RadioButtons for one-click topic selection
Chat history viewer — shows last 10 conversation entries with topics discussed
Error handling for all unexpected or empty inputs


🖥️ How to Run the Application
Requirements

Windows 10 or 11
.NET 8.0 SDK
Visual Studio 2022 or VS Code with the C# Dev Kit extension

Steps

Clone the repository

bash   git clone https://github.com/YOUR-USERNAME/CybersecurityChatbot.git
   cd CybersecurityChatbot

Open the project

Visual Studio: Open CybersecurityChatbot.sln
VS Code: Open the folder and select the .csproj file when prompted


Restore packages

bash   dotnet restore

Run the application

bash   dotnet run
Or press F5 in Visual Studio / VS Code.

📁 Project Structure
CybersecurityChatbot/
│
├── .github/
│   └── workflows/
│       └── ci.yml              ← GitHub Actions CI pipeline
│
├── MainWindow.xaml             ← WPF UI layout and styles
├── MainWindow.xaml.cs          ← Chat logic, event handlers, responses
├── App.xaml                    ← WPF application entry point
├── App.xaml.cs                 ← Application startup
├── CybersecurityChatbot.csproj ← Project file
│
└── README.md                   ← This file

🤖 How to Use the Chatbot

Launch the application
Enter your name in the welcome screen and click Start Chat
Type any of the following to get cybersecurity tips:

Type thisTopicphishingPhishing attack awarenesspasswordPassword safety best practicesmfa or 2faMulti-factor authenticationmalware or virusMalware preventionfirewallFirewall guidancevpnVPN usage tipssocial engineeringSocial engineering defencegeneral tips or adviceGeneral cybersecurity tipsprivacyPrivacy and data protectionhelpFull topic listexitEnd the session

Use the Quick Topics radio buttons at the bottom for one-click access
Type "tell me more", "another tip", or "explain more" for follow-up responses
Click Chat History to see a summary of your session


🔁 Sentiment Detection
The chatbot adjusts its tone based on how you phrase your message:
You say...Bot responds with..."I'm worried about phishing"Empathetic intro + tip"I'm curious about malware"Enthusiastic intro + tip"I'm frustrated with passwords"Calm, understanding intro + tip
