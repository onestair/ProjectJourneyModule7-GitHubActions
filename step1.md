# Azure DevOps Hands-on Lab with GitHub Actions

## Step 1. Azure에서 ASP.NET Core 웹앱 만들기

> 본 실습의 Step 1은 [빠른 시작: ASP.NET 웹앱 배포](https://learn.microsoft.com/ko-kr/azure/app-service/quickstart-dotnetcore?tabs=net60&pivots=development-environment-vscode) 문서의 내용을 발췌하였습니다.

## 사전 요구 사항
* Visual Studio에 [Azure 도구 확장](https://marketplace.visualstudio.com/items?itemName=ms-vscode.vscode-node-azure-pack) 설치
* [최신 .NET 6.0 SDK 설치](https://dotnet.microsoft.com/download/dotnet/6.0)

## ASP.NET 웹앱 만들기
1. MyFirstAzureWebApp이라는 새 폴더를 만들고, Visual Studio Code에서 "File->Open Folder"로 폴더를 엽니다.

2. Visual Studio Code에서 "Terminal->New Terminal" 메뉴를 선택하여 새 터미널 창을 엽니다.

3. Visual Studio Code 터미널에서 "dotnet new webapp" 명령을 사용하여 새 .NET 웹앱을 만듭니다.
    > dotnet new webapp

4. Visual Studio Code 터미널에서 "dotnet run" 명령을 사용하여 애플리케이션을 로컬에서 실행합니다.
    > dotnet run --urls=https://localhost:5001/

5. 웹 브라우저를 열고 https://localhost:5001의 앱으로 이동합니다. 페이지에 아래와 같이 ASP.NET Core 6.0 웹앱 템플릿이 표시됩니다.

    !["id01"](images/step1-01.png)

## 웹앱 게시

1. [Azure Portal](https://portal.azure.com/)으로 접속하여 새 리소스 그룹을 생성합니다.
2. Visual Studio Code에서 명령 팔레트를 엽니다(Ctrl+Shift+P).
3. 프롬프트에 다음과 같이 응답합니다.
    * MyFirstAzureWebApp을 배포할 폴더로 선택합니다.
    * 메세지가 나타나면 "Add Config"를 선택합니다.
    * 메세지가 표시되면 Azure 계정에 로그인합니다.
    * "Subscription"을 선택합니다.
    * "Create new Web App... Advanced"을 선택합니다.
    * 전역적으로 고유한 이름 입력에는 모든 Azure에서 고유한 이름을 사용합니다(유효한 문자: a-z, 0-9 및 - ). 회사 이름과 앱 식별자를 조합하여 사용하는 것이 좋습니다.
    * "Create new resource group"를 선택하고, myResourceGroup와 같은 이름을 지정합니다.
    * 런타임 스택 선택 메시지가 나타나면 .NET 6을 선택합니다.
    * 운영 체제 (Windows 또는 Linux)를 선택합니다.
    * 가까운 위치를 선택합니다.
    * "Create a new App Service plan"을 선택하고, 이름을 제공하고, "F1 Free" 가격 계층을 선택합니다.
    * Application Insights 리소스에 대해 "Skip for now"를 선택합니다.
4. 항상 "MyFirstAzureWebApp" 작업 영역을 <앱이름>에 배포 팝업에서 Visual Studio Code가 해당 작업 영역에 있을 때마다 동일한 App Service 앱에 배포되도록 "예"를 선택합니다.
5. 게시가 완료되면 알림에서 "Browse Website"를 선택하고, 메세지가 나타나면 "Open"을 선택합니다.
    !["id02"](images/step1-02.png)


## 실습 순서

* [Step 1. Azure에서 ASP.NET Core 웹앱 만들기](https://github.com/jeongaelee/Module7-webapp-github-actions/blob/master/step1.md)
* [Step 2. GitHub Repository에 코드 업로드](https://github.com/jeongaelee/Module7-webapp-github-actions/blob/master/step2.md)
* [Step 3. GitHub Actions CI/CD 파이프라인 구성 - Build](https://github.com/jeongaelee/Module7-webapp-github-actions/blob/master/step3.md)
* [Step 4. GitHub Actions CI/CD 파이프라인 구성 - Deploy](https://github.com/jeongaelee/Module7-webapp-github-actions/blob/master/step4.md)
* [Step 5. CodeQL을 이용하여 코드 보안 검사](https://github.com/jeongaelee/Module7-webapp-github-actions/blob/master/step5.md)
* [Step 6. Step 6. GitHub Actions 워크플로에서 Key Vault Secret(비밀) 사용](https://github.com/jeongaelee/Module7-webapp-github-actions/blob/master/step6.md)