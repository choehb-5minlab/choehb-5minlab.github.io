---
title:  "'엿먹고 알아내기'가 아르코 전투의 중추가 된 이유"

categories:
  - 번역
  
tags:
  - Game Developer
toc: true
toc_sticky: true
 
date: 2024-08-15
last_modified_at: 2024-08-15
---
[![Picture of Chris Kerr](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt1c7a117d71555292/650efbcad3423169a8871059/chris_kerr_headshot.jpg?width=100&auto=webp&quality=80&disable=upscale "Picture of Chris Kerr")](https://www.gamedeveloper.com/author/chris-kerr)

[크리스 커](https://www.gamedeveloper.com/author/chris-kerr), 뉴스 에디터

8월 15일, 2024

5분 읽기

![A combat encounter playing out in Arco](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltc634ab4a4f7b1aba/66bce202298cece62f6f006f/Arco_Header.png?width=1280&auto=webp&quality=95&format=jpg&disable=upscale "A combat encounter playing out in Arco")

Panic 이미지 제공

[](https://www.linkedin.com/sharing/share-offsite/?url=https://www.gamedeveloper.com/design/why-fuck-around-and-find-out-became-the-backbone-of-arco-s-combat)[](https://www.facebook.com/sharer/sharer.php?u=https://www.gamedeveloper.com/design/why-fuck-around-and-find-out-became-the-backbone-of-arco-s-combat)[](https://www.twitter.com/intent/tweet?url=https://www.gamedeveloper.com/design/why-fuck-around-and-find-out-became-the-backbone-of-arco-s-combat)[](https://www.gamedeveloper.com/cdn-cgi/l/email-protection#e0df9395828a858394ddb78899c0c6c398d2d7db8695838bc081928f958e84c0818e84c086898e84c08f9594c6c398d2d7dbc0828583818d85c0948885c08281838b828f8e85c08f86c0a192838fc6c398d2d7db93c0838f8d828194c6818d90db828f8499dda9c5d2d094888f95878894c5d2d0948885c5d2d0868f8c8c8f97898e87c5d2d086928f8dc5d2d0a7818d85c5d2d0a48596858c8f908592c5d2d08d89878894c5d2d0898e948592859394c5d2d0998f95cec5d0a4c5d0a1c5d0a4c5d0a1c5d2d0b78899c5d2d0c6c398d2d7db8695838bc5d2d081928f958e84c5d2d0818e84c5d2d086898e84c5d2d08f9594c6c398d2d7dbc5d2d0828583818d85c5d2d0948885c5d2d08281838b828f8e85c5d2d08f86c5d2d0a192838fc6c398d2d7db93c5d2d0838f8d828194c5d0a4c5d0a18894949093c5d3a1c5d2a6c5d2a6979797ce87818d85848596858c8f908592ce838f8dc5d2a684859389878ec5d2a6978899cd8695838bcd81928f958e84cd818e84cd86898e84cd8f9594cd828583818d85cd948885cd8281838b828f8e85cd8f86cd8192838fcd93cd838f8d828194)[](https://www.reddit.com/submit?url=https://www.gamedeveloper.com/design/why-fuck-around-and-find-out-became-the-backbone-of-arco-s-combat&title=Why%20'fuck%20around%20and%20find%20out'%20became%20the%20backbone%20of%20Arco's%20combat)

잠깐만요, 여기요. 거침없는 난장판과 사랑스러운 2차원 라마에 대한 열정을 가진 건방진 타입을 알고 계신가요? 그럼 좋아요. [아르코를](https://store.steampowered.com/app/2366970/Arco/)[한 번 구경해](https://store.steampowered.com/app/2366970/Arco/) 보라고 전해주세요 .

퍼블리셔 Panic과 개발팀 Franek Nowotniak, Max Cahill, Jose Ramon Garcia, Antonio Uribe의 새로운 전술 액션 게임이 오늘 출시되었으며, 모든 징후가 이 게임이 대단한 게임이 될 것임을 암시합니다.

이 영화는 마법과 유혈로 점철된 모험의 결과를 결정지을 수 있는 거대한 복수 이야기입니다. Arco의 감성적인 픽셀 아트 비주얼은 즉각적인 몰입감을 선사하지만, 특히 저희를 흥미롭게 만든 것은 RPG의 동시 턴제 전투 시스템입니다.

간단히 설명하자면, 이 시스템은 플레이어가 시간이 정지된 상태에서 행동을 선택할 수 있는 방식으로 작동합니다. 적도 똑같이 행동합니다. 그런 다음 사이클이 다시 시작되기 전에 그 행동이 동시에 진행됩니다. 이 시스템은 행동, 결과, 반응의 시스템으로, 때때로 시간의 흐름을 거스를 수 있는 무정부적 능력과 아이템이 포함되어 있어 예측할 수 없게 됩니다.

모험을 진행하면서 내리는 선택에 따라 게임의 판도도 달라집니다. 각 플레이 가능한 캐릭터에는 죄책감 레벨이 있습니다. 죄책감이 높아지면 감정적 긴장이 전장에서 플레이어를 사냥하는 적대적인 정령으로 물리적으로 나타납니다. 이 초자연적인 적들은 물리 법칙을 따르지 않으며, 시간이 멈춘 상태에서도 플레이어를 쫓아올 수 있습니다. 내면의 악마를 많이 모을수록 전투는 더욱 어려워집니다. 무겁습니다. 하지만 그 라마들은 그 부담을 덜어줄 것입니다.

## 통제와 대학살 사이의 최적점을 찾다

출시에 앞서 게임 개발자와 함께 아르코의 전투 시스템을 공개하는 자리에서 노보트니악, 우리베, 가르시아는 진정으로 "역동적인" 시스템을 만들고 싶었다고 말했습니다. 다른 액션 게임의 전투는 빠른 버튼 조작이나 반사신경에 의존하는 경우가 많은데, 이러한 기술을 익힌 사람에게는 재미있을 수 있지만 제한적으로 느껴질 수도 있다고 생각했습니다. 반대로 평범한 턴제 전투는 너무 지루하다고 생각했습니다. 개발팀은 플레이어가 능동적으로 참여하지 않고 턴이 전개되는 것을 지켜보도록 강요하는 것을 원치 않았습니다. 그래서 두 가지를 결합했습니다.

이 핵심 콘셉트는 개발 과정에서 크게 변하지 않았지만, 여전히 미세 조정의 여지가 많았습니다. "처음 전투를 구현했을 때는 매우 느렸습니다."라고 노보트니악은 말합니다. "저희는 턴 단계에서 정확한 움직임을 제어하도록 했습니다. 따라갈 선을 그리려면 마우스를 드래그해야 했죠. 많은 컨트롤이 매우 느리고 정확하지 않았지만, 나중에는 아무 곳이나 클릭하여 \[동작을 대기열에 대기\]할 수 있다는 사실을 깨달았습니다. 모든 사소한 부분을 세세하게 관리할 필요가 없었습니다."

전투 시간 표시줄을 포함하지 못한 것도 진행에 차질을 빚을 뻔한 또 다른 문제였습니다. 개발팀은 플레이어에게 각 턴에 어떤 일이 일어날지 알려주는 타임라인이 포함된 사이드 퀘스트를 취소하고 해당 행동에 대응하도록 요청했습니다. 이론적으로는 전투를 예언의 퍼즐에 가까운 것으로 바꾸는 반전이었습니다. 하지만 제대로 작동하지 않았습니다.

노보트니악은 "가장 큰 문제는 전투 자체의 많은 부분을 이해하려고 노력하면서 이를 구현하려 했다는 점이라고 생각합니다."라고 말합니다. "처음부터 전투를 지금의 모습으로 만든 다음 추가하려고 했다면 성공할 수 있었을 겁니다. 하지만 우리는 너무 많은 기능을 동시에 구현하려고 했고, 그 중 하나가 작동하지 않으면 다른 기능을 변경해야 했습니다."

![arco-gameplay-01.gif](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltf07ac9f38a831f3a/66bce0f1d998344ab99ae70d/arco-gameplay-01.gif?width=700&auto=webp&quality=80&disable=upscale "arco-gameplay-01.gif")

노보트니악은 스커미시의 규모를 작게 유지하는 것이 장기적으로 더 효과적이었다고 설명합니다. 그렇다고 해서 문제가 발생하지 않는다는 것은 아닙니다. 언젠가는 플레이어에게 죽음이 찾아오기 때문에 문제가 될 수 있었습니다.

노보트니악은 "플레이어가 죽어도 별다른 결과가 없다는 것을 확실히 알려주고 싶었습니다."라고 말합니다. "이 게임은 다양한 경로가 있는 선형적인 게임입니다. 죽으면 다시 처음으로 밀려나는 로그라이크와는 다릅니다. \[...\] 플레이어가 다양한 시도를 하다가 실패해도 다시 시도할 수 있기를 바랐습니다. 그래야 전투가 빛나기 때문입니다."

플레이어의 실험을 처벌하지 않기로 의견을 모았습니다. 우리베는"턴 기반이 아니기 때문에 플레이어가 인투 더 브리치 같은 방식으로 접근하고 10분 동안 상황을 연구한다면 그런 종류의 게임이 아니라고생각합니다 ."라고 말합니다. "그냥 '실컷 해보고 알아보자'는 식이죠. 실수를 하면 순식간에 죽게 되니까요."

우리베는 전투 시스템이 "화학적"인 방식으로 유동적이라고 말합니다. 아이템과 능력이 서로 연결되어 예측할 수 없는 대학살을 일으킬 수 있습니다. 실제로는 직접플레이해봐야 알 수 있습니다. 비록 그것이 당신의 죽음을 유혹하는 것을 의미하더라도 말입니다.

"예를 들어 던지면 가스 구름을 생성하는 아이템이 있습니다. 그걸 뚫고 화살을 쏘면 화살에 독이 들어가죠. 그런 다음 적을 맞히면 적을 독살합니다."라고 우리베는 이러한 시퀀스가 어떻게 전개될 수 있는지 설명합니다. "우리는 이런 것들을 알려주지는 않지만, 여러분은 이런 상황을 많이 발견할 수 있습니다. 우리가 발견하지 못한 조합도 있을 수 있습니다. 바로 이 부분에서 게임이 빛을 발한다고 생각합니다."

![llama.gif](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt7f82b340ad36ef60/66bcdff40aff840375a74e4a/llama.gif?width=700&auto=webp&quality=80&disable=upscale "llama.gif")

현재 여기에 나열하기에는 아이템, 능력, 가능한 조합이 "너무 많다"고 할 수 있습니다. 따라서 실험을 장려하고 크레딧이 올라갈 때까지 아이템을 모으는 경향이 있는 플레이어를 설득하기 위해 아르코는 밀수품에 대해 관대하게 처리할 것입니다. 폭발하는 선인장이나 곰 덫과 같은 환경적 위험 요소를 배치하여 플레이어가 조금이라도 더 살도록 유도합니다. 이 게임은 플레이어에게 '만약 이렇게 한다면 어떻게 될까요?"라는 질문을 던지며 플레이어가 답을 찾도록 유도합니다.

개발팀이 앞서 언급했듯이, 부정적인 강화의 악순환을 피하기 위해 죽음도 순식간에 지나가게 됩니다. "플레이어에게서 빼앗을 수 있는 가장 큰 것은 시간이라고 생각합니다."라고 노보트니악은 말합니다. "그래서 저희는 \[죽음\]과 다시 시작하기까지의 시간을 최소화하려고 노력했습니다." 그는 플레이어가 사망할 경우 시간을 되돌릴 수 있는 '되돌리기' 버튼도 구현하려고 했지만, 결국 제작상의 제약으로 인해 삭제할 수밖에 없었다고 말합니다.

또한 플레이어가 자신의 바팟 기동을 공유하여 서로를 더 높은 곳으로 밀어붙일 수 있는 라마 라이딩 카오스 상인 커뮤니티를 만들었으면 하는 바람도 있습니다. 혼자서 실험하는 것도 재미있지만, 플레이어가 자신만의 독특한 톰풀리 브랜드를 녹화하고 월드 와이드 웹에 배포하도록 강제하는 시스템을 고안해낸다면 대담한 인디 개발자들에게 또 다른 차원의 성공을 가져다줄 수 있을 것입니다. 정말 대단하지 않을까요?

[](https://www.linkedin.com/sharing/share-offsite/?url=https://www.gamedeveloper.com/design/why-fuck-around-and-find-out-became-the-backbone-of-arco-s-combat)[](https://www.facebook.com/sharer/sharer.php?u=https://www.gamedeveloper.com/design/why-fuck-around-and-find-out-became-the-backbone-of-arco-s-combat)[](https://www.twitter.com/intent/tweet?url=https://www.gamedeveloper.com/design/why-fuck-around-and-find-out-became-the-backbone-of-arco-s-combat)[](https://www.gamedeveloper.com/cdn-cgi/l/email-protection#f6c98583949c939582cba19e8fd6d0d58ec4c1cd9083959dd6978499839892d6979892d6909f9892d6998382d0d58ec4c1cdd6949395979b93d6829e93d69497959d94999893d69990d6b7849599d0d58ec4c1cd85d695999b949782d0979b86cd9499928fcbbfd3c4c6829e9983919e82d3c4c6829e93d3c4c690999a9a99819f9891d3c4c69084999bd3c4c6b1979b93d3c4c6b29380939a99869384d3c4c69b9f919e82d3c4c69f98829384938582d3c4c68f9983d8d3c6b2d3c6b7d3c6b2d3c6b7d3c4c6a19e8fd3c4c6d0d58ec4c1cd9083959dd3c4c6978499839892d3c4c6979892d3c4c6909f9892d3c4c6998382d0d58ec4c1cdd3c4c6949395979b93d3c4c6829e93d3c4c69497959d94999893d3c4c69990d3c4c6b7849599d0d58ec4c1cd85d3c4c695999b949782d3c6b2d3c6b79e82828685d3c5b7d3c4b0d3c4b0818181d891979b93929380939a99869384d895999bd3c4b09293859f9198d3c4b0819e8fdb9083959ddb978499839892db979892db909f9892db998382db949395979b93db829e93db9497959d94999893db9990db97849599db85db95999b949782)[](https://www.reddit.com/submit?url=https://www.gamedeveloper.com/design/why-fuck-around-and-find-out-became-the-backbone-of-arco-s-combat&title=Why%20'fuck%20around%20and%20find%20out'%20became%20the%20backbone%20of%20Arco's%20combat)

## 저자 소개

[![Chris Kerr](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt1c7a117d71555292/650efbcad3423169a8871059/chris_kerr_headshot.jpg?width=400&auto=webp&quality=80&disable=upscale "Chris Kerr")](https://www.gamedeveloper.com/author/chris-kerr)

[

크리스 커

](https://www.gamedeveloper.com/author/chris-kerr)

뉴스 에디터, GameDeveloper.com

게임 개발자 뉴스 에디터인 크리스 커는 게임 업계에서 10년 이상의 경력을 쌓은 수상 경력이 있는 저널리스트이자 리포터입니다. 그의 바이라인은 Edge, Stuff, Wireframe, International Business Times, [PocketGamer.biz](https://pocketgamer.biz/)등 유명 인쇄 및 디지털 간행물에 게재되었습니다 . Chris는 경력 전반에 걸쳐 GDC, PAX Australia, Gamescom, 파리 게임 위크, Develop Brighton 등 주요 업계 행사를 취재했습니다. 여러 차례 디벨롭 스타 어워즈 심사위원으로 참여했으며, BBC 라디오 5 라이브에 출연해 뉴스 속보를 논의하기도 했습니다.

[자세한 내용 보기 크리스 커](https://www.gamedeveloper.com/author/chris-kerr)

게임 개발자의 일일 뉴스, 개발자 블로그, 이야기를 받은 편지함으로 바로 받아보세요.

[최신 소식 받기](https://gd-resources.gamedeveloper.com/free/w_gamf01/prgm.cgi)

추천 콘텐츠

* * *

원문: [https://www.gamedeveloper.com/design/why-fuck-around-and-find-out-became-the-backbone-of-arco-s-combat](https://www.gamedeveloper.com/design/why-fuck-around-and-find-out-became-the-backbone-of-arco-s-combat)