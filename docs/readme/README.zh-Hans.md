# ContactMerge+ Cleaner — 产品文档与支持指南

iPhone 应用 **ContactMerge+ Cleaner** 的官方公开产品文档与使用支持指南。本仓库仅提供面向用户的说明文档，并非应用源代码仓库。

ContactMerge+ Cleaner 在您的设备本地处理联系人数据，不会将您的联系人列表上传至开发者服务器，开发者也不提供云备份服务。（iOS 或账户联系人同步——例如 iCloud 或 Google——以及系统或设备备份属于独立机制，由您自己的账户与 iOS 设置控制。）

- **官方网站**：[官方网站（英文）](https://contactmerge.app)
- **App Store**：[前往 App Store 下载（英文）](https://apps.apple.com/us/app/contactmerge-contacts-cleaner/id6738980785)
- **官方支持**：[官方支持（英文）](https://contactmerge.app/support)
- **语言**：[English](../../README.md) | [Deutsch](README.de.md) | [Français](README.fr.md) | [Italiano](README.it.md) | [Español](README.es.md) | [Português (Brasil)](README.pt-BR.md) | [日本語](README.ja.md) | [한국어](README.ko.md) | **简体中文** | [繁體中文](README.zh-Hant.md)

## 4 步快速上手

1. **提前备份并授予通讯录访问权限**：在进行较大规模清理前，建议保留一份带日期的独立备份（可选择导出 `.vcf` 文件），等待手机迁移或初始同步全部完成，并在 iOS 弹出提示时允许访问通讯录。
2. **扫描**：启动扫描，在您的 iPhone 上查找可能重复的联系人分组。
3. **查看预览、选择主联系人，并在 Apple 系统“通讯录”应用中检查备注**：打开一个重复分组，核对合并预览（`Merge Preview`），选择要作为基础名片保留的主联系人，并前往 Apple 系统**“通讯录”**应用查看是否有需要保存的备注（Notes）。
4. **返回重新核对并谨慎确认**：如果您曾切出本应用，前往 Apple 系统“通讯录”应用查看或编辑过联系人，返回后请先重新核对当前的重复候选列表与合并预览。仅当各张名片明确属于同一个人、且预览保留了您预期的字段时再确认合并。

<img src="../../assets/scan-results-demo.png" alt="英文界面模拟器演示图（并非简体中文界面截图，截取于 2026-11-03）：展示使用虚构示例联系人的 Duplicate Contacts 扫描结果界面，包含 Undo Last Contact Merge、Ready to merge 与 Needs review；实际界面与文案可能因 App 或 iOS 版本而异" width="420">

*使用虚构示例联系人的模拟器演示图（英文界面，并非简体中文界面截图，截取于 2026-11-03）。实际界面、排版和文字表述可能因所安装的 App 版本或 iOS 版本而异。*

## 核心安全边界与注意事项

- **`Ready to merge` 与 `Needs review` 的区别**：
  - `Ready to merge`（合并就绪）表示该分组内的每一对联系人都基于充分匹配证据通过了严格核验。即便如此，确认前仍请务必查看合并预览——仅凭相同的姓名或电话号码，并不能证明两张名片属于同一个人。
  - `Needs review`（需人工核对）表示匹配证据较弱或存在冲突（例如共用家庭电话号码、姓名不同、生日不一致或仅有部分信息重叠）。这是安全保护机制而非扫描错误；请逐组人工检查每一个 `Needs review` 分组，切勿合并代表不同人物的名片。
- **合并前在 Apple 系统“通讯录”应用中检查并保存备注（Notes）**：
  - 非主联系人（即被合并的其他名片）上的备注**不会**被读取或复制到主联系人中，合并后也无法找回。
  - 由于 ContactMerge+ Cleaner 无法读取备注，切勿因为合并预览中未显示备注就认为该联系人没有备注。合并前请直接打开 Apple 系统**“通讯录”**应用检查并复制重要备注；如果您在系统“通讯录”应用中查看或编辑过联系人，返回 ContactMerge+ Cleaner 后请先重新核对当前的重复候选与合并预览再确认（请勿假设已打开的页面会自动刷新）。
- **撤销（Undo）与设备端恢复记录（Recovery History）**：
  - `Undo Last Contact Merge`（撤销上一次联系人合并）仅针对最近完成的单次合并操作（已核实的屏幕位置与版本说明详见[备份、撤销与恢复记录](../zh-Hans/recovery.md)）。
  - `Recovery History`（恢复记录）是本应用保存在设备本地的恢复日志，在本机最多保留 **3 条合并记录和最多 3 条删除记录**，保存期**约 30 天**（其在应用内的具体界面进入路径在本文档中未经核实；详见[备份、撤销与恢复记录](../zh-Hans/recovery.md)）。
  - **并非完整的系统恢复**：非主联系人名片上的备注无法还原，原始系统标识符与关联关系也可能无法还原。开发者不提供云备份服务（这与您自己的 iCloud/Google 同步或 iOS 系统备份相互独立，因此合并结果可能会随您的账户同步到其他设备）。作为保守预防提示，若联系人在合并后经过编辑、应用被卸载或设备丢失，则无法保证能够还原。
- **独立备份与账户安全**：导出 `.vcf` 文件为可选项，但在首次清理前建议保留一份覆盖实际联系人所属账户的带日期独立备份（账户同步不等于独立备份）。排查问题时，切勿删除源联系人、切勿轻点 `"Delete from My iPhone"`（从我的 iPhone 删除），也不要开关或移除账户。

## 免费版（Free）与专业版（Pro）

- **Free（免费版）**：扫描联系人、查看全部重复分组，并支持每次合并 1 个重复分组（该组内最多 3 个联系人）。不包含多分组批量合并。
- **Pro（专业版）**：App Store 一次性买断解锁，无订阅费用；地区价格由 Apple 直接显示。解锁超过 3 个联系人的分组合并，以及在确认后对 `Ready to merge` 分组进行批量合并（`Needs review` 分组始终需要逐一人工核对）。
- **恢复购买与账单说明**：如需在同一 Apple 账户（Apple Account）下恢复已有的 Pro 购买，或了解 Apple 退款流程（退款须通过 Apple 官方入口 [reportaproblem.apple.com（英文）](https://reportaproblem.apple.com) 申请，是否符合条件由 Apple 决定且不保证获批，开发者也无法保证退款获批），请参阅[常见问题解答 (FAQ)](../zh-Hans/faq.md#q16) 或联系[官方支持（英文）](https://contactmerge.app/support)。

## 使用指南

- [快速入门：安全扫描与合并联系人](../zh-Hans/quick-start.md)
- [备份、撤销与恢复记录](../zh-Hans/recovery.md)
- [权限设置与问题排查](../zh-Hans/permissions-troubleshooting.md)
- [常见问题解答 (FAQ)](../zh-Hans/faq.md)

## 官方支持与隐私保护

- **官方支持**：[官方支持（英文）](https://contactmerge.app/support)
- **隐私政策**：[隐私政策（英文）](https://github.com/chenhuaizhe/ContactMergeApp/blob/main/privacy-policy.md)
- **隐私与打码提示**：切勿在公开问题反馈中分享私人联系人列表、`.vcf`（vCard）文件、密码、支付详情或购买收据。在分享任何截图前，请将所有真实姓名、电话号码、电子邮箱、照片、街道地址、备注和账户 ID 打码遮挡——请尽量使用虚构的演示数据。

## 文档状态

核对日期：2026 年 11 月 8 日。实际界面、名称与具体表现可能因您安装的 App 版本和 iOS 版本而异。
