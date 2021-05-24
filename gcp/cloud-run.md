# Cloud Run

`Google Cloud Platform`의 Serverless Docker Container Platform 이다.

컨테이너화된 애플리케이션(Docker Image)을 배포한다.
GCP의 `Cloud Functions`와 달리 개발 언어의 한계가 없다.

|      Lambda      | Cloud Functions |     Cloud Run      |
| :--------------: | :-------------: | :----------------: |
|     Node.js      |     Node.js     | 대부분의 언어 지원 |
|      Python      |     Python      | 대부분의 언어 지원 |
|        Go        |       Go        | 대부분의 언어 지원 |
|       Java       |      Java       | 대부분의 언어 지원 |
|       Ruby       |      Ruby       | 대부분의 언어 지원 |
|       .NET       |      .NET       | 대부분의 언어 지원 |
| Runtime API 지원 |        ?        | 대부분의 언어 지원 |

---

컨테이너화된 애플리케이션을 배포하는 특징때문에 `AWS`의 `Fargate`와 비교되기도 하나,  
`Fargate`와 달리 `Cloud Run`은 `Cloud Functions`처럼 요청이 있을 경우에만 실행되고, 실행 시간만큼 과금 된다.  
트래픽이 많지 않은 사이드 프로젝트를 Cloud Run을 통하여 배포하면 거의 돈이 들지 않는다고 한다.
