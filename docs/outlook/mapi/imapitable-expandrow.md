---
title: IMAPITableExpandRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.ExpandRow
api_type:
- COM
ms.assetid: b96dd8f6-e648-4014-8a1d-ae1da771c439
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 5e2ce756baaefef7bd0028e746b1dbe10756365e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415168"
---
# <a name="imapitableexpandrow"></a><span data-ttu-id="3f658-103">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="3f658-103">IMAPITable::ExpandRow</span></span>

  
  
<span data-ttu-id="3f658-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3f658-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3f658-105">Расширяет категорию свернутой таблицы, добавляя строки заголовков листового или нижнего уровня, принадлежащие этой категории, в представление таблицы.</span><span class="sxs-lookup"><span data-stu-id="3f658-105">Expands a collapsed table category, adding the leaf or lower-level heading rows belonging to the category to the table view.</span></span>
  
```cpp
HRESULT ExpandRow(
ULONG cbInstanceKey,
LPBYTE pbInstanceKey,
ULONG ulRowCount,
ULONG ulFlags,
LPSRowSet FAR * lppRows,
ULONG FAR * lpulMoreRows
);
```

## <a name="parameters"></a><span data-ttu-id="3f658-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3f658-106">Parameters</span></span>

 <span data-ttu-id="3f658-107">_cbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="3f658-107">_cbInstanceKey_</span></span>
  
> <span data-ttu-id="3f658-108">[in] Количество в свойствах PR_INSTANCE_KEY, на которые указывает параметр _pbInstanceKey._</span><span class="sxs-lookup"><span data-stu-id="3f658-108">[in] The count of bytes in the PR_INSTANCE_KEY property pointed to by the  _pbInstanceKey_ parameter.</span></span> 
    
 <span data-ttu-id="3f658-109">_pbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="3f658-109">_pbInstanceKey_</span></span>
  
> <span data-ttu-id="3f658-110">[in] Указатель на свойство **PR_INSTANCE_KEY** ([PidTagInstanceKey),](pidtaginstancekey-canonical-property.md)которое определяет строку заголовка для категории.</span><span class="sxs-lookup"><span data-stu-id="3f658-110">[in] A pointer to the **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property that identifies the heading row for the category.</span></span> 
    
 <span data-ttu-id="3f658-111">_ulRowCount_</span><span class="sxs-lookup"><span data-stu-id="3f658-111">_ulRowCount_</span></span>
  
> <span data-ttu-id="3f658-112">[in] Максимальное число строк, возвращаемого в _параметре lppRows._</span><span class="sxs-lookup"><span data-stu-id="3f658-112">[in] The maximum number of rows to return in the  _lppRows_ parameter.</span></span> 
    
 <span data-ttu-id="3f658-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3f658-113">_ulFlags_</span></span>
  
> <span data-ttu-id="3f658-114">Зарезервировано; должно быть нулем.</span><span class="sxs-lookup"><span data-stu-id="3f658-114">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="3f658-115">_lppRows_</span><span class="sxs-lookup"><span data-stu-id="3f658-115">_lppRows_</span></span>
  
> <span data-ttu-id="3f658-116">[out] Указатель на структуру [SRowSet,](srowset.md) получающего первые строки (до  _ulRowCount),_ которые были вставлены в представление таблицы в результате расширения.</span><span class="sxs-lookup"><span data-stu-id="3f658-116">[out] A pointer to an [SRowSet](srowset.md) structure receiving the first (up to  _ulRowCount_) rows that have been inserted into the table view as a result of the expansion.</span></span> <span data-ttu-id="3f658-117">Эти строки вставляются после строки заголовка, заданной параметром _pbInstanceKey._</span><span class="sxs-lookup"><span data-stu-id="3f658-117">These rows are inserted after the heading row identified by the  _pbInstanceKey_ parameter.</span></span> <span data-ttu-id="3f658-118">Параметр  _lppRows может_ иметь значение NULL, если параметр  _ulRowCount_ имеет нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="3f658-118">The  _lppRows_ parameter can be NULL if the  _ulRowCount_ parameter is zero.</span></span> 
    
 <span data-ttu-id="3f658-119">_lpulMoreRows_</span><span class="sxs-lookup"><span data-stu-id="3f658-119">_lpulMoreRows_</span></span>
  
> <span data-ttu-id="3f658-120">[out] Указатель на общее количество строк, добавленных в представление таблицы.</span><span class="sxs-lookup"><span data-stu-id="3f658-120">[out] A pointer to the total number of rows that were added to the table view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3f658-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3f658-121">Return value</span></span>

<span data-ttu-id="3f658-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="3f658-122">S_OK</span></span> 
  
> <span data-ttu-id="3f658-123">Категория была успешно расширена.</span><span class="sxs-lookup"><span data-stu-id="3f658-123">The category was expanded successfully.</span></span>
    
<span data-ttu-id="3f658-124">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="3f658-124">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="3f658-125">Строка, заданная  _параметром pbInstanceKey,_ не существует.</span><span class="sxs-lookup"><span data-stu-id="3f658-125">The row identified by the  _pbInstanceKey_ parameter does not exist.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="3f658-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="3f658-126">Remarks</span></span>

<span data-ttu-id="3f658-127">Метод **IMAPITable::ExpandRow** расширяет категорию свернутой таблицы, добавляя строки заголовков листового или нижнего уровня, принадлежащие этой категории, в представление таблицы.</span><span class="sxs-lookup"><span data-stu-id="3f658-127">The **IMAPITable::ExpandRow** method expands a collapsed table category, adding the leaf or lower-level heading rows that belong to the category to the table view.</span></span> <span data-ttu-id="3f658-128">В параметре _ulRowCount_ может быть указано ограничение на количество строк, возвращаемого в _параметре lppRows._</span><span class="sxs-lookup"><span data-stu-id="3f658-128">A limit to the number of rows to be returned in the  _lppRows_ parameter can be specified in the  _ulRowCount_ parameter.</span></span> <span data-ttu-id="3f658-129">Если  _ulRowCount_ имеет значение больше нуля и одна или несколько строк возвращаются в наборе строк, на который указывает  _lppRows,_ положение закладки BOOKMARK_CURRENT перемещается в строку сразу после последней строки в наборе строк.</span><span class="sxs-lookup"><span data-stu-id="3f658-129">When  _ulRowCount_ is set to a value greater than zero and one or more rows are returned in the row set pointed to by  _lppRows_, the position of the bookmark BOOKMARK_CURRENT is moved to the row immediately following the last row in the row set.</span></span>
  
<span data-ttu-id="3f658-130">Если _для ulRowCount_ установлено значение 0, запрашивается добавить строки заголовков нулевого или нижнего уровня в категорию или нулевые строки, так как в категории нет строк заголовков конечного или нижнего уровня, положение BOOKMARK_CURRENT устанавливается на строку после строки, заданной _pbInstanceKey._</span><span class="sxs-lookup"><span data-stu-id="3f658-130">When  _ulRowCount_ is set to zero, requesting that zero leaf or lower-level heading rows be added to the category, or zero rows are returned because there are no leaf or lower-level heading rows in the category, the position of BOOKMARK_CURRENT is set to the row following the row identified by  _pbInstanceKey_.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="3f658-131">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="3f658-131">Notes to implementers</span></span>

<span data-ttu-id="3f658-132">Не создавать уведомления для строк, добавляемой в представление таблицы из-за расширения категории.</span><span class="sxs-lookup"><span data-stu-id="3f658-132">Do not generate notifications on rows that are added to a table view due to category expansion.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="3f658-133">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="3f658-133">Notes to callers</span></span>

<span data-ttu-id="3f658-134">Число строк в наборе строк, на которое указывает параметр  _lppRows,_ не может быть равно числу строк, которые были фактически добавлены в таблицу, а также всему набору строк заголовков конечного или нижнего уровня для категории.</span><span class="sxs-lookup"><span data-stu-id="3f658-134">The number of rows in the row set pointed to by the  _lppRows_ parameter might not equal the number of rows that were actually added to the table, the entire set of leaf or lower-level heading rows for the category.</span></span> <span data-ttu-id="3f658-135">Могут возникать ошибки, например недостаточно памяти или число строк в категории, превышающих число, указанное в параметре _ulRowCount._</span><span class="sxs-lookup"><span data-stu-id="3f658-135">Errors can occur, such as insufficient memory, or the number of rows in the category exceeding the number specified in  _ulRowCount_ parameter.</span></span> <span data-ttu-id="3f658-136">В любом случае BOOKMARK_CURRENT будет иметь положение в последней возвращаемой строке.</span><span class="sxs-lookup"><span data-stu-id="3f658-136">In either case, BOOKMARK_CURRENT will be positioned at the last row returned.</span></span> <span data-ttu-id="3f658-137">Чтобы немедленно получить остальные строки в категории, вызовите [IMAPITable::QueryRows.](imapitable-queryrows.md)</span><span class="sxs-lookup"><span data-stu-id="3f658-137">To immediately retrieve the rest of the rows in the category, call [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span>
  
<span data-ttu-id="3f658-138">Не ожидайте получения уведомления таблицы при смене состояния категории.</span><span class="sxs-lookup"><span data-stu-id="3f658-138">Do not expect to receive a table notification when a category changes its state.</span></span> <span data-ttu-id="3f658-139">Можно поддерживать локальный кэш строк, которые можно обновлять с помощью каждого вызова **ExpandRow** **или CollapseRow.**</span><span class="sxs-lookup"><span data-stu-id="3f658-139">You can maintain a local cache of rows that can be updated with every **ExpandRow** or **CollapseRow** call.</span></span> 
  
<span data-ttu-id="3f658-140">Дополнительные сведения о классификации таблиц см. в таблице [сортировки и категоризации.](sorting-and-categorization.md)</span><span class="sxs-lookup"><span data-stu-id="3f658-140">For more information about categorized tables, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="3f658-141">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="3f658-141">MFCMAPI reference</span></span>

<span data-ttu-id="3f658-142">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="3f658-142">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="3f658-143">**Файл**</span><span class="sxs-lookup"><span data-stu-id="3f658-143">**File**</span></span>|<span data-ttu-id="3f658-144">**Функция**</span><span class="sxs-lookup"><span data-stu-id="3f658-144">**Function**</span></span>|<span data-ttu-id="3f658-145">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="3f658-145">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3f658-146">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="3f658-146">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="3f658-147">CContentsTableListCtrl::D oExpandCollapse</span><span class="sxs-lookup"><span data-stu-id="3f658-147">CContentsTableListCtrl::DoExpandCollapse</span></span>  <br/> |<span data-ttu-id="3f658-148">MFCMAPI использует метод **IMAPITable::ExpandRow** для расширения категории свернутой таблицы.</span><span class="sxs-lookup"><span data-stu-id="3f658-148">MFCMAPI uses the **IMAPITable::ExpandRow** method to expand a collapsed table category.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3f658-149">См. также</span><span class="sxs-lookup"><span data-stu-id="3f658-149">See also</span></span>



[<span data-ttu-id="3f658-150">IMAPITable::CollapseRow</span><span class="sxs-lookup"><span data-stu-id="3f658-150">IMAPITable::CollapseRow</span></span>](imapitable-collapserow.md)
  
[<span data-ttu-id="3f658-151">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3f658-151">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="3f658-152">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="3f658-152">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

