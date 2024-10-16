import random

secret_number=random.randint(1,1000)
print("1부터 100까지의 정수를 입력하시오")

tries = 0

while True:
  user_guess = int(input('추측한 숫자를 입력하세요'))
  tries += 1
  
  if user_guess == secret_number:
    print(f'축하합니다! {tries} 번만에 맞추셨습니다.')
    break

  if tries>=10:
    print('10번 시도해도 맞추지 못했습니다.')
    break;

  if user_guess < secret_number:
    print('UP')
  else:
    print('DOWN')
  
