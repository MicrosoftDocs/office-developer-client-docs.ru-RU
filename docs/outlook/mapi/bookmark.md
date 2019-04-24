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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318041"
---
# <a name="bookmark"></a><span data-ttu-id="c04e7-103">BOOKMARK</span><span class="sxs-lookup"><span data-stu-id="c04e7-103">BOOKMARK</span></span>

  
  
<span data-ttu-id="c04e7-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c04e7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c04e7-105">Определяет данные закладок для запоминания положения в таблице.</span><span class="sxs-lookup"><span data-stu-id="c04e7-105">Defines bookmarks data for remembering a position in a table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c04e7-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="c04e7-106">Header file:</span></span>  <br/> |<span data-ttu-id="c04e7-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="c04e7-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="c04e7-108">Связанные методы:</span><span class="sxs-lookup"><span data-stu-id="c04e7-108">Related methods:</span></span>  <br/> |<span data-ttu-id="c04e7-109">[IMAPITable:: креатебукмарк](imapitable-createbookmark.md) [IMAPITable:: фрибукмарк](imapitable-freebookmark.md)</span><span class="sxs-lookup"><span data-stu-id="c04e7-109">[IMAPITable::CreateBookmark](imapitable-createbookmark.md)[IMAPITable::FreeBookmark](imapitable-freebookmark.md)</span></span> <br/> |
   
```cpp
typedef ULONG_PTR BOOKMARK;
```

## <a name="remarks"></a><span data-ttu-id="c04e7-110">Замечания</span><span class="sxs-lookup"><span data-stu-id="c04e7-110">Remarks</span></span>

<span data-ttu-id="c04e7-111">MAPI определяет три закладки, перечисленные ниже.</span><span class="sxs-lookup"><span data-stu-id="c04e7-111">MAPI defines three bookmarks, listed as follows:</span></span>
  
<span data-ttu-id="c04e7-112">БУКМАРК_БЕГИННИНГ</span><span class="sxs-lookup"><span data-stu-id="c04e7-112">BOOKMARK_BEGINNING</span></span> 
  
> <span data-ttu-id="c04e7-113">Запоминает начальную позицию таблицы.</span><span class="sxs-lookup"><span data-stu-id="c04e7-113">Remembers the starting position of the table.</span></span> 
    
<span data-ttu-id="c04e7-114">БУКМАРК_КУРРЕНТ</span><span class="sxs-lookup"><span data-stu-id="c04e7-114">BOOKMARK_CURRENT</span></span> 
  
> <span data-ttu-id="c04e7-115">Запоминает текущую позицию таблицы.</span><span class="sxs-lookup"><span data-stu-id="c04e7-115">Remembers the current position of the table.</span></span>
    
<span data-ttu-id="c04e7-116">БУКМАРК_ЕНД</span><span class="sxs-lookup"><span data-stu-id="c04e7-116">BOOKMARK_END</span></span> 
  
> <span data-ttu-id="c04e7-117">Запоминает конечное положение таблицы.</span><span class="sxs-lookup"><span data-stu-id="c04e7-117">Remembers the ending position of the table.</span></span>
    
<span data-ttu-id="c04e7-118">Клиенты могут создавать другие закладки для запоминания других положений таблиц.</span><span class="sxs-lookup"><span data-stu-id="c04e7-118">Clients can create other bookmarks for remembering other table positions.</span></span> <span data-ttu-id="c04e7-119">Закладки действительны только в том случае, если таблица открыта.</span><span class="sxs-lookup"><span data-stu-id="c04e7-119">Bookmarks are valid only when the table is open.</span></span> <span data-ttu-id="c04e7-120">Перед закрытием связанной таблицы Клиенты должны освободить все созданные вами закладки.</span><span class="sxs-lookup"><span data-stu-id="c04e7-120">Clients must free any bookmarks that they have created before closing the associated table.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c04e7-121">См. также</span><span class="sxs-lookup"><span data-stu-id="c04e7-121">See also</span></span>



[<span data-ttu-id="c04e7-122">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="c04e7-122">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md)
  
[<span data-ttu-id="c04e7-123">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="c04e7-123">IMAPITable::FindRow</span></span>](imapitable-findrow.md)
  
[<span data-ttu-id="c04e7-124">IMAPITable::FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="c04e7-124">IMAPITable::FreeBookmark</span></span>](imapitable-freebookmark.md)
  
[<span data-ttu-id="c04e7-125">IMAPITable::SeekRow</span><span class="sxs-lookup"><span data-stu-id="c04e7-125">IMAPITable::SeekRow</span></span>](imapitable-seekrow.md)


[<span data-ttu-id="c04e7-126">Типы данных MAPI</span><span class="sxs-lookup"><span data-stu-id="c04e7-126">MAPI Data Types</span></span>](mapi-data-types.md)

