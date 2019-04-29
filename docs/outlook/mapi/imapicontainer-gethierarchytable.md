---
title: Имапиконтаинержесиерарчитабле
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
# <a name="imapicontainergethierarchytable"></a><span data-ttu-id="dbb96-103">IMAPIContainer::GetHierarchyTable</span><span class="sxs-lookup"><span data-stu-id="dbb96-103">IMAPIContainer::GetHierarchyTable</span></span>

  
  
<span data-ttu-id="dbb96-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dbb96-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dbb96-105">Возвращает указатель на таблицу иерархии контейнера.</span><span class="sxs-lookup"><span data-stu-id="dbb96-105">Returns a pointer to the container's hierarchy table.</span></span>
  
```cpp
HRESULT GetHierarchyTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="dbb96-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="dbb96-106">Parameters</span></span>

 <span data-ttu-id="dbb96-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="dbb96-107">_ulFlags_</span></span>
  
> <span data-ttu-id="dbb96-108">возврата Битовая маска флагов, определяющих способ возвращения данных в таблице.</span><span class="sxs-lookup"><span data-stu-id="dbb96-108">[in] A bitmask of flags that controls how information is returned in the table.</span></span> <span data-ttu-id="dbb96-109">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="dbb96-109">The following flags can be set:</span></span>
    
<span data-ttu-id="dbb96-110">КОНВЕНИЕНТ_ДЕПС</span><span class="sxs-lookup"><span data-stu-id="dbb96-110">CONVENIENT_DEPTH</span></span> 
  
> <span data-ttu-id="dbb96-111">Заполняет таблицу иерархии контейнерами из нескольких уровней.</span><span class="sxs-lookup"><span data-stu-id="dbb96-111">Fills the hierarchy table with containers from multiple levels.</span></span> <span data-ttu-id="dbb96-112">Если КОНВЕНИЕНТ_ДЕПС не задано, таблица иерархии содержит только непосредственные дочерние контейнеры контейнера.</span><span class="sxs-lookup"><span data-stu-id="dbb96-112">If CONVENIENT_DEPTH is not set, the hierarchy table contains only the container's immediate child containers.</span></span>
    
<span data-ttu-id="dbb96-113">МАПИ_ДЕФЕРРЕД_ЕРРОРС</span><span class="sxs-lookup"><span data-stu-id="dbb96-113">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="dbb96-114">**Жесиерарчитабле** может успешно вернуть, возможно, перед тем, как таблица стала доступна вызывающему объекту.</span><span class="sxs-lookup"><span data-stu-id="dbb96-114">**GetHierarchyTable** can return successfully, possibly before the table is made available to the caller.</span></span> <span data-ttu-id="dbb96-115">Если таблица недоступна, выполнение последующих вызовов таблицы может вызвать ошибку.</span><span class="sxs-lookup"><span data-stu-id="dbb96-115">If the table is not available, making a subsequent table call can raise an error.</span></span> 
    
<span data-ttu-id="dbb96-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="dbb96-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="dbb96-117">ЗаПрашивает возврат столбцов, содержащих строковые данные, в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="dbb96-117">Requests that the columns that contain string data be returned in Unicode format.</span></span> <span data-ttu-id="dbb96-118">Если флаг МАПИ_УНИКОДЕ не установлен, строки должны быть возвращены в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="dbb96-118">If the MAPI_UNICODE flag is not set, the strings should be returned in ANSI format.</span></span> 
    
<span data-ttu-id="dbb96-119">SHOW_SOFT_DELETES</span><span class="sxs-lookup"><span data-stu-id="dbb96-119">SHOW_SOFT_DELETES</span></span>
  
> <span data-ttu-id="dbb96-120">Показывает элементы, которые в настоящее время помечены как обратимо удаленные — то есть они находятся на стадии хранения удаленных элементов.</span><span class="sxs-lookup"><span data-stu-id="dbb96-120">Shows items that are currently marked as soft deleted—that is, they are in the deleted item retention time phase.</span></span>
    
 <span data-ttu-id="dbb96-121">_Лпптабле_</span><span class="sxs-lookup"><span data-stu-id="dbb96-121">_lppTable_</span></span>
  
> <span data-ttu-id="dbb96-122">вышли Указатель на указатель на таблицу иерархии.</span><span class="sxs-lookup"><span data-stu-id="dbb96-122">[out] A pointer to a pointer to the hierarchy table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="dbb96-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dbb96-123">Return value</span></span>

<span data-ttu-id="dbb96-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="dbb96-124">S_OK</span></span> 
  
> <span data-ttu-id="dbb96-125">Таблица иерархии успешно получена.</span><span class="sxs-lookup"><span data-stu-id="dbb96-125">The hierarchy table was successfully retrieved.</span></span>
    
<span data-ttu-id="dbb96-126">МАПИ_Е_БАД_ЧАРВИДС</span><span class="sxs-lookup"><span data-stu-id="dbb96-126">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="dbb96-127">Установлен либо флаг МАПИ_УНИКОДЕ, либо реализация не поддерживает Юникод, или МАПИ_УНИКОДЕ не задано, а реализация поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="dbb96-127">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="dbb96-128">МАПИ_Е_НО_СУППОРТ</span><span class="sxs-lookup"><span data-stu-id="dbb96-128">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="dbb96-129">Контейнер не имеет дочерних контейнеров и не может предоставить таблицу иерархии.</span><span class="sxs-lookup"><span data-stu-id="dbb96-129">The container has no child containers and cannot provide a hierarchy table.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dbb96-130">Примечания</span><span class="sxs-lookup"><span data-stu-id="dbb96-130">Remarks</span></span>

<span data-ttu-id="dbb96-131">Метод **IMAPIContainer:: жесиерарчитабле** возвращает указатель на таблицу иерархии контейнера.</span><span class="sxs-lookup"><span data-stu-id="dbb96-131">The **IMAPIContainer::GetHierarchyTable** method returns a pointer to the hierarchy table of a container.</span></span> <span data-ttu-id="dbb96-132">В таблице иерархий содержатся сводные сведения о дочерних контейнерах в контейнере.</span><span class="sxs-lookup"><span data-stu-id="dbb96-132">A hierarchy table holds summary information about the child containers in the container.</span></span> <span data-ttu-id="dbb96-133">В таблицах иерархии папок хранятся сведения о вложенных папках; в таблицах иерархий адресной книги хранятся сведения о контейнерах дочерних адресных книг и списках рассылки.</span><span class="sxs-lookup"><span data-stu-id="dbb96-133">Folder hierarchy tables hold information about subfolders; address book hierarchy tables hold information about child address book containers and distribution lists.</span></span> 
  
<span data-ttu-id="dbb96-134">Некоторые контейнеры могут не иметь дочерних контейнеров.</span><span class="sxs-lookup"><span data-stu-id="dbb96-134">It is possible for some containers to have no child containers.</span></span> <span data-ttu-id="dbb96-135">Эти контейнеры возвращают МАПИ_Е_НО_СУППОРТ из реализации **жесиерарчитабле**.</span><span class="sxs-lookup"><span data-stu-id="dbb96-135">These containers return MAPI_E_NO_SUPPORT from their implementations of **GetHierarchyTable**.</span></span>
  
<span data-ttu-id="dbb96-136">Если установлен флаг КОНВЕНИЕНТ_ДЕПС, каждая строка в таблице иерархий также включает в себя свойство \*\*пр_депс\*\* ([PidTagDepth](pidtagdepth-canonical-property.md)) в виде столбца.</span><span class="sxs-lookup"><span data-stu-id="dbb96-136">When the CONVENIENT_DEPTH flag is set, each row in the hierarchy table also includes the **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) property as a column.</span></span> <span data-ttu-id="dbb96-137">**Пр_депс** указывает уровень каждого контейнера относительно контейнера, в котором реализуется таблица.</span><span class="sxs-lookup"><span data-stu-id="dbb96-137">**PR_DEPTH** indicates the level of each container relative to the container that implements the table.</span></span> <span data-ttu-id="dbb96-138">Непосредственные дочерние контейнеры реализующего контейнера имеют нулевую глубину, дочерние контейнеры в контейнерах нулевой глубины имеют глубину 1 и т. д.</span><span class="sxs-lookup"><span data-stu-id="dbb96-138">The implementing container's immediate child containers are at depth zero, child containers in the zero depth containers are at depth one, and so on.</span></span> <span data-ttu-id="dbb96-139">Значения **пр_депс** увеличиваются последовательно, как иерархия уровней Дипенс.</span><span class="sxs-lookup"><span data-stu-id="dbb96-139">The values of **PR_DEPTH** increase sequentially as the hierarchy of levels deepens.</span></span> 
  
<span data-ttu-id="dbb96-140">Полный список обязательных и необязательных столбцов в таблицах иерархий представлен в статье [иерархиЧеские таблицы](hierarchy-tables.md).</span><span class="sxs-lookup"><span data-stu-id="dbb96-140">For a complete list of required and optional columns in hierarchy tables, see [Hierarchy Tables](hierarchy-tables.md).</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="dbb96-141">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="dbb96-141">Notes to implementers</span></span>

<span data-ttu-id="dbb96-142">Если вы поддерживаете иерархию для контейнера, необходимо также выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="dbb96-142">If you support a hierarchy table for your container, you must also do the following:</span></span>
  
- <span data-ttu-id="dbb96-143">Поддерживает вызов метода контейнера [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) для открытия свойства **пр_контаинер_хиерарчи** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="dbb96-143">Support a call to the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="dbb96-144">Возвращает **пр_контаинер_хиерарчи** из вызова методов контейнера [IMAPIProp:: жетпроплист](imapiprop-getproplist.md) или [IMAPIProp::: PROPS](imapiprop-getprops.md) .</span><span class="sxs-lookup"><span data-stu-id="dbb96-144">Return **PR_CONTAINER_HIERARCHY** from a call to the container's [IMAPIProp::GetPropList](imapiprop-getproplist.md) or [IMAPIProp::GetProps](imapiprop-getprops.md) methods.</span></span> 
    
## <a name="notes-to-callers"></a><span data-ttu-id="dbb96-145">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="dbb96-145">Notes to callers</span></span>

<span data-ttu-id="dbb96-146">Столбцы таблицы строковых и двоичных содержимого можно усечь.</span><span class="sxs-lookup"><span data-stu-id="dbb96-146">String and binary contents table columns can be truncated.</span></span> <span data-ttu-id="dbb96-147">Как правило, поставщики возвращают 255 символов.</span><span class="sxs-lookup"><span data-stu-id="dbb96-147">Typically, providers return 255 characters.</span></span> <span data-ttu-id="dbb96-148">Так как вы не можете заранее узнать, содержит ли таблица усеченные столбцы, предположим, что столбец усекается, если длина столбца составляет 255 или 510 байт.</span><span class="sxs-lookup"><span data-stu-id="dbb96-148">Because you cannot know beforehand whether a table includes truncated columns, assume that a column is truncated if the length of the column is either 255 or 510 bytes.</span></span> <span data-ttu-id="dbb96-149">Вы всегда можете получить полное значение сокращенного столбца (при необходимости) непосредственно из объекта, используя его идентификатор записи, чтобы открыть его, а затем вызвать метод [IMAPIProp::](imapiprop-getprops.md) /PROPS.</span><span class="sxs-lookup"><span data-stu-id="dbb96-149">You can always retrieve the full value of a truncated column, if necessary, directly from the object by using its entry identifier to open it and then calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
  
<span data-ttu-id="dbb96-150">В зависимости от реализации поставщика, ограничения и операции сортировки можно применить ко всей строке или к усеченной версии этой строки.</span><span class="sxs-lookup"><span data-stu-id="dbb96-150">Depending on the provider's implementation, restrictions and sorting operations can apply to the whole string or to the truncated version of that string.</span></span> <span data-ttu-id="dbb96-151">Кроме того, поставщики хранилища не гарантируют соблюдение порядка сортировки [ссортордерсет](ssortorderset.md) , указанного для таблиц иерархии.</span><span class="sxs-lookup"><span data-stu-id="dbb96-151">Moreover, store providers are not guaranteed to honor the sort order set [SSortOrderSet](ssortorderset.md) specified for hierarchy tables.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="dbb96-152">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="dbb96-152">MFCMAPI reference</span></span>

<span data-ttu-id="dbb96-153">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="dbb96-153">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="dbb96-154">**Файл**</span><span class="sxs-lookup"><span data-stu-id="dbb96-154">**File**</span></span>|<span data-ttu-id="dbb96-155">**Функция**</span><span class="sxs-lookup"><span data-stu-id="dbb96-155">**Function**</span></span>|<span data-ttu-id="dbb96-156">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="dbb96-156">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="dbb96-157">Хиерарчитаблетриктрл. cpp</span><span class="sxs-lookup"><span data-stu-id="dbb96-157">HierarchyTableTreeCtrl.cpp</span></span>  <br/> |<span data-ttu-id="dbb96-158">Чиерарчитаблетриктрл:: Жесиерарчитабле</span><span class="sxs-lookup"><span data-stu-id="dbb96-158">CHierarchyTableTreeCtrl::GetHierarchyTable</span></span>  <br/> |<span data-ttu-id="dbb96-159">Класс Чиерарчитаблетриктрл использует **жесиерарчитабле** для получения таблиц иерархии для отображения в элементе управления представлением в виде дерева.</span><span class="sxs-lookup"><span data-stu-id="dbb96-159">The CHierarchyTableTreeCtrl class uses **GetHierarchyTable** to obtain hierarchy tables to display in a tree view control.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dbb96-160">См. также</span><span class="sxs-lookup"><span data-stu-id="dbb96-160">See also</span></span>



[<span data-ttu-id="dbb96-161">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="dbb96-161">IMAPIProp::GetPropList</span></span>](imapiprop-getproplist.md)
  
[<span data-ttu-id="dbb96-162">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="dbb96-162">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="dbb96-163">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="dbb96-163">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="dbb96-164">Каноническое свойство PidTagContainerHierarchy</span><span class="sxs-lookup"><span data-stu-id="dbb96-164">PidTagContainerHierarchy Canonical Property</span></span>](pidtagcontainerhierarchy-canonical-property.md)
  
[<span data-ttu-id="dbb96-165">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="dbb96-165">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


[<span data-ttu-id="dbb96-166">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="dbb96-166">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

