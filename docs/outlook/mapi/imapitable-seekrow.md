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
ms.openlocfilehash: aead09eb10a3015a54867f14011c56b686bc8624
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586482"
---
# <a name="imapitableseekrow"></a><span data-ttu-id="1f299-103">IMAPITable::SeekRow</span><span class="sxs-lookup"><span data-stu-id="1f299-103">IMAPITable::SeekRow</span></span>

  
  
<span data-ttu-id="1f299-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1f299-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1f299-105">Перемещение курсора в определенное место в таблице.</span><span class="sxs-lookup"><span data-stu-id="1f299-105">Moves the cursor to a specific position in the table.</span></span>
  
```cpp
HRESULT SeekRow(
BOOKMARK bkOrigin,
LONG lRowCount,
LONG FAR * lplRowsSought
);
```

## <a name="parameters"></a><span data-ttu-id="1f299-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1f299-106">Parameters</span></span>

 <span data-ttu-id="1f299-107">_bkOrigin_</span><span class="sxs-lookup"><span data-stu-id="1f299-107">_bkOrigin_</span></span>
  
> <span data-ttu-id="1f299-108">[in] Закладки, определяющее позицию для операции поиска.</span><span class="sxs-lookup"><span data-stu-id="1f299-108">[in] The bookmark identifying the starting position for the seek operation.</span></span> <span data-ttu-id="1f299-109">Закладки можно создать с помощью метода [IMAPITable::CreateBookmark](imapitable-createbookmark.md) или один из следующих предварительно заданных значений может быть передан.</span><span class="sxs-lookup"><span data-stu-id="1f299-109">A bookmark can be created using the [IMAPITable::CreateBookmark](imapitable-createbookmark.md) method, or one of the following predefined values can be passed.</span></span> 
    
<span data-ttu-id="1f299-110">BOOKMARK_BEGINNING</span><span class="sxs-lookup"><span data-stu-id="1f299-110">BOOKMARK_BEGINNING</span></span> 
  
> <span data-ttu-id="1f299-111">Запускает операции поиска с начала таблицы.</span><span class="sxs-lookup"><span data-stu-id="1f299-111">Starts the seek operation from the beginning of the table.</span></span> 
    
<span data-ttu-id="1f299-112">BOOKMARK_CURRENT</span><span class="sxs-lookup"><span data-stu-id="1f299-112">BOOKMARK_CURRENT</span></span> 
  
> <span data-ttu-id="1f299-113">Запускает операцию поиска из строки в таблице, в котором находится курсор.</span><span class="sxs-lookup"><span data-stu-id="1f299-113">Starts the seek operation from the row in the table where the cursor is located.</span></span> 
    
<span data-ttu-id="1f299-114">BOOKMARK_END</span><span class="sxs-lookup"><span data-stu-id="1f299-114">BOOKMARK_END</span></span> 
  
> <span data-ttu-id="1f299-115">Запускает операции поиска с конца таблицы.</span><span class="sxs-lookup"><span data-stu-id="1f299-115">Starts the seek operation from the end of the table.</span></span> 
    
 <span data-ttu-id="1f299-116">_lRowCount_</span><span class="sxs-lookup"><span data-stu-id="1f299-116">_lRowCount_</span></span>
  
> <span data-ttu-id="1f299-117">[in] Счетчик со знаком число строк для перемещения, начиная с закладки определенного параметром _bkOrigin_ .</span><span class="sxs-lookup"><span data-stu-id="1f299-117">[in] The signed count of the number of rows to move, starting from the bookmark identified by the  _bkOrigin_ parameter.</span></span> 
    
 <span data-ttu-id="1f299-118">_lplRowsSought_</span><span class="sxs-lookup"><span data-stu-id="1f299-118">_lplRowsSought_</span></span>
  
> <span data-ttu-id="1f299-119">[out] Если _lRowCount_ допустимый указатель на ввода, _lplRowsSought_ указывает на количество строк, обработанных в операции поиска, знак из которых указывает направление поиска, вперед или назад.</span><span class="sxs-lookup"><span data-stu-id="1f299-119">[out] If  _lRowCount_ is a valid pointer on input,  _lplRowsSought_ points to the number of rows that were processed in the seek operation, the sign of which indicates the direction of search, forward or backward.</span></span> <span data-ttu-id="1f299-120">Если _lRowCount_ является отрицательным, _lplRowsSought_ является отрицательным.</span><span class="sxs-lookup"><span data-stu-id="1f299-120">If  _lRowCount_ is negative, then  _lplRowsSought_ is negative.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1f299-121">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="1f299-121">Return value</span></span>

<span data-ttu-id="1f299-122">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="1f299-122">S_OK</span></span> 
  
> <span data-ttu-id="1f299-123">Операции поиска выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="1f299-123">The seek operation was successful.</span></span>
    
<span data-ttu-id="1f299-124">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="1f299-124">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="1f299-125">В, не позволяющей операции поиска строки запуск выполняется другой операции.</span><span class="sxs-lookup"><span data-stu-id="1f299-125">Another operation is in progress that prevents the row-seeking operation from starting.</span></span> <span data-ttu-id="1f299-126">В процессе выполнения операции должны выполнить либо должна быть остановлена.</span><span class="sxs-lookup"><span data-stu-id="1f299-126">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="1f299-127">MAPI_E_INVALID_BOOKMARK</span><span class="sxs-lookup"><span data-stu-id="1f299-127">MAPI_E_INVALID_BOOKMARK</span></span> 
  
> <span data-ttu-id="1f299-128">Закладки, указанный в параметре _bkOrigin_ является недопустимым, так как он был удален или находится за последней строки запроса.</span><span class="sxs-lookup"><span data-stu-id="1f299-128">The bookmark specified in the  _bkOrigin_ parameter is invalid because it was removed or because it is beyond the last row requested.</span></span> 
    
<span data-ttu-id="1f299-129">MAPI_W_POSITION_CHANGED</span><span class="sxs-lookup"><span data-stu-id="1f299-129">MAPI_W_POSITION_CHANGED</span></span> 
  
> <span data-ttu-id="1f299-130">Вызов завершился успешно, но закладку, указанный в параметре _bkOrigin_ больше не устанавливаются в той же строке, что его последнего использования.</span><span class="sxs-lookup"><span data-stu-id="1f299-130">The call succeeded, but the bookmark specified in the  _bkOrigin_ parameter is no longer set at the same row as it was when it was last used.</span></span> <span data-ttu-id="1f299-131">Если не использовалась закладки, больше не в том же месте, которая была при его создании.</span><span class="sxs-lookup"><span data-stu-id="1f299-131">If the bookmark has not been used, it is no longer in the same position as it was when it was created.</span></span> <span data-ttu-id="1f299-132">При возвращении этого предупреждения вызова необходимо обрабатывать об успешном завершении.</span><span class="sxs-lookup"><span data-stu-id="1f299-132">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="1f299-133">Чтобы проверить это предупреждение, используйте **HR_FAILED** макрос.</span><span class="sxs-lookup"><span data-stu-id="1f299-133">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="1f299-134">Дополнительные сведения можно [С помощью макросов для обработки ошибок](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="1f299-134">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1f299-135">Замечания</span><span class="sxs-lookup"><span data-stu-id="1f299-135">Remarks</span></span>

<span data-ttu-id="1f299-136">Метод **IMAPITable::SeekRow** устанавливает новую BOOKMARK_CURRENT позицию курсора.</span><span class="sxs-lookup"><span data-stu-id="1f299-136">The **IMAPITable::SeekRow** method establishes a new BOOKMARK_CURRENT position for the cursor.</span></span> <span data-ttu-id="1f299-137">Параметр _lRowCount_ указывает число строк, которые перемещает курсор и направление перемещения.</span><span class="sxs-lookup"><span data-stu-id="1f299-137">The  _lRowCount_ parameter indicates the number of rows that the cursor moves and the direction of movement.</span></span> 
  
<span data-ttu-id="1f299-138">Если итоговый позицию за пределами последней строки в таблице, курсор расположен после последней строки.</span><span class="sxs-lookup"><span data-stu-id="1f299-138">If the resulting position is beyond the last row of the table, the cursor is positioned after the last row.</span></span> <span data-ttu-id="1f299-139">Если итоговый положение перед первой строки в таблице, курсор расположен в начале первой строки.</span><span class="sxs-lookup"><span data-stu-id="1f299-139">If the resulting position is before the first row of the table, the cursor is positioned at the beginning of the first row.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="1f299-140">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="1f299-140">Notes to implementers</span></span>

<span data-ttu-id="1f299-141">Если не удается установить новую позицию закладки строки, на который указывает _bkOrigin_ больше не существует в таблице, возвращают MAPI_E_INVALID_BOOKMARK.</span><span class="sxs-lookup"><span data-stu-id="1f299-141">If the row pointed to by  _bkOrigin_ no longer exists in the table and you cannot establish a new position for the bookmark, return MAPI_E_INVALID_BOOKMARK.</span></span> <span data-ttu-id="1f299-142">Если строка, на который указывает _bkOrigin_ больше не существует, можно создать новую позицию закладки возврата MAPI_W_POSITION_CHANGED.</span><span class="sxs-lookup"><span data-stu-id="1f299-142">If the row pointed to by  _bkOrigin_ no longer exists and you can establish a new position for the bookmark, return MAPI_W_POSITION_CHANGED.</span></span> 
  
<span data-ttu-id="1f299-143">Строка, в которой сворачивается из представления таблицы с указанием закладку по-прежнему можно использовать.</span><span class="sxs-lookup"><span data-stu-id="1f299-143">A bookmark pointing to a row that is collapsed out of the table view can still be used.</span></span> <span data-ttu-id="1f299-144">Попытка вызывающего абонента, переместите курсор к такой как закладка переместите курсор к следующей строке видимым и возвращают MAPI_W_POSITION_CHANGED.</span><span class="sxs-lookup"><span data-stu-id="1f299-144">If the caller attempts to move the cursor to such a bookmark, move the cursor to the next visible row and return MAPI_W_POSITION_CHANGED.</span></span> 
  
<span data-ttu-id="1f299-145">Вы можете переместить закладки для положения свернуты экрана, во время использования или во время скрытую строку.</span><span class="sxs-lookup"><span data-stu-id="1f299-145">You can move bookmarks for positions collapsed out of view, either at the time of use or at the time that the row is collapsed.</span></span> <span data-ttu-id="1f299-146">Если закладки перемещается во время скрытую строку, помните, немного закладки, которое указывает, имеет ли закладки перемещен с момента ее последнего использования или, если он имеет никогда не использовался, с момента его создания.</span><span class="sxs-lookup"><span data-stu-id="1f299-146">If a bookmark is moved at the time that the row is collapsed, keep a bit in the bookmark that indicates whether the bookmark has moved since its last use or, if it has never been used, since its creation.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="1f299-147">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="1f299-147">Notes to callers</span></span>

<span data-ttu-id="1f299-148">Чтобы указать обратной перемещения для **SeekRow**, передайте отрицательное значение _lRowCount_.</span><span class="sxs-lookup"><span data-stu-id="1f299-148">To indicate a backward move for **SeekRow**, pass a negative value in  _lRowCount_.</span></span> <span data-ttu-id="1f299-149">Чтобы выполнить поиск в начало таблицы, передайте нулевое значение в _lRowCount_ и значение BOOKMARK_BEGINNING в _bkOrigin_.</span><span class="sxs-lookup"><span data-stu-id="1f299-149">To search to the beginning of the table, pass zero in  _lRowCount_ and the value BOOKMARK_BEGINNING in  _bkOrigin_.</span></span> 
  
<span data-ttu-id="1f299-150">Если большое количество строк в таблице, операция **SeekRow** может быть медленно.</span><span class="sxs-lookup"><span data-stu-id="1f299-150">If there are lots of rows in the table, the **SeekRow** operation can be slow.</span></span> <span data-ttu-id="1f299-151">Может также повлиять на производительность при необходимости число строк должно быть возвращено содержимое параметр _lplRowsSought_ .</span><span class="sxs-lookup"><span data-stu-id="1f299-151">Performance can also be affected if you require a row count to be returned in the contents of the  _lplRowsSought_ parameter.</span></span> 
  
 <span data-ttu-id="1f299-152">**SeekRow** возвращает количество строк, фактически осуществляется через, положительное или отрицательное, указанному в переменной, на который указывает _lRowCount_.</span><span class="sxs-lookup"><span data-stu-id="1f299-152">**SeekRow** returns the number of rows actually searched through, positive or negative, in the variable pointed to by  _lRowCount_.</span></span> <span data-ttu-id="1f299-153">В обычные операции он должен возвращать такое же значение для _lplRowsSought_ как передано в качестве _lRowCount_, если не достигнут начала или окончания в таблице.</span><span class="sxs-lookup"><span data-stu-id="1f299-153">In ordinary operation, it should return the same value for  _lplRowsSought_ as passed in for  _lRowCount_, unless the search reached the beginning or end of the table.</span></span> 
  
<span data-ttu-id="1f299-154">Не следует устанавливать _lRowCount_ значение больше, чем 50.</span><span class="sxs-lookup"><span data-stu-id="1f299-154">Do not set  _lRowCount_ to a number greater than 50.</span></span> <span data-ttu-id="1f299-155">Чтобы поиск с помощью большое число строк, используйте метод [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) .</span><span class="sxs-lookup"><span data-stu-id="1f299-155">To seek through a larger number of rows, use the [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1f299-156">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="1f299-156">MFCMAPI reference</span></span>

<span data-ttu-id="1f299-157">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="1f299-157">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1f299-158">**����**</span><span class="sxs-lookup"><span data-stu-id="1f299-158">**File**</span></span>|<span data-ttu-id="1f299-159">**�������**</span><span class="sxs-lookup"><span data-stu-id="1f299-159">**Function**</span></span>|<span data-ttu-id="1f299-160">**�����������**</span><span class="sxs-lookup"><span data-stu-id="1f299-160">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1f299-161">MAPIProcessor.cpp</span><span class="sxs-lookup"><span data-stu-id="1f299-161">MAPIProcessor.cpp</span></span>  <br/> |<span data-ttu-id="1f299-162">CMAPIProcessor::ProcessMailboxTable</span><span class="sxs-lookup"><span data-stu-id="1f299-162">CMAPIProcessor::ProcessMailboxTable</span></span>  <br/> |<span data-ttu-id="1f299-163">Mfcmapi (en) использует метод **IMAPITable::SeekRow** для обнаружения начало таблицы перед обработкой.</span><span class="sxs-lookup"><span data-stu-id="1f299-163">MFCMAPI uses the **IMAPITable::SeekRow** method to locate the beginning of the table before processing.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1f299-164">См. также</span><span class="sxs-lookup"><span data-stu-id="1f299-164">See also</span></span>



[<span data-ttu-id="1f299-165">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="1f299-165">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md)
  
[<span data-ttu-id="1f299-166">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="1f299-166">IMAPITable::FindRow</span></span>](imapitable-findrow.md)
  
[<span data-ttu-id="1f299-167">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="1f299-167">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="1f299-168">IMAPITable::SeekRowApprox</span><span class="sxs-lookup"><span data-stu-id="1f299-168">IMAPITable::SeekRowApprox</span></span>](imapitable-seekrowapprox.md)
  
[<span data-ttu-id="1f299-169">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1f299-169">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="1f299-170">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="1f299-170">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

