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
# <a name="flatentry"></a><span data-ttu-id="7d80f-103">FLATENTRY</span><span class="sxs-lookup"><span data-stu-id="7d80f-103">FLATENTRY</span></span>

  
  
<span data-ttu-id="7d80f-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7d80f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7d80f-105">Структура [EntryID](entryid.md) и число байтов, определяющее размер структуры **EntryID** .</span><span class="sxs-lookup"><span data-stu-id="7d80f-105">An [ENTRYID](entryid.md) structure plus a byte count that specifies the size of the **ENTRYID** structure.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7d80f-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="7d80f-106">Header file:</span></span>  <br/> |<span data-ttu-id="7d80f-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="7d80f-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="7d80f-108">Связанные макросы:</span><span class="sxs-lookup"><span data-stu-id="7d80f-108">Related macros:</span></span>  <br/> |<span data-ttu-id="7d80f-109">[кбфлатентри](cbflatentry.md), [кбневфлатентри](cbnewflatentry.md)</span><span class="sxs-lookup"><span data-stu-id="7d80f-109">[cbFLATENTRY](cbflatentry.md), [CbNewFLATENTRY](cbnewflatentry.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE abEntry[MAPI_DIM];
} FLATENTRY, FAR *LPFLATENTRY;

```

## <a name="members"></a><span data-ttu-id="7d80f-110">"Участники"</span><span class="sxs-lookup"><span data-stu-id="7d80f-110">Members</span></span>

 <span data-ttu-id="7d80f-111">**cb**</span><span class="sxs-lookup"><span data-stu-id="7d80f-111">**cb**</span></span>
  
> <span data-ttu-id="7d80f-112">Количество байтов в элементе **абентри** .</span><span class="sxs-lookup"><span data-stu-id="7d80f-112">Count of bytes in the **abEntry** member.</span></span> 
    
 <span data-ttu-id="7d80f-113">**абентри**</span><span class="sxs-lookup"><span data-stu-id="7d80f-113">**abEntry**</span></span>
  
> <span data-ttu-id="7d80f-114">Полный идентификатор записи, включающий массив флагов и двоичных данных.</span><span class="sxs-lookup"><span data-stu-id="7d80f-114">The complete entry identifier that includes the array of flags and binary data.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7d80f-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="7d80f-115">Remarks</span></span>

<span data-ttu-id="7d80f-116">Структура **флатентри** похожа на структуру [EntryID](entryid.md) .</span><span class="sxs-lookup"><span data-stu-id="7d80f-116">A **FLATENTRY** structure resembles an [ENTRYID](entryid.md) structure.</span></span> <span data-ttu-id="7d80f-117">Однако существуют некоторые отличия.</span><span class="sxs-lookup"><span data-stu-id="7d80f-117">However, there are some differences:</span></span> 
  
- <span data-ttu-id="7d80f-118">В структуре **флатентри** хранится размер идентификатора записи; Идентификатор **EntryID** — нет.</span><span class="sxs-lookup"><span data-stu-id="7d80f-118">A **FLATENTRY** structure stores the size of the entry identifier; **ENTRYID** does not.</span></span> 
    
- <span data-ttu-id="7d80f-119">Структура **флатентри** сохраняет данные флага вместе с остальной частью идентификатора записи; **EntryID** хранит их по отдельности.</span><span class="sxs-lookup"><span data-stu-id="7d80f-119">A **FLATENTRY** structure stores the flag data together with the rest of the entry identifier; **ENTRYID** stores them separately.</span></span> 
    
- <span data-ttu-id="7d80f-120">Структура **флатентри** используется для хранения идентификатора записи в файле или его передачи в потоке байтов, в то время как структура **EntryID** используется методами интерфейса [IMAPIProp](imapipropiunknown.md) , а также следующими методами **OpenEntry** : [иаблогон:: OpenEntry](iablogon-openentry.md), [IAddrBook:: OpenEntry](iaddrbook-openentry.md), [IMAPIContainer:: OpenEntry](imapicontainer-openentry.md), [IMAPISession:: OpenEntry](imapisession-openentry.md), [имаписуппорт:: OpenEntry](imapisupport-openentry.md), [IMsgStore:: OpenEntry](imsgstore-openentry.md), имслогон:: [OpenEntry](imslogon-openentry.md)</span><span class="sxs-lookup"><span data-stu-id="7d80f-120">A **FLATENTRY** structure is used to store an entry identifier in a file or pass it in a stream of bytes whereas an **ENTRYID** structure is used by the [IMAPIProp](imapipropiunknown.md) interface methods and by the following **OpenEntry** methods: [IABLogon::OpenEntry](iablogon-openentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md), [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), [IMAPISupport::OpenEntry](imapisupport-openentry.md), [IMsgStore::OpenEntry](imsgstore-openentry.md), [IMSLogon::OpenEntry](imslogon-openentry.md)</span></span>
    
- <span data-ttu-id="7d80f-121">Структура **флатентри** используется для хранения идентификатора записи в файле или его передачи в потоке байтов.</span><span class="sxs-lookup"><span data-stu-id="7d80f-121">A **FLATENTRY** structure is used to store an entry identifier in a file or pass it in a stream of bytes.</span></span> <span data-ttu-id="7d80f-122">Структура **EntryID** используется для хранения идентификатора записи на диске.</span><span class="sxs-lookup"><span data-stu-id="7d80f-122">An **ENTRYID** structure is used to store an entry identifier on disk.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="7d80f-123">См. также</span><span class="sxs-lookup"><span data-stu-id="7d80f-123">See also</span></span>



[<span data-ttu-id="7d80f-124">ENTRYID</span><span class="sxs-lookup"><span data-stu-id="7d80f-124">ENTRYID</span></span>](entryid.md)


[<span data-ttu-id="7d80f-125">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="7d80f-125">MAPI Structures</span></span>](mapi-structures.md)

