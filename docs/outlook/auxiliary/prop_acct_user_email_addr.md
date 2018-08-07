---
title: PROP_ACCT_USER_EMAIL_ADDR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fe447899-d37a-4775-a09d-13ba3a878008
description: Указывает адрес электронной почты для учетной записи.
ms.openlocfilehash: 7d0bbba2dcb104326c360da6a10f3e19d1740e46
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807948"
---
# <a name="propacctuseremailaddr"></a><span data-ttu-id="b4bea-103">PROP_ACCT_USER_EMAIL_ADDR</span><span class="sxs-lookup"><span data-stu-id="b4bea-103">PROP_ACCT_USER_EMAIL_ADDR</span></span>

<span data-ttu-id="b4bea-104">Указывает адрес электронной почты для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="b4bea-104">Specifies the email address for the account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="b4bea-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="b4bea-105">Quick info</span></span>

<span data-ttu-id="b4bea-106">В разделе [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="b4bea-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b4bea-107">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="b4bea-107">Identifier:</span></span>  <br/> |<span data-ttu-id="b4bea-108">0x000C</span><span class="sxs-lookup"><span data-stu-id="b4bea-108">0x000C</span></span>  <br/> |
|<span data-ttu-id="b4bea-109">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="b4bea-109">Property type:</span></span>  <br/> |<span data-ttu-id="b4bea-110">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b4bea-110">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="b4bea-111">Свойство tag:</span><span class="sxs-lookup"><span data-stu-id="b4bea-111">Property tag:</span></span>  <br/> |<span data-ttu-id="b4bea-112">0x000C001F</span><span class="sxs-lookup"><span data-stu-id="b4bea-112">0x000C001F</span></span>  <br/> |
|<span data-ttu-id="b4bea-113">Access:</span><span class="sxs-lookup"><span data-stu-id="b4bea-113">Access:</span></span>  <br/> |<span data-ttu-id="b4bea-114">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b4bea-114">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b4bea-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="b4bea-115">Remarks</span></span>

 <span data-ttu-id="b4bea-116">**PROP_ACCT_USER_EMAIL_ADDR** не должен существовать в каждой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="b4bea-116">**PROP_ACCT_USER_EMAIL_ADDR** is not expected to exist on every account.</span></span> <span data-ttu-id="b4bea-117">Например, учетную запись Exchange может быть [PROP_MAPI_IDENTITY_ENTRYID](prop_mapi_identity_entryid.md) , но не **PROP_ACCT_USER_EMAIL_ADDR**, то время как для учетной записи SMTP/POP3, ситуации изменен на обратный.</span><span class="sxs-lookup"><span data-stu-id="b4bea-117">For example, an Exchange account could have [PROP_MAPI_IDENTITY_ENTRYID](prop_mapi_identity_entryid.md) but not **PROP_ACCT_USER_EMAIL_ADDR**, while for an SMTP/POP3 account, the situation is reversed.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b4bea-118">См. также</span><span class="sxs-lookup"><span data-stu-id="b4bea-118">See also</span></span>

- [<span data-ttu-id="b4bea-119">About the Account Management API</span><span class="sxs-lookup"><span data-stu-id="b4bea-119">About the Account Management API</span></span>](about-the-account-management-api.md)

