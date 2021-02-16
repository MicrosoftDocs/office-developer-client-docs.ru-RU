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
# <a name="imapitablegetrowcount"></a><span data-ttu-id="a5336-103">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="a5336-103">IMAPITable::GetRowCount</span></span>

  
  
<span data-ttu-id="a5336-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a5336-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a5336-105">Возвращает общее число строк в таблице.</span><span class="sxs-lookup"><span data-stu-id="a5336-105">Returns the total number of rows in the table.</span></span> 
  
```cpp
HRESULT GetRowCount(
ULONG ulFlags,
ULONG FAR * lpulCount
);
```

## <a name="parameters"></a><span data-ttu-id="a5336-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a5336-106">Parameters</span></span>

 <span data-ttu-id="a5336-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a5336-107">_ulFlags_</span></span>
  
> <span data-ttu-id="a5336-108">Зарезервировано; должно быть нулем.</span><span class="sxs-lookup"><span data-stu-id="a5336-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="a5336-109">_lpulCount_</span><span class="sxs-lookup"><span data-stu-id="a5336-109">_lpulCount_</span></span>
  
> <span data-ttu-id="a5336-110">[out] Указатель на количество строк в таблице.</span><span class="sxs-lookup"><span data-stu-id="a5336-110">[out] Pointer to the number of rows in the table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a5336-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a5336-111">Return value</span></span>

<span data-ttu-id="a5336-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="a5336-112">S_OK</span></span> 
  
> <span data-ttu-id="a5336-113">Количество строк успешно возвращено.</span><span class="sxs-lookup"><span data-stu-id="a5336-113">The row count was successfully returned.</span></span>
    
<span data-ttu-id="a5336-114">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="a5336-114">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="a5336-115">В настоящее время идет другая операция, которая препятствует запуску операции ирисовки подсчета строк.</span><span class="sxs-lookup"><span data-stu-id="a5336-115">Another operation is in progress that prevents the row count retrieval operation from starting.</span></span> <span data-ttu-id="a5336-116">Либо операция должна быть завершена, либо она должна быть остановлена.</span><span class="sxs-lookup"><span data-stu-id="a5336-116">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="a5336-117">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="a5336-117">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="a5336-118">В таблице не удается вычислить количество строк.</span><span class="sxs-lookup"><span data-stu-id="a5336-118">The table cannot calculate the number of rows.</span></span>
    
<span data-ttu-id="a5336-119">MAPI_W_APPROX_COUNT</span><span class="sxs-lookup"><span data-stu-id="a5336-119">MAPI_W_APPROX_COUNT</span></span> 
  
> <span data-ttu-id="a5336-120">Вызов был успешным, но было возвращено приблизительное количество строк, так как точное количество строк не удалось определить, возможно, из-за ограничений памяти.</span><span class="sxs-lookup"><span data-stu-id="a5336-120">The call succeeded, but an approximate row count was returned because the exact row count could not be determined possibly due to memory constraints.</span></span> <span data-ttu-id="a5336-121">Чтобы проверить это предупреждение, используйте **макрос** HR_FAILED.</span><span class="sxs-lookup"><span data-stu-id="a5336-121">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="a5336-122">См. ["Использование макроса для обработки ошибок".](using-macros-for-error-handling.md)</span><span class="sxs-lookup"><span data-stu-id="a5336-122">See [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a5336-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="a5336-123">Remarks</span></span>

<span data-ttu-id="a5336-124">Метод **IMAPITable::GetRowCount** извлекает общее количество строк в таблице.</span><span class="sxs-lookup"><span data-stu-id="a5336-124">The **IMAPITable::GetRowCount** method retrieves the total number of rows in a table.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="a5336-125">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="a5336-125">Notes to implementers</span></span>

<span data-ttu-id="a5336-126">Если точное количество строк таблицы определить не удается, MAPI_W_APPROX_COUNT и приблизительное количество строк в содержимом параметра _lpulCount._</span><span class="sxs-lookup"><span data-stu-id="a5336-126">If you cannot determine the table's exact row count, return MAPI_W_APPROX_COUNT and an approximate row count in the contents of the  _lpulCount_ parameter.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a5336-127">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="a5336-127">Notes to callers</span></span>

<span data-ttu-id="a5336-128">Используйте **Метод GetRowCount,** чтобы узнать, сколько строк содержит таблица перед вызовом метода [IMAPITable::QueryRows](imapitable-queryrows.md) для получения данных.</span><span class="sxs-lookup"><span data-stu-id="a5336-128">Use **GetRowCount** to find out how many rows a table holds before making a call to the [IMAPITable::QueryRows](imapitable-queryrows.md) method to retrieve the data.</span></span> <span data-ttu-id="a5336-129">Если в таблице менее 20 строк, можно вызвать **QueryPosition,** чтобы получить всю таблицу.</span><span class="sxs-lookup"><span data-stu-id="a5336-129">If there are less than twenty rows in the table, it is safe to call **QueryPosition** to retrieve the whole table.</span></span> <span data-ttu-id="a5336-130">Если в таблице более 20 строк, рассмотрите возможность выполнения нескольких вызовов **QueryPosition** и ограничить число строк, полученных в каждом вызове.</span><span class="sxs-lookup"><span data-stu-id="a5336-130">If there are more than twenty rows in the table, consider making multiple calls to **QueryPosition** and limit the number of rows retrieved in each call.</span></span> 
  
<span data-ttu-id="a5336-131">Некоторые таблицы не поддерживают **GetRowCount** и возвращают MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="a5336-131">Some tables do not support **GetRowCount** and return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="a5336-132">Если **GetRowCount** не поддерживается, можно вызвать [IMAPITable::QueryPosition.](imapitable-queryposition.md)</span><span class="sxs-lookup"><span data-stu-id="a5336-132">If **GetRowCount** is not supported, an alternative might be to call [IMAPITable::QueryPosition](imapitable-queryposition.md).</span></span> <span data-ttu-id="a5336-133">С помощью результатов **из QueryPosition** можно определить отношение между текущей строкой и последней строкой.</span><span class="sxs-lookup"><span data-stu-id="a5336-133">With the results from **QueryPosition**, you can determine the relationship between the current row and last row.</span></span> 
  
<span data-ttu-id="a5336-134">Когда **Метод GetRowCount** MAPI_E_BUSY, так как он временно не может получить количество строк, вызовите метод [IMAPITable::WaitForCompletion.](imapitable-waitforcompletion.md)</span><span class="sxs-lookup"><span data-stu-id="a5336-134">When **GetRowCount** returns MAPI_E_BUSY because it is temporarily unable to retrieve a row count, call the [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) method.</span></span> <span data-ttu-id="a5336-135">Когда **waitForCompletion** возвращается, повторить вызов **GetRowCount.**</span><span class="sxs-lookup"><span data-stu-id="a5336-135">When **WaitForCompletion** returns, retry the call to **GetRowCount**.</span></span> <span data-ttu-id="a5336-136">Еще один способ определить, проводится ли асинхронная операция, — вызвать метод [IMAPITable::GetStatus](imapitable-getstatus.md) и проверить содержимое параметра _lpulTableState._</span><span class="sxs-lookup"><span data-stu-id="a5336-136">Another way to detect whether an asynchronous operation is in progress is to call the [IMAPITable::GetStatus](imapitable-getstatus.md) method and check the contents of the  _lpulTableState_ parameter.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a5336-137">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="a5336-137">MFCMAPI reference</span></span>

<span data-ttu-id="a5336-138">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="a5336-138">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a5336-139">**Файл**</span><span class="sxs-lookup"><span data-stu-id="a5336-139">**File**</span></span>|<span data-ttu-id="a5336-140">**Функция**</span><span class="sxs-lookup"><span data-stu-id="a5336-140">**Function**</span></span>|<span data-ttu-id="a5336-141">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="a5336-141">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a5336-142">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="a5336-142">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="a5336-143">CopyFolderContents</span><span class="sxs-lookup"><span data-stu-id="a5336-143">CopyFolderContents</span></span>  <br/> |<span data-ttu-id="a5336-144">MFCMAPI использует метод **IMAPITable::GetRowCount,** чтобы определить количество строк в таблице источника, чтобы можно было выделить память для выполнения копирования.</span><span class="sxs-lookup"><span data-stu-id="a5336-144">MFCMAPI uses the **IMAPITable::GetRowCount** method to determine how many rows are in the source table so memory can be allocated to perform the copy.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a5336-145">См. также</span><span class="sxs-lookup"><span data-stu-id="a5336-145">See also</span></span>



[<span data-ttu-id="a5336-146">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="a5336-146">IMAPITable::GetStatus</span></span>](imapitable-getstatus.md)
  
[<span data-ttu-id="a5336-147">IMAPITable::QueryPosition</span><span class="sxs-lookup"><span data-stu-id="a5336-147">IMAPITable::QueryPosition</span></span>](imapitable-queryposition.md)
  
[<span data-ttu-id="a5336-148">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="a5336-148">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="a5336-149">IMAPITable::WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="a5336-149">IMAPITable::WaitForCompletion</span></span>](imapitable-waitforcompletion.md)
  
[<span data-ttu-id="a5336-150">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a5336-150">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="a5336-151">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="a5336-151">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

