---
title:  "VR용 제스처 주문 캐스팅 시스템 구현하기"

categories:
  - 번역
  
tags:
  - Game Developer
toc: true
toc_sticky: true
 
date: 2024-08-19
last_modified_at: 2024-08-19
---
[![Picture of Edward McNeill](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt1cb9265591310a0b/65088b4ae874592feee571e6/Game_Developer_G_Logo_RGB.png?width=100&auto=webp&quality=80&disable=upscale "Picture of Edward McNeill")](https://www.gamedeveloper.com/author/edward-mcneill)

[에드워드 맥닐](https://www.gamedeveloper.com/author/edward-mcneill), 블로거

8월 19, 2024

6 분 읽기

![](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt5f3ab386e2949946/66be20a87f80456e656fb56c/Header_(1).png?width=1280&auto=webp&quality=95&format=jpg&disable=upscale)

[](https://www.linkedin.com/sharing/share-offsite/?url=https://www.gamedeveloper.com/design/conjuring-a-gestural-spellcasting-system-for-vr)[](https://www.facebook.com/sharer/sharer.php?u=https://www.gamedeveloper.com/design/conjuring-a-gestural-spellcasting-system-for-vr)[](https://www.twitter.com/intent/tweet?url=https://www.gamedeveloper.com/design/conjuring-a-gestural-spellcasting-system-for-vr)[](https://www.gamedeveloper.com/cdn-cgi/l/email-protection#053a7670676f60667138466a6b6f70776c6b622564256260767170776469257675606969666476716c6b6225767c7671606825636a77255357236468753e676a617c384c203735716d6a70626d71203735716d60203735636a69696a726c6b6220373563776a682037354264686020373541607360696a756077203735686c626d712037356c6b7160776076712037357c6a702b203541203544203541203544203735466a6b6f70776c6b622037356420373562607671707764692037357675606969666476716c6b62203735767c76716068203735636a7720373553572035412035446d717175762036442037432037437272722b6264686061607360696a7560772b666a682037436160766c626b203743666a6b6f70776c6b622864286260767170776469287675606969666476716c6b6228767c7671606828636a77287377)[](https://www.reddit.com/submit?url=https://www.gamedeveloper.com/design/conjuring-a-gestural-spellcasting-system-for-vr&title=Conjuring%20a%20gestural%20spellcasting%20system%20for%20VR)

마법사가 된다는 것은어떤 느낌일까요 ?

제가 VR 협동 액션 로그라이트인 [아이언스트라이크의](https://www.ironstrikegame.com/)프로토타입을 제작하기 시작했을 때 가장 먼저 생각한 것이 바로 이 점이었습니다 . 아이언스트라이크의 전작인 [아이언라이트의](https://www.ironlightsgame.com/) 플레이어들이 마법을 추가해 달라는 요청이 많았기 때문에 처음부터 일종의 주문 시전 시스템을 포함하고 싶다는 생각을 했죠. 하지만 단순히 미화된 메뉴에서 주문을 선택하는 것만으로는 부족했습니다. 방사형 메뉴나 원스텝 제스처를 뛰어넘어 VR의 진정한 장점을 살린 무언가를 디자인하고 싶었습니다.

가장 중요한 것은 실력에대한 보상을 제공하는 무언가를 원했습니다 .

제 영감은 꽤 쉽게 추적할 수 있습니다. 전 괴짜거든요. 어렸을 때 싸구려 판타지 책을 많이 읽었죠. 그 책에 나오는 마법사들이 멋있었던 이유는 단순히 불덩이를 던질 수 있다는 것 때문이 아니었어요. 그들은 복잡한 제스처를 연습하고 신비로운 주문을 외우면서 복잡한 에너지를 조작하는 비전술의 숙련된 전문가였기 때문이었죠. (그들도 괴짜들이었죠!)

그래서 저는 마법 시스템을 만들고 싶었습니다:

*   VR 모션 컨트롤을 최대한 활용
    
*   개념적으로 간단하고 초보자도 전투에서 사용할 수 있습니다.
    
*   실력을 연마한 숙련된 플레이어에게 보상 제공
    
*   점프, 회전, 빠른 이동 시에도 사용 가능
    
*   멋진 펄프 판타지 주문술사가 된 듯한 느낌
    

저는 아주 다른 두 가지 접근 방식을 시도해 보았습니다. 스포일러: 둘 다 실패했습니다.

## 실패한 접근법 #1: 룬 추적하기

저는 공중에서 선을 그리는 간단한 아이디어로 시작했습니다.

![Mockup1.png](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt6ae02d4a7f400d13/66be20b7c4fd759372717ce2/Mockup1.png?width=700&auto=webp&quality=80&disable=upscale "Mockup1.png")

(이전 프로토타입을 저장하지 못해서 여기 모형이 있습니다).

여기에는 몇 가지 멋진 기능이 있습니다. 아주 간단한 선(예: X자 그리기)부터 매우 복잡한 선(복잡한 룬)까지 모든 종류의 모양으로 선이 꼬이게 만들 수 있습니다. 선을 멋진 3D 모양으로 만들 수도 있습니다. 양손에 하나씩 두 개의 선이 있을 수도 있습니다!

더 좋은 방법은 플레이어에게 복잡한 경로 전체를 보여주지 않고 추적해야 할 선의 \*다음 부분\*만 보여준다면 어떨까요? 이렇게 하면 주문 전체를 외운 숙련된 플레이어는 서둘러서 따라갈 수 있고, 초보 플레이어는 주문을 외울 때까지 조금씩 계속 따라갈 수 있습니다!

솔직히 저는 이 아이디어가 마음에 들었습니다. 플레이어가 복잡하고 복잡한 제스처로 손을 흔들면서 구조물이 거의 보이지 않을 정도로 빠르게 마법의 에너지를 모아 적을 향해 날려버리는 장면을 상상해 보았어요.

멋지네요! 하지만 플레이 테스트 도중 문제가 발생했습니다.

번개처럼 빠른 손동작과 정확한 선 치수를 결합하는 데 문제가 있었습니다. 주문을 빠르게 시전하려고 할 때마다 0.1인치 차이로 선을 놓치는 일이 반복되어, 놓친 구간을 다시 돌아가서 추적해야 했고, 1초 후에 다시 선을 놓치는 일이 반복되었습니다. 이는 매우 실망스러웠고 경험이 쌓여도 개선되지 않는 것 같았습니다. 물론 어느 정도는 '기술적인 문제'일 수도 있겠지만, 실제로이렇게 불편하게느껴진다면 여전히 문제였습니다 .

처음에는 구현을 미세하게 조정하면 이 문제를 해결할 수 있다고 생각했습니다. 그래서 수많은 변형을 시도했습니다. 예를 들어 주문 줄에서 날카로운 모서리를 제거하면 어떨까요? 아니면 추적하는 동안 필요한 정밀도를 동적으로 낮추면 어떨까요? 아니면 추적 감지 알고리즘을 수십 가지 다른 방식으로 조정하면 어떨까요?

몇 번은 빠른 주문 캐스팅을 실현하는 데 성공했습니다! 하지만 여기에는 시스템을 너무 관대하게 만들었기 때문에 가장 좋은 전략은 손을 거칠게 휘두르는 것이었습니다. 우리가 목표로 했던 '엘리트 마법사'의 분위기와는 정반대였죠.

## 실패한 접근 방식 #2: 방향 시퀀스

복잡한 모양의 선 추적은 잊어버리세요. 전체 주문이 일련의 방향 스와이프 동작으로 이루어진다면 어떨까요? 지팡이를 위로, 아래로, 대각선으로, U-U-D-D-L-R-L-R로 움직이면 불덩이가 만들어집니다!

![Mockup2.png](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt7494862efed8fc72/66be20c9a94f8160b3b2e076/Mockup2.png?width=700&auto=webp&quality=80&disable=upscale "Mockup2.png")

이보다 더 간단할 수는 없습니다! 그리고 암기와 숙련된 실행에 대한 보상을 받을 수 있는 잠재력이 있었습니다. 하지만 몇 가지 문제가 있었습니다. 우선, 가능한 한 빨리 빠르게 원을 그리는(즉, 모든 방향을 타격하는) 방식으로 주문을 시전할 수 있습니다. (이 문제는 여러 가지 방법으로 완화할 수 있지만 다시 복잡해지기 시작합니다.) 또 다른 문제는 이 시스템이 공백을 의미 있게 사용하지 않는다는 점입니다. 주문을 외운다기보다는 코드를 입력하는 것처럼 느껴집니다. 마법사처럼 느껴지지 않아요.

이 기능을 구현할 수는 있지만 저는 이 아이디어가 마음에 들지 않았습니다. 하지만 다행히도 이 아이디어가 실제로 작동하는 메커니즘에 영감을 주었습니다:

## 바로 합성입니다: 라인 크로싱

위의 두 가지 접근 방식을 결합하면 완벽한 메카닉을 만들 수 있다는 것이 밝혀졌습니다! 그런 셈이죠!

주어진 방향으로 스와이프하는 것보다 더 엄격하지만, 경로의 특정 지점에 도달하는 것보다 더 관대한 메카닉이 필요했습니다. 그렇다면 두 가지 아이디어를 합쳐서 플레이어가 특정 지점 근처에서주어진 방향으로 스와이프하도록 하는 것은 어떨까요?

구현하기 쉬울 것 같네요! 주문을 일련의 선분으로 정의하고 플레이어의 모션이 각 선분과 올바른 방향으로 교차하도록 하면 됩니다. 2D(선분과 플레이어의 손 동작 벡터를 모두 2D 평면에 투영하여) 또는 3D(플레이어에게 손에서 뻗은 긴 지팡이/광선을 주고 선분에 닿는 시점을 감지하여)로 '교차점'을 정의할 수 있습니다.

그리고... 작동합니다!

새로운 플레이어에게 쉽게 설명하고 가르칠 수 있습니다:

다양한 복잡한 제스처를 수용하도록 쉽게 확장할 수 있습니다:

연습을 통해 복잡한 주문도 빠르고 원활하게 시전할 수 있습니다:

선분의 길이를 조정하여 어느 지점에서 얼마나 정확한 동작이 필요한지 제어할 수 있지만, 무의식적으로 손을 휘두르면 주문을 효과적으로 시전할 수 없습니다.

이 시스템은 플레이어가 주문을 외우고 빠르게 시전하는 신체 기술을 연습하도록 장려합니다. 다음은 아이언스트라이크 플레이어가 전투에서 자신의 주문 기술을 뽐내기 위해 방금 녹화한 영상입니다:

이 주문 시전 시스템은 지금까지 큰 성공을 거두고 있습니다. 주문 시전자는 아이언스트라이크에서 플레이어의 약 4분의 1을 차지하며, 주로 지원 또는 포병 역할을 담당합니다. 그리고 복잡한 제스처도 쉽게 만들 수 있기 때문에 더 많은 주문으로 시스템을 확장할 수 있는 여지가 많습니다.

이 시스템을 돌아보면 핵심 요소(특정 방향으로 스와이프해야 함/플레이어 앞의 특정 위치)가 VR의 가장 큰 히트작 중 하나인 비트 세이버의 그것과 비슷하다는 점이 흥미롭습니다. 의도한 것은 아니지만, 이런 융합적인 진화를 통해 다른 게임 메커니즘에 유용한 요소가 될 수 있을 것 같다는 생각이 들었습니다. 앞으로 비슷한 접근 방식을 사용하는 다른 시스템에 대해 알아보고 싶어요!

\-[@E\_McNeill](https://twitter.com/e_mcneill)

자세히 읽어보세요:

[블로그추천](https://www.gamedeveloper.com/keyword/blogs)[블로그톱](https://www.gamedeveloper.com/keyword/featured-blogs)[스토리](https://www.gamedeveloper.com/keyword/top-stories)

[](https://www.linkedin.com/sharing/share-offsite/?url=https://www.gamedeveloper.com/design/conjuring-a-gestural-spellcasting-system-for-vr)[](https://www.facebook.com/sharer/sharer.php?u=https://www.gamedeveloper.com/design/conjuring-a-gestural-spellcasting-system-for-vr)[](https://www.twitter.com/intent/tweet?url=https://www.gamedeveloper.com/design/conjuring-a-gestural-spellcasting-system-for-vr)[](https://www.gamedeveloper.com/cdn-cgi/l/email-protection#300f4345525a5553440d735f5e5a4542595e57105110575543444542515c104340555c5c53514344595e571043494344555d10565f4210666216515d400b525f54490d7915020044585f45575844150200445855150200565f5c5c5f47595e5715020056425f5d15020077515d55150200745546555c5f4055421502005d59575844150200595e445542554344150200495f451e150074150071150074150071150200735f5e5a4542595e5715020051150200575543444542515c1502004340555c5c53514344595e5715020043494344555d150200565f42150200666215007415007158444440431503711502761502764747471e57515d55545546555c5f4055421e535f5d15027654554359575e150276535f5e5a4542595e571d511d575543444542515c1d4340555c5c53514344595e571d43494344555d1d565f421d4642)[](https://www.reddit.com/submit?url=https://www.gamedeveloper.com/design/conjuring-a-gestural-spellcasting-system-for-vr&title=Conjuring%20a%20gestural%20spellcasting%20system%20for%20VR)

## 저자 소개

[![Edward McNeill](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt1cb9265591310a0b/65088b4ae874592feee571e6/Game_Developer_G_Logo_RGB.png?width=400&auto=webp&quality=80&disable=upscale "Edward McNeill")](https://www.gamedeveloper.com/author/edward-mcneill)

[

에드워드 맥닐

](https://www.gamedeveloper.com/author/edward-mcneill)

Blogger

[에드워드 맥닐의 더보기](https://www.gamedeveloper.com/author/edward-mcneill)

게임 개발자의 일일 뉴스, 개발자 블로그, 스토리를 받은 편지함으로 바로 받아보세요.

[최신 소식 받기](https://gd-resources.gamedeveloper.com/free/w_gamf01/prgm.cgi)

추천 콘텐츠

* * *

원문: [https://www.gamedeveloper.com/design/conjuring-a-gestural-spellcasting-system-for-vr](https://www.gamedeveloper.com/design/conjuring-a-gestural-spellcasting-system-for-vr)