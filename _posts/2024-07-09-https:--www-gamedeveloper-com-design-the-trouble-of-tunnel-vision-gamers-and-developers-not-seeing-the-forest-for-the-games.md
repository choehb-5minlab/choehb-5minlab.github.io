---
title:  "터널 비전 게이머와 개발자의 고민: 게임의 숲을 보지 못함"

categories:
  - 번역
  
tags:
  - Game Developer
toc: true
toc_sticky: true
 
date: 2024-07-09
last_modified_at: 2024-07-09
---
[![Picture of Josh Bycer](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt98434093b67825eb/650efd6139ff36eea344b067/bycerportrait.jpg?width=100&auto=webp&quality=80&disable=upscale "Picture of Josh Bycer")](https://www.gamedeveloper.com/author/josh-bycer)

[조쉬 바이서](https://www.gamedeveloper.com/author/josh-bycer), 블로거

7월 9일, 2024

12 분 읽기

![](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt7b866fa4cf0ce978/66855fef549553212b6d1de6/Pic.png?width=1280&auto=webp&quality=95&format=jpg&disable=upscale)

[](https://www.linkedin.com/sharing/share-offsite/?url=https://www.gamedeveloper.com/design/the-trouble-of-tunnel-vision-gamers-and-developers-not-seeing-the-forest-for-the-games)[](https://www.facebook.com/sharer/sharer.php?u=https://www.gamedeveloper.com/design/the-trouble-of-tunnel-vision-gamers-and-developers-not-seeing-the-forest-for-the-games)[](https://www.twitter.com/intent/tweet?url=https://www.gamedeveloper.com/design/the-trouble-of-tunnel-vision-gamers-and-developers-not-seeing-the-forest-for-the-games)[](https://www.gamedeveloper.com/cdn-cgi/l/email-protection#251a5650474f40465118714d400571574a50474940054a430571504b4b404905734c564c4a4b0562444840575605444b410561405340494a554057561f056b4a51057640404c4b4205514d4005634a5740565105434a5705514d40056244484056034448551e474a415c186c001715514d4a50424d51001715514d40001715434a49494a524c4b4200171543574a480017156244484000171561405340494a554057001715484c424d510017154c4b5140574056510017155c4a500b001561001564001561001564001715714d4000171571574a504749400017154a4300171571504b4b4049001715734c564c4a4b001715624448405756001715444b4100171561405340494a554057560016640017156b4a510017157640404c4b42001715514d40001715634a57405651001715434a57001715514d4000171562444840560015610015644d515155560016640017630017635252520b4244484041405340494a5540570b464a480017634140564c424b001763514d400851574a50474940084a430851504b4b404908534c564c4a4b0842444840575608444b410841405340494a55405756084b4a51085640404c4b4208514d4008434a5740565108434a5708514d40084244484056)[](https://www.reddit.com/submit?url=https://www.gamedeveloper.com/design/the-trouble-of-tunnel-vision-gamers-and-developers-not-seeing-the-forest-for-the-games&title=The%20Trouble%20of%20Tunnel%20Vision%20Gamers%20and%20Developers%3A%20Not%20Seeing%20the%20Forest%20for%20the%20Games)

지난 10년 동안 소셜 미디어에서 발생하는 모든 게임 개발자의 불만 사항을 목격해야 했던 사람으로서, 현실은 같은 논쟁이 반복적으로 발생하는 로그라이크와 같다고 말할 수 있습니다. 최근 소셜 미디어에서 게임 디자인에 대해 가질 수 있는 최악의 생각 중 하나를 완벽하게 요약한 사람을 봤는데, 그 사람이 혼자가 아니었습니다. 게임을 이해하고 분석할 때 많은 개발자와 소비자가 겪는 문제 중 하나는 게임을 특정 관점에서만 바라 보는 것인데, 이제 터널 비전이 게임 디자인에 나쁜 이유에 대해 이야기해 보려고 합니다.

## 마이 웨이 또는 고속도로

터널 비전이란 특정 관점, 즉 자신의 관점에서만 업계와 게임을 바라보는 것을 말합니다. 비평가, 저널리스트, 유튜버, 스트리머, 소비자에게서 이런 모습을 볼 수 있습니다: "나는 게임 X를 좋아하지 않으니 X는 나쁘다" 또는 "나는 이 게임을 정말 좋아하니 완벽해야 한다"는 식입니다.

또한 Balatros, 뱀파이어 서바이버, FTL 등게임이 깜짝 히트작으로 출시될 때마다 이러한 현상을 볼 수 있습니다 . 항상 "이 게임이 왜 이렇게 잘 되죠?"라고 말하는 사람들의 합창을 듣게 됩니다. 그냥 X 때문이야." 게임 디자인 분석은 업계 외부의 사람들뿐만 아니라 일반인들에게도 여전히 미스터리입니다. 게임의 UI/UX, 진행 방식, 느낌을 살펴보고 사람들의 공감을 얻는다는 것은 마법처럼 들릴 수도 있지만, 저처럼 매일 이 일을 하는 사람에게는 숨 쉬는 것만큼이나 쉬운 일입니다.

게임에 대해 이야기하는 많은 사람들의 문제는 '비디오 게임'을 하나의 게임이 모든 게임과 동일하다는 획일적인 용어로 보는 경향이 있다는 것입니다. 즉,콜 오브 듀티를플레이하면 엘든 링이나 스타듀 밸리를 플레이하는 것과 같은 경험을 할 수 있다는 것입니다. 따라서 하나의 게임만 플레이하거나 하나의 게임만 좋아한다면 게임 측면에서 무언가를 구축하는 데 필요한 것은 그것뿐입니다. 또는 한 종류의 게임이 다른 모든 게임을 판단하는 '게임'의 정의가 되어야 한다고 생각하기도 합니다. 이런 사람들은 자신이 좋아하지 않는 장르를 무시하거나 완전히 다른 장르로 뛰어들어 베스트셀러 게임을 만들 수 있다고 생각하는 사람들과 같은 사람들입니다.

소셜 미디어 게시물은 이미 만들어진 것을 모방하려는 특정 게임에 대한 이야기일 수 있지만, 소비자 및 개발자 측에서는 극단적으로 자신의 게임 또는 특정 스타일의 게임만 중요하고 다른 모든 것은 덜 중요하거나 중요하지 않다고 생각하는 사람들이 있습니다.

이제 매번 저를 골치 아프게 하는 터널 비전의 종류에 대해 이야기할 차례입니다.

## 혐오스러운 건전성

이 글을 읽는 여러분도 잘 알고 계시겠지만, 대부분의 비디오 게임은 어떤 종류의 갈등을 극복하거나 싸우는 내용을 담고 있습니다. 그리고 놀랍게도 폭력이 포함된 게임을 하고 싶지 않은 사람들도 있습니다. 그리고 몇 년 전, 게임에서 폭력을 원하지 않는 사람들을 위한 게임이라는 '건전한' 브랜드를 중심으로 새로운 마케팅 용어와 운동이 만들어졌습니다.

그 자체로도 훌륭하지만, 전투가 전혀 없는 다양한 주제와 주제를 탐구하는 아늑한 게임들이 많이 출시되었습니다. 그러나 이를 너무 지나치게 받아들여 건전한 것을 다른 어떤 것보다 더 좋은 것으로 정의하는 사람들과 디자이너들이 있습니다. 그리고 게임이 매력적이고 아늑해 보이지만 건전하다는 그들의 정의에 부합하지 않는다면 게임이 거짓말을 하고 있고 개발자가 속이려 하고 있으며 게임에 문제가 있다고 생각합니다. 또 다른 문제는 게임이 건전해 보이지만 어둡거나 불안한 내용을 담고 있다면 그 게임도 건전하지 않다고 생각하는 것입니다.

![](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt25101ee56035890a/66856012a9e7e5da8639b75e/image.png?width=700&auto=webp&quality=80&disable=upscale)

(일부) 건전한 팬이 원하는 대로 행동할 때와 그렇지 않을 때의 행동 방식

유독한 부정이 있듯이 유독한 긍정도 있는데, 어떤 것이든 좋고 순수해야 하며 잘못되거나 나쁘거나 비판적인 언급은 절대 있어서는 안 됩니다. 다시 말하지만, 개발자가 그런 게임을 만들고 싶다면 그건 괜찮습니다. 문제는 사람들이 그것을 요구하거나 게임이 자신의 관점을 정확히 따르지 않는다면 게임과 디자이너 자신에게 문제가 있는 것입니다.

다른 예시에서도 볼 수 있듯이 자신의 관점에 맞는 극단적인 사례에만 집중하는 것은 비디오게임을 소화하거나 만드는 방법이 아닙니다.

## 단순한 것은 어리석다

비디오게임은 충분히 오래 전부터 존재해 왔기 때문에 여러 번의 디자인 수정과 진화를 거쳤습니다. 가장 큰 변화는 90년대 중반에 일어난 2D에서 3D로의 전환이었습니다. 그럼에도 불구하고 2010년대 인디씬에서는 2D 혁명이 일어났고, 그 결과 가장 멋진 디자인과 플레이를 자랑하는 게임들이 출시되었습니다. 하지만 2D 디자인은 "단순하다"는 소비자들과 팬들의 정서가 존재하며, 이는 진정한 게임, 즉 3D 게임을 만들기 위한 디딤돌이라는 의미로 받아들여지고 있습니다.

디자인을 이해하지 못하는 사람이 2D 게임을 단순하다거나 쉽다고 조롱하는 것은 디자인을 이해하지 못한다는 것을 가장 잘 보여주는 사례 중 하나입니다. 이는 쉬운 게임은 수준 이하의 게임이라고 생각하는 안티 캐주얼 세력의 일부이기도 합니다. 사실 2D 디자인은 수많은 사례가 존재하기 때문에 제대로 하기가 매우 어렵습니다. 할로우 나이트나 오리처럼 2D 공간에서 잘못된 느낌과 플레이를 하는 게임은 무수히 많습니다. 버튼 하나만 누르면 3D 환경을 2D로, 또는 그 반대로 바꿀 수 있다고 생각한다면 결코 훌륭한 게임을 만들 수 없습니다.

아무리 '단순한' 게임이라도 그렇지 않습니다. 너무 많은 개발자와 소비자는 복잡성을 UI/UX의 문제가 아니라 품질의 척도로 간주합니다. 효과적인 게임용 2D 카메라 제작에 대한 이야기는 이 포스팅에서 다루지 않겠습니다.

## 걷는 것에 대한 통곡

문제의 반대편에는 게임이란 결국 세상/공주/우주를 구하고 영웅으로 불려야 하는 것이라고만 생각하는 사람들이 있습니다. 2010년대 디자인이 진화한 이유 중 하나는 이전과는 전혀 다른 게임들이 등장했기 때문입니다. APM과 전투보다는 스토리텔링, 아트, 시네마토그래피에 중점을 둔 타이틀이 등장했습니다.

워킹 시뮬레이터, 비주얼 노벨 또는 게임플레이가 없는 게임을 싫어할 수도 있지만 그렇다고 해서 게임이 아니라는 뜻은 아닙니다. 다시 말하지만, 슬픈 음악과 텍스트를 화면에 띄우고 천천히 걷는다고 해서 비디오 게임이 피카소와 같은 작품이 될 수 있다고 생각한다면 그것은 잘못된 생각입니다. 좋은 2D 디자인과 나쁜 2D 디자인 사이에는 큰 차이가 있듯이 스토리 중심의 좋은 게임과 나쁜 게임 사이에도 큰 차이가 있습니다.

## 게임은 예술입니다(멋진 폰트 삽입)

이제 비디오 게임에 대한 끝없는 논쟁으로 넘어가겠습니다. 비디오 게임은 예술입니다. 이 점은 '예술'이라고 하면 어린 시절의 핵심 기억을 불러일으키고, 레벨에 숨겨진 비밀을 찾기 위해 3단 벽 점프 다이빙을 하는 기쁨이 아니라 게임을 보고 주체할 수 없이 울음을 터뜨리는 것만을 떠올리는 사람들의 생각에서 나온 말입니다.

현대의 많은 디자이너들은 무엇보다도 스토리에 집중하는 게임을 완벽한 게임으로 여깁니다. 비디오 게임이 고전 영화나 시에서 영감을 얻거나 아리스토텔레스를 언급하지 않는다면 그 게임은 쓰레기라는 것이 이들의 생각입니다. 이는 앞서 2D 디자인을 3D에 비해 수준이 낮다고 보고, "대통령이 닌자에게 납치당했다"로 전체 스토리를 요약할 수 있는 게임을 플레이하는 것은 거의 수준 이하라고 생각한 것과 같은 맥락입니다.

제가 읽은 소셜 미디어 게시물의 일부인데, 요즘 디자이너들은 다른 게임에서 영감을 받을 뿐 다른 어떤 것에서도 영감을 얻지 못하고 있으며, 이는 그들에게 문제가 되고 있습니다.

결국, 비디오게임을 만들고 싶다면 충격적으로도 비디오게임을 플레이하고 공부해야 합니다. 비디오게임은 예술일 뿐만 아니라 이제 하나의 매체이며, 화가가 다른 그림에서 영감을 얻을 수 있는 것처럼 디자이너도 다른 게임에서 영감을 얻을 수 있습니다. 처음 게임을 개발하는 개발자와 학생들이 뛰어난 게임을 많이 만드는 이유는 그들이 수많은 게임, 특히 영감을 받은 게임을 플레이하면서 게임을 연구하고 게임에서 원하는 것이 무엇인지 배웠기 때문입니다.

![](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt0430b7eb05ea7e11/6685603e6b429c39c38ac7cb/image.png?width=700&auto=webp&quality=80&disable=upscale)

비디오 게임은 플레이 가능한 예술이며, 소비자층을 확보하려면 '플레이 가능'이라는 부분이 중요합니다.

저는 오브라 딘의 귀환, 펜티먼트 등 스토리텔링에 중점을 둔 게임을 좋아하는 게임으로 꼽는 디자이너들로부터 이러한 예술적 논의를 많이 들었습니다 . 하지만이 두 게임은 완벽한 게임이나 대중적인 인기를 끌었던 게임도 아니며, 제가 틀렸다거나 반론자라는 메시지를 보내기 전에 소비자층이 그렇게 말한 것은제가 아닙니다 . 비평가들이나 다른 디자이너들이 최고의 게임이라고 호평하는 게임에서 소비자층은 정반대의 반응을 보이는 경우를 많이 볼 수 있습니다. [ROD](https://steamcommunity.com/stats/653530/achievements) [](https://steamcommunity.com/stats/653530/achievements)는 [6개의 운명을 풀기도 전에 Steam에서 플레이어의 40%를 잃었고](https://steamcommunity.com/stats/653530/achievements), [펜티먼트는 1막을 클리어하기도 전에 54%의](https://steamcommunity.com/stats/1205520/achievements) 이탈률을 기록했습니다. 전에도 말씀드렸지만, 게임을 정말 좋아하거나 최고의 게임이라고 생각한다고 해서 게임의 모든 요소가 소비자에게 통하거나 완벽하다는 의미는 아닙니다. 디자이너로서 게임을 이해하고 성장하는 방법 중 하나는 게임을 객관적으로 바라보고 UI/UX를 개선할 수 있는 방법을 찾는 것입니다.

매우 예술적인 게임도 양극화가 심하고, 게임플레이가 다른 게임에 대한 높은 이탈률은 예상할 수 있습니다. 그러나 게임을 구매한 소비자층의 절반 이상이 이탈한 게임을 게임이 예술이라거나 모든 면에서 완벽하다는 증거로 간주해서는 안 되며, 그 게임의 매출을 다른 게임도 잘 될 것이라는 의미로 간주해서는 안 됩니다. 게임은 예술이기는 하지만 여전히 소비자가 즐기는 제품이며, 소비자가 게임을 즐기지 않는다면 다음 게임을 위해 이해해야 할 문제가 있는 것입니다.

## 게임과 게이머에 대한 혐오

마지막으로, 소셜 미디어에서 게임 업계의 '크리에이티브'를 바라보는 시각에 대한 논란이 있었습니다. 2D를 3D의 디딤돌로 보는 사람들이 있듯이, 비디오 게임을 영화, TV 등 '진짜 예술'로 가는 디딤돌로 보는 사람들이 있는 것 같습니다. 이러한 현상은 AAA급 게임 분야에서 볼 수 있는데, 대규모 예산이 투입된 게임의 디자이너와 스튜디오는 이제 게임 팬층을 넘어 외부에서도 인정받고 축하받고 있습니다. 이들은 자신이 만든 게임에 대해 이야기할 때 디자인, 개발팀, 구현에 대해 이야기하지 않고 게임의 문화적 영향과 게임을 만든 영광에 대해서만 이야기합니다.

![](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt03d0bb0dcfc918d8/66856074ca9a04eec11be91b/image.png?width=700&auto=webp&quality=80&disable=upscale)

사람들이 코지마 히데오의 게임에 대해 오해하는 것은 스토리가 게임플레이보다 우선한다는 것인데, 그는 항상 오리지널 스토리에 맞는 독창적인 게임플레이를 디자인합니다.

사람들이 비디오 게임을 다른 매체로 번역하려고 할 때, 게임을 1:1로 만들려고 무리하게 시도하거나 게임 속 모든 것을 알아볼 수 없을 정도로 제거할 때 이런 일이 벌어집니다. 그들은 비디오게임이라는 매체를 이해하지 못하고 있으며, 비디오게임이 다른 모든 것과는 다른 합법적인 매체라는 것을 이해하지 못하고 있습니다. 업계 안팎에는 여전히 비디오게임을 좋아하지 않는 사람들이 있습니다. 다른 모든 매체가 다른 것의 하위 버전으로 취급받던 시기가 있었던 것처럼 말입니다. 만화와 애니메이션은 오랫동안 TV와 영화에 비해 '하위'로 여겨져 경력이 바닥을 치고 있을 때 만화 VA를 하는 것으로 여겨졌습니다. 2000년대 중반, 어쩌면 2010년대 초반이 되어서야 만화와 게임의 성우가 유명 배우를 고용해 최신 GTA나 애니메이션 영화의 목소리를 맡기는 것과함께 존경과 찬사를 받게 되었습니다.

이 시점에서 게임 산업은 다른 '유명한' 매체보다 더 많은 돈을 벌고 있으며, 존중을 받고 독자적으로 서야 할 시기를 지나고 있습니다.

## 게임의 다양성

비디오 게임은 획일적이지 않습니다. 케이팝을 들으며 토끼를 타고 당근을 모으는 비디오 게임은 사랑하는 사람이 세상을 떠난 후 슬픔을 탐구하는 게임과 마찬가지로 정당한 게임입니다. 특정 스타일의 게임이나 장르만 좋아하는 것이 잘못된 것은 아니지만, 그것만 '허용'되고 다른 것은 '잘못된 것'이라고 생각한다면 문제가 있습니다. 그리고 앞서 언급한 것처럼 터널 비전에 시달리는 디자이너라면, 자신의 게임이 훌륭하다고 생각하거나 동료 친구나 디자이너가 그렇게 생각한다고 해서 모든 소비자가 게임을 40초 만에 그만둔다고 해서 큰 의미가 없다는 것을 이해하고 자기만의 생각에서 벗어날 필요가 있습니다.

제가 하는 일을 후원하고매일 더 많은 스트리밍을 할 수 있게 해주고 싶으시다면 제 [Patreon을](https://patreon.com/gwbycer)확인해 주세요. [이제](https://discord.gg/jGWxsj2eZH) 누구나 게임과 게임 디자인에 대해 이야기할 수 있도록 내 [Discord가 열려](https://discord.gg/jGWxsj2eZH) 있습니다.

자세히 읽어보세요:

[블로그추천](https://www.gamedeveloper.com/keyword/blogs)[블로그톱](https://www.gamedeveloper.com/keyword/featured-blogs)[스토리](https://www.gamedeveloper.com/keyword/top-stories)

[](https://www.linkedin.com/sharing/share-offsite/?url=https://www.gamedeveloper.com/design/the-trouble-of-tunnel-vision-gamers-and-developers-not-seeing-the-forest-for-the-games)[](https://www.facebook.com/sharer/sharer.php?u=https://www.gamedeveloper.com/design/the-trouble-of-tunnel-vision-gamers-and-developers-not-seeing-the-forest-for-the-games)[](https://www.twitter.com/intent/tweet?url=https://www.gamedeveloper.com/design/the-trouble-of-tunnel-vision-gamers-and-developers-not-seeing-the-forest-for-the-games)[](https://www.gamedeveloper.com/cdn-cgi/l/email-protection#78470b0d1a121d1b0c452c101d582c0a170d1a141d58171e582c0d16161d14582e110b111716583f19151d0a0b5819161c583c1d0e1d1417081d0a0b425836170c582b1d1d11161f580c101d583e170a1d0b0c581e170a580c101d583f19151d0b5e191508431a171c0145315d4a480c10170d1f100c5d4a480c101d5d4a481e171414170f11161f5d4a481e0a17155d4a483f19151d5d4a483c1d0e1d1417081d0a5d4a4815111f100c5d4a4811160c1d0a1d0b0c5d4a4801170d565d483c5d48395d483c5d48395d4a482c101d5d4a482c0a170d1a141d5d4a48171e5d4a482c0d16161d145d4a482e110b1117165d4a483f19151d0a0b5d4a4819161c5d4a483c1d0e1d1417081d0a0b5d4b395d4a4836170c5d4a482b1d1d11161f5d4a480c101d5d4a483e170a1d0b0c5d4a481e170a5d4a480c101d5d4a483f19151d0b5d483c5d4839100c0c080b5d4b395d4a3e5d4a3e0f0f0f561f19151d1c1d0e1d1417081d0a561b17155d4a3e1c1d0b111f165d4a3e0c101d550c0a170d1a141d55171e550c0d16161d14550e110b111716551f19151d0a0b5519161c551c1d0e1d1417081d0a0b5516170c550b1d1d11161f550c101d551e170a1d0b0c551e170a550c101d551f19151d0b)[](https://www.reddit.com/submit?url=https://www.gamedeveloper.com/design/the-trouble-of-tunnel-vision-gamers-and-developers-not-seeing-the-forest-for-the-games&title=The%20Trouble%20of%20Tunnel%20Vision%20Gamers%20and%20Developers%3A%20Not%20Seeing%20the%20Forest%20for%20the%20Games)

## 저자 소개

[![Josh Bycer](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt98434093b67825eb/650efd6139ff36eea344b067/bycerportrait.jpg?width=400&auto=webp&quality=80&disable=upscale "Josh Bycer")](https://www.gamedeveloper.com/author/josh-bycer)

[

조쉬 바이서

](https://www.gamedeveloper.com/author/josh-bycer)

Blogger

7년 이상 게임 디자인 분야를 연구하고 기여해 왔습니다. 전문 게임 프로덕션의 QA부터 Gamasutra, Quarter To Three와 같은 사이트의 기사 작성에 이르기까지 다양한 분야에서 기여하고 있습니다.

제 사이트인 [Game-Wisdom의](https://game-wisdom.com/) 목표는 매니아, 게임 제작자, 일반 팬 등 모든 사람이 게임 산업에 대해 비판적으로 사고하고 게임의 예술과 과학을 살펴볼 수 있는 중앙 집중식 소스를 만드는 것입니다. 또한 [유튜브 채널에서](https://www.youtube.com/c/game-wisdom) 게임 플레이와 분석 영상을 제작하고 있습니다. 전 세계 게임 업계 종사자 500명 이상을 인터뷰했으며, "[공부해야 할 20가지 필수 게임](https://www.crcpress.com/20-Essential-Games-to-Study/Bycer/p/book/9781138341456)"과 "[게임 디자인 심층 분석 플랫포머](https://www.crcpress.com/Game-Design-Deep-Dive-Jumping-Platformers/Bycer/p/book/9780367211387)"를 통해 게임 디자인에 관한 두 권의 저서를 집필했습니다.

[자세한 내용은 Josh Bycer에서 확인하세요.](https://www.gamedeveloper.com/author/josh-bycer)

게임 개발자의 일일 뉴스, 개발자 블로그, 스토리를 받은 편지함으로 바로 받아보세요.

[최신 소식 받기](https://gd-resources.gamedeveloper.com/free/w_gamf01/prgm.cgi)

추천 콘텐츠

* * *

원문: [https://www.gamedeveloper.com/design/the-trouble-of-tunnel-vision-gamers-and-developers-not-seeing-the-forest-for-the-games](https://www.gamedeveloper.com/design/the-trouble-of-tunnel-vision-gamers-and-developers-not-seeing-the-forest-for-the-games)