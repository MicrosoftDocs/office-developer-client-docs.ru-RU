---
title: IMAPIContainerGetSearchCriteria
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer.GetSearchCriteria
api_type:
- COM
ms.assetid: 41b6c162-9984-43a3-b38e-44f0afae67de
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7845238722ce81b84210b6f4fc33f9df0abacc07
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412025"
---
# <a name="imapicontainergetsearchcriteria"></a><span data-ttu-id="8a85d-103">IMAPIContainer::GetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="8a85d-103">IMAPIContainer::GetSearchCriteria</span></span>

  
  
<span data-ttu-id="8a85d-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8a85d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8a85d-105">Получает критерии поиска для контейнера.</span><span class="sxs-lookup"><span data-stu-id="8a85d-105">Obtains the search criteria for the container.</span></span>
  
```cpp
HRESULT GetSearchCriteria(
  ULONG ulFlags,
  LPSRestriction FAR * lppRestriction,
  LPENTRYLIST FAR * lppContainerList,
  ULONG FAR * lpulSearchState
);
```

## <a name="parameters"></a><span data-ttu-id="8a85d-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="8a85d-106">Parameters</span></span>

 <span data-ttu-id="8a85d-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8a85d-107">_ulFlags_</span></span>
  
> <span data-ttu-id="8a85d-108">[in] Битмашка флагов, контролируемая типом переданных строк.</span><span class="sxs-lookup"><span data-stu-id="8a85d-108">[in] A bitmask of flags that controls the type of the passed-in strings.</span></span> <span data-ttu-id="8a85d-109">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="8a85d-109">The following flag can be set:</span></span>
    
<span data-ttu-id="8a85d-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="8a85d-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="8a85d-111">Переданные строки находятся в формате Unicode.</span><span class="sxs-lookup"><span data-stu-id="8a85d-111">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="8a85d-112">Если флаг MAPI_UNICODE не установлен, строки находятся в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="8a85d-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="8a85d-113">_lppRestriction_</span><span class="sxs-lookup"><span data-stu-id="8a85d-113">_lppRestriction_</span></span>
  
> <span data-ttu-id="8a85d-114">[вышел] Указатель на указатель на [структуру SRestriction,](srestriction.md) определяемую критериями поиска.</span><span class="sxs-lookup"><span data-stu-id="8a85d-114">[out] A pointer to a pointer to an [SRestriction](srestriction.md) structure that defines the search criteria.</span></span> <span data-ttu-id="8a85d-115">Если клиентное приложение передает NULL в _параметре lppRestriction,_ **GetSearchCriteria** не возвращает **структуру SRestriction.**</span><span class="sxs-lookup"><span data-stu-id="8a85d-115">If a client application passes NULL in the  _lppRestriction_ parameter, **GetSearchCriteria** does not return an **SRestriction** structure.</span></span> 
    
 <span data-ttu-id="8a85d-116">_lppContainerList_</span><span class="sxs-lookup"><span data-stu-id="8a85d-116">_lppContainerList_</span></span>
  
> <span data-ttu-id="8a85d-117">[вышел] Указатель на указатель на массив идентификаторов записей, которые представляют контейнеры, которые будут включены в поиск.</span><span class="sxs-lookup"><span data-stu-id="8a85d-117">[out] A pointer to a pointer to an array of entry identifiers that represent containers to be included in the search.</span></span> <span data-ttu-id="8a85d-118">Если клиент передает NULL в  _параметре lppContainerList,_ **GetSearchCriteria** не возвращает массив идентификаторов записи.</span><span class="sxs-lookup"><span data-stu-id="8a85d-118">If a client passes NULL in the  _lppContainerList_ parameter, **GetSearchCriteria** does not return an array of entry identifiers.</span></span> 
    
 <span data-ttu-id="8a85d-119">_lpulSearchState_</span><span class="sxs-lookup"><span data-stu-id="8a85d-119">_lpulSearchState_</span></span>
  
> <span data-ttu-id="8a85d-120">[вышел] Указатель на битмаску флагов, используемых для указать текущее состояние поиска.</span><span class="sxs-lookup"><span data-stu-id="8a85d-120">[out] A pointer to a bitmask of flags used to indicate the current state of the search.</span></span> <span data-ttu-id="8a85d-121">Если клиент передает NULL в  _параметре lpulSearchState,_ **GetSearchCriteria** не возвращает флаги.</span><span class="sxs-lookup"><span data-stu-id="8a85d-121">If a client passes NULL in the  _lpulSearchState_ parameter, **GetSearchCriteria** returns no flags.</span></span> <span data-ttu-id="8a85d-122">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="8a85d-122">The following flags can be set:</span></span> 
    
<span data-ttu-id="8a85d-123">SEARCH_FOREGROUND</span><span class="sxs-lookup"><span data-stu-id="8a85d-123">SEARCH_FOREGROUND</span></span> 
  
> <span data-ttu-id="8a85d-124">Поиск должен работать с высоким приоритетом по сравнению с другими поисками.</span><span class="sxs-lookup"><span data-stu-id="8a85d-124">The search should run at high priority relative to other searches.</span></span> <span data-ttu-id="8a85d-125">Если этот флаг не установлен, поиск выполняется в обычном приоритете по сравнению с другими поисками.</span><span class="sxs-lookup"><span data-stu-id="8a85d-125">If this flag is not set, the search runs at normal priority relative to other searches.</span></span>
    
<span data-ttu-id="8a85d-126">SEARCH_REBUILD</span><span class="sxs-lookup"><span data-stu-id="8a85d-126">SEARCH_REBUILD</span></span> 
  
> <span data-ttu-id="8a85d-127">Поиск находится в режиме интенсивной работы ЦП, пытаясь найти сообщения, которые соответствуют критериям.</span><span class="sxs-lookup"><span data-stu-id="8a85d-127">The search is in the CPU-intensive mode of its operation, trying to locate messages that match the criteria.</span></span> <span data-ttu-id="8a85d-128">Если этот флаг не заданной, то интенсивная для ЦП часть операции поиска будет отсвечена.</span><span class="sxs-lookup"><span data-stu-id="8a85d-128">If this flag is not set, the CPU-intensive part of the search's operation is over.</span></span> <span data-ttu-id="8a85d-129">Этот флаг имеет значение только в том случае, если поиск активен (то есть если SEARCH_RUNNING заданной).</span><span class="sxs-lookup"><span data-stu-id="8a85d-129">This flag has meaning only if the search is active (that is, if the SEARCH_RUNNING flag is set).</span></span>
    
<span data-ttu-id="8a85d-130">SEARCH_RECURSIVE</span><span class="sxs-lookup"><span data-stu-id="8a85d-130">SEARCH_RECURSIVE</span></span> 
  
> <span data-ttu-id="8a85d-131">Поиск ищется в указанных контейнерах и всех их детских контейнерах для совпадающих записей.</span><span class="sxs-lookup"><span data-stu-id="8a85d-131">The search is looking in specified containers and all their child containers for matching entries.</span></span> <span data-ttu-id="8a85d-132">Если этот флаг не установлен, в поиске находятся только контейнеры, явно включенные в последний вызов метода [IMAPIContainer::SetSearchCriteria.](imapicontainer-setsearchcriteria.md)</span><span class="sxs-lookup"><span data-stu-id="8a85d-132">If this flag is not set, only the containers explicitly included in the last call to the [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method are being searched.</span></span> 
    
<span data-ttu-id="8a85d-133">SEARCH_RUNNING</span><span class="sxs-lookup"><span data-stu-id="8a85d-133">SEARCH_RUNNING</span></span> 
  
> <span data-ttu-id="8a85d-134">Поиск активен, а таблица содержимого контейнера обновляется с учетом изменений в хранилище сообщений или адресной книге.</span><span class="sxs-lookup"><span data-stu-id="8a85d-134">The search is active and the container's contents table is being updated to reflect changes in the message store or address book.</span></span> <span data-ttu-id="8a85d-135">Если этот флаг не установлен, поиск неактивный, а таблица содержимого статична.</span><span class="sxs-lookup"><span data-stu-id="8a85d-135">If this flag is not set, the search is inactive and the contents table is static.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8a85d-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8a85d-136">Return value</span></span>

<span data-ttu-id="8a85d-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="8a85d-137">S_OK</span></span> 
  
> <span data-ttu-id="8a85d-138">Критерии поиска были успешно получены.</span><span class="sxs-lookup"><span data-stu-id="8a85d-138">The search criteria was successfully obtained.</span></span>
    
<span data-ttu-id="8a85d-139">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="8a85d-139">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="8a85d-140">Либо был MAPI_UNICODE флаг, а реализация не поддерживает Юникод, либо MAPI_UNICODE не установлена, а реализация поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="8a85d-140">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="8a85d-141">MAPI_E_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="8a85d-141">MAPI_E_NOT_INITIALIZED</span></span> 
  
> <span data-ttu-id="8a85d-142">Для контейнера никогда не были установлены критерии поиска.</span><span class="sxs-lookup"><span data-stu-id="8a85d-142">Search criteria were never established for the container.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8a85d-143">Примечания</span><span class="sxs-lookup"><span data-stu-id="8a85d-143">Remarks</span></span>

<span data-ttu-id="8a85d-144">Метод **IMAPIContainer::GetSearchCriteria** получает критерии поиска для контейнера, поддерживающем поиск, как правило, папки результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="8a85d-144">The **IMAPIContainer::GetSearchCriteria** method obtains the search criteria for a container that supports searches, typically a search-results folder.</span></span> <span data-ttu-id="8a85d-145">Вы создаете критерии поиска, вызывая метод **IMAPIContainer::SetSearchCriteria.**</span><span class="sxs-lookup"><span data-stu-id="8a85d-145">You create search criteria by calling a container's **IMAPIContainer::SetSearchCriteria** method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="8a85d-146">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="8a85d-146">Notes to implementers</span></span>

<span data-ttu-id="8a85d-147">Контейнеры адресных книг могут нуждаться в поддержке **GetSearchCriteria** только в том случае, если они предоставляют расширенные возможности поиска, связанные с **свойством PR_SEARCH** [(PidTagSearch).](pidtagsearch-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="8a85d-147">Address book containers may need to support **GetSearchCriteria** only if they provide the advanced search capabilities associated with the **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) property.</span></span> <span data-ttu-id="8a85d-148">Дополнительные сведения о том, как реализовать функцию расширенный поиск для контейнеров адресных книг, см. в книге [Implementing Advanced Search.](implementing-advanced-searching.md)</span><span class="sxs-lookup"><span data-stu-id="8a85d-148">For more information about how to implement the advanced search feature for address book containers, see [Implementing Advanced Searching](implementing-advanced-searching.md).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="8a85d-149">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="8a85d-149">Notes to callers</span></span>

<span data-ttu-id="8a85d-150">Когда вы закончите работу со структурами данных, на которые указывают параметры  _lppRestriction_ и  _lppContainerList,_ позвоните [ПО MAPIFreeBuffer](mapifreebuffer.md) один раз для выпуска каждой структуры.</span><span class="sxs-lookup"><span data-stu-id="8a85d-150">When you are finished with the data structures pointed to by the  _lppRestriction_ and  _lppContainerList_ parameters, call [MAPIFreeBuffer](mapifreebuffer.md) once for each structure to be released.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="8a85d-151">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="8a85d-151">MFCMAPI reference</span></span>

<span data-ttu-id="8a85d-152">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="8a85d-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="8a85d-153">**Файл**</span><span class="sxs-lookup"><span data-stu-id="8a85d-153">**File**</span></span>|<span data-ttu-id="8a85d-154">**Функция**</span><span class="sxs-lookup"><span data-stu-id="8a85d-154">**Function**</span></span>|<span data-ttu-id="8a85d-155">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="8a85d-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8a85d-156">HierarchyTableDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="8a85d-156">HierarchyTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="8a85d-157">CHierarchyTableDlg::OnEditSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="8a85d-157">CHierarchyTableDlg::OnEditSearchCriteria</span></span>  <br/> |<span data-ttu-id="8a85d-158">MFCMAPI использует **метод IMAPIContainer::GetSearchCriteria** для получения критериев поиска в папке для отображения.</span><span class="sxs-lookup"><span data-stu-id="8a85d-158">MFCMAPI uses the **IMAPIContainer::GetSearchCriteria** method to obtain search criteria from a folder to display.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8a85d-159">См. также</span><span class="sxs-lookup"><span data-stu-id="8a85d-159">See also</span></span>



[<span data-ttu-id="8a85d-160">IMAPIContainer::SetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="8a85d-160">IMAPIContainer::SetSearchCriteria</span></span>](imapicontainer-setsearchcriteria.md)
  
[<span data-ttu-id="8a85d-161">IMAPIFolder::CreateFolder</span><span class="sxs-lookup"><span data-stu-id="8a85d-161">IMAPIFolder::CreateFolder</span></span>](imapifolder-createfolder.md)
  
[<span data-ttu-id="8a85d-162">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="8a85d-162">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="8a85d-163">Каноническое свойство PidTagSearch</span><span class="sxs-lookup"><span data-stu-id="8a85d-163">PidTagSearch Canonical Property</span></span>](pidtagsearch-canonical-property.md)
  
[<span data-ttu-id="8a85d-164">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="8a85d-164">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


[<span data-ttu-id="8a85d-165">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="8a85d-165">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

