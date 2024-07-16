---
title:  "심층 분석: GOG가 알파 프로토콜의 재출시로 불완전한 부분을 보완한 방법"

categories:
  - 번역
  
tags:
  - Game Developer
toc: true
toc_sticky: true
 
date: 2024-07-17
last_modified_at: 2024-07-17
---
[![Picture of Adam Ziółkowski](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltd709c2f6ad0896cd/657b3aae1fb1b4040a0e1821/Game_Developer_G_Logo_RGB.png?width=100&auto=webp&quality=80&disable=upscale "Picture of Adam Ziółkowski")](https://www.gamedeveloper.com/author/adam-zi-kowski)

[아담 지오코프스키](https://www.gamedeveloper.com/author/adam-zi-kowski)

7월 16, 2024

6분 읽기

![](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt982cabcfd520881b/668c022a549553aeb06d2662/6abe0fae79b1106e5645769b0e6e86a2e4bcc5b818e6f359274c94ff59f97926.jpg?width=1280&auto=webp&quality=95&format=jpg&disable=upscale)

SEGA 이미지 제공.

[](https://www.linkedin.com/sharing/share-offsite/?url=https://www.gamedeveloper.com/design/deep-dive-how-gog-perfected-the-imperfect-with-the-re-release-of-alpha-protocol)[](https://www.facebook.com/sharer/sharer.php?u=https://www.gamedeveloper.com/design/deep-dive-how-gog-perfected-the-imperfect-with-the-re-release-of-alpha-protocol)[](https://www.twitter.com/intent/tweet?url=https://www.gamedeveloper.com/design/deep-dive-how-gog-perfected-the-imperfect-with-the-re-release-of-alpha-protocol)[](https://www.gamedeveloper.com/cdn-cgi/l/email-protection#4c733f392e26292f38710829293c6c08253a29766c04233b6c0b030b6c3c293e2a292f3829286c3824296c25213c293e2a292f386c3b2538246c3824296c3e29613e2920292d3f296c232a6c0d203c242d6c1c3e2338232f23206a2d213c772e2328357105697e7c382423392b2438697e7c382429697e7c2a232020233b25222b697e7c2a3e2321697e7c0b2d2129697e7c08293a2920233c293e697e7c21252b2438697e7c252238293e293f38697e7c35233962697c08697c0d697c08697c0d697e7c0829293c697e7c08253a29697f0d697e7c04233b697e7c0b030b697e7c3c293e2a292f382928697e7c382429697e7c25213c293e2a292f38697e7c3b253824697e7c382429697e7c3e29613e2920292d3f29697e7c232a697e7c0d203c242d697e7c1c3e2338232f2320697c08697c0d2438383c3f697f0d697e0a697e0a3b3b3b622b2d212928293a2920233c293e622f2321697e0a28293f252b22697e0a2829293c6128253a296124233b612b232b613c293e2a292f382928613824296125213c293e2a292f38613b25382461382429613e29613e2920292d3f2961232a612d203c242d613c3e2338232f2320)[](https://www.reddit.com/submit?url=https://www.gamedeveloper.com/design/deep-dive-how-gog-perfected-the-imperfect-with-the-re-release-of-alpha-protocol&title=Deep%20Dive%3A%20How%20GOG%20perfected%20the%20imperfect%20with%20the%20re-release%20of%20Alpha%20Protocol)

게임 개발자 심층 분석은 비디오 게임의 특정 디자인, 아트 또는 기술적 특징을 조명하여 단순해 보이는 근본적인 디자인 결정이 실제로는 전혀 단순하지 않다는 것을 보여주기 위해 진행 중인 시리즈입니다.

이전 편 에서는[이스타르 게임즈가 더 라스트 스펠의 새로운 드워프 종족 디자인에 접근한 방법](https://www.gamedeveloper.com/design/deep-dive-designing-a-new-dwarf-race-in-the-last-spell), 크릴바이트 스튜디오가 [곧 출시될 푸드 트럭 시뮬레이션 프룻버스에서 '할리우드 버전'의 요리를](https://www.gamedeveloper.com/programming/deep-dive-cooking-in-fruitbus) 추구한 이유 , [리틀 키티, 빅 시티의 진정성 없는 애니메이션과](https://www.gamedeveloper.com/art/deep-dive-how-little-kitty-big-city-rejects-realism-to-achieve-authenticity)같은 주제를 다뤘습니다 .

이번 편에서는 GOG의 게임 출시 기술 프로듀서인 Adam "Adim" Ziółkowski가 현 시대에 맞게알파 프로토콜을업데이트하는 과정 , 특히 DRM과 클라우드 저장에 대한 요구 사항에 대해 설명합니다.

안녕하세요, 저는 GOG의 게임 출시 기술 프로듀서인 Adam "Adim" Ziółkowski입니다. 오늘은 15년 가까이 된 게임을 최신 디지털 플랫폼에 맞게 업데이트하는 데 따른 어려움에 대해 말씀드리고자 이 자리에 모였습니다.

## 알파 프로토콜이 돌아왔습니다! 하지만 정확히 왜 그리고 어떻게 이런 일이 일어났을까요?

사람들의 일반적인 첫 반응은 "왜 알파 프로토콜이죠? "입니다. 2010년 5월 28일에 알파 프로토콜이 출시되었을 당시에는 완벽한 작품 이 아니었다는 것을 잘 알고 있습니다. 옵시디언 엔터테인먼트는 여러 면에서 혁명적이라고 할 수 있는 매우 야심차고 방대한 프로젝트에 착수했습니다. 플레이어는 자신의 결정에 따라 크게 달라지는 매우 정교한 스토리라인을 갖춘 첩보 RPG를 받게 되었습니다. 그러나 이러한 광범위한 프로젝트에서는 야망이 자신의 꼬리를 먹기 시작하고 게임의 과도한 성장으로 인해 제어가 어려워지는 경우가 종종 발생합니다. 그렇기 때문에 개발자가 출시 후 나타나는 모든 버그와 문제를 예상하고 제거할 수 없었습니다. 요즘에는 개발자가 작품을 수정하는 데 몇 주, 몇 달, 심지어 몇 년을 소비하는 것이 특별한 일이 아닙니다. 플레이어의 불만이 극에 달한 것으로 간주될 수 있는 게임으로는노 맨스 스카이나 디아블로 III와 같은 히트작이 있습니다.

GOG는 출시된 지 1년이 되었든 20년이 되었든 모든 게임은 다시 한 번 기회를 얻을 자격이 있다고 믿습니다. 알파 프로토콜과마찬가지로 저희의 주요 목표 중 하나는 디지털 배포가 불가능한 타이틀을 되살리고 가능한 한 많은 타이틀을 다시 출시하는 것입니다. 과거의 모든 타이틀을 되살리는 것은 불가능한 작업일 수도 있지만, 이것이 바로 저희 회사가 설립된 이유입니다. 그것이 바로 저희의 존재 이유입니다.

![Alpha Protocol Screenshot](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt8be9af69745ff7b9/668bfff4b54ce98ee45f4f6d/2ac9e9704434c4374476cd69760d6d166e53927276c3370b2b5a61dd6169f61f.jpg?width=700&auto=webp&quality=80&disable=upscale "Alpha Protocol Screenshot")

SEGA 이미지 제공.

## 라이선스 투 킬(게임)

고전 게임을 되살리는 데 있어 가장 큰 어려움 중 하나는 수년에 걸쳐 복잡해진 게임의 지위와 모든 법적 문제를 정리하는 것입니다. 알파 프로토콜의경우 가장 큰 미지의 영역은 음악 트랙에 대한 라이선스였습니다. 저희는 최대한 원작에 가까운 콘텐츠를 사용자에게 제공하는 것을 목표로 삼았기 때문에 브랜드 소유자인 SEGA와 협력하여 게임에 등장하는 트랙에 대한 권리를 되찾았습니다. 이 과정을 요약하자면, 모든 트랙에 대한 권리를 갱신할 수 있었다고 말씀드릴 수 있습니다. 하지만 이러한 문제를 해결하는 과정이 항상 쉽고 순조로운 것은 아닙니다. 스타트렉 게임 라이선스 취득의 경우처럼 몇 달이 걸리는 경우도 있습니다.

이는 현재 GOG에서 제공되는 버전의 콘텐츠가 변경되지 않기 때문에 중요합니다. 이러한 전략은 스토어에 있는 모든 게임에 적용되는 DRM-Free 접근 방식과도 일치합니다. 그 이유는 플레이어가 라이브러리에 있는 게임과 함께 모든 트랙이 포함된 오프라인 설치 프로그램에 쉽게 액세스하고 필요한 기간 동안 드라이브에 보관할 수 있기 때문입니다.

## 14년 만에 버그 수정

알파 프로토콜에서는 버전 1.0의 소스 코드에서 편안하게 작업할 수 있었습니다. 이후 버전인 1.1에는 몇 가지 수정 사항이 포함되어 있었지만 저희 팀에서는 액세스할 수 없었습니다. 게다가 1.0 버전에서는 무엇보다도 PC 버전에서는 제공되지 않았던 업적 지원 기능을 추가할 수 있었기 때문에 계속 작업하고 싶었습니다.

SEGA로부터 받은 게임 빌드에는 이미 일부 수정 사항이 포함되어 있었지만, 모든 수정 사항이 포함된 것은 아니었습니다. 예를 들어, 플레이어가 메인 퀘스트 중 하나를 완료하지 못하는 심각한 버그 중 하나를 제거해야 했습니다. 앞서 플레이어에게 최대한 원본에 가까운 버전을 제공하기 위해 노력한다고 말씀드렸지만, 중요하고 중요한 개선의 여지가 있다고 판단되면 항상 이를 구현하려고 노력합니다. 알파 프로토콜에서는 업적을 추가하고 게임을 클라우드 저장을 위해 GOG GALAXY와 호환되도록 만들었습니다. 또한 고해상도 지원을 추가하고 최신 컴퓨터의 성능에 맞게 기본 게임 설정을 최적화했습니다.

가장 어려웠던 부분은 게임 코드를 다시 컴파일하고 업적/트로피를 추가할 수 있는 개발자 환경을 다시 만드는 것이었습니다. 이를 위해 저희는 적절한 코드 컴파일을 보장할 수 있는 시대별 머신을 만들었습니다. 그런 다음 이전 버전의 갤럭시 소프트웨어 개발 키트(SDK) 버전이 이전 컴파일러에서 작동하는지 테스트했습니다. 작동했습니다! 그런 다음 게임의 업적을 처리하는 코드의 Xbox 버전을 구현할 수 있었습니다. 아무도 해보지 않은 일을 할 수 있었기 때문에 이 부분이 프로젝트에서 가장 흥미로웠습니다. 다른 PC 버전에는 없는 독특한 기능을 추가했습니다.

물론 GOG에서 제공되는 버전이 Windows 10과 11이 설치된 PC에서 원활하게 실행되도록 최적화했습니다. 또 다른 중요한 변화는 듀얼센스, 듀얼쇼크 4, 닌텐도 스위치 프로, 엑스박스 시리즈, 엑스박스 원 패드와 같은 최신 컨트롤러를 지원한다는 점입니다. 듀얼센스 엣지는 저희를 놀라게 했지만, 현재 이 디바이스와의 원활한 호환성을 보장하기 위해 노력하고 있습니다. 또한 디지털 릴리스에서는 제공되지 않았던 공식 언어 버전을 다시 선보였습니다. 여기에는 폴란드어, 체코어, 러시아어 현지화가 포함됩니다.

![Alpha Protocol Screenshot](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt4f403c4deca225f0/668c009228803a30a6a4a0fb/cfb4ae030a9d4e1cb08f5c063fe94f3da93898d6d7aea83ac90b5dd7e382221f.jpg?width=700&auto=webp&quality=80&disable=upscale "Alpha Protocol Screenshot")

SEGA 이미지 제공.

## DRM의 족쇄를 벗어 던지다

가장 중요하게 생각한 것은 DRM을 제거하는 것이었습니다. 게임 자체를 망가뜨리고 싶지 않았기 때문에 특히 어려운 작업이었습니다. 다행히도 15년 경력의 숙련된 리버스 엔지니어가 있어 훨씬 더 복잡하고 복잡한 프로젝트에서 종종 문제를 해결해 주었습니다. 전반적인 기술 작업을 고려할 때 DRM을 제거하는 작업은 실제로 게임을 다시 출시하는 전체 과정에서 가장 노동 집약적이고 시간이 많이 소요되는 부분이었습니다.

알파 프로토콜의존재가 다시는 훼손되지 않도록 하는 것이얼마나 중요한지 강조하기 위해 가장 참여도가 높은 유저들에게 500개의 키를 배포했습니다. 또한, 지난 15년 이상 GOG가 존재할 수 있도록 도와준 커뮤니티에 감사를 표할 수 있는 기회이기도 합니다.

알파 프로토콜이 몇 년 전만 해도 따뜻한 환영을 받지 못했지만, GOG로 돌아왔을 때 미디어의 관심을 보니 마음이 뿌듯했습니다. 주요 게임 포털에서 깜짝 출시 소식을 전했고, 일부 에디터는 오랜 세월이 지난 후에도 게임이 어떻게 유지되는지 확인하기 위해 게임을 다시 방문했습니다. 또한 커뮤니티에서도 부활이 필요한 다른 타이틀을 떠올리며 또 하나의 고전 게임이 복원된 것을 반가워하는 긍정적인 댓글이 많이 달렸습니다. 저희는 가능한 한 많은 게임을 여러분께 다시 선보이기 위해 최선을 다하고 있다는 점을 다시 한 번 말씀드리고 싶습니다.

자세히 읽어보세요:

인기 [스토리딥](https://www.gamedeveloper.com/keyword/top-stories)[다이브기능](https://www.gamedeveloper.com/keyword/features)

[](https://www.linkedin.com/sharing/share-offsite/?url=https://www.gamedeveloper.com/design/deep-dive-how-gog-perfected-the-imperfect-with-the-re-release-of-alpha-protocol)[](https://www.facebook.com/sharer/sharer.php?u=https://www.gamedeveloper.com/design/deep-dive-how-gog-perfected-the-imperfect-with-the-re-release-of-alpha-protocol)[](https://www.twitter.com/intent/tweet?url=https://www.gamedeveloper.com/design/deep-dive-how-gog-perfected-the-imperfect-with-the-re-release-of-alpha-protocol)[](https://www.gamedeveloper.com/cdn-cgi/l/email-protection#1f206c6a7d757a7c6b225b7a7a6f3f5b76697a253f5770683f5850583f6f7a6d797a7c6b7a7b3f6b777a3f76726f7a6d797a7c6b3f68766b773f6b777a3f6d7a326d7a737a7e6c7a3f70793f5e736f777e3f4f6d706b707c7073397e726f247d707b6622563a2d2f6b77706a78776b3a2d2f6b777a3a2d2f7970737370687671783a2d2f796d70723a2d2f587e727a3a2d2f5b7a697a73706f7a6d3a2d2f727678776b3a2d2f76716b7a6d7a6c6b3a2d2f66706a313a2f5b3a2f5e3a2f5b3a2f5e3a2d2f5b7a7a6f3a2d2f5b76697a3a2c5e3a2d2f5770683a2d2f5850583a2d2f6f7a6d797a7c6b7a7b3a2d2f6b777a3a2d2f76726f7a6d797a7c6b3a2d2f68766b773a2d2f6b777a3a2d2f6d7a326d7a737a7e6c7a3a2d2f70793a2d2f5e736f777e3a2d2f4f6d706b707c70733a2f5b3a2f5e776b6b6f6c3a2c5e3a2d593a2d5968686831787e727a7b7a697a73706f7a6d317c70723a2d597b7a6c7678713a2d597b7a7a6f327b76697a3277706832787078326f7a6d797a7c6b7a7b326b777a3276726f7a6d797a7c6b3268766b77326b777a326d7a326d7a737a7e6c7a327079327e736f777e326f6d706b707c7073)[](https://www.reddit.com/submit?url=https://www.gamedeveloper.com/design/deep-dive-how-gog-perfected-the-imperfect-with-the-re-release-of-alpha-protocol&title=Deep%20Dive%3A%20How%20GOG%20perfected%20the%20imperfect%20with%20the%20re-release%20of%20Alpha%20Protocol)

## 저자 소개

[![Adam Ziółkowski](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltd709c2f6ad0896cd/657b3aae1fb1b4040a0e1821/Game_Developer_G_Logo_RGB.png?width=400&auto=webp&quality=80&disable=upscale "Adam Ziółkowski")](https://www.gamedeveloper.com/author/adam-zi-kowski)

[

아담 지오코프스키

](https://www.gamedeveloper.com/author/adam-zi-kowski)

[Adam Ziółkowski 더보기](https://www.gamedeveloper.com/author/adam-zi-kowski)

게임 개발자의 일일 뉴스, 개발자 블로그, 스토리를 받은 편지함으로 바로 받아보세요.

[최신 소식 받기](https://gd-resources.gamedeveloper.com/free/w_gamf01/prgm.cgi)

추천 콘텐츠

* * *

원문: [https://www.gamedeveloper.com/design/deep-dive-how-gog-perfected-the-imperfect-with-the-re-release-of-alpha-protocol](https://www.gamedeveloper.com/design/deep-dive-how-gog-perfected-the-imperfect-with-the-re-release-of-alpha-protocol)