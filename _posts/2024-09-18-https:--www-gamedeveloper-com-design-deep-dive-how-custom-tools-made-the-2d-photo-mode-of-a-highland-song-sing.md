---
title:  "심층 분석: 커스텀 툴로 '하이랜드 송'의 2D 사진 모드를 노래로 만든 방법"

categories:
  - 번역
  
tags:
  - Game Developer
toc: true
toc_sticky: true
 
date: 2024-09-18
last_modified_at: 2024-09-18
---
[![Picture of Joseph Humfrey](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt9e8069ea34197b4d/650881a8764ee01ce4913471/Joseph_Humfrey.jpg?width=100&auto=webp&quality=80&disable=upscale "Picture of Joseph Humfrey")](https://www.gamedeveloper.com/author/joseph-humfrey)

[조셉 험프리](https://www.gamedeveloper.com/author/joseph-humfrey), 블로거

9월 17일, 2024

7 분 읽기

![](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt537968df6feb2fdf/66c8fa2c6a0fb360944ed911/Picture14.jpg?width=1280&auto=webp&quality=95&format=jpg&disable=upscale)

Inkle 이미지 제공.

[](https://www.linkedin.com/sharing/share-offsite/?url=https://www.gamedeveloper.com/design/deep-dive-how-custom-tools-made-the-2d-photo-mode-of-a-highland-song-sing)[](https://www.facebook.com/sharer/sharer.php?u=https://www.gamedeveloper.com/design/deep-dive-how-custom-tools-made-the-2d-photo-mode-of-a-highland-song-sing)[](https://www.twitter.com/intent/tweet?url=https://www.gamedeveloper.com/design/deep-dive-how-custom-tools-made-the-2d-photo-mode-of-a-highland-song-sing)[](https://www.gamedeveloper.com/cdn-cgi/l/email-protection#3b04484e59515e584f067f5e5e4b1b7f524d5e011b73544c1b584e484f54561b4f545457481b565a5f5e1b4f535e1b097f1b4b53544f541b56545f5e1b545d1b7a1b73525c53575a555f1b6854555c1b4852555c1d5a564b0059545f4206721e090b4f53544e5c534f1e090b4f535e1e090b5d545757544c52555c1e090b5d4954561e090b7c5a565e1e090b7f5e4d5e57544b5e491e090b56525c534f1e090b52554f5e495e484f1e090b42544e151e0b7f1e0b7a1e0b7f1e0b7a1e090b7f5e5e4b1e090b7f524d5e1e087a1e090b73544c1e090b584e484f54561e090b4f545457481e090b565a5f5e1e090b4f535e1e090b097f1e090b4b53544f541e090b56545f5e1e090b545d1e090b7a1e090b73525c53575a555f1e090b6854555c1e090b4852555c1e0b7f1e0b7a534f4f4b481e087a1e097d1e097d4c4c4c155c5a565e5f5e4d5e57544b5e49155854561e097d5f5e48525c551e097d5f5e5e4b165f524d5e1653544c16584e484f5456164f5454574816565a5f5e164f535e16095f164b53544f541656545f5e16545d165a1653525c53575a555f164854555c164852555c)[](https://www.reddit.com/submit?url=https://www.gamedeveloper.com/design/deep-dive-how-custom-tools-made-the-2d-photo-mode-of-a-highland-song-sing&title=Deep%20Dive%3A%20How%20custom%20tools%20made%20the%202D%20photo%20mode%20of%20A%20Highland%20Song%20sing)

게임 개발자 심층 분석은 비디오 게임의 특정 디자인, 아트 또는 기술적 특징을 조명하여 단순해 보이는 근본적인 디자인 결정이 실제로는 전혀 단순하지 않다는 것을 보여주기 위해 진행 중인 시리즈입니다.

이전 편에서는 [블러드리스의](https://www.gamedeveloper.com/art/deep-dive-behind-the-starkly-stylish-art-direction-of-bloodless)[스타일리시한 아트 디렉션](https://www.gamedeveloper.com/art/deep-dive-behind-the-starkly-stylish-art-direction-of-bloodless) , [GOG가](https://www.gamedeveloper.com/design/deep-dive-how-gog-perfected-the-imperfect-with-the-re-release-of-alpha-protocol) [알파 프로토콜을](https://www.gamedeveloper.com/design/deep-dive-how-gog-perfected-the-imperfect-with-the-re-release-of-alpha-protocol) [최신 디지털 버전으로](https://www.gamedeveloper.com/design/deep-dive-how-gog-perfected-the-imperfect-with-the-re-release-of-alpha-protocol)[업데이트한 방법](https://www.gamedeveloper.com/design/deep-dive-how-gog-perfected-the-imperfect-with-the-re-release-of-alpha-protocol) , [이스타르 게임즈가](https://www.gamedeveloper.com/design/deep-dive-designing-a-new-dwarf-race-in-the-last-spell) [더 라스트 스펠에서](https://www.gamedeveloper.com/design/deep-dive-designing-a-new-dwarf-race-in-the-last-spell)[새로운 드워프 종족의 디자인에 접근한 방법](https://www.gamedeveloper.com/design/deep-dive-designing-a-new-dwarf-race-in-the-last-spell) 등의 주제를 다뤘습니다 .

이번 에피소드에서는 inkle의 조셉 험프리가 2D 게임에서 어떻게 플레이어에게 역동적인 포토 모드를 제공할 수 있었는지 설명합니다.

멋진 게임에서 고퀄리티의 사진 모드를 좋아하지 않는 사람이 있을까요? 초현실적인 렌더링으로 플레이어가 고급 DSLR과 같은 가상 카메라를 설정하고 노출 설정을 조정하고 전문가처럼 초점을 맞출 수 있는 3D 게임의 영역이 대부분이었죠. 하지만 저희는 2D 인디 게임인 [A Highland Song에](https://store.steampowered.com/app/1240060/A_Highland_Song/)사진 모드를 추가하기로 결정했습니다 . 2D 게임에 사진 모드를 추가하는 것이 의미가 있을까요? 놀랍게도 가능합니다! 하지만 플레이어에게 단순한 스크린샷 이상의 것을 만들 수 있는 도구가 제공되어야 합니다.

잉크에서 저는 다양한 프로젝트의 아트 디렉터로서 많은 책임을 맡고 있습니다. 80일을만들 때부터 저는 테일러 라모스와 토니 저우의 유튜브 시리즈 ' 모든 프레임을 그림으로'로 유명해진 '모든 프레임을 그림으로'라는 콘셉트를 목표로 삼았습니다 . 이 아이디어는 영화 촬영이 매우 아름답기 때문에 영화의 모든 프레임을 가져와 벽에 걸 수 있다는 것입니다. 80일 동안에는 텍스트가 주를 이루는 게임임에도 불구하고 모든 순간이 1930년대 아르데코 여행 포스터처럼 보이길 원했습니다. ( 80 Days와 동시대 게임인 모뉴먼트 밸리(Monument Valley)의 제작진도 비슷한 생각을 하고 있었습니다. 그들은 게임의 모든 레벨이 벽에 걸면 예술 작품처럼 멋지게 보인다는 아이디어가 마음에 들었습니다).

관련 내용:[하이랜드 송은 각 모험을 나만의 것으로 만들기 위해 스토리를 제작합니다](https://www.gamedeveloper.com/design/a-highland-song-crafts-its-story-to-make-each-adventure-your-own).

![80 Days Screenshot](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt72bd6d2f821f9a19/66c8fb0105ce3f6997dd05e4/Picture15.jpg?width=700&auto=webp&quality=80&disable=upscale "80 Days Screenshot")

80 Days의 스크린샷. Inkle 이미지 제공.

사진 모드는 여기서 한 걸음 더 나아가 플레이어가 사진의 구도와 구도에 창의력을 발휘할 수 있는 모드입니다. 모뉴먼트 밸리는 본질적으로 아름답지만(실제로 스냅샷 버튼이 내장되어 있습니다), 포토 모드에서는 플레이어가 직접 아름다운 순간을 찾아내야 합니다. 저는 사진 모드가 3D 게임에만 한정된 이유는 더 아름답기 때문이 아니라 6가지 자유도가 표현의 자유를 제공하는 핵심 요소이기 때문이라고 주장하고 싶습니다.

사진은 피사체를 직접 제어하지 않고도 아이디어를 전달할 수 있다는 점에서 매력이 있습니다. 사진을 정렬하여 상반되는 사물을 나란히 배치하거나 2차원 프레임에 움직임의 느낌을 연출할 수 있습니다. 광활한 하늘 아래 넓은 바다 위의 작은 배, 고층 빌딩 사이의 밀폐된 공간, 참새를 향해 발톱을 닫기 직전의 매를 포착하는 등 공간적 관계를 이용해 이야기를 전달할 수 있습니다. 사진은 시간과 공간의 순간을 선택하고, 보는 사람이 보여주고 싶은 것을 볼 수 있는 관점을 찾아 평범한 것에서도 아름다움을 찾아내는 것입니다. 이것이 바로 하이랜드 송에서플레이어가 할 수 있는 일입니다 . 플레이어가 직접 발을 움직이지 않는 한 산이 어디에 있는지, 어떤 유적이 근처에 있는지 제어할 수 없습니다.

관련:[분당 120비트까지 개발하기: _하이랜드 송_ Q&A](https://www.gamedeveloper.com/design/programming-to-120-beats-per-minute-a-highland-song-q-a)

![](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt3261861883afe675/66c8fb20f3ae86ab82303587/Picture16.jpg?width=700&auto=webp&quality=80&disable=upscale)

Unity 에디터의 스택 하이랜드 레이어. Inkle 이미지 제공.

하이랜드 송의비결은 완전한 2D가 아니라는 점입니다. 유니티의 자체 커스텀 툴을 사용하여 수만 개의 평면 레이어를 Z축으로 수 킬로미터에 걸쳐 쌓아 올려 3D로 제작했습니다. 게임을 시작하면 배경에 있는 산은 실제로 게임 내 모든 미래 레벨이며, 플레이어의 목표인 바닷가 등대까지 이어집니다. 수천 개의 평평한 레이어 중 대부분은 횡단이 가능하기 때문에 2D 게임의 "보이면 갈 수 있다"는 특징이 있습니다! 주인공 모이라가 각 레이어가 닿는 곳이면 어디든 이동할 수 있습니다. (저는 이것을 2.5D라고 부르고 싶지만, 인터넷의 올바른 사람들로부터 2.5D는 2D 평면으로 움직임이 제한된 완전한 3D 예술로 엄격하게 정의된다는 말을 들었습니다. 그렇다면 "2.4D"라는 용어에 대해 우리의 주장을 걸까요?)

이 추가 차원을 통해 카메라를 더 풍부하게 배치할 수 있습니다. 플레이어에게 완전한 회전 제어권이 주어지지는 않지만, 카메라를 세 개의 축으로 자유롭게 움직일 수 있기 때문에 월드의 오브젝트를 정렬하고 프레임을 창의적으로 제어할 수 있습니다. 또한 모이라의 얼굴 클로즈업과 같이 게임 내 카메라가 자연스럽게 닿지 않는 위치로 카메라를 이동할 수도 있습니다.

![A Highland Song concept art.](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt78d37754a18cd324/66c8fb43e315a7221c1d3e7e/Picture17.jpg?width=700&auto=webp&quality=80&disable=upscale "A Highland Song concept art.")

하이랜드 송 콘셉트 아트. 폴 스콧 카나반 이미지 제공.

처음부터 사진 모드를 포함할 계획은 없었지만, 저희는 항상 회화적인 아트 스타일을 지향하여 스크린샷을 크레이그 멀린스 같은 아티스트의 디지털 콘셉트 아트처럼 보이게 만들었습니다. 저희는 뛰어난 폴 스콧 카나반과 협력하여 풀잎, 세밀한 바위, 인상주의적인 질감의 물감 등 다양한 스케일의 그림 조각을 여러 겹으로 쌓아 전체적인 아트 디렉션을 개발했습니다. 이러한 조각을 다양한 스케일로 렌더링하면 전체적인 스타일과 개별 브러시 스트로크의 가시성을 유지하면서 카메라를 극적으로 안팎으로 움직일 수 있었습니다.

잉클은 게임에서 낮과 밤의 주기를 잘 표현하는 것을 좋아하는데, 스코틀랜드의 산을 표현할 때 특히 이 점이 중요했습니다. 스코틀랜드 고원의 아름다움은 시시각각 변하는 빛과 악명 높은 변덕스러운 날씨에서 비롯됩니다. 따라서 유니티의 커스텀 그래픽 기술의 핵심 기능은 시간대, 안개, 구름, 비와 눈 등 모든 가능한 변수에 대응할 수 있어야 했습니다. 예를 들어, 카메라 거리에 따라 여러 컬러 스톱을 블렌딩한 후 시간대와 날씨 유형에 따라 그라데이션을 보간하는 커스텀 안개 알고리즘을 사용했습니다. 물리 기반 렌더링이 아니라 모든 조건에서 컬러 팔레트를 직접 제작할 수 있도록 아티스트가 완전히 주도하는 방식입니다.

![](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt2374b61cbf559809/66c8fb64b23b30dc0e4bf724/Picture18.jpg?width=700&auto=webp&quality=80&disable=upscale)

하이랜드 송에 사용된 컬러 팔레트. Inkle 이미지 제공.

이를 반영하여 플레이어가 직접 제어할 수 있는 포토 모드를 통해 플레이어는 게임의 내러티브 현실에서 벗어나 모든 조명과 날씨 변수로 신이 되어 다양한 시각 효과를 구현할 수 있습니다. 또한 플레이어는 최종 이미지에서 노출과 색조를 기본적으로 조정할 수 있습니다.

이러한 모든 제어 기능을 통해 플레이어는 단순한 스크린샷을 찍는 것 이상의 상당한 창의적 자유를 누릴 수 있습니다. 특히 자랑스러운 기능 중 하나는 주인공인 모이라의 대사를 선택할 수 있는 기능입니다. 이 게임은 모이라가 과거에 했던 10개의 대사를 기억하여 플레이어가 그 대사를 반복할 수 있도록 합니다. 모이라의 입에 직접 말을 넣을 수는 없지만, 과거 대사를 바탕으로 특정 순간에 모이라가 하는 말을 바꿀 수 있습니다. 이를 통해 플레이어는 캐릭터의 핵심 목소리를 유지하면서 흥미로운 제한을 통해 약간의 창의적인 제어를 할 수 있습니다. 예를 들어, 몇 분 전에 넘어진 후 "세상에나!"라고 말했다면, 산 정상에서 거대한 독수리가 그녀를 향해 급습하는 대사를 재사용하여 게임에서 제공하는 요소로 자신만의 구도를 만들 수 있습니다.

![](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt1dd2b01eb3c72ceb/66c8fb8dd6db0c86250de60d/Picture19.jpg?width=700&auto=webp&quality=80&disable=upscale)

Inkle 이미지 제공.

대부분의 게임은 카메라 움직임에도 이러한 창의적인 제약을 적용하는데, 하이랜드 송도 예외는 아닙니다. 모이라를 프레임 안에 유지하고 플레이어가 게임의 비하인드 마법을 몰래 엿보는 것을 방지하기 위해 카메라 움직임을 제한했습니다. 플레이어가 레벨을 진행하면서 레벨을 언로드하기 때문에 카메라가 너무 뒤로 이동하지 않도록 하여 당황스러운 노출을 피해야 했습니다.

출시 몇 주 전에포토 모드를 하이랜드 송에도입하게 되어 정말 기쁘게 생각합니다 . 모든 2D 게임에 적합하지는 않지만, 창의력을 충분히 발휘할 수 있다면 매우 유용할 수 있습니다. 팬들이 자신의 작품을 소셜 미디어에 공유하여 새로운 잠재 고객에게 게임을 소개할 수 있는 또 다른 즐거움을 선사할 수 있습니다.

자세히 알아보기:

[심층](https://www.gamedeveloper.com/keyword/deep-dives)[분석기능탑](https://www.gamedeveloper.com/keyword/features)[스토리](https://www.gamedeveloper.com/keyword/top-stories)

[](https://www.linkedin.com/sharing/share-offsite/?url=https://www.gamedeveloper.com/design/deep-dive-how-custom-tools-made-the-2d-photo-mode-of-a-highland-song-sing)[](https://www.facebook.com/sharer/sharer.php?u=https://www.gamedeveloper.com/design/deep-dive-how-custom-tools-made-the-2d-photo-mode-of-a-highland-song-sing)[](https://www.twitter.com/intent/tweet?url=https://www.gamedeveloper.com/design/deep-dive-how-custom-tools-made-the-2d-photo-mode-of-a-highland-song-sing)[](https://www.gamedeveloper.com/cdn-cgi/l/email-protection#f0cf8385929a959384cdb4959580d0b4998695cad0b89f87d0938583849f9dd0849f9f9c83d09d919495d0849895d0c2b4d080989f849fd09d9f9495d09f96d0b1d0b89997989c919e94d0a39f9e97d083999e97d6919d80cb929f9489cdb9d5c2c084989f85979884d5c2c0849895d5c2c0969f9c9c9f87999e97d5c2c096829f9dd5c2c0b7919d95d5c2c0b49586959c9f809582d5c2c09d99979884d5c2c0999e849582958384d5c2c0899f85ded5c0b4d5c0b1d5c0b4d5c0b1d5c2c0b4959580d5c2c0b4998695d5c3b1d5c2c0b89f87d5c2c0938583849f9dd5c2c0849f9f9c83d5c2c09d919495d5c2c0849895d5c2c0c2b4d5c2c080989f849fd5c2c09d9f9495d5c2c09f96d5c2c0b1d5c2c0b89997989c919e94d5c2c0a39f9e97d5c2c083999e97d5c0b4d5c0b19884848083d5c3b1d5c2b6d5c2b6878787de97919d95949586959c9f809582de939f9dd5c2b694958399979ed5c2b694959580dd94998695dd989f87dd938583849f9ddd849f9f9c83dd9d919495dd849895ddc294dd80989f849fdd9d9f9495dd9f96dd91dd989997989c919e94dd839f9e97dd83999e97)[](https://www.reddit.com/submit?url=https://www.gamedeveloper.com/design/deep-dive-how-custom-tools-made-the-2d-photo-mode-of-a-highland-song-sing&title=Deep%20Dive%3A%20How%20custom%20tools%20made%20the%202D%20photo%20mode%20of%20A%20Highland%20Song%20sing)

## 저자 소개

[![Joseph Humfrey](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt9e8069ea34197b4d/650881a8764ee01ce4913471/Joseph_Humfrey.jpg?width=400&auto=webp&quality=80&disable=upscale "Joseph Humfrey")](https://www.gamedeveloper.com/author/joseph-humfrey)

[

조셉 험프리

](https://www.gamedeveloper.com/author/joseph-humfrey)

Blogger

[조셉 험프리의 더보기](https://www.gamedeveloper.com/author/joseph-humfrey)

게임 개발자의 일일 뉴스, 개발자 블로그, 이야기를 받은 편지함으로 바로 받아보세요.

[최신 소식 받기](https://gd-resources.gamedeveloper.com/free/w_gamf01/prgm.cgi)

추천 콘텐츠

* * *

원문: [https://www.gamedeveloper.com/design/deep-dive-how-custom-tools-made-the-2d-photo-mode-of-a-highland-song-sing](https://www.gamedeveloper.com/design/deep-dive-how-custom-tools-made-the-2d-photo-mode-of-a-highland-song-sing)