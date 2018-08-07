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
ms.openlocfilehash: 9d40c21cde6bf3a6e8e37dda80dd6f900f233a0e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810967"
---
# <a name="pidtagcontainerclass-canonical-property"></a><span data-ttu-id="e1e3b-103">Каноническое свойство PidTagContainerClass</span><span class="sxs-lookup"><span data-stu-id="e1e3b-103">PidTagContainerClass Canonical Property</span></span>

  
  
<span data-ttu-id="e1e3b-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e1e3b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e1e3b-105">Содержит текстовая строка, описывающая тип папки.</span><span class="sxs-lookup"><span data-stu-id="e1e3b-105">Contains a text string describing the type of a folder.</span></span> <span data-ttu-id="e1e3b-106">Несмотря на то, что это свойство игнорируется, как правило, версий Microsoft® Exchange Server до диспетчера почтовых ящиков Exchange Server 2003 ожидается, что это свойство должен быть установлен.</span><span class="sxs-lookup"><span data-stu-id="e1e3b-106">Although this property is generally ignored, versions of Microsoft® Exchange Server prior to Exchange Server 2003 Mailbox Manager expect this property to be present.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e1e3b-107">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="e1e3b-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="e1e3b-108">PR_CONTAINER_CLASS, PR_CONTAINER_CLASS_A, PR_CONTAINER_CLASS_W</span><span class="sxs-lookup"><span data-stu-id="e1e3b-108">PR_CONTAINER_CLASS, PR_CONTAINER_CLASS_A, PR_CONTAINER_CLASS_W</span></span>  <br/> |
|<span data-ttu-id="e1e3b-109">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="e1e3b-109">Identifier:</span></span>  <br/> |<span data-ttu-id="e1e3b-110">0x3613</span><span class="sxs-lookup"><span data-stu-id="e1e3b-110">0x3613</span></span>  <br/> |
|<span data-ttu-id="e1e3b-111">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="e1e3b-111">Data type:</span></span>  <br/> |<span data-ttu-id="e1e3b-112">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e1e3b-112">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="e1e3b-113">Область:</span><span class="sxs-lookup"><span data-stu-id="e1e3b-113">Area:</span></span>  <br/> |<span data-ttu-id="e1e3b-114">Контейнер</span><span class="sxs-lookup"><span data-stu-id="e1e3b-114">Container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e1e3b-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="e1e3b-115">Remarks</span></span>

<span data-ttu-id="e1e3b-116">Эти свойства обычно не используется в Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="e1e3b-116">These properties are not normally used by Exchange Server.</span></span> <span data-ttu-id="e1e3b-117">Тем не менее Microsoft Office Outlook® подключает их папки почтовых ящиков.</span><span class="sxs-lookup"><span data-stu-id="e1e3b-117">However, Microsoft Office Outlook® attaches them to mailbox folders.</span></span> <span data-ttu-id="e1e3b-118">Кроме того версии Exchange Server до диспетчера почтовых ящиков Exchange Server 2003 могут неправильно обрабатывать папок, которые не имеют следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e1e3b-118">In addition, versions of Exchange Server prior to Exchange Server 2003 Mailbox Manager might incorrectly handle folders that do not have these properties.</span></span>
  
<span data-ttu-id="e1e3b-119">Эти свойства может быть назначен строковых значений в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="e1e3b-119">These properties can be assigned the string values in the following table.</span></span>
  
|<span data-ttu-id="e1e3b-120">**Значение**</span><span class="sxs-lookup"><span data-stu-id="e1e3b-120">**Value**</span></span>|<span data-ttu-id="e1e3b-121">**Содержимое папки**</span><span class="sxs-lookup"><span data-stu-id="e1e3b-121">**Contents of Folder**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e1e3b-122">IPF. Встречи</span><span class="sxs-lookup"><span data-stu-id="e1e3b-122">IPF.Appointment</span></span>  <br/> |<span data-ttu-id="e1e3b-123">Встречи</span><span class="sxs-lookup"><span data-stu-id="e1e3b-123">Appointments</span></span>  <br/> |
|<span data-ttu-id="e1e3b-124">IPF. Контакт</span><span class="sxs-lookup"><span data-stu-id="e1e3b-124">IPF.Contact</span></span>  <br/> |<span data-ttu-id="e1e3b-125">Контакты</span><span class="sxs-lookup"><span data-stu-id="e1e3b-125">Contacts</span></span>  <br/> |
|<span data-ttu-id="e1e3b-126">IPF. Журнал</span><span class="sxs-lookup"><span data-stu-id="e1e3b-126">IPF.Journal</span></span>  <br/> |<span data-ttu-id="e1e3b-127">Записи журнала в Outlook</span><span class="sxs-lookup"><span data-stu-id="e1e3b-127">Outlook Journal entries</span></span>  <br/> |
|<span data-ttu-id="e1e3b-128">IPF. Примечание</span><span class="sxs-lookup"><span data-stu-id="e1e3b-128">IPF.Note</span></span>  <br/> |<span data-ttu-id="e1e3b-129">Сообщения почты и заметки</span><span class="sxs-lookup"><span data-stu-id="e1e3b-129">Mail Messages and notes</span></span>  <br/> |
|<span data-ttu-id="e1e3b-130">IPF. Заметки</span><span class="sxs-lookup"><span data-stu-id="e1e3b-130">IPF.StickyNote</span></span>  <br/> |<span data-ttu-id="e1e3b-131">Записки Outlook</span><span class="sxs-lookup"><span data-stu-id="e1e3b-131">Outlook Sticky Notes</span></span>  <br/> |
|<span data-ttu-id="e1e3b-132">IPF. Задача</span><span class="sxs-lookup"><span data-stu-id="e1e3b-132">IPF.Task</span></span>  <br/> |<span data-ttu-id="e1e3b-133">Задачи Outlook</span><span class="sxs-lookup"><span data-stu-id="e1e3b-133">Outlook Tasks</span></span>  <br/> |
   
<span data-ttu-id="e1e3b-134">Для папок, содержащих почтовых сообщений эти свойства должны быть установлены для IPF. Примечание.</span><span class="sxs-lookup"><span data-stu-id="e1e3b-134">For folders that contain mail messages, these properties should be set to IPF.Note.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e1e3b-135">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="e1e3b-135">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e1e3b-136">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="e1e3b-136">Protocol specifications</span></span>

<span data-ttu-id="e1e3b-137">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e1e3b-137">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e1e3b-138">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="e1e3b-138">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e1e3b-139">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e1e3b-139">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e1e3b-140">Задает свойства и операции по созданию и поиск специальные папки в почтовом ящике.</span><span class="sxs-lookup"><span data-stu-id="e1e3b-140">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="e1e3b-141">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e1e3b-141">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e1e3b-142">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="e1e3b-142">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="e1e3b-143">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e1e3b-143">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e1e3b-144">Задает свойства и операции, допустимые для объектов списка рассылки и контактов.</span><span class="sxs-lookup"><span data-stu-id="e1e3b-144">Specifies the properties and operations that are permissible for contact and personal distribution list objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e1e3b-145">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="e1e3b-145">Header files</span></span>

<span data-ttu-id="e1e3b-146">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e1e3b-146">Mapidefs.h</span></span>
  
> <span data-ttu-id="e1e3b-147">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="e1e3b-147">Provides data type definitions.</span></span>
    
<span data-ttu-id="e1e3b-148">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e1e3b-148">Mapitags.h</span></span>
  
> <span data-ttu-id="e1e3b-149">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="e1e3b-149">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e1e3b-150">См. также</span><span class="sxs-lookup"><span data-stu-id="e1e3b-150">See also</span></span>



[<span data-ttu-id="e1e3b-151">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="e1e3b-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e1e3b-152">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="e1e3b-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e1e3b-153">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="e1e3b-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e1e3b-154">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="e1e3b-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

