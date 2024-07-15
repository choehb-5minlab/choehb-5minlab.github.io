---
title:  "멀티플레이어 개발자는 콩코드의 크루 빌더 시스템을 자세히 살펴봐야 합니다."

categories:
  - 번역
  
tags:
  - Game Developer
toc: true
toc_sticky: true
 
date: 2024-07-16
last_modified_at: 2024-07-16
---
[![Picture of Bryant Francis](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt862ca995183d2fdf/650efe5138b21120135ae4ac/bryantcropped.jpg?width=100&auto=webp&quality=80&disable=upscale "Picture of Bryant Francis")](https://www.gamedeveloper.com/author/bryant-francis)

[브라이언트 프랜시스](https://www.gamedeveloper.com/author/bryant-francis), 수석 편집자

7월 15일, 2024

6분 읽기

![Three Concord Freegunners pose in front of a colorful background.](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt9b2943da16a0839c/66956ec3f5ef5f532aa73632/concordfeatured.jpg?width=1280&auto=webp&quality=95&format=jpg&disable=upscale "Three Concord Freegunners pose in front of a colorful background.")

Firewalk Studios/PlayStation 이미지 제공.

[](https://www.linkedin.com/sharing/share-offsite/?url=https://www.gamedeveloper.com/design/multiplayer-devs-should-take-a-close-look-at-concords-crew-builder-system)[](https://www.facebook.com/sharer/sharer.php?u=https://www.gamedeveloper.com/design/multiplayer-devs-should-take-a-close-look-at-concords-crew-builder-system)[](https://www.twitter.com/intent/tweet?url=https://www.gamedeveloper.com/design/multiplayer-devs-should-take-a-close-look-at-concords-crew-builder-system)[](https://www.gamedeveloper.com/cdn-cgi/l/email-protection#744b0701161e11170049390118001d0418150d1106541011020754071c1b0118105400151f1154155417181b071154181b1b1f54150054371b1a171b061052570c46434f0754370611035436011d1810110654070d07001119521519044f161b100d493d514644001c1b01131c00514644001c11514644121b18181b031d1a1351464412061b195146443315191151464430110211181b041106514644191d131c005146441d1a0011061107005146440d1b015a514430514435514430514435514644390118001d0418150d110651464410110207514644071c1b01181051464400151f115146441551464417181b0711514644181b1b1f5146441500514644371b1a171b061052570c46434f075146443706110351464436011d18101106514644070d070011195144305144351c000004075147355146325146320303035a1315191110110211181b0411065a171b195146321011071d131a514632190118001d0418150d1106591011020759071c1b0118105900151f1159155917181b071159181b1b1f59150059171b1a171b06100759170611035916011d1810110659070d07001119)[](https://www.reddit.com/submit?url=https://www.gamedeveloper.com/design/multiplayer-devs-should-take-a-close-look-at-concords-crew-builder-system&title=Multiplayer%20devs%20should%20take%20a%20close%20look%20at%20Concord's%20Crew%20Builder%20system)

## 한눈에 보기

*   파이어워크 스튜디오의 콩코드가 PlayStation 5 베타 버전에 출시되었습니다.
*   "영웅 슈팅 게임"인 이 게임에서 플레이어는 경기 중에 교체할 수 있는 캐릭터의 "크루"를 선택할 수 있습니다.
*   성장의 여지가 많은 놀랍도록 창의적인 메커니즘입니다.

소니의 성공적인 라이브 서비스 온라인 게임 시리즈 중 첫 번째 작품이 될 것으로 기대되는파이어워크 게임즈의 1인칭 슈팅 게임콩코드가 7월 13일 주말에 클로즈 베타 기간에 들어 갔습니다.[수많은 라이브 서비스 프로젝트를 중단하거나 미](https://www.gamedeveloper.com/business/sony-pushes-back-half-of-its-planned-live-service-games)뤄온 소니에게 이 게임이 큰 성공을 거둘지는 아직 확실하지 않지만, 현재로서는 플레이어와 개발자가 파이어워크가 준비한 게임을 미리 체험해 볼 수 있습니다.

1인칭 슈팅 게임 베테랑으로 구성된 이 스튜디오의 팀은 확실히 PlayStation 5에서 훌륭하게 플레이할 수 있는 매끄럽고 빠른 게임플레이 루프를 만들어냈지만, 베타 버전 메뉴에 숨겨져 있는 기능 중 가장 눈에 띄는 것은 "크루 빌더"라는 분대 구성 메커니즘입니다.

크루 빌더 도구는 즉각적인 상상력을 자극합니다. 온라인 슈팅 게임에서 캐릭터와 다양한 게임 모드에 최적화하는 방법을 고민하고, 좋아하는캐릭터만 고집하지 않고 플레이하는 동안 다른캐릭터( 콩코드에서는"프리거너"라고 함)로 전환하는 두 가지 목표를 달성할 수 있는 좋은 방법입니다 .

## 콩코드의 승무원 빌더는 플레이어가 캐릭터를 계속 바꾸기를 원합니다.

크루 빌더에서 플레이어는 게임 내 16명의 캐릭터 중 12명으로 구성된 '크루'를 구성합니다(출시 후 더 많은 캐릭터가 추가될 예정). 이 명단은 플레이어가 각 매치에서 캐릭터를 선택할 때 선택할 수 있는 그룹이 됩니다.

관련: 출시[10년을 맞아, 번지가 데스티니 가디언즈의 라이브 서비스 속도를](https://www.gamedeveloper.com/business/10-years-in-bungie-shifts-destiny-2-pacing-in-live-service-shakeup) 바꿉니다.

플레이어는 자신이 보유한 캐릭터의 변형 버전을 최대 3개까지 선택할 수 있는데, 베타 초기에는 각각 다른 패시브 능력을 가진 녹색 피부의 총잡이 레녹스의 두 가지 버전을 잠금 해제했습니다. 승무원을 구성할 때 각 버전을 포함할 수 있는 옵션이 있어서 경기 상황에 따라 교체할 수 있었습니다.

플레이어는 12명의 캐릭터 중 5명의 고유 캐릭터만 선택하면 됩니다. 계산을 해보면, 플레이어는 4명의 캐릭터만 고를 수 있는 것이 아니라 항상 5명 이상을 선택해야 하며, 어떤 변종이 실제로 자신의 자리를 차지할 수 있는지 고려해야 합니다.

이 시스템은 XCOM 2와같은 전술 게임의 캐릭터 선택과 수집형 카드 게임의 덱 구성 로직을 결합한 것같은 느낌을 줍니다.

플레이어에게 캐릭터 제작자를 제어할 수 있는 기능을 부여한 것만으로도 신선한 선택입니다. 에이펙스 레전드와같은 라이브 서비스 슈팅 게임에서는 게임 내 모든 신규 캐릭터에 일정량의 실제 화폐 또는 게임 내 화폐가 필요하기 때문에 과거에는 이러한 기능을 사용할 수 없었습니다. 그 수를 제한함으로써 플레이어가 자신이 좋아하는 캐릭터와 각 게임 모드에 맞는 캐릭터에 대해 생각하도록 유도합니다.

![The Crew Builder menu in Concord. The menu shows which Crew bonuses the player has received.](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt39ffeb0a83302354/66956c48e6031c4025e0f4ee/Concord_Beta_20240715125031.jpg?width=700&auto=webp&quality=80&disable=upscale "The Crew Builder menu in Concord. The menu shows which Crew bonuses the player has received.")

파이어워크 스튜디오/플레이스테이션 이미지 제공.

그 자체로도 클래식 캐릭터 선택에 재미를 더하는 꽤 강력한 방법입니다. 이 시스템은 플레이어가 경기 도중에도 캐릭터를 교체할 수 있도록 장려합니다.

"승무원 보너스"라는 시스템을 통해 그렇게 할 수 있습니다. 각 크루에 다른 캐릭터를 조합하면 경기 진행에 따라 무기 사거리, 재장전 속도, 회복량 증가 등 다양한 패시브 보너스가 크루에 추가됩니다. 이러한 보너스를 획득하려면 플레이어는 게임을 플레이하면서 캐릭터 병과를 전환해야 합니다.

한 팀이 한 캐릭터 그룹에 집착하는 스쿼드에 의해 굴러가게 되면, 이에 대응할 수 있는 캐릭터를 찾아 나선 팀은 상대방이 갖지 못한 능력치를 강화한 채 다시 전투에 참여하게 됩니다.

이 시스템은 한 가지 직업만 플레이하려는 플레이어의 전형적인 멀티플레이어 전형에 압력을 가한다는 점에서 인상적입니다. 한 팀에서 한 번에 한 명의 플레이어만 각 캐릭터를 플레이할 수 있기 때문에, 고집불통인 플레이어는 자신의 실력이 좋지 않더라도 전략을 바꾸지 않을 수 있는 위험이 있습니다. 또는 이미 자신이 좋아하는 프리거를 선택한 다른 플레이어를 공격할 수도 있습니다.

이 시스템을 사용하면 플레이어는 캐릭터 사이를 이동하고 공간을 확보하여 은유적인 장난감을 은유적인 놀이판으로 넘길 가능성이 높아집니다. 플레이어가 프리거 한 명만 고집하다가 죽고 싶다면 여전히 선택의 여지가 있지만, 전략적으로 캐릭터를 섞어 유닛을 강화하는 조직적인 적 팀에 불리하게 작용할 수 있습니다.

이는 유저의 플레이 스타일을 빼앗지 않으면서도 새로운 시도를 할 수 있도록 넌지시와 윙크를 보내는 현명한 디자인 결정입니다.

물론 완벽한 시스템은 없으므로 파이어워크(및 다른 개발사)가 더 나은 시스템을 만들기 위해 할 수 있는 일은 다음과 같습니다.

## 크루 빌더는 몇 가지 개선이 필요할 수 있습니다.

베타 버전과 최종 릴리스 사이에 변경될 가능성이 있지만, 크루 빌더를 최적화하는 것은 물론 사용 방법을 파악하는 것도 어려운 작업이었습니다. 현재 게임에는 튜토리얼이 포함되어 있지 않아서 분대 구성 선택이 어떤 영향을 미치는지 이해하기 위해 한참을 헤매야 했습니다.

현재 승무원 빌더의 영향을 이해하는 데 있어 가장 어려운 점은 사용자 인터페이스 문제인 것 같습니다. 승무원을 선택할 때, 캐릭터를 추가한 후 정확히 어떤 승무원 보너스가 발동되는지 메뉴에서 큰 소리로 알려주지 않습니다. 이러한 보너스는 캐릭터 프로필에서 확인할 수 있으며, 완료 후 승무원 명단에도 표시되지만, 신규 플레이어의 경우 능력의 작동 방식을 이해하려고 할 때 3~4번째로 우선순위를 두어야 합니다(저는 아직도 쓰레기 로봇 1-Off를 어떻게 플레이해야 할지 모르겠습니다).

이 문제는 개별 경기로 이어집니다. 승무원 빌더를 테스트하는 동안 보너스를 잠금 해제했음을 알려주는 팝업이 계속 뜨길 기다렸습니다. 제가 보너스를 획득했는지 알 수 있는 유일한 방법은 아래 선수단 목록에서 TV를 찡그리고 선수 핸들이 있는 카드 아래에 있는 작은 기호를 보는 것이었습니다.

![A screenshot of Concord. A human soldier in futuristic armor stands at the ready on a jumpship. Many screens display gameplay information.](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltbe1b0ef0088e6add/66956bc5053818325b62c7ed/Concord_Beta_20240715132146.jpg?width=700&auto=webp&quality=80&disable=upscale "A screenshot of Concord. A human soldier in futuristic armor stands at the ready on a jumpship. Many screens display gameplay information.")

파이어워크 스튜디오/플레이스테이션 이미지 제공.

다음 문제는 제가 무엇을 잠금 해제했는지 정확히 모른다는 것이었습니다. 승무원 빌더를 중심으로 전략을 세우는 인내심 있는 플레이어라면 어떤 특성이 어떤 기호와 연관되어 있는지 알 수 있겠지만, 경기 중반에 총격전이 벌어지면 어떤 보너스를 활성화했는지 전혀 알 수 없었습니다.

마지막으로 - 개인적인 취향이지만 - 보너스가 지금은 "특별하다"고 느껴지지 않습니다. 저는 [발더스 게이트 3의](https://www.gamedeveloper.com/design/baldur-s-gate-3-s-item-balancing-went-big-because-small-stat-changes-are-not-cool-) [디자인 철학이](https://www.gamedeveloper.com/design/baldur-s-gate-3-s-item-balancing-went-big-because-small-stat-changes-are-not-cool-) "멋지지 않은" 능력치 증가보다 플레이어가 능력치 변화에 대한 인식을 우선시하는 것을 좋아합니다.

승무원 빌더의 기능에 대해 파이어워크 게임즈와 저는 경쟁 플레이를 위해 이러한 보너스를 미묘하게 유지할 필요가 있다고 생각하기 때문에 이 부분에서 의견이 다를 수 있지만, 그래도 괜찮습니다! 다른 스튜디오의 디자이너들이 이 기능의 장점을 잘 파악하여 자신만의 개성을 살릴 수 있기를 바랍니다.

결함은 차치하고서라도 승무원 빌더는 멀티플레이어 게임에 덱 구성 메커니즘을 도입할 수 있는 훌륭한 템플릿입니다. 경기 사이에 할 수 있는 재미있는 활동이며, 최고의 크루를 운영하기 위해 플레이어 간에 토론을 유도할 수 있습니다. 또한 개발자가 밸런스를 조정할 수 있는 레버를 추가하고 새로운 직업이나 업데이트를 출시할 때 새로운 깊이를 더할 수 있습니다.

출시 후에도콩코드를많이 플레이할지는 모르겠지만(요즘 미니어처를 그리느라 너무 바쁘거든요), 앞으로 한동안은 크루 빌더에 대해 계속 생각하게 될 것 같습니다.

자세히 읽어보세요:

\[[회사\] 플레이스테이션톱](https://www.gamedeveloper.com/keyword/-company-playstation)[스토리추천](https://www.gamedeveloper.com/keyword/top-stories)[블로그디자이너](https://www.gamedeveloper.com/keyword/designer)

[](https://www.linkedin.com/sharing/share-offsite/?url=https://www.gamedeveloper.com/design/multiplayer-devs-should-take-a-close-look-at-concords-crew-builder-system)[](https://www.facebook.com/sharer/sharer.php?u=https://www.gamedeveloper.com/design/multiplayer-devs-should-take-a-close-look-at-concords-crew-builder-system)[](https://www.twitter.com/intent/tweet?url=https://www.gamedeveloper.com/design/multiplayer-devs-should-take-a-close-look-at-concords-crew-builder-system)[](https://www.gamedeveloper.com/cdn-cgi/l/email-protection#2d125e584f47484e591060584159445d414c54485f0d49485b5e0d5e45425841490d594c46480d4c0d4e41425e480d414242460d4c590d6e42434e425f490b0e551f1a165e0d6e5f485a0d6f58444149485f0d5e545e5948400b4c405d164f4249541064081f1d594542584a4559081f1d594548081f1d4b424141425a44434a081f1d4b5f4240081f1d6a4c4048081f1d69485b4841425d485f081f1d40444a4559081f1d444359485f485e59081f1d54425803081d69081d6c081d69081d6c081f1d60584159445d414c54485f081f1d49485b5e081f1d5e4542584149081f1d594c4648081f1d4c081f1d4e41425e48081f1d41424246081f1d4c59081f1d6e42434e425f490b0e551f1a165e081f1d6e5f485a081f1d6f58444149485f081f1d5e545e594840081d69081d6c4559595d5e081e6c081f6b081f6b5a5a5a034a4c404849485b4841425d485f034e4240081f6b49485e444a43081f6b40584159445d414c54485f0049485b5e005e454258414900594c4648004c004e41425e480041424246004c59004e42434e425f495e004e5f485a004f58444149485f005e545e594840)[](https://www.reddit.com/submit?url=https://www.gamedeveloper.com/design/multiplayer-devs-should-take-a-close-look-at-concords-crew-builder-system&title=Multiplayer%20devs%20should%20take%20a%20close%20look%20at%20Concord's%20Crew%20Builder%20system)

## 저자 소개

[![Bryant Francis](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt862ca995183d2fdf/650efe5138b21120135ae4ac/bryantcropped.jpg?width=400&auto=webp&quality=80&disable=upscale "Bryant Francis")](https://www.gamedeveloper.com/author/bryant-francis)

[

브라이언트 프랜시스

](https://www.gamedeveloper.com/author/bryant-francis)

선임 편집자, GameDeveloper.com

브라이언트 프랜시스는 매사추세츠주 보스턴에 거주하는 작가, 저널리스트, 내러티브 디자이너입니다. 현재 비디오 게임 업계를 위한 B2B 간행물인 Game Developer에 글을 기고하고 있습니다. 그의 대표작으로는 프록시 스튜디오의 출시 예정인 4X 전략 게임 Zephon과 앰플리튜드 스튜디오의 2017년 게임 Endless Space 2가 있습니다.

[더보기 브라이언트 프랜시스](https://www.gamedeveloper.com/author/bryant-francis)

게임 개발자의 일일 뉴스, 개발자 블로그, 스토리를 받은 편지함으로 바로 받아보세요.

[최신 소식 받기](https://gd-resources.gamedeveloper.com/free/w_gamf01/prgm.cgi)

추천 콘텐츠

* * *

원문: [https://www.gamedeveloper.com/design/multiplayer-devs-should-take-a-close-look-at-concords-crew-builder-system](https://www.gamedeveloper.com/design/multiplayer-devs-should-take-a-close-look-at-concords-crew-builder-system)