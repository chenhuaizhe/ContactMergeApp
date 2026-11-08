# 常见问题解答 (FAQ)

- **概览与语言**：[简体中文概览](../readme/README.zh-Hans.md) | [English Overview](../../README.md)
- **使用指南**：[快速入门](quick-start.md) | [备份与恢复记录](recovery.md) | [权限与问题排查](permissions-troubleshooting.md) | **常见问题 (FAQ)**
- **语言 / Language**：**简体中文** | [English](../en/faq.md)

围绕在 iPhone 上安全使用 **ContactMerge+ Cleaner** 的实用解答，并明确标注已核实的产品表现与版本限制边界。

## 备份与重复项匹配（`q01`–`q06`）

<a id="q01"></a>
### 1. 合并前是否需要准备 `.vcf` 备份，还是仅靠 `Recovery History`（恢复记录）就够了？

导出 `.vcf` 文件属于可选项——应用不会在合并前强制要求导出——但在首次清理或进行较大规模整理前，强烈建议您提前保留一份带日期的独立备份。`Recovery History`（恢复记录）只是应用保存在设备本地的有限恢复日志（最多保留 3 条合并记录和最多 3 条删除记录，在本机保存约 30 天），无法还原非主联系人名片上的备注（Notes），也没有开发者云备份。同时，账户同步（如 iCloud 或 Google）不等于独立备份，因为合并结果可能会同步到关联设备。请确认您的备份覆盖了实际存放联系人的源账户且包含预期的联系人记录，并避免反复重新导入 `.vcf` 文件或盲目执行整机恢复。详见[备份与恢复记录](recovery.md)及官方指南[在 iPhone 上合并联系人前如何备份（英文）](https://contactmerge.app/guides/backup-contacts-before-merge-iphone)。

<a id="q02"></a>
### 2. `Ready to merge` 是什么意思？确认前还需要打开预览查看吗？

`Ready to merge`（合并就绪）表示该分组内的每一对名片都基于充分的匹配证据通过了严格核验。尽管如此，确认前仍请务必打开合并预览（`Merge Preview`）查看：仅凭相同的姓名或电话号码并不能证明两张名片代表同一个人，而且本应用无法读取联系人备注（Notes）。请选定要保留的主联系人名片，前往 Apple 系统**“通讯录”**应用查看非主联系人名片上是否有备注需要保存，在合并预览中核实预期保留的字段，然后再确认合并（或将已确认的 `Ready to merge` 分组纳入 Pro 批量合并）。详见[快速入门](quick-start.md)及[如何安全地合并联系人（英文）](https://contactmerge.app/guides/merge-contacts-safely)。

<a id="q03"></a>
### 3. 为什么某个分组会被标为 `Needs review`？可以对它使用批量合并吗？

`Needs review`（需人工核对）表示名片之间的匹配证据较弱或存在冲突——例如共用家庭固话号码、姓名写法不一致、生日信息冲突或仅有部分信息重叠。这是一项保守的安全保护机制，并非扫描出错。`Needs review` 分组必须每次一组由人工逐一检查与确认，无法纳入 Pro 批量合并（也没有将证据模糊的分组强制纳入批量合并的方式）。如果无法确定各张名片属于同一个人，请保持不合并。详见[快速入门](quick-start.md)。

<a id="q04"></a>
### 4. 姓名不同时应该合并吗？或者两张名片姓名完全相同时就一定该合并吗？

两者都不能自动下结论。姓名存在差异（例如昵称与全名）并不自动代表是两个不同的人；反过来，姓名完全相同的两张名片也可能分别属于同名的亲属或同事。本文档不对运行时匹配中的大小写处理或文本归一化算法规则做精确断言。在合并预览中，请比对那里实际显示的信息（如存在时显示的姓名、电话号码和电子邮箱地址）——切勿因为某个字段或备注未在预览中显示，就假设源名片上该项为空。请打开 Apple 系统**“通讯录”**应用中的原始名片，核实公司/单位信息、其他补充身份详情以及需要保存的备注（Notes）；如果您切出本应用在那里查看或编辑过名片，返回后请先重新核对当前的候选列表与合并预览再确认（请勿假设已打开的页面会自动刷新）。详见[快速入门](quick-start.md)。

<a id="q05"></a>
### 5. 两个不同的人共用同一个家庭固话或公司总机号码，我该如何处理？

请**不要**合并他们。共用家庭座机的家人、留有相同紧急联系电话的伴侣，或共用公司前台总机的同事，常会作为候选分组出现——通常归在 `Needs review` 中。一旦合并，就会把两个独立人物的信息混入同一张名片。请让代表不同人物的名片保持独立不合并，仅当组内每张名片都明确指向现实中的同一个人时才确认合并。详见[快速入门](quick-start.md)。

<a id="q06"></a>
### 6. 为什么生日信息冲突会将某个分组标记为需要人工核对？

名片之间出现相互冲突的生日信息（在历史 1.3.6 版本的发布与支持记录中曾与姓名冲突一同提及），是提示您进行人工核对的实用线索，而非公开承诺的精确算法阈值。不同的生日日期既可能意味着共用联系方式的两位亲属，也可能是旧名片上录入有误。决定是否合并前，请先在合并预览与 Apple 系统**“通讯录”**应用中核实两张名片的详情。详见[快速入门](quick-start.md)。

## 账户同步、换机迁移与 Apple 系统“通讯录”应用（`q07`–`q11`）

<a id="q07"></a>
### 7. 本应用如何与 iCloud 或 Google 联系人同步配合工作？

联系人数据在您的 iPhone 本地进行处理，不会上传至开发者服务器，也没有开发者云备份服务。不过，iCloud/Google 账户同步与 iOS 系统备份属于由您自身设置控制的独立机制，因此已确认的合并结果可能会同步到您连接的其他设备上。排查问题时，切勿反复开关同步、移除账户、轻点 `"Delete from My iPhone"`（从我的 iPhone 删除）或删除已同步的源联系人——删除电子邮箱或云账户中的联系人可能会在多台设备间将其永久删除（参阅 Apple 官方[账户管理指南（英文）](https://support.apple.com/guide/iphone/add-or-remove-accounts-iph7edacccf9/ios)与[删除风险提示（英文）](https://support.apple.com/en-us/111793)）。行动前请先确认联系人所属账户并做好独立备份；如有疑问，请立即停止并联系[官方支持（英文）](https://contactmerge.app/support)。另请参阅[iCloud 同步后出现重复联系人（英文）](https://contactmerge.app/guides/icloud-duplicate-contacts-after-sync)。

<a id="q08"></a>
### 8. 为什么设置新 iPhone 或使用“转移到 iOS”（Move to iOS）后出现了重复联系人？

设置新 iPhone、使用“转移到 iOS”（Move to iOS）、导入文件或连接多个账户，往往会将原本分散在不同账户来源中的旧重复项同时显现出来——这并不说明您的手机有故障，也不代表单一的必然成因。扫描前请先等待数据迁移和初始后台同步完成（单靠等待并不保证能自动清除重复项，但可避免同步中途发生数据变动），随后做好独立备份，再按[快速入门](quick-start.md)查看合并预览。另请参阅[设置新 iPhone 后出现重复联系人（英文）](https://contactmerge.app/guides/duplicate-contacts-after-new-iphone)与[使用“转移到 iOS”后出现重复联系人（英文）](https://contactmerge.app/guides/move-to-ios-duplicate-contacts)。

<a id="q09"></a>
### 9. Apple 系统“通讯录”应用没有显示重复项提示（`View Duplicates`）——本应用与之有何不同？

在 Apple 系统**“通讯录”**应用中，当系统提示可用时会在个人名片（`My Card`）下方显示 `View Duplicates`；而手动关联联系人（`Link Contacts`）只是统一展示视图，并不会真正合并底层的源名片（且在统一名片上的修改可能会同步回源账户；参阅 Apple 官方[重复联系人指南（英文）](https://support.apple.com/guide/iphone/merge-or-hide-duplicate-contacts-iph2ab28320d/ios)）。系统未显示 `View Duplicates` 与本应用的权限设置并非同一回事——不存在保证触发的 1,000 个联系人阈值、固定等待时间或安全的“一键全部合并”万用解法。您可以在授予 ContactMerge+ Cleaner 通讯录权限后进行本地扫描，并逐一核对合并预览。详见[权限与问题排查](permissions-troubleshooting.md)。

<a id="q10"></a>
### 10. 同一个电话号码一张名片带国家/地区代码、另一张不带，也会形成重复联系人吗？

会的——有时一张名片保存的是本地号码格式，另一张则带有国家或地区代码前缀（例如 `+1`），Apple 系统自带的重复项提示未必会将其标为完全一致的重复项。本文档不对内部号码归一化算法规则做精确断言，但您可以在 ContactMerge+ Cleaner 的合并预览中直观比对完整号码。确认前请核实两张名片确实属于同一个人，并确认保留了您预期的号码格式。详见[iOS 重复项提示与国家/地区代码格式说明（英文）](https://contactmerge.app/guides/ios-view-duplicates-country-code)。

<a id="q11"></a>
### 11. 联系人列表数量较多时，ContactMerge+ Cleaner 可以处理吗？

即使在联系人数量较多、Apple 系统“通讯录”应用未显示 `View Duplicates` 的情况下，您依然可以使用本应用在设备本地进行扫描，并在 `Ready to merge` 与 `Needs review` 分类中查看候选结果。不过，本应用不承诺具体的扫描速度或无限制的容量上限。建议先等待后台同步结束、创建一份带日期的独立备份，并先挑选单个分组测试合并。详见[权限与问题排查](permissions-troubleshooting.md)及[联系人数量较多时未显示重复项提示（英文）](https://contactmerge.app/guides/view-duplicates-missing-large-contact-list)。

## 撤销、恢复记录与联系人备注（`q12`–`q14`）

<a id="q12"></a>
### 12. `Undo Last Contact Merge`（撤销上一次联系人合并）在哪里？它覆盖什么范围？

`Undo Last Contact Merge` 仅针对您最近完成的单次合并操作。在已获批核实的 `2026-11-03` 英文 Release 模拟器演示截图中，它位于 `Duplicate Contacts`（重复联系人）扫描结果界面顶部、`Ready to merge` 区域的上方。由于该位置信息基于上述特定日期的模拟器截图，而非对您所安装版本的实机运行测试，实际可点击状态、文字标签及确认提示可能会因版本而异；同时它并非完整的系统恢复（无法还原非主联系人名片上的备注，原始系统标识符与关联关系也可能不会恢复）。详见[备份与恢复记录](recovery.md)。

<a id="q13"></a>
### 13. `Recovery History`（恢复记录）有哪些限制？应该如何打开？

`Recovery History`（恢复记录）在您的设备本地**最多保存 3 条合并记录和最多 3 条删除记录**，保存期**约 30 天**（两类记录各自独立计算上限，并非保证随时有 6 条可用记录）。过期记录或超出单类 3 条上限的旧记录无法还原；卸载应用或丢失、更换设备后也无法保证恢复。**入口路径未核实**：由于已核实的截图中未展示其入口与记录选择步骤，我们不会猜测具体的菜单路径——如需针对您所安装版本的指引，请联系[官方支持（英文）](https://contactmerge.app/support)。详见[备份与恢复记录](recovery.md)。

<a id="q14"></a>
### 14. 为什么合并前要在 Apple 系统“通讯录”应用中查看备注（Notes）？还有哪些因素会限制恢复？

ContactMerge+ Cleaner 无法读取联系人备注：非主联系人名片上的备注在合并时**不会**被复制，事后也无法通过“撤销”或 `Recovery History`（恢复记录）找回。合并预览中未显示备注绝不代表名片本身没有备注——请务必先前往 Apple 系统**“通讯录”**应用查看并复制重要备注。在应用外查看或编辑联系人后，返回本应用时请重新核对当前的候选列表与合并预览（已打开的界面未必会自动刷新）。此外，原始系统标识符（ID）与关联关系可能无法还原；出于保守安全提示，合并后若对联系人进行了后续编辑或发生了同步覆盖，也可能影响顺利还原。详见[备份与恢复记录](recovery.md)。

## 免费版与专业版、购买恢复及支持服务（`q15`–`q18`）

<a id="q15"></a>
### 15. 免费版（Free）和专业版（Pro）分别包含哪些功能？

**Free（免费版）**支持扫描、查看所有候选重复分组，以及每次合并 1 个分组（该组内最多包含 3 个联系人，不含多分组批量合并）。**Pro（专业版）**为 App Store 一次性买断解锁，**无订阅费用**，价格按 Apple 在您所在地区商店展示的当地定价为准。Pro 解锁超过 3 个联系人的分组合并，并支持在确认后对 `Ready to merge` 分组进行批量合并（`Needs review` 分组仍须逐组人工核对）。详见[快速入门](quick-start.md)。

<a id="q16"></a>
### 16. 我该如何恢复已购买的 Pro 专业版权益？

Pro 属于非消耗型内购项目。请确认您的 iPhone 登录了当初购买时使用的**同一 Apple 账户（Apple Account）**，并查阅 Apple 官方支持文章：[如果找不到或无法使用 App 内购买项目（英文）](https://support.apple.com/en-us/108096)。由于应用内恢复购买的具体界面路径在本文档中未经核实，我们不猜测“设置”或“升级”等菜单名称，不建议重复购买，也不承诺一定自动恢复。如果 Pro 仍处于未解锁状态，请联系[官方支持（英文）](https://contactmerge.app/support)或 Apple 官方支持。详见[权限与问题排查](permissions-troubleshooting.md)。

<a id="q17"></a>
### 17. Apple 退款流程是怎样的？有没有需要取消的订阅？

Pro 是一次性购买项目而非订阅制——请勿针对本应用执行取消订阅的操作步骤。App Store 的账单结算由 Apple 处理，是否符合退款条件由 Apple 根据所在国家或地区规则决定，**退款并非保证获批**。如需申请退款，请通过 Apple 官方退款流程在 [reportaproblem.apple.com（英文）](https://reportaproblem.apple.com) 提交（参阅 Apple [官方退款指南（英文）](https://support.apple.com/en-us/118223)）；开发者无法保证退款申请获得批准。详见[权限与问题排查](permissions-troubleshooting.md)。

<a id="q18"></a>
### 18. 如何检查通讯录权限、保护个人隐私并安全地联系官方支持？

请前往 iOS 系统“设置”的隐私与通讯录权限设置中查看授权状态（英文路径参考 `Settings > Privacy & Security > Contacts`，具体系统菜单名称可能因 iOS 版本或语言设置略有差异；参阅 Apple [通讯录访问权限指南（英文）](https://support.apple.com/guide/iphone/control-access-to-contacts-iph9536aa9a5/ios)）；受限访问仅会限制应用可见范围而不会删除联系人，但本应用不保证兼容所有受限访问流程。联系人处理均在设备本地完成，不会上传至开发者服务器（与您自身的 iCloud/Google 同步及 iOS 备份相互独立；详见[隐私政策（英文）](https://github.com/chenhuaizhe/ContactMergeApp/blob/main/privacy-policy.md)）。联系[官方支持（英文）](https://contactmerge.app/support)时，可提供应用版本号、iOS 版本号、问题是出现在 Apple 系统控件还是本应用界面、账户类型（不含账户 ID）、大致联系人数量以及预期与实际观察到的表现——切勿在公开渠道发布私人联系人列表、`.vcf` 文件、真实个人隐私信息、密码或付款收据。详见[权限与问题排查](permissions-troubleshooting.md)。

## 文档状态

核对日期：2026 年 11 月 8 日。实际界面、名称与具体表现可能因您安装的 App 版本和 iOS 版本而异。
