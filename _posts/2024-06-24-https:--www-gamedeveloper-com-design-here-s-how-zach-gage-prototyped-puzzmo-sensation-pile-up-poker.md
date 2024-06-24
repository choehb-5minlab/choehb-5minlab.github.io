---
title:  "잭 게이지가 퍼즐모에서 센세이션을 일으킨 파일업 포커의 프로토타입을 제작한 방법은 다음과 같습니다."

categories:
  - 번역
  
tags:
  - Game Developer
toc: true
toc_sticky: true
 
date: 2024-06-24
last_modified_at: 2024-06-24
---
[![Picture of Chris Kerr](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt1c7a117d71555292/650efbcad3423169a8871059/chris_kerr_headshot.jpg?width=100&auto=webp&quality=80&disable=upscale "Picture of Chris Kerr")](https://www.gamedeveloper.com/author/chris-kerr)

[크리스 커](https://www.gamedeveloper.com/author/chris-kerr), 뉴스 에디터

6월 24일, 2024

5분 읽기

![The final version of Pile-up Poker](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltb2475fed6287a6a1/667967b1e6444c393c40bb6e/PUP_Header.png?width=850&auto=webp&quality=95&format=jpg&disable=upscale "The final version of Pile-up Poker")

Hearst 이미지 제공

[](https://www.linkedin.com/sharing/share-offsite/?url=https://www.gamedeveloper.com/design/here-s-how-zach-gage-prototyped-puzzmo-sensation-pile-up-poker)[](https://www.facebook.com/sharer/sharer.php?u=https://www.gamedeveloper.com/design/here-s-how-zach-gage-prototyped-puzzmo-sensation-pile-up-poker)[](https://www.twitter.com/intent/tweet?url=https://www.gamedeveloper.com/design/here-s-how-zach-gage-prototyped-puzzmo-sensation-pile-up-poker)[](https://www.gamedeveloper.com/cdn-cgi/l/email-protection#142b6761767e717760295c71667132376c26232f67347c7b63344e75777c34537573713464667b607b606d6471703444616e6e797b3467717a6775607d7b7a34447d787139616434447b7f7166327579642f767b706d295d312624607c7b61737c60312624607c71312624727b78787b637d7a7331262472667b793126245375797131262450716271787b647166312624797d737c603126247d7a6071667167603126246d7b613a3124503124553124503124553126245c71667132376c26232f673126247c7b633126244e75777c3126245375737131262464667b607b606d64717031262444616e6e797b31262467717a6775607d7b7a312624447d7871396164312624447b7f71663124503124557c606064673127553126523126526363633a7375797170716271787b6471663a777b793126527071677d737a3126527c7166713967397c7b63396e75777c39737573713964667b607b606d6471703964616e6e797b3967717a6775607d7b7a39647d787139616439647b7f7166)[](https://www.reddit.com/submit?url=https://www.gamedeveloper.com/design/here-s-how-zach-gage-prototyped-puzzmo-sensation-pile-up-poker&title=Here's%20how%20Zach%20Gage%20prototyped%20Puzzmo%20sensation%20Pile-up%20Poker)

[퍼즐모](https://puzzmo.com) 공동창업자 잭 게이지가 최신 프로젝트의 프로토타입을 어떻게 제작했는지 궁금하신가요? 저희도 궁금하실 거라 생각했습니다. 이달 초, 저희 는 TypeShift와 Knotwords의 디자이너와 함께 그의 새로운 한입 크기의 신문 퍼즐 게임인 Pile-up Poker (PUP)에 대해 자세히 알아 봤습니다.

대화 중에 Gage는 프로젝트가 제작 과정에서 어떻게 극적으로 변화하여 급성장하는 허스트의 퍼즐 플랫폼에서 가장 인기 있는 작품 중 하나가 되었는지 설명했습니다.

또한 , 프로젝트가 훨씬 더 친근한 게임으로 재탄생하기까지 어떤 과정을 거쳤는지 알 수 있는4가지 버전의 파일업 포커를살짝 공개했습니다.

게이지가 친절하게도 초기 버전의 이미지와 주석을 공유할 수 있도록 허락해 주셨으며, 이를 통해 이 타이틀이 왜 폐기되고 이후 재구성되어 [오늘날의 실험적인 카드 기반 수수께끼가](https://puzzmo.com/game/pile-up-poker) 되었는지이해하실 수 있습니다.

## PUP-v0 (2월 23일)

![The first version of Pile-up Poker, showing a sparse playspace that focuses on mechanics ](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt42585f14016f87f6/6679629f1b37935f4e06b6c7/PuP_v0.png?width=700&auto=webp&quality=80&disable=upscale "The first version of Pile-up Poker, showing a sparse playspace that focuses on mechanics ")

이것은 게임의 가장 초기에 플레이 가능한 버전이었습니다. Gage는 이 초기 프로토타입의 목표는 "가능한 한 빨리 디지털 버전을 출시하고 제약 조건을 추가하기보다 플레이 가능성을 높이는 데 더 집중하는 것"이었다고 말합니다.

"이 버전에서는 그리드의 어느 곳에나 카드를 배치할 수 있었습니다. 이를 테스트할 때는 배치에 대한 규칙을 코드로 구현하는 대신 규칙이 있는 것처럼 가정했습니다."라고 그는 덧붙입니다. "이렇게 하면 프로그래밍이 더 빨라지고 코드를 변경할 필요 없이 머릿속으로 규칙을 변경하고 시도할 수 있는 유연성을 확보할 수 있었습니다."

다음은 이 첫 번째 반복의 규칙입니다:

*   한 턴에 최대 4장의 카드를 이동할 수 있습니다. 카드는 가장 위쪽의 빈 줄 또는 이미 카드가 있는 줄로 이동할 수 있습니다.
    
*   카드를 동시에 여러 행으로 옮길 수 없습니다.
    
*   한 턴에 최대 n-1장의 카드까지만 이동할 수 있으며, 여기서 n은 지난 턴에 이동한 카드 수입니다. 따라서 1턴에 카드 3장을 이동했다면 2턴에는 최대 2장까지만 이동할 수 있습니다.
    
*   '스탠드'를 하면 이동한 카드가 다시 4개로 초기화되고 다음 패를 받게 됩니다.
    

Gage에 따르면, 여기서 목표는 최고의 포커 핸드 12개를 만드는 것이었습니다(가로, 세로, 대각선 매치 기준). 조커는 와일드 카드로서 각 핸드에서 가장 좋은 카드로 간주되었습니다. 드로우 더미 뒤쪽에서 살짝 보이는 카드가 플레이어가 마지막으로 뽑는 카드였습니다.

## PUP-v1 (3월 6일)

![The second version of Pile-up Poker, featuring artwork and UI elements](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt67a8ff23d45144d8/6679630024a6c9a585b8e271/PuP_v1.png?width=700&auto=webp&quality=80&disable=upscale "The second version of Pile-up Poker, featuring artwork and UI elements")

이 단계에서 퍼즐모 팀은 PUP-0에 만족하고 있었기 때문에 "가독성을 높인 카드 아트, 핸드 수에 따른 승수 구현, 득점한 핸드 옆에 핸드 정보 표시" 등 플레이 편의성을 개선하는 데 집중했습니다.

"이 버전에서 나온 많은 디자인 아이디어가 게임의 최종 버전에 반영된 것을 볼 수 있습니다. 눈썰미가 좋으신 분이라면 이번 버전에서 사용한 수트 아트와 카드가 플립플롭 솔리테어에서 바로 가져온 것임을 눈치챌 수 있을 겁니다."라고 Gage는 덧붙입니다.

"이전 버전의 게임은 매우 기술적인 게임이었으며, 카드가 왼쪽으로 이동하여 빈 공간을 메우기 때문에 버린 카드를 사용하여 세로로 정렬하는 것이 좋은 전략입니다."

## PUP-v2(3월 15일)

![A version of Pile-up Poker that featured a new discard mechanic](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt3f8b3783a0c55c0d/667963722e6ac2b3e1e79e27/PuP_v2.png?width=700&auto=webp&quality=80&disable=upscale "A version of Pile-up Poker that featured a new discard mechanic")

이 버전에서 게이지가 실험한 큰 변화는 플레이어가 카드를 보드 위로 이동하면서 배치할 수 있는 '공백으로 버리기'였습니다.

"게임 전체에 3번의 실제 버리기가 있었고, 이를 사용하면 다음 턴의 이동 수와 이번 턴의 이동 수 모두 한 번의 이동으로 계산되었습니다."라고 Gage는 설명합니다.

"이 아이디어의 목표는 게임의 마지막 라운드가 덜 철도처럼 느껴지도록 하는 것이었습니다. 게임의 마지막 두 턴에는 결정 포인트가 거의 없다는 것을 알게 되었습니다. 플레이어가 끝까지 버릴 수 있는 선택적 버리기 기능을 추가하면 게임의 마지막이 더욱 흥미진진해집니다."

퍼즐모 팀은 또한 PUP-v2에서 윤곽선을 사용하여 카드를 놓을 수 있는 위치를 명확히 하는 등 시각적인 개선도 계속했습니다. 노란색 막대는 '보너스 핸드'를 나타내는데, 매 게임마다 무작위로 주어지며 다른 모든 핸드의 2배의 가치가 있습니다.

## PUP-v3 (4월 2일)

![A more complex and unruly version of Pile-up Poker that needed more fine-tuning](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltb17cd586cc06c552/667963e2fd0db4496777f4e1/PuP_v3.png?width=700&auto=webp&quality=80&disable=upscale "A more complex and unruly version of Pile-up Poker that needed more fine-tuning")

Gage는 PUP-v3가 "조금 이상하고 불안정해지기 시작한" 시점이라고 말합니다. 큰 변화는 버려진 카드를 빈 칸이 아닌 드로우 덱 뒤쪽으로 옮기는 것이었습니다.

"카드를 삭제하는 대신 나중에 자신에게 넘겨주는 방식입니다."라고 Gage는 설명합니다. "이렇게 하면 버리기 이동을 둘러싼 수많은 흥미로운 전략이 가능해져 매우 흥미롭고 역동적인 엔드게임이 만들어집니다. 갑자기 현재 줄, 카드를 이동할 수 있는 자리, 버린 1~4장의 카드가 서로 균형을 맞춰야 했습니다.

"궁극적으로 이 버전의 게임이 가장 기술적이고 가장 흥미롭지만, 플레이하기에는 너무 많은 작업이 필요하고 설명하기에는 너무 많은 작업이 필요한 것처럼 느껴졌습니다."

PUP-v3의 복잡성 때문에 게이지가 프로젝트를 (잠시) 취소하게 되었습니다. 물론 퍼즐모 팀이 몇 가지 선택 포인트를 제공한 후 게이지가 파일업 포커를 훨씬 더 유동적인 게임으로재구성하는 데 도움을 준 덕분에 프로젝트는 위기에서 벗어날 수 있었습니다.

그이후에 일어난 일에 대해 자세히 알아보려면 [게이지와의 인터뷰 전문을 읽어보세요](https://www.gamedeveloper.com/design/how-pile-up-poker-survived-cancellation-to-become-a-puzzmo-hit).

[](https://www.linkedin.com/sharing/share-offsite/?url=https://www.gamedeveloper.com/design/here-s-how-zach-gage-prototyped-puzzmo-sensation-pile-up-poker)[](https://www.facebook.com/sharer/sharer.php?u=https://www.gamedeveloper.com/design/here-s-how-zach-gage-prototyped-puzzmo-sensation-pile-up-poker)[](https://www.twitter.com/intent/tweet?url=https://www.gamedeveloper.com/design/here-s-how-zach-gage-prototyped-puzzmo-sensation-pile-up-poker)[](https://www.gamedeveloper.com/cdn-cgi/l/email-protection#cbf4b8bea9a1aea8bff683aeb9aeede8b3f9fcf0b8eba3a4bceb91aaa8a3eb8caaacaeebbbb9a4bfa4bfb2bbaeafeb9bbeb1b1a6a4ebb8aea5b8aabfa2a4a5eb9ba2a7aee6bebbeb9ba4a0aeb9edaaa6bbf0a9a4afb2f682eef9fbbfa3a4beaca3bfeef9fbbfa3aeeef9fbada4a7a7a4bca2a5aceef9fbadb9a4a6eef9fb8caaa6aeeef9fb8faebdaea7a4bbaeb9eef9fba6a2aca3bfeef9fba2a5bfaeb9aeb8bfeef9fbb2a4bee5eefb8feefb8aeefb8feefb8aeef9fb83aeb9aeede8b3f9fcf0b8eef9fba3a4bceef9fb91aaa8a3eef9fb8caaacaeeef9fbbbb9a4bfa4bfb2bbaeafeef9fb9bbeb1b1a6a4eef9fbb8aea5b8aabfa2a4a5eef9fb9ba2a7aee6bebbeef9fb9ba4a0aeb9eefb8feefb8aa3bfbfbbb8eef88aeef98deef98dbcbcbce5acaaa6aeafaebdaea7a4bbaeb9e5a8a4a6eef98dafaeb8a2aca5eef98da3aeb9aee6b8e6a3a4bce6b1aaa8a3e6acaaacaee6bbb9a4bfa4bfb2bbaeafe6bbbeb1b1a6a4e6b8aea5b8aabfa2a4a5e6bba2a7aee6bebbe6bba4a0aeb9)[](https://www.reddit.com/submit?url=https://www.gamedeveloper.com/design/here-s-how-zach-gage-prototyped-puzzmo-sensation-pile-up-poker&title=Here's%20how%20Zach%20Gage%20prototyped%20Puzzmo%20sensation%20Pile-up%20Poker)

## 저자 소개

[![Chris Kerr](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt1c7a117d71555292/650efbcad3423169a8871059/chris_kerr_headshot.jpg?width=400&auto=webp&quality=80&disable=upscale "Chris Kerr")](https://www.gamedeveloper.com/author/chris-kerr)

[

크리스 커

](https://www.gamedeveloper.com/author/chris-kerr)

뉴스 에디터, GameDeveloper.com

게임 개발자 뉴스 에디터인 크리스 커는 게임 업계에서 10년 이상의 경력을 쌓은 수상 경력이 있는 저널리스트이자 리포터입니다. 그의 바이라인은 Edge, Stuff, Wireframe, International Business Times, [PocketGamer.biz](https://pocketgamer.biz/)등 유명 인쇄 및 디지털 간행물에 게재되었습니다 . Chris는 경력 전반에 걸쳐 GDC, PAX Australia, Gamescom, 파리 게임 위크, 디벨롭 브라이튼 등 주요 업계 행사를 취재했습니다. 여러 차례 디벨롭 스타 어워즈 심사위원으로 참여했으며, BBC 라디오 5 라이브에 출연해 뉴스 속보를 논의하기도 했습니다.

[자세한 내용 보기 크리스 커](https://www.gamedeveloper.com/author/chris-kerr)

게임 개발자의 일일 뉴스, 개발자 블로그, 이야기를 받은 편지함으로 바로 받아보세요.

[최신 소식 받기](https://gd-resources.gamedeveloper.com/free/w_gamf01/prgm.cgi)

추천 콘텐츠

* * *

원문: [https://www.gamedeveloper.com/design/here-s-how-zach-gage-prototyped-puzzmo-sensation-pile-up-poker](https://www.gamedeveloper.com/design/here-s-how-zach-gage-prototyped-puzzmo-sensation-pile-up-poker)