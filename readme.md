# Azure DevOps Hands-on Lab with GitHub Actions

## Hands-on Lab 개요

* [ASP.NET 웹앱](https://learn.microsoft.com/ko-kr/azure/app-service/quickstart-dotnetcore?tabs=net60&pivots=development-environment-vscode)을 Azure의 Azure App Service에 배포하고, GitHub Actions를 사용하여 CI/CD pipeline을 구성함.

* 주요 특징
  * Pipeline 파일은 /.github/workflows 경로에 있는 YAML(.yml) 파일에서 정의됨
  * 배포 자격증명은 Publish Profile, Service Principal, OpenID Connect
  * CI와 CD 스테이지를 분리하고 승인 과정 생성
  * Connection String등의 Secret정보들은 KeyVault를 통해 안전하게 중앙 집중 관리
  * 정적 분석 및 수집 도구를 이용하여 테스트 결과 및 정적점검 현황 확인

## 사전 요구 사항 (필요 도구)

* Azure 구독. Azure 구독이 없는 경우 [체험 계정](https://azure.microsoft.com/ko-kr/free/?WT.mc_id=A261C142F)을 만듭니다.
* [GitHub 계정](https://github.com/)
* [Git Client 설치](https://git-scm.com/downloads)
* [Azure Cli](https://docs.microsoft.com/ko-kr/cli/azure/install-azure-cli)
* [Visual Studio Code](https://code.visualstudio.com/download)
* [Visual Studio Code WSL](https://learn.microsoft.com/en-us/windows/wsl/)

## 사용 리소스 및 환경
* Azure App Service
* Azure Container Registry
* Azure Key Vault
* Azure Contrainer Registry
* GitHub Repository
* GitHub Actions for CI/CD Pipeline
* [Optional] SonarQube


## 실습 순서

* [Step 1. Azure에서 ASP.NET Core 웹앱 만들기](https://github.com/jeongaelee/ProjectJourneyModule7-GitHubActions/blob/master/step1.md)
* [Step 2. GitHub Repository에 코드 업로드](https://github.com/jeongaelee/ProjectJourneyModule7-GitHubActions/blob/master/step2.md)
* [Step 3. GitHub Actions CI/CD 파이프라인 구성 - Build](https://github.com/ProjectJourneyModule7-GitHubActions/blob/master/step3.md)
* [Step 4. GitHub Actions CI/CD 파이프라인 구성 - Deploy](https://github.com/ProjectJourneyModule7-GitHubActions/blob/master/step4.md)
* [Step 5. CodeQL을 이용하여 코드 보안 검사](https://github.com/jeongaelee/ProjectJourneyModule7-GitHubActions/blob/master/step5.md)
* [Step 6. Step 6. GitHub Actions 워크플로에서 Key Vault Secret(비밀) 사용](https://github.com/jeongaelee/ProjectJourneyModule7-GitHubActions/blob/master/step6.md)
