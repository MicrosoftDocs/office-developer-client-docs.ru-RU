---
title: PROP_MAPI_IDENTITY_ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c64db8ea-d6ad-4fb9-97aa-958e5a0daf8f
description: Получает или задает идентификатор записи адресной книги для учетной записи.
ms.openlocfilehash: 2352f64b46e9884e95b7bf1f3693321f7cd224ca
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400350"
---
# <a name="propmapiidentityentryid"></a><span data-ttu-id="8619e-103">PROP_MAPI_IDENTITY_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="8619e-103">PROP_MAPI_IDENTITY_ENTRYID</span></span>

<span data-ttu-id="8619e-104">Получает или задает идентификатор записи адресной книги для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="8619e-104">Retrieves or sets the address book entry ID for the account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="8619e-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="8619e-105">Quick info</span></span>

<span data-ttu-id="8619e-106">В разделе [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="8619e-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8619e-107">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="8619e-107">Identifier:</span></span>  <br/> |<span data-ttu-id="8619e-108">0x2002</span><span class="sxs-lookup"><span data-stu-id="8619e-108">0x2002</span></span>  <br/> |
|<span data-ttu-id="8619e-109">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="8619e-109">Property type:</span></span>  <br/> |<span data-ttu-id="8619e-110">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="8619e-110">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="8619e-111">Свойство tag:</span><span class="sxs-lookup"><span data-stu-id="8619e-111">Property tag:</span></span>  <br/> |<span data-ttu-id="8619e-112">0x20020102</span><span class="sxs-lookup"><span data-stu-id="8619e-112">0x20020102</span></span>  <br/> |
|<span data-ttu-id="8619e-113">Access:</span><span class="sxs-lookup"><span data-stu-id="8619e-113">Access:</span></span>  <br/> |<span data-ttu-id="8619e-114">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8619e-114">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8619e-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="8619e-115">Remarks</span></span>

 <span data-ttu-id="8619e-116">**Свойства\_MAPI\_IDENTITY\_ENTRYID** не должен существовать в каждой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="8619e-116">**PROP\_MAPI\_IDENTITY\_ENTRYID** is not expected to exist on every account.</span></span> <span data-ttu-id="8619e-117">К примеру, могут иметь учетную запись Exchange **Свойства\_MAPI\_УДОСТОВЕРЕНИЯ\_ENTRYID** задать и не [Свойства\_ACCT_USER_EMAIL_ADDR](prop_acct_user_email_addr.md), а для учетной записи SMTP/POP3 ситуации изменен на обратный.</span><span class="sxs-lookup"><span data-stu-id="8619e-117">For example, an Exchange account could have **PROP\_MAPI\_IDENTITY\_ENTRYID** set and not [PROP\_ACCT_USER_EMAIL_ADDR](prop_acct_user_email_addr.md), while for an SMTP/POP3 account the situation is reversed.</span></span> <span data-ttu-id="8619e-118">**СВОЙСТВА\_MAPI_IDENTITY_ENTRYID** возвращает идентификатор записи, похожие на значение, возвращаемое _lppEntryID_ в [IMAPISession::QueryIdentity](https://msdn.microsoft.com/library/a2cdda90-5457-49a7-b98c-7273ffe5cbbc%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="8619e-118">**PROP\_MAPI_IDENTITY_ENTRYID** returns an entry ID that is similar to the value returned by  _lppEntryID_ in [IMAPISession::QueryIdentity](https://msdn.microsoft.com/library/a2cdda90-5457-49a7-b98c-7273ffe5cbbc%28Office.15%29.aspx).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8619e-119">См. также</span><span class="sxs-lookup"><span data-stu-id="8619e-119">See also</span></span>

- [<span data-ttu-id="8619e-120">About the Account Management API</span><span class="sxs-lookup"><span data-stu-id="8619e-120">About the Account Management API</span></span>](about-the-account-management-api.md)

