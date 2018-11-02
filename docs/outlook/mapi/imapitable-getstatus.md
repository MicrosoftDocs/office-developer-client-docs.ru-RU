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
ms.openlocfilehash: cda3de1719ec1b7cfca1a9ecdad7bc3b59a8b17d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571152"
---
# <a name="imapitablegetstatus"></a><span data-ttu-id="ffa2a-103">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="ffa2a-103">IMAPITable::GetStatus</span></span>

  
  
<span data-ttu-id="ffa2a-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ffa2a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ffa2a-105">Возвращает состояние в таблице и тип.</span><span class="sxs-lookup"><span data-stu-id="ffa2a-105">Returns the table's status and type.</span></span>
  
```cpp
HRESULT GetStatus(
ULONG FAR * lpulTableStatus,
ULONG FAR * lpulTableType
);
```

## <a name="parameters"></a><span data-ttu-id="ffa2a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ffa2a-106">Parameters</span></span>

 <span data-ttu-id="ffa2a-107">_lpulTableStatus_</span><span class="sxs-lookup"><span data-stu-id="ffa2a-107">_lpulTableStatus_</span></span>
  
> <span data-ttu-id="ffa2a-108">[out] Указатель на значение, указывающее состояние таблицы.</span><span class="sxs-lookup"><span data-stu-id="ffa2a-108">[out] Pointer to a value indicating the status of the table.</span></span> <span data-ttu-id="ffa2a-109">Можно получить одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="ffa2a-109">One of the following values can be returned:</span></span>
    
<span data-ttu-id="ffa2a-110">TBLSTAT_COMPLETE</span><span class="sxs-lookup"><span data-stu-id="ffa2a-110">TBLSTAT_COMPLETE</span></span> 
  
> <span data-ttu-id="ffa2a-111">Нет операций находятся в процессе выполнения.</span><span class="sxs-lookup"><span data-stu-id="ffa2a-111">No operations are in progress.</span></span>
    
<span data-ttu-id="ffa2a-112">TBLSTAT_QCHANGED</span><span class="sxs-lookup"><span data-stu-id="ffa2a-112">TBLSTAT_QCHANGED</span></span> 
  
> <span data-ttu-id="ffa2a-113">Содержимое таблицы expectantly были изменены.</span><span class="sxs-lookup"><span data-stu-id="ffa2a-113">The contents of the table have expectantly changed.</span></span> <span data-ttu-id="ffa2a-114">Это значение состояния для изменения, в результате операций сортировки или ограничения не возвращается.</span><span class="sxs-lookup"><span data-stu-id="ffa2a-114">This status value is not returned for changes that result from sort or restriction operations.</span></span>
    
<span data-ttu-id="ffa2a-115">TBLSTAT_RESTRICT_ERROR</span><span class="sxs-lookup"><span data-stu-id="ffa2a-115">TBLSTAT_RESTRICT_ERROR</span></span> 
  
> <span data-ttu-id="ffa2a-116">Произошла ошибка во время операции [IMAPITable::Restrict](imapitable-restrict.md) .</span><span class="sxs-lookup"><span data-stu-id="ffa2a-116">An error occurred during an [IMAPITable::Restrict](imapitable-restrict.md) operation.</span></span> 
    
<span data-ttu-id="ffa2a-117">TBLSTAT_RESTRICTING</span><span class="sxs-lookup"><span data-stu-id="ffa2a-117">TBLSTAT_RESTRICTING</span></span> 
  
> <span data-ttu-id="ffa2a-118">Операция **IMAPITable::Restrict** — в стадии разработки.</span><span class="sxs-lookup"><span data-stu-id="ffa2a-118">An **IMAPITable::Restrict** operation is in progress.</span></span> 
    
<span data-ttu-id="ffa2a-119">TBLSTAT_SETCOL_ERROR</span><span class="sxs-lookup"><span data-stu-id="ffa2a-119">TBLSTAT_SETCOL_ERROR</span></span> 
  
> <span data-ttu-id="ffa2a-120">Произошла ошибка во время операции [IMAPITable::SetColumns](imapitable-setcolumns.md) .</span><span class="sxs-lookup"><span data-stu-id="ffa2a-120">An error occurred during an [IMAPITable::SetColumns](imapitable-setcolumns.md) operation.</span></span> 
    
<span data-ttu-id="ffa2a-121">TBLSTAT_SETTING_COLS</span><span class="sxs-lookup"><span data-stu-id="ffa2a-121">TBLSTAT_SETTING_COLS</span></span> 
  
> <span data-ttu-id="ffa2a-122">Операция **IMAPITable::SetColumns** — в стадии разработки.</span><span class="sxs-lookup"><span data-stu-id="ffa2a-122">An **IMAPITable::SetColumns** operation is in progress.</span></span> 
    
<span data-ttu-id="ffa2a-123">TBLSTAT_SORT_ERROR</span><span class="sxs-lookup"><span data-stu-id="ffa2a-123">TBLSTAT_SORT_ERROR</span></span> 
  
> <span data-ttu-id="ffa2a-124">Произошла ошибка во время операции [IMAPITable::SortTable](imapitable-sorttable.md) .</span><span class="sxs-lookup"><span data-stu-id="ffa2a-124">An error occurred during an [IMAPITable::SortTable](imapitable-sorttable.md) operation.</span></span> 
    
<span data-ttu-id="ffa2a-125">TBLSTAT_SORTING</span><span class="sxs-lookup"><span data-stu-id="ffa2a-125">TBLSTAT_SORTING</span></span> 
  
> <span data-ttu-id="ffa2a-126">Операция **IMAPITable::SortTable** — в стадии разработки.</span><span class="sxs-lookup"><span data-stu-id="ffa2a-126">An **IMAPITable::SortTable** operation is in progress.</span></span> 
    
 <span data-ttu-id="ffa2a-127">_lpulTableType_</span><span class="sxs-lookup"><span data-stu-id="ffa2a-127">_lpulTableType_</span></span>
  
> <span data-ttu-id="ffa2a-128">[out] Указатель на значение, которое указывает тип таблицы.</span><span class="sxs-lookup"><span data-stu-id="ffa2a-128">[out] Pointer to a value that indicates the table's type.</span></span> <span data-ttu-id="ffa2a-129">Можно получить одно из следующих типов три таблицы:</span><span class="sxs-lookup"><span data-stu-id="ffa2a-129">One of the following three table types can be returned:</span></span>
    
<span data-ttu-id="ffa2a-130">TBLTYPE_DYNAMIC</span><span class="sxs-lookup"><span data-stu-id="ffa2a-130">TBLTYPE_DYNAMIC</span></span> 
  
> <span data-ttu-id="ffa2a-131">Содержимое таблицы динамических; строки и столбцы можно изменить при изменении базовых данных.</span><span class="sxs-lookup"><span data-stu-id="ffa2a-131">The table's contents are dynamic; the rows and column values can change as the underlying data changes.</span></span>
    
<span data-ttu-id="ffa2a-132">TBLTYPE_KEYSET</span><span class="sxs-lookup"><span data-stu-id="ffa2a-132">TBLTYPE_KEYSET</span></span> 
  
> <span data-ttu-id="ffa2a-133">Исправленные строки в таблице, но значения столбцов в следующих строках динамических и можно изменить при изменении базовых данных.</span><span class="sxs-lookup"><span data-stu-id="ffa2a-133">The rows within the table are fixed, but the values of the columns within these rows are dynamic and can change as the underlying data changes.</span></span>
    
<span data-ttu-id="ffa2a-134">TBLTYPE_SNAPSHOT</span><span class="sxs-lookup"><span data-stu-id="ffa2a-134">TBLTYPE_SNAPSHOT</span></span> 
  
> <span data-ttu-id="ffa2a-135">В таблице является статическим, и его содержимое не изменяются при изменении базовых данных.</span><span class="sxs-lookup"><span data-stu-id="ffa2a-135">The table is static, and its contents do not change when the underlying data changes.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ffa2a-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ffa2a-136">Return value</span></span>

<span data-ttu-id="ffa2a-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="ffa2a-137">S_OK</span></span> 
  
> <span data-ttu-id="ffa2a-138">Состояние таблицы успешно возвращен.</span><span class="sxs-lookup"><span data-stu-id="ffa2a-138">The table's status was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ffa2a-139">Примечания</span><span class="sxs-lookup"><span data-stu-id="ffa2a-139">Remarks</span></span>

<span data-ttu-id="ffa2a-140">Метод **IMAPTable::GetStatus** получает сведения о типе и текущее состояние таблицы.</span><span class="sxs-lookup"><span data-stu-id="ffa2a-140">The **IMAPTable::GetStatus** method retrieves information about a table's type and current status.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ffa2a-141">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="ffa2a-141">Notes to callers</span></span>

<span data-ttu-id="ffa2a-142">Совместно с тремя другие методы **IMAPITable** **GetStatus** можно использовать для отслеживания состояния выполнения этих операций и определить влияние на таблицу.</span><span class="sxs-lookup"><span data-stu-id="ffa2a-142">You can use **GetStatus** in conjunction with three other **IMAPITable** methods to monitor the status of those operations and determine the effect on the table.</span></span> <span data-ttu-id="ffa2a-143">Вызовите **GetStatus** после внесения одного из следующих **IMAPITable** вызовов:</span><span class="sxs-lookup"><span data-stu-id="ffa2a-143">Call **GetStatus** after making one of the following **IMAPITable** calls:</span></span> 
  
- <span data-ttu-id="ffa2a-144">Чтобы задать ограничение [IMAPITable::Restrict](imapitable-restrict.md) .</span><span class="sxs-lookup"><span data-stu-id="ffa2a-144">[IMAPITable::Restrict](imapitable-restrict.md) to set a restriction.</span></span> 
    
- <span data-ttu-id="ffa2a-145">[IMAPITable::SortTable](imapitable-sorttable.md) , чтобы установить порядок сортировки.</span><span class="sxs-lookup"><span data-stu-id="ffa2a-145">[IMAPITable::SortTable](imapitable-sorttable.md) to establish a sort order.</span></span> 
    
- <span data-ttu-id="ffa2a-146">[IMAPITable::SetColumns](imapitable-setcolumns.md) для определения набора столбцов.</span><span class="sxs-lookup"><span data-stu-id="ffa2a-146">[IMAPITable::SetColumns](imapitable-setcolumns.md) to define a column set.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="ffa2a-147">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ffa2a-147">MFCMAPI reference</span></span>

<span data-ttu-id="ffa2a-148">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="ffa2a-148">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ffa2a-149">**Файл**</span><span class="sxs-lookup"><span data-stu-id="ffa2a-149">**File**</span></span>|<span data-ttu-id="ffa2a-150">**Функция**</span><span class="sxs-lookup"><span data-stu-id="ffa2a-150">**Function**</span></span>|<span data-ttu-id="ffa2a-151">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="ffa2a-151">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ffa2a-152">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="ffa2a-152">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="ffa2a-153">CContentsTableListCtrl::GetStatus</span><span class="sxs-lookup"><span data-stu-id="ffa2a-153">CContentsTableListCtrl::GetStatus</span></span>  <br/> |<span data-ttu-id="ffa2a-154">Mfcmapi (en) использует метод **IMAPITable::GetStatus** для отчет о состоянии таблицы.</span><span class="sxs-lookup"><span data-stu-id="ffa2a-154">MFCMAPI uses the **IMAPITable::GetStatus** method to report the status of a table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ffa2a-155">См. также</span><span class="sxs-lookup"><span data-stu-id="ffa2a-155">See also</span></span>



[<span data-ttu-id="ffa2a-156">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="ffa2a-156">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
  
[<span data-ttu-id="ffa2a-157">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="ffa2a-157">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="ffa2a-158">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="ffa2a-158">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="ffa2a-159">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ffa2a-159">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="ffa2a-160">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="ffa2a-160">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

