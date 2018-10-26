---
title: IMAPITableFreeBookmark
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.FreeBookmark
api_type:
- COM
ms.assetid: 797833f7-8295-41bc-8980-977e5f5e05e8
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 36d1518764985c4783d967e263ca5c05d63f935f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588484"
---
# <a name="imapitablefreebookmark"></a><span data-ttu-id="a8a26-103">IMAPITable::FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="a8a26-103">IMAPITable::FreeBookmark</span></span>

  
  
<span data-ttu-id="a8a26-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a8a26-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a8a26-105">Освобождает память, связанную с закладку.</span><span class="sxs-lookup"><span data-stu-id="a8a26-105">Releases the memory associated with a bookmark.</span></span>
  
```cpp
HRESULT FreeBookmark(
BOOKMARK bkPosition
);
```

## <a name="parameters"></a><span data-ttu-id="a8a26-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a8a26-106">Parameters</span></span>

 <span data-ttu-id="a8a26-107">_bkPosition_</span><span class="sxs-lookup"><span data-stu-id="a8a26-107">_bkPosition_</span></span>
  
> <span data-ttu-id="a8a26-108">[in] Закладка освобождения, созданные путем вызова метода [IMAPITable::CreateBookmark](imapitable-createbookmark.md) .</span><span class="sxs-lookup"><span data-stu-id="a8a26-108">[in] The bookmark to be freed, created by calling the [IMAPITable::CreateBookmark](imapitable-createbookmark.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a8a26-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a8a26-109">Return value</span></span>

<span data-ttu-id="a8a26-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="a8a26-110">S_OK</span></span> 
  
> <span data-ttu-id="a8a26-111">Закладки успешно освободить.</span><span class="sxs-lookup"><span data-stu-id="a8a26-111">The bookmark was successfully freed.</span></span>
    
<span data-ttu-id="a8a26-112">MAPI_E_INVALID_BOOKMARK</span><span class="sxs-lookup"><span data-stu-id="a8a26-112">MAPI_E_INVALID_BOOKMARK</span></span> 
  
> <span data-ttu-id="a8a26-113">Указанный закладка не существует.</span><span class="sxs-lookup"><span data-stu-id="a8a26-113">The specified bookmark does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a8a26-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="a8a26-114">Remarks</span></span>

<span data-ttu-id="a8a26-115">Метод **IMAPITable::FreeBookmark** освобождает закладки, больше не требуется.</span><span class="sxs-lookup"><span data-stu-id="a8a26-115">The **IMAPITable::FreeBookmark** method releases a bookmark that is no longer needed.</span></span> <span data-ttu-id="a8a26-116">Закладки больше не является допустимым после этого вызова.</span><span class="sxs-lookup"><span data-stu-id="a8a26-116">The bookmark is no longer valid after this call.</span></span> <span data-ttu-id="a8a26-117">Каждый раз, когда освобождения таблицы из памяти все его связанного закладки также снимается.</span><span class="sxs-lookup"><span data-stu-id="a8a26-117">Whenever a table is released from memory, all of its associated bookmarks are also released.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="a8a26-118">Примечания для реализующих</span><span class="sxs-lookup"><span data-stu-id="a8a26-118">Notes to implementers</span></span>

<span data-ttu-id="a8a26-119">Если вызывающий объект передает один из трех предварительно заданных закладки с помощью параметра _bkPosition_ , пропуск запроса и возвращает значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="a8a26-119">If the caller passes one of the three predefined bookmarks in the  _bkPosition_ parameter, ignore the request and return S_OK.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a8a26-120">См. также</span><span class="sxs-lookup"><span data-stu-id="a8a26-120">See also</span></span>



[<span data-ttu-id="a8a26-121">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="a8a26-121">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md)
  
[<span data-ttu-id="a8a26-122">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a8a26-122">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

