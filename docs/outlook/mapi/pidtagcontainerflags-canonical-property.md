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
ms.openlocfilehash: c9c446097213e5b743a47ec32db17ec0afe63b78
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357549"
---
# <a name="pidtagcontainerflags-canonical-property"></a><span data-ttu-id="40ef1-103">Каноническое свойство PidTagContainerFlags</span><span class="sxs-lookup"><span data-stu-id="40ef1-103">PidTagContainerFlags Canonical Property</span></span>

  
  
<span data-ttu-id="40ef1-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="40ef1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="40ef1-105">Содержит битмаску флагов, описывающих возможности контейнера адресной книги.</span><span class="sxs-lookup"><span data-stu-id="40ef1-105">Contains a bitmask of flags describing capabilities of an address book container.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="40ef1-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="40ef1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="40ef1-107">PR_CONTAINER_FLAGS</span><span class="sxs-lookup"><span data-stu-id="40ef1-107">PR_CONTAINER_FLAGS</span></span>  <br/> |
|<span data-ttu-id="40ef1-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="40ef1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="40ef1-109">0x3600</span><span class="sxs-lookup"><span data-stu-id="40ef1-109">0x3600</span></span>  <br/> |
|<span data-ttu-id="40ef1-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="40ef1-110">Data type:</span></span>  <br/> |<span data-ttu-id="40ef1-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="40ef1-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="40ef1-112">Область:</span><span class="sxs-lookup"><span data-stu-id="40ef1-112">Area:</span></span>  <br/> |<span data-ttu-id="40ef1-113">Адресная книга</span><span class="sxs-lookup"><span data-stu-id="40ef1-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="40ef1-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="40ef1-114">Remarks</span></span>

<span data-ttu-id="40ef1-115">Для bitmask можно установить один или несколько следующих флагов:</span><span class="sxs-lookup"><span data-stu-id="40ef1-115">One or more of the following flags can be set for the bitmask:</span></span>
  
<span data-ttu-id="40ef1-116">AB_FIND_ON_OPEN</span><span class="sxs-lookup"><span data-stu-id="40ef1-116">AB_FIND_ON_OPEN</span></span> 
  
> <span data-ttu-id="40ef1-117">Отображает диалоговое окно для запроса ограничения перед отображением любого содержимого контейнера.</span><span class="sxs-lookup"><span data-stu-id="40ef1-117">Displays a dialog box to request a restriction before displaying any contents of the container.</span></span> 
    
<span data-ttu-id="40ef1-118">AB_MODIFIABLE</span><span class="sxs-lookup"><span data-stu-id="40ef1-118">AB_MODIFIABLE</span></span> 
  
> <span data-ttu-id="40ef1-119">Записи можно добавлять и удалять из контейнера.</span><span class="sxs-lookup"><span data-stu-id="40ef1-119">Entries can be added to and removed from the container.</span></span> <span data-ttu-id="40ef1-120">Этот флаг не указывает, можно ли изменять любые записи в контейнере.</span><span class="sxs-lookup"><span data-stu-id="40ef1-120">This flag does not indicate whether any entries in the container can be modified.</span></span>
    
<span data-ttu-id="40ef1-121">AB_RECIPIENTS</span><span class="sxs-lookup"><span data-stu-id="40ef1-121">AB_RECIPIENTS</span></span> 
  
> <span data-ttu-id="40ef1-122">Контейнер может удерживать получателей.</span><span class="sxs-lookup"><span data-stu-id="40ef1-122">The container can hold recipients.</span></span> <span data-ttu-id="40ef1-123">Этот флаг не указывает, действительно ли получатели присутствуют в контейнере и могут ли они быть добавлены или удалены.</span><span class="sxs-lookup"><span data-stu-id="40ef1-123">This flag does not indicate whether any recipients are actually present in the container, or whether they can be added or removed.</span></span> 
    
<span data-ttu-id="40ef1-124">AB_SUBCONTAINERS</span><span class="sxs-lookup"><span data-stu-id="40ef1-124">AB_SUBCONTAINERS</span></span> 
  
> <span data-ttu-id="40ef1-125">Контейнер может вметь детские контейнеры.</span><span class="sxs-lookup"><span data-stu-id="40ef1-125">The container can hold child containers.</span></span> <span data-ttu-id="40ef1-126">Этот флаг не указывает, присутствуют ли какие-либо подконтейеры в контейнере, а также могут ли они быть добавлены или удалены.</span><span class="sxs-lookup"><span data-stu-id="40ef1-126">This flag does not indicate whether any subcontainers are actually present in the container, nor whether they can be added or removed.</span></span> <span data-ttu-id="40ef1-127">AB_SUBCONTAINERS должен быть установлен для контейнера для [поддержки IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md).</span><span class="sxs-lookup"><span data-stu-id="40ef1-127">AB_SUBCONTAINERS must be set for the container to support [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md).</span></span> 
    
<span data-ttu-id="40ef1-128">AB_UNMODIFIABLE</span><span class="sxs-lookup"><span data-stu-id="40ef1-128">AB_UNMODIFIABLE</span></span> 
  
> <span data-ttu-id="40ef1-129">Записи не могут быть добавлены или удалены из контейнера.</span><span class="sxs-lookup"><span data-stu-id="40ef1-129">Entries cannot be added to or removed from the container.</span></span> <span data-ttu-id="40ef1-130">Этот флаг не указывает, можно ли изменять любые записи в контейнере.</span><span class="sxs-lookup"><span data-stu-id="40ef1-130">This flag does not indicate whether any entries in the container can be modified.</span></span> 
    
<span data-ttu-id="40ef1-131">Флаг AB_FIND_ON_OPEN рекомендуется использовать для контейнеров, используемых с онлайн-службами или с медленным подключением к серверам.</span><span class="sxs-lookup"><span data-stu-id="40ef1-131">The AB_FIND_ON_OPEN flag is highly recommended for containers used with online services or with slow connections to servers.</span></span> <span data-ttu-id="40ef1-132">При открываемом контейнере с AB_FIND_ON_OPEN установлен диалоговое окно **Find** представляется пользователю для ограничения отображаемого пользователя обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="40ef1-132">When a container is opened that has AB_FIND_ON_OPEN set, a **Find** dialog box is presented to the user to restrict the displayed messaging users.</span></span> <span data-ttu-id="40ef1-133">Даже частичная спецификация, ограничивающая пользователей обмена сообщениями, может значительно ускорить отображение содержимого.</span><span class="sxs-lookup"><span data-stu-id="40ef1-133">Even a partial specification limiting the messaging users can dramatically speed up a display of the contents.</span></span> 
  
<span data-ttu-id="40ef1-134">Должен быть AB_MODIFIABLE или AB_UNMODIFIABLE флаг.</span><span class="sxs-lookup"><span data-stu-id="40ef1-134">Either the AB_MODIFIABLE or AB_UNMODIFIABLE flag must be set.</span></span> <span data-ttu-id="40ef1-135">Оба флага могут указывать на то, что контейнер не знает, можно ли его изменить или нет, например, если изменение зависит от прав пользователя на доступ.</span><span class="sxs-lookup"><span data-stu-id="40ef1-135">Both flags can be set to indicate that the container does not know whether it can be modified or not, for example if modification depends on the user's access rights.</span></span> <span data-ttu-id="40ef1-136">В этом случае клиентские приложения должны попытаться вызвать и изучить код возврата, чтобы определить возможности контейнера.</span><span class="sxs-lookup"><span data-stu-id="40ef1-136">In this case, a client application must attempt a call and examine the return code to determine the container's capabilities.</span></span> <span data-ttu-id="40ef1-137">Клиент обычно начинает с изучения AB_MODIFIABLE.</span><span class="sxs-lookup"><span data-stu-id="40ef1-137">A client typically starts by examining AB_MODIFIABLE.</span></span> <span data-ttu-id="40ef1-138">Если она установлена, клиент совершает вызов, который пытается изменить контейнер и проверяет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="40ef1-138">If it is set, the client makes a call that attempts to modify the container and checks the return value.</span></span> 
  
<span data-ttu-id="40ef1-139">Флаг AB_MODIFIABLE не указывает, какие типы записей можно добавить в контейнер.</span><span class="sxs-lookup"><span data-stu-id="40ef1-139">The AB_MODIFIABLE flag does not indicate what types of entries can be added to the container.</span></span> <span data-ttu-id="40ef1-140">Чтобы определить это, клиент должен использовать соответствующий метод [OpenProperty,](imapiprop-openproperty.md) чтобы открыть свойство[PR_CREATE_TEMPLATES (PidTagCreateTemplates).](pidtagcreatetemplates-canonical-property.md) </span><span class="sxs-lookup"><span data-stu-id="40ef1-140">To determine this, the client should use the appropriate [OpenProperty](imapiprop-openproperty.md) method to open the container's **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property.</span></span> <span data-ttu-id="40ef1-141">Открытие **PR_CREATE_TEMPLATES** возвращает разовую таблицу контейнера, перечисляя типы записей, которые можно создать в контейнере.</span><span class="sxs-lookup"><span data-stu-id="40ef1-141">Opening **PR_CREATE_TEMPLATES** causes the container's one-off table to be returned, listing the kinds of entries that can be created in the container.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="40ef1-142">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="40ef1-142">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="40ef1-143">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="40ef1-143">Protocol specifications</span></span>

<span data-ttu-id="40ef1-144">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="40ef1-144">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="40ef1-145">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="40ef1-145">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="40ef1-146">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="40ef1-146">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="40ef1-147">Указывает свойства и операции для списков пользователей, контактов, групп и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="40ef1-147">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="40ef1-148">[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="40ef1-148">[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="40ef1-149">Обрабатывает сообщения клиента с сервером интерфейса поставщика служб имени (NSPI).</span><span class="sxs-lookup"><span data-stu-id="40ef1-149">Handles a client's communications with a Name Service Provider Interface (NSPI) server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="40ef1-150">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="40ef1-150">Header files</span></span>

<span data-ttu-id="40ef1-151">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="40ef1-151">Mapidefs.h</span></span>
  
> <span data-ttu-id="40ef1-152">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="40ef1-152">Provides data type definitions.</span></span>
    
<span data-ttu-id="40ef1-153">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="40ef1-153">Mapitags.h</span></span>
  
> <span data-ttu-id="40ef1-154">Содержит определения свойств, перечисленных в качестве связанных свойств.</span><span class="sxs-lookup"><span data-stu-id="40ef1-154">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="40ef1-155">См. также</span><span class="sxs-lookup"><span data-stu-id="40ef1-155">See also</span></span>



[<span data-ttu-id="40ef1-156">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="40ef1-156">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="40ef1-157">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="40ef1-157">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="40ef1-158">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="40ef1-158">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="40ef1-159">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="40ef1-159">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

