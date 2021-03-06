# 모듈 11 - 랩 1 - 연습 1 - DLP 정책 관리  


이 연습에서는 Adatum의 보안 관리자인 Holly Dickson의 역할을 맡아 가상화된 랩 환경에 배포되어 있는 Microsoft 365를 사용합니다. 현재 진행 중인 Microsoft 365 파일럿 프로젝트의 다음 단계에서는 Adatum의 DLP(데이터 손실 방지) 정책을 구현합니다. 먼저 사용자 지정 DLP 정책을 만든 다음 전자 메일 메시지 보관 및 중요한 데이터가 포함된 전자 메일 관련 DLP 정책을 테스트합니다. 

### 작업 1 - 사용자 지정 설정을 사용하여 DLP 정책 만들기

이 연습에서는 보안 및 준수 센터에서 중요한 데이터를 사용자들이 공유하지 못하도록 하는 데이터 손실 방지 정책을 만듭니다. 여기서 만들 DLP 정책은 사용자가 미국 사회 보장 주소가 포함된 콘텐츠를 공유하려고 하면 알림을 표시합니다.

1. 클라이언트 1 VM(**LON-CL1**)에는 **LON-CL1\Admin** 계정으로, Microsoft 365에는 **Holly Dickson**으로 로그인되어 있는 상태여야 합니다. 

2. 그리고 **Microsoft Edge**에는 Office 365 보안 및 준수 센터 탭이 열려 있어야 합니다. 해당 탭이 열려 있으면 탭을 선택하고 다음 단계를 진행합니다. 해당 탭을 닫았다면 새 탭에서 `https://protection.office.com` 으로 이동합니다.

3. **보안 및 준수 센터**의 왼쪽 탐색 창에서 **데이터 손실 방지**, **정책**을 차례로 선택합니다.

4. **정책** 창에서 **+정책 만들기**를 선택하여 새 데이터 손실 방지 정책을 만드는 마법사를 시작합니다.

5. **서식 파일로 시작하거나 사용자 지정 정책 만들기** 페이지에서 왼쪽 창의 **사용자 지정**을 선택하고 가운데 창에서는 **사용자 지정 정책**을 선택해야 합니다. 하지만 이 두 옵션은 이미 기본적으로 선택되어 있으므로(선택되어 있지 않으면 지금 선택) **다음**을 선택합니다.

6. **정책 이름 지정** 페이지의 **이름** 필드에 `Social Security DLP Policy`을 입력하고 **설명** 필드에는 `Protect social security numbers from being shared`를 입력합니다. **다음**을 선택합니다.

7. **위치 선택** 페이지에서 **켜짐**(**Exchange 전자 메일, SharePoint, OneDrive, Teams 채팅 및 채널 메시지의 경우)** 및 **꺼짐**(**Devices, Microsoft Cloud App Security, 온-프레미스 리포지토리의 경우)**을 선택한 후에 **다음**을 선택합니다.

8. **고급 DLP 규칙 사용자 지정** 페이지에서 **+규칙 만들기**를 선택합니다.

9. **규칙 만들기** 페이지의 **이름** 필드에 **사회 보장 번호**를 입력합니다.

10. **조건** 아래에서 **+조건 추가**를 클릭한 후에 **다음이 포함된 콘텐츠**를 클릭합니다.

11. **기본값**을 그대로 유지하고 **추가**를 선택한 후에 **중요한 정보 유형**을 선택합니다.

12. 검색 필드에 `사회`를 입력하고 Enter 키를 누른 후에 검색 결과가 표시될 때까지 기다립니다.

13. 검색 결과 목록에서 **미국 SSN(사회 보장 번호)** 체크박스를 선택하고 **추가**를 선택합니다.

14. **조건 추가**를 클릭하고 **Microsoft 365의 콘텐츠가 공유됨**을 선택합니다.

15. 그 아래의 필드에서 **조직 내부 사용자만**이 표시되는지 확인합니다.

16. **작업** 섹션으로 스크롤하여

17. **+ 작업 추가*를 클릭합니다.

18. **Microsoft 365 위치에서 액세스 제한 또는 콘텐츠 암호화**를 선택합니다.

19. **Microsoft 365 위치에서 액세스 제한 또는 콘텐츠 암호화** 체크박스를 선택하고 **모든 사람 차단**을 선택합니다.

20. **문제 보고서**로 스크롤합니다.

21. **관리 경고 및 보고서에서 이 심각도 수준 사용** 필드에서 **보통**을 선택합니다.

22. **규칙이 일치하면 관리자에게 알림 보내기**에서 슬라이더 막대를 **켜짐**으로 이동합니다.

23. **저장**을 선택합니다.

24 **다음**을 클릭합니다.

24. **정책 테스트 또는 켜기** 페이지에서 **예, 지금 켜겠습니다.**를 선택하고 **다음**을 선택합니다.

25. **제출**을 클릭합니다.

조직에서 전송하거나 공유하는 전자 메일과 문서에서 미국 사회 보장 번호를 검사하는 DLP 정책을 만들었습니다.


# 연습 2 계속 진행 
