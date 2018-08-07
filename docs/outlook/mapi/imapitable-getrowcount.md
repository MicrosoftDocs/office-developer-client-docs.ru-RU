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
ms.openlocfilehash: a591a49c1cb0ec936d09d59b4632d15e4842dd2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809222"
---
# <a name="imapitablegetrowcount"></a><span data-ttu-id="7a1b9-103">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="7a1b9-103">IMAPITable::GetRowCount</span></span>

  
  
<span data-ttu-id="7a1b9-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7a1b9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7a1b9-105">Возвращает общее число строк в таблице.</span><span class="sxs-lookup"><span data-stu-id="7a1b9-105">Returns the total number of rows in the table.</span></span> 
  
```cpp
HRESULT GetRowCount(
ULONG ulFlags,
ULONG FAR * lpulCount
);
```

## <a name="parameters"></a><span data-ttu-id="7a1b9-106">���������</span><span class="sxs-lookup"><span data-stu-id="7a1b9-106">Parameters</span></span>

 <span data-ttu-id="7a1b9-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7a1b9-107">_ulFlags_</span></span>
  
> <span data-ttu-id="7a1b9-108">Зарезервировано; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="7a1b9-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="7a1b9-109">_lpulCount_</span><span class="sxs-lookup"><span data-stu-id="7a1b9-109">_lpulCount_</span></span>
  
> <span data-ttu-id="7a1b9-110">[out] Указатель на число строк в таблице.</span><span class="sxs-lookup"><span data-stu-id="7a1b9-110">[out] Pointer to the number of rows in the table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7a1b9-111">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="7a1b9-111">Return value</span></span>

<span data-ttu-id="7a1b9-112">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="7a1b9-112">S_OK</span></span> 
  
> <span data-ttu-id="7a1b9-113">Число строк успешно возвращен.</span><span class="sxs-lookup"><span data-stu-id="7a1b9-113">The row count was successfully returned.</span></span>
    
<span data-ttu-id="7a1b9-114">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="7a1b9-114">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="7a1b9-115">В, не позволяющей операцию извлечения строки count запуск выполняется другой операции.</span><span class="sxs-lookup"><span data-stu-id="7a1b9-115">Another operation is in progress that prevents the row count retrieval operation from starting.</span></span> <span data-ttu-id="7a1b9-116">В процессе выполнения операции должны выполнить либо должна быть остановлена.</span><span class="sxs-lookup"><span data-stu-id="7a1b9-116">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="7a1b9-117">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="7a1b9-117">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="7a1b9-118">Таблицы не удается определить число строк.</span><span class="sxs-lookup"><span data-stu-id="7a1b9-118">The table cannot calculate the number of rows.</span></span>
    
<span data-ttu-id="7a1b9-119">MAPI_W_APPROX_COUNT</span><span class="sxs-lookup"><span data-stu-id="7a1b9-119">MAPI_W_APPROX_COUNT</span></span> 
  
> <span data-ttu-id="7a1b9-120">Вызов завершился успешно, но число приблизительно, например строк был возвращен из-за количество точное строк не может быть определена возможно из-за ограничений памяти.</span><span class="sxs-lookup"><span data-stu-id="7a1b9-120">The call succeeded, but an approximate row count was returned because the exact row count could not be determined possibly due to memory constraints.</span></span> <span data-ttu-id="7a1b9-121">Чтобы проверить это предупреждение, используйте **HR_FAILED** макрос.</span><span class="sxs-lookup"><span data-stu-id="7a1b9-121">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="7a1b9-122">В разделе [Использование макросов для обработки ошибок](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="7a1b9-122">See [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7a1b9-123">Замечания</span><span class="sxs-lookup"><span data-stu-id="7a1b9-123">Remarks</span></span>

<span data-ttu-id="7a1b9-124">Метод **IMAPITable::GetRowCount** возвращает общее число строк в таблице.</span><span class="sxs-lookup"><span data-stu-id="7a1b9-124">The **IMAPITable::GetRowCount** method retrieves the total number of rows in a table.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="7a1b9-125">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="7a1b9-125">Notes to implementers</span></span>

<span data-ttu-id="7a1b9-126">Если не удается определить число точное строк таблицы, возвращаемое MAPI_W_APPROX_COUNT и приблизительно, например строку счетчик содержимое параметра _lpulCount_ .</span><span class="sxs-lookup"><span data-stu-id="7a1b9-126">If you cannot determine the table's exact row count, return MAPI_W_APPROX_COUNT and an approximate row count in the contents of the  _lpulCount_ parameter.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="7a1b9-127">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="7a1b9-127">Notes to callers</span></span>

<span data-ttu-id="7a1b9-128">Использование **GetRowCount** , чтобы узнать, сколько строк таблицы содержит перед вызовом метода [IMAPITable::QueryRows](imapitable-queryrows.md) для извлечения данных.</span><span class="sxs-lookup"><span data-stu-id="7a1b9-128">Use **GetRowCount** to find out how many rows a table holds before making a call to the [IMAPITable::QueryRows](imapitable-queryrows.md) method to retrieve the data.</span></span> <span data-ttu-id="7a1b9-129">При наличии менее 20 строк в таблице, безопасно для вызова **QueryPosition** для получения всей таблицы.</span><span class="sxs-lookup"><span data-stu-id="7a1b9-129">If there are less than twenty rows in the table, it is safe to call **QueryPosition** to retrieve the whole table.</span></span> <span data-ttu-id="7a1b9-130">При наличии более чем 20 строк в таблице, можно сделать несколько вызовов **QueryPosition** и ограничить число строк, полученные на каждого вызова.</span><span class="sxs-lookup"><span data-stu-id="7a1b9-130">If there are more than twenty rows in the table, consider making multiple calls to **QueryPosition** and limit the number of rows retrieved in each call.</span></span> 
  
<span data-ttu-id="7a1b9-131">Некоторые таблицы не поддерживают **GetRowCount** и вернуть MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="7a1b9-131">Some tables do not support **GetRowCount** and return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="7a1b9-132">Если **GetRowCount** не поддерживается, вместо возможно для вызова [IMAPITable::QueryPosition](imapitable-queryposition.md).</span><span class="sxs-lookup"><span data-stu-id="7a1b9-132">If **GetRowCount** is not supported, an alternative might be to call [IMAPITable::QueryPosition](imapitable-queryposition.md).</span></span> <span data-ttu-id="7a1b9-133">С результатами из **QueryPosition**можно определить связь между текущей строки и последней строки.</span><span class="sxs-lookup"><span data-stu-id="7a1b9-133">With the results from **QueryPosition**, you can determine the relationship between the current row and last row.</span></span> 
  
<span data-ttu-id="7a1b9-134">При **GetRowCount** возвращает MAPI_E_BUSY, так как они временно не удалось получить число строк, вызовите метод [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) .</span><span class="sxs-lookup"><span data-stu-id="7a1b9-134">When **GetRowCount** returns MAPI_E_BUSY because it is temporarily unable to retrieve a row count, call the [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) method.</span></span> <span data-ttu-id="7a1b9-135">При возврате **WaitForCompletion** повторите вызов **GetRowCount**.</span><span class="sxs-lookup"><span data-stu-id="7a1b9-135">When **WaitForCompletion** returns, retry the call to **GetRowCount**.</span></span> <span data-ttu-id="7a1b9-136">Другим способом для определения, является ли в процессе выполнения асинхронной операции является можно вызвать метод [IMAPITable::GetStatus](imapitable-getstatus.md) , а также просматривать содержимое параметра _lpulTableState_ .</span><span class="sxs-lookup"><span data-stu-id="7a1b9-136">Another way to detect whether an asynchronous operation is in progress is to call the [IMAPITable::GetStatus](imapitable-getstatus.md) method and check the contents of the  _lpulTableState_ parameter.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="7a1b9-137">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="7a1b9-137">MFCMAPI reference</span></span>

<span data-ttu-id="7a1b9-138">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="7a1b9-138">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="7a1b9-139">**����**</span><span class="sxs-lookup"><span data-stu-id="7a1b9-139">**File**</span></span>|<span data-ttu-id="7a1b9-140">**�������**</span><span class="sxs-lookup"><span data-stu-id="7a1b9-140">**Function**</span></span>|<span data-ttu-id="7a1b9-141">**�����������**</span><span class="sxs-lookup"><span data-stu-id="7a1b9-141">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7a1b9-142">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="7a1b9-142">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="7a1b9-143">CopyFolderContents</span><span class="sxs-lookup"><span data-stu-id="7a1b9-143">CopyFolderContents</span></span>  <br/> |<span data-ttu-id="7a1b9-144">Mfcmapi (en) использует метод **IMAPITable::GetRowCount** , чтобы определить, сколько строк в таблице источника, можно выделить память для выполнения копирования.</span><span class="sxs-lookup"><span data-stu-id="7a1b9-144">MFCMAPI uses the **IMAPITable::GetRowCount** method to determine how many rows are in the source table so memory can be allocated to perform the copy.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7a1b9-145">См. также</span><span class="sxs-lookup"><span data-stu-id="7a1b9-145">See also</span></span>



[<span data-ttu-id="7a1b9-146">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="7a1b9-146">IMAPITable::GetStatus</span></span>](imapitable-getstatus.md)
  
[<span data-ttu-id="7a1b9-147">IMAPITable::QueryPosition</span><span class="sxs-lookup"><span data-stu-id="7a1b9-147">IMAPITable::QueryPosition</span></span>](imapitable-queryposition.md)
  
[<span data-ttu-id="7a1b9-148">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="7a1b9-148">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="7a1b9-149">IMAPITable::WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="7a1b9-149">IMAPITable::WaitForCompletion</span></span>](imapitable-waitforcompletion.md)
  
[<span data-ttu-id="7a1b9-150">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7a1b9-150">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="7a1b9-151">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="7a1b9-151">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

