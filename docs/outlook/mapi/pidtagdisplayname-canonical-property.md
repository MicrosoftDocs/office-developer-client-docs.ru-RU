---
title: Каноническое свойство PidTagDisplayName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayName
api_type:
- HeaderDef
ms.assetid: bd094e00-5c60-4bb3-9a45-b943fab52876
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 834141fe3e57fde5e6404776e0ad5ce3b438450e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360804"
---
# <a name="pidtagdisplayname-canonical-property"></a><span data-ttu-id="f85c9-103">Каноническое свойство PidTagDisplayName</span><span class="sxs-lookup"><span data-stu-id="f85c9-103">PidTagDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="f85c9-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f85c9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f85c9-105">Содержит имя отображения для данного объекта MAPI.</span><span class="sxs-lookup"><span data-stu-id="f85c9-105">Contains the display name for a given MAPI object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f85c9-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="f85c9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f85c9-107">PR_DISPLAY_NAME, PR_DISPLAY_NAME_A, PR_DISPLAY_NAME_W</span><span class="sxs-lookup"><span data-stu-id="f85c9-107">PR_DISPLAY_NAME, PR_DISPLAY_NAME_A, PR_DISPLAY_NAME_W</span></span>  <br/> |
|<span data-ttu-id="f85c9-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="f85c9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f85c9-109">0x3001</span><span class="sxs-lookup"><span data-stu-id="f85c9-109">0x3001</span></span>  <br/> |
|<span data-ttu-id="f85c9-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="f85c9-110">Data type:</span></span>  <br/> |<span data-ttu-id="f85c9-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f85c9-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="f85c9-112">Область:</span><span class="sxs-lookup"><span data-stu-id="f85c9-112">Area:</span></span>  <br/> |<span data-ttu-id="f85c9-113">MAPI общие</span><span class="sxs-lookup"><span data-stu-id="f85c9-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f85c9-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="f85c9-114">Remarks</span></span>

<span data-ttu-id="f85c9-115">Папки требуют, чтобы в подмостках для собратов были уникальные имена дисплеев.</span><span class="sxs-lookup"><span data-stu-id="f85c9-115">Folders require sibling subfolders to have unique display names.</span></span> <span data-ttu-id="f85c9-116">Например, если папка содержит два подмастеря, эти два подмастеря не могут использовать одно и то же значение для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="f85c9-116">For example, if a folder contains two subfolders, the two subfolders cannot use the same value for this property.</span></span> <span data-ttu-id="f85c9-117">Это ограничение не распространяется на другие контейнеры, такие как адресные книги и списки рассылки.</span><span class="sxs-lookup"><span data-stu-id="f85c9-117">This restriction does not apply to other containers, such as address books and distribution lists.</span></span> 
  
<span data-ttu-id="f85c9-118">Поставщики услуг должны установить значение этого свойства, чтобы оно содержалось как в типе поставщика, так и в сведениях о конфигурации.</span><span class="sxs-lookup"><span data-stu-id="f85c9-118">Service providers should set the value of this property so that it contains both the provider type and configuration information.</span></span> <span data-ttu-id="f85c9-119">Дополнительные сведения помогают различать экземпляры поставщиков одного типа.</span><span class="sxs-lookup"><span data-stu-id="f85c9-119">The additional information helps to distinguish between instances of providers of the same type.</span></span> <span data-ttu-id="f85c9-120">Неконфигуративные поставщики должны использовать строку, которая называет поставщика.</span><span class="sxs-lookup"><span data-stu-id="f85c9-120">Unconfigured providers should use a string that names the provider.</span></span> <span data-ttu-id="f85c9-121">Настроенные поставщики должны использовать ту же строку, с которой следует различать строку в скобке.</span><span class="sxs-lookup"><span data-stu-id="f85c9-121">Configured providers should use the same string followed by a distinguishing string in parentheses.</span></span> <span data-ttu-id="f85c9-122">Например, поставщик неконфигурационных магазинов сообщений может установить эти свойства:</span><span class="sxs-lookup"><span data-stu-id="f85c9-122">For example, an unconfigured message store provider might set these properties to:</span></span> 
  
<span data-ttu-id="f85c9-123">Хранилище персональных данных</span><span class="sxs-lookup"><span data-stu-id="f85c9-123">Personal Information Store</span></span>
  
<span data-ttu-id="f85c9-124">Затем настроенная версия может установить эти свойства:</span><span class="sxs-lookup"><span data-stu-id="f85c9-124">The configured version could then set these properties to:</span></span> 
  
<span data-ttu-id="f85c9-125">Хранилище персональных данных (6 февраля 1998 г.)</span><span class="sxs-lookup"><span data-stu-id="f85c9-125">Personal Information Store (February 6, 1998)</span></span>
  
<span data-ttu-id="f85c9-126">Для объектов состояния эти свойства содержат имя компонента, который может отображаться пользовательским интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="f85c9-126">For status objects, these properties contain the name of the component that can be displayed by the user interface.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="f85c9-127">Semicolons нельзя использовать в именах получателей в сообщении MAPI.</span><span class="sxs-lookup"><span data-stu-id="f85c9-127">Semicolons cannot be used within recipient names in MAPI messaging.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f85c9-128">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f85c9-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f85c9-129">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="f85c9-129">Protocol specifications</span></span>

<span data-ttu-id="f85c9-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f85c9-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f85c9-131">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="f85c9-131">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f85c9-132">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f85c9-132">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f85c9-133">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="f85c9-133">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="f85c9-134">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f85c9-134">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f85c9-135">Обрабатывает операции папок.</span><span class="sxs-lookup"><span data-stu-id="f85c9-135">Handles folder operations.</span></span>
    
<span data-ttu-id="f85c9-136">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f85c9-136">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f85c9-137">Указывает свойства и операции, допустимые для контактов и личных списков рассылки.</span><span class="sxs-lookup"><span data-stu-id="f85c9-137">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="f85c9-138">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f85c9-138">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f85c9-139">Указывает свойства и операции для списков пользователей, контактов, групп и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f85c9-139">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="f85c9-140">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f85c9-140">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f85c9-141">Преобразуется из стандартных конвенций электронной почты в объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="f85c9-141">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="f85c9-142">[[MS-XWDVSEC]](https://msdn.microsoft.com/library/dc043d09-6b76-4392-aea3-68f8e81c64d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f85c9-142">[[MS-XWDVSEC]](https://msdn.microsoft.com/library/dc043d09-6b76-4392-aea3-68f8e81c64d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f85c9-143">Расширяет протокол WebDAV, который указывает, как запрашивать и Exchange дескриптор безопасности с помощью методов WebDAV.</span><span class="sxs-lookup"><span data-stu-id="f85c9-143">Extends the WebDAV protocol that specifies how to request and set the Exchange security descriptor via WebDAV methods.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f85c9-144">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="f85c9-144">Header files</span></span>

<span data-ttu-id="f85c9-145">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f85c9-145">Mapidefs.h</span></span>
  
> <span data-ttu-id="f85c9-146">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="f85c9-146">Provides data type definitions.</span></span>
    
<span data-ttu-id="f85c9-147">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f85c9-147">Mapitags.h</span></span>
  
> <span data-ttu-id="f85c9-148">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="f85c9-148">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f85c9-149">См. также</span><span class="sxs-lookup"><span data-stu-id="f85c9-149">See also</span></span>



[<span data-ttu-id="f85c9-150">Каноническое свойство PidTagTransmittableDisplayName</span><span class="sxs-lookup"><span data-stu-id="f85c9-150">PidTagTransmittableDisplayName Canonical Property</span></span>](pidtagtransmittabledisplayname-canonical-property.md)


[<span data-ttu-id="f85c9-151">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f85c9-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f85c9-152">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f85c9-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f85c9-153">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="f85c9-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f85c9-154">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="f85c9-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

