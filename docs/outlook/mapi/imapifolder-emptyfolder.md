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
ms.openlocfilehash: 4ca828c3e03cbff886230f2af63485f7b15e8b35
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416785"
---
# <a name="imapifolderemptyfolder"></a><span data-ttu-id="2d3f2-103">IMAPIFolder::EmptyFolder</span><span class="sxs-lookup"><span data-stu-id="2d3f2-103">IMAPIFolder::EmptyFolder</span></span>

  
  
<span data-ttu-id="2d3f2-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2d3f2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2d3f2-105">Удаляет все сообщения и подмостки из папки без удаления самой папки.</span><span class="sxs-lookup"><span data-stu-id="2d3f2-105">Deletes all messages and subfolders from a folder without deleting the folder itself.</span></span>
  
```cpp
HRESULT EmptyFolder(
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="2d3f2-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="2d3f2-106">Parameters</span></span>

 <span data-ttu-id="2d3f2-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="2d3f2-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="2d3f2-108">[in] Ручка родительского окна индикатора прогресса.</span><span class="sxs-lookup"><span data-stu-id="2d3f2-108">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="2d3f2-109">Параметр _ulUIParam_ игнорируется, если флаг FOLDER_DIALOG в параметре _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="2d3f2-109">The  _ulUIParam_ parameter is ignored unless the FOLDER_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="2d3f2-110">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="2d3f2-110">_lpProgress_</span></span>
  
> <span data-ttu-id="2d3f2-111">[in] Указатель на объект progress, отображает индикатор прогресса.</span><span class="sxs-lookup"><span data-stu-id="2d3f2-111">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="2d3f2-112">Если NULL передается в  _lpProgress,_ поставщик магазина сообщений отображает индикатор прогресса с помощью реализации объекта progress MAPI.</span><span class="sxs-lookup"><span data-stu-id="2d3f2-112">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="2d3f2-113">Параметр _lpProgress_ игнорируется, если флаг FOLDER_DIALOG в параметре _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="2d3f2-113">The  _lpProgress_ parameter is ignored unless the FOLDER_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="2d3f2-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2d3f2-114">_ulFlags_</span></span>
  
> <span data-ttu-id="2d3f2-115">[in] Битмашка флагов, контролирующих, как очищается папка.</span><span class="sxs-lookup"><span data-stu-id="2d3f2-115">[in] A bitmask of flags that controls how the folder is emptied.</span></span> <span data-ttu-id="2d3f2-116">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="2d3f2-116">The following flags can be set:</span></span>
    
<span data-ttu-id="2d3f2-117">DEL_ASSOCIATED</span><span class="sxs-lookup"><span data-stu-id="2d3f2-117">DEL_ASSOCIATED</span></span> 
  
> <span data-ttu-id="2d3f2-118">Удаляет все подмостки, включая подмостки, содержащие сообщения со связанным содержимым.</span><span class="sxs-lookup"><span data-stu-id="2d3f2-118">Deletes all subfolders, including subfolders that contain messages with associated content.</span></span> <span data-ttu-id="2d3f2-119">Флаг DEL_ASSOCIATED имеет значение только для папки верхнего уровня, на которая действует вызов.</span><span class="sxs-lookup"><span data-stu-id="2d3f2-119">The DEL_ASSOCIATED flag has meaning only for the top-level folder the call acts on.</span></span>
    
<span data-ttu-id="2d3f2-120">DELETE_HARD_DELETE</span><span class="sxs-lookup"><span data-stu-id="2d3f2-120">DELETE_HARD_DELETE</span></span>
  
> <span data-ttu-id="2d3f2-121">Постоянно удаляет все сообщения, в том числе удаленные с мягкими сообщениями.</span><span class="sxs-lookup"><span data-stu-id="2d3f2-121">Permanently removes all messages, including soft-deleted ones.</span></span>
    
<span data-ttu-id="2d3f2-122">FOLDER_DIALOG</span><span class="sxs-lookup"><span data-stu-id="2d3f2-122">FOLDER_DIALOG</span></span> 
  
> <span data-ttu-id="2d3f2-123">Отображает индикатор прогресса во время выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="2d3f2-123">Displays a progress indicator while the operation proceeds.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2d3f2-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2d3f2-124">Return value</span></span>

<span data-ttu-id="2d3f2-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="2d3f2-125">S_OK</span></span> 
  
> <span data-ttu-id="2d3f2-126">Папка успешно опустошалась.</span><span class="sxs-lookup"><span data-stu-id="2d3f2-126">The folder was successfully emptied.</span></span>
    
<span data-ttu-id="2d3f2-127">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="2d3f2-127">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="2d3f2-128">Вызов удался, но папка не была полностью очищена.</span><span class="sxs-lookup"><span data-stu-id="2d3f2-128">The call succeeded, but the folder was not completely emptied.</span></span> <span data-ttu-id="2d3f2-129">Когда это предупреждение возвращается, вызов должен быть обработан как успешный.</span><span class="sxs-lookup"><span data-stu-id="2d3f2-129">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="2d3f2-130">Чтобы проверить это предупреждение, используйте **HR_FAILED** макрос.</span><span class="sxs-lookup"><span data-stu-id="2d3f2-130">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="2d3f2-131">Дополнительные сведения см. в [дополнительных сведениях Об использовании макроса для обработки ошибок.](using-macros-for-error-handling.md)</span><span class="sxs-lookup"><span data-stu-id="2d3f2-131">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2d3f2-132">Примечания</span><span class="sxs-lookup"><span data-stu-id="2d3f2-132">Remarks</span></span>

<span data-ttu-id="2d3f2-133">Метод **IMAPIFolder::EmptyFolder** удаляет все содержимое папки без удаления самой папки.</span><span class="sxs-lookup"><span data-stu-id="2d3f2-133">The **IMAPIFolder::EmptyFolder** method deletes all of a folder's contents without deleting the folder itself.</span></span> 
  
<span data-ttu-id="2d3f2-134">Во время **вызова EmptyFolder** отправленные сообщения не удаляются.</span><span class="sxs-lookup"><span data-stu-id="2d3f2-134">During an **EmptyFolder** call, submitted messages are not deleted.</span></span> 
  
<span data-ttu-id="2d3f2-135">Связанное содержимое папки включает сообщения, которые используются для описания представлений, правил, настраиваемой формы и хранения настраиваемого решения, а также могут включать определения форм.</span><span class="sxs-lookup"><span data-stu-id="2d3f2-135">A folder's associated contents include messages that are used to describe views, rules, custom forms, and custom solution storage, and can also include form definitions.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="2d3f2-136">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="2d3f2-136">Notes to implementers</span></span>

<span data-ttu-id="2d3f2-137">Не вызывай [метод IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) для сообщений в отправленной папке.</span><span class="sxs-lookup"><span data-stu-id="2d3f2-137">Do not call the [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) method for messages in the folder that have been submitted.</span></span> <span data-ttu-id="2d3f2-138">Отправленные сообщения не удаляются.</span><span class="sxs-lookup"><span data-stu-id="2d3f2-138">Submitted messages are not deleted.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="2d3f2-139">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="2d3f2-139">Notes to callers</span></span>

<span data-ttu-id="2d3f2-140">Ожидайте этих значений возврата в следующих условиях.</span><span class="sxs-lookup"><span data-stu-id="2d3f2-140">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="2d3f2-141">**Condition**</span><span class="sxs-lookup"><span data-stu-id="2d3f2-141">**Condition**</span></span>|<span data-ttu-id="2d3f2-142">**Возвращаемое значение**</span><span class="sxs-lookup"><span data-stu-id="2d3f2-142">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2d3f2-143">**EmptyFolder** успешно опорожняет папку.</span><span class="sxs-lookup"><span data-stu-id="2d3f2-143">**EmptyFolder** has successfully emptied the folder.</span></span>  <br/> |<span data-ttu-id="2d3f2-144">S_OK</span><span class="sxs-lookup"><span data-stu-id="2d3f2-144">S_OK</span></span>  <br/> |
|<span data-ttu-id="2d3f2-145">**EmptyFolder** не смог полностью очистить папку.</span><span class="sxs-lookup"><span data-stu-id="2d3f2-145">**EmptyFolder** was unable to completely empty the folder.</span></span>  <br/> |<span data-ttu-id="2d3f2-146">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="2d3f2-146">MAPI_W_PARTIAL_COMPLETION</span></span>  <br/> |
|<span data-ttu-id="2d3f2-147">**EmptyFolder** не удалось выполнить.</span><span class="sxs-lookup"><span data-stu-id="2d3f2-147">**EmptyFolder** was unable to complete.</span></span>  <br/> |<span data-ttu-id="2d3f2-148">Любое значение ошибки</span><span class="sxs-lookup"><span data-stu-id="2d3f2-148">Any error value</span></span>  <br/> |
   
<span data-ttu-id="2d3f2-149">Если **EmptyFolder** не удается выполнить, не думайте, что работа не была сделана.</span><span class="sxs-lookup"><span data-stu-id="2d3f2-149">When **EmptyFolder** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="2d3f2-150">**EmptyFolder,** возможно, удалось удалить часть содержимого папки, прежде чем столкнуться с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="2d3f2-150">**EmptyFolder** might have been able to delete some of the folder's contents before encountering the error.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="2d3f2-151">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="2d3f2-151">MFCMAPI reference</span></span>

<span data-ttu-id="2d3f2-152">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="2d3f2-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="2d3f2-153">**Файл**</span><span class="sxs-lookup"><span data-stu-id="2d3f2-153">**File**</span></span>|<span data-ttu-id="2d3f2-154">**Функция**</span><span class="sxs-lookup"><span data-stu-id="2d3f2-154">**Function**</span></span>|<span data-ttu-id="2d3f2-155">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="2d3f2-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2d3f2-156">MsgStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="2d3f2-156">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="2d3f2-157">CMsgStoreDlg::OnEmptyFolder</span><span class="sxs-lookup"><span data-stu-id="2d3f2-157">CMsgStoreDlg::OnEmptyFolder</span></span>  <br/> |<span data-ttu-id="2d3f2-158">MFCMAPI использует **метод IMAPIFolder::EmptyFolder** для удаления содержимого указанной папки.</span><span class="sxs-lookup"><span data-stu-id="2d3f2-158">MFCMAPI uses the **IMAPIFolder::EmptyFolder** method to delete the contents of the specified folder.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2d3f2-159">См. также</span><span class="sxs-lookup"><span data-stu-id="2d3f2-159">See also</span></span>



[<span data-ttu-id="2d3f2-160">IMsgStore::AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="2d3f2-160">IMsgStore::AbortSubmit</span></span>](imsgstore-abortsubmit.md)
  
[<span data-ttu-id="2d3f2-161">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="2d3f2-161">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="2d3f2-162">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="2d3f2-162">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="2d3f2-163">Использование макроса для обработки ошибок</span><span class="sxs-lookup"><span data-stu-id="2d3f2-163">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

