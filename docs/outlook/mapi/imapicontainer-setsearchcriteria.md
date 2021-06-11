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
# <a name="imapicontainersetsearchcriteria"></a><span data-ttu-id="24a6a-103">IMAPIContainer::SetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="24a6a-103">IMAPIContainer::SetSearchCriteria</span></span>

  
  
<span data-ttu-id="24a6a-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="24a6a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="24a6a-105">Устанавливает критерии поиска для контейнера.</span><span class="sxs-lookup"><span data-stu-id="24a6a-105">Establishes search criteria for the container.</span></span>
  
```cpp
HRESULT SetSearchCriteria(
  LPSRestriction lpRestriction,
  LPENTRYLIST lpContainerList,
  ULONG ulSearchFlags
);
```

## <a name="parameters"></a><span data-ttu-id="24a6a-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="24a6a-106">Parameters</span></span>

 <span data-ttu-id="24a6a-107">_lpRestriction_</span><span class="sxs-lookup"><span data-stu-id="24a6a-107">_lpRestriction_</span></span>
  
> <span data-ttu-id="24a6a-108">[in] Указатель на [структуру SRestriction,](srestriction.md) определяемую критериями поиска.</span><span class="sxs-lookup"><span data-stu-id="24a6a-108">[in] A pointer to an [SRestriction](srestriction.md) structure that defines the search criteria.</span></span> <span data-ttu-id="24a6a-109">Если NULL передается в  _параметре lpRestriction,_ снова используются критерии поиска, которые использовались совсем недавно для этого контейнера.</span><span class="sxs-lookup"><span data-stu-id="24a6a-109">If NULL is passed in the  _lpRestriction_ parameter, the search criteria that were used most recently for this container are used again.</span></span> <span data-ttu-id="24a6a-110">NULL не следует передавать в  _lpRestriction_ для первого поиска в контейнере.</span><span class="sxs-lookup"><span data-stu-id="24a6a-110">NULL should not be passed in  _lpRestriction_ for the first search in a container.</span></span> 
    
 <span data-ttu-id="24a6a-111">_lpContainerList_</span><span class="sxs-lookup"><span data-stu-id="24a6a-111">_lpContainerList_</span></span>
  
> <span data-ttu-id="24a6a-112">[in] Указатель на массив идентификаторов записей, которые представляют контейнеры, которые будут включены в поиск.</span><span class="sxs-lookup"><span data-stu-id="24a6a-112">[in] A pointer to an array of entry identifiers that represent containers to be included in the search.</span></span> <span data-ttu-id="24a6a-113">Если клиент передает NULL в  _параметре lpContainerList,_ идентификаторы записей, используемые совсем недавно для поиска этого контейнера, используются для нового поиска.</span><span class="sxs-lookup"><span data-stu-id="24a6a-113">If a client passes NULL in the  _lpContainerList_ parameter, the entry identifiers used most recently to search this container are used for the new search.</span></span> <span data-ttu-id="24a6a-114">Клиент не должен передавать NULL в  _lpContainerList_ для первого поиска в контейнере.</span><span class="sxs-lookup"><span data-stu-id="24a6a-114">A client should not pass NULL in  _lpContainerList_ for the first search in a container.</span></span> 
    
 <span data-ttu-id="24a6a-115">_ulSearchFlags_</span><span class="sxs-lookup"><span data-stu-id="24a6a-115">_ulSearchFlags_</span></span>
  
> <span data-ttu-id="24a6a-116">[in] Немного флагов, которые контролируют выполнение поиска.</span><span class="sxs-lookup"><span data-stu-id="24a6a-116">[in] A bitmask of flags that control how the search is performed.</span></span> <span data-ttu-id="24a6a-117">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="24a6a-117">The following flags can be set:</span></span>
    
<span data-ttu-id="24a6a-118">BACKGROUND_SEARCH</span><span class="sxs-lookup"><span data-stu-id="24a6a-118">BACKGROUND_SEARCH</span></span> 
  
> <span data-ttu-id="24a6a-119">Поиск должен работать в обычном приоритете по сравнению с другими поисками.</span><span class="sxs-lookup"><span data-stu-id="24a6a-119">The search should run at normal priority relative to other searches.</span></span> <span data-ttu-id="24a6a-120">Этот флаг нельзя установить одновременно с FOREGROUND_SEARCH флагом.</span><span class="sxs-lookup"><span data-stu-id="24a6a-120">This flag cannot be set at the same time as the FOREGROUND_SEARCH flag.</span></span>
    
<span data-ttu-id="24a6a-121">FOREGROUND_SEARCH</span><span class="sxs-lookup"><span data-stu-id="24a6a-121">FOREGROUND_SEARCH</span></span> 
  
> <span data-ttu-id="24a6a-122">Поиск должен работать с высоким приоритетом по сравнению с другими поисками.</span><span class="sxs-lookup"><span data-stu-id="24a6a-122">The search should run at high priority relative to other searches.</span></span> <span data-ttu-id="24a6a-123">Этот флаг не может быть установлен одновременно с BACKGROUND_SEARCH флагом.</span><span class="sxs-lookup"><span data-stu-id="24a6a-123">This flag cannot be set at the same time as the BACKGROUND_SEARCH flag.</span></span>
    
<span data-ttu-id="24a6a-124">NON_CONTENT_INDEXED_SEARCH</span><span class="sxs-lookup"><span data-stu-id="24a6a-124">NON_CONTENT_INDEXED_SEARCH</span></span>
  
> <span data-ttu-id="24a6a-125">Поиск не должен использовать индексацию контента для поиска совпадающих записей.</span><span class="sxs-lookup"><span data-stu-id="24a6a-125">The search should not use content indexing to find matching entries.</span></span> <span data-ttu-id="24a6a-126">Этот флаг действителен только для Exchange магазинов.</span><span class="sxs-lookup"><span data-stu-id="24a6a-126">This flag is only valid for Exchange stores.</span></span>
    
<span data-ttu-id="24a6a-127">RECURSIVE_SEARCH</span><span class="sxs-lookup"><span data-stu-id="24a6a-127">RECURSIVE_SEARCH</span></span> 
  
> <span data-ttu-id="24a6a-128">Поиск должен включать контейнеры, указанные в параметре  _lpContainerList,_ и все их детские контейнеры.</span><span class="sxs-lookup"><span data-stu-id="24a6a-128">The search should include the containers specified in the  _lpContainerList_ parameter and all their child containers.</span></span> <span data-ttu-id="24a6a-129">Этот флаг нельзя установить одновременно с SHALLOW_SEARCH флагом.</span><span class="sxs-lookup"><span data-stu-id="24a6a-129">This flag cannot be set at the same time as the SHALLOW_SEARCH flag.</span></span> 
    
<span data-ttu-id="24a6a-130">RESTART_SEARCH</span><span class="sxs-lookup"><span data-stu-id="24a6a-130">RESTART_SEARCH</span></span> 
  
> <span data-ttu-id="24a6a-131">Поиск следует начать, если это первый вызов **в SetSearchCriteria,** или перезапустить, если поиск неактивный.</span><span class="sxs-lookup"><span data-stu-id="24a6a-131">The search should be initiated if this is the first call to **SetSearchCriteria**, or restarted if the search is inactive.</span></span> <span data-ttu-id="24a6a-132">Этот флаг нельзя установить одновременно с STOP_SEARCH флагом.</span><span class="sxs-lookup"><span data-stu-id="24a6a-132">This flag cannot be set at the same time as the STOP_SEARCH flag.</span></span>
    
<span data-ttu-id="24a6a-133">SHALLOW_SEARCH</span><span class="sxs-lookup"><span data-stu-id="24a6a-133">SHALLOW_SEARCH</span></span> 
  
> <span data-ttu-id="24a6a-134">Поиск должен искаться только в контейнерах, указанных в параметре  _lpContainerList_ для совпадения записей.</span><span class="sxs-lookup"><span data-stu-id="24a6a-134">The search should look only in the containers specified in the  _lpContainerList_ parameter for matching entries.</span></span> <span data-ttu-id="24a6a-135">Этот флаг нельзя установить одновременно с RECURSIVE_SEARCH флагом.</span><span class="sxs-lookup"><span data-stu-id="24a6a-135">This flag cannot be set at the same time as the RECURSIVE_SEARCH flag.</span></span> 
    
<span data-ttu-id="24a6a-136">STOP_SEARCH</span><span class="sxs-lookup"><span data-stu-id="24a6a-136">STOP_SEARCH</span></span> 
  
> <span data-ttu-id="24a6a-137">Поиск должен быть остановлен.</span><span class="sxs-lookup"><span data-stu-id="24a6a-137">The search should be stopped.</span></span> <span data-ttu-id="24a6a-138">Этот флаг не может быть установлен одновременно с RESTART_SEARCH флагом.</span><span class="sxs-lookup"><span data-stu-id="24a6a-138">This flag cannot be set at the same time as the RESTART_SEARCH flag.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="24a6a-139">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="24a6a-139">Return value</span></span>

<span data-ttu-id="24a6a-140">S_OK</span><span class="sxs-lookup"><span data-stu-id="24a6a-140">S_OK</span></span> 
  
> <span data-ttu-id="24a6a-141">Критерии поиска были успешно установлены.</span><span class="sxs-lookup"><span data-stu-id="24a6a-141">The search criteria was successfully set.</span></span>
    
<span data-ttu-id="24a6a-142">MAPI_E_TOO_COMPLEX</span><span class="sxs-lookup"><span data-stu-id="24a6a-142">MAPI_E_TOO_COMPLEX</span></span> 
  
> <span data-ttu-id="24a6a-143">Поставщик услуг не поддерживает указанные критерии поиска.</span><span class="sxs-lookup"><span data-stu-id="24a6a-143">The service provider does not support the specified search criteria.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="24a6a-144">Примечания</span><span class="sxs-lookup"><span data-stu-id="24a6a-144">Remarks</span></span>

<span data-ttu-id="24a6a-145">Метод **IMAPIContainer::SetSearchCriteria** устанавливает критерии поиска для контейнера, поддерживающем поиск, как правило, папки результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="24a6a-145">The **IMAPIContainer::SetSearchCriteria** method establishes search criteria for a container that supports searches, typically a search-results folder.</span></span> <span data-ttu-id="24a6a-146">Папка результатов поиска содержит ссылки на сообщения, которые соответствуют критериям поиска; фактические сообщения по-прежнему хранятся в исходных расположениях.</span><span class="sxs-lookup"><span data-stu-id="24a6a-146">A search-results folder contains links to the messages that meet the search criteria; the actual messages are still stored in their original locations.</span></span> <span data-ttu-id="24a6a-147">Единственные уникальные данные, содержащиеся в папке результатов поиска, — это ее таблица контента.</span><span class="sxs-lookup"><span data-stu-id="24a6a-147">The only unique data that is contained in a search-results folder is its contents table.</span></span> <span data-ttu-id="24a6a-148">В таблице содержимого папки результатов поиска после примененного ограничения поиска слито содержимое магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="24a6a-148">The contents table of a search-results folder has the merged contents of the message store after the search restriction has been applied.</span></span> 
  
<span data-ttu-id="24a6a-149">Операция поиска работает только в этой объединенной таблице содержимого; он не будет искать в других папках результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="24a6a-149">A search operation works only on this merged contents table; it does not search through other search-results folders.</span></span> <span data-ttu-id="24a6a-150">Результаты поиска возвращают только сообщения, которые соответствуют критериям поиска; иерархия папок не возвращается.</span><span class="sxs-lookup"><span data-stu-id="24a6a-150">The search results return only the messages that match the search criteria; the folder hierarchy is not returned.</span></span>
  
<span data-ttu-id="24a6a-151">Управление возвращается клиенту по завершению поиска.</span><span class="sxs-lookup"><span data-stu-id="24a6a-151">Control is returned to the client when the search has finished.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="24a6a-152">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="24a6a-152">Notes to implementers</span></span>

<span data-ttu-id="24a6a-153">Контейнеры адресных книг устанавливают критерии поиска, применяя ограничения к таблицам контента.</span><span class="sxs-lookup"><span data-stu-id="24a6a-153">Address book containers establish search criteria by applying restrictions to their contents tables.</span></span> <span data-ttu-id="24a6a-154">Дополнительные сведения о критериях поиска и контейнерах адресной книги см. в книге [Implementing Advanced Search.](implementing-advanced-searching.md)</span><span class="sxs-lookup"><span data-stu-id="24a6a-154">For more information about search criteria and address book containers, see [Implementing Advanced Searching](implementing-advanced-searching.md).</span></span>
  
<span data-ttu-id="24a6a-155">Необходимо поддерживать открытие, копирование, перемещение и удаление операций на сообщениях в папках результатов поиска, а не в самой папке результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="24a6a-155">You should support open, copy, move, and delete operations on the messages within search-results folders, not on the search-results folder itself.</span></span> <span data-ttu-id="24a6a-156">Не допускайте создания сообщений в папке результатов поиска или их копирования.</span><span class="sxs-lookup"><span data-stu-id="24a6a-156">Do not allow messages to be created within or copied into a search-results folder.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="24a6a-157">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="24a6a-157">Notes to callers</span></span>

<span data-ttu-id="24a6a-158">Чтобы найти получателей сообщений, установите _lpRestriction,_ чтобы указать на ограничение субобъекта с членом **ulSubObject** в структуре [SSubRestriction,](ssubrestriction.md) задаваемой PR_MESSAGE_RECIPIENTS [(PidTagMessageRecipients).](pidtagmessagerecipients-canonical-property.md) </span><span class="sxs-lookup"><span data-stu-id="24a6a-158">To search for message recipients, set  _lpRestriction_ to point to a subobject restriction with the **ulSubObject** member in the [SSubRestriction](ssubrestriction.md) structure set to **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)).</span></span> <span data-ttu-id="24a6a-159">Чтобы найти вложения, установите **члену ulSubObject** PR_MESSAGE_ATTACHMENTS [(PidTagMessageAttachments).](pidtagmessageattachments-canonical-property.md) </span><span class="sxs-lookup"><span data-stu-id="24a6a-159">To search for attachments, set the **ulSubObject** member to **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)).</span></span> <span data-ttu-id="24a6a-160">Установите **члену lpRes** указать на ограничение свойств, которое описывает критерии поиска для получателей или вложений.</span><span class="sxs-lookup"><span data-stu-id="24a6a-160">Set the **lpRes** member to point to a property restriction that describes the search criteria for the recipients or attachments.</span></span> 
  
<span data-ttu-id="24a6a-161">Например, чтобы найти вложения файлов с расширением .mss, установите **ulSubObject** **для PR_MESSAGE_ATTACHMENTS** и **lpRes** к ограничению свойств, которое соответствует PR_ATTACH_EXTENSION [(PidTagAttachExtension)](pidtagattachextension-canonical-property.md)с .mss. </span><span class="sxs-lookup"><span data-stu-id="24a6a-161">For example, to look for file attachments that have the extension .mss, set **ulSubObject** to **PR_MESSAGE_ATTACHMENTS** and **lpRes** to a property restriction that matches **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) with .mss.</span></span>
  
<span data-ttu-id="24a6a-162">Установка флага FOREGROUND_SEARCH в  _параметре ulSearchFlags_ может привести к снижению производительности системы.</span><span class="sxs-lookup"><span data-stu-id="24a6a-162">Setting the FOREGROUND_SEARCH flag in the  _ulSearchFlags_ parameter could cause a decrease in system performance.</span></span> 
  
<span data-ttu-id="24a6a-163">Вы можете использовать **SetSearchCriteria,** чтобы изменить критерии поиска уже в процессе поиска.</span><span class="sxs-lookup"><span data-stu-id="24a6a-163">You can use **SetSearchCriteria** to change the search criteria of a search already in progress.</span></span> <span data-ttu-id="24a6a-164">Можно указать новые ограничения, новые списки папок для поиска и новый приоритет поиска, например обновление поиска до более высокого приоритета.</span><span class="sxs-lookup"><span data-stu-id="24a6a-164">You can specify new restrictions, new lists of folders to search, and a new search priority, such as upgrading a search to a higher priority.</span></span> <span data-ttu-id="24a6a-165">Изменения приоритета поиска не приводят к перезапуску существующего поиска, но другие изменения в критериях поиска могут быть.</span><span class="sxs-lookup"><span data-stu-id="24a6a-165">Changes in search priority do not cause an existing search to restart, but other changes to search criteria can.</span></span> 
  
<span data-ttu-id="24a6a-166">Когда вы используете папку результатов поиска, вы можете удалить папку или позволить ей оставаться открытой для более позднего использования.</span><span class="sxs-lookup"><span data-stu-id="24a6a-166">When you are through using a search-results folder, you can either delete the folder or let it remain open for later use.</span></span> <span data-ttu-id="24a6a-167">Если вы удалите папку результатов поиска, удаляются только ссылки на сообщения.</span><span class="sxs-lookup"><span data-stu-id="24a6a-167">If you do delete the search-results folder, only message links are deleted.</span></span> <span data-ttu-id="24a6a-168">Фактические сообщения остаются в родительских папках.</span><span class="sxs-lookup"><span data-stu-id="24a6a-168">The actual messages remain in their parent folders.</span></span> 
  
<span data-ttu-id="24a6a-169">Дополнительные сведения о папках результатов поиска см. в [папках поиска MAPI.](mapi-search-folders.md)</span><span class="sxs-lookup"><span data-stu-id="24a6a-169">For more information about search-results folders, see [MAPI Search Folders](mapi-search-folders.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="24a6a-170">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="24a6a-170">MFCMAPI reference</span></span>

<span data-ttu-id="24a6a-171">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="24a6a-171">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="24a6a-172">**Файл**</span><span class="sxs-lookup"><span data-stu-id="24a6a-172">**File**</span></span>|<span data-ttu-id="24a6a-173">**Функция**</span><span class="sxs-lookup"><span data-stu-id="24a6a-173">**Function**</span></span>|<span data-ttu-id="24a6a-174">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="24a6a-174">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="24a6a-175">HierarchyTableDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="24a6a-175">HierarchyTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="24a6a-176">CHierarchyTableDlg::OnEditSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="24a6a-176">CHierarchyTableDlg::OnEditSearchCriteria</span></span>  <br/> |<span data-ttu-id="24a6a-177">MFCMAPI использует метод **IMAPIContainer::SetSearchCriteria** для записи критериев поиска для папки после ее редактирования пользователем.</span><span class="sxs-lookup"><span data-stu-id="24a6a-177">MFCMAPI uses the **IMAPIContainer::SetSearchCriteria** method to write search criteria for a folder after a user has edited it.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="24a6a-178">См. также</span><span class="sxs-lookup"><span data-stu-id="24a6a-178">See also</span></span>



[<span data-ttu-id="24a6a-179">IMAPIContainer::GetContentsTable</span><span class="sxs-lookup"><span data-stu-id="24a6a-179">IMAPIContainer::GetContentsTable</span></span>](imapicontainer-getcontentstable.md)
  
[<span data-ttu-id="24a6a-180">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="24a6a-180">IMAPIContainer::OpenEntry</span></span>](imapicontainer-openentry.md)
  
[<span data-ttu-id="24a6a-181">IMAPIFolder::CreateFolder</span><span class="sxs-lookup"><span data-stu-id="24a6a-181">IMAPIFolder::CreateFolder</span></span>](imapifolder-createfolder.md)
  
[<span data-ttu-id="24a6a-182">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="24a6a-182">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
  
[<span data-ttu-id="24a6a-183">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="24a6a-183">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="24a6a-184">SRestriction</span><span class="sxs-lookup"><span data-stu-id="24a6a-184">SRestriction</span></span>](srestriction.md)
  
[<span data-ttu-id="24a6a-185">SSubRestriction</span><span class="sxs-lookup"><span data-stu-id="24a6a-185">SSubRestriction</span></span>](ssubrestriction.md)
  
[<span data-ttu-id="24a6a-186">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="24a6a-186">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


[<span data-ttu-id="24a6a-187">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="24a6a-187">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

