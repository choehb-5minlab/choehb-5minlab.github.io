---
title:  "리포트: 소니, F2P 게임을 위한 플레이스테이션 모바일 스토어 제작"

categories:
  - 번역
  
tags:
  - Game Developer
toc: true
toc_sticky: true
 
date: 2024-05-23
last_modified_at: 2024-05-23
---
[![Picture of Justin Carter](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt33d97cf9dc327673/650f03deb8329c920e5af96f/Image_from_iOS.jpg?width=100&auto=webp&quality=80&disable=upscale "Picture of Justin Carter")](https://www.gamedeveloper.com/author/justin-carter)

[저스틴 카터](https://www.gamedeveloper.com/author/justin-carter), 기고 편집자

May 22, 2024

1 분 읽기

![Logo for Sony's PlayStation console.](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltcba26829a83b1c4d/650f08bd7b2d0b08113a6998/PlayStation_Header.png?width=850&auto=webp&quality=95&format=jpg&disable=upscale "Logo for Sony's PlayStation console.")

PlayStation/소니 인터랙티브 엔터테인먼트 이미지 제공.

[](https://www.linkedin.com/sharing/share-offsite/?url=https://www.gamedeveloper.com/business/report-sony-making-playstation-mobile-store-for-f2p-games)[](https://www.facebook.com/sharer/sharer.php?u=https://www.gamedeveloper.com/business/report-sony-making-playstation-mobile-store-for-f2p-games)[](https://www.twitter.com/intent/tweet?url=https://www.gamedeveloper.com/business/report-sony-making-playstation-mobile-store-for-f2p-games)[](https://www.gamedeveloper.com/cdn-cgi/l/email-protection#88b7fbfdeae2edebfcb5daedf8e7fafcb2a8dbe7e6f1a8e5e9e3e1e6efa8d8e4e9f1dbfce9fce1e7e6a8e5e7eae1e4eda8fbfce7faeda8eee7faa8cebad8a8efe9e5edfbaee9e5f8b3eae7ecf1b5c1adbab8fce0e7fdefe0fcadbab8fce0edadbab8eee7e4e4e7ffe1e6efadbab8eefae7e5adbab8cfe9e5edadbab8ccedfeede4e7f8edfaadbab8e5e1efe0fcadbab8e1e6fcedfaedfbfcadbab8f1e7fda6adb8ccadb8c9adb8ccadb8c9adbab8daedf8e7fafcadbbc9adbab8dbe7e6f1adbab8e5e9e3e1e6efadbab8d8e4e9f1dbfce9fce1e7e6adbab8e5e7eae1e4edadbab8fbfce7faedadbab8eee7faadbab8cebad8adbab8efe9e5edfbadb8ccadb8c9e0fcfcf8fbadbbc9adbaceadbaceffffffa6efe9e5edecedfeede4e7f8edfaa6ebe7e5adbaceeafdfbe1e6edfbfbadbacefaedf8e7fafca5fbe7e6f1a5e5e9e3e1e6efa5f8e4e9f1fbfce9fce1e7e6a5e5e7eae1e4eda5fbfce7faeda5eee7faa5eebaf8a5efe9e5edfb)[](https://www.reddit.com/submit?url=https://www.gamedeveloper.com/business/report-sony-making-playstation-mobile-store-for-f2p-games&title=Report%3A%20Sony%20making%20PlayStation%20mobile%20store%20for%20F2P%20games)

## 한눈에 보기

*   PC 시장에 진출한 소니가 PlayStation 모바일 플랫폼으로 휴대폰 시장에 첫 발을 내딛는 모양새입니다.

소니는 휴대폰용 플레이스테이션 플랫폼의 형태로 모바일 게임에 큰 발걸음을 내딛고 있는 것으로 알려졌습니다.

[트윅타운은](https://www.tweaktown.com/news/98435/sony-developing-playstation-mobile-platform/index.html)[모바일 플랫폼 아키텍트를](https://boards.greenhouse.io/sonyinteractiveentertainmentglobal/jobs/5078757004) 구하는 새로운 구인 공고를 발견했습니다 . 설명에는 "무료 모바일 게임을 개발, 퍼블리싱 및 운영하는 데 사용할 수 있는 PlayStation 전용 생태계를 위한 아키텍처와 백엔드를 설계"하는 업무가 언급되어 있습니다.

페이트/그랜드 오더를 제외하면 PlayStation의 모바일 게임은 기본적으로 존재 하지 않습니다.하지만 [PC 시장에](https://www.gamedeveloper.com/business/ghost-of-tsushima-s-pc-port-introduces-new-playstation-overlay-trophy-support) 진출하기위해 더 많은 노력을 기울이고 있는 만큼 모바일에서도 같은 노력을 기울이는 것이 당연합니다.

추가 업무로는 PlayStation 내부 팀과 협력하고 "모든 모바일 게임이 PlayStation의 품질 표준을 충족하는지 확인하는 것"이 포함됩니다.

흥미롭게도 직무 설명에는 모바일 타이틀을 PlayStation 서비스에 연결해야 한다는 내용이 포함되어 있습니다. [계정 연결](https://www.gamedeveloper.com/business/sony-reverses-helldivers-2-s-account-linking-requirement)은 최근 [헬다이버 2로](https://www.gamedeveloper.com/business/helldivers-2-to-make-steam-playstation-account-linking-mandatory-in-june) 인해 소니에게 골 칫거리가되었지만, 이 논란으로 인해 퍼블리셔의 아이디어가 완전히 사라지지는 않았습니다.

소니와 Microsoft 모두 과거에는 모바일에 큰 관심을 보이지 않았지만 곧 바뀔 예정입니다. [액티비전 블리자드를](https://www.gamedeveloper.com/business/activision-blizzard-joins-xbox-game-studios-following-microsoft-acquisition)소유하고 있는 Microsoft는 7월에[모바일 게임 스토어](https://www.gamedeveloper.com/mobile/microsoft-launching-web-based-mobile-game-storefront-in-july) (웹 기반이긴 하지만)를 출시할 예정 이라고 합니다.

2022년 소니는 모바일 개발사 [Savage Game Studios를](https://www.gamedeveloper.com/business/playstation-acquires-mobile-game-developer-savage-game-studios)인수하여 당시 신설된 모바일 게임 사업부에 합류했습니다 . 작년에는[네온 코이로](https://www.gamedeveloper.com/business/savage-game-studios-rebrands-as-neon-koi-has-new-action-game-focus) 브랜드를 변경했으며 , CEO [미하일 카코프가](https://www.gamedeveloper.com/business/savage-game-studios-ceo-michail-katkoff-leaves-playstation-mobile-dev) 떠나면서 액션 게임 제작을 위해 모바일을 떠난 것으로 보입니다.

또한 2023년에 소니는 모바일 및 콘솔 게임 제작에 직접 초점을 맞춘 엔씨소프트와 글로벌 파트너십을 체결했습니다.

[](https://www.linkedin.com/sharing/share-offsite/?url=https://www.gamedeveloper.com/business/report-sony-making-playstation-mobile-store-for-f2p-games)[](https://www.facebook.com/sharer/sharer.php?u=https://www.gamedeveloper.com/business/report-sony-making-playstation-mobile-store-for-f2p-games)[](https://www.twitter.com/intent/tweet?url=https://www.gamedeveloper.com/business/report-sony-making-playstation-mobile-store-for-f2p-games)[](https://www.gamedeveloper.com/cdn-cgi/l/email-protection#506f2325323a3533246d0235203f22246a70033f3e29703d313b393e3770003c312903243124393f3e703d3f32393c357023243f223570363f22701662007037313d352376313d206b323f34296d1975626024383f25373824756260243835756260363f3c3c3f27393e3775626036223f3d75626017313d35756260143526353c3f2035227562603d39373824756260393e243522352324756260293f257e7560147560117560147560117562600235203f2224756311756260033f3e297562603d313b393e37756260003c312903243124393f3e7562603d3f32393c3575626023243f2235756260363f2275626016620075626037313d352375601475601138242420237563117562167562162727277e37313d35343526353c3f2035227e333f3d756216322523393e3523237562162235203f22247d233f3e297d3d313b393e377d203c312923243124393f3e7d3d3f32393c357d23243f22357d363f227d3662207d37313d3523)[](https://www.reddit.com/submit?url=https://www.gamedeveloper.com/business/report-sony-making-playstation-mobile-store-for-f2p-games&title=Report%3A%20Sony%20making%20PlayStation%20mobile%20store%20for%20F2P%20games)

## 저자 소개

[![Justin Carter](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt33d97cf9dc327673/650f03deb8329c920e5af96f/Image_from_iOS.jpg?width=400&auto=webp&quality=80&disable=upscale "Justin Carter")](https://www.gamedeveloper.com/author/justin-carter)

[

저스틴 카터

](https://www.gamedeveloper.com/author/justin-carter)

기고 편집자, GameDeveloper.com

미주리주 캔자스시티 출신인 저스틴 카터는 IGN, Polygon, SyFy Wire를 비롯한 여러 사이트에 글을 기고하고 있습니다. Game Developer 외에도 기즈모도의 io9에서 그의 글을 볼 수 있습니다. 그에게 껌을 얼마나 먹었냐고 묻지 마세요. 대답은 그가 인정하는 것보다 더 많을 테니까요.

[저스틴 카터에서 더 보기](https://www.gamedeveloper.com/author/justin-carter)

게임 개발자의 일일 뉴스, 개발자 블로그, 스토리를 받은 편지함으로 바로 받아보세요.

[최신 소식 받기](https://gd-resources.gamedeveloper.com/free/w_gamf01/prgm.cgi)

추천 콘텐츠

* * *

원문: [https://www.gamedeveloper.com/business/report-sony-making-playstation-mobile-store-for-f2p-games](https://www.gamedeveloper.com/business/report-sony-making-playstation-mobile-store-for-f2p-games)