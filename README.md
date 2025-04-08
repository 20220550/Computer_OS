# Computer_OS
컴퓨터 운영체제

해사 인공지능보안 학부, 윤명섭
# 1주차 과제

![Image](https://github.com/user-attachments/assets/74b4dcd1-3303-4d70-bff3-03a8fa900d95)

# 2주차 과제
#### 1번 문제 풀이
시스템 호출(system call)은 응용프로그램 내에서 다른 함수를 호출하는 함수 호출(function call)에 비해 많은 시간 비용을 초래하므로
(시스템 호출 과정에서 사용자 모드가 커널 모드로 전환되고, CPU 레지스터를 커널에 있는 스택에 저장하고, 커널 함수를 호출하는 등 여러 과정이 포함되기 때문)
, 응용프로그램을 작성할 때, 표준 라이브러리 함수를 호출하는 것이 시스템 호출 함수를 호출하는 것보다 낫다. 

#### 3번 문제 풀이
"인터럽트"는 입출력 장치가 처리를 완료하는 시점을 통보하는 역할을 한다. 
만약 인터럽트가 없다면, 입출력 작업을 시킨 후, 응용프로그램이나 운영체제는 입출력이 완료되었는지를 계속 검사하면서 대기해야 하는 폴링(polling)이라는 작업이 진행된다. 
이는 CPU에 의해 처리되기 때문에, CPU는 다른 작업을 할 수 없다. 
인터럽트가 있음으로써, 운영체제는 CPU에게 다른 프로세스를 실행하게 하고, 인터럽트를 통해 입출력의 완료를 인지하면, 입출력을 기다리는 프로세스를 준비 상태로 만들고
, 다음 스케줄 때, 실행시키는 전형적인 다중 프로그래밍을 구현할 수 있다. 
따라서, 인터럽트는 입출력 장치와 CPU가 동시에 각자의 일을 실행하게 하여, 컴퓨터 시스템이 효율적으로 작도하게 한다. 

# 3주차 과제
#### 복합문제 6번
(1) -부모 프로세스의 코드
if (pid > 0) {
  sleep(1);
  return 0;
}

-자식 프로세스의 코드
else if (pid == 0) {
  sleep(2);
  printf("부모 프로세스의 pid = %d", getppid());
  return -1;
}

(2) 고아 프로세스가 발생한다. 

(3) “부모 프로세스의 pid = 1”이 출력된다. 
이 출력은 자식 프로세스에 의해 < printf("부 모프로세스의 pid = %d", getppid()); >가 실행된 결과인데
, getppid()의 값이 1인 이유는 자식 프로세스가 고아 프로세스가 되어 프로세스 번호가 1인 init 프로세스 에 입양되었었기 때문이다. 
리눅스 종류나 버전에 따라 고아 프로세스가 미리 정해진 프로세스에게 입양되는 등 방식이 다를 수 있기 때문에 1이 아닌 다른 값이 출력될 수 있다. 

#### 복합문제 7번

![Image](https://github.com/user-attachments/assets/66ea1d40-f0d9-48e1-bda0-99c32ec0f1eb)

![Image](https://github.com/user-attachments/assets/c1f28088-db8a-4558-a054-b627522e89e7)

![Image](https://github.com/user-attachments/assets/4ca82f6b-23b7-47be-8f14-1188884d8e20)

# 4주차 과제
#### 복합문제 1번
4주차 과제 파일을 열면, 사진(과제 내용)이 있습니다. 

# 5주차 과제
#### 복합문제 1, 2번, 연습문제 27, 28번
5주차 과제 파일에 해당 과제 내용이 있습니다. 




