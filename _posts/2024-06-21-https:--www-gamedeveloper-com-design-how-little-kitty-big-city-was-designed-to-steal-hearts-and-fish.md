---
title:  "리틀 키티, 빅 시티가 하트(와 물고기)를 훔치는 방법"

categories:
  - 번역
  
tags:
  - Game Developer
toc: true
toc_sticky: true
 
date: 2024-06-21
last_modified_at: 2024-06-21
---
[![Picture of John Harris](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt1cb9265591310a0b/65088b4ae874592feee571e6/Game_Developer_G_Logo_RGB.png?width=100&auto=webp&quality=80&disable=upscale "Picture of John Harris")](https://www.gamedeveloper.com/author/john-harris)

[존 해리스](https://www.gamedeveloper.com/author/john-harris), 기여자

6월 20, 2024

12 분 읽기

![](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt5dcd12fd617db62c/66743dfcc76eb159ee0f744b/ss_1a7ec894fc2fb8ebd8d659e689e6c2f67834f523.jpg?width=850&auto=webp&quality=95&format=jpg&disable=upscale)

Double Dagger Studio 이미지 제공.

[](https://www.linkedin.com/sharing/share-offsite/?url=https://www.gamedeveloper.com/design/how-little-kitty-big-city-was-designed-to-steal-hearts-and-fish)[](https://www.facebook.com/sharer/sharer.php?u=https://www.gamedeveloper.com/design/how-little-kitty-big-city-was-designed-to-steal-hearts-and-fish)[](https://www.twitter.com/intent/tweet?url=https://www.gamedeveloper.com/design/how-little-kitty-big-city-was-designed-to-steal-hearts-and-fish)[](https://www.gamedeveloper.com/cdn-cgi/l/email-protection#516e2224333b3432256c193e26711d3825253d34711a382525287d711338367112382528712630227135342238363f343571253e71222534303d713934302325227179303f3571373822397877303c216a333e35286c1874636125393e24363925746361253934746361373e3d3d3e26383f3674636137233e3c74636116303c34746361153427343d3e2134237463613c38363925746361383f253423342225746361283e247f746115746110746115746110746361193e267463611d3825253d347463611a382525287463127463611338367463611238252874636126302274636135342238363f3435746361253e746361222534303d74636139343023252274636179303f35746361373822397874611574611039252521227462107463177463172626267f36303c34353427343d3e2134237f323e3c74631735342238363f746317393e267c3d3825253d347c3a382525287c3338367c323825287c2630227c35342238363f34357c253e7c222534303d7c3934302325227c303f357c37382239)[](https://www.reddit.com/submit?url=https://www.gamedeveloper.com/design/how-little-kitty-big-city-was-designed-to-steal-hearts-and-fish&title=How%20Little%20Kitty%2C%20Big%20City%20was%20designed%20to%20steal%20hearts%20(and%20fish))

아파트 창문에서 길거리로 떨어진 작은 검은 고양이 한 마리가 다시 살아나려면 한참 멀었습니다. 하지만 다행히도 이 동네는 꽤 한적한 동네이고, 차도 없고, 동물들도 친절하며, 흥미로운 장소가 많아요. 집에 돌아가는 건 좀 더 기다려도 되겠죠? 더블 대거의 멋진 탐험형 3D 플랫포머 [리틀 키티, 빅 시티의](https://store.steampowered.com/app/1177980/Little_Kitty_Big_City/)배경이 바로 이곳입니다. 이 스튜디오의 설립자와 함께 게임을 성공적으로 홍보한 비결, 주인공인 고양이의 독특한 몸짓 언어, 낮은 판돈과 차분한 분위기로 몰입도가 높은 환경을 조성하는 방법에 대해 이야기를 나눠보았습니다.  

게임 개발자: 여러분은누구이며 ,리틀 키티, 빅 시티는 어떤 게임인가요?

매트 T. 우드: 안녕하세요, 매트 T. 우드입니다. 저는 1998년부터 게임 업계에 종사해 왔습니다. 리틀키티, 빅 시티 이전에는 Valve에서 16년 동안 근무하며 수많은 모자를 쓰고 하프라이프 2, 레프트 4 데드, 포털 2, 카운터 스트라이크 같은 게임을 개발 했습니다. 2019년에는 혼자서 도전하기로 결심하고 더블 대거 스튜디오를 설립했습니다. 그리고 몇 년 후, 첫 번째 게임인 리틀키티, 빅 시티를 출시했습니다 !

리틀 키티, 빅 시티는 출시된 지 얼마 되지 않았지만 벌써 입소문이 꽤 났어요! 홍보용 게임이 최고 수준인 것 같습니다. 몇 가지 팁을 알려주시겠어요?

우드: 저는 판매할 의도로 무언가를 만드는 것을 중요하게 생각합니다. 즉, 개발 프로세스 초기에 시장성과 브랜드에 대해 생각해야 합니다. "이 게임의 어떤 점이 흥미로워서 사람들이 매력을 느낄까?", "어떻게 하면 사람들의 시선을 사로잡고 다른 사람들 사이에서 돋보일 수 있는 방식으로 브랜드를 시각적으로 표현할 수 있을까?" 같은 질문을 스스로에게 던집니다. 이렇게 하면 사람들의 시선을 사로잡을 때가 왔을 때 훨씬 더 쉬워집니다.

사람들이 게임을 주목하게 만드는 아주 간단한 트릭이 많이 있습니다(솔직히 사람들이 더 많이 사용해야 한다고 생각합니다). 하나는 브랜딩의 어딘가에 항상 풀 프레임 얼굴을 배치하는 것입니다. 사람들은 자연스럽게 얼굴과 눈에 끌립니다. 제 경우에는 귀여운 고양이가 그려져 있어도 나쁘지 않다고 생각해요. 하지만 한 그룹이 웹사이트나 잡지를 스캔할 때 사람들의 눈을 추적한 결과, 사람들은 항상 얼굴에 먼저 끌렸다는 기사를 읽은 기억이 납니다. 그 트릭을 이용해 사람들의 관심을 끌 수 있다면, 그다음은 어려운 부분인데 그걸 유지해야 하죠!

게임 홍보를 위해 저는 주로 트위터라는 한 가지 플랫폼만을 고수했습니다. 별다른 생각 없이 작업하다가 즉흥적으로 올리는 것이 제 스타일과 일정에 맞았기 때문이죠. 다른 소셜 미디어 사이트에는 훨씬 더 많은 시간과 노력, 계획이 필요했고, 게임도 만들고 있었기 때문에 제 생각에는 시간을 잘 활용하지 못했습니다!

하지만 프로젝트 후반부에 팝파젠다의 훌륭한 직원들과 함께 일하면서 훨씬 더 많은 미디어 기회를 얻을 수 있었어요. 그리고 훌륭한 소셜 미디어 담당자인 Shan Moran을 고용할 수 있었죠. 저는 게시물을 작성할 뿐만 아니라 카툰과 아트도 제작할 수 있는 소셜 미디어 담당자를 원했습니다. 섄은 이 역할에 완벽했습니다.

![Little Kitty Big City Duckling Laundromat Screenshot](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt544e9f6e9cb4be7f/66743ec11ab595a01aebfc1b/ss_38521d84439452f27ccdb098b8b4e6bf31e092d4.jpg?width=700&auto=webp&quality=80&disable=upscale "Little Kitty Big City Duckling Laundromat Screenshot")

더블 대거 스튜디오 이미지 제공.

리틀 키티, 빅 시티를 다른 대형 고양이 게임인 스트레이와비교하고 싶지만, 실제로는 고양이가 등장하는 것 외에는 공통점이 거의 없습니다. 게임 플레이는 특히 신선합니다. 체력 측정기, 위험, 생명, 사실상 실패 상태도 없습니다. "판돈"이 없을 때 플레이어의 참여를 유도하는 데 어려움이 있다고 생각하시나요?

우드: 플레이어의 몰입도를 유지하는 것은 확실히 제가 걱정 했던 부분입니다. 과거에 플레이어의 참여를 유도한 경험은 부분적으로는 갈등을 통해, 부분적으로는 퍼즐 디자인을 통해 이루어졌습니다. 리틀 키티, 빅 시티에는 가벼운 퍼즐이 몇 개 있지만 , 큰 갈등이 없기 때문에 디자이너인 저에게는 새로운 영역이었습니다.

개발 도중에 우연히 발견한 점도 있습니다. 저는 RPG를 할 때 메인 퀘스트는 절대 하지 않고 사이드 퀘스트와 활동으로 정신이 산만해져서 돌아다니는 경우가 많았습니다. 제가 해야 할 일을 제외한 모든 것을 탐험하고 하는 것이 저를 행복하게 합니다. 그러니 작년에 47살의 나이에 부주의형 ADHD 진단을 받은 것도 당연한 일인 것 같아요.

그래서 어쨌든.... 이렇게 반복적으로 게임의 구조를 설계하게 되었고, 무엇이 형성되고 있는지 깨닫고 나니 분명해졌습니다. 이 게임은 산만함에 관한 게임이었어요. 메인 퀘스트는 상당히 쉽게 달성할 수 있도록 만들었지만, 플레이어가 시간이나 부담감, 잔소리에 신경 쓰지 않고 자유롭게 저쪽을 탐험하거나 다른 것에 집중할 수 있도록 유도했습니다. 그냥 구불구불 돌아다니며 즐기세요.

고양이를 해칠 수 있는 방법이 없다는 점도 이 게임을 놀이터처럼 느끼게 하는 데 도움이 됩니다. 여기에 경쾌한 재즈 사운드트랙이 더해져 즐겁고 유쾌한 느낌을 주는데, 이는 플레이어가 위험 부담 없이 자유롭게 무언가를 시도할 수 있도록 하는 데 필수적인 요소입니다. 명백한 위험이 없기 때문에 디자인에 제약이 있었나요? 처음부터 그런 식으로 계획했나요?

우드: 사실 저는 '스릴 넘치는' 게임을 만들고 싶었지만, 첫 번째 본능이자 첫 번째 프로토타입은 서바이벌 같은 게임이었어요. 실제로 길거리에서 살아남아야 하고, 음식과 물이 필요하며, 하루 주기가 있다는 아이디어였죠. 잠시 플레이하다가 원래 목표에서 너무 멀리 벗어났다는 것을 깨달았고, 고양이가 고군분투하고 결국 실패하도록 강요하지 않고는 재미있게 만들 수 없다는 것을 깨달았습니다. 더 많이 생각하고 가족과 친구들에게 설명할수록 작은 고양이가 고군분투하거나 실패하거나 다치는 모습은 사람들이 경험하고 싶어 하지 않는다는 것을 깨달았습니다. 그래서 방향을 바꿨죠. 그다음에는 실패 상태나 충돌이 없는 게임에서 무엇을 했는지 알아내기만 하면 됐죠.

처음부터 아이들과 함께 즐길 수 있는 게임을 만들고 싶다는 생각을 했어요. 탐험을 장려하고, 키티를 다치게 하지 않으며, 호기심과 발견을 장려하는 것이 제 목표였죠. 몇 가지 아이디어가 있었지만, 대부분 새로운 영역이었기 때문에 충돌 없이 즐길 수 있는 다른 훌륭한 게임을 찾아보았습니다. 동물의 숲, 마리오 오디세이의 일부 ,브레스 오브 더 와일드의 일부 , 그리고 짧은 하이킹, 피쿠니쿠, 알바 같은 수많은 PC 인디 게임 같은게임들이었습니다 :야생동물 어드벤처, 슬라임 랜처, 모든 속팝 게임, 도넛 카운티....이것들은모두 저에게 큰 영감이 되었습니다.

재즈 사운드트랙은 당연한 선택처럼 느껴졌어요. 고양이는 항상 재즈와 연관이 있었고, 작곡가인 라일리 코닉은 제 모든 엉뚱한 영감을 받아 게임에 완벽하고 유쾌한 사운드트랙을 만들었죠.

![Little Kitty Big City Grocer Screenshot](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt8dc1d555d4a445c9/66743de361be53d513014a9a/ss_b977859322e50fa998f7fa9328e4ed28dbd9f1ad.jpg?width=700&auto=webp&quality=80&disable=upscale "Little Kitty Big City Grocer Screenshot")

더블 대거 스튜디오 이미지 제공.

영감을 받은 또 다른 게임은 언타이틀드 구스 게임(Untitled Goose Game)입니다. 장난스러운 장난이 가능하고, 널리 퍼져 있으며, 눈에 띄는 것은 물론 얼굴 없는 인간 캐릭터는 같은 세계의 다른 마을인언타이틀드 구스 게임의 영국/호주 마을 주민과 일본인의 모습 처럼 보이기도 합니다. 의도한 의도인가요, 아니면 사람의 얼굴을 묘사하지 않은 것이 캐릭터를 묘사하는 데 어떤 도움이 되나요?

우드: 대부분의 고양이 보호자들은 고양이가 진짜 주인이고 우리는 그저 음식과 쉼터, 관심을 제공하기 위해 존재하는 것처럼 느껴질 때가 있다고 생각합니다. 그런 관점을 반영하고 싶었기 때문에 인간 캐릭터는 상당히 단순하고 얼굴이 없습니다. 고양이에게 인간은 배경에서 움직이는 물체에 불과합니다. 그리고 무언가에 얼굴을 부여하면 사람들은 그 대상에 더 공감하는 경향이 있기 때문에 플레이어가 동물보다 인간을 더 연상하게 하고 싶지 않았어요.

예술적 관점에서 보면 오브젝트에 디테일을 더할수록 플레이어는 더 많은 관심을 기울이게 됩니다. 인간은 '움직이는 오브젝트'에 불과하기 때문에 훨씬 더 디테일한 동물 캐릭터와 달리 단순하고 환경과 유사한 모델을 유지하는 것이 합리적이라고 생각했습니다.

오픈 월드 게임은 소규모 팀으로 제작하기 어려워 보입니다. 야생의 숨결이나 왕국의 눈물 같은 게임을만들려면 수백 명의 인원이 지형을 만들어야 합니다.리틀 키티, 빅 시티의 범위는 훨씬 작지만 쉽지 않은 것 같습니다. 어떻게 하셨나요?

우드: 그 과정에서 실수도 많이 했어요. 하지만 결국에는 맵에 밀도와 수직성을 더하는 데 집중했습니다. 플레이어가 거리 레벨에서 모든 것을 탐험했더라도 울타리 뒤나 테라스에 올라가면 여전히 더 많은 것을 발견할 수 있습니다. 또한 메트로바니아에서 영감을 받아 분명 탐험할 수 있지만 플레이어가 게임을 더 진행하기 전까지는 도달할 수 없는 지역을 만들었습니다.

고양이의 애니메이션은 매우 잘 관찰되었고, 달릴 때 귀가 뒤로 접히는 방식이나 낮은 통로를 통과하는 방식과 같은 사소한 디테일이 풍부했습니다. 또한 기차처럼 앞쪽과 뒤쪽이 연결되어 있고 운전석이 엔진을 따라 움직이는 것처럼 제어하는 것도 발견했습니다. 이 관찰이 얼마나 정확한지는 모르겠지만, 이런 방식으로 제어하는 것 같아서 흥미롭다고 생각했습니다. 키티 애니메이션에 대한 인사이트가 있나요?

우드: 저희는 고양이 동영상을 많이 봤 습니다.[캐릭터에 작은 디테일을 많이 더](https://www.gamedeveloper.com/art/deep-dive-how-little-kitty-big-city-rejects-realism-to-achieve-authenticity)한 Micah Breitweiser에게 정말 많은 공을 돌리고 싶습니다! 그는 고양이가 몸짓으로 의사소통하는 방식과 그 움직임을 애니메이션으로 변환하는 방법을 모두 훌륭하게 이해하고 있습니다.

하지만 움직임과 몇 가지 다른 것들은 수작업으로 만든 애니메이션과 게임 내 역동적인 실시간 뼈의 움직임이 결합된 것입니다. 고양이는 부드러운 곡선으로 움직이기 때문에 모든 상황에서 동적으로 움직이게 하기가 어려웠기 때문에 저는 절차적 조합이 최선의 해결책이라고 판단했습니다.

![Little Kitty Leap Screenshot](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt1dc7e5df889334c7/66743e51db6edf115dee177f/ss_c4f23f25a83f230997518faab40e26d224559925.jpg?width=700&auto=webp&quality=80&disable=upscale "Little Kitty Leap Screenshot")

더블 대거 스튜디오 이미지 제공.

월드 내비게이션은 대부분 간단하고 직관적이었습니다. 점프 버튼을 누르고 있으면 게임에 호와 목적지가 표시되고, 이를 조정할 수 있습니다. 다른 게임에서도 이 기능을 사용했는지는 모르겠지만, 이 기능이 없었다면 고양이를 조종하는 것이 훨씬 더 어려웠을 거예요. 처음부터 고양이를 그런 방식으로 제어할 계획이었나요?

우드: 아크 점프 또는 제가 "정밀 점프"라고 부르는 것은 아주 초기에 구현되었지만, 출시 당시에는 훨씬 더 단순했습니다. 저는 게임이 편안하게 느껴지길 원했기 때문에 모든 점프를 정렬하는 데 시간을 들이는 것이 좋은 생각인 것 같았습니다. 하지만 첫 번째 버전을 구현하고 사람들에게 플레이하게 했더니 너무 느려서 플레이어들이 더 빨리 점프할 수 있게 해달라고 요청했습니다. 그래서 저는 빠른 버전을 구현했는데, 내부적으로는 거의 똑같은 점프이지만 모든 타겟팅을 보이지 않게 처리할 뿐입니다.

다른 게임에도 이런 기능이 있는지 모르겠습니다. 저는 고양이가 뛰어오를 준비를 하고 목적지로 튀어 오르는 모습을 상상하니 이치에 맞는 것 같았습니다.

진행은 물고기를 찾는 것으로 시작되는데, 이는 체력을 증가시키는 왕국의 눈물에서신전 오브의 맛있는 버전이라고 생각할 수 있습니다.브레스 오브 더 와일드 게임에서는 물고기가 필요 이상으로 도움이 되지만 ,리틀 키티, 빅 시티에서는 모든 물고기가 필요하도록 설계된 것 같습니다. 스피드 러너가 이 설계를 깨뜨릴 수 있는 방법을 찾을 수 있을까요?

나무요: 물론이죠. 스피드 러너들은 이미 물고기 없이도 30초 이내에 게임을 이긴 적이 있습니다. 정말 대단하죠! 기술적으로는 고급 전략이나 글리치를 사용하지 않고도 물고기 세 마리만 가지고도 집에 도착할 수 있습니다. 원래는 한 마리만 가지고 집에 돌아가고 다른 물고기는 사이드 퀘스트를 수행하기 위해 더 가질 수 있게 하려고 했지만, 대부분의 사람들이 누군가에게서 물고기를 훔치는 기쁨을 경험하길 바랐습니다.

![Little Kitty With A Fish Screenshot](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt602f13e56049ce56/66743e7cdb6edf3857ee1784/ss_cc093f88bbdc4cbcf07fbb69ce601d68974576e4.jpg?width=700&auto=webp&quality=80&disable=upscale "Little Kitty With A Fish Screenshot")

Double Dagger Studio 이미지 제공.

마지막으로, 저는 이 결정을 전적으로 지지하지만 이 게임이 특별히 일본 도시를 배경으로 한 이유는 무엇인가요? 그냥 고양이가 탐험하기에 좋은 장소처럼 보였나요?

우드: 처음 일본을 방문했을 때 도시와 마을의 매력에 푹 빠졌어요. 저는 어떤 식으로든 '유용하다'는 확신이 들지 않으면 어떤 주제에 대해 깊이 파고들지 못하는 문제도 있습니다(저주 같은 거죠). 그래서 일본식 도시 디자인을 연구하고 탐구하고 싶었기 때문에 게임을 일본으로 설정한 것이 완벽한 핑계가 되었죠, 하하. 물론 이는 부분적인 이유일 뿐입니다. 제 마음속에는 고양이와 도쿄 거리에 대한 강한 연상이 있습니다. 게다가 '치의 스위트 홈', '고양이 초보자', 80년대 만화 '마이클이 뭐길래'와 같은 일본 고양이 미디어의 팬이기도 했으니 당연한 일이었죠.

자세히 읽어보세요:

[인터뷰Q&A의특징톱](https://www.gamedeveloper.com/keyword/features)[스토리](https://www.gamedeveloper.com/keyword/top-stories)

[](https://www.linkedin.com/sharing/share-offsite/?url=https://www.gamedeveloper.com/design/how-little-kitty-big-city-was-designed-to-steal-hearts-and-fish)[](https://www.facebook.com/sharer/sharer.php?u=https://www.gamedeveloper.com/design/how-little-kitty-big-city-was-designed-to-steal-hearts-and-fish)[](https://www.twitter.com/intent/tweet?url=https://www.gamedeveloper.com/design/how-little-kitty-big-city-was-designed-to-steal-hearts-and-fish)[](https://www.gamedeveloper.com/cdn-cgi/l/email-protection#724d010710181711064f3a1d05523e1b06061e1752391b06060b5e52301b1552311b060b52051301521617011b151c171652061d52010617131e521a1713000601525a131c1652141b011a5b54131f0249101d160b4f3b574042061a1d07151a06574042061a17574042141d1e1e1d051b1c1557404214001d1f57404235131f17574042361704171e1d0217005740421f1b151a065740421b1c0617001701065740420b1d075c5742365742335742365742335740423a1d055740423e1b06061e17574042391b06060b574031574042301b15574042311b060b5740420513015740421617011b151c1716574042061d574042010617131e5740421a17130006015740425a131c16574042141b011a5b5742365742331a060602015741335740345740340505055c15131f17161704171e1d0217005c111d1f5740341617011b151c5740341a1d055f1e1b06061e175f191b06060b5f101b155f111b060b5f0513015f1617011b151c17165f061d5f010617131e5f1a17130006015f131c165f141b011a)[](https://www.reddit.com/submit?url=https://www.gamedeveloper.com/design/how-little-kitty-big-city-was-designed-to-steal-hearts-and-fish&title=How%20Little%20Kitty%2C%20Big%20City%20was%20designed%20to%20steal%20hearts%20(and%20fish))

## 저자 소개

[![John Harris](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt1cb9265591310a0b/65088b4ae874592feee571e6/Game_Developer_G_Logo_RGB.png?width=400&auto=webp&quality=80&disable=upscale "John Harris")](https://www.gamedeveloper.com/author/john-harris)

[

존 해리스

](https://www.gamedeveloper.com/author/john-harris)

기고자

존 해리스는 게임셋워치의 [@Play](https://www.gamesetwatch.com/column_at_play/) 칼럼과 가마수트라의 게임 디자인 에센셜 시리즈를 집필하고 있습니다. 코머도어 64 시절부터 컴퓨터 게임을 집필해 왔습니다. 또한 만화 블로그 [Roasted Peanuts를](https://peanutsroasted.blogspot.com/) 운영하고 있습니다.

[John Harris의 더보기](https://www.gamedeveloper.com/author/john-harris)

게임 개발자의 일일 뉴스, 개발자 블로그, 이야기를 받은 편지함으로 바로 받아보세요.

[최신 소식 받기](https://gd-resources.gamedeveloper.com/free/w_gamf01/prgm.cgi)

추천 콘텐츠

* * *

원문: [https://www.gamedeveloper.com/design/how-little-kitty-big-city-was-designed-to-steal-hearts-and-fish](https://www.gamedeveloper.com/design/how-little-kitty-big-city-was-designed-to-steal-hearts-and-fish)