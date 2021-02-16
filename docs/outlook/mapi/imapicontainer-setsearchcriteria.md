---
title: IMAPIContainerSetSearchCriteria
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer.SetSearchCriteria
api_type:
- COM
ms.assetid: b5eb1841-e450-4024-aeaa-3b5a492ddb99
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a6168e8fced2fff3a7f9d273e47ed2410ac4c010
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427201"
---
# <a name="imapicontainersetsearchcriteria"></a><span data-ttu-id="24323-103">IMAPIContainer::SetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="24323-103">IMAPIContainer::SetSearchCriteria</span></span>

  
  
<span data-ttu-id="24323-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="24323-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="24323-105">Устанавливает условия поиска для контейнера.</span><span class="sxs-lookup"><span data-stu-id="24323-105">Establishes search criteria for the container.</span></span>
  
```cpp
HRESULT SetSearchCriteria(
  LPSRestriction lpRestriction,
  LPENTRYLIST lpContainerList,
  ULONG ulSearchFlags
);
```

## <a name="parameters"></a><span data-ttu-id="24323-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="24323-106">Parameters</span></span>

 <span data-ttu-id="24323-107">_lpRestriction_</span><span class="sxs-lookup"><span data-stu-id="24323-107">_lpRestriction_</span></span>
  
> <span data-ttu-id="24323-108">[in] Указатель на структуру [SRestriction,](srestriction.md) которая определяет условия поиска.</span><span class="sxs-lookup"><span data-stu-id="24323-108">[in] A pointer to an [SRestriction](srestriction.md) structure that defines the search criteria.</span></span> <span data-ttu-id="24323-109">Если в параметре  _lpRestriction_ передается NULL, критерии поиска, которые использовались недавно для этого контейнера, используются повторно.</span><span class="sxs-lookup"><span data-stu-id="24323-109">If NULL is passed in the  _lpRestriction_ parameter, the search criteria that were used most recently for this container are used again.</span></span> <span data-ttu-id="24323-110">NULL не следует передавать в  _lpRestriction_ для первого поиска в контейнере.</span><span class="sxs-lookup"><span data-stu-id="24323-110">NULL should not be passed in  _lpRestriction_ for the first search in a container.</span></span> 
    
 <span data-ttu-id="24323-111">_lpContainerList_</span><span class="sxs-lookup"><span data-stu-id="24323-111">_lpContainerList_</span></span>
  
> <span data-ttu-id="24323-112">[in] Указатель на массив идентификаторов записей, которые представляют контейнеры, которые необходимо включить в поиск.</span><span class="sxs-lookup"><span data-stu-id="24323-112">[in] A pointer to an array of entry identifiers that represent containers to be included in the search.</span></span> <span data-ttu-id="24323-113">Если клиент передает NULL в  _параметре lpContainerList,_ идентификаторы записей, использованные недавно для поиска в этом контейнере, используются для нового поиска.</span><span class="sxs-lookup"><span data-stu-id="24323-113">If a client passes NULL in the  _lpContainerList_ parameter, the entry identifiers used most recently to search this container are used for the new search.</span></span> <span data-ttu-id="24323-114">Клиент не должен передавать NULL в  _lpContainerList_ для первого поиска в контейнере.</span><span class="sxs-lookup"><span data-stu-id="24323-114">A client should not pass NULL in  _lpContainerList_ for the first search in a container.</span></span> 
    
 <span data-ttu-id="24323-115">_ulSearchFlags_</span><span class="sxs-lookup"><span data-stu-id="24323-115">_ulSearchFlags_</span></span>
  
> <span data-ttu-id="24323-116">[in] Битоваяmas флагов, которые контролируют выполнение поиска.</span><span class="sxs-lookup"><span data-stu-id="24323-116">[in] A bitmask of flags that control how the search is performed.</span></span> <span data-ttu-id="24323-117">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="24323-117">The following flags can be set:</span></span>
    
<span data-ttu-id="24323-118">BACKGROUND_SEARCH</span><span class="sxs-lookup"><span data-stu-id="24323-118">BACKGROUND_SEARCH</span></span> 
  
> <span data-ttu-id="24323-119">Поиск должен запускаться с обычным приоритетом относительно других поисковых запросов.</span><span class="sxs-lookup"><span data-stu-id="24323-119">The search should run at normal priority relative to other searches.</span></span> <span data-ttu-id="24323-120">Этот флаг нельзя установить одновременно с флагом FOREGROUND_SEARCH флага.</span><span class="sxs-lookup"><span data-stu-id="24323-120">This flag cannot be set at the same time as the FOREGROUND_SEARCH flag.</span></span>
    
<span data-ttu-id="24323-121">FOREGROUND_SEARCH</span><span class="sxs-lookup"><span data-stu-id="24323-121">FOREGROUND_SEARCH</span></span> 
  
> <span data-ttu-id="24323-122">Поиск должен работать с высоким приоритетом относительно других поисковых запросов.</span><span class="sxs-lookup"><span data-stu-id="24323-122">The search should run at high priority relative to other searches.</span></span> <span data-ttu-id="24323-123">Этот флаг нельзя установить одновременно с флагом BACKGROUND_SEARCH флага.</span><span class="sxs-lookup"><span data-stu-id="24323-123">This flag cannot be set at the same time as the BACKGROUND_SEARCH flag.</span></span>
    
<span data-ttu-id="24323-124">NON_CONTENT_INDEXED_SEARCH</span><span class="sxs-lookup"><span data-stu-id="24323-124">NON_CONTENT_INDEXED_SEARCH</span></span>
  
> <span data-ttu-id="24323-125">Поиск не должен использовать индексацию контента для поиска совпадающих записей.</span><span class="sxs-lookup"><span data-stu-id="24323-125">The search should not use content indexing to find matching entries.</span></span> <span data-ttu-id="24323-126">Этот флаг действителен только для хранилищ Exchange.</span><span class="sxs-lookup"><span data-stu-id="24323-126">This flag is only valid for Exchange stores.</span></span>
    
<span data-ttu-id="24323-127">RECURSIVE_SEARCH</span><span class="sxs-lookup"><span data-stu-id="24323-127">RECURSIVE_SEARCH</span></span> 
  
> <span data-ttu-id="24323-128">Поиск должен включать контейнеры, указанные в параметре  _lpContainerList,_ и все их потомки.</span><span class="sxs-lookup"><span data-stu-id="24323-128">The search should include the containers specified in the  _lpContainerList_ parameter and all their child containers.</span></span> <span data-ttu-id="24323-129">Этот флаг нельзя установить одновременно с флагом SHALLOW_SEARCH флага.</span><span class="sxs-lookup"><span data-stu-id="24323-129">This flag cannot be set at the same time as the SHALLOW_SEARCH flag.</span></span> 
    
<span data-ttu-id="24323-130">RESTART_SEARCH</span><span class="sxs-lookup"><span data-stu-id="24323-130">RESTART_SEARCH</span></span> 
  
> <span data-ttu-id="24323-131">Поиск следует инициировать, если это первый вызов **SetSearchCriteria,** или перезапустить, если поиск неактивный.</span><span class="sxs-lookup"><span data-stu-id="24323-131">The search should be initiated if this is the first call to **SetSearchCriteria**, or restarted if the search is inactive.</span></span> <span data-ttu-id="24323-132">Этот флаг нельзя установить одновременно с флагом STOP_SEARCH флага.</span><span class="sxs-lookup"><span data-stu-id="24323-132">This flag cannot be set at the same time as the STOP_SEARCH flag.</span></span>
    
<span data-ttu-id="24323-133">SHALLOW_SEARCH</span><span class="sxs-lookup"><span data-stu-id="24323-133">SHALLOW_SEARCH</span></span> 
  
> <span data-ttu-id="24323-134">Поиск должен выглядеть только в контейнерах, указанных в параметре  _lpContainerList_ для совпадающих записей.</span><span class="sxs-lookup"><span data-stu-id="24323-134">The search should look only in the containers specified in the  _lpContainerList_ parameter for matching entries.</span></span> <span data-ttu-id="24323-135">Этот флаг нельзя установить одновременно с флагом RECURSIVE_SEARCH флага.</span><span class="sxs-lookup"><span data-stu-id="24323-135">This flag cannot be set at the same time as the RECURSIVE_SEARCH flag.</span></span> 
    
<span data-ttu-id="24323-136">STOP_SEARCH</span><span class="sxs-lookup"><span data-stu-id="24323-136">STOP_SEARCH</span></span> 
  
> <span data-ttu-id="24323-137">Поиск должен быть остановлен.</span><span class="sxs-lookup"><span data-stu-id="24323-137">The search should be stopped.</span></span> <span data-ttu-id="24323-138">Этот флаг нельзя установить одновременно с флагом RESTART_SEARCH флага.</span><span class="sxs-lookup"><span data-stu-id="24323-138">This flag cannot be set at the same time as the RESTART_SEARCH flag.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="24323-139">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="24323-139">Return value</span></span>

<span data-ttu-id="24323-140">S_OK</span><span class="sxs-lookup"><span data-stu-id="24323-140">S_OK</span></span> 
  
> <span data-ttu-id="24323-141">Критерии поиска успешно установлены.</span><span class="sxs-lookup"><span data-stu-id="24323-141">The search criteria was successfully set.</span></span>
    
<span data-ttu-id="24323-142">MAPI_E_TOO_COMPLEX</span><span class="sxs-lookup"><span data-stu-id="24323-142">MAPI_E_TOO_COMPLEX</span></span> 
  
> <span data-ttu-id="24323-143">Поставщик услуг не поддерживает указанные условия поиска.</span><span class="sxs-lookup"><span data-stu-id="24323-143">The service provider does not support the specified search criteria.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="24323-144">Примечания</span><span class="sxs-lookup"><span data-stu-id="24323-144">Remarks</span></span>

<span data-ttu-id="24323-145">Метод **IMAPIContainer::SetSearchCriteria** устанавливает условия поиска для контейнера, который поддерживает поиск, как правило, папку результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="24323-145">The **IMAPIContainer::SetSearchCriteria** method establishes search criteria for a container that supports searches, typically a search-results folder.</span></span> <span data-ttu-id="24323-146">Папка результатов поиска содержит ссылки на сообщения, которые соответствуют условиям поиска; фактические сообщения по-прежнему хранятся в их исходных расположениях.</span><span class="sxs-lookup"><span data-stu-id="24323-146">A search-results folder contains links to the messages that meet the search criteria; the actual messages are still stored in their original locations.</span></span> <span data-ttu-id="24323-147">Единственные уникальные данные, содержащиеся в папке результатов поиска, — это ее таблица содержимого.</span><span class="sxs-lookup"><span data-stu-id="24323-147">The only unique data that is contained in a search-results folder is its contents table.</span></span> <span data-ttu-id="24323-148">Таблица содержимого папки результатов поиска имеет объединенную информацию о хранилище сообщений после примененного ограничения поиска.</span><span class="sxs-lookup"><span data-stu-id="24323-148">The contents table of a search-results folder has the merged contents of the message store after the search restriction has been applied.</span></span> 
  
<span data-ttu-id="24323-149">Операция поиска работает только в этой объединенной таблице содержимого; он не будет искать другие папки результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="24323-149">A search operation works only on this merged contents table; it does not search through other search-results folders.</span></span> <span data-ttu-id="24323-150">Результаты поиска возвращают только сообщения, которые соответствуют условиям поиска; Иерархия папок не возвращается.</span><span class="sxs-lookup"><span data-stu-id="24323-150">The search results return only the messages that match the search criteria; the folder hierarchy is not returned.</span></span>
  
<span data-ttu-id="24323-151">После завершения поиска клиенту возвращается управление.</span><span class="sxs-lookup"><span data-stu-id="24323-151">Control is returned to the client when the search has finished.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="24323-152">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="24323-152">Notes to implementers</span></span>

<span data-ttu-id="24323-153">Контейнеры адресных книг устанавливают условия поиска, применяя ограничения к своим таблицам содержимого.</span><span class="sxs-lookup"><span data-stu-id="24323-153">Address book containers establish search criteria by applying restrictions to their contents tables.</span></span> <span data-ttu-id="24323-154">Дополнительные сведения о критериях поиска и контейнерах адресной книги см. в этой [теме.](implementing-advanced-searching.md)</span><span class="sxs-lookup"><span data-stu-id="24323-154">For more information about search criteria and address book containers, see [Implementing Advanced Searching](implementing-advanced-searching.md).</span></span>
  
<span data-ttu-id="24323-155">Операции открытия, копирования, перемещения и удаления сообщений в папках результатов поиска должны поддерживаться, а не в самой папке результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="24323-155">You should support open, copy, move, and delete operations on the messages within search-results folders, not on the search-results folder itself.</span></span> <span data-ttu-id="24323-156">Не разрешать создавать сообщения в папке результатов поиска или копировать их в нее.</span><span class="sxs-lookup"><span data-stu-id="24323-156">Do not allow messages to be created within or copied into a search-results folder.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="24323-157">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="24323-157">Notes to callers</span></span>

<span data-ttu-id="24323-158">Чтобы найти получателей сообщений, установите _для lpRestriction_ ограничение подобъекта с членом **ulSubObject** в структуре [SSubRestriction,](ssubrestriction.md) задав для **него** PR_MESSAGE_RECIPIENTS ([PidTagMessageRecipients).](pidtagmessagerecipients-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="24323-158">To search for message recipients, set  _lpRestriction_ to point to a subobject restriction with the **ulSubObject** member in the [SSubRestriction](ssubrestriction.md) structure set to **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)).</span></span> <span data-ttu-id="24323-159">Чтобы найти вложения, установите для члена **ulSubObject** PR_MESSAGE_ATTACHMENTS **(** [PidTagMessageAttachments).](pidtagmessageattachments-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="24323-159">To search for attachments, set the **ulSubObject** member to **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)).</span></span> <span data-ttu-id="24323-160">Установите для **члена lpRes** ограничение свойства, которое описывает условия поиска для получателей или вложений.</span><span class="sxs-lookup"><span data-stu-id="24323-160">Set the **lpRes** member to point to a property restriction that describes the search criteria for the recipients or attachments.</span></span> 
  
<span data-ttu-id="24323-161">Например, чтобы найти вложения с расширением MSS, установите для **ulSubObject** PR_MESSAGE_ATTACHMENTS и **lpRes** ограничение свойства, которое соответствует **PR_ATTACH_EXTENSION** ([PidTagAttachExtension)](pidtagattachextension-canonical-property.md)с .mss. </span><span class="sxs-lookup"><span data-stu-id="24323-161">For example, to look for file attachments that have the extension .mss, set **ulSubObject** to **PR_MESSAGE_ATTACHMENTS** and **lpRes** to a property restriction that matches **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) with .mss.</span></span>
  
<span data-ttu-id="24323-162">Установка флага FOREGROUND_SEARCH в параметре  _ulSearchFlags_ может привести к снижению производительности системы.</span><span class="sxs-lookup"><span data-stu-id="24323-162">Setting the FOREGROUND_SEARCH flag in the  _ulSearchFlags_ parameter could cause a decrease in system performance.</span></span> 
  
<span data-ttu-id="24323-163">С помощью **SetSearchCriteria** можно изменить условия поиска, которые уже ведутся.</span><span class="sxs-lookup"><span data-stu-id="24323-163">You can use **SetSearchCriteria** to change the search criteria of a search already in progress.</span></span> <span data-ttu-id="24323-164">Можно указать новые ограничения, новые списки папок для поиска и новый приоритет поиска, например обновление поиска до более высокого приоритета.</span><span class="sxs-lookup"><span data-stu-id="24323-164">You can specify new restrictions, new lists of folders to search, and a new search priority, such as upgrading a search to a higher priority.</span></span> <span data-ttu-id="24323-165">Изменения приоритета поиска не приводят к перезапуску существующего поиска, но другие изменения в критериях поиска могут быть.</span><span class="sxs-lookup"><span data-stu-id="24323-165">Changes in search priority do not cause an existing search to restart, but other changes to search criteria can.</span></span> 
  
<span data-ttu-id="24323-166">Когда вы используете папку результатов поиска, вы можете удалить ее или позволить ей оставаться открытой для использования в дальнейшем.</span><span class="sxs-lookup"><span data-stu-id="24323-166">When you are through using a search-results folder, you can either delete the folder or let it remain open for later use.</span></span> <span data-ttu-id="24323-167">Если удалить папку результатов поиска, удаляются только ссылки на сообщения.</span><span class="sxs-lookup"><span data-stu-id="24323-167">If you do delete the search-results folder, only message links are deleted.</span></span> <span data-ttu-id="24323-168">Фактические сообщения остаются в родительских папках.</span><span class="sxs-lookup"><span data-stu-id="24323-168">The actual messages remain in their parent folders.</span></span> 
  
<span data-ttu-id="24323-169">Дополнительные сведения о папках результатов поиска см. в папках поиска [MAPI.](mapi-search-folders.md)</span><span class="sxs-lookup"><span data-stu-id="24323-169">For more information about search-results folders, see [MAPI Search Folders](mapi-search-folders.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="24323-170">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="24323-170">MFCMAPI reference</span></span>

<span data-ttu-id="24323-171">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="24323-171">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="24323-172">**Файл**</span><span class="sxs-lookup"><span data-stu-id="24323-172">**File**</span></span>|<span data-ttu-id="24323-173">**Функция**</span><span class="sxs-lookup"><span data-stu-id="24323-173">**Function**</span></span>|<span data-ttu-id="24323-174">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="24323-174">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="24323-175">HierarchyTableDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="24323-175">HierarchyTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="24323-176">CHierarchyTableDlg::OnEditSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="24323-176">CHierarchyTableDlg::OnEditSearchCriteria</span></span>  <br/> |<span data-ttu-id="24323-177">MFCMAPI использует метод **IMAPIContainer::SetSearchCriteria** для написания критериев поиска для папки после ее изменения пользователем.</span><span class="sxs-lookup"><span data-stu-id="24323-177">MFCMAPI uses the **IMAPIContainer::SetSearchCriteria** method to write search criteria for a folder after a user has edited it.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="24323-178">См. также</span><span class="sxs-lookup"><span data-stu-id="24323-178">See also</span></span>



[<span data-ttu-id="24323-179">IMAPIContainer::GetContentsTable</span><span class="sxs-lookup"><span data-stu-id="24323-179">IMAPIContainer::GetContentsTable</span></span>](imapicontainer-getcontentstable.md)
  
[<span data-ttu-id="24323-180">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="24323-180">IMAPIContainer::OpenEntry</span></span>](imapicontainer-openentry.md)
  
[<span data-ttu-id="24323-181">IMAPIFolder::CreateFolder</span><span class="sxs-lookup"><span data-stu-id="24323-181">IMAPIFolder::CreateFolder</span></span>](imapifolder-createfolder.md)
  
[<span data-ttu-id="24323-182">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="24323-182">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
  
[<span data-ttu-id="24323-183">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="24323-183">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="24323-184">SRestriction</span><span class="sxs-lookup"><span data-stu-id="24323-184">SRestriction</span></span>](srestriction.md)
  
[<span data-ttu-id="24323-185">SSubRestriction</span><span class="sxs-lookup"><span data-stu-id="24323-185">SSubRestriction</span></span>](ssubrestriction.md)
  
[<span data-ttu-id="24323-186">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="24323-186">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


[<span data-ttu-id="24323-187">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="24323-187">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

