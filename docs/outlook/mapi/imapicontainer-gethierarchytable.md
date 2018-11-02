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
ms.openlocfilehash: 88b6f220f812f419b3f881aaa7f70a22186b589e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563802"
---
# <a name="imapicontainergethierarchytable"></a><span data-ttu-id="71bd9-103">IMAPIContainer::GetHierarchyTable</span><span class="sxs-lookup"><span data-stu-id="71bd9-103">IMAPIContainer::GetHierarchyTable</span></span>

  
  
<span data-ttu-id="71bd9-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="71bd9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="71bd9-105">Возвращает указатель на таблицу иерархии контейнера.</span><span class="sxs-lookup"><span data-stu-id="71bd9-105">Returns a pointer to the container's hierarchy table.</span></span>
  
```cpp
HRESULT GetHierarchyTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="71bd9-106">���������</span><span class="sxs-lookup"><span data-stu-id="71bd9-106">Parameters</span></span>

 <span data-ttu-id="71bd9-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="71bd9-107">_ulFlags_</span></span>
  
> <span data-ttu-id="71bd9-108">[in] Битовая маска флаги, который определяет, как возвращается информация в таблице.</span><span class="sxs-lookup"><span data-stu-id="71bd9-108">[in] A bitmask of flags that controls how information is returned in the table.</span></span> <span data-ttu-id="71bd9-109">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="71bd9-109">The following flags can be set:</span></span>
    
<span data-ttu-id="71bd9-110">CONVENIENT_DEPTH</span><span class="sxs-lookup"><span data-stu-id="71bd9-110">CONVENIENT_DEPTH</span></span> 
  
> <span data-ttu-id="71bd9-111">Заполнение таблицы иерархии контейнеров из нескольких уровней.</span><span class="sxs-lookup"><span data-stu-id="71bd9-111">Fills the hierarchy table with containers from multiple levels.</span></span> <span data-ttu-id="71bd9-112">Если CONVENIENT_DEPTH не установлен, в таблице иерархии содержит только дочерних контейнеров контейнера.</span><span class="sxs-lookup"><span data-stu-id="71bd9-112">If CONVENIENT_DEPTH is not set, the hierarchy table contains only the container's immediate child containers.</span></span>
    
<span data-ttu-id="71bd9-113">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="71bd9-113">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="71bd9-114">**GetHierarchyTable** может вернуть успешно, возможно перед таблице можно сделать доступной для вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="71bd9-114">**GetHierarchyTable** can return successfully, possibly before the table is made available to the caller.</span></span> <span data-ttu-id="71bd9-115">Если в таблице не поддерживается, вызов последующие таблицы может вызвать ошибку.</span><span class="sxs-lookup"><span data-stu-id="71bd9-115">If the table is not available, making a subsequent table call can raise an error.</span></span> 
    
<span data-ttu-id="71bd9-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="71bd9-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="71bd9-117">Запросы, которые столбцы, которые содержат строковые данные возвращаются в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="71bd9-117">Requests that the columns that contain string data be returned in Unicode format.</span></span> <span data-ttu-id="71bd9-118">Если флаг MAPI_UNICODE не установлен, строки должны возвращаться в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="71bd9-118">If the MAPI_UNICODE flag is not set, the strings should be returned in ANSI format.</span></span> 
    
<span data-ttu-id="71bd9-119">SHOW_SOFT_DELETES</span><span class="sxs-lookup"><span data-stu-id="71bd9-119">SHOW_SOFT_DELETES</span></span>
  
> <span data-ttu-id="71bd9-120">Отображает элементы, которые в настоящее время помечены как программных удалены, то есть, они находятся в хранения удаленных элементов этап времени.</span><span class="sxs-lookup"><span data-stu-id="71bd9-120">Shows items that are currently marked as soft deleted—that is, they are in the deleted item retention time phase.</span></span>
    
 <span data-ttu-id="71bd9-121">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="71bd9-121">_lppTable_</span></span>
  
> <span data-ttu-id="71bd9-122">[out] Указатель на указатель на таблицу иерархии.</span><span class="sxs-lookup"><span data-stu-id="71bd9-122">[out] A pointer to a pointer to the hierarchy table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="71bd9-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="71bd9-123">Return value</span></span>

<span data-ttu-id="71bd9-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="71bd9-124">S_OK</span></span> 
  
> <span data-ttu-id="71bd9-125">В таблице иерархии был успешно извлечен.</span><span class="sxs-lookup"><span data-stu-id="71bd9-125">The hierarchy table was successfully retrieved.</span></span>
    
<span data-ttu-id="71bd9-126">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="71bd9-126">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="71bd9-127">Либо был установлен флажок MAPI_UNICODE и реализация не поддерживает Юникод, или MAPI_UNICODE не было установлено и реализация поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="71bd9-127">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="71bd9-128">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="71bd9-128">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="71bd9-129">Контейнер имеет нет дочерних контейнеров и не могут предоставить таблицы иерархии.</span><span class="sxs-lookup"><span data-stu-id="71bd9-129">The container has no child containers and cannot provide a hierarchy table.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="71bd9-130">Примечания</span><span class="sxs-lookup"><span data-stu-id="71bd9-130">Remarks</span></span>

<span data-ttu-id="71bd9-131">Метод **IMAPIContainer::GetHierarchyTable** возвращает указатель в таблице иерархии контейнера.</span><span class="sxs-lookup"><span data-stu-id="71bd9-131">The **IMAPIContainer::GetHierarchyTable** method returns a pointer to the hierarchy table of a container.</span></span> <span data-ttu-id="71bd9-132">Таблица иерархии содержит сводную информацию о дочерних контейнеров в контейнере.</span><span class="sxs-lookup"><span data-stu-id="71bd9-132">A hierarchy table holds summary information about the child containers in the container.</span></span> <span data-ttu-id="71bd9-133">Таблиц иерархии папок хранения сведений о вложенных папок; таблиц иерархии адресной книги хранения сведений о дочерних контейнеров адресной книги и списки рассылки.</span><span class="sxs-lookup"><span data-stu-id="71bd9-133">Folder hierarchy tables hold information about subfolders; address book hierarchy tables hold information about child address book containers and distribution lists.</span></span> 
  
<span data-ttu-id="71bd9-134">Существует возможность для некоторых контейнеров иметь нет дочерних контейнеров.</span><span class="sxs-lookup"><span data-stu-id="71bd9-134">It is possible for some containers to have no child containers.</span></span> <span data-ttu-id="71bd9-135">Эти контейнеры возврата MAPI_E_NO_SUPPORT из их реализации **GetHierarchyTable**.</span><span class="sxs-lookup"><span data-stu-id="71bd9-135">These containers return MAPI_E_NO_SUPPORT from their implementations of **GetHierarchyTable**.</span></span>
  
<span data-ttu-id="71bd9-136">Если флаг CONVENIENT_DEPTH, каждой строки в таблице иерархии также включает свойство **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) в столбце.</span><span class="sxs-lookup"><span data-stu-id="71bd9-136">When the CONVENIENT_DEPTH flag is set, each row in the hierarchy table also includes the **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) property as a column.</span></span> <span data-ttu-id="71bd9-137">**PR_DEPTH** уровень каждого контейнера относительно контейнера, который реализует таблицы.</span><span class="sxs-lookup"><span data-stu-id="71bd9-137">**PR_DEPTH** indicates the level of each container relative to the container that implements the table.</span></span> <span data-ttu-id="71bd9-138">Реализации контейнер дочерних контейнеров выглядят с глубиной нулю, дочерних контейнеров в ноль глубины контейнеров, число уровней в одно и т. д.</span><span class="sxs-lookup"><span data-stu-id="71bd9-138">The implementing container's immediate child containers are at depth zero, child containers in the zero depth containers are at depth one, and so on.</span></span> <span data-ttu-id="71bd9-139">Последовательная увеличения значения **PR_DEPTH** как deepens иерархию уровней.</span><span class="sxs-lookup"><span data-stu-id="71bd9-139">The values of **PR_DEPTH** increase sequentially as the hierarchy of levels deepens.</span></span> 
  
<span data-ttu-id="71bd9-140">Полный список обязательные и дополнительные столбцы в таблицах иерархии [Таблиц иерархии](hierarchy-tables.md)см.</span><span class="sxs-lookup"><span data-stu-id="71bd9-140">For a complete list of required and optional columns in hierarchy tables, see [Hierarchy Tables](hierarchy-tables.md).</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="71bd9-141">Примечания для реализующих</span><span class="sxs-lookup"><span data-stu-id="71bd9-141">Notes to implementers</span></span>

<span data-ttu-id="71bd9-142">Если вы поддерживаете таблицы иерархии для контейнера, необходимо выполнить следующее:</span><span class="sxs-lookup"><span data-stu-id="71bd9-142">If you support a hierarchy table for your container, you must also do the following:</span></span>
  
- <span data-ttu-id="71bd9-143">Поддерживает вызов метода [IMAPIProp::OpenProperty](imapiprop-openproperty.md) контейнера для открытия свойство **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="71bd9-143">Support a call to the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="71bd9-144">Возвращает **PR_CONTAINER_HIERARCHY** в вызове методов [IMAPIProp::GetPropList](imapiprop-getproplist.md) или [IMAPIProp::GetProps](imapiprop-getprops.md) контейнера.</span><span class="sxs-lookup"><span data-stu-id="71bd9-144">Return **PR_CONTAINER_HIERARCHY** from a call to the container's [IMAPIProp::GetPropList](imapiprop-getproplist.md) or [IMAPIProp::GetProps](imapiprop-getprops.md) methods.</span></span> 
    
## <a name="notes-to-callers"></a><span data-ttu-id="71bd9-145">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="71bd9-145">Notes to callers</span></span>

<span data-ttu-id="71bd9-146">Строка и двоичный столбцов таблицы содержимое может быть усечен.</span><span class="sxs-lookup"><span data-stu-id="71bd9-146">String and binary contents table columns can be truncated.</span></span> <span data-ttu-id="71bd9-147">Как правило поставщики возвращать 255 символов.</span><span class="sxs-lookup"><span data-stu-id="71bd9-147">Typically, providers return 255 characters.</span></span> <span data-ttu-id="71bd9-148">Так как не известно, заранее ли таблицы включает в себя усеченных столбцы, предполагается, что столбец усекается, если длина столбца — 255 или 510 байт.</span><span class="sxs-lookup"><span data-stu-id="71bd9-148">Because you cannot know beforehand whether a table includes truncated columns, assume that a column is truncated if the length of the column is either 255 or 510 bytes.</span></span> <span data-ttu-id="71bd9-149">Всегда можно будет извлечь полное значение усеченных столбца, при необходимости непосредственно из объекта с помощью его идентификатор записи чтобы его открыть, затем вызвать метод [IMAPIProp::GetProps](imapiprop-getprops.md) .</span><span class="sxs-lookup"><span data-stu-id="71bd9-149">You can always retrieve the full value of a truncated column, if necessary, directly from the object by using its entry identifier to open it and then calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
  
<span data-ttu-id="71bd9-150">В зависимости от реализации поставщика, ограничения и операции сортировки можно применять к строку целиком или усеченных версии этой строки.</span><span class="sxs-lookup"><span data-stu-id="71bd9-150">Depending on the provider's implementation, restrictions and sorting operations can apply to the whole string or to the truncated version of that string.</span></span> <span data-ttu-id="71bd9-151">Кроме того поставщики хранилища не обязательно соблюдать набор порядок сортировки, который [SSortOrderSet](ssortorderset.md) , указанный для таблиц иерархии.</span><span class="sxs-lookup"><span data-stu-id="71bd9-151">Moreover, store providers are not guaranteed to honor the sort order set [SSortOrderSet](ssortorderset.md) specified for hierarchy tables.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="71bd9-152">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="71bd9-152">MFCMAPI reference</span></span>

<span data-ttu-id="71bd9-153">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="71bd9-153">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="71bd9-154">**Файл**</span><span class="sxs-lookup"><span data-stu-id="71bd9-154">**File**</span></span>|<span data-ttu-id="71bd9-155">**Функция**</span><span class="sxs-lookup"><span data-stu-id="71bd9-155">**Function**</span></span>|<span data-ttu-id="71bd9-156">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="71bd9-156">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="71bd9-157">HierarchyTableTreeCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="71bd9-157">HierarchyTableTreeCtrl.cpp</span></span>  <br/> |<span data-ttu-id="71bd9-158">CHierarchyTableTreeCtrl::GetHierarchyTable</span><span class="sxs-lookup"><span data-stu-id="71bd9-158">CHierarchyTableTreeCtrl::GetHierarchyTable</span></span>  <br/> |<span data-ttu-id="71bd9-159">Класс CHierarchyTableTreeCtrl **GetHierarchyTable** используется для получения таблиц иерархии для отображения в элементе управления дерева.</span><span class="sxs-lookup"><span data-stu-id="71bd9-159">The CHierarchyTableTreeCtrl class uses **GetHierarchyTable** to obtain hierarchy tables to display in a tree view control.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="71bd9-160">См. также</span><span class="sxs-lookup"><span data-stu-id="71bd9-160">See also</span></span>



[<span data-ttu-id="71bd9-161">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="71bd9-161">IMAPIProp::GetPropList</span></span>](imapiprop-getproplist.md)
  
[<span data-ttu-id="71bd9-162">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="71bd9-162">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="71bd9-163">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="71bd9-163">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="71bd9-164">Каноническое свойство PidTagContainerHierarchy</span><span class="sxs-lookup"><span data-stu-id="71bd9-164">PidTagContainerHierarchy Canonical Property</span></span>](pidtagcontainerhierarchy-canonical-property.md)
  
[<span data-ttu-id="71bd9-165">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="71bd9-165">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


[<span data-ttu-id="71bd9-166">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="71bd9-166">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

