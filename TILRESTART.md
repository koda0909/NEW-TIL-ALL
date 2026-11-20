오늘의 TIL
오늘은 수강신청하는것을 만들었는데
def list_courses(conn): 이걸로 예시를들어보면
def: 함수를 정의하는 명령어
list_courses: 함수 이름 (강좌 목록 조회)
conn: 데이터베이스 연결 객체 라는 뜻인데
음 이것도 ai가 도와줬다 아무리 한달다되간다지만 검은건 화면 알록달록한건
글자로 내머리에는 그렇게 들어온다 질문을 하면 된다고들 생각할것이다.
그런데 질문을 할 개념조차 머리에 없다면 처음 어디서부터 어디까지 질문을 할것인가가 문제가
된다 그래서 질문을 하기에도 이걸 어떻게 질문을 해야할지도 모르는 참 안좋은 상황인것이다
어쩄든 위대하긴 ai님의 힘을 빌어 계속 적어보자면
자 두번쨰 예시 강좌명 검색 기능이다
# 강좌명 검색 기능
def search_courses(conn):
    keyword = input("검색할 강좌명을 입력하세요: ")

    rows = conn.execute("""
        SELECT course_id, course_name, class_days, fee
        FROM courses
        WHERE course_name LIKE %s
        ORDER BY course_id
    """, (f"%{keyword}%",)).fetchall()

    if not rows:
        print("검색 결과가 없습니다.")
        return

    print("\n===== 강좌 검색 결과 =====")
    for row in rows:
        print(
            f"ID: {row['course_id']} | "
            f"강좌명: {row['course_name']} | "
            f"요일: {row['class_days']} | "
            f"수강료: {row['fee']:,}원"
        )


def search_courses(conn):
    keyword = input("검색할 강좌명을 입력하세요: ")

def: 함수를 정의하는 명령어
search_courses: 강좌 검색 함수 이름
conn: 데이터베이스 연결 객체
input(): 사용자에게 입력을 받는 명령어
keyword: 사용자가 입력한 검색어를 저장하는 변수
예를 들어 사용자가 수영이라고 입력하면 keyword에 수영이 저장된다라는것

rows = conn.execute("""
    SELECT course_id, course_name, class_days, fee
    FROM courses
    WHERE course_name LIKE %s
    ORDER BY course_id
""", (f"%{keyword}%",)).fetchall()

rows =	              검색 결과를 rows 변수에 저장
conn.execute()	      SQL 명령어 실행
SELECT	              조회할 항목 선택
course_id	          강좌 ID
course_name	          강좌명
class_days	          수업 요일
fee	                  수강료
FROM courses	      courses 테이블에서 조회
WHERE	              검색 조건 지정
LIKE	              특정 문자열이 포함된 데이터 검색
ORDER BY course_id	  강좌 ID 순서대로 정렬
fetchall()	          검색 결과 전체 가져오기
인데.... 여기까지만해도 머리가 멈추고 터질것만 같다 음 진짜 머리가 안돌아가는게 체감이 크다
요리는 몸만 어찌저찌 쓰면 반은가는데 얘는 시작선도 못넘은것같아 걱정이크다
아직도 겁나게 어렵다