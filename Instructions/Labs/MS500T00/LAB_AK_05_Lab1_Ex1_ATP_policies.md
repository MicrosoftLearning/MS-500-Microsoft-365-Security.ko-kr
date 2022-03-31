# 모듈 5 - 랩 1 - 연습 1 - ATP 정책 구현  

이전 연습에서 Holly Dickson의 전역 관리자 계정을 설정했으며, 현재 Microsoft 365에 Holly로 로그인한 상태입니다. Adatum 파일럿 프로젝트의 이 단계에서는 기존 ATP 안전한 링크 정책을 편집합니다. 그런 다음 안전한 첨부 파일 정책을 만들고 SharePoint, OneDrive, Microsoft Teams를 대상으로 Advanced Threat Protection을 활성화합니다. 그리고 두 정책의 유효성을 검사하여 정책이 정상적으로 작동하는지도 확인합니다.

### 작업 1 - 안전한 링크 정책 만들기

이 작업에서는 회사 전체 차단된 URL 목록에 **http://tailspintoys.com** URL을 추가합니다. 그리고 테넌트의 모든 사용자에게 적용되는 ATP 안전한 링크 받는 사람 정책을 만듭니다.

1. 클라이언트 1 VM(**LON-CL1**)에는 **LON-CL1\Admin** 계정으로, Microsoft 365에는 **Holly Dickson**으로 여전히 로그인되어 있는 상태여야 합니다.

2. 그리고 Microsoft 365 보안 및 규정 준수 센터가 계속 표시되어 있어야 합니다. 그렇지 않은 경우에는 브라우저에서 `https://protection.office.com`을 입력합니다.

3. **보안 및 규정 준수 센터**의 왼쪽 탐색 창에서 **위협 관리**, **정책**을 차례로 선택합니다.

4. **정책** 창에서 필요한 경우 오른쪽으로 스크롤하여 **안전한 링크** 타일을 선택합니다.

5. **안전한 링크** 창에서 **전역 설정**을 클릭합니다.

6. **활성 안전한 링크 정책에 포함된 사용자의 전역 설정** 창의 **다음 URL 차단** 섹션에서 차단하려는 URL을 입력할 수 있습니다. 이 테스트 랩에서는 **올바른 URL을 입력하세요.** 필드에 `http://tailspintoys.com`을 입력하여 정책에 해당 URL을 추가합니다.

7. **저장**을 선택합니다.

8. **+ 만들기**를 선택하여 새 받는 사람 정책을 추가합니다.

9. **정책 이름 지정** 창의 **이름** 필드에 랩 세션 `Unique Name`을 입력합니다. **다음**을 클릭합니다.

10. **사용자 및 도메인** 창의 **그룹** 필드에 `All Company`를 입력하고 목록에서 모든 회사를 선택합니다. **다음**을 클릭합니다.

11. **보호 설정** 창에서 다음 옵션을 선택하고 **다음**을 클릭합니다.

    - **메시지의 알 수 없는 잠재적 악성 URL에 대한 작업을 선택합니다.** 아래에서 다음 작업을 수행합니다. **설정 - 사용자가 링크를 클릭하면 URL이 다시 작성되고 알려진 악성 링크 목록에 포함되어 있는지 확인합니다.** 를 선택합니다.

    - Microsoft Teams 내의 알 수 없는 URL 또는 잠재적 악성 URL에 대해서도 **설정**을 선택합니다.

    - **의심스러운 링크 및 파일을 가리키는 링크에 대해 실시간 URL 검사를 적용합니다.** 옆의 체크박스를 선택합니다.

    - **조직 내부 사용자가 보낸 전자 메일 메시지에 안전한 링크를 적용합니다.** 옆의 체크박스를 선택합니다.

12. **알림** 창에서 기본 알림 텍스트를 선택한 상태로 유지합니다. **다음**을 클릭합니다.

13. **검토** 창에서 **제출**을 선택하여 정책을 만듭니다.

14. Office 365 보안 및 준수 탭은 이후 작업에서 사용할 수 있도록 열어 둡니다.

### 작업 2 - 안전한 링크 정책 유효성 검사

이 작업에서는 방금 만든 안전한 링크 정책, 즉 `http://tailspintoys.com` URL로 이동하는 링크를 차단하는 정책을 테스트합니다.

1. 클라이언트 1 VM(**LON-CL1**)에는 **LON-CL1\Admin** 계정으로, Microsoft 365에는 **Holly Dickson**으로 로그인되어 있는 상태여야 합니다.

2. **Microsoft Edge** 브라우저에서 **Microsoft Office 홈** 탭을 선택(또는 `https://office.com`으로 이동)하여 **Outlook**을 선택합니다.

3. **Outlook이 업데이트되었습니다.** 메시지가 표시되면 **나중에**를 선택하고, **환영** 메시지가 표시되면 메시지를 닫습니다.

4. **웹용 Outlook**의 화면 왼쪽 위에서 **새 메시지**를 선택합니다.

5. 오른쪽 창에서 다음 전자 메일 정보를 입력합니다.

    - 받는 사람: MOD 관리자에게 전자 메일을 보낼 것이므로 **받는 사람** 필드에 **mod**를 입력한 후 드롭다운 목록에서 **MOD 관리자** 전자 메일 주소를 선택합니다.

    - 제목 추가: `Free stuff from Microsoft`

    - 메시지 추가: `Please click on me for free toys from Microsoft`.

6. 메시지 본문에 추가한 텍스트를 선택합니다.

7. 세부 정보 창 아래쪽의 메시지 본문 아래에 작업 표시줄이 있습니다. 작업 표시줄에서 **하이퍼링크 삽입** 아이콘을 선택하여 링크 삽입 창을 표시합니다.

9. **링크 삽입** 창의 **표시 형식** 필드에 메시지 본문에서 강조 표시한 텍스트가 표시됩니다. **웹 주소(URL)** 필드에 다음 URL을 입력합니다. `http://tailspintoys.com/aboutus/freetoys`.

10. **확인**을 선택합니다.

11. 전자 메일 본문에서 메시지가 여전히 선택되어 있는 상태여야 합니다. 메시지 본문에서 아무 곳이나 클릭하여 강조 표시를 해제합니다. 텍스트가 파란색으로 표시되며 텍스트에 밑줄이 표시됩니다. 이러한 서식은 해당 메시지에 특정 URL로 이동하는 하이퍼링크가 적용되었음을 나타냅니다.

12. 메시지 위에 표시되는 메뉴 모음에서 **보내기**를 선택합니다(페이지 아래쪽의 **보내기** 단추를 선택해도 됨).

13. 이제 Outlook에서 MOD 관리자의 받은 편지함을 열어 방금 Holly의 계정에서 보낸 전자 메일에 이전 작업에서 만든 ATP 정책이 적용되었는지 유효성을 검사하겠습니다. 이렇게 하려면 클라이언트 2 VM(LON-CL2)으로 전환해야 합니다.

14. 필요한 경우 **암호** 필드에 **Ps55w.rd**를 입력하여 **Admin** 계정으로 VM에 로그인합니다.

15. 작업 표시줄에서 **Microsoft Edge** 아이콘을 선택하고 창을 최대화한 다음 주소 표시줄에 다음 URL을 입력합니다. `https://outlook.office365.com`

16. 여기서는 MOD 관리자로 로그인할 것이므로 **로그인** 창에 **admin@M365xZZZZZZ.onmicrosoft.com**을 입력하고(여기서 ZZZZZZ는 랩 호스팅 공급자가 제공한 테넌트 ID임) **다음**을 선택합니다.

17. **암호 입력** 창에 랩 호스팅 공급자가 제공한 암호를 입력하고 **로그인**을 선택합니다. 셀프 서비스 암호 정보를 입력하라는 메시지가 표시되면 **취소**를 클릭합니다.

18. **Microsoft Edge는 다음에 이 사이트의 암호를 저장하고 채웁니다.** 배너에서 **안 함**을 선택하여 해당 배너를 닫습니다.

19. **로그인 상태를 유지하시겠습니까?** 대화 상자에서 **이 메시지를 다시 표시 안 함** 체크박스를 선택하고 **예**를 선택합니다.

20. **환영** 창이 표시되면 닫습니다.

21. MOD 관리자의 **받은 편지함**에서 Holly의 계정으로 보낸 전자 메일을 엽니다.

22. 전자 메일 본문에 표시되는 파란색 링크 위에 커서를 올리면 브라우저 창 아래쪽에 긴 URL이 표시됩니다. 해당 URL은 `https://nam03.safelinks.protection.outlook.com`으로 시작됩니다.

    하이퍼링크를 선택하여 열면 **Edge**에 새 탭이 열리고 다음 경고 메시지가 표시됩니다. **이 웹 사이트를 열면 위험할 수 있습니다.** 이 메시지는 ATP 안전한 링크 정책이 정상적으로 작동하며, ATP 안전한 링크로 인해 URL 액세스가 차단되었음을 나타냅니다.

23. 클라이언트 2 VM을 열어 두고, 나중에 사용할 수 있도록 Outlook에서 MOD 관리자의 받은 편지함도 열어 둡니다.

### 작업 3 - 안전한 첨부 파일 정책을 만들고 SharePoint, OneDrive 및 Microsoft Teams에 대해 ATP 활성화

이 작업에서는 ATP 안전한 첨부 파일 정책을 만듭니다. 이 정책은 M365xZZZZZZ.on microsoft.com 도메인 내의 받는 사람에게 전송된 전자 메일 첨부 파일을 테스트하여 맬웨어 유무를 확인합니다. 여기에서 받는 사람에게 전송된 전자 메일에서 차단된 첨부 파일을 제거하도록 정책을 구성합니다. 해당 전자 메일의 복사본은 추가 검토를 위해 Joni Sherman에게 리디렉션됩니다.

1. 클라이언트 1 VM(**LON-CL1**)으로 다시 전환합니다. 클라이언트 1 VM에는 **LON-CL1\Admin** 계정으로, Microsoft 365에는 **Holly Dickson**으로 여전히 로그인되어 있는 상태여야 합니다.

2. **Edge** 브라우저에서 **Office 365 보안 및 준수** 탭을 선택합니다.

3. **Office 365 보안 및 규정 준수 센터**의 왼쪽 탐색 창 내 **위협 관리** 아래에서 **정책**을 선택합니다.

4. **정책** 창에서 **안전한 첨부 파일** 타일을 선택합니다.

5. **안전한 첨부 파일** 창 페이지 위쪽의 **전역 설정** 아래 **SharePoint, OneDrive 및 Microsoft Teams의 파일 보호** 섹션에서 **SharePoint, OneDrive 및 Microsoft Teams에 대해 Office 365용 Defender 사용** 스위치를 선택합니다. **저장**을 선택합니다.

6. 메뉴 모음에서 **+ 만들기**를 선택하여 새 안전한 첨부 파일 정책을 추가합니다.

7. 새 안전한 첨부 파일 정책 창의 **이름** 필드에 `AttachmentPolicy1`을 입력하고 **다음**을 선택합니다.

8. **사용자 및 도메인**의 **사용자** 필드에 `All Company`를 입력하고 **다음**을 선택합니다.

9. **안전 첨부 파일에서 알 수 없는 맬웨어 응답** 섹션에서 **동적 배달**을 선택합니다(이 옵션을 선택하면 전자 메일은 여전히 전송되지만 첨부 파일은 검사 후 허용 가능 파일로 표시될 때까지 배달되지 않음).

10. **첨부 파일을 분리하여 메시지 리디렉션** 섹션에서 **리디렉션 사용**을 선택합니다.

11. **차단되었거나 모니터링되거나 바뀐 첨부 파일이 포함된 메시지를 지정된 전자 메일 주소로 전송** 필드에 **JoniS@M365xZZZZZZ.onmicrosoft.com**을 입력합니다(여기서 ZZZZZZ는 랩 호스팅 공급자가 제공한 고유 테넌트 ID임).

1. **검토** 창에서 앞에서 선택한 **안전 첨부 파일 검색 응답:** 및 **첨부 파일 리디렉션:** 옵션과 관련된 메시지 2개를 확인하고 **제출**을 선택합니다.

12. 조직 설정이 업데이트되려면 1~2분 정도 걸릴 수 있습니다. **업데이트 완료** 창에서 **확인**을 선택합니다.

**참고:** 방금 만든 ATP 안전한 첨부 파일 정책의 유효성을 검사할 수 있는 교육 랩을 제작하는 것은 현재로서는 불가능합니다. 이 정책의 유효성을 검사하는 방법은 악성 첨부 파일이 포함된 전자 메일을 보내는 것뿐입니다. EICAR 테스트 바이러스 등의 흔히 사용되는 테스트 바이러스를 사용할 수도 있습니다. 하지만 EICAR처럼 널리 알려진 테스트 바이러스를 사용하는 경우 해당 바이러스가 첨부된 메시지는 Office 365 ATP를 통해 처리되기 전에 격리됩니다. ATP 안전한 첨부 파일 기능은 알 수 없는 바이러스 및 제로 데이 바이러스와 맬웨어를 차단하기 위한 것인데, 이러한 첨부 파일을 만드는 것은 매우 어려우며 권장되지도 않습니다.

그러므로 실제 환경에서는 ATP 안전한 첨부 파일 정책을 정의한 후 Advanced Threat Protection 보고서를 통해 서비스 작동 방식을 확인할 수 있습니다. ATP 보고 기능을 사용하여 안전한 링크 및 안전한 첨부 파일 정책의 유효성을 검사하는 방법에 대한 자세한 내용은 [Office 365 Advanced Threat Protection의 보고서 보기](https://docs.microsoft.com/ko-kr/office365/securitycompliance/view-reports-for-atp)를 참조하세요.


# 랩 종료