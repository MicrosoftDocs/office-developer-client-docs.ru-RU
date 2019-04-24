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
# <a name="pidtagcontainerflags-canonical-property"></a><span data-ttu-id="cc050-103">Каноническое свойство PidTagContainerFlags</span><span class="sxs-lookup"><span data-stu-id="cc050-103">PidTagContainerFlags Canonical Property</span></span>

  
  
<span data-ttu-id="cc050-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cc050-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cc050-105">Содержит битовую маску флагов, описывающих возможности контейнера адресной книги.</span><span class="sxs-lookup"><span data-stu-id="cc050-105">Contains a bitmask of flags describing capabilities of an address book container.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cc050-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="cc050-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cc050-107">ПР_КОНТАИНЕР_ФЛАГС</span><span class="sxs-lookup"><span data-stu-id="cc050-107">PR_CONTAINER_FLAGS</span></span>  <br/> |
|<span data-ttu-id="cc050-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="cc050-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cc050-109">0x3600</span><span class="sxs-lookup"><span data-stu-id="cc050-109">0x3600</span></span>  <br/> |
|<span data-ttu-id="cc050-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="cc050-110">Data type:</span></span>  <br/> |<span data-ttu-id="cc050-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="cc050-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="cc050-112">Область:</span><span class="sxs-lookup"><span data-stu-id="cc050-112">Area:</span></span>  <br/> |<span data-ttu-id="cc050-113">Адресная книга</span><span class="sxs-lookup"><span data-stu-id="cc050-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cc050-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="cc050-114">Remarks</span></span>

<span data-ttu-id="cc050-115">Для битовой маски можно задать один или несколько из следующих флагов:</span><span class="sxs-lookup"><span data-stu-id="cc050-115">One or more of the following flags can be set for the bitmask:</span></span>
  
<span data-ttu-id="cc050-116">АБ_ФИНД_ОН_ОПЕН</span><span class="sxs-lookup"><span data-stu-id="cc050-116">AB_FIND_ON_OPEN</span></span> 
  
> <span data-ttu-id="cc050-117">Отображает диалоговое окно, чтобы запрашивать ограничение перед отображением содержимого контейнера.</span><span class="sxs-lookup"><span data-stu-id="cc050-117">Displays a dialog box to request a restriction before displaying any contents of the container.</span></span> 
    
<span data-ttu-id="cc050-118">АБ_МОДИФИАБЛЕ</span><span class="sxs-lookup"><span data-stu-id="cc050-118">AB_MODIFIABLE</span></span> 
  
> <span data-ttu-id="cc050-119">Записи можно добавлять в контейнер и удалять из него.</span><span class="sxs-lookup"><span data-stu-id="cc050-119">Entries can be added to and removed from the container.</span></span> <span data-ttu-id="cc050-120">Этот флаг не указывает, можно ли изменять какие бы то ни было записи в контейнере.</span><span class="sxs-lookup"><span data-stu-id="cc050-120">This flag does not indicate whether any entries in the container can be modified.</span></span>
    
<span data-ttu-id="cc050-121">АБ_РЕЦИПИЕНТС</span><span class="sxs-lookup"><span data-stu-id="cc050-121">AB_RECIPIENTS</span></span> 
  
> <span data-ttu-id="cc050-122">В контейнере могут храниться получатели.</span><span class="sxs-lookup"><span data-stu-id="cc050-122">The container can hold recipients.</span></span> <span data-ttu-id="cc050-123">Этот флаг не указывает, присутствуют ли получатели в контейнере или они могут добавляться или удаляться.</span><span class="sxs-lookup"><span data-stu-id="cc050-123">This flag does not indicate whether any recipients are actually present in the container, or whether they can be added or removed.</span></span> 
    
<span data-ttu-id="cc050-124">АБ_СУБКОНТАИНЕРС</span><span class="sxs-lookup"><span data-stu-id="cc050-124">AB_SUBCONTAINERS</span></span> 
  
> <span data-ttu-id="cc050-125">В контейнере могут храниться дочерние контейнеры.</span><span class="sxs-lookup"><span data-stu-id="cc050-125">The container can hold child containers.</span></span> <span data-ttu-id="cc050-126">Этот флаг не указывает, присутствуют ли в контейнере подконтейнеры и могут ли они добавляться или удаляться.</span><span class="sxs-lookup"><span data-stu-id="cc050-126">This flag does not indicate whether any subcontainers are actually present in the container, nor whether they can be added or removed.</span></span> <span data-ttu-id="cc050-127">Чтобы контейнер поддерживал [IMAPIContainer:: жесиерарчитабле](imapicontainer-gethierarchytable.md), необходимо настроить аб_субконтаинерс.</span><span class="sxs-lookup"><span data-stu-id="cc050-127">AB_SUBCONTAINERS must be set for the container to support [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md).</span></span> 
    
<span data-ttu-id="cc050-128">АБ_УНМОДИФИАБЛЕ</span><span class="sxs-lookup"><span data-stu-id="cc050-128">AB_UNMODIFIABLE</span></span> 
  
> <span data-ttu-id="cc050-129">Записи нельзя добавлять в контейнер или удалять из него.</span><span class="sxs-lookup"><span data-stu-id="cc050-129">Entries cannot be added to or removed from the container.</span></span> <span data-ttu-id="cc050-130">Этот флаг не указывает, можно ли изменять какие бы то ни было записи в контейнере.</span><span class="sxs-lookup"><span data-stu-id="cc050-130">This flag does not indicate whether any entries in the container can be modified.</span></span> 
    
<span data-ttu-id="cc050-131">Флаг АБ_ФИНД_ОН_ОПЕН настоятельно рекомендуется для контейнеров, используемых в веб-службах или с медленными подключениями к серверам.</span><span class="sxs-lookup"><span data-stu-id="cc050-131">The AB_FIND_ON_OPEN flag is highly recommended for containers used with online services or with slow connections to servers.</span></span> <span data-ttu-id="cc050-132">При открытии контейнера, у которого есть набор АБ_ФИНД_ОН_ОПЕН, пользователю предлагается диалоговое окно **поиска** для ограничения отображаемых пользователей системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="cc050-132">When a container is opened that has AB_FIND_ON_OPEN set, a **Find** dialog box is presented to the user to restrict the displayed messaging users.</span></span> <span data-ttu-id="cc050-133">Даже частичная спецификация, ограничивающая пользователей обмена сообщениями, может значительно ускорить отображение содержимого.</span><span class="sxs-lookup"><span data-stu-id="cc050-133">Even a partial specification limiting the messaging users can dramatically speed up a display of the contents.</span></span> 
  
<span data-ttu-id="cc050-134">Должно быть задано значение флага АБ_МОДИФИАБЛЕ или АБ_УНМОДИФИАБЛЕ.</span><span class="sxs-lookup"><span data-stu-id="cc050-134">Either the AB_MODIFIABLE or AB_UNMODIFIABLE flag must be set.</span></span> <span data-ttu-id="cc050-135">Оба флага указывают на то, что контейнер не знает, можно ли его изменить или нет, например, если изменение зависит от прав доступа пользователя.</span><span class="sxs-lookup"><span data-stu-id="cc050-135">Both flags can be set to indicate that the container does not know whether it can be modified or not, for example if modification depends on the user's access rights.</span></span> <span data-ttu-id="cc050-136">В этом случае клиентское приложение должно выполнить вызов и проверить код возврата, чтобы определить возможности контейнера.</span><span class="sxs-lookup"><span data-stu-id="cc050-136">In this case, a client application must attempt a call and examine the return code to determine the container's capabilities.</span></span> <span data-ttu-id="cc050-137">Клиент обычно начинает с изучения АБ_МОДИФИАБЛЕ.</span><span class="sxs-lookup"><span data-stu-id="cc050-137">A client typically starts by examining AB_MODIFIABLE.</span></span> <span data-ttu-id="cc050-138">Если задано, клиент выполняет вызов, который пытается изменить контейнер и проверяет возвращаемое значение.</span><span class="sxs-lookup"><span data-stu-id="cc050-138">If it is set, the client makes a call that attempts to modify the container and checks the return value.</span></span> 
  
<span data-ttu-id="cc050-139">Флаг АБ_МОДИФИАБЛЕ не указывает, какие типы записей можно добавлять в контейнер.</span><span class="sxs-lookup"><span data-stu-id="cc050-139">The AB_MODIFIABLE flag does not indicate what types of entries can be added to the container.</span></span> <span data-ttu-id="cc050-140">Чтобы определить это, клиент должен использовать соответствующий метод [опенпроперти](imapiprop-openproperty.md) для открытия свойства контейнера **пр_креате_темплатес** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="cc050-140">To determine this, the client should use the appropriate [OpenProperty](imapiprop-openproperty.md) method to open the container's **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property.</span></span> <span data-ttu-id="cc050-141">При открытии **пр_креате_темплатес** возвращается таблица, в которой возвращается таблица, в которой перечислены типы записей, которые могут быть созданы в контейнере.</span><span class="sxs-lookup"><span data-stu-id="cc050-141">Opening **PR_CREATE_TEMPLATES** causes the container's one-off table to be returned, listing the kinds of entries that can be created in the container.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="cc050-142">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="cc050-142">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cc050-143">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="cc050-143">Protocol specifications</span></span>

<span data-ttu-id="cc050-144">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cc050-144">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cc050-145">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="cc050-145">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="cc050-146">[[MS — ОКСОАБК]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cc050-146">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cc050-147">Задает свойства и операции для списков пользователей, контактов, групп и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cc050-147">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="cc050-148">[[MS — NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cc050-148">[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cc050-149">Обрабатывает связь клиента с сервером интерфейса поставщика услуг имен (NSPI).</span><span class="sxs-lookup"><span data-stu-id="cc050-149">Handles a client's communications with a Name Service Provider Interface (NSPI) server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cc050-150">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="cc050-150">Header files</span></span>

<span data-ttu-id="cc050-151">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="cc050-151">Mapidefs.h</span></span>
  
> <span data-ttu-id="cc050-152">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="cc050-152">Provides data type definitions.</span></span>
    
<span data-ttu-id="cc050-153">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="cc050-153">Mapitags.h</span></span>
  
> <span data-ttu-id="cc050-154">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="cc050-154">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cc050-155">См. также</span><span class="sxs-lookup"><span data-stu-id="cc050-155">See also</span></span>



[<span data-ttu-id="cc050-156">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="cc050-156">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cc050-157">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="cc050-157">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cc050-158">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="cc050-158">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cc050-159">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="cc050-159">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

