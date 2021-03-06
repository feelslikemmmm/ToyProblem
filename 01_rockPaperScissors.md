# rockPaperScissors

# Problem

가위바위보 게임은 2인 이상의 사람이 동시에 '가위, 바위, 보'를 외치고 동시에 가위, 바위 또는 보 중에서 한 가지를 의미하는 손 모양을 내밀어 승부를 결정짓는 게임이다. 세 판의 가위바위보 게임을 할 경우, 한 사람은 세 번의 선택(예. 가위, 가위, 보)을 할 수 있습니다. 세 번의 선택으로 가능한 모든 경우의 수를 구하는 함수를 작성합니다.

## 입력

- 없음

## 출력

- 2차원 배열(arr[i])을 리턴 해야 합니다.
- arr[i]는 전체 경우의 수 중 한 가지 경우(총 세 번의 선택)를 의미하는 배열입니다.
- arr[i]는 'rock', 'paper', 'scissors' 중 한 가지 이상을 요소로 갖는 배열입니다.
- arr[i].length는 3입니다.

## 제한 사항

- 최종적으로 리턴되는 배열의 순서는 가중치 적용 정렬(Weighted Sort)을 따릅니다.
- 중요도는 'rock', 'paper', 'scissors' 순으로 높습니다.
- 쉽게 생각해 올림픽 순위 결정 방식을 참고하면 됩니다.
- 금메달('rock')이 은메달('paper')보다 우선하고, 은메달('paper')이 동메달('scissors')보다 우선합니다.

## 입출력 예시

![carbon (14)](https://user-images.githubusercontent.com/67893516/97648377-eb992c00-1a97-11eb-969c-72cdc8ceeb54.png)

# 해결 방법

가중치 적용 정렬이 적용되는데, 중요도는 rock, paper, scissors 순으로 높다는 게 이미 주어졌다

2중 배열을 리턴해야 하기 때문에 우선 마지막 결과를 담을 배열을 하나 선언해두고,

이번엔 다른 배열을 선언해서 중요도 순으로 배열에 담아 놓은 뒤 index를 for문으로 순회한다

가위, 바위, 보 3가지의 중요도가 있기 때문에 각 각 순회하기 위해 3중 for문을 사용

arr[i] = rock, arr[j] = paper, arr[k] = scissors 

각 for문을 순서대로 돌며 나온 결과를 담을 배열을 선언하고 그 안에 푸쉬해준다

푸쉬된 결과물을 미리 선언해돈 결과를 담을 배열에 푸쉬해준다.

# 코드 구현

![carbon (15)](https://user-images.githubusercontent.com/67893516/97648378-ec31c280-1a97-11eb-98e3-8ed429654571.png)