# 권한 설정 및 문제 해결

- **개요 및 언어**: [한국어 개요](../readme/README.ko.md) | [영문 개요 (English)](../../README.md) | [영문 원본 가이드 (English)](../en/permissions-troubleshooting.md)
- **가이드**: [빠른 시작](quick-start.md) | [백업 및 복구](recovery.md) | **권한 및 문제 해결** | [FAQ](faq.md)

이 가이드는 iPhone 연락처 접근 권한 설정, Apple 기본 중복 기능과 **ContactMerge+ Cleaner**의 차이점, 동기화 계정 및 기기 이전 시 안전한 대처 방법, Pro 구매 복원·환불 관련 안내, 그리고 안전하게 고객지원에 문의하는 방법을 다룹니다.

## iPhone 연락처 접근 권한

- **스캔 및 병합에 필요한 권한**: ContactMerge+ Cleaner가 iPhone에서 중복 연락처를 찾고 병합하려면 연락처 접근 권한이 필요합니다. 연락처 처리는 기기 내부에서 이루어지며 주소록이 개발자 서버로 업로드되지 않고, 개발자는 클라우드 백업 서비스를 제공하지 않습니다(사용자 본인의 설정으로 관리되는 iCloud·Google 연락처 동기화 및 iOS 시스템 백업과는 별개입니다).
- **iOS의 전체 접근과 제한된 접근**: 사용 중인 iOS 버전에 따라 iPhone 설정의 개인정보 보호 및 연락처 권한 항목(영문 iOS 기준 `Settings > Privacy & Security > Contacts`, 기기 언어 및 iOS 버전에 따라 표시명은 다를 수 있음)에서 앱이 접근할 수 있는 연락처 범위(전체 접근 또는 선택한 일부 연락처만 제한 접근)를 직접 관리할 수 있습니다(Apple 공식 가이드: [iPhone의 연락처에 대한 접근 제어하기 (영문)](https://support.apple.com/guide/iphone/control-access-to-contacts-iph9536aa9a5/ios) 참고).
- **스캔이 차단되거나 일부 연락처가 보이지 않는 경우**:
  - iOS 설정에서 ContactMerge+ Cleaner에 부여된 연락처 접근 권한 수준을 확인하세요. 권한이 불완전하거나 제한된 접근으로 설정되어 있으면 앱에서 볼 수 있는 연락처 범위가 제한될 수 있습니다. 이는 연락처가 삭제된 것이 아니지만, 앱이 모든 제한된 접근(limited-access) 방식을 완벽히 지원한다고 보장되지는 않습니다.
  - iOS 설정을 확인한 뒤에도 설정 항목이 비활성화되어 있거나 예상과 다르게 동작한다면 [공식 고객지원 (영문)](https://contactmerge.app/support)에 문의하세요.
- **절대 하지 말아야 할 행동**: 권한 문제를 해결하려고 계정 동기화를 껐다 켜거나, 계정을 제거하거나, 연락처를 삭제하거나, `.vcf` 파일을 다시 가져오지 마세요.

## ContactMerge+ Cleaner와 Apple 기본 중복 정리 도구의 차이점

Apple 기본 **연락처**(Contacts) 앱에 내장된 중복 정리 및 연결 기능은 ContactMerge+ Cleaner와 다르게 작동합니다(Apple 공식 가이드: [iPhone에서 중복 연락처 병합 또는 가리기 (영문)](https://support.apple.com/guide/iphone/merge-or-hide-duplicate-contacts-iph2ab28320d/ios) 참고):

- **Apple 연락처 앱의 `View Duplicates` (중복 항목 보기)**: 사용 가능한 경우 Apple은 `My Card`(내 카드) 아래에 감지된 중복 연락처를 검토하고 병합할 수 있는 `View Duplicates` 알림을 표시합니다. 전화번호의 국가 코드 형식이 서로 다르거나 주소록 규모가 큰 경우처럼 Apple의 `View Duplicates` 배너가 나타나지 않을 때는, 이러한 시스템 동작을 앱 권한 문제와 구분해야 합니다. 본 문서는 Apple의 내부 감지 규칙, 보장된 연락처 수 기준(예: 1,000개 기준 등), 일정 대기 시간 또는 일괄 "모두 병합(Merge All)" 해결책을 단정하거나 보장하지 않습니다.
- **연결된(통합) 연락처와 실제 병합된 카드의 차이**: Apple 연락처 앱에서 수동으로 연락처를 연결(`Link Contacts`)하면 원본 카드를 실제로 합치지 않고 화면에만 하나의 통합 카드로 묶어 보여주며, 통합 카드에서 수정한 내용은 연결된 계정에 반영될 수 있습니다.
- **ContactMerge+ Cleaner의 차별점**: ContactMerge+ Cleaner는 기기 내에서 직접 스캔하여 후보를 `Ready to merge`와 `Needs review`로 구분해 주므로, 병합 전에 미리보기를 꼼꼼히 확인하고 Apple 기본 **연락처** 앱에서 메모(Notes)를 먼저 챙길 수 있습니다. 단, 특정 스캔 속도나 주소록 최대 크기 한도, 또는 이전 주소록 손상의 자동 복구를 보장하지는 않습니다.
- 관련 공식 웹 가이드:
  - [iOS 중복 항목 보기와 국가 코드 형식 차이 (영문)](https://contactmerge.app/guides/ios-view-duplicates-country-code)
  - [대규모 연락처 목록에서 중복 항목 보기가 나타나지 않을 때 (영문)](https://contactmerge.app/guides/view-duplicates-missing-large-contact-list)

## 기기 이전, 계정 동기화 및 실수로 인한 삭제 방지

새 iPhone 설정, Move to iOS(iOS로 이동) 사용, 파일 가져오기, 또는 여러 계정(iCloud와 Google 등) 연결 후에는 여러 출처에 흩어져 있던 오래된 중복 연락처가 드러나는 경우가 흔하며, 이는 기기 불량을 의미하지 않습니다:

- **초기 동기화 완료 대기 후 백업 먼저 하기**: 중복 여부를 판단하기 전에 기기 이전이나 초기 계정 동기화가 끝날 때까지 기다리세요(기다리는 것만으로 중복이 자동 제거된다고 보장하지는 않지만 동기화 도중의 혼선을 막아줍니다). 연락처가 어느 계정에 저장되어 있는지 파악하고, 무언가를 변경하기 전에 날짜가 표시된 독립 백업을 먼저 만드세요.
- **신중하게 검토하기**: 병합 미리보기(특히 `Needs review` 그룹)를 확인하고 보조 연락처의 메모(Notes)는 Apple 기본 **연락처** 앱에서 먼저 따로 보관하세요. 연락처를 확인하거나 수정하려고 앱 밖으로 나갔다면 돌아온 뒤 현재 중복 후보와 미리보기를 다시 확인한 후 확정하세요.
- **필수 삭제 방지 수칙**: 연락처 설정에서 계정을 제거하는 것은 개별 연락처를 삭제하는 것과 다르게 작동하며, 동기화된 이메일이나 클라우드 계정에서 연락처를 삭제하면 동기화된 모든 기기에서 영구적으로 삭제될 수 있습니다(배경 설명은 Apple의 [iPhone의 연락처에서 계정 추가 또는 제거하기 (영문)](https://support.apple.com/guide/iphone/add-or-remove-accounts-iph7edacccf9/ios) 및 [연락처 삭제 관련 안내 (영문)](https://support.apple.com/en-us/111793) 참고). 빠른 정리를 위해 원본 연락처를 삭제하거나, `"Delete from My iPhone"`을 탭하거나, 동기화를 껐다 켜거나, `.vcf` 파일을 반복해서 다시 가져오지 **마세요**. 확신이 없다면 즉시 중단하고 [공식 고객지원 (영문)](https://contactmerge.app/support)에 문의하세요.
- 공식 상황별 웹 가이드:
  - [새 iPhone 설정 후 중복 연락처 정리 (영문)](https://contactmerge.app/guides/duplicate-contacts-after-new-iphone)
  - [Move to iOS 사용 후 중복 연락처 정리 (영문)](https://contactmerge.app/guides/move-to-ios-duplicate-contacts)
  - [동기화 후 iCloud 중복 연락처 정리 (영문)](https://contactmerge.app/guides/icloud-duplicate-contacts-after-sync)
  - [iPhone에서 병합 전 연락처 백업하기 (영문)](https://contactmerge.app/guides/backup-contacts-before-merge-iphone)
  - [연락처를 안전하게 병합하는 방법 (영문)](https://contactmerge.app/guides/merge-contacts-safely)

## Pro 잠금 해제, 구매 복원 및 환불 안내

- **일회성 잠금 해제(구독 아님)**: Pro는 Apple이 지역별 가격을 표시하는 App Store 일회성 비소모성 구매 상품이므로, 이 앱에 대해 구독 해지 절차를 따르지 **마세요**. Pro를 잠금 해제하면 3개를 초과하는 연락처가 포함된 그룹(한 그룹 내 연락처 카드 3개 초과)의 병합, 그리고 확인을 거친 여러 `Ready to merge` 그룹의 일괄 병합을 사용할 수 있습니다(`Needs review` 그룹은 계속 한 번에 하나씩 검토합니다).
- **Pro 구매 복원**: iPhone이 원래 구매할 때 사용했던 **동일한 Apple 계정(Apple Account)**으로 로그인되어 있는지 확인하고 Apple 공식 가이드([앱 내 구입 항목을 찾을 수 없거나 사용할 수 없는 경우 (영문)](https://support.apple.com/en-us/108096))를 살펴보세요. 본 문서에서는 앱 내 정확한 복원 버튼 경로가 검증되지 않았으므로 임의로 메뉴 이름을 추측하거나 재구매를 권장하거나 자동 복원을 보장하지 않습니다. 복원이 되지 않으면 [공식 고객지원 (영문)](https://contactmerge.app/support) 또는 Apple 지원에 문의하세요.
- **환불 요청**: App Store 결제 및 환불 대상 여부는 국가 또는 지역 기준에 따라 Apple이 결정하며, **환불이 보장되지는 않습니다**. 환불 요청은 Apple의 공식 절차인 [reportaproblem.apple.com (영문)](https://reportaproblem.apple.com)을 통해 진행하며(Apple의 [Apple에서 구입한 앱 또는 콘텐츠의 환불 요청하기 (영문)](https://support.apple.com/en-us/118223) 참고), 개발자가 환불 승인을 보장할 수는 없습니다.

## 고객지원 문의 및 개인정보 보호

- **고객지원**: [공식 고객지원 (영문)](https://contactmerge.app/support)
- **문의 시 함께 알려주면 좋은 안전한 정보**: ContactMerge+ Cleaner 앱 버전, iOS 버전, 기대했던 동작과 실제로 관찰된 현상, 해당 화면이 Apple 시스템 제어 화면인지 ContactMerge+ Cleaner 앱 내부 화면인지 여부, 관련 계정 유형(예: iCloud, Google — 이메일이나 계정 ID는 **제외**), 필요한 경우 대략적인 연락처 수.
- **엄격한 개인정보 및 가림 처리 원칙**:
  - 공개 이슈에 개인 연락처 목록, `.vcf`(vCard) 파일, 비밀번호, 결제 정보 또는 구매 영수증을 절대 업로드하지 마세요(결제 관련 구체적 사항은 필요한 경우 Apple 공식 보안 채널이나 적절한 비공개 공식 지원 채널을 통해서만 처리하세요).
  - 스크린샷을 공유하기 전에 실제 이름, 전화번호, 이메일 주소, 사진, 도로명·상세 주소, 메모 및 각종 ID를 모두 가리고, 가능하면 항상 가상의 데모 데이터를 사용하세요.

## 관련 링크

- [빠른 시작: 안전하게 스캔하고 병합하기](quick-start.md)
- [백업, 실행 취소 및 복구 기록](recovery.md)
- [자주 묻는 질문 (FAQ)](faq.md)
- [공식 웹사이트 (영문)](https://contactmerge.app)
- [개인정보 처리방침 (영문)](https://github.com/chenhuaizhe/ContactMergeApp/blob/main/privacy-policy.md)

## 문서 상태

2026년 11월 8일 확인 기준. 설치된 앱 버전과 iOS 버전에 따라 화면, 레이아웃, 문구 및 동작이 다를 수 있습니다.
