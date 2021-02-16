---
title: IMAPIContainerGetHierarchyTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer.GetHierarchyTable
api_type:
- COM
ms.assetid: d0c54092-86a3-47e0-8133-72e119e74b65
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: efc7f7a2fa703004afe361d766e0209ba40ffe46
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426200"
---
# <a name="imapicontainergethierarchytable"></a><span data-ttu-id="b6c3c-103">IMAPIContainer::GetHierarchyTable</span><span class="sxs-lookup"><span data-stu-id="b6c3c-103">IMAPIContainer::GetHierarchyTable</span></span>

  
  
<span data-ttu-id="b6c3c-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b6c3c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b6c3c-105">Возвращает указатель на таблицу иерархии контейнера.</span><span class="sxs-lookup"><span data-stu-id="b6c3c-105">Returns a pointer to the container's hierarchy table.</span></span>
  
```cpp
HRESULT GetHierarchyTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="b6c3c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b6c3c-106">Parameters</span></span>

 <span data-ttu-id="b6c3c-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b6c3c-107">_ulFlags_</span></span>
  
> <span data-ttu-id="b6c3c-108">[in] Битоваяmas флагов, которая управляет тем, как информация возвращается в таблице.</span><span class="sxs-lookup"><span data-stu-id="b6c3c-108">[in] A bitmask of flags that controls how information is returned in the table.</span></span> <span data-ttu-id="b6c3c-109">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="b6c3c-109">The following flags can be set:</span></span>
    
<span data-ttu-id="b6c3c-110">CONVENIENT_DEPTH</span><span class="sxs-lookup"><span data-stu-id="b6c3c-110">CONVENIENT_DEPTH</span></span> 
  
> <span data-ttu-id="b6c3c-111">Заполняет таблицу иерархии контейнерами из нескольких уровней.</span><span class="sxs-lookup"><span data-stu-id="b6c3c-111">Fills the hierarchy table with containers from multiple levels.</span></span> <span data-ttu-id="b6c3c-112">Если CONVENIENT_DEPTH не установлено, таблица иерархии содержит только непосредственные юные контейнеры контейнера.</span><span class="sxs-lookup"><span data-stu-id="b6c3c-112">If CONVENIENT_DEPTH is not set, the hierarchy table contains only the container's immediate child containers.</span></span>
    
<span data-ttu-id="b6c3c-113">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="b6c3c-113">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="b6c3c-114">**GetHierarchyTable** может успешно вернуться, возможно, до того, как таблица будет доступна вызываемой.</span><span class="sxs-lookup"><span data-stu-id="b6c3c-114">**GetHierarchyTable** can return successfully, possibly before the table is made available to the caller.</span></span> <span data-ttu-id="b6c3c-115">Если таблица недоступна, последующий вызов таблицы может вызвать ошибку.</span><span class="sxs-lookup"><span data-stu-id="b6c3c-115">If the table is not available, making a subsequent table call can raise an error.</span></span> 
    
<span data-ttu-id="b6c3c-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b6c3c-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="b6c3c-117">Запрашивает, чтобы столбцы, содержащие строку данных, возвращались в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="b6c3c-117">Requests that the columns that contain string data be returned in Unicode format.</span></span> <span data-ttu-id="b6c3c-118">Если флаг MAPI_UNICODE не установлен, строки должны возвращаться в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="b6c3c-118">If the MAPI_UNICODE flag is not set, the strings should be returned in ANSI format.</span></span> 
    
<span data-ttu-id="b6c3c-119">SHOW_SOFT_DELETES</span><span class="sxs-lookup"><span data-stu-id="b6c3c-119">SHOW_SOFT_DELETES</span></span>
  
> <span data-ttu-id="b6c3c-120">Отображает элементы, которые в настоящее время помечены как "мягко удаленные", то есть находятся на этапе хранения удаленных элементов.</span><span class="sxs-lookup"><span data-stu-id="b6c3c-120">Shows items that are currently marked as soft deleted—that is, they are in the deleted item retention time phase.</span></span>
    
 <span data-ttu-id="b6c3c-121">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="b6c3c-121">_lppTable_</span></span>
  
> <span data-ttu-id="b6c3c-122">[out] Указатель на указатель на таблицу иерархии.</span><span class="sxs-lookup"><span data-stu-id="b6c3c-122">[out] A pointer to a pointer to the hierarchy table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b6c3c-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b6c3c-123">Return value</span></span>

<span data-ttu-id="b6c3c-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="b6c3c-124">S_OK</span></span> 
  
> <span data-ttu-id="b6c3c-125">Таблица иерархии успешно извлечена.</span><span class="sxs-lookup"><span data-stu-id="b6c3c-125">The hierarchy table was successfully retrieved.</span></span>
    
<span data-ttu-id="b6c3c-126">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="b6c3c-126">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="b6c3c-127">Либо флаг MAPI_UNICODE установлен, а реализация не поддерживает Юникод, либо MAPI_UNICODE не установлен, а реализация поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="b6c3c-127">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="b6c3c-128">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="b6c3c-128">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="b6c3c-129">Контейнер не имеет child containers и не может предоставить таблицу иерархии.</span><span class="sxs-lookup"><span data-stu-id="b6c3c-129">The container has no child containers and cannot provide a hierarchy table.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b6c3c-130">Примечания</span><span class="sxs-lookup"><span data-stu-id="b6c3c-130">Remarks</span></span>

<span data-ttu-id="b6c3c-131">Метод **IMAPIContainer::GetHierarchyTable** возвращает указатель на таблицу иерархии контейнера.</span><span class="sxs-lookup"><span data-stu-id="b6c3c-131">The **IMAPIContainer::GetHierarchyTable** method returns a pointer to the hierarchy table of a container.</span></span> <span data-ttu-id="b6c3c-132">В таблице иерархии содержится сводная информация о child containers в контейнере.</span><span class="sxs-lookup"><span data-stu-id="b6c3c-132">A hierarchy table holds summary information about the child containers in the container.</span></span> <span data-ttu-id="b6c3c-133">В таблицах иерархии папок есть сведения о вложенных папках; В таблицах иерархии адресных книг содержится информация о контейнерах адресных книг и списках рассылки.</span><span class="sxs-lookup"><span data-stu-id="b6c3c-133">Folder hierarchy tables hold information about subfolders; address book hierarchy tables hold information about child address book containers and distribution lists.</span></span> 
  
<span data-ttu-id="b6c3c-134">У некоторых контейнеров может не быть никаких child-контейнеров.</span><span class="sxs-lookup"><span data-stu-id="b6c3c-134">It is possible for some containers to have no child containers.</span></span> <span data-ttu-id="b6c3c-135">Эти контейнеры MAPI_E_NO_SUPPORT из своих реализаций **GetHierarchyTable.**</span><span class="sxs-lookup"><span data-stu-id="b6c3c-135">These containers return MAPI_E_NO_SUPPORT from their implementations of **GetHierarchyTable**.</span></span>
  
<span data-ttu-id="b6c3c-136">При CONVENIENT_DEPTH флага каждая строка в таблице иерархии также включает свойство **PR_DEPTH** ([PidTagDepth)](pidtagdepth-canonical-property.md)в качестве столбца.</span><span class="sxs-lookup"><span data-stu-id="b6c3c-136">When the CONVENIENT_DEPTH flag is set, each row in the hierarchy table also includes the **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) property as a column.</span></span> <span data-ttu-id="b6c3c-137">**PR_DEPTH** указывает уровень каждого контейнера относительно контейнера, который реализует таблицу.</span><span class="sxs-lookup"><span data-stu-id="b6c3c-137">**PR_DEPTH** indicates the level of each container relative to the container that implements the table.</span></span> <span data-ttu-id="b6c3c-138">Непосредственные потомки контейнера реализующих контейнеров находятся на нулевой глубине, контейнеры-потомки в контейнерах нулевой глубины находятся на глубине 1 и так далее.</span><span class="sxs-lookup"><span data-stu-id="b6c3c-138">The implementing container's immediate child containers are at depth zero, child containers in the zero depth containers are at depth one, and so on.</span></span> <span data-ttu-id="b6c3c-139">Значения PR_DEPTH **последовательно** увеличиваются по мере углубления иерархии уровней.</span><span class="sxs-lookup"><span data-stu-id="b6c3c-139">The values of **PR_DEPTH** increase sequentially as the hierarchy of levels deepens.</span></span> 
  
<span data-ttu-id="b6c3c-140">Полный список необходимых и необязательных столбцов в таблицах иерархии см. в [статье "Таблицы иерархии".](hierarchy-tables.md)</span><span class="sxs-lookup"><span data-stu-id="b6c3c-140">For a complete list of required and optional columns in hierarchy tables, see [Hierarchy Tables](hierarchy-tables.md).</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="b6c3c-141">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="b6c3c-141">Notes to implementers</span></span>

<span data-ttu-id="b6c3c-142">Если вы поддерживаете таблицу иерархии для контейнера, необходимо также сделать следующее:</span><span class="sxs-lookup"><span data-stu-id="b6c3c-142">If you support a hierarchy table for your container, you must also do the following:</span></span>
  
- <span data-ttu-id="b6c3c-143">Поддержка вызова метода [IMAPIProp::OpenProperty](imapiprop-openproperty.md) контейнера для открытия **свойства PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy).](pidtagcontainerhierarchy-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="b6c3c-143">Support a call to the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="b6c3c-144">Возвращает **PR_CONTAINER_HIERARCHY** из вызова методов [IMAPIProp::GetPropList](imapiprop-getproplist.md) или [IMAPIProp::GetProps](imapiprop-getprops.md) контейнера.</span><span class="sxs-lookup"><span data-stu-id="b6c3c-144">Return **PR_CONTAINER_HIERARCHY** from a call to the container's [IMAPIProp::GetPropList](imapiprop-getproplist.md) or [IMAPIProp::GetProps](imapiprop-getprops.md) methods.</span></span> 
    
## <a name="notes-to-callers"></a><span data-ttu-id="b6c3c-145">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="b6c3c-145">Notes to callers</span></span>

<span data-ttu-id="b6c3c-146">Строки и столбцы таблицы двоичного содержимого можно усечены.</span><span class="sxs-lookup"><span data-stu-id="b6c3c-146">String and binary contents table columns can be truncated.</span></span> <span data-ttu-id="b6c3c-147">Обычно поставщики возвращают 255 символов.</span><span class="sxs-lookup"><span data-stu-id="b6c3c-147">Typically, providers return 255 characters.</span></span> <span data-ttu-id="b6c3c-148">Так как вы не можете заранее узнать, содержит ли таблица усеченные столбцы, предположим, что столбец усечен, если длина столбца составляет 255 или 510 bytes.</span><span class="sxs-lookup"><span data-stu-id="b6c3c-148">Because you cannot know beforehand whether a table includes truncated columns, assume that a column is truncated if the length of the column is either 255 or 510 bytes.</span></span> <span data-ttu-id="b6c3c-149">При необходимости вы всегда можете получить полное значение усеченного столбца непосредственно из объекта, используя идентификатор записи, чтобы открыть его, а затем вызывать метод [IMAPIProp::GetProps.](imapiprop-getprops.md)</span><span class="sxs-lookup"><span data-stu-id="b6c3c-149">You can always retrieve the full value of a truncated column, if necessary, directly from the object by using its entry identifier to open it and then calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
  
<span data-ttu-id="b6c3c-150">В зависимости от реализации поставщика ограничения и операции сортировки могут применяться к всей строке или к усеченной версии этой строки.</span><span class="sxs-lookup"><span data-stu-id="b6c3c-150">Depending on the provider's implementation, restrictions and sorting operations can apply to the whole string or to the truncated version of that string.</span></span> <span data-ttu-id="b6c3c-151">Кроме того, не гарантируется, что поставщики магазина будут соблюдать набор [сортировки SSortOrderSet,](ssortorderset.md) указанный для таблиц иерархии.</span><span class="sxs-lookup"><span data-stu-id="b6c3c-151">Moreover, store providers are not guaranteed to honor the sort order set [SSortOrderSet](ssortorderset.md) specified for hierarchy tables.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b6c3c-152">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="b6c3c-152">MFCMAPI reference</span></span>

<span data-ttu-id="b6c3c-153">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="b6c3c-153">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b6c3c-154">**Файл**</span><span class="sxs-lookup"><span data-stu-id="b6c3c-154">**File**</span></span>|<span data-ttu-id="b6c3c-155">**Функция**</span><span class="sxs-lookup"><span data-stu-id="b6c3c-155">**Function**</span></span>|<span data-ttu-id="b6c3c-156">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="b6c3c-156">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b6c3c-157">HierarchyTableTreeCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="b6c3c-157">HierarchyTableTreeCtrl.cpp</span></span>  <br/> |<span data-ttu-id="b6c3c-158">CHierarchyTableTreeCtrl::GetHierarchyTable</span><span class="sxs-lookup"><span data-stu-id="b6c3c-158">CHierarchyTableTreeCtrl::GetHierarchyTable</span></span>  <br/> |<span data-ttu-id="b6c3c-159">Класс CHierarchyTableTreeCtrl использует **GetHierarchyTable** для получения таблиц иерархии для отображения в иерархическом представлении.</span><span class="sxs-lookup"><span data-stu-id="b6c3c-159">The CHierarchyTableTreeCtrl class uses **GetHierarchyTable** to obtain hierarchy tables to display in a tree view control.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b6c3c-160">См. также</span><span class="sxs-lookup"><span data-stu-id="b6c3c-160">See also</span></span>



[<span data-ttu-id="b6c3c-161">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="b6c3c-161">IMAPIProp::GetPropList</span></span>](imapiprop-getproplist.md)
  
[<span data-ttu-id="b6c3c-162">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="b6c3c-162">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="b6c3c-163">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b6c3c-163">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="b6c3c-164">Каноническое свойство PidTagContainerHierarchy</span><span class="sxs-lookup"><span data-stu-id="b6c3c-164">PidTagContainerHierarchy Canonical Property</span></span>](pidtagcontainerhierarchy-canonical-property.md)
  
[<span data-ttu-id="b6c3c-165">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="b6c3c-165">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


[<span data-ttu-id="b6c3c-166">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="b6c3c-166">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

