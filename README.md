# Microsoft-Intune-Device-Enrollment-Guide

This guide provides step-by-step instructions for enrolling devices into Microsoft Intune. It covers common enrollment scenarios: User Self-Service for Windows and mobile devices, and Zero-Touch enrollment via Windows Autopilot.

Part 1: Prerequisites & Admin Setup (Brief Overview)

Before enrolling devices, ensure the following prerequisites are met:

Prerequisites

Active Microsoft Intune license assigned to the user.

Administrative rights (for admin setup tasks, not required for user self-service).

MDM Authority set to Intune in the Microsoft Endpoint Manager admin center.

Devices meet the minimum requirements for Intune enrollment (Windows 10/11, iOS 13+, Android 8+).

Admin Setup (High-Level)

Assign licenses to users:

In Microsoft 365 admin center: Users > Active users > Assign licenses.

Create groups to manage devices and policies:

Example: All Windows Devices, All Mobile Devices.

Assign devices or users to these groups for policy deployment.

Verify Intune settings:

Navigate to Microsoft Endpoint Manager admin center > Tenant administration > MDM Authority.

Part 2: User Self-Service Enrollment (Windows 10/11)

Windows devices can be enrolled by the end-user without IT intervention.

End-User Steps

Open Settings.

Navigate to Accounts > Access work or school.

Click Connect.

Enter your work or school account credentials.

Follow the prompts to complete enrollment.

Once enrolled, your device will appear in Company Portal (if installed), and policies will be applied automatically.

Notes:

Ensure the device is connected to the internet during enrollment.

Company Portal may prompt for device compliance or app installation.

Part 3: User Self-Service Enrollment (iOS & Android)

Mobile devices require installation of the Company Portal app.

End-User Steps

iOS

Download Company Portal from the App Store.

Open the app and sign in with your work/school account.

Follow the prompts to add your work profile and enroll your device.

Grant required permissions (device management, notifications).

Android

Download Company Portal from Google Play.

Open the app and sign in with your work/school account.

Follow prompts to create a work profile and enroll your device.

Accept the device management policies.

Notes:

Device enrollment may prompt for MFA verification if required by policy.

Ensure internet connection during the enrollment process.

Part 4: Windows Autopilot (Zero-Touch Enrollment)

Windows Autopilot allows new devices to be automatically enrolled with minimal user intervention.

Admin Steps (High-Level)

Register devices in Autopilot:

Upload CSV file from OEM/vendor or use partner integration.

Create an Autopilot deployment profile:

Choose Azure AD Join and enable Intune enrollment.

Assign profile to a device group:

Example: All Autopilot Devices.

End-User Steps

Power on the new Windows device.

Connect to Wi-Fi.

Sign in with your work or school account.

Device will automatically configure with company settings, apps, and policies.

Notes:

Minimal user interaction is required.

Enrollment includes automatic device registration with Intune.

Part 5: Key Considerations

Device limits: By default, users can enroll up to 5 devices in Intune.

Multi-Factor Authentication (MFA): May be required depending on company policies.

Device compliance: Ensure enrolled devices meet security policies (e.g., encryption, PIN/password, OS updates) to access company resources.
