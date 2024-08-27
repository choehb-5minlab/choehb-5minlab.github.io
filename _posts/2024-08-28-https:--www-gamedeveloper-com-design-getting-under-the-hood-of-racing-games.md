---
title:  "레이싱 게임 자세히 알아보기"

categories:
  - 번역
  
tags:
  - Game Developer
toc: true
toc_sticky: true
 
date: 2024-08-28
last_modified_at: 2024-08-28
---
[![Picture of Steve Lycett](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltd709c2f6ad0896cd/657b3aae1fb1b4040a0e1821/Game_Developer_G_Logo_RGB.png?width=100&auto=webp&quality=80&disable=upscale "Picture of Steve Lycett")](https://www.gamedeveloper.com/author/steve-lycett)

[스티브 리셋](https://www.gamedeveloper.com/author/steve-lycett)

2024년 8월 27일

17 분 읽기

![](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt2638a8adf802a111/66cde4955026665eb67a1cfe/GUzApxWXQAAODBa_(1)_(1).jpg?width=1280&auto=webp&quality=95&format=jpg&disable=upscale)

Microsoft 이미지 제공

[](https://www.linkedin.com/sharing/share-offsite/?url=https://www.gamedeveloper.com/design/getting-under-the-hood-of-racing-games)[](https://www.facebook.com/sharer/sharer.php?u=https://www.gamedeveloper.com/design/getting-under-the-hood-of-racing-games)[](https://www.twitter.com/intent/tweet?url=https://www.gamedeveloper.com/design/getting-under-the-hood-of-racing-games)[](https://www.gamedeveloper.com/cdn-cgi/l/email-protection#152a6660777f70766128527061617c7b7235607b71706735617d70357d7a7a71357a73356774767c7b72357274787066337478652e777a716c285c302725617d7a60727d61302725617d70302725737a79797a627c7b7230272573677a783027255274787030272551706370797a657067302725787c727d613027257c7b6170677066613027256c7a603b302551302554302551302554302725527061617c7b72302725607b717067302725617d703027257d7a7a713027257a733027256774767c7b7230272572747870663025513025547d616165663026543027533027536262623b7274787071706370797a6570673b767a783027537170667c727b302753727061617c7b7238607b71706738617d70387d7a7a71387a73386774767c7b72387274787066)[](https://www.reddit.com/submit?url=https://www.gamedeveloper.com/design/getting-under-the-hood-of-racing-games&title=Getting%20under%20the%20hood%20of%20racing%20games)

정말 좋은 레이싱 게임의 운전대를 잡고 처음으로 트랙을 달리는 것만큼 짜릿한 기분은 없습니다. 사실적인 경쟁 레이싱, 빠르고 격렬한 혼돈, 숨막히는 풍경, 라디오에서 흘러나오는 좋은 음악 등 레이싱 게임은 가장 유연하고 적응력이 뛰어나며 오래 지속되는 게임 장르 중 하나입니다.

1974년 5월에 출시된 아타리의 Gran Trak 10을 통해 플레이어가 처음으로 가상 운전석에 앉을 수 있게 된 지 50년이 넘었지만, 이 장르는 계속해서 빠른 속도로 성장해왔으며 시장에서 가장 인기 있는 장르 중 하나로서 그 자리를 놓치지 않고 있습니다.

저는 스모 셰필드의 프랜차이즈 개발 디렉터로서 레이싱 게임에 대해 잘 알고 있습니다. 저는 27년 넘게 레이싱 게임을 개발해왔고요. 27년 이상 레이싱 게임을 개발해왔으며, 그 중 21년은 Sumo에서 근무하면서 Outrun2, Outrun 2006: Coast2Coast, Sonic & All-Stars Racing 등의 게임에 참여했습니다: 트랜스폼드.

이제 레이싱 게임의 인기 요인, 레이싱 게임의 역사, 레이싱 게임 역사의 주요 체크 포인트, 개발자가 게임을 성공으로 이끄는 방법에 대해 자세히 알아봅시다.

## 도로와 당신: 레이싱 게임의 인기

교통 체증도 없고 파란 하늘이 펼쳐지며 좋아하는 음악이 흘러나오는 탁 트인 도로를 달리고 있는 자신을 발견한 적이 있나요? 없나요? 저도 그렇습니다! 우리 대부분은 운전할 때 진정한 자유를 경험할 기회를 얻지 못합니다... 좋아하는 운전 또는 레이싱 게임을 선택하기 전까지는 말입니다.

비디오 게임은 플레이어에게 다양한 경험을 제공하고, 소원을 성취하고, 안전한 환경에서 다양한 감정을 표현할 수 있는 완벽한 매개체입니다. 따라서 현실에서는 꽉 막힌 도로에 갇혀 있지만 게임 속에서는 오프로드 크루징의 꿈을 실현할 수 있습니다.

여기에 레이싱 게임은 플레이어가 본질적으로 이해할 수 있는 비교적 간단한 게임플레이를 제공하고, 말 그대로 수백 가지의 다양한 스타일을 선택할 수 있으며, 캐주얼한 '픽업 앤 플레이' 유저부터 고도로 헌신적인 진행을 추구하는 유저까지 다양한 경험을 제공할 수 있다는 점이 더해져 레이싱 게임은 가장 인기 있고 지속적인 게임 장르 중 하나가 되었습니다.

![SteamDB_racing_games_figures_-_Aug_2024..png](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltdb5f170df066f54e/66cbf43bb23b302c9e4bf7b4/SteamDB_racing_games_figures_-_Aug_2024..png?width=700&auto=webp&quality=80&disable=upscale "SteamDB_racing_games_figures_-_Aug_2024..png")

2024년 8월에 캡처한 자료입니다. 이 볼륨 차트는 2006년부터 2024년 사이에 Steam에 출시된 레이싱 게임을 대상으로 합니다. 슈팅 게임이나 액션 어드벤처와 같은 상위 장르에 비해서는 수치가 크지 않지만, 레이싱 장르의 인기와 규모가 계속 성장하고 있음을 보여주는 좋은 지표입니다.

그리고 일반적으로 플레이어의 요구에 정면으로 맞설 준비가 되어 있는 게임 업계는 이를 잘 알고 있습니다. SteamDB에 따르면 지난 10년간 플랫폼에 레이싱 및 운전 게임이 출시되는 속도는 느리지만 확실하게 증가하여 2014년에는 68개에 불과했지만 2023년에는 538개가 출시될 것으로 예상됩니다. 레이싱이 가장 인기 있는 장르인 슈팅과 액션 어드벤처를 추월하지는 못했지만, 출시되는 게임 수에서는 여전히 플레이어에게 재미와 스릴, 교육적 효과까지 제공하는 장르로서 그 자리를 굳건히 지키고 있습니다.

레이싱에 대한 유니티의 사랑은 게임 산업의 초창기부터 이어져 왔으며, 새로운 하드웨어의 성능과 기능을 가장 잘 보여줄 수 있는 장르 중 하나라고 생각합니다. 1983년 아타리 2600용으로 엔듀로가 출시된 이래로, 오리지널 PlayStation의 출시 타이틀에 레이싱 게임이 포함되는 추세를 보아왔으며, 오리지널 PlayStation은 Ridge Racer, SEGA Saturn은 Daytona USA, Xbox와 Xbox 360 모두 프로젝트 고담 레이싱, 그리고 Wii U는 Sonic & 올스타 레이싱 트랜스폼드 출시 등 게임 콘솔의 출시 타이틀 카탈로그에 레이싱 게임이 포함되는 것을 볼 수 있었습니다! 각 타이틀은 다른 어떤 장르보다 향상된 속도, 가장 반응성이 뛰어난 컨트롤, 놀라운 비주얼을 선보이며 콘솔의 기술적 성능의 한계를 뛰어넘을 수 있습니다.

마지막으로, 스타일과 유연성은 비디오 게임의 인기가 계속 증가하는 주요 이유 중 하나입니다. 실제 트랙에서 순위를 올리고 사실적인 자동차를 운전하는 초현실적인 시뮬레이션 경험을 원하든, 트로피를 차지하기 위해 가족과 친구를 배신하는 멀티플레이어 혼돈을 원하든, 그냥 순항하며 풍경과 환경을 탐험하고 싶든, 여러분에게 맞는 레이싱 게임이 있습니다.

![There’s_something_about_the_sunshine…_a_still_from_the_world_of_Outrun_2006_Coast2Coast._From_the_hyper-realistic_to_cartoon_kart-racers_and_everything_in_between!.png](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltdf894210cd006dc7/66cbf47bac1dab50fc1a89f7/There%E2%80%99s_something_about_the_sunshine%E2%80%A6_a_still_from_the_world_of_Outrun_2006_Coast2Coast._From_the_hyper-realistic_to_cartoon_kart-racers_and_everything_in_between!.png?width=700&auto=webp&quality=80&disable=upscale "There’s_something_about_the_sunshine…_a_still_from_the_world_of_Outrun_2006_Coast2Coast._From_the_hyper-realistic_to_cartoon_kart-racers_and_everything_in_between!.png")

아웃런 2006의 세계관인 햇살에 대한 무언가가 있습니다: Coast2Coast. 초현실적인 레이싱 게임부터 카툰 카트 레이서까지... 그리고 그 사이의 모든 장르의 레이싱 게임은 다양한 스타일, 게임플레이 메커니즘 및 기능을 제공하므로 누구나 즐길 수 있습니다.\]

## 하이라이트 릴 | 레이싱 게임 역사의 상징적인 순간들

저는 게임 업계에서 오랫동안 일해 오면서 시청자가 게임을 접하는 방식, 게임이 만들어지는 방식, 게임이 세상에 받아들여지는 방식을 형성하고 발전시킨 수많은 주요 출시작을 목격해 왔습니다. 즉각적인 히트를 기록한 클래식 게임, 오랜 프랜차이즈에 박차를 가한 게임, 시간이 지났지만 여전히 큰 인기를 누리고 있는 게임 등 많은 타이틀이 레이싱 장르에 속하거나 인접한 것은 당연한 일입니다.

레이싱 게임 역사에서 개발자들의 판도를 바꾼 가장 중요한 순간을 소개합니다:  
  
폴포지션(1982) - 템플릿의 정의:  
폴 포지션은 최초의 아케이드 레이싱 게임은 아니지만, 이후 많은 레이싱 게임의 템플릿을 정의했습니다. 먼저 낮지만 넓은 시야각으로 속도감을 주는 카메라, 로/하이 시프터, 수많은 경쟁자, 그리고 무엇보다도 가장 무서운 적인 시간! 여기에 밝고 화려한 그래픽과 고품질 사운드(그리고 음성까지!)가 더해져 이 게임은 즉각적인 아케이드 히트작이 되었습니다. 당시의 기술을 고려할 때 대단한 업적이며 오늘날 우리가 알고 있는 많은 레이싱 게임의 조상이기도 합니다.  
  
OutRun (1986) - 디지털 소원 성취:  
음, 이 게임을 언급하지 않을 수 없습니다! 레이싱 서킷 대신, 이제 우리는 최고의 여자와 함께 페라리 테스타로사를 타고 석양을 향해 달리는 여행을 떠나고 있습니다. 아웃런은 SEGA의 슈퍼 스케일러 기술로 구동되는 캐논볼 런이라는 놀라운 로드 트립이었습니다. 좋아하는 음악(물론 스플래시 웨이브!)을 선택하고 도로를 달리면 처음으로 각 스테이지가 끝날 때 어느 방향으로 향할지 선택할 수 있습니다. 시각적, 청각적, 물리적으로 아웃런은 즉각적인 클래식으로 자리 잡으며 드라이빙 게임의 판도를 완전히 바꿔놓았습니다.  
  

슈퍼 마리오 카트(1992) - 편안한 캐릭터와 함께하는 가족의 즐거움:  
콧수염을 기른 영웅과 다채로운 캐릭터들이 이 목록 어딘가에 있을 테니 모든 것이 시작된 곳으로 돌아가는 것이 좋겠습니다. SNES에서 16비트 버전으로 시작된 마리오 카트는 시간이 흐르면서 IP를 통합한 거대한 프랜차이즈로 성장했습니다. 마리오 카트는 항상 인기를 끌었으며, 새로운 세대의 닌텐도 콘솔이 출시될 때마다 핵심 타이틀이 된 역사를 가지고 있습니다. 마리오 카트는 재미있는 게임플레이 메커니즘, 재미있는 파워업, 편안하고 친숙한 캐릭터와 함께 즐길 수 있는 멀티플레이 또는 싱글플레이 캠페인으로 온 가족이 함께 즐길 수 있는 빠른 재미를 선사하는 동시에 숙련된 플레이어가 자신의 실력을 키울 수 있는 기회를 제공합니다. 새로운 게임이 출시될 때마다 속도와 조작법이 개선되고 발전하며, 새로운 트랙과 캐릭터가 추가되고, 향수를 불러일으키는 복고풍 게임도 다시 등장합니다.

![Virtua_Racing_completely_refreshed_the_way_racing_games_were_made_–_bringing_a_cartoon_art_style_into_3D_worlds_which_players_could_experience_from_four_different_angles..jpg](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blta983d2882ea236ec/66cbf4d377adf42b51772eed/Virtua_Racing_completely_refreshed_the_way_racing_games_were_made_%E2%80%93_bringing_a_cartoon_art_style_into_3D_worlds_which_players_could_experience_from_four_different_angles..jpg?width=700&auto=webp&quality=80&disable=upscale "Virtua_Racing_completely_refreshed_the_way_racing_games_were_made_–_bringing_a_cartoon_art_style_into_3D_worlds_which_players_could_experience_from_four_different_angles..jpg")

버추어 레이싱은 레이싱 게임의 제작 방식을 완전히 새롭게 바꾼 게임으로, 카툰 아트 스타일을 3D 세계로 가져와 플레이어가 네 가지 각도에서 경험할 수 있도록 했으며, 가장 중요한 푸른 하늘도 잊지 마세요!

버츄어 레이싱(1992) - 폴리곤 시대의 개막:  
같은 달에 출시된 버츄어 레이싱은 아케이드에 등장했고 레이싱 게임은 다시는 예전과 같지 않을 것입니다. 2D에서 풀 3D로 전환되어 이제 4가지 카메라 위치 중 하나에서 레이스를 펼칠 수 있으며, 모두 빠른 고해상도 그래픽과 16:9 화면에서 실행되는 최초의 아케이드 게임 중 하나입니다! 놀라운 엔진 사운드와 SEGA의 클래식 음악, 그리고 업계 최고의 푸른 하늘이 더해져 다른 모든 레이싱 게임이 구식처럼 느껴집니다. 시각적으로는 스모의 핫샷 레이싱에 영감을 주었을지도모르죠 ...

릿지 레이서(1993) - 핵심 메카닉으로서 드리프트를 개척하다  
1년 후, 가장 사실적인 3D 그래픽을 구현하기 위한 남코와 세가 간의 기술 군비 경쟁이 시작됩니다. 릿지 레이서에는 텍스처와 구로 셰이딩이 추가되었지만, 가장 중요한 것은 게임플레이입니다. 코너에 진입할 때 브레이크를 누르면 코너에서 가장 만족스러운 드리프트를 할 수 있고, 이를 잘 활용하면 랩 타임을 몇 초 단축할 수 있습니다. 음악적으로도 테크노에서 영감을 받은 최신 곡으로 레이싱을 즐길 수 있습니다. 물론, 불과 2년 후 Ridge Racer는 PlayStation 출시 타이틀이 되었고 콘솔은 혁신의 측면에서 아케이드를 추월하기 시작합니다...!  
  
Gran Turismo (1997) - 실제 자동차를 게임 세계로 가져오다:  
사람들이 아케이드 스타일의 레이서에서 좋아했던 모든 것을 시뮬레이션 경험과 결합하여 사람들의 가정으로 가져온 Gran Turismo는 출시 당시 정말 독보적이었습니다. 이 게임은 실버스톤, 뉘르부르크링, 르망 등 자동차 물리와 외관, 그래픽과 트랙 디테일에 있어 높은 수준의 사실감을 제공하며, 플레이어는 크레딧을 모으고 기술을 발전시키며 트로피와 상품을 획득할 수 있습니다. 비디오 게임 세계에 라이선스 자동차를 최초로 도입한 것은 아니지만, 그란 투리스모는 그 개념을 기반으로 확장하여 Aston Martin V8 밴티지, 1967년형 쉐보레 콜벳, 닷지 바이퍼를 등장시켰습니다... 이제 누가 이런 차를 운전해보고 싶지 않을까요?

![A_screenshot_from_the_2018_remaster_of_Burnout_Paradise._Instead_of_getting_players_to_focus_on_great_driving_skills_Burnout_brought_a_new_dynamic_to_the_racing_genre..jpg](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltfdec2f7761ffae06/66cbf4fa05ce3f48d9dd0664/A_screenshot_from_the_2018_remaster_of_Burnout_Paradise._Instead_of_getting_players_to_focus_on_great_driving_skills_Burnout_brought_a_new_dynamic_to_the_racing_genre..jpg?width=700&auto=webp&quality=80&disable=upscale "A_screenshot_from_the_2018_remaster_of_Burnout_Paradise._Instead_of_getting_players_to_focus_on_great_driving_skills_Burnout_brought_a_new_dynamic_to_the_racing_genre..jpg")

번아웃 파라다이스 2018 리마스터의 스크린샷입니다. 번아웃은 플레이어가 뛰어난 운전 기술에 집중하게 하는 대신 최대한 많은 피해와 혼란을 일으키도록 유도하여 레이싱 장르에 새로운 역동성을 불어넣었습니다.

번아웃(2001) - 나쁠수록 좋다:  
00년대 초에 번아웃에 접속한 플레이어들은 트랙에서의 부드러운 운전 기술과 스킬이 아니라 교통 체증, 교차로, 장애물을 극복해야 하는 레이스에 초점을 맞추고 있다는 사실에 놀라움을 금치 못했습니다. 이러한 요소들은 우리가 실제 운전 경험에서 적극적으로 피하고 싶어 하는 것들이지만, 번아웃이 다른 게임과 차별화되는 점은 바로 과격한 액션과 극적인 충돌입니다! 후속작인 번아웃 2: 포인트 오브 임팩트에서는 제한 시간 내에 최대한 많은 피해를 입히는 '크래시' 모드가 별도로 도입되었습니다. 이 모드는 장르에 혁신적인 변화를 가져왔고, 수년 동안 시리즈를 대표하는 특징이 되었습니다.

  
프로젝트 고담 레이싱 2(2005) - 더 많은 플레이어 = 더 많은 재미!  
엄밀히 말하면 시리즈의 세 번째 게임(드림캐스트에서 메트로폴리스 스트리트 레이서로 시작)인 PGR 2는 실제 도시, 놀라운 자동차, 훌륭한 Kudos 시스템(스타일리시한 드라이브!)이라는 훌륭한 요소에 온라인 플레이를 추가했습니다. Xbox Live를 사용하면 플레이어는 전 세계 누구와도 경쟁하거나(물론 험담을 주고받으며) 리더보드 순위를 놓고 비동기식으로 전투를 벌일 수 있었고, 나중에는 플레이어가 도전할 수 있는 새로운 자동차와 도시가 등장하는 DLC까지 추가되었습니다. 후대의 게임들이 이 공식을 더욱 발전시켰지만, PGR2는 이후 출시된 모든 게임에 확실한 새로운 기준을 세웠습니다.

![Outrun_2006_Coast2Coast_is_one_of_the_most_fun_games_I’ve_worked_on_during_my_careers..png](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt5d4e74f0871c023d/66cbf526d2a552dfb3d2a8a8/Outrun_2006_Coast2Coast_is_one_of_the_most_fun_games_I%E2%80%99ve_worked_on_during_my_careers..png?width=700&auto=webp&quality=80&disable=upscale "Outrun_2006_Coast2Coast_is_one_of_the_most_fun_games_I’ve_worked_on_during_my_careers..png")

아웃런 2006: Coast2Coast는 제 경력 중 가장 재미있는 게임 중 하나입니다. 원작의 아케이드 게임기 버전을 충실하게 각색하고 새로운 기능을 추가할 수 있는 기회를 가졌는데, 제가 개인적으로 가장 좋아하는 기능도 포함해서요: "여자 친구를 잃지 마세요"는 이전 게임에서는 볼 수 없었던 위험 보상 메커니즘을 도입했습니다.

아웃런 2006: Coast2Coast(2006) - 슬립스트림 시스템 소개  
물론 저는 항상 작업할 때뿐만 아니라 플레이할 때도 가장 좋아하는 게임 중 하나를 포함하려고 했습니다. SEGA와 아웃런 2006 도입에 대해 이야기를 나눴을 때: Coast2Coast를 오락실 기계에서 플레이어의 거실로 가져오는 것에 대해 이야기했을 때, 저희는 원작의 '오락실 느낌', 고속 주행, 멋진 비주얼 및 모든 재미를 유지하면서 우리만의 미션, 레벨 디자인 및 감각을 추가해야 하는 과제를 안게 되었습니다. 불과 2년 전 아웃런2에서 했던 작업을 기반으로 개발했지만, 코스트 2 코스트에서는 IP에 익숙해지면서 체계적인 게임플레이 경험과 진행 시스템, 더 많은 자동차, 새로운 모드, 온라인 플레이, 현대 레이싱 게임에서 볼 수 있는 슬립스트림 시스템 도입 등 프랜차이즈에 적합하다고 생각되는 요소들을 도입할 수 있었죠. 플레이어에게 동등한 도전과 보상을 제공하며, 수년 전과 마찬가지로 여전히 밝고 다채로우며 진정으로 재미있는 게임이라고 생각합니다. 그리고 이동 중에도 플레이할 수 있도록 PSP로 압축했습니다!

포르자 호라이즌(2012) - 오픈 월드에 도전하다:  
포르자 호라이즌 시리즈는 크고 아름답고 탐험하기 좋은 환경, 다양한 라이선스 차량, 전반적으로 멋진 분위기와 분위기 등 우리가 운전하면서 갈망하는 모든 것을 플레이어에게 제공합니다. 저는 이 오픈 월드 게임이 전작의 모든 교훈을 바탕으로 진정으로 독특하고 매력적인 게임을 만들어냈으며, 속편과 스핀오프에 이르기까지 계속 진화하고 발전해 왔다고 믿습니다. 플레이어는 서킷, 오프로드, 전통 레이싱 등 수많은 유형의 레이스에 참가할 수 있을 뿐만 아니라, 안전벨트를 매고 광활한 지형에 도전할 수도 있습니다. 성공적인 콘텐츠 업데이트와 커뮤니티와의 강력한 참여, 그리고 라이브 서비스에서 장르의 미래를 위한 기준을 한층 더 높인 Microsoft의 경험을 바탕으로 포르자 호라이즌이 어떻게 발전해왔는지 확인할 수 있습니다.

![Is_it_a_plane_Is_it_a_boat_Is_it_a_car_YES!_Sonic_&_All-Stars_Racing_Transformed_made_popular_the_transforming_tracks_concept..jpg](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt7b8d5f705fa5fbcc/66cbf553cba99c2d882d45f5/Is_it_a_plane_Is_it_a_boat_Is_it_a_car_YES!_Sonic_&_All-Stars_Racing_Transformed_made_popular_the_transforming_tracks_concept..jpg?width=700&auto=webp&quality=80&disable=upscale "Is_it_a_plane_Is_it_a_boat_Is_it_a_car_YES!_Sonic_&_All-Stars_Racing_Transformed_made_popular_the_transforming_tracks_concept..jpg")

비행기인가요? 보트인가요? 자동차인가요? YES! 소닉 & 올스타 레이싱 트랜스포메이션은 변신 트랙 콘셉트로 인기를 끌었으며, 플레이어가 플레이할 때마다 메인 레이스뿐만 아니라 다양한 볼거리를 제공했습니다. 날아다니는 용, 점프하는 고래, 전투하는 배 등 다채로운 카트 레이싱의 혼돈을 더하는 요소들을 찾아보세요.

소닉 & 올스타 레이싱 트랜스포메이션 (2012) - 트랜스포밍 트랙  
죄송합니다, 마지막으로 제 욕심을 부려서 죄송하지만, 이 게임은 제가 가장 좋아하는 출시 게임이자 이전의 모든 레이싱 게임 경험을 바탕으로 플레이어가 예상하지 못한 방식으로 장르를 발전시킨 게임입니다! 자동차가 보트나 비행기로 변신할 수 있다면 어떨까요? 우리가 가장 좋아하는 SEGA 캐릭터와 세계관을 혼합하면 어떨까요? 용암 위를 달리는 경주에서 기계 거북이를 탈 수 있다면 어떨까요? 트랜스포머는 이 모든 질문에 대한 답을 제시합니다! 저희는 레이싱 게임 팬들에게 보내는 거대한 러브레터에 법적으로 허용되는 한도 내에서 최대한 많은 SEGA를 집어넣었고, 심지어 보너스 아웃런2 테마 트랙도 슬쩍 넣었습니다! 게다가 드림캐스트 컨트롤러로 레이싱을 할 수 있는 게임이 또 뭐가 있을까요? 5인 분할 화면 플레이가 가능한 Wii U 출시 타이틀이라는 사실도 잊지 마세요!

![Audio_plays_a_huge_role_in_creating_a_great_racing_game_with_a_combination_of_authentic_car_audio_ambient_road_noise_and_of_course_some_really_great_music.png](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltd54fcdef2b5c7c68/66cbf584cba99c0f7f2d45f9/Audio_plays_a_huge_role_in_creating_a_great_racing_game_with_a_combination_of_authentic_car_audio_ambient_road_noise_and_of_course_some_really_great_music.png?width=700&auto=webp&quality=80&disable=upscale "Audio_plays_a_huge_role_in_creating_a_great_racing_game_with_a_combination_of_authentic_car_audio_ambient_road_noise_and_of_course_some_really_great_music.png")

오디오는 실제 자동차 오디오, 주변 도로 소음, 그리고 물론 멋진 음악의 조합으로 멋진 레이싱 게임을 만드는 데 큰 역할을 합니다. 이 모든 것이 집약된 것이 바로 드라이빙 어드벤처 게임인 그랜트 시프트 오토이며, 이 게임의 라디오 방송국은 전설이 되었습니다. 2023년, Spotify는 모든 장르에 걸쳐 좋아하는 아티스트의 숨겨진 주옥같은 명곡과 클래식 음악을 마치 GTA 라디오 방송국의 트랙처럼 들려주는 'Grand Theft Auto Radio'를 출시했습니다.

## 개발 속도 향상 | 레이싱 게임을 준비하는 방법 팁

  
레이싱 게임 작업의 가장 좋은 점은 레이싱 게임을 만드는 것이 정말 재미있다는 점입니다. 예측할 수 없는 레이스, 시각적 요소, 속도를 내는 즐거움 덕분에 플레이 테스트가 항상 즐겁고, 항상 할 수 있는 한계를 뛰어넘는 새로운 방법을 모색하고 있습니다.

제 경험에 비추어 볼 때, 레이싱 게임을 3위에서 챔피언으로 끌어올릴 수 있는 몇 가지 핵심 요소가 있습니다. 레이싱 게임을 개발하려는 모든 개발자를 위한 몇 가지 팁을 소개합니다...

올바른 속도감 확보: 모든 레이싱 게임에서는 플레이어에게 다양한 속도를 제공해야 하며, 모두 사실적이고 정확하게 느껴져야 합니다. 컨트롤러로 전속력으로 달리는데 차가 30마일로 공회전하는 것을 보고 싶어하는 사람은 아무도 없을 것입니다. 이를 위해서는 카메라를 낮고 넓게 설치하여 속도와 움직임을 느낄 수 있도록 하고, 이미 최고 속도로 달리고 있더라도 엔진이 항상 가속하는 것처럼 들리는 오디오를 만들어야 합니다. 빠르게 보이고 빠르게 들린다면 대부분 성공한 것입니다.

오디오를 과소평가하지 마세요: 레이싱 게임의 주된 초점은 비주얼이라고 생각할 수 있지만, 플레이어가 액션에 몰입하려면 오디오 작업도 많이 이루어져야 합니다. 차량의 SFX는 사실적이고 박진감 넘치는 느낌을 주어야 할 뿐만 아니라 환경 사운드는 플레이어의 행동을 반영해야 하고, 음악은 물론 게임의 속도감을 더해야 합니다... 컵 시리즈의 마지막 라운드에서 피아노 소나타를 듣는 것은 우승에 도움이 되지 않습니다!

학습 곡선을 구현하세요: 대부분의 레이싱 게임은 기술 수준에 관계없이 누구나 쉽게 익히고 플레이할 수 있는 순수성을 가지고 있으며, 꾸준히 사랑받는 게임은 플레이어가 학습 곡선을 따라가며 실력을 키울 수 있는 옵션을 제공하는 게임입니다. 이를 통해 플레이어는 자신의 방식대로 플레이할 수 있습니다. 어떤 플레이어는 소셜 환경에서 레이스를 즐기고 싶어 하고, 어떤 플레이어는 트랙과 메커니즘을 배우고 기술을 완벽하게 익히고 싶어 하며, 그렇게 함으로써 보상을 받기를 원합니다.

물리학과 핸들링: 시뮬레이션, 아케이드 시뮬레이션, 실감나는 체험 등 어떤 유형의 레이싱 게임을 만들든 플레이어는 자신이 컨트롤하고 있다는 느낌을 받아야 합니다. 플레이어의 충격에 대한 확실하고 예측 가능한 반응, 다양한 상황에서 차량이 어떻게 행동하는지, 업그레이드/커스터마이징이 차량의 동작을 어떻게 변화시키는지에 대한 심도 있는 설명이 있어야 플레이어가 계속 플레이하고, 구축하고, 성장하도록 유도할 수 있습니다. 또한, 스타일에 관계없이 다양한 모델과 유형의 자동차의 핸들링 느낌을 포착할 수 있다면 플레이어가 가장 좋아하는 자동차를 운전할 수 있는 기회를 제공하는 것이며, 이는 사람들이 게임을 좋아하는 이유의 핵심입니다!

![Games_like_Forza_Horizon_5_take_environments_to_a_new_level_and_give_players_an_open-world_experience_where_they_can_encounter_breathtaking_scenery_and_stunning_visuals..jpg](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltbc6a21c007263ad6/66cbf5be41be8332edcdb465/Games_like_Forza_Horizon_5_take_environments_to_a_new_level_and_give_players_an_open-world_experience_where_they_can_encounter_breathtaking_scenery_and_stunning_visuals..jpg?width=700&auto=webp&quality=80&disable=upscale "Games_like_Forza_Horizon_5_take_environments_to_a_new_level_and_give_players_an_open-world_experience_where_they_can_encounter_breathtaking_scenery_and_stunning_visuals..jpg")

Forza Horizon 5와 같은 게임은 환경을 새로운 차원으로 끌어올리고 플레이어에게 숨막히는 풍경과 멋진 비주얼을 만날 수 있는 오픈 월드 경험을 제공합니다. 매일 혼잡한 출퇴근길과는 또 다른 세계. 기술이 계속 발전함에 따라 개발자는 환경을 배경에서 경험의 핵심 요소로 끌어올리는 더욱 멋진 그래픽을 제작할 수 있습니다.

환경: 멋진 풍경과 탁 트인 전망으로 가득한 아름다운 도로를 따라 달릴 때의 행복감은 개인적으로 레이싱 게임에서 얻는 즐거움 중 하나입니다. 하지만 오픈 로드 주행 경험이든, 좁은 트랙에서 진행되는 시험 주행이든, 액션을 둘러싼 환경을 제대로 구현하는 것이 중요합니다. 날씨부터 도로 폭까지 최적의 주행 경험을 위해 세밀하게 조정된 다양한 디테일과 함께 주변 환경과 눈에 거슬리지 않는 균형이 맞아야 합니다!

경쟁을 포착하세요: 레이싱 게임의 매력 중 하나는 좋은 성적을 내고 승리하고 싶은 욕구입니다. 이를 위한 방법으로는 강력한 소셜 메커니즘을 통해 플레이어가 자신의 승리를 전 세계와 공유하고, 다양한 업적을 달성하거나 수집품 또는 잠금 해제 가능한 아이템을 획득할 수 있는 기회를 제공하는 것이 있습니다. 이러한 요소는 진행 과정과 다양성과 결합하여 레이싱 게임의 훌륭한 토대가 됩니다.

\---

레이싱 게임은 항상 더 넓은 게임 산업에 큰 영향을 미쳐왔고 앞으로도 그럴 것입니다. 레이싱 게임에는 차량 기반 이동 수단(말이 중요합니다!)과 전투, 운전 메커니즘, 타임 트라이얼 등 많은 기능이 다른 장르에 맞게 진화해 왔습니다.

지난 50년 동안 레이싱 게임은 긴 여정을 걸어왔으며, 개발자들은 플레이어를 위한 경험을 만들기 위해 많은 교훈을 얻고 기술을 연마해 왔습니다. 제 경력을 통해 이 장르의 성장을 지켜본 사람으로서, 개발자들이 계속해서 신선하고 관련성 있는 게임을 만드는 방법을 찾고 있을 뿐만 아니라 플레이어들이 계속해서 두 팔 벌려 환영해 주는 것을 보면 가슴이 벅찹니다.

자세히 읽어보세요:

[블로그추천](https://www.gamedeveloper.com/keyword/blogs)[블로그톱](https://www.gamedeveloper.com/keyword/featured-blogs)[스토리](https://www.gamedeveloper.com/keyword/top-stories)

[](https://www.linkedin.com/sharing/share-offsite/?url=https://www.gamedeveloper.com/design/getting-under-the-hood-of-racing-games)[](https://www.facebook.com/sharer/sharer.php?u=https://www.gamedeveloper.com/design/getting-under-the-hood-of-racing-games)[](https://www.twitter.com/intent/tweet?url=https://www.gamedeveloper.com/design/getting-under-the-hood-of-racing-games)[](https://www.gamedeveloper.com/cdn-cgi/l/email-protection#19266a6c7b737c7a6d245e7c6d6d70777e396c777d7c6b396d717c397176767d39767f396b787a70777e397e78747c6a3f787469227b767d6024503c2b296d71766c7e716d3c2b296d717c3c2b297f767575766e70777e3c2b297f6b76743c2b295e78747c3c2b295d7c6f7c7576697c6b3c2b2974707e716d3c2b2970776d7c6b7c6a6d3c2b2960766c373c295d3c29583c295d3c29583c2b295e7c6d6d70777e3c2b296c777d7c6b3c2b296d717c3c2b297176767d3c2b29767f3c2b296b787a70777e3c2b297e78747c6a3c295d3c2958716d6d696a3c2a583c2b5f3c2b5f6e6e6e377e78747c7d7c6f7c7576697c6b377a76743c2b5f7d7c6a707e773c2b5f7e7c6d6d70777e346c777d7c6b346d717c347176767d34767f346b787a70777e347e78747c6a)[](https://www.reddit.com/submit?url=https://www.gamedeveloper.com/design/getting-under-the-hood-of-racing-games&title=Getting%20under%20the%20hood%20of%20racing%20games)

## 작성자 소개

[![Steve Lycett](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltd709c2f6ad0896cd/657b3aae1fb1b4040a0e1821/Game_Developer_G_Logo_RGB.png?width=400&auto=webp&quality=80&disable=upscale "Steve Lycett")](https://www.gamedeveloper.com/author/steve-lycett)

[

스티브 라이셋

](https://www.gamedeveloper.com/author/steve-lycett)

[Steve Lycett의 더보기](https://www.gamedeveloper.com/author/steve-lycett)

게임 개발자의 일일 뉴스, 개발자 블로그, 스토리를 받은 편지함으로 바로 받아보세요.

[최신 소식 받기](https://gd-resources.gamedeveloper.com/free/w_gamf01/prgm.cgi)

추천 콘텐츠

* * *

원문: [https://www.gamedeveloper.com/design/getting-under-the-hood-of-racing-games](https://www.gamedeveloper.com/design/getting-under-the-hood-of-racing-games)