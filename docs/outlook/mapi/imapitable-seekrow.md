---
title: имапитаблесикров
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
# <a name="imapitableseekrow"></a><span data-ttu-id="bf27f-103">IMAPITable::SeekRow</span><span class="sxs-lookup"><span data-stu-id="bf27f-103">IMAPITable::SeekRow</span></span>

  
  
<span data-ttu-id="bf27f-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bf27f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bf27f-105">Перемещает курсор к определенному положению в таблице.</span><span class="sxs-lookup"><span data-stu-id="bf27f-105">Moves the cursor to a specific position in the table.</span></span>
  
```cpp
HRESULT SeekRow(
BOOKMARK bkOrigin,
LONG lRowCount,
LONG FAR * lplRowsSought
);
```

## <a name="parameters"></a><span data-ttu-id="bf27f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bf27f-106">Parameters</span></span>

 <span data-ttu-id="bf27f-107">_бкоригин_</span><span class="sxs-lookup"><span data-stu-id="bf27f-107">_bkOrigin_</span></span>
  
> <span data-ttu-id="bf27f-108">возврата Закладка, указывающая начальную позицию для операции поиска.</span><span class="sxs-lookup"><span data-stu-id="bf27f-108">[in] The bookmark identifying the starting position for the seek operation.</span></span> <span data-ttu-id="bf27f-109">Можно создать закладку с помощью метода [IMAPITable:: креатебукмарк](imapitable-createbookmark.md) или одного из следующих предварительно заданных значений.</span><span class="sxs-lookup"><span data-stu-id="bf27f-109">A bookmark can be created using the [IMAPITable::CreateBookmark](imapitable-createbookmark.md) method, or one of the following predefined values can be passed.</span></span> 
    
<span data-ttu-id="bf27f-110">BOOKMARK_BEGINNING</span><span class="sxs-lookup"><span data-stu-id="bf27f-110">BOOKMARK_BEGINNING</span></span> 
  
> <span data-ttu-id="bf27f-111">Начинает операцию поиска с начала таблицы.</span><span class="sxs-lookup"><span data-stu-id="bf27f-111">Starts the seek operation from the beginning of the table.</span></span> 
    
<span data-ttu-id="bf27f-112">BOOKMARK_CURRENT</span><span class="sxs-lookup"><span data-stu-id="bf27f-112">BOOKMARK_CURRENT</span></span> 
  
> <span data-ttu-id="bf27f-113">Начинает операцию поиска из строки в таблице, в которой находится курсор.</span><span class="sxs-lookup"><span data-stu-id="bf27f-113">Starts the seek operation from the row in the table where the cursor is located.</span></span> 
    
<span data-ttu-id="bf27f-114">BOOKMARK_END</span><span class="sxs-lookup"><span data-stu-id="bf27f-114">BOOKMARK_END</span></span> 
  
> <span data-ttu-id="bf27f-115">Начинает операцию поиска с конца таблицы.</span><span class="sxs-lookup"><span data-stu-id="bf27f-115">Starts the seek operation from the end of the table.</span></span> 
    
 <span data-ttu-id="bf27f-116">_лровкаунт_</span><span class="sxs-lookup"><span data-stu-id="bf27f-116">_lRowCount_</span></span>
  
> <span data-ttu-id="bf27f-117">возврата Число подписанных строк, которые необходимо переместить, начиная с закладки, указанной параметром _бкоригин_ .</span><span class="sxs-lookup"><span data-stu-id="bf27f-117">[in] The signed count of the number of rows to move, starting from the bookmark identified by the  _bkOrigin_ parameter.</span></span> 
    
 <span data-ttu-id="bf27f-118">_лплровссаугхт_</span><span class="sxs-lookup"><span data-stu-id="bf27f-118">_lplRowsSought_</span></span>
  
> <span data-ttu-id="bf27f-119">вышли Если _лровкаунт_ является допустимым указателем на входе, _лплровссаугхт_ указывает на количество строк, обработанных в операции поиска, знак, указывающий направление поиска, вперед или назад.</span><span class="sxs-lookup"><span data-stu-id="bf27f-119">[out] If  _lRowCount_ is a valid pointer on input,  _lplRowsSought_ points to the number of rows that were processed in the seek operation, the sign of which indicates the direction of search, forward or backward.</span></span> <span data-ttu-id="bf27f-120">Если _лровкаунт_ отрицательно, то _лплровссаугхт_ является отрицательным.</span><span class="sxs-lookup"><span data-stu-id="bf27f-120">If  _lRowCount_ is negative, then  _lplRowsSought_ is negative.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="bf27f-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bf27f-121">Return value</span></span>

<span data-ttu-id="bf27f-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="bf27f-122">S_OK</span></span> 
  
> <span data-ttu-id="bf27f-123">Операция поиска выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="bf27f-123">The seek operation was successful.</span></span>
    
<span data-ttu-id="bf27f-124">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="bf27f-124">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="bf27f-125">Выполняется другая операция, которая не позволяет запустить операцию поиска строк.</span><span class="sxs-lookup"><span data-stu-id="bf27f-125">Another operation is in progress that prevents the row-seeking operation from starting.</span></span> <span data-ttu-id="bf27f-126">Выполнение выполняемой операции должно быть разрешено или остановлено.</span><span class="sxs-lookup"><span data-stu-id="bf27f-126">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="bf27f-127">MAPI_E_INVALID_BOOKMARK</span><span class="sxs-lookup"><span data-stu-id="bf27f-127">MAPI_E_INVALID_BOOKMARK</span></span> 
  
> <span data-ttu-id="bf27f-128">Закладка, указанная в параметре _бкоригин_ , является недопустимой, так как она была удалена или находится за пределами последней запрошенной строки.</span><span class="sxs-lookup"><span data-stu-id="bf27f-128">The bookmark specified in the  _bkOrigin_ parameter is invalid because it was removed or because it is beyond the last row requested.</span></span> 
    
<span data-ttu-id="bf27f-129">MAPI_W_POSITION_CHANGED</span><span class="sxs-lookup"><span data-stu-id="bf27f-129">MAPI_W_POSITION_CHANGED</span></span> 
  
> <span data-ttu-id="bf27f-130">Вызов выполнен успешно, но закладка, указанная в параметре _бкоригин_ , больше не задается в той же строке, что и при ее последнем использовании.</span><span class="sxs-lookup"><span data-stu-id="bf27f-130">The call succeeded, but the bookmark specified in the  _bkOrigin_ parameter is no longer set at the same row as it was when it was last used.</span></span> <span data-ttu-id="bf27f-131">Если закладка не использовалась, она больше не находится в той же позиции, что и при ее создании.</span><span class="sxs-lookup"><span data-stu-id="bf27f-131">If the bookmark has not been used, it is no longer in the same position as it was when it was created.</span></span> <span data-ttu-id="bf27f-132">При возвращении этого предупреждения вызов должен обрабатываться как успешный.</span><span class="sxs-lookup"><span data-stu-id="bf27f-132">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="bf27f-133">Чтобы проверить это предупреждение, используйте макрос **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="bf27f-133">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="bf27f-134">Дополнительные сведения см. [в разделе Использование макросов для обработки ошибок](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="bf27f-134">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bf27f-135">Примечания</span><span class="sxs-lookup"><span data-stu-id="bf27f-135">Remarks</span></span>

<span data-ttu-id="bf27f-136">Метод **IMAPITable:: сикров** устанавливает новое положение BOOKMARK_CURRENT курсора.</span><span class="sxs-lookup"><span data-stu-id="bf27f-136">The **IMAPITable::SeekRow** method establishes a new BOOKMARK_CURRENT position for the cursor.</span></span> <span data-ttu-id="bf27f-137">Параметр _лровкаунт_ указывает количество строк, на которые курсор перемещается и направление движения.</span><span class="sxs-lookup"><span data-stu-id="bf27f-137">The  _lRowCount_ parameter indicates the number of rows that the cursor moves and the direction of movement.</span></span> 
  
<span data-ttu-id="bf27f-138">Если полученная позиция находится за пределами последней строки таблицы, курсор помещается после последней строки.</span><span class="sxs-lookup"><span data-stu-id="bf27f-138">If the resulting position is beyond the last row of the table, the cursor is positioned after the last row.</span></span> <span data-ttu-id="bf27f-139">Если полученная позиция находится перед первой строкой таблицы, курсор помещается в начало первой строки.</span><span class="sxs-lookup"><span data-stu-id="bf27f-139">If the resulting position is before the first row of the table, the cursor is positioned at the beginning of the first row.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="bf27f-140">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="bf27f-140">Notes to implementers</span></span>

<span data-ttu-id="bf27f-141">Если строка, на которую указывает _бкоригин_ , больше не существует в таблице, и вы не можете установить новую позицию для закладки, возвращайте MAPI_E_INVALID_BOOKMARK.</span><span class="sxs-lookup"><span data-stu-id="bf27f-141">If the row pointed to by  _bkOrigin_ no longer exists in the table and you cannot establish a new position for the bookmark, return MAPI_E_INVALID_BOOKMARK.</span></span> <span data-ttu-id="bf27f-142">Если строка, на которую указывает _бкоригин_ , больше не существует, и вы можете задать новую позицию для закладки, возвращайте MAPI_W_POSITION_CHANGED.</span><span class="sxs-lookup"><span data-stu-id="bf27f-142">If the row pointed to by  _bkOrigin_ no longer exists and you can establish a new position for the bookmark, return MAPI_W_POSITION_CHANGED.</span></span> 
  
<span data-ttu-id="bf27f-143">По-прежнему можно использовать закладку, указывающую на строку, свернутую в представлении таблицы.</span><span class="sxs-lookup"><span data-stu-id="bf27f-143">A bookmark pointing to a row that is collapsed out of the table view can still be used.</span></span> <span data-ttu-id="bf27f-144">Если вызывающий объект пытается переместить курсор на такую закладку, переместите курсор на следующую видимую строку и возвратите MAPI_W_POSITION_CHANGED.</span><span class="sxs-lookup"><span data-stu-id="bf27f-144">If the caller attempts to move the cursor to such a bookmark, move the cursor to the next visible row and return MAPI_W_POSITION_CHANGED.</span></span> 
  
<span data-ttu-id="bf27f-145">Можно переместить закладки для элементов, свернутых в представлении, в момент использования или во время свертывания строки.</span><span class="sxs-lookup"><span data-stu-id="bf27f-145">You can move bookmarks for positions collapsed out of view, either at the time of use or at the time that the row is collapsed.</span></span> <span data-ttu-id="bf27f-146">Если закладка перемещается в то время, когда строка свернута, сохраните бит в закладку, которая указывает на то, была ли эта закладка перемещена с момента ее последнего использования, или, если она никогда не использовалась, с момента ее создания.</span><span class="sxs-lookup"><span data-stu-id="bf27f-146">If a bookmark is moved at the time that the row is collapsed, keep a bit in the bookmark that indicates whether the bookmark has moved since its last use or, if it has never been used, since its creation.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="bf27f-147">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="bf27f-147">Notes to callers</span></span>

<span data-ttu-id="bf27f-148">Чтобы указать обратное перемещение для **сикров**, передайте отрицательное значение в _лровкаунт_.</span><span class="sxs-lookup"><span data-stu-id="bf27f-148">To indicate a backward move for **SeekRow**, pass a negative value in  _lRowCount_.</span></span> <span data-ttu-id="bf27f-149">Чтобы выполнить поиск в начале таблицы, в _лровкаунт_ передается ноль и значение BOOKMARK_BEGINNING в _бкоригин_.</span><span class="sxs-lookup"><span data-stu-id="bf27f-149">To search to the beginning of the table, pass zero in  _lRowCount_ and the value BOOKMARK_BEGINNING in  _bkOrigin_.</span></span> 
  
<span data-ttu-id="bf27f-150">Если в таблице много строк, операция **сикров** может быть медленной.</span><span class="sxs-lookup"><span data-stu-id="bf27f-150">If there are lots of rows in the table, the **SeekRow** operation can be slow.</span></span> <span data-ttu-id="bf27f-151">Кроме того, если необходимо вернуть количество строк в содержимом параметра _лплровссаугхт_ , это может повлиять на производительность.</span><span class="sxs-lookup"><span data-stu-id="bf27f-151">Performance can also be affected if you require a row count to be returned in the contents of the  _lplRowsSought_ parameter.</span></span> 
  
 <span data-ttu-id="bf27f-152">**Сикров** возвращает количество строк, на которые фактически выполнялось Поиск, положительное или отрицательное, в переменной, на которую указывает _лровкаунт_.</span><span class="sxs-lookup"><span data-stu-id="bf27f-152">**SeekRow** returns the number of rows actually searched through, positive or negative, in the variable pointed to by  _lRowCount_.</span></span> <span data-ttu-id="bf27f-153">В обычной операции она должна возвращать одно и то же значение для _лплровссаугхт_ , как было передано в _лровкаунт_, если поиск не достиг начала или конца таблицы.</span><span class="sxs-lookup"><span data-stu-id="bf27f-153">In ordinary operation, it should return the same value for  _lplRowsSought_ as passed in for  _lRowCount_, unless the search reached the beginning or end of the table.</span></span> 
  
<span data-ttu-id="bf27f-154">Не присвойте параметру _лровкаунт_ значение больше 50.</span><span class="sxs-lookup"><span data-stu-id="bf27f-154">Do not set  _lRowCount_ to a number greater than 50.</span></span> <span data-ttu-id="bf27f-155">Чтобы выполнить поиск по большему количеству строк, используйте метод [IMAPITable:: сикроваппрокс](imapitable-seekrowapprox.md) .</span><span class="sxs-lookup"><span data-stu-id="bf27f-155">To seek through a larger number of rows, use the [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="bf27f-156">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="bf27f-156">MFCMAPI reference</span></span>

<span data-ttu-id="bf27f-157">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="bf27f-157">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="bf27f-158">**Файл**</span><span class="sxs-lookup"><span data-stu-id="bf27f-158">**File**</span></span>|<span data-ttu-id="bf27f-159">**Функция**</span><span class="sxs-lookup"><span data-stu-id="bf27f-159">**Function**</span></span>|<span data-ttu-id="bf27f-160">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="bf27f-160">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bf27f-161">Мапипроцессор. cpp</span><span class="sxs-lookup"><span data-stu-id="bf27f-161">MAPIProcessor.cpp</span></span>  <br/> |<span data-ttu-id="bf27f-162">Кмапипроцессор::P Роцессмаилбокстабле</span><span class="sxs-lookup"><span data-stu-id="bf27f-162">CMAPIProcessor::ProcessMailboxTable</span></span>  <br/> |<span data-ttu-id="bf27f-163">MFCMAPI использует метод **IMAPITable:: сикров** для обнаружения начала таблицы перед обработкой.</span><span class="sxs-lookup"><span data-stu-id="bf27f-163">MFCMAPI uses the **IMAPITable::SeekRow** method to locate the beginning of the table before processing.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bf27f-164">См. также</span><span class="sxs-lookup"><span data-stu-id="bf27f-164">See also</span></span>



[<span data-ttu-id="bf27f-165">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="bf27f-165">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md)
  
[<span data-ttu-id="bf27f-166">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="bf27f-166">IMAPITable::FindRow</span></span>](imapitable-findrow.md)
  
[<span data-ttu-id="bf27f-167">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="bf27f-167">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="bf27f-168">IMAPITable::SeekRowApprox</span><span class="sxs-lookup"><span data-stu-id="bf27f-168">IMAPITable::SeekRowApprox</span></span>](imapitable-seekrowapprox.md)
  
[<span data-ttu-id="bf27f-169">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="bf27f-169">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="bf27f-170">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="bf27f-170">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

