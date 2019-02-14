import random as R

def rand7():
  return R.randint(0,7)

def rand5():
  return ((rand7() + rand7() + rand7() + rand7() + rand7()) % 5) + 1

def test(randomFunction):
  frequency = [0, 0, 0, 0, 0]

  for i in range(0, 10000):
    r = randomFunction()
    frequency[r - 1] = frequency[r - 1] + 1

  print(frequency)