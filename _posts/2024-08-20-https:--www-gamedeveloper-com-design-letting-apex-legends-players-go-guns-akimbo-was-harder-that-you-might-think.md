---
title:  "에이펙스 레전드 플레이어가 아킴보로 총을 쏘게 하는 것은 생각보다 어려웠습니다."

categories:
  - 번역
  
tags:
  - Game Developer
toc: true
toc_sticky: true
 
date: 2024-08-20
last_modified_at: 2024-08-20
---
[![Picture of Bryant Francis](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt862ca995183d2fdf/650efe5138b21120135ae4ac/bryantcropped.jpg?width=100&auto=webp&quality=80&disable=upscale "Picture of Bryant Francis")](https://www.gamedeveloper.com/author/bryant-francis)

[브라이언트 프랜시스](https://www.gamedeveloper.com/author/bryant-francis), 수석 편집자

8월 20, 2024

3 분 읽기

![A player character dual-wields two red pistols against a cyberpunk background in Apex Legends.](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltc41360fabe82757b/66c37671d99834ad659aed21/apexakimbofeatured.jpg?width=1280&auto=webp&quality=95&format=jpg&disable=upscale "A player character dual-wields two red pistols against a cyberpunk background in Apex Legends.")

Respawn Entertainment/Electronic Arts 이미지 제공.

[](https://www.linkedin.com/sharing/share-offsite/?url=https://www.gamedeveloper.com/design/letting-apex-legends-players-go-guns-akimbo-was-harder-that-you-might-think)[](https://www.facebook.com/sharer/sharer.php?u=https://www.gamedeveloper.com/design/letting-apex-legends-players-go-guns-akimbo-was-harder-that-you-might-think)[](https://www.twitter.com/intent/tweet?url=https://www.gamedeveloper.com/design/letting-apex-legends-players-go-guns-akimbo-was-harder-that-you-might-think)[](https://www.gamedeveloper.com/cdn-cgi/l/email-protection#c3fcb0b6a1a9a6a0b7fe8fa6b7b7aaada4e382b3a6bbe38fa6a4a6ada7b0e3b3afa2baa6b1b0e3a4ace3a4b6adb0e3a2a8aaaea1ace3b4a2b0e3aba2b1a7a6b1e3b7aba2ade3baacb6e3aeaaa4abb7e3b7abaaada8e5a2aeb3f8a1aca7bafe8ae6f1f3b7abacb6a4abb7e6f1f3b7aba6e6f1f3a5acafafacb4aaada4e6f1f3a5b1acaee6f1f384a2aea6e6f1f387a6b5a6afacb3a6b1e6f1f3aeaaa4abb7e6f1f3aaadb7a6b1a6b0b7e6f1f3baacb6ede6f387e6f382e6f387e6f382e6f1f38fa6b7b7aaada4e6f1f382b3a6bbe6f1f38fa6a4a6ada7b0e6f1f3b3afa2baa6b1b0e6f1f3a4ace6f1f3a4b6adb0e6f1f3a2a8aaaea1ace6f1f3b4a2b0e6f1f3aba2b1a7a6b1e6f1f3b7aba2ade6f1f3baacb6e6f1f3aeaaa4abb7e6f1f3b7abaaada8e6f387e6f382abb7b7b3b0e6f082e6f185e6f185b4b4b4eda4a2aea6a7a6b5a6afacb3a6b1eda0acaee6f185a7a6b0aaa4ade6f185afa6b7b7aaada4eea2b3a6bbeeafa6a4a6ada7b0eeb3afa2baa6b1b0eea4aceea4b6adb0eea2a8aaaea1aceeb4a2b0eeaba2b1a7a6b1eeb7aba2b7eebaacb6eeaeaaa4abb7eeb7abaaada8)[](https://www.reddit.com/submit?url=https://www.gamedeveloper.com/design/letting-apex-legends-players-go-guns-akimbo-was-harder-that-you-might-think&title=Letting%20Apex%20Legends%20players%20go%20guns%20akimbo%20was%20harder%20than%20you%20might%20think)

## 한눈에 보기

*   에이펙스 레전드 최신 시즌에는 플레이어가 결투를 통해 권총을 휘두를 수 있는 새로운 "아킴보" 시스템이 도입되었습니다.
*   리스폰 엔터테인먼트의 에릭 카나베즈는 5년 된 게임에서 이 시스템을 구현하는 것은 '기념비적인' 도전이었다고 말합니다.

리스폰 엔터테인먼트의 배틀로얄 게임 에이펙스 레전드최신 시즌에는 [1980년대와 90년대에 영화감독 존 우가 상징적으로](https://www.vulture.com/2016/10/john-wick-gun-fu.html) 사용한 슈팅 스타일인 쌍권총을 도입했습니다 . 하드보일드에서 차우윤 팻이 난간을 미끄러져 내려온 이후, 게임 개발자들은 이 스타일과 액션의 조합을 구현하기 위해 끊임없이 노력해왔지만, 모든 종류의 슈팅 장르(탑다운, 1인칭, 3인칭 등)가 존재하는 게임에서 제대로 구현하기란 의외로 까다로운 메커니즘입니다.

왜 그럴까요?에이펙스 레전드의"[아킴보](https://www.ea.com/games/apex-legends/news/shockwave-game-updates)" 시스템을 살펴보면 그 이유를 알 수 있습니다. 리스폰의 몇몇 개발자와의 이메일 채팅에 따르면, 이 시스템을 구현하려면 시즌 22의 신규 맵 "E-District"를 개발하는 "예술" 작업보다 더 힘든 "기념비적인" 기술 작업이 필요했다고 합니다.

수석 레벨 디자이너 스티브 영과 맵 디자이너 가렛 메트칼프 같은 개발자들은 [새로운 캐릭터 레벨링 시스템을](https://www.gamedeveloper.com/business/apex-legends-next-season-brings-mid-match-character-leveling)중심으로 새로운 로케일을 구축하는 실험을 할 수 있었지만 , 수석 시스템 BR 디자이너 에릭 카나베스와 그의 동료들은 P2020과 모잠비크 같은 기본 권총을 쌍권총으로 사용하는 시대를 열기 위해 5년이 넘는 콘텐츠와 코드를 다시 살펴봐야 했습니다.

## 에이펙스 레전드의 아킴보 시스템, 새로운 디자인 가능성을 열다

카나베즈에 따르면 리스폰은 원래 아킴보 무기를 플레이어가 집어들 수 있는 독특한 총기로 생각했습니다. 그렇게 하면 모든 애니메이션, 디자인, 코드 요구 사항을 다른 새로운 무기와 마찬가지로 디자인하는 과정을 거칠 수 있었기 때문입니다.

관련 내용:[에이펙스 레전드에서 멋진 1인칭 애니메이션을 구현한 비결은 무엇일까요? 마우스 카메라](https://www.gamedeveloper.com/art/the-secret-to-apex-legends-gorgeous-first-person-animation-mouth-cameras)

카나베즈는 이 아이디어를 "평가"하는 동안 팀에서 전체 듀얼 휘두르기 시스템을 구축할 수 있는 기회, 즉 하위 단계 무기에 생명력을 불어넣고 게임 전체에서 매력적인 옵션이 될 수 있는 기회를 발견했다고 말했습니다.

하지만 존 우 액션 판타지를 구현하기 위해 보다 개방적인 시스템을 만들었음에도 불구하고 리스폰의 솔루션은 1인칭 개발자가 직면한 제약을 강조했습니다. 다른 총을 잡으면 해당 무기의 발사 속도가 빨라지고, 자동 사격이 가능해지며, 사격 범위가 더 좁아집니다.

플레이어의 무기가 한 방향으로 고정되어 있어 다른 목표물을 조준할 수 있는 가능성이 제한된다는 점은 이미 판타지에서 빠진 한 조각을 볼 수 있습니다. 이 제한된 시스템으로 인해 헤일로와 울펜슈타인 시리즈에서처럼 서로 다른 무기를 이중으로 사용할 수 없습니다. 하지만 개발팀이 직면한 하드코어한 개발 과제에 직면하게 됩니다.

에이펙스 레전드는 출시된 지 5년이 지난 게임으로, 보급품 보관함과 같은 일부 핵심 기능은 시간이 지나면서 업데이트되었지만 5년 전의 레거시 코드와 디자인 방향은 여전히 고려해야 할 사항입니다. 리스폰의 고품질 1인칭 애니메이션은 무기와 캐릭터 디자인에 깊숙이 내장되어 있으며, 양손에 총을 들고 있으면 애니메이션에 골머리를 앓기 시작합니다.

예를 들어, 아드레날린이 솟구치는 스피드스터 옥테인(Octane)은 플레이어가 다양한 동작 상태에서 '찌르기'를 사용하는 모습을 볼 수 있는 커스텀 애니메이션이 있습니다. 플레이어는 무기를 재장전하는 동안 속도 부스트를 활성화하여 이론적으로는 세 번째 손을 사용해야 하는 동작을 수행할 때 이미 애니메이션을 극한까지 끌어올립니다. 옥탄이 쌍검을 사용하는 파티에 합류하려면 스팀과 총을 저글링하는 특별한 애니메이션이 필요했습니다.

플레이어가 표면적으로는 한 손으로 줄을 타지만 총을 발사하려면 양손이 모두 필요한 짚라인에서는 이 모든 애니메이션이 더욱 복잡해집니다.

그다음 밸런싱이 필요했습니다. 플레이어에게 동일한 능력치를 가진 두 개의 권총을 제공하는 것만으로는 충분하지 않았습니다. 카나베즈는 두 개를 사용하면 파워가 급상승하는 것처럼 느껴지지만 너무 크지는않도록 기본 형태를 "완전히 재평가"해야 한다고 말했습니다 .

시즌 22 이전에는 "거의 쓸모가 없던" 두 가지 무기를 강력한 옵션으로 만들었기 때문에 이 개편에 올인한 결과 큰 성과를 거둘 수 있었습니다.

멀티플레이어 게임에서 틈새 시장을 찾지 못한 무기는 팀이 해당 무기를 위한 새로운 시스템을 구축할 수 있는 리소스가 있을 때 빛을 발할 수 있습니다. 이는 해당 무기를 지금 더 재미있게 만들 뿐만 아니라 애초에 무기를 만들기로 한 결정에 대한 확신을 심어줍니다. 라이브 서비스 게임에서 좋은 아이디어를 실현하려면 5년 정도의 시간이 필요한 경우도 있습니다.

자세히 읽어보세요:

[인터뷰기능톱](https://www.gamedeveloper.com/keyword/features)[스토리](https://www.gamedeveloper.com/keyword/top-stories)

[](https://www.linkedin.com/sharing/share-offsite/?url=https://www.gamedeveloper.com/design/letting-apex-legends-players-go-guns-akimbo-was-harder-that-you-might-think)[](https://www.facebook.com/sharer/sharer.php?u=https://www.gamedeveloper.com/design/letting-apex-legends-players-go-guns-akimbo-was-harder-that-you-might-think)[](https://www.twitter.com/intent/tweet?url=https://www.gamedeveloper.com/design/letting-apex-legends-players-go-guns-akimbo-was-harder-that-you-might-think)[](https://www.gamedeveloper.com/cdn-cgi/l/email-protection#7f400c0a1d151a1c0b42331a0b0b1611185f3e0f1a075f331a181a111b0c5f0f131e061a0d0c5f18105f180a110c5f1e1416121d105f081e0c5f171e0d1b1a0d5f0b171e115f06100a5f121618170b5f0b17161114591e120f441d101b0642365a4d4f0b17100a18170b5a4d4f0b171a5a4d4f1910131310081611185a4d4f190d10125a4d4f381e121a5a4d4f3b1a091a13100f1a0d5a4d4f121618170b5a4d4f16110b1a0d1a0c0b5a4d4f06100a515a4f3b5a4f3e5a4f3b5a4f3e5a4d4f331a0b0b1611185a4d4f3e0f1a075a4d4f331a181a111b0c5a4d4f0f131e061a0d0c5a4d4f18105a4d4f180a110c5a4d4f1e1416121d105a4d4f081e0c5a4d4f171e0d1b1a0d5a4d4f0b171e115a4d4f06100a5a4d4f121618170b5a4d4f0b171611145a4f3b5a4f3e170b0b0f0c5a4c3e5a4d395a4d3908080851181e121a1b1a091a13100f1a0d511c10125a4d391b1a0c1618115a4d39131a0b0b161118521e0f1a0752131a181a111b0c520f131e061a0d0c52181052180a110c521e1416121d1052081e0c52171e0d1b1a0d520b171e0b5206100a52121618170b520b17161114)[](https://www.reddit.com/submit?url=https://www.gamedeveloper.com/design/letting-apex-legends-players-go-guns-akimbo-was-harder-that-you-might-think&title=Letting%20Apex%20Legends%20players%20go%20guns%20akimbo%20was%20harder%20than%20you%20might%20think)

## 저자 소개

[![Bryant Francis](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt862ca995183d2fdf/650efe5138b21120135ae4ac/bryantcropped.jpg?width=400&auto=webp&quality=80&disable=upscale "Bryant Francis")](https://www.gamedeveloper.com/author/bryant-francis)

[

브라이언트 프랜시스

](https://www.gamedeveloper.com/author/bryant-francis)

선임 편집자, GameDeveloper.com

브라이언트 프랜시스는 매사추세츠주 보스턴에 거주하는 작가, 저널리스트, 내러티브 디자이너입니다. 현재 비디오 게임 업계를 위한 B2B 간행물인 Game Developer에 글을 기고하고 있습니다. 그의 대표작으로는 프록시 스튜디오의 출시 예정인 4X 전략 게임 제폰과 앰플리튜드 스튜디오의 2017년 게임 엔들리스 스페이스 2가 있습니다.

[더보기 브라이언트 프랜시스](https://www.gamedeveloper.com/author/bryant-francis)

게임 개발자의 일일 뉴스, 개발자 블로그, 스토리를 받은 편지함으로 바로 받아보세요.

[최신 소식 받기](https://gd-resources.gamedeveloper.com/free/w_gamf01/prgm.cgi)

추천 콘텐츠

* * *

원문: [https://www.gamedeveloper.com/design/letting-apex-legends-players-go-guns-akimbo-was-harder-that-you-might-think](https://www.gamedeveloper.com/design/letting-apex-legends-players-go-guns-akimbo-was-harder-that-you-might-think)