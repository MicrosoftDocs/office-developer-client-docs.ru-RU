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
ms.openlocfilehash: 8f5f3bc454e18b1dbab434fc1b7cc094b0d6a360
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808283"
---
# <a name="bookmark"></a><span data-ttu-id="6a4f6-103">BOOKMARK</span><span class="sxs-lookup"><span data-stu-id="6a4f6-103">BOOKMARK</span></span>

  
  
<span data-ttu-id="6a4f6-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6a4f6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6a4f6-105">Определяет данные закладки запоминание позицию в таблице.</span><span class="sxs-lookup"><span data-stu-id="6a4f6-105">Defines bookmarks data for remembering a position in a table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6a4f6-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="6a4f6-106">Header file:</span></span>  <br/> |<span data-ttu-id="6a4f6-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6a4f6-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="6a4f6-108">Связанные методы:</span><span class="sxs-lookup"><span data-stu-id="6a4f6-108">Related methods:</span></span>  <br/> |<span data-ttu-id="6a4f6-109">[IMAPITable::CreateBookmark](imapitable-createbookmark.md) [IMAPITable::FreeBookmark](imapitable-freebookmark.md)</span><span class="sxs-lookup"><span data-stu-id="6a4f6-109">[IMAPITable::CreateBookmark](imapitable-createbookmark.md)[IMAPITable::FreeBookmark](imapitable-freebookmark.md)</span></span> <br/> |
   
```cpp
typedef ULONG_PTR BOOKMARK;
```

## <a name="remarks"></a><span data-ttu-id="6a4f6-110">Замечания</span><span class="sxs-lookup"><span data-stu-id="6a4f6-110">Remarks</span></span>

<span data-ttu-id="6a4f6-111">MAPI определяет три закладки, перечисленных следующим образом:</span><span class="sxs-lookup"><span data-stu-id="6a4f6-111">MAPI defines three bookmarks, listed as follows:</span></span>
  
<span data-ttu-id="6a4f6-112">BOOKMARK_BEGINNING</span><span class="sxs-lookup"><span data-stu-id="6a4f6-112">BOOKMARK_BEGINNING</span></span> 
  
> <span data-ttu-id="6a4f6-113">Запоминает позицию в таблице.</span><span class="sxs-lookup"><span data-stu-id="6a4f6-113">Remembers the starting position of the table.</span></span> 
    
<span data-ttu-id="6a4f6-114">BOOKMARK_CURRENT</span><span class="sxs-lookup"><span data-stu-id="6a4f6-114">BOOKMARK_CURRENT</span></span> 
  
> <span data-ttu-id="6a4f6-115">Запоминает сведения о текущей позиции в таблице.</span><span class="sxs-lookup"><span data-stu-id="6a4f6-115">Remembers the current position of the table.</span></span>
    
<span data-ttu-id="6a4f6-116">BOOKMARK_END</span><span class="sxs-lookup"><span data-stu-id="6a4f6-116">BOOKMARK_END</span></span> 
  
> <span data-ttu-id="6a4f6-117">Запоминает конечную позицию в таблице.</span><span class="sxs-lookup"><span data-stu-id="6a4f6-117">Remembers the ending position of the table.</span></span>
    
<span data-ttu-id="6a4f6-118">Клиенты могут создавать другие закладки запоминание другие положения в таблице.</span><span class="sxs-lookup"><span data-stu-id="6a4f6-118">Clients can create other bookmarks for remembering other table positions.</span></span> <span data-ttu-id="6a4f6-119">Закладки являются допустимыми только когда таблица открыта.</span><span class="sxs-lookup"><span data-stu-id="6a4f6-119">Bookmarks are valid only when the table is open.</span></span> <span data-ttu-id="6a4f6-120">Клиенты необходимо освободить все закладки, которые они созданы перед закрытием в связанной таблице.</span><span class="sxs-lookup"><span data-stu-id="6a4f6-120">Clients must free any bookmarks that they have created before closing the associated table.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6a4f6-121">См. также</span><span class="sxs-lookup"><span data-stu-id="6a4f6-121">See also</span></span>



[<span data-ttu-id="6a4f6-122">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="6a4f6-122">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md)
  
[<span data-ttu-id="6a4f6-123">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="6a4f6-123">IMAPITable::FindRow</span></span>](imapitable-findrow.md)
  
[<span data-ttu-id="6a4f6-124">IMAPITable::FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="6a4f6-124">IMAPITable::FreeBookmark</span></span>](imapitable-freebookmark.md)
  
[<span data-ttu-id="6a4f6-125">IMAPITable::SeekRow</span><span class="sxs-lookup"><span data-stu-id="6a4f6-125">IMAPITable::SeekRow</span></span>](imapitable-seekrow.md)


[<span data-ttu-id="6a4f6-126">Типы данных MAPI</span><span class="sxs-lookup"><span data-stu-id="6a4f6-126">MAPI Data Types</span></span>](mapi-data-types.md)

