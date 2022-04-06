---
ms.openlocfilehash: 688125296622bda20edfda3b0b6ddf9a43f3a389
ms.sourcegitcommit: c203d5d5aaaf93bae4a8af2ae04b27f6314242c4
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/13/2021
ms.locfileid: "137820991"
---
# <a name="module-3---lab-2---exercise-4---directory-roles-general"></a>모듈 3 - 랩 2 - 연습 4 - 디렉터리 역할(일반)


### <a name="task-1-start-an-access-review-for-azure-ad-directory-roles-in-pim"></a>작업 1: PIM에서 Azure AD 디렉터리 역할의 액세스 검토 시작


사용자가 더 이상 필요 없는 권한 있는 액세스를 가진 경우 "오래된" 역할 할당이 됩니다. 이러한 오래된 역할 할당과 관련된 위험을 줄이기 위해 권한 있는 역할 관리자 또는 전역 관리자는 정기적으로 액세스 검토를 생성하여 사용자에게 부여된 역할을 검토하도록 관리자에게 요청해야 합니다. 이 작업에서는 Azure AD PIM(Privileged Identity Management)에서 액세스 검토를 시작하는 단계를 설명합니다.


1.  전역 관리자인 Holly Dickson의 계정으로 로그인되어 있는 브라우저로 돌아옵니다.

1.  PIM 애플리케이션 기본 페이지에서 **관리** 섹션 아래의 **Azure AD 역할** 을 선택하고 **액세스 검토**, **새로 만들기** 를 차례로 선택합니다.

     ![스크린샷](../Media/1704b3b2-05a7-47c8-a3e3-20ba6546b9d6.png)

1.  다음 세부 정보를 입력하고 **시작** 을 클릭합니다.

      - 검토 이름: `Global Admin Review`
      - 시작 날짜: `Enter Today's Date` 
      - 빈도: `Drop down to One time`
      - 종료 날짜: `Enter End of next month`
      - 역할 구성원 검토: `Global Administrator`
      - 검토자: `Holly Dickson`
 
 
     ![스크린샷](../Media/84274ed2-be53-4b3f-853a-c85f0dcfeab2.png)
 
1.  검토가 완료되어 활성 상태로 표시되면 **전역 관리자 검토** 를 클릭합니다. Azure에서 보기를 새로 고쳐야 할 수도 있습니다.

1.  **결과** 를 선택하고 결과가 **검토되지 않음** 으로 표시되는지 확인합니다.

     ![스크린샷](../Media/04c32a26-be67-48dd-bf3d-7b60e81e2fff.png)

### <a name="task-2-approve-or-deny-access"></a>작업 2: 액세스 승인 또는 거부


액세스를 승인하거나 거부할 때는 검토자에게 이 역할을 계속 사용하는지 여부만 전달합니다. 역할을 유지하려면 승인을, 또는 더 이상 액세스를 필요로 하지 않는 경우 거부를 선택합니다. 검토자가 결과를 적용할 때까지는 사용자의 상태가 바로 변경되지 않습니다. 액세스 검토를 찾아 완료하려면 다음 단계를 수행합니다.


1.  PIM 애플리케이션 **액세스 검토** 를 선택합니다. 

2.  **전역 관리자 검토** 를 선택합니다.

     ![스크린샷](../Media/3f5a8e6a-05a7-4cc0-96ea-d1a10d23c38f.png)

3.  검토를 만들지 않은 한, 검토에서 유일한 사용자로 나타납니다. Holly Dickson 옆의 체크박스를 선택하고 **보기** 를 클릭합니다.

     ![스크린샷](../Media/081d9886-8482-4d62-827c-68eb380c00a0.png)

5.  **Review Azure AD roles** (Azure AD 역할 검토)를 닫습니다.

### <a name="task-3-complete-an-access-review-for-azure-ad-directory-roles-in-pim"></a>작업 3: PIM에서 Azure AD 디렉터리 역할의 액세스 검토 완료


액세스 검토가 시작되면 권한 있는 역할 관리자가 권한이 있는 액세스를 검토할 수 있습니다. Azure AD PIM(Privileged Identity Management)이 사용자에게 해당 액세스를 검토하도록 요청하는 메일을 자동으로 전송합니다. 사용자가 메일을 받지 못한 경우 액세스 검토를 수행하는 방법에 대한 지침을 보낼 수 있습니다.

액세스 검토 기간이 끝나거나 모든 사용자가 자체 검토를 완료하고 나면 이 작업의 단계를 수행하여 검토를 관리하고 결과를 확인합니다.



1. **Azure portal** 로 이동하고 `Azure AD Privileged Identity Management`를 선택합니다.

1. **Azure AD 역할** 을 선택합니다.

2. **액세스 검토** 를 선택합니다.

3. 전역 관리자 검토를 선택합니다. 

4. 검토 완료에 사용 가능한 옵션 중 하나를 선택합니다.
     - **중지** - 모든 액세스 검토는 종료 날짜가 있지만, 중지 단추를 사용하여 일찍 완료할 수 있습니다. 만일 이 때까지 검토하지 않은 사용자가 있다면, 검토를 중지한 후에는 그들을 검토할 수 없습니다. 검토를 중단한 후에는 다시 시작할 수 없습니다.
     - **적용** - 종료 날짜가 되었거나 수동으로 중지하여 액세스 검토가 완료되면, 적용 단추가 검토 결과를 구현합니다. 사용자의 액세스가 검토 중에 거부되었다면, 이는 그들의 역할 할당을 제거할 단계입니다.
     - **삭제** - 더 이상 검토가 필요 없는 경우 검토를 삭제합니다. 삭제 단추는 Privileged Identity Management 서비스에서 검토를 제거합니다.


### <a name="task-4-configure-security-alerts-for-azure-ad-directory-roles-in-pim"></a>작업 4: PIM에서 Azure AD 디렉터리 역할용 보안 경고 구성


PIM의 일부 보안 경고를 환경 및 보안 목표에 맞게 사용자 지정할 수 있습니다. 보안 경고 설정을 열려면 다음이 단계를 따릅니다.



1.  `Azure AD Privileged Identity Management`를 엽니다.

1.  **Azure AD 역할** 을 클릭합니다.

1.  **경고**, **설정** 을 차례로 클릭합니다.

1.  경고 이름을 클릭하여 해당 경고에 대해 설정을 구성합니다.


# <a name="continue-to-exercise-5"></a>연습 5 계속 진행
