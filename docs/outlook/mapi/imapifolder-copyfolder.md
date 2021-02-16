---
title: IMAPIFolderCopyFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.CopyFolder
api_type:
- COM
ms.assetid: 2c1c25c6-1aec-4d9e-a2a3-bf1b4a2908b8
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3d9c1e88b12baf50593212a3ae3c02907ce6617b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425661"
---
# <a name="imapifoldercopyfolder"></a><span data-ttu-id="aee45-103">IMAPIFolder::CopyFolder</span><span class="sxs-lookup"><span data-stu-id="aee45-103">IMAPIFolder::CopyFolder</span></span>

  
  
<span data-ttu-id="aee45-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aee45-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aee45-105">Копирует или перемещает в подсайт.</span><span class="sxs-lookup"><span data-stu-id="aee45-105">Copies or moves a subfolder.</span></span>
  
```cpp
HRESULT CopyFolder(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  LPVOID lpDestFolder,
  LPSTR lpszNewFolderName,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="aee45-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="aee45-106">Parameters</span></span>

 <span data-ttu-id="aee45-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="aee45-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="aee45-108">[in] Количество byte в идентификаторе записи, на который указывает параметр _lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="aee45-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="aee45-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="aee45-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="aee45-110">[in] Указатель на идентификатор записи в подкамере для копирования или перемещения.</span><span class="sxs-lookup"><span data-stu-id="aee45-110">[in] A pointer to the entry identifier of the subfolder to copy or move.</span></span>
    
 <span data-ttu-id="aee45-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="aee45-111">_lpInterface_</span></span>
  
> <span data-ttu-id="aee45-112">[in] Указатель на идентификатор интерфейса ( IID), который представляет интерфейс, используемый для доступа к папке, на которую указывает параметр _lpDestFolder._</span><span class="sxs-lookup"><span data-stu-id="aee45-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the folder that the  _lpDestFolder_ parameter points to.</span></span> <span data-ttu-id="aee45-113">Передача NULL приводит к возврату поставщиком услуг стандартного интерфейса папки [IMAPIFolder : IMAPIContainer.](imapifolderimapicontainer.md)</span><span class="sxs-lookup"><span data-stu-id="aee45-113">Passing NULL causes the service provider to return the standard folder interface, [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="aee45-114">Допустимые значения  _lpInterface_ включают IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer и IID_IMAPIFolder.</span><span class="sxs-lookup"><span data-stu-id="aee45-114">Valid values for  _lpInterface_ include IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer, and IID_IMAPIFolder.</span></span> 
    
 <span data-ttu-id="aee45-115">_lpDestFolder_</span><span class="sxs-lookup"><span data-stu-id="aee45-115">_lpDestFolder_</span></span>
  
> <span data-ttu-id="aee45-116">[in] Указатель на открытую папку для получения скопированной или перемещенной вложенной папки.</span><span class="sxs-lookup"><span data-stu-id="aee45-116">[in] A pointer to the open folder to receive the copied or moved subfolder.</span></span>
    
 <span data-ttu-id="aee45-117">_lpszNewFolderName_</span><span class="sxs-lookup"><span data-stu-id="aee45-117">_lpszNewFolderName_</span></span>
  
> <span data-ttu-id="aee45-118">[in] Указатель на имя скопированной или перемещенной папки в новом месте назначения.</span><span class="sxs-lookup"><span data-stu-id="aee45-118">[in] A pointer to the name of the copied or moved folder in its new destination.</span></span> <span data-ttu-id="aee45-119">Если  _lpszNewFolderName_ имеет NULL, имя вложенной папки источника используется для имени конечной папки.</span><span class="sxs-lookup"><span data-stu-id="aee45-119">If  _lpszNewFolderName_ is set to NULL, the name of the source subfolder is used for the name of the destination folder.</span></span> 
    
 <span data-ttu-id="aee45-120">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="aee45-120">_ulUIParam_</span></span>
  
> <span data-ttu-id="aee45-121">[in] Handle to the parent window of the progress indicator.</span><span class="sxs-lookup"><span data-stu-id="aee45-121">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="aee45-122">Параметр _ulUIParam_ игнорируется, если FOLDER_DIALOG флага в параметре _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="aee45-122">The  _ulUIParam_ parameter is ignored unless the FOLDER_DIALOG flag in the  _ulFlags_ parameter is set.</span></span> 
    
 <span data-ttu-id="aee45-123">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="aee45-123">_lpProgress_</span></span>
  
> <span data-ttu-id="aee45-124">[in] Указатель на объект хода выполнения, который отображает индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="aee45-124">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="aee45-125">Если в  _lpProgress_ передается NULL, поставщик хранилище сообщений отображает индикатор хода выполнения с помощью реализации объекта хода выполнения MAPI.</span><span class="sxs-lookup"><span data-stu-id="aee45-125">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="aee45-126">Параметр _lpProgress_ игнорируется, если флаг FOLDER_DIALOG не установлен в _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="aee45-126">The  _lpProgress_ parameter is ignored unless the FOLDER_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="aee45-127">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="aee45-127">_ulFlags_</span></span>
  
> <span data-ttu-id="aee45-128">[in] Битоваяmas флагов, которая управляет операцией копирования или перемещения.</span><span class="sxs-lookup"><span data-stu-id="aee45-128">[in] A bitmask of flags that controls the copy or move operation.</span></span> <span data-ttu-id="aee45-129">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="aee45-129">The following flags can be set:</span></span>
    
<span data-ttu-id="aee45-130">COPY_SUBFOLDERS</span><span class="sxs-lookup"><span data-stu-id="aee45-130">COPY_SUBFOLDERS</span></span> 
  
> <span data-ttu-id="aee45-131">Также следует скопировать все в подкамеры во вкопированную в нее.</span><span class="sxs-lookup"><span data-stu-id="aee45-131">All of the subfolders in the subfolder to be copied should also be copied.</span></span> <span data-ttu-id="aee45-132">Если COPY_SUBFOLDERS не задан для операции копирования, копируется только подпапка, заданная _lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="aee45-132">When COPY_SUBFOLDERS is not set for a copy operation, only the subfolder identified by  _lpEntryID_ is copied.</span></span> <span data-ttu-id="aee45-133">При операции перемещения поведение COPY_SUBFOLDERS по умолчанию независимо от того, установлен ли флаг.</span><span class="sxs-lookup"><span data-stu-id="aee45-133">With a move operation, the COPY_SUBFOLDERS behavior is the default regardless of whether the flag is set.</span></span> 
    
<span data-ttu-id="aee45-134">FOLDER_DIALOG</span><span class="sxs-lookup"><span data-stu-id="aee45-134">FOLDER_DIALOG</span></span> 
  
> <span data-ttu-id="aee45-135">Запрашивает отображение индикатора хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="aee45-135">Requests the display of a progress indicator.</span></span>
    
<span data-ttu-id="aee45-136">FOLDER_MOVE</span><span class="sxs-lookup"><span data-stu-id="aee45-136">FOLDER_MOVE</span></span> 
  
> <span data-ttu-id="aee45-137">В нее необходимо не копировать, а перемещаемую в нее ветвь.</span><span class="sxs-lookup"><span data-stu-id="aee45-137">The subfolder is to be moved instead of copied.</span></span> <span data-ttu-id="aee45-138">Если FOLDER_MOVE не установлен, подкамера копируется.</span><span class="sxs-lookup"><span data-stu-id="aee45-138">If FOLDER_MOVE is not set, the subfolder is copied.</span></span>
    
<span data-ttu-id="aee45-139">MAPI_DECLINE_OK</span><span class="sxs-lookup"><span data-stu-id="aee45-139">MAPI_DECLINE_OK</span></span> 
  
> <span data-ttu-id="aee45-140">Сообщает поставщику хранения сообщений, что если он реализует **CopyFolder,** вызывая метод [IMAPISupport::D oCopyTo](imapisupport-docopyto.md) или [IMAPISupport::D oCopyProps,](imapisupport-docopyprops.md) **CopyFolder** должен немедленно вернуть MAPI_E_DECLINE_COPY.</span><span class="sxs-lookup"><span data-stu-id="aee45-140">Informs the message store provider that if it implements **CopyFolder** by calling its support object's [IMAPISupport::DoCopyTo](imapisupport-docopyto.md) or [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md) method, **CopyFolder** should instead immediately return MAPI_E_DECLINE_COPY.</span></span> 
    
<span data-ttu-id="aee45-141">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="aee45-141">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="aee45-142">Имя конечной папки имеет формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="aee45-142">The name of the destination folder is in Unicode format.</span></span> <span data-ttu-id="aee45-143">Если флаг MAPI_UNICODE не установлен, имя папки будет в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="aee45-143">If the MAPI_UNICODE flag is not set, the folder name is in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="aee45-144">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="aee45-144">Return value</span></span>

<span data-ttu-id="aee45-145">S_OK</span><span class="sxs-lookup"><span data-stu-id="aee45-145">S_OK</span></span> 
  
> <span data-ttu-id="aee45-146">Указанная папка успешно скопирована или перемещена.</span><span class="sxs-lookup"><span data-stu-id="aee45-146">The specified folder has been successfully copied or moved.</span></span>
    
<span data-ttu-id="aee45-147">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="aee45-147">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="aee45-148">Либо флаг MAPI_UNICODE установлен, а поставщик юникод не поддерживает Юникод, либо MAPI_UNICODE не установлен, а поставщик магазина сообщений поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="aee45-148">Either the MAPI_UNICODE flag was set and the message store provider does not support Unicode, or MAPI_UNICODE was not set and the message store provider supports only Unicode.</span></span>
    
<span data-ttu-id="aee45-149">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="aee45-149">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="aee45-150">Имя перемещаемой или копируется папки так же, как и имя вложенной папки в конечной папке.</span><span class="sxs-lookup"><span data-stu-id="aee45-150">The name of the folder being moved or copied is the same as that of a subfolder in the destination folder.</span></span> <span data-ttu-id="aee45-151">Поставщику store сообщений требуются уникальные имена папок.</span><span class="sxs-lookup"><span data-stu-id="aee45-151">The message store provider requires unique folder names.</span></span>
    
<span data-ttu-id="aee45-152">MAPI_E_DECLINE_COPY</span><span class="sxs-lookup"><span data-stu-id="aee45-152">MAPI_E_DECLINE_COPY</span></span> 
  
> <span data-ttu-id="aee45-153">Поставщик реализует этот метод, вызывая метод объекта поддержки, и вызываемая стороны передает флаг MAPI_DECLINE_OK.</span><span class="sxs-lookup"><span data-stu-id="aee45-153">The provider implements this method by calling a support object method, and the caller has passed the MAPI_DECLINE_OK flag.</span></span>
    
<span data-ttu-id="aee45-154">MAPI_E_FOLDER_CYCLE</span><span class="sxs-lookup"><span data-stu-id="aee45-154">MAPI_E_FOLDER_CYCLE</span></span> 
  
> <span data-ttu-id="aee45-155">Папка источника напрямую или косвенно содержит папку назначения.</span><span class="sxs-lookup"><span data-stu-id="aee45-155">The source folder directly or indirectly contains the destination folder.</span></span> <span data-ttu-id="aee45-156">Перед обнаружением этого условия могли быть выполнены значительные трудоемкие работы, поэтому папка источника и назначения может быть частично изменена.</span><span class="sxs-lookup"><span data-stu-id="aee45-156">Significant work may have been performed before this condition was discovered, so the source and destination folder may be partially modified.</span></span> 
    
<span data-ttu-id="aee45-157">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="aee45-157">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="aee45-158">Вызов был успешным, но не все записи были успешно скопированы.</span><span class="sxs-lookup"><span data-stu-id="aee45-158">The call succeeded, but not all entries were successfully copied.</span></span> <span data-ttu-id="aee45-159">При возврате этого предупреждения вызов должен быть обработан как успешный.</span><span class="sxs-lookup"><span data-stu-id="aee45-159">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="aee45-160">Чтобы проверить это предупреждение, используйте **макрос** HR_FAILED.</span><span class="sxs-lookup"><span data-stu-id="aee45-160">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="aee45-161">Дополнительные сведения см. в теме ["Использование макроса для обработки ошибок".](using-macros-for-error-handling.md)</span><span class="sxs-lookup"><span data-stu-id="aee45-161">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="aee45-162">Примечания</span><span class="sxs-lookup"><span data-stu-id="aee45-162">Remarks</span></span>

<span data-ttu-id="aee45-163">Метод **IMAPIFolder::CopyFolder** копирует или перемещает вложение из одного расположения в другое.</span><span class="sxs-lookup"><span data-stu-id="aee45-163">The **IMAPIFolder::CopyFolder** method copies or moves a subfolder from one location to another.</span></span> <span data-ttu-id="aee45-164">Вложенная папка, скопированная или перемещенная, добавляется в пунктов назначения в качестве вложенной папки.</span><span class="sxs-lookup"><span data-stu-id="aee45-164">The subfolder being copied or moved is added to the destination folder as a subfolder.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="aee45-165">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="aee45-165">Notes to implementers</span></span>

<span data-ttu-id="aee45-166">Если операция копирования или перемещения включает несколько папок, как указано при установке флага COPY_SUBFOLDERS, выполните операцию для каждой папки максимально возможно.</span><span class="sxs-lookup"><span data-stu-id="aee45-166">When the copy or move operation involves more than one folder, as indicated by setting the COPY_SUBFOLDERS flag, perform the operation as completely as possible for each folder.</span></span> <span data-ttu-id="aee45-167">Иногда одна из перемещаемой или копируется папки не существует или уже была перемещена или скопирована в другое место.</span><span class="sxs-lookup"><span data-stu-id="aee45-167">Sometimes one of the folders to be moved or copied does not exist or has already been moved or copied elsewhere.</span></span> <span data-ttu-id="aee45-168">Не останавливайте операцию раньше времени, если не произойдет сбой, который находится вне вашего контроля, например, если недостаточно памяти, недостаточно места на диске или не будет повреждения в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="aee45-168">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span>
  
<span data-ttu-id="aee45-169">Попытайтесь сохранить все идентификаторы записей сообщений в скопированные сообщения.</span><span class="sxs-lookup"><span data-stu-id="aee45-169">Try to retain all message entry identifiers in the copied messages.</span></span> <span data-ttu-id="aee45-170">Также следует попытаться сохранить идентификаторы записей, но это не требуется.</span><span class="sxs-lookup"><span data-stu-id="aee45-170">You should also try to preserve entry identifiers, but it is not required.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="aee45-171">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="aee45-171">Notes to callers</span></span>

<span data-ttu-id="aee45-172">Эти возвращаемые значения следует ожидать при следующих условиях.</span><span class="sxs-lookup"><span data-stu-id="aee45-172">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="aee45-173">**Condition**</span><span class="sxs-lookup"><span data-stu-id="aee45-173">**Condition**</span></span>|<span data-ttu-id="aee45-174">**Возвращаемое значение**</span><span class="sxs-lookup"><span data-stu-id="aee45-174">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="aee45-175">**CopyFolder** успешно скопировал или переместил каждое сообщение и в подчиненную копию.</span><span class="sxs-lookup"><span data-stu-id="aee45-175">**CopyFolder** has successfully copied or moved every message and subfolder.</span></span>  <br/> |<span data-ttu-id="aee45-176">S_OK</span><span class="sxs-lookup"><span data-stu-id="aee45-176">S_OK</span></span>  <br/> |
|<span data-ttu-id="aee45-177">**CopyFolder** не удалось успешно скопировать или переместить все сообщения и в подкамеру.</span><span class="sxs-lookup"><span data-stu-id="aee45-177">**CopyFolder** was unable to successfully copy or move every message and subfolder.</span></span>  <br/> |<span data-ttu-id="aee45-178">MAPI_W_PARTIAL_COMPLETION или MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="aee45-178">MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND</span></span>  <br/> |
|<span data-ttu-id="aee45-179">**CopyFolder** не удалось завершить.</span><span class="sxs-lookup"><span data-stu-id="aee45-179">**CopyFolder** was unable to complete.</span></span>  <br/> |<span data-ttu-id="aee45-180">Любое значение ошибки, кроме MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="aee45-180">Any error value except MAPI_E_NOT_FOUND</span></span>  <br/> |
   
<span data-ttu-id="aee45-181">Если **copyFolder** не удается завершить, не предполагать, что никаких работ не было сделано.</span><span class="sxs-lookup"><span data-stu-id="aee45-181">When **CopyFolder** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="aee45-182">**Возможно, copyFolder** мог скопировать или переместить одно или несколько сообщений и вудерок, прежде чем столкнуться с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="aee45-182">**CopyFolder** might have been able to copy or move one or more of the messages and subfolders before encountering the error.</span></span> 
  
<span data-ttu-id="aee45-183">Если идентификатор записи для папки, которая не существует, передается в  _lpEntryID,_ **CopyFolder** возвращает MAPI_W_PARTIAL_COMPLETION или MAPI_E_NOT_FOUND в зависимости от реализации в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="aee45-183">If an entry identifier for a folder that does not exist is passed in  _lpEntryID_, **CopyFolder** returns MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND, depending on the message store's implementation.</span></span> 
  
<span data-ttu-id="aee45-184">В зависимости от поставщика службы хранения сообщений идентификатор записи исходного сообщения может быть сохранен или не сохранен в скопированном сообщении.</span><span class="sxs-lookup"><span data-stu-id="aee45-184">Depending on the message store provider, the entry identifier of the original message may or may not be preserved in the copied message.</span></span> <span data-ttu-id="aee45-185">Идентификаторы записей следует сохранять, когда это возможно, но это не обязательно.</span><span class="sxs-lookup"><span data-stu-id="aee45-185">You should preserve entry identifiers whenever possible, but it is not a requirement.</span></span> <span data-ttu-id="aee45-186">Как правило, можно зависеть от следующих сценариев:</span><span class="sxs-lookup"><span data-stu-id="aee45-186">You can generally depend on the following scenarios:</span></span>
  
- <span data-ttu-id="aee45-187">При изменении папки между двумя различными типами хранилищ сообщений идентификатор записи гарантированно меняется.</span><span class="sxs-lookup"><span data-stu-id="aee45-187">When you move a folder between two different types of message stores, the entry identifier is guaranteed to change.</span></span>
    
- <span data-ttu-id="aee45-188">При перемещение папки между двумя хранилищами сообщений одного типа идентификатор записи почти всегда изменяется.</span><span class="sxs-lookup"><span data-stu-id="aee45-188">When you move a folder between two message stores of the same type, the entry identifier almost always changes.</span></span>
    
- <span data-ttu-id="aee45-189">При изменении папки в другое расположение в том же хранилище сообщений идентификатор записи может изменяться или не изменяться в зависимости от поставщика.</span><span class="sxs-lookup"><span data-stu-id="aee45-189">When you move a folder to another location in the same message store, the entry identifier may or may not change, depending on the message store provider.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="aee45-190">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="aee45-190">MFCMAPI reference</span></span>

<span data-ttu-id="aee45-191">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="aee45-191">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="aee45-192">**Файл**</span><span class="sxs-lookup"><span data-stu-id="aee45-192">**File**</span></span>|<span data-ttu-id="aee45-193">**Функция**</span><span class="sxs-lookup"><span data-stu-id="aee45-193">**Function**</span></span>|<span data-ttu-id="aee45-194">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="aee45-194">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="aee45-195">MsgStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="aee45-195">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="aee45-196">CMsgStoreDlg::OnPasteFolder</span><span class="sxs-lookup"><span data-stu-id="aee45-196">CMsgStoreDlg::OnPasteFolder</span></span>  <br/> |<span data-ttu-id="aee45-197">MFCMAPI использует метод **IMAPIFolder::CopyFolder** для копирования папок из одного расположения в другое.</span><span class="sxs-lookup"><span data-stu-id="aee45-197">MFCMAPI uses the **IMAPIFolder::CopyFolder** method to copy folders from one location to another.</span></span> <span data-ttu-id="aee45-198">MFCMAPI запоминает исходные папки во время операции копирования и фактически выполняет копирование во время операции вкладки.</span><span class="sxs-lookup"><span data-stu-id="aee45-198">MFCMAPI remembers the source folder during the copy operation and actually performs the copy during the paste operation.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="aee45-199">См. также</span><span class="sxs-lookup"><span data-stu-id="aee45-199">See also</span></span>



[<span data-ttu-id="aee45-200">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="aee45-200">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="aee45-201">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="aee45-201">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

