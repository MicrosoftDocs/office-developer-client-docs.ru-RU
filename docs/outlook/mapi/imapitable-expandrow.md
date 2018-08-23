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
ms.openlocfilehash: ce78c6873f3a1dc034ae33f3c9e965ef8f2f1815
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563781"
---
# <a name="imapitableexpandrow"></a><span data-ttu-id="43638-103">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="43638-103">IMAPITable::ExpandRow</span></span>

  
  
<span data-ttu-id="43638-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="43638-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="43638-105">При развертывании категории свернутые таблицы, добавление конечных или нижнем уровне заголовка строки, относящегося к категории, которую требуется в табличном представлении.</span><span class="sxs-lookup"><span data-stu-id="43638-105">Expands a collapsed table category, adding the leaf or lower-level heading rows belonging to the category to the table view.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="43638-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="43638-106">Parameters</span></span>

 <span data-ttu-id="43638-107">_cbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="43638-107">_cbInstanceKey_</span></span>
  
> <span data-ttu-id="43638-108">[in] Число байт в свойстве PR_INSTANCE_KEY, на который указывает параметр _pbInstanceKey_ .</span><span class="sxs-lookup"><span data-stu-id="43638-108">[in] The count of bytes in the PR_INSTANCE_KEY property pointed to by the  _pbInstanceKey_ parameter.</span></span> 
    
 <span data-ttu-id="43638-109">_pbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="43638-109">_pbInstanceKey_</span></span>
  
> <span data-ttu-id="43638-110">[in] Указатель на свойство **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), идентифицирующий строку заголовков для категории.</span><span class="sxs-lookup"><span data-stu-id="43638-110">[in] A pointer to the **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property that identifies the heading row for the category.</span></span> 
    
 <span data-ttu-id="43638-111">_ulRowCount_</span><span class="sxs-lookup"><span data-stu-id="43638-111">_ulRowCount_</span></span>
  
> <span data-ttu-id="43638-112">[in] Максимальное число строк для возвращения в параметре _lppRows_ .</span><span class="sxs-lookup"><span data-stu-id="43638-112">[in] The maximum number of rows to return in the  _lppRows_ parameter.</span></span> 
    
 <span data-ttu-id="43638-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="43638-113">_ulFlags_</span></span>
  
> <span data-ttu-id="43638-114">Зарезервировано; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="43638-114">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="43638-115">_lppRows_</span><span class="sxs-lookup"><span data-stu-id="43638-115">_lppRows_</span></span>
  
> <span data-ttu-id="43638-116">[out] Указатель на структуру [SRowSet](srowset.md) , получение первого (до _ulRowCount_) строк, добавленных в табличном представлении из-за развертывание.</span><span class="sxs-lookup"><span data-stu-id="43638-116">[out] A pointer to an [SRowSet](srowset.md) structure receiving the first (up to  _ulRowCount_) rows that have been inserted into the table view as a result of the expansion.</span></span> <span data-ttu-id="43638-117">Эти строки вставляется после строки заголовка, определенного параметром _pbInstanceKey_ .</span><span class="sxs-lookup"><span data-stu-id="43638-117">These rows are inserted after the heading row identified by the  _pbInstanceKey_ parameter.</span></span> <span data-ttu-id="43638-118">Параметр _lppRows_ может быть NULL, если параметр _ulRowCount_ равно нулю.</span><span class="sxs-lookup"><span data-stu-id="43638-118">The  _lppRows_ parameter can be NULL if the  _ulRowCount_ parameter is zero.</span></span> 
    
 <span data-ttu-id="43638-119">_lpulMoreRows_</span><span class="sxs-lookup"><span data-stu-id="43638-119">_lpulMoreRows_</span></span>
  
> <span data-ttu-id="43638-120">[out] Указатель на общее количество строк, которые были добавлены в табличном представлении.</span><span class="sxs-lookup"><span data-stu-id="43638-120">[out] A pointer to the total number of rows that were added to the table view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="43638-121">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="43638-121">Return value</span></span>

<span data-ttu-id="43638-122">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="43638-122">S_OK</span></span> 
  
> <span data-ttu-id="43638-123">Категории была расширена успешно.</span><span class="sxs-lookup"><span data-stu-id="43638-123">The category was expanded successfully.</span></span>
    
<span data-ttu-id="43638-124">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="43638-124">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="43638-125">Строка, определенного параметром _pbInstanceKey_ не существует.</span><span class="sxs-lookup"><span data-stu-id="43638-125">The row identified by the  _pbInstanceKey_ parameter does not exist.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="43638-126">Замечания</span><span class="sxs-lookup"><span data-stu-id="43638-126">Remarks</span></span>

<span data-ttu-id="43638-127">Метод **IMAPITable::ExpandRow** разворачивает свернутые категорию, добавление конечных или нижнем уровне заголовка строки, относящихся к категории, которую требуется в табличном представлении.</span><span class="sxs-lookup"><span data-stu-id="43638-127">The **IMAPITable::ExpandRow** method expands a collapsed table category, adding the leaf or lower-level heading rows that belong to the category to the table view.</span></span> <span data-ttu-id="43638-128">Максимальное число строк, возвращаемых с помощью параметра _lppRows_ можно указать с помощью параметра _ulRowCount_ .</span><span class="sxs-lookup"><span data-stu-id="43638-128">A limit to the number of rows to be returned in the  _lppRows_ parameter can be specified in the  _ulRowCount_ parameter.</span></span> <span data-ttu-id="43638-129">Если одна или несколько строк, возвращенных в наборе строк, на который указывает _lppRows_ _ulRowCount_ задано значение больше нуля, задайте положение закладки, BOOKMARK_CURRENT перемещается в строку сразу после последней строки в строке.</span><span class="sxs-lookup"><span data-stu-id="43638-129">When  _ulRowCount_ is set to a value greater than zero and one or more rows are returned in the row set pointed to by  _lppRows_, the position of the bookmark BOOKMARK_CURRENT is moved to the row immediately following the last row in the row set.</span></span>
  
<span data-ttu-id="43638-130">Когда _ulRowCount_ имеет значение нуль, разрешения на запрос, который нуль конечного или нижнем уровне строки заголовка добавляется по категории или не возвращается ноль строки, так как нет конечного или нижнем уровне заголовков строк в категории, положение BOOKMARK_CURRENT задано значение строки следующие строки, _pbInstanceKey_.</span><span class="sxs-lookup"><span data-stu-id="43638-130">When  _ulRowCount_ is set to zero, requesting that zero leaf or lower-level heading rows be added to the category, or zero rows are returned because there are no leaf or lower-level heading rows in the category, the position of BOOKMARK_CURRENT is set to the row following the row identified by  _pbInstanceKey_.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="43638-131">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="43638-131">Notes to implementers</span></span>

<span data-ttu-id="43638-132">Не создавать уведомления на строки, которые добавлены в представлении таблицы из-за расширения категории.</span><span class="sxs-lookup"><span data-stu-id="43638-132">Do not generate notifications on rows that are added to a table view due to category expansion.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="43638-133">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="43638-133">Notes to callers</span></span>

<span data-ttu-id="43638-134">Количество строк в наборе строк, на который указывает параметр _lppRows_ не может быть равен максимальному числу строк, которые фактически были добавлены к таблице, весь набор конечных или нижнем уровне заголовка строки для категории.</span><span class="sxs-lookup"><span data-stu-id="43638-134">The number of rows in the row set pointed to by the  _lppRows_ parameter might not equal the number of rows that were actually added to the table, the entire set of leaf or lower-level heading rows for the category.</span></span> <span data-ttu-id="43638-135">Например, недостаточно памяти или количество строк в категории, превышающие номер, указанный в параметре _ulRowCount_ могут возникать ошибки.</span><span class="sxs-lookup"><span data-stu-id="43638-135">Errors can occur, such as insufficient memory, or the number of rows in the category exceeding the number specified in  _ulRowCount_ parameter.</span></span> <span data-ttu-id="43638-136">В любом случае BOOKMARK_CURRENT будет размещен в последней строки.</span><span class="sxs-lookup"><span data-stu-id="43638-136">In either case, BOOKMARK_CURRENT will be positioned at the last row returned.</span></span> <span data-ttu-id="43638-137">Чтобы немедленно получить остальных строк в категории, вызовите [IMAPITable::QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="43638-137">To immediately retrieve the rest of the rows in the category, call [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span>
  
<span data-ttu-id="43638-138">Не ожидается в таблице уведомлений при изменении состояния категории.</span><span class="sxs-lookup"><span data-stu-id="43638-138">Do not expect to receive a table notification when a category changes its state.</span></span> <span data-ttu-id="43638-139">Удовлетворяет локальный кэш строк, которые могут быть обновлены с каждым вызовом **ExpandRow** или **CollapseRow** .</span><span class="sxs-lookup"><span data-stu-id="43638-139">You can maintain a local cache of rows that can be updated with every **ExpandRow** or **CollapseRow** call.</span></span> 
  
<span data-ttu-id="43638-140">Дополнительные сведения о таблицах по категориям можно [Сортировка и классификации](sorting-and-categorization.md).</span><span class="sxs-lookup"><span data-stu-id="43638-140">For more information about categorized tables, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="43638-141">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="43638-141">MFCMAPI reference</span></span>

<span data-ttu-id="43638-142">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="43638-142">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="43638-143">**����**</span><span class="sxs-lookup"><span data-stu-id="43638-143">**File**</span></span>|<span data-ttu-id="43638-144">**�������**</span><span class="sxs-lookup"><span data-stu-id="43638-144">**Function**</span></span>|<span data-ttu-id="43638-145">**�����������**</span><span class="sxs-lookup"><span data-stu-id="43638-145">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="43638-146">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="43638-146">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="43638-147">CContentsTableListCtrl::DoExpandCollapse</span><span class="sxs-lookup"><span data-stu-id="43638-147">CContentsTableListCtrl::DoExpandCollapse</span></span>  <br/> |<span data-ttu-id="43638-148">Mfcmapi (en) использует метод **IMAPITable::ExpandRow** разверните категорию свернутые.</span><span class="sxs-lookup"><span data-stu-id="43638-148">MFCMAPI uses the **IMAPITable::ExpandRow** method to expand a collapsed table category.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="43638-149">См. также</span><span class="sxs-lookup"><span data-stu-id="43638-149">See also</span></span>



[<span data-ttu-id="43638-150">IMAPITable::CollapseRow</span><span class="sxs-lookup"><span data-stu-id="43638-150">IMAPITable::CollapseRow</span></span>](imapitable-collapserow.md)
  
[<span data-ttu-id="43638-151">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="43638-151">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="43638-152">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="43638-152">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

