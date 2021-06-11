---
title: IMAPITableSeekRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.SeekRow
api_type:
- COM
ms.assetid: 93ac63ae-f254-45e1-a9b1-347d69d2ed9f
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: fbc990a8c962883aa07987b200d1d2fd55434f93
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413047"
---
# <a name="imapitableseekrow"></a><span data-ttu-id="7a5d3-103">IMAPITable::SeekRow</span><span class="sxs-lookup"><span data-stu-id="7a5d3-103">IMAPITable::SeekRow</span></span>

  
  
<span data-ttu-id="7a5d3-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7a5d3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7a5d3-105">Перемещает курсор в определенное положение в таблице.</span><span class="sxs-lookup"><span data-stu-id="7a5d3-105">Moves the cursor to a specific position in the table.</span></span>
  
```cpp
HRESULT SeekRow(
BOOKMARK bkOrigin,
LONG lRowCount,
LONG FAR * lplRowsSought
);
```

## <a name="parameters"></a><span data-ttu-id="7a5d3-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="7a5d3-106">Parameters</span></span>

 <span data-ttu-id="7a5d3-107">_bkOrigin_</span><span class="sxs-lookup"><span data-stu-id="7a5d3-107">_bkOrigin_</span></span>
  
> <span data-ttu-id="7a5d3-108">[in] Закладки, определяющие исходное положение для операции поиска.</span><span class="sxs-lookup"><span data-stu-id="7a5d3-108">[in] The bookmark identifying the starting position for the seek operation.</span></span> <span data-ttu-id="7a5d3-109">Закладки можно создать с помощью [метода IMAPITable::CreateBookmark](imapitable-createbookmark.md) или передать одно из следующих предопределяемых значений.</span><span class="sxs-lookup"><span data-stu-id="7a5d3-109">A bookmark can be created using the [IMAPITable::CreateBookmark](imapitable-createbookmark.md) method, or one of the following predefined values can be passed.</span></span> 
    
<span data-ttu-id="7a5d3-110">BOOKMARK_BEGINNING</span><span class="sxs-lookup"><span data-stu-id="7a5d3-110">BOOKMARK_BEGINNING</span></span> 
  
> <span data-ttu-id="7a5d3-111">Начинает операцию поиска с начала таблицы.</span><span class="sxs-lookup"><span data-stu-id="7a5d3-111">Starts the seek operation from the beginning of the table.</span></span> 
    
<span data-ttu-id="7a5d3-112">BOOKMARK_CURRENT</span><span class="sxs-lookup"><span data-stu-id="7a5d3-112">BOOKMARK_CURRENT</span></span> 
  
> <span data-ttu-id="7a5d3-113">Запускает операцию поиска из строки в таблице, где расположен курсор.</span><span class="sxs-lookup"><span data-stu-id="7a5d3-113">Starts the seek operation from the row in the table where the cursor is located.</span></span> 
    
<span data-ttu-id="7a5d3-114">BOOKMARK_END</span><span class="sxs-lookup"><span data-stu-id="7a5d3-114">BOOKMARK_END</span></span> 
  
> <span data-ttu-id="7a5d3-115">Запускает операцию поиска с конца таблицы.</span><span class="sxs-lookup"><span data-stu-id="7a5d3-115">Starts the seek operation from the end of the table.</span></span> 
    
 <span data-ttu-id="7a5d3-116">_lRowCount_</span><span class="sxs-lookup"><span data-stu-id="7a5d3-116">_lRowCount_</span></span>
  
> <span data-ttu-id="7a5d3-117">[in] Подписанный подсчет числа строк для перемещения, начиная с закладки, выделенной _параметром bkOrigin._</span><span class="sxs-lookup"><span data-stu-id="7a5d3-117">[in] The signed count of the number of rows to move, starting from the bookmark identified by the  _bkOrigin_ parameter.</span></span> 
    
 <span data-ttu-id="7a5d3-118">_lplRowsSought_</span><span class="sxs-lookup"><span data-stu-id="7a5d3-118">_lplRowsSought_</span></span>
  
> <span data-ttu-id="7a5d3-119">[вышел] Если  _lRowCount_ является допустимым указателем ввода,  _lplRowsSought_ указывает на количество строк, обработанных в операции поиска, знак которого указывает направление поиска, вперед или назад.</span><span class="sxs-lookup"><span data-stu-id="7a5d3-119">[out] If  _lRowCount_ is a valid pointer on input,  _lplRowsSought_ points to the number of rows that were processed in the seek operation, the sign of which indicates the direction of search, forward or backward.</span></span> <span data-ttu-id="7a5d3-120">Если  _lRowCount_ является отрицательным,  _то lplRowsSought —_ отрицательным.</span><span class="sxs-lookup"><span data-stu-id="7a5d3-120">If  _lRowCount_ is negative, then  _lplRowsSought_ is negative.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="7a5d3-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7a5d3-121">Return value</span></span>

<span data-ttu-id="7a5d3-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="7a5d3-122">S_OK</span></span> 
  
> <span data-ttu-id="7a5d3-123">Операция поиска прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="7a5d3-123">The seek operation was successful.</span></span>
    
<span data-ttu-id="7a5d3-124">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="7a5d3-124">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="7a5d3-125">В настоящее время продолжается другая операция, которая не позволяет начать операцию поиска строки.</span><span class="sxs-lookup"><span data-stu-id="7a5d3-125">Another operation is in progress that prevents the row-seeking operation from starting.</span></span> <span data-ttu-id="7a5d3-126">Либо операция должна быть разрешена к завершению, либо она должна быть остановлена.</span><span class="sxs-lookup"><span data-stu-id="7a5d3-126">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="7a5d3-127">MAPI_E_INVALID_BOOKMARK</span><span class="sxs-lookup"><span data-stu-id="7a5d3-127">MAPI_E_INVALID_BOOKMARK</span></span> 
  
> <span data-ttu-id="7a5d3-128">Закладки, указанные в  _параметре bkOrigin,_ недействительны, так как она была удалена или находится за пределами последней строки, запрашиваемой.</span><span class="sxs-lookup"><span data-stu-id="7a5d3-128">The bookmark specified in the  _bkOrigin_ parameter is invalid because it was removed or because it is beyond the last row requested.</span></span> 
    
<span data-ttu-id="7a5d3-129">MAPI_W_POSITION_CHANGED</span><span class="sxs-lookup"><span data-stu-id="7a5d3-129">MAPI_W_POSITION_CHANGED</span></span> 
  
> <span data-ttu-id="7a5d3-130">Вызов удался, но закладки, указанные в параметре  _bkOrigin,_ больше не заданы в том же ряду, что и в последний раз.</span><span class="sxs-lookup"><span data-stu-id="7a5d3-130">The call succeeded, but the bookmark specified in the  _bkOrigin_ parameter is no longer set at the same row as it was when it was last used.</span></span> <span data-ttu-id="7a5d3-131">Если закладка не была использована, она больше не находится в том же положении, что и при ее создания.</span><span class="sxs-lookup"><span data-stu-id="7a5d3-131">If the bookmark has not been used, it is no longer in the same position as it was when it was created.</span></span> <span data-ttu-id="7a5d3-132">Когда это предупреждение возвращается, вызов должен быть обработан как успешный.</span><span class="sxs-lookup"><span data-stu-id="7a5d3-132">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="7a5d3-133">Чтобы проверить это предупреждение, используйте **HR_FAILED** макрос.</span><span class="sxs-lookup"><span data-stu-id="7a5d3-133">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="7a5d3-134">Дополнительные сведения см. в [дополнительных сведениях Об использовании макроса для обработки ошибок.](using-macros-for-error-handling.md)</span><span class="sxs-lookup"><span data-stu-id="7a5d3-134">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7a5d3-135">Примечания</span><span class="sxs-lookup"><span data-stu-id="7a5d3-135">Remarks</span></span>

<span data-ttu-id="7a5d3-136">Метод **IMAPITable::SeekRow** устанавливает новое BOOKMARK_CURRENT для курсора.</span><span class="sxs-lookup"><span data-stu-id="7a5d3-136">The **IMAPITable::SeekRow** method establishes a new BOOKMARK_CURRENT position for the cursor.</span></span> <span data-ttu-id="7a5d3-137">Параметр  _lRowCount_ указывает количество строк, которые перемещает курсор, и направление движения.</span><span class="sxs-lookup"><span data-stu-id="7a5d3-137">The  _lRowCount_ parameter indicates the number of rows that the cursor moves and the direction of movement.</span></span> 
  
<span data-ttu-id="7a5d3-138">Если итоговая позиция находится за последней строкой таблицы, курсор находится после последней строки.</span><span class="sxs-lookup"><span data-stu-id="7a5d3-138">If the resulting position is beyond the last row of the table, the cursor is positioned after the last row.</span></span> <span data-ttu-id="7a5d3-139">Если итоговая позиция находится перед первым ряду таблицы, курсор находится в начале первого ряда.</span><span class="sxs-lookup"><span data-stu-id="7a5d3-139">If the resulting position is before the first row of the table, the cursor is positioned at the beginning of the first row.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="7a5d3-140">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="7a5d3-140">Notes to implementers</span></span>

<span data-ttu-id="7a5d3-141">Если строка, на которую указывает  _bkOrigin,_ больше не существует в таблице и вы не можете установить новую позицию для закладки, MAPI_E_INVALID_BOOKMARK.</span><span class="sxs-lookup"><span data-stu-id="7a5d3-141">If the row pointed to by  _bkOrigin_ no longer exists in the table and you cannot establish a new position for the bookmark, return MAPI_E_INVALID_BOOKMARK.</span></span> <span data-ttu-id="7a5d3-142">Если строка, на которую указывает  _bkOrigin,_ больше не существует и можно установить новую позицию для закладки, верни MAPI_W_POSITION_CHANGED.</span><span class="sxs-lookup"><span data-stu-id="7a5d3-142">If the row pointed to by  _bkOrigin_ no longer exists and you can establish a new position for the bookmark, return MAPI_W_POSITION_CHANGED.</span></span> 
  
<span data-ttu-id="7a5d3-143">Закладки, указывающие на строку, которая рухнула из представления таблицы, по-прежнему можно использовать.</span><span class="sxs-lookup"><span data-stu-id="7a5d3-143">A bookmark pointing to a row that is collapsed out of the table view can still be used.</span></span> <span data-ttu-id="7a5d3-144">Если вызыватель пытается переместить курсор в такую закладку, переместить курсор в следующую видимую строку и MAPI_W_POSITION_CHANGED.</span><span class="sxs-lookup"><span data-stu-id="7a5d3-144">If the caller attempts to move the cursor to such a bookmark, move the cursor to the next visible row and return MAPI_W_POSITION_CHANGED.</span></span> 
  
<span data-ttu-id="7a5d3-145">Вы можете переместить закладки для позиций, схвастимые из виду, либо во время использования, либо во время обрушения строки.</span><span class="sxs-lookup"><span data-stu-id="7a5d3-145">You can move bookmarks for positions collapsed out of view, either at the time of use or at the time that the row is collapsed.</span></span> <span data-ttu-id="7a5d3-146">Если закладки перемещаются при обрушении строки, держите немного в закладке, которая указывает, переместилась ли закладка с момента последнего использования или, если она никогда не использовалась, с момента ее создания.</span><span class="sxs-lookup"><span data-stu-id="7a5d3-146">If a bookmark is moved at the time that the row is collapsed, keep a bit in the bookmark that indicates whether the bookmark has moved since its last use or, if it has never been used, since its creation.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="7a5d3-147">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="7a5d3-147">Notes to callers</span></span>

<span data-ttu-id="7a5d3-148">Чтобы указать обратный ход **для SeekRow,** передай отрицательное значение _в lRowCount._</span><span class="sxs-lookup"><span data-stu-id="7a5d3-148">To indicate a backward move for **SeekRow**, pass a negative value in  _lRowCount_.</span></span> <span data-ttu-id="7a5d3-149">Чтобы найти в начале таблицы, передай ноль  _в lRowCount_ и значение BOOKMARK_BEGINNING  _в bkOrigin_.</span><span class="sxs-lookup"><span data-stu-id="7a5d3-149">To search to the beginning of the table, pass zero in  _lRowCount_ and the value BOOKMARK_BEGINNING in  _bkOrigin_.</span></span> 
  
<span data-ttu-id="7a5d3-150">Если в таблице много строк, операция **SeekRow** может быть медленной.</span><span class="sxs-lookup"><span data-stu-id="7a5d3-150">If there are lots of rows in the table, the **SeekRow** operation can be slow.</span></span> <span data-ttu-id="7a5d3-151">Производительность также может быть затронута, если требуется вернуть количество строк в содержимом _параметра lplRowsSought._</span><span class="sxs-lookup"><span data-stu-id="7a5d3-151">Performance can also be affected if you require a row count to be returned in the contents of the  _lplRowsSought_ parameter.</span></span> 
  
 <span data-ttu-id="7a5d3-152">**SeekRow** возвращает количество строк, которые на самом деле искали в переменной  _lRowCount,_ положительное или отрицательное.</span><span class="sxs-lookup"><span data-stu-id="7a5d3-152">**SeekRow** returns the number of rows actually searched through, positive or negative, in the variable pointed to by  _lRowCount_.</span></span> <span data-ttu-id="7a5d3-153">В обычной операции оно должно возвращать то же значение  _для lplRowsSought,_ что и для  _lRowCount,_ если поиск не достиг начала или конца таблицы.</span><span class="sxs-lookup"><span data-stu-id="7a5d3-153">In ordinary operation, it should return the same value for  _lplRowsSought_ as passed in for  _lRowCount_, unless the search reached the beginning or end of the table.</span></span> 
  
<span data-ttu-id="7a5d3-154">Не установите  _lRowCount_ на число больше 50.</span><span class="sxs-lookup"><span data-stu-id="7a5d3-154">Do not set  _lRowCount_ to a number greater than 50.</span></span> <span data-ttu-id="7a5d3-155">Чтобы найти больше строк, используйте метод [IMAPITable::SeekRowApprox.](imapitable-seekrowapprox.md)</span><span class="sxs-lookup"><span data-stu-id="7a5d3-155">To seek through a larger number of rows, use the [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="7a5d3-156">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="7a5d3-156">MFCMAPI reference</span></span>

<span data-ttu-id="7a5d3-157">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="7a5d3-157">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="7a5d3-158">**Файл**</span><span class="sxs-lookup"><span data-stu-id="7a5d3-158">**File**</span></span>|<span data-ttu-id="7a5d3-159">**Функция**</span><span class="sxs-lookup"><span data-stu-id="7a5d3-159">**Function**</span></span>|<span data-ttu-id="7a5d3-160">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="7a5d3-160">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7a5d3-161">MAPIProcessor.cpp</span><span class="sxs-lookup"><span data-stu-id="7a5d3-161">MAPIProcessor.cpp</span></span>  <br/> |<span data-ttu-id="7a5d3-162">CMAPIProcessor::P rocessMailboxTable</span><span class="sxs-lookup"><span data-stu-id="7a5d3-162">CMAPIProcessor::ProcessMailboxTable</span></span>  <br/> |<span data-ttu-id="7a5d3-163">MFCMAPI использует **метод IMAPITable::SeekRow** для определения начала таблицы перед обработкой.</span><span class="sxs-lookup"><span data-stu-id="7a5d3-163">MFCMAPI uses the **IMAPITable::SeekRow** method to locate the beginning of the table before processing.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7a5d3-164">См. также</span><span class="sxs-lookup"><span data-stu-id="7a5d3-164">See also</span></span>



[<span data-ttu-id="7a5d3-165">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="7a5d3-165">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md)
  
[<span data-ttu-id="7a5d3-166">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="7a5d3-166">IMAPITable::FindRow</span></span>](imapitable-findrow.md)
  
[<span data-ttu-id="7a5d3-167">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="7a5d3-167">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="7a5d3-168">IMAPITable::SeekRowApprox</span><span class="sxs-lookup"><span data-stu-id="7a5d3-168">IMAPITable::SeekRowApprox</span></span>](imapitable-seekrowapprox.md)
  
[<span data-ttu-id="7a5d3-169">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7a5d3-169">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="7a5d3-170">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="7a5d3-170">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

