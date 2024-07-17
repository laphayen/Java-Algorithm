### 자바 큐 사용하기

```
import java.util.LinkedList;
import java.util.Queue;
```
으로 불러온다.

### 큐 생성
```
Queue<Integer> queue = new LinkedList<>();
```

### 큐의 요소 추가 

큐의 마지막에 요소를 추가
```
queue.offer(3);
```

### 큐의 요소 제거

큐의 첫번째 요소 제거
```
queue.poll()
```

### 큐의 요소 확인

큐의 첫 번째 요소
```
queue.peek()
```

큐의 전체 요소 확인 - [요소1, 요소2, ...]의 형식으로 출력
```
// 큐의 요소: [1, 2, 3, 4]
System.out.println("큐의 요소: " + queue);
```