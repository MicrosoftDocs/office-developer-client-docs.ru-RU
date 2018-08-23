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
ms.openlocfilehash: cf84c7d94e67da0ce7453829042e7be0d4e313f1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585551"
---
# <a name="flatentry"></a><span data-ttu-id="b1c7a-103">FLATENTRY</span><span class="sxs-lookup"><span data-stu-id="b1c7a-103">FLATENTRY</span></span>

  
  
<span data-ttu-id="b1c7a-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b1c7a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b1c7a-105">Кроме того в байтах, задающее размер структуры **ENTRYID** структуру [ENTRYID](entryid.md) .</span><span class="sxs-lookup"><span data-stu-id="b1c7a-105">An [ENTRYID](entryid.md) structure plus a byte count that specifies the size of the **ENTRYID** structure.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b1c7a-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="b1c7a-106">Header file:</span></span>  <br/> |<span data-ttu-id="b1c7a-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b1c7a-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="b1c7a-108">Связанные макросы:</span><span class="sxs-lookup"><span data-stu-id="b1c7a-108">Related macros:</span></span>  <br/> |<span data-ttu-id="b1c7a-109">[cbFLATENTRY](cbflatentry.md), [CbNewFLATENTRY](cbnewflatentry.md)</span><span class="sxs-lookup"><span data-stu-id="b1c7a-109">[cbFLATENTRY](cbflatentry.md), [CbNewFLATENTRY](cbnewflatentry.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE abEntry[MAPI_DIM];
} FLATENTRY, FAR *LPFLATENTRY;

```

## <a name="members"></a><span data-ttu-id="b1c7a-110">Members</span><span class="sxs-lookup"><span data-stu-id="b1c7a-110">Members</span></span>

 <span data-ttu-id="b1c7a-111">**cb**</span><span class="sxs-lookup"><span data-stu-id="b1c7a-111">**cb**</span></span>
  
> <span data-ttu-id="b1c7a-112">Число байт в элемент **abEntry** .</span><span class="sxs-lookup"><span data-stu-id="b1c7a-112">Count of bytes in the **abEntry** member.</span></span> 
    
 <span data-ttu-id="b1c7a-113">**abEntry**</span><span class="sxs-lookup"><span data-stu-id="b1c7a-113">**abEntry**</span></span>
  
> <span data-ttu-id="b1c7a-114">Идентификатор полная запись, которая включает в себя массив флаги и двоичных данных.</span><span class="sxs-lookup"><span data-stu-id="b1c7a-114">The complete entry identifier that includes the array of flags and binary data.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b1c7a-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="b1c7a-115">Remarks</span></span>

<span data-ttu-id="b1c7a-116">Структура **FLATENTRY** напоминает структуру [ENTRYID](entryid.md) .</span><span class="sxs-lookup"><span data-stu-id="b1c7a-116">A **FLATENTRY** structure resembles an [ENTRYID](entryid.md) structure.</span></span> <span data-ttu-id="b1c7a-117">Тем не менее существуют некоторые отличия:</span><span class="sxs-lookup"><span data-stu-id="b1c7a-117">However, there are some differences:</span></span> 
  
- <span data-ttu-id="b1c7a-118">Структура **FLATENTRY** сохраняет размер идентификатор записи; **Идентификатор записи** — нет.</span><span class="sxs-lookup"><span data-stu-id="b1c7a-118">A **FLATENTRY** structure stores the size of the entry identifier; **ENTRYID** does not.</span></span> 
    
- <span data-ttu-id="b1c7a-119">Структура **FLATENTRY** хранит данные флаг с другими идентификатор записи; **Идентификатор записи** сохраняет их отдельно.</span><span class="sxs-lookup"><span data-stu-id="b1c7a-119">A **FLATENTRY** structure stores the flag data together with the rest of the entry identifier; **ENTRYID** stores them separately.</span></span> 
    
- <span data-ttu-id="b1c7a-120">Структура **FLATENTRY** используется для хранения идентификатора записи в файле и передайте его в поток байтов, то время как структуру **ENTRYID** используется путем методов интерфейса [IMAPIProp](imapipropiunknown.md) и следующие методы **OpenEntry** : [IABLogon: : OpenEntry](iablogon-openentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md), [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), [IMAPISupport::OpenEntry](imapisupport-openentry.md), [IMsgStore::OpenEntry](imsgstore-openentry.md), [IMSLogon::OpenEntry](imslogon-openentry.md)</span><span class="sxs-lookup"><span data-stu-id="b1c7a-120">A **FLATENTRY** structure is used to store an entry identifier in a file or pass it in a stream of bytes whereas an **ENTRYID** structure is used by the [IMAPIProp](imapipropiunknown.md) interface methods and by the following **OpenEntry** methods: [IABLogon::OpenEntry](iablogon-openentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md), [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), [IMAPISupport::OpenEntry](imapisupport-openentry.md), [IMsgStore::OpenEntry](imsgstore-openentry.md), [IMSLogon::OpenEntry](imslogon-openentry.md)</span></span>
    
- <span data-ttu-id="b1c7a-121">Структура **FLATENTRY** используется для хранения идентификатора записи в файл или передайте его в виде потока в байтах.</span><span class="sxs-lookup"><span data-stu-id="b1c7a-121">A **FLATENTRY** structure is used to store an entry identifier in a file or pass it in a stream of bytes.</span></span> <span data-ttu-id="b1c7a-122">Структура **ENTRYID** используется для хранения идентификатора записи на диск.</span><span class="sxs-lookup"><span data-stu-id="b1c7a-122">An **ENTRYID** structure is used to store an entry identifier on disk.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="b1c7a-123">См. также</span><span class="sxs-lookup"><span data-stu-id="b1c7a-123">See also</span></span>



[<span data-ttu-id="b1c7a-124">ENTRYID</span><span class="sxs-lookup"><span data-stu-id="b1c7a-124">ENTRYID</span></span>](entryid.md)


[<span data-ttu-id="b1c7a-125">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="b1c7a-125">MAPI Structures</span></span>](mapi-structures.md)

