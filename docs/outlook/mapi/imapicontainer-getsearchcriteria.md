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
ms.openlocfilehash: 4ca565f97851a2efe2f3279f062f6ea89a4c6326
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579965"
---
# <a name="imapicontainergetsearchcriteria"></a><span data-ttu-id="41d44-103">IMAPIContainer::GetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="41d44-103">IMAPIContainer::GetSearchCriteria</span></span>

  
  
<span data-ttu-id="41d44-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="41d44-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="41d44-105">Получает параметры поиска для контейнера.</span><span class="sxs-lookup"><span data-stu-id="41d44-105">Obtains the search criteria for the container.</span></span>
  
```cpp
HRESULT GetSearchCriteria(
  ULONG ulFlags,
  LPSRestriction FAR * lppRestriction,
  LPENTRYLIST FAR * lppContainerList,
  ULONG FAR * lpulSearchState
);
```

## <a name="parameters"></a><span data-ttu-id="41d44-106">���������</span><span class="sxs-lookup"><span data-stu-id="41d44-106">Parameters</span></span>

 <span data-ttu-id="41d44-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="41d44-107">_ulFlags_</span></span>
  
> <span data-ttu-id="41d44-108">[in] Битовая маска флаги, определяющее тип строк, переданное.</span><span class="sxs-lookup"><span data-stu-id="41d44-108">[in] A bitmask of flags that controls the type of the passed-in strings.</span></span> <span data-ttu-id="41d44-109">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="41d44-109">The following flag can be set:</span></span>
    
<span data-ttu-id="41d44-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="41d44-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="41d44-111">Строки переданное хранятся в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="41d44-111">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="41d44-112">Если флаг MAPI_UNICODE не установлен, они в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="41d44-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="41d44-113">_lppRestriction_</span><span class="sxs-lookup"><span data-stu-id="41d44-113">_lppRestriction_</span></span>
  
> <span data-ttu-id="41d44-114">[out] Указатель на указатель на структуру [SRestriction](srestriction.md) , определяющий условия поиска.</span><span class="sxs-lookup"><span data-stu-id="41d44-114">[out] A pointer to a pointer to an [SRestriction](srestriction.md) structure that defines the search criteria.</span></span> <span data-ttu-id="41d44-115">Если клиентское приложение передает значение NULL в параметре _lppRestriction_ , **GetSearchCriteria** не возвращает структуру **SRestriction** .</span><span class="sxs-lookup"><span data-stu-id="41d44-115">If a client application passes NULL in the  _lppRestriction_ parameter, **GetSearchCriteria** does not return an **SRestriction** structure.</span></span> 
    
 <span data-ttu-id="41d44-116">_lppContainerList_</span><span class="sxs-lookup"><span data-stu-id="41d44-116">_lppContainerList_</span></span>
  
> <span data-ttu-id="41d44-117">[out] Указатель на указатель на массив идентификаторов записи, которые представляют контейнеров, включаемых в поиск.</span><span class="sxs-lookup"><span data-stu-id="41d44-117">[out] A pointer to a pointer to an array of entry identifiers that represent containers to be included in the search.</span></span> <span data-ttu-id="41d44-118">Если клиент передает значение NULL в параметре _lppContainerList_ , **GetSearchCriteria** не возвращает массив идентификаторов запись.</span><span class="sxs-lookup"><span data-stu-id="41d44-118">If a client passes NULL in the  _lppContainerList_ parameter, **GetSearchCriteria** does not return an array of entry identifiers.</span></span> 
    
 <span data-ttu-id="41d44-119">_lpulSearchState_</span><span class="sxs-lookup"><span data-stu-id="41d44-119">_lpulSearchState_</span></span>
  
> <span data-ttu-id="41d44-120">[out] Указатель на битовой маски флагов, используемых для указания текущего состояния поиска.</span><span class="sxs-lookup"><span data-stu-id="41d44-120">[out] A pointer to a bitmask of flags used to indicate the current state of the search.</span></span> <span data-ttu-id="41d44-121">Если клиент передает значение NULL в параметре _lpulSearchState_ , **GetSearchCriteria** Возвращает флаги не.</span><span class="sxs-lookup"><span data-stu-id="41d44-121">If a client passes NULL in the  _lpulSearchState_ parameter, **GetSearchCriteria** returns no flags.</span></span> <span data-ttu-id="41d44-122">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="41d44-122">The following flags can be set:</span></span> 
    
<span data-ttu-id="41d44-123">SEARCH_FOREGROUND</span><span class="sxs-lookup"><span data-stu-id="41d44-123">SEARCH_FOREGROUND</span></span> 
  
> <span data-ttu-id="41d44-124">Поиск должен выполняться с наивысший приоритет относительно других операций поиска.</span><span class="sxs-lookup"><span data-stu-id="41d44-124">The search should run at high priority relative to other searches.</span></span> <span data-ttu-id="41d44-125">Если этот флаг не установлен, с обычным приоритетом относительно других операций поиска выполняется поиск.</span><span class="sxs-lookup"><span data-stu-id="41d44-125">If this flag is not set, the search runs at normal priority relative to other searches.</span></span>
    
<span data-ttu-id="41d44-126">SEARCH_REBUILD</span><span class="sxs-lookup"><span data-stu-id="41d44-126">SEARCH_REBUILD</span></span> 
  
> <span data-ttu-id="41d44-127">Поиск — в режиме высокой загрузкой ЦП операции, чтобы найти сообщения, соответствующие критериям.</span><span class="sxs-lookup"><span data-stu-id="41d44-127">The search is in the CPU-intensive mode of its operation, trying to locate messages that match the criteria.</span></span> <span data-ttu-id="41d44-128">Если этот флаг не установлен, окончена высокой загрузкой ЦП частью операции поиска.</span><span class="sxs-lookup"><span data-stu-id="41d44-128">If this flag is not set, the CPU-intensive part of the search's operation is over.</span></span> <span data-ttu-id="41d44-129">Этот флаг имеет значение только в том случае, если поиск является активным (то есть, если установлен флаг SEARCH_RUNNING).</span><span class="sxs-lookup"><span data-stu-id="41d44-129">This flag has meaning only if the search is active (that is, if the SEARCH_RUNNING flag is set).</span></span>
    
<span data-ttu-id="41d44-130">SEARCH_RECURSIVE</span><span class="sxs-lookup"><span data-stu-id="41d44-130">SEARCH_RECURSIVE</span></span> 
  
> <span data-ttu-id="41d44-131">Поиск в заданных контейнеров и всех их дочерних контейнеров для соответствующих записей.</span><span class="sxs-lookup"><span data-stu-id="41d44-131">The search is looking in specified containers and all their child containers for matching entries.</span></span> <span data-ttu-id="41d44-132">Если этот флаг не установлен, только контейнеры, явно включены в последнем вызове метода [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) которых осуществляется поиск.</span><span class="sxs-lookup"><span data-stu-id="41d44-132">If this flag is not set, only the containers explicitly included in the last call to the [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method are being searched.</span></span> 
    
<span data-ttu-id="41d44-133">SEARCH_RUNNING</span><span class="sxs-lookup"><span data-stu-id="41d44-133">SEARCH_RUNNING</span></span> 
  
> <span data-ttu-id="41d44-134">Поиск является активной и контейнера содержимое таблицы обновляется для отражения изменений в хранилище сообщений или адресная книга.</span><span class="sxs-lookup"><span data-stu-id="41d44-134">The search is active and the container's contents table is being updated to reflect changes in the message store or address book.</span></span> <span data-ttu-id="41d44-135">Если этот флаг не установлен, поиска неактивных и статического содержимого таблицы.</span><span class="sxs-lookup"><span data-stu-id="41d44-135">If this flag is not set, the search is inactive and the contents table is static.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="41d44-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="41d44-136">Return value</span></span>

<span data-ttu-id="41d44-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="41d44-137">S_OK</span></span> 
  
> <span data-ttu-id="41d44-138">Условия поиска успешно был получен.</span><span class="sxs-lookup"><span data-stu-id="41d44-138">The search criteria was successfully obtained.</span></span>
    
<span data-ttu-id="41d44-139">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="41d44-139">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="41d44-140">Либо был установлен флажок MAPI_UNICODE и реализация не поддерживает Юникод, или MAPI_UNICODE не было установлено и реализация поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="41d44-140">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="41d44-141">MAPI_E_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="41d44-141">MAPI_E_NOT_INITIALIZED</span></span> 
  
> <span data-ttu-id="41d44-142">Условия поиска никогда не были настроены для контейнера.</span><span class="sxs-lookup"><span data-stu-id="41d44-142">Search criteria were never established for the container.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="41d44-143">Замечания</span><span class="sxs-lookup"><span data-stu-id="41d44-143">Remarks</span></span>

<span data-ttu-id="41d44-144">Метод **IMAPIContainer::GetSearchCriteria** получает условия поиска для контейнера, поддерживающего поиск, обычно в папку результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="41d44-144">The **IMAPIContainer::GetSearchCriteria** method obtains the search criteria for a container that supports searches, typically a search-results folder.</span></span> <span data-ttu-id="41d44-145">Создание условия поиска, вызвав метод **IMAPIContainer::SetSearchCriteria** контейнера.</span><span class="sxs-lookup"><span data-stu-id="41d44-145">You create search criteria by calling a container's **IMAPIContainer::SetSearchCriteria** method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="41d44-146">Примечания для реализующих</span><span class="sxs-lookup"><span data-stu-id="41d44-146">Notes to implementers</span></span>

<span data-ttu-id="41d44-147">Контейнеры адресной книги может потребоваться поддержка **GetSearchCriteria** только в том случае, если они предоставляют возможности расширенного поиска, связанного со свойством **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="41d44-147">Address book containers may need to support **GetSearchCriteria** only if they provide the advanced search capabilities associated with the **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) property.</span></span> <span data-ttu-id="41d44-148">Дополнительные сведения о том, как реализовать функцию расширенного поиска для контейнеров адресной книги, можно [Реализация расширенный поиск](implementing-advanced-searching.md).</span><span class="sxs-lookup"><span data-stu-id="41d44-148">For more information about how to implement the advanced search feature for address book containers, see [Implementing Advanced Searching](implementing-advanced-searching.md).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="41d44-149">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="41d44-149">Notes to callers</span></span>

<span data-ttu-id="41d44-150">После завершения структуры данных, на который указывает параметры _lppRestriction_ и _lppContainerList_ вызов [MAPIFreeBuffer](mapifreebuffer.md) один раз для каждого структуры нужно освободить.</span><span class="sxs-lookup"><span data-stu-id="41d44-150">When you are finished with the data structures pointed to by the  _lppRestriction_ and  _lppContainerList_ parameters, call [MAPIFreeBuffer](mapifreebuffer.md) once for each structure to be released.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="41d44-151">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="41d44-151">MFCMAPI reference</span></span>

<span data-ttu-id="41d44-152">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="41d44-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="41d44-153">**Файл**</span><span class="sxs-lookup"><span data-stu-id="41d44-153">**File**</span></span>|<span data-ttu-id="41d44-154">**Функция**</span><span class="sxs-lookup"><span data-stu-id="41d44-154">**Function**</span></span>|<span data-ttu-id="41d44-155">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="41d44-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="41d44-156">HierarchyTableDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="41d44-156">HierarchyTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="41d44-157">CHierarchyTableDlg::OnEditSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="41d44-157">CHierarchyTableDlg::OnEditSearchCriteria</span></span>  <br/> |<span data-ttu-id="41d44-158">Mfcmapi (en) использует метод **IMAPIContainer::GetSearchCriteria** для получения условия поиска из папки для отображения.</span><span class="sxs-lookup"><span data-stu-id="41d44-158">MFCMAPI uses the **IMAPIContainer::GetSearchCriteria** method to obtain search criteria from a folder to display.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="41d44-159">См. также</span><span class="sxs-lookup"><span data-stu-id="41d44-159">See also</span></span>



[<span data-ttu-id="41d44-160">IMAPIContainer::SetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="41d44-160">IMAPIContainer::SetSearchCriteria</span></span>](imapicontainer-setsearchcriteria.md)
  
[<span data-ttu-id="41d44-161">IMAPIFolder::CreateFolder</span><span class="sxs-lookup"><span data-stu-id="41d44-161">IMAPIFolder::CreateFolder</span></span>](imapifolder-createfolder.md)
  
[<span data-ttu-id="41d44-162">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="41d44-162">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="41d44-163">Каноническое свойство PidTagSearch</span><span class="sxs-lookup"><span data-stu-id="41d44-163">PidTagSearch Canonical Property</span></span>](pidtagsearch-canonical-property.md)
  
[<span data-ttu-id="41d44-164">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="41d44-164">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


[<span data-ttu-id="41d44-165">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="41d44-165">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

