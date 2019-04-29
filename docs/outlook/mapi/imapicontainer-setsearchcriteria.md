---
title: Имапиконтаинерсетсеарчкритериа
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
# <a name="imapicontainersetsearchcriteria"></a><span data-ttu-id="f05c9-103">IMAPIContainer::SetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="f05c9-103">IMAPIContainer::SetSearchCriteria</span></span>

  
  
<span data-ttu-id="f05c9-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f05c9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f05c9-105">Устанавливает критерии поиска для контейнера.</span><span class="sxs-lookup"><span data-stu-id="f05c9-105">Establishes search criteria for the container.</span></span>
  
```cpp
HRESULT SetSearchCriteria(
  LPSRestriction lpRestriction,
  LPENTRYLIST lpContainerList,
  ULONG ulSearchFlags
);
```

## <a name="parameters"></a><span data-ttu-id="f05c9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f05c9-106">Parameters</span></span>

 <span data-ttu-id="f05c9-107">_Лпрестриктион_</span><span class="sxs-lookup"><span data-stu-id="f05c9-107">_lpRestriction_</span></span>
  
> <span data-ttu-id="f05c9-108">возврата Указатель на структуру [срестриктион](srestriction.md) , которая определяет критерии поиска.</span><span class="sxs-lookup"><span data-stu-id="f05c9-108">[in] A pointer to an [SRestriction](srestriction.md) structure that defines the search criteria.</span></span> <span data-ttu-id="f05c9-109">Если в параметре _лпрестриктион_ переДАЕТСЯ значение null, то условия поиска, использовавшиеся последними для этого контейнера, повторно используются.</span><span class="sxs-lookup"><span data-stu-id="f05c9-109">If NULL is passed in the  _lpRestriction_ parameter, the search criteria that were used most recently for this container are used again.</span></span> <span data-ttu-id="f05c9-110">ЗНАЧЕНИЕ NULL не должно передаваться в _лпрестриктион_ для первого поиска в контейнере.</span><span class="sxs-lookup"><span data-stu-id="f05c9-110">NULL should not be passed in  _lpRestriction_ for the first search in a container.</span></span> 
    
 <span data-ttu-id="f05c9-111">_Лпконтаинерлист_</span><span class="sxs-lookup"><span data-stu-id="f05c9-111">_lpContainerList_</span></span>
  
> <span data-ttu-id="f05c9-112">возврата Указатель на массив идентификаторов записей, представляющих контейнеры, которые необходимо включить в поиск.</span><span class="sxs-lookup"><span data-stu-id="f05c9-112">[in] A pointer to an array of entry identifiers that represent containers to be included in the search.</span></span> <span data-ttu-id="f05c9-113">Если клиент передает значение NULL в параметр _лпконтаинерлист_ , для нового поиска используются идентификаторы записей, использовавшиеся последними для поиска в этом контейнере.</span><span class="sxs-lookup"><span data-stu-id="f05c9-113">If a client passes NULL in the  _lpContainerList_ parameter, the entry identifiers used most recently to search this container are used for the new search.</span></span> <span data-ttu-id="f05c9-114">Клиент не должен передавать значение NULL в _лпконтаинерлист_ для первого поиска в контейнере.</span><span class="sxs-lookup"><span data-stu-id="f05c9-114">A client should not pass NULL in  _lpContainerList_ for the first search in a container.</span></span> 
    
 <span data-ttu-id="f05c9-115">_Улсеарчфлагс_</span><span class="sxs-lookup"><span data-stu-id="f05c9-115">_ulSearchFlags_</span></span>
  
> <span data-ttu-id="f05c9-116">возврата Битовая маска флагов, которые управляют выполнением поиска.</span><span class="sxs-lookup"><span data-stu-id="f05c9-116">[in] A bitmask of flags that control how the search is performed.</span></span> <span data-ttu-id="f05c9-117">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="f05c9-117">The following flags can be set:</span></span>
    
<span data-ttu-id="f05c9-118">БАККГРАУНД_СЕАРЧ</span><span class="sxs-lookup"><span data-stu-id="f05c9-118">BACKGROUND_SEARCH</span></span> 
  
> <span data-ttu-id="f05c9-119">Поиск должен выполняться с обычным приоритетом относительно других поисков.</span><span class="sxs-lookup"><span data-stu-id="f05c9-119">The search should run at normal priority relative to other searches.</span></span> <span data-ttu-id="f05c9-120">Этот флаг не может быть установлен одновременно с флагом ФОРЕГРАУНД_СЕАРЧ.</span><span class="sxs-lookup"><span data-stu-id="f05c9-120">This flag cannot be set at the same time as the FOREGROUND_SEARCH flag.</span></span>
    
<span data-ttu-id="f05c9-121">ФОРЕГРАУНД_СЕАРЧ</span><span class="sxs-lookup"><span data-stu-id="f05c9-121">FOREGROUND_SEARCH</span></span> 
  
> <span data-ttu-id="f05c9-122">Поиск должен выполняться с высоким приоритетом, связанным с другими поисковыми операциями.</span><span class="sxs-lookup"><span data-stu-id="f05c9-122">The search should run at high priority relative to other searches.</span></span> <span data-ttu-id="f05c9-123">Этот флаг не может быть установлен одновременно с флагом БАККГРАУНД_СЕАРЧ.</span><span class="sxs-lookup"><span data-stu-id="f05c9-123">This flag cannot be set at the same time as the BACKGROUND_SEARCH flag.</span></span>
    
<span data-ttu-id="f05c9-124">НОН_КОНТЕНТ_ИНДЕКСЕД_СЕАРЧ</span><span class="sxs-lookup"><span data-stu-id="f05c9-124">NON_CONTENT_INDEXED_SEARCH</span></span>
  
> <span data-ttu-id="f05c9-125">Для поиска совпадений не следует использовать индексирование контента.</span><span class="sxs-lookup"><span data-stu-id="f05c9-125">The search should not use content indexing to find matching entries.</span></span> <span data-ttu-id="f05c9-126">Этот флаг действителен только для хранилищ Exchange.</span><span class="sxs-lookup"><span data-stu-id="f05c9-126">This flag is only valid for Exchange stores.</span></span>
    
<span data-ttu-id="f05c9-127">РЕКУРСИВЕ_СЕАРЧ</span><span class="sxs-lookup"><span data-stu-id="f05c9-127">RECURSIVE_SEARCH</span></span> 
  
> <span data-ttu-id="f05c9-128">Поиск должен включать в себя контейнеры, указанные в параметре _лпконтаинерлист_ , и все дочерние контейнеры.</span><span class="sxs-lookup"><span data-stu-id="f05c9-128">The search should include the containers specified in the  _lpContainerList_ parameter and all their child containers.</span></span> <span data-ttu-id="f05c9-129">Этот флаг не может быть установлен одновременно с флагом ШАЛЛОВ_СЕАРЧ.</span><span class="sxs-lookup"><span data-stu-id="f05c9-129">This flag cannot be set at the same time as the SHALLOW_SEARCH flag.</span></span> 
    
<span data-ttu-id="f05c9-130">РЕСТАРТ_СЕАРЧ</span><span class="sxs-lookup"><span data-stu-id="f05c9-130">RESTART_SEARCH</span></span> 
  
> <span data-ttu-id="f05c9-131">Поиск должен быть инициирован при первом вызове **сетсеарчкритериа**или перезапуске, если поиск неактивен.</span><span class="sxs-lookup"><span data-stu-id="f05c9-131">The search should be initiated if this is the first call to **SetSearchCriteria**, or restarted if the search is inactive.</span></span> <span data-ttu-id="f05c9-132">Этот флаг не может быть установлен одновременно с флагом СТОП_СЕАРЧ.</span><span class="sxs-lookup"><span data-stu-id="f05c9-132">This flag cannot be set at the same time as the STOP_SEARCH flag.</span></span>
    
<span data-ttu-id="f05c9-133">ШАЛЛОВ_СЕАРЧ</span><span class="sxs-lookup"><span data-stu-id="f05c9-133">SHALLOW_SEARCH</span></span> 
  
> <span data-ttu-id="f05c9-134">Поиск должен искать только в контейнерах, указанных в параметре _лпконтаинерлист_ для совпадений записей.</span><span class="sxs-lookup"><span data-stu-id="f05c9-134">The search should look only in the containers specified in the  _lpContainerList_ parameter for matching entries.</span></span> <span data-ttu-id="f05c9-135">Этот флаг не может быть установлен одновременно с флагом РЕКУРСИВЕ_СЕАРЧ.</span><span class="sxs-lookup"><span data-stu-id="f05c9-135">This flag cannot be set at the same time as the RECURSIVE_SEARCH flag.</span></span> 
    
<span data-ttu-id="f05c9-136">СТОП_СЕАРЧ</span><span class="sxs-lookup"><span data-stu-id="f05c9-136">STOP_SEARCH</span></span> 
  
> <span data-ttu-id="f05c9-137">Поиск должен быть остановлен.</span><span class="sxs-lookup"><span data-stu-id="f05c9-137">The search should be stopped.</span></span> <span data-ttu-id="f05c9-138">Этот флаг не может быть установлен одновременно с флагом РЕСТАРТ_СЕАРЧ.</span><span class="sxs-lookup"><span data-stu-id="f05c9-138">This flag cannot be set at the same time as the RESTART_SEARCH flag.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f05c9-139">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f05c9-139">Return value</span></span>

<span data-ttu-id="f05c9-140">S_OK</span><span class="sxs-lookup"><span data-stu-id="f05c9-140">S_OK</span></span> 
  
> <span data-ttu-id="f05c9-141">Условия поиска успешно заданы.</span><span class="sxs-lookup"><span data-stu-id="f05c9-141">The search criteria was successfully set.</span></span>
    
<span data-ttu-id="f05c9-142">МАПИ_Е_ТУ_КОМПЛЕКС</span><span class="sxs-lookup"><span data-stu-id="f05c9-142">MAPI_E_TOO_COMPLEX</span></span> 
  
> <span data-ttu-id="f05c9-143">Поставщик услуг не поддерживает указанные критерии поиска.</span><span class="sxs-lookup"><span data-stu-id="f05c9-143">The service provider does not support the specified search criteria.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f05c9-144">Примечания</span><span class="sxs-lookup"><span data-stu-id="f05c9-144">Remarks</span></span>

<span data-ttu-id="f05c9-145">Метод **IMAPIContainer:: сетсеарчкритериа** устанавливает критерии поиска для контейнера, поддерживающего Поиск, как правило, папка результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="f05c9-145">The **IMAPIContainer::SetSearchCriteria** method establishes search criteria for a container that supports searches, typically a search-results folder.</span></span> <span data-ttu-id="f05c9-146">В папке результатов поиска содержатся ссылки на сообщения, соответствующие условиям поиска; фактические сообщения по-прежнему хранятся в исходных расположениях.</span><span class="sxs-lookup"><span data-stu-id="f05c9-146">A search-results folder contains links to the messages that meet the search criteria; the actual messages are still stored in their original locations.</span></span> <span data-ttu-id="f05c9-147">Единственными уникальными данными, которые хранятся в папке результатов поиска, является его таблица содержимого.</span><span class="sxs-lookup"><span data-stu-id="f05c9-147">The only unique data that is contained in a search-results folder is its contents table.</span></span> <span data-ttu-id="f05c9-148">В таблице содержимого папки результатов поиска имеется объединенное содержимое хранилища сообщений после применения ограничения поиска.</span><span class="sxs-lookup"><span data-stu-id="f05c9-148">The contents table of a search-results folder has the merged contents of the message store after the search restriction has been applied.</span></span> 
  
<span data-ttu-id="f05c9-149">Операция поиска работает только в этой таблице Объединенных оглавлений; Он не выполняет поиск в других папках результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="f05c9-149">A search operation works only on this merged contents table; it does not search through other search-results folders.</span></span> <span data-ttu-id="f05c9-150">Результаты поиска возвращают только те сообщения, которые отвечают условиям поиска; Иерархия папок не возвращается.</span><span class="sxs-lookup"><span data-stu-id="f05c9-150">The search results return only the messages that match the search criteria; the folder hierarchy is not returned.</span></span>
  
<span data-ttu-id="f05c9-151">Управление возвращается клиенту по завершении поиска.</span><span class="sxs-lookup"><span data-stu-id="f05c9-151">Control is returned to the client when the search has finished.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="f05c9-152">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="f05c9-152">Notes to implementers</span></span>

<span data-ttu-id="f05c9-153">Контейнеры адресных книг установите условия поиска, применяя ограничения к их таблицам содержимого.</span><span class="sxs-lookup"><span data-stu-id="f05c9-153">Address book containers establish search criteria by applying restrictions to their contents tables.</span></span> <span data-ttu-id="f05c9-154">Для получения дополнительных сведений о критериях поиска и контейнерах адресной книги, ознакомьтесь со статьей [Реализация расширенНого поиска](implementing-advanced-searching.md).</span><span class="sxs-lookup"><span data-stu-id="f05c9-154">For more information about search criteria and address book containers, see [Implementing Advanced Searching](implementing-advanced-searching.md).</span></span>
  
<span data-ttu-id="f05c9-155">Вы должны поддерживать операции по открытию, копированию, перемещению и удалению сообщений в папках результатов поиска, а не в самой папке результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="f05c9-155">You should support open, copy, move, and delete operations on the messages within search-results folders, not on the search-results folder itself.</span></span> <span data-ttu-id="f05c9-156">Не разрешать создание сообщений в папке результатов поиска или копирование в нее.</span><span class="sxs-lookup"><span data-stu-id="f05c9-156">Do not allow messages to be created within or copied into a search-results folder.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="f05c9-157">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="f05c9-157">Notes to callers</span></span>

<span data-ttu-id="f05c9-158">Чтобы найти получателей сообщения, задайте для параметра _лпрестриктион_ значение, которое указывает на ограничение на вложенный объект, с элементом **Улсубобжект** в структуре [ссубрестриктион](ssubrestriction.md) , равным **пр_мессаже_реЦипиентс** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="f05c9-158">To search for message recipients, set  _lpRestriction_ to point to a subobject restriction with the **ulSubObject** member in the [SSubRestriction](ssubrestriction.md) structure set to **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)).</span></span> <span data-ttu-id="f05c9-159">Чтобы выполнить поиск вложений, установите для члена **улсубобжект** значение **пр_мессаже_аттачментс** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="f05c9-159">To search for attachments, set the **ulSubObject** member to **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)).</span></span> <span data-ttu-id="f05c9-160">ПриСвойте элементу **лпрес** ограничение свойства, которое описывает критерии поиска для получателей или вложений.</span><span class="sxs-lookup"><span data-stu-id="f05c9-160">Set the **lpRes** member to point to a property restriction that describes the search criteria for the recipients or attachments.</span></span> 
  
<span data-ttu-id="f05c9-161">Например, чтобы найти вложенные файлы с расширением MSS, задайте для параметра **улсубобжект** значение **пр_мессаже_аттачментс** и **лпрес** в ограничении свойств, которое соответствует **пр_аттач_екстенсион** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md) ) с. MSS.</span><span class="sxs-lookup"><span data-stu-id="f05c9-161">For example, to look for file attachments that have the extension .mss, set **ulSubObject** to **PR_MESSAGE_ATTACHMENTS** and **lpRes** to a property restriction that matches **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) with .mss.</span></span>
  
<span data-ttu-id="f05c9-162">Установка флага ФОРЕГРАУНД_СЕАРЧ в параметре _улсеарчфлагс_ может привести к снижению производительности системы.</span><span class="sxs-lookup"><span data-stu-id="f05c9-162">Setting the FOREGROUND_SEARCH flag in the  _ulSearchFlags_ parameter could cause a decrease in system performance.</span></span> 
  
<span data-ttu-id="f05c9-163">Вы можете использовать **сетсеарчкритериа** , чтобы изменить условия поиска, выполняемые при поиске.</span><span class="sxs-lookup"><span data-stu-id="f05c9-163">You can use **SetSearchCriteria** to change the search criteria of a search already in progress.</span></span> <span data-ttu-id="f05c9-164">Вы можете указать новые ограничения, новые списки папок для поиска и новый приоритет поиска, например обновление поиска с более высоким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="f05c9-164">You can specify new restrictions, new lists of folders to search, and a new search priority, such as upgrading a search to a higher priority.</span></span> <span data-ttu-id="f05c9-165">Изменения, внесенные в приоритет поиска, не приводят к перезапуску существующего поиска, но другие изменения в условиях поиска могут.</span><span class="sxs-lookup"><span data-stu-id="f05c9-165">Changes in search priority do not cause an existing search to restart, but other changes to search criteria can.</span></span> 
  
<span data-ttu-id="f05c9-166">При работе с папкой результатов поиска вы можете либо удалить эту папку, либо оставить ее открытой для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="f05c9-166">When you are through using a search-results folder, you can either delete the folder or let it remain open for later use.</span></span> <span data-ttu-id="f05c9-167">Если вы удаляете папку результатов поиска, удаляются только ссылки на сообщения.</span><span class="sxs-lookup"><span data-stu-id="f05c9-167">If you do delete the search-results folder, only message links are deleted.</span></span> <span data-ttu-id="f05c9-168">Фактические сообщения хранятся в их родительских папках.</span><span class="sxs-lookup"><span data-stu-id="f05c9-168">The actual messages remain in their parent folders.</span></span> 
  
<span data-ttu-id="f05c9-169">Для получения дополнительных сведений о папках результатов поиска в разделе [MAPI Search Folders](mapi-search-folders.md).</span><span class="sxs-lookup"><span data-stu-id="f05c9-169">For more information about search-results folders, see [MAPI Search Folders](mapi-search-folders.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f05c9-170">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="f05c9-170">MFCMAPI reference</span></span>

<span data-ttu-id="f05c9-171">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="f05c9-171">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f05c9-172">**Файл**</span><span class="sxs-lookup"><span data-stu-id="f05c9-172">**File**</span></span>|<span data-ttu-id="f05c9-173">**Функция**</span><span class="sxs-lookup"><span data-stu-id="f05c9-173">**Function**</span></span>|<span data-ttu-id="f05c9-174">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="f05c9-174">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f05c9-175">Хиерарчитабледлг. cpp</span><span class="sxs-lookup"><span data-stu-id="f05c9-175">HierarchyTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="f05c9-176">Чиерарчитабледлг:: Онедитсеарчкритериа</span><span class="sxs-lookup"><span data-stu-id="f05c9-176">CHierarchyTableDlg::OnEditSearchCriteria</span></span>  <br/> |<span data-ttu-id="f05c9-177">MFCMAPI использует метод **IMAPIContainer:: сетсеарчкритериа** для записи условий поиска для папки после того, как пользователь редактировал ее.</span><span class="sxs-lookup"><span data-stu-id="f05c9-177">MFCMAPI uses the **IMAPIContainer::SetSearchCriteria** method to write search criteria for a folder after a user has edited it.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f05c9-178">См. также</span><span class="sxs-lookup"><span data-stu-id="f05c9-178">See also</span></span>



[<span data-ttu-id="f05c9-179">IMAPIContainer::GetContentsTable</span><span class="sxs-lookup"><span data-stu-id="f05c9-179">IMAPIContainer::GetContentsTable</span></span>](imapicontainer-getcontentstable.md)
  
[<span data-ttu-id="f05c9-180">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="f05c9-180">IMAPIContainer::OpenEntry</span></span>](imapicontainer-openentry.md)
  
[<span data-ttu-id="f05c9-181">IMAPIFolder::CreateFolder</span><span class="sxs-lookup"><span data-stu-id="f05c9-181">IMAPIFolder::CreateFolder</span></span>](imapifolder-createfolder.md)
  
[<span data-ttu-id="f05c9-182">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="f05c9-182">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
  
[<span data-ttu-id="f05c9-183">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="f05c9-183">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="f05c9-184">SRestriction</span><span class="sxs-lookup"><span data-stu-id="f05c9-184">SRestriction</span></span>](srestriction.md)
  
[<span data-ttu-id="f05c9-185">SSubRestriction</span><span class="sxs-lookup"><span data-stu-id="f05c9-185">SSubRestriction</span></span>](ssubrestriction.md)
  
[<span data-ttu-id="f05c9-186">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="f05c9-186">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


[<span data-ttu-id="f05c9-187">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="f05c9-187">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

