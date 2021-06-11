---
title: FLATENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FLATENTRY
api_type:
- COM
ms.assetid: 03e53e08-9113-4101-84c9-ccf6d43127f6
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e47f4e0d1ab9ab3ecfd53932b8ef26440134c603
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407244"
---
# <a name="flatentry"></a><span data-ttu-id="570e7-103">FLATENTRY</span><span class="sxs-lookup"><span data-stu-id="570e7-103">FLATENTRY</span></span>

  
  
<span data-ttu-id="570e7-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="570e7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="570e7-105">Структура [ENTRYID](entryid.md) плюс количество byte, которое указывает размер **структуры ENTRYID.**</span><span class="sxs-lookup"><span data-stu-id="570e7-105">An [ENTRYID](entryid.md) structure plus a byte count that specifies the size of the **ENTRYID** structure.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="570e7-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="570e7-106">Header file:</span></span>  <br/> |<span data-ttu-id="570e7-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="570e7-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="570e7-108">Связанные макрос:</span><span class="sxs-lookup"><span data-stu-id="570e7-108">Related macros:</span></span>  <br/> |<span data-ttu-id="570e7-109">[cbFLATENTRY,](cbflatentry.md) [CbNewFLATENTRY](cbnewflatentry.md)</span><span class="sxs-lookup"><span data-stu-id="570e7-109">[cbFLATENTRY](cbflatentry.md), [CbNewFLATENTRY](cbnewflatentry.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE abEntry[MAPI_DIM];
} FLATENTRY, FAR *LPFLATENTRY;

```

## <a name="members"></a><span data-ttu-id="570e7-110">"Участники"</span><span class="sxs-lookup"><span data-stu-id="570e7-110">Members</span></span>

 <span data-ttu-id="570e7-111">**cb**</span><span class="sxs-lookup"><span data-stu-id="570e7-111">**cb**</span></span>
  
> <span data-ttu-id="570e7-112">Количество bytes в **члене abEntry.**</span><span class="sxs-lookup"><span data-stu-id="570e7-112">Count of bytes in the **abEntry** member.</span></span> 
    
 <span data-ttu-id="570e7-113">**abEntry**</span><span class="sxs-lookup"><span data-stu-id="570e7-113">**abEntry**</span></span>
  
> <span data-ttu-id="570e7-114">Полный идентификатор записи, который включает массив флагов и двоичных данных.</span><span class="sxs-lookup"><span data-stu-id="570e7-114">The complete entry identifier that includes the array of flags and binary data.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="570e7-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="570e7-115">Remarks</span></span>

<span data-ttu-id="570e7-116">Структура **FLATENTRY** похожа на [структуру ENTRYID.](entryid.md)</span><span class="sxs-lookup"><span data-stu-id="570e7-116">A **FLATENTRY** structure resembles an [ENTRYID](entryid.md) structure.</span></span> <span data-ttu-id="570e7-117">Однако существуют некоторые различия:</span><span class="sxs-lookup"><span data-stu-id="570e7-117">However, there are some differences:</span></span> 
  
- <span data-ttu-id="570e7-118">Структура **FLATENTRY** сохраняет размер идентификатора записи; **ENTRYID** этого не делает.</span><span class="sxs-lookup"><span data-stu-id="570e7-118">A **FLATENTRY** structure stores the size of the entry identifier; **ENTRYID** does not.</span></span> 
    
- <span data-ttu-id="570e7-119">Структура **FLATENTRY** хранит данные флага вместе с остальным идентификатором записи; **ENTRYID** хранит их отдельно.</span><span class="sxs-lookup"><span data-stu-id="570e7-119">A **FLATENTRY** structure stores the flag data together with the rest of the entry identifier; **ENTRYID** stores them separately.</span></span> 
    
- <span data-ttu-id="570e7-120">Структура **FLATENTRY** используется для хранения идентификатора записи в файле или передачи его в потоке bytes, в то время как структура **ENTRYID** используется методами интерфейса [IMAPIProp](imapipropiunknown.md) и следующими методами **OpenEntry:** [IABLogon::OpenEntry](iablogon-openentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md), [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), [IMAPISupport::OpenEntry](imapisupport-openentry.md), [IMsgStore::OpenEntry](imsgstore-openentry.md), [IMSLogon::OpenEntry](imslogon-openentry.md)</span><span class="sxs-lookup"><span data-stu-id="570e7-120">A **FLATENTRY** structure is used to store an entry identifier in a file or pass it in a stream of bytes whereas an **ENTRYID** structure is used by the [IMAPIProp](imapipropiunknown.md) interface methods and by the following **OpenEntry** methods: [IABLogon::OpenEntry](iablogon-openentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md), [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), [IMAPISupport::OpenEntry](imapisupport-openentry.md), [IMsgStore::OpenEntry](imsgstore-openentry.md), [IMSLogon::OpenEntry](imslogon-openentry.md)</span></span>
    
- <span data-ttu-id="570e7-121">Структура **FLATENTRY** используется для хранения идентификатора записи в файле или передачи его в потоке bytes.</span><span class="sxs-lookup"><span data-stu-id="570e7-121">A **FLATENTRY** structure is used to store an entry identifier in a file or pass it in a stream of bytes.</span></span> <span data-ttu-id="570e7-122">Структура **ENTRYID** используется для хранения идентификатора записи на диске.</span><span class="sxs-lookup"><span data-stu-id="570e7-122">An **ENTRYID** structure is used to store an entry identifier on disk.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="570e7-123">См. также</span><span class="sxs-lookup"><span data-stu-id="570e7-123">See also</span></span>



[<span data-ttu-id="570e7-124">ENTRYID</span><span class="sxs-lookup"><span data-stu-id="570e7-124">ENTRYID</span></span>](entryid.md)


[<span data-ttu-id="570e7-125">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="570e7-125">MAPI Structures</span></span>](mapi-structures.md)

