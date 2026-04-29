# MOB-7 Biometric Authentication

## Overview
Add biometric login support (fingerprint and Face ID) to allow 
users to securely access the app without entering credentials each time.

## Technical Approach
- Use Android BiometricPrompt API for fingerprint/face unlock
- Use Apple LocalAuthentication framework for Face ID / Touch ID
- Store encrypted session token in device secure keystore
- Fallback to PIN/password if biometric fails 3 times

## Acceptance Criteria
- [ ] User can enable biometric login from security settings
- [ ] App prompts biometric on every launch if enabled
- [ ] Fallback to password after 3 failed biometric attempts
- [ ] Biometric data never leaves the device

## Notes
- Must comply with GDPR — no biometric data stored on server
- Test on devices with and without biometric hardware
