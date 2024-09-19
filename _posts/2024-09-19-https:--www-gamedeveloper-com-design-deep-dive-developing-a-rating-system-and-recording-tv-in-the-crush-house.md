---
title:  "심층 분석: 더 크러쉬 하우스에서 등급 시스템 개발 및 시청률이 높은 TV 제작하기"

categories:
  - 번역
  
tags:
  - Game Developer
toc: true
toc_sticky: true
 
date: 2024-09-19
last_modified_at: 2024-09-19
---
[![Picture of Finn Carney](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltd709c2f6ad0896cd/66df238c1ceec85b3ae644da/Game_Developer_G_Logo_RGB.webp?width=100&auto=webp&quality=80&disable=upscale "Picture of Finn Carney")](https://www.gamedeveloper.com/author/finn-carney)

[핀 카니](https://www.gamedeveloper.com/author/finn-carney)

9월 19일, 2024

10 분 읽기

![](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt6d9f6247c72661a9/66da6b6e691afe6b75490dc6/ss_0ef54cc0ee58336b2b91ea1638ed86496f936eec.jpg?width=1280&auto=webp&quality=95&format=jpg&disable=upscale)

Devolver Digital 이미지 제공.

[](https://www.linkedin.com/sharing/share-offsite/?url=https://www.gamedeveloper.com/design/deep-dive-developing-a-rating-system-and-recording-tv-in-the-crush-house)[](https://www.facebook.com/sharer/sharer.php?u=https://www.gamedeveloper.com/design/deep-dive-developing-a-rating-system-and-recording-tv-in-the-crush-house)[](https://www.twitter.com/intent/tweet?url=https://www.gamedeveloper.com/design/deep-dive-developing-a-rating-system-and-recording-tv-in-the-crush-house)[](https://www.gamedeveloper.com/cdn-cgi/l/email-protection#556a2620373f303621681130302575113c23306f7511302330393a253c3b327534752734213c3b3275262c2621303875343b317538343e3c3b32753f203c362c750103753c3b75013d3075162720263d751d3a202630733438256e373a312c681c706765213d3a20323d21706765213d30706765333a39393a223c3b3270676533273a387067651234383070676511302330393a253027706765383c323d217067653c3b2130273026217067652c3a207b70651170651470651170651470676511303025706765113c233070661470676511302330393a253c3b32706765347067652734213c3b32706765262c26213038706765343b3170676538343e3c3b327067653f203c362c70676501037067653c3b706765013d30706765162720263d7067651d3a2026307065117065143d212125267066147067137067132222227b3234383031302330393a2530277b363a387067133130263c323b7067133130302578313c23307831302330393a253c3b327834782734213c3b3278262c2621303878343b31782730363a27313c3b32782123783c3b78213d3078362720263d783d3a202630)[](https://www.reddit.com/submit?url=https://www.gamedeveloper.com/design/deep-dive-developing-a-rating-system-and-recording-tv-in-the-crush-house&title=Deep%20Dive%3A%20Developing%20a%20rating%20system%20and%20making%20juicy%20TV%20in%20The%20Crush%20House)

게임 개발자 심층 분석은 비디오 게임의 특정 디자인, 아트 또는 기술적 특징을 조명하여 단순해 보이는 근본적인 디자인 결정이 실제로는 전혀 단순하지 않다는 것을 보여주기 위해 진행 중인 시리즈입니다.

이전 편에서는 [블러드리스의](https://www.gamedeveloper.com/art/deep-dive-behind-the-starkly-stylish-art-direction-of-bloodless)[스타일리시한 아트 디렉션](https://www.gamedeveloper.com/art/deep-dive-behind-the-starkly-stylish-art-direction-of-bloodless) , [GOG가](https://www.gamedeveloper.com/design/deep-dive-how-gog-perfected-the-imperfect-with-the-re-release-of-alpha-protocol) [알파 프로토콜을](https://www.gamedeveloper.com/design/deep-dive-how-gog-perfected-the-imperfect-with-the-re-release-of-alpha-protocol) [최신 디지털 버전으로](https://www.gamedeveloper.com/design/deep-dive-how-gog-perfected-the-imperfect-with-the-re-release-of-alpha-protocol)[업데이트한 방법](https://www.gamedeveloper.com/design/deep-dive-how-gog-perfected-the-imperfect-with-the-re-release-of-alpha-protocol) , [이스타르 게임즈가](https://www.gamedeveloper.com/design/deep-dive-designing-a-new-dwarf-race-in-the-last-spell) [더 라스트 스펠의](https://www.gamedeveloper.com/design/deep-dive-designing-a-new-dwarf-race-in-the-last-spell)[새로운 드워프 종족 디자인에 접근한 방법과](https://www.gamedeveloper.com/design/deep-dive-designing-a-new-dwarf-race-in-the-last-spell) 같은 주제를 다루었습니다 .

이번 에피소드에서는 네리얼의 레벨 디자이너 핀 카니가 더 크러쉬 하우스에서라이브 영상을 비평적으로 평가하는 복잡한 디자인 과정과 비평을 플레이어에게 맡기면서 벌어진 일에 대해 설명합니다 .

더 크러쉬 하우스에서 플레이어는 리얼리티 TV 쇼의 카메라맨을 맡게 되는데, 리얼리티 TV의 많은 부분이 네리얼 스튜디오(레인즈, 카드 샤크)의 기존 강점인 내러티브 분기 및 복잡성, 개성 있는 상호작용, 로그라이크적인 구조와 유사합니다. 하지만 그 어떤 것도 촬영의 핵심 메커니즘을 준비하지 못했고, 메커니즘을 촬영하기 위한 외부 레퍼런스도 많지 않았습니다( 미시간: 지옥으로부터의 보고를 외치며 ). 그 이유는 메카닉촬영이 매우 복잡한 기술이기때문인 것으로 밝혀졌습니다 .

메카닉으로서의 사진은 수년에 걸쳐 많은 발전을 거듭해 왔으며, 특히 우무랑기 제너레이션과 데드라이징같은 게임이 저희의 사고 프로세스에 영향을 미쳤습니다. 하지만 촬영 메커니즘과 달리 사진 메커니즘은 한 번에 한 프레임만 분석하고 등급을 매기면 된다는 점이 다릅니다. 촬영은 매초마다 수십 개의 프레임을 분석하고 등급을 매긴 다음, 그 모든 정보를 최소한 분석 가능한 방식으로 플레이어에게 표시해야 하며, 이상적으로는 실제로 재미있게 표시해야 합니다. 다시 말하지만, 복잡합니다.

### 시즌 0

제작 초기의 콘셉트는 플레이어가 영상을 녹화한 다음 영상을 편집하는 것이었습니다. 개념적으로는 매우 멋지지만 기술적으로는 악몽과도 같았습니다. 적절한 프레임 속도와 화질로 영상을 녹화하려면 많은 메모리와 비디오 카드의 디스크 공간이 필요했기 때문입니다. 그 다음에는 촬영한 영상을 실제로 분석하고 분류해야 했습니다. 우리가 시도한 한 가지 시스템은 영상의 마지막 몇 초를 버퍼링하고 그 시간 동안 '흥미로운' 일이 발생했는지 확인한 후 그렇지 않은 경우 폐기하는 것이었습니다. 하지만 어떤 것이 흥미로운지, 심지어 '흥미로운 것'이 무엇인지 판단하는 방법은 매우 어려웠습니다.

![](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blta2a1b0a8ea30d28d/66da6a295c6d7881db402b1b/Picture3.png?width=700&auto=webp&quality=80&disable=upscale)

Devolver Digital 이미지 제공.

게다가 순수한 플레이어의 관점에서 보면 최종 편집본에만 등급이 매겨지기 때문에 촬영과 편집 단계 모두에서 플레이어에게 피드백을 제공하는 것이 거의 불가능하다는 것을 깨달았습니다. 방송이 방영된 후에는 플레이어에게 산더미 같은 피드백을 던져주고 플레이어가 이를 분석해 주기를 바라야 했습니다.

이 문제를 해결하려면 편집 단계를 완전히 생략하고 전체 프로그램을 라이브 스트리밍으로 재구성해야 했습니다. 이를 통해 기술적 수준에서 큰 안도감을 얻었고 시청자 수와 댓글을 통해 실시간 피드백을 제공할 수 있는 다이제틱한 방법을 확보할 수 있었습니다. 하지만 이 과정에서 가장 큰 디자인 문제가 드러나기도 했습니다.

### 한 사람의 쓰레기 TV

특히 리얼리티 TV에서는 그 정의가 매우 다양할 수 있기 때문에 우리는 "좋은" 또는 "나쁜" TV를 정의하고 싶지 않았습니다. 하지만 게임의 실패 상태는 쇼가 취소되는 것이며, 이는 플레이어의 영상에 등급을 매기는 것을 의미한다는 것도 알고 있었습니다. 이 두 가지 아이디어는 서로 모순되는 것처럼 느껴졌지만, 시청자 자체의 아이디어에 완전히 집중하기 전까지는 오랜 시간 동안 필요했습니다. 좀 더 구체적으로 말하자면, 여러 시청자.

![](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltf93230e39274f4c1/66da6a57eafc0a335c720489/Picture4.png?width=700&auto=webp&quality=80&disable=upscale)

Devolver Digital 이미지 제공.

각자의 만족 기준과 정체성을 가진 여러 시청자를 확보함으로써 개발자로서 '좋은' 리얼리티 TV가 무엇인지에 대한객관적인 의견을제시할 수 있게 되었습니다. 실제로 이 시스템을 통해 거의 모든 유형의 리얼리티 TV 시청자의 의견을 반영할 수 있었습니다. 더 중요한 것은 재미있었다는 점입니다! 우리는 언어를 단순화하기 위해 '갈증'을 '해소'해야 하는 용어를 만들었습니다(이 시스템 구현을 담당한 수석 프로그래머인 벤 오비코야는 "갈증-인간 사수"라는 악명 높은 표현을 사용하게 되었습니다). 또한 이모티콘과 댓글을 제공함으로써 청중에게 갈증에 대한 힌트를 제공할 뿐만 아니라 갈증을 더욱 정의하고 차별화할 수 있었습니다.

### 보는 방식

디자인이 다듬어지면서 플레이어가 실제로 무엇을 촬영하고 있는지 파악하는 기술적 문제도 해결해야 했습니다. 이 문제의 시작은 카메라에서 감지하고자 하는 모든 정보를 나타내는 시청률 태그, 즉 V태그였습니다. 처음에는 관련 오브젝트에 부모를 둔 단순한 구체 충돌기인 필름블에서 방출되는 '엉덩이', '출연자', '라이트하우스'와 같은 단순한 태그였습니다.

하지만 이 시스템으로는 다른 오브젝트 뒤에 숨겨진 오브젝트를 설명할 수 없고, 출연진과 집이 온전히 구체로 구성되어 있지 않다는 사실을 고려할 때 분석할 수 있는 카메라의 시야를 더 정확하게 표현해야 한다는 것을 알았습니다. 수석 프로그래머 닐 굿맨은 장면의 각 물체를 다른 색으로 렌더링한 다음 마우스 아래 픽셀의 색을 확인하여 물체를 식별하는 오래된 마우스 선택 알고리즘에서 영감을 얻었습니다.

![](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt5a5d0fe1c7b0fd4e/66da6a922ab38e81ce498fcc/Picture5.png?width=700&auto=webp&quality=80&disable=upscale)

Devolver Digital 이미지 제공.

따라서 낮은 프레임 속도(5fps)에서 특수 셰이더를 사용하여 게임을 작은(320x180) 오프스크린 텍스처로 렌더링했습니다. 셰이더는 관심 없는 오브젝트에는 빨간색 단색을 사용했고, 녹색과 파란색 채널은 필름 가능한 오브젝트의 고유 ID를 인코딩하는 데 사용했습니다. 투명한 오브젝트의 경우, 기본 파란색/녹색 값을 조정하지 않기 때문에 그 뒤에 있는 오브젝트에 작은 수준의 빨간색을 적용했습니다. 따라서 GPU에서 텍스처를 다시 읽고 모든 픽셀을 반복함으로써 어떤 필름블이 화면인지뿐만 아니라 뒤에 있는 창 수나 화면 공간을 얼마나 차지하는지와 같은 다른 지표까지 확인할 수 있었습니다.

### 다른 사람의 두뇌에 관하여

하지만 이러한 주요 기술 및 디자인 질문에 대한 답을 찾으면서도 플레이어가 같은 콘텐츠를 반복해서 촬영하는 것을 어떻게 막아야 하는지, 어떤 시청자가 다른 시청자보다 본질적으로 더 쉽게 만족하는 것을 어떻게 막아야 하는지(항상 주먹다짐은 없지만 엉덩이는 항상 있습니다) 같은 세부적인 문제가 남아있었습니다. 가장 큰 문제는커뮤니케이션이었습니다. 수많은 반복을 통해 사전 테스트 버전과 최신 버전 사이를 연결했지만, 플레이어가 이러한 시스템을 어떻게 이해할 수 있을지에 대해서는 구체적으로 집중하지 못했습니다. 이 게임플레이 모드를 '해결'하려는 모든 시도에서 플레이어의 기대와 이해를 충분히 고려하지 않았다는 사실을 깨달았습니다.

그래서 UI 디자이너 엠마 모린(Emma Morin)과 게임/레벨 디자이너 핀 카니(Finn Carney)가 최종 반복 작업을 맡았습니다. 우선, 상징적인 '캠코더' UI를 가능한 한 많이 없애는 것은 물론, 모든 것이 '다이제틱'해야 한다는 생각을 근본적으로 배제하기로 결정했습니다. 이것은 낯설고 새로운 시스템이었기 때문에 댓글, 캐스트 작업, 아이콘, 자막을 위한 공간이 필요했습니다. 근거 있는 미학을 부여하려고 노력해서 얻은 모든 것이 가독성이 떨어지면 사라지게 됩니다.

![](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt15df552f1371d522/66da6ab80982766c56cf7546/Picture6.gif?width=700&auto=webp&quality=80&disable=upscale)

Devolver Digital 이미지 제공.

그리고 반대편에서는 현재 갈증이 해소되고 있는 모든 갈증 아이콘 위에 관련 시청자의 크고 육즙이 흐르는 아이콘을 배치하고, 플레이어가 이를 촬영할 때마다 점수를 부여했습니다(이전에는 플레이어가 갈증을 완전히 해소한 후에만 점수를 부여했었습니다). 이로 인해 플레이어는 한 프레임에 최대한 많은 것을 담아내려고 노력하게 되고, 결과적으로 화면이 상당히 복잡해질 수 있습니다. 하지만 플레이어가 무언가에 대한 보상을 기대한다면 당연히 그래야 한다고 생각했습니다. 너무 많이 찍는다고 누가 뭐라고 하겠습니까?

밸런스를 맞추기 위해 추가 시스템을 추가했습니다. 갈증이 해소되면 짧은 시간 동안 "고갈"되어 플레이어가 다른 촬영 장면을 찾도록 유도했습니다. '오버플로'는 플레이어가 이미 만족한 시청자에게서 계속 얻던 포인트를 현재 불만족한 시청자에게 대신 지급하도록 했습니다. '스왑 아웃' 메커니즘은 포인트가 없는 청중이 포인트 임계값이 낮은 무작위 새 청중으로 대체되는 것을 의미했습니다. 마지막으로, '온 파이어' 메커니즘은 한 번에 여러 시청자를 만족시키면 추가 점수를 부여하여 플레이어에게물질적인 격려뿐만 아니라 게임에서 가장 보상이 큰 맥시멀리즘 촬영 스타일을 채택하도록 장려하는동기를제공했습니다 .

### 렌즈를 통해

이러한 최종 변경 사항을 적용하면서 아이러니하게도 전체 시스템의 중심이 되는 카메라 자체로 초점을 옮겼습니다. 특히 게임 루프가 최종 디자인과 관련이 있을 만큼 충분히 안정화될 때까지는 카메라에 집중하지 않았습니다. 일부 메커니즘은 쉽게 결정할 수 있었습니다(줌이 없는 카메라 게임이 있을까요?). 다른 메커니즘은 그렇지 않았습니다. 예를 들어 뎁스 오브 필드(뎁스 오브 필드)가 그렇습니다.

![](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltcc33427c44427a95/66da6adb92d0374ccead9395/Picture7.png?width=700&auto=webp&quality=80&disable=upscale)

데볼버 디지털 이미지 제공.

일부 사진 게임에는 수동 피사계 심도 슬라이더가 있는데, 특히 초기에 초점에 대한 갈증이 많았던저희 팀원 중 일부는 더 크러쉬 하우스에이 슬라이더를 원했습니다 . 하지만 게임의 빠른 속도를 고려할 때 플레이어는 기껏해야 이 기능을 완전히 무시하거나 최악의 경우 실수로 게임 내내 흐릿한 화면에 갇히는 경우가 발생하기 쉬웠습니다. 따라서 저희는 플레이어가 직접 제어할 수 없는 상황으로 인해 불이익을 받지 않도록 자동 초점 기능만 제공하고 갈증은 초점 수준을 무시하도록 변경하여 출시했습니다.

마지막에야 우선순위를 둔 주요 요소는 오브젝트의 프레임 방식이었습니다. 저희는 프레임 내 위치가 반드시 "재미있는" 게임플레이 메커니즘이 아니라고 판단했습니다(참조: 포켓몬 스냅에서 피사체를 프레임 중앙에 배치해야 한다는 모든 불만 사항). 대신, 촬영 가능한 화면 픽셀의 비율을 사용하여 프레임 크기를 지정했습니다. 이렇게 하면 최소 프레임 크기에 대한 임계값을 설정하여 카메라가 의미 있게 볼 수 있는 물체에 대해서만 V태그를 생성할 수 있을 뿐만 아니라 얼굴, 예술품, 엉덩이 클로즈업과 같이 프레임이 특히 커야 하는 사물에 대한 갈증도 해소할 수 있었습니다.

플레이어가 출연자를 본질적으로 '고정'할 수 있는 타겟 잠금 기능은 접근성 문제에서 출발했습니다. 저희는 이 게임이 1인칭 게임을 즐기지 않는 플레이어를 끌어들일 수 있고, 플레이어가 출연진 주위를 '선회'할 수 있게 하면 카메라 조작에 능숙하지 않아도 움직임과 프레임에 집중할 수 있다는 것을 알았습니다. 재미있는 사실은 타겟 락의 일부인 기대기 기능이 여러 번 잘릴 뻔했다는 점입니다. 첫 번째 언론 시연에서 여러 기자들이 영화 학생들의 '더치 앵글' 기능에 대한 갈증을 구체적으로 언급했기 때문에 이 기능을 계속 사용할 수 있었습니다.

### 리어 윈도우

더 크러쉬 하우스에서촬영 방식을 연마하면서 막다른 골목과 유턴이 많았지만, 그 과정에서 얻은 교훈을 한마디로 요약하자면 이런 것입니다:

특히 새로운 게임플레이 모드를 탐색할 때는 가장 쉬운 방법이 가장 좋은 방법일 때가 많습니다. 실제로 영상을 녹화하고 편집하는 것이 재미있고 기술적으로 가능하든, 예술에 대한 객관적인 점수를 찾는 것이든, 문제가 너무 크게 느껴진다면 아마도 그럴 것입니다. 이러한 큰 문제를 줄이기 위해 취한 모든 조치는 문제를 해결할 수 없는 개발 지옥에서 벗어날 수 있게 했을 뿐만 아니라, 게임플레이 촬영에 새로운 기회를 열어주었습니다.

마찬가지로 항상 플레이어의 렌즈를 통해 생각하세요. 플레이어가 시스템을 이해하고 재미있게 즐길 수 없다면 복잡하고 완벽하게 설계된 시스템이나 시스템의 모든 측면에 대한 깊은 수준의 제어는 의미가 없습니다. 플레이어가 게임과 어떻게 상호작용할지 먼저 파악한 다음, 플레이어가 의미 있게 참여할 수 있는 범위 내에서 복잡성을 설계하세요.

우리 중 누구도 게임플레이 메커니즘으로 촬영을해결했다고착각하지 않습니다 . 사실 최종 디자인이 어떻게 완성되었는지에 대한 비판도 많았습니다. 하지만 우리 모두는 디자인하기 정말 어렵지만 정말 재미있는 메커니즘의 가능성을 의미 있게 탐구한 것에 자부심을 느끼며, 다음번에는 누가 이 문제를 해결할지 무척 기대하고 있습니다.

자세히 읽어보세요:

[심층 분석톱](https://www.gamedeveloper.com/keyword/deep-dives)[스토리특징스포트라이트](https://www.gamedeveloper.com/keyword/features)[시리즈](https://www.gamedeveloper.com/keyword/spotlight-series)

[](https://www.linkedin.com/sharing/share-offsite/?url=https://www.gamedeveloper.com/design/deep-dive-developing-a-rating-system-and-recording-tv-in-the-crush-house)[](https://www.facebook.com/sharer/sharer.php?u=https://www.gamedeveloper.com/design/deep-dive-developing-a-rating-system-and-recording-tv-in-the-crush-house)[](https://www.twitter.com/intent/tweet?url=https://www.gamedeveloper.com/design/deep-dive-developing-a-rating-system-and-recording-tv-in-the-crush-house)[](https://www.gamedeveloper.com/cdn-cgi/l/email-protection#ccf3bfb9aea6a9afb8f188a9a9bcec88a5baa9f6ec88a9baa9a0a3bca5a2abecadecbeadb8a5a2abecbfb5bfb8a9a1ecada2a8eca1ada7a5a2abeca6b9a5afb5ec989aeca5a2ec98a4a9ec8fbeb9bfa4ec84a3b9bfa9eaada1bcf7aea3a8b5f185e9fefcb8a4a3b9aba4b8e9fefcb8a4a9e9fefcaaa3a0a0a3bba5a2abe9fefcaabea3a1e9fefc8bada1a9e9fefc88a9baa9a0a3bca9bee9fefca1a5aba4b8e9fefca5a2b8a9bea9bfb8e9fefcb5a3b9e2e9fc88e9fc8de9fc88e9fc8de9fefc88a9a9bce9fefc88a5baa9e9ff8de9fefc88a9baa9a0a3bca5a2abe9fefcade9fefcbeadb8a5a2abe9fefcbfb5bfb8a9a1e9fefcada2a8e9fefca1ada7a5a2abe9fefca6b9a5afb5e9fefc989ae9fefca5a2e9fefc98a4a9e9fefc8fbeb9bfa4e9fefc84a3b9bfa9e9fc88e9fc8da4b8b8bcbfe9ff8de9fe8ae9fe8abbbbbbe2abada1a9a8a9baa9a0a3bca9bee2afa3a1e9fe8aa8a9bfa5aba2e9fe8aa8a9a9bce1a8a5baa9e1a8a9baa9a0a3bca5a2abe1ade1beadb8a5a2abe1bfb5bfb8a9a1e1ada2a8e1bea9afa3bea8a5a2abe1b8bae1a5a2e1b8a4a9e1afbeb9bfa4e1a4a3b9bfa9)[](https://www.reddit.com/submit?url=https://www.gamedeveloper.com/design/deep-dive-developing-a-rating-system-and-recording-tv-in-the-crush-house&title=Deep%20Dive%3A%20Developing%20a%20rating%20system%20and%20making%20juicy%20TV%20in%20The%20Crush%20House)

## 저자 소개

[![Finn Carney](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltd709c2f6ad0896cd/66df238c1ceec85b3ae644da/Game_Developer_G_Logo_RGB.webp?width=400&auto=webp&quality=80&disable=upscale "Finn Carney")](https://www.gamedeveloper.com/author/finn-carney)

[

핀 카니

](https://www.gamedeveloper.com/author/finn-carney)

[핀 카니의 더보기](https://www.gamedeveloper.com/author/finn-carney)

게임 개발자의 일일 뉴스, 개발자 블로그, 스토리를 받은 편지함으로 바로 받아보세요.

[최신 소식 받기](https://gd-resources.gamedeveloper.com/free/w_gamf01/prgm.cgi)

추천 콘텐츠

* * *

원문: [https://www.gamedeveloper.com/design/deep-dive-developing-a-rating-system-and-recording-tv-in-the-crush-house](https://www.gamedeveloper.com/design/deep-dive-developing-a-rating-system-and-recording-tv-in-the-crush-house)