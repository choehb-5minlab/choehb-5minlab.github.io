---
title:  "게임 내 파워 진행: 보람 있는 플레이어 경험 제작"

categories:
  - 번역
  
tags:
  - Game Developer
toc: true
toc_sticky: true
 
date: 2024-09-06
last_modified_at: 2024-09-06
---
[![Picture of Cameron McKellar](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltd709c2f6ad0896cd/657b3aae1fb1b4040a0e1821/Game_Developer_G_Logo_RGB.png?width=100&auto=webp&quality=80&disable=upscale "Picture of Cameron McKellar")](https://www.gamedeveloper.com/author/cameron-mckellar)

[카메론 맥켈러](https://www.gamedeveloper.com/author/cameron-mckellar)

9월 6일, 2024

11 분 읽기

![](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltbbb99dce25da7a97/66d938c6f949673e6c7845ec/pexels-ivan-samkov-4240497_(1).jpg?width=1280&auto=webp&quality=95&format=jpg&disable=upscale)

Ivan Samkov 이미지 제공.

[](https://www.linkedin.com/sharing/share-offsite/?url=https://www.gamedeveloper.com/design/power-progression-in-games-crafting-rewarding-player-experiences)[](https://www.facebook.com/sharer/sharer.php?u=https://www.gamedeveloper.com/design/power-progression-in-games-crafting-rewarding-player-experiences)[](https://www.twitter.com/intent/tweet?url=https://www.gamedeveloper.com/design/power-progression-in-games-crafting-rewarding-player-experiences)[](https://www.gamedeveloper.com/cdn-cgi/l/email-protection#d2eda1a7b0b8b7b1a6ef82bda5b7a0f2a2a0bdb5a0b7a1a1bbbdbcf2bbbcf2b5b3bfb7a1e8f291a0b3b4a6bbbcb5f2a0b7a5b3a0b6bbbcb5f2a2beb3abb7a0f2b7aaa2b7a0bbb7bcb1b7a1f4b3bfa2e9b0bdb6abef9bf7e0e2a6babda7b5baa6f7e0e2a6bab7f7e0e2b4bdbebebda5bbbcb5f7e0e2b4a0bdbff7e0e295b3bfb7f7e0e296b7a4b7bebda2b7a0f7e0e2bfbbb5baa6f7e0e2bbbca6b7a0b7a1a6f7e0e2abbda7fcf7e296f7e293f7e296f7e293f7e0e282bda5b7a0f7e0e2a2a0bdb5a0b7a1a1bbbdbcf7e0e2bbbcf7e0e2b5b3bfb7a1f7e193f7e0e291a0b3b4a6bbbcb5f7e0e2a0b7a5b3a0b6bbbcb5f7e0e2a2beb3abb7a0f7e0e2b7aaa2b7a0bbb7bcb1b7a1f7e296f7e293baa6a6a2a1f7e193f7e094f7e094a5a5a5fcb5b3bfb7b6b7a4b7bebda2b7a0fcb1bdbff7e094b6b7a1bbb5bcf7e094a2bda5b7a0ffa2a0bdb5a0b7a1a1bbbdbcffbbbcffb5b3bfb7a1ffb1a0b3b4a6bbbcb5ffa0b7a5b3a0b6bbbcb5ffa2beb3abb7a0ffb7aaa2b7a0bbb7bcb1b7a1)[](https://www.reddit.com/submit?url=https://www.gamedeveloper.com/design/power-progression-in-games-crafting-rewarding-player-experiences&title=Power%20progression%20in%20games%3A%20Crafting%20rewarding%20player%20experiences)

이 글에서는 게임 디자인의 기본 요소인 성장과 숙달이 인간의 성장과 숙달에 대한 욕구를 어떻게 활용하는지에 대해 살펴볼 것입니다. 플레이어이자 게임 디자이너로서 제 자신의 이해와 경험을 소개하겠습니다.

캐릭터의 레벨을 올리거나 새로운 능력을 습득하거나 강력한 장비를 잠금 해제할 때 플레이어는 더 강해지거나 능력이 향상되었을 때의 만족감을 통해 게임 세계에 계속 몰입하고 투자하게 됩니다. 게임 디자이너는 능력치 상승의 심리를 이해하면 플레이어가 더 깊이 공감할 수 있는 경험을 만들어 더욱 몰입감 있고 즐거운 게임을 만들 수 있습니다.

## 1\. 성장의 매력: 플레이어는 왜 성장을 갈망할까요?

### 내재적 동기와 외재적 동기:

게임에서 성장의 핵심은 내재적 동기와 외재적 동기 사이의 미묘한 균형에 있습니다. 내재적 동기는 기술을 습득하거나, 도전을 극복하거나, 스토리를 발견했을 때의 내적 만족감을 통해 플레이어를 움직이게 합니다. 다른 일반적인 내재적 동기로는 탐험과 호기심이 있습니다. 디트로이트: 비컴 휴먼은 플레이어의 행동에 따라 스토리가 달라지며, 플레이어가 게임을 다시 플레이하고 다른 버전의 스토리를 탐색하도록 유도하는 호기심을 이용해 이러한 유형의 동기에 크게 의존합니다.

![](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltb7e616ff61935b79/66d879fe944f3a1a0864087a/image.png?width=700&auto=webp&quality=80&disable=upscale)

반면 외재적 동기는 레벨 업, 전리품 획득, 타인으로부터 인정받는 것과 같은 외부 보상에 의해 촉진됩니다. 많은 멀티플레이어 경쟁 게임은 순위 시스템과 명성 또는 잠금 해제 가능한 스킨으로 자신의 순위를 보여줄 수 있는 기능을 통해 플레이어에게 동기를 부여합니다.

밸로란트와 콜 오브 듀티는 플레이어의 게임 숙련도 또는 전체 플레이 시간을 나타내는 아이콘을 수여합니다. 내재적 동기 부여(숙달)를 외재적 동기 부여(인정)로 전환합니다.

![](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltae6cdc701c27cfa5/66d87a19944f3a9b01640881/image.png?width=700&auto=webp&quality=80&disable=upscale)

![](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltba6080143fcdf6d6/66d87a25a3c00da66dfe2c46/image.png?width=700&auto=webp&quality=80&disable=upscale)

### 도파민의 역할:

![](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt6fe65c36e839b880/66d87a54c9ec5a4a0311db95/image.png?width=700&auto=webp&quality=80&disable=upscale)

젤다의 전설 시리즈에서도 새로운 주요 아이템을 획득할 때 이러한 축적감을 활용합니다. 이 게임은 큰 상자에는 게임의 새로운 영역에 접근할 수 있는 무언가가 들어 있을 것이라는 기대감을 조성합니다. 앞서 언급한 여러 요소를 결합하여 이 아이템의 중요성을 더욱 강조하고, 음악이 흘러나오고 애니메이션이 재생되며 링크가 상자를 여는 장면에 모든 초점을 맞춥니다.

![](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt0923a1a3c0d8373e/66d87a7fb61079681c844351/image.png?width=700&auto=webp&quality=80&disable=upscale)

### 피드백 루프:

피드백 루프는 게임 디자인의 기본 개념이며, 특히 파워 진행의 맥락에서 더욱 그렇습니다. 긍정적인 피드백 루프는 게임에서의 성공이 또 다른 성공으로 이어져 추진력과 성장의 느낌을 만들어낼 때 발생합니다. 레벨이 고정된 오픈 월드 게임에서는 플레이어가 이러한 힘의 상승을 느낄 수 있으며, 예전에는 힘들었던 적을 쉽게 처치할 수 있고 이전에는 생존할 수 없었던 지역이 이제는 플레이어가 탐험할 수 있는 플레이 영역이 될 수 있습니다.

반대로 부정적인 피드백 루프는 플레이어가 너무 빨리 전진하지 못하도록 도전을 도입하여 게임의 몰입도와 균형을 유지하는 데 사용할 수 있습니다. 마리오 카트에서는 아이템 분배 시스템에 네거티브 피드백 루프를 사용하여 레이스에서 좋은 위치를 차지할수록 아이템이 약해집니다.

![](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltd072fa11af2200c6/66d87a8b889509753ed8c994/image.png?width=700&auto=webp&quality=80&disable=upscale)

## 2\. 효과적인 진행 시스템 설계

### 도전과 보상의 균형:

효과적인 진행 시스템의 핵심은 도전과 보상의 균형에 있습니다. 게임이 너무 어렵다면 플레이어는 좌절감을 느끼고 몰입을 잃을 수 있으며, 너무 쉬우면 보상을 얻지 못했다고 느껴 성취감이 떨어질 수 있습니다. 적절한 균형을 잡는다는 것은 점진적으로 증가하는 난이도 곡선을 만들어 플레이어가 지속적으로 시험을 받으면서도 노력에 대한 보상을 지속적으로 받을 수 있도록 하는 것을 의미합니다. 이러한 균형은 플레이어가 게임에 몰입할 수 있을 만큼 충분히 도전적이지만 너무 어려워서 낙담하지 않는 '흐름' 상태를 유지하도록 합니다. Left 4 Dead2의 더 패리시 레벨에서는 디렉터 시스템이 플레이어의 진행 상황에 따라 공동묘지 통과 경로와 전투 강도를 결정하여 플레이어가 구역을 이동하는 동안 적절한 흐름 상태를 유지할 수 있도록 합니다.

![](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt6b2d118fd681292d/66d87a965026664e867a2ae6/image.png?width=700&auto=webp&quality=80&disable=upscale)

### 이정표와 고원:

모든 진행 시스템에서 보상의 속도는 매우 중요합니다. 작은 보상을 자주 제공하면 플레이어의 동기를 부여하고, 더 크고 중요한 마일스톤을 달성하면 큰 성취감을 느낄 수 있습니다. 그러나 진행 속도가 느린 기간, 즉 정체기 또한 중요한 역할을 할 수 있습니다. 이러한 상대적인 정체의 순간은 기대감을 조성하고 최종적인 돌파구를 더욱 만족스럽게 만듭니다. 게임 디자이너는 마일스톤과 의도적인 정체기를 적절히 배치한 진행 시스템을 설계함으로써 플레이어의 몰입도를 높이고 여정을 계속 이어나가고 싶어지게 만들 수 있습니다.

점진적 게임인유어 크로니클은 이 원칙을 잘 보여줍니다. 플레이어는 각 지역의 작은 던전을 진행하여 완료 시 소량의 콘텐츠를 잠금 해제할 수 있지만(마이너 마일스톤), 플레이어가 크리처의 힘을 키우는 데 집중하여 지역 보스를 물리치고 다음 지역의 콘텐츠를 잠금 해제하지 않으면 스토리 콘텐츠가 정체됩니다(메이저 마일스톤).

![](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt8d3b01bad47df6e3/66d87aa2c929b2484446ccc0/image.png?width=700&auto=webp&quality=80&disable=upscale)

### 커스터마이징 가능한 진행 경로:

플레이어의 몰입도를 높이는 가장 효과적인 방법 중 하나는 커스터마이징 가능한 진행 경로를 제공하는 것입니다. 스킬 트리, 분기 스토리라인, 개인화된 업그레이드 등 플레이어가 게임 진행 방식을 선택할 수 있게 하면 캐릭터 개발에 대한 주인의식과 투자 의식이 더욱 커집니다. 이러한 개인화는 게임 진행을 더욱 의미 있게 만들 뿐만 아니라 다양한 플레이 스타일을 충족시켜 다양한 플레이어가 자신만의 독특한 게임 여정에서 만족감을 찾을 수 있도록 합니다.

패스 오브엑자일의 스킬 트리는 플레이어가 어떤 캐릭터로 시작하느냐에 따라 다른 시작점에 배치되며, 플레이어는 스킬 포인트를 획득하면서 트리를 이동하며 원하는 대로 빌드를 커스터마이징할 수 있습니다.

![](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt5aaae2bb02e41c09/66d87ab242be9e85a0df9895/image.png?width=700&auto=webp&quality=80&disable=upscale)

## 3\. 감정적인 성장의 여정

### 초보자에서 마스터로:

플레이어는 능력과 지식이 부족한 초보자로 시작하여 점차 점점 더 복잡한 도전을 극복할 수 있는 전문가로 성장합니다. 이러한 진행 과정은 주인공이 시련과 고난을 겪으며 진화하는 많은 고전 동화와 유사합니다. 게임 디자이너는 이러한 성장의 속도를 신중하게 조절함으로써 플레이어와 캐릭터 사이에 깊은 감정적 유대감을 형성하여 승리할 때마다 숙달을 향한 힘겨운 발걸음처럼 느껴지도록 만들 수 있습니다. 시간이 지남에 따라 자신의 실력이 발전하는 것을 보는 만족감은 장기적인 몰입을 유도하는 핵심 동인입니다.

### 장애물 극복:

새로운 장애물과 좌절에 직면하면 플레이어는 기존에 사용하던 전략을 측정하고 비교하고 조정하여 새로운 전략을 개발할 수 있으며, 결국 학습과 승리로 이어집니다. 플레이어가 새로운 아이템이나 능력과 상호작용하도록 하면 게임에 대한 전반적인 이해와 숙련도가 높아집니다. 효과적인 장애물 디자인은 실험을 장려하고 플레이어의 성취감을 높여 어려움을 겪는 순간을 학습 포인트로 전환합니다.

![](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt5e0258aaea96c489/66d87ac12bad5e11c9d07b37/image.png?width=700&auto=webp&quality=80&disable=upscale)

제가 만든 게임 Deadbeat Wizard에서는 플레이어가 번개 주문을 사용하여 보호막을 쓴 적을 무력화해야 합니다.

### 엔드게임:

플레이어가 엔드게임에 가까워지면 기존의 파워 진행 속도가 느려지거나 정점에 도달하는 경우가 많습니다. 하지만 이 단계에서 플레이어의 참여를 유지하는 것이 중요합니다. 엔드게임에서는 고급 메커니즘 숙달, 게임 플레이어 커뮤니티 내 사회적 지위, 희귀하고 권위 있는 보상 추구와 같은 새로운 형태의 진행 방식이 도입될 수 있습니다. 디자이너는 성장에서 세련미로, 힘에서 명성으로 초점을 전환함으로써 플레이어의 여정에 만족스러운 결론을 내면서도 노력할 목표를 제시할 수 있습니다. 이러한 접근 방식은 주요 진행이 완료된 후에도 게임에 대한 감정적 투자가 계속되도록 보장합니다.

![](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltdfc56a57c5eb8c5e/66d87ad19ba222a4c7cb32c6/image.png?width=700&auto=webp&quality=80&disable=upscale)

![](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt2b0529443b8cf988/66d87af9edc972a68be714a3/image.png?width=700&auto=webp&quality=80&disable=upscale)

## 4\. 효과적인 파워 진행의 예

### 클래식 RPG:

발더스 게이트와 크로노 트리거와같은 RPG는 게임의 내러티브와 메커니즘에 파워 진행을 통합하는 방법을 보여주는 예시입니다. 발더스 게이트의 성장 시스템은 던전 앤 드래곤의 세계관과 깊이 연관되어 있으며, 플레이어는 레벨을 올리고 새로운 주문을 습득하고 전설적인 장비를 획득하면서 상당한 성장을 경험합니다. 크로노 트리거는 캐릭터가 강해지는 것뿐만 아니라 플레이어가 다양한 시대를 탐험하고 역사의 흐름을 바꿀 수 있는 새로운 능력을 잠금 해제하는 독특한 방식을 제공합니다. 이 두 RPG는 게임플레이와 스토리텔링을 모두 향상시키는 데 성장을 어떻게 활용할 수 있는지 보여주며, 각 이정표가 플레이어의 여정에서 의미 있는 단계처럼 느껴지도록 합니다.

![](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt389ab2008ea32f4b/66d87b05e4fe46ea756f0402/image.png?width=700&auto=webp&quality=80&disable=upscale)

![](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt4f4c2c9ba6d7f648/66d87b21ef93d56433eab72e/image.png?width=700&auto=webp&quality=80&disable=upscale)

발더스 게이트에서2레벨 치유 주문과 5레벨 치유 주문을 비교했을 때의 위력 증가 .

### 현대적인 혁신:

최신 게임은 기존 진행 시스템의 한계를 뛰어넘어 다양한 플레이어의 선호도를 충족하는 혁신을 도입했습니다. 예를 들어 적응형 난이도 시스템은 플레이어의 실력에 따라 게임의 난이도를 동적으로 조정하여 플레이어가 이상적인 '흐름' 상태를 유지할 수 있는 균형 잡힌 경험을 보장합니다. 반면, 로그라이트는 각 플레이가 이전 플레이를 기반으로 하여 학습과 개선의 사이클을 만들어내는 포스트-런 진행 방식을 사용하여 독특한 변주를 제공합니다. 이러한 혁신은 진행 시스템을 신선하고 매력적으로 유지하는 새로운 방법을 제공함으로써 현대 게임 디자인이 어떻게 계속 진화하고 있는지를 보여줍니다.

### 라이브 서비스 게임:

데스티니 가디언즈와 포트나이트와같은 라이브 서비스 게임은 시간이 지남에 따라 플레이어 경험을 새롭게 하는 시즌 콘텐츠를 도입하여 파워 진척도에 혁신을 일으켰습니다. 이러한 게임은 지속적인 업데이트, 새로운 목표, 시간 제한 보상을 통해 플레이어의 참여를 유도하여 정기적인 플레이를 장려합니다. 시즌 진행 시스템은 매 시즌마다 새로운 도전과 성장의 기회를 제공하고 새로운 기술을 익힐 수 있는 기회를 제공함으로써 새로움과 흥미를 선사합니다. 이러한 접근 방식은 플레이어의 장기적인 관심을 유지할 뿐만 아니라, 진행도가 끊임없이 재정의되는 역동적이고 끊임없이 진화하는 게임 세계를 만들어냅니다.

![](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt7d86bf0e31b718cf/66d87b45b95af75793e0ff37/image.png?width=700&auto=webp&quality=80&disable=upscale)

![](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt1defd7dd73703d61/66d87b4ec929b261bb46cccc/image.png?width=700&auto=webp&quality=80&disable=upscale)

![](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt019247afd90c6a25/66d87b58ef93d54a7eeab732/image.png?width=700&auto=webp&quality=80&disable=upscale)

포트나이트 시즌 4 배너는 해당 챕터에 추가된 새로운 기능과 장소를 보여줍니다.

## 5\. 파워 성장의 일반적인 함정 피하기

### 파워 크리프:

파워 크리프는 새로운 콘텐츠가 점차적으로 파워 상한을 높여 시간이 지남에 따라 오래된 능력, 장비, 전략의 효과가 떨어질 때 발생합니다. 이는 불균형과 좌절감으로 이어질 수 있으며, 플레이어는 경쟁력을 유지하기 위해 끊임없이 최신 메타를 쫓아야 한다는 강박감을 느낄 수 있습니다. 파워 크리프를 방지하기 위해 디자이너는 단순히 파워를 높이는 대신 새로운 콘텐츠가 다양한 플레이 스타일이나 능력을 제공하는 수평적 진행을 도입할 수 있습니다. 또한 시즌 초기화 또는 레벨 제한을 통해 오래된 콘텐츠의 관련성을 유지하고 모든 플레이어에게 공정하고 보람 있는 진행을 보장함으로써 균형을 유지할 수 있습니다.

### 단조로움:

파워 진행 시스템을 설계할 때의 위험 중 하나는 플레이어가 점진적인 이득을 얻기 위해 반복적인 작업을 수행하는 것처럼 느껴지는 단조로움에 빠지는 것입니다. 이는 곧 지루함과 몰입도 저하로 이어질 수 있습니다. 단조로움을 극복하려면 플레이어의 진행 방식에 다양성을 도입하는 것이 필수적입니다. 여기에는 여러 유형의 도전 과제를 제공하거나, 내러티브 중심의 진행 요소를 통합하거나, 비슷한 목표에 도달하기 위한 다양한 경로를 제공하는 것이 포함됩니다. 진행 경험을 역동적이고 다양하게 유지함으로써 디자이너는 플레이어의 흥미를 유지하고 여정의 각 단계가 신선하고 흥미진진하게 느껴지도록 만들 수 있습니다.

![](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blte4de01886b706e71/66d87b64e589004e410c26a2/image.png?width=700&auto=webp&quality=80&disable=upscale)

스킬 레벨 92는 룬스케이프에서 스킬 레벨 99에 도달하기 위한 경험치 측면에서 중간 지점입니다.

### 플레이어 피로도:

플레이어의 피로는 광범위한 능력치 성장 시스템을 갖춘 게임에서 흔히 발생하는 문제이며, 특히 플레이어가 지속적으로 성장해야 한다는 압박감을 느낄 때 더욱 심해집니다. 이는 플레이어의 피로와 게임의 즐거움 감소로 이어질 수 있습니다. 피로를 방지하려면 휴식과 다운타임을 허용하는 진행 시스템을 설계하는 것이 중요합니다. 일일 또는 주간 진행률 제한, 진행률과 무관한 활동 제공, 내러티브 일시 정지 등의 기능을 구현하면 플레이어가 뒤처진다는 느낌 없이 재충전할 수 있는 기회를 제공할 수 있습니다. 디자이너는 플레이어의 시간을 존중하고 균형 잡힌 진행 속도를 제공함으로써 플레이어의 장기적인 참여와 즐거움을 유지할 수 있습니다.

## 결론 매력적인 파워 진행 시스템 제작하기

도전과 보상 사이의 적절한 균형을 맞추는 것은 필수적입니다. 플레이어가 자신의 진행이 합당하고 영향력이 있다고 느낄 때, 게임에 대한 유대감이 깊어지고 각 마일스톤마다 성취감이 향상됩니다. 파워 크립이나 지나치게 느린 진행과 같은 실수를 방지하면 진행이 흥미롭고 보람 있게 유지되어 플레이어가 여정을 계속하도록 장려할 수 있습니다.

파워 진행의 혁신은 익숙한 시스템에 새로운 생명을 불어넣어 플레이어의 흥미를 유지하는 신선한 경험을 제공합니다. 디자이너는 고전적인 메커니즘을 재검토하든 완전히 새로운 메커니즘을 도입하든, 깊은 공감을 불러일으키는 진행 시스템을 만들어 매 단계가 의미 있고 매력적으로 느껴지도록 할 수 있습니다.

결국 성장 시스템은 단순히 플레이어의 능력을 향상시키는 수단이 아니라 게임의 감정과 내러티브의 깊이를 더하는 원동력입니다. 이 시스템은 플레이어를 성장의 여정으로 안내하며, 모든 도전 과제를 극복하고 습득한 모든 기술이 플레이어의 진화하는 실력을 증명하는 증거가 됩니다. 성장의 진정한 힘은 플레이어의 참여와 동기를 부여하고 여정에 감정적으로 투자하게 만드는 능력에 있습니다.

자세히 읽어보세요:

[블로그추천](https://www.gamedeveloper.com/keyword/blogs)[블로그톱](https://www.gamedeveloper.com/keyword/featured-blogs)[스토리](https://www.gamedeveloper.com/keyword/top-stories)

[](https://www.linkedin.com/sharing/share-offsite/?url=https://www.gamedeveloper.com/design/power-progression-in-games-crafting-rewarding-player-experiences)[](https://www.facebook.com/sharer/sharer.php?u=https://www.gamedeveloper.com/design/power-progression-in-games-crafting-rewarding-player-experiences)[](https://www.twitter.com/intent/tweet?url=https://www.gamedeveloper.com/design/power-progression-in-games-crafting-rewarding-player-experiences)[](https://www.gamedeveloper.com/cdn-cgi/l/email-protection#f6c98583949c939582cba699819384d686849991849385859f9998d69f98d691979b9385ccd6b5849790829f9891d68493819784929f9891d6869a978f9384d6938e8693849f9398959385d0979b86cd9499928fcbbfd3c4c6829e9983919e82d3c4c6829e93d3c4c690999a9a99819f9891d3c4c69084999bd3c4c6b1979b93d3c4c6b29380939a99869384d3c4c69b9f919e82d3c4c69f98829384938582d3c4c68f9983d8d3c6b2d3c6b7d3c6b2d3c6b7d3c4c6a699819384d3c4c686849991849385859f9998d3c4c69f98d3c4c691979b9385d3c5b7d3c4c6b5849790829f9891d3c4c68493819784929f9891d3c4c6869a978f9384d3c4c6938e8693849f9398959385d3c6b2d3c6b79e82828685d3c5b7d3c4b0d3c4b0818181d891979b93929380939a99869384d895999bd3c4b09293859f9198d3c4b08699819384db86849991849385859f9998db9f98db91979b9385db95849790829f9891db8493819784929f9891db869a978f9384db938e8693849f9398959385)[](https://www.reddit.com/submit?url=https://www.gamedeveloper.com/design/power-progression-in-games-crafting-rewarding-player-experiences&title=Power%20progression%20in%20games%3A%20Crafting%20rewarding%20player%20experiences)

## 저자 소개

[![Cameron McKellar](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltd709c2f6ad0896cd/657b3aae1fb1b4040a0e1821/Game_Developer_G_Logo_RGB.png?width=400&auto=webp&quality=80&disable=upscale "Cameron McKellar")](https://www.gamedeveloper.com/author/cameron-mckellar)

[

카메론 맥켈러

](https://www.gamedeveloper.com/author/cameron-mckellar)

[카메론 맥켈러(Cameron McKellar) 더보기](https://www.gamedeveloper.com/author/cameron-mckellar)

게임 개발자의 일일 뉴스, 개발자 블로그, 이야기를 받은 편지함으로 바로 받아보세요.

[최신 소식 받기](https://gd-resources.gamedeveloper.com/free/w_gamf01/prgm.cgi)

추천 콘텐츠

* * *

원문: [https://www.gamedeveloper.com/design/power-progression-in-games-crafting-rewarding-player-experiences](https://www.gamedeveloper.com/design/power-progression-in-games-crafting-rewarding-player-experiences)