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
# <a name="pidtagcontainerclass-canonical-property"></a><span data-ttu-id="c44ca-103">Каноническое свойство PidTagContainerClass</span><span class="sxs-lookup"><span data-stu-id="c44ca-103">PidTagContainerClass Canonical Property</span></span>

  
  
<span data-ttu-id="c44ca-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c44ca-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c44ca-105">Содержит текстовую строку, описывающую тип папки.</span><span class="sxs-lookup"><span data-stu-id="c44ca-105">Contains a text string describing the type of a folder.</span></span> <span data-ttu-id="c44ca-106">Несмотря на то что это свойство обычно игнорируется, версии Microsoft® Exchange Server до Exchange Server 2003 почтовых ящиков ожидают, что это свойство присутствует.</span><span class="sxs-lookup"><span data-stu-id="c44ca-106">Although this property is generally ignored, versions of Microsoft® Exchange Server prior to Exchange Server 2003 Mailbox Manager expect this property to be present.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c44ca-107">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="c44ca-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="c44ca-108">PR_CONTAINER_CLASS, PR_CONTAINER_CLASS_A PR_CONTAINER_CLASS_W</span><span class="sxs-lookup"><span data-stu-id="c44ca-108">PR_CONTAINER_CLASS, PR_CONTAINER_CLASS_A, PR_CONTAINER_CLASS_W</span></span>  <br/> |
|<span data-ttu-id="c44ca-109">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="c44ca-109">Identifier:</span></span>  <br/> |<span data-ttu-id="c44ca-110">0x3613</span><span class="sxs-lookup"><span data-stu-id="c44ca-110">0x3613</span></span>  <br/> |
|<span data-ttu-id="c44ca-111">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="c44ca-111">Data type:</span></span>  <br/> |<span data-ttu-id="c44ca-112">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c44ca-112">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="c44ca-113">Область:</span><span class="sxs-lookup"><span data-stu-id="c44ca-113">Area:</span></span>  <br/> |<span data-ttu-id="c44ca-114">Container</span><span class="sxs-lookup"><span data-stu-id="c44ca-114">Container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c44ca-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="c44ca-115">Remarks</span></span>

<span data-ttu-id="c44ca-116">Эти свойства обычно не используются сервером Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="c44ca-116">These properties are not normally used by Exchange Server.</span></span> <span data-ttu-id="c44ca-117">Однако Microsoft Office Outlook® присоединяет их к папкам почтовых ящиков.</span><span class="sxs-lookup"><span data-stu-id="c44ca-117">However, Microsoft Office Outlook® attaches them to mailbox folders.</span></span> <span data-ttu-id="c44ca-118">Кроме того, версии сервера Exchange Server до Exchange Server 2003 почтовых ящиков могут неправильно обрабатывать папки, не имеющие этих свойств.</span><span class="sxs-lookup"><span data-stu-id="c44ca-118">In addition, versions of Exchange Server prior to Exchange Server 2003 Mailbox Manager might incorrectly handle folders that do not have these properties.</span></span>
  
<span data-ttu-id="c44ca-119">Этим свойствам можно присвоить строковые значения в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="c44ca-119">These properties can be assigned the string values in the following table.</span></span>
  
|<span data-ttu-id="c44ca-120">**Значение**</span><span class="sxs-lookup"><span data-stu-id="c44ca-120">**Value**</span></span>|<span data-ttu-id="c44ca-121">**Содержимое папки**</span><span class="sxs-lookup"><span data-stu-id="c44ca-121">**Contents of Folder**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c44ca-122">Кросс. События</span><span class="sxs-lookup"><span data-stu-id="c44ca-122">IPF.Appointment</span></span>  <br/> |<span data-ttu-id="c44ca-123">Встречи</span><span class="sxs-lookup"><span data-stu-id="c44ca-123">Appointments</span></span>  <br/> |
|<span data-ttu-id="c44ca-124">Кросс. Лицу</span><span class="sxs-lookup"><span data-stu-id="c44ca-124">IPF.Contact</span></span>  <br/> |<span data-ttu-id="c44ca-125">Контакты</span><span class="sxs-lookup"><span data-stu-id="c44ca-125">Contacts</span></span>  <br/> |
|<span data-ttu-id="c44ca-126">Кросс. Фин</span><span class="sxs-lookup"><span data-stu-id="c44ca-126">IPF.Journal</span></span>  <br/> |<span data-ttu-id="c44ca-127">Записи дневника Outlook</span><span class="sxs-lookup"><span data-stu-id="c44ca-127">Outlook Journal entries</span></span>  <br/> |
|<span data-ttu-id="c44ca-128">Кросс. Ноте</span><span class="sxs-lookup"><span data-stu-id="c44ca-128">IPF.Note</span></span>  <br/> |<span data-ttu-id="c44ca-129">Почтовые сообщения и заметки</span><span class="sxs-lookup"><span data-stu-id="c44ca-129">Mail Messages and notes</span></span>  <br/> |
|<span data-ttu-id="c44ca-130">Кросс. стиккиноте</span><span class="sxs-lookup"><span data-stu-id="c44ca-130">IPF.StickyNote</span></span>  <br/> |<span data-ttu-id="c44ca-131">Outlook для клейких заметок</span><span class="sxs-lookup"><span data-stu-id="c44ca-131">Outlook Sticky Notes</span></span>  <br/> |
|<span data-ttu-id="c44ca-132">Кросс. Ее</span><span class="sxs-lookup"><span data-stu-id="c44ca-132">IPF.Task</span></span>  <br/> |<span data-ttu-id="c44ca-133">Задачи Outlook</span><span class="sxs-lookup"><span data-stu-id="c44ca-133">Outlook Tasks</span></span>  <br/> |
   
<span data-ttu-id="c44ca-134">Для папок, содержащих почтовые сообщения, эти свойства должны иметь значение IPF. Ноте.</span><span class="sxs-lookup"><span data-stu-id="c44ca-134">For folders that contain mail messages, these properties should be set to IPF.Note.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c44ca-135">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c44ca-135">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c44ca-136">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="c44ca-136">Protocol specifications</span></span>

<span data-ttu-id="c44ca-137">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c44ca-137">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c44ca-138">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="c44ca-138">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c44ca-139">[[MS — ОКСОСФЛД]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c44ca-139">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c44ca-140">Задает свойства и операции для создания и поиска специальных папок в почтовом ящике.</span><span class="sxs-lookup"><span data-stu-id="c44ca-140">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="c44ca-141">[[MS — ОКСОКАЛ]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c44ca-141">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c44ca-142">Задает свойства и операции для встречи, приглашения на собрание и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="c44ca-142">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="c44ca-143">[[MS — ОКСОКНТК]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c44ca-143">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c44ca-144">Задает свойства и операции, которые являются допустимыми для объектов контакта и личного списка рассылки.</span><span class="sxs-lookup"><span data-stu-id="c44ca-144">Specifies the properties and operations that are permissible for contact and personal distribution list objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c44ca-145">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="c44ca-145">Header files</span></span>

<span data-ttu-id="c44ca-146">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="c44ca-146">Mapidefs.h</span></span>
  
> <span data-ttu-id="c44ca-147">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="c44ca-147">Provides data type definitions.</span></span>
    
<span data-ttu-id="c44ca-148">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="c44ca-148">Mapitags.h</span></span>
  
> <span data-ttu-id="c44ca-149">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="c44ca-149">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c44ca-150">См. также</span><span class="sxs-lookup"><span data-stu-id="c44ca-150">See also</span></span>



[<span data-ttu-id="c44ca-151">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c44ca-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c44ca-152">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="c44ca-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c44ca-153">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="c44ca-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c44ca-154">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="c44ca-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

