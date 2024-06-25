---
title:  "HUD를 버려야 할까요? 플레이어 흐름에 미치는 영향 살펴보기"

categories:
  - 번역
  
tags:
  - Game Developer
toc: true
toc_sticky: true
 
date: 2024-06-25
last_modified_at: 2024-06-25
---
[![Picture of Reinard Baertsoen](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltd709c2f6ad0896cd/657b3aae1fb1b4040a0e1821/Game_Developer_G_Logo_RGB.png?width=100&auto=webp&quality=80&disable=upscale "Picture of Reinard Baertsoen")](https://www.gamedeveloper.com/author/reinard-baertsoen)

[레이나르 바에르소엔](https://www.gamedeveloper.com/author/reinard-baertsoen)

6월 25일, 2024

3분 읽기

![](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt48e6513c62cfa302/65cfc3fc4950cc040a3bbaac/GDBlogs_Header_Center_FINAL.png?width=850&auto=webp&quality=95&format=jpg&disable=upscale)

[](https://www.linkedin.com/sharing/share-offsite/?url=https://www.gamedeveloper.com/design/should-we-abandon-the-hud-examining-its-impact-on-player-flow)[](https://www.facebook.com/sharer/sharer.php?u=https://www.gamedeveloper.com/design/should-we-abandon-the-hud-examining-its-impact-on-player-flow)[](https://www.twitter.com/intent/tweet?url=https://www.gamedeveloper.com/design/should-we-abandon-the-hud-examining-its-impact-on-player-flow)[](https://www.gamedeveloper.com/cdn-cgi/l/email-protection#ac93dfd9cec6c9cfd891ffc4c3d9c0c88cdbc98ccdcecdc2c8c3c28cd8c4c98ce4f9e8938ce9d4cdc1c5c2c5c2cb8ce5d8df8ce5c1dccdcfd88cc3c28cfcc0cdd5c9de8ceac0c3db8acdc1dc97cec3c8d591e5899e9cd8c4c3d9cbc4d8899e9cd8c4c9899e9ccac3c0c0c3dbc5c2cb899e9ccadec3c1899e9cebcdc1c9899e9ce8c9dac9c0c3dcc9de899e9cc1c5cbc4d8899e9cc5c2d8c9dec9dfd8899e9cd5c3d982899ce8899ced899ce8899ced899e9cffc4c3d9c0c8899e9cdbc9899e9ccdcecdc2c8c3c2899e9cd8c4c9899e9ce4f9e8899fea899e9ce9d4cdc1c5c2c5c2cb899e9ce5d8df899e9ce5c1dccdcfd8899e9cc3c2899e9cfcc0cdd5c9de899e9ceac0c3db899ce8899cedc4d8d8dcdf899fed899eea899eeadbdbdb82cbcdc1c9c8c9dac9c0c3dcc9de82cfc3c1899eeac8c9dfc5cbc2899eeadfc4c3d9c0c881dbc981cdcecdc2c8c3c281d8c4c981c4d9c881c9d4cdc1c5c2c5c2cb81c5d8df81c5c1dccdcfd881c3c281dcc0cdd5c9de81cac0c3db)[](https://www.reddit.com/submit?url=https://www.gamedeveloper.com/design/should-we-abandon-the-hud-examining-its-impact-on-player-flow&title=Should%20we%20abandon%20the%20HUD%3F%20Examining%20Its%20Impact%20on%20Player%20Flow)

게임 디자이너는 스스로에게 계속 질문해야 합니다: 내 디자인의 목표는 무엇인가? 많은 경우 몰입감 있는 경험을 만드는 것이 목표이며, 이는 플레이어를 플로우 상태로 유도함으로써 달성할 수 있습니다. 플레이어를 몰입 상태로 만들려면 무엇이 방해가 될 수 있는지 파악해야 합니다. 한동안 논란이 되어온 게임플레이 요소 중 하나가 바로 헤드업 디스플레이(HUD)입니다.

## 게임에서의 흐름

플로우가 실제로 무엇인지 명확히 해보겠습니다. 도전과 기술의 균형을 맞추는 것이라고 들어보셨을 텐데요, 이는 사실이지만 그 이상의 의미가 있습니다.

![Diagram-of-flow-theory-by-Csikszentmihalyi.jpg](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt069557dc730e7427/667470e3db6edf48daee1805/Diagram-of-flow-theory-by-Csikszentmihalyi.jpg?width=700&auto=webp&quality=80&disable=upscale "Diagram-of-flow-theory-by-Csikszentmihalyi.jpg")

기술/도전 곡선(식센트미할리, 1990)

플로우란 플레이어가 게임에 너무 몰입한 나머지 시간, 공간 등 다른 모든 것을 잊어버리는 특별한 상태를 말합니다. 플레이어는 너무 집중해서 다른 것은 중요하지 않습니다. 플레이어에게 통제감을 부여하고 게임플레이 경험을 놀랍도록 몰입감 있게 만들어 줍니다.

하지만 문제가 있습니다. 플로우 상태에서는 플레이어가 자기 성찰을 잃고 무슨 일이 일어났는지 기억하기 어려워질 수 있습니다. 따라서 게임 디자이너는 항상 디자인 목표를 고려해야 합니다. 잊을 수 없는 경험을 만들고 싶다면 플로우는 적합하지 않을 수 있습니다.

## 게임에서 HUD의 역할

HUD는 게임플레이를 오버레이하는 사용자 인터페이스(UI)로서 중요한 역할을 합니다. 플레이어에게 정보와 피드백을 전달하지만 보조적인 역할도 합니다. HUD에 표시되는 정보와 피드백은 다른 수단을 통해 수집할 수 있는 경우가 많습니다. 예를 들어 치유 효과를 생각해 보겠습니다. 이를 표시하는 주요 방법은 일부 VFX와 애니메이션이지만, 플레이어에게 이 중요한 정보를 전달하는 데 도움이 되는 사운드와 HUD 애니메이션으로도 표시됩니다.

![OverwatchHealEffect Screenshot](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blte0f0231895f5074e/6674718c61e23ca7489739b5/OverwatchHealEffect-NoName.png?width=700&auto=webp&quality=80&disable=upscale "OverwatchHealEffect Screenshot")

오버워치 2(블리자드, 2022년) 스크린샷

요컨대, 정보와 플레이어 피드백은 여러 가지 방식으로 표현되는 경우가 많으며, HUD는 그 중 하나입니다.

## 흐름에 대한 HUD의 영향

그렇다면 HUD는 흐름에 어떤 영향을 미칠까요? 몇 가지 방법이 있습니다. 첫째, HUD를 제거하면 플레이어가 약간 통제 불능 상태가 될 수 있습니다. 이는 플레이어가 정보에 쉽게 접근하지 못하면 길을 잃었다고 느낄 수 있기 때문에 흐름이 약해질 수 있습니다. 하지만 이러한 편의성 부족은 장점도 있습니다. 플레이어는 자신이 하는 일에 더 집중하게 되고, 이는 더 강력한 흐름 상태로 이어질 수 있습니다. HUD를 없애면 흐름 상태가 강화되기도 하고 약화되기도 하는 혼란스러운 상황이 발생할 수 있습니다.

## 그렇다면 이 기능을 포기해야 할까요?

이 질문에 대한 명확한 답은 아직 없습니다. HUD 사용에는 장단점이 있으며, 게임 디자이너가 게임에서 이점이 단점보다 더 큰지 파악하는 것은 게임 디자이너의 몫입니다. 게임 디자인에는 정해진 규칙이 없다는 한 가지 큰 규칙이 있습니다. 게임의 핵심을 염두에 두고 실험하는 것이 중요합니다. 따라서 HUD를 버려야 할지 고민 중이라면 일단 시도해 보세요. 누가 알겠습니까? 게임이 더 좋아질지도 모르죠. 아니면 아닐 수도 있으니 실험해 보는 겁니다.

자세히 읽어보세요:

[블로그추천](https://www.gamedeveloper.com/keyword/blogs)[블로그톱](https://www.gamedeveloper.com/keyword/featured-blogs)[스토리](https://www.gamedeveloper.com/keyword/top-stories)

[](https://www.linkedin.com/sharing/share-offsite/?url=https://www.gamedeveloper.com/design/should-we-abandon-the-hud-examining-its-impact-on-player-flow)[](https://www.facebook.com/sharer/sharer.php?u=https://www.gamedeveloper.com/design/should-we-abandon-the-hud-examining-its-impact-on-player-flow)[](https://www.twitter.com/intent/tweet?url=https://www.gamedeveloper.com/design/should-we-abandon-the-hud-examining-its-impact-on-player-flow)[](https://www.gamedeveloper.com/cdn-cgi/l/email-protection#5c632f293e36393f28610f34332930387c2b397c3d3e3d323833327c2834397c140918637c19243d31353235323b7c15282f7c15312c3d3f287c33327c0c303d25392e7c1a30332b7a3d312c673e3338256115796e6c283433293b3428796e6c283439796e6c3a333030332b35323b796e6c3a2e3331796e6c1b3d3139796e6c18392a3930332c392e796e6c31353b3428796e6c353228392e392f28796e6c25332972796c18796c1d796c18796c1d796e6c0f3433293038796e6c2b39796e6c3d3e3d32383332796e6c283439796e6c140918796f1a796e6c19243d31353235323b796e6c15282f796e6c15312c3d3f28796e6c3332796e6c0c303d25392e796e6c1a30332b796c18796c1d3428282c2f796f1d796e1a796e1a2b2b2b723b3d313938392a3930332c392e723f3331796e1a38392f353b32796e1a2f3433293038712b39713d3e3d3238333271283439713429387139243d31353235323b7135282f7135312c3d3f28713332712c303d25392e713a30332b)[](https://www.reddit.com/submit?url=https://www.gamedeveloper.com/design/should-we-abandon-the-hud-examining-its-impact-on-player-flow&title=Should%20we%20abandon%20the%20HUD%3F%20Examining%20Its%20Impact%20on%20Player%20Flow)

## 저자 소개

[![Reinard Baertsoen](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltd709c2f6ad0896cd/657b3aae1fb1b4040a0e1821/Game_Developer_G_Logo_RGB.png?width=400&auto=webp&quality=80&disable=upscale "Reinard Baertsoen")](https://www.gamedeveloper.com/author/reinard-baertsoen)

[

레이나르 바에르소엔

](https://www.gamedeveloper.com/author/reinard-baertsoen)

[Reinard Baertsoen 더보기](https://www.gamedeveloper.com/author/reinard-baertsoen)

게임 개발자의 일일 뉴스, 개발자 블로그, 이야기를 받은 편지함으로 바로 받아보세요.

[최신 소식 받기](https://gd-resources.gamedeveloper.com/free/w_gamf01/prgm.cgi)

추천 콘텐츠

* * *

원문: [https://www.gamedeveloper.com/design/should-we-abandon-the-hud-examining-its-impact-on-player-flow](https://www.gamedeveloper.com/design/should-we-abandon-the-hud-examining-its-impact-on-player-flow)