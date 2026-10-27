# Microsoft Entra ID Privileged Access Governance: <br/>PIM, Just-in-Time Access, and Access Reviews

Microsoft Entra ID 特權存取治理：PIM、即時存取與存取審查

<br/>

---------

<h2>Outline｜專題簡介</h2>

This project demonstrates privileged access governance in Microsoft Entra ID using Privileged Identity Management (PIM), Just-in-Time (JIT) role activation, privileged access validation, auditing, and access reviews.

本專題透過 Microsoft Entra ID Privileged Identity Management (PIM)、Just-in-Time (JIT) 角色啟用、特權存取驗證、稽核與存取審查，實作特權存取治理。

It explores how privileged roles can be assigned as eligible rather than permanently active, allowing administrative permissions to remain inactive until explicitly required. Role activation requirements such as MFA, justification, and limited activation duration provide additional controls before elevated access becomes available.

內容進一步探討如何將特權角色設定為 Eligible，而非持續維持 Active 狀態，使管理權限僅在實際需要時才進行啟用。透過 MFA、啟用理由與限時存取等要求，可在取得提升權限前建立額外控制。

Privileged access was validated before and after activation to confirm the separation between role eligibility and active administrative permissions. Audit records and access reviews were also used to examine privileged activities and evaluate whether elevated role assignments remained appropriate over time.

此外，透過比較角色啟用前後的存取結果，驗證角色資格與實際管理權限之間的差異；並利用稽核紀錄與存取審查檢查特權活動，以及評估提升權限的角色指派是否仍具持續保留的必要性。

<br/>

---------

<h2>Key Learning Outcomes｜主要學習成果</h2>

* Configure Microsoft Entra Privileged Identity Management (PIM) role settings<br/>
設定 Microsoft Entra Privileged Identity Management (PIM) 角色政策

* Assign privileged roles using eligible rather than permanently active access<br/>
以 Eligible 而非永久 Active 的方式指派特權角色

* Configure time-bound privileged role assignments<br/>
設定限時特權角色指派

* Apply activation requirements including MFA, justification, and activation duration<br/>
套用 MFA、啟用理由與啟用時間等角色啟用要求

* Activate privileged roles using Just-in-Time (JIT) access<br/>
使用 Just-in-Time (JIT) 存取啟用特權角色

* Validate access boundaries before and after privileged role activation<br/>
驗證特權角色啟用前後的存取邊界

* Deactivate privileged access after completing administrative tasks<br/>
完成管理作業後停用特權存取

* Review privileged role assignment and activation activities through audit records<br/>
透過稽核紀錄檢查特權角色指派與啟用活動

* Conduct access reviews to evaluate continued privileged access requirements<br/>
執行存取審查，以評估持續保留特權存取的必要性

* Understand how PIM supports least privilege and privileged access governance<br/>
理解 PIM 如何支援最小權限與特權存取治理

<br/>

---------


<h2>Tools and Concepts Covered｜涵蓋工具與概念</h2>

| Category (分類)                                      | Tools / Concepts (工具 / 概念)       |
| ------------------------------------------------ | ------------------------------ |
| Cloud Identity Management <br/>雲端身分管理          | Microsoft Entra ID |
| Identity Administration <br/>身分管理                | Microsoft Entra Admin Center |
| Premium Identity Features <br/>進階身分安全功能       | Microsoft Entra ID P2 (Trial) |
| Privileged Access Management <br/>特權存取管理        | Privileged Identity Management (PIM) |
| Privileged Role Management <br/>特權角色管理          | Microsoft Entra Roles |
| Privileged Role Assignment <br/>特權角色指派          | Eligible Assignment |
| Administrative Roles <br/>管理角色                   | User Administrator |
| Just-in-Time Access <br/>即時存取                    | Role Activation |
| Time-Bound Access <br/>限時存取                     | Activation Duration, Assignment Expiration |
| Strong Authentication <br/>強式身分驗證              | MFA on Activation |
| Privileged Access Controls <br/>特權存取控制          | Activation Justification |
| Least Privilege <br/>最小權限                       | Eligible vs Active Access |
| Access Validation <br/>存取驗證                     | Before and After Activation Testing |
| Privileged Access Monitoring <br/>特權存取監控        | PIM Audit History |
| Access Governance <br/>存取治理                     | Access Reviews |
| Access Recertification <br/>存取再認證               | Review Decisions and Remediation |

<br/>

---------

<br/>

---------

<h2>Materials and Methods｜材料與方法</h2>

[Environment]

* Microsoft Azure Portal (Azure 雲端管理平台)</b>
* Microsoft Entra ID tenant (Entra ID 租戶環境)</b>
* Microsoft Entra ID P2 - Trial (Microsoft Entra ID P2 - 試用版)</b>
* Microsoft Entra admin center (Microsoft Entra 管理中心)</b>

[Tasks]

* Configure Privileged Role Settings (設定特權角色政策)
* Assign an Eligible Privileged Role (指派可啟用的特權角色)
* Activate Just-in-Time Privileged Access (啟用即時特權存取)
* Validate Privileged Access Boundaries (驗證特權存取邊界)
* Review Privileged Access Activity (檢查特權存取活動)
* Perform a Privileged Access Review (執行特權存取審查)
<br/>

---------

<h2>Practice｜實踐</h2> <p align="center">

<p align="center">
<b>Task 1: Configure Privileged Role Settings<br/> (設定特權角色政策)</b><br/>
<img src="https://i.imgur.com/cKizjxV.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
* Configured the User Administrator role to require MFA and business justification during activation, <br/>with a maximum activation duration of one hour.<br/>
設定 User Administrator 角色，要求啟用時完成 MFA 與業務理由說明，<br/>並將特權啟用時間上限限制為一小時<br/>
<br />
<br />
<b>Task 2: Assign an Eligible Privileged Role<br/> (指派可啟用的特權角色)</b><br/>
<img src="https://i.imgur.com/ibt24XG.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
* Assigned the User Administrator role as a time-bound eligible assignment to a non-administrator test account, <br/>allowing temporary privilege activation without granting permanent administrative access.<br/>
將 User Administrator 角色以限時 Eligible Assignment 指派給非管理員測試帳號，<br/>使其可在指定期間內啟用特權，而無須授予永久管理權限<br/>
<br />
<br />
<b>Task 3-1: Verify Access Before Activation<br/> (驗證啟用前的存取權限)</b><br/>
<img src="https://i.imgur.com/IxMNtmd.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<b>Task 3-2: Activate the Privileged Role<br/> (啟用特權角色)</b><br/>
<img src="https://i.imgur.com/jyIOXk6.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<b>Task 3-3: Verify Active Privileged Access<br/> (驗證已啟用的特權存取)</b><br/>
<img src="https://i.imgur.com/sP9qEm6.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<b>Task 4: Deactivate Privileged Access<br/> (停用特權存取)</b><br/>
<img src="https://i.imgur.com/etwQJyB.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<b>Task 5: Review Privileged Access Activity<br/> (檢查特權存取活動)</b><br/>
<img src="https://i.imgur.com/eSEqtR7.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<b>Task 6-1: Create a Privileged Access Review<br/> (建立特權存取審查)</b><br/>
<img src="https://i.imgur.com/ixtxcWY.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
* Created a one-time access review for the User Administrator role, <br/>targeting eligible role assignments to evaluate whether privileged access remains necessary.<br/>
建立針對 User Administrator 角色的一次性存取審查，<br/>檢查 Eligible 角色指派是否仍有保留特權存取的必要<br/>
<br />
* Configured a designated reviewer and disabled automatic enforcement <br/>to maintain control over access review decisions.<br/>
指定審查人員並停用自動執行機制，以保留對存取審查決策的管理控制<br/>
<br />
<br />
<b>Task 6-2: Review the Privileged Assignment<br/> (審查特權角色指派)</b><br/>
<img src="https://i.imgur.com/nXp5Obu.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
* Reviewed the User Administrator eligible assignment for the <br/>test user and recorded an access decision with a documented justification.<br/>
審查測試使用者的 User Administrator Eligible 角色指派，<br/>並記錄存取審查決策與對應理由<br/>
<br />
* Access reviews help organisations periodically verify whether privileged assignments <br/>remain appropriate, supporting least-privilege access governance.<br/>
存取審查可協助組織定期確認特權角色指派是否仍然適當，<br/>以支援最小權限存取治理<br/>
<br />
<br />
<b>Task 6-3: Review the Access Review Result<br/> (檢查存取審查結果)</b><br/>
<img src="https://i.imgur.com/OXefyGB.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
* Completed the privileged access review and examined the <br/>recorded decisions, reviewer information, and final review status.<br/>
完成特權存取審查，並檢查已記錄的審查決策、審查人員資訊及最終審查狀態<br/>
<br />
* Access review results provide evidence of periodic privilege recertification <br/>and support accountability, compliance, and audit readiness.<br/>
存取審查結果可作為定期特權重新認證的證據，支援責任追蹤、合規管理與稽核準備<br/>
<br />
<br />



---------

<h2>Results｜專題結論</h2>

This project demonstrated privileged access governance in Microsoft Entra ID using Privileged Identity Management (PIM). A privileged role was configured as an eligible assignment rather than permanent active access, allowing administrative privileges to remain inactive until explicitly required.

本專題透過 Microsoft Entra ID Privileged Identity Management (PIM) 實作特權存取治理。特權角色以 Eligible 方式指派，而非永久維持 Active 狀態，使管理權限在實際需要前保持未啟用狀態。

The privileged role was activated through a controlled Just-in-Time (JIT) process with defined activation requirements, and access was validated before and after activation to confirm that elevated permissions were only available during the authorised period. Privileged activity was subsequently reviewed through audit records to provide visibility into role assignment and activation events.

透過具備明確啟用條件的 Just-in-Time (JIT) 流程啟用特權角色，並比較角色啟用前後的存取結果，以確認提升權限僅在授權期間內可用。隨後透過稽核紀錄檢查特權角色指派與啟用活動，提升特權存取事件的可視性。

An access review was also conducted to evaluate whether the privileged assignment remained appropriate, extending the project from temporary privilege activation into periodic access recertification and governance.

最後執行存取審查，以評估特權角色指派是否仍具必要性，將專題從暫時性權限啟用進一步延伸至定期權限再認證與存取治理。

<br />
<br />



---------

<h2>Security Insight｜安全洞察</h2>


Privileged access presents significantly higher risk than standard user access because compromised or misused administrative permissions can affect large portions of an identity environment. Replacing standing administrative access with eligible, time-bound activation reduces the duration in which privileged permissions are available and therefore helps limit the attack surface.

特權存取的風險明顯高於一般使用者權限，因為遭入侵或遭濫用的管理權限可能影響大範圍的身分環境。以 Eligible 與限時啟用取代持續存在的管理權限，可縮短特權權限實際可用的時間，進而降低攻擊面。

Just-in-Time activation also separates role eligibility from active privilege. A user may be authorised to request a privileged role without continuously holding that privilege, while activation requirements such as MFA, justification, and limited duration introduce additional controls before elevated access becomes available.

Just-in-Time 啟用亦將「具備角色資格」與「實際持有特權」分離。使用者可以具備申請特權角色的資格，而不需持續擁有該權限；MFA、啟用理由與時間限制等要求，則在取得提升權限前增加額外控制。

Privileged access should remain both temporary and auditable. Reviewing assignment, activation, and deactivation events provides evidence of how elevated permissions were used, while access reviews help determine whether users should continue to retain privileged eligibility over time.

特權存取除了應具備暫時性，也必須維持可稽核性。檢查角色指派、啟用與停用事件，可留下提升權限使用方式的證據；存取審查則有助於定期判斷使用者是否仍應保有特權角色資格。

This project also highlights that least privilege is not limited to assigning fewer permissions. Effective privileged access governance requires controlling when elevated access is available, how it is activated, how long it remains active, and whether the underlying entitlement continues to be justified.

本專題亦顯示，最小權限並不只是單純減少授予的權限。有效的特權存取治理還必須控制提升權限何時可用、如何啟用、可維持多久，以及其原始角色資格是否仍具合理性。

<br />
<br />

---------

<h2>Reference｜參考</h2>

* [Microsoft] [Microsoft Certified: Identity and Access Administrator Associate (SC-300)](https://learn.microsoft.com/en-us/credentials/certifications/identity-and-access-administrator/?practice-assessment-type=certification)<br/>
<br/>
