---
title: IMAPIFolderEmptyFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.EmptyFolder
api_type:
- COM
ms.assetid: 4cfcb498-9182-4906-bd6f-d9bc387bc88b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 287577babc9a40b771aa9917211ba5dcbf8190ad
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584942"
---
# <a name="imapifolderemptyfolder"></a><span data-ttu-id="a4196-103">IMAPIFolder::EmptyFolder</span><span class="sxs-lookup"><span data-stu-id="a4196-103">IMAPIFolder::EmptyFolder</span></span>

  
  
<span data-ttu-id="a4196-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a4196-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a4196-105">Удаляет все сообщения и вложенные папки из папки без удаления самой папке.</span><span class="sxs-lookup"><span data-stu-id="a4196-105">Deletes all messages and subfolders from a folder without deleting the folder itself.</span></span>
  
```cpp
HRESULT EmptyFolder(
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="a4196-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a4196-106">Parameters</span></span>

 <span data-ttu-id="a4196-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="a4196-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="a4196-108">[in] Дескриптор родительского окна индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="a4196-108">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="a4196-109">Параметр _ulUIParam_ игнорируется, пока флаг FOLDER_DIALOG будет выполнен с помощью параметра _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="a4196-109">The  _ulUIParam_ parameter is ignored unless the FOLDER_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="a4196-110">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="a4196-110">_lpProgress_</span></span>
  
> <span data-ttu-id="a4196-111">[in] Указатель на объект хода выполнения, который отображает индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="a4196-111">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="a4196-112">Если в _lpProgress_передается значение NULL, поставщика хранилища сообщений отображает индикатор выполнения с помощью реализация объекта MAPI хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="a4196-112">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="a4196-113">Параметр _lpProgress_ игнорируется, пока флаг FOLDER_DIALOG будет выполнен с помощью параметра _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="a4196-113">The  _lpProgress_ parameter is ignored unless the FOLDER_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="a4196-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a4196-114">_ulFlags_</span></span>
  
> <span data-ttu-id="a4196-115">[in] Битовая маска флаги, который определяет, как папки.</span><span class="sxs-lookup"><span data-stu-id="a4196-115">[in] A bitmask of flags that controls how the folder is emptied.</span></span> <span data-ttu-id="a4196-116">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="a4196-116">The following flags can be set:</span></span>
    
<span data-ttu-id="a4196-117">DEL_ASSOCIATED</span><span class="sxs-lookup"><span data-stu-id="a4196-117">DEL_ASSOCIATED</span></span> 
  
> <span data-ttu-id="a4196-118">Удаляет все вложенные папки, включая вложенные папки, содержащие сообщения с связанный контент.</span><span class="sxs-lookup"><span data-stu-id="a4196-118">Deletes all subfolders, including subfolders that contain messages with associated content.</span></span> <span data-ttu-id="a4196-119">Флаг DEL_ASSOCIATED имеет значение только для папки верхнего уровня, которое обрабатывает вызов.</span><span class="sxs-lookup"><span data-stu-id="a4196-119">The DEL_ASSOCIATED flag has meaning only for the top-level folder the call acts on.</span></span>
    
<span data-ttu-id="a4196-120">DELETE_HARD_DELETE</span><span class="sxs-lookup"><span data-stu-id="a4196-120">DELETE_HARD_DELETE</span></span>
  
> <span data-ttu-id="a4196-121">Безвозвратно удаляет все сообщения, включая удаленные из них.</span><span class="sxs-lookup"><span data-stu-id="a4196-121">Permanently removes all messages, including soft-deleted ones.</span></span>
    
<span data-ttu-id="a4196-122">FOLDER_DIALOG</span><span class="sxs-lookup"><span data-stu-id="a4196-122">FOLDER_DIALOG</span></span> 
  
> <span data-ttu-id="a4196-123">Отображает индикатор хода выполнения во время операции.</span><span class="sxs-lookup"><span data-stu-id="a4196-123">Displays a progress indicator while the operation proceeds.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a4196-124">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="a4196-124">Return value</span></span>

<span data-ttu-id="a4196-125">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="a4196-125">S_OK</span></span> 
  
> <span data-ttu-id="a4196-126">Папка успешно очищается.</span><span class="sxs-lookup"><span data-stu-id="a4196-126">The folder was successfully emptied.</span></span>
    
<span data-ttu-id="a4196-127">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="a4196-127">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="a4196-128">Вызов завершился успешно, но папка не была полностью.</span><span class="sxs-lookup"><span data-stu-id="a4196-128">The call succeeded, but the folder was not completely emptied.</span></span> <span data-ttu-id="a4196-129">При возвращении этого предупреждения вызова необходимо обрабатывать об успешном завершении.</span><span class="sxs-lookup"><span data-stu-id="a4196-129">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="a4196-130">Чтобы проверить это предупреждение, используйте **HR_FAILED** макрос.</span><span class="sxs-lookup"><span data-stu-id="a4196-130">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="a4196-131">Дополнительные сведения можно [С помощью макросов для обработки ошибок](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="a4196-131">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a4196-132">Замечания</span><span class="sxs-lookup"><span data-stu-id="a4196-132">Remarks</span></span>

<span data-ttu-id="a4196-133">Метод **IMAPIFolder::EmptyFolder** удаляет все содержимое папки не удаляя саму папку.</span><span class="sxs-lookup"><span data-stu-id="a4196-133">The **IMAPIFolder::EmptyFolder** method deletes all of a folder's contents without deleting the folder itself.</span></span> 
  
<span data-ttu-id="a4196-134">Во время вызова **EmptyFolder** отправляемого сообщения не удаляются.</span><span class="sxs-lookup"><span data-stu-id="a4196-134">During an **EmptyFolder** call, submitted messages are not deleted.</span></span> 
  
<span data-ttu-id="a4196-135">Связанное содержимое папки включают сообщения, которые используются для описания представлений, правил, настраиваемых форм и хранение пользовательских решений, а также может включать определения формы.</span><span class="sxs-lookup"><span data-stu-id="a4196-135">A folder's associated contents include messages that are used to describe views, rules, custom forms, and custom solution storage, and can also include form definitions.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="a4196-136">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="a4196-136">Notes to implementers</span></span>

<span data-ttu-id="a4196-137">Не вызывайте метод [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) для сообщений в папке, которые были отправлены.</span><span class="sxs-lookup"><span data-stu-id="a4196-137">Do not call the [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) method for messages in the folder that have been submitted.</span></span> <span data-ttu-id="a4196-138">Отправленные сообщения не удаляются.</span><span class="sxs-lookup"><span data-stu-id="a4196-138">Submitted messages are not deleted.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a4196-139">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="a4196-139">Notes to callers</span></span>

<span data-ttu-id="a4196-140">Ожидается, что эти возвращаемые значения в следующих случаях.</span><span class="sxs-lookup"><span data-stu-id="a4196-140">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="a4196-141">**Условие**</span><span class="sxs-lookup"><span data-stu-id="a4196-141">**Condition**</span></span>|<span data-ttu-id="a4196-142">**������������ ��������**</span><span class="sxs-lookup"><span data-stu-id="a4196-142">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a4196-143">**EmptyFolder** успешно очистки папки.</span><span class="sxs-lookup"><span data-stu-id="a4196-143">**EmptyFolder** has successfully emptied the folder.</span></span>  <br/> |<span data-ttu-id="a4196-144">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="a4196-144">S_OK</span></span>  <br/> |
|<span data-ttu-id="a4196-145">**EmptyFolder** не удалось полностью очистить папку.</span><span class="sxs-lookup"><span data-stu-id="a4196-145">**EmptyFolder** was unable to completely empty the folder.</span></span>  <br/> |<span data-ttu-id="a4196-146">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="a4196-146">MAPI_W_PARTIAL_COMPLETION</span></span>  <br/> |
|<span data-ttu-id="a4196-147">**EmptyFolder** не удалось завершить.</span><span class="sxs-lookup"><span data-stu-id="a4196-147">**EmptyFolder** was unable to complete.</span></span>  <br/> |<span data-ttu-id="a4196-148">Любое значение ошибки</span><span class="sxs-lookup"><span data-stu-id="a4196-148">Any error value</span></span>  <br/> |
   
<span data-ttu-id="a4196-149">При **EmptyFolder** не удается завершить, не предполагают, что работа не выполнена.</span><span class="sxs-lookup"><span data-stu-id="a4196-149">When **EmptyFolder** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="a4196-150">**EmptyFolder** мог на удаление папки перед ошибок.</span><span class="sxs-lookup"><span data-stu-id="a4196-150">**EmptyFolder** might have been able to delete some of the folder's contents before encountering the error.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a4196-151">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="a4196-151">MFCMAPI reference</span></span>

<span data-ttu-id="a4196-152">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="a4196-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a4196-153">**����**</span><span class="sxs-lookup"><span data-stu-id="a4196-153">**File**</span></span>|<span data-ttu-id="a4196-154">**�������**</span><span class="sxs-lookup"><span data-stu-id="a4196-154">**Function**</span></span>|<span data-ttu-id="a4196-155">**�����������**</span><span class="sxs-lookup"><span data-stu-id="a4196-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a4196-156">MsgStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="a4196-156">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="a4196-157">CMsgStoreDlg::OnEmptyFolder</span><span class="sxs-lookup"><span data-stu-id="a4196-157">CMsgStoreDlg::OnEmptyFolder</span></span>  <br/> |<span data-ttu-id="a4196-158">Mfcmapi (en) использует метод **IMAPIFolder::EmptyFolder** для удаления содержимого указанной папки.</span><span class="sxs-lookup"><span data-stu-id="a4196-158">MFCMAPI uses the **IMAPIFolder::EmptyFolder** method to delete the contents of the specified folder.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a4196-159">См. также</span><span class="sxs-lookup"><span data-stu-id="a4196-159">See also</span></span>



[<span data-ttu-id="a4196-160">IMsgStore::AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="a4196-160">IMsgStore::AbortSubmit</span></span>](imsgstore-abortsubmit.md)
  
[<span data-ttu-id="a4196-161">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="a4196-161">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="a4196-162">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="a4196-162">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="a4196-163">Обработка ошибок с помощью макросов</span><span class="sxs-lookup"><span data-stu-id="a4196-163">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

