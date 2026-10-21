# Microsoft Entra Privileged Identity Management: <br/>Just-in-Time Role Activation and Access Governance

Microsoft Entra 特權身分管理：即時角色啟用與存取治理

<br/>

---------

<h2>Outline｜專題簡介</h2>

This project demonstrates identity authentication and access control management in Microsoft Entra ID, including multifactor authentication (MFA), MFA account lockout, and Conditional Access policy configuration.

本專題展示 Microsoft Entra ID 中的身分驗證與存取控制管理，包括多重要素驗證 (MFA)、MFA 帳號鎖定，以及條件式存取政策設定。

It explores how MFA provides an additional layer of authentication beyond passwords, while Conditional Access enables administrators to apply targeted access controls based on users and cloud resources.

內容進一步探討 MFA 如何在密碼之外提供額外的身分驗證層級，以及 Conditional Access 如何讓管理員依據使用者與雲端資源套用特定的存取控制。

The Conditional Access What If tool is also used to evaluate policy behaviour across different application access scenarios, demonstrating how access policies can be validated before or during deployment.

此外，透過 Conditional Access What If 工具評估不同應用程式存取情境下的政策行為，以展示如何在政策部署前或部署期間驗證存取控制結果。

<br/>

---------

<h2>Key Learning Outcomes｜主要學習成果</h2>

* Enable multifactor authentication (MFA) for a selected user<br/>
為指定使用者啟用多重要素驗證 (MFA)

* Review MFA service settings and available authentication controls<br/>
檢視 MFA 服務設定與可用的身分驗證控制

* Configure MFA account lockout settings<br/>
設定 MFA 帳號鎖定機制

* Create and configure a Conditional Access policy<br/>
建立並設定 Conditional Access 政策

* Configure user inclusion and administrative exclusions<br/>
設定使用者納入範圍與管理員排除條件

* Restrict access to a selected cloud application<br/>
限制指定雲端應用程式的存取

* Apply block access controls through Conditional Access<br/>
透過 Conditional Access 套用封鎖存取控制

* Validate Conditional Access policies using the What If tool<br/>
使用 What If 工具驗證 Conditional Access 政策

* Compare policy outcomes across different application access scenarios<br/>
比較不同應用程式存取情境下的政策結果

<br/>

---------

<h2>Tools and Concepts Covered｜涵蓋工具與概念</h2>

| Category (分類)                                      | Tools / Concepts (工具 / 概念)       |
| ------------------------------------------------ | ------------------------------ |
| Cloud Identity Management <br/>雲端身分管理          | Microsoft Entra ID |
| Identity Administration <br/>身分管理                | Microsoft Entra Admin Center |
| Multifactor Authentication <br/>多重要素驗證          | Microsoft Entra MFA |
| User-Based MFA <br/>使用者式 MFA                    | Per-user MFA |
| MFA Configuration <br/>MFA 設定                    | MFA Service Settings |
| Account Protection <br/>帳號保護                    | MFA Account Lockout |
| Access Control <br/>存取控制                        | Conditional Access |
| Policy Assignments <br/>政策指派                    | Users and Groups |
| Administrative Exclusions <br/>管理員排除            | Excluded Users |
| Cloud Resource Control <br/>雲端資源控制             | Target Resources |
| Access Controls <br/>存取控制措施                    | Block Access |
| Policy Evaluation <br/>政策評估                     | Conditional Access What If |
| Application-Based Access <br/>應用程式存取控制         | Office 365 |
| Policy Validation <br/>政策驗證                     | Applied and Not Applied Policies |


<br/>

---------

<h2>Materials and Methods｜材料與方法</h2>

[Environment]

* Microsoft Azure Portal (Azure 雲端管理平台)</b>
* Microsoft Entra ID tenant (Entra ID 租戶環境)</b>
* Microsoft Entra ID P2 - Trial (Microsoft Entra ID P2 - 試用版)</b>
* Microsoft Entra admin center (Microsoft Entra 管理中心)</b>

[Tasks]

* Configure MFA Account Lockout (設定 MFA 帳號鎖定)
* Configure Conditional Access (設定 Conditional Access)
* Validate Conditional Access with What If (使用 What If 驗證 Conditional Access)
<br/>

---------

<h2>Practice｜實踐</h2> <p align="center">

<p align="center">
<b>Task 1: Configure MFA Account Lockout<br/> (設定 MFA 帳號鎖定)</b><br/>
<img src="https://i.imgur.com/WdPIUHO.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<b>Task 2-1: Configure User Assignment and Exclusion<br/> (設定使用者指派與排除)</b><br/>
<img src="https://i.imgur.com/CTmcBxT.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<b>Task 2-2: Configure the Target Resource<br/> (設定目標資源)</b><br/>
<img src="https://i.imgur.com/1F6Q4qY.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<b>Task 2-3: Configure Block Access<br/> (設定封鎖存取)</b><br/>
<img src="https://i.imgur.com/P0uvv2U.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<b>Task 3-1: Validate the Block Policy with What If<br/> (使用 What If 驗證封鎖政策)</b><br/>
<img src="https://i.imgur.com/2W8NL6B.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
* Used the Conditional Access What If tool to verify that the Office 365 block policy applies to the selected test user. <br/>The policy remained in Report-only mode without enforcing the access restriction.<br/>
透過 Conditional Access What If 工具驗證 Office 365 封鎖政策適用於指定測試使用者；<br/>政策維持 Report-only 模式，並未實際強制執行存取限制<br/>
<br />
<br />
<b>Task 3-2: Compare Conditional Access Results<br/> (比較 Conditional Access 政策結果)</b><br/>
<img src="https://i.imgur.com/viFvKGi.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

---------

<h2>Results｜專題結論</h2>

This project demonstrated identity authentication protection and access control management in Microsoft Entra ID through MFA account lockout and Conditional Access policies. MFA account lockout was configured to limit repeated denied authentication attempts and provide additional protection against abusive MFA requests.

本專題透過 MFA 帳號鎖定與 Conditional Access 政策，實作 Microsoft Entra ID 中的身分驗證防護與存取控制管理。MFA 帳號鎖定可限制重複遭拒的驗證嘗試，並為異常或濫用的 MFA 請求提供額外防護。

Conditional Access was configured with specific user assignments, administrative exclusions, target resources, and block access controls. This demonstrated how access policies can be scoped to selected identities and cloud resources rather than being applied universally across the tenant.

Conditional Access 則透過指定使用者、管理員排除、目標資源及封鎖存取控制進行設定，展示存取政策如何針對特定身分與雲端資源套用，而非一律套用至整個租戶環境。

The Conditional Access What If tool was used to compare policy outcomes across different target resources. The analysis demonstrated how the same user can receive different policy evaluation results depending on whether the requested application matches the configured policy scope.

最後使用 Conditional Access What If 工具比較不同目標資源下的政策結果，確認相同使用者會依據所存取的應用程式是否符合政策範圍，而產生不同的政策評估結果。


<br />
<br />



---------

<h2>Security Insight｜安全洞察</h2>


Identity protection is more effective when authentication controls and access policies are applied in layers. MFA account lockout can help limit repeated denied authentication requests, while Conditional Access provides more granular control over who can access specific resources and under what conditions.

身分安全在採用多層次控制時能發揮更完整的效果。MFA 帳號鎖定可限制重複遭拒的驗證請求，而 Conditional Access 則能進一步控制哪些使用者可存取特定資源，以及存取行為需要符合哪些條件。

Conditional Access policies should be scoped carefully. Including only the required users and resources helps reduce unnecessary access disruption, while excluding appropriate administrative or emergency-access accounts can reduce the risk of accidentally locking administrators out of the environment.

Conditional Access 政策應謹慎設定適用範圍。僅納入必要的使用者與資源，可降低非預期的存取中斷；適當排除管理帳號或緊急存取帳號，則有助於避免政策設定錯誤造成管理人員無法進入環境。

Policy configuration alone does not confirm that access controls will behave as intended. The What If tool provides a practical way to evaluate Conditional Access decisions by comparing applicable and non-applicable scenarios before relying on the policy in normal operations.

僅完成政策設定並不能證明存取控制一定會依照預期運作。透過 What If 工具比較政策適用與不適用的情境，可在實際依賴政策進行存取控制前，更清楚地驗證 Conditional Access 的判斷結果。

The MFA account lockout values and Conditional Access scenarios used in this project were based on the lab environment and should not be treated as universal production settings. In a real organisation, authentication thresholds, policy exclusions, target resources, and enforcement modes should be adjusted according to risk, operational requirements, and potential business impact.

本專題使用的 MFA 帳號鎖定參數與 Conditional Access 情境依據實驗環境設定，不應視為所有正式環境皆適用的標準值。在實際組織中，驗證閾值、政策排除條件、目標資源及強制執行模式，仍應依據風險、營運需求與可能造成的業務影響進行調整。


<br />
<br />

---------

<h2>Reference｜參考</h2>

* [Microsoft] [Microsoft Certified: Identity and Access Administrator Associate (SC-300)](https://learn.microsoft.com/en-us/credentials/certifications/identity-and-access-administrator/?practice-assessment-type=certification)<br/>
* [Microsoft] [Get started with identity and access labs](https://learn.microsoft.com/en-au/training/modules/get-started-identity-access-labs/)<br/>
<br/>
