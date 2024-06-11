---
title:  "커맨드 앤 컨커 회고전"

categories:
  - 번역
  
tags:
  - Game Developer
toc: true
toc_sticky: true
 
date: 2024-06-11
last_modified_at: 2024-06-11
---
[![Picture of Josh Bycer](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt98434093b67825eb/650efd6139ff36eea344b067/bycerportrait.jpg?width=100&auto=webp&quality=80&disable=upscale "Picture of Josh Bycer")](https://www.gamedeveloper.com/author/josh-bycer)

[조쉬 바이서](https://www.gamedeveloper.com/author/josh-bycer), 블로거

6월 11, 2024

20 분 읽기

![](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltdde8b3c9181622bc/66632c02a63e652506d93f4e/Picture1.png?width=850&auto=webp&quality=95&format=jpg&disable=upscale)

저자가 제공한 이미지.

[](https://www.linkedin.com/sharing/share-offsite/?url=https://www.gamedeveloper.com/design/a-command-conquer-retrospective)[](https://www.facebook.com/sharer/sharer.php?u=https://www.gamedeveloper.com/design/a-command-conquer-retrospective)[](https://www.twitter.com/intent/tweet?url=https://www.gamedeveloper.com/design/a-command-conquer-retrospective)[](https://www.gamedeveloper.com/cdn-cgi/l/email-protection#c1feb2b4a3aba4a2b5fc80e182aeacaca0afa5e1e7a0acb1fae182aeafb0b4a4b3e193a4b5b3aeb2b1a4a2b5a8b7a4e7a0acb1faa3aea5b8fc88e4f3f1b5a9aeb4a6a9b5e4f3f1b5a9a4e4f3f1a7aeadadaeb6a8afa6e4f3f1a7b3aeace4f3f186a0aca4e4f3f185a4b7a4adaeb1a4b3e4f3f1aca8a6a9b5e4f3f1a8afb5a4b3a4b2b5e4f3f1b8aeb4efe4f185e4f180e4f185e4f180e4f3f180e4f3f182aeacaca0afa5e4f3f1e4f3f7e4f3f182aeafb0b4a4b3e4f3f193a4b5b3aeb2b1a4a2b5a8b7a4e4f185e4f180a9b5b5b1b2e4f280e4f387e4f387b6b6b6efa6a0aca4a5a4b7a4adaeb1a4b3efa2aeace4f387a5a4b2a8a6afe4f387a0eca2aeacaca0afa5eca2aeafb0b4a4b3ecb3a4b5b3aeb2b1a4a2b5a8b7a4)[](https://www.reddit.com/submit?url=https://www.gamedeveloper.com/design/a-command-conquer-retrospective&title=A%20Command%20%26%20Conquer%20Retrospective)

제가 집필 중인 RTS 책을 위해 과거에 커맨드 앤 컨커 시리즈 중 일부만 플레이했던 커맨드 앤 컨커 시리즈 전체를 다시 플레이하기로 결심했습니다. 당시 전체 장르를 정의했던 게임으로 돌아간다는 것은 게임 디자인과 게임 표현에 있어서도 다른 시대로 돌아간다는 의미이기 때문에 흥미로웠습니다. 이 게임이 오늘날에도 유효한지 여부는 논란의 여지가 있지만, 그 스타일은 확실히 시대를 초월합니다.

## 나는 메카닉이다, 나는 메카닉이다...

오리지널 게임은 많은 RTS 팬들에게 이 장르의 시초가 된 게임으로 기억되고 있습니다. 25년이 지난 지금, 게임의 스타일은 최첨단에서 90년대 FMV와 애니메이션의 타임캡슐로 변모했습니다. 실사 장면은 다소 촌스러울 수 있지만, 이것이 매력의 일부입니다.

진영디자인은 스타크래프트가 달성하고 표준을 세운 것과같은 깊이를 갖지는 못했지만, AI의 도전을 고려할 때 충분히 잘 해냈습니다. GDI 유닛이 더 강력하지만 카운터를 중심으로 하는 게임에서는 상대보다 더 많은 유닛을 배치할 수 있는 것이 더 큰 장점입니다.

재미있게도 NOD는 기술적으로는 모든 유닛이 약하지만, 게임 내 AI와 경로 덕분에 이를 보완할 수 있습니다. 더 무거운 전차로 보병을 추월할 수 있기 때문에 게임의 균형이 완전히 NOD에 유리하게 바뀝니다. GDI의 중형 전차는 너무 느려서 유닛을 안정적으로 뛰어넘을 수 없고, 흩어지기 명령으로 유닛을 피할 수 있지만 가벼운 NOD 전차로는 불가능합니다. 게임에서 제가 거둔 대부분의 승리는 대전차 전차를 포함한 모든 보병 유닛을 경전차로 몰아붙인 결과였습니다. 유닛의 AI가 이동과 사격에 있어서 약간 이상하기 때문에 이 점이 중요합니다. 화염방사기와 수류탄은 적 보병을 파괴할 수 있지만, 적 보병을 조준하고 발사할 수 있을 만큼 가까이 다가가야 합니다.

임무 설계는 기반이 없는 임무와 건설해야 하는 임무에 중점을 두어 전반적으로 진행됩니다. AI는 재건할 때 매우 공격적이며, 모든 상황에서 플레이어의 목표는 사령부를 파괴하여 제거하는 것입니다.

이 게임의 어려운 점은 두 진영 모두 쉽게 승리할 수 있는 유닛이 없는 맵이 주어진다는 것입니다.

![](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blteac0cac8c5c351b6/66632c23f1075148a5a683c2/image.png?width=700&auto=webp&quality=80&disable=upscale)

슈퍼무기는 지금도 여전히 슈퍼입니다(출처 작성자)

GDI에서는 강력한 전차 없이 대보병 방어를 갖춘 여러 기지를 점령해야 합니다. 반면 NOD는 시리즈 전체에서 최악의 대공 방어력을 갖춘 공습에 대처해야 합니다. 이러한 초기 게임에서는 실제로 RTS 전투를 하는 것이 아니라 승리를 위해 풀어야 하는 RTS 퍼즐을 플레이하는 것과 같습니다. 리마스터 버전에서도 GUI는 최신 버전에 비해 다소 투박하며, 공격 이동이 없다는 점은 게임을 플레이하는 데 있어 가장 큰 걸림돌 중 하나입니다. 음악은 여전히 클래식한 트랙이 많으며, 최고의 버전을 플레이하고 싶다면 2020년에 출시된 리마스터를 꼭 플레이해 보세요.

## 지옥 행진

레드 얼럿 1은 독자적인 세계관과 기억에 남는 음악, 그리고 가장 기묘한 FMV 영상으로 스핀오프를 선보였습니다. 또한 웨스트우드는 게임마다 진영의 강점을 바꾸는 전통을 시작했는데, 이제 아군은 약하지만 민첩한 유닛을, 소련군은 더 강하지만 비싼 유닛을 보유하게 되었습니다.

더 큰 맵, 더 고급스러운 지휘 임무, 그리고... 한숨이 절로 나오는 해전 등 전체적으로 미션 디자인이 대대적으로 개편되었습니다. 해전 미션은 제가 RTS에서 가장 싫어하는 미션인데, 이 게임에는 여러 가지 미션이 있습니다. 전작과 마찬가지로, 사령부가 살아 있는 동안 계속 건설하는 것을 좋아하는 AI를 상대로 승리하는 방법을 찾아야 합니다. 화염방사기 타워와 슈퍼 점프 공격견으로 인해 경로 탐색이 여전히 불안정한 곳이 많습니다. 스토리 측면에서 원작과 같은 매력은 없지만, 앞으로 더 많은 광기를 불러일으킬 수 있는 무대를 마련했습니다.

![](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt15bd28046686d151/66632c35e306e839ccc106a4/image.png?width=700&auto=webp&quality=80&disable=upscale)

첫 번째 레드 얼럿은 시리즈가 나아갈 방향과는 거리가 멀다(출처: 저자)

대부분의 GUI와 구조가 동일하기 때문에 이 게임은 오리지널 게임의 확장/사이드 프로젝트로 시작했으며, 다음 게임이 되어서야 제작 가치와 디자인이 크게 발전했다고 볼 수 있습니다.

고전 게임 중에서는 레드 얼럿 1도 괜찮았지만, 지옥의 행진 1을 제외하고는 원작만큼 애정이 가는 기억은 없습니다.

## 공상 과학 채널 오리지널 영화

티베리안 선은 웨스트우드가 영화에 정말 많은 예산을 들였다는 것을 알 수 있는 작품으로, 초반에 "일렉트로닉 아츠의 일부"라는 태그를 보고 마음이 아팠어요. 다시 한 번 24년 전에는 최첨단이었던 것이 지금은 더 촌스럽지만 여전히 유효합니다. 다시 이 작품으로 돌아와서, 제임스 얼 존스 같은 전문 배우가 조 쿠칸과 함께 풍경을 씹는 장면을 보는 것은 약간 충격적이었습니다.

이 작품은 유닛 디자인 측면에서 흥미롭습니다. 이제 우리는 진영이 최대한 서로 달라야 하는 시대에 살고 있습니다. 그래서 원반 투척 수류탄을 사용하는 GDI, 터널을 뚫는 APC와 화염 탱크를 사용하는 NOD, 그리고 NOD가 보유한 포병은 아마도 역대 최고의 지상 유닛일 것입니다.

이 게임의 미션 디자인은 이전 게임에 비해 더욱 다양해졌습니다. 많은 미션이 스토리에서 연쇄적으로 연결되어 있으며, 어떤 미션을 수행해야 메인 미션에서 유리할지 자유롭게 결정할 수 있습니다. 원한다면 더 어려운 미션을 위해 무시할 수 있지만 플레이 시간이 단축됩니다. 진영 디자인 측면에서 저는 NOD에 올인하는 편입니다. 이전 게임과 마찬가지로 유닛 카운터가 매우 중요하며, 모든 유닛의 체력은 더 높지만 카운터 데미지는 훨씬 더 강력합니다. 로켓 보병 몇 명으로 공중 유닛을 쉽게 제압할 수 있고, NOD의 지하 APC를 이용한 APC 돌격은 정말 재미있습니다.

![](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt2281e772a6d7d881/66632c53aa368153e0163ef0/image.png?width=700&auto=webp&quality=80&disable=upscale)

티베리안 선은 이 시리즈가 다른 게임과 차별화되기 시작한 시기입니다(출처: 작성자)

NOD에 대해 말하자면, 개발자들이 NOD를 멋진 진영으로 받아들이고 최고의 장난감을 선사한 것도 바로 이 때입니다. 당시 스타크래프트와 워크래프트를비롯한 모든 전략 게임 중에서 NOD는 RTS의 공식 '트롤 진영'이 되었습니다. 독성 미사일을 퍼붓고, 기지 전체와 유닛을 완전히 은폐하고, APC와 탱크를 지하로 보내 괴롭힐 수 있는 군대가 있고, 터미네이터 사이보그와 스텔스 탱크, 앞서 언급한 천상의 대포까지 얻게 됩니다. 한편, GDI는 제트팩 부대와 음파 탱크를 얻지만 여전히 멋지지만 카운터 시스템이 작동하면 쉽게 쓰러집니다.

티베리안 선에존재하는 대부분의 괴상함은 UI 덕분에 모든 이전 게임에서 볼 수 있는 것입니다. 아직 실제 공격 이동 명령이 있는 단계는 아니며, "말 그대로 적의 모든 유닛과 건물, 벽 부분을 죽이기"라는 미션 목표가 정말 마음에 듭니다. 임무 설계는 잘 되어 있지만 AI와 방어에 의해 깨집니다. NOD의 대포에 대응할 지상 유닛이 없기 때문입니다. 확장팩에서 GDI가 자체 포위 유닛을 얻더라도 사거리가 짧고 장갑이 적으며 정확도가 떨어집니다. 여기에 경로 찾기 및 AI까지 더해져 일부 임무는 플레이하기 너무 짜증나서 즐길 수 없습니다. 이 게임은 확장팩 내내 흥미로운 미션 디자인을 선보이기 때문에 아쉽습니다.

그래도 90년대부터 2000년대까지 공상 과학이 어떻게 변화했는지 타임캡슐을 통해 살펴볼 수 있다는 점에서 이 게임을 추천하고 싶어요.

## 지옥의 행진 2

레드 얼럿 2는 웨스트우드가 공식적으로 작업한 마지막 C&C 게임이 될 것입니다.티베리안 선과 같이 진영을 최대한 멋지게 만들면서 연합군과 소련군은 이제 유닛과 전략 면에서 완전히 달라졌습니다. 연합군은 더 유연한 항공기와 제트팩 병사를, 소련군은 테슬라 파워, 아포칼립스 탱크, 소련 오징어를 얻게 됩니다.

양쪽 모두 플레이하기에 좋고 독특한 느낌을 주며, 이는 최고의 다양한 미션 디자인 덕분입니다. 여전히 기지가 있는 임무와 없는 임무가 혼합되어 있지만, 움직이는 모든 것을 처치하는 것 외에도 처리해야 할 요소가 더 많습니다. 또한 AI는 주요 건물을 잃으면 가능한 한 빨리 경기를 끝내기 위해 플레이어에게 모든 것을 보내도록 프로그래밍되어 있습니다.

![](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltde4717f283985d28/66632c63177b6a5bf0065b49/image.png?width=700&auto=webp&quality=80&disable=upscale)

톤과 유닛 디자인 측면에서 레드 얼럿 2는 제가 가장 좋아하는 게임입니다(출처: 게임).

2000년대 초반의 기술과 당시 인기 배우들이 등장하는 FMV는 보는 즐거움과 감탄을 자아냅니다. 개선 사항으로는 드디어 건물에서 집결지를 설정할 수 있게 되었지만 여전히 공격 이동은 불가능합니다.

멀티플레이의 경우 ,레드 얼럿 2는에이지 오브 엠파이어 시리즈처럼 연합군과 소련군이 각기 다른 국가로 구분되어 고유 유닛이 하나씩 추가되었기 때문에 여전히 흥미로운 RTS 중 하나로 꼽 히고 있습니다.저는 플레이어가 더욱 독특한 미션에서 자신만의 트릭과 건물로 유리와 맞서 싸워야 하는 확장팩이 정말 마음에 듭니다. 모든 미션은 무차별 대입을 통해 승리할 수 있지만, 자신이 무엇을 하고 있는지 알고 있다면 적을 빠르게 완전히 제압할 수 있는 방법도 종종 있습니다.

이 게임은 다시 플레이하기 좋은 게임이며, 웨스트우드 스튜디오에 어울리는 슬픈 백조의 노래이기도 합니다. 이전 게임을 다시 플레이할 기회가 있다면 이 게임을 꼭 플레이해 보시고, 더 많은 콘텐츠를 추가하는 팬 모드도 있습니다.

## C&C 24

제너럴스는 공식적으로 EA 로스앤젤레스가 C&C의 개발사로 인수한 게임으로, 게임 톤과 디자인에 큰 변화를 가져온 게임입니다. 2003년에 출시된 이 게임은 9/11 사태 이후 애국심이 고조되던 시기에 출시되었습니다. 이 게임은 대체 세계가 아닌 '현실 세계'에서 미국, 중국, 중동 테러리스트의 대리인인 세계해방군을 조종하는 내용으로 진행됩니다. 이상하게도 이 부분은 커맨드 앤 컨커 게임을 다시 플레이할 때 가장 오래된 부분이며 , 분위기는 더욱 심각해졌습니다.

이제 세 개의 개별 캠페인 대신 중국, GLA, 미국으로 이어지는 세 진영으로 나뉘어진 느슨한 임무 세트가 있습니다. 이 기간 동안 EA 로스앤젤레스가 C&C를 e스포츠 친화적으로 만들기 위해 노력했다는 것을 알 수 있습니다. 유닛 경로 찾기와 AI는 이전 버전에 비해 훨씬 더 나빠졌습니다. 플레이어가 지켜보고 있지 않을 때 유닛이 어떤 행동을 할 것으로 예상되면 공격 또는 수비로 이동하도록 설정해야 합니다. 유닛 카운터는 목표물을 매우 빠르게 파괴하지만 AI 자체가 목표물의 우선순위를 잘 정하지 못하기 때문에 10대의 탱크가 보병 한 명을 공격하는 동안 뒤에서 탱크가 그들을 공격하는 것을 지켜봐야 했습니다.

문제는 개발자가 너무 많은 것을 원한다는 것입니다: 플레이어가 모든 전투에 집중하는 것에 대한 보상을 원하지만, 그렇게 하면서 동시에 합리적으로 군대를 건설하고 경제를 관리할 수는 없습니다. 건물과 건설을 위한 세로형 커맨드 바가 없는 것은 제 생각에는 정말 아쉬운 부분입니다. 전력을 다한 군대를 보내서 작은 적과 싸웠는데, 약한 것으로 추정되는 유닛 하나가 제 병력을 바로 죽이면 기분이 좋지 않죠.

![](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blta134407d60132fee/66632cab2d69e68eac979ff6/image.png?width=700&auto=webp&quality=80&disable=upscale)

장군들은 C&C4 다음으로 플레이하는 것이 가장 불쾌하다고 느꼈습니다(출처: 작성자).

이 게임은 시리즈 최초의 3D RTS로, 매우 블록적인 폴리곤과 모든 것에 텍스처가 부족하다는 것을 보여줍니다. 제가 좋아하는 제너럴스의한 가지 측면은 제로 아워에 등장하는 다양한 장군들의 하위 진영입니다 . 각 장군은 기본 장군과 비교하여 특정 강점과 약점을 가지면서 진영을 다른 방향으로 밀어붙입니다. 저는 RTS에서 플레이어가 자신의 진영을 커스터마이징하고 표준 빌드 오더를 넘어서는 일을 할 수 있다는 점이 마음에 들어서Age of Empires 3의 고향 도시 개념을 여전히 좋아합니다 . 경쟁적인 RTS 플레이와 UI/UX를 즐기지 않는 저에게 제너럴스는 그다지 매력적이지 않았고, 특히 오리지널을 여기까지 플레이하고 나니 더더욱 그랬습니다.

## 케인 라이즈

커맨드 앤 컨커 3 티베리움 전쟁과 그 확장팩은 팬들에게 티베리움 시리즈의 진정한 결말로 여겨지고 있으며, 지금까지 실제로 플레이하지 않은 저는 그 의견에 동의해야 합니다. 경로 찾기와 일반 AI는 제너럴스보다 훨씬 더 개선되었으며 , 레이저와 샷에 더 많은 효과를 사용하여 3D가 훨씬 더 향상되었으며 그래픽은 오늘날까지도 여전히 유지되고 있습니다.

이 시리즈의 캠페인 구조는 제가 가장 좋아하는 부분으로, 플레이어가 미션을 쉽게 다시 플레이하고, 어떻게 했는지, 무엇을 놓쳤는지 확인할 수 있습니다. 이 게임에는 여전히 마이크로 매니지먼트가 있고 저는 단축키를 좋아하지 않지만, 모든 키를 원하는 대로 다시 바인딩할 수 있다는 점이 마음에 듭니다.

FMV가 돌아온 것은 좋은 일이지만, 분위기가 매우 다르며 어떤 면에서는 90년대에서 2000년대까지 공상 과학과 TV가 어떻게 변화했는지를 나타냅니다. 90년대는 액션 쇼의 캠프와 치즈의 시대였다면, 2000년대는 드라마와 진지함이 더 인기를 끌었던 시기였습니다. 그래도 조 쿠칸은 자신이 무엇을 하는지 잘 알고 있고, 빌리 디 윌리엄스와 마이클 아이언사이드가 GDI에 출연하는 것을 보는 것은 즐거웠습니다.

하지만 게임에는 몇 가지 큰 문제가 있어 점수를 깎아먹었습니다. 게임의 최종 패치는 멀티플레이어의 밸런스를 재조정했지만 싱글플레이어 캠페인에도 영향을 미쳤습니다. 적에게 돈을 쓰지 않아도 말 그대로 방어와 공격을 위해 무한대의 유닛을 쏟아내는 맵이 있습니다. 어떤 맵에서는 적을 공격할 군대를 만들 수 있는 티베리움도 충분하지 않았습니다. 하드 난이도에서 게임을 이기고 싶다면 프로 e스포츠 RTS 플레이어가 되어야 할 것입니다. 팬들이 왜 이 게임을 더 나은 현대 C&C 게임 중 하나로 취급하는지 알 수 있어서 아쉽지만, 대보병 타워가 보병에게 패배하고 대공포가 적 항공기를 막지 못하는 것을 보면 모드 없이 좀 더 캐주얼한 경험을 원한다면 이 상태로는 기본 게임을 완전히 추천할 수 없습니다.

기본 게임 전후에 부족한 부분을 채우는 미션을 추가하고 세 가지 하위 진영을 각각 새롭게 도입한훌륭한 확장팩 케인의 분노로 이러한문제가 해결되었습니다 . 하위 진영에는 각 진영을 다른 방향으로 이끄는 고유한 기술 업그레이드와 유닛이 있습니다. 또한 이 게임은 기본 게임의 대대적인 밸런스 패치 이후에 출시되었기 때문에 전체 캠페인은 멀티플레이어 변경 사항을 중심으로 밸런스가 맞춰져 있습니다. 슬프게도 두 게임 모두 실제 티베리움을 배경으로 한 마지막 게임이기 때문에 두 게임을 모두 플레이하는 것을 추천합니다. 유닛 디자인 측면에서는 전작에 이어 세 진영이 모두 100% 서로 다르며, 이는 Wrath에 도입된 하위 진영을 통해 더욱 뚜렷해졌습니다. 제가 플레이한 게임 중 밸런스 문제에도 불구하고 디자인 측면에서 두 번째로 마음에 드는 게임으로 꼽고 싶습니다.

## 우주!

레드 얼럿 3는 레드 얼럿 프랜차이즈의 마지막 게임으로, 이 게임에서 큰 성공을 거두었습니다. 이 게임은 제작 가치가 가장 높은 게임으로, RTS 중 가장 멋지고 디테일이 뛰어난 유닛이 등장합니다. 특히 모든 유명인이 등장하는 FMV 컷씬은 치즈 팩터의 정점에 달하며 '샤크네이도' 시리즈를 떠올리게 합니다.

저희 게임에는 커맨드 앤 컨커 3처럼완전히 다른 세 개의 진영이 존재하며, 각 진영에는 고유한 유닛이 있습니다. 이 게임은 이전 게임의 카피본이 결코 아니 며,제너럴즈 다음으로 가장 색다른 게임입니다. 모든 맵은 협동 플레이를 위해 설계되었으며, AI는 이 맵에서 정말 잘 작동합니다. 대신 레드 얼럿 3의 맵 디자인은 좋지만, 모든 맵이 2인용으로 설계되어 이전 게임에서 볼 수 있었던 다양한 미션이 부족합니다. 적 AI는 대부분의 맵에서 2 대 1 효과로 인해 플레이어와 같은 게임을 플레이하지 않기 때문에 약합니다. 구조물을 재건하지 않으며, 필수 유닛 생산물을 일찍 저격하면 어떤 맵이든 쉽게 승리할 수 있습니다.

게임 플레이는 시리즈 중 가장 세밀하지만 다른 RTS에 비하면 여전히 낮은 수준입니다. 모든 유닛에는 형태 변경, 특수 공격 발사 등 다양한 기능을 수행할 수 있는 보조 또는 특수 기능이 있습니다. 추적하기가 다소 번거로울 수 있으며, 이것이 제가 C&C 3에 비해 목록에서 더 낮은 순위를 매기는 이유입니다. 전작과 비교했을 때 가장 큰 차이점은 광석 필드당 수확기가 한 대만 허용되어 자원 채집이 훨씬 간편해졌다는 점입니다. 경제를 훨씬 쉽게 설정할 수 있지만 누군가가 경제를 방해하기가 매우 쉬워지고 이전 게임의 고급 플레이 및 경제 전략 중 일부가 제거됩니다.

![](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blta582074486be0a91/66632cd4a63e655057d93f53/image.png?width=700&auto=webp&quality=80&disable=upscale)

이것이 레드얼럿 3의 불합리함을 요약하지 않는다면, 무엇이 더 불합리할지 모르겠습니다. (출처 작성자)

장군의 진영 능력도 돌아와서 플레이어가 전투 중에 더 많은 능력을 사용할 수 있고, 더 많은 마이크로 플레이를 추가할 수 있습니다.

이 확장팩은 케인의 망령에 비해 스토리가 많이 추가되지는 않았지만, 장군 챌린지 모드의 퍼즐 기반 도전이라는 아이디어가 마음에 듭니다. 각 맵은 기본 게임에서는 볼 수 없었던 독특한 상황에서 플레이어가 상대를 상대하도록 도전하며, 모두 혼자서 플레이할 수 있습니다.

전작의다양한 미션과 1 대 1 대결을 기대했다면 레드 얼럿 3는 실망스러울 수 있습니다. 하지만 이 게임은 시리즈의 마지막을 장식하는 작품으로, 게임 플레이와 컷신에서 충분히 다른 점을 확인할 가치가 있습니다.

## 아쉬운 결말

안타깝게도 커맨드 앤 컨커 시리즈의 마지막 게임은 티베리움( ) 트와일라잇으로, EA가 C&C를 정식으로 경쟁 e스포츠화하려는 시도입니다. 훨씬 적은 군대 제한, 항상 온라인 연결, 최악의 멀티플레이어용 계정 진행 상황 등이 특징입니다. 많은 시행착오 끝에 겨우 작동하는 데 성공했지만, 시리즈 중 최악이라는 사실은 쉽게 알 수 있었습니다.

전작의 하위 진영 역할을 하는 다양한 MCV가 있다는 개념은 좋지만, 여기서는 그 방식이 제대로 작동하지 않습니다. 다양한 캐릭터가 작동하도록 하기 위해 하나의 캐릭터(배트맨)를 네 가지로 나눈다는 점에서제가 고담 나이츠를플레이했을 때가 많이 생각납니다 . 여기서는 '방어' 클래스가 아니면 방어를 구축할 수 없습니다. 레드 얼럿 3처럼 협 동 플레이를 할 수 있지만, 여기에는 플레이어를 도와주거나 지원을 제공하는 AI가 없기 때문에 게임의 미션이 근본적으로 깨집니다. 각 플레이어가 건설할 수 있는 유닛이 크게 제한되어 있기 때문에 더 많은 유닛을 생산할 수 있는 AI와 대결하면 숫자 게임에서 절대 이길 수 없으며, 초반에는 진행이 불가능합니다. 저는 싱글플레이어에서 균형을 맞추기 위해 단순히 두 대의 MCV를 지휘할 수 있도록 만들었습니다. 물론 각 병과마다 업그레이드를 받을 수는 있지만 계정 레벨과 연동되어 있기 때문에 싱글플레이는 답답하고 멀티플레이는 계정 0에서 시작하면 불가능하다고 생각됩니다.

![](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltd01ffe322fd6175c/66632cf6fc8ab6320ed8c395/image.png?width=700&auto=webp&quality=80&disable=upscale)

제한된 유닛 풀에서는 전체 계정 시스템 개념이 작동하지 않습니다(출처: 작성자).

유닛마다 개성이 거의 없고 전작에 비해 훨씬 더 많은 유닛이 등장하지만, 이는 새로운 카운터 시스템을 부풀리기 위해 다양한 갑옷 유형을 추가하는 데 사용되어 전작에 비해 상황을 더욱 혼란스럽게 만듭니다. 건물에 대항할 수 있는 유닛이 없기 때문에 다른 MCV와 구조물과 싸우는 데 시간이 오래 걸립니다. 또한 전작의 유쾌한 컷신과 치즈도 사라졌습니다. 네 개의 미션에서 약 3분 정도의 상영 시간을 가진 '아내'가 죽는데, 제 캐릭터가 카메라이고 캠페인 내내 아무 말도 하지 않는다는 점을 고려하면 신경 쓰이기 어렵습니다.

RTS 디자인에 관한 책을 집필 중인데, C&C4에서 더 빠른 속도의 RTS를 만들기 위한 좋은 아이디어가 있었다고 생각하지만 여기서는 그 아이디어가 제대로 구현되지 않았습니다. 낮은 품질의 유닛으로 낮은 유닛 총합을 가질 수 없으며, 대부분의 사람들이 뛰어넘지 않을 계정 레벨에 모든 것을 묶는 것은 나쁜 생각입니다.

## 어떻게 유지되나요?

돌이켜보면 커맨드 앤 컨커는 미학으로 정의할 수 있는 프랜차이즈입니다 .스타크래프트와 같은 수준의 기술적 정밀도와 밸런스를 구현하지는 못했지만,그럴 필요도 없었습니다.멋진 FMV 장면, 다양한 미션과 유닛, 환상적인 음악 덕분에 이 모든 것이 가능했습니다. 아이러니한 점은 EA가 차별화되고 경쟁 친화적으로 만들기 위해 정말 많은 노력을 기울였다고 말할 수 있는 게임들(제너럴스와 C&C4 )이기억에 남지 않는 최악의 작품으로 판명되었다는 점입니다.

또한 오늘날 RTS 디자이너에게 중요한 교훈을 주는 것은 스타일이 많은 게임에서 빠진 요소라는 점입니다. 키로프, 아바타, 심지어 GDI 궤도 레이저처럼 기억에 남는 유닛은 이제 어디에서도 볼 수 없습니다. 유닛의 다양성도 이 게임이 전략과 전술 측면에서 기억에 남는 큰 이유입니다. 저는 여전히 제로 아워와 C&C 3에서와같은 서브 팩션의 아이디어가 가치가 있다고 생각하지만, 아직 다른 스튜디오에서 이런 스타일의 디자인을 활용하는 것을 본 적이 없습니다.

GUI/UX 관점에서 보면 이 시리즈는 먼 길을 걸어왔습니다. 사이드바 GUI는 여전히 제가 가장 좋아하는 기능 중 하나이며, 맵의 어느 곳에서나 유닛을 쉽게 건설할 수 있고,제너럴스가 작동하지 않는 이유이기도 합니다.하지만 모든 게임에서 핫키 표준화가 혼재되어 있고, 유닛 생산에서 컨트롤 그룹을 쉽게 설정할 수 있는 방법이 없다는 점은 캐주얼 플레이어에게 불편함을 줍니다. 레드얼럿 2까지공격 이동 기능이 없었던 것은 정말 아쉬웠습니다. 저에게 있어 GUI와 단축키 디자인의 표준은 여전히 라이즈 오브 네이션즈입니다.

지난 30년 동안 출시된 최고의 RTS 중 몇 가지를 끝내고 추억의 길로 내려가는 것은 씁쓸한 여행이었습니다. 이 시점에서 다시는 키로프 보고에 대한 소식을 들을 수 있을지 모르겠습니다.

RTS 디자인에 대해 더 자세히 알아보려면 게임 디자인 심층 분석이 공개되면 꼭 확인해 보세요.

(https://youtu.be/uJObGmz3fG0)

제가 하는 일을 후원하고매일 더 많은 스트리밍을 할 수 있게 해주고 싶으시다면 제 [후원](https://patreon.com/gwbycer)페이지를 확인해 주세요. [이제](https://discord.gg/XzRdQAXPHh) 게임과 게임 디자인에 대한 이야기를 나눌 수 있는 제 [디스코드가](https://discord.gg/XzRdQAXPHh) 모두에게[열려](https://discord.gg/XzRdQAXPHh) 있습니다.

자세히 읽어보세요:

[추천 블로그인기](https://www.gamedeveloper.com/keyword/featured-blogs)[스토리](https://www.gamedeveloper.com/keyword/top-stories)

[](https://www.linkedin.com/sharing/share-offsite/?url=https://www.gamedeveloper.com/design/a-command-conquer-retrospective)[](https://www.facebook.com/sharer/sharer.php?u=https://www.gamedeveloper.com/design/a-command-conquer-retrospective)[](https://www.twitter.com/intent/tweet?url=https://www.gamedeveloper.com/design/a-command-conquer-retrospective)[](https://www.gamedeveloper.com/cdn-cgi/l/email-protection#c0ffb3b5a2aaa5a3b4fd81e083afadada1aea4e0e6a1adb0fbe083afaeb1b5a5b2e092a5b4b2afb3b0a5a3b4a9b6a5e6a1adb0fba2afa4b9fd89e5f2f0b4a8afb5a7a8b4e5f2f0b4a8a5e5f2f0a6afacacafb7a9aea7e5f2f0a6b2afade5f2f087a1ada5e5f2f084a5b6a5acafb0a5b2e5f2f0ada9a7a8b4e5f2f0a9aeb4a5b2a5b3b4e5f2f0b9afb5eee5f084e5f081e5f084e5f081e5f2f081e5f2f083afadada1aea4e5f2f0e5f2f6e5f2f083afaeb1b5a5b2e5f2f092a5b4b2afb3b0a5a3b4a9b6a5e5f084e5f081a8b4b4b0b3e5f381e5f286e5f286b7b7b7eea7a1ada5a4a5b6a5acafb0a5b2eea3afade5f286a4a5b3a9a7aee5f286a1eda3afadada1aea4eda3afaeb1b5a5b2edb2a5b4b2afb3b0a5a3b4a9b6a5)[](https://www.reddit.com/submit?url=https://www.gamedeveloper.com/design/a-command-conquer-retrospective&title=A%20Command%20%26%20Conquer%20Retrospective)

## 저자 소개

[![Josh Bycer](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt98434093b67825eb/650efd6139ff36eea344b067/bycerportrait.jpg?width=400&auto=webp&quality=80&disable=upscale "Josh Bycer")](https://www.gamedeveloper.com/author/josh-bycer)

[

조쉬 바이서

](https://www.gamedeveloper.com/author/josh-bycer)

Blogger

7년 이상 게임 디자인 분야를 연구하고 기여해 왔습니다. 전문 게임 프로덕션의 QA부터 Gamasutra, Quarter To Three와 같은 사이트의 기사 작성까지 다양한 분야에서 기여하고 있습니다.

제 사이트인 [Game-Wisdom의](https://game-wisdom.com/) 목표는 매니아, 게임 제작자, 일반 팬 등 모든 사람이 게임 산업에 대해 비판적으로 사고하고 게임의 예술과 과학을 살펴볼 수 있는 중앙 집중식 소스를 만드는 것입니다. 또한 [유튜브 채널에서](https://www.youtube.com/c/game-wisdom) 게임 플레이와 분석 영상을 제작하고 있습니다. 전 세계 게임 업계 종사자 500명 이상을 인터뷰했으며, "[공부해야 할 20가지 필수 게임](https://www.crcpress.com/20-Essential-Games-to-Study/Bycer/p/book/9781138341456)"과 "[게임 디자인 심층 분석 플랫포머](https://www.crcpress.com/Game-Design-Deep-Dive-Jumping-Platformers/Bycer/p/book/9780367211387)"를 통해 게임 디자인에 관한 두 권의 저서를 집필했습니다.

[자세한 내용은 Josh Bycer에서 확인하세요.](https://www.gamedeveloper.com/author/josh-bycer)

게임 개발자의 일일 뉴스, 개발자 블로그, 스토리를 받은 편지함으로 바로 받아보세요.

[최신 소식 받기](https://gd-resources.gamedeveloper.com/free/w_gamf01/prgm.cgi)

추천 콘텐츠

* * *

원문: [https://www.gamedeveloper.com/design/a-command-conquer-retrospective](https://www.gamedeveloper.com/design/a-command-conquer-retrospective)