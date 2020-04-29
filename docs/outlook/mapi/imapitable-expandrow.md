---
title: имапитабликспандров
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
# <a name="imapitableexpandrow"></a><span data-ttu-id="375a4-103">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="375a4-103">IMAPITable::ExpandRow</span></span>

  
  
<span data-ttu-id="375a4-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="375a4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="375a4-105">Расширяет категорию свернутой таблицы, добавляя конечные или нижние строки заголовков, принадлежащих к категории, в представление таблицы.</span><span class="sxs-lookup"><span data-stu-id="375a4-105">Expands a collapsed table category, adding the leaf or lower-level heading rows belonging to the category to the table view.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="375a4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="375a4-106">Parameters</span></span>

 <span data-ttu-id="375a4-107">_кбинстанцекэй_</span><span class="sxs-lookup"><span data-stu-id="375a4-107">_cbInstanceKey_</span></span>
  
> <span data-ttu-id="375a4-108">возврата Количество байтов в свойстве PR_INSTANCE_KEY, на которое указывает параметр _пбинстанцекэй_ .</span><span class="sxs-lookup"><span data-stu-id="375a4-108">[in] The count of bytes in the PR_INSTANCE_KEY property pointed to by the  _pbInstanceKey_ parameter.</span></span> 
    
 <span data-ttu-id="375a4-109">_пбинстанцекэй_</span><span class="sxs-lookup"><span data-stu-id="375a4-109">_pbInstanceKey_</span></span>
  
> <span data-ttu-id="375a4-110">возврата Указатель на свойство **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), которое определяет строку заголовка для категории.</span><span class="sxs-lookup"><span data-stu-id="375a4-110">[in] A pointer to the **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property that identifies the heading row for the category.</span></span> 
    
 <span data-ttu-id="375a4-111">_улровкаунт_</span><span class="sxs-lookup"><span data-stu-id="375a4-111">_ulRowCount_</span></span>
  
> <span data-ttu-id="375a4-112">возврата Максимальное число строк, возвращаемых в параметре _лппровс_ .</span><span class="sxs-lookup"><span data-stu-id="375a4-112">[in] The maximum number of rows to return in the  _lppRows_ parameter.</span></span> 
    
 <span data-ttu-id="375a4-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="375a4-113">_ulFlags_</span></span>
  
> <span data-ttu-id="375a4-114">Резервирования должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="375a4-114">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="375a4-115">_лппровс_</span><span class="sxs-lookup"><span data-stu-id="375a4-115">_lppRows_</span></span>
  
> <span data-ttu-id="375a4-116">вышли Указатель на структуру [SRowSet](srowset.md) , получающую первые (вплоть до _улровкаунт_) строк, которые были вставлены в представление таблицы в результате расширения.</span><span class="sxs-lookup"><span data-stu-id="375a4-116">[out] A pointer to an [SRowSet](srowset.md) structure receiving the first (up to  _ulRowCount_) rows that have been inserted into the table view as a result of the expansion.</span></span> <span data-ttu-id="375a4-117">Эти строки вставляются после строки заголовков, определяемой параметром _пбинстанцекэй_ .</span><span class="sxs-lookup"><span data-stu-id="375a4-117">These rows are inserted after the heading row identified by the  _pbInstanceKey_ parameter.</span></span> <span data-ttu-id="375a4-118">Параметр _лппровс_ может иметь значение null, если параметр _улровкаунт_ равен нулю.</span><span class="sxs-lookup"><span data-stu-id="375a4-118">The  _lppRows_ parameter can be NULL if the  _ulRowCount_ parameter is zero.</span></span> 
    
 <span data-ttu-id="375a4-119">_лпулмореровс_</span><span class="sxs-lookup"><span data-stu-id="375a4-119">_lpulMoreRows_</span></span>
  
> <span data-ttu-id="375a4-120">вышли Указатель на общее число строк, добавленных в представление таблицы.</span><span class="sxs-lookup"><span data-stu-id="375a4-120">[out] A pointer to the total number of rows that were added to the table view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="375a4-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="375a4-121">Return value</span></span>

<span data-ttu-id="375a4-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="375a4-122">S_OK</span></span> 
  
> <span data-ttu-id="375a4-123">Категория успешно развернута.</span><span class="sxs-lookup"><span data-stu-id="375a4-123">The category was expanded successfully.</span></span>
    
<span data-ttu-id="375a4-124">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="375a4-124">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="375a4-125">Строка, указанная с помощью параметра _пбинстанцекэй_ , не существует.</span><span class="sxs-lookup"><span data-stu-id="375a4-125">The row identified by the  _pbInstanceKey_ parameter does not exist.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="375a4-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="375a4-126">Remarks</span></span>

<span data-ttu-id="375a4-127">Метод **IMAPITable:: експандров** расширяет категорию свернутой таблицы, добавляя конечные или нижние строки заголовков, принадлежащие к категории, в представление таблицы.</span><span class="sxs-lookup"><span data-stu-id="375a4-127">The **IMAPITable::ExpandRow** method expands a collapsed table category, adding the leaf or lower-level heading rows that belong to the category to the table view.</span></span> <span data-ttu-id="375a4-128">В параметре _улровкаунт_ можно указать только число строк, возвращаемых в параметре _лппровс_ .</span><span class="sxs-lookup"><span data-stu-id="375a4-128">A limit to the number of rows to be returned in the  _lppRows_ parameter can be specified in the  _ulRowCount_ parameter.</span></span> <span data-ttu-id="375a4-129">Если для _улровкаунт_ задано значение больше нуля и одна или несколько строк возвращаются в наборе строк, на который указывает _лппровс_, то положение закладки BOOKMARK_CURRENT перемещается в строку сразу после последней строки в наборе строк.</span><span class="sxs-lookup"><span data-stu-id="375a4-129">When  _ulRowCount_ is set to a value greater than zero and one or more rows are returned in the row set pointed to by  _lppRows_, the position of the bookmark BOOKMARK_CURRENT is moved to the row immediately following the last row in the row set.</span></span>
  
<span data-ttu-id="375a4-130">Если для параметра _улровкаунт_ задано значение 0, в категорию добавляются строки заголовков из нуля или более низкого уровня, так как в категории отсутствуют строки заголовков конечных или нижних уровней, для позиции BOOKMARK_CURRENT задается строка, указанная с помощью _пбинстанцекэй_.</span><span class="sxs-lookup"><span data-stu-id="375a4-130">When  _ulRowCount_ is set to zero, requesting that zero leaf or lower-level heading rows be added to the category, or zero rows are returned because there are no leaf or lower-level heading rows in the category, the position of BOOKMARK_CURRENT is set to the row following the row identified by  _pbInstanceKey_.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="375a4-131">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="375a4-131">Notes to implementers</span></span>

<span data-ttu-id="375a4-132">Не создавайте уведомления для строк, которые добавляются в табличное представление из-за расширения категории.</span><span class="sxs-lookup"><span data-stu-id="375a4-132">Do not generate notifications on rows that are added to a table view due to category expansion.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="375a4-133">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="375a4-133">Notes to callers</span></span>

<span data-ttu-id="375a4-134">Количество строк в наборе строк, на которое указывает параметр _лппровс_ , может не равняться количеству строк, которые были в действительности добавлены в таблицу, а также ко всему набору заголовков конечных или нижних уровней для категории.</span><span class="sxs-lookup"><span data-stu-id="375a4-134">The number of rows in the row set pointed to by the  _lppRows_ parameter might not equal the number of rows that were actually added to the table, the entire set of leaf or lower-level heading rows for the category.</span></span> <span data-ttu-id="375a4-135">Могут возникать ошибки, например недостаток памяти или количество строк в категории, превышающее число, указанное в параметре _улровкаунт_ .</span><span class="sxs-lookup"><span data-stu-id="375a4-135">Errors can occur, such as insufficient memory, or the number of rows in the category exceeding the number specified in  _ulRowCount_ parameter.</span></span> <span data-ttu-id="375a4-136">В обоих случаях BOOKMARK_CURRENT будет размещена в последней возвращенной строке.</span><span class="sxs-lookup"><span data-stu-id="375a4-136">In either case, BOOKMARK_CURRENT will be positioned at the last row returned.</span></span> <span data-ttu-id="375a4-137">Чтобы немедленно извлечь остальные строки в категории, вызовите команду [IMAPITable:: QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="375a4-137">To immediately retrieve the rest of the rows in the category, call [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span>
  
<span data-ttu-id="375a4-138">Не ожидать получения табличного уведомления при изменении состояния категории.</span><span class="sxs-lookup"><span data-stu-id="375a4-138">Do not expect to receive a table notification when a category changes its state.</span></span> <span data-ttu-id="375a4-139">Вы можете поддерживать локальный кэш строк, которые можно обновлять при каждом вызове **експандров** или **коллапсеров** .</span><span class="sxs-lookup"><span data-stu-id="375a4-139">You can maintain a local cache of rows that can be updated with every **ExpandRow** or **CollapseRow** call.</span></span> 
  
<span data-ttu-id="375a4-140">Для получения дополнительных сведений об классифицированных таблицах, ознакомьтесь со статьей [Сортировка и категоризация](sorting-and-categorization.md).</span><span class="sxs-lookup"><span data-stu-id="375a4-140">For more information about categorized tables, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="375a4-141">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="375a4-141">MFCMAPI reference</span></span>

<span data-ttu-id="375a4-142">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="375a4-142">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="375a4-143">**Файл**</span><span class="sxs-lookup"><span data-stu-id="375a4-143">**File**</span></span>|<span data-ttu-id="375a4-144">**Функция**</span><span class="sxs-lookup"><span data-stu-id="375a4-144">**Function**</span></span>|<span data-ttu-id="375a4-145">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="375a4-145">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="375a4-146">Контентстаблелистктрл. cpp</span><span class="sxs-lookup"><span data-stu-id="375a4-146">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="375a4-147">Кконтентстаблелистктрл::D Оекспандколлапсе</span><span class="sxs-lookup"><span data-stu-id="375a4-147">CContentsTableListCtrl::DoExpandCollapse</span></span>  <br/> |<span data-ttu-id="375a4-148">MFCMAPI использует метод **IMAPITable:: експандров** , чтобы развернуть категорию свернутой таблицы.</span><span class="sxs-lookup"><span data-stu-id="375a4-148">MFCMAPI uses the **IMAPITable::ExpandRow** method to expand a collapsed table category.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="375a4-149">См. также</span><span class="sxs-lookup"><span data-stu-id="375a4-149">See also</span></span>



[<span data-ttu-id="375a4-150">IMAPITable::CollapseRow</span><span class="sxs-lookup"><span data-stu-id="375a4-150">IMAPITable::CollapseRow</span></span>](imapitable-collapserow.md)
  
[<span data-ttu-id="375a4-151">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="375a4-151">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="375a4-152">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="375a4-152">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

