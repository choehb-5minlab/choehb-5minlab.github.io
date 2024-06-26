---
title:  "아늑한 농사/생활 시뮬레이션 어드벤처에서 매력적이고 지속적인 게임플레이 만들기"

categories:
  - 번역
  
tags:
  - Game Developer
toc: true
toc_sticky: true
 
date: 2024-06-27
last_modified_at: 2024-06-27
---
[![Picture of Deborah Chantson](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltacf0ac70802bf305/65087f540db1edff5f8461fa/Deborah_Chantson.jpg?width=100&auto=webp&quality=80&disable=upscale "Picture of Deborah Chantson")](https://www.gamedeveloper.com/author/deborah-chantson)

[데보라 챈슨](https://www.gamedeveloper.com/author/deborah-chantson), 블로거

6월 26일, 2024

5분 읽기

![](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt19a9854537b8426a/667ade59e161e51dadce9fda/Coral_Island_6_22_2024_8_54_30_AM.png?width=850&auto=webp&quality=95&format=jpg&disable=upscale)

[](https://www.linkedin.com/sharing/share-offsite/?url=https://www.gamedeveloper.com/design/creating-compelling-and-continuous-gameplay-in-a-cozy-farming-life-sim-adventure)[](https://www.facebook.com/sharer/sharer.php?u=https://www.gamedeveloper.com/design/creating-compelling-and-continuous-gameplay-in-a-cozy-farming-life-sim-adventure)[](https://www.twitter.com/intent/tweet?url=https://www.gamedeveloper.com/design/creating-compelling-and-continuous-gameplay-in-a-cozy-farming-life-sim-adventure)[](https://www.gamedeveloper.com/cdn-cgi/l/email-protection#b788c4c2d5ddd2d4c38af4c5d2d6c3ded9d097f4d8dac7d2dbdbded9d097d6d9d397f4d8d9c3ded9c2d8c2c497f0d6dad2c7dbd6ce97ded997d697f4d8cdce97f1d6c5daded9d098fbded1d297e4deda97f6d3c1d2d9c3c2c5d291d6dac78cd5d8d3ce8afe928587c3dfd8c2d0dfc3928587c3dfd2928587d1d8dbdbd8c0ded9d0928587d1c5d8da928587f0d6dad2928587f3d2c1d2dbd8c7d2c5928587daded0dfc3928587ded9c3d2c5d2c4c3928587ced8c2999287f39287f69287f39287f6928587f4c5d2d6c3ded9d0928587f4d8dac7d2dbdbded9d0928587d6d9d3928587f4d8d9c3ded9c2d8c2c4928587f0d6dad2c7dbd6ce928587ded9928587d6928587f4d8cdce928587f1d6c5daded9d09285f1fbded1d2928587e4deda928587f6d3c1d2d9c3c2c5d29287f39287f6dfc3c3c7c49284f69285f19285f1c0c0c099d0d6dad2d3d2c1d2dbd8c7d2c599d4d8da9285f1d3d2c4ded0d99285f1d4c5d2d6c3ded9d09ad4d8dac7d2dbdbded9d09ad6d9d39ad4d8d9c3ded9c2d8c2c49ad0d6dad2c7dbd6ce9aded99ad69ad4d8cdce9ad1d6c5daded9d09adbded1d29ac4deda9ad6d3c1d2d9c3c2c5d2)[](https://www.reddit.com/submit?url=https://www.gamedeveloper.com/design/creating-compelling-and-continuous-gameplay-in-a-cozy-farming-life-sim-adventure&title=Creating%20Compelling%20and%20Continuous%20Gameplay%20in%20a%20Cozy%20Farming%2FLife%20Sim%20Adventure)

저는 [코럴 아일랜드에](https://blog.stairwaygames.com/coral-island)중독되었습니다 . 제가 말했잖아요. Xbox Game Pass로 게임을 시작한 지 몇 달밖에 되지 않았는데 지금까지 300시간 이상(수많은 팟캐스트와 오디오북을 들으면서요, 오디오 팀에 죄송합니다) 플레이했습니다.

스티키 브레인 스튜디오의 작가이자 내러티브 디자이너인 저는 발표되지 않은 다음 타이틀을 위한 리서치로 몇 가지 게임을 테스트하고 있었습니다. 저는 스타듀 밸리를 분노에 차서 그만둔 후에야 코랄 아일랜드에 빠져들었습니다 (저희 팀의 애니메이션 디렉터이자 다음 게임의 콘셉트 크리에이터인 [E. 조안 리는](https://www.linkedin.com/in/ejoanlee-illustration/) 이 사실을재밌게 생각하더군요). 때로는 정말 미학적인 부분과 시작 방법을 설명하는 것으로 귀결되기도 합니다.

제 동료들의 이야기를 들어 보면산호섬은스타듀 밸리와 놀라울 정도로 비슷하다고 합니다. 코랄 아일랜드의메인 스토리 퀘스트는 바다의 쓰레기를 치우고 섬과 주변 바다를 오염시키고 있는 기름 유출 뿌리를 관통하여 녹이는 비콘을 발견하는 것입니다.약간 단조로워지기 때문에(그래서 저는 오디오북을 들었습니다) 농사짓는 시뮬레이션 부분도 있고 NPC와의 상호작용과 수집으로 게임플레이에 활기를 불어넣는 것이 좋습니다.

저는 제작 퀘스트와 자원 관리가 있는 게임을 좋아합니다. 미네코의 야시장도 두 번이나플레이하며 오랜 시간을 보냈어요 . 코랄 아일랜드에는 다양한 인종의 NPC가 등장하고, 인도네시아 스튜디오/개발팀이 동아시아에 초점을 맞춰 한가위 달 축제, 월병, 벚꽃 축제, 인도네시아 음식 등이 등장한다는 점도 마음에 들어요. 바람이 부는 날 디지털 콜리플라워 밭을 달리는 것이 이렇게 만족스러울 줄은 몰랐을 정도로 디테일에 신경을 쓴 시각적으로 놀라운 경험입니다.

아직 플레이 시간이 긴 게임을 작업할기회는 없었지만, 게임 개발자로서 항상 매력적인 게임플레이를 만드는 요소를 찾고 있다고 생각합니다. 제가 300시간 이상 플레이한코랄 아일랜드보다 훨씬 더 오래 플레이한마인크래프트에 대한 애정을 아이들과 공유하지는 못하지만 ,'게임 세계에서 환상적으로 길을 잃는다는 느낌 극대화하기'라는 제목으로 주요 고려 사항을 정리해두면 도움이 될 것 같았습니다: 내러티브 디자이너의 위시리스트"라는 제목을 붙였어도 좋았을 것입니다.

캐릭터의 외형과 플레이어 이름을 커스터마이징하는 것은플레이어가 스토리 세계의 일부가 된 듯한 느낌을 주는 데 큰 도움이 됩니다.NPC가 "고마워요, 뎁!"이라고 말할 때마다 저는 "캐릭터 이름 레이블에 이름이 없었다면 기억하지 못했을 NPC, 천만에요"라고 말합니다. 플레이어가 등장방식에 대한 주도권을 가지면 게임과의 유대감이 더욱 깊어질 수 있습니다.

모든 대화의 목적이 있는지 확인하세요. 기획, 글쓰기, 선택, 에셋 제작, 애니메이션, 코딩, 로컬라이제이션에 들어가는 모든 노력에 대해 플레이어에게 건너뛸 이유를 주지 마세요! 대화 인터랙션과 컷씬을 사용하여 다음과 같이 하세요:

\- 힌트 제공

\- 스토리에 깊이 더하기

\- 플레이어가 더 긴 퀘스트를 위해 아이템을 찾거나 제작할 수 있도록 안내합니다. 이 경우, 단순한 제안이 아니라 퀘스트 목록에 추가되는 실행 가능한 아이템이 되어야 합니다.

텍스트에서 핵심 단어를 강조하면 그 중요성을 파악하는 데 도움이 될 것입니다. 미네코의 야시장은 이 기능을 정말 잘 활용하고 있습니다. 저는 종이 노트를 작성했지만, 공인 장애인 플레이어 경험 전문가인 제 자신은 이를 일종의 퀘스트 일지로 만드는 것을 추천합니다.

NPC와의 의미 있는 상호작용은 게임의 몰입감을 더욱 깊게 해줍니다. 저는 NPC와 로맨틱한 관계를 맺을 수 있는코랄 아일랜드의 Steam 버전을 플레이해 보지 않았기 때문에 이에 대해서는 말할 수 없습니다. 하지만 배우자와의 대화가 부족할 수 있다는 이야기를 간접적으로 들었기 때문에 기본 대화를 "사랑해!"로 설정하는 것이 좋습니다. 당신이 있어서 내 인생이 훨씬 더 행복해!"와 같은 대화로 설정해 보세요.

평범한 플라토닉 대화에더 깊은 주제를 파고들 수 있는 옵션을 제공하여 수집가 퀘스트와 같은 것에 연결할 수 있습니다.

예시

NPC: 안녕하세요 \[플레이어 이름 입력\]! 어떻게 지내세요?

You: 잘 지내요! 잘 지내셨나요, \[플레이할 수 없는 캐릭터 이름\]?

NPC: 더 잘할 수 있지.

당신:

옵션 1: 지금은 얘기할 시간이 없으니 나중에 얘기하자.

NPC: 그러죠.

또는

당신:

옵션 2: 왜요? 무슨 일이죠?

NPC: 오늘 아침에 엄마랑 싸웠어요. 제 잘못이에요. 단순한 사과로는 소용없다는 걸 알아요. 엄마가 좋아하는 어린 시절의 특별한 케이크를 만들어 드리려고 생각 중이에요. 그런데 어디서 펌퍼니켈로디언 스폰지밥 팬시 꽃을 구할 수 있을지 모르겠어요.

플레이어가 스토리에 기여하면서 더 많은 스토리를 전개하고 캐릭터를 발전시킬 수 있는 기회, 특히 플레이어가 스토리에 더 많이 투자한다고 느낄 때 더욱 그렇습니다.

아이템/공예 퀘스트는 단순한 심부름 이상의 의미를 제공해야 합니다.

예시:

펌프니켈로데온 스폰지밥 팬츠 퀘스트 수락: 예 / 아니오

산호섬에는아름다운 세트 데크가 있어 플레이어는 거의 모든 NPC의 멋진 가구로 꾸며진 집에 들어갈 수 있습니다. 이 시점에서는 필요하지 않은 화폐 보상을 제외하고는 요청한 아이템을 찾거나 수확하고, NPC를 추적하고, 아이템을 주고, 인정을 받은 후 다른 상호 작용이나 언급이 없는 것이 많은 노력처럼 느껴집니다.

이전 상호 작용은 향후 상호 작용에 반영됩니다.

예시:

펌퍼니켈로데온 스폰지밥팬티 꽃 퀘스트를 완료한 후, 대화에서 NPC가 여러분의 노력 덕분에 어머니와의 관계가 치유되었음을 암시하는 대화가 나옵니다.

새로운 것은 보상 본능을 자극합니다.

자세히 설명할필요는 없겠지만, 마법의 온실을 얻거나 머피족을 발견하는 것은 잠을 조금, 아니 훨씬 더 오래 자고 깨어 있을 만한가치가 있었습니다.

게임마다 수익 모델이 다르다는 것을 이해하지만, 프리미엄 다운로드 시뮬레이션 게임은 게임 플레이 시간이 한정되어 있고 개발자가 메인 스토리 라인을 넘어서는 연장할 의무가 없다는 것을 알고 있습니다. 문제는 많은 게임이 수집 퀘스트를 통해 플레이어가 지루하다고 느끼든, 아니면 그냥 쉬면서 낚시를 즐기든 간에 광범위한 게임 플레이를 제공한다는 것입니다. 하지만 곧 출시될 [헬로키티 아일랜드 어드벤처처럼](https://youtu.be/VcOeBW92ioU) 해변, 광산, 레시피, 방 꾸미기 등매우 유사한 유형의 경험을 제공하는 게임의 홍수 속에서 정서적으로 의미 있는 관계를 형성하는 것은 기억에 남는 경험을 만드는 데 큰 도움이 됩니다. 이는 적어도 속편을 출시할 때까지는 모든 스튜디오가 원하는 것입니다.

자세히 읽어보세요:

[블로그추천](https://www.gamedeveloper.com/keyword/blogs)[블로그톱](https://www.gamedeveloper.com/keyword/featured-blogs)[스토리](https://www.gamedeveloper.com/keyword/top-stories)

[](https://www.linkedin.com/sharing/share-offsite/?url=https://www.gamedeveloper.com/design/creating-compelling-and-continuous-gameplay-in-a-cozy-farming-life-sim-adventure)[](https://www.facebook.com/sharer/sharer.php?u=https://www.gamedeveloper.com/design/creating-compelling-and-continuous-gameplay-in-a-cozy-farming-life-sim-adventure)[](https://www.twitter.com/intent/tweet?url=https://www.gamedeveloper.com/design/creating-compelling-and-continuous-gameplay-in-a-cozy-farming-life-sim-adventure)[](https://www.gamedeveloper.com/cdn-cgi/l/email-protection#c2fdb1b7a0a8a7a1b6ff81b0a7a3b6abaca5e281adafb2a7aeaeabaca5e2a3aca6e281adacb6abacb7adb7b1e285a3afa7b2aea3bbe2abace2a3e281adb8bbe284a3b0afabaca5ed8eaba4a7e291abafe283a6b4a7acb6b7b0a7e4a3afb2f9a0ada6bbff8be7f0f2b6aaadb7a5aab6e7f0f2b6aaa7e7f0f2a4adaeaeadb5abaca5e7f0f2a4b0adafe7f0f285a3afa7e7f0f286a7b4a7aeadb2a7b0e7f0f2afaba5aab6e7f0f2abacb6a7b0a7b1b6e7f0f2bbadb7ece7f286e7f283e7f286e7f283e7f0f281b0a7a3b6abaca5e7f0f281adafb2a7aeaeabaca5e7f0f2a3aca6e7f0f281adacb6abacb7adb7b1e7f0f285a3afa7b2aea3bbe7f0f2abace7f0f2a3e7f0f281adb8bbe7f0f284a3b0afabaca5e7f0848eaba4a7e7f0f291abafe7f0f283a6b4a7acb6b7b0a7e7f286e7f283aab6b6b2b1e7f183e7f084e7f084b5b5b5eca5a3afa7a6a7b4a7aeadb2a7b0eca1adafe7f084a6a7b1aba5ace7f084a1b0a7a3b6abaca5efa1adafb2a7aeaeabaca5efa3aca6efa1adacb6abacb7adb7b1efa5a3afa7b2aea3bbefabacefa3efa1adb8bbefa4a3b0afabaca5efaeaba4a7efb1abafefa3a6b4a7acb6b7b0a7)[](https://www.reddit.com/submit?url=https://www.gamedeveloper.com/design/creating-compelling-and-continuous-gameplay-in-a-cozy-farming-life-sim-adventure&title=Creating%20Compelling%20and%20Continuous%20Gameplay%20in%20a%20Cozy%20Farming%2FLife%20Sim%20Adventure)

## 저자 소개

[![Deborah Chantson](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltacf0ac70802bf305/65087f540db1edff5f8461fa/Deborah_Chantson.jpg?width=400&auto=webp&quality=80&disable=upscale "Deborah Chantson")](https://www.gamedeveloper.com/author/deborah-chantson)

[

데보라 챈슨

](https://www.gamedeveloper.com/author/deborah-chantson)

Blogger

[데보라 챈슨의 더보기](https://www.gamedeveloper.com/author/deborah-chantson)

게임 개발자의 일일 뉴스, 개발자 블로그, 스토리를 받은 편지함으로 바로 받아보세요.

[최신 소식 받기](https://gd-resources.gamedeveloper.com/free/w_gamf01/prgm.cgi)

추천 콘텐츠

* * *

원문: [https://www.gamedeveloper.com/design/creating-compelling-and-continuous-gameplay-in-a-cozy-farming-life-sim-adventure](https://www.gamedeveloper.com/design/creating-compelling-and-continuous-gameplay-in-a-cozy-farming-life-sim-adventure)