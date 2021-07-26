# CPU 스케줄링 알고리즘
------------------------------------------------
## CPU Scheduling
Ready Que, 혹은 Main memory 안에 여러 개의 프로세서들이 줄을 서서 기다리고 있을 때 하나의 작업이 끝나고 난 뒤 어느 프로세스를 수행할지를 결정하는 것.

* Preemptive(선점) vs Non-preemptive(비선점)
선점: CPU가 어떤 프로세서를 수행 중인 상태일 때, 대기 중인 프로세서도 없고 프로세서 수행이 진행 중임에도 강제로 다른 프로세스를 수행할 수 있도록 하는 방식.
비선점: CPU가 어떤 프로세스를 수행 중인 상태일 때, 수행 중인 프로세스가 종료되거나 다른 프로세서를 수행하기 전까지는 스케줄링이 일어나지 않는 방식.

* Scheduling criteria
어떤 스케줄링 방식이 더 좋은지에 대한 척도

1. CPU Utilization(CPU 이용률) : CPU가 얼마나 일하는가? (단위: %)
2. Throughput(처리율) : 단위 시간 당 몇 개의 작업이 끝나는가? (단위: jobs/sec)
3. Turnaround time(반환 시간) : 어떤 작업이 Ready Que에 들어와서 작업을 마치고 나가는 데까지 소요되는 시간
4. Waiting time(대기 시간) : CPU의 서비스를 받기 위해 얼마나 기다려야 하는가(->Ready Que에서)
5. Response time(응답 시간) : 인터럽트 서비스에서 중요한 개념. 처음 응답이 나올 때까지 소요되는 시간

## CPU Scheduling Algorithms

> First-Come, First-Served(FCFS) => 먼저 온 서비스를 먼저 처리  
- 가장 간편하고 일반적으로 공평한 방법

Example: Ready Queue에 처리 시간(burst time)이 다른 세 개의 프로세스가 다음과 같은 순서로 들어온다.  
P1 : 24 msec
P2 : 3 msec
P3 : 3 msec
=> P1에서 P3까지 시간은 총 30msec
=> AWT(averge wating time) : {0(P1의 대기시간) + 24(P2의 대기시간) + 27(P3의 대기시간)}/3  = 17msec

만약, 순서를 뒤바꾸어 P3 -> P2 -> P1 순서로 처리한다면,
=> AWT = (6+3+0)/3 = 3msec

척도를 Wating Time으로 했을 때 두 번째 방법이 더 효율적이다. 먼저 실행된 프로세스 뒤에 있는 프로세스들은 무조건 대기해야 하기 때문(Convoy Effect:호위효과).
따라서, FCFS 방식처럼 들어온 순서대로 처리하는 방법은 항상 효율적이지 않다. 

=> Non-Preemptive Scheduling

> Shortest-Job-First(SJF) => 작업 시간이 짧은 것을 먼저 처리  

 
* Priority => 우선순위가 높은 것들을 먼저 처리
* Round-Robin(RR) => 돌면서 순서대로 처리
* Multilevel Queue => 큐를 여러 개 두어 처리
* Multilevel Feedback Queue

