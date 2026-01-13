Microsoft Intune Device Enrollment Guide

This guide provides comprehensive, step-by-step instructions for enrolling devices into Microsoft Intune. It covers the most common enrollment scenarios:

User Self-Service Enrollment for Windows 10/11, iOS, and Android devices.

Zero-Touch Enrollment using Windows Autopilot for new Windows devices.

The guide is divided into five parts: prerequisites & admin setup, user self-service enrollment (Windows), user self-service enrollment (mobile), Windows Autopilot enrollment, and key considerations.

Part 1: Prerequisites & Admin Setup

Before devices can be enrolled in Intune, certain prerequisites must be met, and initial administrative setup must be completed.

1.1 Prerequisites

Ensure the following conditions are met before enrollment:

Licenses

The user must have an active Microsoft Intune license assigned.

Verify licenses in the Microsoft 365 Admin Center: Users > Active Users > Licenses.

Administrative Rights

Admin access is required for Intune setup, user and device group creation, and Autopilot configuration.

End-users performing self-service enrollment do not need admin rights on their devices.

MDM Authority

Confirm that the Mobile Device Management (MDM) authority is set to Intune.

Navigate to Microsoft Endpoint Manager Admin Center > Tenant administration > MDM Authority.

Device Requirements

Windows 10 version 1709 or later / Windows 11

iOS 13 or later

Android 8.0 or later

Ensure the device is connected to the internet during enrollment.

1.2 Admin Setup (High-Level Overview)

Assign Licenses to Users

Go to Microsoft 365 Admin Center > Users > Active Users.

Select the user account and click Assign licenses.

Ensure the Intune license is applied.

Create Device/User Groups

Navigate to Microsoft Endpoint Manager Admin Center > Groups.

Example groups:

All Windows Devices

All Mobile Devices

All Autopilot Devices

Assign users or devices to these groups to deploy policies, apps, and configurations.

Verify Intune Settings

Confirm policies, compliance rules, and enrollment restrictions are configured.

Verify in Microsoft Endpoint Manager Admin Center > Devices > Enroll devices.

Part 2: User Self-Service Enrollment (Windows 10/11)

Windows devices can be enrolled directly by the user without IT assistance.

2.1 End-User Steps

Open Settings on the Windows device.

Navigate to Accounts > Access work or school.

Click Connect.

Enter your work or school account credentials.

Follow the prompts:

Verify identity (may require MFA if enabled)

Accept device management policies

Device will automatically register with Intune

Optional: Install the Company Portal app to manage devices and apps.

Policies and applications will deploy automatically once enrollment is complete.

Notes:

Device must have an active internet connection during enrollment.

Company Portal may prompt for device compliance checks or required app installations.

Part 3: User Self-Service Enrollment (iOS & Android)

Mobile devices require installation of the Intune Company Portal app to complete enrollment.

3.1 iOS Devices

Open the App Store and download Intune Company Portal.

Launch the app and sign in with your work/school account.

Follow the prompts to:

Add a work profile

Enroll your device

Grant required permissions for device management and notifications

Wait for policies and apps to deploy automatically.

3.2 Android Devices

Open Google Play Store and download Intune Company Portal.

Launch the app and sign in with your work/school account.

Follow the prompts to:

Create a work profile

Enroll the device

Accept company device management policies

Notes:

MFA may be required depending on company security policies.

Enrollment requires an active internet connection.

Part 4: Windows Autopilot (Zero-Touch Enrollment)

Autopilot allows new Windows devices to enroll automatically with minimal user interaction.

4.1 Admin Steps

Register Devices

Obtain hardware IDs from the OEM/vendor in a CSV file.

Upload the CSV to Microsoft Endpoint Manager Admin Center > Devices > Windows > Windows enrollment > Devices.

Create an Autopilot Deployment Profile

Navigate to Devices > Windows > Windows enrollment > Deployment Profiles > Create profile

Set deployment type to Azure AD Join

Enable Intune enrollment

Assign Profile to a Device Group

Example: All Autopilot Devices

All devices in this group will automatically apply the deployment profile upon first boot.

4.2 End-User Steps

Power on the new Windows device.

Connect to Wi-Fi.

Sign in with your work or school account.

Device will automatically configure:

Azure AD join

Intune enrollment

App deployment and policy enforcement

Notes:

Minimal user interaction is required.

Devices will automatically register in Intune and apply company settings.

Part 5: Key Considerations

Device Limits: Users can enroll up to 5 devices by default.

Multi-Factor Authentication (MFA): May be enforced based on company policy.

Device Compliance: Ensure devices meet security policies, including:

Encryption

PIN/password requirements

OS version and updates

Required apps installed
