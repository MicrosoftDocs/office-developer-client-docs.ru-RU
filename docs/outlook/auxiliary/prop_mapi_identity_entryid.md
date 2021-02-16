---
title: PROP_MAPI_IDENTITY_ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c64db8ea-d6ad-4fb9-97aa-958e5a0daf8f
description: Извлекает или задает ИД записи адресной книги для учетной записи.
ms.openlocfilehash: 2352f64b46e9884e95b7bf1f3693321f7cd224ca
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326434"
---
# <a name="prop_mapi_identity_entryid"></a><span data-ttu-id="de90b-103">PROP_MAPI_IDENTITY_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="de90b-103">PROP_MAPI_IDENTITY_ENTRYID</span></span>

<span data-ttu-id="de90b-104">Извлекает или задает ИД записи адресной книги для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="de90b-104">Retrieves or sets the address book entry ID for the account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="de90b-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="de90b-105">Quick info</span></span>

<span data-ttu-id="de90b-106">См. [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="de90b-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="de90b-107">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="de90b-107">Identifier:</span></span>  <br/> |<span data-ttu-id="de90b-108">0x2002</span><span class="sxs-lookup"><span data-stu-id="de90b-108">0x2002</span></span>  <br/> |
|<span data-ttu-id="de90b-109">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="de90b-109">Property type:</span></span>  <br/> |<span data-ttu-id="de90b-110">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="de90b-110">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="de90b-111">Тег свойства:</span><span class="sxs-lookup"><span data-stu-id="de90b-111">Property tag:</span></span>  <br/> |<span data-ttu-id="de90b-112">0x20020102</span><span class="sxs-lookup"><span data-stu-id="de90b-112">0x20020102</span></span>  <br/> |
|<span data-ttu-id="de90b-113">Access:</span><span class="sxs-lookup"><span data-stu-id="de90b-113">Access:</span></span>  <br/> |<span data-ttu-id="de90b-114">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="de90b-114">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="de90b-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="de90b-115">Remarks</span></span>

 <span data-ttu-id="de90b-116">**PROP \_ ИДЕНТИФИКАТОР MAPI \_ IDENTITY \_ ENTRYID** не должен существовать в каждой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="de90b-116">**PROP\_MAPI\_IDENTITY\_ENTRYID** is not expected to exist on every account.</span></span> <span data-ttu-id="de90b-117">Например, у учетной записи Exchange может быть задан ИДЕНТИФИКАТОР **\_ PROP MAPI \_ \_ ENTRYID,** а не [PROP \_ ACCT_USER_EMAIL_ADDR](prop_acct_user_email_addr.md), тогда как для учетной записи SMTP/POP3 ситуация обратная.</span><span class="sxs-lookup"><span data-stu-id="de90b-117">For example, an Exchange account could have **PROP\_MAPI\_IDENTITY\_ENTRYID** set and not [PROP\_ACCT_USER_EMAIL_ADDR](prop_acct_user_email_addr.md), while for an SMTP/POP3 account the situation is reversed.</span></span> <span data-ttu-id="de90b-118">**PROP \_ MAPI_IDENTITY_ENTRYID** возвращает ИД записи, аналогичный значению, возвращаемого _lppEntryID_ в [IMAPISession::QueryIdentity.](https://msdn.microsoft.com/library/a2cdda90-5457-49a7-b98c-7273ffe5cbbc%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="de90b-118">**PROP\_MAPI_IDENTITY_ENTRYID** returns an entry ID that is similar to the value returned by  _lppEntryID_ in [IMAPISession::QueryIdentity](https://msdn.microsoft.com/library/a2cdda90-5457-49a7-b98c-7273ffe5cbbc%28Office.15%29.aspx).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="de90b-119">См. также</span><span class="sxs-lookup"><span data-stu-id="de90b-119">See also</span></span>

- [<span data-ttu-id="de90b-120">Сведения об API управления учетными записями</span><span class="sxs-lookup"><span data-stu-id="de90b-120">About the Account Management API</span></span>](about-the-account-management-api.md)

