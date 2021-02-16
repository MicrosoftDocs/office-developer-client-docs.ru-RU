---
title: IMAPITableCollapseRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.CollapseRow
api_type:
- COM
ms.assetid: 1a23e555-be26-43fb-a715-cfc4ffa623cd
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e6a180ceb325a705ebf226bb728c52cce7396490
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416176"
---
# <a name="imapitablecollapserow"></a><span data-ttu-id="cbea5-103">IMAPITable::CollapseRow</span><span class="sxs-lookup"><span data-stu-id="cbea5-103">IMAPITable::CollapseRow</span></span>

  
  
<span data-ttu-id="cbea5-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cbea5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cbea5-105">Свернет категорию расширенной таблицы, удалив все заголовки нижнего уровня и строки листов, принадлежащие этой категории, из представления таблицы.</span><span class="sxs-lookup"><span data-stu-id="cbea5-105">Collapses an expanded table category, removing any lower-level headings and leaf rows belonging to the category from the table view.</span></span>
  
```cpp
HRESULT CollapseRow(
ULONG cbInstanceKey,
LPBYTE pbInstanceKey,
ULONG ulFlags,
ULONG FAR * lpulRowCount
);
```

## <a name="parameters"></a><span data-ttu-id="cbea5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cbea5-106">Parameters</span></span>

 <span data-ttu-id="cbea5-107">_cbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="cbea5-107">_cbInstanceKey_</span></span>
  
> <span data-ttu-id="cbea5-108">[in] Количество в свойствах PR_INSTANCE_KEY, на которые указывает параметр _pbInstanceKey._</span><span class="sxs-lookup"><span data-stu-id="cbea5-108">[in] The count of bytes in the PR_INSTANCE_KEY property pointed to by the  _pbInstanceKey_ parameter.</span></span> 
    
 <span data-ttu-id="cbea5-109">_pbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="cbea5-109">_pbInstanceKey_</span></span>
  
> <span data-ttu-id="cbea5-110">[in] Указатель на свойство **PR_INSTANCE_KEY** ([PidTagInstanceKey),](pidtaginstancekey-canonical-property.md)которое определяет строку заголовка для категории.</span><span class="sxs-lookup"><span data-stu-id="cbea5-110">[in] A pointer to the **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property that identifies the heading row for the category.</span></span> 
    
 <span data-ttu-id="cbea5-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="cbea5-111">_ulFlags_</span></span>
  
> <span data-ttu-id="cbea5-112">Зарезервировано; должно быть нулем.</span><span class="sxs-lookup"><span data-stu-id="cbea5-112">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="cbea5-113">_lpulRowCount_</span><span class="sxs-lookup"><span data-stu-id="cbea5-113">_lpulRowCount_</span></span>
  
> <span data-ttu-id="cbea5-114">[out] Указатель на общее количество строк, которые удаляются из представления таблицы.</span><span class="sxs-lookup"><span data-stu-id="cbea5-114">[out] A pointer to the total number of rows that are being removed from the table view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="cbea5-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cbea5-115">Return value</span></span>

<span data-ttu-id="cbea5-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="cbea5-116">S_OK</span></span> 
  
> <span data-ttu-id="cbea5-117">Операция свернуть успешно.</span><span class="sxs-lookup"><span data-stu-id="cbea5-117">The collapse operation has succeeded.</span></span>
    
<span data-ttu-id="cbea5-118">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="cbea5-118">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="cbea5-119">Строка, заданная  _параметром pbInstanceKey,_ не существует.</span><span class="sxs-lookup"><span data-stu-id="cbea5-119">The row identified by the  _pbInstanceKey_ parameter does not exist.</span></span> 
    
<span data-ttu-id="cbea5-120">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="cbea5-120">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="cbea5-121">Строка, заданная  _параметром pbInstanceKey,_ не существует.</span><span class="sxs-lookup"><span data-stu-id="cbea5-121">The row identified by the  _pbInstanceKey_ parameter does not exist.</span></span> <span data-ttu-id="cbea5-122">Эта ошибка является альтернативой MAPI_E_NOT_FOUND; поставщики услуг могут вернуть один из них.</span><span class="sxs-lookup"><span data-stu-id="cbea5-122">This error is an alternative to MAPI_E_NOT_FOUND; service providers can return either one.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="cbea5-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="cbea5-123">Remarks</span></span>

<span data-ttu-id="cbea5-124">Метод **IMAPITable::CollapseRow** свергает категорию таблицы и удаляет ее из представления таблицы.</span><span class="sxs-lookup"><span data-stu-id="cbea5-124">The **IMAPITable::CollapseRow** method collapses a table category and removes it from the table view.</span></span> <span data-ttu-id="cbea5-125">Строки свернуты, начиная со строки, заданной свойством **PR_INSTANCE_KEY,** на который указывает параметр _pbInstanceKey._</span><span class="sxs-lookup"><span data-stu-id="cbea5-125">The rows are collapsed starting at the row identified by the **PR_INSTANCE_KEY** property pointed to by the  _pbInstanceKey_ parameter.</span></span> <span data-ttu-id="cbea5-126">Количество строк, которые удаляются из представления, возвращается в содержимом параметра _lpulRowCount._</span><span class="sxs-lookup"><span data-stu-id="cbea5-126">The number of rows that are removed from the view is returned in the contents of the  _lpulRowCount_ parameter.</span></span> 
  
<span data-ttu-id="cbea5-127">Уведомления никогда не создаются для строк таблиц, которые удаляются из представления в результате операции свернуть.</span><span class="sxs-lookup"><span data-stu-id="cbea5-127">Notifications are never generated for table rows that are removed from a view as the result of a collapse operation.</span></span> 
  
<span data-ttu-id="cbea5-128">Когда строка, определяемая закладкой, свернута из представления, закладка перемещается, чтобы указать на следующую видимую строку.</span><span class="sxs-lookup"><span data-stu-id="cbea5-128">When a row that is defined by a bookmark is collapsed out of view, the bookmark is moved to point to the next visible row.</span></span> 
  
<span data-ttu-id="cbea5-129">Дополнительные сведения о классификации таблиц см. в таблице [сортировки и категоризации.](sorting-and-categorization.md)</span><span class="sxs-lookup"><span data-stu-id="cbea5-129">For more information about categorized tables, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="cbea5-130">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="cbea5-130">MFCMAPI reference</span></span>

<span data-ttu-id="cbea5-131">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="cbea5-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="cbea5-132">**Файл**</span><span class="sxs-lookup"><span data-stu-id="cbea5-132">**File**</span></span>|<span data-ttu-id="cbea5-133">**Функция**</span><span class="sxs-lookup"><span data-stu-id="cbea5-133">**Function**</span></span>|<span data-ttu-id="cbea5-134">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="cbea5-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="cbea5-135">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="cbea5-135">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="cbea5-136">CContentsTableListCtrl::D oExpandCollapse</span><span class="sxs-lookup"><span data-stu-id="cbea5-136">CContentsTableListCtrl::DoExpandCollapse</span></span>  <br/> |<span data-ttu-id="cbea5-137">MFCMAPI использует метод **IMAPITable::CollapseRow** для свернуть категорию таблицы.</span><span class="sxs-lookup"><span data-stu-id="cbea5-137">MFCMAPI uses the **IMAPITable::CollapseRow** method to collapse a table category.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cbea5-138">См. также</span><span class="sxs-lookup"><span data-stu-id="cbea5-138">See also</span></span>



[<span data-ttu-id="cbea5-139">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="cbea5-139">IMAPITable::ExpandRow</span></span>](imapitable-expandrow.md)
  
[<span data-ttu-id="cbea5-140">IMAPITable::GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="cbea5-140">IMAPITable::GetCollapseState</span></span>](imapitable-getcollapsestate.md)
  
[<span data-ttu-id="cbea5-141">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="cbea5-141">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="cbea5-142">IMAPITable::SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="cbea5-142">IMAPITable::SetCollapseState</span></span>](imapitable-setcollapsestate.md)
  
[<span data-ttu-id="cbea5-143">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="cbea5-143">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="cbea5-144">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="cbea5-144">SSortOrderSet</span></span>](ssortorderset.md)
  
[<span data-ttu-id="cbea5-145">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cbea5-145">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="cbea5-146">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="cbea5-146">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

