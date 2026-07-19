# Mobile Device Forensics Investigation Lab

<p align="center">
  <strong>iOS and Android Evidence Analysis with Paraben’s E3</strong>
</p>

---

## Overview

This lab documents a mobile-device forensic investigation involving an iPhone and an Android smartphone recovered during an organized vehicle-theft investigation. Using Paraben’s E3, I examined previously acquired mobile evidence, compared two iOS data cases, analyzed Android application data, bookmarked relevant artifacts, and generated formal mobile-evidence reports.

The suspects used the codenames **Bonnie** and **Clyde**. Relevant evidence was recovered from contacts, calendar events, messages, notes, images, browser history, anonymous chat activity, installed applications, deleted contacts, and SQLite databases.

> **Training Scenario:** All names, devices, and evidence in this repository are part of an authorized educational lab.

---

## Lab Objectives

- Import and analyze iOS and Android E3 data cases.
- Identify relevant contacts, events, messages, notes, and images.
- Compare two acquisitions from the same iPhone.
- Recover deleted Android contact information.
- Reconstruct Android activity during a known time window.
- Examine Whisper, Chrome, and Keep Notes artifacts.
- Bookmark evidence and generate mobile-evidence reports.
- Draft a case summary, findings, and conclusion.

---

## Skills Demonstrated

- Mobile-device forensics
- iOS and Android artifact analysis
- Paraben E3 case management
- Evidence triage and bookmarking
- Timeline reconstruction
- Deleted-contact recovery
- Mobile Evidence Comparer
- SQLite database examination
- Cross-device evidence correlation
- Investigative report generation

---

## Lab Environment

| Component | Details |
|---|---|
| Workstation | Windows Server 2019 virtual workstation |
| Forensic Tool | Paraben’s E3 |
| iOS Evidence 1 | `iPhone_Acquisition_08-12-2021_11-40-13.e3d` |
| iOS Evidence 2 | `iPhone_Acquisition_08-12-2021_11-55-18.e3d` |
| Android Evidence | `Lab_Android_Acquisition_06-02-2021_17-52-55` |
| Android Device | Honor smartphone manufactured by Huawei |
| Suspect Codenames | Bonnie and Clyde |
| Suspected Activity | Organized vehicle theft |

---

## Section 1: iOS Forensic Investigation

### Import the iOS Evidence

I imported:

```text
C:\Mobile Forensics Evidence\Case 1 (before)\
iPhone_Acquisition_08-12-2021_11-40-13.e3d
```

I then navigated to the iPhone node and reviewed its parsed data.

---

### Finding 1: iPhone Properties

The Properties pane contained device details such as the model, device name, iOS version, serial number, modem firmware, and Wi-Fi address.

<p align="center">
  <img src="https://github.com/user-attachments/assets/e07f9402-de4b-444f-9f5f-4f408cfceebc"
       alt="Paraben E3 displaying identifying properties for the acquired iPhone"
       width="800">
</p>

<p align="center">
  <em>Figure 1: The iPhone Properties pane showing identifying information for the acquired device.</em>
</p>

---

### Finding 2: iPhone Contacts

The Contacts grid displayed names, phone numbers, email addresses, and available creation or modification timestamps.

<p align="center">
  <img src="https://github.com/user-attachments/assets/2b1e6d7d-7206-4979-a4f9-fa57138cadec"
       alt="iPhone mobile forensic investigation evidence"
       width="800">
</p>

---

<p align="center">
  <em>Figure 2: Contacts recovered from the iPhone.</em>
</p>

---

### Finding 3: Vehicle-Related Calendar Event

The Calendar grid contained a user-created event with a car icon. In the context of the training scenario, the event was potentially relevant to vehicle-related planning, but the icon alone did not establish criminal intent.

<p align="center">
  <img src="https://github.com/user-attachments/assets/59e2a17d-85a0-463b-a075-78c8e7a5be8b"
       alt="Paraben E3 displaying a vehicle-related calendar event from the iPhone"
       width="800">
</p>

<p align="center">
  <em>Figure 3: A user-created calendar event containing a vehicle-related reference.</em>
</p>

---

### Finding 4: Vehicle-Related Messages

Two outgoing messages were relevant:

- A message to **Stinky** asking about a specific vehicle.
- A message to **ICE Mylady** indicating that a vehicle was located in **Windy City**.

<p align="center">
  <img src="https://github.com/user-attachments/assets/008e69cc-21dd-4331-804c-a59dc7fd7518"
       alt="Paraben E3 displaying iPhone messages referencing a vehicle and Windy City"
       width="800">
</p>

<p align="center">
  <em>Figure 4: iPhone messages referencing a specific vehicle and a vehicle located in `Windy City`.</em>
</p>

---

### Finding 5: Notes Concerning License Plates

The iPhone Notes data included:

- A note indicating that a specific license plate was known to police.
- Three notes concerning the replacement of license plates.

<p align="center">
  <img src="https://github.com/user-attachments/assets/4e510f25-c161-4936-ace3-43882fbd12c5"
       alt="Paraben E3 displaying iPhone notes concerning license plates"
       width="800">
</p>

<p align="center">
  <em>Figure 5: Notes concerning a plate known to police and the replacement of license plates.</em>
</p>

---

### Finding 6: Vehicle Photographs

E3 Content Analysis identified 13 vehicle photographs. Several showed visible license plates that investigators could compare with stolen-vehicle reports, vehicle-registration records, and other case evidence.

<p align="center">
  <img src="https://github.com/user-attachments/assets/c6490899-1bd2-4f54-8c7c-5be813f7b67a"
       alt="Paraben E3 displaying vehicle photographs recovered from the iPhone"
       width="800">
</p>

<p align="center">
  <em>Figure 6: Vehicle photographs recovered from the iPhone, including images with visible plates.</em>
</p>

---

### iOS Investigative Report

I bookmarked the relevant event, messages, notes, and images and generated a Mobile Evidence PDF Report.

<p align="center">
  <img src="https://github.com/user-attachments/assets/3feb93cf-d77f-4018-b811-502b85bfdcac"
       alt="Table of contents from the generated iOS mobile evidence report"
       width="515">
</p>

<p align="center">
  <em>Figure 7: The table of contents from the generated iOS report.</em>
</p>

---

## Section 1, Part 2: iOS Acquisition Comparison

I loaded the following acquisitions into E3’s Mobile Evidence Comparer:

```text
Case 1 (before): iPhone_Acquisition_08-12-2021_11-40-13.e3d
Case 2 (after):  iPhone_Acquisition_08-12-2021_11-55-18.e3d
```

### Finding 7: Property Difference

The comparison identified a difference in the data-case timestamp.

<p align="center">
  <img src="https://github.com/user-attachments/assets/90122bf0-bb7e-4380-aeb6-2634d6abc614"
       alt="Paraben E3 Mobile Evidence Comparer showing a timestamp difference between iOS acquisitions"
       width="800">
</p>

<p align="center">
  <em>Figure 8: A timestamp difference identified between the two iOS data cases.</em>
</p>

### Finding 8: Changes in Notes

The Notes comparison showed records that were not present in both acquisitions. This demonstrated how repeated acquisitions can identify differences that may reflect records created, modified, removed, or parsed differently between collection times.

<p align="center">
  <img src="https://github.com/user-attachments/assets/2f3cb54c-3102-4123-a139-12c46d51dbd8"
       alt="Paraben E3 Mobile Evidence Comparer showing differences between iOS Notes records"
       width="800">
</p>

<p align="center">
  <em>Figure 9: Differences identified between the Notes records in the two iOS data cases.</em>
</p>

---

## Section 2: Android Forensic Investigation

### Import the Android Evidence

I imported:

```text
C:\Mobile Forensics Evidence\
Lab_Android_Acquisition_06-02-2021_17-52-55
```

I then reviewed the Mobile Data Triage categories.

---

### Finding 9: Device Information

The Android evidence identified an Honor smartphone manufactured by Huawei.

<p align="center">
  <img src="https://github.com/user-attachments/assets/7c889223-1fc9-440f-80ac-527d5b808af8"
       alt="iPhone mobile forensic investigation evidence"
       width="800">
</p>

---

<p align="center">
  <em>Figure 10: Device information for the Honor smartphone manufactured by Huawei.</em>
</p>

---

### Finding 10: ICE Contacts and Possible Device Association

The device contained two emergency contacts:

- `Clyde`
- `Daddy Dear`

Because `Clyde` appeared as an ICE contact on the Android device, I treated the phone as potentially associated with **Bonnie** in the training scenario. This was an investigative inference and did not independently establish device ownership.

<p align="center">
  <img src="https://github.com/user-attachments/assets/f8c9730d-a02d-4e38-9044-a1d475ae8514"
       alt="Paraben E3 displaying Clyde and Daddy Dear in the Android ICE Contacts grid"
       width="800">
</p>

<p align="center">
  <em>Figure 11: The Android ICE Contacts grid showing `Clyde` and `Daddy Dear`.</em>
</p>

---

### Finding 11: Contact Email Accounts

The Android evidence contained contact records for:

- Lucas Carter
- Emma Chicago
- Tom Audi&amp;BMW

The display name `Tom Audi&BMW` was documented as potentially relevant because it referenced two vehicle manufacturers. The name alone did not establish involvement in vehicle theft.

<p align="center">
  <img src="https://github.com/user-attachments/assets/63fd1e96-bfbd-4221-a2ef-cfc9c5fcc48e"
       alt="Paraben E3 displaying Android contact email accounts including Tom Audi and BMW"
       width="800">
</p>

<p align="center">
  <em>Figure 12: Contact email accounts, including `Tom Audi&amp;BMW`.</em>
</p>

---

### Finding 12: eBay Motors Installed

The Installed Applications category showed the **eBay Motors** application.

<p align="center">
  <img src="https://github.com/user-attachments/assets/e4f12b83-8558-48eb-b087-9ce7f3815a95"
       alt="Paraben E3 displaying the eBay Motors application in the Android installed-applications list"
       width="800">
</p>

<p align="center">
  <em>Figure 13: The eBay Motors application identified on the Android phone.</em>
</p>

---

### Finding 13: Recovered Contacts

The Recovered Contacts grid contained four partial records:

- One with an eBay URL
- One with only a phone number
- One blank record
- One with only an email address

<p align="center">
  <img src="https://github.com/user-attachments/assets/11d67ece-51ea-4e06-b405-d069f0faf69b"
       alt="Paraben E3 displaying partially recovered Android contact records"
       width="800">
</p>

<p align="center">
  <em>Figure 14: Partially recovered contact records from the Android phone.</em>
</p>

---

### Finding 14: User Activity Timeline

I changed E3 to Eastern Time and reviewed activity from:

```text
6/2/2021 9:17:47 AM through 9:24:51 AM
```

The device accessed:

- Whisper
- Chrome
- VPN Unlimited
- Contacts
- Calendar
- System UI
- Huawei Home

<p align="center">
  <img src="https://github.com/user-attachments/assets/d961eff4-f148-4ce7-bb57-ea88be35cad4"
       alt="Paraben E3 displaying the first portion of the Android activity timeline"
       width="49%">
  <img src="https://github.com/user-attachments/assets/96979f90-fdd0-42b7-aba6-db9fd49ee80a"
       alt="Paraben E3 displaying the second portion of the Android activity timeline"
       width="49%">
</p>

<p align="center">
  <em>Figure 15: Android activity during the suspected crime window.</em>
</p>

---

### Finding 15: Whisper Posts

The Own Whispers grid contained three relevant posts:

- A Porsche 911 reference
- A Windy City reference
- A post mocking law enforcement

The phrase `Windy City` also appeared in the iPhone messages, providing a cross-device term for further correlation.

<p align="center">
  <img src="https://github.com/user-attachments/assets/c3e0be66-dc8d-434b-9cf6-bbc6ecfb9b7e"
       alt="Paraben E3 displaying Whisper posts referencing a Porsche 911 Windy City and law enforcement"
       width="800">
</p>

<p align="center">
  <em>Figure 16: Whisper posts referencing a Porsche 911, Windy City, and law enforcement.</em>
</p>

---

### Finding 16: Chrome History

The Chrome History grid showed:

- `autonews.com`
- `tesla.com`
- `ebay.com/motors`
- Porsche 911 searches
- New Tesla model searches

<p align="center">
  <img src="https://github.com/user-attachments/assets/1d4f003b-51ec-43b8-8d66-77ecc48e1d78"
       alt="Paraben E3 displaying vehicle-related entries in Android Chrome history"
       width="800">
</p>

<p align="center">
  <em>Figure 17: Vehicle-related websites and searches in the Android Chrome history.</em>
</p>

---

### Finding 17: Keep Notes Records

I opened the Keep Notes database:

```text
databases
└── keep.db
    └── SQLite Database
        └── Tables
            └── list_item
                └── list_item 1-5
```

The table contained five note records. Two referenced license plate numbers.

<p align="center">
  <img src="https://github.com/user-attachments/assets/2e818493-2d1d-48c4-893c-1318db82486d"
       alt="Paraben E3 displaying Keep Notes database records containing license-plate references"
       width="800">
</p>

<p align="center">
  <em>Figure 18: Keep Notes records containing license-plate references.</em>
</p>

---

### Finding 18: Keep Notes Account Owner

The account table identified:

```text
julriley1990@gmail.com
```

Because the Android device was potentially associated with Bonnie in the training scenario, the address could provide investigators with an identity lead. Additional account records or subscriber information would be needed to confirm the user's identity.

<p align="center">
  <img src="https://github.com/user-attachments/assets/c13352ad-c777-4e6a-bde0-c1d8a8d059ee"
       alt="Paraben E3 displaying the Keep Notes account julriley1990 at gmail"
       width="800">
</p>

<p align="center">
  <em>Figure 19: The Keep Notes account owner identified as `julriley1990@gmail.com`.</em>
</p>

---

### Android Investigative Report

I bookmarked the relevant Android evidence and generated a Mobile Evidence PDF Report.

<p align="center">
  <img src="https://github.com/user-attachments/assets/fe8559f2-b91c-404e-a65c-4dd8b101fc04"
       alt="Table of contents from the generated Android mobile evidence report"
       width="511">
</p>

<p align="center">
  <em>Figure 20: The table of contents from the generated Android report.</em>
</p>

---

## Section 3: Final Forensic Report

### Case Summary

The Madison Police Department recovered an iPhone and an Android smartphone during an organized vehicle-theft investigation. The suspected participants used the codenames Bonnie and Clyde. I used Paraben’s E3 to examine both devices, compare the two iOS acquisitions, identify relevant evidence, and generate formal mobile evidence reports.

### Findings and Analysis

The iPhone contained vehicle-related messages, license-plate notes, a potentially relevant calendar event, and multiple vehicle photographs. The Android evidence contained `Clyde` as an ICE contact, the eBay Motors application, vehicle-related browsing history, Whisper posts, recovered contacts, license-plate notes, and the Keep Notes account `julriley1990@gmail.com`.

The term **Windy City** appeared in artifacts from both devices. License-plate references also appeared in iOS and Android notes, providing cross-device correlation that warranted further investigation.

### Conclusion

The recovered evidence showed that both devices contained information relevant to the vehicle-theft investigation. Repeated references to `Windy City`, vehicles, and license plates provided cross-device corroboration within the training scenario. The Keep Notes email address also provided a potential identity lead, but additional records would be required to confirm the person using the Bonnie codename.

---

## Evidence Correlation

| Source | Finding | Significance |
|---|---|---|
| iPhone Calendar | Vehicle-related event | Possible planning activity |
| iPhone Messages | Vehicle and Windy City references | Relevant communication and location |
| iPhone Notes | Known and replacement plates | Potentially relevant to concealment or plate replacement |
| iPhone Images | Vehicle photographs with visible plates | Supports comparison with registration and stolen-vehicle records |
| Android ICE Contacts | Clyde and Daddy Dear | Supports a possible device-association inference |
| Android Applications | eBay Motors | Potential marketplace or vehicle-research relevance |
| Whisper | Porsche 911 and Windy City | Cross-device correlation |
| Chrome | Vehicle sites and searches | Vehicle research |
| Keep Notes | License-plate references | Corroborates iPhone notes |
| Keep Notes Account | `julriley1990@gmail.com` | Potential identity lead requiring corroboration |

---

> **Ethical Use Notice:** This repository documents an authorized educational forensic investigation. Mobile devices and user data should only be examined with proper legal authority or explicit permission.
