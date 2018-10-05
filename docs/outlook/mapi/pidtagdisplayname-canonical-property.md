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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386420"
---
# <a name="pidtagdisplayname-canonical-property"></a><span data-ttu-id="dc77e-103">Каноническое свойство PidTagDisplayName</span><span class="sxs-lookup"><span data-stu-id="dc77e-103">PidTagDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="dc77e-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dc77e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dc77e-105">Содержит отображаемое имя для данного объекта MAPI.</span><span class="sxs-lookup"><span data-stu-id="dc77e-105">Contains the display name for a given MAPI object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dc77e-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="dc77e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="dc77e-107">PR_DISPLAY_NAME, PR_DISPLAY_NAME_A, PR_DISPLAY_NAME_W</span><span class="sxs-lookup"><span data-stu-id="dc77e-107">PR_DISPLAY_NAME, PR_DISPLAY_NAME_A, PR_DISPLAY_NAME_W</span></span>  <br/> |
|<span data-ttu-id="dc77e-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="dc77e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="dc77e-109">0x3001</span><span class="sxs-lookup"><span data-stu-id="dc77e-109">0x3001</span></span>  <br/> |
|<span data-ttu-id="dc77e-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="dc77e-110">Data type:</span></span>  <br/> |<span data-ttu-id="dc77e-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="dc77e-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="dc77e-112">Область:</span><span class="sxs-lookup"><span data-stu-id="dc77e-112">Area:</span></span>  <br/> |<span data-ttu-id="dc77e-113">Распространенные MAPI</span><span class="sxs-lookup"><span data-stu-id="dc77e-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dc77e-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="dc77e-114">Remarks</span></span>

<span data-ttu-id="dc77e-115">Папки требуют вложенных папок одноуровневого иметь уникальные отображаемые имена.</span><span class="sxs-lookup"><span data-stu-id="dc77e-115">Folders require sibling subfolders to have unique display names.</span></span> <span data-ttu-id="dc77e-116">Например если папка содержит два вложенных папок, два вложенных папок нельзя использовать такое же значение для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="dc77e-116">For example, if a folder contains two subfolders, the two subfolders cannot use the same value for this property.</span></span> <span data-ttu-id="dc77e-117">Это ограничение не применяется к другим контейнеров, такие как адресные книги и списки рассылки.</span><span class="sxs-lookup"><span data-stu-id="dc77e-117">This restriction does not apply to other containers, such as address books and distribution lists.</span></span> 
  
<span data-ttu-id="dc77e-118">Поставщиков услуг необходимо задать значение этого свойства, чтобы он содержит оба типа и конфигурации сведения о поставщике.</span><span class="sxs-lookup"><span data-stu-id="dc77e-118">Service providers should set the value of this property so that it contains both the provider type and configuration information.</span></span> <span data-ttu-id="dc77e-119">Дополнительная информация помогает различать экземпляры поставщиков одного типа.</span><span class="sxs-lookup"><span data-stu-id="dc77e-119">The additional information helps to distinguish between instances of providers of the same type.</span></span> <span data-ttu-id="dc77e-120">Ненастроенный поставщиков следует использовать строку с именем поставщика.</span><span class="sxs-lookup"><span data-stu-id="dc77e-120">Unconfigured providers should use a string that names the provider.</span></span> <span data-ttu-id="dc77e-121">Настроенных поставщиков следует использовать ту же строку и отличительные строки в скобки.</span><span class="sxs-lookup"><span data-stu-id="dc77e-121">Configured providers should use the same string followed by a distinguishing string in parentheses.</span></span> <span data-ttu-id="dc77e-122">Например поставщика хранилища ненастроенный сообщение может задать эти свойства:</span><span class="sxs-lookup"><span data-stu-id="dc77e-122">For example, an unconfigured message store provider might set these properties to:</span></span> 
  
<span data-ttu-id="dc77e-123">Личное хранилище данных</span><span class="sxs-lookup"><span data-stu-id="dc77e-123">Personal Information Store</span></span>
  
<span data-ttu-id="dc77e-124">Затем настроенную версию может задать эти свойства:</span><span class="sxs-lookup"><span data-stu-id="dc77e-124">The configured version could then set these properties to:</span></span> 
  
<span data-ttu-id="dc77e-125">Личное хранилище данных (6 февраля 1998 г.)</span><span class="sxs-lookup"><span data-stu-id="dc77e-125">Personal Information Store (February 6, 1998)</span></span>
  
<span data-ttu-id="dc77e-126">Для объектов состояния эти свойства содержит имя компонента, который может отображаться в интерфейсе пользователя.</span><span class="sxs-lookup"><span data-stu-id="dc77e-126">For status objects, these properties contain the name of the component that can be displayed by the user interface.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="dc77e-127">Запятой нельзя использовать в рамках получателей в системе обмена сообщениями MAPI.</span><span class="sxs-lookup"><span data-stu-id="dc77e-127">Semicolons cannot be used within recipient names in MAPI messaging.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="dc77e-128">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="dc77e-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="dc77e-129">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="dc77e-129">Protocol specifications</span></span>

<span data-ttu-id="dc77e-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dc77e-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dc77e-131">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="dc77e-131">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="dc77e-132">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dc77e-132">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dc77e-133">Обрабатывает объекты сообщения и вложения.</span><span class="sxs-lookup"><span data-stu-id="dc77e-133">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="dc77e-134">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dc77e-134">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dc77e-135">Обрабатывает операции папки.</span><span class="sxs-lookup"><span data-stu-id="dc77e-135">Handles folder operations.</span></span>
    
<span data-ttu-id="dc77e-136">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dc77e-136">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dc77e-137">Задает свойства и операции, допустимые для контакты и списки рассылки.</span><span class="sxs-lookup"><span data-stu-id="dc77e-137">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="dc77e-138">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dc77e-138">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dc77e-139">Задает свойства и операции для списков пользователей, контактов, групп и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dc77e-139">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="dc77e-140">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dc77e-140">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dc77e-141">Преобразование conventions стандартных электронной почты Интернета объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="dc77e-141">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="dc77e-142">[[MS-XWDVSEC]](https://msdn.microsoft.com/library/dc043d09-6b76-4392-aea3-68f8e81c64d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dc77e-142">[[MS-XWDVSEC]](https://msdn.microsoft.com/library/dc043d09-6b76-4392-aea3-68f8e81c64d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dc77e-143">Расширяет протокол WebDAV, определяющее, как для запроса и задать дескриптор безопасности Exchange с помощью методов WebDAV.</span><span class="sxs-lookup"><span data-stu-id="dc77e-143">Extends the WebDAV protocol that specifies how to request and set the Exchange security descriptor via WebDAV methods.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="dc77e-144">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="dc77e-144">Header files</span></span>

<span data-ttu-id="dc77e-145">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="dc77e-145">Mapidefs.h</span></span>
  
> <span data-ttu-id="dc77e-146">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="dc77e-146">Provides data type definitions.</span></span>
    
<span data-ttu-id="dc77e-147">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="dc77e-147">Mapitags.h</span></span>
  
> <span data-ttu-id="dc77e-148">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="dc77e-148">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dc77e-149">См. также</span><span class="sxs-lookup"><span data-stu-id="dc77e-149">See also</span></span>



[<span data-ttu-id="dc77e-150">Каноническое свойство PidTagTransmittableDisplayName</span><span class="sxs-lookup"><span data-stu-id="dc77e-150">PidTagTransmittableDisplayName Canonical Property</span></span>](pidtagtransmittabledisplayname-canonical-property.md)


[<span data-ttu-id="dc77e-151">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="dc77e-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="dc77e-152">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="dc77e-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="dc77e-153">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="dc77e-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="dc77e-154">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="dc77e-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

