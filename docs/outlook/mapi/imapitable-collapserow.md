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
ms.openlocfilehash: b4dd7e9715c2d3c99eda44f7eed0b3360a2e33be
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595302"
---
# <a name="imapitablecollapserow"></a><span data-ttu-id="daa9c-103">IMAPITable::CollapseRow</span><span class="sxs-lookup"><span data-stu-id="daa9c-103">IMAPITable::CollapseRow</span></span>

  
  
<span data-ttu-id="daa9c-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="daa9c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="daa9c-105">Сворачивание категорию расширенной таблицы, удаление все заголовки нижнего уровня и конечные строки, относящегося к категории из в табличном представлении.</span><span class="sxs-lookup"><span data-stu-id="daa9c-105">Collapses an expanded table category, removing any lower-level headings and leaf rows belonging to the category from the table view.</span></span>
  
```cpp
HRESULT CollapseRow(
ULONG cbInstanceKey,
LPBYTE pbInstanceKey,
ULONG ulFlags,
ULONG FAR * lpulRowCount
);
```

## <a name="parameters"></a><span data-ttu-id="daa9c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="daa9c-106">Parameters</span></span>

 <span data-ttu-id="daa9c-107">_cbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="daa9c-107">_cbInstanceKey_</span></span>
  
> <span data-ttu-id="daa9c-108">[in] Число байт в свойстве PR_INSTANCE_KEY, на который указывает параметр _pbInstanceKey_ .</span><span class="sxs-lookup"><span data-stu-id="daa9c-108">[in] The count of bytes in the PR_INSTANCE_KEY property pointed to by the  _pbInstanceKey_ parameter.</span></span> 
    
 <span data-ttu-id="daa9c-109">_pbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="daa9c-109">_pbInstanceKey_</span></span>
  
> <span data-ttu-id="daa9c-110">[in] Указатель на свойство **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), идентифицирующий строку заголовков для категории.</span><span class="sxs-lookup"><span data-stu-id="daa9c-110">[in] A pointer to the **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property that identifies the heading row for the category.</span></span> 
    
 <span data-ttu-id="daa9c-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="daa9c-111">_ulFlags_</span></span>
  
> <span data-ttu-id="daa9c-112">Зарезервировано; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="daa9c-112">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="daa9c-113">_lpulRowCount_</span><span class="sxs-lookup"><span data-stu-id="daa9c-113">_lpulRowCount_</span></span>
  
> <span data-ttu-id="daa9c-114">[out] Указатель на общее количество строк, которые были исключены из в табличном представлении.</span><span class="sxs-lookup"><span data-stu-id="daa9c-114">[out] A pointer to the total number of rows that are being removed from the table view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="daa9c-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="daa9c-115">Return value</span></span>

<span data-ttu-id="daa9c-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="daa9c-116">S_OK</span></span> 
  
> <span data-ttu-id="daa9c-117">Свернуть операция успешно выполнено.</span><span class="sxs-lookup"><span data-stu-id="daa9c-117">The collapse operation has succeeded.</span></span>
    
<span data-ttu-id="daa9c-118">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="daa9c-118">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="daa9c-119">Строка, определенного параметром _pbInstanceKey_ не существует.</span><span class="sxs-lookup"><span data-stu-id="daa9c-119">The row identified by the  _pbInstanceKey_ parameter does not exist.</span></span> 
    
<span data-ttu-id="daa9c-120">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="daa9c-120">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="daa9c-121">Строка, определенного параметром _pbInstanceKey_ не существует.</span><span class="sxs-lookup"><span data-stu-id="daa9c-121">The row identified by the  _pbInstanceKey_ parameter does not exist.</span></span> <span data-ttu-id="daa9c-122">Эта ошибка является альтернативой MAPI_E_NOT_FOUND; поставщиков услуг можно вернуть одну.</span><span class="sxs-lookup"><span data-stu-id="daa9c-122">This error is an alternative to MAPI_E_NOT_FOUND; service providers can return either one.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="daa9c-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="daa9c-123">Remarks</span></span>

<span data-ttu-id="daa9c-124">Метод **IMAPITable::CollapseRow** сворачивает категории таблицы и удаляет его из в табличном представлении.</span><span class="sxs-lookup"><span data-stu-id="daa9c-124">The **IMAPITable::CollapseRow** method collapses a table category and removes it from the table view.</span></span> <span data-ttu-id="daa9c-125">Строки свернуты начиная со строки, заданной свойством **PR_INSTANCE_KEY** указывает параметр _pbInstanceKey_ .</span><span class="sxs-lookup"><span data-stu-id="daa9c-125">The rows are collapsed starting at the row identified by the **PR_INSTANCE_KEY** property pointed to by the  _pbInstanceKey_ parameter.</span></span> <span data-ttu-id="daa9c-126">Число строк, которые удалены в представлении возвращается в содержимое параметра _lpulRowCount_ .</span><span class="sxs-lookup"><span data-stu-id="daa9c-126">The number of rows that are removed from the view is returned in the contents of the  _lpulRowCount_ parameter.</span></span> 
  
<span data-ttu-id="daa9c-127">Уведомления для строки таблицы, которые удаляются из представления, в результате выполнения операции свернуть никогда не создаются.</span><span class="sxs-lookup"><span data-stu-id="daa9c-127">Notifications are never generated for table rows that are removed from a view as the result of a collapse operation.</span></span> 
  
<span data-ttu-id="daa9c-128">Если строка, в которой определяется закладку сворачивается из представления, закладки перемещается для указания на ней отображается строка.</span><span class="sxs-lookup"><span data-stu-id="daa9c-128">When a row that is defined by a bookmark is collapsed out of view, the bookmark is moved to point to the next visible row.</span></span> 
  
<span data-ttu-id="daa9c-129">Дополнительные сведения о таблицах по категориям можно [Сортировка и классификации](sorting-and-categorization.md).</span><span class="sxs-lookup"><span data-stu-id="daa9c-129">For more information about categorized tables, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="daa9c-130">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="daa9c-130">MFCMAPI reference</span></span>

<span data-ttu-id="daa9c-131">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="daa9c-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="daa9c-132">**Файл**</span><span class="sxs-lookup"><span data-stu-id="daa9c-132">**File**</span></span>|<span data-ttu-id="daa9c-133">**Функция**</span><span class="sxs-lookup"><span data-stu-id="daa9c-133">**Function**</span></span>|<span data-ttu-id="daa9c-134">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="daa9c-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="daa9c-135">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="daa9c-135">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="daa9c-136">CContentsTableListCtrl::DoExpandCollapse</span><span class="sxs-lookup"><span data-stu-id="daa9c-136">CContentsTableListCtrl::DoExpandCollapse</span></span>  <br/> |<span data-ttu-id="daa9c-137">Mfcmapi (en) использует метод **IMAPITable::CollapseRow** для Свернуть категорию в таблице.</span><span class="sxs-lookup"><span data-stu-id="daa9c-137">MFCMAPI uses the **IMAPITable::CollapseRow** method to collapse a table category.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="daa9c-138">См. также</span><span class="sxs-lookup"><span data-stu-id="daa9c-138">See also</span></span>



[<span data-ttu-id="daa9c-139">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="daa9c-139">IMAPITable::ExpandRow</span></span>](imapitable-expandrow.md)
  
[<span data-ttu-id="daa9c-140">IMAPITable::GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="daa9c-140">IMAPITable::GetCollapseState</span></span>](imapitable-getcollapsestate.md)
  
[<span data-ttu-id="daa9c-141">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="daa9c-141">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="daa9c-142">IMAPITable::SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="daa9c-142">IMAPITable::SetCollapseState</span></span>](imapitable-setcollapsestate.md)
  
[<span data-ttu-id="daa9c-143">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="daa9c-143">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="daa9c-144">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="daa9c-144">SSortOrderSet</span></span>](ssortorderset.md)
  
[<span data-ttu-id="daa9c-145">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="daa9c-145">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="daa9c-146">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="daa9c-146">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

