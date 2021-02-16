---
title: IMAPIFolderDeleteFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.DeleteFolder
api_type:
- COM
ms.assetid: 6c3e883c-80c0-4eda-8f81-8277d933a74b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a476607927f3563ede94a04ccfe4f7a3749c978e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417408"
---
# <a name="imapifolderdeletefolder"></a><span data-ttu-id="c1de2-103">IMAPIFolder::DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="c1de2-103">IMAPIFolder::DeleteFolder</span></span>

  
  
<span data-ttu-id="c1de2-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c1de2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c1de2-105">Удаляет в подсайт.</span><span class="sxs-lookup"><span data-stu-id="c1de2-105">Deletes a subfolder.</span></span>
  
```cpp
HRESULT DeleteFolder(
  ULONG_PTR cbEntryID,
  LPENTRYID lpEntryID,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="c1de2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c1de2-106">Parameters</span></span>

 <span data-ttu-id="c1de2-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="c1de2-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="c1de2-108">[in] Количество byte в идентификаторе записи, на который указывает параметр _lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="c1de2-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="c1de2-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="c1de2-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="c1de2-110">[in] Указатель на идентификатор записи в подкамере, который необходимо удалить.</span><span class="sxs-lookup"><span data-stu-id="c1de2-110">[in] A pointer to the entry identifier of the subfolder to delete.</span></span>
    
 <span data-ttu-id="c1de2-111">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="c1de2-111">_ulUIParam_</span></span>
  
> <span data-ttu-id="c1de2-112">[in] Handle to the parent window of the progress indicator.</span><span class="sxs-lookup"><span data-stu-id="c1de2-112">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="c1de2-113">Параметр  _ulUIParam_ игнорируется, если FOLDER_DIALOG в параметре  _ulFlags_ не задан флаг FOLDER_DIALOG.</span><span class="sxs-lookup"><span data-stu-id="c1de2-113">The  _ulUIParam_ parameter is ignored unless the FOLDER_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="c1de2-114">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="c1de2-114">_lpProgress_</span></span>
  
> <span data-ttu-id="c1de2-115">[in] Указатель на объект хода выполнения, который отображает индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="c1de2-115">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="c1de2-116">Если в  _lpProgress_ передается NULL, поставщик хранилище сообщений отображает индикатор хода выполнения с помощью реализации объекта хода выполнения MAPI.</span><span class="sxs-lookup"><span data-stu-id="c1de2-116">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="c1de2-117">Параметр _lpProgress_ игнорируется, если флаг FOLDER_DIALOG не установлен в _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="c1de2-117">The  _lpProgress_ parameter is ignored unless the FOLDER_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="c1de2-118">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c1de2-118">_ulFlags_</span></span>
  
> <span data-ttu-id="c1de2-119">[in] Битоваяmas флагов, которая управляет удалением вуза.</span><span class="sxs-lookup"><span data-stu-id="c1de2-119">[in] A bitmask of flags that controls the deletion of the subfolder.</span></span> <span data-ttu-id="c1de2-120">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="c1de2-120">The following flags can be set:</span></span>
    
<span data-ttu-id="c1de2-121">DEL_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="c1de2-121">DEL_FOLDERS</span></span> 
  
> <span data-ttu-id="c1de2-122">Все впапные в подпапки, на которые указывает  _lpEntryID,_ необходимо удалить.</span><span class="sxs-lookup"><span data-stu-id="c1de2-122">All subfolders of the subfolder pointed to by  _lpEntryID_ should be deleted.</span></span> 
    
<span data-ttu-id="c1de2-123">DEL_MESSAGES</span><span class="sxs-lookup"><span data-stu-id="c1de2-123">DEL_MESSAGES</span></span> 
  
> <span data-ttu-id="c1de2-124">Все сообщения в подпапке, на которые указывает  _lpEntryID,_ должны быть удалены.</span><span class="sxs-lookup"><span data-stu-id="c1de2-124">All messages in the subfolder pointed to by  _lpEntryID_ should be deleted.</span></span> 
    
<span data-ttu-id="c1de2-125">FOLDER_DIALOG</span><span class="sxs-lookup"><span data-stu-id="c1de2-125">FOLDER_DIALOG</span></span> 
  
> <span data-ttu-id="c1de2-126">Индикатор хода выполнения должен отображаться во время выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="c1de2-126">A progress indicator should be displayed while the operation proceeds.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c1de2-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c1de2-127">Return value</span></span>

<span data-ttu-id="c1de2-128">S_OK</span><span class="sxs-lookup"><span data-stu-id="c1de2-128">S_OK</span></span> 
  
> <span data-ttu-id="c1de2-129">Указанная папка успешно удалена.</span><span class="sxs-lookup"><span data-stu-id="c1de2-129">The specified folder has been successfully deleted.</span></span>
    
<span data-ttu-id="c1de2-130">MAPI_E_HAS_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="c1de2-130">MAPI_E_HAS_FOLDERS</span></span> 
  
> <span data-ttu-id="c1de2-131">В удаляемой в подкамере содержатся в том же DEL_FOLDERS, что и флаг DEL_FOLDERS не установлен.</span><span class="sxs-lookup"><span data-stu-id="c1de2-131">The subfolder being deleted contains subfolders, and the DEL_FOLDERS flag was not set.</span></span> <span data-ttu-id="c1de2-132">В подмайки не были удалены.</span><span class="sxs-lookup"><span data-stu-id="c1de2-132">The subfolders were not deleted.</span></span>
    
<span data-ttu-id="c1de2-133">MAPI_E_HAS_MESSAGES</span><span class="sxs-lookup"><span data-stu-id="c1de2-133">MAPI_E_HAS_MESSAGES</span></span> 
  
> <span data-ttu-id="c1de2-134">В удаляемой подкамере содержатся сообщения, флаг DEL_MESSAGES не установлен.</span><span class="sxs-lookup"><span data-stu-id="c1de2-134">The subfolder being deleted contains messages, and the DEL_MESSAGES flag was not set.</span></span> <span data-ttu-id="c1de2-135">Подкамерка не была удалена.</span><span class="sxs-lookup"><span data-stu-id="c1de2-135">The subfolder was not deleted.</span></span>
    
<span data-ttu-id="c1de2-136">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="c1de2-136">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="c1de2-137">Вызов был успешным, но не все записи были успешно удалены.</span><span class="sxs-lookup"><span data-stu-id="c1de2-137">The call succeeded, but not all of the entries were successfully deleted.</span></span> <span data-ttu-id="c1de2-138">При возвращении этого предупреждения вызов должен быть обработан как успешный.</span><span class="sxs-lookup"><span data-stu-id="c1de2-138">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="c1de2-139">Чтобы проверить это предупреждение, используйте **макрос HR_FAILED.**</span><span class="sxs-lookup"><span data-stu-id="c1de2-139">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="c1de2-140">Дополнительные сведения см. в [теме "Использование макроса для обработки ошибок".](using-macros-for-error-handling.md)</span><span class="sxs-lookup"><span data-stu-id="c1de2-140">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c1de2-141">Примечания</span><span class="sxs-lookup"><span data-stu-id="c1de2-141">Remarks</span></span>

<span data-ttu-id="c1de2-142">Метод **IMAPIFolder::D eleteFolder** удаляет впапную.</span><span class="sxs-lookup"><span data-stu-id="c1de2-142">The **IMAPIFolder::DeleteFolder** method deletes a subfolder.</span></span> <span data-ttu-id="c1de2-143">По умолчанию **DeleteFolder** работает только с пустыми папками, но его можно успешно использовать для непустых папок, установив два флага: DEL_FOLDERS и DEL_MESSAGES.</span><span class="sxs-lookup"><span data-stu-id="c1de2-143">By default, **DeleteFolder** operates only on empty folders, but you can use it successfully on non-empty folders by setting two flags: DEL_FOLDERS and DEL_MESSAGES.</span></span> <span data-ttu-id="c1de2-144">Удалять можно только пустые папки или папки, DEL_FOLDERS и DEL_MESSAGES флаги для вызова **DeleteFolder.**</span><span class="sxs-lookup"><span data-stu-id="c1de2-144">Only empty folders or folders that set both the DEL_FOLDERS and DEL_MESSAGES flags on the **DeleteFolder** call can be deleted.</span></span> <span data-ttu-id="c1de2-145">DEL_FOLDERS позволяет удалить все вложенные папки папки; DEL_MESSAGES позволяет удалять все сообщения папки.</span><span class="sxs-lookup"><span data-stu-id="c1de2-145">DEL_FOLDERS enables all of the folder's subfolders to be removed; DEL_MESSAGES enables all of the folder's messages to be removed.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="c1de2-146">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="c1de2-146">Notes to implementers</span></span>

<span data-ttu-id="c1de2-147">Если операция удаления включает несколько папок, выполните ее как можно точнее для каждой папки.</span><span class="sxs-lookup"><span data-stu-id="c1de2-147">When the delete operation involves more than one folder, perform the operation as completely as possible for each folder.</span></span> <span data-ttu-id="c1de2-148">Иногда одна из удаляемой папки не существует или была перемещена или скопирована в другое место.</span><span class="sxs-lookup"><span data-stu-id="c1de2-148">Sometimes one of the folders to be deleted does not exist or has been moved or copied elsewhere.</span></span> <span data-ttu-id="c1de2-149">Не останавливайте операцию раньше времени, если не произойдет сбой, который находится вне вашего контроля, например, если недостаточно памяти, недостаточно места на диске или не будет повреждения в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="c1de2-149">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="c1de2-150">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="c1de2-150">Notes to callers</span></span>

<span data-ttu-id="c1de2-151">Эти возвращаемые значения следует ожидать при следующих условиях.</span><span class="sxs-lookup"><span data-stu-id="c1de2-151">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="c1de2-152">**Condition**</span><span class="sxs-lookup"><span data-stu-id="c1de2-152">**Condition**</span></span>|<span data-ttu-id="c1de2-153">**Возвращаемое значение**</span><span class="sxs-lookup"><span data-stu-id="c1de2-153">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c1de2-154">**DeleteFolder** успешно удалил все сообщения и в подкамеру.</span><span class="sxs-lookup"><span data-stu-id="c1de2-154">**DeleteFolder** has successfully deleted every message and subfolder.</span></span>  <br/> |<span data-ttu-id="c1de2-155">S_OK</span><span class="sxs-lookup"><span data-stu-id="c1de2-155">S_OK</span></span>  <br/> |
|<span data-ttu-id="c1de2-156">**DeleteFolder** не удалось успешно удалить все сообщения и в подкамеру.</span><span class="sxs-lookup"><span data-stu-id="c1de2-156">**DeleteFolder** was unable to successfully delete every message and subfolder.</span></span>  <br/> |<span data-ttu-id="c1de2-157">MAPI_W_PARTIAL_COMPLETION или MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="c1de2-157">MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND</span></span>  <br/> |
|<span data-ttu-id="c1de2-158">**DeleteFolder** не удалось завершить.</span><span class="sxs-lookup"><span data-stu-id="c1de2-158">**DeleteFolder** was unable to complete.</span></span>  <br/> |<span data-ttu-id="c1de2-159">Любое значение ошибки, кроме MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="c1de2-159">Any error value except MAPI_E_NOT_FOUND</span></span>  <br/> |
   
<span data-ttu-id="c1de2-160">Если **deleteFolder** не удается завершить, не предполагайте, что никаких работ не было сделано.</span><span class="sxs-lookup"><span data-stu-id="c1de2-160">When **DeleteFolder** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="c1de2-161">**Возможно, deleteFolder** удалось удалить одно или несколько сообщений и вудерок, прежде чем столкнуться с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="c1de2-161">**DeleteFolder** might have been able to delete one or more of the messages and subfolders before encountering the error.</span></span> 
  
<span data-ttu-id="c1de2-162">Если не удается удалить одну или несколько ветвей, **DeleteFolder** возвращает MAPI_W_PARTIAL_COMPLETION или MAPI_E_NOT_FOUND в зависимости от реализации поставщика store сообщений.</span><span class="sxs-lookup"><span data-stu-id="c1de2-162">If one or more subfolders cannot be deleted, **DeleteFolder** returns MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND, depending on the message store provider's implementation.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="c1de2-163">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="c1de2-163">MFCMAPI reference</span></span>

<span data-ttu-id="c1de2-164">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="c1de2-164">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c1de2-165">**Файл**</span><span class="sxs-lookup"><span data-stu-id="c1de2-165">**File**</span></span>|<span data-ttu-id="c1de2-166">**Функция**</span><span class="sxs-lookup"><span data-stu-id="c1de2-166">**Function**</span></span>|<span data-ttu-id="c1de2-167">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="c1de2-167">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c1de2-168">MsgStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="c1de2-168">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="c1de2-169">CMsgStoreDlg::OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="c1de2-169">CMsgStoreDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="c1de2-170">MFCMAPI использует метод **IMAPIFolder::D eleteFolder** для удаления папок.</span><span class="sxs-lookup"><span data-stu-id="c1de2-170">MFCMAPI uses the **IMAPIFolder::DeleteFolder** method to delete folders.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c1de2-171">См. также</span><span class="sxs-lookup"><span data-stu-id="c1de2-171">See also</span></span>



[<span data-ttu-id="c1de2-172">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="c1de2-172">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="c1de2-173">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="c1de2-173">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

