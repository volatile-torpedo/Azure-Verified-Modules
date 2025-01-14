---
title: Issue/Triage Automation
geekdocNav: true
geekdocAlign: left
geekdocAnchor: true
geekdocToC: 1
---

{{< toc >}}

This page details the automation that is in place to help with the triage of issues and PRs raised against the AVM modules.

## Schedule based automation

This section details all automation rules that are based on a schedule.

{{< hint type=note >}}
When calculating the number of business days in the issue/triage automation, the built-in logic considers Monday-Friday as business days. The logic doesn't consider any holidays.
{{< /hint >}}

### ITA01TF.1-2

If a bug/feature/request/general question is not responded to after 3 business days, then the AVM Core team will be tagged in a comment on the issue to reach out to the module owner. The AVM core team will also be assigned on the issue.

### ITA01BCP.1-2

If a bug/feature/request/general question that has the label of "<mark style="background-color:#F0FFFF;">Type: AVM 🅰️ ✌️ ⓜ️</mark>" is not responded to after 3 business days, then the AVM Core team will be tagged in a comment on the issue to reach out to the module owner. The AVM core team will also be assigned on the issue.

### ITA02BCP.1-2

If after an additional 3 business days there's still no update to the issue that has the label of "<mark style="background-color:#F0FFFF;">Type: AVM 🅰️ ✌️ ⓜ️</mark>", the AVM core team will be assigned to the issue and a further comment stating module owner is unresponsive.

### ITA02TF.1-2

If after an additional 3 business days there's still no update to the issue, the AVM core team will be assigned to the issue and a further comment stating module owner is unresponsive.

### ITA03BCP

If after 5 days (total from start of issue being raised) and no response the Bicep PG GitHub Team will be tagged and assigned to the issue to assist.

### ITA03TF

If after 5 days (total from start of issue being raised) and no response the Terraform PG GitHub Team will be tagged and assigned to the issue to assist.

### ITA04

If an issue/PR has been labelled with "<mark style="background-color:#CB6BA2;color:white;">Needs: Author Feedback 👂</mark>" and hasn't had a response in 4 days, label with "<mark style="background-color:#808080;color:white;">Status: No Recent Activity 💤</mark>" and add a comment.

### ITA05

If an issue/PR has been labelled with "<mark style="background-color:#808080;color:white;">Status: No Recent Activity 💤</mark>" and hasn't had any update in 3 days from that point, automatically close it and comment, unless the issue/PR has a "<mark style="background-color:#B60205;color:white;">Status: long-term ⏳</mark>" - in which case, do not close it.

<br>

## Event based automation

This chapter details all automation rules that are based on an event.

### ITA06

When a new issue of any type is created add the "<mark style="background-color:#FBCA04;">Needs: Triage 🔍</mark>" label.

### ITA07

When a new PR of any type is created add the "<mark style="background-color:#FBCA04;">Needs: Triage 🔍</mark>" label.

### ITA08BCP

If AVM or "Azure Verified Modules" is mentioned in an uncategorized issue (i.e., one not using any template), apply the label of "<mark style="background-color:#F0FFFF;">Type: AVM 🅰️ ✌️ ⓜ️</mark>" on the issue.

### ITA09

When #RR is used in an issue, add the label of "<mark style="background-color:#CB6BA2;color:white;">Needs: Author Feedback 👂</mark>".

### ITA10

When #wontfix is used in an issue, mark it by using the label of "<mark style="background-color:#FFFFFF;">Status: Won't Fix 💔</mark>" and close it as not planned.

### ITA11

When a reply from anyone to an issue occurs, remove the "<mark style="background-color:#CB6BA2;color:white;">Needs: Author Feedback 👂</mark>" label and label with "<mark style="background-color:#E99695;color:white;">Needs: Attention 👋</mark>".

### ITA12

Clean up e-mail replies to GitHub Issues for readability.

### ITA13

If the language is set to Bicep in the Module proposal, assign the "<mark style="background-color:#1D73B3;color:white;">Language: Bicep 💪</mark>" label on the issue.

### ITA14

If the language is set to Terraform in the Module proposal, assign the "<mark style="background-color:#7740B6;color:white;">Language: Terraform 🌐</mark>" label on the issue.

### ITA15

Remove the "<mark style="background-color:#FBCA04;">Needs: Triage 🔍</mark>" label from a PR, if it already has a "<mark>Type: *XYZ*</mark>" label assigned at the time of creating it.

### ITA16

Add the "<mark style="background-color:#FBEF2A;">Status: Owners Identified 🤘</mark>" label when someone is assigned to a Module Proposal.

<br>

## Where to apply these rules?

The below table details which repositories the above rules are applied to.

| ID                          | AVM Core repository | BRM repository | TF repositories |
|-----------------------------|:-------------------:|:--------------:|:---------------:|
| [ITA01BCP1-2](#ita01bcp1-2) |                     |       ✔️       |                 |
| [ITA01TF1-2](#ita01tf1-2)   |                     |                |       ✔️        |
| [ITA02BCP1-2](#ita02bcp1-2) |                     |       ✔️       |                 |
| [ITA02TF1-2](#ita02tf1-2)   |                     |                |       ✔️        |
| [ITA03BCP](#ita03bcp)       |                     |       ✔️       |                 |
| [ITA03TF](#ita03tf)         |                     |                |       ✔️        |
| [ITA04](#ita04)             |         ✔️          |       ✔️       |       ✔️        |
| [ITA05](#ita05)             |         ✔️          |       ✔️       |       ✔️        |
| [ITA06](#ita06)             |         ✔️          |       ✔️       |       ✔️        |
| [ITA07](#ita07)             |         ✔️          |       ✔️       |       ✔️        |
| [ITA08BCP](#ita08bcp)       |                     |       ✔️       |                 |
| [ITA09](#ita09)             |         ✔️          |       ✔️       |       ✔️        |
| [ITA10](#ita10)             |         ✔️          |       ✔️       |       ✔️        |
| [ITA11](#ita11)             |         ✔️          |       ✔️       |       ✔️        |
| [ITA12](#ita12)             |         ✔️          |       ✔️       |       ✔️        |
| [ITA13](#ita13)             |         ✔️          |                |                 |
| [ITA14](#ita14)             |         ✔️          |                |                 |
| [ITA15](#ita15)             |         ✔️          |       ✔️       |       ✔️        |
| [ITA16](#ita16)             |         ✔️          |                |                 |
