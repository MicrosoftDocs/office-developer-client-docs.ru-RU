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
# <a name="imapitableexpandrow"></a><span data-ttu-id="45a1f-103">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="45a1f-103">IMAPITable::ExpandRow</span></span>

  
  
<span data-ttu-id="45a1f-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="45a1f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="45a1f-105">Расширяет категорию обрушения таблицы, добавляя в представление таблицы лист или строки заголовка нижнего уровня, принадлежащие этой категории.</span><span class="sxs-lookup"><span data-stu-id="45a1f-105">Expands a collapsed table category, adding the leaf or lower-level heading rows belonging to the category to the table view.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="45a1f-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="45a1f-106">Parameters</span></span>

 <span data-ttu-id="45a1f-107">_cbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="45a1f-107">_cbInstanceKey_</span></span>
  
> <span data-ttu-id="45a1f-108">[in] Количество битов в свойстве PR_INSTANCE_KEY, на который указывает параметр _pbInstanceKey._</span><span class="sxs-lookup"><span data-stu-id="45a1f-108">[in] The count of bytes in the PR_INSTANCE_KEY property pointed to by the  _pbInstanceKey_ parameter.</span></span> 
    
 <span data-ttu-id="45a1f-109">_pbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="45a1f-109">_pbInstanceKey_</span></span>
  
> <span data-ttu-id="45a1f-110">[in] Указатель на **свойство PR_INSTANCE_KEY** [(PidTagInstanceKey),](pidtaginstancekey-canonical-property.md)которое определяет строку заголовка для категории.</span><span class="sxs-lookup"><span data-stu-id="45a1f-110">[in] A pointer to the **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property that identifies the heading row for the category.</span></span> 
    
 <span data-ttu-id="45a1f-111">_ulRowCount_</span><span class="sxs-lookup"><span data-stu-id="45a1f-111">_ulRowCount_</span></span>
  
> <span data-ttu-id="45a1f-112">[in] Максимальное количество строк, возвращаемых в _параметре lppRows._</span><span class="sxs-lookup"><span data-stu-id="45a1f-112">[in] The maximum number of rows to return in the  _lppRows_ parameter.</span></span> 
    
 <span data-ttu-id="45a1f-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="45a1f-113">_ulFlags_</span></span>
  
> <span data-ttu-id="45a1f-114">Зарезервировано; должно быть нулевой.</span><span class="sxs-lookup"><span data-stu-id="45a1f-114">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="45a1f-115">_lppRows_</span><span class="sxs-lookup"><span data-stu-id="45a1f-115">_lppRows_</span></span>
  
> <span data-ttu-id="45a1f-116">[вышел] Указатель на структуру [SRowSet,](srowset.md) получающего первые (до  _ulRowCount)_ строки, вставленные в представление таблицы в результате расширения.</span><span class="sxs-lookup"><span data-stu-id="45a1f-116">[out] A pointer to an [SRowSet](srowset.md) structure receiving the first (up to  _ulRowCount_) rows that have been inserted into the table view as a result of the expansion.</span></span> <span data-ttu-id="45a1f-117">Эти строки вставляются после строки заголовка, которая определена _параметром pbInstanceKey._</span><span class="sxs-lookup"><span data-stu-id="45a1f-117">These rows are inserted after the heading row identified by the  _pbInstanceKey_ parameter.</span></span> <span data-ttu-id="45a1f-118">Параметр  _lppRows может_ быть NULL, если  _параметр ulRowCount_ — ноль.</span><span class="sxs-lookup"><span data-stu-id="45a1f-118">The  _lppRows_ parameter can be NULL if the  _ulRowCount_ parameter is zero.</span></span> 
    
 <span data-ttu-id="45a1f-119">_lpulMoreRows_</span><span class="sxs-lookup"><span data-stu-id="45a1f-119">_lpulMoreRows_</span></span>
  
> <span data-ttu-id="45a1f-120">[вышел] Указатель на общее количество строк, добавленных в представление таблицы.</span><span class="sxs-lookup"><span data-stu-id="45a1f-120">[out] A pointer to the total number of rows that were added to the table view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="45a1f-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="45a1f-121">Return value</span></span>

<span data-ttu-id="45a1f-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="45a1f-122">S_OK</span></span> 
  
> <span data-ttu-id="45a1f-123">Категория была успешно расширена.</span><span class="sxs-lookup"><span data-stu-id="45a1f-123">The category was expanded successfully.</span></span>
    
<span data-ttu-id="45a1f-124">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="45a1f-124">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="45a1f-125">Строка, определенная  _параметром pbInstanceKey,_ не существует.</span><span class="sxs-lookup"><span data-stu-id="45a1f-125">The row identified by the  _pbInstanceKey_ parameter does not exist.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="45a1f-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="45a1f-126">Remarks</span></span>

<span data-ttu-id="45a1f-127">Метод **IMAPITable::ExpandRow** расширяет категорию обрушения таблицы, добавляя в представление таблицы лист или строки заголовка более низкого уровня, которые относятся к категории.</span><span class="sxs-lookup"><span data-stu-id="45a1f-127">The **IMAPITable::ExpandRow** method expands a collapsed table category, adding the leaf or lower-level heading rows that belong to the category to the table view.</span></span> <span data-ttu-id="45a1f-128">Ограничение количества строк, возвращаемого в _параметре lppRows,_ может быть указано в _параметре ulRowCount._</span><span class="sxs-lookup"><span data-stu-id="45a1f-128">A limit to the number of rows to be returned in the  _lppRows_ parameter can be specified in the  _ulRowCount_ parameter.</span></span> <span data-ttu-id="45a1f-129">Если  _значение ulRowCount_ превышает 0, а в наборе строк, на которые указывают  _lppRows,_ возвращается одно или несколько строк, положение закладки BOOKMARK_CURRENT перемещается в строку сразу после последней строки в наборе строк.</span><span class="sxs-lookup"><span data-stu-id="45a1f-129">When  _ulRowCount_ is set to a value greater than zero and one or more rows are returned in the row set pointed to by  _lppRows_, the position of the bookmark BOOKMARK_CURRENT is moved to the row immediately following the last row in the row set.</span></span>
  
<span data-ttu-id="45a1f-130">Если _значение ulRowCount_ установлено на нулевом уровне, запрашивая, чтобы в категорию добавлялись строки с нулевой или нижней строками заголовков, либо возвращались нулевые строки, так как в этой категории нет строки заголовка на уровне листа или нижнего уровня, положение BOOKMARK_CURRENT заданной строкой после строки, идентифицированной _pbInstanceKey._</span><span class="sxs-lookup"><span data-stu-id="45a1f-130">When  _ulRowCount_ is set to zero, requesting that zero leaf or lower-level heading rows be added to the category, or zero rows are returned because there are no leaf or lower-level heading rows in the category, the position of BOOKMARK_CURRENT is set to the row following the row identified by  _pbInstanceKey_.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="45a1f-131">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="45a1f-131">Notes to implementers</span></span>

<span data-ttu-id="45a1f-132">Не создавать уведомления на строках, которые добавляются в представление таблицы из-за расширения категорий.</span><span class="sxs-lookup"><span data-stu-id="45a1f-132">Do not generate notifications on rows that are added to a table view due to category expansion.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="45a1f-133">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="45a1f-133">Notes to callers</span></span>

<span data-ttu-id="45a1f-134">Количество строк в наборе строк, на которое указывает параметр  _lppRows,_ может не равняться количеству строк, которые были добавлены в таблицу, всему набору строк заголовка листа или строки заголовка более низкого уровня для категории.</span><span class="sxs-lookup"><span data-stu-id="45a1f-134">The number of rows in the row set pointed to by the  _lppRows_ parameter might not equal the number of rows that were actually added to the table, the entire set of leaf or lower-level heading rows for the category.</span></span> <span data-ttu-id="45a1f-135">Могут возникать ошибки, такие как нехватка памяти или количество строк в категории, превышающих число, указанное в параметре _ulRowCount._</span><span class="sxs-lookup"><span data-stu-id="45a1f-135">Errors can occur, such as insufficient memory, or the number of rows in the category exceeding the number specified in  _ulRowCount_ parameter.</span></span> <span data-ttu-id="45a1f-136">В любом случае BOOKMARK_CURRENT будет позицион BOOKMARK_CURRENT в последней строке.</span><span class="sxs-lookup"><span data-stu-id="45a1f-136">In either case, BOOKMARK_CURRENT will be positioned at the last row returned.</span></span> <span data-ttu-id="45a1f-137">Чтобы немедленно получить остальные строки в этой категории, позвоните [в IMAPITable::QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="45a1f-137">To immediately retrieve the rest of the rows in the category, call [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span>
  
<span data-ttu-id="45a1f-138">Не ожидайте получения уведомления таблицы при смене состояния категории.</span><span class="sxs-lookup"><span data-stu-id="45a1f-138">Do not expect to receive a table notification when a category changes its state.</span></span> <span data-ttu-id="45a1f-139">Можно сохранить локальный кэш строк, которые можно обновить с помощью каждого вызова **ExpandRow** или **CollapseRow.**</span><span class="sxs-lookup"><span data-stu-id="45a1f-139">You can maintain a local cache of rows that can be updated with every **ExpandRow** or **CollapseRow** call.</span></span> 
  
<span data-ttu-id="45a1f-140">Дополнительные сведения о классификации таблиц см. в [рубрике Сортировка и классификация.](sorting-and-categorization.md)</span><span class="sxs-lookup"><span data-stu-id="45a1f-140">For more information about categorized tables, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="45a1f-141">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="45a1f-141">MFCMAPI reference</span></span>

<span data-ttu-id="45a1f-142">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="45a1f-142">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="45a1f-143">**Файл**</span><span class="sxs-lookup"><span data-stu-id="45a1f-143">**File**</span></span>|<span data-ttu-id="45a1f-144">**Функция**</span><span class="sxs-lookup"><span data-stu-id="45a1f-144">**Function**</span></span>|<span data-ttu-id="45a1f-145">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="45a1f-145">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="45a1f-146">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="45a1f-146">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="45a1f-147">CContentsTableListCtrl::D oExpandCollapse</span><span class="sxs-lookup"><span data-stu-id="45a1f-147">CContentsTableListCtrl::DoExpandCollapse</span></span>  <br/> |<span data-ttu-id="45a1f-148">MFCMAPI использует **метод IMAPITable::ExpandRow** для расширения категории обрушения таблицы.</span><span class="sxs-lookup"><span data-stu-id="45a1f-148">MFCMAPI uses the **IMAPITable::ExpandRow** method to expand a collapsed table category.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="45a1f-149">См. также</span><span class="sxs-lookup"><span data-stu-id="45a1f-149">See also</span></span>



[<span data-ttu-id="45a1f-150">IMAPITable::CollapseRow</span><span class="sxs-lookup"><span data-stu-id="45a1f-150">IMAPITable::CollapseRow</span></span>](imapitable-collapserow.md)
  
[<span data-ttu-id="45a1f-151">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="45a1f-151">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="45a1f-152">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="45a1f-152">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

