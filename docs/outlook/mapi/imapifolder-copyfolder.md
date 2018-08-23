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
ms.openlocfilehash: 134a492dbc86dd0ce6b3795d5ae40b334c14d468
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585152"
---
# <a name="imapifoldercopyfolder"></a><span data-ttu-id="0c9e4-103">IMAPIFolder::CopyFolder</span><span class="sxs-lookup"><span data-stu-id="0c9e4-103">IMAPIFolder::CopyFolder</span></span>

  
  
<span data-ttu-id="0c9e4-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0c9e4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0c9e4-105">Копирование или перемещение вложенной папке.</span><span class="sxs-lookup"><span data-stu-id="0c9e4-105">Copies or moves a subfolder.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="0c9e4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0c9e4-106">Parameters</span></span>

 <span data-ttu-id="0c9e4-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="0c9e4-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="0c9e4-108">[in] Число байтов в идентификатор записи, на который указывает параметр _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="0c9e4-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="0c9e4-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="0c9e4-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="0c9e4-110">[in] Указатель на идентификатор записи вложенной папки для копирования или перемещения.</span><span class="sxs-lookup"><span data-stu-id="0c9e4-110">[in] A pointer to the entry identifier of the subfolder to copy or move.</span></span>
    
 <span data-ttu-id="0c9e4-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="0c9e4-111">_lpInterface_</span></span>
  
> <span data-ttu-id="0c9e4-112">[in] Указатель на идентификатор интерфейса (ИД интерфейса), который представляет интерфейс, который будет использоваться для доступа к папке, которую указывает параметр _lpDestFolder_ .</span><span class="sxs-lookup"><span data-stu-id="0c9e4-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the folder that the  _lpDestFolder_ parameter points to.</span></span> <span data-ttu-id="0c9e4-113">Значение NULL вызывает поставщика услуг для возврата интерфейсе стандартные папки [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="0c9e4-113">Passing NULL causes the service provider to return the standard folder interface, [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="0c9e4-114">Допустимые значения для _lpInterface_ — IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer и IID_IMAPIFolder.</span><span class="sxs-lookup"><span data-stu-id="0c9e4-114">Valid values for  _lpInterface_ include IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer, and IID_IMAPIFolder.</span></span> 
    
 <span data-ttu-id="0c9e4-115">_lpDestFolder_</span><span class="sxs-lookup"><span data-stu-id="0c9e4-115">_lpDestFolder_</span></span>
  
> <span data-ttu-id="0c9e4-116">[in] Указатель открыть папку для получения вложенной папке копируемые или перемещения.</span><span class="sxs-lookup"><span data-stu-id="0c9e4-116">[in] A pointer to the open folder to receive the copied or moved subfolder.</span></span>
    
 <span data-ttu-id="0c9e4-117">_lpszNewFolderName_</span><span class="sxs-lookup"><span data-stu-id="0c9e4-117">_lpszNewFolderName_</span></span>
  
> <span data-ttu-id="0c9e4-118">[in] Указатель на имя папки копируемые или перемещения в поле нового назначения.</span><span class="sxs-lookup"><span data-stu-id="0c9e4-118">[in] A pointer to the name of the copied or moved folder in its new destination.</span></span> <span data-ttu-id="0c9e4-119">Если _lpszNewFolderName_ имеет значение NULL, имя вложенной папке источника используется для имени папки назначения.</span><span class="sxs-lookup"><span data-stu-id="0c9e4-119">If  _lpszNewFolderName_ is set to NULL, the name of the source subfolder is used for the name of the destination folder.</span></span> 
    
 <span data-ttu-id="0c9e4-120">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="0c9e4-120">_ulUIParam_</span></span>
  
> <span data-ttu-id="0c9e4-121">[in] Дескриптор родительского окна индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="0c9e4-121">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="0c9e4-122">Параметр _ulUIParam_ — это игнорируется, если не задан флаг FOLDER_DIALOG с помощью параметра _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="0c9e4-122">The  _ulUIParam_ parameter is ignored unless the FOLDER_DIALOG flag in the  _ulFlags_ parameter is set.</span></span> 
    
 <span data-ttu-id="0c9e4-123">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="0c9e4-123">_lpProgress_</span></span>
  
> <span data-ttu-id="0c9e4-124">[in] Указатель на объект хода выполнения, который отображает индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="0c9e4-124">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="0c9e4-125">Если в _lpProgress_передается значение NULL, поставщика хранилища сообщений отображает индикатор выполнения с помощью реализация объекта MAPI хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="0c9e4-125">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="0c9e4-126">Параметр _lpProgress_ используется только флаг FOLDER_DIALOG установлен в _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="0c9e4-126">The  _lpProgress_ parameter is ignored unless the FOLDER_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="0c9e4-127">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0c9e4-127">_ulFlags_</span></span>
  
> <span data-ttu-id="0c9e4-128">[in] Битовая маска флаги, который определяет операцию копирования или перемещения.</span><span class="sxs-lookup"><span data-stu-id="0c9e4-128">[in] A bitmask of flags that controls the copy or move operation.</span></span> <span data-ttu-id="0c9e4-129">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="0c9e4-129">The following flags can be set:</span></span>
    
<span data-ttu-id="0c9e4-130">COPY_SUBFOLDERS</span><span class="sxs-lookup"><span data-stu-id="0c9e4-130">COPY_SUBFOLDERS</span></span> 
  
> <span data-ttu-id="0c9e4-131">Все вложенные папки во вложенной папке для копирования следует также копируются.</span><span class="sxs-lookup"><span data-stu-id="0c9e4-131">All of the subfolders in the subfolder to be copied should also be copied.</span></span> <span data-ttu-id="0c9e4-132">Если COPY_SUBFOLDERS не задан для операции копирования, копируется только вложенную папку, определяемую средством _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="0c9e4-132">When COPY_SUBFOLDERS is not set for a copy operation, only the subfolder identified by  _lpEntryID_ is copied.</span></span> <span data-ttu-id="0c9e4-133">С помощью операции перемещения поведение COPY_SUBFOLDERS используется по умолчанию, независимо от того, является ли настройка.</span><span class="sxs-lookup"><span data-stu-id="0c9e4-133">With a move operation, the COPY_SUBFOLDERS behavior is the default regardless of whether the flag is set.</span></span> 
    
<span data-ttu-id="0c9e4-134">FOLDER_DIALOG</span><span class="sxs-lookup"><span data-stu-id="0c9e4-134">FOLDER_DIALOG</span></span> 
  
> <span data-ttu-id="0c9e4-135">Запрос на отображение индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="0c9e4-135">Requests the display of a progress indicator.</span></span>
    
<span data-ttu-id="0c9e4-136">FOLDER_MOVE</span><span class="sxs-lookup"><span data-stu-id="0c9e4-136">FOLDER_MOVE</span></span> 
  
> <span data-ttu-id="0c9e4-137">— Это вложенной папке перемещаемых вместо копируются.</span><span class="sxs-lookup"><span data-stu-id="0c9e4-137">The subfolder is to be moved instead of copied.</span></span> <span data-ttu-id="0c9e4-138">Если FOLDER_MOVE не задано, копируется вложенной папке.</span><span class="sxs-lookup"><span data-stu-id="0c9e4-138">If FOLDER_MOVE is not set, the subfolder is copied.</span></span>
    
<span data-ttu-id="0c9e4-139">MAPI_DECLINE_OK</span><span class="sxs-lookup"><span data-stu-id="0c9e4-139">MAPI_DECLINE_OK</span></span> 
  
> <span data-ttu-id="0c9e4-140">Информирует поставщика хранилища сообщений, что, если он реализует **CopyFolder** путем вызова метода [IMAPISupport::DoCopyTo](imapisupport-docopyto.md) или [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md) возвращается объект поддержки, **CopyFolder** вместо немедленно вернет MAPI_E_ DECLINE_COPY.</span><span class="sxs-lookup"><span data-stu-id="0c9e4-140">Informs the message store provider that if it implements **CopyFolder** by calling its support object's [IMAPISupport::DoCopyTo](imapisupport-docopyto.md) or [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md) method, **CopyFolder** should instead immediately return MAPI_E_DECLINE_COPY.</span></span> 
    
<span data-ttu-id="0c9e4-141">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0c9e4-141">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="0c9e4-142">— Это имя папки назначения в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="0c9e4-142">The name of the destination folder is in Unicode format.</span></span> <span data-ttu-id="0c9e4-143">Если флаг MAPI_UNICODE не установлен, — это имя папки в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="0c9e4-143">If the MAPI_UNICODE flag is not set, the folder name is in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0c9e4-144">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="0c9e4-144">Return value</span></span>

<span data-ttu-id="0c9e4-145">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="0c9e4-145">S_OK</span></span> 
  
> <span data-ttu-id="0c9e4-146">Указанная папка успешно копирования или перемещения.</span><span class="sxs-lookup"><span data-stu-id="0c9e4-146">The specified folder has been successfully copied or moved.</span></span>
    
<span data-ttu-id="0c9e4-147">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="0c9e4-147">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="0c9e4-148">Либо был установлен флажок MAPI_UNICODE и поставщика хранилища сообщений не поддерживает Юникод, или MAPI_UNICODE не было установлено и поставщика хранилища сообщений поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="0c9e4-148">Either the MAPI_UNICODE flag was set and the message store provider does not support Unicode, or MAPI_UNICODE was not set and the message store provider supports only Unicode.</span></span>
    
<span data-ttu-id="0c9e4-149">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="0c9e4-149">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="0c9e4-150">Имя папки перемещения или копирования — это же, как вложенную папку в папке назначения.</span><span class="sxs-lookup"><span data-stu-id="0c9e4-150">The name of the folder being moved or copied is the same as that of a subfolder in the destination folder.</span></span> <span data-ttu-id="0c9e4-151">Поставщик хранения сообщений требуется имена уникальный папок.</span><span class="sxs-lookup"><span data-stu-id="0c9e4-151">The message store provider requires unique folder names.</span></span>
    
<span data-ttu-id="0c9e4-152">MAPI_E_DECLINE_COPY</span><span class="sxs-lookup"><span data-stu-id="0c9e4-152">MAPI_E_DECLINE_COPY</span></span> 
  
> <span data-ttu-id="0c9e4-153">Поставщик реализует этот метод, вызвав метод объекта поддержки и вызывающего абонента, истекло флаг MAPI_DECLINE_OK.</span><span class="sxs-lookup"><span data-stu-id="0c9e4-153">The provider implements this method by calling a support object method, and the caller has passed the MAPI_DECLINE_OK flag.</span></span>
    
<span data-ttu-id="0c9e4-154">MAPI_E_FOLDER_CYCLE</span><span class="sxs-lookup"><span data-stu-id="0c9e4-154">MAPI_E_FOLDER_CYCLE</span></span> 
  
> <span data-ttu-id="0c9e4-155">Папка источника прямо или косвенно содержит папки назначения.</span><span class="sxs-lookup"><span data-stu-id="0c9e4-155">The source folder directly or indirectly contains the destination folder.</span></span> <span data-ttu-id="0c9e4-156">Важные может были выполнены перед был обнаружен это условие, поэтому исходной и целевой папке частично может быть изменена.</span><span class="sxs-lookup"><span data-stu-id="0c9e4-156">Significant work may have been performed before this condition was discovered, so the source and destination folder may be partially modified.</span></span> 
    
<span data-ttu-id="0c9e4-157">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="0c9e4-157">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="0c9e4-158">Вызов завершился успешно, но не все элементы скопированы успешно.</span><span class="sxs-lookup"><span data-stu-id="0c9e4-158">The call succeeded, but not all entries were successfully copied.</span></span> <span data-ttu-id="0c9e4-159">При возвращении этого предупреждения вызова необходимо обрабатывать об успешном завершении.</span><span class="sxs-lookup"><span data-stu-id="0c9e4-159">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="0c9e4-160">Чтобы проверить это предупреждение, используйте **HR_FAILED** макрос.</span><span class="sxs-lookup"><span data-stu-id="0c9e4-160">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="0c9e4-161">Дополнительные сведения можно [С помощью макросов для обработки ошибок](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="0c9e4-161">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0c9e4-162">Замечания</span><span class="sxs-lookup"><span data-stu-id="0c9e4-162">Remarks</span></span>

<span data-ttu-id="0c9e4-163">Метод **IMAPIFolder::CopyFolder** копирует или перемещает вложенную папку из одного места в другое.</span><span class="sxs-lookup"><span data-stu-id="0c9e4-163">The **IMAPIFolder::CopyFolder** method copies or moves a subfolder from one location to another.</span></span> <span data-ttu-id="0c9e4-164">Копирование или перемещение вложенной папке добавляется в конечную папку в качестве вложенной папке.</span><span class="sxs-lookup"><span data-stu-id="0c9e4-164">The subfolder being copied or moved is added to the destination folder as a subfolder.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="0c9e4-165">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="0c9e4-165">Notes to implementers</span></span>

<span data-ttu-id="0c9e4-166">При операции копирования или перемещения состоит из нескольких папок, как определяется параметром флаг COPY_SUBFOLDERS, как можно выполните операцию для каждой папки.</span><span class="sxs-lookup"><span data-stu-id="0c9e4-166">When the copy or move operation involves more than one folder, as indicated by setting the COPY_SUBFOLDERS flag, perform the operation as completely as possible for each folder.</span></span> <span data-ttu-id="0c9e4-167">В некоторых случаях один из папки для перемещения или копирования не существует или уже был перемещен или скопирован в другое место.</span><span class="sxs-lookup"><span data-stu-id="0c9e4-167">Sometimes one of the folders to be moved or copied does not exist or has already been moved or copied elsewhere.</span></span> <span data-ttu-id="0c9e4-168">Не останавливайте операции преждевременно Если произошла ошибка, которая находится за пределами элементу управления, такие как хватает памяти, недостаточно места на диске или повреждение в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="0c9e4-168">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span>
  
<span data-ttu-id="0c9e4-169">Попробуйте сохранять все идентификаторы запись сообщений в скопированной сообщения.</span><span class="sxs-lookup"><span data-stu-id="0c9e4-169">Try to retain all message entry identifiers in the copied messages.</span></span> <span data-ttu-id="0c9e4-170">Рекомендуется сохранить идентификаторы записей, но не требуется.</span><span class="sxs-lookup"><span data-stu-id="0c9e4-170">You should also try to preserve entry identifiers, but it is not required.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="0c9e4-171">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="0c9e4-171">Notes to callers</span></span>

<span data-ttu-id="0c9e4-172">Ожидается, что эти возвращаемые значения в следующих случаях.</span><span class="sxs-lookup"><span data-stu-id="0c9e4-172">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="0c9e4-173">**Условие**</span><span class="sxs-lookup"><span data-stu-id="0c9e4-173">**Condition**</span></span>|<span data-ttu-id="0c9e4-174">**������������ ��������**</span><span class="sxs-lookup"><span data-stu-id="0c9e4-174">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0c9e4-175">**CopyFolder** успешно после копирования или перемещения каждого сообщения и вложенные папки.</span><span class="sxs-lookup"><span data-stu-id="0c9e4-175">**CopyFolder** has successfully copied or moved every message and subfolder.</span></span>  <br/> |<span data-ttu-id="0c9e4-176">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="0c9e4-176">S_OK</span></span>  <br/> |
|<span data-ttu-id="0c9e4-177">**CopyFolder** не удалось успешно скопируйте или переместите каждого сообщения и вложенные папки.</span><span class="sxs-lookup"><span data-stu-id="0c9e4-177">**CopyFolder** was unable to successfully copy or move every message and subfolder.</span></span>  <br/> |<span data-ttu-id="0c9e4-178">MAPI_W_PARTIAL_COMPLETION или MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="0c9e4-178">MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND</span></span>  <br/> |
|<span data-ttu-id="0c9e4-179">**CopyFolder** не удалось завершить.</span><span class="sxs-lookup"><span data-stu-id="0c9e4-179">**CopyFolder** was unable to complete.</span></span>  <br/> |<span data-ttu-id="0c9e4-180">Любое значение ошибки, за исключением MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="0c9e4-180">Any error value except MAPI_E_NOT_FOUND</span></span>  <br/> |
   
<span data-ttu-id="0c9e4-181">При **CopyFolder** не удается завершить, не предполагают, что работа не выполнена.</span><span class="sxs-lookup"><span data-stu-id="0c9e4-181">When **CopyFolder** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="0c9e4-182">**CopyFolder** мог для копирования или перемещения одно или несколько сообщений и вложенных папок, прежде чем ошибок.</span><span class="sxs-lookup"><span data-stu-id="0c9e4-182">**CopyFolder** might have been able to copy or move one or more of the messages and subfolders before encountering the error.</span></span> 
  
<span data-ttu-id="0c9e4-183">Если в _lpEntryID_передается идентификатор записи для папки, которая не существует, **CopyFolder** возвращает MAPI_W_PARTIAL_COMPLETION или MAPI_E_NOT_FOUND, в зависимости от реализации хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="0c9e4-183">If an entry identifier for a folder that does not exist is passed in  _lpEntryID_, **CopyFolder** returns MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND, depending on the message store's implementation.</span></span> 
  
<span data-ttu-id="0c9e4-184">В зависимости от поставщика хранилища сообщений идентификатор записи исходного сообщения могут или не могут быть сохранены в скопированной сообщения.</span><span class="sxs-lookup"><span data-stu-id="0c9e4-184">Depending on the message store provider, the entry identifier of the original message may or may not be preserved in the copied message.</span></span> <span data-ttu-id="0c9e4-185">Необходимо хранить идентификаторы записей, когда это возможно, но не требуется.</span><span class="sxs-lookup"><span data-stu-id="0c9e4-185">You should preserve entry identifiers whenever possible, but it is not a requirement.</span></span> <span data-ttu-id="0c9e4-186">Как правило, может зависеть от следующих сценариев:</span><span class="sxs-lookup"><span data-stu-id="0c9e4-186">You can generally depend on the following scenarios:</span></span>
  
- <span data-ttu-id="0c9e4-187">При перемещении папки между двумя разными типами хранилищ сообщений идентификатор записи гарантированно изменить.</span><span class="sxs-lookup"><span data-stu-id="0c9e4-187">When you move a folder between two different types of message stores, the entry identifier is guaranteed to change.</span></span>
    
- <span data-ttu-id="0c9e4-188">При перемещении папки между двумя хранилищ сообщений из того же типа почти всегда изменяется идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="0c9e4-188">When you move a folder between two message stores of the same type, the entry identifier almost always changes.</span></span>
    
- <span data-ttu-id="0c9e4-189">При перемещении папки в другое расположение в том же хранилище сообщений идентификатор записи может или может изменить, в зависимости от сообщения поставщик хранилища.</span><span class="sxs-lookup"><span data-stu-id="0c9e4-189">When you move a folder to another location in the same message store, the entry identifier may or may not change, depending on the message store provider.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="0c9e4-190">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="0c9e4-190">MFCMAPI reference</span></span>

<span data-ttu-id="0c9e4-191">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="0c9e4-191">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="0c9e4-192">**����**</span><span class="sxs-lookup"><span data-stu-id="0c9e4-192">**File**</span></span>|<span data-ttu-id="0c9e4-193">**�������**</span><span class="sxs-lookup"><span data-stu-id="0c9e4-193">**Function**</span></span>|<span data-ttu-id="0c9e4-194">**�����������**</span><span class="sxs-lookup"><span data-stu-id="0c9e4-194">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0c9e4-195">MsgStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="0c9e4-195">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="0c9e4-196">CMsgStoreDlg::OnPasteFolder</span><span class="sxs-lookup"><span data-stu-id="0c9e4-196">CMsgStoreDlg::OnPasteFolder</span></span>  <br/> |<span data-ttu-id="0c9e4-197">Mfcmapi (en) использует метод **IMAPIFolder::CopyFolder** копирование папок из одного места в другое.</span><span class="sxs-lookup"><span data-stu-id="0c9e4-197">MFCMAPI uses the **IMAPIFolder::CopyFolder** method to copy folders from one location to another.</span></span> <span data-ttu-id="0c9e4-198">Mfcmapi (en) запоминает исходной папки во время операции копирования и выполняет эту копию во время операции вставки.</span><span class="sxs-lookup"><span data-stu-id="0c9e4-198">MFCMAPI remembers the source folder during the copy operation and actually performs the copy during the paste operation.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0c9e4-199">См. также</span><span class="sxs-lookup"><span data-stu-id="0c9e4-199">See also</span></span>



[<span data-ttu-id="0c9e4-200">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="0c9e4-200">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="0c9e4-201">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="0c9e4-201">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

