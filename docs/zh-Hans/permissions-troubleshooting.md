# 权限设置与问题排查

- **概览与语言**：[简体中文概览](../readme/README.zh-Hans.md) | [English Overview](../../README.md)
- **使用指南**：[快速入门](quick-start.md) | [备份与恢复记录](recovery.md) | **权限与问题排查** | [常见问题 (FAQ)](faq.md)
- **语言 / Language**：**简体中文** | [English](../en/permissions-troubleshooting.md)

本指南涵盖 iPhone 上的通讯录访问权限管理、**ContactMerge+ Cleaner** 与 Apple 系统自带重复项处理工具的区别、同步账户与手机迁移时的安全操作原则、购买恢复与退款常见问题，以及如何安全地联系官方支持。

## iPhone 上的通讯录访问权限

- **扫描与合并所必需的权限**：ContactMerge+ Cleaner 需要获得通讯录访问权限，才能在您的 iPhone 上查找并合并重复联系人。联系人处理完全在您的设备本地进行——您的联系人列表不会上传至开发者服务器，开发者也不提供云备份服务（这与由您自身设置控制的 iCloud/Google 联系人同步或 iOS 系统备份相互独立）。
- **iOS 中的完全访问与受限访问**：视您的 iOS 版本而定，Apple 允许您在 iOS 系统“设置”的隐私与通讯录权限设置中（英文界面参考 `Settings > Privacy & Security > Contacts`，具体菜单名称可能因 iOS 版本或语言设置略有差异），控制应用可访问哪些联系人——包括完全访问权限或仅访问所选联系人的受限权限（请参阅 Apple 官方指南：[控制对 iPhone 上“通讯录”的访问权限（英文）](https://support.apple.com/guide/iphone/control-access-to-contacts-iph9536aa9a5/ios)）。
- **如果无法扫描或显示的联系人似乎不完整**：
  - 请前往 iOS 系统设置检查授予 ContactMerge+ Cleaner 的通讯录权限级别。未完整授权或受限访问会限制本应用能够看到的联系人范围——这**不会**删除您的联系人，但本应用并不保证支持所有受限访问操作流程。
  - 如果检查 iOS 系统设置后发现相关选项不可用，或表现依然异常，请联系[官方支持（英文）](https://contactmerge.app/support)。
- **切勿采取的错误操作**：排查权限问题时，切勿反复开关账户同步、移除账户、删除联系人或重复导入 `.vcf` 文件。

## ContactMerge+ Cleaner 与 Apple 系统自带重复项工具的区别

Apple 系统**“通讯录”**应用内置了重复项提示与名片关联功能，其运作机制与 ContactMerge+ Cleaner 不同（请参阅 Apple 官方指南：[在 iPhone 上合并或隐藏重复联系人（英文）](https://support.apple.com/guide/iphone/merge-or-hide-duplicate-contacts-iph2ab28320d/ios)）：

- **Apple 系统“通讯录”中的重复项提示（`View Duplicates`）**：当系统检测到可用提示时，Apple 会在个人名片（`My Card`）下方显示 `View Duplicates` 入口，供您查看并合并系统识别出的重复项。如果 Apple 系统“通讯录”未显示 `View Duplicates` 横幅——例如电话号码使用了不同的国家/地区代码格式，或在某些联系人数量较多的通讯录中——请将该系统自带机制的表现与本应用的权限问题区分开来。本文档不对 Apple 内部的检测规则、特定的联系人数量阈值（如 1,000 个联系人）、固定等待时间或“一键全部合并”的通用修复方案做任何承诺。
- **关联/统一名片与真正合并名片的区别**：在 Apple 系统“通讯录”应用中手动关联联系人（`Link Contacts`），只是将多张名片统一在同一个界面视图中展示，并不会合并底层的源联系人名片；同时，在统一名片上所做的编辑可能会传播同步到所连接的各个源账户。
- **ContactMerge+ Cleaner 的不同之处**：ContactMerge+ Cleaner 在您的设备本地进行扫描，并将候选分组划分为 `Ready to merge`（合并就绪）与 `Needs review`（需人工核对），方便您先查看合并预览（同时配合在 Apple 系统**“通讯录”**应用中检查备注）。本应用不承诺特定的扫描速度、联系人列表容量上限，也不承诺自动修复此前的联系人数据历史损坏。
- 相关官方网页指南：
  - [iOS 重复项提示与国家/地区代码格式说明（英文）](https://contactmerge.app/guides/ios-view-duplicates-country-code)
  - [联系人数量较多时未显示重复项提示（英文）](https://contactmerge.app/guides/view-duplicates-missing-large-contact-list)

## 换机迁移、账户同步与防止误删联系人

设置新 iPhone、使用“转移到 iOS”（Move to iOS）、导入备份文件，或同时关联多个账户（例如 iCloud 与 Google），往往会将散落在不同来源中的旧有重复联系人显现出来，这并不意味着您的设备出现了故障：

- **先等待初始同步结束并做好独立备份**：在判断重复情况前，请先等待设备迁移或账户初始同步全部完成（等待同步本身不保证会自动消除重复项，但能避免同步未完成时的混乱）。在做任何更改前，请先确认联系人实际存放在哪个账户中，并保留一份带日期的独立备份。
- **谨慎核对后再确认**：请仔细检查合并预览（尤其是 `Needs review` 分组），并先在 Apple 系统**“通讯录”**应用中保存非主联系人名片上的重要备注（Notes）；如果您切出本应用去查看或编辑过联系人，返回后请重新核对当前的候选列表与合并预览再确认。
- **严禁采取破坏性删除操作**：在系统“通讯录”中移除账户与逐条删除联系人的行为完全不同；而删除存储在同步电子邮箱或云账户中的联系人，可能会在所有同步设备上将其永久删除（如需了解背景说明，可参阅 Apple 官方指南[在 iPhone“通讯录”中添加或移除账户（英文）](https://support.apple.com/guide/iphone/add-or-remove-accounts-iph7edacccf9/ios)及[删除同步联系人风险提示（英文）](https://support.apple.com/en-us/111793)）。清理过程中，**切勿**将删除源联系人、轻点 `"Delete from My iPhone"`（从我的 iPhone 删除）、开关账户同步或反复重新导入 `.vcf` 文件当作捷径——如果不确定如何处理，请先暂停并咨询[官方支持（英文）](https://contactmerge.app/support)。
- 官方场景说明指南：
  - [设置新 iPhone 后出现重复联系人（英文）](https://contactmerge.app/guides/duplicate-contacts-after-new-iphone)
  - [使用“转移到 iOS”后出现重复联系人（英文）](https://contactmerge.app/guides/move-to-ios-duplicate-contacts)
  - [iCloud 同步后出现重复联系人（英文）](https://contactmerge.app/guides/icloud-duplicate-contacts-after-sync)
  - [在 iPhone 上合并联系人前如何备份（英文）](https://contactmerge.app/guides/backup-contacts-before-merge-iphone)
  - [如何安全地合并联系人（英文）](https://contactmerge.app/guides/merge-contacts-safely)

## Pro 专业版解锁、恢复购买与退款说明

- **一次性解锁（非订阅制）**：Pro 是 App Store 的一次性非消耗型内购项目，地区价格由 Apple 直接显示——请**不要**按照取消订阅的流程处理本应用。Pro 解锁包含超过 3 个联系人的分组合并，以及在确认后对 `Ready to merge` 分组进行批量合并（`Needs review` 分组仍保持逐组人工核对）。
- **恢复已购买的 Pro 权益**：请确保您的 iPhone 登录了当初购买时使用的**同一 Apple 账户（Apple Account）**，并参考 Apple 官方支持指南：[如果找不到或无法使用 App 内购买项目（英文）](https://support.apple.com/en-us/108096)。由于应用内恢复购买按钮的具体界面路径在本文档中未经核实，我们不会猜测菜单名称、不建议重复付费购买，也不承诺一定能自动完成恢复——如果恢复失败，请联系[官方支持（英文）](https://contactmerge.app/support)或 Apple 官方支持。
- **退款申请**：App Store 的账单与退款流程由 Apple 管理并决定。部分购买项目可能符合退款条件，具体资格由 Apple 根据所在国家或地区规则判定，**退款并非保证获批**。如需申请退款，请通过 Apple 官方流程在 [reportaproblem.apple.com（英文）](https://reportaproblem.apple.com) 提交（参阅 Apple 官方说明：[为从 Apple 购买的 App 或内容申请退款（英文）](https://support.apple.com/en-us/118223)）；开发者无法保证退款申请获得批准。

## 联系官方支持与保护个人隐私

- **支持入口**：[官方支持（英文）](https://contactmerge.app/support)
- **建议提供的安全排查信息**：您的 ContactMerge+ Cleaner 应用版本号、iOS 版本号、您的预期表现与实际观察到的现象、问题出现在 Apple 系统界面还是 ContactMerge+ Cleaner 应用内界面、涉及的账户类型（例如 iCloud 或 Google，但**请勿**附带您的邮箱地址或账户 ID），以及在相关情况下的大致联系人数量。
- **严格的隐私与打码规范**：
  - 切勿在公开问题反馈中上传私人联系人列表、`.vcf`（vCard）文件、密码、支付详情或购买收据（任何涉及账单的具体信息，仅应在确有必要时通过 Apple 官方安全渠道或适当的官方私密支持渠道处理）。
  - 在分享任何截图前，请务必将所有真实姓名、电话号码、电子邮箱、照片、街道地址、备注和各类 ID 彻底打码遮挡——请尽量使用虚构的演示数据。

## 相关链接

- [快速入门：安全扫描与合并联系人](quick-start.md)
- [备份、撤销与恢复记录](recovery.md)
- [常见问题解答 (FAQ)](faq.md)
- [官方网站（英文）](https://contactmerge.app)
- [隐私政策（英文）](https://github.com/chenhuaizhe/ContactMergeApp/blob/main/privacy-policy.md)

## 文档状态

核对日期：2026 年 11 月 8 日。实际界面、名称与具体表现可能因您安装的 App 版本和 iOS 版本而异。
