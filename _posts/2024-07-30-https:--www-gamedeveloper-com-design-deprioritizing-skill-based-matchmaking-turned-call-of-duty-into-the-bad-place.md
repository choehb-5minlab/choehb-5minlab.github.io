---
title:  "스킬 기반 매치메이킹을 우선순위에 두지 않으면 콜 오브 듀티가 나쁜 곳이 됩니다."

categories:
  - 번역
  
tags:
  - Game Developer
toc: true
toc_sticky: true
 
date: 2024-07-30
last_modified_at: 2024-07-30
---
[![Picture of Chris Kerr](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt1c7a117d71555292/650efbcad3423169a8871059/chris_kerr_headshot.jpg?width=100&auto=webp&quality=80&disable=upscale "Picture of Chris Kerr")](https://www.gamedeveloper.com/author/chris-kerr)

[크리스 커](https://www.gamedeveloper.com/author/chris-kerr), 뉴스 에디터

7월 29일, 2024

4분 읽기

![Players taking fire in Call of Duty: Modern Warfare III](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltc4d1314133af45ef/66a7b2c1a87f1226527e088f/Call_of_Duty_Header.png?width=1280&auto=webp&quality=95&format=jpg&disable=upscale "Players taking fire in Call of Duty: Modern Warfare III")

액티비전 블리자드 이미지 제공

[](https://www.linkedin.com/sharing/share-offsite/?url=https://www.gamedeveloper.com/design/deprioritizing-skill-based-matchmaking-turned-call-of-duty-into-the-bad-place)[](https://www.facebook.com/sharer/sharer.php?u=https://www.gamedeveloper.com/design/deprioritizing-skill-based-matchmaking-turned-call-of-duty-into-the-bad-place)[](https://www.twitter.com/intent/tweet?url=https://www.gamedeveloper.com/design/deprioritizing-skill-based-matchmaking-turned-call-of-duty-into-the-bad-place)[](https://www.gamedeveloper.com/cdn-cgi/l/email-protection#d1eea2a4b3bbb4b2a5ec95b4a1a3b8bea3b8a5b8abb8bfb6f1a2bab8bdbdfcb3b0a2b4b5f1bcb0a5b2b9bcb0bab8bfb6f1a5a4a3bfb4b5f192b0bdbdf1beb7f195a4a5a8f1b8bfa5bef185b9b4f193b0b5f181bdb0b2b4f7b0bca1eab3beb5a8ec98f4e3e1a5b9bea4b6b9a5f4e3e1a5b9b4f4e3e1b7bebdbdbea6b8bfb6f4e3e1b7a3bebcf4e3e196b0bcb4f4e3e195b4a7b4bdbea1b4a3f4e3e1bcb8b6b9a5f4e3e1b8bfa5b4a3b4a2a5f4e3e1a8bea4fff4e195f4e190f4e195f4e190f4e3e195b4a1a3b8bea3b8a5b8abb8bfb6f4e3e1a2bab8bdbdfcb3b0a2b4b5f4e3e1bcb0a5b2b9bcb0bab8bfb6f4e3e1a5a4a3bfb4b5f4e3e192b0bdbdf4e3e1beb7f4e3e195a4a5a8f4e3e1b8bfa5bef4e3e185b9b4f4e3e193b0b5f4e3e181bdb0b2b4f4e195f4e190b9a5a5a1a2f4e290f4e397f4e397a6a6a6ffb6b0bcb4b5b4a7b4bdbea1b4a3ffb2bebcf4e397b5b4a2b8b6bff4e397b5b4a1a3b8bea3b8a5b8abb8bfb6fca2bab8bdbdfcb3b0a2b4b5fcbcb0a5b2b9bcb0bab8bfb6fca5a4a3bfb4b5fcb2b0bdbdfcbeb7fcb5a4a5a8fcb8bfa5befca5b9b4fcb3b0b5fca1bdb0b2b4)[](https://www.reddit.com/submit?url=https://www.gamedeveloper.com/design/deprioritizing-skill-based-matchmaking-turned-call-of-duty-into-the-bad-place&title=Deprioritizing%20skill-based%20matchmaking%20turned%20Call%20of%20Duty%20into%20The%20Bad%20Place)

액티비전 블리자드가 콜 오브 듀티에서 기술 기반 매치메이킹(SBMM)을 중단했을 때 어떤 일이 있었는지 설명하는[장문의 백서를 발표했습니다](https://www.activision.com/cdn/research/CallofDuty_Matchmaking_Series_2.pdf). TL:DR 버전? 거의 모든 사람이 싫어했습니다.

콜 오브 듀티: 모던 워페어 3에서는 올해 초'스킬 우선순위 해제 테스트'를 실시하여 SBMM이 플레이어에게 다양한 방식으로 어떤 영향을 미치는지 살펴보고자 했습니다.

이 실험에서 스튜디오는 A/B 테스트 프레임워크를 활용하여 매치메이킹에서 숙련도에 대한 제약을 완화했습니다. 2024년 북미에서 테스트를 진행하면서 전체 인구의 50%로 구성된 치료 그룹을 설정했습니다. 나머지 절반의 플레이어는 아무런 영향을 받지 않았습니다.

## 실력 기반 매치메이킹을 완화했을 때 재접속률이 감소했습니다.

자신도 모르게 SBMM이 줄어든 것을 경험한 플레이어들은 만족하지 않았습니다. 한 달 동안 테스트를 진행한 후, Activision은 실험군을 스킬에 따라 동일한 규모의 10개 그룹으로 분류했습니다. SBMM을 우선순위에 두지 않은 결과, 90%의 플레이어의 재방문율이 크게 감소했습니다. 가장 숙련도가 높은 10%의 플레이어만 복귀율이 증가했지만, 전체적으로는 "의미 있게 적은 수의 플레이어가 게임을 다시 찾았다"고 액티비전 블리자드는 분석했습니다.

"이 효과는 작아 보일 수 있지만 테스트 기간 동안 이러한 변화를 관찰할 수 있었습니다. 이는 이자처럼 시간이 지남에 따라 누적되어 플레이어 인구에 의미 있는 영향을 미칠 것입니다. 이러한 패턴이 계속된다면 상위 10%를 포함한 모든 플레이어가 게임을 이탈하는 사례가 증가할 것이기 때문에 이는 우려되는 부분입니다."라고 설명했습니다.

"결국 상위 10%의 플레이어는 상위 20%의 플레이어가 되고, 결국에는 상위 30%의 플레이어가 되어 최고의 플레이어만 게임을 플레이하게 될 것입니다. 기존 상위 플레이어들은 게임에 다시 돌아오지 않을 가능성이 점점 더 높아질 것입니다. 결국, 함께 플레이할 수 있는 플레이어가 점점 줄어들기 때문에 모든 플레이어에게 더 나쁜 경험을 선사하게 될 것입니다. 또한, 위에서 언급했듯이 이번 테스트에서는 매칭 규칙에서 스킬의 우선순위를 낮췄습니다. 만약 이 기능이 완전히 제거된다면 몇 달 안에 플레이어 수가 급격히 줄어들 것으로 예상됩니다."

우선순위 하락 스킬 테스트의 영향을 받은 플레이어는 게임 도중에 게임을 그만둘 가능성도 높았으며, 액티비전 블리자드는 80%의 플레이어에서 게임 종료율이 "상당히" 증가했다고 설명했습니다. 상위 10%의 플레이어만 게임 이탈률이 의미 있게 감소했지만, 액티비전 블리자드는 이러한 상승세가 일시적일 것이라고 언급했습니다.

"낮은 실력대의 플레이어 이탈이 가속화됨에 따라 결국 상위 10% 플레이어는 (원래 상위 10% 플레이어가 전체 플레이어 기반에서 점점 더 많은 비중을 차지하기 때문에) 실력 분포가 하향 조정될 것입니다."라고 말합니다. "그 결과, 상위 10% 플레이어가 게임을 그만두는 비율이 점점 더 높아질 것으로 예상되며, 실력이 낮은 많은 플레이어가 게임을 떠난 후 50번째 퍼센타일 플레이어가 될 것입니다."

## 팀 데스 매치에서 더 많은 파열음이 발생했습니다.

팀 데스 매치(TDM)의 '난전' 횟수도 증가했습니다. 액티비전 블리자드는 한 로비의 한 팀이 "점수 차가 30점 이상으로 승리"하는 경우, 즉 상대방을 완전히 제압한 것을 폭파라고 설명했습니다. TDM 로비에 있는 모든 우선순위 지정 기술 테스트 플레이어의 타격전 횟수가 증가했으며, 이는 모든 플레이어가 덜 재미있게 게임을 즐기고 있다는 의미라고 말했습니다. "다른 게임 모드에서도 비슷한 결과가 나타났습니다."라고 덧붙였습니다.

실험의 영향을 받은 로비에서 분당 킬 수(KPM) 및 분당 점수(SPM)와 같은 다른 지표를 추적한 결과, 실력이 낮은 플레이어는 전반적으로 성적이 나빠진 반면 상위 10%는 "우위를 점할 수 있었다"는 것을 알 수 있었습니다.

"하위 20~30% 플레이어의 분당 킬 수가 크게 감소했습니다. 그 다음 60%의 플레이어는 큰 변화가 없었고, 상위 10%의 플레이어는 훨씬 더 높은 KPM을 기록했습니다."라고 액티비전 블리자드는 말합니다. "KPM과 마찬가지로 SPM도 비슷한 추세를 따릅니다. 실력이 낮은 플레이어는 실력이 떨어지는 반면, 상위 10%의 플레이어는 우위를 점할 수 있습니다. KPM과 마찬가지로 시간이 지남에 따라 저실력 플레이어의 게임 복귀율이 낮아지면서 플레이어가 이 분포에서 왼쪽으로 이동하는 것을 볼 수 있을 것으로 예상합니다.

"킬스트릭의 사용과 KPM 및 SPM의 증가는 로비 스킬 백분위수 격차가 더 커진 것은 상위 10%의 플레이어가 불균형을 활용하고 있다는 것을 보여줍니다. 안타깝게도 이러한 성능 향상은 스킬 분포의 하위 30%에 해당하는 훨씬 더 많은 인구가 훨씬 더 큰 영향을 받는 대가를 치르고 있습니다."

액티비전 블리자드는 최신 테스트와 과거 실험을 통해 SBMM과 플레이어 리텐션 사이에 분명한 연관성이 있음을 확인했다고 말합니다.

"스킬이 느슨해지면 플레이어가 게임에 계속 관심을 갖도록 하는 능력에 부정적인 영향을 미친다는 것을 알 수 있습니다."라고 말합니다. "위에서 설명한 우선순위 해제 스킬 테스트와 유사한 테스트에서 , 느슨한 스킬 매칭을 적용했을 때콜 오브 듀티: 모던 워페어 (2019)를 플레이하는 플레이어 수가 크게 감소하고 전체 경기 종료율이 증가하는 것을 확인할 수 있었습니다. 이후 하위 25%의 플레이어만 보호하고 나머지 75%의 플레이어에게 더 느슨한 매치메이킹을 허용한 결과, 스스로 보고한 '재미'에 대한 부정적인 지표가 뚜렷하게 나타났습니다."

[백서 전문은 액티비전 블리자드 웹사이트에서 확인할 수 있습니다](https://www.activision.com/cdn/research/CallofDuty_Matchmaking_Series_2.pdf).

자세히 알아보기

[주요 스토리](https://www.gamedeveloper.com/keyword/top-stories)

[](https://www.linkedin.com/sharing/share-offsite/?url=https://www.gamedeveloper.com/design/deprioritizing-skill-based-matchmaking-turned-call-of-duty-into-the-bad-place)[](https://www.facebook.com/sharer/sharer.php?u=https://www.gamedeveloper.com/design/deprioritizing-skill-based-matchmaking-turned-call-of-duty-into-the-bad-place)[](https://www.twitter.com/intent/tweet?url=https://www.gamedeveloper.com/design/deprioritizing-skill-based-matchmaking-turned-call-of-duty-into-the-bad-place)[](https://www.gamedeveloper.com/cdn-cgi/l/email-protection#09367a7c6b636c6a7d344d6c797b60667b607d607360676e297a62606565246b687a6c6d2964687d6a6164686260676e297d7c7b676c6d294a68656529666f294d7c7d702960677d66295d616c294b686d295965686a6c2f686479326b666d7034402c3b397d61667c6e617d2c3b397d616c2c3b396f666565667e60676e2c3b396f7b66642c3b394e68646c2c3b394d6c7f6c6566796c7b2c3b3964606e617d2c3b3960677d6c7b6c7a7d2c3b3970667c272c394d2c39482c394d2c39482c3b394d6c797b60667b607d607360676e2c3b397a62606565246b687a6c6d2c3b3964687d6a6164686260676e2c3b397d7c7b676c6d2c3b394a6865652c3b39666f2c3b394d7c7d702c3b3960677d662c3b395d616c2c3b394b686d2c3b395965686a6c2c394d2c3948617d7d797a2c3a482c3b4f2c3b4f7e7e7e276e68646c6d6c7f6c6566796c7b276a66642c3b4f6d6c7a606e672c3b4f6d6c797b60667b607d607360676e247a62606565246b687a6c6d2464687d6a6164686260676e247d7c7b676c6d246a68656524666f246d7c7d702460677d66247d616c246b686d247965686a6c)[](https://www.reddit.com/submit?url=https://www.gamedeveloper.com/design/deprioritizing-skill-based-matchmaking-turned-call-of-duty-into-the-bad-place&title=Deprioritizing%20skill-based%20matchmaking%20turned%20Call%20of%20Duty%20into%20The%20Bad%20Place)

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

원문: [https://www.gamedeveloper.com/design/deprioritizing-skill-based-matchmaking-turned-call-of-duty-into-the-bad-place](https://www.gamedeveloper.com/design/deprioritizing-skill-based-matchmaking-turned-call-of-duty-into-the-bad-place)