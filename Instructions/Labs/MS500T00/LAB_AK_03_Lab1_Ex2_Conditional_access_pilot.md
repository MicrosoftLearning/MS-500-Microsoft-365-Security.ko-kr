---
ms.openlocfilehash: 122bdaf3d5a1dbd026c22458869ac41fc06d4380
ms.sourcegitcommit: 25b9793190d40e69ed31815267fb6754397768bd
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/02/2022
ms.locfileid: "137943331"
---
# <a name="module-3---lab-1---exercise-2----mfa-conditional-access-complete-an-azure-multi-factor-authentication-pilot-roll-out"></a>모듈 3 - 랩 1 - 연습 3 - MFA 조건부 액세스(Azure Multi-Factor Authentication 파일럿 출시 완료)


이 연습에서는 Azure Portal에 로그인할 때 Azure MFA(Multi-Factor Authentication)를 사용하도록 설정하는 조건부 액세스 정책을 구성합니다. 이 정책은 특정 파일럿 사용자 그룹에 배포되고 테스트됩니다. 조건부 액세스를 사용하여 Azure MFA를 배포하면 기존에 적용된 방법에 비해 조직과 관리자에게 상당히 많은 유연성이 제공됩니다.

- Azure Multi-Factor Authentication 사용
- Azure Multi-Factor Authentication 테스트


### <a name="task-1-enable-azure-multi-factor-authentication"></a>작업 1: Azure Multi-Factor Authentication을 사용하도록 설정

1.  전역 관리자인 Holly Dickson으로 로그인되어 있는 Azure Portal로 돌아옵니다.

1.  허브에서 **Azure Active Directory** 로 이동합니다.

1.  **그룹**, **+ 새 그룹** 을 차례로 클릭합니다.

     ![스크린샷](../Media/cb9c5324-cbb6-476e-9c7d-1920de301d40.png)

1.  다음 정보를 입력하고 **만들기** 를 선택합니다.

      * 그룹 유형: `Security`
      * 그룹 이름: `MFA Pilot`
      * 그룹 설명: `MFA Pilot Group`
      * 구성원 자격 유형: `Assigned`
      * 구성원: `Lynne Robbins`을 선택합니다.
  
  
      ![스크린샷](../Media/5457b62d-dc78-4043-bd72-3d7901bbcd71.png)
  
2.  **Azure Active Directory** 로 이동하여 **보안** 을 클릭하고 **정책** 블레이드에서 **조건부 액세스** 를 선택합니다.


3.  **+ 새 정책** 을 선택한 다음 **새 정책 만들기** 를 선택합니다.


4.  정책 이름 지정 `MFA Pilot`
5.  **사용자 또는 워크로드 ID** 에서 **0명의 사용자 또는 워크로드 ID가 선택됨** 을 클릭합니다. **사용자 및 그룹 선택** 라디오 단추를 선택하고 **사용자 및 그룹** 상자를 선택합니다.
    * 파일럿 그룹 선택 `MFA Pilot`
    * **선택** 클릭

6.  **클라우드 앱 또는 작업** 섹션에서 **클라우드 앱, 작업 또는 인증 컨텍스트가 선택되지 않음** 을 클릭합니다.
    * **선택** 을 클릭합니다. Azure Portal용 클라우드 앱인 `Microsoft Azure Management`를 선택합니다.
    * **앱 선택** 을 클릭합니다.

7.  **조건** 섹션은 건너뜁니다.
8.  **권한 부여** 아래의 **Access 제어** 섹션에서 **컨트롤 0개 선택됨** 을 클릭하고 **액세스 권한 부여** 라디오 단추가 선택되어 있는지 확인합니다.
    * **Multi-Factor Authentication 필요** 확인란을 선택합니다.
    * **선택** 클릭

9.  **세션** 섹션을 건너뜁니다.
10. **정책 사용** 토글을 **켜기** 로 설정합니다.
11. **생성**

    **참고**: 정책 적용이 실패하면 작업 내용을 확인하고 **만들기** 를 다시 클릭합니다. 

### <a name="task-2-test-azure-multi-factor-authentication"></a>작업 2: Azure Multi-Factor Authentication 테스트


조건부 액세스 정책이 작동하는지 증명하려면 MFA를 요구하지 않아야 하는 리소스에 로그인 후 MFA가 필요한 Azure Portal에 로그인하는 테스트를 수행하세요.


2.  InPrivate 또는 incognito 모드에서 새 브라우저 창을 열고 **`https://portal.azure.com`** 으로 이동합니다.

       * Lynne Robbins 사용자로 로그인합니다(Lynne의 암호는 랩 호스팅 공급자가 제공한 MOD 관리자 암호와 동일할 가능성이 높음). 그런 다음 이제는 Azure Multi-Factor Authentication에 등록하고 MFA를 사용해야 함을 확인합니다.
       * 브라우저 창을 닫습니다.



# <a name="end-of-lab"></a>랩 종료
