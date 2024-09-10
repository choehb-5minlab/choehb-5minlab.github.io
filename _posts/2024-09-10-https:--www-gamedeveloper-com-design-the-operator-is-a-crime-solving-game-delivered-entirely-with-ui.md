---
title:  "더 오퍼레이터는 UI로만 제공되는 범죄 해결 게임입니다."

categories:
  - 번역
  
tags:
  - Game Developer
toc: true
toc_sticky: true
 
date: 2024-09-10
last_modified_at: 2024-09-10
---
[![Picture of Joel Couture](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltef4298d364a9bfa1/6508832dca23d12f34840106/Joel_Couture.jpg?width=100&auto=webp&quality=80&disable=upscale "Picture of Joel Couture")](https://www.gamedeveloper.com/author/joel-couture)

[조엘 꾸뛰르](https://www.gamedeveloper.com/author/joel-couture), 기여자

9월 10일, 2024

8분 읽기

![](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt377bfcf33b9cdc5d/66d927b2d45ddd3a83fd06e4/ss_51d780cd40f7bba5e3eee5ff98b17b917c3e2f33.jpg?width=1280&auto=webp&quality=95&format=jpg&disable=upscale)

Bureau 81 이미지 제공.

[](https://www.linkedin.com/sharing/share-offsite/?url=https://www.gamedeveloper.com/design/the-operator-is-a-crime-solving-game-delivered-entirely-with-ui)[](https://www.facebook.com/sharer/sharer.php?u=https://www.gamedeveloper.com/design/the-operator-is-a-crime-solving-game-delivered-entirely-with-ui)[](https://www.twitter.com/intent/tweet?url=https://www.gamedeveloper.com/design/the-operator-is-a-crime-solving-game-delivered-entirely-with-ui)[](https://www.gamedeveloper.com/cdn-cgi/l/email-protection#615e1214030b0402155c350904412e11041300150e134108124100410213080c0441120e0d17080f064106000c044105040d08170413040541040f150813040d18411608150941342847000c115a030e05185c2844535115090e14060915445351150904445351070e0d0d0e16080f0644535107130e0c44535126000c04445351250417040d0e1104134453510c08060915445351080f150413041215445351180e144f4451254451204451254451204453513509044453512e11041300150e134453510812445351004453510213080c04445351120e0d17080f0644535106000c0444535105040d081704130405445351040f150813040d1844535116081509445351342844512544512009151511124452204453274453271616164f06000c04050417040d0e1104134f020e0c44532705041208060f4453271509044c0e11041300150e134c08124c004c0213080c044c120e0d17080f064c06000c044c05040d0817041304054c040f150813040d184c160815094c1408)[](https://www.reddit.com/submit?url=https://www.gamedeveloper.com/design/the-operator-is-a-crime-solving-game-delivered-entirely-with-ui&title=The%20Operator%20is%20a%20crime%20solving%20game%20delivered%20entirely%20with%20UI)

[오퍼레이터](https://store.steampowered.com/app/1771980/The_Operator/) 는 플레이어가 복잡한 범죄를 해결하는 게임이지만, 플레이어가 데이터베이스를 검색하고 복잡한 소프트웨어를 사용하여 단서를 분석하여 현장 요원을 도와 범인을 검거하는 간접적인 방식으로 진행됩니다.

게임 개발자는 게임 제작자인 바스티앙 지아페리와 만나 범죄 해결에서 실험실 기술자와 분석가의 역할을 탐구하는 것의 매력, 다양한 종류의 분석 도구와 데이터베이스를 위한 다양한 인터페이스를 설계하는 사고 과정, 플레이어가 탐색하는 데 사용할 시스템을 형성하는 데 스토리 비트가 어떻게 도움이 되는지에 대해 이야기를 나눴습니다.

게임 개발자: 오퍼레이터에서는 플레이어가 현장 요원을 도와 복잡한 범죄를 조사하는 역할을 맡게 됩니다. 이 게임을 만들게 된 계기는 무엇인가요?

지아페리: 엑스파일을 10번째로 보면서 게임에 대한 아이디어를 얻었습니다 . 멀더와 스컬리가 시체에서 이상한 샘플을 발견하고 실험실 기술자에게 분석을 의뢰하는 장면이 나옵니다. 기술자가 결과를 알려주자 멀더는 충격을 받고 샘플을 어디서 찾았냐고 묻습니다. 그 순간 이 사람의 입장에서 행동하는 것이 좋았을 것 같다는 생각이 들었습니다.

플레이어가 현장의 요원이 아닌 조력자 역할을 하게 된 계기는 무엇인가요? 그것이 게임에서 범죄를 해결하는 디자인에 어떤 영향을 미쳤나요?

더 독창적이었다고 생각합니다. 제가 가진 가장 큰 제약 중 하나는 제 기술력이었습니다. 저는 미술 자체를 할 수 없기 때문에 뭔가 다른 것을 해야 했죠. 그러던 중 UI만 있는 게임을 만들자는 아이디어가 떠올랐고, 플레이어가 실제 에이전트가 아니라 조력자 역할을 하는 것이 합리적이라고 생각했습니다. 저는 제약 조건을 창의적인 도구로 사용하는 것을 정말 좋아합니다.

이 결정의 가장 큰 결과는 플레이어가 요원보다 사건에 대해 더 잘 파악하고 있기 때문에 어딘가에 음모가 있을 거라는 생각이 들었기 때문입니다. 또한 플레이어에게 직접 상황을 제시하고 일부 증거에 제한적으로 접근하여 특정 문제를 해결하도록 요청할 수 있기 때문에 더 효과적이었습니다. 기본적으로 게임이 퍼즐 게임으로 바뀌었죠.

![](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt0b6cca17c44088cf/66d93222012051c4076ac777/ss_152c464d71afa7bf2a0546cab74008d0e91b20c8.jpg?width=700&auto=webp&quality=80&disable=upscale)

Bureau 81 이미지 제공.

게임의 인터페이스에는 어떤 생각이 반영되었나요? 플레이어가 복잡한 첨단 수사 시스템을 사용하는 것처럼 느끼도록 게임의 전체적인 외관을 어떻게 디자인했나요?

제 목표는 실제 운영체제를 모방하는 것이었습니다. 저는 Windows, macOS, Linux에서 작업하기 때문에 각 운영체제에서 조금씩 차용했습니다. 인터페이스는 한 번에 한 단계씩 디자인했고, 각 부분에 대해 소프트웨어가 실제로 어떻게 작동할지 생각하려고 노력했습니다. 예를 들어, 화학 분석 소프트웨어의 경우 샘플을 저장할 수 있는 장소와 이 샘플을 가져와서 샘플에 따라 설정을 입력해야 하는 매우 정교한 기계에 넣는 자동화 시스템이 FDI 어딘가에 있는 것이 합리적일 것 같았습니다. 이렇게 하면 게임플레이와 스토리를 모두 구현할 수 있었습니다. 몰입감이 이 게임의 핵심 요소 중 하나였기 때문에 인터페이스와 소프트웨어를 최대한 신뢰할 수 있게 만들려고 노력했습니다.

플레이어가 게임에서 사용할 분석 시스템은 어떻게 선택하셨나요? 어떤 아이디어를 바탕으로 설계했으며, 어떻게 하면 증거 확인을 더 재미있게 만들 수 있을까요?

각 시퀀스에 대한 아이디어를 바탕으로 시스템을 선택했습니다. 대부분의 경우 특정 시퀀스에 대한 아이디어는 스토리 목표에 기반한 것이었고, 이전 시퀀스와는 달라야 했습니다. 같은 시스템을 같은 방식으로 두 번 사용하고 싶지 않았어요.

예를 들어 앤드루스 요원을 다룬 첫 번째 시퀀스의 경우, 제 스토리 목표는 FDI가 정보를 검열하고 있다는 것을 보여주는 것이었고, HAL과 앤드루스 요원이 처음으로 함께 작업하는 것이었죠. 이 시퀀스의 유일한 목표는 사건을 재개하기 위해 미아 콜의 목숨을 앗아간 우발적인 화재가 사고가 아니라는 것을 증명하는 것이었습니다. 이를 염두에 두고 화재가 사고가 아니라는 것을 증명할 방법을 찾았습니다. 제가 생각해낸 최선의 아이디어는 재 샘플을 분석하여 휘발유가 화재를 일으키는 데 사용되었다는 것을 알아내는 것이었습니다(사고는 아니었지만...). 그런 다음 그 사용 사례를 위해 화학 분석기를 만들었습니다.

플레이어에게 사건 진행 방법에 대한 선택지를 너무 많이 주지 않으면서도 흥미를 유발하는 시스템을 만드는 데 어떤 어려움이 있었나요?

저는 모든 사람이 게임에 접근할 수 있도록 하고 싶었습니다. 복잡한 지식이 필요한 게임플레이는 포함하고 싶지 않았어요. 폭탄 해체처럼 일부러 어렵고 압도적인 요소도 있지만 스토리에 도움이 됩니다. 폭탄의 경우 무력감을 느끼게 하는 것이 목표였습니다. 첫 날이고, 그곳에 있는 것도 아니기 때문에 적절한 지식 없이는 폭탄 해체가 당연히 어렵습니다!

게임을 다듬을 때 제 자신의 한계를 극복하는 것이 가장 힘들었던 것 같아요. 제가 가진 아이디어 중 상당수는 다듬기에는 너무 복잡했어요. 그래서 저는 먼저 필수적인 증거에 집중했습니다. 시퀀스가 너무 쉽거나 너무 뻔하면 증거를 약간 난해하게 만들거나 만들기 쉬운 증거를 추가해 중요한 부분을 숨겼습니다. 플레이어에게 정보가 어떻게 표시되느냐에 따라 핵심 정보를 숨기거나 더 분명하게 만들 수 있습니다.

![ss_8680804522ae426afb2df3c75ae928a1d03a7e26.jpg](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt99848fb20a6c28d7/66d932672664e4bd16ff7a80/ss_8680804522ae426afb2df3c75ae928a1d03a7e26.jpg?width=700&auto=webp&quality=80&disable=upscale "ss_8680804522ae426afb2df3c75ae928a1d03a7e26.jpg")

Bureau 81 이미지 제공.

게임에서 플레이어에게 제공하는 증거를 만들 때 어떤 어려움에 직면하나요? 플레이어에게 너무 많은 정보를 주지 않으면서도 추리할 수 있는 충분한 단서를 제공하려면 어떻게 해야 하나요?

솔직히 말해서 제가 직면한 가장 큰 도전은 제 자신의 연마 능력이었습니다. 다듬기가 너무 어려워서 '맛'을 내는 증거를 많이 잘라내야 했죠. 제가 오퍼레이터를개발하기 시작했을 때 인공지능은 이제 막 훌륭한 결과를 얻기 시작했을 때였어요. 저 같은 소규모 크리에이터에게는 정말 훌륭한 도구였고, 훨씬 더 많은 것을 할 수 있게 해줬죠. 하지만 개발이 진행되면서 AI에 대한 윤리적 우려(특히 AI 학습에 사용되는 데이터에 대한 우려)가 커지자 저는 AI가 생성한 콘텐츠를 완전히 제거하기로 결정했습니다. 그러나 적절한 예산 없이는 대체할 수 없는 일부 증거(예를 들어 불에 탄 아파트 사진 등)는 삭제해야 했습니다.

'단서 분배'의 경우, 각 시퀀스에서 플레이어가 무엇을 알고 무엇을 이해하길 원하는지 정확히 알고 있었기 때문에 해당 시퀀스에 대한 게임플레이나 퍼즐을 찾으면 거기에 어떤 증거를 넣을지 결정했습니다. 플레이어가 무엇을 이해했는지에 대해서는 많은 플레이 테스트를 거쳤습니다!

![Screenshot 2024-09-04 203100.png](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt895d99cfc82aad52/66d927642bad5e7d35d07bdd/Screenshot_2024-09-04_203100.png?width=700&auto=webp&quality=80&disable=upscale "Screenshot 2024-09-04 203100.png")

Bureau 81 이미지 제공.

게임의 케이스 디자인 과정을 구체적인 예를 들어 설명해 주시겠어요? 콘셉트를 어떻게 떠올렸는지, 내러티브의 순간과 증거를 통해 스토리를 어떻게 전달할지 처음부터 끝까지 설명해 주세요.

저는 제가 염두에 두고 있던 플롯 반전과 만들고 싶었던 시퀀스 아이디어로 시작했습니다. 예를 들어, 요원이 전화로 폭탄 해체를 돕는 시퀀스를 만들고 싶었습니다(영화 '계속 말해도 아무도 폭발하지 않는다'와비슷하죠 ). 그런 다음 이러한 시퀀스 아이디어와 반전을 결합하여 스토리와 캐릭터를 만들었습니다.

예를 들어 증거 보관실 시퀀스에서는 이전 사건에서 숨겨진 증거를 찾는 것이 스토리의 목표였습니다. 이 증거에 접근하기 위해 FDI의 증거실에 침입해야 했기 때문에 완전히 새로운 인터페이스를 만들 수 있는 좋은 기회였습니다. 저는 MSDOS에서 영감을 받은 UI를 사용하기로 결정했습니다. 게임플레이 측면에서는 기본 UI에서 최대한 벗어나는 것이 목표였기 때문에 키보드 전용 내비게이션을 사용하기로 결정했습니다.

숙련된 플레이어에게는 쉽지만, 익숙하지 않은 플레이어에게는 첫 번째 도전 과제입니다. 사용 가능한 모든 키가 창 아래에 표시되므로 이런 인터페이스에 익숙하지 않더라도 약간의 시행착오를 거쳐 작동 방식을 이해할 수 있습니다. 또한 이 인터페이스는 고도로 기술적인 것이어서 원하는 것을 찾기가 더 어렵습니다.

조사 시스템 자체에도 중요한 스토리가 담겨 있습니다. 플레이어가 '비밀' 요소를 찾는 데 있어 영리하다고 느낄 수 있도록 분석 시스템에 어떻게 스토리를 엮어냈는지 설명해 주시겠어요?

사실 그 반대라고 생각합니다. 저는 시스템을 스토리에 녹여냈습니다. 스토리가 먼저 짜여져 있었기 때문에 무엇을 어디에 숨길 수 있는지 정확히 알고 있었기 때문에 중요하지 않은 요소처럼 보일 수 있었죠. 일부 플레이어는 이러한 디테일을 눈치채고 예상보다 빨리 줄거리의 반전을 알아챘을 수도 있지만, 괜찮습니다. 예를 들어 (스포일러) 게임 초반 어느 시점에 마이크(마이크는 '친구'가 아닌 '플레이어'입니다)에게 아내에 대해 물어보면 마이크는 사실인 것처럼 말하지만 이 시점에서 데이터베이스를 확인하면 아내가 없다는 것을 알 수 있습니다. 아무도 눈치채지 못하는 숨겨진 세부 사항이지만, 알아차린다면 정말 똑똑하다고 느낄 것입니다.

자세히 읽어보세요:

[Q&A인터뷰딥](https://www.gamedeveloper.com/keyword/interviews)[다이브톱](https://www.gamedeveloper.com/keyword/deep-dives)[스토리기능](https://www.gamedeveloper.com/keyword/features)

[](https://www.linkedin.com/sharing/share-offsite/?url=https://www.gamedeveloper.com/design/the-operator-is-a-crime-solving-game-delivered-entirely-with-ui)[](https://www.facebook.com/sharer/sharer.php?u=https://www.gamedeveloper.com/design/the-operator-is-a-crime-solving-game-delivered-entirely-with-ui)[](https://www.twitter.com/intent/tweet?url=https://www.gamedeveloper.com/design/the-operator-is-a-crime-solving-game-delivered-entirely-with-ui)[](https://www.gamedeveloper.com/cdn-cgi/l/email-protection#7c430f091e16191f08412814195c330c190e1d08130e5c150f5c1d5c1f0e1511195c0f13100a15121b5c1b1d11195c181910150a190e19185c191208150e1910055c0b1508145c29355a1d110c471e1318054135594e4c081413091b1408594e4c081419594e4c1a131010130b15121b594e4c1a0e1311594e4c3b1d1119594e4c38190a1910130c190e594e4c11151b1408594e4c151208190e190f08594e4c05130952594c38594c3d594c38594c3d594e4c281419594e4c330c190e1d08130e594e4c150f594e4c1d594e4c1f0e151119594e4c0f13100a15121b594e4c1b1d1119594e4c181910150a190e1918594e4c191208150e191005594e4c0b150814594e4c2935594c38594c3d1408080c0f594f3d594e3a594e3a0b0b0b521b1d111918190a1910130c190e521f1311594e3a18190f151b12594e3a08141951130c190e1d08130e51150f511d511f0e151119510f13100a15121b511b1d111951181910150a190e191851191208150e191005510b150814510915)[](https://www.reddit.com/submit?url=https://www.gamedeveloper.com/design/the-operator-is-a-crime-solving-game-delivered-entirely-with-ui&title=The%20Operator%20is%20a%20crime%20solving%20game%20delivered%20entirely%20with%20UI)

## 저자 소개

[![Joel Couture](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltef4298d364a9bfa1/6508832dca23d12f34840106/Joel_Couture.jpg?width=400&auto=webp&quality=80&disable=upscale "Joel Couture")](https://www.gamedeveloper.com/author/joel-couture)

[

조엘 쿠튀르

](https://www.gamedeveloper.com/author/joel-couture)

기여자

[Joel Couture의 더보기](https://www.gamedeveloper.com/author/joel-couture)

게임 개발자의 일일 뉴스, 개발자 블로그, 스토리를 받은 편지함으로 바로 받아보세요.

[최신 소식 받기](https://gd-resources.gamedeveloper.com/free/w_gamf01/prgm.cgi)

추천 콘텐츠

* * *

원문: [https://www.gamedeveloper.com/design/the-operator-is-a-crime-solving-game-delivered-entirely-with-ui](https://www.gamedeveloper.com/design/the-operator-is-a-crime-solving-game-delivered-entirely-with-ui)