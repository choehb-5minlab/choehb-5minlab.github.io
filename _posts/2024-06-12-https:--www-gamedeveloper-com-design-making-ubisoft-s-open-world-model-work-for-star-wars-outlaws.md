---
title:  "스타워즈 아웃로즈에 유비소프트의 오픈 월드 모델 적용하기"

categories:
  - 번역
  
tags:
  - Game Developer
toc: true
toc_sticky: true
 
date: 2024-06-12
last_modified_at: 2024-06-12
---
[![Picture of George Yang](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltd709c2f6ad0896cd/657b3aae1fb1b4040a0e1821/Game_Developer_G_Logo_RGB.png?width=100&auto=webp&quality=80&disable=upscale "Picture of George Yang")](https://www.gamedeveloper.com/author/george-yang)

[조지 양](https://www.gamedeveloper.com/author/george-yang), 기여자

6월 12일, 2024

5분 읽기

![Star Wars Outlaws heroine Vess runs and guns while fighting Stormtroopers.](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltf940eba7291977f1/6668b3391329a6c45aef5b36/SWO_UbiFW_station_escape_NoLogo.png?width=850&auto=webp&quality=95&format=jpg&disable=upscale "Star Wars Outlaws heroine Vess runs and guns while fighting Stormtroopers.")

Ubisoft 이미지 제공

[](https://www.linkedin.com/sharing/share-offsite/?url=https://www.gamedeveloper.com/design/making-ubisoft-s-open-world-model-work-for-star-wars-outlaws)[](https://www.facebook.com/sharer/sharer.php?u=https://www.gamedeveloper.com/design/making-ubisoft-s-open-world-model-work-for-star-wars-outlaws)[](https://www.twitter.com/intent/tweet?url=https://www.gamedeveloper.com/design/making-ubisoft-s-open-world-model-work-for-star-wars-outlaws)[](https://www.gamedeveloper.com/cdn-cgi/l/email-protection#310e4244535b5452450c7c505a585f5611645358425e574517124903060a42115e41545f11465e435d55115c5e55545d11465e435a11575e4311624550431166504342117e44455d50464217505c410a535e55480c7814030145595e44565945140301455954140301575e5d5d5e46585f5614030157435e5c14030176505c54140301755447545d5e4154431403015c58565945140301585f455443544245140301485e441f1401751401701401751401701403017c505a585f56140301645358425e574517124903060a421403015e41545f140301465e435d551403015c5e55545d140301465e435a140301575e4314030162455043140301665043421403017e44455d50464214017514017059454541421402701403771403774646461f56505c54555447545d5e4154431f525e5c14037755544258565f1403775c505a585f561c445358425e57451c421c5e41545f1c465e435d551c5c5e55545d1c465e435a1c575e431c424550431c465043421c5e44455d504642)[](https://www.reddit.com/submit?url=https://www.gamedeveloper.com/design/making-ubisoft-s-open-world-model-work-for-star-wars-outlaws&title=Making%20Ubisoft's%20open%20world%20model%20work%20for%20Star%20Wars%20Outlaws)

## 한눈에 보기

*   스타워즈 아웃로즈는 많은 유비소프트 오픈월드 디자인 관습을 차용했지만, 여전히 눈에 띄는 것을 목표로 합니다.

수년 동안 Ubisoft는 넓고 거대한 맵, 수많은 사이드 퀘스트 마커, 플레이어가 발견할 수 있는 랜드마크로 완성되는 오픈 월드 게임 공식으로 유명했습니다. 이 공식은 어쌔신 크리드, 와치 독스, 파 크라이 등 Ubisoft의 대형 프랜차이즈 게임 대부분에서 볼 수 있습니다. 끝이 없어 보이는 콘텐츠에 대한 탐구에서 스타워즈 아웃로즈는 이러한 전철을 밟 고 있는 것으로 보입니다. 하지만 이렇게 거대한 세계를 더욱 친밀하고 촘촘하게 짜인 스토리로 채우는 것은 쉽지 않은 일입니다.

훌륭한 스토리를 전달하려면 게임 개발자는 시각적 연출에 대한 뛰어난 감각이 필요합니다. 그리고 스타워즈처럼 엄격하게 통제되는 라이선스 자산을 다루는 작업에는 항상 고유한 어려움이 있습니다.

Ubisoft 포워드에서 게임 개발자는 스타워즈 아웃로즈를한 시간 동안 플레이하고 , 부월드 디자이너 클로 해먼드와 부 DRT 디렉터 마르테 존커스와 함께 주인공 디자인에 담긴 영감과 스타워즈 미학을 지향하면서도 아웃로즈를 독특하게 보이게 하기 위한 노력에 대해 이야기를 나눌 수 있는 기회를 가졌습니다.

## 스타워즈아웃로즈의 여주인공은 '생존주의자'

스타워즈 아웃로즈는 신인 악당 케이 베스와 그녀의 반려동물 닉스의 이야기를 다룹니다. 케이의 디자인에는 한 솔로에서 영감을 받은 부분이 있지만, 개발자들은 케이가 여전히 신인 도둑이라는 점을 분명히 하고 싶었습니다. 케이의 생존주의적 사고방식과 투박한 성격 덕분에 임시 자물쇠 역할을 하는 머리핀을 비롯해 무엇이든 도구로 만들 수 있습니다. 이러한 작은 디테일이 베스를 훨씬 더 친근하고 현실감 있는 캐릭터로 만들어 줍니다. 베스의 반려동물은 닉스라는 이름의 귀여운 동물로, 아웃로즈에 새롭게 등장한 머카알이라는 종입니다.

닉스는 정글과 같은 환경에서 생존할 수 있는 생물에서 영감을 받아 디자인되었습니다. 예를 들어, 그의 비늘은 혹독한 날씨로부터 그를 보호할 수 있습니다. 닉스 역시 수염이 악솔로틀과 매우 흡사하여 개발팀은 그에게 감정을 표현할 수 있는 무언가를 부여하고자 했습니다. 게임에서 베스는 닉스를 호출하여 적의 주의를 분산시키고 공격하며 물건을 훔칠 수도 있습니다.

![The player character's ship battles TIE Fighters in Star Wars Outlaws.](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltd867561acaec7a19/6668b389e61f656440f4035a/SWO_UbiFW_Trailblazer_combat_NoLogo.png?width=700&auto=webp&quality=80&disable=upscale "The player character's ship battles TIE Fighters in Star Wars Outlaws.")

Ubisoft 이미지 제공.

많은 오픈월드 비디오 게임에는 일반적으로 캐릭터가 돌을 던지거나 로봇이 주변의 전자기기를 단락시켜 적을 유인하는 등 주의를 분산시키는 방법이 있습니다. 아웃로즈에서는 닉스가 바닥에 쭈그리고 누워 있으면 적들이 자신이 무엇을 하고 있는지조차 헷갈려하며 다가오기도 합니다. 이는 닉스에게 개성을 더해주며, 인기 스타워즈 스핀오프 TV 쇼인 만달로리안에서 아기 요다를 닮은 그로구 동료가 폭발적인 인기를 얻은 이후 닉스가 '귀여운' 외계 생명체 트렌드를 구현하는 것은 놀라운 일이 아닙니다.

베스와 닉스의 끊임없는 상호작용은 그들이 가족이며 서로를 끊임없이 돌보고 있다는 느낌을 줍니다.

존커스는 "닉스 스틸이 스타워즈의 세계에서 실제로 살아남을 수 있는 믿을 만한 생명체처럼 느껴지도록 하기 위해 많은 영감을 받았습니다."라고 말합니다. "하지만 동시에 베스에게 아주 좋은 동반자가 될 것입니다."

베스는 자신의 우주선인 트레일블레이저도 이용할 수 있습니다. 닉스처럼 트레일블레이저 역시 실제 동물, 이번에는 겸손한 거북이에서 영감을 받았습니다. 60~70년대 모노레일과 레트로 퓨처리즘의 힌트, 즉 조지 루카스가 스타워즈를 처음 만들던 시대의 미래 모습을 상상하는 데 영향을 받은 디자인입니다. 당시 사람들은 하늘을 나는 자동차와 로봇 하인이 있는 2000년대 미래를 상상했는데, 스타워즈의 미래와 크게 다르지 않죠.

행성에서 베스는 스피더라는 모터크로스를 탈 수 있는데, 존커스는 이 역시 레트로한 미래 스타일에서 영감을 받았다고 덧붙였습니다. "모든 스타워즈 디자인에는 친숙함이 있습니다."라고 그녀는 말합니다. "하지만 이국적이고 외계적인 요소도 적지 않습니다." 레트로 퓨처리즘은 1800년대 후반에 뿌리를 두고 있지만, 우주 시대가 열린 60년대와 스타워즈가 문화 현상으로 자리 잡은 70년대까지 이어졌습니다.

## 새로운 세상 만들기

데모에는 게임플레이의 오픈 월드 부분이 포함되지 않았지만, 해먼드는 팀이 세 가지 독특한 방식으로 오픈 월드 콘텐츠를 제작하고자 했다고 설명했습니다. 첫 번째는 플레이어가 베스 같은 악당이 관심을 가질 만한 대화와 소문을 엿들을 수 있는 밀집된 도시를 만드는 것이었습니다. 베스는 정보를 얻고 캐릭터를 추적하여 새로운 기술을 배울 수 있으므로 플레이어가 오픈월드 활동에 참여하도록 게임플레이 동기를 부여할 수 있습니다.

두 번째 방법은 차량과 이동을 이용하는 것입니다. 트레일블레이저를 통해 플레이어는 새로운 우주 정거장과 궤도 지역을 발견할 수 있습니다. 이 측면에서 눈에 띄는 점은 플레이어가 탑승 옵션이 나타나기 전에 실제로 행성을 향해 더 가까이 비행할 수 있다는 것인데, 이는스타필드나 매스 이펙트같은 게임에서처럼 행성을 선택하고 착륙을 선택하는 것보다 훨씬 더 매력적인 게임플레이 기능입니다 .

세 번째 측면은 베스가 여행하는 동안 마주치는 행성의 멋진 환경과 넓은 풍경을 전달하는 것이었습니다. 데모에서는 베스를 열대 및 눈 덮인 환경을 포함한 다양한 생물권에 배치하여 플레이어가 기대할 수 있는 다양한 환경을 엿볼 수 있도록 했습니다.

![Star Wars Outlaws player character Vess and her animal companion explore a factory.](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt973f42b985331b84/6668b3c67d25f49ace4b2fa9/SWO_UbiFW_Reactor_Grapple_NoLogo.png?width=700&auto=webp&quality=80&disable=upscale "Star Wars Outlaws player character Vess and her animal companion explore a factory.")

Ubisoft 이미지 제공.

겉으로 보기에스타워즈 아웃로즈는 완료해야 할 활동 체크리스트가 있는 전형적인 유비소프트 오픈 월드 공식에 스타워즈 스킨을 적용한 것처럼 보입니다. 하지만 베스와 닉스 사이의 관계는 플레이어가 전체 여정에서 계속 투자하게 만드는 요소입니다. 또한 개발사 Massive Entertainment가 이 세계를 만드는 데 많은 정성을 쏟았다는 것도 분명합니다.

해먼드는 베스와 외계인 조수를 암시하며 "그들은 신인 도둑 듀오로 시작하여 지하 세계를 탐험하게 될 것입니다."라고 말했습니다. "저희는 다양성을 제공한다고 생각합니다. 장소, 퀘스트, 다양한 캐릭터 등 모든 것이 우리가 하고자 하는 진정한 스토리텔링에 맞춰져 있습니다."

자세히 알아보기

[2024 서머 게임 페스트톱](https://www.gamedeveloper.com/keyword/summer-game-fest)[스토리인터뷰](https://www.gamedeveloper.com/keyword/interviews)

[](https://www.linkedin.com/sharing/share-offsite/?url=https://www.gamedeveloper.com/design/making-ubisoft-s-open-world-model-work-for-star-wars-outlaws)[](https://www.facebook.com/sharer/sharer.php?u=https://www.gamedeveloper.com/design/making-ubisoft-s-open-world-model-work-for-star-wars-outlaws)[](https://www.twitter.com/intent/tweet?url=https://www.gamedeveloper.com/design/making-ubisoft-s-open-world-model-work-for-star-wars-outlaws)[](https://www.gamedeveloper.com/cdn-cgi/l/email-protection#7a45090f18101f190e47371b1113141d5a2f181309151c0e5c5902484d41095a150a1f145a0d1508161e5a17151e1f165a0d1508115a1c15085a290e1b085a2d1b08095a350f0e161b0d095c1b170a4118151e0347335f484a0e12150f1d120e5f484a0e121f5f484a1c151616150d13141d5f484a1c0815175f484a3d1b171f5f484a3e1f0c1f16150a1f085f484a17131d120e5f484a13140e1f081f090e5f484a03150f545f4a3e5f4a3b5f4a3e5f4a3b5f484a371b1113141d5f484a2f181309151c0e5c5902484d41095f484a150a1f145f484a0d1508161e5f484a17151e1f165f484a0d1508115f484a1c15085f484a290e1b085f484a2d1b08095f484a350f0e161b0d095f4a3e5f4a3b120e0e0a095f493b5f483c5f483c0d0d0d541d1b171f1e1f0c1f16150a1f08541915175f483c1e1f09131d145f483c171b1113141d570f181309151c0e570957150a1f14570d1508161e5717151e1f16570d150811571c150857090e1b08570d1b080957150f0e161b0d09)[](https://www.reddit.com/submit?url=https://www.gamedeveloper.com/design/making-ubisoft-s-open-world-model-work-for-star-wars-outlaws&title=Making%20Ubisoft's%20open%20world%20model%20work%20for%20Star%20Wars%20Outlaws)

## 저자 소개

[![George Yang](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltd709c2f6ad0896cd/657b3aae1fb1b4040a0e1821/Game_Developer_G_Logo_RGB.png?width=400&auto=webp&quality=80&disable=upscale "George Yang")](https://www.gamedeveloper.com/author/george-yang)

[

조지 양

](https://www.gamedeveloper.com/author/george-yang)

기고자

[George Yang에서 더 보기](https://www.gamedeveloper.com/author/george-yang)

게임 개발자의 일일 뉴스, 개발자 블로그, 스토리를 받은 편지함으로 바로 받아보세요.

[최신 소식 받기](https://gd-resources.gamedeveloper.com/free/w_gamf01/prgm.cgi)

추천 콘텐츠

* * *

원문: [https://www.gamedeveloper.com/design/making-ubisoft-s-open-world-model-work-for-star-wars-outlaws](https://www.gamedeveloper.com/design/making-ubisoft-s-open-world-model-work-for-star-wars-outlaws)