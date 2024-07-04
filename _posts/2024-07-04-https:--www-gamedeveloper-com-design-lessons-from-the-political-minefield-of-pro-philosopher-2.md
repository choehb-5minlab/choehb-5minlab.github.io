---
title:  "프로 철학자의 정치적 지뢰밭에서 얻은 교훈 2"

categories:
  - 번역
  
tags:
  - Game Developer
toc: true
toc_sticky: true
 
date: 2024-07-04
last_modified_at: 2024-07-04
---
[![Picture of Connor Fallon](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt7ce731765a3f128b/65087eb422641ec82885b962/Connor_Fallon.jpg?width=100&auto=webp&quality=80&disable=upscale "Picture of Connor Fallon")](https://www.gamedeveloper.com/author/connor-fallon)

[코너 팰런](https://www.gamedeveloper.com/author/connor-fallon), 블로거

7월 4일, 2024

10분 읽기

![](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltadd488650619ea54/6682b5576b424fb2252b1a1c/ss_64b5cd1099e2c45c69540403513178a97883970d.jpg?width=850&auto=webp&quality=95&format=jpg&disable=upscale)

[](https://www.linkedin.com/sharing/share-offsite/?url=https://www.gamedeveloper.com/design/lessons-from-the-political-minefield-of-pro-philosopher-2)[](https://www.facebook.com/sharer/sharer.php?u=https://www.gamedeveloper.com/design/lessons-from-the-political-minefield-of-pro-philosopher-2)[](https://www.twitter.com/intent/tweet?url=https://www.gamedeveloper.com/design/lessons-from-the-political-minefield-of-pro-philosopher-2)[](https://www.gamedeveloper.com/cdn-cgi/l/email-protection#457a3630272f20263178092036362a2b366523372a2865312d2065152a292c312c26242965082c2b20232c202921652a236515372a65152d2c292a362a352d20376577632428357e272a213c780c607775312d2a30222d31607775312d20607775232a29292a322c2b2260777523372a286077750224282060777501203320292a352037607775282c222d316077752c2b3120372036316077753c2a306b607501607504607501607504607775092036362a2b3660777523372a28607775312d20607775152a292c312c262429607775082c2b20232c2029216077752a2360777515372a607775152d2c292a362a352d2037607775776075016075042d313135366076046077036077033232326b2224282021203320292a3520376b262a286077032120362c222b607703292036362a2b366823372a2868312d2068352a292c312c26242968282c2b20232c202921682a236835372a68352d2c292a362a352d20376877)[](https://www.reddit.com/submit?url=https://www.gamedeveloper.com/design/lessons-from-the-political-minefield-of-pro-philosopher-2&title=Lessons%20from%20the%20Political%20Minefield%20of%20Pro%20Philosopher%202)

저는 유명한 철학자들을 애니메이션으로 표현한 퍼즐 토론에 도전하는 곧 출시될 인디 게임인 프로 철학자 2의메인 디자이너이자 작가인 코너 팰런입니다 . 이 이름이 익숙하게 들린다면 첫 번째 게임인 소크라테스 존스를 플레이해 본 적이 있을 것입니다: 2013년 콩그레게이트에서 컬트적인 인기를 끌었던 소크라테스 존스:프로 철학자를 기억하실 겁니다.([현재 Steam에서 무료로 재출시되었습니다!](https://store.steampowered.com/app/2120060/Socrates_Jones_Pro_Philosopher/))

당시 [저는 에이스 어쏘시에이트에서 영감을 받은 게임플레이를 철학적 토론이라는 추상적인 주제에 맞게 조정하는 데 따른 어려움에 대해 글을 썼](https://www.gamedeveloper.com/design/making-a-debate-game-the-design-challenges-of-socrates-jones)습니다. 그 이후로 저희 팀은 낮에는 여러 AAA 게임을 출시하고 밤에는[엘시노어를](https://store.steampowered.com/app/512890/Elsinore/) 출시하면서 많은 것을 배웠기 때문에 속편 개발이 더 쉬울 것이라고 생각하는 것은 당연한 일입니다. 하지만 프로 철학자 2는 완전히 새로운 도전과 교훈을 제시했는데, 이 모든 것은프로 철학자 2: 정부와 불만이라는한 가지 단순한 사실에서 비롯된 것이었습니다.

2024년의 정치에 대해 토론하는 것이 어렵다고 생각했다면, 정치에 관한 게임을 만들어 보세요!

## 그런데... 왜요?

좋은 질문이네요, 제가 쓴 섹션 제목입니다!

처음에 정치 철학은 소크라테스 존스의 도덕 철학을 다루면서 자연스럽게 발전한 것처럼 느껴졌지만, 사람들이 직감은 가지고 있었지만 공식적으로 생각해 볼 시간을 가진 사람은 거의 없었습니다.프로 철학자 2에등장하는 많은 논증은 첫 번째 게임이 출시된 후 엘시노어 작업을 시작하기 몇 달 전에 초안이 작성되었습니다 . 하지만 2019년에 속편 개발에 착수했을 때는 정치적 분위기가 더욱 격렬해져 있었습니다.

사람들이 가졌던 그 '직감'은요? 점점 더 유독한 담론에 직면하여 상처를 입고 굳어졌으며, 참여에 대한 극단주의를 증폭시키는 알고리즘이 등장했습니다. 사람들은 점점 더 이념적 반향실에서 고립되고 있으며, 모두가 동의할 수 있는 유일한 것은 분위기가 나쁘다는 것뿐입니다.

![Shot_01.png](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt145fd6a9a4c55e04/6682afe25c9ba2bf65ebbdd0/Shot_01.png?width=700&auto=webp&quality=80&disable=upscale "Shot_01.png")

정치 철학을 주제로 선택하면서 우리는 반발의 가능성이 높아지는 것을 받아들여야 했습니다. 핵심 질문이 말 그대로 '이상적인 정부란 무엇인가'일때,게임에서 정치를 배제할 수는 없습니다.그냥... 안 하는 것이 더 안전했을 것입니다.

하지만 초기 플레이 테스트는 저희의 기반을 다지는 데 도움이 되었습니다. 의도적으로 다양한 견해를 가진 플레이어를 찾았고, 긍정적인 반응을 통해 깨진 담론이 게임의 가치를높여준다는 것을 알 수 있었습니다.우리는 사람들이 실제 정치 토론의 판단과 분노 없이도 게임 환경에서 편안하게 흥미진진한 정치적, 철학적 두뇌 싸움에 참여할 수 있도록 할 수 있었습니다.

그렇게 해서 저희는 피치의 핵심을 발견했습니다: 프로 철학자 2는 누구와도 토론을 할 수 있고,실제로 내 주장을 경 청할 수 있다는 '파워 판타지 '입니다.할아버지가 그랬으면 하는 것처럼요.

하지만 우리가 그렇게 하기로 결정했더라도 쉽지 않은 일이었습니다. 그래서 저희 팀이 그 과정에서 얻은 몇 가지 교훈을 소개합니다:

## 교훈 1: 소스에서 시작하라

판타지를 전달하기 위해서는 다양한 정치적 관점을 각자의 관점에서 탐구하여 그 관점이 왜 설득력이 있는지, 그리고 어디에서 걸림돌이 되는지 보여줘야 합니다. 이를 위해서는 사상을 잘이해해야 하며, 이는 필연적으로 한 곳, 즉 철학 텍스트 자체로 이어집니다.  
  

철학을 더 쉽게 접근하고 재미있게 만드는 게임에서 "원전만 있으면 된다!"라고 주장하는 것은 자기 패배적일 수 있으므로 분명히 말씀드리자면, 개요에는 엄청난 가치가 있습니다. 저의 옛 철학 교수인 Andy Norman이 기꺼이 개요를 보내주셨고, 스탠포드 철학 백과사전과 같은 온라인 자료도 충분히 충실합니다.하지만 저희의 목적에 비추어 볼 때, 그러한 요약본에서 대충 넘어갈 수 있는 세부 사항은 마키아벨리가 무작위 질문 342에 어떻게 응답할지 파악하는 데 매우 중요합니다.

![Shot_02.png](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blta4197eefcf46d3d2/6682afaf247dd779cb860157/Shot_02.png?width=700&auto=webp&quality=80&disable=upscale "Shot_02.png")

이 철학자들에 대해 자세히 알아보는 작업은 '우리가 설교하는 것을 실천하는 것'의 핵심적인 부분이었으며, 그들의 관점의 뉘앙스를 정확하게 포착하는 데 필수적이었습니다. 이 게임을 연구하면서 개인적으로 저와 근본적으로 다른 견해를 가진 철학자 몇 명을 알게 되었습니다. 철학자들의 개성이 코믹하게 과장되어 있지만 그들의 사상은 결코 허무맹랑하지 않다는 것을 텍스트에서도 느낄 수 있습니다.

3장의 임의의 대사에 대해 화가 난 사람이 갈퀴를 들고 찾아온다면 로크가 묻힌 곳으로 불만을 보내라고 안내할 수도 있습니다. 아직 이러한 아이디어를 해석하고, 플랫폼화하고, 리믹스하는 중이기 때문에 여기까지만 설명할 수 있지만 도움이 됩니다.

## 레슨 2: 혼란을 통합하기

첫 번째프로 철학자 게임에는 임마누엘 칸트가 떠오르는 등 '문제적 애호가'가 없었던 것은 아니지만, 가족을 먹여 살리지 못했다고 해서 칸트를 비난하는 사람은 거의 없었습니다. 2의 철학자들은? 전혀 다른 이야기입니다.

정치 철학자들은 오늘날 정부와 지도자의 운영 방식을 형성했으며 ,종종 복잡하고 상충되는 방식으로 영향을 미쳤습니다.마키아벨리의 군주론은 많은 독재자들에게 영감을 준 책으로 인용되어 왔지만, 이 책이 묘사하는 행동을 지지하거나 폭로하려는 의도가 있었는지에 대한 논쟁도 많습니다. 중국 역사에서 공자의 명예로운 위치에는 여러 가지 짐이 있습니다. 그리고 우리가 아직 밝히지 않은 철학자 중 일부에 도달하면...

![Shot_03.png](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt9e91126aa1b56e34/6682afca1afd5b3628b21961/Shot_03.png?width=700&auto=webp&quality=80&disable=upscale "Shot_03.png")

플레이어가 프로 철학자 2의 철학자들과 기존 관계를 맺을 확률은 첫 번째 게임보다훨씬 더 높습니다 .초기 테스트에서 한 플레이어는 마키아벨리와의 대화에 흥분한 반면, 다른 플레이어는 그 개념을 두려워했습니다. 이러한 감정을 인정하지 않으면 토론이 불완전하게 느껴집니다. 극단적인 경우에는 플레이어가 완전히 소외될 수도 있습니다.

그래서 저희는 이 모든 혼란을 텍스트에 담았습니다.

첫 번째 게임에서는 철학자들이 현재 세계에 대해 어느 정도 인식하고 있다는 자만심이 있었고, 주로 대중문화 농담에 사용되었습니다. 두 번째 게임에서는 좀 더 극적인 결말을 위한 것이었습니다. 오리지널 출연진과 철학자 모두 자신의 사상이 미친 영향을 알고 있으며, 유산에 대한 이러한 감정을 공개적으로 논의하여 다양한 시작점을 다양한 캐릭터를 통해 '보고' 표현할 수 있도록 했습니다.

역사적 인물들이 자신과 다른 사람들에 대해 혼란스러운 감정을 갖도록 하는 것은프로 철학자 2에서가장 풍성한 순간을 만들어냅니다 . 더 많은 짐을 짊어지고 있다는 뜻이지만, 이런 요소가 없었다면 게임이 제대로 작동하지 않았을 거라고 생각해요.

## 레슨 3: 독특한 난이도 수식어

저는 '게임 개발자'이기 때문에 복잡도와 난이도 진행을 관리하는 데 어느 정도 익숙하다고 가정하겠습니다(에디터에서 좋은 리소스를 링크해 드릴 수도 있습니다!) 대부분의 게임과 마찬가지로, 저희는 시간이 지나면서 콘텐츠가 증가하도록 설계하고 플레이 테스트를 통해 이러한 계획이 얼마나 잘 작동하는지 확인했습니다. 하지만 프로 철학자는 플레이어마다 일관성이 없고 사실상 조정이 불가능한 독특한 변수와 싸워야 했습니다.

챕터의 난이도를 결정하는 가장 큰 요인 중 하나는 철학자의 의견 에얼마나 동의하느냐였습니다 .구체적으로 말하면, 가장 어려운 챕터는 일반적으로 가장 동의하는철학자였습니다 .

![Shot_04.png](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt188c56c3fff1ab2d/6682b0033e9e350915119858/Shot_04.png?width=700&auto=webp&quality=80&disable=upscale "Shot_04.png")

심리적으로 이해가 되는 부분입니다. 이미 로크의 정부 모델에 심각한 결함이 있다고 생각한다면 몇 가지 반론을 염두에 두고 있을 것이고, 그 중 적어도 하나는 질문을 통해 드러날 가능성이 높습니다. 하지만 이 게임에는 "당신 말이 맞아요, 이 진술에는 아무런 문제가 없습니다"라고 말할 수 있는 버튼이 없습니다. 동의하는 사람에게 이의를 제기하려면 플레이어 자신의 세계관을 크게 조정해야 합니다.

일반적으로 챕터 순서를 정할 때 현대적이고 공감할 수 있는 철학자가 나중에 나오도록 하는 것 외에, 다소 예측할 수 없는 급격한 변화는 감수해야 했습니다. 긍정적인 점은 다른 사람만큼이나 자신에게 질문하는 것이 중요하다는 저희의 주제와 잘 어울린다는 점입니다. 우리 스토리에 등장하는 대부분의 인물과 철학자들은 언젠가는 이 문제에 직면하게 됩니다. 플레이어도 이를 느끼는 것은 당연한 일입니다.

## 레슨 4: 화제의 폭풍을 예측할 수 없다

정치적 핫토픽은 일정하지 않습니다. 지금 또는 3년 후의사건으로 인해 사람들이 몇 년 전에 작성한 콘텐츠를 해석하는 방식이 크게 달라질 수 있습니다. 사례 연구로, 2015년 초안 작성 이후 거의 변하지 않은 공자 교환을 예로 들어보겠습니다:

![Shot_05.png](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt7e1b6644eac8587a/6682b070430aca601c840e5e/Shot_05.png?width=700&auto=webp&quality=80&disable=upscale "Shot_05.png")

상당히 표준적인 유교 사상입니다! 저는 2007년에 중국 역사를 공부할 때 천명(天命)에 대해 배웠던 기억이 납니다. 하지만 2020년으로 넘어오면서 이 대사는 플레이 테스터들 사이에서 놀라운 비중을 차지하게 되었습니다. 갑자기 이 대사는팬데믹이라는구체적인 상황에 관한 것이었습니다.

  
"아하!" 플레이 테스터들은 "공자가 \[선택한 지도자 삽입\]의 실패로 상황이 이렇게 나빠지는 것을 막지 못했다고 외치고 있군요! 그들이 지는 게 마땅하다고 말하는 거예요!"라고 말합니다. 그들은 의도적인 연결인지 의심 하지 않았습니다. 연결이너무도 분명했기 때문이죠. 제가 의도한 것은 아니었지만 이러한 연결은 사람들의 흥미와 관심을 끌었고, 이 오래된 아이디어가 현재에도 유효하다는 증거였습니다!

하지만 2024년까지 플레이 테스트를 계속한 결과, 이 공자 대사는 이제 거의 언급되지 않습니다. 대사는 전혀 바뀐 것이 아니라 세상이 바뀌었기 때문입니다. 이제 게임의 다른 부분이 튀어나와 새로운 갈등과 사건으로 연결됩니다. 다음 레슨으로 이어집니다...

## 레슨 5: 시사의 흐름에 저항하기

지역적이든 국제적이든, 과거든 현재든, 어떤 위기의 이름을 대면프로 철학자 2에서 "그것에 관한"무언가를 찾을 수 있을 것입니다. 우리는 의도적으로 거대하고 반복되는 패턴과 갈등을 다루는 철학자를 선택했는데, 결국 이러한 패턴 중 상당수가 지금 일어나고 있기 때문입니다. 이것이 이 게임을 만들 가치가 있는 이유의 큰 부분입니다.

잠재적으로 이 게임에 기대야 할 이유가 있었습니다. 보다 노골적인 화제성은 입소문을 내고 마케팅에 도움이 될 수 있으며, 인디 게임은 얻을 수 있는 모든 이점이 필요합니다. 하지만 로크에게 정부의 책임이 트럼프의 재판에 어떻게 적용되는지 묻는 게임 버전은 장기적으로는 더 나쁠 것입니다. 왜냐하면 이 글을 쓰는 지금 이 순간에도 이러한 구체적인 내용은 뜨겁지만 곧 어제의 뉴스가 될 것이기 때문입니다.

하지만 앞서 살펴본 바와 같이 과거와 현재 사이의 경계는 전체 게임을 더욱 설득력 있게 만듭니다. 그래서 저희는 프레임 내러티브에서 이러한 유사점을 끌어내기 위해 주인공의 어머니인 피티아 스미스를 정치인으로 바꾸는 등 여러 가지 선택을 했습니다. 그녀의 경험은 이러한 패턴의 구체적이고 현대적인 예시 , 즉현재의 많은 상황과 비슷하지만 꼭 그렇지는않은 이야기를 만들어냅니다 .그리고 파이시아가 자신의 경험과 논증을 연결하면서 플레이어도 그렇게 하도록 독려합니다.

요컨대 ,프로 필로소피 2는 핫 테이크용 게임이 아닙니다. 이 게임은 느리게 요리된 테이크를 위한 게임입니다. 텍스트에 명백한 선을 긋는 것은 어제의 문제에 머물게 하는 반면, 플레이어가 스스로 연결 짓는 것을 신뢰하면 앞으로 다가올 모든 날에 관련성을 부여할 수 있습니다.

## 그래서... 그만한 가치가 있었나요?

게임 개발이 시작된 이후 팬데믹, 몇 차례의 격동적인 세계 선거, 자연재해, 잔혹한 전쟁이 있었습니다. 저희는 최선을 다하고 있지만 세상은 복잡하고 어수선합니다. 여기서 얻은 교훈 중 상당수가 "통제할 수 없다는 사실을 인정하라"는 것으로 요약됩니다.

하지만 그렇게 많은 것을 받아들인 후에도: 네, 그만한 가치가 있습니다.

몇 년 전에초기 빌드를 플레이 테스트한 사람들은 저에게 메시지를 보내 게임에 대해 얼마나 생각하는지 알려주곤 합니다.가족 및 친구들과 아이디어에 대해 어떻게 토론했는지, 지금 일어나는 갈등을 더 잘 이해할 수 있는 렌즈를 제공했는지. 어려운 시기에 우리의 바보 같은 농담이 어떻게 떠올랐는지. 단 몇 명이라도 더 많은 사람들이 이러한 경험을 통해 현재의 문제에 대처할 수 있는 더 나은 도구를 얻게 된다면, 우리는 중요한 일을 해낸 것입니다.

우리는 최선을 다하고 있습니다. 아무것도 하지 않는 것보다는 낫죠.

자세히 읽어보세요:

[주요](https://www.gamedeveloper.com/keyword/featured-blogs)[블로그블로그문화톱](https://www.gamedeveloper.com/keyword/culture)[스토리](https://www.gamedeveloper.com/keyword/top-stories)

[](https://www.linkedin.com/sharing/share-offsite/?url=https://www.gamedeveloper.com/design/lessons-from-the-political-minefield-of-pro-philosopher-2)[](https://www.facebook.com/sharer/sharer.php?u=https://www.gamedeveloper.com/design/lessons-from-the-political-minefield-of-pro-philosopher-2)[](https://www.twitter.com/intent/tweet?url=https://www.gamedeveloper.com/design/lessons-from-the-political-minefield-of-pro-philosopher-2)[](https://www.gamedeveloper.com/cdn-cgi/l/email-protection#cef1bdbbaca4abadbaf382abbdbda1a0bdeea8bca1a3eebaa6abee9ea1a2a7baa7adafa2ee83a7a0aba8a7aba2aaeea1a8ee9ebca1ee9ea6a7a2a1bda1bea6abbceefce8afa3bef5aca1aab7f387ebfcfebaa6a1bba9a6baebfcfebaa6abebfcfea8a1a2a2a1b9a7a0a9ebfcfea8bca1a3ebfcfe89afa3abebfcfe8aabb8aba2a1beabbcebfcfea3a7a9a6baebfcfea7a0baabbcabbdbaebfcfeb7a1bbe0ebfe8aebfe8febfe8aebfe8febfcfe82abbdbda1a0bdebfcfea8bca1a3ebfcfebaa6abebfcfe9ea1a2a7baa7adafa2ebfcfe83a7a0aba8a7aba2aaebfcfea1a8ebfcfe9ebca1ebfcfe9ea6a7a2a1bda1bea6abbcebfcfefcebfe8aebfe8fa6bababebdebfd8febfc88ebfc88b9b9b9e0a9afa3abaaabb8aba2a1beabbce0ada1a3ebfc88aaabbda7a9a0ebfc88a2abbdbda1a0bde3a8bca1a3e3baa6abe3bea1a2a7baa7adafa2e3a3a7a0aba8a7aba2aae3a1a8e3bebca1e3bea6a7a2a1bda1bea6abbce3fc)[](https://www.reddit.com/submit?url=https://www.gamedeveloper.com/design/lessons-from-the-political-minefield-of-pro-philosopher-2&title=Lessons%20from%20the%20Political%20Minefield%20of%20Pro%20Philosopher%202)

## 저자 소개

[![Connor Fallon](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt7ce731765a3f128b/65087eb422641ec82885b962/Connor_Fallon.jpg?width=400&auto=webp&quality=80&disable=upscale "Connor Fallon")](https://www.gamedeveloper.com/author/connor-fallon)

[

코너 팰런

](https://www.gamedeveloper.com/author/connor-fallon)

Blogger

[코너 팰런의 더보기](https://www.gamedeveloper.com/author/connor-fallon)

게임 개발자의 일일 뉴스, 개발자 블로그, 스토리를 받은 편지함으로 바로 받아보세요.

[최신 소식 받기](https://gd-resources.gamedeveloper.com/free/w_gamf01/prgm.cgi)

추천 콘텐츠

* * *

원문: [https://www.gamedeveloper.com/design/lessons-from-the-political-minefield-of-pro-philosopher-2](https://www.gamedeveloper.com/design/lessons-from-the-political-minefield-of-pro-philosopher-2)