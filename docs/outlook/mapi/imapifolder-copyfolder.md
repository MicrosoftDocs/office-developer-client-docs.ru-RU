---
title: имапифолдеркопифолдер
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
# <a name="imapifoldercopyfolder"></a><span data-ttu-id="b001a-103">IMAPIFolder::CopyFolder</span><span class="sxs-lookup"><span data-stu-id="b001a-103">IMAPIFolder::CopyFolder</span></span>

  
  
<span data-ttu-id="b001a-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b001a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b001a-105">Копирует или перемещает вложенную папку.</span><span class="sxs-lookup"><span data-stu-id="b001a-105">Copies or moves a subfolder.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="b001a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b001a-106">Parameters</span></span>

 <span data-ttu-id="b001a-107">_кбентрид_</span><span class="sxs-lookup"><span data-stu-id="b001a-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="b001a-108">возврата Число байтов в идентификаторе записи, на которое указывает параметр _лпентрид_ .</span><span class="sxs-lookup"><span data-stu-id="b001a-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="b001a-109">_лпентрид_</span><span class="sxs-lookup"><span data-stu-id="b001a-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="b001a-110">возврата Указатель на идентификатор записи вложенной папки, которую необходимо скопировать или переместить.</span><span class="sxs-lookup"><span data-stu-id="b001a-110">[in] A pointer to the entry identifier of the subfolder to copy or move.</span></span>
    
 <span data-ttu-id="b001a-111">_лпинтерфаце_</span><span class="sxs-lookup"><span data-stu-id="b001a-111">_lpInterface_</span></span>
  
> <span data-ttu-id="b001a-112">возврата Указатель на идентификатор интерфейса (IID), представляющий интерфейс, который будет использоваться для доступа к папке, на которую указывает параметр _лпдестфолдер_ .</span><span class="sxs-lookup"><span data-stu-id="b001a-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the folder that the  _lpDestFolder_ parameter points to.</span></span> <span data-ttu-id="b001a-113">При передаче значения NULL поставщику услуг возвращается интерфейс стандартных папок, [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="b001a-113">Passing NULL causes the service provider to return the standard folder interface, [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="b001a-114">Допустимые значения для _лпинтерфаце_ : IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer и IID_IMAPIFolder.</span><span class="sxs-lookup"><span data-stu-id="b001a-114">Valid values for  _lpInterface_ include IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer, and IID_IMAPIFolder.</span></span> 
    
 <span data-ttu-id="b001a-115">_лпдестфолдер_</span><span class="sxs-lookup"><span data-stu-id="b001a-115">_lpDestFolder_</span></span>
  
> <span data-ttu-id="b001a-116">возврата Указатель на открытую папку для получения скопированной или перемещенной вложенной папки.</span><span class="sxs-lookup"><span data-stu-id="b001a-116">[in] A pointer to the open folder to receive the copied or moved subfolder.</span></span>
    
 <span data-ttu-id="b001a-117">_лпсзневфолдернаме_</span><span class="sxs-lookup"><span data-stu-id="b001a-117">_lpszNewFolderName_</span></span>
  
> <span data-ttu-id="b001a-118">возврата Указатель на имя скопированной или перемещенной папки в новом месте назначения.</span><span class="sxs-lookup"><span data-stu-id="b001a-118">[in] A pointer to the name of the copied or moved folder in its new destination.</span></span> <span data-ttu-id="b001a-119">Если для _лпсзневфолдернаме_ ЗАДАНО значение null, имя исходной вложенной папки используется для имени конечной папки.</span><span class="sxs-lookup"><span data-stu-id="b001a-119">If  _lpszNewFolderName_ is set to NULL, the name of the source subfolder is used for the name of the destination folder.</span></span> 
    
 <span data-ttu-id="b001a-120">_улуипарам_</span><span class="sxs-lookup"><span data-stu-id="b001a-120">_ulUIParam_</span></span>
  
> <span data-ttu-id="b001a-121">возврата Дескриптор родительского окна индикатора хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="b001a-121">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="b001a-122">Параметр _улуипарам_ игнорируется, если не установлен флаг FOLDER_DIALOG в параметре _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="b001a-122">The  _ulUIParam_ parameter is ignored unless the FOLDER_DIALOG flag in the  _ulFlags_ parameter is set.</span></span> 
    
 <span data-ttu-id="b001a-123">_лппрогресс_</span><span class="sxs-lookup"><span data-stu-id="b001a-123">_lpProgress_</span></span>
  
> <span data-ttu-id="b001a-124">возврата Указатель на объект Progress, который отображает индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="b001a-124">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="b001a-125">Если в _лппрогресс_передается значение null, то поставщик хранилища сообщений отображает индикатор хода выполнения с помощью реализации объекта Progress для MAPI.</span><span class="sxs-lookup"><span data-stu-id="b001a-125">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="b001a-126">Параметр _лппрогресс_ игнорируется, если не установлен флаг FOLDER_DIALOG в _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="b001a-126">The  _lpProgress_ parameter is ignored unless the FOLDER_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="b001a-127">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b001a-127">_ulFlags_</span></span>
  
> <span data-ttu-id="b001a-128">возврата Битовая маска флагов, управляющих операциями копирования или перемещения.</span><span class="sxs-lookup"><span data-stu-id="b001a-128">[in] A bitmask of flags that controls the copy or move operation.</span></span> <span data-ttu-id="b001a-129">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="b001a-129">The following flags can be set:</span></span>
    
<span data-ttu-id="b001a-130">COPY_SUBFOLDERS</span><span class="sxs-lookup"><span data-stu-id="b001a-130">COPY_SUBFOLDERS</span></span> 
  
> <span data-ttu-id="b001a-131">Все вложенные папки в вложенной папке также должны быть скопированы.</span><span class="sxs-lookup"><span data-stu-id="b001a-131">All of the subfolders in the subfolder to be copied should also be copied.</span></span> <span data-ttu-id="b001a-132">Если для операции копирования не задано COPY_SUBFOLDERS, копируется только вложенная папка, определенная с помощью _лпентрид_ .</span><span class="sxs-lookup"><span data-stu-id="b001a-132">When COPY_SUBFOLDERS is not set for a copy operation, only the subfolder identified by  _lpEntryID_ is copied.</span></span> <span data-ttu-id="b001a-133">При выполнении операции перемещения COPY_SUBFOLDERS поведение по умолчанию независимо от того, установлен ли флаг.</span><span class="sxs-lookup"><span data-stu-id="b001a-133">With a move operation, the COPY_SUBFOLDERS behavior is the default regardless of whether the flag is set.</span></span> 
    
<span data-ttu-id="b001a-134">FOLDER_DIALOG</span><span class="sxs-lookup"><span data-stu-id="b001a-134">FOLDER_DIALOG</span></span> 
  
> <span data-ttu-id="b001a-135">Запрашивает отображение индикатора хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="b001a-135">Requests the display of a progress indicator.</span></span>
    
<span data-ttu-id="b001a-136">FOLDER_MOVE</span><span class="sxs-lookup"><span data-stu-id="b001a-136">FOLDER_MOVE</span></span> 
  
> <span data-ttu-id="b001a-137">Вложенная папка перемещается, а не копируется.</span><span class="sxs-lookup"><span data-stu-id="b001a-137">The subfolder is to be moved instead of copied.</span></span> <span data-ttu-id="b001a-138">Если FOLDER_MOVE не задано, то подпапка копируется.</span><span class="sxs-lookup"><span data-stu-id="b001a-138">If FOLDER_MOVE is not set, the subfolder is copied.</span></span>
    
<span data-ttu-id="b001a-139">MAPI_DECLINE_OK</span><span class="sxs-lookup"><span data-stu-id="b001a-139">MAPI_DECLINE_OK</span></span> 
  
> <span data-ttu-id="b001a-140">Информирует поставщика хранилища сообщений, что если он реализует **CopyFolder** , вызывая его объект поддержки [Имаписуппорт::D окопито](imapisupport-docopyto.md) или [имаписуппорт::D окопипропс](imapisupport-docopyprops.md) метод, **CopyFolder** должен немедленно возвратить MAPI_E_DECLINE_COPY.</span><span class="sxs-lookup"><span data-stu-id="b001a-140">Informs the message store provider that if it implements **CopyFolder** by calling its support object's [IMAPISupport::DoCopyTo](imapisupport-docopyto.md) or [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md) method, **CopyFolder** should instead immediately return MAPI_E_DECLINE_COPY.</span></span> 
    
<span data-ttu-id="b001a-141">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b001a-141">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="b001a-142">Имя конечной папки имеет формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="b001a-142">The name of the destination folder is in Unicode format.</span></span> <span data-ttu-id="b001a-143">Если флаг MAPI_UNICODE не установлен, имя папки указывается в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="b001a-143">If the MAPI_UNICODE flag is not set, the folder name is in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b001a-144">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b001a-144">Return value</span></span>

<span data-ttu-id="b001a-145">S_OK</span><span class="sxs-lookup"><span data-stu-id="b001a-145">S_OK</span></span> 
  
> <span data-ttu-id="b001a-146">Указанная папка успешно скопирована или перемещена.</span><span class="sxs-lookup"><span data-stu-id="b001a-146">The specified folder has been successfully copied or moved.</span></span>
    
<span data-ttu-id="b001a-147">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="b001a-147">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="b001a-148">Установлен флаг MAPI_UNICODE, а поставщик хранилища сообщений не поддерживает Юникод или MAPI_UNICODE не задан, а поставщик хранилища сообщений поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="b001a-148">Either the MAPI_UNICODE flag was set and the message store provider does not support Unicode, or MAPI_UNICODE was not set and the message store provider supports only Unicode.</span></span>
    
<span data-ttu-id="b001a-149">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="b001a-149">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="b001a-150">Имя папки, которую вы перемещаете или копирует, совпадает с именем вложенной папки в папке назначения.</span><span class="sxs-lookup"><span data-stu-id="b001a-150">The name of the folder being moved or copied is the same as that of a subfolder in the destination folder.</span></span> <span data-ttu-id="b001a-151">Для поставщика хранилища сообщений требуются уникальные имена папок.</span><span class="sxs-lookup"><span data-stu-id="b001a-151">The message store provider requires unique folder names.</span></span>
    
<span data-ttu-id="b001a-152">MAPI_E_DECLINE_COPY</span><span class="sxs-lookup"><span data-stu-id="b001a-152">MAPI_E_DECLINE_COPY</span></span> 
  
> <span data-ttu-id="b001a-153">Поставщик реализует этот метод, вызывая метод объекта поддержки, и вызывающий абонент передал флаг MAPI_DECLINE_OK.</span><span class="sxs-lookup"><span data-stu-id="b001a-153">The provider implements this method by calling a support object method, and the caller has passed the MAPI_DECLINE_OK flag.</span></span>
    
<span data-ttu-id="b001a-154">MAPI_E_FOLDER_CYCLE</span><span class="sxs-lookup"><span data-stu-id="b001a-154">MAPI_E_FOLDER_CYCLE</span></span> 
  
> <span data-ttu-id="b001a-155">Исходная папка напрямую или косвенно содержит целевую папку.</span><span class="sxs-lookup"><span data-stu-id="b001a-155">The source folder directly or indirectly contains the destination folder.</span></span> <span data-ttu-id="b001a-156">Перед обнаружением этого условия может быть выполнено большое количество действий, поэтому исходная и конечная папки могут быть частично изменены.</span><span class="sxs-lookup"><span data-stu-id="b001a-156">Significant work may have been performed before this condition was discovered, so the source and destination folder may be partially modified.</span></span> 
    
<span data-ttu-id="b001a-157">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="b001a-157">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="b001a-158">Вызов выполнен успешно, но не все записи успешно скопированы.</span><span class="sxs-lookup"><span data-stu-id="b001a-158">The call succeeded, but not all entries were successfully copied.</span></span> <span data-ttu-id="b001a-159">При возвращении этого предупреждения вызов должен обрабатываться как успешный.</span><span class="sxs-lookup"><span data-stu-id="b001a-159">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="b001a-160">Чтобы проверить это предупреждение, используйте макрос **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="b001a-160">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="b001a-161">Дополнительные сведения см. [в разделе Использование макросов для обработки ошибок](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="b001a-161">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b001a-162">Примечания</span><span class="sxs-lookup"><span data-stu-id="b001a-162">Remarks</span></span>

<span data-ttu-id="b001a-163">Метод **IMAPIFolder:: CopyFolder** копирует или перемещает вложенную папку из одного расположения в другое.</span><span class="sxs-lookup"><span data-stu-id="b001a-163">The **IMAPIFolder::CopyFolder** method copies or moves a subfolder from one location to another.</span></span> <span data-ttu-id="b001a-164">Подпапка, которую необходимо скопировать или переместить, добавляется в папку назначения в качестве вложенной папки.</span><span class="sxs-lookup"><span data-stu-id="b001a-164">The subfolder being copied or moved is added to the destination folder as a subfolder.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="b001a-165">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="b001a-165">Notes to implementers</span></span>

<span data-ttu-id="b001a-166">Если операция копирования или перемещения включает несколько папок, как показано в результате установки флага COPY_SUBFOLDERS, выполните операцию как можно скорее для каждой папки.</span><span class="sxs-lookup"><span data-stu-id="b001a-166">When the copy or move operation involves more than one folder, as indicated by setting the COPY_SUBFOLDERS flag, perform the operation as completely as possible for each folder.</span></span> <span data-ttu-id="b001a-167">Иногда одна из папок, которую необходимо переместить или скопировать, не существует или уже была перемещена или скопирована в другом месте.</span><span class="sxs-lookup"><span data-stu-id="b001a-167">Sometimes one of the folders to be moved or copied does not exist or has already been moved or copied elsewhere.</span></span> <span data-ttu-id="b001a-168">Не прекращайте выполнение операции преждевременно, если не произойдет сбой, который выходит за рамки элемента управления, например, не хватает памяти, не хватает места на диске или повреждено хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="b001a-168">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span>
  
<span data-ttu-id="b001a-169">Попробуйте сохранить все идентификаторы записи сообщений в скопированных сообщениях.</span><span class="sxs-lookup"><span data-stu-id="b001a-169">Try to retain all message entry identifiers in the copied messages.</span></span> <span data-ttu-id="b001a-170">Также следует попытаться сохранить идентификаторы записей, но это не обязательно.</span><span class="sxs-lookup"><span data-stu-id="b001a-170">You should also try to preserve entry identifiers, but it is not required.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="b001a-171">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="b001a-171">Notes to callers</span></span>

<span data-ttu-id="b001a-172">Эти возвращаемые значения следует ожидать при соблюдении следующих условий.</span><span class="sxs-lookup"><span data-stu-id="b001a-172">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="b001a-173">**Условие**</span><span class="sxs-lookup"><span data-stu-id="b001a-173">**Condition**</span></span>|<span data-ttu-id="b001a-174">**Возвращаемое значение**</span><span class="sxs-lookup"><span data-stu-id="b001a-174">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b001a-175">**CopyFolder** успешно копирует или перемещает все сообщения и вложенную папку.</span><span class="sxs-lookup"><span data-stu-id="b001a-175">**CopyFolder** has successfully copied or moved every message and subfolder.</span></span>  <br/> |<span data-ttu-id="b001a-176">S_OK</span><span class="sxs-lookup"><span data-stu-id="b001a-176">S_OK</span></span>  <br/> |
|<span data-ttu-id="b001a-177">**CopyFolder** не удалось успешно скопировать или переместить все сообщения и вложенную папку.</span><span class="sxs-lookup"><span data-stu-id="b001a-177">**CopyFolder** was unable to successfully copy or move every message and subfolder.</span></span>  <br/> |<span data-ttu-id="b001a-178">MAPI_W_PARTIAL_COMPLETION или MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="b001a-178">MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND</span></span>  <br/> |
|<span data-ttu-id="b001a-179">**CopyFolder** не удалось выполнить.</span><span class="sxs-lookup"><span data-stu-id="b001a-179">**CopyFolder** was unable to complete.</span></span>  <br/> |<span data-ttu-id="b001a-180">Любое значение ошибки, кроме MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="b001a-180">Any error value except MAPI_E_NOT_FOUND</span></span>  <br/> |
   
<span data-ttu-id="b001a-181">Если **CopyFolder** не удается выполнить, не следует предполагать, что работа не выполнялась.</span><span class="sxs-lookup"><span data-stu-id="b001a-181">When **CopyFolder** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="b001a-182">Возможно, в **CopyFolder** удалось скопировать или переместить одно или несколько сообщений и вложенных папок, прежде чем возникнет ошибка.</span><span class="sxs-lookup"><span data-stu-id="b001a-182">**CopyFolder** might have been able to copy or move one or more of the messages and subfolders before encountering the error.</span></span> 
  
<span data-ttu-id="b001a-183">Если идентификатор записи для несуществующей папки передается в _лпентрид_, **CopyFolder** возвращает MAPI_W_PARTIAL_COMPLETION или MAPI_E_NOT_FOUND, в зависимости от реализации хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="b001a-183">If an entry identifier for a folder that does not exist is passed in  _lpEntryID_, **CopyFolder** returns MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND, depending on the message store's implementation.</span></span> 
  
<span data-ttu-id="b001a-184">В зависимости от поставщика хранилища сообщений идентификатор элемента исходного сообщения может быть не сохранен в скопированном сообщении.</span><span class="sxs-lookup"><span data-stu-id="b001a-184">Depending on the message store provider, the entry identifier of the original message may or may not be preserved in the copied message.</span></span> <span data-ttu-id="b001a-185">Рекомендуется сохранять идентификаторы записей везде, где это возможно, но это не является обязательным требованием.</span><span class="sxs-lookup"><span data-stu-id="b001a-185">You should preserve entry identifiers whenever possible, but it is not a requirement.</span></span> <span data-ttu-id="b001a-186">Как правило, вы можете зависеть от следующих сценариев:</span><span class="sxs-lookup"><span data-stu-id="b001a-186">You can generally depend on the following scenarios:</span></span>
  
- <span data-ttu-id="b001a-187">Когда вы перемещаете папку между двумя разными типами хранилищ сообщений, идентификатор записи гарантированно изменяется.</span><span class="sxs-lookup"><span data-stu-id="b001a-187">When you move a folder between two different types of message stores, the entry identifier is guaranteed to change.</span></span>
    
- <span data-ttu-id="b001a-188">Когда вы перемещаете папку между двумя хранилищами одного и того же типа, идентификатор записи почти всегда изменяется.</span><span class="sxs-lookup"><span data-stu-id="b001a-188">When you move a folder between two message stores of the same type, the entry identifier almost always changes.</span></span>
    
- <span data-ttu-id="b001a-189">Когда вы перемещаете папку в другое расположение в том же хранилище сообщений, идентификатор записи может измениться или может не измениться в зависимости от поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="b001a-189">When you move a folder to another location in the same message store, the entry identifier may or may not change, depending on the message store provider.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="b001a-190">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="b001a-190">MFCMAPI reference</span></span>

<span data-ttu-id="b001a-191">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="b001a-191">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b001a-192">**Файл**</span><span class="sxs-lookup"><span data-stu-id="b001a-192">**File**</span></span>|<span data-ttu-id="b001a-193">**Функция**</span><span class="sxs-lookup"><span data-stu-id="b001a-193">**Function**</span></span>|<span data-ttu-id="b001a-194">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="b001a-194">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b001a-195">Мсгсторедлг. cpp</span><span class="sxs-lookup"><span data-stu-id="b001a-195">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="b001a-196">Кмсгсторедлг:: Онпастефолдер</span><span class="sxs-lookup"><span data-stu-id="b001a-196">CMsgStoreDlg::OnPasteFolder</span></span>  <br/> |<span data-ttu-id="b001a-197">MFCMAPI использует метод **IMAPIFolder:: CopyFolder** , чтобы скопировать папки из одного расположения в другое.</span><span class="sxs-lookup"><span data-stu-id="b001a-197">MFCMAPI uses the **IMAPIFolder::CopyFolder** method to copy folders from one location to another.</span></span> <span data-ttu-id="b001a-198">MFCMAPI запоминает исходную папку во время операции копирования и фактически выполняет копию во время операции вставки.</span><span class="sxs-lookup"><span data-stu-id="b001a-198">MFCMAPI remembers the source folder during the copy operation and actually performs the copy during the paste operation.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b001a-199">См. также</span><span class="sxs-lookup"><span data-stu-id="b001a-199">See also</span></span>



[<span data-ttu-id="b001a-200">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="b001a-200">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="b001a-201">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="b001a-201">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

