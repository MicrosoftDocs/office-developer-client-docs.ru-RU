---
title: PROP_ACCT_USER_EMAIL_ADDR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fe447899-d37a-4775-a09d-13ba3a878008
description: Указывает адрес электронной почты для учетной записи.
ms.openlocfilehash: 115941fdf2fdec01da8d6bc1320ac6cdc0930ffa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436778"
---
# <a name="prop_acct_user_email_addr"></a><span data-ttu-id="e2f79-103">PROP_ACCT_USER_EMAIL_ADDR</span><span class="sxs-lookup"><span data-stu-id="e2f79-103">PROP_ACCT_USER_EMAIL_ADDR</span></span>

<span data-ttu-id="e2f79-104">Указывает адрес электронной почты для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="e2f79-104">Specifies the email address for the account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="e2f79-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="e2f79-105">Quick info</span></span>

<span data-ttu-id="e2f79-106">См. [iOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="e2f79-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e2f79-107">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="e2f79-107">Identifier:</span></span>  <br/> |<span data-ttu-id="e2f79-108">0x000C</span><span class="sxs-lookup"><span data-stu-id="e2f79-108">0x000C</span></span>  <br/> |
|<span data-ttu-id="e2f79-109">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="e2f79-109">Property type:</span></span>  <br/> |<span data-ttu-id="e2f79-110">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e2f79-110">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="e2f79-111">Тег свойства:</span><span class="sxs-lookup"><span data-stu-id="e2f79-111">Property tag:</span></span>  <br/> |<span data-ttu-id="e2f79-112">0x000C001F</span><span class="sxs-lookup"><span data-stu-id="e2f79-112">0x000C001F</span></span>  <br/> |
|<span data-ttu-id="e2f79-113">Доступ:</span><span class="sxs-lookup"><span data-stu-id="e2f79-113">Access:</span></span>  <br/> |<span data-ttu-id="e2f79-114">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="e2f79-114">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e2f79-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="e2f79-115">Remarks</span></span>

 <span data-ttu-id="e2f79-116">**PROP_ACCT_USER_EMAIL_ADDR** ожидается, что на каждой учетной записи не будет существовать.</span><span class="sxs-lookup"><span data-stu-id="e2f79-116">**PROP_ACCT_USER_EMAIL_ADDR** is not expected to exist on every account.</span></span> <span data-ttu-id="e2f79-117">Например, учетная запись Exchange может [](prop_mapi_identity_entryid.md) иметь PROP_MAPI_IDENTITY_ENTRYID, но не **PROP_ACCT_USER_EMAIL_ADDR,** в то время как для учетной записи SMTP/POP3 ситуация обратная.</span><span class="sxs-lookup"><span data-stu-id="e2f79-117">For example, an Exchange account could have [PROP_MAPI_IDENTITY_ENTRYID](prop_mapi_identity_entryid.md) but not **PROP_ACCT_USER_EMAIL_ADDR**, while for an SMTP/POP3 account, the situation is reversed.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e2f79-118">См. также</span><span class="sxs-lookup"><span data-stu-id="e2f79-118">See also</span></span>

- [<span data-ttu-id="e2f79-119">Сведения об API управления учетными записями</span><span class="sxs-lookup"><span data-stu-id="e2f79-119">About the Account Management API</span></span>](about-the-account-management-api.md)

