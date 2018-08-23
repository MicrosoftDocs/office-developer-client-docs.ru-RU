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
ms.openlocfilehash: 5a3a83153dc799154edc6a46946682684cad8a09
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593776"
---
# <a name="pidtagcontainerclass-canonical-property"></a><span data-ttu-id="fdb9f-103">Каноническое свойство PidTagContainerClass</span><span class="sxs-lookup"><span data-stu-id="fdb9f-103">PidTagContainerClass Canonical Property</span></span>

  
  
<span data-ttu-id="fdb9f-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fdb9f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fdb9f-105">Содержит текстовая строка, описывающая тип папки.</span><span class="sxs-lookup"><span data-stu-id="fdb9f-105">Contains a text string describing the type of a folder.</span></span> <span data-ttu-id="fdb9f-106">Несмотря на то, что это свойство игнорируется, как правило, версий Microsoft® Exchange Server до диспетчера почтовых ящиков Exchange Server 2003 ожидается, что это свойство должен быть установлен.</span><span class="sxs-lookup"><span data-stu-id="fdb9f-106">Although this property is generally ignored, versions of Microsoft® Exchange Server prior to Exchange Server 2003 Mailbox Manager expect this property to be present.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fdb9f-107">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="fdb9f-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="fdb9f-108">PR_CONTAINER_CLASS, PR_CONTAINER_CLASS_A, PR_CONTAINER_CLASS_W</span><span class="sxs-lookup"><span data-stu-id="fdb9f-108">PR_CONTAINER_CLASS, PR_CONTAINER_CLASS_A, PR_CONTAINER_CLASS_W</span></span>  <br/> |
|<span data-ttu-id="fdb9f-109">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="fdb9f-109">Identifier:</span></span>  <br/> |<span data-ttu-id="fdb9f-110">0x3613</span><span class="sxs-lookup"><span data-stu-id="fdb9f-110">0x3613</span></span>  <br/> |
|<span data-ttu-id="fdb9f-111">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="fdb9f-111">Data type:</span></span>  <br/> |<span data-ttu-id="fdb9f-112">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="fdb9f-112">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="fdb9f-113">Область:</span><span class="sxs-lookup"><span data-stu-id="fdb9f-113">Area:</span></span>  <br/> |<span data-ttu-id="fdb9f-114">Контейнер</span><span class="sxs-lookup"><span data-stu-id="fdb9f-114">Container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fdb9f-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="fdb9f-115">Remarks</span></span>

<span data-ttu-id="fdb9f-116">Эти свойства обычно не используется в Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="fdb9f-116">These properties are not normally used by Exchange Server.</span></span> <span data-ttu-id="fdb9f-117">Тем не менее Microsoft Office Outlook® подключает их папки почтовых ящиков.</span><span class="sxs-lookup"><span data-stu-id="fdb9f-117">However, Microsoft Office Outlook® attaches them to mailbox folders.</span></span> <span data-ttu-id="fdb9f-118">Кроме того версии Exchange Server до диспетчера почтовых ящиков Exchange Server 2003 могут неправильно обрабатывать папок, которые не имеют следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="fdb9f-118">In addition, versions of Exchange Server prior to Exchange Server 2003 Mailbox Manager might incorrectly handle folders that do not have these properties.</span></span>
  
<span data-ttu-id="fdb9f-119">Эти свойства может быть назначен строковых значений в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="fdb9f-119">These properties can be assigned the string values in the following table.</span></span>
  
|<span data-ttu-id="fdb9f-120">**Значение**</span><span class="sxs-lookup"><span data-stu-id="fdb9f-120">**Value**</span></span>|<span data-ttu-id="fdb9f-121">**Содержимое папки**</span><span class="sxs-lookup"><span data-stu-id="fdb9f-121">**Contents of Folder**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fdb9f-122">IPF. Встречи</span><span class="sxs-lookup"><span data-stu-id="fdb9f-122">IPF.Appointment</span></span>  <br/> |<span data-ttu-id="fdb9f-123">Встречи</span><span class="sxs-lookup"><span data-stu-id="fdb9f-123">Appointments</span></span>  <br/> |
|<span data-ttu-id="fdb9f-124">IPF. Контакт</span><span class="sxs-lookup"><span data-stu-id="fdb9f-124">IPF.Contact</span></span>  <br/> |<span data-ttu-id="fdb9f-125">Contacts</span><span class="sxs-lookup"><span data-stu-id="fdb9f-125">Contacts</span></span>  <br/> |
|<span data-ttu-id="fdb9f-126">IPF. Журнал</span><span class="sxs-lookup"><span data-stu-id="fdb9f-126">IPF.Journal</span></span>  <br/> |<span data-ttu-id="fdb9f-127">Записи журнала в Outlook</span><span class="sxs-lookup"><span data-stu-id="fdb9f-127">Outlook Journal entries</span></span>  <br/> |
|<span data-ttu-id="fdb9f-128">IPF. Примечание</span><span class="sxs-lookup"><span data-stu-id="fdb9f-128">IPF.Note</span></span>  <br/> |<span data-ttu-id="fdb9f-129">Сообщения почты и заметки</span><span class="sxs-lookup"><span data-stu-id="fdb9f-129">Mail Messages and notes</span></span>  <br/> |
|<span data-ttu-id="fdb9f-130">IPF. Заметки</span><span class="sxs-lookup"><span data-stu-id="fdb9f-130">IPF.StickyNote</span></span>  <br/> |<span data-ttu-id="fdb9f-131">Записки Outlook</span><span class="sxs-lookup"><span data-stu-id="fdb9f-131">Outlook Sticky Notes</span></span>  <br/> |
|<span data-ttu-id="fdb9f-132">IPF. Задача</span><span class="sxs-lookup"><span data-stu-id="fdb9f-132">IPF.Task</span></span>  <br/> |<span data-ttu-id="fdb9f-133">Задачи Outlook</span><span class="sxs-lookup"><span data-stu-id="fdb9f-133">Outlook Tasks</span></span>  <br/> |
   
<span data-ttu-id="fdb9f-134">Для папок, содержащих почтовых сообщений эти свойства должны быть установлены для IPF. Примечание.</span><span class="sxs-lookup"><span data-stu-id="fdb9f-134">For folders that contain mail messages, these properties should be set to IPF.Note.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="fdb9f-135">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="fdb9f-135">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fdb9f-136">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="fdb9f-136">Protocol specifications</span></span>

<span data-ttu-id="fdb9f-137">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fdb9f-137">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fdb9f-138">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="fdb9f-138">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fdb9f-139">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fdb9f-139">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fdb9f-140">Задает свойства и операции по созданию и поиск специальные папки в почтовом ящике.</span><span class="sxs-lookup"><span data-stu-id="fdb9f-140">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="fdb9f-141">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fdb9f-141">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fdb9f-142">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="fdb9f-142">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="fdb9f-143">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fdb9f-143">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fdb9f-144">Задает свойства и операции, допустимые для объектов списка рассылки и контактов.</span><span class="sxs-lookup"><span data-stu-id="fdb9f-144">Specifies the properties and operations that are permissible for contact and personal distribution list objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fdb9f-145">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="fdb9f-145">Header files</span></span>

<span data-ttu-id="fdb9f-146">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fdb9f-146">Mapidefs.h</span></span>
  
> <span data-ttu-id="fdb9f-147">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="fdb9f-147">Provides data type definitions.</span></span>
    
<span data-ttu-id="fdb9f-148">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="fdb9f-148">Mapitags.h</span></span>
  
> <span data-ttu-id="fdb9f-149">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="fdb9f-149">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fdb9f-150">См. также</span><span class="sxs-lookup"><span data-stu-id="fdb9f-150">See also</span></span>



[<span data-ttu-id="fdb9f-151">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="fdb9f-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fdb9f-152">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="fdb9f-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fdb9f-153">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="fdb9f-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fdb9f-154">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="fdb9f-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

