---
title:  "클래식 포스트모템: 오리지널 사이코넛의 개발은 험난한 과정이었습니다."

categories:
  - 번역
  
tags:
  - Game Developer
toc: true
toc_sticky: true
 
date: 2024-07-27
last_modified_at: 2024-07-27
---
[![Picture of Holly Green](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltdec6f50070a70555/650f059f457d12263163b2ca/75258562_10220983058707614_8585122828469141504_n.jpg?width=100&auto=webp&quality=80&disable=upscale "Picture of Holly Green")](https://www.gamedeveloper.com/author/holly-green)

[홀리 그린](https://www.gamedeveloper.com/author/holly-green), 커뮤니티 편집 코디네이터

7월 26일, 2024

2 분 읽기

![](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt5580863a349d6c3c/66a3c8fe60a745f69acd5fca/Psychonauts_Postmortem_GDM_Aug_2005.png?width=1280&auto=webp&quality=95&format=jpg&disable=upscale)

[](https://www.linkedin.com/sharing/share-offsite/?url=https://www.gamedeveloper.com/design/classic-postmortem-the-development-of-the-original-psychonauts-was-a-fraught-experience)[](https://www.facebook.com/sharer/sharer.php?u=https://www.gamedeveloper.com/design/classic-postmortem-the-development-of-the-original-psychonauts-was-a-fraught-experience)[](https://www.twitter.com/intent/tweet?url=https://www.gamedeveloper.com/design/classic-postmortem-the-development-of-the-original-psychonauts-was-a-fraught-experience)[](https://www.gamedeveloper.com/cdn-cgi/l/email-protection#ccf3bfb9aea6a9afb8f18fa0adbfbfa5afec9ca3bfb8a1a3beb8a9a1f6ec98a4a9eca8a9baa9a0a3bca1a9a2b8eca3aaecb8a4a9eca3bea5aba5a2ada0ec9cbfb5afa4a3a2adb9b8bfecbbadbfecadecaabeadb9aba4b8eca9b4bca9bea5a9a2afa9eaada1bcf7aea3a8b5f185e9fefcb8a4a3b9aba4b8e9fefcb8a4a9e9fefcaaa3a0a0a3bba5a2abe9fefcaabea3a1e9fefc8bada1a9e9fefc88a9baa9a0a3bca9bee9fefca1a5aba4b8e9fefca5a2b8a9bea9bfb8e9fefcb5a3b9e2e9fc88e9fc8de9fc88e9fc8de9fefc8fa0adbfbfa5afe9fefc9ca3bfb8a1a3beb8a9a1e9ff8de9fefc98a4a9e9fefca8a9baa9a0a3bca1a9a2b8e9fefca3aae9fefcb8a4a9e9fefca3bea5aba5a2ada0e9fefc9cbfb5afa4a3a2adb9b8bfe9fefcbbadbfe9fefcade9fefcaabeadb9aba4b8e9fefca9b4bca9bea5a9a2afa9e9fc88e9fc8da4b8b8bcbfe9ff8de9fe8ae9fe8abbbbbbe2abada1a9a8a9baa9a0a3bca9bee2afa3a1e9fe8aa8a9bfa5aba2e9fe8aafa0adbfbfa5afe1bca3bfb8a1a3beb8a9a1e1b8a4a9e1a8a9baa9a0a3bca1a9a2b8e1a3aae1b8a4a9e1a3bea5aba5a2ada0e1bcbfb5afa4a3a2adb9b8bfe1bbadbfe1ade1aabeadb9aba4b8e1a9b4bca9bea5a9a2afa9)[](https://www.reddit.com/submit?url=https://www.gamedeveloper.com/design/classic-postmortem-the-development-of-the-original-psychonauts-was-a-fraught-experience&title=Classic%20Postmortem%3A%20The%20development%20of%20the%20original%20Psychonauts%20was%20a%20fraught%20experience)

2005년, 기발한 사이키델릭 플랫포머인 사이코넛은 더블 파인의 첫 번째 프로젝트로 데뷔하여 기발한 유머 감각과 기괴한 비주얼 스타일, 잊을 수 없는 독특한 캐릭터로 관객들을 즐겁게 했습니다. 2000년대 초반 닷컴 붐이 불던 샌프란시스코에서 탄생한 이 게임은 팀 셰퍼의 창의적인 비전과 우수성을 향한 헌신이 집약된 작품으로 호평을 받았으며,사이코넛 개발 직후 Valve의 포탈 게임을 집필하게 된 공동 작가 Erik Wolpaw를 비롯한 유능한 협업 팀의 헌신적인 노력으로 완성 되었습니다.

하지만 이 게임은 비평가들의 사랑을 받았지만 열악한 작업 환경, 경험 부족, 빠르게 쇠퇴하는 커뮤니케이션, 끊임없는 크런치 주기, 퍼블리셔 찾기, 제작 과정에서 여러 역할을 맡게 된 셰퍼의 과도한 업무 확장 등 여러 장애물과 좌절로 인해 창의적인 성공을 거두지 못했습니다. 이러한 혼란을 관리하기 위해 고용된 프로듀서 캐롤라인 에스머독은 "게임 제작 과정에서 우리의 성공은 '확실한 패배의 문턱에서 승리를 거듭 빼앗은 것'으로 정의할 수 있을 것 같았습니다."라고 말합니다.

압박감에도 불구하고 팀은 촉박한 기한 내에 퍼블리셔를 찾았을 뿐만 아니라 "게임의 품질을 떨어뜨리거나 회사의 소유권을 잃거나 단 하루도 급여를 받지 못한 일 없이" 게임을 출시할 수 있었다고 에스머독은 말합니다. "다른 그룹이었다면 좌절하고 실망했을 일련의 좌절과 실망 속에서도 더블 파인 크루는 흔들리지 않는 정신을 발휘하여 제가 본 것 중 가장 응집력 있는 팀 중 하나를 만들었습니다. 이런 연대는 모집할 수 있는 것이 아니라 불 속에서만 만들어지는 것입니다."

게임 출시 10주년을 맞아 2015년에 재출간된[게임 개발자 매거진 2005년 8월호에](https://chrome-extension://efaidnbmnnnibpcajpcglclefindmkaj/https://ubm-twvideo01.s3.amazonaws.com/o1/vault/GD_Mag_Archives/GDM_August_2005.pdf) 실린[이 고전적인 포스트모템에서](https://www.gamedeveloper.com/audio/classic-postmortem-double-fine-s-i-psychonauts-i-)사이코넛개발 과정에서 무엇이 옳고 그랬는지에 대한 그녀의 분석을 읽어보세요 .

자세히 읽어보세요:

인기 [스토리포스트모템가마](https://www.gamedeveloper.com/keyword/postmortems)[아카이브](https://www.gamedeveloper.com/keyword/gama-archive)

[](https://www.linkedin.com/sharing/share-offsite/?url=https://www.gamedeveloper.com/design/classic-postmortem-the-development-of-the-original-psychonauts-was-a-fraught-experience)[](https://www.facebook.com/sharer/sharer.php?u=https://www.gamedeveloper.com/design/classic-postmortem-the-development-of-the-original-psychonauts-was-a-fraught-experience)[](https://www.twitter.com/intent/tweet?url=https://www.gamedeveloper.com/design/classic-postmortem-the-development-of-the-original-psychonauts-was-a-fraught-experience)[](https://www.gamedeveloper.com/cdn-cgi/l/email-protection#350a4640575f5056410876595446465c5615655a4641585a474150580f15615d501551504350595a4558505b41155a5315415d50155a475c525c5b54591565464c565d5a5b544041461542544615541553475440525d4115504d4550475c505b5650135458450e575a514c087c100705415d5a40525d41100705415d50100705535a59595a425c5b5210070553475a581007057254585010070571504350595a455047100705585c525d411007055c5b4150475046411007054c5a401b10057110057410057110057410070576595446465c56100705655a4641585a47415058100674100705615d5010070551504350595a4558505b411007055a53100705415d501007055a475c525c5b545910070565464c565d5a5b544041461007054254461007055410070553475440525d41100705504d4550475c505b56501005711005745d414145461006741007731007734242421b5254585051504350595a4550471b565a581007735150465c525b10077356595446465c5618455a4641585a4741505818415d501851504350595a4558505b41185a5318415d50185a475c525c5b54591845464c565d5a5b544041461842544618541853475440525d4118504d4550475c505b5650)[](https://www.reddit.com/submit?url=https://www.gamedeveloper.com/design/classic-postmortem-the-development-of-the-original-psychonauts-was-a-fraught-experience&title=Classic%20Postmortem%3A%20The%20development%20of%20the%20original%20Psychonauts%20was%20a%20fraught%20experience)

## 저자 소개

[![Holly Green](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltdec6f50070a70555/650f059f457d12263163b2ca/75258562_10220983058707614_8585122828469141504_n.jpg?width=400&auto=webp&quality=80&disable=upscale "Holly Green")](https://www.gamedeveloper.com/author/holly-green)

[

홀리 그린

](https://www.gamedeveloper.com/author/holly-green)

커뮤니티 편집 코디네이터, GameDeveloper.com

홀리 그린은 15년 동안 게임 미디어에 종사해 왔으며, 다양한 매체에서 리포터와 비평가로 일했습니다. 커뮤니티 편집 코디네이터로서 게임 개발자 독자들이 제출하는 글을 관리하고, 수십 년 동안 Game Developer 브랜드로 업계 전문가를 교육해 온 대표적인 칼럼과 기능의 성장을 감독하는 일을 담당하고 있습니다. 비디오 게임을 플레이하거나 글을 쓰지 않을 때는 워싱턴 주 시애틀에서 남편과 함께 요리, 정원 가꾸기, 맥주 양조 등을 즐기고 있습니다.

[더보기 홀리 그린](https://www.gamedeveloper.com/author/holly-green)

Game Developer의 일일 뉴스, 개발자 블로그, 스토리를 받은 편지함으로 바로 받아보세요.

[최신 소식 받기](https://gd-resources.gamedeveloper.com/free/w_gamf01/prgm.cgi)

추천 콘텐츠

* * *

원문: [https://www.gamedeveloper.com/design/classic-postmortem-the-development-of-the-original-psychonauts-was-a-fraught-experience](https://www.gamedeveloper.com/design/classic-postmortem-the-development-of-the-original-psychonauts-was-a-fraught-experience)