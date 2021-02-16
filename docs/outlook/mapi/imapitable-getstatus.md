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
# <a name="imapitablegetstatus"></a><span data-ttu-id="0dcd0-103">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="0dcd0-103">IMAPITable::GetStatus</span></span>

  
  
<span data-ttu-id="0dcd0-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0dcd0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0dcd0-105">Возвращает состояние и тип таблицы.</span><span class="sxs-lookup"><span data-stu-id="0dcd0-105">Returns the table's status and type.</span></span>
  
```cpp
HRESULT GetStatus(
ULONG FAR * lpulTableStatus,
ULONG FAR * lpulTableType
);
```

## <a name="parameters"></a><span data-ttu-id="0dcd0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0dcd0-106">Parameters</span></span>

 <span data-ttu-id="0dcd0-107">_lpulTableStatus_</span><span class="sxs-lookup"><span data-stu-id="0dcd0-107">_lpulTableStatus_</span></span>
  
> <span data-ttu-id="0dcd0-108">[out] Указатель на значение, указывающее состояние таблицы.</span><span class="sxs-lookup"><span data-stu-id="0dcd0-108">[out] Pointer to a value indicating the status of the table.</span></span> <span data-ttu-id="0dcd0-109">Может быть возвращено одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="0dcd0-109">One of the following values can be returned:</span></span>
    
<span data-ttu-id="0dcd0-110">TBLSTAT_COMPLETE</span><span class="sxs-lookup"><span data-stu-id="0dcd0-110">TBLSTAT_COMPLETE</span></span> 
  
> <span data-ttu-id="0dcd0-111">Операции не находятся в процессе выполнения.</span><span class="sxs-lookup"><span data-stu-id="0dcd0-111">No operations are in progress.</span></span>
    
<span data-ttu-id="0dcd0-112">TBLSTAT_QCHANGED</span><span class="sxs-lookup"><span data-stu-id="0dcd0-112">TBLSTAT_QCHANGED</span></span> 
  
> <span data-ttu-id="0dcd0-113">Содержимое таблицы было значительно изменено.</span><span class="sxs-lookup"><span data-stu-id="0dcd0-113">The contents of the table have expectantly changed.</span></span> <span data-ttu-id="0dcd0-114">Это значение состояния не возвращается для изменений, которые являются результатом операций сортировки или ограничений.</span><span class="sxs-lookup"><span data-stu-id="0dcd0-114">This status value is not returned for changes that result from sort or restriction operations.</span></span>
    
<span data-ttu-id="0dcd0-115">TBLSTAT_RESTRICT_ERROR</span><span class="sxs-lookup"><span data-stu-id="0dcd0-115">TBLSTAT_RESTRICT_ERROR</span></span> 
  
> <span data-ttu-id="0dcd0-116">Во время операции [IMAPITable::Restrict произошла](imapitable-restrict.md) ошибка.</span><span class="sxs-lookup"><span data-stu-id="0dcd0-116">An error occurred during an [IMAPITable::Restrict](imapitable-restrict.md) operation.</span></span> 
    
<span data-ttu-id="0dcd0-117">TBLSTAT_RESTRICTING</span><span class="sxs-lookup"><span data-stu-id="0dcd0-117">TBLSTAT_RESTRICTING</span></span> 
  
> <span data-ttu-id="0dcd0-118">Идет **операция IMAPITable::Restrict.**</span><span class="sxs-lookup"><span data-stu-id="0dcd0-118">An **IMAPITable::Restrict** operation is in progress.</span></span> 
    
<span data-ttu-id="0dcd0-119">TBLSTAT_SETCOL_ERROR</span><span class="sxs-lookup"><span data-stu-id="0dcd0-119">TBLSTAT_SETCOL_ERROR</span></span> 
  
> <span data-ttu-id="0dcd0-120">Во время операции [IMAPITable::SetColumns произошла](imapitable-setcolumns.md) ошибка.</span><span class="sxs-lookup"><span data-stu-id="0dcd0-120">An error occurred during an [IMAPITable::SetColumns](imapitable-setcolumns.md) operation.</span></span> 
    
<span data-ttu-id="0dcd0-121">TBLSTAT_SETTING_COLS</span><span class="sxs-lookup"><span data-stu-id="0dcd0-121">TBLSTAT_SETTING_COLS</span></span> 
  
> <span data-ttu-id="0dcd0-122">Идет **операция IMAPITable::SetColumns.**</span><span class="sxs-lookup"><span data-stu-id="0dcd0-122">An **IMAPITable::SetColumns** operation is in progress.</span></span> 
    
<span data-ttu-id="0dcd0-123">TBLSTAT_SORT_ERROR</span><span class="sxs-lookup"><span data-stu-id="0dcd0-123">TBLSTAT_SORT_ERROR</span></span> 
  
> <span data-ttu-id="0dcd0-124">Во время операции [IMAPITable::SortTable произошла](imapitable-sorttable.md) ошибка.</span><span class="sxs-lookup"><span data-stu-id="0dcd0-124">An error occurred during an [IMAPITable::SortTable](imapitable-sorttable.md) operation.</span></span> 
    
<span data-ttu-id="0dcd0-125">TBLSTAT_SORTING</span><span class="sxs-lookup"><span data-stu-id="0dcd0-125">TBLSTAT_SORTING</span></span> 
  
> <span data-ttu-id="0dcd0-126">Идет **операция IMAPITable::SortTable.**</span><span class="sxs-lookup"><span data-stu-id="0dcd0-126">An **IMAPITable::SortTable** operation is in progress.</span></span> 
    
 <span data-ttu-id="0dcd0-127">_lpulTableType_</span><span class="sxs-lookup"><span data-stu-id="0dcd0-127">_lpulTableType_</span></span>
  
> <span data-ttu-id="0dcd0-128">[out] Указатель на значение, которое указывает тип таблицы.</span><span class="sxs-lookup"><span data-stu-id="0dcd0-128">[out] Pointer to a value that indicates the table's type.</span></span> <span data-ttu-id="0dcd0-129">Может быть возвращен один из следующих трех типов таблиц:</span><span class="sxs-lookup"><span data-stu-id="0dcd0-129">One of the following three table types can be returned:</span></span>
    
<span data-ttu-id="0dcd0-130">TBLTYPE_DYNAMIC</span><span class="sxs-lookup"><span data-stu-id="0dcd0-130">TBLTYPE_DYNAMIC</span></span> 
  
> <span data-ttu-id="0dcd0-131">Содержимое таблицы является динамическим; значения строк и столбцов могут изменяться по мере изменения данных.</span><span class="sxs-lookup"><span data-stu-id="0dcd0-131">The table's contents are dynamic; the rows and column values can change as the underlying data changes.</span></span>
    
<span data-ttu-id="0dcd0-132">TBLTYPE_KEYSET</span><span class="sxs-lookup"><span data-stu-id="0dcd0-132">TBLTYPE_KEYSET</span></span> 
  
> <span data-ttu-id="0dcd0-133">Строки в таблице являются фиксированными, но значения столбцов в этих строках являются динамическими и могут изменяться по мере изменения данных.</span><span class="sxs-lookup"><span data-stu-id="0dcd0-133">The rows within the table are fixed, but the values of the columns within these rows are dynamic and can change as the underlying data changes.</span></span>
    
<span data-ttu-id="0dcd0-134">TBLTYPE_SNAPSHOT</span><span class="sxs-lookup"><span data-stu-id="0dcd0-134">TBLTYPE_SNAPSHOT</span></span> 
  
> <span data-ttu-id="0dcd0-135">Таблица является статической, и ее содержимое не меняется при изменении данных.</span><span class="sxs-lookup"><span data-stu-id="0dcd0-135">The table is static, and its contents do not change when the underlying data changes.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0dcd0-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0dcd0-136">Return value</span></span>

<span data-ttu-id="0dcd0-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="0dcd0-137">S_OK</span></span> 
  
> <span data-ttu-id="0dcd0-138">Состояние таблицы было успешно возвращено.</span><span class="sxs-lookup"><span data-stu-id="0dcd0-138">The table's status was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0dcd0-139">Примечания</span><span class="sxs-lookup"><span data-stu-id="0dcd0-139">Remarks</span></span>

<span data-ttu-id="0dcd0-140">Метод **IMAPTable::GetStatus** извлекает сведения о типе таблицы и текущем состоянии.</span><span class="sxs-lookup"><span data-stu-id="0dcd0-140">The **IMAPTable::GetStatus** method retrieves information about a table's type and current status.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="0dcd0-141">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="0dcd0-141">Notes to callers</span></span>

<span data-ttu-id="0dcd0-142">**GetStatus** можно использовать в сочетании с тремя другими методами **IMAPITable** для отслеживания состояния этих операций и определения влияния на таблицу.</span><span class="sxs-lookup"><span data-stu-id="0dcd0-142">You can use **GetStatus** in conjunction with three other **IMAPITable** methods to monitor the status of those operations and determine the effect on the table.</span></span> <span data-ttu-id="0dcd0-143">Вызовите **GetStatus** после одного из следующих вызовов **IMAPITable:**</span><span class="sxs-lookup"><span data-stu-id="0dcd0-143">Call **GetStatus** after making one of the following **IMAPITable** calls:</span></span> 
  
- <span data-ttu-id="0dcd0-144">[IMAPITable::Restrict](imapitable-restrict.md) to set a restriction.</span><span class="sxs-lookup"><span data-stu-id="0dcd0-144">[IMAPITable::Restrict](imapitable-restrict.md) to set a restriction.</span></span> 
    
- <span data-ttu-id="0dcd0-145">[IMAPITable::SortTable](imapitable-sorttable.md) для создания порядка сортировки.</span><span class="sxs-lookup"><span data-stu-id="0dcd0-145">[IMAPITable::SortTable](imapitable-sorttable.md) to establish a sort order.</span></span> 
    
- <span data-ttu-id="0dcd0-146">[IMAPITable::SetColumns](imapitable-setcolumns.md) для определения набора столбцов.</span><span class="sxs-lookup"><span data-stu-id="0dcd0-146">[IMAPITable::SetColumns](imapitable-setcolumns.md) to define a column set.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="0dcd0-147">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="0dcd0-147">MFCMAPI reference</span></span>

<span data-ttu-id="0dcd0-148">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="0dcd0-148">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="0dcd0-149">**Файл**</span><span class="sxs-lookup"><span data-stu-id="0dcd0-149">**File**</span></span>|<span data-ttu-id="0dcd0-150">**Функция**</span><span class="sxs-lookup"><span data-stu-id="0dcd0-150">**Function**</span></span>|<span data-ttu-id="0dcd0-151">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="0dcd0-151">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0dcd0-152">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="0dcd0-152">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="0dcd0-153">CContentsTableListCtrl::GetStatus</span><span class="sxs-lookup"><span data-stu-id="0dcd0-153">CContentsTableListCtrl::GetStatus</span></span>  <br/> |<span data-ttu-id="0dcd0-154">MFCMAPI использует метод **IMAPITable::GetStatus** для отчета о состоянии таблицы.</span><span class="sxs-lookup"><span data-stu-id="0dcd0-154">MFCMAPI uses the **IMAPITable::GetStatus** method to report the status of a table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0dcd0-155">См. также</span><span class="sxs-lookup"><span data-stu-id="0dcd0-155">See also</span></span>



[<span data-ttu-id="0dcd0-156">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="0dcd0-156">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
  
[<span data-ttu-id="0dcd0-157">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="0dcd0-157">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="0dcd0-158">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="0dcd0-158">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="0dcd0-159">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0dcd0-159">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="0dcd0-160">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="0dcd0-160">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

