---
title: Имапитаблекуерисортордер
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.QuerySortOrder
api_type:
- COM
ms.assetid: 7b4ca523-0703-417c-8586-c4324c200020
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 61991972fdf8674a9ffd2b790e26c7fa669df357
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328863"
---
# <a name="imapitablequerysortorder"></a><span data-ttu-id="12340-103">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="12340-103">IMAPITable::QuerySortOrder</span></span>

  
  
<span data-ttu-id="12340-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="12340-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="12340-105">Получает текущий порядок сортировки таблицы.</span><span class="sxs-lookup"><span data-stu-id="12340-105">Retrieves the current sort order for a table.</span></span>
  
```cpp
HRESULT QuerySortOrder(
LPSSortOrderSet FAR * lppSortCriteria
);
```

## <a name="parameters"></a><span data-ttu-id="12340-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="12340-106">Parameters</span></span>

 <span data-ttu-id="12340-107">_Лппсорткритериа_</span><span class="sxs-lookup"><span data-stu-id="12340-107">_lppSortCriteria_</span></span>
  
> <span data-ttu-id="12340-108">вышли Указатель на указатель на структуру [ссортордерсет](ssortorderset.md) , содержащую текущий порядок сортировки.</span><span class="sxs-lookup"><span data-stu-id="12340-108">[out] Pointer to a pointer to the [SSortOrderSet](ssortorderset.md) structure holding the current sort order.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="12340-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="12340-109">Return value</span></span>

<span data-ttu-id="12340-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="12340-110">S_OK</span></span> 
  
> <span data-ttu-id="12340-111">Текущий порядок сортировки успешно возвращен.</span><span class="sxs-lookup"><span data-stu-id="12340-111">The current sort order was successfully returned.</span></span>
    
<span data-ttu-id="12340-112">МАПИ_Е_БУСИ</span><span class="sxs-lookup"><span data-stu-id="12340-112">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="12340-113">Выполняется другая операция, которая не позволяет запустить операцию извлечения порядка сортировки.</span><span class="sxs-lookup"><span data-stu-id="12340-113">Another operation is in progress that prevents the sort order retrieval operation from starting.</span></span> <span data-ttu-id="12340-114">Выполнение выполняемой операции должно быть разрешено или остановлено.</span><span class="sxs-lookup"><span data-stu-id="12340-114">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="12340-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="12340-115">Remarks</span></span>

<span data-ttu-id="12340-116">Метод **IMAPITable:: куерисортордер** получает текущий порядок сортировки таблицы.</span><span class="sxs-lookup"><span data-stu-id="12340-116">The **IMAPITable::QuerySortOrder** method retrieves the current sort order for a table.</span></span> <span data-ttu-id="12340-117">Порядок сортировки описан в структуре [ссортордерсет](ssortorderset.md) .</span><span class="sxs-lookup"><span data-stu-id="12340-117">Sort orders are described with an [SSortOrderSet](ssortorderset.md) structure.</span></span> 
  
- <span data-ttu-id="12340-118">Элемент **ксортс** структуры **ссортордерсет** может иметь нулевое значение, если:</span><span class="sxs-lookup"><span data-stu-id="12340-118">The **cSorts** member of the **SSortOrderSet** structure can be set to zero if:</span></span> 
    
- <span data-ttu-id="12340-119">Таблица не отсортирована.</span><span class="sxs-lookup"><span data-stu-id="12340-119">The table is unsorted.</span></span>
    
- <span data-ttu-id="12340-120">Нет сведений о том, как сортируется таблица.</span><span class="sxs-lookup"><span data-stu-id="12340-120">There is no information about how the table is sorted.</span></span>
    
- <span data-ttu-id="12340-121">Структура **ссортордерсет** не подходит для описания порядка сортировки.</span><span class="sxs-lookup"><span data-stu-id="12340-121">The **SSortOrderSet** structure is not appropriate for describing the sort order.</span></span> 
    
## <a name="notes-to-implementers"></a><span data-ttu-id="12340-122">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="12340-122">Notes to implementers</span></span>

<span data-ttu-id="12340-123">Если вызывается метод [IMAPITable:: сорттабле](imapitable-sorttable.md) с структурой **ссортордерсет** , содержащей нулевые столбцы в ключе сортировки, удалите текущий порядок сортировки и примените порядок по умолчанию, если таковой имеется.</span><span class="sxs-lookup"><span data-stu-id="12340-123">If a call is made to your [IMAPITable::SortTable](imapitable-sorttable.md) method with an **SSortOrderSet** structure containing zero columns in the sort key, remove the current sort order and apply the default order, if there is one.</span></span> <span data-ttu-id="12340-124">При последующих вызовах **куерисортордер**можно выбрать, возвращать ли ноль или больше столбцов для ключа сортировки.</span><span class="sxs-lookup"><span data-stu-id="12340-124">In subsequent calls to **QuerySortOrder**, you can choose whether to return zero or more columns for the sort key.</span></span> <span data-ttu-id="12340-125">Можно вернуть больше столбцов, чем в указанном представлении.</span><span class="sxs-lookup"><span data-stu-id="12340-125">You can return more columns than are in the present view.</span></span>
  
<span data-ttu-id="12340-126">Более подробную информацию о сортировке можно узнать в статье [Сортировка и категоризация](sorting-and-categorization.md).</span><span class="sxs-lookup"><span data-stu-id="12340-126">For more information about sorting, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="12340-127">См. также</span><span class="sxs-lookup"><span data-stu-id="12340-127">See also</span></span>



[<span data-ttu-id="12340-128">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="12340-128">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="12340-129">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="12340-129">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="12340-130">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="12340-130">SSortOrderSet</span></span>](ssortorderset.md)
  
[<span data-ttu-id="12340-131">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="12340-131">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

