---
# required metadata

title: Microsoft Intune reports
titleSuffix: Microsoft Intune
description: Intune provides specific report types with focused views that contain consistent and timely data. 
keywords:
author: erikre
ms.author: erikre
manager: dougeby
ms.date: 10/20/2020
ms.topic: how-to
ms.service: microsoft-intune
ms.subservice: fundamentals
ms.localizationpriority: high
ms.assetid: 

# optional metadata

#ROBOTS:
#audience:

ms.suite: ems
#ms.tgt_pltfrm:
ms.custom: intune-azure
ms.collection: M365-identity-device-management
---
# Intune reports
Microsoft Intune reports allows you to more effectively and proactively monitor the health and activity of endpoints across your organization, and also provides other reporting data across Intune. For example, you will be able to see reports about device compliance, device health, and device trends. In addition, you can create custom reports to obtain more specific data. 

> [!NOTE]
> The Intune reporting changes will roll out gradually over a period of time to help you prepare and adapt to the new structure.

The report types are organized into the following focus areas:
- **Operational** - Provides timely, targeted data that helps you focus and take action. Admins, subject matter experts, and helpdesk will find these reports most helpful.
- **Organizational** - Provides a broader summary of an overall view, such as device management state. Managers and admins will find these reports most helpful.
- **Historical** - Provides patterns and trends over a period of time. Managers and admins will find these reports most helpful.
- **Specialist** - Allows you to use raw data to create your own custom reports. Admins will find these reports most helpful.

The reporting framework provides a consistent and more comprehensive reporting experience. The available reports provide the following functionality:
- **Search and sort** – You can search and sort across every column, no matter how large the dataset.
- **Data paging** – You can scan your data based on paging, either page-by-page or by jumping to a specific page.
- **Performance** - You can quickly generate and view reports created from large tenants.
- **Export** – You can quickly export reporting data generated from large tenants.

### Who can access the data?

Users with the following permissions can review logs:

- Global Administrator
- Intune Service Administrator
- Administrators assigned to an Intune role with **Read** permissions

## Non-compliant devices report (Operational)
The Non-compliant devices report provides data typically used by Helpdesk or admin roles to identify problems and help remediate issues. The data found in this report is timely, calls out unexpected behavior, and is meant to be actionable. The report is available alongside the workload, making the non-compliant devices report accessible without browsing away from active workflows. This report provides filtering, searching, paging, and sorting capabilities. Also, you can drill down to help troubleshoot.

You can view the **Noncompliant devices** report using the following steps:

1. Sign in to the [Microsoft Endpoint Manager admin center](https://go.microsoft.com/fwlink/?linkid=2109431).
2. Select **Devices** > **Monitor** > **Noncompliant devices**.

    ![Noncompliant device report](./media/intune-reports/intune-reports-02.png)

    > [!TIP]
    > If you have previously used Intune in the Azure portal, you found the above details in the Azure portal by signing in to [Intune](https://go.microsoft.com/fwlink/?linkid=2090973) and selecting **Device compliance** > **Noncompliant devices**.

## Windows 10 unhealthy endpoints report (Operational)
The **Windows 10 unhealthy endpoints** report surfaces data typically used by Helpdesk or admin roles to identify problems and help remediate issues. The data found in this report is timely, calls out the unhealthy device, the primary user principal name (UPN), and the status of a number of settings. The report is available as a tab within the primary **Antivirus** workload. This report provides filtering, searching, paging, and sorting. 

You can view the **Windows 10 unhealthy endpoints** report using the following steps:

1. Sign in to the [Microsoft Endpoint Manager admin center](https://go.microsoft.com/fwlink/?linkid=2109431).
2. Select **Endpoint security** > **Antivirus** > **Windows 10 unhealthy endpoints**.

## Windows 10 detected malware report (Operational)
The **Windows 10 detected malware** report provides data to identify devices with malware problems and help remediate issues. The data found in this report is timely, calls out the unhealthy device, the user name, and severity. The report is available as a tab within the primary **Antivirus** workload. This report provides filtering, searching, paging, and sorting. 

You can view the **Windows 10 detected malware** report using the following steps:

1. Sign in to the [Microsoft Endpoint Manager admin center](https://go.microsoft.com/fwlink/?linkid=2109431).
2. Select **Endpoint security** > **Antivirus** > **Windows 10 detected malware**.

### Bulk actions for devices
The **Windows 10 detected malware** report provides bulk actions that are applicable to the devices selected within the report. To use a bulk action, you select a row corresponding to each device (up to 100 devices at a time) and select the action. The actions available are the following:
- **Restart** - This action performs a restart of the selected devices.
- **Quick scan** - This action performs a Windows Defender quick scan of the selected devices. 
- **Full scan** - This action performs a Windows Defender full scan of the selected devices. 

For more information about the difference between a *quick scan* and a *full scan*, see [Configure scheduled quick or full Microsoft Defender Antivirus scans](/windows/security/threat-protection/microsoft-defender-antivirus/scheduled-catch-up-scans-microsoft-defender-antivirus).

## Feature update failures report (Operational)
The **Feature update failures** operational report provides failure details for devices that are targeted with a **Windows 10 feature updates** policy and have attempted an update. The data found in this report is timely and calls out number of devices with errors. You can drill down to help troubleshoot. This report provides filtering, searching, paging, and sorting. 

You can view the **Feature update failures** report using the following steps:

1. Sign in to the [Microsoft Endpoint Manager admin center](https://go.microsoft.com/fwlink/?linkid=2109431).
2. Select **Devices** > **Monitor** > **Feature update failures**.

## Device compliance report (Organizational)

Device compliance reports are meant to be broad in nature and provide a more traditional reporting view of data to identify aggregated metrics. This report is designed to work with large datasets to get a full device compliance picture. For example, the device compliance report for device compliance shows all the compliance states for devices to give a broader view of the data, no matter how large the dataset. This report shows the full breakdown of records in addition to a convenient visualization of aggregated metrics. This report can be generated by applying filters on it and selecting the "Generate report" button. This will refresh the data to show the latest state with the ability to view the individual records that make up the aggregate data. Like most reports in the new framework, these records can be sorted and searched upon to focus on the information you need.

To see a generated report of device state, you can use the following steps:

1. Sign in to the [Microsoft Endpoint Manager admin center](https://go.microsoft.com/fwlink/?linkid=2109431).
2. Select **Reports** to view the reports summary.
3. Select **Device compliance**.
4. Select the **Compliance status**, **OS**, and **Ownership** filters to refine your report.
5. Click **Generate report** (or **Generate again**) to retrieve current data.

    ![Device compliance report](./media/intune-reports/intune-reports-02a.png)

    > [!NOTE]
    > This **Device compliance** report provides a time stamp of when the report was last generated. 

For related information, see [Enforce compliance for Microsoft Defender ATP with Conditional Access in Intune](../protect/advanced-threat-protection.md).

## Reports summary 

The device compliance report is available as the summary report in the **Reports** workload. Use the following steps to view the device compliance report:

1. Sign in to the [Microsoft Endpoint Manager admin center](https://go.microsoft.com/fwlink/?linkid=2109431).
2. Select **Reports** to view the reports summary.

    ![Intune Reports summary](./media/intune-reports/intune-reports-01.png)

## Antivirus agent status report (Organizational)
The **Antivirus agent status** report provides the agent status of your organization's devices. This report shows which devices have real-time or network protection, as well as their state. The data found in this report is timely, calls out the unhealthy device, the user name, and severity. This report shows data visualizations as a pie chart for a breakdown of agent status count across devices. In addition, remote actions are included in this report. The report is available from the primary **Microsoft Defender Antivirus** workload. This report provides filtering, searching, paging, and sorting. 

You can view the **Antivirus agent status** report using the following steps:

1. Sign in to the [Microsoft Endpoint Manager admin center](https://go.microsoft.com/fwlink/?linkid=2109431).
2. Select **Reports** > **Microsoft Defender Antivirus** > **Antivirus agent status**.

## Detected malware report (Organizational)
The **Detected malware** report provides the malware state of your organization's devices. This report shows the number of devices with detected malware, as well as malware details. The data found in this report is timely, calls out the device name and severity, as well as other malware related details. This report show a pie chart for the count of devices in each malware state. The report is available from the primary **Microsoft Defender Antivirus** workload. This report also provides filtering, searching, paging, and sorting. 

You can view the **Detected malware** report using the following steps:

1. Sign in to the [Microsoft Endpoint Manager admin center](https://go.microsoft.com/fwlink/?linkid=2109431).
2. Select **Reports** > **Microsoft Defender Antivirus** > **Detected malware**.

## Windows 10 feature updates (Organizational)
The **Windows 10 feature updates** report provides an overall view of compliance for devices that are targeted with a **Windows 10 feature updates** policy. This report provides the update status based on update state. You can also see specific device update details. The data found in these reports is timely, calls out the device name and state, as well as other update related details. A summary report is available in the **Windows updates** workload. This report also provides filtering, searching, paging, and sorting. 

You can view the **Windows 10 feature updates** report using the following steps:

1. Sign in to the [Microsoft Endpoint Manager admin center](https://go.microsoft.com/fwlink/?linkid=2109431).
2. Select **Reports** > **Windows updates** to view the summary report.
3. Select the **Reports** tab and click the **Windows Feature Update Report** to see the **Windows 10 feature updates** report.

## Device compliance trend report (Historical)

Device compliance trend reports are more likely to be used by admins and architects to identify long term trends for device compliance. The aggregated data is displayed over a period of time, and is useful for making future investment decisions, driving process improvements, or prompting investigation into any anomalies. Filters can also be applied to see specific trends. The data provided by this report is a snapshot of the current tenant state (near real-time). 

A device compliance trend report for device compliance trends can show the trend of device compliance states over a period of time. You can identify where compliance peaks occurred and focus your time and effort accordingly.

You can view the **Trends** report using the following steps:

1. Sign in to the [Microsoft Endpoint Manager admin center](https://go.microsoft.com/fwlink/?linkid=2109431).
2. Select **Reports** > **Trends** to view device compliance over a 60 day trend.

    ![Intune trend report](./media/intune-reports/intune-reports-03.png)

## Azure Monitor integration reports (Specialist)
You can customize your own reports to get the data you want. The data in your reports will optionally be available via [Azure Monitor](/azure/azure-monitor/overview) using [Log Analytics](reports.md#log-analytics) and [Azure Monitor workbooks](reports.md#workbooks). These solutions allow you to create custom queries, configure alerts, and make dashboards to show the device compliance data in the manner you want. Additionally, you can retain the activity logs in your Azure storage account, integrate with the reports using [security information and event management (SIEM) tools](/microsoft-365/security/office-365-security/siem-server-integration), and correlate the reports to Azure AD activity logs. Azure Monitor workbooks can be used in addition to importing dashboards for custom reporting needs.

> [!NOTE]
> Complex reporting functionality require an Azure subscription.

An example specialist report would corelate device ownership data with platform enrollment data in a custom report. Then, this custom report could be displayed on an existing dashboard in the Azure Active Directory portal.

You can create and view custom reports using the following steps:

1. Sign in to the [Microsoft Endpoint Manager admin center](https://go.microsoft.com/fwlink/?linkid=2109431).
2. Select **Reports** > **Diagnostic settings** add a [diagnostic setting](reports.md#diagnostic-settings).

    ![Intune Reports - Add diagnostic setting](./media/intune-reports/intune-reports-04.png)

3. Click **Add diagnostic setting** to display the **Diagnostic settings** pane. 
4. Add a **Name** for the diagnostic settings. 
5. Select the **Send to Log Analytics** and **DeviceComplianceOrg** settings.

    ![Intune Reports - Diagnostic settings](./media/intune-reports/intune-reports-04a.png)

6. Click **Save**.
7. Next, select **Log analytics** to create and run a new log query using [Log Analytics](reports.md#log-analytics).

   ![Log Analytics - Log query](./media/intune-reports/intune-reports-05.png)

8. Select **Workbooks** to create or open an interactive report using [Azure Monitor workbooks](reports.md#workbooks).

   ![Workbooks - Interactive reports](./media/intune-reports/intune-reports-07.png)

### Diagnostic settings
Each Azure resource requires its own diagnostic setting. The diagnostic setting defines the following for a resource:

- Categories of logs and metric data sent to the destinations defined in the setting. The available categories will vary for different resource types.
- One or more destinations to send the logs. Current destinations include Log Analytics workspace, Event Hubs, and Azure Storage.
- Retention policy for data stored in Azure Storage.

A single diagnostic setting can define one of each of the destinations. If you want to send data to more than one of a particular destination type (for example, two different Log Analytics workspaces), then create multiple settings. Each resource can have up to 5 diagnostic settings.

For more information, about diagnostic settings, see [Create diagnostic setting to collect platform logs and metrics in Azure](/azure/azure-monitor/platform/diagnostic-settings).

### Log Analytics
Log Analytics is the primary tool in the Azure portal for writing log queries and interactively analyzing the results of the queries. Even if a log query is used elsewhere in Azure Monitor, you'll typically write and test the query first using Log Analytics. For details about using Log Analytics and creating log queries, see [Overview of log queries in Azure Monitor](/azure/azure-monitor/log-query/log-query-overview). 

### Workbooks
Workbooks combine text, Analytics queries, Azure Metrics, and parameters into rich interactive reports. Workbooks are editable by any other team members who have access to the same Azure resources. For more information about workbooks, see [Azure Monitor workbooks](/azure/azure-monitor/app/usage-workbooks). Also, you can work with and contribute to workbook templates. For more information, see [Azure Monitor Workbook Templates](https://go.microsoft.com/fwlink/?linkid=867045).

## Next steps 

Learn more about the following technologies:
- [Blog - Microsoft Intune reporting framework](https://techcommunity.microsoft.com/t5/Intune-Customer-Success/New-Reporting-Framework-Coming-to-Intune/ba-p/1009553)
- [Azure Monitor](/azure/active-directory/reports-monitoring/concept-activity-logs-azure-monitor)
- [What is Log Analytics?](/azure/azure-monitor/log-query/log-query-overview#what-is-log-analytics)
- [Log queries](/azure/azure-monitor/log-query/log-query-overview)
- [Get started with Log Analytics in Azure Monitor](/azure/azure-monitor/log-query/get-started-portal)
- [Azure Monitor workbooks](/azure/azure-monitor/app/usage-workbooks)
- [security information and event management (SIEM) tools](/microsoft-365/security/office-365-security/siem-server-integration)