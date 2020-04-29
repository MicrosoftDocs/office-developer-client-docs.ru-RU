---
title: имапиконтаинержетсеарчкритериа
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
# <a name="imapicontainergetsearchcriteria"></a><span data-ttu-id="409ba-103">IMAPIContainer::GetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="409ba-103">IMAPIContainer::GetSearchCriteria</span></span>

  
  
<span data-ttu-id="409ba-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="409ba-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="409ba-105">Получает условия поиска для контейнера.</span><span class="sxs-lookup"><span data-stu-id="409ba-105">Obtains the search criteria for the container.</span></span>
  
```cpp
HRESULT GetSearchCriteria(
  ULONG ulFlags,
  LPSRestriction FAR * lppRestriction,
  LPENTRYLIST FAR * lppContainerList,
  ULONG FAR * lpulSearchState
);
```

## <a name="parameters"></a><span data-ttu-id="409ba-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="409ba-106">Parameters</span></span>

 <span data-ttu-id="409ba-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="409ba-107">_ulFlags_</span></span>
  
> <span data-ttu-id="409ba-108">возврата Битовая маска флагов, которые управляют типом переданных строк.</span><span class="sxs-lookup"><span data-stu-id="409ba-108">[in] A bitmask of flags that controls the type of the passed-in strings.</span></span> <span data-ttu-id="409ba-109">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="409ba-109">The following flag can be set:</span></span>
    
<span data-ttu-id="409ba-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="409ba-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="409ba-111">Переданные строки имеют формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="409ba-111">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="409ba-112">Если флаг MAPI_UNICODE не установлен, строки представлены в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="409ba-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="409ba-113">_лппрестриктион_</span><span class="sxs-lookup"><span data-stu-id="409ba-113">_lppRestriction_</span></span>
  
> <span data-ttu-id="409ba-114">вышли Указатель на указатель на структуру [срестриктион](srestriction.md) , которая определяет критерии поиска.</span><span class="sxs-lookup"><span data-stu-id="409ba-114">[out] A pointer to a pointer to an [SRestriction](srestriction.md) structure that defines the search criteria.</span></span> <span data-ttu-id="409ba-115">Если клиентское приложение передает значение NULL в параметр _лппрестриктион_ , то **жетсеарчкритериа** не возвращает структуру **срестриктион** .</span><span class="sxs-lookup"><span data-stu-id="409ba-115">If a client application passes NULL in the  _lppRestriction_ parameter, **GetSearchCriteria** does not return an **SRestriction** structure.</span></span> 
    
 <span data-ttu-id="409ba-116">_лппконтаинерлист_</span><span class="sxs-lookup"><span data-stu-id="409ba-116">_lppContainerList_</span></span>
  
> <span data-ttu-id="409ba-117">вышли Указатель на указатель на массив идентификаторов записей, которые представляют контейнеры, включаемые в поиск.</span><span class="sxs-lookup"><span data-stu-id="409ba-117">[out] A pointer to a pointer to an array of entry identifiers that represent containers to be included in the search.</span></span> <span data-ttu-id="409ba-118">Если клиент передает значение NULL в параметр _лппконтаинерлист_ , то **жетсеарчкритериа** не возвращает массив идентификаторов записей.</span><span class="sxs-lookup"><span data-stu-id="409ba-118">If a client passes NULL in the  _lppContainerList_ parameter, **GetSearchCriteria** does not return an array of entry identifiers.</span></span> 
    
 <span data-ttu-id="409ba-119">_лпулсеарчстате_</span><span class="sxs-lookup"><span data-stu-id="409ba-119">_lpulSearchState_</span></span>
  
> <span data-ttu-id="409ba-120">вышли Указатель на битовую маску флагов, используемый для указания текущего состояния поиска.</span><span class="sxs-lookup"><span data-stu-id="409ba-120">[out] A pointer to a bitmask of flags used to indicate the current state of the search.</span></span> <span data-ttu-id="409ba-121">Если клиент передает значение NULL в параметр _лпулсеарчстате_ , **жетсеарчкритериа** не возвращает флагов.</span><span class="sxs-lookup"><span data-stu-id="409ba-121">If a client passes NULL in the  _lpulSearchState_ parameter, **GetSearchCriteria** returns no flags.</span></span> <span data-ttu-id="409ba-122">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="409ba-122">The following flags can be set:</span></span> 
    
<span data-ttu-id="409ba-123">SEARCH_FOREGROUND</span><span class="sxs-lookup"><span data-stu-id="409ba-123">SEARCH_FOREGROUND</span></span> 
  
> <span data-ttu-id="409ba-124">Поиск должен выполняться с высоким приоритетом, связанным с другими поисковыми операциями.</span><span class="sxs-lookup"><span data-stu-id="409ba-124">The search should run at high priority relative to other searches.</span></span> <span data-ttu-id="409ba-125">Если этот флаг не установлен, поиск выполняется с нормальным приоритетом относительно других поисков.</span><span class="sxs-lookup"><span data-stu-id="409ba-125">If this flag is not set, the search runs at normal priority relative to other searches.</span></span>
    
<span data-ttu-id="409ba-126">SEARCH_REBUILD</span><span class="sxs-lookup"><span data-stu-id="409ba-126">SEARCH_REBUILD</span></span> 
  
> <span data-ttu-id="409ba-127">Поиск выполняется в режиме интенсивного использования ЦП для операции, пытаясь найти сообщения, соответствующие условиям.</span><span class="sxs-lookup"><span data-stu-id="409ba-127">The search is in the CPU-intensive mode of its operation, trying to locate messages that match the criteria.</span></span> <span data-ttu-id="409ba-128">Если этот флаг не установлен, часть операции поиска, интенсивно использующая ЦП, превышает.</span><span class="sxs-lookup"><span data-stu-id="409ba-128">If this flag is not set, the CPU-intensive part of the search's operation is over.</span></span> <span data-ttu-id="409ba-129">Этот флаг имеет значение только в том случае, если активен Поиск (то есть, если установлен флаг SEARCH_RUNNING).</span><span class="sxs-lookup"><span data-stu-id="409ba-129">This flag has meaning only if the search is active (that is, if the SEARCH_RUNNING flag is set).</span></span>
    
<span data-ttu-id="409ba-130">SEARCH_RECURSIVE</span><span class="sxs-lookup"><span data-stu-id="409ba-130">SEARCH_RECURSIVE</span></span> 
  
> <span data-ttu-id="409ba-131">Поиск выполняется в указанных контейнерах и всех дочерних контейнерах для соответствующих записей.</span><span class="sxs-lookup"><span data-stu-id="409ba-131">The search is looking in specified containers and all their child containers for matching entries.</span></span> <span data-ttu-id="409ba-132">Если этот флаг не задан, поиск выполняется только для контейнеров, явно включенных в последний вызов метода [IMAPIContainer:: сетсеарчкритериа](imapicontainer-setsearchcriteria.md) .</span><span class="sxs-lookup"><span data-stu-id="409ba-132">If this flag is not set, only the containers explicitly included in the last call to the [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method are being searched.</span></span> 
    
<span data-ttu-id="409ba-133">SEARCH_RUNNING</span><span class="sxs-lookup"><span data-stu-id="409ba-133">SEARCH_RUNNING</span></span> 
  
> <span data-ttu-id="409ba-134">Поиск активен, и таблица содержимого контейнера обновляется в соответствии с изменениями, внесенными в хранилище сообщений или адресную книгу.</span><span class="sxs-lookup"><span data-stu-id="409ba-134">The search is active and the container's contents table is being updated to reflect changes in the message store or address book.</span></span> <span data-ttu-id="409ba-135">Если этот флаг не установлен, поиск является неактивным и таблица содержимого является статической.</span><span class="sxs-lookup"><span data-stu-id="409ba-135">If this flag is not set, the search is inactive and the contents table is static.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="409ba-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="409ba-136">Return value</span></span>

<span data-ttu-id="409ba-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="409ba-137">S_OK</span></span> 
  
> <span data-ttu-id="409ba-138">Условия поиска успешно получены.</span><span class="sxs-lookup"><span data-stu-id="409ba-138">The search criteria was successfully obtained.</span></span>
    
<span data-ttu-id="409ba-139">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="409ba-139">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="409ba-140">Установлен флаг MAPI_UNICODE, а реализация не поддерживает Юникод, или MAPI_UNICODE не задано, а реализация поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="409ba-140">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="409ba-141">MAPI_E_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="409ba-141">MAPI_E_NOT_INITIALIZED</span></span> 
  
> <span data-ttu-id="409ba-142">Условия поиска для контейнера никогда не были установлены.</span><span class="sxs-lookup"><span data-stu-id="409ba-142">Search criteria were never established for the container.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="409ba-143">Примечания</span><span class="sxs-lookup"><span data-stu-id="409ba-143">Remarks</span></span>

<span data-ttu-id="409ba-144">Метод **IMAPIContainer:: жетсеарчкритериа** получает условия поиска для контейнера, поддерживающего Поиск, как правило, папка результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="409ba-144">The **IMAPIContainer::GetSearchCriteria** method obtains the search criteria for a container that supports searches, typically a search-results folder.</span></span> <span data-ttu-id="409ba-145">Вы создаете критерии поиска, вызывая метод контейнера **IMAPIContainer:: сетсеарчкритериа** .</span><span class="sxs-lookup"><span data-stu-id="409ba-145">You create search criteria by calling a container's **IMAPIContainer::SetSearchCriteria** method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="409ba-146">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="409ba-146">Notes to implementers</span></span>

<span data-ttu-id="409ba-147">Для контейнеров адресных книг может потребоваться поддержка **жетсеарчкритериа** только в том случае, если они предоставляют расширенные возможности поиска, связанные со свойством **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="409ba-147">Address book containers may need to support **GetSearchCriteria** only if they provide the advanced search capabilities associated with the **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) property.</span></span> <span data-ttu-id="409ba-148">Дополнительные сведения о том, как реализовать функцию расширенного поиска для контейнеров адресных книг, можно узнать в статье [Реализация расширенного](implementing-advanced-searching.md)поиска.</span><span class="sxs-lookup"><span data-stu-id="409ba-148">For more information about how to implement the advanced search feature for address book containers, see [Implementing Advanced Searching](implementing-advanced-searching.md).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="409ba-149">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="409ba-149">Notes to callers</span></span>

<span data-ttu-id="409ba-150">По завершении работы с структурами данных, на которые указывает параметр _лппрестриктион_ и _лппконтаинерлист_ , вызовите [мапифрибуффер](mapifreebuffer.md) один раз для каждой структуры, чтобы освободить их.</span><span class="sxs-lookup"><span data-stu-id="409ba-150">When you are finished with the data structures pointed to by the  _lppRestriction_ and  _lppContainerList_ parameters, call [MAPIFreeBuffer](mapifreebuffer.md) once for each structure to be released.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="409ba-151">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="409ba-151">MFCMAPI reference</span></span>

<span data-ttu-id="409ba-152">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="409ba-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="409ba-153">**Файл**</span><span class="sxs-lookup"><span data-stu-id="409ba-153">**File**</span></span>|<span data-ttu-id="409ba-154">**Функция**</span><span class="sxs-lookup"><span data-stu-id="409ba-154">**Function**</span></span>|<span data-ttu-id="409ba-155">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="409ba-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="409ba-156">Хиерарчитабледлг. cpp</span><span class="sxs-lookup"><span data-stu-id="409ba-156">HierarchyTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="409ba-157">Чиерарчитабледлг:: Онедитсеарчкритериа</span><span class="sxs-lookup"><span data-stu-id="409ba-157">CHierarchyTableDlg::OnEditSearchCriteria</span></span>  <br/> |<span data-ttu-id="409ba-158">MFCMAPI использует метод **IMAPIContainer:: жетсеарчкритериа** для получения условий поиска из папки для отображения.</span><span class="sxs-lookup"><span data-stu-id="409ba-158">MFCMAPI uses the **IMAPIContainer::GetSearchCriteria** method to obtain search criteria from a folder to display.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="409ba-159">См. также</span><span class="sxs-lookup"><span data-stu-id="409ba-159">See also</span></span>



[<span data-ttu-id="409ba-160">IMAPIContainer::SetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="409ba-160">IMAPIContainer::SetSearchCriteria</span></span>](imapicontainer-setsearchcriteria.md)
  
[<span data-ttu-id="409ba-161">IMAPIFolder::CreateFolder</span><span class="sxs-lookup"><span data-stu-id="409ba-161">IMAPIFolder::CreateFolder</span></span>](imapifolder-createfolder.md)
  
[<span data-ttu-id="409ba-162">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="409ba-162">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="409ba-163">Каноническое свойство PidTagSearch</span><span class="sxs-lookup"><span data-stu-id="409ba-163">PidTagSearch Canonical Property</span></span>](pidtagsearch-canonical-property.md)
  
[<span data-ttu-id="409ba-164">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="409ba-164">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


[<span data-ttu-id="409ba-165">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="409ba-165">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

