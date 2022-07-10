# 인프런 01-01 문제

- 대소문자 변환
    - https://cote.inflearn.com/contest/10/problem/01-02

### 문제 이해하기
대문자와 소문자가 같이 존재하는 문자열을 입력받아 대문자는 소문자로 소문자는 대문자로 변환하여 출력하라.

### 문제 접근 방법
문자열을 받아 순회하면서 대, 소문자 여부를 체크 후 대 <-> 소 변경을 처리한다.

### 구현 배경 지식
- 문자열을 입력 받는 방법
- 문자열을 `char`타입 배열로 만드는 방법
- `StringBuilder` 사용법
- 문자를 대문자, 소문자로 변경하는 방법

### 문제를 해결한 코드
```java
import java.util.Scanner;

public class Main {
  public static void main(String[] args) {
    Scanner in = new Scanner(System.in);
    String text = in.next();
    StringBuilder result = reverseCase(text);
    System.out.println(result);
  }

  private static StringBuilder reverseCase(String text) {
    StringBuilder result = new StringBuilder();
    for (char character : text.toCharArray()) {
      if (Character.isUpperCase(character))
        result.append(Character.toLowerCase(character));
      else
        result.append(Character.toUpperCase(character));
    }
    return result;
  }
}
```

### 해결하지 못한 이유
