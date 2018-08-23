---
title: IMAPISupportCopyFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.CopyFolder
api_type:
- COM
ms.assetid: c2e0939f-0668-473f-856c-a27af094070b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6ffbf74496d4b61357a0fb473b82deedf39ee576
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570676"
---
# <a name="imapisupportcopyfolder"></a><span data-ttu-id="00172-103">IMAPISupport::CopyFolder</span><span class="sxs-lookup"><span data-stu-id="00172-103">IMAPISupport::CopyFolder</span></span>

  
  
<span data-ttu-id="00172-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="00172-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="00172-105">Копирование или перемещение папки текущей родительской папки в другую.</span><span class="sxs-lookup"><span data-stu-id="00172-105">Copies or moves a folder from its current parent folder to another parent folder.</span></span>
  
```cpp
HRESULT CopyFolder(
  LPCIID lpSrcInterface,
  LPVOID lpSrcFolder,
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

## <a name="parameters"></a><span data-ttu-id="00172-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="00172-106">Parameters</span></span>

 <span data-ttu-id="00172-107">_lpSrcInterface_</span><span class="sxs-lookup"><span data-stu-id="00172-107">_lpSrcInterface_</span></span>
  
> <span data-ttu-id="00172-108">[in] Указатель на идентификатор интерфейса (ИД интерфейса), который представляет интерфейс, который будет использоваться для доступа к папке родительской папки можно скопировать или переместить.</span><span class="sxs-lookup"><span data-stu-id="00172-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the parent folder of the folder to be copied or moved.</span></span>
    
 <span data-ttu-id="00172-109">_lpSrcFolder_</span><span class="sxs-lookup"><span data-stu-id="00172-109">_lpSrcFolder_</span></span>
  
> <span data-ttu-id="00172-110">[in] Указатель на папку родительской папки можно скопировать или переместить.</span><span class="sxs-lookup"><span data-stu-id="00172-110">[in] A pointer to the parent folder of the folder to be copied or moved.</span></span> 
    
 <span data-ttu-id="00172-111">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="00172-111">_cbEntryID_</span></span>
  
> <span data-ttu-id="00172-112">[in] Число байтов в идентификатор записи, на который указывает _lpEntryID_.</span><span class="sxs-lookup"><span data-stu-id="00172-112">[in] The byte count in the entry identifier pointed to by  _lpEntryID_.</span></span>
    
 <span data-ttu-id="00172-113">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="00172-113">_lpEntryID_</span></span>
  
> <span data-ttu-id="00172-114">[in] Указатель на идентификатор записи папки можно скопировать или переместить.</span><span class="sxs-lookup"><span data-stu-id="00172-114">[in] A pointer to the entry identifier of the folder to be copied or moved.</span></span> 
    
 <span data-ttu-id="00172-115">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="00172-115">_lpInterface_</span></span>
  
> <span data-ttu-id="00172-116">[in] Зарезервировано; должен иметь значение NULL.</span><span class="sxs-lookup"><span data-stu-id="00172-116">[in] Reserved; must be NULL.</span></span>
    
 <span data-ttu-id="00172-117">_lpDestFolder_</span><span class="sxs-lookup"><span data-stu-id="00172-117">_lpDestFolder_</span></span>
  
> <span data-ttu-id="00172-118">[in] Указатель на папку, находящуюся на получение папки можно скопировать или переместить.</span><span class="sxs-lookup"><span data-stu-id="00172-118">[in] A pointer to the folder that is to receive the folder to be copied or moved.</span></span>
    
 <span data-ttu-id="00172-119">_lpszNewFolderName_</span><span class="sxs-lookup"><span data-stu-id="00172-119">_lpszNewFolderName_</span></span>
  
> <span data-ttu-id="00172-120">[in] Указатель на имя папки, копируемые или перемещения; в противном случае — значение NULL, который указывает, что папка скопированной или перемещенной следует таким же именем как исходной папки (папка, на который указывает _lpEntryID_).</span><span class="sxs-lookup"><span data-stu-id="00172-120">[in] A pointer to the name of the copied or moved folder; otherwise, NULL, which indicates that the copied or moved folder should have the same name as the source folder (the folder pointed to by  _lpEntryID_).</span></span>
    
 <span data-ttu-id="00172-121">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="00172-121">_ulUIParam_</span></span>
  
> <span data-ttu-id="00172-122">[in] Дескриптор окна для диалогового окна индикатор хода выполнения и связанных с ними windows.</span><span class="sxs-lookup"><span data-stu-id="00172-122">[in] A handle of the window for the progress indicator dialog box and related windows.</span></span> <span data-ttu-id="00172-123">Параметр _ulUIParam_ игнорируется, пока флаг FOLDER_DIALOG будет выполнен с помощью параметра _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="00172-123">The  _ulUIParam_ parameter is ignored unless the FOLDER_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="00172-124">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="00172-124">_lpProgress_</span></span>
  
> <span data-ttu-id="00172-125">[in] Указатель на объект хода выполнения, который отображает индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="00172-125">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="00172-126">Если в _lpProgress_передается значение NULL, поставщика хранилища сообщений отображает индикатор выполнения с помощью реализация объекта MAPI хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="00172-126">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="00172-127">Параметр _lpProgress_ используется только флаг FOLDER_DIALOG установлен в _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="00172-127">The  _lpProgress_ parameter is ignored unless the FOLDER_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="00172-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="00172-128">_ulFlags_</span></span>
  
> <span data-ttu-id="00172-129">[in] Битовая маска флаги, который определяет, как выполнить операцию копирования или перемещения.</span><span class="sxs-lookup"><span data-stu-id="00172-129">[in] A bitmask of flags that controls how the copy or move operation is accomplished.</span></span> <span data-ttu-id="00172-130">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="00172-130">The following flags can be set:</span></span>
    
<span data-ttu-id="00172-131">COPY_SUBFOLDERS</span><span class="sxs-lookup"><span data-stu-id="00172-131">COPY_SUBFOLDERS</span></span> 
  
> <span data-ttu-id="00172-132">Все вложенные папки следует скопировать или переместить.</span><span class="sxs-lookup"><span data-stu-id="00172-132">All of the folder's subfolders should be copied or moved.</span></span> <span data-ttu-id="00172-133">При COPY_SUBFOLDERS установлено для операции копирования, копируются только папку, определяемую средством _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="00172-133">When COPY_SUBFOLDERS is not set for a copy operation, only the folder identified by  _lpEntryID_ is copied.</span></span> <span data-ttu-id="00172-134">С помощью операции перемещения поведение COPY_SUBFOLDERS используется по умолчанию, независимо от того, является ли настройка.</span><span class="sxs-lookup"><span data-stu-id="00172-134">With a move operation, the COPY_SUBFOLDERS behavior is the default regardless of whether the flag is set.</span></span> 
    
<span data-ttu-id="00172-135">FOLDER_DIALOG</span><span class="sxs-lookup"><span data-stu-id="00172-135">FOLDER_DIALOG</span></span> 
  
> <span data-ttu-id="00172-136">Запрос на отображение индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="00172-136">Requests the display of a progress indicator.</span></span>
    
<span data-ttu-id="00172-137">FOLDER_MOVE</span><span class="sxs-lookup"><span data-stu-id="00172-137">FOLDER_MOVE</span></span> 
  
> <span data-ttu-id="00172-138">Следует переместить папку вместо копируются.</span><span class="sxs-lookup"><span data-stu-id="00172-138">The folder should be moved instead of copied.</span></span> <span data-ttu-id="00172-139">Если FOLDER_MOVE не задано, скопировать папку.</span><span class="sxs-lookup"><span data-stu-id="00172-139">If FOLDER_MOVE is not set, the folder is copied.</span></span>
    
<span data-ttu-id="00172-140">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="00172-140">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="00172-141">— Это имя папки в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="00172-141">The name of the folder is in Unicode format.</span></span> <span data-ttu-id="00172-142">Если флаг MAPI_UNICODE не установлен, — это имя папки в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="00172-142">If the MAPI_UNICODE flag is not set, the name of the folder is in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="00172-143">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="00172-143">Return value</span></span>

<span data-ttu-id="00172-144">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="00172-144">S_OK</span></span> 
  
> <span data-ttu-id="00172-145">Папка успешно скопировать или переместить.</span><span class="sxs-lookup"><span data-stu-id="00172-145">The folder has been successfully copied or moved.</span></span>
    
<span data-ttu-id="00172-146">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="00172-146">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="00172-147">Имя папки перемещения или копирования — это же, как вложенную папку в папке назначения.</span><span class="sxs-lookup"><span data-stu-id="00172-147">The name of the folder being moved or copied is the same as that of a subfolder in the destination folder.</span></span> <span data-ttu-id="00172-148">Поставщик хранения сообщений требует уникальные имена папок.</span><span class="sxs-lookup"><span data-stu-id="00172-148">The message store provider requires that folder names be unique.</span></span> <span data-ttu-id="00172-149">Операция останавливает без выполнения.</span><span class="sxs-lookup"><span data-stu-id="00172-149">The operation stops without completing.</span></span>
    
<span data-ttu-id="00172-150">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="00172-150">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="00172-151">Вызов завершился успешно, но не все элементы скопированы успешно.</span><span class="sxs-lookup"><span data-stu-id="00172-151">The call succeeded, but not all entries were successfully copied.</span></span> <span data-ttu-id="00172-152">При возвращении этого предупреждения вызова необходимо обрабатывать об успешном завершении.</span><span class="sxs-lookup"><span data-stu-id="00172-152">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="00172-153">Чтобы проверить это предупреждение, используйте **HR_FAILED** макрос.</span><span class="sxs-lookup"><span data-stu-id="00172-153">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="00172-154">Дополнительные сведения можно [С помощью макросов для обработки ошибок](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="00172-154">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="00172-155">Замечания</span><span class="sxs-lookup"><span data-stu-id="00172-155">Remarks</span></span>

<span data-ttu-id="00172-156">Метод **IMAPISupport::CopyFolder** реализуется для объектов поддержки поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="00172-156">The **IMAPISupport::CopyFolder** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="00172-157">Поставщики хранилища сообщений можно вызвать **IMAPISupport::CopyFolder** в их реализации [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md) для копирования или перемещения одного папки из одной родительской папки в другую.</span><span class="sxs-lookup"><span data-stu-id="00172-157">Message store providers can call **IMAPISupport::CopyFolder** in their implementation of [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md) to copy or move a single folder from one parent folder to another.</span></span> 
  
 <span data-ttu-id="00172-158">**IMAPISupport::CopyFolder** Добавляет копируемые или перемещения папки в качестве вложенной папке назначения.</span><span class="sxs-lookup"><span data-stu-id="00172-158">**IMAPISupport::CopyFolder** adds the copied or moved folder as a subfolder of the destination folder.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="00172-159">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="00172-159">Notes to callers</span></span>

 <span data-ttu-id="00172-160">**IMAPISupport::CopyFolder** позволяет одновременно работающих переименование или перемещение папки и копирование или перемещение вложенные папки.</span><span class="sxs-lookup"><span data-stu-id="00172-160">**IMAPISupport::CopyFolder** allows simultaneous renaming and moving of folders and the copying or moving of subfolders of the affected folder.</span></span> <span data-ttu-id="00172-161">Копирование или перемещение всех вложенных папок, вложенных в папку скопированной или перемещенной, передайте флаг COPY_SUBFOLDERS _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="00172-161">To copy or move all subfolders nested in the copied or moved folder, pass the COPY_SUBFOLDERS flag in  _ulFlags_.</span></span> 
  
<span data-ttu-id="00172-162">Ожидается, что следующие возвращаемые значения в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="00172-162">Expect the following return values under the following conditions:</span></span>
  
|<span data-ttu-id="00172-163">**Условие**</span><span class="sxs-lookup"><span data-stu-id="00172-163">**Condition**</span></span>|<span data-ttu-id="00172-164">**������������ ��������**</span><span class="sxs-lookup"><span data-stu-id="00172-164">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="00172-165">**CopyFolder** успешно скопировать или переместить папка и все ее вложенные папки, если это возможно.</span><span class="sxs-lookup"><span data-stu-id="00172-165">**CopyFolder** successfully copied or moved the folder and all its subfolders, if applicable.</span></span>  <br/> |<span data-ttu-id="00172-166">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="00172-166">S_OK</span></span>  <br/> |
|<span data-ttu-id="00172-167">**CopyFolder** не удалось успешно копирование или перемещение всех папок.</span><span class="sxs-lookup"><span data-stu-id="00172-167">**CopyFolder** was unable to successfully copy or move all of the folders.</span></span>  <br/> |<span data-ttu-id="00172-168">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="00172-168">MAPI_W_PARTIAL_COMPLETION</span></span>  <br/> |
|<span data-ttu-id="00172-169">**CopyFolder** не удалось завершить.</span><span class="sxs-lookup"><span data-stu-id="00172-169">**CopyFolder** was unable to complete.</span></span>  <br/> |<span data-ttu-id="00172-170">Любое значение ошибки</span><span class="sxs-lookup"><span data-stu-id="00172-170">Any error value</span></span>  <br/> |
   
<span data-ttu-id="00172-171">Если **CopyFolder** возвращает код ошибки, не перейти предполагается, что работа не выполнена.</span><span class="sxs-lookup"><span data-stu-id="00172-171">If **CopyFolder** returns an error value, do not proceed on the assumption that no work was done.</span></span> <span data-ttu-id="00172-172">Невозможно, одной или нескольких папок скопировать или переместить перед **CopyFolder** произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="00172-172">One or more folders could have been copied or moved before **CopyFolder** experienced the failure.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="00172-173">См. также</span><span class="sxs-lookup"><span data-stu-id="00172-173">See also</span></span>



[<span data-ttu-id="00172-174">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="00172-174">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

