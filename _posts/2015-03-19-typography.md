---
title: Thread
---
![Test](/emerald/img/img-test.png "Test")
program : 일종의 softwareprocess : 현재 cpu가 실행중인 프로그램
  
  	- thread : 한 프로세스 안에서 동시에(?) 여러 작업 (게임 가동시 작동하는 여러 작업)
  	- multi로 작업을 하기 위해 사용
  	
  	// multiprocess와 multi thread의 차이
  		: 멀티 프로세스는 게임/음악/이클립스의 작업을 쪼개서 runnable에 대기 한 후, 하나씩 run한는 것임
  	- 예) 채팅(나의 입력은 이벤트, 상대방의 입력은 thread)
  	cf)processor는 cpu를 말하는 것임  	
 * 자바의 쓰레드 처리 절차
 1. Thread 클래스를 상속 (Runnable 인터페이스 구현 implements)
 	- run() 오버라이딩
 2. start() 호출 -> run() 호출됨 //start는 대기 상태로 보내 줌
 // 처리 과정을 컨트롤 할 수 없음. 결과값은 매번 달라짐
 
 //when multi tasks are sharing same resources, it needs to synchronize tasks(methods or functions
 until a task is finished and takes a turn.  

## This is a h2

### h3, h4, h5 and h6 have the same style.

Lorem ipsum dolor sit amet, consectetur adipisicing elit. Voluptas sed quo atque *perspiciatis*. Eius cum possimus, maxime unde, asperiores neque blanditiis molestiae ipsa odit. **Laboriosam**, error! Ipsa officia magnam at ratione commodi porro nulla consequuntur eum quia nisi officiis cupiditate reprehenderit provident facilis rem, nobis quidem fugiat, et! Tempore maiores reprehenderit laboriosam rerum? 

> This is a blockquote

### Unordered list
- list 1
- list 2
- list 3
- list 4

### Ordered list
1. one
2. two
3. three
4. four
