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
ms.openlocfilehash: a1ad209ff127a34d7da5ca8dbe1f4a6656d32876
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409456"
---
# <a name="imapitablefreebookmark"></a><span data-ttu-id="5dfcb-103">IMAPITable::FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="5dfcb-103">IMAPITable::FreeBookmark</span></span>

  
  
<span data-ttu-id="5dfcb-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5dfcb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5dfcb-105">Освобождает память, связанную с закладкой.</span><span class="sxs-lookup"><span data-stu-id="5dfcb-105">Releases the memory associated with a bookmark.</span></span>
  
```cpp
HRESULT FreeBookmark(
BOOKMARK bkPosition
);
```

## <a name="parameters"></a><span data-ttu-id="5dfcb-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="5dfcb-106">Parameters</span></span>

 <span data-ttu-id="5dfcb-107">_bkPosition_</span><span class="sxs-lookup"><span data-stu-id="5dfcb-107">_bkPosition_</span></span>
  
> <span data-ttu-id="5dfcb-108">[in] Закладки, которые необходимо освободить, создаются путем вызова [метода IMAPITable::CreateBookmark.](imapitable-createbookmark.md)</span><span class="sxs-lookup"><span data-stu-id="5dfcb-108">[in] The bookmark to be freed, created by calling the [IMAPITable::CreateBookmark](imapitable-createbookmark.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="5dfcb-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5dfcb-109">Return value</span></span>

<span data-ttu-id="5dfcb-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="5dfcb-110">S_OK</span></span> 
  
> <span data-ttu-id="5dfcb-111">Закладка была успешно освобождена.</span><span class="sxs-lookup"><span data-stu-id="5dfcb-111">The bookmark was successfully freed.</span></span>
    
<span data-ttu-id="5dfcb-112">MAPI_E_INVALID_BOOKMARK</span><span class="sxs-lookup"><span data-stu-id="5dfcb-112">MAPI_E_INVALID_BOOKMARK</span></span> 
  
> <span data-ttu-id="5dfcb-113">Указанная закладка не существует.</span><span class="sxs-lookup"><span data-stu-id="5dfcb-113">The specified bookmark does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5dfcb-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="5dfcb-114">Remarks</span></span>

<span data-ttu-id="5dfcb-115">Метод **IMAPITable::FreeBookmark** выпускает закладки, которые больше не нужны.</span><span class="sxs-lookup"><span data-stu-id="5dfcb-115">The **IMAPITable::FreeBookmark** method releases a bookmark that is no longer needed.</span></span> <span data-ttu-id="5dfcb-116">Закладки больше не допустимы после этого вызова.</span><span class="sxs-lookup"><span data-stu-id="5dfcb-116">The bookmark is no longer valid after this call.</span></span> <span data-ttu-id="5dfcb-117">Всякий раз, когда таблица выходит из памяти, все связанные с ней закладки также выпускаются.</span><span class="sxs-lookup"><span data-stu-id="5dfcb-117">Whenever a table is released from memory, all of its associated bookmarks are also released.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="5dfcb-118">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="5dfcb-118">Notes to implementers</span></span>

<span data-ttu-id="5dfcb-119">Если звонячий передает одну из трех заранее заданных закладок в  _параметре bkPosition,_ проигнорировать запрос и S_OK.</span><span class="sxs-lookup"><span data-stu-id="5dfcb-119">If the caller passes one of the three predefined bookmarks in the  _bkPosition_ parameter, ignore the request and return S_OK.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5dfcb-120">См. также</span><span class="sxs-lookup"><span data-stu-id="5dfcb-120">See also</span></span>



[<span data-ttu-id="5dfcb-121">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="5dfcb-121">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md)
  
[<span data-ttu-id="5dfcb-122">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5dfcb-122">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

