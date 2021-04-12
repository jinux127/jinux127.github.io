---
title:  "숫자 카드 게임"
excerpt: "이것이 코딩 테스트다"

toc: true
toc_sticky: true

categories:
  - Algorithm
tags:
  - Algorithm
  - greedy
last_modified_at: 2021-04-11T22:00-22:00

---

# 숫자 카드 게임

```java
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;
import java.util.Arrays;
import java.util.StringTokenizer;


public class main {

	public static void main(String[] args) throws IOException {
		BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
		StringTokenizer st = new StringTokenizer(br.readLine());
		
		int n = Integer.parseInt(st.nextToken());
		int m = Integer.parseInt(st.nextToken());
		int k = Integer.parseInt(st.nextToken());
		
		int [] arr = new int[n];
		
		StringTokenizer st2 = new StringTokenizer(br.readLine());
		for (int i = 0; i < arr.length; i++) {
			arr[i] = Integer.parseInt(st2.nextToken());
		}
		
		Arrays.sort(arr);
		
		int first = arr[n-1];
		int second = arr[n-2];
		int result = 0;
//		내 풀이 
		for (int i = 0; i < m; i++) {
			int j=0;
			for (j = 0; j < k; j++) {
				result += first;
				++i;
			}
			result += second;
		}
		System.out.println(result);
		
//		답안
		result = 0;
		
		int count = (m/(k+1))*k;
		count += m%(k+1);
		
		result = 0;
		result += count * first;
		result += (m- count) * second;
		System.out.println(result);
		
	}

}

```

콘솔에 입력받는 것이 오랜만이여서 가장 버벅였고 그 외에 어려웠던점은 없었던 것 같다. 

답안을 보고 너무 일차원적으로 풀었던 것 같다는 생각이 들었다.

이 문제는 가장 큰 수와 그 다음 큰수를 일정 규칙에 맞게 반복되게 더하는 경우를 생각하는게 더 효율적이였다. 