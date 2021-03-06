### 회원가입/로그인 후 보안설정까지 해보자

##### 1. AWS 홈페이지에서 회원가입을 한다

---
##### 2. 회원가입이 되었으면 우측 상단 주황색 버튼을 클릭해 로그인을 한다
<img src="img/01_LoginToSecure/01_HomePage.png" alt="AWS Homepage" />
   
![Console Page](img/01_LoginToSecure/02_ConsolePage.PNG)

---
##### 3. All Service 를 클릭 후 IAM 메뉴를 클릭해 들어간다
![Service Menu](img/01_LoginToSecure/03_ServiceMenu.PNG)
---
##### 4. 그러면 다음과 같이 아직 보안이 부족하다고 나올것이다.
![IAM Page](img/01_LoginToSecure/04_SecurityPage.PNG)

> 우린 여기있는 항목들을 모두 만족시킬 것이다.

---
##### 5. Activate MFA ... 항목을 클릭하면 접속되는 페이지이다
##### 아래 사진들을 따라서 설정을 완료하자
![Security Page](img/01_LoginToSecure/05_MFAPage.PNG)
> 여기서 Activate MFA 버튼을 클릭한다

![MFA Popup1](img/01_LoginToSecure/06_MFAPopup.PNG)
> 자신에게 맞는 MFA 디바이스를 선택한다
> 나는 모바일 어플을 쓸 것 이기 때문에 가상 디바이스를 선택했다

![MFA App List](img/01_LoginToSecure/07_MFAAppList.PNG)
> MFA 어플 목록이다

![MFA Popup2](img/01_LoginToSecure/08_MFAPopup2.PNG)
> 1번 항목: 링크를 통해 위에 있는 어플 목록을 볼 수 있다
> 2번 항목: Show QR Code 를 클릭해 QR 코드로 어플에 등록한다
> 3번 항목: MFA 코드는 시간이 지남에 따라 바뀌는데, 이때 연속된 두 개의 코드를 입력해준다(코드 2는 코드 1 직후 바뀐 코드)

![MFA Popup3](img/01_LoginToSecure/09_MFAPopup3.PNG)
> MFA 설정이 완료되었다

---
##### 6. 다시 IAM 홈으로 돌아와서 Create individual IAM users 항목에 들어간다
##### 그 다음 아래 사진들을 따라서 설정을 완료하자

![IAM User Page](img/01_LoginToSecure/10_IAMUserPage.PNG)
> 왼쪽 상단의 Add user 버튼을 누른다

![IAM User Page2](img/01_LoginToSecure/11_IAMUserPage2.PNG)
> 여기서 user name 을 주고 Access type 은 AWS Management Console access 를 주자
> IAM 유저도 콘솔에 들어와서 작업 할 수 있게 해줄거다

![IAM User Page3](img/01_LoginToSecure/12_IAMUserPage3.PNG)
> 그룹을 지정해 권한을 지정한다
> 난 만들어둔 그룹이 없어서 새로 만들겠다

![Create Group](img/01_LoginToSecure/13_CreateGroup.PNG)
> 그룹 이름과 권한을 지정해준다
> 권한 잘 모르겠으니 루트 권한을 준다

![IAM User Page4](img/01_LoginToSecure/14_IAMUserPage4.PNG)
> 태그를 생성하라는데 optional 이라서 안했다
> 이제 다음 버튼을 눌러서 유저 생성을 마친다

![Account ID](img/01_LoginToSecure/15_AccountID.PNG)
> IAM 유저로 로그인 하려면 AWS Account ID 가 필요하다
> 이건 여기서 확인 할 수 있다.
---

##### 7. 다시 IAM 메인페이지로 돌아오면 맨 아래 IAM password policy 만 남아있다
##### 이 항목을 선택해 들어간다
##### 그 다음 아래 사진들을 따라서 설정을 마무리하자

![Password Policy](img/01_LoginToSecure/16_PasswordPolicy.PNG)
> Set password policy 버튼을 누른다

![Password Policy2](img/01_LoginToSecure/17_PasswordPolicy2.PNG)
> 여기에 비밀번호 정책을 설정해준다

#### 마무리

![Secure Setting Complete](img/01_LoginToSecure/18_SecureSettingComplete.PNG)
##### 모든 상태가 초록색이 된걸 볼 수 있다
##### 다음에는 EC2 인스턴스를 만들어보자