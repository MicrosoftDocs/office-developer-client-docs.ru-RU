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
ms.openlocfilehash: 71178f1a531bd381387e0aa7fbacb02d4431a401
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584326"
---
# <a name="imapitablegetrowcount"></a><span data-ttu-id="9d1b4-103">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="9d1b4-103">IMAPITable::GetRowCount</span></span>

  
  
<span data-ttu-id="9d1b4-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9d1b4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9d1b4-105">Возвращает общее число строк в таблице.</span><span class="sxs-lookup"><span data-stu-id="9d1b4-105">Returns the total number of rows in the table.</span></span> 
  
```cpp
HRESULT GetRowCount(
ULONG ulFlags,
ULONG FAR * lpulCount
);
```

## <a name="parameters"></a><span data-ttu-id="9d1b4-106">���������</span><span class="sxs-lookup"><span data-stu-id="9d1b4-106">Parameters</span></span>

 <span data-ttu-id="9d1b4-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9d1b4-107">_ulFlags_</span></span>
  
> <span data-ttu-id="9d1b4-108">Зарезервировано; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="9d1b4-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="9d1b4-109">_lpulCount_</span><span class="sxs-lookup"><span data-stu-id="9d1b4-109">_lpulCount_</span></span>
  
> <span data-ttu-id="9d1b4-110">[out] Указатель на число строк в таблице.</span><span class="sxs-lookup"><span data-stu-id="9d1b4-110">[out] Pointer to the number of rows in the table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9d1b4-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9d1b4-111">Return value</span></span>

<span data-ttu-id="9d1b4-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="9d1b4-112">S_OK</span></span> 
  
> <span data-ttu-id="9d1b4-113">Число строк успешно возвращен.</span><span class="sxs-lookup"><span data-stu-id="9d1b4-113">The row count was successfully returned.</span></span>
    
<span data-ttu-id="9d1b4-114">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="9d1b4-114">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="9d1b4-115">В, не позволяющей операцию извлечения строки count запуск выполняется другой операции.</span><span class="sxs-lookup"><span data-stu-id="9d1b4-115">Another operation is in progress that prevents the row count retrieval operation from starting.</span></span> <span data-ttu-id="9d1b4-116">В процессе выполнения операции должны выполнить либо должна быть остановлена.</span><span class="sxs-lookup"><span data-stu-id="9d1b4-116">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="9d1b4-117">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="9d1b4-117">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="9d1b4-118">Таблицы не удается определить число строк.</span><span class="sxs-lookup"><span data-stu-id="9d1b4-118">The table cannot calculate the number of rows.</span></span>
    
<span data-ttu-id="9d1b4-119">MAPI_W_APPROX_COUNT</span><span class="sxs-lookup"><span data-stu-id="9d1b4-119">MAPI_W_APPROX_COUNT</span></span> 
  
> <span data-ttu-id="9d1b4-120">Вызов завершился успешно, но число приблизительно, например строк был возвращен из-за количество точное строк не может быть определена возможно из-за ограничений памяти.</span><span class="sxs-lookup"><span data-stu-id="9d1b4-120">The call succeeded, but an approximate row count was returned because the exact row count could not be determined possibly due to memory constraints.</span></span> <span data-ttu-id="9d1b4-121">Чтобы проверить это предупреждение, используйте **HR_FAILED** макрос.</span><span class="sxs-lookup"><span data-stu-id="9d1b4-121">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="9d1b4-122">В разделе [Использование макросов для обработки ошибок](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="9d1b4-122">See [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9d1b4-123">Замечания</span><span class="sxs-lookup"><span data-stu-id="9d1b4-123">Remarks</span></span>

<span data-ttu-id="9d1b4-124">Метод **IMAPITable::GetRowCount** возвращает общее число строк в таблице.</span><span class="sxs-lookup"><span data-stu-id="9d1b4-124">The **IMAPITable::GetRowCount** method retrieves the total number of rows in a table.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="9d1b4-125">Примечания для реализующих</span><span class="sxs-lookup"><span data-stu-id="9d1b4-125">Notes to implementers</span></span>

<span data-ttu-id="9d1b4-126">Если не удается определить число точное строк таблицы, возвращаемое MAPI_W_APPROX_COUNT и приблизительно, например строку счетчик содержимое параметра _lpulCount_ .</span><span class="sxs-lookup"><span data-stu-id="9d1b4-126">If you cannot determine the table's exact row count, return MAPI_W_APPROX_COUNT and an approximate row count in the contents of the  _lpulCount_ parameter.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="9d1b4-127">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="9d1b4-127">Notes to callers</span></span>

<span data-ttu-id="9d1b4-128">Использование **GetRowCount** , чтобы узнать, сколько строк таблицы содержит перед вызовом метода [IMAPITable::QueryRows](imapitable-queryrows.md) для извлечения данных.</span><span class="sxs-lookup"><span data-stu-id="9d1b4-128">Use **GetRowCount** to find out how many rows a table holds before making a call to the [IMAPITable::QueryRows](imapitable-queryrows.md) method to retrieve the data.</span></span> <span data-ttu-id="9d1b4-129">При наличии менее 20 строк в таблице, безопасно для вызова **QueryPosition** для получения всей таблицы.</span><span class="sxs-lookup"><span data-stu-id="9d1b4-129">If there are less than twenty rows in the table, it is safe to call **QueryPosition** to retrieve the whole table.</span></span> <span data-ttu-id="9d1b4-130">При наличии более чем 20 строк в таблице, можно сделать несколько вызовов **QueryPosition** и ограничить число строк, полученные на каждого вызова.</span><span class="sxs-lookup"><span data-stu-id="9d1b4-130">If there are more than twenty rows in the table, consider making multiple calls to **QueryPosition** and limit the number of rows retrieved in each call.</span></span> 
  
<span data-ttu-id="9d1b4-131">Некоторые таблицы не поддерживают **GetRowCount** и вернуть MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="9d1b4-131">Some tables do not support **GetRowCount** and return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="9d1b4-132">Если **GetRowCount** не поддерживается, вместо возможно для вызова [IMAPITable::QueryPosition](imapitable-queryposition.md).</span><span class="sxs-lookup"><span data-stu-id="9d1b4-132">If **GetRowCount** is not supported, an alternative might be to call [IMAPITable::QueryPosition](imapitable-queryposition.md).</span></span> <span data-ttu-id="9d1b4-133">С результатами из **QueryPosition**можно определить связь между текущей строки и последней строки.</span><span class="sxs-lookup"><span data-stu-id="9d1b4-133">With the results from **QueryPosition**, you can determine the relationship between the current row and last row.</span></span> 
  
<span data-ttu-id="9d1b4-134">При **GetRowCount** возвращает MAPI_E_BUSY, так как они временно не удалось получить число строк, вызовите метод [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) .</span><span class="sxs-lookup"><span data-stu-id="9d1b4-134">When **GetRowCount** returns MAPI_E_BUSY because it is temporarily unable to retrieve a row count, call the [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) method.</span></span> <span data-ttu-id="9d1b4-135">При возврате **WaitForCompletion** повторите вызов **GetRowCount**.</span><span class="sxs-lookup"><span data-stu-id="9d1b4-135">When **WaitForCompletion** returns, retry the call to **GetRowCount**.</span></span> <span data-ttu-id="9d1b4-136">Другим способом для определения, является ли в процессе выполнения асинхронной операции является можно вызвать метод [IMAPITable::GetStatus](imapitable-getstatus.md) , а также просматривать содержимое параметра _lpulTableState_ .</span><span class="sxs-lookup"><span data-stu-id="9d1b4-136">Another way to detect whether an asynchronous operation is in progress is to call the [IMAPITable::GetStatus](imapitable-getstatus.md) method and check the contents of the  _lpulTableState_ parameter.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="9d1b4-137">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="9d1b4-137">MFCMAPI reference</span></span>

<span data-ttu-id="9d1b4-138">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="9d1b4-138">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="9d1b4-139">**Файл**</span><span class="sxs-lookup"><span data-stu-id="9d1b4-139">**File**</span></span>|<span data-ttu-id="9d1b4-140">**Функция**</span><span class="sxs-lookup"><span data-stu-id="9d1b4-140">**Function**</span></span>|<span data-ttu-id="9d1b4-141">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="9d1b4-141">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9d1b4-142">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="9d1b4-142">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="9d1b4-143">CopyFolderContents</span><span class="sxs-lookup"><span data-stu-id="9d1b4-143">CopyFolderContents</span></span>  <br/> |<span data-ttu-id="9d1b4-144">Mfcmapi (en) использует метод **IMAPITable::GetRowCount** , чтобы определить, сколько строк в таблице источника, можно выделить память для выполнения копирования.</span><span class="sxs-lookup"><span data-stu-id="9d1b4-144">MFCMAPI uses the **IMAPITable::GetRowCount** method to determine how many rows are in the source table so memory can be allocated to perform the copy.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9d1b4-145">См. также</span><span class="sxs-lookup"><span data-stu-id="9d1b4-145">See also</span></span>



[<span data-ttu-id="9d1b4-146">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="9d1b4-146">IMAPITable::GetStatus</span></span>](imapitable-getstatus.md)
  
[<span data-ttu-id="9d1b4-147">IMAPITable::QueryPosition</span><span class="sxs-lookup"><span data-stu-id="9d1b4-147">IMAPITable::QueryPosition</span></span>](imapitable-queryposition.md)
  
[<span data-ttu-id="9d1b4-148">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="9d1b4-148">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="9d1b4-149">IMAPITable::WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="9d1b4-149">IMAPITable::WaitForCompletion</span></span>](imapitable-waitforcompletion.md)
  
[<span data-ttu-id="9d1b4-150">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9d1b4-150">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="9d1b4-151">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="9d1b4-151">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

