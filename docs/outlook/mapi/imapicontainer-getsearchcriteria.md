---
title: Имапиконтаинержетсеарчкритериа
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349296"
---
# <a name="imapicontainergetsearchcriteria"></a><span data-ttu-id="bfa29-103">IMAPIContainer::GetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="bfa29-103">IMAPIContainer::GetSearchCriteria</span></span>

  
  
<span data-ttu-id="bfa29-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bfa29-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bfa29-105">Получает условия поиска для контейнера.</span><span class="sxs-lookup"><span data-stu-id="bfa29-105">Obtains the search criteria for the container.</span></span>
  
```cpp
HRESULT GetSearchCriteria(
  ULONG ulFlags,
  LPSRestriction FAR * lppRestriction,
  LPENTRYLIST FAR * lppContainerList,
  ULONG FAR * lpulSearchState
);
```

## <a name="parameters"></a><span data-ttu-id="bfa29-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bfa29-106">Parameters</span></span>

 <span data-ttu-id="bfa29-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="bfa29-107">_ulFlags_</span></span>
  
> <span data-ttu-id="bfa29-108">возврата Битовая маска флагов, которые управляют типом переданных строк.</span><span class="sxs-lookup"><span data-stu-id="bfa29-108">[in] A bitmask of flags that controls the type of the passed-in strings.</span></span> <span data-ttu-id="bfa29-109">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="bfa29-109">The following flag can be set:</span></span>
    
<span data-ttu-id="bfa29-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="bfa29-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="bfa29-111">Переданные строки имеют формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="bfa29-111">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="bfa29-112">Если флаг МАПИ_УНИКОДЕ не установлен, строки представлены в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="bfa29-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="bfa29-113">_Лппрестриктион_</span><span class="sxs-lookup"><span data-stu-id="bfa29-113">_lppRestriction_</span></span>
  
> <span data-ttu-id="bfa29-114">вышли Указатель на указатель на структуру [срестриктион](srestriction.md) , которая определяет критерии поиска.</span><span class="sxs-lookup"><span data-stu-id="bfa29-114">[out] A pointer to a pointer to an [SRestriction](srestriction.md) structure that defines the search criteria.</span></span> <span data-ttu-id="bfa29-115">Если клиентское приложение передает значение NULL в параметр _лппрестриктион_ , то **жетсеарчкритериа** не возвращает структуру **срестриктион** .</span><span class="sxs-lookup"><span data-stu-id="bfa29-115">If a client application passes NULL in the  _lppRestriction_ parameter, **GetSearchCriteria** does not return an **SRestriction** structure.</span></span> 
    
 <span data-ttu-id="bfa29-116">_Лппконтаинерлист_</span><span class="sxs-lookup"><span data-stu-id="bfa29-116">_lppContainerList_</span></span>
  
> <span data-ttu-id="bfa29-117">вышли Указатель на указатель на массив идентификаторов записей, которые представляют контейнеры, включаемые в поиск.</span><span class="sxs-lookup"><span data-stu-id="bfa29-117">[out] A pointer to a pointer to an array of entry identifiers that represent containers to be included in the search.</span></span> <span data-ttu-id="bfa29-118">Если клиент передает значение NULL в параметр _лппконтаинерлист_ , то **жетсеарчкритериа** не возвращает массив идентификаторов записей.</span><span class="sxs-lookup"><span data-stu-id="bfa29-118">If a client passes NULL in the  _lppContainerList_ parameter, **GetSearchCriteria** does not return an array of entry identifiers.</span></span> 
    
 <span data-ttu-id="bfa29-119">_Лпулсеарчстате_</span><span class="sxs-lookup"><span data-stu-id="bfa29-119">_lpulSearchState_</span></span>
  
> <span data-ttu-id="bfa29-120">вышли Указатель на битовую маску флагов, используемый для указания текущего состояния поиска.</span><span class="sxs-lookup"><span data-stu-id="bfa29-120">[out] A pointer to a bitmask of flags used to indicate the current state of the search.</span></span> <span data-ttu-id="bfa29-121">Если клиент передает значение NULL в параметр _лпулсеарчстате_ , **жетсеарчкритериа** не возвращает флагов.</span><span class="sxs-lookup"><span data-stu-id="bfa29-121">If a client passes NULL in the  _lpulSearchState_ parameter, **GetSearchCriteria** returns no flags.</span></span> <span data-ttu-id="bfa29-122">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="bfa29-122">The following flags can be set:</span></span> 
    
<span data-ttu-id="bfa29-123">СЕАРЧ_ФОРЕГРАУНД</span><span class="sxs-lookup"><span data-stu-id="bfa29-123">SEARCH_FOREGROUND</span></span> 
  
> <span data-ttu-id="bfa29-124">Поиск должен выполняться с высоким приоритетом, связанным с другими поисковыми операциями.</span><span class="sxs-lookup"><span data-stu-id="bfa29-124">The search should run at high priority relative to other searches.</span></span> <span data-ttu-id="bfa29-125">Если этот флаг не установлен, поиск выполняется с нормальным приоритетом относительно других поисков.</span><span class="sxs-lookup"><span data-stu-id="bfa29-125">If this flag is not set, the search runs at normal priority relative to other searches.</span></span>
    
<span data-ttu-id="bfa29-126">СЕАРЧ_РЕБУИЛД</span><span class="sxs-lookup"><span data-stu-id="bfa29-126">SEARCH_REBUILD</span></span> 
  
> <span data-ttu-id="bfa29-127">Поиск выполняется в режиме интенсивного использования ЦП для операции, пытаясь найти сообщения, соответствующие условиям.</span><span class="sxs-lookup"><span data-stu-id="bfa29-127">The search is in the CPU-intensive mode of its operation, trying to locate messages that match the criteria.</span></span> <span data-ttu-id="bfa29-128">Если этот флаг не установлен, часть операции поиска, интенсивно использующая ЦП, превышает.</span><span class="sxs-lookup"><span data-stu-id="bfa29-128">If this flag is not set, the CPU-intensive part of the search's operation is over.</span></span> <span data-ttu-id="bfa29-129">Этот флаг имеет значение только в том случае, если активен Поиск (то есть, если установлен флаг СЕАРЧ_РУННИНГ).</span><span class="sxs-lookup"><span data-stu-id="bfa29-129">This flag has meaning only if the search is active (that is, if the SEARCH_RUNNING flag is set).</span></span>
    
<span data-ttu-id="bfa29-130">СЕАРЧ_РЕКУРСИВЕ</span><span class="sxs-lookup"><span data-stu-id="bfa29-130">SEARCH_RECURSIVE</span></span> 
  
> <span data-ttu-id="bfa29-131">Поиск выполняется в указанных контейнерах и всех дочерних контейнерах для соответствующих записей.</span><span class="sxs-lookup"><span data-stu-id="bfa29-131">The search is looking in specified containers and all their child containers for matching entries.</span></span> <span data-ttu-id="bfa29-132">Если этот флаг не задан, поиск выполняется только для контейнеров, явно включенных в последний вызов метода [IMAPIContainer:: сетсеарчкритериа](imapicontainer-setsearchcriteria.md) .</span><span class="sxs-lookup"><span data-stu-id="bfa29-132">If this flag is not set, only the containers explicitly included in the last call to the [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method are being searched.</span></span> 
    
<span data-ttu-id="bfa29-133">СЕАРЧ_РУННИНГ</span><span class="sxs-lookup"><span data-stu-id="bfa29-133">SEARCH_RUNNING</span></span> 
  
> <span data-ttu-id="bfa29-134">Поиск активен, и таблица содержимого контейнера обновляется в соответствии с изменениями, внесенными в хранилище сообщений или адресную книгу.</span><span class="sxs-lookup"><span data-stu-id="bfa29-134">The search is active and the container's contents table is being updated to reflect changes in the message store or address book.</span></span> <span data-ttu-id="bfa29-135">Если этот флаг не установлен, поиск является неактивным и таблица содержимого является статической.</span><span class="sxs-lookup"><span data-stu-id="bfa29-135">If this flag is not set, the search is inactive and the contents table is static.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="bfa29-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bfa29-136">Return value</span></span>

<span data-ttu-id="bfa29-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="bfa29-137">S_OK</span></span> 
  
> <span data-ttu-id="bfa29-138">Условия поиска успешно получены.</span><span class="sxs-lookup"><span data-stu-id="bfa29-138">The search criteria was successfully obtained.</span></span>
    
<span data-ttu-id="bfa29-139">МАПИ_Е_БАД_ЧАРВИДС</span><span class="sxs-lookup"><span data-stu-id="bfa29-139">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="bfa29-140">Установлен либо флаг МАПИ_УНИКОДЕ, либо реализация не поддерживает Юникод, или МАПИ_УНИКОДЕ не задано, а реализация поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="bfa29-140">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="bfa29-141">МАПИ_Е_НОТ_ИНИТИАЛИЗЕД</span><span class="sxs-lookup"><span data-stu-id="bfa29-141">MAPI_E_NOT_INITIALIZED</span></span> 
  
> <span data-ttu-id="bfa29-142">Условия поиска для контейнера никогда не были установлены.</span><span class="sxs-lookup"><span data-stu-id="bfa29-142">Search criteria were never established for the container.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bfa29-143">Примечания</span><span class="sxs-lookup"><span data-stu-id="bfa29-143">Remarks</span></span>

<span data-ttu-id="bfa29-144">Метод **IMAPIContainer:: жетсеарчкритериа** получает условия поиска для контейнера, поддерживающего Поиск, как правило, папка результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="bfa29-144">The **IMAPIContainer::GetSearchCriteria** method obtains the search criteria for a container that supports searches, typically a search-results folder.</span></span> <span data-ttu-id="bfa29-145">Вы создаете критерии поиска, вызывая метод контейнера **IMAPIContainer:: сетсеарчкритериа** .</span><span class="sxs-lookup"><span data-stu-id="bfa29-145">You create search criteria by calling a container's **IMAPIContainer::SetSearchCriteria** method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="bfa29-146">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="bfa29-146">Notes to implementers</span></span>

<span data-ttu-id="bfa29-147">Для контейнеров адресных книг может потребоваться поддержка **жетсеарчкритериа** только в том случае, если они предоставляют расширенные возможности поиска, связанные со свойством **пр_сеарч** ([PidTagSearch](pidtagsearch-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="bfa29-147">Address book containers may need to support **GetSearchCriteria** only if they provide the advanced search capabilities associated with the **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) property.</span></span> <span data-ttu-id="bfa29-148">Дополнительные сведения о том, как реализовать функцию расширенного поиска для контейнеров адресных книг, можно узнать в статье [Реализация расширенного](implementing-advanced-searching.md)поиска.</span><span class="sxs-lookup"><span data-stu-id="bfa29-148">For more information about how to implement the advanced search feature for address book containers, see [Implementing Advanced Searching](implementing-advanced-searching.md).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="bfa29-149">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="bfa29-149">Notes to callers</span></span>

<span data-ttu-id="bfa29-150">По завершении работы с структурами данных, на которые указывает параметр _лппрестриктион_ и _лппконтаинерлист_ , вызовите [мапифрибуффер](mapifreebuffer.md) один раз для каждой структуры, чтобы освободить их.</span><span class="sxs-lookup"><span data-stu-id="bfa29-150">When you are finished with the data structures pointed to by the  _lppRestriction_ and  _lppContainerList_ parameters, call [MAPIFreeBuffer](mapifreebuffer.md) once for each structure to be released.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="bfa29-151">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="bfa29-151">MFCMAPI reference</span></span>

<span data-ttu-id="bfa29-152">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="bfa29-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="bfa29-153">**Файл**</span><span class="sxs-lookup"><span data-stu-id="bfa29-153">**File**</span></span>|<span data-ttu-id="bfa29-154">**Функция**</span><span class="sxs-lookup"><span data-stu-id="bfa29-154">**Function**</span></span>|<span data-ttu-id="bfa29-155">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="bfa29-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bfa29-156">Хиерарчитабледлг. cpp</span><span class="sxs-lookup"><span data-stu-id="bfa29-156">HierarchyTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="bfa29-157">Чиерарчитабледлг:: Онедитсеарчкритериа</span><span class="sxs-lookup"><span data-stu-id="bfa29-157">CHierarchyTableDlg::OnEditSearchCriteria</span></span>  <br/> |<span data-ttu-id="bfa29-158">MFCMAPI использует метод **IMAPIContainer:: жетсеарчкритериа** для получения условий поиска из папки для отображения.</span><span class="sxs-lookup"><span data-stu-id="bfa29-158">MFCMAPI uses the **IMAPIContainer::GetSearchCriteria** method to obtain search criteria from a folder to display.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bfa29-159">См. также</span><span class="sxs-lookup"><span data-stu-id="bfa29-159">See also</span></span>



[<span data-ttu-id="bfa29-160">IMAPIContainer::SetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="bfa29-160">IMAPIContainer::SetSearchCriteria</span></span>](imapicontainer-setsearchcriteria.md)
  
[<span data-ttu-id="bfa29-161">IMAPIFolder::CreateFolder</span><span class="sxs-lookup"><span data-stu-id="bfa29-161">IMAPIFolder::CreateFolder</span></span>](imapifolder-createfolder.md)
  
[<span data-ttu-id="bfa29-162">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="bfa29-162">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="bfa29-163">Каноническое свойство PidTagSearch</span><span class="sxs-lookup"><span data-stu-id="bfa29-163">PidTagSearch Canonical Property</span></span>](pidtagsearch-canonical-property.md)
  
[<span data-ttu-id="bfa29-164">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="bfa29-164">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


[<span data-ttu-id="bfa29-165">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="bfa29-165">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

