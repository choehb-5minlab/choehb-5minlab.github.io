---
title:  "HoYoverse의 최신 가챠 엔진 해부하기"

categories:
  - 번역
  
tags:
  - NAAVIK
toc: true
toc_sticky: true
 
date: 2024-07-08
last_modified_at: 2024-07-08
---
![ZZZ](https://naavik.co/wp-content/uploads/2024/07/ZZZ-1-1024x576.jpg)

_출처: [Naavik](https://naavik.co/)_

젠리스 존 제로는 호요버스의 새로운 어반 판타지 액션 RPG로, 판타지 액션 RPG 겐신 임팩트와 작년 출시된 공상 과학 턴제 배틀 RPG 혼카이: 스타 레일의 후속작입니다. 7월 4일에 iOS, Android, PC, PS5로 전 세계에 출시되었습니다.

ZZZ는 포스트 아포칼립스 미래 도시 뉴 에리두를 배경으로 하며, [트레일러에서](https://youtu.be/_KC-ZVNqbdQ?si=-giYbc5x5qAxu27A) 볼 수 있듯이 호요버스의 트레이드마크인 높은 제작 퀄리티가 돋보이는 게임입니다. 사전 등록자 수가 4,000만 명을 넘어선 모에를 감안할 때 출시가 성사될 것은 의심의 여지가 없습니다. 이 수치는 '겐신'(사전 등록자 수 1,000만 명)과 '혼카이'(2,300만 명)를 쉽게 뛰어넘는 수치입니다.

![Pre-Registrations vs Launch Week Downloads](https://naavik.co/wp-content/uploads/2024/07/Pre-registrations-vs-Launch-1024x576.jpg)

_출처: [data.ai](https://data.ai/), [Naavik](https://naavik.co/)_

데이터닷에이아이의 추산에 따르면 출시 주 동안 겐신은 2,300만 다운로드를 기록했고, 혼카이는 4,300만 다운로드를 기록한 것으로 나타났습니다. 데이터닷에이아이의 수치는 애플과 구글의 모바일 앱스토어만 집계한 것으로, 호요버스 게임은 다양한 PC/콘솔 스토어와 타사 모바일 스토어에도 출시되어 있으므로 실제 수치는 더 높을 것입니다.

![RPD GI vs HSR](https://naavik.co/wp-content/uploads/2024/07/RPD-GI-vs-HSR-1024x576.jpg)

_출처: [data.ai](https://data.ai/), [Naavik](https://naavik.co/)_

하지만 [혼카이 해체에서](https://naavik.co/deep-dives/how-honkai-star-rail-reveals-cracks-in-the-hoyoverse/) 보았듯이 호요버스에게 모든 것이 장밋빛인 것은 아닙니다. 2024년 1분기에 겐신과 혼카이의 합산 Apple/Google 모바일 스토어 매출은 2억 8,400만 달러로, 작년 1분기에 겐신만 3억 2,000만 달러로 더 많은 수익을 올렸던 것에 비해 감소했습니다. 이는 LTV의 대리 지표인 겐신과 혼카이의 RPD 추세를 보면 알 수 있는데, 14개월째인 현재 혼카이의 RPD는 10.43달러로 겐신의 13.64달러에 비해 여전히 뒤처지고 있습니다.

호요버스 게임이 가챠 시스템을 통해 수익을 창출하는 F2P RPG라는 점을 고려할 때, F2P 친화적인 ZZZ의 가챠 엔진을 자세히 살펴보고 기존 타이틀과의 변화를 비교해 봅시다. 겐신의 큰 성공과 함께, ZZZ와 같은 타이틀을 통해 HoYoverse는 다양한 가챠 수익화 모델을 실험할 수 있었고, **향후 가챠 RPG의 성장 가능성을 제시할** 수 있었습니다.

# **Gotta Catch 'Em All**

![ZZZ's Gacha System](https://naavik.co/wp-content/uploads/2024/07/ZZZs-gacha-system-1024x576.jpg)

_출처: [Naavik](https://naavik.co/)_

ZZZ의 가챠 상점은 이전의 모든 HoYoverse 타이틀의 표준 설정을 따릅니다: 플레이어는 실제 돈을 슬롯머신에 굴려서 최종 게임 콘텐츠를 클리어하는 데 필요한 희귀 캐릭터와 무기를 획득할 수 있는 기회를 얻을 수 있습니다. 3주마다 상점에 새로운 슬롯머신(게임 용어로는 배너)이 추가되며, 이 슬롯머신에는 드랍률이 높은 기간 한정 아이템이 새롭게 등장합니다. 3주가 지나면 이러한 아이템은 기본 배너에 추가되고 새로운 배너로 주기가 계속 이어집니다.

플레이어가 새로운 배너를 통해 조금 더 강력한 최신 캐릭터와 무기를 획득하기 위해 3주마다 매출이 급증하는 이유도 바로 이 때문입니다. 또한, 추천 캐릭터 배너와 무기 배너가 서로 완벽하게 일치하는 경우가 대부분입니다.

이러한 표준화를 통해 핵심 게임플레이와 메타게임이 플레이어가 새로운 배너를 정기적으로 뽑도록 유도한다는 가정 하에, 겐신, 혼카이, ZZZ의 HoYoverse 가챠 엔진은 상당히 비슷해졌습니다. 당기는 데 드는 비용도 모든 HoYoverse 게임에 공통적으로 적용되어 1회당 약 2달러이며, "X"를 당긴 후에는 더 희귀한 드롭이 보장되는 동정 시스템을 통해 편견 없이 비교할 수 있습니다.

# **"최고를 바라고, 최악을 예상하라" - 가챠를 한마디로 요약하면 다음과 같습니다.**

![Character Gacha GI vs HSR vs ZZZ](https://naavik.co/wp-content/uploads/2024/07/Gacha-Gi-vs-HSR-1024x576.jpg)

_출처: [Naavik](https://naavik.co/)_

ZZZ의 한정 캐릭터 배너 드랍률을 보면, 5성 캐릭터 드랍률은 세 게임에서 동일하게 유지되었지만(겐신, 혼카이, ZZZ 모두 0.60%), 4성 캐릭터와 무기 드랍률은 더 넉넉한 편입니다. ZZZ의 4성 캐릭터 드랍률은 7.05%로 겐신의 3.33%보다 두 배 이상 높으며, 4성 무기 드랍률은 2.35%로 겐신의 1.77%보다 높습니다.

이러한 드랍률의 변화는 5성 캐릭터를 쫓는 슈퍼 팬과 노련한 플레이어에게 피해를 주지는 않지만, 모든 플레이어가 게임을 진행하기 위해 최대 4성 캐릭터로 구성된 B팀을 더 쉽게 얻을 수 있게 되어 여정을 더 수월하게 만듭니다. 현재 가챠 RPG로 붐비는 공간에 ZZZ가 진입한 만큼, 이러한 초기 관대함은 게임을 다소 끈적하게 만들 가능성이 높습니다.

![Weapon Gacha GI vs HSR vs ZZZ](https://naavik.co/wp-content/uploads/2024/07/Weapon-Gacha-vs-HSR-vs-ZZZ-1024x576.jpg)

_출처: [Naavik](https://naavik.co/)_

ZZZ의 무기 배너 드랍률도 전반적으로 상승했습니다. 겐신의 5성 무기 드랍률은 0.70%, 혼카이는 0.80%, ZZZ는 1.00%입니다. ZZZ는 4성 무기의 드랍률도 크게 증가하여 드랍률이 두 배 이상 증가했습니다.

하지만 모든 게임에서 1달러당 드랍 확률은 동일하기 때문에 같은 1달러로 5성 드랍 확률이 0.30% 증가한 것은 혼카이와 겐신에 비해 ZZZ에게 불리하게 작용할 가능성이 높습니다.

또한 이러한 확률이 높아지면 더 많은 지출을 장려하고 더 많은 플레이어가 캐릭터 배너를 주로 사용한 후 무기 배너를 사용하는 흐름으로 유도할 수 있습니다. 이것이 LTV 방정식의 어느 쪽에 해당하는지는 게임이 한동안 운영되면 RPD 추세선에서 확인할 수 있을 것입니다.

![Standard Gacha GI vs HSr vs ZZZ](https://naavik.co/wp-content/uploads/2024/07/Standard-Gacha-GI-vs-HSR-vs-ZZZ-1024x576.jpg)

_출처: [Naavik](https://naavik.co/)_

ZZZ는 5성 아이템의 드랍률은 동일하지만 4성 아이템의 경우 플레이어가 보통 실제 돈을 쓰지 않는 일반 뽑기의 드랍률이 크게 증가했습니다. 이는 지난 두 게임인 겐신과 혼카이에서도 동일하게 유지되었습니다.

다른 호요버스 게임과 비교했을 때, ZZZ에서는 4성 캐릭터와 무기에 대해 모든 가챠 기계가 더 관대해지는 경향이 있습니다. 덕분에 게임 초반부터 중반까지의 진행이 다른 가챠 RPG보다 훨씬 원활하게 진행됩니다.

이 때문에 겐신의 글로벌 성공 이후 출시된 텐센트의 [타워 오브 판타지와](https://www.toweroffantasy-global.com/) 최근 출시된 쿠로게임즈의 [우더링 웨이브](https://wutheringwaves.kurogames.com/) 등 다른 가챠 RPG의 드롭률이 겐신보다 약간 높습니다.

마찬가지로, 이 분야의 새로운 경쟁자인 ZZZ의 넉넉한 가챠 머신은 5성 아이템 판매를 약간 희생하는 대신 아이템 수집과 진행 속도를 높여 플레이어를 즉시 끌어들이기 위해 설계되었을 가능성이 높습니다.

# **ZZZ의 새로운 F2P 전용 뽑기 기계**

![ZZZ's unique F2P Gacha](https://naavik.co/wp-content/uploads/2024/07/ZZZs-Unique-F2P-Gacha-1024x576.jpg)

_출처: [Naavik](https://naavik.co/)_

ZZZ는 또한 플레이어가 뽑아서 지원 캐릭터인 [방부스를](https://youtu.be/__45HTgembM?si=FieCa7_F9faISg02) 받을 수 있는 소프트 화폐 전용 배너를 10년 만에 새롭게 도입했습니다. 플레이어는 이벤트에 참여하고 스토리 미션을 완료하여 이 배너를 뽑을 수 있는 티켓을 모으지만, 다른 가챠 머신과 달리 이 방부 배너는 실제 돈으로 구매할 수 없습니다.

**ZZZ에서는 플레이어의 팀에 캐릭터 3명과 뱅부 1명이 포함되지만, 다른 HoYoverse 게임에서는 캐릭터 4명이 포함됩니다.** 따라서 플레이어는 팀을 최대로 끌어올리기 위해 필요한 5성 아이템이 더 적고, 가챠 배너를 완료하는 데 걸리는 시간도 더 짧습니다. 5성 아이템을 획득할 확률이 겐신과 혼카이에 비해 높아졌기 때문에 두 배로 증가했습니다. 이 점을 연결해 보면 장기적으로 ZZZ의 상대적인 수익 창출에 어떤 영향을 미칠지 알 수 있습니다.

ZZZ는 이러한 덱 크기 감소에 대응하기 위해 이전 호오버스와 다른 점이 한 가지 더 있습니다: 겐신과 혼카이에서는 플레이어가 5성 전투력을 가진 캐릭터로 시작하지만, ZZZ에서는 주인공이 전투에서 분대를 이끄는 비전투 캐릭터입니다. 주인공이 비전투 캐릭터로 바뀌었기 때문에 **ZZZ 플레이어는** 기본적으로 **덱 크기가 변경되었음에도 불구하고 5성 캐릭터 3명으로 팀을 계속 업데이트해야** 합니다.

# **"모든 시스템은 결과를 얻을 수 있도록 완벽하게 설계되었습니다"**

HoYoverse는 10년 넘게 업계에서 가장 수익성이 높은 여러 가챠 엔진을 운영해 왔습니다( [설립 여정에서](https://naavik.co/digest/mihoyos-founding-journey/) 다룬 것처럼). 특히 4천만 명이 넘는 사전 등록자를 고려할 때 ZZZ가 HoYoverse의 차세대 블록버스터 히트작이 될 것이라는 데는 의심의 여지가 없지만, 개선되고 친근해진 가챠 엔진이 게임의 상대적 수익화에 어떤 영향을 미치는지 지켜보는 것은 흥미로울 것입니다.

또한, 혼카이의 출시에서 보았듯이 회사 게임 전반에 걸쳐 카니발라이제이션이 발생했는데, 이번에도 그런 현상이 발생한다면 이전 게임과 비교했을 때 가장 많은 비용을 지출하는 유저의 기여도에 영향을 미칠 수 있습니다.

겐신과 같은 텐트폴의 성공으로 가챠 수익화에 대한 호요버스의 실험은 혼카이와 현재 ZZZ와 같은 후속작으로 이어졌습니다. 이는 업계의 다른 곳에서도 볼 수 있습니다: 캔디 크러쉬 사가에 대한 King의 전략은 캔디 크러쉬 소다나 프렌즈와 같은 타이틀에서 이벤트와 라이브 운영을 시도한 후 성공적인 테스트가 플래그십 타이틀에 적용하는 것이었습니다.

겐신의 가챠 엔진은 출시 이후 지금까지 그대로 유지되고 있습니다. 혼카이는 출시된 지 14개월이 지났지만 여전히 LTV 측면에서 겐신을 따라잡고 있기 때문에 가챠 엔진 변경은 아직 겐신을 따라잡지 못했습니다. ZZZ의 보다 관대한 접근 방식과 소프트 화폐 전용 배너의 추가는 위험한 시도입니다. 하지만 이러한 시도가 성과를 거둔다면 다른 호오버스 게임에도 적용될 가능성이 높습니다.

이러한 새로운 변화가 포트폴리오 전체에 즉시 확산되지는 않더라도 호요버스 전체적으로는 혼카이와 겐신을 모두 출시하는 것이 겐신만 출시하는 것보다 월 평균 1,000만 달러의 수익이 더 높습니다. 따라서 게임의 수명을 고려할 때 여전히 가치 있는 투자이며 다른 퍼블리셔에 대한 방어책이기도 합니다. ZZZ의 출시로 호요버스는 가챠 RPG 장르에서 장기적인 지배력을 더욱 강화할 수 있게 되었습니다.

* * *

# **스폰서의 한마디: NEFTA**

![NEFTA](https://naavik.co/wp-content/uploads/2024/07/NEFTA-1024x247.png)

## **추적을 옵트아웃한 iOS 사용자로부터의 우수한 IAA 수익 창출**

네프타의 광고 네트워크는 퍼블리셔와 광고주가 직면한 문제, 즉 ATT를 통해 추적을 옵트아웃하는 iOS 사용자로부터의 수익 및 eCPM 감소에 대한 개인정보 보호 준수 솔루션을 제공합니다. 네프타는 인앱 광고 수익을 개선하기 위해 퍼스트 파티 데이터를 사용하는 접근 방식을 고안했습니다.

퍼블리셔는 SDK를 기본으로 또는 LevelPlay 또는 Max 미디에이션을 통해 통합하고 Nefta의 게임 이벤트 분류를 추가하여 플레이어 행동에 대한 더 큰 인사이트를 확보할 수 있습니다. 네프타의 플랫폼은 이러한 게임 이벤트와 사용 패턴을 앱별로 관찰하고 고급 머신 러닝과 행동 분석을 적용하여 프로필 그룹을 생성합니다. 네프타는 특정 프로필 그룹이 특정 크리에이티브를 클릭할 가능성이 더 높다는 사실을 발견하여 잠재고객 참여, 광고 상호 작용, 매출 증가를 이끌어냈습니다.

이를 통해 100% 개인정보를 준수하는 방식으로 광고주에게 우수한 성과를 제공하는 동시에 퍼블리셔의 ARPDAU를 높일 수 있습니다.

[자세히 알아보기](https://marketing.nefta.io/more-revenue-for-ios-op-out-users)

* * *

# **다른 뉴스**

#### 💸 펀딩 및 인수:

*   [키워드 스튜디오, 스웨덴 투자회사 EQT와 22억 파운드 규모의 인수 계약 체결](https://www.gamesindustry.biz/keywords-studios-reaches-22bn-acquisition-agreement-with-swedish-investment-company-eqt)
*   [나자라, 3,600만 달러 규모의 거래로 키도피아 완전 인수 추진](https://www.pocketgamer.biz/nazara-eyes-full-acquisition-of-kiddopia-in-36m-deal/)
*   [Gen AI 플랫폼 Bitmagic, 펀딩 라운드에서 4 백만 달러 모금](https://www.gamesindustry.biz/gen-ai-platform-bitmagic-raises-4m-in-funding-round)
*   [2024 년 2 분기 벤처 캐피탈을 살펴보면 거래를위한 지속적인 투쟁이 드러납니다 | NVCA Pitchbook](https://venturebeat.com/games/first-look-at-q2-2024-venture-capital-reveals-continued-struggle-for-deals-nvca-pitchbook/)
*   [데이브레이크, 싱귤래리티 6 인수](https://www.gamesindustry.biz/daybreak-acquires-singularity-6)

#### **📊 비즈니스 및 제품:**

*   [데이터 요약: 워크래프트 럼블, 모노폴리 고, 스타 워즈 헌터스, 스쿼드 버스터즈, 키워드의 22 억 파운드 거래 등](https://mobilegamer.biz/data-digest-warcraft-rumble-monopoly-go-star-wars-hunters-and-squad-busters-numbers-keywords-2-2bn-deal-and-more/)
*   [슈퍼셀의 스쿼드 버스터즈, 첫 30일간 2,400만 달러의 순익 달성](https://www.pocketgamer.biz/supercells-squad-busters-hits-24m-net-revenue-in-first-30-days/)
*   [니코 파트너스: 중국 PC 플레이어의 62%가 작년보다 게임에 더 많은 지출을 합니다.](https://www.gamesindustry.biz/niko-partners-62-of-china-pc-players-spending-more-on-games-than-last-year)
*   [썬더풀 그룹, 게임에 집중하기 위해 유통 사업 매각](https://www.pocketgamer.biz/thunderful-group-sells-off-distribution-business-as-it-focuses-on-games/)
*   [포트나이트의 로켓 레이싱에 익숙한 도로를 도입한 NASCAR](https://venturebeat.com/games/nascar-brings-its-familiar-roadways-to-fortnites-rocket-racing/)

#### 👾 기타:

*   [게임 개발, MENA 성장, 자금 조달 문제에서 AI를 탐구하는 스포일즈 CEO 무사브 알말키의 이야기](https://www.pocketgamer.biz/spoilz-ceo-musab-almalki-on-exploring-ai-in-game-development-mena-growth-and-funding-challenges-and/)
*   [FTC는 수리 권리를 겁주는 PC 제조업체를 조사하고 있습니다.](https://www.theverge.com/2024/7/3/24191790/asrock-gigabyte-zotac-ftc-warranty-void-right-to-repair)
*   [닌텐도, AI](https://www.gamesindustry.biz/nintendo-says-ai-can-be-more-creative-but-also-recognises-that-it-has-issues) [](https://www.gamesindustry.biz/nintendo-says-ai-can-be-more-creative-but-also-recognises-that-it-has-issues)["](https://www.gamesindustry.biz/nintendo-says-ai-can-be-more-creative-but-also-recognises-that-it-has-issues) [더 창의적](https://www.gamesindustry.biz/nintendo-says-ai-can-be-more-creative-but-also-recognises-that-it-has-issues) 일 [수있다](https://www.gamesindustry.biz/nintendo-says-ai-can-be-more-creative-but-also-recognises-that-it-has-issues) ["고 말하지만](https://www.gamesindustry.biz/nintendo-says-ai-can-be-more-creative-but-also-recognises-that-it-has-issues) [](https://www.gamesindustry.biz/nintendo-says-ai-can-be-more-creative-but-also-recognises-that-it-has-issues)["또한](https://www.gamesindustry.biz/nintendo-says-ai-can-be-more-creative-but-also-recognises-that-it-has-issues) [문제가 있음을 인식"](https://www.gamesindustry.biz/nintendo-says-ai-can-be-more-creative-but-also-recognises-that-it-has-issues)
*   [데이비드 핫셀 호프, 게임으로 기후 변화에 맞서기 위해 Make Green Tuesday Moves에 합류](https://venturebeat.com/games/david-hasselhoff-joins-make-green-tuesday-moves-to-fight-climate-change-with-games/)
*   [게임 보이 카메라는 곧 끔찍한 웹캠으로 두 번째 삶을 살게 될 것입니다.](https://www.theverge.com/2024/7/3/24191794/gb-operator-game-boy-camera-webcam-epilogue-nintendo)

* * *

# **제품 컨설팅 서비스**

![Naavik](https://naavik.co/wp-content/uploads/2024/07/Naavik.png)

전체 라이프사이클 제품 및 디자인 서비스를 제공하는 Naavik은 원격 제품 팀입니다. 핵심/메타게임 콘셉트, 기능 디자인, 경제 모델링, 게임플레이 밸런싱, 수익화 설계, 라이브 운영 실험 등 다양한 플랫폼과 장르의 게임 팀이 게임의 KPI를 크게 향상시킬 수 있도록 지원해 왔습니다. 유니티의 고객 중 한 명이 한 말을 소개합니다.

![Andrew Green](https://naavik.co/wp-content/uploads/2024/06/andrew.png)

_"나빅 팀과의 협업은 환상적인 경험이었습니다. 커뮤니케이션이 빠르고 정확하고, 프로젝트 온보딩이 원활하며, 지식 기반과 분석 전문 지식에 대한 접근성이 뛰어납니다. 제품 연구 결과물은 포괄적이고 매우 귀중한 것이었습니다."_

\-[_Andrew N. Green_](https://www.linkedin.com/in/andrewngreen10/?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=ios_app)_, 고문, 전 파트너_ ,[_a16z_](https://a16z.com/);

더 자세히 알고 싶으시면 [여기](https://naavik.us7.list-manage.com/track/click?u=640af053471c877a3c39f0007&id=87cf0eae4c&e=488c5fc418)! 확장된 컨설팅 서비스 포트폴리오도 확인해 보세요. [여기](https://naavik.us7.list-manage.com/track/click?u=640af053471c877a3c39f0007&id=c2d2be9cd3&e=488c5fc418).

[우리와 함께 일하기](https://www.naavik.co/consulting/)

* * *

태그: [가](https://naavik.co/tag/gacha/)챠, [호이오버스](https://naavik.co/tag/hoyoverse/), [젠리스 존 제로](https://naavik.co/tag/zenless-zone-zero/)

## 다음 호를 놓치지 마세요!

_게임 업계 최고의 뉴스레터를 신청하고 받은 편지함에서 바로 받아보세요._

구독 신청하기

<div class="kadence-blocks-form-message kadence-blocks-form-warning">양식을 제출하려면 브라우저에서 JavaScript를 활성화해 주세요.</div><style>.kadence-form-8651\_c37b23-d9 .kadence-blocks-form-field.kb-submit-field { display: none; }</style>

원문: [https://naavik.co/digest/zzz-hoyoverse-friendliest-gacha/](https://naavik.co/digest/zzz-hoyoverse-friendliest-gacha/)