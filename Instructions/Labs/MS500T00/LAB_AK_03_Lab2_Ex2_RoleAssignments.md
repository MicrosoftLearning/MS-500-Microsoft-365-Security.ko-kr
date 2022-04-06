---
ms.openlocfilehash: 31718150ab2a0d5a4607e667b6936d7fd541ecdb
ms.sourcegitcommit: c203d5d5aaaf93bae4a8af2ae04b27f6314242c4
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/13/2021
ms.locfileid: "137820986"
---
# <a name="module-3---lab-2---exercise-2---assign-directory-roles"></a>모듈 3 - 랩 2 - 연습 2 - 디렉터리 역할 할당


### <a name="task-1--make-a-user-eligible-for-a-role"></a>작업 1:  사용자에게 역할 부여


다음 작업에서는 사용자에게 Azure AD 디렉터리 역할을 할당할 수 있도록 설정합니다.


1.  Azure Portal에 로그인

1.  Azure Portal에서 **모든 서비스** 를 클릭하고 `Azure AD Privileged Identity Management`를 선택합니다.

     ![스크린샷](../Media/a52510a3-b2a2-4b21-91a8-ee7f34b39a72.png)

1.  **관리** 아래에서 **Azure AD 역할** 을 선택한 다음 관리 아래에서 **역할** 을 선택합니다. 이 옵션이 아직 회색으로 표시된다면 브라우저를 새로 고쳐야 할 수 있습니다.

1.  `Billing Administrator`를 선택합니다.

1.  **+ 할당 추가** 를 선택하여 구성원 선택을 엽니다. 할당 추가 화면에서 **선택한 구성원이 없음** 을 클릭합니다.

1.  **구성원 선택 화면** 에서 `Patti Fernandez`를 선택하고 **선택** 을 클릭합니다.

1.  할당 추가 화면에서 **다음** 을 클릭합니다. **할당** 을 클릭합니다.  할당 창에서 추가한 구성원을 검토합니다.

1.  역할이 할당되면 선택한 사용자가 멤버 목록에 해당 역할의 **적격** 사용자로 표시됩니다. 


### <a name="task-2-make-a-role-assignment-permanent"></a>작업 2: 역할 영구 할당


역할 할당을 영구적으로 지정하려면 다음 단계를 수행합니다.



1.  Azure Portal에서 **모든 서비스** 를 클릭하고 `Azure AD Privileged Identity Management`를 선택합니다.

     ![스크린샷](../Media/a52510a3-b2a2-4b21-91a8-ee7f34b39a72.png)

1.  **Azure AD 역할** 을 클릭합니다.

1.  **할당** 을 클릭합니다.
 
1.  **업데이트** 를 클릭하여 Patti를 대금 청구 관리자로 할당한 후 **영구적으로 적격** 체크박스를 선택합니다.  구성원 자격 설정에서 **저장** 을 클릭합니다.

**결과**: 이제 Patti Fernandez의 구성원 자격에 대금 청구 역할이 **영구** 로 표시됩니다.  즉, Patti는 대금 청구 관리자 역할로 권한을 상승할 수 있도록 영구적으로 설정되었습니다.


### <a name="task-3-remove-a-user-from-a-role"></a>작업 3: 역할에서 사용자 제거


역할 할당에서 사용자를 제거할 수 있지만 영구 전역 관리자인 사용자가 최소 한 명은 항상 있어야 합니다.



1.  Azure Portal에서 **모든 서비스** 를 클릭하고 `Azure AD Privileged Identity Management`를 선택합니다.

     ![스크린샷](../Media/a52510a3-b2a2-4b21-91a8-ee7f34b39a72.png)

1.  **Azure AD 역할** 을 클릭합니다.

1.  **할당** 을 클릭합니다.

1.  구성원 필터를 사용하여 Patti Fernandez를 다시 선택합니다.
 
1.  작업 영역의 적격 할당 아래에서 **제거** 를 클릭합니다.
 
1.  확인하라는 메시지에서 **예** 를 클릭합니다. 역할 할당이 제거됩니다.


# <a name="continue-to-exercise-3"></a>연습 3 계속 진행
