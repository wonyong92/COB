<!-- -->
태그 레퍼런스 찾기 : http://www.tcpschool.com/html-tags/intro

<!DOCTYPE html><!-- 주의:태그가 아닌 '선언문'. DTD라고도 불림.  해당 페이지의 HTML 버전을 선언.  -->
<html lang="ko"> <!-- DTD를 제외한 다른 HTML 루트 요소를 포함하는 컨테이너. 주로 lang 속성을 부여하여 브라우저에서 언어 감지 기능 등을 가능케한다.-->

    <head>  <!--해당 페이지의 정보(메타데이터)의 집합을 정의. <title> <style> <base> <link> <meta> <script> <noscript>  요소 사용 가능-->
        <title> 문서의 제목(브라우저 제목 창에 표시)</title>
        <style> 스타일 정보(CSS 코드 사용)</style>
        <link rel="stylesheet" type="text.css" href="***/외부주소.css"><!--외부 소스와의 관계를 정의. 속성만 가지는 태그(닫는 태그 없음) -->
            <!- 태그의 속성은 공백으로 구분되므로 불필요한 공백 사용하지 않기- -->
            <!--rel = 현재문서와 연결문서의 관계표시. type과 href는 한쌍으로 사용해야한다.  text/css text/javascript application/xml-->
            <!-- media 속성을 이용하여 연결된 문서가 표시할 미디어,장치, 조건 명시 가능-->
            <meta charset="UTF-8"><!-- 메타데이터 정의. 검색엔진 등 외부에서 문서에 대한 정보 검색시 사용. 뷰포트 제어 가능 -->
                                   <!-- name = "메타데이터 종류(키워드-검색엔진용, 디스크립션-페이지 설명, 뷰포트-보이는 영역 제어" content="메타데이터 내용" -->
        <script> 자바 스크립트 코드 사용가능</script>
            <script src="외부문서.js"> src 속성 설정시 자바 스크립트 코드 사용 불가능</script>
        <noscript> 주의 : 사용시 스크립트 태그의 내용이 그대로 표시될 수 있다. 스크립트 태그 기능 정지. </noscript>
    </head>


    <!-- -->
    <header>
        상단 영역 나누는 태그. 주로 메뉴바, 검색창, 로고 등이 들어간다. 단순히 섹션을 나누는 태그이므로 여러개 사용가능.
        <h1></h1> bigger ~  smaller <h6></h6> 를 이용하여 블록영역 할당, 문서의 제목을 표현 가능.
    </header>
        

    <body>
        주의 : 하나만 사용 가능하다. 주요 컨텐츠 섹선.
        
        구역 나누는 태그.
        블록 : 옆으로 전체 영역 차지. 줄바꿈 발생.
        인라인 : 다른 요소와 한 줄에 배치. 컨텐츠 크기로 고정. width, height, margin-top,bottom, padding-top,bottom 미적용.
        인라인-블록 : 줄바꿈 없이 인라인과 같이 나란히 배치. 크기 관련 모든 속성 부여 가능.
        
        <div class="클래스 이름" id="ID 이름, 유일해야한다."> 블록 영역을 생성. 블록 속성을 이용, 전체적인 레이아웃 설정용. 여러 요소에 한번에 스타일 적용 가능</div>
        <p> 주의:위아래 기본 마진이 있음. 블록 영역을 생성. 문단 생성용.</p>
        <span> 인라인 영역 생성. 인라인 속성을 이용, 요소들에 대한 레이아웃 설정용. 텍스트 요소에 주로 사용</span>
        <ul> 순서가 없는 리스트 생성
            <li> 앞에 마커가 추가된다. css 속성을 이용하여 마크제거 가능.
            ....
        </ul>
        
        <ol type="A" start="2"> 순서가 있는 리스트 생성. type ="A" 대문자 알파벳, start ="2" 시작 번호.
            <li> 앞에 순서가 있는 마커(숫자 or 알파벳)가 추가된다.
            ....
        </ol>
        
        기능 구현용 태그
        
        <img src="이미지주소" alt="이미지 로드 실패시 출력 텍스트"> 인라인-블록 영역 할당. 이미지를 참조 및 링크하고, 해당 이미지를 위한 영역 할당. 
        <form action="폼데이터가 도착할 url" method="http 메소드 명시" name="폼의 이름을 명시. js에서 사용" >
            <input type="인풋 요소가 나타낼 타입 ex button, checkbox, text " value="초기값" src="image 타입의 이미지 주소" >
                다양한 데이터를 입력받기 위한 태그. 타입을 변경하여 다양한 데이터 종류 선택 가능. 내용을 가지지 못하므로 <label>과 함께 사용.
            <button type="버튼,리셋,서브밋 기능별 타입 지정" value="초기값" name="버튼 이름 지정. js에서 사용">
                input type="button" 과는 다르게 버튼 내부에 이미지나 텍스트 삽입 가능.
            </button>
            <select> 드롭다운 리스트 정의.
                <option value="리턴될 값">내용</option>
                ....
            </select>
            <textarea cols="열 개수" rows="행 개수" name="이름 지정. js에서 사용"> 여러줄 텍스트 입력 상자.
            </form>
            <label for="연결 요소 ID"> 해당 요소의 내용 입력. 텍스트로 출력된다. 텍스트 클릭시 연결된 요소가 바로 선택된다.(영역 확장) </label>
        </form>
        <a href="연결될 링크 주소"> 텍스트 or <img> 태그 사용가능 </a> 하이퍼링크 요소 연결. 다운로드 기능을 연결 가능.
            <scripts></script>
        
    </body>
    
    <footer>
        
    </footer>
 

</html>

