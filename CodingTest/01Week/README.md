# 1주차 - 기본 자바 다루기

## 백준 기준 기본틀

```
public class Main() {
    public static void main(String[] args) {
        
    }
}
```

## 기본 출력 - 개행

```
System.out.println();
```

## 기본 입력

자바에서 입력은 Scanner를 사용합니다.

해당 클래스를 사용하기 위해 java.util 패키지에 포함된 패키지를 import를 합니다.
(모듈의 이름은 대문자)

```
import java.util.Scanner;
```

Scanner 객체를 생성하여 표준 입력(System.in)과 연결합니다.

```
Scanner sc = new Scanner(System.in);
```

> 프로그램이 실행 중에 사용자로부터 입력을 받기 위함입니다. 표준 입력(System.in)은 기본적으로 키보드의 입력을 의미하고, 프로그램 실행 중에 사용자의 입력을 받을 수 있습니다.

> Scanner 클래스는 파일, 문자열, 네트워크 등의 다양한 입력을 받을 수 있습니다.

## 공백 기준 입력

다음과 같은 공백 기준으로 2가지의 입력을 받는 경우입니다.
```
7 3
```

Scanner는 기본적으로 공백, 탭, 줄바꿈 등을 구분자로 사용하기 때문에 별도의 처리가 필요하지 않습니다.

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int A = sc.nextInt();
        int B = sc.nextInt();

        System.out.println(A + B);
    }
}
```

## 형변환(Casting)

* 문자(char)에서 숫자(int)으로 형변환

```
int c = '7';

// 방법 1: 문자 '0'의 아스키 값을 이용한 변환
int num1 = c - '0';
System.out.println(num1);

// 방법 2: Character 클래스의 메소드를 이용한 변환
int num2 = Character.getNumericValue(c);
System.out.println(num2);

// 방법 3: Integer 클래스의 메소드를 이용한 변환
int num3 = Integer.parseInt(String.valueOf(c));
System.out.println(num3);
```

* 문자열(String)에서 숫자(int)로 형변환

```
String s = "777";

int num = Integer.parseInt(s);
System.out.println(num);
```