---
title:  "레인보우 6 SMOL: 디자인 심층 분석"

categories:
  - 번역
  
tags:
  - The Why Of Play
toc: true
toc_sticky: true
 
date: 2024-11-26
last_modified_at: 2024-11-26
---
_**면책 조항**: 여기에 표현된 모든 생각은 본인의 생각이며 어떤 자격으로도 공식적이거나 고용주를 대표하지 않습니다._

## 소개

Rainbow 6: SMOL은 Ubisoft에서 개발한 아이소메트릭 로그라이트 슈팅 게임으로, 올해 2월에 iOS와 Android에서 넷플릭스 독점 타이틀로 출시되었습니다.

F2P 게임 디자이너로서 프리미엄 게임은 수익화가 게임 메커니즘과 시스템 설계에 대한 결정을 좌우하지 않는 모바일 게임을 경험하고 분석할 수 있는 기회를 제공하며, 이를 통해 참여도와 리텐션, 즉 '재미'를 중심으로 한 게임플레이와 기타 메커니즘에 집중할 수 있게 해줍니다.

이 게임을 특별히 선택한 이유 중 하나는 제 관심과 시간을 성공적으로 사로잡은 몇 안 되는 프리미엄 게임 중 하나이기 때문이라고도 할 수 있습니다. 그리고 기쁘게도 좋은 시간을 보냈습니다.

이 게임이 제 관심을 끌 수 있었던 이유를 이해하기 위해 이 특별한 기사를 작성하게 되었습니다. 그렇다면 Rainbow 6 : SMOL의 장점은 무엇일까요?

## 레인보우 6 IP와의 연관성

전통적인 레인보우 6 프랜차이즈는 파괴 가능한 환경과 오퍼레이터를 통한 클래스 기반 게임플레이를 갖춘 사실적인 1인칭 전술 슈팅 게임으로 알려져 있습니다.

![](https://thewhyofplay.com/wp-content/uploads/2024/11/image.png?w=709)

다양한 오퍼레이터와 파괴 가능한 환경으로 유명한 레인보우 6

Rainbow 6: SMOL은 전통적으로 하드코어한 AAA 콘솔/PC 중심의 공식에서 약간 벗어났으며(제 생각에는 당연히 그렇죠), 훨씬 더 캐주얼한 아트 스타일의 모바일 친화적인 아이소메트릭 로그 라이트 슈팅 게임으로 이 프랜차이즈에 자신만의 기발한 해석을 가져왔습니다. 또한 오리지널 R6 IP와의 연결고리를 다음과 같이 유지합니다.

**플레이어 클래스:** R6: 시즈에서는 플레이어가 스킬을 통해 다양한 플레이 가능한 클래스를 대표하는 오퍼레이터를 선택하지만, R6: SMOL에서는 미리 정의된 일반적인 플레이어 클래스가 있습니다.

![](https://thewhyofplay.com/wp-content/uploads/2024/11/image-1.png?w=1024)

운영자는 Rainbow 6에서 전통적으로 클래스 역할을 수행합니다

.

**파괴 가능한 환경:** R6 게임의 또 다른 특징으로는 무엇보다도 문을 걷어차는 전용 버튼이 있을 정도로 R6:SMOL에 의도적으로 통합된 파괴 가능한 환경이 있습니다.

**운영자** : R6: SMOL에서 운영자는 플레이 가능한 캐릭터가 아니라 별도의 NPC 스킬을 통해 핵심 게임에서 플레이어를 보조하는 NPC입니다. 이 시리즈를 잘 아는 사람이라면 누구나 이 오퍼레이터를 알아볼 수 있습니다(배경 지식과 함께!)

![](https://thewhyofplay.com/wp-content/uploads/2024/11/image-2.png?w=1024)

닮은꼴이 묘하다!

그러나 이 게임이 R6 IP를 얻기 전, 이미 약 2년 전 < href="https://youtu.be/3Z2jzit\_ke4?si=uRa8JC5vEofjCn9d">클라우드섬 게임즈(아마도 유비소프트의 화이트 레이블)에서 퍼블리싱한 '타이니'라는 이름으로 시장에 출시되었다는 점이 흥미롭습니다.

![](https://thewhyofplay.com/wp-content/uploads/2024/11/image-7.png?w=1024)

게임은 약간의 시각적 변화를 겪었지만 게임플레이 측면에서는 대부분 동일하게 유지되었습니다

.

## 게임플레이

R6: SMOL은 다이렉트 포트(이미 실제 F2P 버전이 있습니다)라는 일반적인 관행에서 벗어나, 전술 슈팅 게임에 뿌리를 두고 있지만 상대적으로 더 캐주얼한 로그라이트 슈팅 게임으로 접근하는 방식을 택했습니다.

![](https://thewhyofplay.com/wp-content/uploads/2024/11/image-9.png?w=950)

슈터리픽 재미!

이 결정의 배경에는 플랫폼, 수익화 모델 등 여러 가지 이유 중 하나가 작용했을 수도 있고, 상대적으로 재정적으로 더 보장된 F2P 포트에서 하드코어 팬을 외면할 가능성 없이 고립된 플랫폼에서 게임의 관심을 안전하게 측정할 수 있는 보다 캐주얼한 Rainbow 6 게임에 대한 Ubisoft의 실험으로 Rainbow 6 IP에 더 많은 시선과 잠재적인 관심을 얻기 위한 시도일 수도 있습니다.

### 핵심 루프

추측은 제쳐두고, R6:SMOL에서 플레이어는

*   맵에 로드할 캐릭터 클래스를 선택하는 것으로 시작합니다. 맵 내에서 일련의 미션을 완료하여 맵을 '해방'하는 것이 목표입니다.

<그림 class="wp-block-이미지 크기-대형">![](https://thewhyofplay.com/wp-content/uploads/2024/11/image-10.png?w=1024)

사후 리플레이에서도 각 캐릭터는 고유한 개성을 유지합니다(헬다이버처럼)

.

*   지도에서 '해방'할 지역과 작전을 선택하세요.

![](https://thewhyofplay.com/wp-content/uploads/2024/11/image-25.png?w=1024)

별거 아닌데, 약간 살인적인 느낌입니다. 나쁜 놈들을 암살할지도 모르죠.

*   작전 시작 시 다양한 스탯 부스트 또는 NPC 분대원(오퍼레이터) 등 여러 특전 중 하나를 선택합니다.

<그림 class="wp-block-이미지 크기-대형">![](https://thewhyofplay.com/wp-content/uploads/2024/11/image-11.png?w=1024)

선택으로 각 세션 시작

*   작전 중 적을 처치하고 목표를 완료하여 스킬 포인트를 획득하고 이 포인트를 사용하여 일시적으로 레벨을 올리고 능력치를 향상하거나 캐릭터 직업의 영구 특전을 잠금 해제할 수 있습니다.

![](https://thewhyofplay.com/wp-content/uploads/2024/11/image-12.png?w=1024)

*   **추가** 미션을 완료하면 영구적인 전역 스탯 업그레이드를 부여하는 데 사용되는 크레딧(직업에 묶이지 않음)

![](https://thewhyofplay.com/wp-content/uploads/2024/11/image-52.png?w=1024)

맵 해방 전 임무 수행 중 플레이어가 사망하면 모든 능력치, 특전, 누적 재화를 잃고 새로운 캐릭터(및 클래스)로 다시 시작해야 합니다. 리스폰 시 선택되는 병과 유형은 무작위입니다.

![](https://thewhyofplay.com/wp-content/uploads/2024/11/image-14.png?w=1024)

운영자와 패치 없이 새로운 신병으로 죽음에서 다시 시작하세요

### 게임플레이 경험

이 게임은 아이소메트릭 카메라를 사용하여 가로로 플레이합니다. 독특하고 기발한 아트 스타일과 함께 똑같이 기발한 UI, UX 및 오디오 디자인이 특징입니다.

플레이어의 기대와 완전히 상반되는 방식이라고 주장할 수도 있습니다. 하지만 저처럼 Rainbow 6 게임을 한 번도 해본 적이 없는 사람에게는 시각적 미학에 대한 이러한 접근 방식이 재미있고 신선했으며 실제로 게임을 플레이하는 데 큰 기여를 했습니다.

#### 컨트롤

<그림 class="wp-block-이미지 크기-대형">![](https://thewhyofplay.com/wp-content/uploads/2024/11/image-17.png?w=1024)

플레이어에게 오퍼레이터가 동행하면 오른쪽에 오퍼레이터 스킬도 표시됩니다. 지금까지는 3명의 오퍼레이터를 미션에 동행할 수 있었지만, UI는 최대 4명까지 수용할 수 있을 것 같습니다.

이동과 조준 컨트롤의 조합은 게임을 훨씬 더 아케이드처럼 만들고, 전반적인 게임 플레이는 매우 혼란스럽습니다. 게임 후반부에는 사격을 자동화하는 옵션이 있어 오퍼레이터 스킬 사용과 캐릭터 이동에 집중할 수 있습니다.

#### 환경 디자인

원작 IP에 충실한 R6: SMOL은 파괴 가능한 환경 요소와 특히 중독성 있는 '도어 바스트' 메카닉이 특징입니다.

![](https://thewhyofplay.com/wp-content/uploads/2024/11/kick-door.gif?w=1024)

문을 차는 것은 전술적이지요?

Sledge와 같은 특정 운영자는 벽을 부수는 능력으로 지름길을 개척할 수 있습니다.

벽을 부수는 능력 외에도 게임의 특정 지점에서 약간의 플랫폼 플레이를 추가하는 환경 함정도 있지만, 대부분 선택 사항입니다.

![](https://thewhyofplay.com/wp-content/uploads/2024/11/envi.gif?w=1024)

사물이 정말 빨리 '가열'될 수 있습니다

환경은 또한 전쟁의 안개, 발자국 감지, 부비트랩을 통해 은신할 수 있는 기회를 제공합니다.

지도에는 크레딧과 게임 내 지식이 흩어져 있어 탐험을 장려합니다.

요약하자면, R6: SMOL은 전술 슈팅, 액션 로그라이트, 총알 지옥의 교차점에 위치하며, 해당 장르의 메커니즘을 차용하여 캐주얼하고 재미있는 로그라이트 경험을 선사합니다.

![](https://thewhyofplay.com/wp-content/uploads/2024/11/image-28.png?w=1024)

## 프로그레션

R6:SMOL에는 여러 가지 진행 벡터가 있으며, 각 진행 벡터는 게임 시스템의 특정 부분을 나타냅니다. 가장 주목할 만한 것은

*   지도
*   캐릭터 클래스
*   운영자
*   패치

### 지도

게임의 콘텐츠 진행은 지도를 통해 시각화됩니다. 지도는 국가를 포함하는 대륙으로 나뉘며, 대륙은 다시 여러 지역으로 구성됩니다.

각 지역은 여러 개의 일련의 노드로 구성되며, 각 노드를 '작전'이라고 합니다.

![](https://thewhyofplay.com/wp-content/uploads/2024/11/image-19.png?w=1024)

작업은 하나의 게임플레이 세션을 나타냅니다. 작전 유형은 세션의 목표를 정의하며, 다음과 같은 여러 유형이 있습니다.

*   암살/타겟 처치
*   폭탄 확산
*   탑 방어하기
*   인질 구하기 등

플레이어는 작전을 완료하여 새로운 유형의 특전(세션 전 선택 사항), 플레이 가능한 직업 및 오퍼레이터를 잠금 해제합니다. 게임 내 콘텐츠 잠금 해제의 원천입니다.

지역을 완료하려면 플레이어는 일련의 작전을 완료해야 합니다. 플레이어는 지도에서 사용할 수 있는 다양한 경로에 따라 어떤 유형의 작전을 선택할 수 있습니다.

작전에 실패하면 세션이 종료되고 해당 경로가 닫힙니다. 그리고 플레이어는 해당 지역을 완료하기 위해 지점 끝으로 가는 다른 경로를 찾아야 하며, 이는 Slay the Spire의 맵과 매우 유사합니다.

실패하면 획득한 크레딧 일부, 누적된 모든 패치, 오퍼레이터 및 스킬 스탯을 잃는 등의 다른 결과도 발생합니다.

![](https://thewhyofplay.com/wp-content/uploads/2024/11/image-26.png?w=1024)

죽음이 가혹한 선생님이 될 수 있지만 적어도 노력은 했잖아요!

경로는 종종 분기하고 서로 교차하며, 플레이어는 분기점에서 갈래를 바꿀 수 있습니다.

플레이어가 무료 임무 특전이나 오퍼레이터를 획득할 수 있는 작전 대신 '휴식 구역'이 노드에 생성될 가능성이 있습니다. 이 휴식 지대는 메타를 진행하면 잠금 해제됩니다.

![](https://thewhyofplay.com/wp-content/uploads/2024/11/image-21.png?w=1024)

각 경로에서 가능한 작업의 종류와 난이도에 따라 플레이어가 현명하게 경로를 선택해야 합니다

.

일반적으로 플레이어는 3~6개의 작전을 완료해야 한 지역을 완료할 수 있습니다. 한 지역을 완료하면 인접한 새로운 지역이 잠금 해제되고, 한 국가 내의 모든 지역을 완료하면 새로운 국가가 잠금 해제됩니다.

![](https://thewhyofplay.com/wp-content/uploads/2024/11/image-27.png?w=1024)

모든 국가를 완료하면 새로운 대륙 등이 잠금 해제됩니다.

![](https://thewhyofplay.com/wp-content/uploads/2024/11/image-22.png?w=1024)

몇 시간에 걸쳐 플레이할 수 있는 콘텐츠가 꽤 많습니다(10시간도 가능)

.

### 캐릭터 클래스

R6:SMOL에서 플레이어는 다양한 클래스를 선택하여 플레이할 수 있습니다. 플레이어가 클래스를 선택하면 사망할 때까지 해당 클래스/캐릭터에 고정됩니다.

![](https://thewhyofplay.com/wp-content/uploads/2024/11/image-29.png?w=1024)

클래스에 따라 능력치와 사용하는 무기가 다릅니다. 무기 자체도 사거리, 피해량, 범위, 클립 크기가 다릅니다.

캐릭터는 두 가지 진행 경로를 통해 성장할 수 있으며, 두 경로 모두 동일한 자원인 스킬 포인트를 사용합니다. 스킬 포인트는 세션 중에 어느 쪽에 투자할 수 있습니다.

*   **스탯 업그레이드** \- 플레이어가 사망하면 이 스탯은 손실되지만, 현재 세션 동안 캐릭터를 더 강하게 만들어 더 어려운 지역과 국가에서 생존 확률을 높입니다.

<그림 class="wp-block-이미지 크기-대형">![](https://thewhyofplay.com/wp-content/uploads/2024/11/image-31.png?w=1024)

*   **클래스 업그레이드** - 클래스 업그레이드는 영구적이며 다른 게임에서 볼 수 있는 '마스터리'와 동일합니다. 직업에 포인트를 투자하면 플레이어가 해당 직업에 사용할 수 있는 새로운 무기와 스킨을 잠금 해제할 수 있습니다.

![](https://thewhyofplay.com/wp-content/uploads/2024/11/image-32.png?w=1024)

세션에서 플레이어는 스탯을 통해 캐릭터를 즉시 강화할지, 아니면 새로운 무기를 잠금 해제하여 직업의 플레이 스타일을 최적화할지 결정해야 합니다.

스킬 포인트를 투자할 수 있는 스탯은 매우 다양합니다. 일시적인 스탯 부스트 외에도 플레이어가 작전을 통해 획득한 크레딧을 사용하여 능력서를 영구적으로 업그레이드할 수도 있습니다.

![](https://thewhyofplay.com/wp-content/uploads/2024/11/image-30.png?w=1024)

작전 중 플레이어가 사망하면 캐릭터와 함께 누적된 모든 특전, 오퍼레이터, 능력치가 '손실'됩니다.

사망 시 병과가 변경되는 이 시스템으로 인해 플레이어는 스킬 포인트를 어떻게 투자할지 결정해야 하는 미묘한 상황에 처하게 됩니다.

이러한 이유로 플레이어는 크레딧으로 과거에 사망한 캐릭터를 '부활'할 수 있는 옵션이 있습니다. 캐릭터의 레벨이 높을수록 부활하는 데 더 많은 비용이 듭니다.

![](https://thewhyofplay.com/wp-content/uploads/2024/11/image-33.png?w=1024)

각자의 외모, 성격, 개성을 가진 리크루트들이 더 멋집니다!

새로운 병과 유형은 맵의 특정 지역에서 목표를 완료하여 잠금 해제할 수 있습니다.

### 운영자

R6:SMOL에서 오퍼레이터는 플레이어가 작전 수행 시 함께할 수 있는 NPC 동료입니다.

이들은 스쿼드 게임플레이의 역할을 수행하며, 레인보우 6에서 영감을 받은 전술적 스킬 사용을 통해 게임플레이의 깊이를 더합니다.

![](https://thewhyofplay.com/wp-content/uploads/2024/11/image-34.png?w=1024)

운영자는 액티브 스킬(능력)과 패시브 스킬을 가지고 있습니다. 액티브 스킬은 게임에서 버튼으로 표시되며, 패시브 스킬은 플레이어와 스쿼드의 다른 오퍼레이터에게 스탯 부스트를 제공합니다.

![](https://thewhyofplay.com/wp-content/uploads/2024/11/image-35.png?w=1024)

오퍼레이터는 오퍼레이션을 완료하여 업그레이드할 수 있습니다. 오퍼레이터를 업그레이드하면 새로운 액티브 스킬, 패시브 스킬, 스킨, 장착 무기를 잠금 해제할 수 있습니다.

![](https://thewhyofplay.com/wp-content/uploads/2024/11/image-36.png?w=1024)

게임 플레이 중 플레이어에게 표시되는 오퍼레이터는 사용 가능한 오퍼레이터 풀에서 무작위로 선택됩니다. 플레이어가 사망하면 사라집니다.

각 오퍼레이터는 각기 다른 기술을 가지고 있습니다. 일반적으로 공격형, 방어형 또는 유틸리티 기반일 수 있습니다.

<그림 class="wp-block-이미지 크기-대형">![](https://thewhyofplay.com/wp-content/uploads/2024/11/castle.gif?w=1024)

운영자 능력은 다양하지만 플레이 스타일과 팀 구성에 따라 가장 잘 활용됩니다

새로운 오퍼레이터는 작전을 수행하여 맵의 특정 지역에서 구출하면 잠금 해제됩니다.

### 패치

패치는 플레이어가 작전을 수행하는 동안 선택할 수 있는 특전입니다.

일반적으로 플레이어는 패치 또는 오퍼레이터의 3가지 옵션 중 하나를 선택할 수 있습니다.

![](https://thewhyofplay.com/wp-content/uploads/2024/11/image-37.png?w=1024)

패치는 다음과 같은 다양한 효과를 낼 수 있습니다.

*   스탯 부스트
*   공격 수정자
*   HP 회복
*   통화 부스트 등

패치는 게임 내 또는 메타를 개선할 수 있는 수단이나 방법이 없습니다. 또한 다른 패치나 캐릭터 클래스와의 시너지 효과도 없습니다.

![](https://thewhyofplay.com/wp-content/uploads/2024/11/image-39.png?w=917)

각자의 정체를 모르겠지만 너무 귀여워요!

지도에서 목표를 완료하면 잠금이 해제되며, 잠금이 해제되면 공통 선택 풀에 추가됩니다.

## 기타 기능

R6:SMOL은 싱글 플레이어 프리미엄 게임이기 때문에 메타게임 기능 측면에서 많은 시도를 하지 않습니다. 이 게임은 리텐션을 위해 메타에서 다음과 같은 몇 가지 기본 기능을 사용합니다.

### 권력의 책

권력의 서에는 다른 로그라이트 게임에서 볼 수 있는 재능 시스템과 유사한 다양한 가지와 고유한 진행 방식이 있습니다.

![](https://thewhyofplay.com/wp-content/uploads/2024/11/image-44.png?w=1024)

각 탭은 게임의 특정 측면을 전문으로 다룹니다

.

권력의 서는 또한 특전 선택의 재롤 횟수 증가, 특전 및 캐릭터 클래스 옵션, 화폐 한도 증가, 추가 생명력 등 다른 게임 내 특전을 부여하고 맵에 휴식 구역을 생성하여 맵 선택 사항을 변경할 수도 있습니다.

![](https://thewhyofplay.com/wp-content/uploads/2024/11/image-42.png?w=1024)

### 목적

목표는 특정 지역과 연계된 목표입니다. 패치와 클래스 등 맵의 새로운 콘텐츠를 잠금 해제하는 관문으로 사용됩니다.

![](https://thewhyofplay.com/wp-content/uploads/2024/11/image-45.png?w=964)

목표도 플레이어가 다른 직업으로 같은 미션을 다시 플레이할 수 있도록 합니다.

### 바운티

플레이어에게 크레딧을 보상으로 지급하는 글로벌 업적을 말합니다.

![](https://thewhyofplay.com/wp-content/uploads/2024/11/image-47.png?w=940)

### 베스트스토리 및 진행 상황 추적

이 게임을 통해 플레이어는 게임 진행 상황과 함께 자신이 만나고 쓰러뜨린 다양한 종류의 적을 추적할 수 있습니다.

![](https://thewhyofplay.com/wp-content/uploads/2024/11/image-49.png?w=1024)

Me too Assassin... me too.

### 게임 뉴스

게임의 뉴스 섹션은 작전 중에 지식 서류가방을 발견하면 게임 내 지식의 원천이 되는 역할을 합니다.

![](https://thewhyofplay.com/wp-content/uploads/2024/11/image-50.png?w=961)

## 장단점

### 강점

*   **아트스타일과 시각적 매력** - 이 게임은 컬러, 총격, 날아다니는 문이 폭발적으로 표현되는 동시에 사운드 디자인과 작문도 똑같이 유쾌합니다. 이 게임에 많은 애정을 쏟은 흔적이 역력합니다.

*   **복잡성 대 접근성의 절묘한 지점** - 이 게임은 진지하게 받아들이기 위한 것이 아니었기 때문에 메커니즘의 복잡성에 대한 접근 방식은 장르에 익숙하지 않은 사람도 쉽게 익힐 수 있을 만큼 충분히 쉽고 게임플레이의 깊이와 콘텐츠가 적절하게 조화를 이루고 있습니다. 하지만 여기에는 대가가 따릅니다.

*   **독창성을 위해 IP의 뿌리를 활용** - R6:SMOL은 파괴 가능한 환경과 분대 게임플레이를 통해 전술 슈팅 게임에 대한 독특한 해석을 제공하면서 IP에 충실하려고 노력합니다. 하드코어 FPS를 표방하지 않고 아케이드 게임플레이를 수용하는 대신 로그라이트 메커니즘을 혼합하여 폭발적이고 재미있고 기발한 경험을 선사합니다.

### 단점

*   **핵심 장르 유저층에 대한 강력한 어필 부족** \- 이 게임은 캐주얼한 매력이 강하기 때문에 정밀하고 정확한 총기 메커니즘을 갖춘 슈팅 게임을 즐기는 사람(전형적인 R6 팬)이나 로그라이트 게임의 혼돈과 복잡함을 즐기는 사람(Enter the Gungeon, Hades 등)의 요구를 충족시킬 수 없기 때문에 게임의 발목을 잡습니다.
.

*   **반복적인 게임플레이** - 로그라이트 게임의 가장 큰 매력은 무기/직업에 따른 뚜렷한 플레이 스타일과 로그라이트 스킬의 조합에 따라 형성되는 새로운 게임플레이에서 오는 의미 있는 반복성입니다. R6: SMOL은 클래스의 차별성이 충분히 느껴지지 않고 패치 선택에 따른 흥미로운 게임 내 결과의 가능성도 없기 때문에 두 부문 모두에서 부족합니다.

*   **원래 IP 팬들을 고립시킬 수 있음** - 게임플레이 관점에서 보면 핵심 IP에서 벗어난 것이 이해가 되지만, Ubisoft가 핵심 고객층에게 좀 더 어필할 수 있는 시도를 하지 않았을까 하는 의문이 들 수 있습니다. 조준과 사격이 모두 자동화된 전술 슈팅 게임은 더 이상 슈팅 게임이라고 할 수 없습니다.

## 결론

Rainbow 6:SMOL은 아트 스타일에 이끌려 순수한 호기심에 시작한 게임이었지만, 결국 예상보다 훨씬 더 많은 시간을 할애하게 된 게임이었습니다.

![](https://thewhyofplay.com/wp-content/uploads/2024/11/image-51.png?w=668)

명확하게, 그들의 우선 순위는 올바른 곳에 있습니다

이 게임은 다른 로그라이트 서바이벌 스타일의 게임들 사이에서 모든 올바른 이유로 돋보이는 게임이며, 단순하고 순수하며 재미있는 경험으로 얼굴에 미소를 남길 수 있는 게임이기 때문에 진심으로 추천하고 싶은 게임입니다.

### 이걸 공유하세요:

*   [트위터](https://thewhyofplay.com/2024/11/26/rainbow-6-smol-design-deep-dive/?share=twitter "트위터에서 공유하려면 클릭하세요")
*   [페이스북](https://thewhyofplay.com/2024/11/26/rainbow-6-smol-design-deep-dive/?share=facebook "페이스북에서 공유하려면 클릭")

좋아요 로딩 중입니다...

### _관련_

원문: [https://thewhyofplay.com/2024/11/26/rainbow-6-smol-design-deep-dive/](https://thewhyofplay.com/2024/11/26/rainbow-6-smol-design-deep-dive/)