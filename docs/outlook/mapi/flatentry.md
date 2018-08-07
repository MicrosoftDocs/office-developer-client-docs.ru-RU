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
ms.openlocfilehash: 2f5f4d50b085c437d1caab5f70dcb741afe090bb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808446"
---
# <a name="flatentry"></a><span data-ttu-id="fe8b0-103">FLATENTRY</span><span class="sxs-lookup"><span data-stu-id="fe8b0-103">FLATENTRY</span></span>

  
  
<span data-ttu-id="fe8b0-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fe8b0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fe8b0-105">Кроме того в байтах, задающее размер структуры **ENTRYID** структуру [ENTRYID](entryid.md) .</span><span class="sxs-lookup"><span data-stu-id="fe8b0-105">An [ENTRYID](entryid.md) structure plus a byte count that specifies the size of the **ENTRYID** structure.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fe8b0-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="fe8b0-106">Header file:</span></span>  <br/> |<span data-ttu-id="fe8b0-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fe8b0-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="fe8b0-108">Связанные макросы:</span><span class="sxs-lookup"><span data-stu-id="fe8b0-108">Related macros:</span></span>  <br/> |<span data-ttu-id="fe8b0-109">[cbFLATENTRY](cbflatentry.md), [CbNewFLATENTRY](cbnewflatentry.md)</span><span class="sxs-lookup"><span data-stu-id="fe8b0-109">[cbFLATENTRY](cbflatentry.md), [CbNewFLATENTRY](cbnewflatentry.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE abEntry[MAPI_DIM];
} FLATENTRY, FAR *LPFLATENTRY;

```

## <a name="members"></a><span data-ttu-id="fe8b0-110">Members</span><span class="sxs-lookup"><span data-stu-id="fe8b0-110">Members</span></span>

 <span data-ttu-id="fe8b0-111">**cb**</span><span class="sxs-lookup"><span data-stu-id="fe8b0-111">**cb**</span></span>
  
> <span data-ttu-id="fe8b0-112">Число байт в элемент **abEntry** .</span><span class="sxs-lookup"><span data-stu-id="fe8b0-112">Count of bytes in the **abEntry** member.</span></span> 
    
 <span data-ttu-id="fe8b0-113">**abEntry**</span><span class="sxs-lookup"><span data-stu-id="fe8b0-113">**abEntry**</span></span>
  
> <span data-ttu-id="fe8b0-114">Идентификатор полная запись, которая включает в себя массив флаги и двоичных данных.</span><span class="sxs-lookup"><span data-stu-id="fe8b0-114">The complete entry identifier that includes the array of flags and binary data.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fe8b0-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="fe8b0-115">Remarks</span></span>

<span data-ttu-id="fe8b0-116">Структура **FLATENTRY** напоминает структуру [ENTRYID](entryid.md) .</span><span class="sxs-lookup"><span data-stu-id="fe8b0-116">A **FLATENTRY** structure resembles an [ENTRYID](entryid.md) structure.</span></span> <span data-ttu-id="fe8b0-117">Тем не менее существуют некоторые отличия:</span><span class="sxs-lookup"><span data-stu-id="fe8b0-117">However, there are some differences:</span></span> 
  
- <span data-ttu-id="fe8b0-118">Структура **FLATENTRY** сохраняет размер идентификатор записи; **Идентификатор записи** — нет.</span><span class="sxs-lookup"><span data-stu-id="fe8b0-118">A **FLATENTRY** structure stores the size of the entry identifier; **ENTRYID** does not.</span></span> 
    
- <span data-ttu-id="fe8b0-119">Структура **FLATENTRY** хранит данные флаг с другими идентификатор записи; **Идентификатор записи** сохраняет их отдельно.</span><span class="sxs-lookup"><span data-stu-id="fe8b0-119">A **FLATENTRY** structure stores the flag data together with the rest of the entry identifier; **ENTRYID** stores them separately.</span></span> 
    
- <span data-ttu-id="fe8b0-120">Структура **FLATENTRY** используется для хранения идентификатора записи в файле и передайте его в поток байтов, то время как структуру **ENTRYID** используется путем методов интерфейса [IMAPIProp](imapipropiunknown.md) и следующие методы **OpenEntry** : [IABLogon: : OpenEntry](iablogon-openentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md), [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), [IMAPISupport::OpenEntry](imapisupport-openentry.md), [IMsgStore::OpenEntry](imsgstore-openentry.md), [IMSLogon::OpenEntry](imslogon-openentry.md)</span><span class="sxs-lookup"><span data-stu-id="fe8b0-120">A **FLATENTRY** structure is used to store an entry identifier in a file or pass it in a stream of bytes whereas an **ENTRYID** structure is used by the [IMAPIProp](imapipropiunknown.md) interface methods and by the following **OpenEntry** methods: [IABLogon::OpenEntry](iablogon-openentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md), [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), [IMAPISupport::OpenEntry](imapisupport-openentry.md), [IMsgStore::OpenEntry](imsgstore-openentry.md), [IMSLogon::OpenEntry](imslogon-openentry.md)</span></span>
    
- <span data-ttu-id="fe8b0-121">Структура **FLATENTRY** используется для хранения идентификатора записи в файл или передайте его в виде потока в байтах.</span><span class="sxs-lookup"><span data-stu-id="fe8b0-121">A **FLATENTRY** structure is used to store an entry identifier in a file or pass it in a stream of bytes.</span></span> <span data-ttu-id="fe8b0-122">Структура **ENTRYID** используется для хранения идентификатора записи на диск.</span><span class="sxs-lookup"><span data-stu-id="fe8b0-122">An **ENTRYID** structure is used to store an entry identifier on disk.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="fe8b0-123">См. также</span><span class="sxs-lookup"><span data-stu-id="fe8b0-123">See also</span></span>



[<span data-ttu-id="fe8b0-124">ENTRYID</span><span class="sxs-lookup"><span data-stu-id="fe8b0-124">ENTRYID</span></span>](entryid.md)


[<span data-ttu-id="fe8b0-125">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="fe8b0-125">MAPI Structures</span></span>](mapi-structures.md)

