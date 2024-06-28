---
title:  "길드워 2의 플레이어 하우징은 땅 쟁탈보다 장식을 우선시합니다."

categories:
  - 번역
  
tags:
  - Game Developer
toc: true
toc_sticky: true
 
date: 2024-06-28
last_modified_at: 2024-06-28
---
[![Picture of Bryant Francis](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt862ca995183d2fdf/650efe5138b21120135ae4ac/bryantcropped.jpg?width=100&auto=webp&quality=80&disable=upscale "Picture of Bryant Francis")](https://www.gamedeveloper.com/author/bryant-francis)

[브라이언트 프랜시스](https://www.gamedeveloper.com/author/bryant-francis), 수석 편집자

6월 28일, 2024

7분 읽기

![A farmlike Homestead from Guild Wars 2.](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt9fcd700d026b326d/667b04795e349100210aa65e/guildwars2homesteadfeatured.jpg?width=850&auto=webp&quality=95&format=jpg&disable=upscale "A farmlike Homestead from Guild Wars 2.")

ArenaNet 이미지 제공.

[](https://www.linkedin.com/sharing/share-offsite/?url=https://www.gamedeveloper.com/design/guild-wars-2-s-player-housing-pushes-decorating-over-land-grabs)[](https://www.facebook.com/sharer/sharer.php?u=https://www.gamedeveloper.com/design/guild-wars-2-s-player-housing-pushes-decorating-over-land-grabs)[](https://www.twitter.com/intent/tweet?url=https://www.gamedeveloper.com/design/guild-wars-2-s-player-housing-pushes-decorating-over-land-grabs)[](https://www.gamedeveloper.com/cdn-cgi/l/email-protection#744b0701161e1117004933011d18105423150607544652570c46434f07540418150d1106541c1b01071d1a13540401071c1107541011171b0615001d1a13541b0211065418151a10541306151607521519044f161b100d493d514644001c1b01131c00514644001c11514644121b18181b031d1a1351464412061b195146443315191151464430110211181b041106514644191d131c005146441d1a0011061107005146440d1b015a51443051443551443051443551464433011d1810514644231506075146444652570c46434f075146440418150d11065146441c1b01071d1a135146440401071c11075146441011171b0615001d1a135146441b02110651464418151a1051464413061516075144305144351c000004075147355146325146320303035a1315191110110211181b0411065a171b195146321011071d131a51463213011d1810590315060759465907590418150d1106591c1b01071d1a13590401071c1107591011171b0615001d1a13591b0211065918151a10591306151607)[](https://www.reddit.com/submit?url=https://www.gamedeveloper.com/design/guild-wars-2-s-player-housing-pushes-decorating-over-land-grabs&title=Guild%20Wars%202's%20player%20housing%20pushes%20decorating%20over%20land%20grabs)

## 한눈에 보기

*   길드워 2의 새로운 플레이어 주택 기능은 10년이 넘은 MMORPG에 중요한 추가 기능입니다.
*   이 기능을 구현하려면 매우 독특한 디자인 과제를 해결해야 했습니다.
*   아레나넷은 주택 소유권을 더 잘 구현하기 위해 부동산 관리가 아닌 개인 표현을 시스템의 핵심 축으로 삼았습니다.

온라인 게임에서 플레이어의 주택은 의외로 매력적인 주제입니다. 가상 세계에서 롤플레잉의 판타지를 더해주기 때문에 자주 요청되는 기능이지만, 개발자가 디지털 토지[공급을 고려하지](https://www.gamedeveloper.com/business/digital-real-estate-and-the-digital-housing-crisis) 않으면이를 구현할 때 여러 가지 부작용이 발생할 수 있습니다.

아레나넷은 다행히도 길드워 2의다음 확장팩인 얀티르 와일즈를개발하는 동안 이 문제에 직면하지 않았습니다. 개발자 조엘 에커트, 릭 루버스, 앤드류 그레이는 최근 게임 디벨로퍼와의 인터뷰에서 이 게임의 새로운 "홈스테드" 기능의 목표는 완전히 구현된 동네를 건설하는 것이 아니라 플레이어가 직접 커스터마이징하고 만들 수 있는 새로운 공간을 추가하는 것이었다고 밝혔습니다.

루버스의 말처럼 "건설 부상은 시뮬레이션할 필요가 없었습니다." 엄청나게 높은 주택 비용이나 폭압적인 주택 소유자 협회도 마찬가지였습니다.

홈스테드 기능은 오래된 온라인 게임이 충성도 높은 유저를 위해 어떻게 발전할 수 있는지에 대한 흥미로운 사례 연구입니다. 아레나넷은 주택 공급량을 제한하지 않음으로써 한 방은 피했지만 , 기존 경험을 짓밟지 않으면서도 길드워2의 게임플레이에홈스테드가 잘 어울리도록 해야 하는 과제를 안고 있었습니다.

## 길드워 2의 주택 기능은 기존 꾸미기 도구를 기반으로 합니다.

관련:[심층](https://www.gamedeveloper.com/production/deep-dive-reimagining-the-battle-pass-to-maximize-enjoyment-in-guild-wars-2) 분석:[길드워 2의 배틀패스 재구성하기](https://www.gamedeveloper.com/production/deep-dive-reimagining-the-battle-pass-to-maximize-enjoyment-in-guild-wars-2)

길드워2처럼 오랜 기간 동안MMORPG가 운영된 경우 , 충성도가 높은 많은 플레이어는 자신의 캐릭터를 꾸미고 싶은 욕구를 느끼게 됩니다. 하지만 수천 개의 방어구를 업그레이드하고 나면 "몸의 공간이 부족해지기 시작한다"고 그레이는 말합니다(말장난인가요?).

길드워 2에는 이미 길드에 모인 플레이어 그룹이 공유할 수 있는 '길드 홀'과 '아레나'라는 커스터마이징 가능한 공간이 있었습니다. 이 홀에서 플레이어는 벽, 깃발, 기념비, 심지어 사용자 지정 조명으로 공간을 꾸밀 수 있습니다. 즉, 아레나넷은 기존의 데코레이션 기술을 기반으로 구축할 수 있었으며 처음부터 다시 시작하지 않았습니다.

![A player Homestead interior in Guild Wars 2. A high-backed red chair is in the foreground.](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltffb8894ac6a0ed95/667b0579e161e540c7cea072/GW2_JW_PR_10.png?width=700&auto=webp&quality=80&disable=upscale "A player Homestead interior in Guild Wars 2. A high-backed red chair is in the foreground.")

ArenaNet 이미지 제공.

홈스테드는 일반 게임 월드에 있는 것이 아니라 각 플레이어가 획득할 수 있는 개인 인스턴스입니다(계정당 하나만 얻을 수 있음). 홈스테드에 들어가면 몇 가지 장식이 이미 배치된 단순한 건물을 발견할 수 있습니다. 에커트는 심즈 4를 개발하면서 많은 플레이어가 백지 상태의 무한한 가능성에 겁먹지 않기 위해 기존 장식물이 필요하다는 사실을 알게 되었다고설명했습니다 ."심즈에서 우리가 발견한 것은 많은 플레이어층이 뛰어넘을 수 있는 예시가 필요하다는 것이었습니다."라고 그는 회상했습니다. 그는 (자신과 같은) 작가들이 기본적인 빈 페이지에 겁을 먹을 수 있다는 점을 암시했습니다. "많은 자유가 주어지지만 때로는 그 자유가 무서울 수도 있습니다."

공간을 꾸미기로 결정한 후에는 친구를 초대할 때 어떤 권한을 부여할지 결정할 수도 있습니다. 낙하 피해를 켜거나 끄고 맞춤형 점프 퍼즐을 만들 수 있습니다. 함께 농사를 지을 수 있는 자원 노드를 설정할 수도 있습니다.

여기서 흥미로운 점이 있습니다. 길드워 2의집 은 현실 세계의 집과 같은 기능을 하지 않습니다.Minecraft, Rust, Enshrouded와 같은 서바이벌 게임에서 플레이어가 조립하는 집과는 비교조차 할 수 없습니다. 길드워 2에서 플레이어는 던전을 탐험하고 레이드 보스와 싸우기 위해 세계를 돌아다닙니다. 집은 몬스터나 외부 요소의 위험에 노출되지 않습니다. 어떤 면에서 집은 하루를 시작하고 끝내는 장소라기보다는 방문해야 하는 공간에 가깝습니다.

이는 모두 아레나넷이 의도한 것이라고 그레이는 말합니다. "저희는 어떻게 하면 플레이어를 세상으로 다시 밀어낼 수 있을지에 대해 더 많이 생각했습니다."라고 그는 설명합니다. 개발팀은 플레이어가 모험 경험에서 농장이 필수라고 느끼는 것을 싫어했습니다. 모든 플레이어가 하루를 시작하기 전에 본거지에서 자원을 채굴하는 것을 즐기지는 않을 것이기 때문입니다.

이 결정은 경험치 경제와 같은 홈스테드 시스템을 만드는 데 엄청난 파급 효과를 가져왔습니다. 예를 들어, 플레이어가 집에 배치하기 위해 많은 장식을 "제작"하지만, 장식 제작 시스템에는 "제작 경험치" 시스템이 사용되지 않습니다. 길드워 2에서는 캐릭터의 최대 레벨에 도달한 플레이어를 위한 진행 시스템인 "마스터리 XP "를사용합니다 . 마스터리 XP 는길드워 2의 세계로 나가 다양한 업적을 완료하면 획득할 수 있습니다.

그레이는 이를 다음과 같이 설명했습니다. 플레이어가 많은 양의 제작 경험치가 필요한 홈스테드 아이템을 만들고 싶을 때, 가장 빠르게 잠금을 해제하는 방법은 가만히 서서 "물건 제작"을 반복해서 클릭해 수치를 올리는 것입니다.

![A player character wielding a spear stands in front of an explosion in Guild Wars 2.](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt2c869c7c140fd56b/667b04c4cf7a986e4a3f4608/GW2_JW_PR_07-1024x576.png?width=700&auto=webp&quality=80&disable=upscale "A player character wielding a spear stands in front of an explosion in Guild Wars 2.")

ArenaNet 이미지 제공.

플레이어가 세계로 나가서 숙련도 XP를 획득하면 실제로는 길드워 2를플레이하면서 홈스테딩 목표를 쫓고 있는 것입니다. 그레이는 아레나넷이 가능한 한 많은 플레이어가 농장에 참여하기를 원한다고 말했습니다. 길드워2를 정기적으로 플레이하고 여러 확장팩의 콘텐츠를 즐기는 플레이어라면 농장에서할 수 있는 재미있는 일을 찾을 수 있다는 것이 스튜디오의 목표입니다 .

## 12년 된 게임에 꾸미기 도구를 추가하는 것은 쉽지 않습니다.

길드워 2는 플레이어가 벽돌 하나하나를 쌓아 집을 짓고 장식을 하는 서바이벌 게임의 전철을 밟지 않습니다. 기존 장식 도구를 발전시킨 것이기 때문에 플레이어가 '비행 모드'에 들어가서 카메라를 움직이며 공간을 탐색하고 원하는 대로 정확하게 물건을 배치할 수 있도록 설계되었습니다.

루버스는 홈스테드 기능을 플레이 테스트하면서 아레나넷이 새로운 도구를 설계하는 데 영감을 얻었다고 말합니다. 플레이어는 자신의 집 영역에서 "와이어프레임 모드"에 액세스하여 홈스테드의 오브젝트를 쉽게 볼 수 있는 윤곽선으로 렌더링할 수 있습니다. 플레이어는 장애물과 지형을 투과하여 볼 수 있고, 잘못 배치했거나 이전에 땅에 묻혀 있던 장식물을 더 잘 찾을 수 있게 됩니다.

기존 장식 도구를 확장하는 데에는 '자해적'인 기술 부채가 따랐습니다. 아레나넷은 농장의 기존 장식 도구를 업데이트하려면 길드 회관에도 소급 적용해야 한다고 결정했습니다. 결국, 여전히 자신의 집보다 길드 전당을 꾸미는 데 더 많은 투자를 하는 플레이어가 있을 것이기 때문입니다. 단순한 시스템으로 남겨두면 불필요한 실망을 초래할 수 있습니다.

그리고 더 중요한 문제는 길드워 2에서장식 개체의 작동 방식을 업데이트하면 기존 장식 도구와 개체의 작동 방식이 깨질 수 있다는 점입니다. 홀 전체가 폐허가 될 것입니다. 당연히 좋은 결과는 아닙니다.

![A Homestead interior in Guild Wars 2. It looks like a log cabin with various fantasy accoutrements. ](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt641ed9a6e2ca79fe/667b0520cb7c270bc1e696dd/GW2_JW_PR_11.jpg?width=700&auto=webp&quality=80&disable=upscale "A Homestead interior in Guild Wars 2. It looks like a log cabin with various fantasy accoutrements. ")

ArenaNet 이미지 제공.

그레이는 가장 큰 한계는 "오래된 게임"의 데이터 저장 작업이 복잡할 수 있다는 점이라고 말했습니다. 그래서 플레이어는 계정당 하나의 홈스테드만 허용되며 모든 캐릭터가 공유할 수 있습니다. 그레이는 팀이 "\[거주 가능한\] 공간의 최대 크기, 장식의 수 등 한계를 뛰어넘을 수 있는 모든 종류의 것들을 파악하려고 노력했다"고 회상했습니다. 모든 플레이어 캐릭터가 농장을 가질 수 있다면(모든 플레이어 계정이 아닌) 농장의 규모를 "대폭 축소"할 수 있습니다.

그레이와 루버스는 MMORPG에 플레이어 주택을 추가하려면 "현실적"이 되기 전에 재미가 있어야 한다는 점을 익히 지적한 바 있습니다. 하지만 게임 후반부에 이 기능을 추가한 것은 이러한 기능을 "재미있게" 만드는 데 필요한 창의성을 보여줍니다. 자원을 채집하고 건물을 직접 조립하는 것과 같은 일상적인 작업을 플레이어가 원하는 곳에 가구를 놓을 수 있는 간편한 도구를 제공하는 과정으로 대체하는 것은 판타지 세계에서 사는 현실적인 경험을 시뮬레이션하지 못합니다.

하지만 주택 시스템의 목적이 생존 가능성이 아니라 자기 표현이라면 플레이어가 왜 집을 소유하는 일상적인 어려움을 시뮬레이션하고 싶을까요? 플레이어의 창의성을 우선시하는 것은 아레나넷과 다른 개발자들이 어떻게 장기적인 온라인 게임에서 더 많은 생명을 불어넣을 수 있는지 보여줍니다.

자세히 읽어보세요:

[인기 스토리](https://www.gamedeveloper.com/keyword/top-stories)

[](https://www.linkedin.com/sharing/share-offsite/?url=https://www.gamedeveloper.com/design/guild-wars-2-s-player-housing-pushes-decorating-over-land-grabs)[](https://www.facebook.com/sharer/sharer.php?u=https://www.gamedeveloper.com/design/guild-wars-2-s-player-housing-pushes-decorating-over-land-grabs)[](https://www.twitter.com/intent/tweet?url=https://www.gamedeveloper.com/design/guild-wars-2-s-player-housing-pushes-decorating-over-land-grabs)[](https://www.gamedeveloper.com/cdn-cgi/l/email-protection#e5da9690878f808691d8a2908c8981c5b2849796c5d7c3c69dd7d2de96c59589849c8097c58d8a90968c8b82c59590968d8096c58180868a9784918c8b82c58a938097c589848b81c58297848796c3848895de878a819cd8acc0d7d5918d8a90828d91c0d7d5918d80c0d7d5838a89898a928c8b82c0d7d583978a88c0d7d5a2848880c0d7d5a1809380898a958097c0d7d5888c828d91c0d7d58c8b918097809691c0d7d59c8a90cbc0d5a1c0d5a4c0d5a1c0d5a4c0d7d5a2908c8981c0d7d5b2849796c0d7d5d7c3c69dd7d2de96c0d7d59589849c8097c0d7d58d8a90968c8b82c0d7d59590968d8096c0d7d58180868a9784918c8b82c0d7d58a938097c0d7d589848b81c0d7d58297848796c0d5a1c0d5a48d91919596c0d6a4c0d7a3c0d7a3929292cb8284888081809380898a958097cb868a88c0d7a38180968c828bc0d7a382908c8981c892849796c8d7c896c89589849c8097c88d8a90968c8b82c89590968d8096c88180868a9784918c8b82c88a938097c889848b81c88297848796)[](https://www.reddit.com/submit?url=https://www.gamedeveloper.com/design/guild-wars-2-s-player-housing-pushes-decorating-over-land-grabs&title=Guild%20Wars%202's%20player%20housing%20pushes%20decorating%20over%20land%20grabs)

## 저자 소개

[![Bryant Francis](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt862ca995183d2fdf/650efe5138b21120135ae4ac/bryantcropped.jpg?width=400&auto=webp&quality=80&disable=upscale "Bryant Francis")](https://www.gamedeveloper.com/author/bryant-francis)

[

브라이언트 프랜시스

](https://www.gamedeveloper.com/author/bryant-francis)

선임 편집자, GameDeveloper.com

브라이언트 프랜시스는 매사추세츠주 보스턴에 거주하는 작가, 저널리스트, 내러티브 디자이너입니다. 현재 비디오 게임 업계를 위한 선도적인 B2B 간행물인 Game Developer에 글을 기고하고 있습니다. 그의 대표작으로는 프록시 스튜디오의 출시 예정인 4X 전략 게임 제폰과 앰플리튜드 스튜디오의 2017년 게임 엔들리스 스페이스 2가 있습니다.

[더보기 브라이언트 프랜시스](https://www.gamedeveloper.com/author/bryant-francis)

게임 개발자의 일일 뉴스, 개발자 블로그, 스토리를 받은 편지함으로 바로 받아보세요.

[최신 소식 받기](https://gd-resources.gamedeveloper.com/free/w_gamf01/prgm.cgi)

추천 콘텐츠

* * *

원문: [https://www.gamedeveloper.com/design/guild-wars-2-s-player-housing-pushes-decorating-over-land-grabs](https://www.gamedeveloper.com/design/guild-wars-2-s-player-housing-pushes-decorating-over-land-grabs)