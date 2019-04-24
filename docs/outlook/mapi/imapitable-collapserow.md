---
title: Имапитаблеколлапсеров
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328969"
---
# <a name="imapitablecollapserow"></a><span data-ttu-id="d6fca-103">IMAPITable::CollapseRow</span><span class="sxs-lookup"><span data-stu-id="d6fca-103">IMAPITable::CollapseRow</span></span>

  
  
<span data-ttu-id="d6fca-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d6fca-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d6fca-105">Сворачивает развернутую категорию таблицы, удаляя все заголовки нижнего уровня и конечные строки, принадлежащие к категории, из представления таблицы.</span><span class="sxs-lookup"><span data-stu-id="d6fca-105">Collapses an expanded table category, removing any lower-level headings and leaf rows belonging to the category from the table view.</span></span>
  
```cpp
HRESULT CollapseRow(
ULONG cbInstanceKey,
LPBYTE pbInstanceKey,
ULONG ulFlags,
ULONG FAR * lpulRowCount
);
```

## <a name="parameters"></a><span data-ttu-id="d6fca-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d6fca-106">Parameters</span></span>

 <span data-ttu-id="d6fca-107">_Кбинстанцекэй_</span><span class="sxs-lookup"><span data-stu-id="d6fca-107">_cbInstanceKey_</span></span>
  
> <span data-ttu-id="d6fca-108">возврата Количество байтов в свойстве ПР_ИНСТАНЦЕ_КЭЙ, на которое указывает параметр _пбинстанцекэй_ .</span><span class="sxs-lookup"><span data-stu-id="d6fca-108">[in] The count of bytes in the PR_INSTANCE_KEY property pointed to by the  _pbInstanceKey_ parameter.</span></span> 
    
 <span data-ttu-id="d6fca-109">_Пбинстанцекэй_</span><span class="sxs-lookup"><span data-stu-id="d6fca-109">_pbInstanceKey_</span></span>
  
> <span data-ttu-id="d6fca-110">возврата Указатель на свойство **пр_инстанце_кэй** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), которое определяет строку заголовка для категории.</span><span class="sxs-lookup"><span data-stu-id="d6fca-110">[in] A pointer to the **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property that identifies the heading row for the category.</span></span> 
    
 <span data-ttu-id="d6fca-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d6fca-111">_ulFlags_</span></span>
  
> <span data-ttu-id="d6fca-112">Резервирования должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="d6fca-112">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="d6fca-113">_Лпулровкаунт_</span><span class="sxs-lookup"><span data-stu-id="d6fca-113">_lpulRowCount_</span></span>
  
> <span data-ttu-id="d6fca-114">вышли Указатель на общее число строк, которые удаляются из представления таблицы.</span><span class="sxs-lookup"><span data-stu-id="d6fca-114">[out] A pointer to the total number of rows that are being removed from the table view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d6fca-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d6fca-115">Return value</span></span>

<span data-ttu-id="d6fca-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="d6fca-116">S_OK</span></span> 
  
> <span data-ttu-id="d6fca-117">Операция сворачивания выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="d6fca-117">The collapse operation has succeeded.</span></span>
    
<span data-ttu-id="d6fca-118">МАПИ_Е_НОТ_ФАУНД</span><span class="sxs-lookup"><span data-stu-id="d6fca-118">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="d6fca-119">Строка, указанная с помощью параметра _пбинстанцекэй_ , не существует.</span><span class="sxs-lookup"><span data-stu-id="d6fca-119">The row identified by the  _pbInstanceKey_ parameter does not exist.</span></span> 
    
<span data-ttu-id="d6fca-120">МАПИ_Е_ИНВАЛИД_ЕНТРИД</span><span class="sxs-lookup"><span data-stu-id="d6fca-120">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="d6fca-121">Строка, указанная с помощью параметра _пбинстанцекэй_ , не существует.</span><span class="sxs-lookup"><span data-stu-id="d6fca-121">The row identified by the  _pbInstanceKey_ parameter does not exist.</span></span> <span data-ttu-id="d6fca-122">Эта ошибка является альтернативой МАПИ_Е_НОТ_ФАУНД; поставщики услуг могут возвращать один из них.</span><span class="sxs-lookup"><span data-stu-id="d6fca-122">This error is an alternative to MAPI_E_NOT_FOUND; service providers can return either one.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="d6fca-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d6fca-123">Remarks</span></span>

<span data-ttu-id="d6fca-124">Метод **IMAPITable:: коллапсеров** сворачивает категорию таблицы и удаляет ее из представления таблицы.</span><span class="sxs-lookup"><span data-stu-id="d6fca-124">The **IMAPITable::CollapseRow** method collapses a table category and removes it from the table view.</span></span> <span data-ttu-id="d6fca-125">Строки свернуты, начиная со строки, указанной свойством **пр_инстанце_кэй** , на которую указывает параметр _пбинстанцекэй_ .</span><span class="sxs-lookup"><span data-stu-id="d6fca-125">The rows are collapsed starting at the row identified by the **PR_INSTANCE_KEY** property pointed to by the  _pbInstanceKey_ parameter.</span></span> <span data-ttu-id="d6fca-126">Количество строк, удаленных из представления, возвращается в содержимом параметра _лпулровкаунт_ .</span><span class="sxs-lookup"><span data-stu-id="d6fca-126">The number of rows that are removed from the view is returned in the contents of the  _lpulRowCount_ parameter.</span></span> 
  
<span data-ttu-id="d6fca-127">Уведомления никогда не создаются для строк таблицы, которые удаляются из представления в результате выполнения операции свертывания.</span><span class="sxs-lookup"><span data-stu-id="d6fca-127">Notifications are never generated for table rows that are removed from a view as the result of a collapse operation.</span></span> 
  
<span data-ttu-id="d6fca-128">Когда строка, определенная закладками, свернута в представлении, закладка перемещается в указатель на следующую видимую строку.</span><span class="sxs-lookup"><span data-stu-id="d6fca-128">When a row that is defined by a bookmark is collapsed out of view, the bookmark is moved to point to the next visible row.</span></span> 
  
<span data-ttu-id="d6fca-129">Для получения дополнительных сведений об классифицированных таблицах, ознакомьтесь со статьей [Сортировка и категоризация](sorting-and-categorization.md).</span><span class="sxs-lookup"><span data-stu-id="d6fca-129">For more information about categorized tables, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="d6fca-130">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="d6fca-130">MFCMAPI reference</span></span>

<span data-ttu-id="d6fca-131">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="d6fca-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d6fca-132">**Файл**</span><span class="sxs-lookup"><span data-stu-id="d6fca-132">**File**</span></span>|<span data-ttu-id="d6fca-133">**Функция**</span><span class="sxs-lookup"><span data-stu-id="d6fca-133">**Function**</span></span>|<span data-ttu-id="d6fca-134">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="d6fca-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d6fca-135">Контентстаблелистктрл. cpp</span><span class="sxs-lookup"><span data-stu-id="d6fca-135">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="d6fca-136">Кконтентстаблелистктрл::D Оекспандколлапсе</span><span class="sxs-lookup"><span data-stu-id="d6fca-136">CContentsTableListCtrl::DoExpandCollapse</span></span>  <br/> |<span data-ttu-id="d6fca-137">MFCMAPI использует метод **IMAPITable:: коллапсеров** для сворачивания категории таблицы.</span><span class="sxs-lookup"><span data-stu-id="d6fca-137">MFCMAPI uses the **IMAPITable::CollapseRow** method to collapse a table category.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d6fca-138">См. также</span><span class="sxs-lookup"><span data-stu-id="d6fca-138">See also</span></span>



[<span data-ttu-id="d6fca-139">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="d6fca-139">IMAPITable::ExpandRow</span></span>](imapitable-expandrow.md)
  
[<span data-ttu-id="d6fca-140">IMAPITable::GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="d6fca-140">IMAPITable::GetCollapseState</span></span>](imapitable-getcollapsestate.md)
  
[<span data-ttu-id="d6fca-141">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="d6fca-141">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="d6fca-142">IMAPITable::SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="d6fca-142">IMAPITable::SetCollapseState</span></span>](imapitable-setcollapsestate.md)
  
[<span data-ttu-id="d6fca-143">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="d6fca-143">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="d6fca-144">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="d6fca-144">SSortOrderSet</span></span>](ssortorderset.md)
  
[<span data-ttu-id="d6fca-145">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d6fca-145">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="d6fca-146">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="d6fca-146">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

