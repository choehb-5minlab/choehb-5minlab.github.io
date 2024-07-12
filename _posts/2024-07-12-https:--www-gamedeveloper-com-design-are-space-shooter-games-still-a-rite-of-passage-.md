---
title:  "우주 슈팅 게임은 여전히 '통과의례'인가요?"

categories:
  - 번역
  
tags:
  - Game Developer
toc: true
toc_sticky: true
 
date: 2024-07-12
last_modified_at: 2024-07-12
---
[![Picture of Andrew Sataiyah](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltd709c2f6ad0896cd/657b3aae1fb1b4040a0e1821/Game_Developer_G_Logo_RGB.png?width=100&auto=webp&quality=80&disable=upscale "Picture of Andrew Sataiyah")](https://www.gamedeveloper.com/author/andrew-sataiyah)

[앤드류 사타이야](https://www.gamedeveloper.com/author/andrew-sataiyah)

7월 12, 2024

9 분 읽기

![](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blte214b3fd5e0456f7/668ffc18b6a60d937ac2501f/space_invaders_taito_1978.png?width=1280&auto=webp&quality=95&format=jpg&disable=upscale)

[](https://www.linkedin.com/sharing/share-offsite/?url=https://www.gamedeveloper.com/design/are-space-shooter-games-still-a-rite-of-passage-)[](https://www.facebook.com/sharer/sharer.php?u=https://www.gamedeveloper.com/design/are-space-shooter-games-still-a-rite-of-passage-)[](https://www.twitter.com/intent/tweet?url=https://www.gamedeveloper.com/design/are-space-shooter-games-still-a-rite-of-passage-)[](https://www.gamedeveloper.com/cdn-cgi/l/email-protection#39064a4c5b535c5a4d04784b5c194a49585a5c194a5156564d5c4b195e58545c4a194a4d505555191f1a410b0e0258194b504d5c19565f1949584a4a585e5c1f1a410b0e02061f585449025b565d4004701c0b094d51564c5e514d1c0b094d515c1c0b095f565555564e50575e1c0b095f4b56541c0b097e58545c1c0b097d5c4f5c5556495c4b1c0b0954505e514d1c0b0950574d5c4b5c4a4d1c0b0940564c171c097d1c09781c097d1c09781c0b09784b5c1c0b094a49585a5c1c0b094a5156564d5c4b1c0b095e58545c4a1c0b094a4d5055551c0b091f1a410b0e02581c0b094b504d5c1c0b09565f1c0b0949584a4a585e5c1f1a410b0e021c0a7f1c097d1c0978514d4d494a1c0a781c0b7f1c0b7f4e4e4e175e58545c5d5c4f5c5556495c4b175a56541c0b7f5d5c4a505e571c0b7f584b5c144a49585a5c144a5156564d5c4b145e58545c4a144a4d5055551458144b504d5c14565f1449584a4a585e5c14)[](https://www.reddit.com/submit?url=https://www.gamedeveloper.com/design/are-space-shooter-games-still-a-rite-of-passage-&title=Are%20space%20shooter%20games%20still%20'a%20rite%20of%20passage'%3F)

비디오 게임 업계에는 "우주 슈팅 게임은 통과의례"라는 오래된 속담이 있습니다. 이 말은 아마도 게임 개발자들 사이에서 "쉽게 만들 수 있다"는 기본 개념으로 인기를 얻었지만 ,많은 인디 개발자들은 "가서 탁구를 만들어라"와 비슷한 말을 할 것입니다. 저는 이 두 가지를 모두 해본 사람으로서(물론 상업용 게임은 우주 슈팅 게임 하나만 출시했고 개인 프로젝트는 꽤 많이 했지만요) 게임 개발자 커뮤니티에 '1인 인디' 게임 개발에 뛰어든 계기에 대한 제 생각을 알려드리려고 합니다. 제가 5살 때인 90년대 \*기침\* \*기침\* 때부터 게임 개발자가 되고 싶었기 때문에 개인 프로젝트에 대해서는 자세히 설명하지 않겠습니다.

## 인디로 가자.

![Indie_game_dev_the_movie_.jpg](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltdbafece3309044bd/668ffc707ee21059e8655f88/Indie_game_dev_the_movie_.jpg?width=700&auto=webp&quality=80&disable=upscale "Indie_game_dev_the_movie_.jpg")

기침에 대해 말하자면, 올해는 2020년이었고, 코로나19가 막 닥쳤고, 막내를 학교에 보내고 나서 "비디오 게임을 만들어야겠다"고 스스로에게 말한 직후 영국은 마침내 이를 '진지하게' 받아들이기 시작했습니다 - 슈퍼마켓이 약탈당하고 당시 모든 아이들을 홈스쿨링하게 된 후 최초의 상업 비디오 게임처럼요.

그래서 어디서부터 시작했나요? 정말 오래 전 일인 것 같지만 저는 게임 엔진을 다운로드하는 것부터 시작했습니다: 고닷, 유니티, 게임 메이커. 각 엔진의 이용 약관을 읽어보고 어떤 것이 "자신의 필요에 맞는지" 또는 "가장 쉽게 적응할 수 있는지" 알아보기 위해 이 접근 방식을 사용하는 것이 좋습니다 - PS: 저는 Game maker로 결정했습니다. 다른 엔진이 나쁘다는 것은 아니지만 2D 게임으로 시작하려고 했는데 게임 메이커 워크플로가 저에게 '딱' 맞았습니다(물론 90년대에 사용했던 RPG 메이커 등 다른 엔진도 있습니다).

![Pong.png](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt1767ec5a9d3d254d/668ffc82371c561fe33617dc/Pong.png?width=700&auto=webp&quality=80&disable=upscale "Pong.png")

(인디 게임 개발자가 된 후) 처음 만들려고 했던 게임은 퐁이었는데 , 앞서 언급한모든 엔진의튜토리얼을 따라 해도 실제로는 실패했습니다 . 그러던 중 '친절한 우주비행사'가 게임 메이커 엔진을 사용하여 '우주 바위'라는 소행성 클론을 만드는 튜토리얼을 발견했습니다. 그 튜토리얼 이후 엔진이 업데이트되었다는 사실을 깨닫고 몇 주 동안 키보드로 머리를 두드렸습니다: 드디어 소행성 클론을 만들었습니다. 완벽한 클론이었나요? 아니요, 여기저기 프로그래머용 덕트 테이프를 붙인 정도였죠. 소행성 클론 이후에는 스페이스 인베이더와 같은 튜토리얼을 사용하지 않고 퐁 및 기타 우주 슈팅 게임 클론을 몇 개 만들었습니다.

이 모든 것에서 무엇을 배웠나요? 새로운 것을 처음 시도하는 것은 매우 어색하고 험난하다는 것입니다. 저는 레벨 디자인이 아닌 '인디' 게임 개발에 뛰어들기 전에는 픽셀 아트 커미션을 맡곤 했는데, 새로운 커미션을 할 때마다 한 번도 시도하지 않은 일을 하는 것 같았어요. 수년 전에는 C#과 C++를 배우려고 했지만 하루나 이틀 만에 포기한 적도 있었습니다(포기하지 마세요). 이번에는 그 어떤 것도 저를 막을 수 없었고, 몇 년이 지난 지금은 아트, 애니메이션, 사운드 FX, 성우, 프로그래밍 등 개인 또는 소규모 팀으로 여러 가지 모자를 쓸 준비를 하고 있습니다! 심지어 첫 상업용 게임인 '크리스탈 혜성'을 위해 고용한 몇 명의 직원들을 관리해야 했는데, 다행히 다른 업계에서 슈퍼바이저로 일해본 경험이 있었어요!

## 제 첫 상업용 우주 슈팅 게임.

![Crystal_Gameplay_Screenshot_1920_x_1080.png](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt965b32e3312373c0/668ffce03599c83e93974199/Crystal_Gameplay_Screenshot_1920_x_1080.png?width=700&auto=webp&quality=80&disable=upscale "Crystal_Gameplay_Screenshot_1920_x_1080.png")

여기서부터 일이 꼬이기 시작합니다! "크리스탈 혜성"은 제가 만들고 싶었던 게임이었으며(스타폭스64와 레프트4데드의 팬으로서 인공지능 팀원을 사용했습니다), 당시에는 일종의 특이한 '보너스'처럼 보였지만 저에게는 "통과의례"로 여겨지지 않았습니다. 하지만 이 장르의 다른 게임들을 살펴볼까요? 다음과 같은 게임이 있습니다: Jamestown+, 제로 레인저, 죽음의 미소 및 시쿄 게임과 같은 오래된 인기 게임 등이 있습니다. 이 게임들 중 일부는 해당 장르뿐만 아니라 다른 장르에서도 가장 아름다운 게임입니다! "슈밍" 장르에는 치열한 경쟁이 있으며, 팬층은 좋아하는 것과 싫어하는 것에 대해 매우 구체적이어서 종종 "틈새 속의 틈새"에 빠지는 경우가 많습니다. 잠재적으로 만들 수 있는 슈팅 게임의 유형은 무궁무진합니다. 저는 "수직형 트윈 스틱 슈터 카테고리"에 속했는데, 조금만 시장 조사를 했더라면 이런 재앙을 피할 수 있었을 거예요!

![Jamestown_.jpg](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltd464b237a7aabcf5/668ffcec732a2022f4d80d6c/Jamestown_.jpg?width=700&auto=webp&quality=80&disable=upscale "Jamestown_.jpg")

수평 슈팅, 수직 슈팅, 복고풍 슈팅, 총알 지옥, '유로' 슈팅(장르 팬들 사이에서 비하하는 용어) 등이 있습니다. 일부 팬들은 '슈팅'이라는 용어를 싫어하기도 하지만, '슈팅'이라는 태그는 이미오래 전에 1인칭 및 3인칭 슈팅 게임에 의해 과밀화되었습니다 . 그리고 불량배 같은 종류도 있습니다. 예를 들어, 뱀파이어 생존자가 오는 것을 본 사람이 있나요? "총알 천국"? 글쎄요, 저는 그랬지만 재미있는 점은 순수한 팬들 사이에서는 "슈머"가 아니라 "슈머 인접" 게임으로 간주된다는 것입니다 - 장르의 일부 팬들은 심지어 그런 말조차도 저에게 화를 낼 수도 있습니다!

![vampire_survivors.jpg](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltaa8cc1e60eb65120/668ffcf78397a061a621c8d6/vampire_survivors.jpg?width=700&auto=webp&quality=80&disable=upscale "vampire_survivors.jpg")

모두 나쁜 소식인가요? 솔직히 첫 상업용 게임으로 게임을 만들면 비상업용 게임에 비해 더 많은 것을 배울 수 있습니다. '쉬업'을 만들 때의 장점은 게임 디자인에 대해 많은 것을 배울 수 있는소수지만 매우 충 실한 유저층이 있다는 것입니다. 그러나 상업성 측면에서는 특정 장르를 더 많이 만들수록 해당 장르의 잠재 고객이 더 많이 늘어날 수 있습니다. 예를 들어 최근에 꽤 잘 팔린 "황혼의 천사"라는 게임이 있습니다! - 개발자가 '슈팅' 장르의 게임을 개발한 지 꽤 오래 된 것 같지만요. 하지만 어떤 장르는 다른 장르보다 수요가 더 많다고 말씀드리고 싶습니다. "슈팅" 또는 "슈팅" 장르는 출시되는 많은 게임과 함께 상업성 측면에서 다소 "과포화" 상태입니다.

또 다른 "슈팅" 게임을 만들게 되나요? - 그럴 가능성은 낮습니다(원래 Crystal 혜성이 3부작이 되기를 바랐던 열정적인 프로젝트가 아니라면요). 두 곳의 퍼블리셔로부터 연락을 받았지만(솔직히 나쁘지 않습니다), 퍼블리셔는 '누가 물리는지' 보기 위해 낚싯줄을 많이 던진다는 점을 기억해야 합니다 - 여전히 아무것도 얻지 못할 수도 있습니다. 크리스탈 혜성의 초기 판매량은 아마도 다른 경쟁작을 뛰어넘기에는 충분하지 않을 것입니다. 설령 제가 다른 게임을 만들 수 있도록 '죽어라' 기다리는 '슈퍼 팬'이 있다고 해도, 미안하지만 그 정도 매출로는 크리스탈 혜성 게임을 만들어서 먹고 살 수 없을 것입니다.

첫 번째 우주 슈팅 게임을 상업용 프로젝트로 개발하면서 무엇을 배웠나요? 그 자체로 한 편의 기사가 될 수 있는 만큼 요약된 '클리프 노트'를 알려드리겠습니다. 모든 게임을 만드는 것은 어려운 일이며, 특히 오늘날과 같은 시대에는 더욱 그렇습니다. 플레이어는 더 많은 것을 기대하며, 기술은 크게 발전했고, 그 결과 모든 게임의 품질 기준이 크게 높아졌습니다. 만약제가 2010년에 크리스탈 혜성을 출시했더라면 괜찮았을지도 모릅니다. 하지만 앞서 말했듯이 상업용 게임은 비상업용 게임에서 배울 수 없는 것을 가르쳐 줍니다(저는 비상업용 프로젝트를 많이 만들었지만 어떤 일이 일어날지 전혀 예상하지 못했습니다).

하지만 논의를 위해 시간을 절약할 수 있는 몇 가지 사항을 '요점'으로 정리해 보겠습니다:

1.  혼자서 풀 게임을 '대부분' 만드는 것은 생각보다 훨씬 더 어려울 것입니다. 원래 저는 Crystal comet이 약 9개월 정도 걸릴 것이라고 생각했습니다. 이 게임은 2020년에 시작되어 2024년에 완성되었습니다.
    
2.  무엇이든하기 전에 타겟층을 조사하세요 \- 그들은 특정한 것을 좋아합니다. 그들이 원하는 것을 제공하세요!
    
3.  "처음부터 아트" - 게임 플레이 자체보다 게임의 아트가 더 중요할 수 있다는 말은 정말 가슴 아픈 말입니다.
    
4.  최대한 빨리 초기 반응을 얻으세요. 제 게임은 '파티 갈라가'로 인식되었는데, 개발 막바지에야 그 사실을 알았더라면 좋았을 텐데요! 역사상가장 유명한 슈팅 게임중 하나에 약간의 반전이 있는 것은 나쁘지 않아요!
    
5.  스토어 페이지를 최대한 빨리 설정하여 초반에 얼마나 잘 진행되고 있는지 파악하세요. 반응 등에 따라 필요한 경우 기능을 줄이세요. 필요한 경우 출시일을 앞당기고 가격을 낮추고 계속 진행하세요. 그렇지 않다면 그렇게 하지 않는 것이 훨씬 더 나은 상황입니다.
    
6.  보너스 팁: 여러분보다 더 많은 경험을 가진 사람들의 조언에 귀를 기울이세요. 저는 어렸을 때부터 직접 게이머가 되어서 더 잘 안다고 생각하며 수많은 조언을 무시했지만, 그것만으로는 충분하지 않았습니다! 하지만 훨씬 더 큰 회사를 위한 조언이 나에게 직접적으로 적용되지 않는 경우도 있습니다. 솔로라면 정말 솔로입니다. 일부 1인 개발자나 듀오 개발자는 출시 전 오랜 기간 동안 위시리스트를 쌓으며 게임을 개발하기도 합니다.
    

*   물론 제가 배운 것이 훨씬 더 많지만 지금은 '단순하게 바보처럼'이라는 말로 마무리하겠습니다.
    

![In_a_galaxy_far_far_away.png](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt93c34d0d0972ec19/668ffd068397a03ae021c8da/In_a_galaxy_far_far_away.png?width=700&auto=webp&quality=80&disable=upscale "In_a_galaxy_far_far_away.png")

## 결론

우주 슈팅 게임은 통과의례인가요? 그렇다, 아니다. 이론적으로 우주 슈팅 게임은 '공기 견적'입니다: "만들기는 쉽지만" '상업적' 규모는 아닙니다. 게임 잼 게임과 상업용 게임의 차이를 평가할 때와 같은 맥락입니다. 장르를 불문하고 상업용 게임은 취미용 프로젝트나 학습용 프로젝트보다 훨씬 더 많은 것을 필요로 합니다. '크리스탈 혜성'에 컨트롤러 리매핑을 추가할 때만 해도 처음부터 코딩하는 데 몇 달은 아니더라도 몇 주가 걸릴 줄은 몰랐습니다(폴리싱, 디버깅 및 플레이 테스트 등을 고려하면). 게임 개발자 모임에서 다른 개발자에게 "일주일은 걸릴 줄 알았다"고 말했더니 웃으며 고개를 절레절레 흔들더군요. 결론적으로, 게임을 시작할 때 만들 수 있는 게임은 간단할수록 좋습니다! 지난 몇 년 동안 Crystal 혜성을 만드는 동안 저를 바쁘게 했던 '슈멉' 인디 개발자들이 '대박' 게임을 만들고 있으니 '실행 가능한 상업 프로젝트'를 고려할 때는 경쟁작을 살펴보고 어떤 게임인지 정확히 파악하는 것이 좋습니다.

![RewdanSpritesSplashScree.png](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blte43521d75a22b0e6/668ffd17874ac76c67c42f24/RewdanSpritesSplashScree.png?width=700&auto=webp&quality=80&disable=upscale "RewdanSpritesSplashScree.png")

## 레단스프릿의 다음 계획은 무엇인가요?

현재 다음 프로젝트를 준비 중입니다. 20년 동안 게임 업계에 뛰어들었다가 실패하고 지금은 '인디 게임 개발'에 빠져 있지만 아직 포기하지 않았어요! (그리고 앞으로도 절대 포기하지 않을 것입니다). 따라서 게임 회사에서 언제 그만둘지 모르는 사람을 찾는다면 저는 훌륭한 레벨 디자이너가 될 것입니다(저는 플랫포머 및 아레나 슈팅 게임 장르에서 수천 개는 아니더라도 수백 개를 만들었고 대회에서도 좋은 성적을 거뒀습니다). 하지만 그 외에는 그냥 인디 게임을 계속 만들 것 같아요.

## 저를 어디서 찾을 수 있나요?

유튜브: [https://www.youtube.com/@RewdanSprites](https://www.youtube.com/@RewdanSprites)

트위터/X: [https://x.com/RewdanSprites](https://x.com/RewdanSprites)

비디오 게임 "크리스탈 혜성": [https://store.steampowered.com/app/2642920/Crystal\_Comet/](https://store.steampowered.com/app/2642920/Crystal_Comet/)

이메일 [\[이메일 보호\]](https://www.gamedeveloper.com/cdn-cgi/l/email-protection)

자세히 알아보기:

[추천](https://www.gamedeveloper.com/keyword/featured-blogs)[블로그블로그톱](https://www.gamedeveloper.com/keyword/blogs)[스토리](https://www.gamedeveloper.com/keyword/top-stories)

[](https://www.linkedin.com/sharing/share-offsite/?url=https://www.gamedeveloper.com/design/are-space-shooter-games-still-a-rite-of-passage-)[](https://www.facebook.com/sharer/sharer.php?u=https://www.gamedeveloper.com/design/are-space-shooter-games-still-a-rite-of-passage-)[](https://www.twitter.com/intent/tweet?url=https://www.gamedeveloper.com/design/are-space-shooter-games-still-a-rite-of-passage-)[](https://www.gamedeveloper.com/cdn-cgi/l/email-protection#c7f8b4b2a5ada2a4b3fa86b5a2e7b4b7a6a4a2e7b4afa8a8b3a2b5e7a0a6aaa2b4e7b4b3aeababe7e1e4bff5f0fca6e7b5aeb3a2e7a8a1e7b7a6b4b4a6a0a2e1e4bff5f0fcf8e1a6aab7fca5a8a3befa8ee2f5f7b3afa8b2a0afb3e2f5f7b3afa2e2f5f7a1a8ababa8b0aea9a0e2f5f7a1b5a8aae2f5f780a6aaa2e2f5f783a2b1a2aba8b7a2b5e2f5f7aaaea0afb3e2f5f7aea9b3a2b5a2b4b3e2f5f7bea8b2e9e2f783e2f786e2f783e2f786e2f5f786b5a2e2f5f7b4b7a6a4a2e2f5f7b4afa8a8b3a2b5e2f5f7a0a6aaa2b4e2f5f7b4b3aeababe2f5f7e1e4bff5f0fca6e2f5f7b5aeb3a2e2f5f7a8a1e2f5f7b7a6b4b4a6a0a2e1e4bff5f0fce2f481e2f783e2f786afb3b3b7b4e2f486e2f581e2f581b0b0b0e9a0a6aaa2a3a2b1a2aba8b7a2b5e9a4a8aae2f581a3a2b4aea0a9e2f581a6b5a2eab4b7a6a4a2eab4afa8a8b3a2b5eaa0a6aaa2b4eab4b3aeababeaa6eab5aeb3a2eaa8a1eab7a6b4b4a6a0a2ea)[](https://www.reddit.com/submit?url=https://www.gamedeveloper.com/design/are-space-shooter-games-still-a-rite-of-passage-&title=Are%20space%20shooter%20games%20still%20'a%20rite%20of%20passage'%3F)

## 저자 소개

[![Andrew Sataiyah](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltd709c2f6ad0896cd/657b3aae1fb1b4040a0e1821/Game_Developer_G_Logo_RGB.png?width=400&auto=webp&quality=80&disable=upscale "Andrew Sataiyah")](https://www.gamedeveloper.com/author/andrew-sataiyah)

[

앤드류 사타이야

](https://www.gamedeveloper.com/author/andrew-sataiyah)

[더보기 앤드류 사타이야](https://www.gamedeveloper.com/author/andrew-sataiyah)

게임 개발자의 일일 뉴스, 개발자 블로그, 이야기를 받은 편지함으로 바로 받아보세요.

[최신 소식 받기](https://gd-resources.gamedeveloper.com/free/w_gamf01/prgm.cgi)

추천 콘텐츠

* * *

원문: [https://www.gamedeveloper.com/design/are-space-shooter-games-still-a-rite-of-passage-](https://www.gamedeveloper.com/design/are-space-shooter-games-still-a-rite-of-passage-)