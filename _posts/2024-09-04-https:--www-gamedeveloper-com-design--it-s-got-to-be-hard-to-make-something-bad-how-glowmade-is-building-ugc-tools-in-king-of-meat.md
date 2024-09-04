---
title:  "'나쁜 것을 만들기는 어렵습니다': Glowmade가 King of Meat에서 UGC 도구를 구축하는 방법"

categories:
  - 번역
  
tags:
  - Game Developer
toc: true
toc_sticky: true
 
date: 2024-09-04
last_modified_at: 2024-09-04
---
[![Picture of Chris Kerr](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt1c7a117d71555292/650efbcad3423169a8871059/chris_kerr_headshot.jpg?width=100&auto=webp&quality=80&disable=upscale "Picture of Chris Kerr")](https://www.gamedeveloper.com/author/chris-kerr)

[크리스 커](https://www.gamedeveloper.com/author/chris-kerr), 뉴스 에디터

9월 4일, 2024

4 분 읽기

![Players tackle a dungeon in King of Meat](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt716d817829d4cafa/66d842db9ba222fa73cb31c6/King_of_Meat_Header.png?width=1280&auto=webp&quality=95&format=jpg&disable=upscale "Players tackle a dungeon in King of Meat")

Glowmade 이미지 제공

[](https://www.linkedin.com/sharing/share-offsite/?url=https://www.gamedeveloper.com/design/-it-s-got-to-be-hard-to-make-something-bad-how-glowmade-is-building-ugc-tools-in-king-of-meat)[](https://www.facebook.com/sharer/sharer.php?u=https://www.gamedeveloper.com/design/-it-s-got-to-be-hard-to-make-something-bad-how-glowmade-is-building-ugc-tools-in-king-of-meat)[](https://www.twitter.com/intent/tweet?url=https://www.gamedeveloper.com/design/-it-s-got-to-be-hard-to-make-something-bad-how-glowmade-is-building-ugc-tools-in-king-of-meat)[](https://www.gamedeveloper.com/cdn-cgi/l/email-protection#dae5a9afb8b0bfb9aee7fcf9a2e8ede193aefcf9a2e8ede1a9fabdb5aefaaeb5fab8bffab2bba8befaaeb5fab7bbb1bffaa9b5b7bfaeb2b3b4bdfab8bbbee0fcf9a2e8ede1fa92b5adfa9db6b5adb7bbbebffab3a9fab8afb3b6beb3b4bdfa8f9d99faaeb5b5b6a9fab3b4fa91b3b4bdfab5bcfa97bfbbaefcbbb7aae1b8b5bea3e793ffe8eaaeb2b5afbdb2aeffe8eaaeb2bfffe8eabcb5b6b6b5adb3b4bdffe8eabca8b5b7ffe8ea9dbbb7bfffe8ea9ebfacbfb6b5aabfa8ffe8eab7b3bdb2aeffe8eab3b4aebfa8bfa9aeffe8eaa3b5aff4ffea9effea9bffea9effea9bffe8eafcf9a2e8ede193aefcf9a2e8ede1a9ffe8eabdb5aeffe8eaaeb5ffe8eab8bfffe8eab2bba8beffe8eaaeb5ffe8eab7bbb1bfffe8eaa9b5b7bfaeb2b3b4bdffe8eab8bbbeffe99bfcf9a2e8ede1ffe8ea92b5adffe8ea9db6b5adb7bbbebfffe8eab3a9ffe8eab8afb3b6beb3b4bdffe8ea8f9d99ffe8eaaeb5b5b6a9ffe8eab3b4ffe8ea91b3b4bdffe8eab5bcffe8ea97bfbbaeffea9effea9bb2aeaeaaa9ffe99bffe89cffe89cadadadf4bdbbb7bfbebfacbfb6b5aabfa8f4b9b5b7ffe89cbebfa9b3bdb4ffe89cf7b3aef7a9f7bdb5aef7aeb5f7b8bff7b2bba8bef7aeb5f7b7bbb1bff7a9b5b7bfaeb2b3b4bdf7b8bbbef7b2b5adf7bdb6b5adb7bbbebff7b3a9f7b8afb3b6beb3b4bdf7afbdb9f7aeb5b5b6a9f7b3b4f7b1b3b4bdf7b5bcf7b7bfbbae)[](https://www.reddit.com/submit?url=https://www.gamedeveloper.com/design/-it-s-got-to-be-hard-to-make-something-bad-how-glowmade-is-building-ugc-tools-in-king-of-meat&title='It's%20got%20to%20be%20hard%20to%20make%20something%20bad%3A'%20How%20Glowmade%20is%20building%20UGC%20tools%20in%20King%20of%20Meat)

아마존 게임즈와 글로우메이드는 [킹 오브](https://store.steampowered.com/app/1926980/King_of_Meat/) [미트로](https://store.steampowered.com/app/1926980/King_of_Meat/)UGC(사용자 제작 콘텐츠) 시장을 노리고 있습니다 . 곧 출시될 이 던전 격투 게임은 아마도 Fall Guys와 Little Big Planet의 후예라고 할 수 있습니다. 경쟁을 좋아하는 분들은 유쾌하고 치명적인 도구 세트를 활용하여 자신만의 던전을 만들 수 있습니다. 아드레날린을 좋아하는 분들은 혼자 또는 최대 4명의 플레이어와 함께 건틀렛을 플레이할 수 있습니다.

2015년 미디어 몰리클과 라이온헤드의 베테랑들이 설립한 영국 스튜디오인 개발사 글로우메이드가 개발한 일련의 코스로 출시되지만, 킹오브 미트의 성공을 위해서는 궁극적으로 플레이어가 직접 악마 같은 던전을 제작하는 아이디어를 받아들여야 할 것입니다.

게임스컴 2024에서 게임 개발자들과 만난 스튜디오 공동 창립자이자 크리에이티브 디렉터인 조니 호퍼는글로우메이드가 플레이어가 자신의 꿈을 다른 누군가의 악몽으로 바꿀 수 있는킹 오브 미트의 크리에이트 모드를 설득력과 즐거움을 주는 툴로어떻게 구현할 계획인지 설명하며, 팀의 모토는 간단하다고 말했습니다.

## 일관된 시각적 언어는 크리에이터의 역량을 강화하는 핵심 요소입니다.

"나쁜 것을 만들기는 어렵습니다."라고 호퍼는 말합니다. "우리 대부분이 앉을 수 있는 중간 선이 있고, 이 선에서 여러 가지를 조합하여 레벨을 만들 수 있습니다. 기본은 간단해야 하고 실행 불가능한 것을 만들기는 어려워야 합니다."

호퍼는 글로우메이드가 "촉감이 느껴지는" 툴킷을 만들고자 노력했다고 말합니다. 즉, 플레이어가 활용할 수 있는 모든 도구나 아이템이 기대에 어긋나지 않고 기대에 부응하는 방식으로 작동해야 한다는 뜻입니다. "우리가 하고 있는 일은 플레이어에게 시각적인 것을 중심으로 만들어진 촉각적인 툴킷을 제공하는 것입니다."라고 그는 말합니다.

"수많은 메뉴가 있지만, 회전하는 스파이크 트랩을 내려놓으면 매번 예상한 대로 작동합니다. 이것이 우리가 시각적 언어에 접근한 방식입니다. 버튼은 버튼이니까요. 저희는 '여기 버튼이 있고, 이것은 압력 패드입니다'라는 방식이 아니라 플레이어가 모든 로직을 구성하여 자신만의 압력 패드를 만들도록 했습니다."

이러한 시각적 언어를 연마하는 과정에서 스튜디오는 슈퍼 마리오 메이커에서 영감을 얻었습니다. 글로우메이드의 공동 창립자인 마이크 그린은 플레이어가 슈퍼 마리오 레벨에서 아이템과 능력이 어떻게 작동하는지에 대한 선천적인 이해를 가지고 접근했기 때문에 이 프로젝트가 성공할 수 있었다고 생각합니다. 이러한 무의식적인 지식 덕분에 게임이 친근하게 느껴졌습니다.

"첫 번째 게임인 원더월드에는 정말 포괄적인 로직 시스템이 있었습니다. 그 게임에서는 많은 것을 할 수 있었지만 본질적으로 더 복잡해졌습니다. 예를 들어 문을 만들고 싶으면 그냥 문을 내려놓을 수 없었습니다. 나무로 무언가를 만든 다음 그 위에 회전 장치를 달아야 했죠."라고 그린은 말합니다.

"하지만 마리오 메이커를 사용하면 누구나 슈퍼 마리오를 알기 때문에 녹색 파이프가 무엇을 하는지, 적들이 어떻게 작동하는지 모두 알 수 있습니다. 제가 좋아하는 점은 일관성이 있다는 점입니다. 어떤 레벨에 들어가도 어떻게 작동하는지 알 수 있기 때문입니다."

그린은 글로우메이드가 원더월드에적용한 것과 동일한 기술을 사용하여 게임플레이 툴과 오브젝트를 빠르게 프로토타이핑하고있다고 설명합니다 . 즉, 팀은 빠르게 반복 작업을 수행하여 새로운 아이템을 만든 다음 검토하고 개선하여 코딩할 수 있는 '더 나은 버전'을 만들 수 있습니다.

임박한 추가 사항은 사용하기에 즐겁고 직관적인지 여부에 따라 승인 또는 거부됩니다. 이러한 심사 과정에서 가장 명백한 위험 신호 중 하나는 단순성보다 구체성과 복잡성에 대한 요구입니다.

"매우 구체적인 요청이 있었던 대화가 기억나는데, '내가 발명한 문제에 대한 놀라운 엣지 케이스를 해결해야 하는데 이 도구가 이를 해결해 주었으면 좋겠다'는 식의 경우였습니다."라고 호퍼는 말합니다.

"이 시점에서 우리는 한 발 물러서야 합니다. 왜냐하면 그것은 아주 작은 엣지 케이스에 복잡성을 더하는 것일 뿐이기 때문입니다. 이 도구가 정말 문제를 해결할 수 있을까요, 아니면 \[이 한 가지 사례\]에만 도움이 될까요? 전문 레벨 디자이너가 모든 것을 아우르는 레벨 디자인 툴에서 원하는 것과 다른 모든 사람에게 제공해야 하는 것 사이에서 균형을 유지해야 합니다."

호퍼는 UGC 툴은 누구나 쉽게 접근할 수 있어야 한다고 주장하지만, 단순히 제작만 원하는 플레이어 그룹과 순수하게 플레이만 원하는 플레이어 그룹이 존재한다는 점을 인정합니다. 이를 염두에 두고, 그는 King of Meat가 지속 가능한 성공을 거두려면 플레이어의 약 10%가 실제로 창작에 전념해야한다고 제안합니다 .

"플레이어의 10%가 창작을 선택한다면 정말 좋은 일입니다. 플레이어가 만든 콘텐츠 중 10%가 좋은 콘텐츠라면 기본적으로 필요한 것보다 더 많은 레벨을 확보한 셈이죠."라고 그는 말합니다. "1억 명의 플레이어가 있어야만 성공할 수 있는 것은 아닙니다. 그것이 우리의 성공 지표입니다."

자세히 읽어보세요:

[인기 스토리](https://www.gamedeveloper.com/keyword/top-stories)[\[이벤트\]](https://www.gamedeveloper.com/keyword/-event-gamescom)[게임스컴인터뷰](https://www.gamedeveloper.com/keyword/interviews)

[](https://www.linkedin.com/sharing/share-offsite/?url=https://www.gamedeveloper.com/design/-it-s-got-to-be-hard-to-make-something-bad-how-glowmade-is-building-ugc-tools-in-king-of-meat)[](https://www.facebook.com/sharer/sharer.php?u=https://www.gamedeveloper.com/design/-it-s-got-to-be-hard-to-make-something-bad-how-glowmade-is-building-ugc-tools-in-king-of-meat)[](https://www.twitter.com/intent/tweet?url=https://www.gamedeveloper.com/design/-it-s-got-to-be-hard-to-make-something-bad-how-glowmade-is-building-ugc-tools-in-king-of-meat)[](https://www.gamedeveloper.com/cdn-cgi/l/email-protection#b986caccdbd3dcdacd849f9ac18b8e82f0cd9f9ac18b8e82ca99ded6cd99cdd699dbdc99d1d8cbdd99cdd699d4d8d2dc99cad6d4dccdd1d0d7de99dbd8dd839f9ac18b8e8299f1d6ce99fed5d6ced4d8dddc99d0ca99dbccd0d5ddd0d7de99ecfefa99cdd6d6d5ca99d0d799f2d0d7de99d6df99f4dcd8cd9fd8d4c982dbd6ddc084f09c8b89cdd1d6ccded1cd9c8b89cdd1dc9c8b89dfd6d5d5d6ced0d7de9c8b89dfcbd6d49c8b89fed8d4dc9c8b89fddccfdcd5d6c9dccb9c8b89d4d0ded1cd9c8b89d0d7cddccbdccacd9c8b89c0d6cc979c89fd9c89f89c89fd9c89f89c8b899f9ac18b8e82f0cd9f9ac18b8e82ca9c8b89ded6cd9c8b89cdd69c8b89dbdc9c8b89d1d8cbdd9c8b89cdd69c8b89d4d8d2dc9c8b89cad6d4dccdd1d0d7de9c8b89dbd8dd9c8af89f9ac18b8e829c8b89f1d6ce9c8b89fed5d6ced4d8dddc9c8b89d0ca9c8b89dbccd0d5ddd0d7de9c8b89ecfefa9c8b89cdd6d6d5ca9c8b89d0d79c8b89f2d0d7de9c8b89d6df9c8b89f4dcd8cd9c89fd9c89f8d1cdcdc9ca9c8af89c8bff9c8bffcecece97ded8d4dcdddccfdcd5d6c9dccb97dad6d49c8bffdddccad0ded79c8bff94d0cd94ca94ded6cd94cdd694dbdc94d1d8cbdd94cdd694d4d8d2dc94cad6d4dccdd1d0d7de94dbd8dd94d1d6ce94ded5d6ced4d8dddc94d0ca94dbccd0d5ddd0d7de94ccdeda94cdd6d6d5ca94d0d794d2d0d7de94d6df94d4dcd8cd)[](https://www.reddit.com/submit?url=https://www.gamedeveloper.com/design/-it-s-got-to-be-hard-to-make-something-bad-how-glowmade-is-building-ugc-tools-in-king-of-meat&title='It's%20got%20to%20be%20hard%20to%20make%20something%20bad%3A'%20How%20Glowmade%20is%20building%20UGC%20tools%20in%20King%20of%20Meat)

## 저자 소개

[![Chris Kerr](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt1c7a117d71555292/650efbcad3423169a8871059/chris_kerr_headshot.jpg?width=400&auto=webp&quality=80&disable=upscale "Chris Kerr")](https://www.gamedeveloper.com/author/chris-kerr)

[

크리스 커

](https://www.gamedeveloper.com/author/chris-kerr)

뉴스 에디터, GameDeveloper.com

게임 개발자 뉴스 에디터 크리스 커는 게임 업계에서 10년 이상의 경력을 쌓은 수상 경력이 있는 저널리스트이자 리포터입니다. 그의 바이라인은 Edge, Stuff, Wireframe, International Business Times, [PocketGamer.biz](https://pocketgamer.biz/)등 유명 인쇄 및 디지털 간행물에 게재되었습니다 . Chris는 경력 전반에 걸쳐 GDC, PAX Australia, Gamescom, 파리 게임 위크, 디벨롭 브라이튼 등 주요 업계 행사를 취재했습니다. 또한 여러 차례 디벨롭 스타 어워즈 심사위원으로 참여했으며, BBC 라디오 5 라이브에 출연해 뉴스 속보를 논의하기도 했습니다.

[자세한 내용 보기 크리스 커](https://www.gamedeveloper.com/author/chris-kerr)

게임 개발자의 일일 뉴스, 개발자 블로그, 이야기를 받은 편지함으로 바로 받아보세요.

[최신 소식 받기](https://gd-resources.gamedeveloper.com/free/w_gamf01/prgm.cgi)

추천 콘텐츠

* * *

원문: [https://www.gamedeveloper.com/design/-it-s-got-to-be-hard-to-make-something-bad-how-glowmade-is-building-ugc-tools-in-king-of-meat](https://www.gamedeveloper.com/design/-it-s-got-to-be-hard-to-make-something-bad-how-glowmade-is-building-ugc-tools-in-king-of-meat)