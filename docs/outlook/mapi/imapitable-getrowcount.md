---
title: IMAPITableGetRowCount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.GetRowCount
api_type:
- COM
ms.assetid: 44a12c92-7462-4acf-9520-5d4c2d7f1d47
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b13bf3bdd8392efc42ad189e48dffad8636f0708
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425605"
---
# <a name="imapitablegetrowcount"></a><span data-ttu-id="11bb5-103">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="11bb5-103">IMAPITable::GetRowCount</span></span>

  
  
<span data-ttu-id="11bb5-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="11bb5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="11bb5-105">Возвращает общее количество строк в таблице.</span><span class="sxs-lookup"><span data-stu-id="11bb5-105">Returns the total number of rows in the table.</span></span> 
  
```cpp
HRESULT GetRowCount(
ULONG ulFlags,
ULONG FAR * lpulCount
);
```

## <a name="parameters"></a><span data-ttu-id="11bb5-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="11bb5-106">Parameters</span></span>

 <span data-ttu-id="11bb5-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="11bb5-107">_ulFlags_</span></span>
  
> <span data-ttu-id="11bb5-108">Зарезервировано; должно быть нулевой.</span><span class="sxs-lookup"><span data-stu-id="11bb5-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="11bb5-109">_lpulCount_</span><span class="sxs-lookup"><span data-stu-id="11bb5-109">_lpulCount_</span></span>
  
> <span data-ttu-id="11bb5-110">[вышел] Указатель на количество строк в таблице.</span><span class="sxs-lookup"><span data-stu-id="11bb5-110">[out] Pointer to the number of rows in the table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="11bb5-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="11bb5-111">Return value</span></span>

<span data-ttu-id="11bb5-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="11bb5-112">S_OK</span></span> 
  
> <span data-ttu-id="11bb5-113">Количество строк было успешно возвращено.</span><span class="sxs-lookup"><span data-stu-id="11bb5-113">The row count was successfully returned.</span></span>
    
<span data-ttu-id="11bb5-114">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="11bb5-114">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="11bb5-115">В настоящее время продолжается еще одна операция, которая не позволяет начать операцию по ирисовке подсчета строк.</span><span class="sxs-lookup"><span data-stu-id="11bb5-115">Another operation is in progress that prevents the row count retrieval operation from starting.</span></span> <span data-ttu-id="11bb5-116">Либо операция должна быть разрешена к завершению, либо она должна быть остановлена.</span><span class="sxs-lookup"><span data-stu-id="11bb5-116">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="11bb5-117">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="11bb5-117">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="11bb5-118">Таблица не может рассчитать количество строк.</span><span class="sxs-lookup"><span data-stu-id="11bb5-118">The table cannot calculate the number of rows.</span></span>
    
<span data-ttu-id="11bb5-119">MAPI_W_APPROX_COUNT</span><span class="sxs-lookup"><span data-stu-id="11bb5-119">MAPI_W_APPROX_COUNT</span></span> 
  
> <span data-ttu-id="11bb5-120">Вызов удался, но было возвращено приблизительное число строк, так как точное число строк не удалось определить из-за ограничений памяти.</span><span class="sxs-lookup"><span data-stu-id="11bb5-120">The call succeeded, but an approximate row count was returned because the exact row count could not be determined possibly due to memory constraints.</span></span> <span data-ttu-id="11bb5-121">Чтобы проверить это предупреждение, используйте **HR_FAILED** макрос.</span><span class="sxs-lookup"><span data-stu-id="11bb5-121">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="11bb5-122">См. в руб. Использование [макроса для обработки ошибок.](using-macros-for-error-handling.md)</span><span class="sxs-lookup"><span data-stu-id="11bb5-122">See [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="11bb5-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="11bb5-123">Remarks</span></span>

<span data-ttu-id="11bb5-124">Метод **IMAPITable::GetRowCount** извлекает общее количество строк в таблице.</span><span class="sxs-lookup"><span data-stu-id="11bb5-124">The **IMAPITable::GetRowCount** method retrieves the total number of rows in a table.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="11bb5-125">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="11bb5-125">Notes to implementers</span></span>

<span data-ttu-id="11bb5-126">Если вы не можете определить точное количество строк в таблице, MAPI_W_APPROX_COUNT и приблизительное число строк в содержимом _параметра lpulCount._</span><span class="sxs-lookup"><span data-stu-id="11bb5-126">If you cannot determine the table's exact row count, return MAPI_W_APPROX_COUNT and an approximate row count in the contents of the  _lpulCount_ parameter.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="11bb5-127">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="11bb5-127">Notes to callers</span></span>

<span data-ttu-id="11bb5-128">Чтобы получить данные, используйте **GetRowCount,** чтобы узнать, сколько строк занимает таблица перед вызовом метода [IMAPITable::QueryRows.](imapitable-queryrows.md)</span><span class="sxs-lookup"><span data-stu-id="11bb5-128">Use **GetRowCount** to find out how many rows a table holds before making a call to the [IMAPITable::QueryRows](imapitable-queryrows.md) method to retrieve the data.</span></span> <span data-ttu-id="11bb5-129">Если в таблице менее 20 строк, можно с уверенностью вызвать **QueryPosition,** чтобы получить всю таблицу.</span><span class="sxs-lookup"><span data-stu-id="11bb5-129">If there are less than twenty rows in the table, it is safe to call **QueryPosition** to retrieve the whole table.</span></span> <span data-ttu-id="11bb5-130">Если в таблице более 20 строк, следует сделать несколько вызовов **в QueryPosition** и ограничить количество строк, полученных в каждом вызове.</span><span class="sxs-lookup"><span data-stu-id="11bb5-130">If there are more than twenty rows in the table, consider making multiple calls to **QueryPosition** and limit the number of rows retrieved in each call.</span></span> 
  
<span data-ttu-id="11bb5-131">Некоторые таблицы не поддерживают **GetRowCount** и возвращают MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="11bb5-131">Some tables do not support **GetRowCount** and return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="11bb5-132">Если **GetRowCount** не поддерживается, можно вызвать [IMAPITable::QueryPosition.](imapitable-queryposition.md)</span><span class="sxs-lookup"><span data-stu-id="11bb5-132">If **GetRowCount** is not supported, an alternative might be to call [IMAPITable::QueryPosition](imapitable-queryposition.md).</span></span> <span data-ttu-id="11bb5-133">С помощью результатов **queryPosition** можно определить связь между текущей строкой и последней строкой.</span><span class="sxs-lookup"><span data-stu-id="11bb5-133">With the results from **QueryPosition**, you can determine the relationship between the current row and last row.</span></span> 
  
<span data-ttu-id="11bb5-134">Когда **GetRowCount** возвращает MAPI_E_BUSY, так как она временно не может получить количество строк, позвоните по методу [IMAPITable::WaitForCompletion.](imapitable-waitforcompletion.md)</span><span class="sxs-lookup"><span data-stu-id="11bb5-134">When **GetRowCount** returns MAPI_E_BUSY because it is temporarily unable to retrieve a row count, call the [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) method.</span></span> <span data-ttu-id="11bb5-135">Когда **waitForCompletion** возвращается, повторно вызов **GetRowCount**.</span><span class="sxs-lookup"><span data-stu-id="11bb5-135">When **WaitForCompletion** returns, retry the call to **GetRowCount**.</span></span> <span data-ttu-id="11bb5-136">Другой способ определить, проводится ли асинхронная операция, — вызвать метод [IMAPITable::GetStatus](imapitable-getstatus.md) и проверить содержимое _параметра lpulTableState._</span><span class="sxs-lookup"><span data-stu-id="11bb5-136">Another way to detect whether an asynchronous operation is in progress is to call the [IMAPITable::GetStatus](imapitable-getstatus.md) method and check the contents of the  _lpulTableState_ parameter.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="11bb5-137">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="11bb5-137">MFCMAPI reference</span></span>

<span data-ttu-id="11bb5-138">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="11bb5-138">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="11bb5-139">**Файл**</span><span class="sxs-lookup"><span data-stu-id="11bb5-139">**File**</span></span>|<span data-ttu-id="11bb5-140">**Функция**</span><span class="sxs-lookup"><span data-stu-id="11bb5-140">**Function**</span></span>|<span data-ttu-id="11bb5-141">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="11bb5-141">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="11bb5-142">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="11bb5-142">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="11bb5-143">CopyFolderContents</span><span class="sxs-lookup"><span data-stu-id="11bb5-143">CopyFolderContents</span></span>  <br/> |<span data-ttu-id="11bb5-144">MFCMAPI использует метод **IMAPITable::GetRowCount,** чтобы определить, сколько строк в исходных таблицах, чтобы можно было выделить память для выполнения копии.</span><span class="sxs-lookup"><span data-stu-id="11bb5-144">MFCMAPI uses the **IMAPITable::GetRowCount** method to determine how many rows are in the source table so memory can be allocated to perform the copy.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="11bb5-145">См. также</span><span class="sxs-lookup"><span data-stu-id="11bb5-145">See also</span></span>



[<span data-ttu-id="11bb5-146">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="11bb5-146">IMAPITable::GetStatus</span></span>](imapitable-getstatus.md)
  
[<span data-ttu-id="11bb5-147">IMAPITable::QueryPosition</span><span class="sxs-lookup"><span data-stu-id="11bb5-147">IMAPITable::QueryPosition</span></span>](imapitable-queryposition.md)
  
[<span data-ttu-id="11bb5-148">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="11bb5-148">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="11bb5-149">IMAPITable::WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="11bb5-149">IMAPITable::WaitForCompletion</span></span>](imapitable-waitforcompletion.md)
  
[<span data-ttu-id="11bb5-150">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="11bb5-150">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="11bb5-151">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="11bb5-151">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

