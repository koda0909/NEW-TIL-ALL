TIL 재시작 2일차
오늘은 pandas 라고 하는것을 배우게됬다
Pandas = 파이썬에서 엑셀처럼 데이터를 다루는 도구 라고 생각하면 편할것이다(이해를 못한 나로서는 음 그렇구나 이렇게 생각중이다)
amounts = [3200, 1500, 15000, 6500, 32000, 4800,
           10900, 1500, 2700, 3000, 18500, 7000]

print(amounts)
print("합계", sum(amounts))

print(amounts * 2)
print("==="*3)
이거는 amounts는 가격 리스트라고 생각하면 될것이고 아래의 print(amounts)는 리스트를 출력한다고 생각하면된다
sum(amounts)는 리스트에 있는것을 전부더해 합계를 계산해 출력하는것이다

import numpy as np

arr = np.array(amounts)
arr * 2

print("합계:", arr.sum())
print("평균:", round(arr.mean()))
print("최소:", arr.min())
print("최대:", arr.max())

print("모양: ", arr.shape, "데이터 타입: ", arr.dtype)

import numpy as np
import : 라이브러리를 불러오는 명령어이고
numpy : 숫자 계산을 편리하게 해주는 라이브러리라고 생각하면 편할듯하다
as np : numpy를 np라는 짧은 이름으로 사용함

arr = np.array(amounts)
arr * 2
np.array() : 기존 리스트를 NumPy 배열로 변환하는것이고
arr : 변환된 배열을 저장하는 변수이다
arr * 2 : 배열 안에 있는 모든 숫자를 2배로 만든다고한다...

print("평균:", round(arr.mean()))
arr.mean() : 배열에 저장된 숫자들의 평균을 계산하고
round() : 소수점을 반올림한다

print("최소:", arr.min())
print("최대:", arr.max())
arr.min() : 가장 작은 금액을 찾는것
arr.max() : 가장 큰 금액을 찾는것이다

print("모양: ", arr.shape, "데이터 타입: ", arr.dtype)
arr.shape : 배열에 저장된 데이터의 개수와 형태를 확인하는것
arr.dtype : 배열에 저장된 데이터의 자료형을 확인함

오늘은 조금은 이해가 갔지만 여전히 어려운것같다 어우 이제 검정은 화면 색깔은 글자에서 가나다에서 ㄱ을 떈거같다
