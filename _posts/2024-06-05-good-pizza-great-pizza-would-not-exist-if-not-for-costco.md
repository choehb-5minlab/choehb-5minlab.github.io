---
title:  "코스트코가 없었다면 좋은 피자, 위대한 피자는 존재하지 않았을 것입니다."

categories:
  - 번역
  
tags:
  - Game Developer
toc: true
toc_sticky: true
 
date: 2024-06-05
last_modified_at: 2024-06-05
---
[![Picture of Joel Couture](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltef4298d364a9bfa1/6508832dca23d12f34840106/Joel_Couture.jpg?width=100&auto=webp&quality=80&disable=upscale "Picture of Joel Couture")](https://www.gamedeveloper.com/author/joel-couture)

[조엘 꾸뛰르](https://www.gamedeveloper.com/author/joel-couture), 기여자

6월 5일, 2024

8분 읽기

![](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltdac6e73dc7ad0ec6/663d196bc81985be39310e64/ss_bc55e35f82ab00f2d57a945a18d53cd198415066.jpg?width=850&auto=webp&quality=95&format=jpg&disable=upscale)

TapBlaze 이미지 제공.

[](https://www.linkedin.com/sharing/share-offsite/?url=https://www.gamedeveloper.com/design/good-pizza-great-pizza-would-not-exist-if-not-for-costco)[](https://www.facebook.com/sharer/sharer.php?u=https://www.gamedeveloper.com/design/good-pizza-great-pizza-would-not-exist-if-not-for-costco)[](https://www.twitter.com/intent/tweet?url=https://www.gamedeveloper.com/design/good-pizza-great-pizza-would-not-exist-if-not-for-costco)[](https://www.gamedeveloper.com/cdn-cgi/l/email-protection#506f2325323a3533246d173f3f347000392a2a317c7017223531247000392a2a3170273f253c34703e3f24703528392324703936703e3f2470363f2270133f2324333f76313d206b323f34296d1975626024383f25373824756260243835756260363f3c3c3f27393e3775626036223f3d75626017313d35756260143526353c3f2035227562603d39373824756260393e243522352324756260293f257e756014756011756014756011756260173f3f3475626000392a2a31756213756260172235312475626000392a2a31756260273f253c347562603e3f24756260352839232475626039367562603e3f24756260363f22756260133f2324333f75601475601138242420237563117562167562162727277e37313d35343526353c3f2035227e333f3d75621634352339373e756216373f3f347d20392a2a317d37223531247d20392a2a317d273f253c347d3e3f247d35283923247d39367d3e3f247d363f227d333f2324333f)[](https://www.reddit.com/submit?url=https://www.gamedeveloper.com/design/good-pizza-great-pizza-would-not-exist-if-not-for-costco&title=Good%20Pizza%2C%20Great%20Pizza%20would%20not%20exist%20if%20not%20for%20Costco)

굿 피자, 그레이트 피자에서는 플레이어가 직접 피자 가게 문을 열고 들어오는 수많은 고객을 위해 맛있어 보이는 파이를 요리하는 과정을 직접 체험할 수 있습니다.

게임 개발자는 탭블레이즈 팀과 함께 플레이어에게 피자 만들기를 통해 자신을 표현할 수 있는 능력을 부여하는 방법, 요리와 상점 기능을 만드는 데 도움이 된 실제 경험과 추억, 플레이어가 접할 수 있는 백만 가지 이상의 피자 주문을 만들 수 있는 시스템을 설계한 방법에 대해 이야기를 나눴습니다.

굿 피자, 그레이트 피자에서는 플레이어가 고객에게 피자를 서빙하는 모습을 볼 수 있습니다. 나만의 피자 가게를 운영하는 게임을 만들게 된 계기는 무엇인가요?

조유니, 커뮤니티 마케팅 매니저: 저희의 CEO인 앤서니 라이는 다양한 문화와 계층의 사람들이 피자를 보편적인 음식으로 먹고 즐기는 뉴욕 퀸즈에서 자랐습니다. 어린 시절 가장 좋았던 기억 중 하나는 동네에 있는 아케이드 가게에 가서 조각 피자를 먹었던 것이었는데, 이것이 나중에 Good Pizza, Great Pizza의 일반적인 "구멍가게" 동네 피자집 분위기에 영감을 주었습니다.

저희는 피자를 만드는 관점에서 전 세계로 뻗어나갈 수 있는 다양한 게임을 만들고 싶다는 영감을 얻었습니다. 마이 피자 숍과 마이 피자 숍 2를 반복한 끝에 마침내굿 피자, 그레이트 피자가 탄생했습니다. 스토리 중심의 캐주얼 게임과 기술적인 비즈니스 시뮬레이터, 창의적인 피자 만들기 메커니즘이 결합된 독특한 구조의 게임입니다.

실제 피자 제작을 중심으로 게임플레이를 디자인할 때 어떤 생각을 하셨나요? 음식을 만드는 체험형 플레이 스타일을 만들면서 어떤 점이 매력적으로 다가왔나요? 이 체험형 플레이가 경험에 어떤 점을 더한다고 생각하시나요?

앤서니 라이, 탭블레이즈의 CEO 겸 설립자: 초기 팀은 처음부터 피자를 좋아했습니다. 원래 아티스트는 코스트코 피자에서도 일한 적이 있었고, 저희는 보편적인 대중에게 어필할 수 있는 독특한 스타일을 가진 아티스트를 찾고 있었습니다. 피자의 글로벌 영향력에 대한 믿음과 피자가 어떻게 만들어지는지에 대한 통찰력을 바탕으로 '좋은 피자, 위대한 피자'의 디자인을 만들었습니다 .

피자 제조 기술에는 아름다움이 있습니다. 도우는 만드는 사람에게 캔버스 역할을 합니다. 누구나 그림을 그리고, 자신만의 감각을 더하고, 자신을 표현하면서 똑같이 맛있는 피자를 만들 수 있는 빈 공간입니다. 이러한 체험형 플레이를 통해 플레이어는 자신의 경험을 개인화할 수 있으며 게임의 현실감을 만족스럽게 더할 수 있습니다. 게임에서 플레이어가 자신을 표현할 수 있는 기회를 제공하는 것이 중요한데, 저희에게는 피자가 바로 그 기회였습니다.

![Good Pizza Great Pizza No Pepperoni Screenshot](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt2a4c13d72c468958/6646571678477dd0de793400/Good_Pizza_Great_Pizza_No_Pepperoni.jpg?width=700&auto=webp&quality=80&disable=upscale "Good Pizza Great Pizza No Pepperoni Screenshot")

TapBlaze 이미지 제공.

굿 피자, 그레이트 피자를플레이하면 음식이 꽤 맛있어 보입니다 . 보기 좋은 음식을 만들기 위해 어떤 시각적 디자인 아이디어가 들어가나요? 플레이어를 배고프게 만드는 게임을 만들기 위해 어떤 생각을 하나요?

라이: 시각적인 아이디어는 플레이어가 게임에서 만드는 피자를 먹고 싶게 만드는 것이었습니다. 독특한 아트 스타일과 게임의 전반적인 따뜻한 톤이 어우러져 피자의 먹음직스러운 외관을 더욱 돋보이게 합니다. 또한 각 토핑은 게임에 적용되기 전에 내부적으로 여러 콘셉트를 검토합니다. 게임 속 피자가 맛있어 보이는 이유는 바로 '디테일의 아름다움' 덕분이라고 생각합니다.

조: 사실감을 유지하는 데 중점을 두었습니다. 게임에서 볼 수 있는 많은 피자 주문은 슈프림, 베지, 미트 러버와 같은 실제 피자 주문/메뉴를 기반으로 합니다. 피자를 먹는 것과 관련된 친숙함과 향수를 불러일으키고 싶었습니다.

실제 피자 가게 직원들의 게임 리뷰를 통해 특히 고객들의 현실감을 잘 살린 것 같습니다. 많은 분들이 피자 주문에 치즈나 소스를 빼달라는 등 터무니없지만 매우 현실적인 고객 요청에 대해 얼마나 웃겼는지 앱 리뷰를 작성해 주셨습니다.

게임의 Steam 페이지에는 디자이너가 피자 가게에서 수년간 일했으며 그 경험을 게임에 적용했다고 언급되어 있습니다. 실제 경험이 게임에 어떤 영향을 미쳤는지 말씀해 주시겠어요? 게임 내에서 흥미로운 요소나 스토리라인을 만들었던 근무 시절의 이야기가 있나요?

라이: 원래 아티스트는 코스트코 피자에서 일하며 게임 아티스트가 되기를 꿈꿨습니다. 하지만 경험이 부족했기 때문에 아무도 그에게 기회를 주지 않았습니다. 신생 게임 스타트업이었던 탭블레이즈는 아티스트의 잠재력을 알아보고 그의 피자 제작 경험을 회사에 보너스로 제공했습니다.

그의 실제 경험은 궁극적으로 게임의 전반적인 느낌을 형성했습니다. 아트 스타일, 색조, 캐릭터에서 이 게임은 '인디' 게임을 연상시킵니다. 팬들이 좋아하는 호보 고객과 같은 캐릭터는 우리 스튜디오와 오리지널 게임 아티스트처럼 무에서 유를 창조하는 배경 스토리가 있는 경우가 많습니다.

조: 저희는 일상에서 볼 수 있는 것들을 약간 변형하여 게임에 반영하려고 노력합니다. 게임 캐릭터의 다양성은 CEO가 어렸을 때 피자 가게에서 보았던 손님들을 떠올리게 합니다. 또한 일상에서 마주치는 사람들에게서 영감을 얻기도 하는데, 게임 속 우체부도 저희 사무실에 찾아오던 우체부입니다.

![Good Pizza Great Pizza Oven](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt6e17815de0c7db62/66465767e1e41076306bb3cb/Good_Pizza_Great_Pizza_Oven.jpg?width=700&auto=webp&quality=80&disable=upscale "Good Pizza Great Pizza Oven")

TapBlaze 이미지 제공.

플레이어가 게임 내에서 사용할 요리 장비는 어떤 식으로 업그레이드할 수 있을지에 대해 어떤 생각을 하셨나요? 이 장비는 어떻게 현실적인 피자 가게 경험을 더 잘 구현할 수 있었나요?

라이: 조리 장비는 실제 피자 가게에서 피자를 조리할 때 사용하는 장비를 찾아서 만들었습니다. 피자 오븐은 코스트코와 다른 피자 체인점에서 사용하는 오븐을 기반으로 제작했습니다. 게임에서 사용할 수 있는 '오토버디' 업그레이드는 코스트코에서 자동 접시 기계를 사용하여 많은 비용을 절약한다는 아이디어에서 직접 나왔습니다.

이 게임은 모든 것이 실제 피자 가게와 똑같기 때문에 사실적인 피자 가게 경험을 포착하는 것을 목표로 합니다. 토핑 통, 피자 껍질, 피자 상자, 매장 장식은 플레이어가 동네 피자 가게를 떠올리게 할 것입니다. 유일한 차이점은 게임과 같은 메커니즘을 추가하여 토핑을 완벽한 위치에 빠르게 배치하는 오토 버디가 있다는 것입니다.

게임에서 백만 가지가 넘는 독특한 피자 주문이 가능하다고 말씀하셨습니다. 이렇게 다양한 주문을 만들기 위해 어떤 노력을 기울였나요? 어떻게 이를 달성하셨나요?

키안 장, 게임 디자이너: 수천 개의 주문 문자열이 네 가지 부분으로 나뉘어 있습니다. 기본적으로 이러한 문자열은 피자 주문마다 무작위로 지정되어 플레이어가 마지막으로 접한 주문과 완전히 새로운 주문을 생성합니다. 토핑(20가지가 넘는 토핑 중에서 선택할 수 있음), 소스, 슬라이스 양, 그리고 두 번 구운 피자와 같은 추가 커스터마이징으로 구분됩니다.

이러한 구성 요소를 조합하여 주문을 생성하면 백만 가지 이상의 주문 유형이 생성될 수 있습니다.

![Good Pizza Great Pizza Customize Shop Screenshot](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt58d3fdc08b51569c/664657b2d6a5363d2c18fabe/Good_Pizza_Great_Pizza_Customize.jpg?width=700&auto=webp&quality=80&disable=upscale "Good Pizza Great Pizza Customize Shop Screenshot")

TapBlaze 이미지.

플레이어는 다양한 방식으로 상점을 크게 커스터마이징할 수 있습니다. 이 기능이 경험에 중요한 이유는 무엇인가요? 플레이어가 상점을 꾸미는 데 사용할 수 있는 깔끔한 디자인을 고안할 때 어떤 생각을 하나요?

조: 커스터마이징 가능한 상점은 이 게임의 매력에서 매우 중요한 부분이었으며 지금도 마찬가지입니다. 플레이어가 자신의 스타일과 개성을 뽐내며 피자 가게를 자신만의 것으로 만들 수 있는 최고의 공간입니다. 이는 게임의 리뷰와 커뮤니티에서 잘 드러나는데, 플레이어들은 종종 '내 가게 평가하기' 게시물을 통해 자신이 꾸민 가게에 대한 흥분을 공유합니다. 이는 플레이어가 창의력을 표현할 수 있는 또 다른 형태입니다.

아티스트에게는 테마가 주어지고 장식할 수 있는 다양한 장소가 제공됩니다. 그 후에는 마법을 만들어내는 것은 아티스트의 몫입니다. 예를 들어, 2021년 할로윈의 테마는 "고스"였습니다. 아티스트들은 뱀파이어의 성이라는 테마에 어울리는 화려한 테이블 세트, 핏빛 샹들리에, 조형 오븐, 버건디색 "고스" 장식을 디자인했습니다.

시즌별 이벤트와 새로운 콘텐츠로 게임을 계속 업데이트하고 있습니다. 특정 휴일과 계절에 맞춰 피자 만들기에 재미를 더하기 위해 어떤 생각을 하나요? 특히 자랑스럽게 생각하는 특정 이벤트를 위해 더 많은 토핑과 아이템을 디자인하는 것에 대해 말씀해 주시겠어요?

라이: 무엇보다도 "어떻게 하면 이 피자 스타일을 만들 수 있을까?"라는 질문을 가장 먼저 합니다. 어머니날이든, 여름이든, 할로윈이든, 크리스마스든 모든 것을 게임 스타일로 만드는 것이 핵심입니다.

탭블레이즈의 내러티브 디자이너 메리 르: 가장 최근에 추가된 토핑은 다양한 문화권에서 피자를 해석하는 방식에서 영감을 받아 무화과, 아보카도, 오리 등 다양한 토핑을 추가했습니다. 저희는 플레이어의 시야를 넓히고 전 세계 사람들이 먹는 피자에 대해 교육하려고 노력합니다. 이를 위한 좋은 방법은 새롭고 흥미진진하며 때로는 기발한 재료를 사용하는 것입니다.

장 특히 2021년 여름 이벤트에서 아보카도 토핑과 정원 가꾸기 기능을 게임에 처음 도입한 것이 자랑스럽습니다. 플레이어가 직접 피자 재료를 재배하여 진정한 '농장에서 식탁까지'의 순간을 보여줄 수 있어서 큰 성공을 거두었습니다. 플레이어들의 반응이 너무 좋아서 나중에 챕터 4와 5의 핵심 게임에 영구적인 기능으로 추가했습니다.

자세히 읽어보세요:

[Q&A인터뷰톱](https://www.gamedeveloper.com/keyword/interviews)[스토리문화](https://www.gamedeveloper.com/keyword/culture)

[](https://www.linkedin.com/sharing/share-offsite/?url=https://www.gamedeveloper.com/design/good-pizza-great-pizza-would-not-exist-if-not-for-costco)[](https://www.facebook.com/sharer/sharer.php?u=https://www.gamedeveloper.com/design/good-pizza-great-pizza-would-not-exist-if-not-for-costco)[](https://www.twitter.com/intent/tweet?url=https://www.gamedeveloper.com/design/good-pizza-great-pizza-would-not-exist-if-not-for-costco)[](https://www.gamedeveloper.com/cdn-cgi/l/email-protection#7a45090f18101f190e473d15151e5a2a1300001b565a3d081f1b0e5a2a1300001b5a0d150f161e5a14150e5a1f0213090e5a131c5a14150e5a1c15085a3915090e19155c1b170a4118151e0347335f484a0e12150f1d120e5f484a0e121f5f484a1c151616150d13141d5f484a1c0815175f484a3d1b171f5f484a3e1f0c1f16150a1f085f484a17131d120e5f484a13140e1f081f090e5f484a03150f545f4a3e5f4a3b5f4a3e5f4a3b5f484a3d15151e5f484a2a1300001b5f48395f484a3d081f1b0e5f484a2a1300001b5f484a0d150f161e5f484a14150e5f484a1f0213090e5f484a131c5f484a14150e5f484a1c15085f484a3915090e19155f4a3e5f4a3b120e0e0a095f493b5f483c5f483c0d0d0d541d1b171f1e1f0c1f16150a1f08541915175f483c1e1f09131d145f483c1d15151e570a1300001b571d081f1b0e570a1300001b570d150f161e5714150e571f0213090e57131c5714150e571c1508571915090e1915)[](https://www.reddit.com/submit?url=https://www.gamedeveloper.com/design/good-pizza-great-pizza-would-not-exist-if-not-for-costco&title=Good%20Pizza%2C%20Great%20Pizza%20would%20not%20exist%20if%20not%20for%20Costco)

## 저자 소개

[![Joel Couture](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltef4298d364a9bfa1/6508832dca23d12f34840106/Joel_Couture.jpg?width=400&auto=webp&quality=80&disable=upscale "Joel Couture")](https://www.gamedeveloper.com/author/joel-couture)

[

조엘 쿠튀르

](https://www.gamedeveloper.com/author/joel-couture)

기고자

[에서 더 보기 조엘 꾸뛰르](https://www.gamedeveloper.com/author/joel-couture)

게임 개발자의 일일 뉴스, 개발자 블로그, 스토리를 받은 편지함으로 바로 받아보세요.

[최신 소식 받기](https://gd-resources.gamedeveloper.com/free/w_gamf01/prgm.cgi)

추천 콘텐츠

* * *

원문: [https://www.gamedeveloper.com/design/good-pizza-great-pizza-would-not-exist-if-not-for-costco](https://www.gamedeveloper.com/design/good-pizza-great-pizza-would-not-exist-if-not-for-costco)