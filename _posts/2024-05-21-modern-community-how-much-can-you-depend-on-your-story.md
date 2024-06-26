---
title:  "앱러빈의 최신 커뮤니티와 게임 내러티브의 힘"

categories:
  - 번역
  
tags:
  - DoF
toc: true
toc_sticky: true
 
date: 2024-05-21
last_modified_at: 2024-05-21
---
[

![](https://images.squarespace-cdn.com/content/v1/58af450eb3db2b0582612f1d/2ea19d0a-1333-4d75-83a4-4fd21f8261df/ahmetcan.jpeg)



](https://www.linkedin.com/in/ahmetcan-demirel-686519171/)

_제품 관리의 거장이자_ _독일 출신의_ _팟캐스트 진행자(_[_게임 개발 다이어리_](https://open.spotify.com/show/6ttSIEYkixmKtmgKy1Xevo?dlsi=2394ffdc86254b93&nd=1&si=e816c75155924844))인[_아멧칸 데미렐이_](https://www.linkedin.com/in/ahmetcan-demirel-686519171/)_쓴_ 글입니다_! 퍼즐, 아케이드, 시뮬레이션 게임에 능통합니다._

_아멧칸은 분석이나 고객 컨설팅을 위한 킬러 기능을 설계하느라 바쁘지 않을 때는 베를린의 활기찬 기술 현장을 탐험하거나 도시의 힙스터 카페에서 Deconstructor of Fun에 글을 기고하고 있는 모습을 볼 수 있습니다._

* * *

성공적인 매치 3를 만드는 것은 모바일 게임 개발자가 해결할 수 있는 가장 어려운 과제 중 하나입니다. 성공하려면 매력적이고 차별화된 메타게임과 더불어 최고 수준의 게임 엔진이 필요하며, 이 두 가지를 모두 갖추고 있더라도 플레이어를 유인할 수 있는 강력한 UA 캠페인이 필요합니다. 가장 수익성이 높은 게임 기업들과 가장 막대한 자금력을 바탕으로 경쟁하게 될 것입니다. 이 과정에서 많은 별을 모으고 자금이 부족하지 않아야 합니다.

그렇기 때문에 상위 매치 3 게임 중 상당수가 소수의 개발사에 속해 있습니다. 차트 상위권은 캔디 크러쉬 게임의 King, 스케이프 게임과 _피쉬돔_ (여전히 강세를 보이고 있습니다!)의 Playrix, _로얄 매치의_ Dream이 상위권을 차지했습니다. AppLovin은 _프로젝트 메이크오버로_ 그 뒤를 바짝 쫓고 있으며, 경쟁에서 밀리지 않고 또 다른 새로운 매치 3 게임을 출시했습니다: _모던 커뮤니티_.

3월 초에 출시되었기 때문에 아직 데이터가 채워지고 있지만, 게임의 전략적 목표, 전반적인 디자인, 극복해야 할 과제와 관련하여 언급할 내용이 많습니다. **게임 엔진에 초점을 맞춘 매치 3 게임 시장이 혼잡한 가운데, _모던 커뮤니티는_ 매치 3 게임 중 최고의 메타게임인 심즈 게임이라고 할 수 있습니다.**

## **메타게임의 새로운 표준 설정**

[Tactile의 _Makeover Match를_ 해체하는](https://www.deconstructoroffun.com/blog/2023/6/4/iteration-over-innovation) 과정에서 한 가지 중요한 변화를 제외하고는 _Project Makeover의_ 스토리라인을 그대로 고수하고 있다고 언급했습니다: 바로 모든 캐릭터를 3D로 만든 것입니다. 스토리에 3D 캐릭터와 애니메이션을 추가하면 스토리에 생동감이 더해지지만, 기존 스토리의 제작이 복잡해지는 경우가 대부분입니다. 예를 들어 스페이스 에이프는 _크롬 밸리 커스텀에서_ 단순히 미적 감각을 높이기 위해 비주얼을 개선하려 하지 않았습니다. 그들은 소외된 남성 퍼즐 플레이어에 초점을 맞춘 메타게임에 대한 구체적인 시각을 가지고 있었고, 제작의 복잡성을 높이는 대신 그 목표를 향해 비주얼 스타일을 구축했습니다. 전자는 아직 자리를 잡기 위해 노력 중이고 후자는 어느 정도 성공을 거두었습니다;

전체 크기 보기

![](https://images.squarespace-cdn.com/content/v1/58af450eb3db2b0582612f1d/ac32c9b7-34f8-40ba-831d-114ab928745e/Screenshot+2024-05-20+at+13.29.44.png)

물리적 복원은 _매칭턴 맨션과_ 완전히 동일하며, 화장은 _프로젝트 메이크오버의_ 속도 향상 버전입니다.

**반면,_모던 커뮤니티는_ 메타게임에 올인하여 스토리를 진행하는 동안 백그라운드에서 미니 심즈 게임이 실행됩니다.** 아주 거칠게 말하자면, _Matchington Mansion과_ _Project Makeover의_ 장점만 모아놓은 게임이라고 할 수 있습니다: 주인공 페이지가 도시와 자신의 아파트를 개조하고 커뮤니티를 꾸미며 로맨스에 빠져드는 모험을 따라가게 됩니다. _매칭턴 맨션_ 파트에서는 매콤한 대화와 함께 내부 및 외부 리노베이션을 진행하게 됩니다. 이 게임은 또한 플레이어가 스토리 속 캐릭터의 삶을 개선하기 위해 빠른 메이크오버를 수행하게 합니다. 본격적인 화장은 _모던 커뮤니티의_ 몇 가지 작업으로 완료되므로 이 부분은 _프로젝트 메이크오버의_ 압축 버전이라고 할 수 있습니다. AppLovin은 기존의 모든 복원/메이크오버 메커니즘을 사용하여 메타게임의 모든 기반을 다루고 있습니다. 이 게임이 내러티브 중심의 매치 3 게임에 새로운 기준을 제시할 수 있는 이유는 크게 세 가지입니다: 게임플레이 커스터마이징, 성공 스토리의 모방, 최고 수준의 제작 품질 보장.

### **게임플레이 커스터마이징**

플레이어는 게임에서 주인공과 주인공의 집을 커스터마이징할 수 있습니다. 이 자체만으로는 큰 의미가 없으며, _Project Makeover는_ 이미 오래전부터 이 기능을 제공해 왔습니다. **_현대 커뮤니티는_ 플레이어가 스토리를 진행하면서 캐릭터의 변화를 볼 수 있기 때문에 눈에 띕니다!** 이는 참여도가 높은 플레이어가 자신의 캐릭터를 커스터마이징하고 다른 플레이어와 공유하기 위해 마련된 신기한 기능이 아니라(추후 도입할 예정이라고 합니다), 게임 내에서 눈에 띄는 진정한 변화입니다. _프로젝트_ 화장에서 각 챕터의 특정 탭을 열어야만 가능했던 캐릭터와 NPC의 화장을 게임 전체에서 볼 수 있습니다.

전체 크기 보기

![](https://images.squarespace-cdn.com/content/v1/58af450eb3db2b0582612f1d/f0a1436d-2e52-44ad-95ef-6c51235dd3df/Screenshot+2024-05-20+at+13.32.57.png)

방(왼쪽)과 캐릭터(오른쪽)를 개조할 수 있습니다.

메이크오버를 디자인하는 방식은 결과적으로 매우 중요한 것을 달성합니다: 플레이어가 스토리를 진행하는 동안 내가 한 메이크오버를 보면 메이크오버와 스토리 자체에 더욱 몰입하게 됩니다. 물론 모든 플레이어가 같은 방식으로 메타게임과 상호작용하는 것은 아니지만, 이런 방식으로 메이크오버를 통합하면 플레이어가 메타게임과 상호작용하고 머무는 시간이 늘어날 가능성이 높습니다;

전체 크기 보기

![](https://images.squarespace-cdn.com/content/v1/58af450eb3db2b0582612f1d/d72c0d63-7408-4c91-a2a4-542a7d4dbf0a/Screenshot+2024-05-20+at+13.33.59.png)

사소하게 들릴지 모르지만, 게임에서 캐릭터의 변화를 보면 게임이 더욱 생동감 있게 느껴집니다.

### **성공 사례 모방하기**

메타게임이 있는 매치3에서 플레이어는 레벨을 완료하여 별이나 자원을 획득하고, 이를 사용하여 과제를 완료하고 메타게임을 진행합니다. 메타 레이어가 많은 게임, 즉 스토리가 있는 게임에는 주로 복원과 스토리의 두 가지 종류의 작업이 있습니다. 복원 작업에서는 주변 공간을 어떻게 디자인할지 선택해야 합니다. 벽의 색이나 나무의 종류를 선택하는 것이 그 예입니다. 반면 스토리 작업은 일반적으로 게임 내 캐릭터 간의 상호작용을 지켜보는 것 외에는 아무것도 할 필요가 없습니다.

_모던 커뮤니티는_ 복원 작업과 관련하여 대부분의 다른 매치 3 게임과 매우 유사한 경험을 제공합니다. 선택지가 주어지는 방식이나 플레이어의 선택에 반응하는 캐릭터는 시중에 나와 있는 다른 매치 3 게임과 크게 다르지 않습니다. 하지만 이 게임은 내러티브 디자인에 많은 투자를 했습니다. 지금까지 우리는 매치 3 게임에서 저택을 물려받는 노인이나 사람들의 삶을 더 나은 방향으로 바꾸도록 돕는 TV 제작진과 같은 순진한 이야기를 보는 데 익숙해져 있었습니다. _모던 커뮤니티는_ 내러티브 디자인에 다른 각도로 접근하여 처음부터 다소 유치한 대사가 포함된 삼각 관계를 제시합니다. 섹시한 소방관과 근육질의 예술가들이 페이지가 도시 곳곳에서 겪는 어려움을 극복하는 데 도움을 주는 넷플릭스 쇼를 보는 것 같은 느낌입니다.

전체 크기 보기

![](https://images.squarespace-cdn.com/content/v1/58af450eb3db2b0582612f1d/b7bcae69-a406-4be9-bd91-5599f766c9d3/Screenshot+2024-05-20+at+13.35.01.png)

어디에 선을 그어야 할지 잘 모르겠지만, 이 정도면 유치하다고 봐야 할 것 같아요...

그리고 이것은 넷플릭스 쇼뿐만 아니라 다른 게임에서도 널리 퍼져 있습니다. 비슷한 취향을 가진 또 다른 게임으로는 최근 꽤 잘하고 있는 가십 _하버가_ 있습니다. 가십 _하버의_내러티브는 가십 하버가 잘하고 있는 여러 가지 요소 중에서도 흥행에 기여하는 요소 중 하나라고 할 수 있습니다. 초기 대화는 위와 비슷하게 시작부터 수많은 등장인물이 싸구려 대사를 주고받는 것이 특징입니다. 앱러빈이 스토리를 작성하면서 그들의 플레이북에서 한 페이지를 가져온 것 같습니다. 앞서 말했듯이 우리는 시장에서 특정 유형의 스토리를 보는 데 익숙해져 있는데, 이것이 새로운 트렌드가 될지 궁금합니다...

### **넷플릭스와 경쟁하기 위해...**

넷플릭스와의 경쟁에 대해 말하자면, _모던 커뮤니티는_ 단순히 넷플릭스 프로그램과 비슷한 내러티브를 가지고 있는 것에서 그치지 않습니다. 이 게임은 촌스러운 대사와 주요 스토리 순간을 더욱 돋보이게 하는 시네마틱으로 가득합니다. **저는 "게임은 다른 게임뿐만 아니라 다른 형태의 엔터테인먼트와도 경쟁한다"는 생각을 계속 강조하고 있습니다. 이 게임은 다른 형태의 엔터테인먼트와 경쟁하기 위해 제작 품질의 기준을 한 차원 높였습니다.** 게임 개발팀은 스토리 제작에 많은 시간과 노력을 투자했을 것입니다. 메타게임의 제작 품질이 이렇게 높은 매치 3 게임은 본 적이 없습니다.

전체 크기 보기

![](https://images.squarespace-cdn.com/content/v1/58af450eb3db2b0582612f1d/d7a0f9c7-6cf9-4118-afa2-13cffbe21fe5/Modern_Community__Chapter_1__Gameplay.gif)

다루기엔 너무 뜨거운...에서 발췌한 것 같은 느낌입니다.

높은 제작 퀄리티는 스토리에만 국한되지 않고 진행 중인 이벤트에도 적용됩니다. 많은 퍼즐 게임에는 특정 행동을 완료하여 특정 아이템을 모아 보상을 받는 이벤트가 흔히 있습니다. 특정 아이템을 맞추거나 레벨 내에서 파워 업을 사용하거나 이벤트 전용 아이템을 모으는 등의 방식이 있습니다. 매우 일반적이고 기본적인 이벤트이기 때문에 모든 퍼즐 게임은 플레이어가 도달해야 하는 마일스톤 옆에 단순히 플레이어의 진행 상황을 표시합니다. 반면, _모던 커뮤니티는_ 특별한 장면으로 시작하는 '뉴스' 이벤트로 전환합니다. 그런 다음 플레이어는 이벤트에 대해 소개받고 해당 이벤트 전반에 걸쳐 또 다른 컷신을 잠금 해제하는 동시에 보상을 받습니다. 게임에서 가장 일반적이고 기본적인 이벤트 중 하나를 위한 특별한 장면을 만드는 것입니다. 제작 품질에 대해 이야기하자면...

지금까지 매치 3 게임 중 메타게임 제작의 표준을 정립한 게임은 단 한 개도 없었습니다. _홈스케이프와_ _프로젝트 메이크오버처럼_ 메타게임이 있는 게임과 없는 게임( _로얄 매치_, _캔디 크러시_ 등)이 모두 성공했습니다. **_모던 커뮤니티는_ 메타게임 품질에 대한 새로운 기준을 정립하기 위해 여기에** 왔습니다. 메타게임의 다양한 부분을 그 어느 때보다 잘 통합하면서 플레이어에게 훨씬 더 깊이 있는 경험을 제공하는 것은 분명 중요한 차별화 요소가 될 것입니다. 또한 현재의 제작 품질을 유지할 수 있다면 결과적으로 경쟁사에 비해 훨씬 더 매력적인 게임을 만들 수 있을 것입니다.

## **핵심 게임플레이가 달라 보일 때**

몇 년 전만 해도 모두가 사용자 확보를 위해 가짜 광고를 사용하던 시절이 있었습니다. 매치3에서 4X 전략에 이르기까지 대부분의 성공적인 게임들은 어떤 형태로든 이를 적용했습니다. 하지만 "핀을 뽑아라" 광고를 통해 확보한 플레이어들은 더 많은 "핀을 뽑아라" 퍼즐을 플레이하기를 원했기 때문에 여기서 멈추지 않았습니다. (알아요, 충격적이죠). 그런 다음 이 가짜 광고를 게임에 통합하여 플레이어에게 '미니 게임'으로 알려진 것을 제공했습니다. 실제로 이 분야의 선구자 중 하나인 Playrix는 현재 _홈스케이프와_ _가든스케이프에서_ 거의 3레벨마다 미니 게임을 제공합니다.

전체 크기 보기

![](https://images.squarespace-cdn.com/content/v1/58af450eb3db2b0582612f1d/ad9314a7-e717-4052-ad87-9ba09e548847/Screenshot+2024-05-20+at+13.53.30.png)

_로얄 매치에서_ 미니 게임에서 영감을 받은 레벨 레이아웃.

드림게임즈는 자신들만의 독창적인 방식으로 지금은 악명 높은 "왕의 악몽" 크리에이티브를 개발하여 _로얄 매치에_ 적용했습니다. 플레이어는 _로열 매_치의 왕인 로버트 왕이 위험한 상황에 처해 있으며, 매치 3 퍼즐을 풀어서 그를 구해야 하는 임무를 부여받습니다. 이러한 크리에이티브를 사용한 직후, Dream은 해당 레벨을 게임에 통합하여 플레이어에게 주기적으로 "왕의 악몽" 레벨을 제공했습니다. 앱러빈은 _모던 커뮤니티에서도_ 플레이어의 여정 초반에 특별한 레벨을 제공함으로써 동일한 기능을 수행합니다. 캐릭터가 위험한 상황에 처하게 되면 플레이어는 '왕의 악몽' 레벨과 같은 특별 레벨을 완료해야만 캐릭터를 구할 수 있습니다. 그리고 이 레벨은 단순히 이상한 장면을 보여주는 보너스 레벨이 아니라 실제 스토리의 일부입니다! 플레이어는 먼저 불을 끄려는 캐릭터들을 보게 되고, 특별한 레벨이 주어집니다.

전체 크기 보기

![](https://images.squarespace-cdn.com/content/v1/58af450eb3db2b0582612f1d/a41183d5-e53e-420f-b3d2-b74f5e559eec/Screenshot+2024-05-20+at+13.54.18.png)

캐릭터가 겪는 어려움을 본 후 이 특별 레벨을 플레이하면 훨씬 더 이해가 잘 됩니다.

미니 게임이나 특별 레벨은 빠르고 편리한 해결책이지만, 모든 문제가 그렇게 쉽게 해결될 수 있는 것은 아닙니다. 특히 문제가 디자인 기둥 안에 있을 때는 더욱 그렇습니다. 우리는 _모던 커뮤니티의_메타게임이 얼마나 훌륭한지, 그리고 모든 것이 얼마나 아름답게 조화를 이루는지에 대해 이야기했습니다. 메타게임에 많은 시간과 노력을 투자했다면 새로운 플레이어를 확보하는 데 사용하고 싶은 것은 당연한 일입니다. 하지만 메타게임에 주로 초점을 맞춘 광고를 통해 유입된 플레이어는 결국 여러분의 레벨을 플레이하게 될 것입니다. 그리고 레벨이 메타게임처럼 시각적으로 플레이어를 사로잡지 못하면 다음과 같이 많은 업보트를 받은 리뷰가 나올 수 있습니다;

![](https://images.squarespace-cdn.com/content/v1/58af450eb3db2b0582612f1d/827f8afa-560d-4b1d-a176-469b7a1f401c/Screenshot+2024-05-20+at+13.55.17.png)

플레이어에게 스토리를 보여준 다음 퍼즐 레벨을 제공하는 모순을 말하는 것이 아닙니다. 일종의 메타 레이어가 있는 다른 모든 퍼즐 게임이 그러하죠. 하지만 메타 레이어와 핵심 게임플레이가 서로 다를수록 플레이어의 감정은 더 나빠집니다. _모던 커뮤니티에서_ 메타게임의 높은 제작 가치를 고려할 때, 플레이어는 레벨을 플레이할 때 그에 상응하는 수준의 경험을 기대합니다. [이 동영상에서 레벨이 어떻게 보이는지 자세히 살펴볼 수 있습니다](https://www.youtube.com/watch?v=XZC07zVcjlE).

![](https://images.squarespace-cdn.com/content/v1/58af450eb3db2b0582612f1d/a74c7d4c-74f8-4b40-ba99-c289194e153d/Screenshot+2024-05-20+at+13.55.52.png)

_모던 커뮤니티의_ 레벨은 메타게임의 과대광고에 부응하지 못할 수도 있습니다.

그렇다고 게임의 핵심 게임플레이 경험이 나쁘다는 뜻은 아닙니다. _모던 커뮤니티의_ 게임 엔진이 열등하다고 생각하지 않습니다. 앞서 언급한 대로 속도와 단순성 면에서 _크롬 밸리 커스텀즈와_ 매우 흡사한 느낌을 줍니다. **하지만 가장 큰 문제는 고도로 세련된 메타게임과 상대적으로 단순한 핵심 게임플레이 사이의 극명한 대조인 것 같습니다.** 예를 들어, _크롬 밸리 커스텀즈가_ 메타게임에서 플레이어에게 제공하는 것은 레벨에서 제공하는 경험과 일관성이 없습니다. 게임의 외형과 느낌이 스토리부터 레벨까지 변하지 않기 때문에 적응하기 위해 정신적으로 기어를 바꿀 필요가 없습니다.

전체 크기 보기

![](https://images.squarespace-cdn.com/content/v1/58af450eb3db2b0582612f1d/0e4bdf65-c9c0-47cc-9141-6728c81e1702/Screenshot+2024-05-20+at+13.57.05.png)

_크롬 밸리 커스텀즈에서는_ 메타 게임플레이와 핵심 게임플레이 사이를 오가는 동안 정신적으로 기어를 바꿀 필요가 없습니다.

**_모던 커뮤니티에서는_ 세련된 애니메이션과 리얼리티 쇼 같은 대화로 가득한 풍부한 스토리가 저를 맞이합니다.** 그런 다음 방금 본 것과는 상반되는 매우 빠르고 비교적 간단한 핵심 게임플레이가 주어집니다. 스토리 발췌본이나 캐릭터 상호작용을 보여주는 동영상을 보고 게임을 다운로드한 플레이어는 이러한 불일치에 실망할 수 있습니다. 다시 말씀드리지만, 다른 게임에서도 이런 문제가 발생하지 않는다는 것은 아니며 다른 성공적인 퍼즐 게임에도 비슷한 리뷰가 있을 것입니다. 하지만 _모던 커뮤니티는_ 최고의 메타게임을 가지고 있기 때문에 현재의 핵심 게임플레이와 차이가 더 커질 것이라고 생각합니다.

## **다음 단계는 무엇인가요?**

_모던 커뮤니티는_ 이미 너무 많은 기능을 갖추고 있어서 현재로서는 당장 목표를 찾기가 어렵습니다. 하지만 앱러빈이 얼마나 위험을 감수할 수 있는지에 따라 시도해 볼 수 있는 것들이 여전히 많이 있습니다:

1.  **레벨 비주얼을 조정합니다:** 앞서 말했듯이 게임 엔진 자체가 열등하다고 생각하지는 않지만 게임 아이템에 '정체성'이 없습니다. 인기 있는 매치 3 게임을 보면 게임의 테마를 반영하는 맞춤형 게임 아이템이 있습니다. 책, 베개, 사탕 등 레벨을 통해 게임의 주제가 무엇인지 알 수 있습니다. 현재 이 게임은 게임 아이템에 단순한 기하학적 모양을 사용하여 주제적 의미가 부족합니다. 핵심 게임플레이와 메타게임 경험 사이의 주제적 연계성을 개선하면 전반적인 게임 경험을 향상시킬 수 있습니다.
    
2.  **스토리를 두 배로 강화하세요:** 게임의 스토리는 처음부터 이미 액션과 다양한 캐릭터로 가득 차 있습니다. 일부 플레이어가 실망한 점은 위의 추천 리뷰에서 보았듯이 대화형 선택과 사실적인 시뮬레이션 기능이 부족하다는 것입니다. 스토리 전달 방식을 조정하여 이러한 플레이어를 더 잘 만족시킬 수 있습니다. _모던 커뮤니티는_ 플레이어가 메타게임에서 여러 주인공을 동시에 따라가는 GTA와 유사한 모델을 채택할 수 있습니다. GTA를 참고하는 것은 어렵게 느껴질 수 있지만, 일관된 경험을 보장하기 위해 내러티브 디자인에 중점을 두어야 합니다. 이러한 스토리 요소를 추가하려면 글쓰기와 애니메이션 모두에 상당한 투자가 필요하지만, 스토리 전달 방식이나 메타게임 운영 방식의 근본적인 구조를 변경할 필요는 없습니다.
    
3.  **메타게임을 개척하세요:** Playrix는 플레이어에게 시뮬레이션 게임을 제공하는 두 '스케이프' 게임에서 이벤트를 진행했습니다. 플레이어는 제한된 에너지와 메인 스토리처럼 점진적으로 전개되는 작업 시스템의 제약을 받으며 탐험할 수 있는 광활한 지역을 제공받습니다. _모던 커뮤니티는_ 메타게임 내의 미니 게임을 통해 스토리를 확장하고 플레이어가 별도의 시스템을 사용하여 이를 탐험할 수 있도록 함으로써 유사한 접근 방식을 구현할 수 있습니다. 이 접근 방식은 스토리 중심의 플레이어가 게임에 계속 참여하도록 하는 동시에 레벨을 완료하면 에너지를 얻을 수 있기 때문에 레벨 플레이에 대한 인센티브도 제공할 수 있습니다.

원문: [https://www.deconstructoroffun.com/blog/2024/5/20/modern-community-how-much-can-you-depend-on-your-story](https://www.deconstructoroffun.com/blog/2024/5/20/modern-community-how-much-can-you-depend-on-your-story)