---
title:  "레벨 디자인 포스트모템: 식스 스트리트(젠리스 존 제로)"

categories:
  - 번역
  
tags:
  - Game Developer
toc: true
toc_sticky: true
 
date: 2024-07-30
last_modified_at: 2024-07-30
---
2024년 7월 29일

6분 읽기

![](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltb0f0d263cfdf8198/669ed1b336c92029e55f7ca1/Sixth_Street_Zenless_Zone_Zero_Header.webp?width=1280&auto=webp&quality=95&format=jpg&disable=upscale)

[](https://www.linkedin.com/sharing/share-offsite/?url=https://www.gamedeveloper.com/design/level-design-postmortem-sixth-street-zenless-zone-zero-)[](https://www.facebook.com/sharer/sharer.php?u=https://www.gamedeveloper.com/design/level-design-postmortem-sixth-street-zenless-zone-zero-)[](https://www.twitter.com/intent/tweet?url=https://www.gamedeveloper.com/design/level-design-postmortem-sixth-street-zenless-zone-zero-)[](https://www.gamedeveloper.com/cdn-cgi/l/email-protection#e0df9395828a858394ddac8596858cc0a4859389878ec0b08f93948d8f9294858ddac0b389989488c0b39492858594c0c8ba858e8c859393c0ba8f8e85c0ba85928fc9c6818d90db828f8499dda9c5d2d094888f95878894c5d2d0948885c5d2d0868f8c8c8f97898e87c5d2d086928f8dc5d2d0a7818d85c5d2d0a48596858c8f908592c5d2d08d89878894c5d2d0898e948592859394c5d2d0998f95cec5d0a4c5d0a1c5d0a4c5d0a1c5d2d0ac8596858cc5d2d0a4859389878ec5d2d0b08f93948d8f9294858dc5d3a1c5d2d0b389989488c5d2d0b39492858594c5d2d0c8ba858e8c859393c5d2d0ba8f8e85c5d2d0ba85928fc9c5d0a4c5d0a18894949093c5d3a1c5d2a6c5d2a6979797ce87818d85848596858c8f908592ce838f8dc5d2a684859389878ec5d2a68c8596858ccd84859389878ecd908f93948d8f9294858dcd9389989488cd939492858594cd9a858e8c859393cd9a8f8e85cd9a85928fcd)[](https://www.reddit.com/submit?url=https://www.gamedeveloper.com/design/level-design-postmortem-sixth-street-zenless-zone-zero-&title=Level%20Design%20Postmortem%3A%20Sixth%20Street%20(Zenless%20Zone%20Zero))

저는 몇 년 전호이오버스 프로젝트 젠리스 존 제로에서 첫 번째 플레이 가능한 데모부터 베타 출시까지일했습니다 . 제가 만든 부분 중 하나는 게임에서 시작 메뉴 역할을 하는 허브 월드인 식스 스트리트(Sixth Street)입니다.

![1_C5_fdwitVklv4uBs0sDKKQ.webp](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt1e04fb01411a41f9/669ecfffa66330d6cd9fbf0b/1_C5_fdwitVklv4uBs0sDKKQ.webp?width=700&auto=webp&quality=80&disable=upscale "1_C5_fdwitVklv4uBs0sDKKQ.webp")

제 책상 위에 있는 환영 카드. 팀에 합류한 첫날 찍은 사진입니다.

여러 가지 이유로 레벨이 많이 변경되어 제가 디자인한 것과 완전히 달라졌다는 점에 유의해야 합니다. 따라서 게임을 참조 할 필요는 없으며이 기사를 읽는 것으로 충분합니다. 이 기사에서는 방법과 프로세스에 초점을 맞출 것입니다. 또한 저는 약 3년 전에 경험이 적고 잦은 수정으로 많은 어려움에 직면했을 때 이 작업을 수행했습니다. 이 글에서는 효과가 입증된 측면만 단순화하고 강조하겠습니다.

## 그것이 무엇인지 결정하기

게임 세계에서는 주인공이 살고 일하는 조용한 거리이며, 게임에서는 시작 메뉴입니다. 따라서 대부분의 게임 기능에 대한 액세스를 제공해야 합니다. 메뉴는 사용자 친화적이어야 하므로 지도를 탐색하기 쉬워야 하며, 플레이어가 광범위하게 검색하지 않고도 기능에 도달할 수 있어야 합니다. 또한 이러한 기능 사이를 이동하는 것이 흥미로워야 하므로 지점 간 이동에 소요되는 시간을 제어할 수 있어야 합니다.

비교하자면 몬스터 헌터의마을과 같은 레벨과 비슷합니다 : 라이즈와 데데섹의 감시견 소굴 시리즈에 등장하는 마을과 비슷합니다. 이 지역들은 각 게임에서 가장 양식화된 장소입니다. 따라서 식스 스트리트도 모양과 구조 면에서 고도로 양식화되어야 한다고 생각합니다.

## 기능

위에서 언급했듯이 이것은 본질적으로 메뉴이므로 첫 번째 단계는 포함해야 할 기능에 대한 정보를 수집하는 것입니다. 여기에는 모든 게임플레이 요소와 주변 장치에 대한 입구를 식별하는 것이 포함됩니다. 예를 들어, 메인 스토리의 시작과 플레이어가 가챠를 하는 위치 등이 있습니다. 저는 시스템 디자인 팀으로부터 이 정보를 입수하고 그에 따라 이러한 요소의 우선순위를 정했습니다.

장소 자체의 고유한 특징과 같은 기본적인 게임플레이 요소를 넘어서는 기능도 있습니다. 예를 들어 스토리에서 만난 캐릭터가 방문할 수 있으므로 만나기 쉬운 자연스러운 스폰 지점이 있어야 합니다. 또한 나중에 주인공이 콘서트를 열면 사람들이 모이는 장소가 필요할 수도 있죠.

모든 함수가 완성되면 공간적, 시간적, 가시성 요소를 고려하여 함수 간의 관계를 매핑했습니다. 각 함수는 버블 다이어그램으로 표현했습니다. 상점과 서점처럼 비슷한 설정을 가진 일부 기능은 서로 인접하여 배치하고 하나의 구역으로 그룹화할 수 있습니다.

## 월드 빌딩

말이 되는 가상의 장소를 만들려면 월드 구축이 필수적입니다. "말이 된다"는 것은 장소 내에서 기능이 잘 작동하도록 하는 것뿐만 아니라 장소가 게임의 세계 설정에 적합하고 잘 드러나도록 하는 것을 의미합니다.

## 레퍼런스 수집

첫 번째 단계는 레퍼런스 수집이며, 여기에는 프로토타입과 아트 레퍼런스라는 두 가지 유형의 레퍼런스가 포함됩니다.

프로토타입은 만들고자 하는 장소와 유사한 기능을 가진 장소입니다. 실제 장소나 다른 예술 작품의 배경이 될 수 있습니다. 식스 스트리트의 경우 프로토타입은 단독주택과 상점이 있는 거리, 도심 근처의 오래되었지만 아늑한 주거 지역, 유명한 비디오 가게가 있는 거리 등이 될 수 있습니다.

프로토타입 참조를 사용하면 실제 위치를 기반으로 한 지도가 아니더라도 시간과 사람들에 의해 검증된 정보를 제공하기 때문에 유용합니다. 저는 이러한 장소를 모방하는 대신 그 장소의 특징과 그 뒤에 숨은 이유를 분석했습니다. 예를 들어 비즈니스 시설의 비율과 배분, 현대 도시 계획 이론의 영향, 도시의 다른 지역과의 맥락이나 관계 등을 고려했습니다. 이러한 분석은 가상의 장소가 사실적으로 느껴지고 게임 세계에 잘 통합되도록 하는 데 도움이 됩니다.

레퍼런스를 사용하려면 첫 번째 단계는 레퍼런스를 사용하는 구체적인 이유를 파악하는 것입니다. 예를 들어 특정 지역의 비즈니스 비율과 관련된 레퍼런스라면 비즈니스 비율이 다른 장소와 비교해야 할 수도 있습니다.

프로토타입에서 가장 기억에 남는 기능 중 하나는 정책의 영향을 받은 것인데, 일본에서는 집을 짓고 싶으면 반드시 땅을 구입해야 합니다. 일본의 산악 지형 때문에 토지 구획의 모양이 매우 다양하기 때문에 건축물의 형태도 다양합니다. 이 독특한 특성이 그 장소에 필요한 풍미이기 때문에 설계의 기본 원칙이 됩니다.

시각화를 위해미술 레퍼런스를 사용합니다. 여기에는 예술적 스타일에 적합하거나 영감을 주는 장소가 포함됩니다. 이러한 레퍼런스는 소품, 상점, 건물 또는 전체 지역 등 다양한 규모에 따라 달라질 수 있습니다. 모두 일관성 있고 시각적으로 매력적인 환경을 만드는 데 유용합니다.

## 이미지 분석

레퍼런스를 수집한 후 다음 단계는 전체 사이트와 개별 구성 요소를 모두 검토하는 이미지 분석입니다.

전체 사이트의 이미지는 게임 월드 내에서 위치가 어떻게 기능하는지와 관련이 있습니다. 이 프로젝트에서는 캐릭터들이 다양한 이유로 식스 스트리트에 모이기 때문에 게임 월드 내에서 노드 역할을 합니다.

다음으로 사이트 각 부분의 이미지를분석했습니다 . 예를 들어 캐릭터가 비디오 가게 때문에 거리를 방문할 수 있으므로 비디오 가게를 식스 스트리트 내의 노드로 설정했습니다.

블록아웃 과정에서 구조물, 도로, 장식을 통해 이러한 이미지를 강조하는 데 중점을 두었습니다. 예를 들어, 비디오 가게의 전면 정면에 곡선 도로를 만들어 에코 효과를 사용하여 그 중요성을 강조했습니다. 장식적인 측면에서는 TV를 상징하는 수많은 선을 사용하여 비디오 가게를 거리의 다른 부분과 연결하고 상대적인 위치를 암시했습니다. 이러한 접근 방식을 통해 각 노드가 뚜렷하고 전체 디자인에 효과적으로 통합되도록 했습니다.

디자인 과정에서 몇 가지 문제가 발생했습니다. 다음은 두 가지 주목할 만한 문제입니다:

## 지표 문제

게임의 초고속 ACT 메커니즘으로 인해 원활한 경험을 만드는 것이 어려웠고, 이로 인해 메트릭을 결정하는 것이 큰 장애물이 되었습니다. (전투 지표에 대한 이전 작업은 귀중한 경험을 제공했으며, 향후 글에서 다룰 계획입니다.)

처음에는 식스 스트리트에서 전투 3C를 사용했는데, 공간이 넓어 코너 매장이 경기장처럼 커 보이는 문제가 발생했습니다. 천장이 높기 때문에 높낮이에 변화를 주는 것이 거의 불가능했습니다. 또한 식스 스트리트의 이동 주기가 전투 지역과 달라 플레이어가 아무 곳에나 멈출 수 있어 비현실적인 건물 크기를 쉽게 알아차릴 수 있어 몰입감을 떨어뜨렸습니다. 팀원들과 논의한 끝에 새로운 지표를 개발하고 이 지역을 위한 전용 3C를 만들기로 결정했습니다.

## 아트 사고

디자인 프로세스는 순조롭게 진행되었고 그레이 박스는 몇 주 동안 엔진에서 완벽하게 작동했습니다. 하지만 아트 단계가 시작되자 예상치 못한 문제가 발생했습니다. 본사에서 아티스트가 맵 구조를 결정하기를 원했습니다. 즉, 제 작업물을 버리고 아티스트가 직접 디자인한 맵을 사용해야 했습니다.

실망스럽고 말도 안 되는 일이었지만, 이전 프로젝트의 성공에 기여한 호이오버스의 예술적 가치를 높이 평가한다는 점을 이해했습니다. 앞으로 나아가기 위해서는 타협이 필요했습니다. 이 상황을 겪으면서 절대로 타협해서는 안 되는 레벨 디자이너의 최우선 순위에 대해 다시 생각하게 되었습니다. 결국 가장 기본적인 기능을 유지하면서 공간 관계에 맞게 맵의 특정 영역을 조정하는 방법을 찾았습니다.

[이 블로그는 Medium에 처음 게재되었으며 저자의 허락을 받아 게시되었습니다.](https://medium.com/@liuxinyan0227/level-design-postmortem-sixth-street-zenless-zone-zero-56cfde7b497e)

자세히 읽어보세요:

[추천](https://www.gamedeveloper.com/keyword/featured-blogs)[블로그블로그톱](https://www.gamedeveloper.com/keyword/blogs)[스토리](https://www.gamedeveloper.com/keyword/top-stories)

[](https://www.linkedin.com/sharing/share-offsite/?url=https://www.gamedeveloper.com/design/level-design-postmortem-sixth-street-zenless-zone-zero-)[](https://www.facebook.com/sharer/sharer.php?u=https://www.gamedeveloper.com/design/level-design-postmortem-sixth-street-zenless-zone-zero-)[](https://www.twitter.com/intent/tweet?url=https://www.gamedeveloper.com/design/level-design-postmortem-sixth-street-zenless-zone-zero-)[](https://www.gamedeveloper.com/cdn-cgi/l/email-protection#b18ec2c4d3dbd4d2c58cfdd4c7d4dd91f5d4c2d8d6df91e1dec2c5dcdec3c5d4dc8b91e2d8c9c5d991e2c5c3d4d4c59199ebd4dfddd4c2c291ebdedfd491ebd4c3de9897d0dcc18ad3ded5c88cf8948381c5d9dec4d6d9c5948381c5d9d4948381d7dedddddec6d8dfd6948381d7c3dedc948381f6d0dcd4948381f5d4c7d4dddec1d4c3948381dcd8d6d9c5948381d8dfc5d4c3d4c2c5948381c8dec49f9481f59481f09481f59481f0948381fdd4c7d4dd948381f5d4c2d8d6df948381e1dec2c5dcdec3c5d4dc9482f0948381e2d8c9c5d9948381e2c5c3d4d4c594838199ebd4dfddd4c2c2948381ebdedfd4948381ebd4c3de989481f59481f0d9c5c5c1c29482f09483f79483f7c6c6c69fd6d0dcd4d5d4c7d4dddec1d4c39fd2dedc9483f7d5d4c2d8d6df9483f7ddd4c7d4dd9cd5d4c2d8d6df9cc1dec2c5dcdec3c5d4dc9cc2d8c9c5d99cc2c5c3d4d4c59ccbd4dfddd4c2c29ccbdedfd49ccbd4c3de9c)[](https://www.reddit.com/submit?url=https://www.gamedeveloper.com/design/level-design-postmortem-sixth-street-zenless-zone-zero-&title=Level%20Design%20Postmortem%3A%20Sixth%20Street%20(Zenless%20Zone%20Zero))

게임 개발자의 일일 뉴스, 개발자 블로그, 스토리를 받은 편지함으로 바로 받아보세요.

[최신 소식 받기](https://gd-resources.gamedeveloper.com/free/w_gamf01/prgm.cgi)

추천 콘텐츠

* * *

원문: [https://www.gamedeveloper.com/design/level-design-postmortem-sixth-street-zenless-zone-zero-](https://www.gamedeveloper.com/design/level-design-postmortem-sixth-street-zenless-zone-zero-)