---
title: IMAPITableGetStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.GetStatus
api_type:
- COM
ms.assetid: f114f1fa-bc05-4587-875b-71548c5912ea
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ec305fc872d1bf1718592dabdd230617d50d3f54
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434335"
---
# <a name="imapitablegetstatus"></a><span data-ttu-id="89410-103">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="89410-103">IMAPITable::GetStatus</span></span>

  
  
<span data-ttu-id="89410-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="89410-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="89410-105">Возвращает состояние и тип таблицы.</span><span class="sxs-lookup"><span data-stu-id="89410-105">Returns the table's status and type.</span></span>
  
```cpp
HRESULT GetStatus(
ULONG FAR * lpulTableStatus,
ULONG FAR * lpulTableType
);
```

## <a name="parameters"></a><span data-ttu-id="89410-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="89410-106">Parameters</span></span>

 <span data-ttu-id="89410-107">_lpulTableStatus_</span><span class="sxs-lookup"><span data-stu-id="89410-107">_lpulTableStatus_</span></span>
  
> <span data-ttu-id="89410-108">[вышел] Указатель на значение, указывающее состояние таблицы.</span><span class="sxs-lookup"><span data-stu-id="89410-108">[out] Pointer to a value indicating the status of the table.</span></span> <span data-ttu-id="89410-109">Одно из следующих значений можно вернуть:</span><span class="sxs-lookup"><span data-stu-id="89410-109">One of the following values can be returned:</span></span>
    
<span data-ttu-id="89410-110">TBLSTAT_COMPLETE</span><span class="sxs-lookup"><span data-stu-id="89410-110">TBLSTAT_COMPLETE</span></span> 
  
> <span data-ttu-id="89410-111">Нет операций в процессе.</span><span class="sxs-lookup"><span data-stu-id="89410-111">No operations are in progress.</span></span>
    
<span data-ttu-id="89410-112">TBLSTAT_QCHANGED</span><span class="sxs-lookup"><span data-stu-id="89410-112">TBLSTAT_QCHANGED</span></span> 
  
> <span data-ttu-id="89410-113">Содержимое таблицы значительно изменилось.</span><span class="sxs-lookup"><span data-stu-id="89410-113">The contents of the table have expectantly changed.</span></span> <span data-ttu-id="89410-114">Это значение состояния не возвращается для изменений, которые происходят в результате операций сортировки или ограничения.</span><span class="sxs-lookup"><span data-stu-id="89410-114">This status value is not returned for changes that result from sort or restriction operations.</span></span>
    
<span data-ttu-id="89410-115">TBLSTAT_RESTRICT_ERROR</span><span class="sxs-lookup"><span data-stu-id="89410-115">TBLSTAT_RESTRICT_ERROR</span></span> 
  
> <span data-ttu-id="89410-116">Ошибка произошла во время [операции IMAPITable::Restrict.](imapitable-restrict.md)</span><span class="sxs-lookup"><span data-stu-id="89410-116">An error occurred during an [IMAPITable::Restrict](imapitable-restrict.md) operation.</span></span> 
    
<span data-ttu-id="89410-117">TBLSTAT_RESTRICTING</span><span class="sxs-lookup"><span data-stu-id="89410-117">TBLSTAT_RESTRICTING</span></span> 
  
> <span data-ttu-id="89410-118">Операция **IMAPITable::Restrict** продолжается.</span><span class="sxs-lookup"><span data-stu-id="89410-118">An **IMAPITable::Restrict** operation is in progress.</span></span> 
    
<span data-ttu-id="89410-119">TBLSTAT_SETCOL_ERROR</span><span class="sxs-lookup"><span data-stu-id="89410-119">TBLSTAT_SETCOL_ERROR</span></span> 
  
> <span data-ttu-id="89410-120">Ошибка произошла во время [операции IMAPITable::SetColumns.](imapitable-setcolumns.md)</span><span class="sxs-lookup"><span data-stu-id="89410-120">An error occurred during an [IMAPITable::SetColumns](imapitable-setcolumns.md) operation.</span></span> 
    
<span data-ttu-id="89410-121">TBLSTAT_SETTING_COLS</span><span class="sxs-lookup"><span data-stu-id="89410-121">TBLSTAT_SETTING_COLS</span></span> 
  
> <span data-ttu-id="89410-122">Операция **IMAPITable::SetColumns** продолжается.</span><span class="sxs-lookup"><span data-stu-id="89410-122">An **IMAPITable::SetColumns** operation is in progress.</span></span> 
    
<span data-ttu-id="89410-123">TBLSTAT_SORT_ERROR</span><span class="sxs-lookup"><span data-stu-id="89410-123">TBLSTAT_SORT_ERROR</span></span> 
  
> <span data-ttu-id="89410-124">Ошибка произошла во время [операции IMAPITable::SortTable.](imapitable-sorttable.md)</span><span class="sxs-lookup"><span data-stu-id="89410-124">An error occurred during an [IMAPITable::SortTable](imapitable-sorttable.md) operation.</span></span> 
    
<span data-ttu-id="89410-125">TBLSTAT_SORTING</span><span class="sxs-lookup"><span data-stu-id="89410-125">TBLSTAT_SORTING</span></span> 
  
> <span data-ttu-id="89410-126">Операция **IMAPITable::SortTable** продолжается.</span><span class="sxs-lookup"><span data-stu-id="89410-126">An **IMAPITable::SortTable** operation is in progress.</span></span> 
    
 <span data-ttu-id="89410-127">_lpulTableType_</span><span class="sxs-lookup"><span data-stu-id="89410-127">_lpulTableType_</span></span>
  
> <span data-ttu-id="89410-128">[вышел] Указатель на значение, которое указывает тип таблицы.</span><span class="sxs-lookup"><span data-stu-id="89410-128">[out] Pointer to a value that indicates the table's type.</span></span> <span data-ttu-id="89410-129">Один из следующих трех типов таблицы можно вернуть:</span><span class="sxs-lookup"><span data-stu-id="89410-129">One of the following three table types can be returned:</span></span>
    
<span data-ttu-id="89410-130">TBLTYPE_DYNAMIC</span><span class="sxs-lookup"><span data-stu-id="89410-130">TBLTYPE_DYNAMIC</span></span> 
  
> <span data-ttu-id="89410-131">Содержимое таблицы динамическое; значения строк и столбцов могут изменяться по мере изменения данных.</span><span class="sxs-lookup"><span data-stu-id="89410-131">The table's contents are dynamic; the rows and column values can change as the underlying data changes.</span></span>
    
<span data-ttu-id="89410-132">TBLTYPE_KEYSET</span><span class="sxs-lookup"><span data-stu-id="89410-132">TBLTYPE_KEYSET</span></span> 
  
> <span data-ttu-id="89410-133">Строки в таблице фиксируются, но значения столбцов в этих строках динамически и могут изменяться по мере изменения данных.</span><span class="sxs-lookup"><span data-stu-id="89410-133">The rows within the table are fixed, but the values of the columns within these rows are dynamic and can change as the underlying data changes.</span></span>
    
<span data-ttu-id="89410-134">TBLTYPE_SNAPSHOT</span><span class="sxs-lookup"><span data-stu-id="89410-134">TBLTYPE_SNAPSHOT</span></span> 
  
> <span data-ttu-id="89410-135">Таблица статична, и ее содержимое не меняется при изменении данных.</span><span class="sxs-lookup"><span data-stu-id="89410-135">The table is static, and its contents do not change when the underlying data changes.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="89410-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="89410-136">Return value</span></span>

<span data-ttu-id="89410-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="89410-137">S_OK</span></span> 
  
> <span data-ttu-id="89410-138">Состояние таблицы было успешно возвращено.</span><span class="sxs-lookup"><span data-stu-id="89410-138">The table's status was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="89410-139">Примечания</span><span class="sxs-lookup"><span data-stu-id="89410-139">Remarks</span></span>

<span data-ttu-id="89410-140">Метод **IMAPTable::GetStatus** извлекает сведения о типе таблицы и текущем состоянии.</span><span class="sxs-lookup"><span data-stu-id="89410-140">The **IMAPTable::GetStatus** method retrieves information about a table's type and current status.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="89410-141">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="89410-141">Notes to callers</span></span>

<span data-ttu-id="89410-142">Вы можете использовать **GetStatus** совместно с тремя другими методами **IMAPITable** для мониторинга состояния этих операций и определения эффекта на таблице.</span><span class="sxs-lookup"><span data-stu-id="89410-142">You can use **GetStatus** in conjunction with three other **IMAPITable** methods to monitor the status of those operations and determine the effect on the table.</span></span> <span data-ttu-id="89410-143">Вызов **GetStatus** после одного из следующих вызовов **IMAPITable:**</span><span class="sxs-lookup"><span data-stu-id="89410-143">Call **GetStatus** after making one of the following **IMAPITable** calls:</span></span> 
  
- <span data-ttu-id="89410-144">[IMAPITable:::Restrict](imapitable-restrict.md) to set a restriction.</span><span class="sxs-lookup"><span data-stu-id="89410-144">[IMAPITable::Restrict](imapitable-restrict.md) to set a restriction.</span></span> 
    
- <span data-ttu-id="89410-145">[IMAPITable::SortTable](imapitable-sorttable.md) для создания порядка сортировки.</span><span class="sxs-lookup"><span data-stu-id="89410-145">[IMAPITable::SortTable](imapitable-sorttable.md) to establish a sort order.</span></span> 
    
- <span data-ttu-id="89410-146">[IMAPITable::SetColumns](imapitable-setcolumns.md) для определения набора столбцов.</span><span class="sxs-lookup"><span data-stu-id="89410-146">[IMAPITable::SetColumns](imapitable-setcolumns.md) to define a column set.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="89410-147">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="89410-147">MFCMAPI reference</span></span>

<span data-ttu-id="89410-148">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="89410-148">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="89410-149">**Файл**</span><span class="sxs-lookup"><span data-stu-id="89410-149">**File**</span></span>|<span data-ttu-id="89410-150">**Функция**</span><span class="sxs-lookup"><span data-stu-id="89410-150">**Function**</span></span>|<span data-ttu-id="89410-151">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="89410-151">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="89410-152">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="89410-152">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="89410-153">CContentsTableListCtrl::GetStatus</span><span class="sxs-lookup"><span data-stu-id="89410-153">CContentsTableListCtrl::GetStatus</span></span>  <br/> |<span data-ttu-id="89410-154">MFCMAPI использует **метод IMAPITable::GetStatus** для отчета о состоянии таблицы.</span><span class="sxs-lookup"><span data-stu-id="89410-154">MFCMAPI uses the **IMAPITable::GetStatus** method to report the status of a table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="89410-155">См. также</span><span class="sxs-lookup"><span data-stu-id="89410-155">See also</span></span>



[<span data-ttu-id="89410-156">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="89410-156">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
  
[<span data-ttu-id="89410-157">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="89410-157">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="89410-158">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="89410-158">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="89410-159">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="89410-159">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="89410-160">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="89410-160">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

