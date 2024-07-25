# TimeTableGenerator
바탕화면에 '한국디지털미디어고등학교'의 시간표를 표시합니다.

---

# 설치 방법
Release에서 TimeTable_installer.exe를 받아 설치합니다.

---

# 초기 세팅
1. 설치 폴더 (기본 : C:\TimeTableGenerator)에 적용하고 싶은 **바탕화면 사진**을 background.jpg로 저장합니다. (꼭 jpg!)
2. https://open.neis.go.kr/portal/guide/actKeyPage.do 이곳에서 **나이스 API 키**를 발급받습니다.
3. 설치 폴더 (기본 : C:\TimeTableGenerator)속 **.env 파일**을 '메모장'으로 열어 발급받은 나이스 API 키를 입력합니다.
4. 바탕화면에 '시간표 수정' 바로가기를 열어 **학년, 반, 기본 시간표**를 입력합니다.
5. 기본 시간표는 ','로 구분하며 줄바꿈을 통해 교시를 구분합니다.

ex.

↓월  ↓화  ↓수  ↓목  ↓금

수학,PY,과학,플밍,진로    -> 1교시

플밍,컴일,국어,미술,사회    -> 2교시

미술,과학,진로,영어,수학    -> 3교시

국어,수학,컴일,영어,국어    -> 4교시

체육,사회,PY,PY,영어    -> 5교시

사회,미술,CA,컴일,과학    -> 6교시

자율,플밍,,체육,컴일    -> 7교시

<img src="https://github.com/user-attachments/assets/aeaee7e9-fe25-47f7-bcd8-fae36940a175"  width="350" height="500">

---

# 작업 스케줄러 설정법 (매일 아침 자동 실행)
1. 윈도우에서 **'작업 스케줄러'** 를 실행합니다.
2. 오른쪽 메뉴에서 **작업 만들기** 를 클릭합니다.
3. **'일반'** 탭에서 원하는 작업의 이름을 입력합니다.
4. **'트리거'** 탭에서 **새로 만들기**를 누르고 **시작**시간을 오전 8시 30분으로 변경 후, **매일**로 설정하고 **확인**을 누릅니다.
5. **'동작'** 탭에서 **새로 만들기**를 누르고 **찾아보기** 버튼을 눌러 **ImageGenerator.exe**를 선택합니다. (기본 폴더 : C:\TimeTableGenerator\ImageGenerator.exe)
6. **'조건'** 탭에서 **전원**메뉴의 모든 항목을 체크 해제합니다. (컴퓨터의 AC 전원이 켜져 있는 경우에만 작업 시작)
7. **확인**을 누릅니다.
8. 매일 아침 8시 30분마다 시간표가 업데이트됩니다.

---

# 주의 사항
1. **추가 시간표**는 방과후, 야자 시간에 할 활동을 입력하는 칸 입니다.
2. 양식은 (일정):(날짜)(활동시간)으로 입력하고, 각 활동은 줄바꿈으로 구분합니다.

ex.

전공UP:월야자1

전공UP:월야자2

스쿼시:화방과후1

3. **'검은 테두리'** 체크박스는 바탕화면이 밝은 색일 때 표시되는 시간표를 검은색으로 바꾸는 기능입니다. 바탕화면 색에 맞게 조절하여 사용하면 됩니다.
4. **'나이스 API'**와 **'컴시간'** 둘 중 하나를 선택하여 어디서 시간표를 가져올지 선택할 수 있습니다. 평소에는 나이스가 더 정확하지만, 자율과정이나 학기가 바뀔 때는 컴시간이 더 정확할 때도 있습니다.
