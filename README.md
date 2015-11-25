15/11/19/18:23:05

# **vhd 사용하기**

<table>
<col width="100%" />
<tbody>
<tr class="odd">
<td align="left"><p>vhd 사용하기</p>
<p><br /></p>
<p><br /></p>
<p><br /></p>
## 1. 머릿말
<p>1. 머릿말</p>
<p><br /></p>
<p>안녕하세요.</p>
<p>vhd에 대해서 많은 분들께서 아실 것이고 많은 분들께서 사용하고 계실 것입니다.</p>
<p>하지만 처음 들어보신 분들도 계실 것이고 들어보긴 했지만 모르시는 분들도 계실 것입니다.</p>
<p>vhd를 잘 모르시는 분들을 위해서 vhd를 소개하고자 vhd 대해서 아는 대로 적어보았습니다.</p>
<p>저는 초보라서 자세히는 잘 모릅니다. 초보가 작성한 글이기 때문에 글이 다소 이상하거나 맘에 들지 않으시더라도 너그럽게 봐주시기 바랍니다.</p>
<p>이 글의 내용은 제가 알아낸 것이 아니고 다른 사이트에 있는 정보를 옮긴 것입니다.</p>
<p>그래서 이 글의 출처는 맨 아래에 적었습니다. 출처가 궁금하시다면 맨 아래로 가보시기 바랍니다.</p>
<p><br /></p>
<p><br /></p>
<p>##2. vhd란?</p>
<p><br /></p>
<p>vhd는 Virtual Hard Disk의 약자입니다.</p>
<p>우리말로는 가상하드디스크입니다.</p>
<p>CD나 DVD로 이미지 만들기를 한번쯤은 해보셨을 겁니다.</p>
<p>이미지 만들기를 하면 컴퓨터로 DVD 정보가 담긴 이미지파일이 생성되며 대표적으로 iso라는 파일로 만들어집니다. 생성된 iso 파일은 DVD 정보를 포함하고 있지만 DVD 아닌 가상 DVD입니다. 이와 같이 vhd도 파일로 존재하며 물리 하드디스크가 아닌 하드디스크의 이미지파일입니다.</p>
<p><br /></p>
<p>vhd의 주 기능은 윈도우 백업입니다.</p>
<p>윈도우를 백업하기 위해서 고스트라는 프로그램을 한번쯤은 사용해보셨을 겁니다.</p>
<p>고스트 프로그램으로 OS가 설치된 하드를 백업하면 하드에 대한 정보가 저장된 이미지 파일이 생성됩니다. 그리고 OS를 복구할 때 미리 백업해둔 이미지파일로 복구를 하게 됩니다.</p>
<p>vhd는 고스트와 동일한 기능을 합니다. 윈도우 자체에서 지원하는 백업 프로그램으로 하드나 파티션을 백업하게 되면 이미지파일이 생성되는데 vhd라는 파일로 만들어집니다. 그리고 만들어진 vhd 이미지로 복구를 할 수 있습니다.</p>
<p>이 기능은 고스트 프로그램과 다를 바가 없습니다.</p>
<p><br /></p>
<p>vhd가 고스트 프로그램 보다 무엇이 더 좋기에 소개를 하는지 궁금하실 겁니다.</p>
<p>고스트 프로그램을 사용하시면서 한번쯤은 격어 보셨을 단점들이 있을 것입니다.</p>
<p>고스트 백업을 하게 되면 생성된 이미지파일은 수정하기 힘듭니다. 백업을 잘못하게 되면 파일 수정이 힘들기 때문에 백업을 다시 해야 하는 경우가 있습니다.</p>
<p>그리고 고스트 백업 이미지로는 부팅이 불가능합니다. 또한 백업이미지의 용량이 커질수록 복구하는데 시간이 오래 걸립니다. 복구하는 시간을 단축시키려면 백업이미지의 용량을 줄여야합니다.</p>
<p>고스트 프로그램과는 다르게 vhd는 위에서 서술된 단점들이 보안되어 있습니다.</p>
<p>vhd는 생성된 이미지를 수정할 수 있고, 뿐만 아니라 vhd로 윈도우 부팅이 가능합니다.</p>
<p>또한 vhd의 기능 중에 하나인 Differencing vhd를 사용하면 순식간에 복구가 가능합니다. 많이 과장을 해서 말씀들이자면 용량에 상관없이 1초 만에 복구가 될 수도 있습니다.</p>
<p>이것이 vhd의 장점입니다.</p>
<p><br /></p>
<p>아쉽지만 모든 OS 가 vhd 부팅을 지원하지는 않습니다.</p>
<p>XP, vista는 vhd부팅을 지원하지 않습니다.</p>
<p>그리고 같은 OS라고 하더라도 모든 에디션이 부팅을 지원하지 않습니다.</p>
<p>windows 7 은 Ultimate와 Enterprise 에디션만 vhd 부팅을 지원합니다.</p>
<p>widnws 10은 pro, Enterprise, education만 vhd 부팅을 지원합니다.</p>
<p>vhd로 부팅을 하고 싶으시다면 사용하시는 OS 가 vhd 부팅을 지원하는지 잘 알아보시기 바랍니다.</p>
<p><br /></p>
<p><br /></p>
<p><br /></p>
<p>3. vhd에 윈도우 설치하기</p>
<p><br /></p>
<p>vhd를 설치하는 방법에는 다양한 방법이 있습니다.</p>
<p>하지만 저는 다른 프로그램 도움없이 윈도우 설치 DVD 만으로 vhd를 설치하는 방법을 적어보겠습니다.</p>
<p><br /></p>
<p>먼저 윈도우 상에서 vhd를 만드는 방법입니다.</p>
<p>내 컴퓨터에서 오른쪽 마우스를 누르고 관리로 들어갑니다.</p>
<p><img src="http://image.coolenjoy.net/SWFUpload/resizedemo/saved/1c96579784c5e9b56d228def8c8affe11127511511191036.jpg" /></p>
<p><br /></p>
<p><br /></p>
<p>디스크 관리로 이동한 후 메뉴에서 동작 -&gt;vhd 만들기를 클릭합니다.</p>
<p><img src="http://image.coolenjoy.net/SWFUpload/resizedemo/saved/77b17ef3c27767b43694facce2dc8c021127511511191037.jpg" /></p>
<p></p>
<p><br /></p>
<p><br /></p>
<p>저장할 경로와 용량을 지정하고 동적확장을 선택한 후 확인을 누릅니다.</p>
<p><img src="http://image.coolenjoy.net/SWFUpload/resizedemo/saved/95f68ee6e9608eb6778551f88c5831ab1127511511191037.jpg" /></p>
<p></p>
<p><br /></p>
<p><br /></p>
<p>cmd 도스창으로 만들려면 아래와 같이 입력합니다.</p>
<p><img src="http://image.coolenjoy.net/SWFUpload/resizedemo/saved/m__7fd40d229f484bff4d296bdf66e881fa1127511511191038__m.jpg" /></p>
<p></p>
<p><br /></p>
<p><br /></p>
<p>type=expandable 은 동적확장 (사용한만큼 늘어남)입니다.</p>
<p>type=fixed는 고정크기 (처음부터 용량이 고정됨)입니다.</p>
<p>참고로 fixed로 하게되면 vhd가 생성되는 시간이 몹시 오래 걸립니다.</p>
<p>maximum=20480 은 vhd를 생성할 가상드라이브의 최대 크기입니다. 단위는 MB입니다.</p>
<p><br /></p>
<p><br /></p>
<p>자 이제 본론으로 들어가서 vhd에 윈도우 설치해봅시다.</p>
<p><br /></p>
<p>윈도우 DVD 또는 USB로 부팅을 하여 설치화면을 띄웁니다.</p>
<p><img src="http://image.coolenjoy.net/SWFUpload/resizedemo/saved/63949dc8e8c18cf02fc1a86d394c180f1127511511191039.jpg" /></p>
<p></p>
<p><br /></p>
<p><br /></p>
<p>shift + F10 을 눌러서 도스창을 띄웁니다.</p>
<p>그 다음 아래 스샷과 같이 입력합니다.</p>
<p>파일경로와 파일 이름은 각자 원하는 이름으로 설정합니다.</p>
<p><img src="http://image.coolenjoy.net/SWFUpload/resizedemo/saved/m__711a052a9d025df9d11b1993177b008d1127511511191040__m.jpg" /></p>
<p></p>
<p><br /></p>
<p><br /></p>
<p>주의하실점은 vhd를 만드실 때 vhd가 생성될 하드디스크 파티션 용량보다 작게 만드셔야합니다.</p>
<p>그렇지 않으면 부팅할 때 블루스크린이 뜨면서 부팅이 안됩니다.</p>
<p><br /></p>
<p>vhd 생성과 연결이 완료되면 설치를 계속합니다.</p>
<p>&quot;이 디스크에 Windows를 설치할 수 없습니다&quot; 라는 문구가 뜨는 디스크에 설치를 합니다.</p>
<p><img src="http://image.coolenjoy.net/SWFUpload/resizedemo/saved/b481764e8380fbced8c33288a527363e1127511511191041.jpg" /></p>
<p><br /></p>
<p><br /></p>
<p>vhd에 설치가 되는 모습입니다.</p>
<p><img src="http://image.coolenjoy.net/SWFUpload/resizedemo/saved/b1041a91a59cf4d212e9b583db331f171127511511191042.jpg" /></p>
<p><br /></p>
<p><br /></p>
<p>설치가 완료되면 자동으로 부팅됩니다.</p>
<p><br /></p>
<p>아래는 설치가 완료된 상태이고,</p>
<p>D 로컬 디스크의 vhd로 부팅한 win.vhd 용량이 20G 로 늘어난 상태입니다.</p>
<p><img src="http://image.coolenjoy.net/SWFUpload/resizedemo/saved/m__094f58c79b50048878469a5958ce31271127511511191043__m.jpg" /></p>
<p><br /></p>
<p><br /></p>
<p>원래 하드가 1개 뿐인데 vhd로 윈도우를 설치하게 되면 로컬 디스크가 2개로 보일 것입니다.</p>
<p>이것은 공짜로 하드가 굴러들어온 것이 아닙니다.</p>
<p>C 로컬 디스크는 가상 하드디스크입니다. 용량을 확인해보면 20GB입니다.</p>
<p>20GB의 용량이 생겼다면 어딘가에서 그만큼 손실이 있겠죠?</p>
<p>위의 스샷을 확인해보시면 아시겠지만 D로컬 디스크의 vhd 용량이 20GB입니다.</p>
<p>결론을 말씀들이자면 D 로컬 디스크의 vhd가 차지한 용량만큼 C 로컬 디스크로 반환한 것입니다.</p>
<p>D 로컬 디스크의 vhd = 윈도우가 설치된 C 로컬 디스크</p>
<p><br /></p>
<p>위에 방법으로는 vhd를 동적 확장으로 만들었는데 20GB가 되었습니다.</p>
<p>동적으로 만들어도 OS가 설치된 vhd로 부팅하게 되면 최대용량으로 늘어나게 됩니다. 시스템 종료를 하게 되면 반대로 사용한 만큼의 용량으로 줄어들게 됩니다.</p>
<p>만약에 HDD 또는 SSD의 파티션용량보다 vhd의 용량을 더 크게 만들게 되면 vhd로 부팅할 때 최대용량으로 늘어나지 못하기 때문에 블루스크린 오류가 나면서 부팅이 불가능하게 됩니다. 따라서 vhd를 생성하실 때는 vhd가 들어있는 파티션보다 작게 만드셔야합니다.</p>
<p><br /></p>
<p>vhd에 윈도우를 설치하셨다면 드라이버도 잡아주시고 사용할 프로그램들도 깔아주시고 최적화 해주시기 바랍니다.</p>
<p><br /></p>
<p>작업이 끝났다면 다음 단계로 넘어갑니다.</p>
<p><br /></p>
<p><br /></p>
<p><br /></p>
<p>4. 자식 vhd (Differencing VHD) 만들기</p>
<p><br /></p>
<p>윈도우 DVD 나 USB로 부팅하여 설치화면을 띄웁니다.</p>
<p>참고로 사용 중이거나 부팅중인 vhd의 자식(Differencing VHD)은 만들지 못합니다.</p>
<p>부팅중이 vhd에 자식 vhd를 만들려고 한다면 아래와 같이 나옵니다.</p>
<p><img src="http://image.coolenjoy.net/SWFUpload/resizedemo/saved/m__be2acb775b24673e4a0f7f713f2b1b601127511511191045__m.jpg" /></p>
<p></p>
<p><br /></p>
<p><br /></p>
<p>그러므로 윈도우 DVD, USB로 부팅합니다.</p>
<p><img src="http://image.coolenjoy.net/SWFUpload/resizedemo/saved/53e4740f526c5cebdbdac3af5028df031127511511191046.jpg" /></p>
<p></p>
<p><br /></p>
<p><br /></p>
<p>Shift + F10 을 눌러서 도스창을 띄웁니다.</p>
<p>create vdisk  --------&gt; 가상 하드디스크를 만들어라는 명령어 입니다.</p>
<p>file=C:win-diff.vhd  --&gt; 자식 vhd (Differencing VHD)를 만들 디스크 경로와 파일 이름입니다.</p>
<p>parent=C:win.vhd  ---&gt; C:win.vhd를 원본(부모)으로 하라는 명령어 입니다.</p>
<p>아래 스샷과 같이 작성합니다.</p>
<p><img src="http://image.coolenjoy.net/SWFUpload/resizedemo/saved/m__cda51644388e51899e86f7f0a6a85bc51127511511191047__m.jpg" /></p>
<p></p>
<p><br /></p>
<p><br /></p>
<p>자식 vhd (Differencing VHD) 생성과 부팅작업을 완료하면 재부팅합니다.</p>
<p><br /></p>
<p>작업을 무사히 마치면 아래와 같이 2개의 부팅 목록이 나타날 것입니다.</p>
<p>첫 번째 부팅목록이 바로 지금 막 생성한 따끈따끈한 자식 vhd로 부팅하는 목록입니다.</p>
<p>두 번째 부팅목록은 원본 vhd 로 부팅하는 목록입니다.</p>
<p>따끈따끈한 자식 vhd로 부팅합니다.</p>
<p><img src="http://image.coolenjoy.net/SWFUpload/resizedemo/saved/m__043bb579346de46eef87bff15196948e1127511511191048__m.jpg" /></p>
<p><br /></p>
<p><br /></p>
<p>아래와 같이 win.vhd 원본이 7G로 줄었습니다.</p>
<p>원본 win.vhd로 부팅을 하지 않았기 때문에 사용한 만큼의 용량으로 줄었습니다.</p>
<p><img src="http://image.coolenjoy.net/SWFUpload/resizedemo/saved/m__1543be60ae3ff30c25d205d2e8d75f281127511511191049__m.jpg" /></p>
<p><br /></p>
<p><br /></p>
<p>win-diff.vhd 가 생성되었으며 부팅중이므로 20G로 늘어난 상태입니다.</p>
<p><img src="http://image.coolenjoy.net/SWFUpload/resizedemo/saved/m__70fa351c18b16115a1f4145615fd54991127511511191049__m.jpg" /></p>
<p><br /></p>
<p><br /></p>
<p>마지막으로 원본 win.vhd의 부팅목록을 삭제해보겠습니다.</p>
<p><br /></p>
<p>아래스샷과 같이 따라하시면 됩니다.</p>
<p><img src="http://image.coolenjoy.net/SWFUpload/resizedemo/saved/m__245c63d3180737ed7e5e9fe841b2fd271127511511191050__m.jpg" /></p>
<p></p>
<p><br /></p>
<p><br /></p>
<p>이렇게 설정하면 1개의 목록만 남게 됩니다.</p>
<p>그러면 멀티부팅 메뉴가 나타나지 않고 바로 자식(diff)vhd 로 부팅할 수 있습니다.</p>
<p>원본 윈도우를 자주 편집하실 생각이 있으시면 그대로 두셔도 상관없습니다.</p>
<p><br /></p>
<p><br /></p>
<p><br /></p>
<p>5. 자식 vhd(Differencing VHD)을 바꿔서 윈도우 초기화 시키기</p>
<p><br /></p>
<p>먼저 아래와 같이 윈도우 배경화면을 바꾼상태입니다. 그리고 바이러스가 들어왔습니다.</p>
<p><img src="http://image.coolenjoy.net/SWFUpload/resizedemo/saved/ddb1948f8bd3340e21565bf4a922dcd41127511511191052.jpg" /></p>
<p><br /></p>
<p><br /></p>
<p>win.vhd는 윈도우가 설치된 vhd 원본파일입니다.</p>
<p>그리고 win-diff.vhd는 사용중인 상태이며 바이러스가 들어와있는 자식 vhd (Differencing VHD) 입니다.</p>
<p>backup.vhd 는 순수한 때타지 않은 자식 vhd 입니다.</p>
<p><br /></p>
<p>윈도우를 초기화 시키려면 바이러스에 감염된 win-diff.vhd를 삭제하고 순수한 backup.vhd로 교체하면 초기화 됩니다.</p>
<p>아래 스샷은 윈도우로 부팅한 상태이며 오염된 win-diff.vhd를 지워보겠습니다.</p>
<p><img src="http://image.coolenjoy.net/SWFUpload/resizedemo/saved/m__3c66bfa769f2f2d024180fb305dfd7111127511511191053__m.jpg" /></p>
<p></p>
<p><br /></p>
<p><br /></p>
<p>지우기를 시도했지만 사용중인 상태이므로 지울 수가 없습니다.</p>
<p><img src="http://image.coolenjoy.net/SWFUpload/resizedemo/saved/944243e5b1db486905cc2668aac2d3801127511511191054.jpg" /></p>
<p><br /></p>
<p><br /></p>
<p>윈도우를 부팅한 상태에서는 교체가 힘들기 때문에 윈도우설치 DVD 나 USB로 부팅합니다.</p>
<p><br /></p>
<p>vhd의 교체방법은 여러 가지가 있습니다. 멀티부팅 방법으로 교체할 수도 있고, 윈도우 PE 부팅으로 교체가 할 수 있는 등 여려가지 방법이 있습니다.</p>
<p><br /></p>
<p>아래 방법은 누구나 가지고 있는 윈도우 DVD 나 USB로 vhd를 교체하는 방법입니다.</p>
<p><img src="http://image.coolenjoy.net/SWFUpload/resizedemo/saved/3d0b13d6c87bc3d7ad7cf562fd7147551127511511191055.jpg" /></p>
<p></p>
<p><br /></p>
<p><br /></p>
<p>shift + F10을 눌러서 아래 스샷을 참고하여 작성합니다.</p>
<p><img src="http://image.coolenjoy.net/SWFUpload/resizedemo/saved/m__6e4471e47065abe97e421bb9cb118c1e1127511511191055__m.jpg" /></p>
<p></p>
<p><br /></p>
<p><br /></p>
<p>작업이 무사히 완료되었다면 재부팅합니다.</p>
<p><br /></p>
<p>윈도우 초기화를 시켰더니 아래와 같이 바이러스가 사라졌으며, 윈도우 배경화면이 원래대로 돌아왔습니다.</p>
<p><img src="http://image.coolenjoy.net/SWFUpload/resizedemo/saved/1520294a548204c569134bb417b861c11127511511191057.jpg" /></p>
<p></p>
<p><br /></p>
<p><br /></p>
<p><br /></p>
<p>6. vhd를 다른하드로 옮겨 부팅하기 (마이그레이션)</p>
<p><br /></p>
<p>vhd를 사용하게 되면 별도의 마이그레이션 툴이 필요없게 됩니다.</p>
<p>왜냐하면 vhd를 다른하드에 옮겨놓고 부팅연결만 하면 되기 때문입니다.</p>
<p>기존하드에 있는 vhd를 새로운 하드에 복사하고, 기존하드를 제거하여 새로운 하드로 부팅해보겠습니다.</p>
<p><br /></p>
<p>먼저 2TB 이하 용량의 새 하드를 연결합니다. MBR을 선택합니다.</p>
<p><img src="http://image.coolenjoy.net/SWFUpload/resizedemo/saved/6c68758e74e090e1bc50fa96bfce90ad1127511511191058.jpg" /></p>
<p></p>
<p><br /></p>
<p><br /></p>
<p>설정이 완료되었다면 할당되지 않은 디스크를 찾아서 파티션을 생성해줍니다.</p>
<p><img src="http://image.coolenjoy.net/SWFUpload/resizedemo/saved/m__38e896a76e1ac9ab8c59723f691bf71c1127511511191059__m.jpg" /></p>
<p><br /></p>
<p><br /></p>
<p>F 로컬 디스크로 생성되었습니다.</p>
<p><img src="http://image.coolenjoy.net/SWFUpload/resizedemo/saved/m__4f7b025f0ebb641f07faea4efdcc42b01127511511191059__m.jpg" /></p>
<p></p>
<p><br /></p>
<p><br /></p>
<p>파티션 생성이 완료되면 &quot;파티션을 활성 파티션으로 표시&quot;를 해줍니다.</p>
<p><img src="http://image.coolenjoy.net/SWFUpload/resizedemo/saved/m__7d244c97e08d520c66425aafd415d0d4112751151119110__m.jpg" /></p>
<p></p>
<p><img src="http://image.coolenjoy.net/SWFUpload/resizedemo/saved/m__605c4fa5bf093c29876f360723db3f34112751151119110__m.jpg" /></p>
<p></p>
<p><br /></p>
<p><br /></p>
<p>파티션을 생성과 설정을 다했다면 새로 생성된 디스크에 vhd를 복사합니다.</p>
<p><br /></p>
<p>D 디스크에 있는 파일들입니다. 여기서 vhd 파일만 복사합니다.</p>
<p><img src="http://image.coolenjoy.net/SWFUpload/resizedemo/saved/m__145e4ad5752dbb63811232c1d6be7910112751151119111__m.jpg" /></p>
<p></p>
<p><br /></p>
<p><br /></p>
<p>새로운 하드의 파티션 문자가 F로 할당되었으므로 F로컬 디스크에 vhd를 복사합니다.</p>
<p>하드를 새로 바꿨으니 깨끗한 윈도우를 사용하시고 싶으시면 win-diff.vhd는 그대로 놓아두고 원본 vhd인 win.vhd와 깨끗한 backup.vhd를 복사합니다.</p>
<p>그런다음 backup.vhd를 win-diff.vhd로 복사해 줍니다.</p>
<p><img src="http://image.coolenjoy.net/SWFUpload/resizedemo/saved/m__aca530389bdc92913af8868c6ce15828112751151119112__m.jpg" /></p>
<p></p>
<p><br /></p>
<p><br /></p>
<p>마이그레이션은 사용중인 윈도우를 그대로 옮기는 것이기 때문에 마이그레이션이 아니라고 따질 수 있습니다.</p>
<p>위의 상황은 윈도우가 초기화된 상태로 옮기는 아주 사소한 팁으로 그냥 알려드린 것입니다.</p>
<p><br /></p>
<p>사용중인 윈도우를 통째로 옮겨야 마이그레이션이겠죠?</p>
<p><br /></p>
<p>사용중인 윈도우를 통째로 옮기시려면 win.vhd와 win-diff.vhd를 그냥 복사하셔서 옮기시면 됩니다. 매우 간단하죠?</p>
<p><img src="http://image.coolenjoy.net/SWFUpload/resizedemo/saved/m__0dd191881df96d0bd6ba8ee740ead5d0112751151119112__m.jpg" /></p>
<p></p>
<p><br /></p>
<p><br /></p>
<p>현재 부팅하여 사용되고 있는 win-diff.vhd (20GB로 늘어난 자식 vhd) 까지 모두 복사가 완료되었습니다.</p>
<p><br /></p>
<p>여기까지 윈도우를 옮기는 작업은 끝났습니다.</p>
<p><br /></p>
<p>그럼 부팅이 되게끔 부팅연결만 해주면 됩니다.</p>
<p><br /></p>
<p>컴퓨터 관리를 켜시고 디스크 관리로 이동합니다.</p>
<p>그런후 동작 -&gt; vhd 연결을 클릭합니다.</p>
<p><img src="http://image.coolenjoy.net/SWFUpload/resizedemo/saved/m__b28c16045e31cf5bf0b75595834c54bd112751151119113__m.jpg" /></p>
<p><br /></p>
<p><br /></p>
<p>새 하드에 복사한 Win-diff.vhd를 연결합니다.</p>
<p><img src="http://image.coolenjoy.net/SWFUpload/resizedemo/saved/deada6834c9ad156a6988a782cf38143112751151119114.jpg" /></p>
<p><br /></p>
<p><br /></p>
<p>vhd 불러오기를 하셨다면 아래와 같이 오프라인으로 나타납니다.</p>
<p><img src="http://image.coolenjoy.net/SWFUpload/resizedemo/saved/m__386498d3221a61f9b358a520081f1c2c112751151119114__m.jpg" /></p>
<p><br /></p>
<p><br /></p>
<p>불러온 vhd에 오른쪽 마우스를 클릭하고 온라인을 선택합니다.</p>
<p><img src="http://image.coolenjoy.net/SWFUpload/resizedemo/saved/m__40bbb704a2c04c11341889fbba7bc31f112751151119115__m.jpg" /></p>
<p></p>
<p><img src="http://image.coolenjoy.net/SWFUpload/resizedemo/saved/m__b54133706a078a064e52107b6632f93b112751151119117__m.jpg" /></p>
<p></p>
<p><br /></p>
<p><br /></p>
<p>새로운 하드에 복사된 vhd가 G 로컬 디스크로 연결되었습니다.</p>
<p><br /></p>
<p>그렇다면 컴퓨터 관리 창을 닫습니다.</p>
<p><br /></p>
<p>다시 설명을 드리자면 F 로컬 디스크가 새로운 하드 디스크입니다.</p>
<p>그리고 G로컬 디스크는 F 디스크에 들어있는 vhd가 연결되어 나타난 디스크입니다.</p>
<p><img src="http://image.coolenjoy.net/SWFUpload/resizedemo/saved/m__1376669e6f7f1f02376eae3e8edd32cc112751151119116__m.jpg" /></p>
<p><br /></p>
<p><br /></p>
<p>cmd 창을 관리자 권한으로 실행합니다.</p>
<p>아래와 같이 입력합니다.</p>
<p>G:windows /s F: /l ko-kr</p>
<p>G 디스크에 설치된 윈도우의 부트매니저를 F디스크에 생성하라는 의미입니다.</p>
<p>/l ko-kr 은 부팅 메뉴 언어를 한글로 표시하라는 의미입니다. /l은 소문자 L입니다.</p>
<p><img src="http://image.coolenjoy.net/SWFUpload/resizedemo/saved/m__87ba75e2fd75445b73719a50eaa0cb6f112751151119118__m.jpg" /></p>
<p></p>
<p><br /></p>
<p><br /></p>
<p>이제 마지막으로 bootsect 설정을 해줍니다.</p>
<p>cmd 창에 아래와 같이 입력합니다.</p>
<p>bootsect /nt60 F: /mbr</p>
<p><img src="http://image.coolenjoy.net/SWFUpload/resizedemo/saved/m__f49b1b32d26e015279174598ca14b2941127511511191110__m.jpg" /></p>
<p><br /></p>
<p><br /></p>
<p>이 작업을 빠트리면 부팅이 되지 않습니다.</p>
<p><br /></p>
<p>여기까지 완료되셨다면 마이그레이션이 끝났습니다.</p>
<p>이 작업이 진행되지 않는다면 글을 아래쪽 7번 글에 해결방법을 적어놓았습니다.</p>
<p>작업이 잘 되었는지 확인합니다.</p>
<p><img src="http://image.coolenjoy.net/SWFUpload/resizedemo/saved/m__3e91dc3d0925786bc415716c5d5440841127511511191110__m.jpg" /></p>
<p><br /></p>
<p><br /></p>
<p>이제 이전에 사용했던 하드를 분리하고 마이그레이션을 했던 새로운 하드로 부팅합니다.</p>
<p><br /></p>
<p>부팅에 성공한 스샷입니다.</p>
<p><img src="http://image.coolenjoy.net/SWFUpload/resizedemo/saved/m__1fd262a1d12a1cdc144d492736e2f1d21127511511191111__m.jpg" /></p>
<p><img src="http://image.coolenjoy.net/SWFUpload/resizedemo/saved/m__6a044bc26372909c83a51b690648fd1c1127511511191112__m.jpg" /></p>
<p><br /></p>
<p><br /></p>
<p>새로 바꾼 하드의 문자가 F 문자로 할당되어 있습니다. </p>
<p>문자를 바꾸시기 귀찮다거나 상관없으시다면 그냥 사용하셔도 됩니다.</p>
<p>만약 문자를 바꾸고 싶다면 컴퓨터 관리를 실행합니다.</p>
<p><br /></p>
<p>F 디스크에서 오른쪽 마우스 클릭 후 “드라이브 문자 및 경로 변경”을 선택하셔 문자를 바꾸시면 됩니다.</p>
<p><img src="http://image.coolenjoy.net/SWFUpload/resizedemo/saved/m__5cdca3bf3982dda726134bdc0fd65a6e1127511511191113__m.jpg" /></p>
<p><img src="http://image.coolenjoy.net/SWFUpload/resizedemo/saved/m__d16e95739b72e513366ee54e3458d7e31127511511191113__m.jpg" /></p>
<p><br /></p>
<p><br /></p>
<p>D 로컬 디스크로 문자를 바꿨습니다.</p>
<p>이제 모든 작업이 완료되었습니다.</p>
<p><br /></p>
<p>약간의 팁을 더 드리자면 윈도우 8, 8.1, 10을 vhd로 설치하여 위의 방법으로 USB로 옮기면 매우 간단하게 Win To Go 가 됩니다. USB에 Win To Go를 직접 만들게 되면 만드는데 시간이 오래 걸리고 부팅해서 새로운 프로그램을 설치하는 것도 시간이 오래 걸립니다.</p>
<p>vhd에 8이상의 윈도우를 하드나 SSD에 설치하고 원하시는 작업을 하신 후 USB로 옮기시면 시간절략도 되고 스트레스도 덜 받고 손쉽게 Win To Go를 만드실 수 있습니다.</p>
<p><br /></p>
<p><br /></p>
<p><br /></p>
<p>7. 윈도우 7에서 bootsect 명령어를 사용하지 못할 때</p>
<p><br /></p>
<p>윈도우 8 이상 버전에서는 아무런 문제없이 bootsect 설정이 잘 될 것입니다.</p>
<p>윈도우 7에서 작업하실 때는 마지막단계인 bootsect 설정에서 막힐 겁니다.</p>
<p>cmd 창에 bootsect를 입력하면 아래와 같이 나올 것입니다.</p>
<p><img src="http://image.coolenjoy.net/SWFUpload/resizedemo/saved/dfc5c44bbe2620faa6252613eb2f47d31127511511191116.jpg" /></p>
<p><br /></p>
<p><br /></p>
<p>왜냐하면 윈도우 7에는 기본적으로 bootsect.exe파일이 없기 때문에 명령어가 작동하지 않습니다.</p>
<p>그러므로 윈도우 7에서 작업할때는 bootsect.exe파일을 가져와야합니다.</p>
<p>8 이상의 윈도우에서 bootsect.exe 파일을 가져오면 깔끔하게 해결됩니다.</p>
<p>만약 8 이상의 윈도우가 없어서 bootsect.exe 파일을 가져오지 못하는 경우에는 윈도우 설치 DVD나 iso에서 추출해야합니다.</p>
<p><br /></p>
<p>bootsect.exe 파일을 가져오기 위해서는 2가지의 준비물이 필요합니다.</p>
<p>1) 7zip 프로그램(<a href="http://www.7-zip.org/">http://www.7-zip.org/</a>)</p>
<p>2) 윈도우 DVD 또는 iso (윈도우 7, 8, 8.1, 10)</p>
<p>(32bit 윈도우7이 설치된 컴퓨터에서는 윈도우 32bit의 설치 DVD나 iso가 필요합니다.)</p>
<p>(64bit 윈도우7이 설치된 컴퓨터에서는 윈도우 DVD나 윈도우 iso 파일이 필요합니다. 32bit, 64bit 모두 가능)</p>
<p><br /></p>
<p>제일 먼저 7zip을 설치합니다.</p>
<p>설치가 완료되면 윈도우 설치 DVD 또는 iso를 마운트합니다.</p>
<p>윈도우 설치 DVD가 마운트된 디스크 -&gt; sources -&gt; boot.wim을 찾습니다.</p>
<p><img src="http://image.coolenjoy.net/SWFUpload/resizedemo/saved/m__807a9e593f39dde7cfb3a8ea61ed9ff21127511511191118__m.jpg" /></p>
<p></p>
<p><br /></p>
<p><br /></p>
<p>boot.wim 파일에 오른쪽 클릭을 하여 7zip 압축파일 열기를 클릭합니다.</p>
<p><img src="http://image.coolenjoy.net/SWFUpload/resizedemo/saved/m__d9d630b492fa5c33f6c224fc22af9a591127511511191118__m.jpg" /></p>
<p></p>
<p><br /></p>
<p><br /></p>
<p>2 -&gt; windows -&gt; system32 폴더에서 bootsect.exe 파일을 찾습니다.</p>
<p><img src="http://image.coolenjoy.net/SWFUpload/resizedemo/saved/01d7c840c5a8c2a187453e146ffe277a1127511511191119.jpg" /></p>
<p></p>
<p><img src="http://image.coolenjoy.net/SWFUpload/resizedemo/saved/56596500ccedd6b252cf9ed8c640928a1127511511191119.jpg" /></p>
<p></p>
<p><img src="http://image.coolenjoy.net/SWFUpload/resizedemo/saved/4952b1581d5ff97c981a88dee1c7966a1127511511191119.jpg" /></p>
<p></p>
<p><img src="http://image.coolenjoy.net/SWFUpload/resizedemo/saved/15a011f124e4295b1bfb4545dfcfb46e1127511511191120.jpg" /></p>
<p></p>
<p><br /></p>
<p><br /></p>
<p>찾은 bootsect.exe 파일을 C로컬 디스크 -&gt; windows -&gt; system32 폴더에 복사합니다.</p>
<p><img src="http://image.coolenjoy.net/SWFUpload/resizedemo/saved/m__59cc27e9f31ed1b92e15f6170c3375d41127511511191120__m.jpg" /></p>
<p><br /></p>
<p><br /></p>
<p>복사를 완료했다면 bootsect 명령어를 사용하실 수 있습니다.</p>
<p><img src="http://image.coolenjoy.net/SWFUpload/resizedemo/saved/328ccaabd0b6d4ad1835a9f491e202051127511511191121.jpg" /></p>
<p><br /></p>
<p><br /></p>
<p><br /></p>
<p>8. vhd 용량 줄이기</p>
<p><br /></p>
<p>vhd를 동적으로 만들게 되면 사용한 만큼 늘어나게 됩니다.</p>
<p>하지만 늘어난 vhd에 들어있는 파일을 삭제한다고 하더라도 다시 용량이 줄어들지 않습니다.</p>
<p>아래의 방법은 vhd의 용량을 줄이는 방법입니다.</p>
<p>여기서 핵심은 vhd에 제로필드를 하는 것입니다.</p>
<p>제로필드를 하는 프로그램이 많이 있습니다만 쉽게 구할 수 있는 CCleaner를 사용하였습니다.</p>
<p><br /></p>
<p>아래 스샷과 같이 3.14GB의 TEST.vhd가 있습니다. 아래 TEST.vhd의 용량을 줄여보겠습니다.</p>
<p><img src="http://image.coolenjoy.net/SWFUpload/resizedemo/saved/m__03e6a6934b1a899e2f4e9fbadaf85ccb1127511511191123__m.jpg" /></p>
<p><br /></p>
<p><br /></p>
<p>vhd를 연결합니다.</p>
<p>컴퓨터 관리 -&gt; 디스크 관리 -&gt; 동작 -&gt; VHD 연결을 선택합니다.</p>
<p><img src="http://image.coolenjoy.net/SWFUpload/resizedemo/saved/m__3b7048b57a37cc69a72b9fa2d3580eaf1127511511191123__m.jpg" /></p>
<p></p>
<p><img src="http://image.coolenjoy.net/SWFUpload/resizedemo/saved/4083a115e771166489a2379a793168681127511511191124.jpg" /></p>
<p></p>
<p><br /></p>
<p><br /></p>
<p>연결한 vhd에 내용을 확인해보니 아래 스샷과 같이 아무것도 없습니다.</p>
<p>파일과 내용물이 없는데 3.14GB를 차지하고 있었습니다.</p>
<p><img src="http://image.coolenjoy.net/SWFUpload/resizedemo/saved/m__a6f2816683073d688ef6e14fbeba8f8d1127511511191124__m.jpg" /></p>
<p></p>
<p><br /></p>
<p><br /></p>
<p>CCleaner를 실행하여 연결된 vhd디스크에 1단계 보안삭제(제로필드)를 시작합니다.</p>
<p><img src="http://image.coolenjoy.net/SWFUpload/resizedemo/saved/m__907de480d28243e94db686cf339fa23b1127511511191124__m.jpg" /></p>
<p></p>
<p><br /></p>
<p><br /></p>
<p>보안삭제가 완료되었다면 CCleaner를 닫습니다.</p>
<p><img src="http://image.coolenjoy.net/SWFUpload/resizedemo/saved/m__aa808b547c61abb72a2f8ead21a125bf1127511511191125__m.jpg" /></p>
<p><br /></p>
<p><br /></p>
<p>vhd의 연결을 해제합니다.</p>
<p><img src="http://image.coolenjoy.net/SWFUpload/resizedemo/saved/m__f43e1738d8c0d93b1580ade8ecb28e661127511511191125__m.jpg" /></p>
<p><br /></p>
<p><br /></p>
<p>cmd 창을 관리자 권한으로 실행하여 아래와 같이 입력합니다.</p>
<p><img src="http://image.coolenjoy.net/SWFUpload/resizedemo/saved/m__3bf2ceda9b524e0b986591c6953b7d371127511511191127__m.jpg" /></p>
<p></p>
<p><br /></p>
<p><br /></p>
<p>압축이 끝날때까지 기다리면 아래와 같이 완료됩니다.</p>
<p><img src="http://image.coolenjoy.net/SWFUpload/resizedemo/saved/m__e6bb7da9b9bd050354fc1abfee2f93a01127511511191127__m.jpg" /></p>
<p><br /></p>
<p><br /></p>
<p>완료가 되었다면 cmd 창을 닫습니다.</p>
<p><br /></p>
<p>vhd 용량을 다시 확인해보니 용량이 56.1MB로 줄었습니다.</p>
<p><img src="http://image.coolenjoy.net/SWFUpload/resizedemo/saved/m__b506a02eff2d45cde957e7a867f234df1127511511191127__m.jpg" /></p>
<p></p>
<p><br /></p>
<p><br /></p>
<p><br /></p>
<p>9. 꼬리말</p>
<p><br /></p>
<p>추가로 Differencing vhd가 무엇인지 좀더 알려드리겠습니다.</p>
<p>아래 스샷에서 처음 생성한 Differencing vhd용량이 1MB도 안되는 매우 작은 용량입니다.</p>
<p><img src="http://image.coolenjoy.net/SWFUpload/resizedemo/saved/m__165bd1fe223750b4597060092bd3fba71127511511191129__m.jpg" /></p>
<p><br /></p>
<p><br /></p>
<p>아래와 같이 Differencing vhd를 메모장으로 열어보니 부모 vhd(원본 vhd)에 대한 주소가 들어있습니다.</p>
<p><img src="http://image.coolenjoy.net/SWFUpload/resizedemo/saved/m__bea21fd75f6694e61c27009c2619d2051127511511191129__m.jpg" /></p>
<p><br /></p>
<p><br /></p>
<p>위에 보시는 것과 같이 특별한 것은 없고 부모(원본) vhd에 대한 주소가 들어있습니다.</p>
<p>주소의 의미는 부모 vhd를 불러오라는 의미입니다.</p>
<p>자식 vhd는 부모 vhd를 불러와서 부모 vhd의 정보를 뼈대로 사용하게 됩니다.</p>
<p>그리고 자식 vhd로 부팅해서 설정을 변경하거나 파일 삭제 또는 파일을 새로 설치했다고 하면 추가로 변경된 사항들을 부모 vhd가 아닌 자식 vhd에 저장하게 됩니다.</p>
<p>그러기 때문에 자식 vhd를 날려버리면 자식 vhd에 저장되어있던 모든 정보가 삭제되고 부모 vhd의 정보만 남게되어 빠르고 깔끔하게 이전 상태로 되돌릴 수 있습니다.</p>
<p><br /></p>
<p>포맷하고 윈도우를 설치하다보면 또 다시 재설치를 해야 될 때가 있습니다.</p>
<p>윈도우를 클린설치하고 드라이버 다잡아놓고 사용하려고하니 드라이버가 꼬였거나 윈도우 업데이트가 꼬였거나 바이러스가 들어왔거나 하면 윈도우 재설치를 또 해야 됩니다.</p>
<p>Differencing vhd(자식 vhd)를 사용하게 되면 포맷을 하지 않고 윈도우를 처음 설치한 상태로 초기화 시킬 수 있습니다.</p>
<p><br /></p>
<p>vhd를 사용하게되면 복구가 쉽고 마이그레이션이 쉽다는 것을 위의 내용을 통해서 확인하셨을 것입니다.</p>
<p>단점은 자식 vhd는 부모 vhd와 동일한 폴더에 있어야합니다. 그렇지 않으면 자식 vhd를 사용할 수 없습니다.</p>
<p>그리고 vhd를 SSD에 사용하게 되면 트림기능이 안된다고 합니다.</p>
<p>또한 최대 절전모드를 사용하실 수 없습니다.</p>
<p>확실하지는 않지만 vhdx를 사용하게 되면 트림이 작동된다고 합니다만 직접 사용을 해보지 않아서 정확한 정보인지는 모르겠습니다.</p>
<p><br /></p>
<p>위에서 설명했던 vhd의 교체방법 외에도 여러 가지 방법이 있습니다.</p>
<p>검색하시면 충분히 많이 나옵니다.</p>
<p>다른 방법을 원하시면 검색해보시기 바랍니다.</p>
<p><br /></p>
<p>저는 초보라 잘못 적었을 수 있고, 설명이 부족할 수도 있습니다만 너그럽게 봐주시기 바랍니다.</p>
<p>문제가 된다면 글을 지우겠습니다.</p>
<p>이만 글을 마치겠습니다.</p>
<p>허접한 긴글을 끝까지 읽어주셔서 감사합니다.</p>
<p><br /></p>
<p><br /></p>
<p><br /></p>
<p>10. 출처 </p>
<p><br /></p>
<p>스누피 블로그</p>
<p>캐플 블로그</p>
<p>매니안 닷컴 (윈도우 포럼)</p>
<p><br /></p>
<p>이 글은 위의 출처 3곳에 있는 정보를 모아서 재구성하였습니다.</p>
<p><br /></p></td>
</tr>
<p><br /></p></td>
</tr>
</tbody>
</table>
