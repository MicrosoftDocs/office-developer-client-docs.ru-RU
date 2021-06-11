---
title: BOOKMARK
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.BOOKMARK
api_type:
- COM
ms.assetid: 678bdc52-3404-48b2-9154-64ce2a941555
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 069cb41ceac70a2eaaa08440e43745605890f071
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418136"
---
# <a name="bookmark"></a><span data-ttu-id="d5fa9-103">BOOKMARK</span><span class="sxs-lookup"><span data-stu-id="d5fa9-103">BOOKMARK</span></span>

  
  
<span data-ttu-id="d5fa9-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d5fa9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d5fa9-105">Определяет данные закладки для запоминания позиции в таблице.</span><span class="sxs-lookup"><span data-stu-id="d5fa9-105">Defines bookmarks data for remembering a position in a table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d5fa9-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="d5fa9-106">Header file:</span></span>  <br/> |<span data-ttu-id="d5fa9-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d5fa9-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="d5fa9-108">Связанные методы:</span><span class="sxs-lookup"><span data-stu-id="d5fa9-108">Related methods:</span></span>  <br/> |<span data-ttu-id="d5fa9-109">[IMAPITable::CreateBookmark](imapitable-createbookmark.md)[IMAPITable::FreeBookmark](imapitable-freebookmark.md)</span><span class="sxs-lookup"><span data-stu-id="d5fa9-109">[IMAPITable::CreateBookmark](imapitable-createbookmark.md)[IMAPITable::FreeBookmark](imapitable-freebookmark.md)</span></span> <br/> |
   
```cpp
typedef ULONG_PTR BOOKMARK;
```

## <a name="remarks"></a><span data-ttu-id="d5fa9-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="d5fa9-110">Remarks</span></span>

<span data-ttu-id="d5fa9-111">MAPI определяет три закладки, перечисленные следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d5fa9-111">MAPI defines three bookmarks, listed as follows:</span></span>
  
<span data-ttu-id="d5fa9-112">BOOKMARK_BEGINNING</span><span class="sxs-lookup"><span data-stu-id="d5fa9-112">BOOKMARK_BEGINNING</span></span> 
  
> <span data-ttu-id="d5fa9-113">Запоминает исходное положение таблицы.</span><span class="sxs-lookup"><span data-stu-id="d5fa9-113">Remembers the starting position of the table.</span></span> 
    
<span data-ttu-id="d5fa9-114">BOOKMARK_CURRENT</span><span class="sxs-lookup"><span data-stu-id="d5fa9-114">BOOKMARK_CURRENT</span></span> 
  
> <span data-ttu-id="d5fa9-115">Запоминает текущее положение таблицы.</span><span class="sxs-lookup"><span data-stu-id="d5fa9-115">Remembers the current position of the table.</span></span>
    
<span data-ttu-id="d5fa9-116">BOOKMARK_END</span><span class="sxs-lookup"><span data-stu-id="d5fa9-116">BOOKMARK_END</span></span> 
  
> <span data-ttu-id="d5fa9-117">Запоминает конечную позицию таблицы.</span><span class="sxs-lookup"><span data-stu-id="d5fa9-117">Remembers the ending position of the table.</span></span>
    
<span data-ttu-id="d5fa9-118">Клиенты могут создавать другие закладки для запоминания других позиций таблицы.</span><span class="sxs-lookup"><span data-stu-id="d5fa9-118">Clients can create other bookmarks for remembering other table positions.</span></span> <span data-ttu-id="d5fa9-119">Закладки действительны только в том случае, если таблица открыта.</span><span class="sxs-lookup"><span data-stu-id="d5fa9-119">Bookmarks are valid only when the table is open.</span></span> <span data-ttu-id="d5fa9-120">Клиенты должны освободить все закладки, созданные ими, перед закрытием связанной таблицы.</span><span class="sxs-lookup"><span data-stu-id="d5fa9-120">Clients must free any bookmarks that they have created before closing the associated table.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d5fa9-121">См. также</span><span class="sxs-lookup"><span data-stu-id="d5fa9-121">See also</span></span>



[<span data-ttu-id="d5fa9-122">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="d5fa9-122">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md)
  
[<span data-ttu-id="d5fa9-123">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="d5fa9-123">IMAPITable::FindRow</span></span>](imapitable-findrow.md)
  
[<span data-ttu-id="d5fa9-124">IMAPITable::FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="d5fa9-124">IMAPITable::FreeBookmark</span></span>](imapitable-freebookmark.md)
  
[<span data-ttu-id="d5fa9-125">IMAPITable::SeekRow</span><span class="sxs-lookup"><span data-stu-id="d5fa9-125">IMAPITable::SeekRow</span></span>](imapitable-seekrow.md)


[<span data-ttu-id="d5fa9-126">Типы данных MAPI</span><span class="sxs-lookup"><span data-stu-id="d5fa9-126">MAPI Data Types</span></span>](mapi-data-types.md)

