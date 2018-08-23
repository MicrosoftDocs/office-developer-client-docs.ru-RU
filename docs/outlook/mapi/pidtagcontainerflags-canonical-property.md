---
title: Каноническое свойство PidTagContainerFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContainerFlags
api_type:
- HeaderDef
ms.assetid: 66b8d333-227e-464d-8cf9-cd8a5ff15efb
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b62fc62bb9232b7106019fca82f502221e50bad0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583563"
---
# <a name="pidtagcontainerflags-canonical-property"></a><span data-ttu-id="3d3cd-103">Каноническое свойство PidTagContainerFlags</span><span class="sxs-lookup"><span data-stu-id="3d3cd-103">PidTagContainerFlags Canonical Property</span></span>

  
  
<span data-ttu-id="3d3cd-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3d3cd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3d3cd-105">Содержит битовую маску флаги, описывающие возможности контейнер адресной книги.</span><span class="sxs-lookup"><span data-stu-id="3d3cd-105">Contains a bitmask of flags describing capabilities of an address book container.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3d3cd-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="3d3cd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3d3cd-107">PR_CONTAINER_FLAGS</span><span class="sxs-lookup"><span data-stu-id="3d3cd-107">PR_CONTAINER_FLAGS</span></span>  <br/> |
|<span data-ttu-id="3d3cd-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="3d3cd-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3d3cd-109">0x3600</span><span class="sxs-lookup"><span data-stu-id="3d3cd-109">0x3600</span></span>  <br/> |
|<span data-ttu-id="3d3cd-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="3d3cd-110">Data type:</span></span>  <br/> |<span data-ttu-id="3d3cd-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="3d3cd-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="3d3cd-112">Область:</span><span class="sxs-lookup"><span data-stu-id="3d3cd-112">Area:</span></span>  <br/> |<span data-ttu-id="3d3cd-113">Адресная книга</span><span class="sxs-lookup"><span data-stu-id="3d3cd-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3d3cd-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="3d3cd-114">Remarks</span></span>

<span data-ttu-id="3d3cd-115">Для Битовая маска, которая может быть установлено одно или несколько из следующих флагов:</span><span class="sxs-lookup"><span data-stu-id="3d3cd-115">One or more of the following flags can be set for the bitmask:</span></span>
  
<span data-ttu-id="3d3cd-116">AB_FIND_ON_OPEN</span><span class="sxs-lookup"><span data-stu-id="3d3cd-116">AB_FIND_ON_OPEN</span></span> 
  
> <span data-ttu-id="3d3cd-117">Отображает диалоговое окно для запроса ограничение перед отображением любое содержимое контейнера.</span><span class="sxs-lookup"><span data-stu-id="3d3cd-117">Displays a dialog box to request a restriction before displaying any contents of the container.</span></span> 
    
<span data-ttu-id="3d3cd-118">AB_MODIFIABLE</span><span class="sxs-lookup"><span data-stu-id="3d3cd-118">AB_MODIFIABLE</span></span> 
  
> <span data-ttu-id="3d3cd-119">Записи могут быть добавлены в и удаляется из контейнера.</span><span class="sxs-lookup"><span data-stu-id="3d3cd-119">Entries can be added to and removed from the container.</span></span> <span data-ttu-id="3d3cd-120">Этот флаг указывает, можно ли изменить все записи из контейнера.</span><span class="sxs-lookup"><span data-stu-id="3d3cd-120">This flag does not indicate whether any entries in the container can be modified.</span></span>
    
<span data-ttu-id="3d3cd-121">AB_RECIPIENTS</span><span class="sxs-lookup"><span data-stu-id="3d3cd-121">AB_RECIPIENTS</span></span> 
  
> <span data-ttu-id="3d3cd-122">Получатели может содержаться в контейнере.</span><span class="sxs-lookup"><span data-stu-id="3d3cd-122">The container can hold recipients.</span></span> <span data-ttu-id="3d3cd-123">Этот флаг указывает, ли все получатели действительно присутствует в контейнере или ли они могут добавлять или удалять.</span><span class="sxs-lookup"><span data-stu-id="3d3cd-123">This flag does not indicate whether any recipients are actually present in the container, or whether they can be added or removed.</span></span> 
    
<span data-ttu-id="3d3cd-124">AB_SUBCONTAINERS</span><span class="sxs-lookup"><span data-stu-id="3d3cd-124">AB_SUBCONTAINERS</span></span> 
  
> <span data-ttu-id="3d3cd-125">Контейнер может содержать дочерних контейнеров.</span><span class="sxs-lookup"><span data-stu-id="3d3cd-125">The container can hold child containers.</span></span> <span data-ttu-id="3d3cd-126">Этот флаг не указывает, являются ли все подконтейнеры действительно присутствует в контейнере, а также является ли они могут добавлять или удалять.</span><span class="sxs-lookup"><span data-stu-id="3d3cd-126">This flag does not indicate whether any subcontainers are actually present in the container, nor whether they can be added or removed.</span></span> <span data-ttu-id="3d3cd-127">AB_SUBCONTAINERS должен иметь значение для контейнера для поддержки [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md).</span><span class="sxs-lookup"><span data-stu-id="3d3cd-127">AB_SUBCONTAINERS must be set for the container to support [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md).</span></span> 
    
<span data-ttu-id="3d3cd-128">AB_UNMODIFIABLE</span><span class="sxs-lookup"><span data-stu-id="3d3cd-128">AB_UNMODIFIABLE</span></span> 
  
> <span data-ttu-id="3d3cd-129">Невозможно добавить для записи или удаляется из контейнера.</span><span class="sxs-lookup"><span data-stu-id="3d3cd-129">Entries cannot be added to or removed from the container.</span></span> <span data-ttu-id="3d3cd-130">Этот флаг указывает, можно ли изменить все записи из контейнера.</span><span class="sxs-lookup"><span data-stu-id="3d3cd-130">This flag does not indicate whether any entries in the container can be modified.</span></span> 
    
<span data-ttu-id="3d3cd-131">Флаг AB_FIND_ON_OPEN настоятельно рекомендуется для контейнеры, используемые с Интернет-служб или медленных подключений к серверам.</span><span class="sxs-lookup"><span data-stu-id="3d3cd-131">The AB_FIND_ON_OPEN flag is highly recommended for containers used with online services or with slow connections to servers.</span></span> <span data-ttu-id="3d3cd-132">При открытии контейнера, который имеет значение AB_FIND_ON_OPEN, диалоговое окно **Найти** представлены пользователю для ограничения отображаемых пользователи обмена мгновенными сообщениями.</span><span class="sxs-lookup"><span data-stu-id="3d3cd-132">When a container is opened that has AB_FIND_ON_OPEN set, a **Find** dialog box is presented to the user to restrict the displayed messaging users.</span></span> <span data-ttu-id="3d3cd-133">Даже частичное спецификацию ограничение числа пользователей, обмена мгновенными сообщениями можно значительно ускорить отображения содержимого.</span><span class="sxs-lookup"><span data-stu-id="3d3cd-133">Even a partial specification limiting the messaging users can dramatically speed up a display of the contents.</span></span> 
  
<span data-ttu-id="3d3cd-134">Должен быть установлен флаг AB_MODIFIABLE или AB_UNMODIFIABLE.</span><span class="sxs-lookup"><span data-stu-id="3d3cd-134">Either the AB_MODIFIABLE or AB_UNMODIFIABLE flag must be set.</span></span> <span data-ttu-id="3d3cd-135">Чтобы указать, что контейнер не знает ли его можно изменить или нет, например, если изменения зависит от прав доступа можно задать обоих флагов.</span><span class="sxs-lookup"><span data-stu-id="3d3cd-135">Both flags can be set to indicate that the container does not know whether it can be modified or not, for example if modification depends on the user's access rights.</span></span> <span data-ttu-id="3d3cd-136">В этом случае клиентского приложения должен попытаться звонка и проанализировать код возврата для определения возможности контейнера.</span><span class="sxs-lookup"><span data-stu-id="3d3cd-136">In this case, a client application must attempt a call and examine the return code to determine the container's capabilities.</span></span> <span data-ttu-id="3d3cd-137">Клиент обычно начинает проверять AB_MODIFIABLE.</span><span class="sxs-lookup"><span data-stu-id="3d3cd-137">A client typically starts by examining AB_MODIFIABLE.</span></span> <span data-ttu-id="3d3cd-138">Если оно установлено, клиент вызывает метод, пытается изменить контейнер и проверяет возвращаемое значение.</span><span class="sxs-lookup"><span data-stu-id="3d3cd-138">If it is set, the client makes a call that attempts to modify the container and checks the return value.</span></span> 
  
<span data-ttu-id="3d3cd-139">Флаг AB_MODIFIABLE Указывает типы записей, которые могут быть добавлены в контейнер.</span><span class="sxs-lookup"><span data-stu-id="3d3cd-139">The AB_MODIFIABLE flag does not indicate what types of entries can be added to the container.</span></span> <span data-ttu-id="3d3cd-140">Для определения этого клиента следует использовать соответствующий метод [OpenProperty](imapiprop-openproperty.md) для открытия контейнера свойств **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="3d3cd-140">To determine this, the client should use the appropriate [OpenProperty](imapiprop-openproperty.md) method to open the container's **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property.</span></span> <span data-ttu-id="3d3cd-141">Открытие **PR_CREATE_TEMPLATES** причины раза контейнера таблицы должно быть возвращено список типов записей, которые могут быть созданы в контейнере.</span><span class="sxs-lookup"><span data-stu-id="3d3cd-141">Opening **PR_CREATE_TEMPLATES** causes the container's one-off table to be returned, listing the kinds of entries that can be created in the container.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="3d3cd-142">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="3d3cd-142">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3d3cd-143">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="3d3cd-143">Protocol specifications</span></span>

<span data-ttu-id="3d3cd-144">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3d3cd-144">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3d3cd-145">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="3d3cd-145">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3d3cd-146">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3d3cd-146">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3d3cd-147">Задает свойства и операции для списков пользователей, контактов, групп и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3d3cd-147">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="3d3cd-148">[[MS-NSPI]](http://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3d3cd-148">[[MS-NSPI]](http://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3d3cd-149">Обрабатывает клиентами с сервером интерфейса поставщика имя службы (NSPI).</span><span class="sxs-lookup"><span data-stu-id="3d3cd-149">Handles a client's communications with a Name Service Provider Interface (NSPI) server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3d3cd-150">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="3d3cd-150">Header files</span></span>

<span data-ttu-id="3d3cd-151">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3d3cd-151">Mapidefs.h</span></span>
  
> <span data-ttu-id="3d3cd-152">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="3d3cd-152">Provides data type definitions.</span></span>
    
<span data-ttu-id="3d3cd-153">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3d3cd-153">Mapitags.h</span></span>
  
> <span data-ttu-id="3d3cd-154">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="3d3cd-154">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3d3cd-155">См. также</span><span class="sxs-lookup"><span data-stu-id="3d3cd-155">See also</span></span>



[<span data-ttu-id="3d3cd-156">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="3d3cd-156">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3d3cd-157">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="3d3cd-157">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3d3cd-158">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="3d3cd-158">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3d3cd-159">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="3d3cd-159">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

