﻿---
title: Upgrade Readiness - Upgrade Overview (Windows 10)
description: Displays the total count of computers sharing data and upgraded.
ms.prod: w10
author: greg-lindsay
---

# Upgrade Readiness - Upgrade overview

The first blade in the Upgrade Readiness solution is the upgrade overview blade. This blade displays the total count of computers sharing data with Microsoft, and the count of computers upgraded. As you successfully upgrade computers, the count of computers upgraded increases.

The upgrade overivew blade displays data refresh status, including the date and time of the most recent data update and whether user changes are reflected. The upgrade overview blade also displays the current target OS version.  For more information about the target OS version, see [target version](use-upgrade-readiness-to-manage-windows-upgrades.md).

The following color-coded status changes are reflected on the upgrade overview blade:

- The "Last updated" banner:
    - No delay in processing device inventory data = "Last updated" banner is displayed in green.
    - Delay processing device inventory data = "Last updated" banner is displayed in amber.
- Computers with incomplete data:
    - Less than 4% = Count is displayed in green.
    - 4% - 10% = Count is displayed in amber.
    - Greater than 10%  = Count is displayed in red.
- Computers with outdated KB:
    - Less than 10% = Count is displayed in green.
    - 10% - 30% = Count is displayed in amber.
    - Greater than 30%  = Count is displayed in red.
- User changes:
    - Pending user changes = User changes count displays "Data refresh pending" in amber.
    - No pending user changes = User changes count displays "Up to date" in green.
- Target version:
    - If the current value matches the recommended value, the version is displayed in green.
    - If the current value is an older OS version than the recommended value, but not deprecated, the version is displayed in amber.
    - If the current value is a deprecated OS version, the version is displayed in red.

Click on a row to drill down and see details about individual computers. If KBs are missing, see [Deploy the compatibility update and related KBs](https://technet.microsoft.com/en-us/itpro/windows/deploy/upgrade-readiness-get-started#deploy-the-compatibility-update-and-related-kbs) for information on required KBs.

In the following example, there is no delay in data processing, less than 4% of computers (6k\294k) have incomplete data, there are no pending user changes, and the currently selected target OS version is the same as the recommended version:

![Upgrade overview](images/ur-overview.png)

<!-- PRESERVING ORIGINAL IMAGE CODING JUST IN CASE
<img src="media/image3.png" width="214" height="345" />
-->

If data processing is delayed, you can continue using your workspace as normal. However, any changes or additional information that is added might not be displayed. Data is typically refreshed and the display will return to normal again within 24 hours.

If there are computers with incomplete data, verify that you have installed the latest compatibilty update and run the most recent [Update Readiness deployment script](https://go.microsoft.com/fwlink/?LinkID=822966&clcid=0x409) from the Microsoft download center.

Select **Total computers** for a list of computers and details about them, including:

-   Computer ID and computer name
-   Computer manufacturer
-   Computer model
-   Operating system version and build
-   Count of system requirement, application, and driver issues per computer
-   Upgrade assessment based on analysis of computer telemetry data
-   Upgrade decision status

Select **Total applications** for a list of applications discovered on user computers and details about them, including:

-   Application vendor
-   Application version
-   Count of computers the application is installed on
-   Count of computers that opened the application at least once in the past 30 days
-   Percentage of computers in your total computer inventory that opened the application in the past 30 days
-   Issues detected, if any
-   Upgrade assessment based on analysis of application data
-   Rollup level