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
# <a name="imapicontainergetsearchcriteria"></a><span data-ttu-id="1eabe-103">IMAPIContainer::GetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="1eabe-103">IMAPIContainer::GetSearchCriteria</span></span>

  
  
<span data-ttu-id="1eabe-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1eabe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1eabe-105">Получает условия поиска для контейнера.</span><span class="sxs-lookup"><span data-stu-id="1eabe-105">Obtains the search criteria for the container.</span></span>
  
```cpp
HRESULT GetSearchCriteria(
  ULONG ulFlags,
  LPSRestriction FAR * lppRestriction,
  LPENTRYLIST FAR * lppContainerList,
  ULONG FAR * lpulSearchState
);
```

## <a name="parameters"></a><span data-ttu-id="1eabe-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1eabe-106">Parameters</span></span>

 <span data-ttu-id="1eabe-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1eabe-107">_ulFlags_</span></span>
  
> <span data-ttu-id="1eabe-108">[in] Битоваяmas флагов, которая управляет типом переданных строк.</span><span class="sxs-lookup"><span data-stu-id="1eabe-108">[in] A bitmask of flags that controls the type of the passed-in strings.</span></span> <span data-ttu-id="1eabe-109">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="1eabe-109">The following flag can be set:</span></span>
    
<span data-ttu-id="1eabe-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1eabe-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="1eabe-111">Переданные строки имеют формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="1eabe-111">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="1eabe-112">Если флаг MAPI_UNICODE не установлен, строки будут в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="1eabe-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="1eabe-113">_lppRestriction_</span><span class="sxs-lookup"><span data-stu-id="1eabe-113">_lppRestriction_</span></span>
  
> <span data-ttu-id="1eabe-114">[out] Указатель на указатель на [структуру SRestriction,](srestriction.md) которая определяет условия поиска.</span><span class="sxs-lookup"><span data-stu-id="1eabe-114">[out] A pointer to a pointer to an [SRestriction](srestriction.md) structure that defines the search criteria.</span></span> <span data-ttu-id="1eabe-115">Если клиентские приложения проходят NULL в _параметре lppRestriction,_ **GetSearchCriteria** не возвращает **структуру SRestriction.**</span><span class="sxs-lookup"><span data-stu-id="1eabe-115">If a client application passes NULL in the  _lppRestriction_ parameter, **GetSearchCriteria** does not return an **SRestriction** structure.</span></span> 
    
 <span data-ttu-id="1eabe-116">_lppContainerList_</span><span class="sxs-lookup"><span data-stu-id="1eabe-116">_lppContainerList_</span></span>
  
> <span data-ttu-id="1eabe-117">[out] Указатель на указатель на массив идентификаторов записей, которые представляют контейнеры, которые необходимо включить в поиск.</span><span class="sxs-lookup"><span data-stu-id="1eabe-117">[out] A pointer to a pointer to an array of entry identifiers that represent containers to be included in the search.</span></span> <span data-ttu-id="1eabe-118">Если клиент передает NULL в  _параметре lppContainerList,_ **GetSearchCriteria** не возвращает массив идентификаторов записей.</span><span class="sxs-lookup"><span data-stu-id="1eabe-118">If a client passes NULL in the  _lppContainerList_ parameter, **GetSearchCriteria** does not return an array of entry identifiers.</span></span> 
    
 <span data-ttu-id="1eabe-119">_lpulSearchState_</span><span class="sxs-lookup"><span data-stu-id="1eabe-119">_lpulSearchState_</span></span>
  
> <span data-ttu-id="1eabe-120">[out] Указатель на битовуюметку флагов, которая указывает текущее состояние поиска.</span><span class="sxs-lookup"><span data-stu-id="1eabe-120">[out] A pointer to a bitmask of flags used to indicate the current state of the search.</span></span> <span data-ttu-id="1eabe-121">Если клиент передает NULL в  _параметре lpulSearchState,_ **GetSearchCriteria** не возвращает флаги.</span><span class="sxs-lookup"><span data-stu-id="1eabe-121">If a client passes NULL in the  _lpulSearchState_ parameter, **GetSearchCriteria** returns no flags.</span></span> <span data-ttu-id="1eabe-122">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="1eabe-122">The following flags can be set:</span></span> 
    
<span data-ttu-id="1eabe-123">SEARCH_FOREGROUND</span><span class="sxs-lookup"><span data-stu-id="1eabe-123">SEARCH_FOREGROUND</span></span> 
  
> <span data-ttu-id="1eabe-124">Поиск должен работать с высоким приоритетом относительно других поисковых запросов.</span><span class="sxs-lookup"><span data-stu-id="1eabe-124">The search should run at high priority relative to other searches.</span></span> <span data-ttu-id="1eabe-125">Если этот флаг не установлен, поиск выполняется с обычным приоритетом относительно других поисковых запросов.</span><span class="sxs-lookup"><span data-stu-id="1eabe-125">If this flag is not set, the search runs at normal priority relative to other searches.</span></span>
    
<span data-ttu-id="1eabe-126">SEARCH_REBUILD</span><span class="sxs-lookup"><span data-stu-id="1eabe-126">SEARCH_REBUILD</span></span> 
  
> <span data-ttu-id="1eabe-127">Поиск находится в режиме интенсивной работы ЦП и пытается найти сообщения, которые соответствуют условиям.</span><span class="sxs-lookup"><span data-stu-id="1eabe-127">The search is in the CPU-intensive mode of its operation, trying to locate messages that match the criteria.</span></span> <span data-ttu-id="1eabe-128">Если этот флаг не установлен, интенсивное ЦП часть операции поиска будет установлена.</span><span class="sxs-lookup"><span data-stu-id="1eabe-128">If this flag is not set, the CPU-intensive part of the search's operation is over.</span></span> <span data-ttu-id="1eabe-129">Этот флаг имеет значение, только если поиск активен (то есть если SEARCH_RUNNING установлен).</span><span class="sxs-lookup"><span data-stu-id="1eabe-129">This flag has meaning only if the search is active (that is, if the SEARCH_RUNNING flag is set).</span></span>
    
<span data-ttu-id="1eabe-130">SEARCH_RECURSIVE</span><span class="sxs-lookup"><span data-stu-id="1eabe-130">SEARCH_RECURSIVE</span></span> 
  
> <span data-ttu-id="1eabe-131">Поиск ищет в указанных контейнерах и всех их потомков контейнерах для поиска совпадающих записей.</span><span class="sxs-lookup"><span data-stu-id="1eabe-131">The search is looking in specified containers and all their child containers for matching entries.</span></span> <span data-ttu-id="1eabe-132">Если этот флаг не установлен, поиск ведется только в контейнерах, явно включенных в последний вызов метода [IMAPIContainer::SetSearchCriteria.](imapicontainer-setsearchcriteria.md)</span><span class="sxs-lookup"><span data-stu-id="1eabe-132">If this flag is not set, only the containers explicitly included in the last call to the [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method are being searched.</span></span> 
    
<span data-ttu-id="1eabe-133">SEARCH_RUNNING</span><span class="sxs-lookup"><span data-stu-id="1eabe-133">SEARCH_RUNNING</span></span> 
  
> <span data-ttu-id="1eabe-134">Поиск активен, и таблица содержимого контейнера обновляется с учетом изменений в хранилище сообщений или адресной книге.</span><span class="sxs-lookup"><span data-stu-id="1eabe-134">The search is active and the container's contents table is being updated to reflect changes in the message store or address book.</span></span> <span data-ttu-id="1eabe-135">Если этот флаг не установлен, поиск неактивный, а таблица содержимого является статической.</span><span class="sxs-lookup"><span data-stu-id="1eabe-135">If this flag is not set, the search is inactive and the contents table is static.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1eabe-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1eabe-136">Return value</span></span>

<span data-ttu-id="1eabe-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="1eabe-137">S_OK</span></span> 
  
> <span data-ttu-id="1eabe-138">Критерии поиска успешно получены.</span><span class="sxs-lookup"><span data-stu-id="1eabe-138">The search criteria was successfully obtained.</span></span>
    
<span data-ttu-id="1eabe-139">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="1eabe-139">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="1eabe-140">Либо флаг MAPI_UNICODE установлен, а реализация не поддерживает Юникод, либо MAPI_UNICODE не установлен, а реализация поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="1eabe-140">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="1eabe-141">MAPI_E_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="1eabe-141">MAPI_E_NOT_INITIALIZED</span></span> 
  
> <span data-ttu-id="1eabe-142">Условия поиска для контейнера не были установлены.</span><span class="sxs-lookup"><span data-stu-id="1eabe-142">Search criteria were never established for the container.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1eabe-143">Примечания</span><span class="sxs-lookup"><span data-stu-id="1eabe-143">Remarks</span></span>

<span data-ttu-id="1eabe-144">Метод **IMAPIContainer::GetSearchCriteria** получает условия поиска для контейнера, который поддерживает поиск, обычно папку результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="1eabe-144">The **IMAPIContainer::GetSearchCriteria** method obtains the search criteria for a container that supports searches, typically a search-results folder.</span></span> <span data-ttu-id="1eabe-145">Критерии поиска создаются путем вызова метода **IMAPIContainer::SetSearchCriteria контейнера.**</span><span class="sxs-lookup"><span data-stu-id="1eabe-145">You create search criteria by calling a container's **IMAPIContainer::SetSearchCriteria** method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="1eabe-146">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="1eabe-146">Notes to implementers</span></span>

<span data-ttu-id="1eabe-147">Контейнерам адресной книги может потребоваться поддержка **GetSearchCriteria,** только если они предоставляют расширенные возможности поиска, связанные со свойством **PR_SEARCH** ([PidTagSearch).](pidtagsearch-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="1eabe-147">Address book containers may need to support **GetSearchCriteria** only if they provide the advanced search capabilities associated with the **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) property.</span></span> <span data-ttu-id="1eabe-148">Дополнительные сведения о реализации функции расширенный поиск для контейнеров адресной книги см. в [реализации функции "Расширенный поиск".](implementing-advanced-searching.md)</span><span class="sxs-lookup"><span data-stu-id="1eabe-148">For more information about how to implement the advanced search feature for address book containers, see [Implementing Advanced Searching](implementing-advanced-searching.md).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="1eabe-149">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="1eabe-149">Notes to callers</span></span>

<span data-ttu-id="1eabe-150">Завершив работу со структурами данных, на которые указывают параметры  _lppRestriction_ и  _lppContainerList,_ вызовите [MAPIFreeBuffer](mapifreebuffer.md) один раз, чтобы освободить каждую структуру.</span><span class="sxs-lookup"><span data-stu-id="1eabe-150">When you are finished with the data structures pointed to by the  _lppRestriction_ and  _lppContainerList_ parameters, call [MAPIFreeBuffer](mapifreebuffer.md) once for each structure to be released.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1eabe-151">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="1eabe-151">MFCMAPI reference</span></span>

<span data-ttu-id="1eabe-152">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="1eabe-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1eabe-153">**Файл**</span><span class="sxs-lookup"><span data-stu-id="1eabe-153">**File**</span></span>|<span data-ttu-id="1eabe-154">**Функция**</span><span class="sxs-lookup"><span data-stu-id="1eabe-154">**Function**</span></span>|<span data-ttu-id="1eabe-155">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="1eabe-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1eabe-156">HierarchyTableDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="1eabe-156">HierarchyTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="1eabe-157">CHierarchyTableDlg::OnEditSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="1eabe-157">CHierarchyTableDlg::OnEditSearchCriteria</span></span>  <br/> |<span data-ttu-id="1eabe-158">MFCMAPI использует метод **IMAPIContainer::GetSearchCriteria** для получения критериев поиска из папки для отображения.</span><span class="sxs-lookup"><span data-stu-id="1eabe-158">MFCMAPI uses the **IMAPIContainer::GetSearchCriteria** method to obtain search criteria from a folder to display.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1eabe-159">См. также</span><span class="sxs-lookup"><span data-stu-id="1eabe-159">See also</span></span>



[<span data-ttu-id="1eabe-160">IMAPIContainer::SetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="1eabe-160">IMAPIContainer::SetSearchCriteria</span></span>](imapicontainer-setsearchcriteria.md)
  
[<span data-ttu-id="1eabe-161">IMAPIFolder::CreateFolder</span><span class="sxs-lookup"><span data-stu-id="1eabe-161">IMAPIFolder::CreateFolder</span></span>](imapifolder-createfolder.md)
  
[<span data-ttu-id="1eabe-162">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="1eabe-162">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="1eabe-163">Каноническое свойство PidTagSearch</span><span class="sxs-lookup"><span data-stu-id="1eabe-163">PidTagSearch Canonical Property</span></span>](pidtagsearch-canonical-property.md)
  
[<span data-ttu-id="1eabe-164">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="1eabe-164">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


[<span data-ttu-id="1eabe-165">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="1eabe-165">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

