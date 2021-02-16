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
# <a name="flatentry"></a><span data-ttu-id="00d26-103">FLATENTRY</span><span class="sxs-lookup"><span data-stu-id="00d26-103">FLATENTRY</span></span>

  
  
<span data-ttu-id="00d26-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="00d26-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="00d26-105">Структура [ENTRYID](entryid.md) и количество byte, которое определяет размер **структуры ENTRYID.**</span><span class="sxs-lookup"><span data-stu-id="00d26-105">An [ENTRYID](entryid.md) structure plus a byte count that specifies the size of the **ENTRYID** structure.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="00d26-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="00d26-106">Header file:</span></span>  <br/> |<span data-ttu-id="00d26-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="00d26-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="00d26-108">Связанные макросы:</span><span class="sxs-lookup"><span data-stu-id="00d26-108">Related macros:</span></span>  <br/> |<span data-ttu-id="00d26-109">[cbFLATENTRY](cbflatentry.md), [CbNewFLATENTRY](cbnewflatentry.md)</span><span class="sxs-lookup"><span data-stu-id="00d26-109">[cbFLATENTRY](cbflatentry.md), [CbNewFLATENTRY](cbnewflatentry.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE abEntry[MAPI_DIM];
} FLATENTRY, FAR *LPFLATENTRY;

```

## <a name="members"></a><span data-ttu-id="00d26-110">"Участники"</span><span class="sxs-lookup"><span data-stu-id="00d26-110">Members</span></span>

 <span data-ttu-id="00d26-111">**cb**</span><span class="sxs-lookup"><span data-stu-id="00d26-111">**cb**</span></span>
  
> <span data-ttu-id="00d26-112">Количествобайтов в **члене abEntry.**</span><span class="sxs-lookup"><span data-stu-id="00d26-112">Count of bytes in the **abEntry** member.</span></span> 
    
 <span data-ttu-id="00d26-113">**abEntry**</span><span class="sxs-lookup"><span data-stu-id="00d26-113">**abEntry**</span></span>
  
> <span data-ttu-id="00d26-114">Полный идентификатор записи, который включает массив флагов и двоичных данных.</span><span class="sxs-lookup"><span data-stu-id="00d26-114">The complete entry identifier that includes the array of flags and binary data.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="00d26-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="00d26-115">Remarks</span></span>

<span data-ttu-id="00d26-116">Структура **FLATENTRY** похожа на [структуру ENTRYID.](entryid.md)</span><span class="sxs-lookup"><span data-stu-id="00d26-116">A **FLATENTRY** structure resembles an [ENTRYID](entryid.md) structure.</span></span> <span data-ttu-id="00d26-117">Однако существуют некоторые различия:</span><span class="sxs-lookup"><span data-stu-id="00d26-117">However, there are some differences:</span></span> 
  
- <span data-ttu-id="00d26-118">В **структуре FLATENTRY** хранится размер идентификатора записи; **ENTRYID** этого не делает.</span><span class="sxs-lookup"><span data-stu-id="00d26-118">A **FLATENTRY** structure stores the size of the entry identifier; **ENTRYID** does not.</span></span> 
    
- <span data-ttu-id="00d26-119">Структура **FLATENTRY** сохраняет данные флага вместе с остальным идентификатором записи; **ENTRYID** хранит их отдельно.</span><span class="sxs-lookup"><span data-stu-id="00d26-119">A **FLATENTRY** structure stores the flag data together with the rest of the entry identifier; **ENTRYID** stores them separately.</span></span> 
    
- <span data-ttu-id="00d26-120">Структура **FLATENTRY** используется для хранения идентификатора записи в файле или передачи его в потоке в битах, тогда как структура **ENTRYID** используется методами интерфейса [IMAPIProp](imapipropiunknown.md) и следующими методами **OpenEntry:** [IABLogon::OpenEntry](iablogon-openentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md), [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), [IMAPISupport::OpenEntry](imapisupport-openentry.md), [IMsgStore::OpenEntry](imsgstore-openentry.md), [IMSLogon::OpenEntry](imslogon-openentry.md)</span><span class="sxs-lookup"><span data-stu-id="00d26-120">A **FLATENTRY** structure is used to store an entry identifier in a file or pass it in a stream of bytes whereas an **ENTRYID** structure is used by the [IMAPIProp](imapipropiunknown.md) interface methods and by the following **OpenEntry** methods: [IABLogon::OpenEntry](iablogon-openentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md), [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), [IMAPISupport::OpenEntry](imapisupport-openentry.md), [IMsgStore::OpenEntry](imsgstore-openentry.md), [IMSLogon::OpenEntry](imslogon-openentry.md)</span></span>
    
- <span data-ttu-id="00d26-121">Структура **FLATENTRY** используется для хранения идентификатора записи в файле или передачи его в потоке данных.</span><span class="sxs-lookup"><span data-stu-id="00d26-121">A **FLATENTRY** structure is used to store an entry identifier in a file or pass it in a stream of bytes.</span></span> <span data-ttu-id="00d26-122">Структура **ENTRYID** используется для хранения идентификатора записи на диске.</span><span class="sxs-lookup"><span data-stu-id="00d26-122">An **ENTRYID** structure is used to store an entry identifier on disk.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="00d26-123">См. также</span><span class="sxs-lookup"><span data-stu-id="00d26-123">See also</span></span>



[<span data-ttu-id="00d26-124">ENTRYID</span><span class="sxs-lookup"><span data-stu-id="00d26-124">ENTRYID</span></span>](entryid.md)


[<span data-ttu-id="00d26-125">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="00d26-125">MAPI Structures</span></span>](mapi-structures.md)

