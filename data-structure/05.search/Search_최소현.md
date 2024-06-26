# 탐색


자료를 찾는 작업. 

탐색의 단위는 항목(value)이며, 구분의 기준은 키(key) 이다.


- 정렬 되지 않은 놈들의 탐색 : 선형, 해시
- 정렬 된 놈들의 탐색 : 이진

## 선형 탐색


- 단순히 처음부터 끝까지 검사하여 항목을 찾는 방식
- 코드
    

## 이진 탐색


- 정렬되어있는 배열에서 중간 부분의 원소를 기준으로 두부분으로 나누고 탐색 범위를 줄여가는 탐색 방식
- 코드
    

## 해시 탐색


- 값과 index를 연결해 둠으로써 O(1)의 시간으로 값을 찾는 방식
- 데이터 저장하는 알고리즘 & 데이터 검색하는 알고리즘 필요
    - 공간 : 해시 배열을 저장하기 위해 기존 배열x2 사이즈의 배열이 추가로 필요함
    - 해시값 충돌 : 해시값이 겹치면 다음 인덱스를 훑음 —> 해시값 충돌을 막기위한 다양한 기법이 존재


# 예상 질문

- Hash Table을 사용하면 O(1)의 시간복잡도인데, BST를 사용하는 경우는 언제일까?
    
    해시 테이블은 키를 기반으로 값을 빠르게 검색할 수 있고, 이상적으로는 O(1)의 시간복잡도를 가지지만, 해시 충돌이 발생하면 O(1)의 시간복잡도가 나오지 않을 수 있다.
    
    특히 해시 함수는 순서를 가지지 않는 무작위 값에서 더 좋은 성능을 보이기 때문에, **정렬 등 순서를 가지는 데이터나 범위를 검색해야 할 때**는 BST가 더 적합하다.
    
- 주어진 Tree가 BST인지 확인하는 방법은?
    
    **중위 순회**를 통해 정렬된 값인지 확인해보면 알 수 있다.