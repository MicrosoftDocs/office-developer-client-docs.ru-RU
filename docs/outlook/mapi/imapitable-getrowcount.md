---
title: Имапитаблежетровкаунт
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
# <a name="imapitablegetrowcount"></a><span data-ttu-id="62cea-103">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="62cea-103">IMAPITable::GetRowCount</span></span>

  
  
<span data-ttu-id="62cea-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="62cea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="62cea-105">Возвращает общее количество строк в таблице.</span><span class="sxs-lookup"><span data-stu-id="62cea-105">Returns the total number of rows in the table.</span></span> 
  
```cpp
HRESULT GetRowCount(
ULONG ulFlags,
ULONG FAR * lpulCount
);
```

## <a name="parameters"></a><span data-ttu-id="62cea-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="62cea-106">Parameters</span></span>

 <span data-ttu-id="62cea-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="62cea-107">_ulFlags_</span></span>
  
> <span data-ttu-id="62cea-108">Резервирования должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="62cea-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="62cea-109">_Лпулкаунт_</span><span class="sxs-lookup"><span data-stu-id="62cea-109">_lpulCount_</span></span>
  
> <span data-ttu-id="62cea-110">вышли Указатель на число строк в таблице.</span><span class="sxs-lookup"><span data-stu-id="62cea-110">[out] Pointer to the number of rows in the table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="62cea-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="62cea-111">Return value</span></span>

<span data-ttu-id="62cea-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="62cea-112">S_OK</span></span> 
  
> <span data-ttu-id="62cea-113">Успешно возвращено значение счетчика строк.</span><span class="sxs-lookup"><span data-stu-id="62cea-113">The row count was successfully returned.</span></span>
    
<span data-ttu-id="62cea-114">МАПИ_Е_БУСИ</span><span class="sxs-lookup"><span data-stu-id="62cea-114">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="62cea-115">Выполняется другая операция, которая не позволяет запустить операцию получения количества строк.</span><span class="sxs-lookup"><span data-stu-id="62cea-115">Another operation is in progress that prevents the row count retrieval operation from starting.</span></span> <span data-ttu-id="62cea-116">Выполнение выполняемой операции должно быть разрешено или остановлено.</span><span class="sxs-lookup"><span data-stu-id="62cea-116">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="62cea-117">МАПИ_Е_НО_СУППОРТ</span><span class="sxs-lookup"><span data-stu-id="62cea-117">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="62cea-118">В таблице невозможно вычислить количество строк.</span><span class="sxs-lookup"><span data-stu-id="62cea-118">The table cannot calculate the number of rows.</span></span>
    
<span data-ttu-id="62cea-119">МАПИ_В_АППРОКС_КАУНТ</span><span class="sxs-lookup"><span data-stu-id="62cea-119">MAPI_W_APPROX_COUNT</span></span> 
  
> <span data-ttu-id="62cea-120">Вызов выполнен успешно, но приблизительное число строк было возвращено из-за того, что не удалось определить точное количество строк, возможно, из-за ограничений памяти.</span><span class="sxs-lookup"><span data-stu-id="62cea-120">The call succeeded, but an approximate row count was returned because the exact row count could not be determined possibly due to memory constraints.</span></span> <span data-ttu-id="62cea-121">Чтобы проверить это предупреждение, используйте макрос **хр_фаилед** .</span><span class="sxs-lookup"><span data-stu-id="62cea-121">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="62cea-122">Просмотр и [Использование макросов для обработки ошибок](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="62cea-122">See [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="62cea-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="62cea-123">Remarks</span></span>

<span data-ttu-id="62cea-124">Метод **IMAPITable::** GetRows получает общее количество строк в таблице.</span><span class="sxs-lookup"><span data-stu-id="62cea-124">The **IMAPITable::GetRowCount** method retrieves the total number of rows in a table.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="62cea-125">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="62cea-125">Notes to implementers</span></span>

<span data-ttu-id="62cea-126">Если не удается определить точное количество строк в таблице, возвращается МАПИ_В_АППРОКС_КАУНТ и приблизительное число строк в содержимом параметра _лпулкаунт_ .</span><span class="sxs-lookup"><span data-stu-id="62cea-126">If you cannot determine the table's exact row count, return MAPI_W_APPROX_COUNT and an approximate row count in the contents of the  _lpulCount_ parameter.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="62cea-127">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="62cea-127">Notes to callers</span></span>

<span data-ttu-id="62cea-128">Используйте \*\*\*\* функцию GetRows, чтобы узнать, сколько строк содержит таблица, прежде чем совершать вызов метод [IMAPITable:: QueryRows](imapitable-queryrows.md) для получения данных.</span><span class="sxs-lookup"><span data-stu-id="62cea-128">Use **GetRowCount** to find out how many rows a table holds before making a call to the [IMAPITable::QueryRows](imapitable-queryrows.md) method to retrieve the data.</span></span> <span data-ttu-id="62cea-129">Если в таблице менее двадцати строк, для получения всей таблицы можно безопасно вызвать **куерипоситион** .</span><span class="sxs-lookup"><span data-stu-id="62cea-129">If there are less than twenty rows in the table, it is safe to call **QueryPosition** to retrieve the whole table.</span></span> <span data-ttu-id="62cea-130">Если таблица содержит более двадцати строк, рекомендуется выполнить несколько вызовов **куерипоситион** и ограничить количество строк, извлекаемых при каждом вызове.</span><span class="sxs-lookup"><span data-stu-id="62cea-130">If there are more than twenty rows in the table, consider making multiple calls to **QueryPosition** and limit the number of rows retrieved in each call.</span></span> 
  
<span data-ttu-id="62cea-131">В некоторых таблицах не \*\*\*\* поддерживаются мапи_е_но_суппорт и Return.</span><span class="sxs-lookup"><span data-stu-id="62cea-131">Some tables do not support **GetRowCount** and return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="62cea-132">Если \*\*\*\* метод куерипоситион не поддерживается, то альтернативным вариантом может быть вызов [IMAPITable::](imapitable-queryposition.md).</span><span class="sxs-lookup"><span data-stu-id="62cea-132">If **GetRowCount** is not supported, an alternative might be to call [IMAPITable::QueryPosition](imapitable-queryposition.md).</span></span> <span data-ttu-id="62cea-133">С помощью результатов из **куерипоситион**можно определить связь между текущей строкой и последней строкой.</span><span class="sxs-lookup"><span data-stu-id="62cea-133">With the results from **QueryPosition**, you can determine the relationship between the current row and last row.</span></span> 
  
<span data-ttu-id="62cea-134">Если \*\*\*\* метод мапи_е_буси ВОЗВРАЩАЕТ значение, так как временно не удается получить количество строк, вызовите метод [IMAPITable:: ваитфоркомплетион](imapitable-waitforcompletion.md) .</span><span class="sxs-lookup"><span data-stu-id="62cea-134">When **GetRowCount** returns MAPI_E_BUSY because it is temporarily unable to retrieve a row count, call the [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) method.</span></span> <span data-ttu-id="62cea-135">Когда возвращается Ваитфоркомплетион, повторите вызов метода \*\*\*\* . \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="62cea-135">When **WaitForCompletion** returns, retry the call to **GetRowCount**.</span></span> <span data-ttu-id="62cea-136">Другой способ определить, выполняется ли асинхронная операция, — вызвать метод [IMAPITable::-Status](imapitable-getstatus.md) и проверить содержимое параметра _лпултаблестате_ .</span><span class="sxs-lookup"><span data-stu-id="62cea-136">Another way to detect whether an asynchronous operation is in progress is to call the [IMAPITable::GetStatus](imapitable-getstatus.md) method and check the contents of the  _lpulTableState_ parameter.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="62cea-137">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="62cea-137">MFCMAPI reference</span></span>

<span data-ttu-id="62cea-138">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="62cea-138">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="62cea-139">**Файл**</span><span class="sxs-lookup"><span data-stu-id="62cea-139">**File**</span></span>|<span data-ttu-id="62cea-140">**Функция**</span><span class="sxs-lookup"><span data-stu-id="62cea-140">**Function**</span></span>|<span data-ttu-id="62cea-141">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="62cea-141">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="62cea-142">Мапифунктионс. cpp</span><span class="sxs-lookup"><span data-stu-id="62cea-142">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="62cea-143">Копифолдерконтентс</span><span class="sxs-lookup"><span data-stu-id="62cea-143">CopyFolderContents</span></span>  <br/> |<span data-ttu-id="62cea-144">MFCMAPI использует метод **IMAPITable::** , чтобы определить количество строк в исходной таблице, чтобы можно было выделить память для выполнения копирования.</span><span class="sxs-lookup"><span data-stu-id="62cea-144">MFCMAPI uses the **IMAPITable::GetRowCount** method to determine how many rows are in the source table so memory can be allocated to perform the copy.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="62cea-145">См. также</span><span class="sxs-lookup"><span data-stu-id="62cea-145">See also</span></span>



[<span data-ttu-id="62cea-146">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="62cea-146">IMAPITable::GetStatus</span></span>](imapitable-getstatus.md)
  
[<span data-ttu-id="62cea-147">IMAPITable::QueryPosition</span><span class="sxs-lookup"><span data-stu-id="62cea-147">IMAPITable::QueryPosition</span></span>](imapitable-queryposition.md)
  
[<span data-ttu-id="62cea-148">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="62cea-148">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="62cea-149">IMAPITable::WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="62cea-149">IMAPITable::WaitForCompletion</span></span>](imapitable-waitforcompletion.md)
  
[<span data-ttu-id="62cea-150">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="62cea-150">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="62cea-151">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="62cea-151">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

