# Application Documentation: COLEv2 Mobile Application


# General Information
-App Name: COLEv2 Apk (Caller Offline Lookup Extraction)

-Version: v1.0.3

-Created: 6-22-26 - 10:55 AM

-Last Update: 6-22-26 - 1:50 PM

-Developer: MINU_DO

-Purpose: White Hat Tools for Call logs and Cyber Security

-Languages: Native Kotlin (Jetpack Compose)

-Architecture: Offline-First, JSON-based Persistence

# User Acess

username: dev
password: dev@123


# Summary
COLEv2 is a sophisticated, privacy-centric "White Hat" security application designed to provide users with complete control over their incoming call data without ever requiring an internet connection. By leveraging Android’s native CallScreeningService, COLEv2 acts as an invisible shield, intercepting unknown or malicious callers before the phone even rings. The app maps raw caller ID metadata against a local prefix database (db.json) to identify carriers and regions, ensuring that sensitive data never leaves the device.

The app features a "High-Visibility" security aesthetic (Deep Orange & Black) and follows a rigorous authentication process to ensure that only authorized developers or investigators can access the "Vault" where intercepted data is stored.

# Core Functions & Modules
# 1. The Authentication Gate (Login System)
• Security First: Prevents unauthorized access with a hardcoded developer credential system (dev / dev@123).
• Splash Screen: Features a 2-second fading animation of the MINU_DO logo upon entry.

# 2. Offline Screening Engine (The Interception)
• Native Hook: Uses Android's CallScreeningService to intercept calls in real-time.
• Prefix Mapping: Instantly identifies the carrier (e.g., Smart, Globe) and region based on local prefix rules.
• Instant Blocking: Automatically rejects calls from numbers flagged as CRITICAL in the local vault.

# 3. COLE Vault Dashboard
• System Status: Real-time view of protection levels and database integrity.
• Vault Report (PDF): A native PDF engine that generates an official "COLE Vault Report" saved locally, summarizing carrier prefixes and security status.

# 4. Live Performance Statistics
• Performance Checker: A dynamic dashboard showing live CPU and Memory usage.
• Integrity Monitoring: Tracks active background threads to ensure the screening core is running efficiently.

# 5. Call History CRUD (with Data Lock)
• Persistent Logs: Stores intercepted call data in history.json.
• Advanced CRUD: Users can select individual or multiple logs to delete.
• Vault Lock: Each log can be "Locked" (Red Icon) to prevent accidental deletion, ensuring critical evidence is preserved.

# 6. Investigation Notes
• Local Ledger: A dedicated section to store investigative details, carrier patterns, or suspicious number behaviors.
• JSON Sync: All notes are saved to notes.json for persistent storage across app restarts.

# 7. Audio Capture Core (Technophone Recorder)
• Device Sound Optimization: Uses the VOICE_COMMUNICATION audio source to prioritize capturing the caller's voice output from the device.
• Downloads Integration: Automatically saves recordings as .mp3 files to the public Downloads folder for easy access and analysis.

# Technical Highlights
• 100% Offline: No network permissions are required for the core identification engine, mitigating the risk of data leaks.
• Modern UI: Built entirely with Jetpack Compose for a fluid, responsive mobile experience.
• Secure Storage: Uses local internal storage blocks (filesDir) for JSON databases, keeping logs isolated from other apps.
