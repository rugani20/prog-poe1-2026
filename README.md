# Cybersecurity Awareness Bot

## Project Structure

```
CybersecurityBot/
├── Program.cs          - Entry point
├── ChatBot.cs          - Startup sequence and chat loop
├── Display.cs          - Colour printing helpers
├── ImageConverter.cs   - Converts logo.jpg to ASCII art
├── VoiceGreeting.cs    - Plays greeting.wav on startup
├── ResponseEngine.cs   - Keyword responses and input validation
├── CybersecurityBot.csproj
└── .github/workflows/ci.yml
```

## Setup - Adding Your Own Files

Both files must be placed in the same folder as the compiled `.exe`:
`bin\Release\net8.0-windows\`

### Voice greeting (greeting.wav)
1. Record a short welcome message using Windows Voice Recorder
2. Export/save it as `greeting.wav`
3. Copy it to the output folder next to the .exe

### Logo image (logo.jpg)
1. Use any JPG image - a cybersecurity logo, shield, lock icon, etc.
2. Rename it to `logo.jpg`
3. Copy it to the output folder next to the .exe

The bot converts the JPG to ASCII art using System.Drawing.Bitmap in pure C#.

## How to Run

```
dotnet restore
dotnet build --configuration Release
dotnet run
```

## Suggested Commit Messages

1. Initial commit: Set up project structure and main files
2. Add Display helper for coloured console output
3. Add ImageConverter to display JPG as ASCII art
4. Add VoiceGreeting to play WAV file on startup
5. Add ResponseEngine with cybersecurity keyword responses and input validation
6. Add ChatBot controller with greeting and chat loop
7. Add GitHub Actions CI workflow
