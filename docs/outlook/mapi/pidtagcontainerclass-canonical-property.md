---
title: Каноническое свойство PidTagContainerClass
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContainerClass
api_type:
- HeaderDef
ms.assetid: db249e9e-f1f0-4b95-8cd9-daa7c53ddb32
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c5b80831607f473208ce987a720c7e80e44b6d80
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283151"
---
# <a name="pidtagcontainerclass-canonical-property"></a><span data-ttu-id="f2d41-103">Каноническое свойство PidTagContainerClass</span><span class="sxs-lookup"><span data-stu-id="f2d41-103">PidTagContainerClass Canonical Property</span></span>

  
  
<span data-ttu-id="f2d41-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f2d41-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f2d41-105">Содержит текстовую строку, описываемую тип папки.</span><span class="sxs-lookup"><span data-stu-id="f2d41-105">Contains a text string describing the type of a folder.</span></span> <span data-ttu-id="f2d41-106">Хотя это свойство обычно игнорируется, версии Microsoft® Exchange Server предшествующие Exchange Server Mailbox Manager 2003, ожидают, что это свойство будет присутствовать.</span><span class="sxs-lookup"><span data-stu-id="f2d41-106">Although this property is generally ignored, versions of Microsoft® Exchange Server prior to Exchange Server 2003 Mailbox Manager expect this property to be present.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f2d41-107">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="f2d41-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="f2d41-108">PR_CONTAINER_CLASS, PR_CONTAINER_CLASS_A, PR_CONTAINER_CLASS_W</span><span class="sxs-lookup"><span data-stu-id="f2d41-108">PR_CONTAINER_CLASS, PR_CONTAINER_CLASS_A, PR_CONTAINER_CLASS_W</span></span>  <br/> |
|<span data-ttu-id="f2d41-109">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="f2d41-109">Identifier:</span></span>  <br/> |<span data-ttu-id="f2d41-110">0x3613</span><span class="sxs-lookup"><span data-stu-id="f2d41-110">0x3613</span></span>  <br/> |
|<span data-ttu-id="f2d41-111">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="f2d41-111">Data type:</span></span>  <br/> |<span data-ttu-id="f2d41-112">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f2d41-112">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="f2d41-113">Область:</span><span class="sxs-lookup"><span data-stu-id="f2d41-113">Area:</span></span>  <br/> |<span data-ttu-id="f2d41-114">Container</span><span class="sxs-lookup"><span data-stu-id="f2d41-114">Container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f2d41-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="f2d41-115">Remarks</span></span>

<span data-ttu-id="f2d41-116">Эти свойства обычно не используются Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="f2d41-116">These properties are not normally used by Exchange Server.</span></span> <span data-ttu-id="f2d41-117">Однако Microsoft Office Outlook® вложенные в папки почтовых ящиков.</span><span class="sxs-lookup"><span data-stu-id="f2d41-117">However, Microsoft Office Outlook® attaches them to mailbox folders.</span></span> <span data-ttu-id="f2d41-118">Кроме того, версии Exchange Server, предшествующие Exchange Server 2003 Mailbox Manager, могут неправильно обрабатывать папки, которые не имеют этих свойств.</span><span class="sxs-lookup"><span data-stu-id="f2d41-118">In addition, versions of Exchange Server prior to Exchange Server 2003 Mailbox Manager might incorrectly handle folders that do not have these properties.</span></span>
  
<span data-ttu-id="f2d41-119">Этим свойствам могут быть назначены строки, указанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="f2d41-119">These properties can be assigned the string values in the following table.</span></span>
  
|<span data-ttu-id="f2d41-120">**Значение**</span><span class="sxs-lookup"><span data-stu-id="f2d41-120">**Value**</span></span>|<span data-ttu-id="f2d41-121">**Содержимое папки**</span><span class="sxs-lookup"><span data-stu-id="f2d41-121">**Contents of Folder**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f2d41-122">IPF. Встреча</span><span class="sxs-lookup"><span data-stu-id="f2d41-122">IPF.Appointment</span></span>  <br/> |<span data-ttu-id="f2d41-123">Встречи</span><span class="sxs-lookup"><span data-stu-id="f2d41-123">Appointments</span></span>  <br/> |
|<span data-ttu-id="f2d41-124">IPF. Контакт</span><span class="sxs-lookup"><span data-stu-id="f2d41-124">IPF.Contact</span></span>  <br/> |<span data-ttu-id="f2d41-125">Контакты</span><span class="sxs-lookup"><span data-stu-id="f2d41-125">Contacts</span></span>  <br/> |
|<span data-ttu-id="f2d41-126">IPF. Журнал</span><span class="sxs-lookup"><span data-stu-id="f2d41-126">IPF.Journal</span></span>  <br/> |<span data-ttu-id="f2d41-127">Записи журнала Outlook</span><span class="sxs-lookup"><span data-stu-id="f2d41-127">Outlook Journal entries</span></span>  <br/> |
|<span data-ttu-id="f2d41-128">IPF. Примечание</span><span class="sxs-lookup"><span data-stu-id="f2d41-128">IPF.Note</span></span>  <br/> |<span data-ttu-id="f2d41-129">Почтовые сообщения и заметки</span><span class="sxs-lookup"><span data-stu-id="f2d41-129">Mail Messages and notes</span></span>  <br/> |
|<span data-ttu-id="f2d41-130">IPF. StickyNote</span><span class="sxs-lookup"><span data-stu-id="f2d41-130">IPF.StickyNote</span></span>  <br/> |<span data-ttu-id="f2d41-131">Заметки о тиках Outlook</span><span class="sxs-lookup"><span data-stu-id="f2d41-131">Outlook Sticky Notes</span></span>  <br/> |
|<span data-ttu-id="f2d41-132">IPF. Задача</span><span class="sxs-lookup"><span data-stu-id="f2d41-132">IPF.Task</span></span>  <br/> |<span data-ttu-id="f2d41-133">Задачи Outlook</span><span class="sxs-lookup"><span data-stu-id="f2d41-133">Outlook Tasks</span></span>  <br/> |
   
<span data-ttu-id="f2d41-134">Для папок, содержащих сообщения электронной почты, эти свойства должны иметь iPF. Примечание.</span><span class="sxs-lookup"><span data-stu-id="f2d41-134">For folders that contain mail messages, these properties should be set to IPF.Note.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f2d41-135">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f2d41-135">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f2d41-136">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="f2d41-136">Protocol specifications</span></span>

<span data-ttu-id="f2d41-137">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f2d41-137">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f2d41-138">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="f2d41-138">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f2d41-139">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f2d41-139">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f2d41-140">Указывает свойства и операции для создания и размещения специальных папок в почтовом ящике.</span><span class="sxs-lookup"><span data-stu-id="f2d41-140">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="f2d41-141">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f2d41-141">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f2d41-142">Указывает свойства и операции для встреч, запросов на собрание и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="f2d41-142">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="f2d41-143">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f2d41-143">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f2d41-144">Указывает свойства и операции, которые разрешены для объектов контактов и личных списков рассылки.</span><span class="sxs-lookup"><span data-stu-id="f2d41-144">Specifies the properties and operations that are permissible for contact and personal distribution list objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f2d41-145">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="f2d41-145">Header files</span></span>

<span data-ttu-id="f2d41-146">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f2d41-146">Mapidefs.h</span></span>
  
> <span data-ttu-id="f2d41-147">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="f2d41-147">Provides data type definitions.</span></span>
    
<span data-ttu-id="f2d41-148">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f2d41-148">Mapitags.h</span></span>
  
> <span data-ttu-id="f2d41-149">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="f2d41-149">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f2d41-150">См. также</span><span class="sxs-lookup"><span data-stu-id="f2d41-150">See also</span></span>



[<span data-ttu-id="f2d41-151">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f2d41-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f2d41-152">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f2d41-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f2d41-153">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="f2d41-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f2d41-154">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="f2d41-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

