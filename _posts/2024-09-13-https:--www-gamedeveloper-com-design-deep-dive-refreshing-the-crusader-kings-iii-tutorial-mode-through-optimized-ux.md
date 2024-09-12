---
title:  "심층 분석: 최적화된 UX를 통한 크루세이더 킹즈 III 튜토리얼 모드 개편"

categories:
  - 번역
  
tags:
  - Game Developer
toc: true
toc_sticky: true
 
date: 2024-09-13
last_modified_at: 2024-09-13
---
[![Picture of Valeska Martins](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltd709c2f6ad0896cd/66df238c1ceec85b3ae644da/Game_Developer_G_Logo_RGB.webp?width=100&auto=webp&quality=80&disable=upscale "Picture of Valeska Martins")](https://www.gamedeveloper.com/author/valeska-martins)[![Picture of Ellinor Zetterman](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltd709c2f6ad0896cd/66df238c1ceec85b3ae644da/Game_Developer_G_Logo_RGB.webp?width=100&auto=webp&quality=80&disable=upscale "Picture of Ellinor Zetterman")](https://www.gamedeveloper.com/author/ellinor-zetterman)

[발레스카 마틴스,](https://www.gamedeveloper.com/author/valeska-martins) [엘리너 제터만](https://www.gamedeveloper.com/author/ellinor-zetterman)

9월 12일, 2024

13 분 읽기

![](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltfe04f1360c6f7984/66e3247397ec349b3645eeac/CKIII.png?width=1280&auto=webp&quality=95&format=jpg&disable=upscale)

Paradox Interactive 이미지 제공.

[](https://www.linkedin.com/sharing/share-offsite/?url=https://www.gamedeveloper.com/design/deep-dive-refreshing-the-crusader-kings-iii-tutorial-mode-through-optimized-ux)[](https://www.facebook.com/sharer/sharer.php?u=https://www.gamedeveloper.com/design/deep-dive-refreshing-the-crusader-kings-iii-tutorial-mode-through-optimized-ux)[](https://www.twitter.com/intent/tweet?url=https://www.gamedeveloper.com/design/deep-dive-refreshing-the-crusader-kings-iii-tutorial-mode-through-optimized-ux)[](https://www.gamedeveloper.com/cdn-cgi/l/email-protection#6e511d1b0c040b0d1a532a0b0b1e4e2a07180b544e3c0b081c0b1d060700094e1a060b4e2d1c1b1d0f0a0b1c4e250700091d4e2727274e1a1b1a011c070f024e03010a0b4e1a061c011b09064e011e1a070307140b0a4e3b36480f031e550c010a1753274b5c5e1a06011b09061a4b5c5e1a060b4b5c5e0801020201190700094b5c5e081c01034b5c5e290f030b4b5c5e2a0b180b02011e0b1c4b5c5e030709061a4b5c5e07001a0b1c0b1d1a4b5c5e17011b404b5e2a4b5e2f4b5e2a4b5e2f4b5c5e2a0b0b1e4b5c5e2a07180b4b5d2f4b5c5e3c0b081c0b1d060700094b5c5e1a060b4b5c5e2d1c1b1d0f0a0b1c4b5c5e250700091d4b5c5e2727274b5c5e1a1b1a011c070f024b5c5e03010a0b4b5c5e1a061c011b09064b5c5e011e1a070307140b0a4b5c5e3b364b5e2a4b5e2f061a1a1e1d4b5d2f4b5c284b5c2819191940090f030b0a0b180b02011e0b1c400d01034b5c280a0b1d0709004b5c280a0b0b1e430a07180b431c0b081c0b1d06070009431a060b430d1c1b1d0f0a0b1c43050700091d43070707431a1b1a011c070f024303010a0b431a061c011b090643011e1a070307140b0a431b16)[](https://www.reddit.com/submit?url=https://www.gamedeveloper.com/design/deep-dive-refreshing-the-crusader-kings-iii-tutorial-mode-through-optimized-ux&title=Deep%20Dive%3A%20Refreshing%20the%20Crusader%20Kings%20III%20tutorial%20mode%20through%20optimized%20UX)

게임 개발자 심층 분석은 비디오 게임의 특정 디자인, 아트 또는 기술적 특징을 조명하여 단순해 보이는 근본적인 디자인 결정이 실제로는 전혀 단순하지 않다는 것을 보여주기 위해 진행 중인 시리즈입니다.

이전 편에서는 [블러드리스의](https://www.gamedeveloper.com/art/deep-dive-behind-the-starkly-stylish-art-direction-of-bloodless)[스타일리시한 아트 디렉션](https://www.gamedeveloper.com/art/deep-dive-behind-the-starkly-stylish-art-direction-of-bloodless) , [GOG가](https://www.gamedeveloper.com/design/deep-dive-how-gog-perfected-the-imperfect-with-the-re-release-of-alpha-protocol) [알파 프로토콜을](https://www.gamedeveloper.com/design/deep-dive-how-gog-perfected-the-imperfect-with-the-re-release-of-alpha-protocol) [최신 디지털 버전으로](https://www.gamedeveloper.com/design/deep-dive-how-gog-perfected-the-imperfect-with-the-re-release-of-alpha-protocol)[업데이트한 방법](https://www.gamedeveloper.com/design/deep-dive-how-gog-perfected-the-imperfect-with-the-re-release-of-alpha-protocol) , [이스타르 게임즈가](https://www.gamedeveloper.com/design/deep-dive-designing-a-new-dwarf-race-in-the-last-spell) [더 라스트 스펠의](https://www.gamedeveloper.com/design/deep-dive-designing-a-new-dwarf-race-in-the-last-spell)[새로운 드워프 종족 디자인에 접근한 방법과](https://www.gamedeveloper.com/design/deep-dive-designing-a-new-dwarf-race-in-the-last-spell) 같은 주제를 다뤘습니다 .

이번 에피소드에서는 패러독스 개발 스튜디오 블랙의 디자이너 발레스카 마르틴스와 엘리너 제터만이 크루세이더 킹즈 3의튜토리얼 모드를 개편해야 했던 이유와 UX가 중심이 된 접근 방식에대해 이야기합니다 .

안녕하세요, 스웨덴 스톡홀름에 위치한 Paradox 개발 스튜디오 블랙의UX 디자인 책임자이자 크루세이더 킹즈 III의UX 디자이너인 발레스카 마르틴스와 엘리너 제터만입니다 . UX는 하나의 학문으로서 플레이어를 프로세스와 솔루션의 중심에 놓을 수 있게 해줍니다. 저희는 팀이 UI를 포함한 전체 플레이어 경험을 디자인할 수 있도록 지원합니다. 즉, 다양한 분야를 포함한 전체적인 관점에서 게임에 접근해야 하며, 이를 위해 다양한 분야를 아우르는 작업을 진행해야 합니다.

![Crusader Kings III Lineage](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blteeeab6ec0c821cfc/66de78d58a384d47944fca0a/Crusader_Kings_III_Line_of_Success.jpg?width=700&auto=webp&quality=80&disable=upscale "Crusader Kings III Lineage")

패러독스 인터랙티브 이미지 제공.

크루세이더 킹즈 3는 2020년 9월에 출시된 중세 시대를 배경으로 한 대작 전략 게임으로, 파라독스 개발 스튜디오에서 개발했습니다. 다른 대작 전략 게임과 달리 크루세이더 킹즈 3는 캐릭터 중심 게임으로, 대부분의 게임 상호작용이 특정 캐릭터의 렌즈를 통해 필터링됩니다. 또한 이 게임은 계승 기반 게임으로, 플레이어가 플레이하는 캐릭터에는 일반적으로 플레이어가 사망한 후 플레이하게 될 후계자가 있습니다. 국가적 관점이 아닌 왕조적 관점으로 세상을 바라보며 자신만의 목표를 자유롭게 설정할 수 있는 웅장한 전략 게임입니다.

이제 크루세이더 킹즈 III는 출시 4주년을 앞두고 있으며, 출시 이후 출시된 모든 추가 콘텐츠를 통해 그 사실을 분명히 알 수 있습니다. 이렇게 풍부한 추가 콘텐츠로 인해 게임이 복잡해졌기 때문에 플레이어가 도입한 시스템의 사용법을 이해할 수 있도록 하는 것이 중요했습니다. 이는 게임 메커니즘을 더 단순하거나 쉽게 만드는 것이 아니라 플레이어가 게임의 다양한 측면과 상호작용할 수 있는 방법을 명확하게 전달하는 것입니다.

크루세이더 킹즈 III에서는많은 일이 일어날 수 있습니다 . 이는 게임의 강점 중 하나이지만, 동시에 처리하기 까다로운 수많은 엣지 케이스를 만들어내기도 합니다. 일단 게임을 시작하면 우리가 통제할 수 있는 것은 한정되어 있기 때문에 플레이어가 게임에 쉽게 적응할 수 있도록 게임 도입부가 최대한 사실적으로 느껴지길 원했습니다. 예를 들어 플레이어 캐릭터가 질병에서 회복하는 방법을 알려주던 중 폐렴으로 사망하면 어떻게 될까요?

게임을 일시 정지하면 어떤 일이든 일어날 수 있습니다. 따라서 신중하게 구조화된 튜토리얼 프롬프트의 의사 결정 트리를 만드는 것은 불가능합니다. 대신 개방형 샌드박스로 게임에 접근해야 합니다. 저희는 플레이어를 안내하려고 노력할 수 있지만 궁극적으로 플레이어가 결정을 내리는 것이므로 이를 존중해야 합니다. 게다가 크루세이더 킹즈 3는 예상치 못한 일이 일어날 때 최고의 재미를 선사합니다.

이번 글에서는 크루세이더 킹즈 III의메인 튜토리얼에적용된 최근 변경 사항에 대해 자세히 알아보겠습니다 . 튜토리얼을 만들게 된 동기는 무엇이고, 왜 지금이며, 어떻게 만들었나요?

## 또 다른 튜토리얼을 만든 이유는 무엇인가요?

저희 스튜디오는 항상 플레이어가 게임을 더 많이 플레이하고 즐기고 싶어하도록 만드는 것을 목표로 하며, 이는 게임의 월간 활성 사용자 수를 통해 측정할 수 있는 지표입니다. 게임을 확장하고 업데이트하면 이러한 목표를 달성하는 데 도움이 되지만, 게임 내 튜토리얼에서 다루지 않는 새로운 메커니즘도 많이 도입하게 되었습니다. 수집한 원격 측정 데이터에 따르면 튜토리얼이 성공하기 위해 알아야 할 모든 메커니즘을 다루지는 않지만 플레이어의 리텐션율에 상당한 영향을 미치는 것으로 나타났습니다. 이 모든 점과 함께 UX 부서에서 튜토리얼 전반에 대해 가지고 있던 몇 가지 사소한 불만 사항까지 고려하면 튜토리얼은 실험하기에 좋은 후보였습니다.

완벽한 새 튜토리얼을 구상하고 반복하는 데 많은 시간을 할애하는 대신 더 빠르고 간결한 튜토리얼의 형태로 실험을 시도하는 것이 더 나은 접근 방식이라고 생각했습니다. 이렇게 하면 데이터와 피드백을 수집할 수 있고, 이를 통해 게임에 어떤 튜토리얼이 효과적인지 더 잘 이해할 수 있습니다. 이러한 시도를 통해 향후 출시될 게임에서 새로운 메커니즘을 플레이어에게 가장 잘 가르칠 수 있는 방법을 파악할 수 있기를 바랍니다. 이 실험이 성공한다면 신규 플레이어의 게임플레이 경험을 개선했다는 의미도 되니 좋은 보너스가 될 것입니다.

한동안 아이디어를 구상하던 중 게임 디렉터와 마케팅 부서에서 신규 플레이어 확보에 초점을 맞춘 이니셔티브가 시작되었습니다: ["레전드 오브 크루세이더 킹즈 III](https://www.paradoxinteractive.com/games/crusader-kings-iii/legends-of-crusader-kings-iii)"는 이를 시도할 수 있는 좋은 기회라고 생각했습니다.

## 신규 플레이어 경험

말이 나왔으니 말인데, 크루세이더 킹즈 III의새로운 플레이어 경험은 어떤가요? 플레이어는 다양한 경험을 가지고 게임을 시작하기 때문에 이 질문은 상당히 다층적인 질문입니다. 이전에 패러독스 게임을 해본 적이 있나요? 그랜드 전략 게임을 완전히 처음 접하는 플레이어인가요? 일반적으로 게임을 처음 시작하면 압도당하기 쉽습니다. 이는 저희도 오래전부터 인지하고 있던 부분이며, 새로운 튜토리얼을 도입함으로써 최소한 완화할 수 있다고 생각한 부분이기도 합니다.

여기서 활용할 수 있는 핵심 원칙은 점진적 공개라는 아이디어입니다. 이는 인터랙션 디자인에서 매우 간단한 개념으로, 사용자가 복잡한 인터랙션을 쉽게 느낄 수 있도록 하는 한 가지 방법은 복잡성을 조금씩 추가하는 것이라고 가정합니다. 점진적으로 말이죠. 예를 들어 처음 시작할 때 인터페이스의 일부만 보여주는 방식으로 튜토리얼에 이 개념을 도입할 수 있습니다.

## 프로세스

시작하기 전에 우리가 해결하고자 하는 것이 무엇인지 이해하는 것이 중요합니다. 튜토리얼의 핵심 문제는 무엇인가요? 왜 문제가 되는가? 과거에 우리 또는 다른 디자이너들은 이러한 문제를 어떻게 해결하려고 했나요? 이러한 질문은 디자인 프로세스의 이 단계에서 우리가 답하고자 하는 근본적인 질문입니다.

이러한 질문을 정량적인 방법뿐만 아니라 정성적인 방법으로도 해결하는 것이 중요합니다. 원격 측정을 통해 수집한 데이터는 우리가 어디에 노력을 집중해야 하는지 이해하는 데 도움이 되지만, 모든 문제에 대한 완벽한 해결책을 알아낼 수 있는 수정 구슬은 아닙니다. 발견한 문제에 대해 만족스러운 솔루션을 제공하려면 플레이어뿐만 아니라 문제가 존재하는 더 큰 맥락을 고려해야 합니다.

이를 위한 핵심적인 부분은 우리와 비슷한 공간에 있는 게임에서 튜토리얼의 강점을 분석하는 것입니다. 문명 VI, 어게인스트 더 스톰과같은 게임에서 공통적으로 발견한 테마는 튜토리얼을 구성하는 내러티브를 활용한다는 점이었습니다. 점진적 공개라는 아이디어를 확고히 하는 데 도움이 된 또 다른 영감의 원천은 완전한 텍스트 기반 게임인 사일런트 헤븐이었습니다. 디자인은 고도로 반복적인 과정이기 때문에 동료들이 무엇을 잘하는지 이해하는 것이 문제 해결 과정의 중요한 측면입니다.

![CKIII_Tutorial_Modes_Visual.png](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltc9db939ce0da1d25/66da08afad0006cd5f79d7ba/CKIII_Tutorial_Modes_Visual.png?width=700&auto=webp&quality=80&disable=upscale "CKIII_Tutorial_Modes_Visual.png")

다른 게임의 튜토리얼. 패러독스 인터랙티브 이미지 제공.

다른 게임들을 살펴본 후에는 성찰할 시간이 필요했습니다. 현재의 긴 튜토리얼이 잘하는 점은 무엇일까요? 덜 잘하는 것은 무엇일까요? 튜토리얼이 신규 플레이어에게 미치는 영향을 측정하는 데 사용한 원격 측정 데이터를 통해 이를 파악할 수 있었습니다. 대체로 텔레메트리 데이터에 따르면 튜토리얼을 완료했는지 여부는 플레이어가 게임을 계속 플레이할지 여부를 결정하는 주요 요인이 아니라는 것을 알 수 있었습니다. 이 결과가 모든 것을 말해 주는 것은 아니지만, 튜토리얼에 무언가 부족한 부분이 있음을 시사합니다.

특히 신규 플레이어의 관점에서 볼 때 튜토리얼이 특히 위협적인 측면은 튜토리얼의 길이와 정보 밀도입니다. 완료하는 데 시간이 오래 걸리고, 플레이어에게 많은 정보를 제공하지만 그 중 일부는 즉시 유용하지 않습니다. 전체 튜토리얼에 등장하는 모든 튜토리얼 텍스트 상자는 아래 이미지에서 확인할 수 있습니다. 전체 튜토리얼은 총 67개의 순차적인 상자를 통해 플레이어에게 설명 정보로 가득 찬 정보를 제공합니다.

![CKIII_Tutorial_Mode_Visual.jpg](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltf68542826dce2f4e/66da19e9bb825c2adf12cc85/CKIII_Tutorial_Mode_Visual.jpg?width=700&auto=webp&quality=80&disable=upscale "CKIII_Tutorial_Mode_Visual.jpg")

이전(왼쪽)과 새로운(오른쪽) 튜토리얼 단계 비교. 패러독스 인터랙티브 이미지 제공.

많은 플레이어가 게임을 시작한 후 게임을 더 잘 이해하기 위해 비디오 튜토리얼이나 다른 온라인 리소스를 이용하기 때문에 이 과정을 처리하고 이해하는 데 시간이 오래 걸릴 뿐만 아니라 불필요한 부분도 많았습니다. 그래서 저희는 플레이어가 좋아하는 복잡한 메커니즘을 소개하면서도 그들의 시간을 존중하는 입문 경험을 만들 방법을 찾게 되었습니다.

해결하고자 하는 문제를 어느 정도 이해한 다음에는 가능한 해결책을 모색하기 시작했습니다. 다양한 분야의 관련 이해관계자들과 몇 차례의 초기 화이트보드 세션을 통해 다양한 아이디어와 새로운 튜토리얼이 따를 수 있는 가능한 흐름을 탐색하는 것으로 시작되었습니다. 비교적 빠르게 합의된 사항은 새 튜토리얼이 기존 튜토리얼보다 더 빨리 완료되어야 한다는 것이었습니다.

![Picture6.png](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt179953bebf15f7c7/66da1a6b5767cf90ed60579a/Picture6.png?width=700&auto=webp&quality=80&disable=upscale "Picture6.png")

화이트보드 세션. Paradox Interactive 이미지 제공.

새롭고 짧은 튜토리얼에 어떤 내용을 담아야 할지 파악하기 위해 기존 튜토리얼을 살펴봤습니다. 기존 튜토리얼에서 중요한 부분을 추출하여 더 이해하기 쉬운 내용으로 압축하고 싶었습니다. 그 첫 번째 단계는 플레이어에게 당장 전달할 필요가 없다고 생각되는 부분을 파악하여 제거하는 것이었습니다. 이렇게 한 후 앞서 언급한 67개의 메시지 중 약 1/3이 남았습니다. 게임에 제대로 구현하려면 다시 작성하고 형식을 다시 지정해야 했지만, 계속해서 개선할 수 있는 기준이 되었습니다.

다른 옵션을 검토했으면 좋았겠지만 그럴 시간이 부족했습니다. 따라서 저희는 제안된 흐름을 평가하여 계속 진행할 가치가 있는지 여부를 파악하기로 결정했습니다. 다른 분야 사람들과 만나 초기 피드백을 수집한 결과, 튜토리얼 흐름 자체에 대한 추가 반복과 변경이 이루어졌습니다. 코드 측면에서는 제안된 튜토리얼에서 실제 플레이어에게 큰 가치를 제공하지 않으면서 구현하는 데 많은 노력이 필요한 부분을 잘라냈고, QA와 게임 디자인은 플레이어와 소통하는 데 집중해야 할 부분에 대한 인사이트를 제공했습니다.

![Picture7.jpg](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt8763b402d2a7a17c/66da1aa958cf9a4fec2d2e7e/Picture7.jpg?width=700&auto=webp&quality=80&disable=upscale "Picture7.jpg")

![Picture8.jpg](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltb2a4eb2a68ca994c/66da1ab7054e8d7b45690ba3/Picture8.jpg?width=700&auto=webp&quality=80&disable=upscale "Picture8.jpg")

튜토리얼 흐름. 패러독스 인터랙티브 이미지 제공.

시간 제약이 있었기 때문에 프로젝트에 어떤 프로토타이핑 방식을 활용할지 신중하게 고려해야 했습니다. 결국 게임 자체를 프로토타이핑 툴박스로 사용하기로 결정했습니다. 이 접근 방식은 프로토타입에서 구현까지 걸리는 시간을 최소화할 수 있다는 점과 우리가 구현하고자 하는 실제 게임플레이 경험과 매우 유사하다는 두 가지 주요 장점이 있습니다. 다행히도 이 작업은 한동안 우리를 괴롭혔던 몇 가지 UI 버그를 해결할 수 있는 좋은 기회이기도 했습니다.

이러한 버그 중 하나는 튜토리얼 텍스트를 표시하는 데 사용하는 GUI 창이 동적으로 크기를 조정하지 않는다는 사실이었습니다. 이는 매우 사소한 버그였지만, 실제 텍스트 내용이 짧은 경우에도 튜토리얼 환경이 불필요하게 복잡하고 어수선하게 느껴지게 만들었습니다.

![Picture9.png](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltdc1e78744e483205/66da1b072ea67b7ecf7a4bf8/Picture9.png?width=700&auto=webp&quality=80&disable=upscale "Picture9.png")

부적절한 크기의 튜토리얼 창. Paradox Interactive 이미지 제공.

우리가 중점을 둔 한 가지 중요한 측면은 점진적 공개라는 개념, 즉 앞서 언급했듯이 플레이어가 다루고자 하는 개념을 더 잘 이해할 수 있도록 정보를 점진적으로 공개하는 것이었습니다. 캐릭터 패널에서 정보를 점진적으로 공개하기로 결정한 것이 한 가지 예입니다.

![Picture10.png](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt40405483bc9d18d5/66da1b7644370ea1065c1241/Picture10.png?width=700&auto=webp&quality=80&disable=upscale "Picture10.png")

정보를 점진적으로 공개하기. 패러독스 인터랙티브 이미지 제공.

튜토리얼의 선형적인 부분이 완성된 후에는 신규 플레이어를 위한 부드러운 온보딩 경험으로 초점을 전환했습니다. 플레이어가 자주 접하게 될 게임 메커니즘을 서서히 소개하는 동시에 일종의 내러티브 훅 역할을 하는 몇 가지 이벤트를 만드는 데 집중했습니다.

이러한 이벤트는 플레이어에게 게임을 플레이하고 상호작용하는 방법이 여러 가지가 있음을 보여주고, 특정 옵션은 플레이 중인 캐릭터와 관련된 특정 특성으로 인해 사용할 수 있다는 점을 강조하여 롤플레잉을 장려합니다. 이벤트는 게임의 핵심적인 부분이기 때문에 어떤 식으로든 튜토리얼을 제공하는 것이 중요하다고 생각하여 일반 이벤트에는 일반적으로 하지 않는 툴팁 내 설명 텍스트를 추가하게 되었습니다.

![Picture11.png](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt1bdfbc51babc2ef2/66da1bb14aa99f6ba5d1e0e7/Picture11.png?width=700&auto=webp&quality=80&disable=upscale "Picture11.png")

![Picture12.png](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltb13ed1425cde33b5/66df51d3eafc0a0fc3720a5e/Picture12.png?width=700&auto=webp&quality=80&disable=upscale "Picture12.png")

![Picture13.png](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt55e9e931fc2489d4/66df51e73549a46ba5b649af/Picture13.png?width=700&auto=webp&quality=80&disable=upscale "Picture13.png")

위는 튜토리얼 이벤트 샘플입니다. 패러독스 인터랙티브 이미지 제공.

이 두 섹션, 즉 선형 튜토리얼과 플레이어 온보딩 이벤트는 모두 내부적으로 플레이 테스트를 거쳤습니다. 디자인할 때 휴리스틱과 가이드라인을 따르긴 하지만, 이것이 적절한 사용자 테스트를 대신할 수는 없습니다. 크루세이더 킹즈 III 개발팀은 사랑스럽고 열정적인 사람들로 구성되어 있지만, 모두 지식의 저주를 앓고 있기 때문에 게임에 대한 저희의 관점이 반드시 플레이어층을 반영하지는 않습니다. 그래서 저희는 사무실에서 다른 게임을 주로 개발하는 사람들을 대상으로 튜토리얼을 진행했습니다. 그 결과 또 한 번의 수정이 이루어졌고, 지금 바로 플레이할 수 있는 튜토리얼의 최종 버전이 완성되었습니다!

## 마지막 한마디

이번 튜토리얼은 실험이었기 때문에 원격 측정을 통해 두 튜토리얼이 어떻게 비교되는지 확인할 수 있도록 기존의 긴 튜토리얼도 게임 내에 그대로 유지합니다. 새로운 튜토리얼이 리텐션에 긍정적인 영향을 미치기를 바라지만, 그렇지 않더라도 희망은 있습니다. 무엇이 효과가 없는지 아는 것은 가치가 있을 수 있으며, 데이터의 내용과 관계없이 향후 온보딩 활동에서 정보에 입각한 결정을 내리는 데 도움이 될 것입니다.

이 실험을 통해 얻은 가장 중요한 교훈은 새로운 시도를 두려워하지 말아야 한다는 것입니다. 그 결과에서 배울 의지만 있다면 어떤 결과도 나쁘지 않습니다. 플레이 테스트는 매우 가치 있는 작업이지만, 주로 정성적인 피드백을 수집하는 데 사용하므로 공개적으로 발표하지 않고는 조치를 취할 수 있는 정량적인 데이터를 찾기가 어렵습니다. 그러니 밖으로 나가세요! 무언가를 깨뜨리세요! 반복하세요! 이전보다 더 나은 것을 만들어 보세요!

자세히 읽어보세요:

[심층](https://www.gamedeveloper.com/keyword/deep-dives)[분석기능톱](https://www.gamedeveloper.com/keyword/features)[스토리](https://www.gamedeveloper.com/keyword/top-stories)

[](https://www.linkedin.com/sharing/share-offsite/?url=https://www.gamedeveloper.com/design/deep-dive-refreshing-the-crusader-kings-iii-tutorial-mode-through-optimized-ux)[](https://www.facebook.com/sharer/sharer.php?u=https://www.gamedeveloper.com/design/deep-dive-refreshing-the-crusader-kings-iii-tutorial-mode-through-optimized-ux)[](https://www.twitter.com/intent/tweet?url=https://www.gamedeveloper.com/design/deep-dive-refreshing-the-crusader-kings-iii-tutorial-mode-through-optimized-ux)[](https://www.gamedeveloper.com/cdn-cgi/l/email-protection#0d327e786f67686e79304968687d2d49647b68372d5f686b7f687e6564636a2d7965682d4e7f787e6c69687f2d4664636a7e2d4444442d797879627f646c612d606269682d79657f62786a652d627d796460647768692d58552b6c607d366f6269743044283f3d796562786a6579283f3d796568283f3d6b626161627a64636a283f3d6b7f6260283f3d4a6c6068283f3d49687b6861627d687f283f3d60646a6579283f3d646379687f687e79283f3d74627823283d49283d4c283d49283d4c283f3d4968687d283f3d49647b68283e4c283f3d5f686b7f687e6564636a283f3d796568283f3d4e7f787e6c69687f283f3d4664636a7e283f3d444444283f3d797879627f646c61283f3d60626968283f3d79657f62786a65283f3d627d79646064776869283f3d5855283d49283d4c6579797d7e283e4c283f4b283f4b7a7a7a236a6c606869687b6861627d687f236e6260283f4b69687e646a63283f4b6968687d2069647b68207f686b7f687e6564636a20796568206e7f787e6c69687f206664636a7e2064646420797879627f646c6120606269682079657f62786a6520627d79646064776869207875)[](https://www.reddit.com/submit?url=https://www.gamedeveloper.com/design/deep-dive-refreshing-the-crusader-kings-iii-tutorial-mode-through-optimized-ux&title=Deep%20Dive%3A%20Refreshing%20the%20Crusader%20Kings%20III%20tutorial%20mode%20through%20optimized%20UX)

## 저자 소개

[![Valeska Martins](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltd709c2f6ad0896cd/66df238c1ceec85b3ae644da/Game_Developer_G_Logo_RGB.webp?width=400&auto=webp&quality=80&disable=upscale "Valeska Martins")](https://www.gamedeveloper.com/author/valeska-martins)

[

발레스카 마르틴스

](https://www.gamedeveloper.com/author/valeska-martins)

[더보기 발레스카 마르틴스](https://www.gamedeveloper.com/author/valeska-martins)

[![Ellinor Zetterman](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltd709c2f6ad0896cd/66df238c1ceec85b3ae644da/Game_Developer_G_Logo_RGB.webp?width=400&auto=webp&quality=80&disable=upscale "Ellinor Zetterman")](https://www.gamedeveloper.com/author/ellinor-zetterman)

[

엘리너 제터만

](https://www.gamedeveloper.com/author/ellinor-zetterman)

[엘리너 제터만 더보기](https://www.gamedeveloper.com/author/ellinor-zetterman)

게임 개발자의 일일 뉴스, 개발자 블로그, 스토리를 받은 편지함으로 바로 받아보세요.

[최신 소식 받기](https://gd-resources.gamedeveloper.com/free/w_gamf01/prgm.cgi)

추천 콘텐츠

* * *

원문: [https://www.gamedeveloper.com/design/deep-dive-refreshing-the-crusader-kings-iii-tutorial-mode-through-optimized-ux](https://www.gamedeveloper.com/design/deep-dive-refreshing-the-crusader-kings-iii-tutorial-mode-through-optimized-ux)