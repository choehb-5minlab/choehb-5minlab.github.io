---
title:  "RANKED: 작은 키보드 단축키의 꿈을 실현하는 4개의 작은 화면"

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

4분 읽기

![The words 'Tiny Screens' on a green background](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltb0bf33e8f94a52b4/66be03d99c9bc603a593330e/Screens_Header.png?width=1280&auto=webp&quality=95&format=jpg&disable=upscale "The words 'Tiny Screens' on a green background")

Game Developer 이미지 제공

[](https://www.linkedin.com/sharing/share-offsite/?url=https://www.gamedeveloper.com/design/ranked-four-tiny-screens-to-power-your-tiny-alt-ctrl-dreams)[](https://www.facebook.com/sharer/sharer.php?u=https://www.gamedeveloper.com/design/ranked-four-tiny-screens-to-power-your-tiny-alt-ctrl-dreams)[](https://www.twitter.com/intent/tweet?url=https://www.gamedeveloper.com/design/ranked-four-tiny-screens-to-power-your-tiny-alt-ctrl-dreams)[](https://www.gamedeveloper.com/cdn-cgi/l/email-protection#6c531f190e06090f18513e2d22272928564c2a03191e4c180502154c1f0f1e0909021f4c18034c1c031b091e4c1503191e4c180502154c0d00184c0f181e004c081e090d011f4a0d011c570e0308155125495e5c180403190b0418495e5c180409495e5c0a030000031b05020b495e5c0a1e0301495e5c2b0d0109495e5c28091a0900031c091e495e5c01050b0418495e5c050218091e091f18495e5c15031942495c28495c2d495c28495c2d495e5c3e2d22272928495f2d495e5c2a03191e495e5c18050215495e5c1f0f1e0909021f495e5c1803495e5c1c031b091e495e5c1503191e495e5c18050215495e5c0d0018495e5c0f181e00495e5c081e090d011f495c28495c2d0418181c1f495f2d495e2a495e2a1b1b1b420b0d010908091a0900031c091e420f0301495e2a08091f050b02495e2a1e0d02070908410a03191e4118050215411f0f1e0909021f411803411c031b091e411503191e4118050215410d0018410f181e0041081e090d011f)[](https://www.reddit.com/submit?url=https://www.gamedeveloper.com/design/ranked-four-tiny-screens-to-power-your-tiny-alt-ctrl-dreams&title=RANKED%3A%20Four%20tiny%20screens%20to%20power%20your%20tiny%20alt%20ctrl%20dreams)

어메이즈 셰필드에서 작은 스크린에 대한 작은 글을 쓰고 싶으신가요? 대안 컨트롤러 게임 디자이너 줄리아 마키빅이 바로 그런 이야기를 들려주었으니 운이 좋은 날입니다.

잠깐의 하이퍼 토크에서 자신이 가장 좋아하고 가장 경멸하는 작은 화면의 목록을 나열하며, 한 입 크기의 디스플레이를 통합한 비디오 게임을 개발하는 데 관심이 있는 다른 개발자들에게 몇 가지 지혜를 전하고자 했던 Makivic은 다음과 같이 말했습니다. 그녀는 작은 화면이 자신의 프로세스에서 "큰 부분"이 되었다고 설명합니다.

또한 비디오 게임을 염두에 두고 설계되지 않았기 때문에 때때로 엄청나게 실망스럽기도 합니다. "센서의 판독값이나 보드 자체에 대한 기타 정보를 표시하도록 설계되었습니다."라고 그녀는 설명합니다. "그래서 저는 이 성가신 작은 화면을 제가 원하는 기능을 수행하도록 조정하기 위해 노력해 왔습니다."

마키빅이 '가장 성가신' 1점부터 '가장 성가신' 10점까지 맞춤형 10점 척도로 평가한, 여러분이 결국 소중히 여기거나 싫어하게 될지도 모르는 작은 화면들을 소개합니다.

## Ardunio MEGA + Adafruit HX8357 (6/10)

"제가 처음 해본 프로젝트는 Arduino Mega의 HX8357 화면과 함께 Adafruit 라이브러리를 사용했는데, 이 프로젝트는 10점 만점에 6점을 주고 싶습니다. 작은 화면치고는 정말 큰 화면입니다. 5인치 정도 되죠."라고 Makivic은 말합니다. "하지만 투명 디스플레이에서는 작동하지 않습니다. 짜증나는 일이죠. 스프라이트와 이미지를 렌더링할 때도 전체 이미지를 한 번에 렌더링하지 않고 한 줄씩 렌더링합니다. \[...\] 실용성 측면에서 좋지 않죠. 또한 핀이 너무 많습니다. SPI나 I2C 프로토콜은 그렇게 많은 핀을 필요로 하지 않습니다."

## Picographics + Pico 디스플레이 팩 /터프티 2040(3/10)

"다음은 Pico 디스플레이가 포함된 Picographics 라이브러리입니다. 여기 계신 분들 중 마이크로컨트롤러용[Pimoroni 웹사이트의](https://shop.pimoroni.com) 팬이시라면 제가 무슨 말을 하는지 아실 겁니다. 그렇지 않다면 약간 틈새 시장입니다. 이 경험은 전체 강연에 영감을 주었는데, Pimoroni 웹사이트가 너무 친근하고 귀여워서 \[...\] '와우, 이걸로 JPEG를 표시하는 게 쉬울 거야'라고 생각하기 때문입니다. 아니죠."라고 마키빅은 말합니다.

"그들은 특정 형식의 JPEG가 있어야 하는 JPEG 코딩 라이브러리를 사용합니다. 하지만 그 형식이 무엇인지, 어떻게 정의해야 하는지 알려주지 않습니다. 제가 아는 것은 ProStudioPaint에서 JPEG를 사용할 때는 괜찮지만 Photoshop에서 JPEG를 사용할 때는 화를 낸다는 것뿐입니다. Adobe는 사악한 회사니까 그 말이 맞을 수도 있습니다."

## Adafruit GFX 비트맵 - ST7789 (5/10)

"다음은 ST7789의 Adafruit GFX 및 비트맵입니다. 5/10점입니다. ST7789가 작다는 점이 마음에 들었습니다. 귀엽기도 하고요. 가격은 비싸지만 동그란 모양도 있어서 멋지죠. 또한 Adafruit는 좋은 설명서를 제공합니다. 원하는 것을 얻기 위해 무엇을 해야 하는지 알려줍니다. 훌륭하죠. 그 점이 큰 장점입니다."라고 Makivic은 말합니다.

"하지만 이 화면에서 사용해야 하는 한 가지는 비트맵입니다. 이 작업을 하려면 비트맵이 무엇인지 배워야 했습니다. 비트맵은 이미지를 나타내는 배열입니다. 배열의 각 값은 이미지의 특정 픽셀을 나타냅니다. 따라서 비트맵을 그리드로 나눈 다음 게임에서 비트맵의 해당 부분을 언제 사용할지 확인해야 합니다.

"그런 픽셀 수준에서 이미지를 조작하는 것은 멋진 일입니다. 하지만 더 쉬운 방법이 있을지도 모르죠. 그리고 다른 모든 화면과 마찬가지로 비트맵도 투명할 수 없습니다. 따라서 흰색 배경이 게임 배경과 일치해야 하는데, 이는 모두에게 큰 번거로움입니다. 또한 비트맵의 크기, 너비, 높이도 알아야 합니다. 이 작업을 하려면 수학을 해야 하는데, 왜 그럴까요? 또한 너무 많은 비트맵을 동시에 사용하려고 하면 문제가 생깁니다."

## ESP32 + ILI9341, ST7789, GC9A01 (8/10)

"마지막으로 가장 좋은 점으로 넘어가고 싶습니다. 투명도를 사용할 수 없는 암흑기를 벗어나 이미지에 투명도를 사용할 수 있는 현대에 들어섰습니다. 저는 ILI9341, ST7789, GC9A01을 비롯한 다양한 스크린에 ESP32 마이크로컨트롤러를 사용하고 있습니다."라고 Makivic은 말합니다.

"솔직히 정말 훌륭합니다. 사용하기 매우 쉬워서 추천하고 싶어요. 유일한 단점은 초급자 풀에서 벗어나 중급자 풀로 뛰어들어야 한다는 점입니다. ESP32는 직관적이지 않을 수도 있지만 그렇게 나쁘지는 않아요. 그리고 저는 매우 저렴하고 원형인 GC9A01 화면을 사용할 수 있습니다."

[더 많은 AMAZE 셰필드 소식을 보려면 여기를 클릭하세요.](https://www.gamedeveloper.com/keyword/amaze-sheffield)

자세히 읽어보세요:

[AMAZE 셰필드톱](https://www.gamedeveloper.com/keyword/amaze-sheffield)[스토리](https://www.gamedeveloper.com/keyword/top-stories)

[](https://www.linkedin.com/sharing/share-offsite/?url=https://www.gamedeveloper.com/design/ranked-four-tiny-screens-to-power-your-tiny-alt-ctrl-dreams)[](https://www.facebook.com/sharer/sharer.php?u=https://www.gamedeveloper.com/design/ranked-four-tiny-screens-to-power-your-tiny-alt-ctrl-dreams)[](https://www.twitter.com/intent/tweet?url=https://www.gamedeveloper.com/design/ranked-four-tiny-screens-to-power-your-tiny-alt-ctrl-dreams)[](https://www.gamedeveloper.com/cdn-cgi/l/email-protection#98a7ebedfaf2fdfbeca5cad9d6d3dddca2b8def7edeab8ecf1f6e1b8ebfbeafdfdf6ebb8ecf7b8e8f7effdeab8e1f7edeab8ecf1f6e1b8f9f4ecb8fbeceaf4b8fceafdf9f5ebbef9f5e8a3faf7fce1a5d1bdaaa8ecf0f7edfff0ecbdaaa8ecf0fdbdaaa8fef7f4f4f7eff1f6ffbdaaa8feeaf7f5bdaaa8dff9f5fdbdaaa8dcfdeefdf4f7e8fdeabdaaa8f5f1fff0ecbdaaa8f1f6ecfdeafdebecbdaaa8e1f7edb6bda8dcbda8d9bda8dcbda8d9bdaaa8cad9d6d3dddcbdabd9bdaaa8def7edeabdaaa8ecf1f6e1bdaaa8ebfbeafdfdf6ebbdaaa8ecf7bdaaa8e8f7effdeabdaaa8e1f7edeabdaaa8ecf1f6e1bdaaa8f9f4ecbdaaa8fbeceaf4bdaaa8fceafdf9f5ebbda8dcbda8d9f0ecece8ebbdabd9bdaadebdaadeefefefb6fff9f5fdfcfdeefdf4f7e8fdeab6fbf7f5bdaadefcfdebf1fff6bdaadeeaf9f6f3fdfcb5fef7edeab5ecf1f6e1b5ebfbeafdfdf6ebb5ecf7b5e8f7effdeab5e1f7edeab5ecf1f6e1b5f9f4ecb5fbeceaf4b5fceafdf9f5eb)[](https://www.reddit.com/submit?url=https://www.gamedeveloper.com/design/ranked-four-tiny-screens-to-power-your-tiny-alt-ctrl-dreams&title=RANKED%3A%20Four%20tiny%20screens%20to%20power%20your%20tiny%20alt%20ctrl%20dreams)

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

원문: [https://www.gamedeveloper.com/design/ranked-four-tiny-screens-to-power-your-tiny-alt-ctrl-dreams](https://www.gamedeveloper.com/design/ranked-four-tiny-screens-to-power-your-tiny-alt-ctrl-dreams)