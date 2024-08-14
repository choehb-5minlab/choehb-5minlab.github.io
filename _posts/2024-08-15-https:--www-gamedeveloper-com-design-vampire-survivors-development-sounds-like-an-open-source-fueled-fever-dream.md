---
title:  "뱀파이어 서바이버 개발은 오픈 소스를 기반으로 한 열광적인 꿈처럼 들립니다."

categories:
  - 번역
  
tags:
  - Game Developer
toc: true
toc_sticky: true
 
date: 2024-08-15
last_modified_at: 2024-08-15
---
[![Picture of Bryant Francis](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt862ca995183d2fdf/650efe5138b21120135ae4ac/bryantcropped.jpg?width=100&auto=webp&quality=80&disable=upscale "Picture of Bryant Francis")](https://www.gamedeveloper.com/author/bryant-francis)

[브라이언트 프랜시스](https://www.gamedeveloper.com/author/bryant-francis), 수석 편집자

8월 14, 2024

3 분 읽기

![Key art for Vampire Survivors. A classic pale vampire glowers in front of a blood-red moon.](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt6cfb777200bb862f/66bcea7a0cad5d8f5c868a8a/vampiresurvivorsfeatured.jpg?width=1280&auto=webp&quality=95&format=jpg&disable=upscale "Key art for Vampire Survivors. A classic pale vampire glowers in front of a blood-red moon.")

폰클/미래의 친구들 이미지 제공.

[](https://www.linkedin.com/sharing/share-offsite/?url=https://www.gamedeveloper.com/design/vampire-survivors-development-sounds-like-an-open-source-fueled-fever-dream)[](https://www.facebook.com/sharer/sharer.php?u=https://www.gamedeveloper.com/design/vampire-survivors-development-sounds-like-an-open-source-fueled-fever-dream)[](https://www.twitter.com/intent/tweet?url=https://www.gamedeveloper.com/design/vampire-survivors-development-sounds-like-an-open-source-fueled-fever-dream)[](https://www.gamedeveloper.com/cdn-cgi/l/email-protection#f3cc80869199969087cea5929e839a8196d3a08681859a859c8180d3979685969f9c839e969d87d3809c869d9780d39f9a9896d3929dd39c83969dd3809c86819096de9586969f9697d39596859681d3978196929ed5929e83c8919c978acebad6c1c3879b9c86949b87d6c1c3879b96d6c1c3959c9f9f9c849a9d94d6c1c395819c9ed6c1c3b4929e96d6c1c3b79685969f9c839681d6c1c39e9a949b87d6c1c39a9d879681968087d6c1c38a9c86ddd6c3b7d6c3b2d6c3b7d6c3b2d6c1c3a5929e839a8196d6c1c3a08681859a859c8180d6c1c3979685969f9c839e969d87d6c1c3809c869d9780d6c1c39f9a9896d6c1c3929dd6c1c39c83969dd6c1c3809c86819096de9586969f9697d6c1c39596859681d6c1c3978196929ed6c3b7d6c3b29b87878380d6c0b2d6c1b5d6c1b5848484dd94929e96979685969f9c839681dd909c9ed6c1b59796809a949dd6c1b585929e839a8196de808681859a859c8180de979685969f9c839e969d87de809c869d9780de9f9a9896de929dde9c83969dde809c86819096de9586969f9697de9596859681de978196929e)[](https://www.reddit.com/submit?url=https://www.gamedeveloper.com/design/vampire-survivors-development-sounds-like-an-open-source-fueled-fever-dream&title=Vampire%20Survivors%20development%20sounds%20like%20an%20open%20source-fueled%20fever%20dream)

## 한눈에 보기

*   게임 인포머의 마지막 호에는 뱀파이어 서바이버 제작자 루카 갈란테의 게임 제작에 관한 인터뷰가 실렸습니다.
*   갈란테는 오픈 소스 툴과 무료 스프라이트 팩으로 가능해진 개발 주기에 대해 설명합니다.
*   게임의 혼란스럽고 열광적인 분위기는 마치 제작 과정에서 바로 나온 것 같은 느낌을 줍니다.

게임 인포머의 마지막 인쇄판에는 뱀파이어 서바이버의 제작자 루카 갈란테와의멋진 인터뷰가 실렸는데 , 정말 대단했습니다. 과거에도 수많은 "서바이벌" 게임을 탄생시킨 그의 깜짝 히트작에 대해 많은 인터뷰를 진행한 바 있는 갈란테는 Game Informer와의 인터뷰에서 게임에 생명을 불어넣은 도구와 기술에 대해 자세히 설명했습니다.

갈란테는 파오 유몰과의 인터뷰에서 도박 앱 프로그래밍 경력이 게임 디자인 전체에 영향을 미치지는 않았고 보물 상자를 여는 부분에만 영향을 미쳤다는 점, LEME의 모바일 게임 Magic Survival에서 처음 영감을 받았다는 점 등 개발 과정에서 [익숙한 이야기(](https://www.nme.com/features/vampire-survivors-creator-luca-galante-talks-quitting-his-job-to-fulfil-his-promise-3153107) ) [를](https://www.androidpolice.com/vampire-survivors-developer-interview/)들려주었지만게임 제작이 어떻게 가능했는지 알려주는 몇 가지 새로운 정보도 들려주었습니다.

예를 들어, 오픈 소스 툴과 무료 에셋의 확산은 갈란테가 직접 게임을 제작하는 여정을 시작하게 된 계기가 되었습니다. 갈란테는 특히 HTML5 오픈 소스 게임 엔진인 [Phaser를](https://phaser.io/)사용했으며 , 기본 엔진 에셋으로뱀파이어 서바이버의 기본을 구축했습니다 .

수백 개의 스프라이트가 화면에 쏟아져 나올 때 통제 불능 상태가 되는 이 게임의 불안정한 비주얼은 그가 캐슬바니아 테마의 스프라이트 팩을 가져왔을 때부터 이미 존재했습니다. 그는 게임 인포머와의 인터뷰에서 스프라이트가 "적절한 크기로 렌더링되지 않았다"고 말하며, 이러한 불완전함에 반했다고 합니다.

"모두 매우 혼란스럽고 지저분했습니다. 화면에는 거대한 사마귀와 바닥에 풀이 무성한 녹색이 많았죠."

## 오픈 소스 게임 엔진을 사용하면 적은 비용으로 많은 것을 할 수 있습니다.

갈란테는 플레이 가능한 캐릭터와 무기를 디자인하기 시작하면서 개발 프로세스에서 여전히 '가장 좋아하는 부분'인 디자인 작업을 시작했다고 합니다. 그는 자신의 디자인 접근 방식을 "용병"이라고 설명하며, 스프라이트 팩에서 개별 에셋을 가져와 캐릭터, 느낌, 일관성을 거의 고려하지 않고 즉석에서 공격 패턴을 코딩했다고 합니다.

이러한 "방법론"은 2023년, 게임을 열어본 그가 "알지 못하는" 캐릭터를 발견했을 때 이상한 방식으로 나타났습니다. 개발 중 언젠가 그는 "블랙아웃"(그의 표현)을 일으켜 잠들기 전에 캐릭터를 만들었다는 사실을 잊어버렸다고 합니다.

게임 개발 중 블랙아웃에 대한 이야기는 많은 개발자에게 긴장감과 과로의 기억을 떠올리게 할 수 있지만, 갈란테는 자신의 툴킷에 익숙해졌기 때문이라고 생각한 것 같습니다. "때로는 프로그래밍 언어, 게임 프레임워크 등 자신의 툴을 잘 아는 것에서 비롯되기도 합니다."

이야기는 가만히 서서 적을 쏟아붓는 능력을 가진 크리스마스 트리 캐릭터 페피노의 이야기로 마무리됩니다. 갈란테는 2022년 1월 7일, 유튜버 스플래터캣이 게임 리뷰를 올린 후 게임 매출이 폭발적으로 증가하고 있다는 친구의 메시지를 받고 크리스마스 트리에 경의를 표하기 위해 페피노를 만들었습니다.

갈란테에 따르면, 그는 나무를 철거하는 것을 잊고 영원히 그대로 두기로 결정했다고 합니다.

하지만 그뿐이 아닙니다. 페피노의 '가만히 서 있기' 기믹은 갈란테가 스스로 '움직이지 않기' 챌린지에 도전하는 플레이어를 보고 착안한 것입니다. 갈란테는 게임 인포머와의 인터뷰에서 사용하지 않는 소나무 스프라이트와 자신의 아파트에 여전히 서 있는 크리스마스 트리가 있었다고 말했습니다.

"이탈리아어로 페피노라는 이름은 기본적으로 소나무를 뜻합니다."라고 그는 이 매체에 말했습니다. "그래서 제 믿을 수 없을 정도로 멍청한 두뇌가 그 모든 것을 조합했습니다."

유몰과 갈란테의 나머지 인터뷰는 Game Informer 웹사이트를 통해 확인하실 수 있지만, 게임스톱이 매장을 폐쇄하고 온라인 아카이브를 삭제하기로 결정함에 따라 온라인에 게시되지 않았습니다.

이 인터뷰와 다른 멋진 이야기를 직접 읽어보시려면 Game Informer의 마지막 호를 직접 찾아보시기 바랍니다.

[](https://www.linkedin.com/sharing/share-offsite/?url=https://www.gamedeveloper.com/design/vampire-survivors-development-sounds-like-an-open-source-fueled-fever-dream)[](https://www.facebook.com/sharer/sharer.php?u=https://www.gamedeveloper.com/design/vampire-survivors-development-sounds-like-an-open-source-fueled-fever-dream)[](https://www.twitter.com/intent/tweet?url=https://www.gamedeveloper.com/design/vampire-survivors-development-sounds-like-an-open-source-fueled-fever-dream)[](https://www.gamedeveloper.com/cdn-cgi/l/email-protection#af90dcdacdc5caccdb92f9cec2dfc6ddca8ffcdaddd9c6d9c0dddc8fcbcad9cac3c0dfc2cac1db8fdcc0dac1cbdc8fc3c6c4ca8fcec18fc0dfcac18fdcc0daddccca82c9dacac3cacb8fc9cad9cadd8fcbddcacec289cec2df94cdc0cbd692e68a9d9fdbc7c0dac8c7db8a9d9fdbc7ca8a9d9fc9c0c3c3c0d8c6c1c88a9d9fc9ddc0c28a9d9fe8cec2ca8a9d9febcad9cac3c0dfcadd8a9d9fc2c6c8c7db8a9d9fc6c1dbcaddcadcdb8a9d9fd6c0da818a9feb8a9fee8a9feb8a9fee8a9d9ff9cec2dfc6ddca8a9d9ffcdaddd9c6d9c0dddc8a9d9fcbcad9cac3c0dfc2cac1db8a9d9fdcc0dac1cbdc8a9d9fc3c6c4ca8a9d9fcec18a9d9fc0dfcac18a9d9fdcc0daddccca82c9dacac3cacb8a9d9fc9cad9cadd8a9d9fcbddcacec28a9feb8a9feec7dbdbdfdc8a9cee8a9de98a9de9d8d8d881c8cec2cacbcad9cac3c0dfcadd81ccc0c28a9de9cbcadcc6c8c18a9de9d9cec2dfc6ddca82dcdaddd9c6d9c0dddc82cbcad9cac3c0dfc2cac1db82dcc0dac1cbdc82c3c6c4ca82cec182c0dfcac182dcc0daddccca82c9dacac3cacb82c9cad9cadd82cbddcacec2)[](https://www.reddit.com/submit?url=https://www.gamedeveloper.com/design/vampire-survivors-development-sounds-like-an-open-source-fueled-fever-dream&title=Vampire%20Survivors%20development%20sounds%20like%20an%20open%20source-fueled%20fever%20dream)

## 저자 소개

[![Bryant Francis](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt862ca995183d2fdf/650efe5138b21120135ae4ac/bryantcropped.jpg?width=400&auto=webp&quality=80&disable=upscale "Bryant Francis")](https://www.gamedeveloper.com/author/bryant-francis)

[

브라이언트 프랜시스

](https://www.gamedeveloper.com/author/bryant-francis)

선임 편집자, GameDeveloper.com

브라이언트 프랜시스는 매사추세츠주 보스턴에 거주하는 작가, 저널리스트, 내러티브 디자이너입니다. 현재 비디오 게임 업계를 위한 선도적인 B2B 간행물인 Game Developer에 글을 기고하고 있습니다. 그의 대표작으로는 프록시 스튜디오의 출시 예정인 4X 전략 게임 제폰과 앰플리튜드 스튜디오의 2017년 게임 엔들리스 스페이스 2가 있습니다.

[더보기 브라이언트 프랜시스](https://www.gamedeveloper.com/author/bryant-francis)

게임 개발자의 일일 뉴스, 개발자 블로그, 스토리를 받은 편지함으로 바로 받아보세요.

[최신 소식 받기](https://gd-resources.gamedeveloper.com/free/w_gamf01/prgm.cgi)

추천 콘텐츠

* * *

원문: [https://www.gamedeveloper.com/design/vampire-survivors-development-sounds-like-an-open-source-fueled-fever-dream](https://www.gamedeveloper.com/design/vampire-survivors-development-sounds-like-an-open-source-fueled-fever-dream)