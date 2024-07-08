---
title:  "스타일과 사용자 편의성을 갖춘 워 로봇의 상금 시스템 재구성"

categories:
  - 번역
  
tags:
  - Game Developer
toc: true
toc_sticky: true
 
date: 2024-07-08
last_modified_at: 2024-07-08
---
[![Picture of Nikolay Berezkin](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltd709c2f6ad0896cd/657b3aae1fb1b4040a0e1821/Game_Developer_G_Logo_RGB.png?width=100&auto=webp&quality=80&disable=upscale "Picture of Nikolay Berezkin")](https://www.gamedeveloper.com/author/nikolay-berezkin)

[니콜라이 베레즈킨](https://www.gamedeveloper.com/author/nikolay-berezkin)

7월 8일, 2024

9 분 읽기

![](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltb269b334c1a971a0/66853518b6a60de0f3c23d21/Pic_1.jpg?width=850&auto=webp&quality=95&format=jpg&disable=upscale)

[](https://www.linkedin.com/sharing/share-offsite/?url=https://www.gamedeveloper.com/design/reworking-war-robots-prize-system-with-style-and-user-friendliness)[](https://www.facebook.com/sharer/sharer.php?u=https://www.gamedeveloper.com/design/reworking-war-robots-prize-system-with-style-and-user-friendliness)[](https://www.twitter.com/intent/tweet?url=https://www.gamedeveloper.com/design/reworking-war-robots-prize-system-with-style-and-user-friendliness)[](https://www.gamedeveloper.com/cdn-cgi/l/email-protection#93ace0e6f1f9f6f0e7aec1f6e4fce1f8fafdf4b3c4f2e1b3c1fcf1fce7e0b5b0eba1a4a8b3e3e1fae9f6b3e0eae0e7f6feb3e4fae7fbb3e0e7eafff6b3f2fdf7b3e6e0f6e1bef5e1faf6fdf7fffafdf6e0e0b5f2fee3a8f1fcf7eaaedab6a1a3e7fbfce6f4fbe7b6a1a3e7fbf6b6a1a3f5fcfffffce4fafdf4b6a1a3f5e1fcfeb6a1a3d4f2fef6b6a1a3d7f6e5f6fffce3f6e1b6a1a3fefaf4fbe7b6a1a3fafde7f6e1f6e0e7b6a1a3eafce6bdb6a3d7b6a3d2b6a3d7b6a3d2b6a1a3c1f6e4fce1f8fafdf4b6a1a3c4f2e1b6a1a3c1fcf1fce7e0b5b0eba1a4a8b6a1a3e3e1fae9f6b6a1a3e0eae0e7f6feb6a1a3e4fae7fbb6a1a3e0e7eafff6b6a1a3f2fdf7b6a1a3e6e0f6e1bef5e1faf6fdf7fffafdf6e0e0b6a3d7b6a3d2fbe7e7e3e0b6a0d2b6a1d5b6a1d5e4e4e4bdf4f2fef6f7f6e5f6fffce3f6e1bdf0fcfeb6a1d5f7f6e0faf4fdb6a1d5e1f6e4fce1f8fafdf4bee4f2e1bee1fcf1fce7e0bee3e1fae9f6bee0eae0e7f6febee4fae7fbbee0e7eafff6bef2fdf7bee6e0f6e1bef5e1faf6fdf7fffafdf6e0e0)[](https://www.reddit.com/submit?url=https://www.gamedeveloper.com/design/reworking-war-robots-prize-system-with-style-and-user-friendliness&title=Reworking%20War%20Robots'%20prize%20system%20with%20style%20and%20user-friendliness)

새로운 게임 기능을 구현하는 것은 콘텐츠 레이어를 추가하든, 핵심 메커니즘을 수정하든, 인터페이스를 재작업하든, 삶의 질을 변경하든 상관없이 계획에서 시작됩니다. 성공적인 기획은 명확한 목표에서 시작됩니다. 그리고 저희의 목표는 워 로봇의 이벤트 상금 시스템을 완전히 개편하는 야심찬 목표였습니다.

안녕하세요! 저는 워 로봇의 수석 게임 디자이너인 니콜라이 베레즈킨이고, 픽소닉(MY.GAMES)의 리드 2D 아티스트인 안톤 트로피모프와 함께합니다. 오늘은 워 로봇의 새로운 콘텐츠 시스템인 데이터 패드가 어떻게 탄생하게 되었는지 여러분과 함께 이야기를 나누게 되어 기쁩니다.

## 상금 시스템을 개편한 이유는 무엇인가요?

데이터 패드는 수년 동안 거의 변하지 않았던 낡은 이벤트 상금 시스템을 혁신하고자 하는 열망에서 탄생했습니다. 플레이어가 이벤트 상품을 경험하는 방식을 혁신하여 시각적으로 더 매력적이고 사용자 친화적으로 만들고 싶었습니다.

또한, 모든 플레이어가 가치 있는 상품을 받을 수 있도록 이벤트 기간 동안 제공 범위를 확대하고 제작 비용과 시각적 업데이트 빈도를 줄이고자 했습니다.

또한 상품을 받는 과정에 내러티브 요소를 도입하여 작은 '컨테이너'에 거대한 로봇과 우주선을 담을 수 있는 이유를 암시하는 것도 중요했습니다. 게임의 10년 역사와 수많은 레거시 시스템을 고려할 때 이는 결코 쉬운 일이 아니었습니다.

## 외관의 변화

개편의 첫 번째 단계는 구식 비주얼을 버리고 현대적이고 보편적이며 읽기 쉬운 비주얼로 바꾸는 것이었습니다. '데이터 패드'라는 이름 자체가 미래의 태블릿과 같은 미래형 저장 매체인 카드형 디자인을 암시했기 때문에 폼 팩터를 결정하는 것은 쉬운 일이 아니었습니다.

처음에 저희는 각 데이터 패드에 3D 사진이나 렌더링된 메인 상품을 표시하는 것을 구상했습니다. 하지만 이 아이디어를 다시 검토한 결과, 렌더링은 개발 비용이 많이 들고 이점이 제한적이기 때문에 결국 포기하기로 결정했습니다. 이러한 변경에도 불구하고 플레이어는 데이터 패드를 열었을 때 영리한 디자인 컨셉과 매력적인 시각 효과 덕분에 가장 가치 있고 바람직한 보상이 들어 있는 데이터 패드를 쉽게 식별할 수 있습니다. 각 데이터 패드는 데이터 패드의 품질을 나타내는 은색 또는 황금색 테두리와 경품 팩의 내용에 해당하는 파란색, 보라색, 빨간색 등 데이터 패드 자체의 색상으로 구분됩니다.

또 다른 주요 목표 중 하나는 이벤트마다 비주얼을 업데이트하는 주기에서 벗어나는 것이었습니다. 플레이어가 일관된 데이터 패드 디자인에 익숙해지고 다른 요소와의 혼동을 없애고 싶었습니다. 이를 위해 데이터 패드의 핵심 디자인을 변경하지 않고 새로운 느낌을 더하는 이벤트별 업데이트인 '카드 뒷면'을 도입했습니다.

데이터 패드가 등장한 첫 번째 이벤트는 비스트 나이츠를 테마로 진행되었습니다. 이에 걸맞게 늑대, 사자, 곰 등 동물 문장을 카드 뒷면으로 선택했습니다. 플레이어는 데이터 패드를 살펴봄으로써 문장에 따라 일반 버전과 프리미엄(골드) 버전 모두에서 기대할 수 있는 보상을 유추할 수 있었습니다.

![Pic_2.jpg](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltff2bc8bbd9545cb7/66853523792bbe1fb39dc682/Pic_2.jpg?width=700&auto=webp&quality=80&disable=upscale "Pic_2.jpg")

일반 데이터 패드와 황금 데이터 패드의 예시. 후자는 직접 구매할 수 없으며 리더보드 경쟁과 같은 게임 내 활동을 통해서만 획득할 수 있습니다.

## 사용자가 데이터 패드를 여는 방법 간소화

다음 미니 과제는 데이터 패드를 여는 새로운 기능을 개발하기 위해 부서 간의 원활한 협업을 촉진하는 것이었습니다. 시각적 요소에 크게 의존하는 대규모 기능을 작업할 수 있는 흔치 않은 기회였습니다. 하지만 게임의 연식으로 인해 클라이언트 개발과 아트에 몇 가지 제약이 있었기 때문에 신중하게 고려해야 했습니다.

이러한 장애물을 극복하기 위해 전체 경품 응모 워크플로를 개선해야 했습니다. 이벤트 HUD, 시네마틱, 경품 공개, 다시 HUD로 돌아가기 등 몇 가지 주요 단계로 기능을 세분화했습니다. 각 단계마다 다양한 전문가의 전문 지식이 필요했습니다. 한편, 프로듀서와 게임 디자이너는 기능의 전반적인 비전을 감독하여 개발 프로세스 전반에 걸쳐 팀 전체가 일치된 의견을 낼 수 있도록 했습니다.

![Pic_3.png](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt8c9777b1e092f910/6685356d7141a09a633847c1/Pic_3.png?width=700&auto=webp&quality=80&disable=upscale "Pic_3.png")

우리는 메인 화면 탐색을 시뮬레이션하는 작은 UI 프로토타입으로 시작했습니다. 동시에 데이터 패드가 열렸을 때 게임 엔진에서 재생되는 짧은 동영상인 시네마틱 작업을 시작했습니다.

이 단계에서 몇 가지 중요한 측면을 명확히 해야 했습니다. 데이터 패드의 모양에 대한 대략적인 아이디어는 있었지만, 이를 플레이어에게 어떻게 보여줄 수 있을까요? 한 회의 중에 한 가지 아이디어가 떠올랐습니다: "텔레포트 빔과 FX를 사용하여 하늘에서 떨어뜨리고, 플레이어가 보상을 받으면 펑!"이라는 아이디어가 나왔습니다. 구현된 최종 버전도 이 콘셉트와 크게 다르지 않습니다. 저희는 이 기능에 플레이어의 기대감을 불러일으키고 보상에 대한 빌드업이 필요하다는 것을 알고 있었습니다.

![Pic_4.jpg](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt4343b468b5051030/66853587b6a60d13cac23d25/Pic_4.jpg?width=700&auto=webp&quality=80&disable=upscale "Pic_4.jpg")

플레이어가 보상을 어떻게 받을지, 어디에 나타날지, 어떻게 구체화할지 브레인스토밍하는 데 많은 시간을 보냈습니다. 수많은 실험 끝에 '천상의 쾅' 콘셉트는 복도를 지나 방으로 날아가는 카메라가 갑자기 빛의 섬광과 함께 보상이 나타나는 것으로 발전했습니다.

![GIF.gif](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt60074b72db3287b6/66853595b6a60d19a7c23d2a/GIF.gif?width=665&auto=webp&quality=80&disable=upscale "GIF.gif")

두 번째 중요한 질문: 데이터 패드는 정확히 무엇일까요? 데이터 패드는 정보를 전달하는 매개체이지만 게임에서는 실제로 거대한 로봇과 총이 들어 있습니다. 저희는 이 장치의 사실성과 게임의 논리적 세계를 위반하지 않는 방법에 대해 고민했습니다. 이를 해결하기 위해 새로운 개념을 생각해냈습니다: 데이터 패드에는 게임 내 화폐, 로봇, 기타 콘텐츠 등 플레이어가 획득한 상품의 위치를 가리키는 좌표와 같은 암호화된 정보가 들어 있습니다.

![Pic_5.jpg](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltfe9dd673039b7f18/668535b56b429c42808ac6c7/Pic_5.jpg?width=700&auto=webp&quality=80&disable=upscale "Pic_5.jpg")

플레이어 사령관은 우주선에 있는 디코더 키를 사용하여 코드를 해독하면 좌표가 즉시 화면에 표시됩니다. 이 아이디어가 개발의 토대가 되었습니다.

데이터 패드 카드와 상품 사이의 연관성을 보여주기 위해 스포트라이트 받침대 콘셉트를 도입했습니다. 데이터 패드가 먼저 받침대에서 공개되고 '해독'된 다음, 시네마틱이 끝날 때 비슷한 받침대에서 상품 자체가 구체화됩니다.

![Pic_6.png](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt1c48281650730019/668535bf792bbe4bcb9dc687/Pic_6.png?width=700&auto=webp&quality=80&disable=upscale "Pic_6.png")

최종 버전에서는 이 받침대 콘셉트가 원하는 만큼 명확하게 드러나지 않았고, 화면마다 받침대의 가시성이 달라서 구도를 방해할까 봐 카드의 높이를 높이고 싶지 않았기 때문입니다. 현재는 디자인을 더욱 멋지게 만들기 위해 미세 조정하는 방법을 모색하고 있습니다.

## UI 개편

또한 플레이어가 어떤 상품을 받을 수 있는지 명확하게 파악할 수 있도록 하는 데 중점을 두었습니다. 이전에는 전리품 상자에 칙칙하고 오래된 상품 목록이 표시되어 사용자 편의성과는 거리가 멀었습니다. 기능적으로도 플레이어가 가능한 보상을 보기 위해 스크롤을 내려야 하는 긴 카드 회전 목마가 있었고, 상품이 아무렇게나 배치되어 있는 것처럼 보였습니다.

![Pic_7.png](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltb58cd2b12b0d6f1c/668535df0226d963e5a4cfd4/Pic_7.png?width=700&auto=webp&quality=80&disable=upscale "Pic_7.png")

이제 UI를 업데이트하고 새로운 생명을 불어넣어 플레이어가 상품의 가치를 더 잘 확인하고, 상품을 더 쉽게 분류하고, 관심 있는 상품을 선택할 수 있게 되었습니다.

![Pic_8.png](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltf5784f863f134644/668535fd5d116533e01f32ca/Pic_8.png?width=700&auto=webp&quality=80&disable=upscale "Pic_8.png")

또한 시스템의 메커니즘도 전면적으로 개편했습니다. 기존 시스템은 정해진 수의 이벤트 코인을 사용해 상자를 열 수 있는 정적인 화면으로 구성되었으며, 플레이어는 간단한 탭으로 한 번에 하나 또는 열 개의 상자를 열 수 있었습니다.

실험을 통해 3개의 상자, 3개의 화폐 시스템을 결정했습니다. 각 상자와 화폐는 각기 다른 시각적 특징을 가지고 있어 진행에 대한 느낌을 주며, 이를 강화하기 위해 다양한 보상이 포함되어 있습니다. 상자를 여는 데 사용되는 코인은 게임 내 퀘스트, 혜택 등 다양한 수익화 기능에도 활용되었습니다.

또한 기존 인터페이스는 플레이어에게 코인을 통해 얻을 수 있는 잠재적 보상에 대한 정보를 제공하지 않는다는 한 가지 중요한 측면이 부족했습니다. 플레이어는 해당 정보를 얻기 위해 별도의 화면으로 이동하여 자신의 코인에 해당하는 상자를 검색하는 데 시간을 낭비해야 했습니다.

기존 시스템에서는 플레이어가 무슨 일이 일어나고 있는지 이해하기 어려운 문제가 많았는데, 코인과 상자가 혼란스러울 정도로 비슷하거나 크게 달라서 플레이어의 불만과 혼란을 초래하는 경우가 많았습니다.

이번 개편을 통해 이러한 문제를 정면으로 해결했습니다. 우선, 이제 데이터 패드를 잠금 해제하는 열쇠 대신 데이터 패드를 직접 제공합니다. 이렇게 하면 플레이어가 불필요한 정보를 추적할 필요가 없어지고 어떤 코인이 어떤 상자에 해당하는지 혼동할 필요가 없어집니다. 또한 이러한 변경으로 제작 파이프라인이 최적화되어 아트 팀이 이벤트 화폐 형태의 중간 링크를 만들 필요 없이 단일 엔티티에 집중할 수 있게 되었습니다.

둘째, 이제 각 데이터 패드에는 정보 창을 열어 잠재적인 상품을 표시하는 버튼이 있습니다. 이제 플레이어는 어떤 데이터 패드에 더 원하는 보상이 들어 있는지 쉽게 확인할 수 있으므로 구매 절차가 간소화됩니다. 이 버튼은 배틀패스, 순위표, 혜택 등 데이터 패드를 획득할 수 있는 모든 지점에서 편리하게 사용할 수 있습니다.

![Pic_9.png](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt45a9324e7c4d4132/668536120c2c2755534b9f8f/Pic_9.png?width=700&auto=webp&quality=80&disable=upscale "Pic_9.png")

셋째, 이벤트 인터페이스가 대폭 개편되었습니다. 더 이상 플레이어가 접근할 수 없는 데이터 패드가 표시되지 않습니다. 화면에 3개의 상자가 고정적으로 표시되던 것과 달리 데이터 패드가 없을 수도 있으며, 플레이어가 한 가지 유형의 데이터 패드만 가지고 있는 경우 해당 데이터 패드와만 상호작용할 수 있습니다.

\*\*\*

저희의 여정은 아직 끝나지 않았습니다. 저희는 모든 작업을 통해 계속해서 기능을 개선해나가고 있으며, 데이터 패드도 예외는 아닙니다.

모든 것이 순조롭게 진행된 것은 아니지만, 경험을 통해 많은 것을 배웠습니다. 마지막 예로, 받침대를 통해 화면을 연결하려는 아이디어는 계획대로 진행되지 않았습니다.

또한 첫 번째 데이터 패드 사이의 값의 가독성을 개선해야 했는데, 이는 다음 이벤트에서 해결되었습니다. 또한 데이터 패드의 희귀도에 대한 플레이어의 인식에 큰 영향을 미치는 폴리싱 효과도 개선했습니다.

![Pic_10.jpg](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt102547e9d5748571/66853623fb5061e33478f458/Pic_10.jpg?width=700&auto=webp&quality=80&disable=upscale "Pic_10.jpg")

가장 중요한 것은 이 기능이 플레이어의 공감을 불러일으키고 이벤트에 대한 관심 감소 추세를 반전시켜 폭발적인 '와우' 효과를 창출한다는 1차 목표를 달성했다는 점입니다. 수집한 지표를 통해 이러한 기능에서 다양한 선택지를 제공하는 것이 중요하다는 것을 확인할 수 있었습니다. 끝으로, 데이터 패드로 뛰어난 성과를 거둔 모든 팀원들에게 감사의 말씀을 전하고 싶습니다!

자세히 읽어보세요:

[추천](https://www.gamedeveloper.com/keyword/featured-blogs)[블로그블로그톱](https://www.gamedeveloper.com/keyword/blogs)[스토리](https://www.gamedeveloper.com/keyword/top-stories)

[](https://www.linkedin.com/sharing/share-offsite/?url=https://www.gamedeveloper.com/design/reworking-war-robots-prize-system-with-style-and-user-friendliness)[](https://www.facebook.com/sharer/sharer.php?u=https://www.gamedeveloper.com/design/reworking-war-robots-prize-system-with-style-and-user-friendliness)[](https://www.twitter.com/intent/tweet?url=https://www.gamedeveloper.com/design/reworking-war-robots-prize-system-with-style-and-user-friendliness)[](https://www.gamedeveloper.com/cdn-cgi/l/email-protection#221d515740484741561f7047554d50494b4c450275435002704d404d565104015a1015190252504b584702515b5156474f02554b564a0251565b4e4702434c4602575147500f44504b474c464e4b4c47515104434f5219404d465b1f6b071012564a4d57454a56071012564a47071012444d4e4e4d554b4c4507101244504d4f07101265434f47071012664754474e4d5247500710124f4b454a560710124b4c5647504751560710125b4d570c0712660712630712660712630710127047554d50494b4c45071012754350071012704d404d565104015a10151907101252504b5847071012515b5156474f071012554b564a07101251565b4e47071012434c46071012575147500f44504b474c464e4b4c4751510712660712634a565652510711630710640710645555550c45434f47464754474e4d5247500c414d4f0710644647514b454c0710645047554d50494b4c450f5543500f504d404d56510f52504b58470f515b5156474f0f554b564a0f51565b4e470f434c460f575147500f44504b474c464e4b4c475151)[](https://www.reddit.com/submit?url=https://www.gamedeveloper.com/design/reworking-war-robots-prize-system-with-style-and-user-friendliness&title=Reworking%20War%20Robots'%20prize%20system%20with%20style%20and%20user-friendliness)

## 저자 소개

[![Nikolay Berezkin](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltd709c2f6ad0896cd/657b3aae1fb1b4040a0e1821/Game_Developer_G_Logo_RGB.png?width=400&auto=webp&quality=80&disable=upscale "Nikolay Berezkin")](https://www.gamedeveloper.com/author/nikolay-berezkin)

[

니콜라이 베레즈킨

](https://www.gamedeveloper.com/author/nikolay-berezkin)

[Nikolay Berezkin에서 더 보기](https://www.gamedeveloper.com/author/nikolay-berezkin)

게임 개발자의 일일 뉴스, 개발자 블로그, 이야기를 받은 편지함으로 바로 받아보세요.

[최신 소식 받기](https://gd-resources.gamedeveloper.com/free/w_gamf01/prgm.cgi)

추천 콘텐츠

* * *

원문: [https://www.gamedeveloper.com/design/reworking-war-robots-prize-system-with-style-and-user-friendliness](https://www.gamedeveloper.com/design/reworking-war-robots-prize-system-with-style-and-user-friendliness)