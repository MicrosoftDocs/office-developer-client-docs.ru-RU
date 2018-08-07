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
ms.openlocfilehash: 93578300e2520dda4a9621b05ac6a79c54eca2ef
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/15/2018
ms.locfileid: "19808839"
---
# <a name="imapicontainersetsearchcriteria"></a><span data-ttu-id="7d0ed-103">IMAPIContainer::SetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="7d0ed-103">IMAPIContainer::SetSearchCriteria</span></span>

  
  
<span data-ttu-id="7d0ed-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7d0ed-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7d0ed-105">Устанавливает условия поиска для контейнера.</span><span class="sxs-lookup"><span data-stu-id="7d0ed-105">Establishes search criteria for the container.</span></span>
  
```cpp
HRESULT SetSearchCriteria(
  LPSRestriction lpRestriction,
  LPENTRYLIST lpContainerList,
  ULONG ulSearchFlags
);
```

## <a name="parameters"></a><span data-ttu-id="7d0ed-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7d0ed-106">Parameters</span></span>

 <span data-ttu-id="7d0ed-107">_lpRestriction_</span><span class="sxs-lookup"><span data-stu-id="7d0ed-107">_lpRestriction_</span></span>
  
> <span data-ttu-id="7d0ed-108">[in] Указатель на структуру [SRestriction](srestriction.md) , определяющий условия поиска.</span><span class="sxs-lookup"><span data-stu-id="7d0ed-108">[in] A pointer to an [SRestriction](srestriction.md) structure that defines the search criteria.</span></span> <span data-ttu-id="7d0ed-109">Если NULL передается в параметре _lpRestriction_ , условия поиска, которые использовались для этого контейнера наиболее часто используются еще раз.</span><span class="sxs-lookup"><span data-stu-id="7d0ed-109">If NULL is passed in the  _lpRestriction_ parameter, the search criteria that were used most recently for this container are used again.</span></span> <span data-ttu-id="7d0ed-110">NULL не следует передавать в _lpRestriction_ для первого поиска в контейнере.</span><span class="sxs-lookup"><span data-stu-id="7d0ed-110">NULL should not be passed in  _lpRestriction_ for the first search in a container.</span></span> 
    
 <span data-ttu-id="7d0ed-111">_lpContainerList_</span><span class="sxs-lookup"><span data-stu-id="7d0ed-111">_lpContainerList_</span></span>
  
> <span data-ttu-id="7d0ed-112">[in] Указатель на массив идентификаторов записи, которые представляют контейнеров, включаемых в поиск.</span><span class="sxs-lookup"><span data-stu-id="7d0ed-112">[in] A pointer to an array of entry identifiers that represent containers to be included in the search.</span></span> <span data-ttu-id="7d0ed-113">Если клиент передает значение NULL в параметре _lpContainerList_ , идентификаторы записей, наиболее часто используемых для поиска в этом контейнере используются для нового поиска.</span><span class="sxs-lookup"><span data-stu-id="7d0ed-113">If a client passes NULL in the  _lpContainerList_ parameter, the entry identifiers used most recently to search this container are used for the new search.</span></span> <span data-ttu-id="7d0ed-114">Клиент не должны передавать NULL в _lpContainerList_ для первого поиска в контейнере.</span><span class="sxs-lookup"><span data-stu-id="7d0ed-114">A client should not pass NULL in  _lpContainerList_ for the first search in a container.</span></span> 
    
 <span data-ttu-id="7d0ed-115">_ulSearchFlags_</span><span class="sxs-lookup"><span data-stu-id="7d0ed-115">_ulSearchFlags_</span></span>
  
> <span data-ttu-id="7d0ed-116">[in] Битовая маска флаги, определяющие, как выполняется поиск.</span><span class="sxs-lookup"><span data-stu-id="7d0ed-116">[in] A bitmask of flags that control how the search is performed.</span></span> <span data-ttu-id="7d0ed-117">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="7d0ed-117">The following flags can be set:</span></span>
    
<span data-ttu-id="7d0ed-118">BACKGROUND_SEARCH</span><span class="sxs-lookup"><span data-stu-id="7d0ed-118">BACKGROUND_SEARCH</span></span> 
  
> <span data-ttu-id="7d0ed-119">Поиск должна запускаться с обычным приоритетом относительно других операций поиска.</span><span class="sxs-lookup"><span data-stu-id="7d0ed-119">The search should run at normal priority relative to other searches.</span></span> <span data-ttu-id="7d0ed-120">Этот флаг не могут задаваться одновременно флаг FOREGROUND_SEARCH.</span><span class="sxs-lookup"><span data-stu-id="7d0ed-120">This flag cannot be set at the same time as the FOREGROUND_SEARCH flag.</span></span>
    
<span data-ttu-id="7d0ed-121">FOREGROUND_SEARCH</span><span class="sxs-lookup"><span data-stu-id="7d0ed-121">FOREGROUND_SEARCH</span></span> 
  
> <span data-ttu-id="7d0ed-122">Поиск должен выполняться с наивысший приоритет относительно других операций поиска.</span><span class="sxs-lookup"><span data-stu-id="7d0ed-122">The search should run at high priority relative to other searches.</span></span> <span data-ttu-id="7d0ed-123">Этот флаг не могут задаваться одновременно флаг BACKGROUND_SEARCH.</span><span class="sxs-lookup"><span data-stu-id="7d0ed-123">This flag cannot be set at the same time as the BACKGROUND_SEARCH flag.</span></span>
    
<span data-ttu-id="7d0ed-124">NON_CONTENT_INDEXED_SEARCH</span><span class="sxs-lookup"><span data-stu-id="7d0ed-124">NON_CONTENT_INDEXED_SEARCH</span></span>
  
> <span data-ttu-id="7d0ed-125">Поиск не следует использовать индексирование содержимого для поиска соответствующих записей.</span><span class="sxs-lookup"><span data-stu-id="7d0ed-125">The search should not use content indexing to find matching entries.</span></span> <span data-ttu-id="7d0ed-126">Этот флаг допустимо только для хранилищ Exchange.</span><span class="sxs-lookup"><span data-stu-id="7d0ed-126">This flag is only valid for Exchange stores.</span></span>
    
<span data-ttu-id="7d0ed-127">RECURSIVE_SEARCH</span><span class="sxs-lookup"><span data-stu-id="7d0ed-127">RECURSIVE_SEARCH</span></span> 
  
> <span data-ttu-id="7d0ed-128">Поиск должен включать контейнеров, указанный в параметре _lpContainerList_ и всех его дочерних контейнеров.</span><span class="sxs-lookup"><span data-stu-id="7d0ed-128">The search should include the containers specified in the  _lpContainerList_ parameter and all their child containers.</span></span> <span data-ttu-id="7d0ed-129">Этот флаг не могут задаваться одновременно флаг SHALLOW_SEARCH.</span><span class="sxs-lookup"><span data-stu-id="7d0ed-129">This flag cannot be set at the same time as the SHALLOW_SEARCH flag.</span></span> 
    
<span data-ttu-id="7d0ed-130">RESTART_SEARCH</span><span class="sxs-lookup"><span data-stu-id="7d0ed-130">RESTART_SEARCH</span></span> 
  
> <span data-ttu-id="7d0ed-131">Поиск должен инициировал, если это первый вызов **SetSearchCriteria**или перезапустить Если поиска неактивных.</span><span class="sxs-lookup"><span data-stu-id="7d0ed-131">The search should be initiated if this is the first call to **SetSearchCriteria**, or restarted if the search is inactive.</span></span> <span data-ttu-id="7d0ed-132">Этот флаг не могут задаваться одновременно флаг STOP_SEARCH.</span><span class="sxs-lookup"><span data-stu-id="7d0ed-132">This flag cannot be set at the same time as the STOP_SEARCH flag.</span></span>
    
<span data-ttu-id="7d0ed-133">SHALLOW_SEARCH</span><span class="sxs-lookup"><span data-stu-id="7d0ed-133">SHALLOW_SEARCH</span></span> 
  
> <span data-ttu-id="7d0ed-134">Поиск должен выглядеть только в контейнерах, указанный в параметре _lpContainerList_ для соответствующих записей.</span><span class="sxs-lookup"><span data-stu-id="7d0ed-134">The search should look only in the containers specified in the  _lpContainerList_ parameter for matching entries.</span></span> <span data-ttu-id="7d0ed-135">Этот флаг не могут задаваться одновременно флаг RECURSIVE_SEARCH.</span><span class="sxs-lookup"><span data-stu-id="7d0ed-135">This flag cannot be set at the same time as the RECURSIVE_SEARCH flag.</span></span> 
    
<span data-ttu-id="7d0ed-136">STOP_SEARCH</span><span class="sxs-lookup"><span data-stu-id="7d0ed-136">STOP_SEARCH</span></span> 
  
> <span data-ttu-id="7d0ed-137">Поиск должна быть остановлена.</span><span class="sxs-lookup"><span data-stu-id="7d0ed-137">The search should be stopped.</span></span> <span data-ttu-id="7d0ed-138">Этот флаг не могут задаваться одновременно флаг RESTART_SEARCH.</span><span class="sxs-lookup"><span data-stu-id="7d0ed-138">This flag cannot be set at the same time as the RESTART_SEARCH flag.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7d0ed-139">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="7d0ed-139">Return value</span></span>

<span data-ttu-id="7d0ed-140">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="7d0ed-140">S_OK</span></span> 
  
> <span data-ttu-id="7d0ed-141">Условия поиска успешно установлены.</span><span class="sxs-lookup"><span data-stu-id="7d0ed-141">The search criteria was successfully set.</span></span>
    
<span data-ttu-id="7d0ed-142">MAPI_E_TOO_COMPLEX</span><span class="sxs-lookup"><span data-stu-id="7d0ed-142">MAPI_E_TOO_COMPLEX</span></span> 
  
> <span data-ttu-id="7d0ed-143">Поставщик услуг поддерживает заданным критериям поиска.</span><span class="sxs-lookup"><span data-stu-id="7d0ed-143">The service provider does not support the specified search criteria.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7d0ed-144">Замечания</span><span class="sxs-lookup"><span data-stu-id="7d0ed-144">Remarks</span></span>

<span data-ttu-id="7d0ed-145">Метод **IMAPIContainer::SetSearchCriteria** устанавливает условия поиска для контейнера, поддерживающего поиск, обычно в папку результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="7d0ed-145">The **IMAPIContainer::SetSearchCriteria** method establishes search criteria for a container that supports searches, typically a search-results folder.</span></span> <span data-ttu-id="7d0ed-146">Папка результатов поиска содержит ссылки на сообщения, которые соответствуют критериям поиска; Фактические сообщения по-прежнему хранятся в исходных местах.</span><span class="sxs-lookup"><span data-stu-id="7d0ed-146">A search-results folder contains links to the messages that meet the search criteria; the actual messages are still stored in their original locations.</span></span> <span data-ttu-id="7d0ed-147">Только уникальные данные, содержащиеся в папке результатов поиска — таблица его содержимого.</span><span class="sxs-lookup"><span data-stu-id="7d0ed-147">The only unique data that is contained in a search-results folder is its contents table.</span></span> <span data-ttu-id="7d0ed-148">В таблице содержимое папки результатов поиска имеет объединенное содержимое хранилища сообщений после применения ограничения поиска.</span><span class="sxs-lookup"><span data-stu-id="7d0ed-148">The contents table of a search-results folder has the merged contents of the message store after the search restriction has been applied.</span></span> 
  
<span data-ttu-id="7d0ed-149">Операция поиска работает только в этой таблице объединенные содержимого; Поиск в других папках результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="7d0ed-149">A search operation works only on this merged contents table; it does not search through other search-results folders.</span></span> <span data-ttu-id="7d0ed-150">Возвращает результаты поиска только сообщения, соответствующие критериям поиска; Иерархия папок не возвращаются.</span><span class="sxs-lookup"><span data-stu-id="7d0ed-150">The search results return only the messages that match the search criteria; the folder hierarchy is not returned.</span></span>
  
<span data-ttu-id="7d0ed-151">Управление возвращается клиенту после завершения поиска.</span><span class="sxs-lookup"><span data-stu-id="7d0ed-151">Control is returned to the client when the search has finished.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="7d0ed-152">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="7d0ed-152">Notes to implementers</span></span>

<span data-ttu-id="7d0ed-153">Контейнеры адресной книги устанавливать условия поиска с применением ограничений на их содержимое таблицы.</span><span class="sxs-lookup"><span data-stu-id="7d0ed-153">Address book containers establish search criteria by applying restrictions to their contents tables.</span></span> <span data-ttu-id="7d0ed-154">Дополнительные сведения о критерии поиска и адресной книги контейнеров см [Реализация расширенного поиска](implementing-advanced-searching.md).</span><span class="sxs-lookup"><span data-stu-id="7d0ed-154">For more information about search criteria and address book containers, see [Implementing Advanced Searching](implementing-advanced-searching.md).</span></span>
  
<span data-ttu-id="7d0ed-155">Следует поддержки open, копирование, перемещение и удаления сообщений в папках результатов поиска, а не к самой папке результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="7d0ed-155">You should support open, copy, move, and delete operations on the messages within search-results folders, not on the search-results folder itself.</span></span> <span data-ttu-id="7d0ed-156">Не разрешать сообщения, чтобы быть созданы в рамках или скопирован в папку результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="7d0ed-156">Do not allow messages to be created within or copied into a search-results folder.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="7d0ed-157">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="7d0ed-157">Notes to callers</span></span>

<span data-ttu-id="7d0ed-158">Чтобы найти получателей сообщения, задайте _lpRestriction_ для указания на ограничений вложенные объекты с член **ulSubObject** в структуре [SSubRestriction](ssubrestriction.md) , задайте значение **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="7d0ed-158">To search for message recipients, set  _lpRestriction_ to point to a subobject restriction with the **ulSubObject** member in the [SSubRestriction](ssubrestriction.md) structure set to **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)).</span></span> <span data-ttu-id="7d0ed-159">Поиск вложений, укажите элемент **ulSubObject** в **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="7d0ed-159">To search for attachments, set the **ulSubObject** member to **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)).</span></span> <span data-ttu-id="7d0ed-160">Укажите элемент **lpRes** для указания на ограничение свойство, которое описывает условия поиска для получателей или вложения.</span><span class="sxs-lookup"><span data-stu-id="7d0ed-160">Set the **lpRes** member to point to a property restriction that describes the search criteria for the recipients or attachments.</span></span> 
  
<span data-ttu-id="7d0ed-161">Например для поиска файлов вложений, которые имеют расширение .mss, задайте **ulSubObject** **PR_MESSAGE_ATTACHMENTS** и **lpRes** для свойства ограничение, которое соответствует **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md) ) с. mss.</span><span class="sxs-lookup"><span data-stu-id="7d0ed-161">For example, to look for file attachments that have the extension .mss, set **ulSubObject** to **PR_MESSAGE_ATTACHMENTS** and **lpRes** to a property restriction that matches **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) with .mss.</span></span>
  
<span data-ttu-id="7d0ed-162">Установка флага FOREGROUND_SEARCH с помощью параметра _ulSearchFlags_ может привести к снижению производительности системы.</span><span class="sxs-lookup"><span data-stu-id="7d0ed-162">Setting the FOREGROUND_SEARCH flag in the  _ulSearchFlags_ parameter could cause a decrease in system performance.</span></span> 
  
<span data-ttu-id="7d0ed-163">Чтобы изменить параметры поиска для поиска в уже начатую можно использовать **SetSearchCriteria** .</span><span class="sxs-lookup"><span data-stu-id="7d0ed-163">You can use **SetSearchCriteria** to change the search criteria of a search already in progress.</span></span> <span data-ttu-id="7d0ed-164">Можно указать новые ограничения, новые списки папок для поиска и новый приоритет поиска, такие как обновление поиска более высокий приоритет.</span><span class="sxs-lookup"><span data-stu-id="7d0ed-164">You can specify new restrictions, new lists of folders to search, and a new search priority, such as upgrading a search to a higher priority.</span></span> <span data-ttu-id="7d0ed-165">Изменения в приоритет поиска не существующий поиск для перезапуска, но можно другие изменения в условия поиска.</span><span class="sxs-lookup"><span data-stu-id="7d0ed-165">Changes in search priority do not cause an existing search to restart, but other changes to search criteria can.</span></span> 
  
<span data-ttu-id="7d0ed-166">После завершения работы с помощью папки результатов поиска, можно удалить папку или сообщите его остаются открытыми для дальнейшего использования.</span><span class="sxs-lookup"><span data-stu-id="7d0ed-166">When you are through using a search-results folder, you can either delete the folder or let it remain open for later use.</span></span> <span data-ttu-id="7d0ed-167">Если удалить папку результатов поиска, только ссылки сообщения будут удалены.</span><span class="sxs-lookup"><span data-stu-id="7d0ed-167">If you do delete the search-results folder, only message links are deleted.</span></span> <span data-ttu-id="7d0ed-168">Фактические сообщения остаются в родительских папок.</span><span class="sxs-lookup"><span data-stu-id="7d0ed-168">The actual messages remain in their parent folders.</span></span> 
  
<span data-ttu-id="7d0ed-169">Дополнительные сведения о папках результатов поиска можно [Папок поиска MAPI](mapi-search-folders.md).</span><span class="sxs-lookup"><span data-stu-id="7d0ed-169">For more information about search-results folders, see [MAPI Search Folders](mapi-search-folders.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="7d0ed-170">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="7d0ed-170">MFCMAPI reference</span></span>

<span data-ttu-id="7d0ed-171">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="7d0ed-171">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="7d0ed-172">**����**</span><span class="sxs-lookup"><span data-stu-id="7d0ed-172">**File**</span></span>|<span data-ttu-id="7d0ed-173">**�������**</span><span class="sxs-lookup"><span data-stu-id="7d0ed-173">**Function**</span></span>|<span data-ttu-id="7d0ed-174">**�����������**</span><span class="sxs-lookup"><span data-stu-id="7d0ed-174">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7d0ed-175">HierarchyTableDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="7d0ed-175">HierarchyTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="7d0ed-176">CHierarchyTableDlg::OnEditSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="7d0ed-176">CHierarchyTableDlg::OnEditSearchCriteria</span></span>  <br/> |<span data-ttu-id="7d0ed-177">Mfcmapi (en) использует метод **IMAPIContainer::SetSearchCriteria** для записи условия поиска для папки после измененный пользователя.</span><span class="sxs-lookup"><span data-stu-id="7d0ed-177">MFCMAPI uses the **IMAPIContainer::SetSearchCriteria** method to write search criteria for a folder after a user has edited it.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7d0ed-178">См. также</span><span class="sxs-lookup"><span data-stu-id="7d0ed-178">See also</span></span>



[<span data-ttu-id="7d0ed-179">IMAPIContainer::GetContentsTable</span><span class="sxs-lookup"><span data-stu-id="7d0ed-179">IMAPIContainer::GetContentsTable</span></span>](imapicontainer-getcontentstable.md)
  
[<span data-ttu-id="7d0ed-180">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="7d0ed-180">IMAPIContainer::OpenEntry</span></span>](imapicontainer-openentry.md)
  
[<span data-ttu-id="7d0ed-181">IMAPIFolder::CreateFolder</span><span class="sxs-lookup"><span data-stu-id="7d0ed-181">IMAPIFolder::CreateFolder</span></span>](imapifolder-createfolder.md)
  
[<span data-ttu-id="7d0ed-182">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="7d0ed-182">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
  
[<span data-ttu-id="7d0ed-183">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="7d0ed-183">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="7d0ed-184">SRestriction</span><span class="sxs-lookup"><span data-stu-id="7d0ed-184">SRestriction</span></span>](srestriction.md)
  
[<span data-ttu-id="7d0ed-185">SSubRestriction</span><span class="sxs-lookup"><span data-stu-id="7d0ed-185">SSubRestriction</span></span>](ssubrestriction.md)
  
[<span data-ttu-id="7d0ed-186">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="7d0ed-186">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


[<span data-ttu-id="7d0ed-187">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="7d0ed-187">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

