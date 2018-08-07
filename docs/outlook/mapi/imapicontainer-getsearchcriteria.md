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
ms.openlocfilehash: 13c151a134e4334e8ed2e75e031a6fc9dddbf941
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808829"
---
# <a name="imapicontainergetsearchcriteria"></a><span data-ttu-id="dc0d6-103">IMAPIContainer::GetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="dc0d6-103">IMAPIContainer::GetSearchCriteria</span></span>

  
  
<span data-ttu-id="dc0d6-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="dc0d6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="dc0d6-105">Получает параметры поиска для контейнера.</span><span class="sxs-lookup"><span data-stu-id="dc0d6-105">Obtains the search criteria for the container.</span></span>
  
```cpp
HRESULT GetSearchCriteria(
  ULONG ulFlags,
  LPSRestriction FAR * lppRestriction,
  LPENTRYLIST FAR * lppContainerList,
  ULONG FAR * lpulSearchState
);
```

## <a name="parameters"></a><span data-ttu-id="dc0d6-106">���������</span><span class="sxs-lookup"><span data-stu-id="dc0d6-106">Parameters</span></span>

 <span data-ttu-id="dc0d6-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="dc0d6-107">_ulFlags_</span></span>
  
> <span data-ttu-id="dc0d6-108">[in] Битовая маска флаги, определяющее тип строк, переданное.</span><span class="sxs-lookup"><span data-stu-id="dc0d6-108">[in] A bitmask of flags that controls the type of the passed-in strings.</span></span> <span data-ttu-id="dc0d6-109">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="dc0d6-109">The following flag can be set:</span></span>
    
<span data-ttu-id="dc0d6-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="dc0d6-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="dc0d6-111">Строки переданное хранятся в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="dc0d6-111">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="dc0d6-112">Если флаг MAPI_UNICODE не установлен, они в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="dc0d6-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="dc0d6-113">_lppRestriction_</span><span class="sxs-lookup"><span data-stu-id="dc0d6-113">_lppRestriction_</span></span>
  
> <span data-ttu-id="dc0d6-114">[out] Указатель на указатель на структуру [SRestriction](srestriction.md) , определяющий условия поиска.</span><span class="sxs-lookup"><span data-stu-id="dc0d6-114">[out] A pointer to a pointer to an [SRestriction](srestriction.md) structure that defines the search criteria.</span></span> <span data-ttu-id="dc0d6-115">Если клиентское приложение передает значение NULL в параметре _lppRestriction_ , **GetSearchCriteria** не возвращает структуру **SRestriction** .</span><span class="sxs-lookup"><span data-stu-id="dc0d6-115">If a client application passes NULL in the  _lppRestriction_ parameter, **GetSearchCriteria** does not return an **SRestriction** structure.</span></span> 
    
 <span data-ttu-id="dc0d6-116">_lppContainerList_</span><span class="sxs-lookup"><span data-stu-id="dc0d6-116">_lppContainerList_</span></span>
  
> <span data-ttu-id="dc0d6-117">[out] Указатель на указатель на массив идентификаторов записи, которые представляют контейнеров, включаемых в поиск.</span><span class="sxs-lookup"><span data-stu-id="dc0d6-117">[out] A pointer to a pointer to an array of entry identifiers that represent containers to be included in the search.</span></span> <span data-ttu-id="dc0d6-118">Если клиент передает значение NULL в параметре _lppContainerList_ , **GetSearchCriteria** не возвращает массив идентификаторов запись.</span><span class="sxs-lookup"><span data-stu-id="dc0d6-118">If a client passes NULL in the  _lppContainerList_ parameter, **GetSearchCriteria** does not return an array of entry identifiers.</span></span> 
    
 <span data-ttu-id="dc0d6-119">_lpulSearchState_</span><span class="sxs-lookup"><span data-stu-id="dc0d6-119">_lpulSearchState_</span></span>
  
> <span data-ttu-id="dc0d6-120">[out] Указатель на битовой маски флагов, используемых для указания текущего состояния поиска.</span><span class="sxs-lookup"><span data-stu-id="dc0d6-120">[out] A pointer to a bitmask of flags used to indicate the current state of the search.</span></span> <span data-ttu-id="dc0d6-121">Если клиент передает значение NULL в параметре _lpulSearchState_ , **GetSearchCriteria** Возвращает флаги не.</span><span class="sxs-lookup"><span data-stu-id="dc0d6-121">If a client passes NULL in the  _lpulSearchState_ parameter, **GetSearchCriteria** returns no flags.</span></span> <span data-ttu-id="dc0d6-122">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="dc0d6-122">The following flags can be set:</span></span> 
    
<span data-ttu-id="dc0d6-123">SEARCH_FOREGROUND</span><span class="sxs-lookup"><span data-stu-id="dc0d6-123">SEARCH_FOREGROUND</span></span> 
  
> <span data-ttu-id="dc0d6-124">Поиск должен выполняться с наивысший приоритет относительно других операций поиска.</span><span class="sxs-lookup"><span data-stu-id="dc0d6-124">The search should run at high priority relative to other searches.</span></span> <span data-ttu-id="dc0d6-125">Если этот флаг не установлен, с обычным приоритетом относительно других операций поиска выполняется поиск.</span><span class="sxs-lookup"><span data-stu-id="dc0d6-125">If this flag is not set, the search runs at normal priority relative to other searches.</span></span>
    
<span data-ttu-id="dc0d6-126">SEARCH_REBUILD</span><span class="sxs-lookup"><span data-stu-id="dc0d6-126">SEARCH_REBUILD</span></span> 
  
> <span data-ttu-id="dc0d6-127">Поиск — в режиме высокой загрузкой ЦП операции, чтобы найти сообщения, соответствующие критериям.</span><span class="sxs-lookup"><span data-stu-id="dc0d6-127">The search is in the CPU-intensive mode of its operation, trying to locate messages that match the criteria.</span></span> <span data-ttu-id="dc0d6-128">Если этот флаг не установлен, окончена высокой загрузкой ЦП частью операции поиска.</span><span class="sxs-lookup"><span data-stu-id="dc0d6-128">If this flag is not set, the CPU-intensive part of the search's operation is over.</span></span> <span data-ttu-id="dc0d6-129">Этот флаг имеет значение только в том случае, если поиск является активным (то есть, если установлен флаг SEARCH_RUNNING).</span><span class="sxs-lookup"><span data-stu-id="dc0d6-129">This flag has meaning only if the search is active (that is, if the SEARCH_RUNNING flag is set).</span></span>
    
<span data-ttu-id="dc0d6-130">SEARCH_RECURSIVE</span><span class="sxs-lookup"><span data-stu-id="dc0d6-130">SEARCH_RECURSIVE</span></span> 
  
> <span data-ttu-id="dc0d6-131">Поиск в заданных контейнеров и всех их дочерних контейнеров для соответствующих записей.</span><span class="sxs-lookup"><span data-stu-id="dc0d6-131">The search is looking in specified containers and all their child containers for matching entries.</span></span> <span data-ttu-id="dc0d6-132">Если этот флаг не установлен, только контейнеры, явно включены в последнем вызове метода [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) которых осуществляется поиск.</span><span class="sxs-lookup"><span data-stu-id="dc0d6-132">If this flag is not set, only the containers explicitly included in the last call to the [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method are being searched.</span></span> 
    
<span data-ttu-id="dc0d6-133">SEARCH_RUNNING</span><span class="sxs-lookup"><span data-stu-id="dc0d6-133">SEARCH_RUNNING</span></span> 
  
> <span data-ttu-id="dc0d6-134">Поиск является активной и контейнера содержимое таблицы обновляется для отражения изменений в хранилище сообщений или адресная книга.</span><span class="sxs-lookup"><span data-stu-id="dc0d6-134">The search is active and the container's contents table is being updated to reflect changes in the message store or address book.</span></span> <span data-ttu-id="dc0d6-135">Если этот флаг не установлен, поиска неактивных и статического содержимого таблицы.</span><span class="sxs-lookup"><span data-stu-id="dc0d6-135">If this flag is not set, the search is inactive and the contents table is static.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="dc0d6-136">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="dc0d6-136">Return value</span></span>

<span data-ttu-id="dc0d6-137">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="dc0d6-137">S_OK</span></span> 
  
> <span data-ttu-id="dc0d6-138">Условия поиска успешно был получен.</span><span class="sxs-lookup"><span data-stu-id="dc0d6-138">The search criteria was successfully obtained.</span></span>
    
<span data-ttu-id="dc0d6-139">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="dc0d6-139">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="dc0d6-140">Либо был установлен флажок MAPI_UNICODE и реализация не поддерживает Юникод, или MAPI_UNICODE не было установлено и реализация поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="dc0d6-140">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="dc0d6-141">MAPI_E_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="dc0d6-141">MAPI_E_NOT_INITIALIZED</span></span> 
  
> <span data-ttu-id="dc0d6-142">Условия поиска никогда не были настроены для контейнера.</span><span class="sxs-lookup"><span data-stu-id="dc0d6-142">Search criteria were never established for the container.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dc0d6-143">Замечания</span><span class="sxs-lookup"><span data-stu-id="dc0d6-143">Remarks</span></span>

<span data-ttu-id="dc0d6-144">Метод **IMAPIContainer::GetSearchCriteria** получает условия поиска для контейнера, поддерживающего поиск, обычно в папку результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="dc0d6-144">The **IMAPIContainer::GetSearchCriteria** method obtains the search criteria for a container that supports searches, typically a search-results folder.</span></span> <span data-ttu-id="dc0d6-145">Создание условия поиска, вызвав метод **IMAPIContainer::SetSearchCriteria** контейнера.</span><span class="sxs-lookup"><span data-stu-id="dc0d6-145">You create search criteria by calling a container's **IMAPIContainer::SetSearchCriteria** method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="dc0d6-146">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="dc0d6-146">Notes to implementers</span></span>

<span data-ttu-id="dc0d6-147">Контейнеры адресной книги может потребоваться поддержка **GetSearchCriteria** только в том случае, если они предоставляют возможности расширенного поиска, связанного со свойством **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="dc0d6-147">Address book containers may need to support **GetSearchCriteria** only if they provide the advanced search capabilities associated with the **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) property.</span></span> <span data-ttu-id="dc0d6-148">Дополнительные сведения о том, как реализовать функцию расширенного поиска для контейнеров адресной книги, можно [Реализация расширенный поиск](implementing-advanced-searching.md).</span><span class="sxs-lookup"><span data-stu-id="dc0d6-148">For more information about how to implement the advanced search feature for address book containers, see [Implementing Advanced Searching](implementing-advanced-searching.md).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="dc0d6-149">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="dc0d6-149">Notes to callers</span></span>

<span data-ttu-id="dc0d6-150">После завершения структуры данных, на который указывает параметры _lppRestriction_ и _lppContainerList_ вызов [MAPIFreeBuffer](mapifreebuffer.md) один раз для каждого структуры нужно освободить.</span><span class="sxs-lookup"><span data-stu-id="dc0d6-150">When you are finished with the data structures pointed to by the  _lppRestriction_ and  _lppContainerList_ parameters, call [MAPIFreeBuffer](mapifreebuffer.md) once for each structure to be released.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="dc0d6-151">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="dc0d6-151">MFCMAPI reference</span></span>

<span data-ttu-id="dc0d6-152">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="dc0d6-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="dc0d6-153">**����**</span><span class="sxs-lookup"><span data-stu-id="dc0d6-153">**File**</span></span>|<span data-ttu-id="dc0d6-154">**�������**</span><span class="sxs-lookup"><span data-stu-id="dc0d6-154">**Function**</span></span>|<span data-ttu-id="dc0d6-155">**�����������**</span><span class="sxs-lookup"><span data-stu-id="dc0d6-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="dc0d6-156">HierarchyTableDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="dc0d6-156">HierarchyTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="dc0d6-157">CHierarchyTableDlg::OnEditSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="dc0d6-157">CHierarchyTableDlg::OnEditSearchCriteria</span></span>  <br/> |<span data-ttu-id="dc0d6-158">Mfcmapi (en) использует метод **IMAPIContainer::GetSearchCriteria** для получения условия поиска из папки для отображения.</span><span class="sxs-lookup"><span data-stu-id="dc0d6-158">MFCMAPI uses the **IMAPIContainer::GetSearchCriteria** method to obtain search criteria from a folder to display.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dc0d6-159">См. также</span><span class="sxs-lookup"><span data-stu-id="dc0d6-159">See also</span></span>



[<span data-ttu-id="dc0d6-160">IMAPIContainer::SetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="dc0d6-160">IMAPIContainer::SetSearchCriteria</span></span>](imapicontainer-setsearchcriteria.md)
  
[<span data-ttu-id="dc0d6-161">IMAPIFolder::CreateFolder</span><span class="sxs-lookup"><span data-stu-id="dc0d6-161">IMAPIFolder::CreateFolder</span></span>](imapifolder-createfolder.md)
  
[<span data-ttu-id="dc0d6-162">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="dc0d6-162">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="dc0d6-163">Каноническое свойство PidTagSearch</span><span class="sxs-lookup"><span data-stu-id="dc0d6-163">PidTagSearch Canonical Property</span></span>](pidtagsearch-canonical-property.md)
  
[<span data-ttu-id="dc0d6-164">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="dc0d6-164">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


[<span data-ttu-id="dc0d6-165">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="dc0d6-165">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

