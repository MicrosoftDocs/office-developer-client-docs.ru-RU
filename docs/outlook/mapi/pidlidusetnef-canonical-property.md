---
title: Каноническое свойство PidLidUseTnef
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidUseTnef
api_type:
- COM
ms.assetid: 954048d6-e2eb-43e7-b52c-c2f047bb84a4
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 56f6e2355ee2e64cc766bafe27cd59454e210ab6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315423"
---
# <a name="pidlidusetnef-canonical-property"></a><span data-ttu-id="5decd-103">Каноническое свойство PidLidUseTnef</span><span class="sxs-lookup"><span data-stu-id="5decd-103">PidLidUseTnef Canonical Property</span></span>

  
  
<span data-ttu-id="5decd-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5decd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5decd-105">Указывает, следует ли включить формат транспортной нейтральной инкапсуляции (TNEF) в сообщение при преобразовании этого сообщения из MAPI в многоцелевые расширения интернет-почты (MIME) или простой протокол передачи почты (SMTP).</span><span class="sxs-lookup"><span data-stu-id="5decd-105">Specifies whether Transport Neutral Encapsulation Format (TNEF) should be included on a message when that message is converted from MAPI to Multipurpose Internet Mail Extensions (MIME) or Simple Mail Transfer Protocol (SMTP) format.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5decd-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="5decd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5decd-107">dispidUseTNEF</span><span class="sxs-lookup"><span data-stu-id="5decd-107">dispidUseTNEF</span></span>  <br/> |
|<span data-ttu-id="5decd-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="5decd-108">Property set:</span></span>  <br/> |<span data-ttu-id="5decd-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="5decd-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="5decd-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="5decd-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="5decd-111">0x00008582</span><span class="sxs-lookup"><span data-stu-id="5decd-111">0x00008582</span></span>  <br/> |
|<span data-ttu-id="5decd-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="5decd-112">Data type:</span></span>  <br/> |<span data-ttu-id="5decd-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="5decd-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="5decd-114">Область:</span><span class="sxs-lookup"><span data-stu-id="5decd-114">Area:</span></span>  <br/> |<span data-ttu-id="5decd-115">Конфигурация времени запуска</span><span class="sxs-lookup"><span data-stu-id="5decd-115">Run-time configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5decd-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="5decd-116">Remarks</span></span>

<span data-ttu-id="5decd-117">В этом свойстве указывается, следует ли включить TNEF в сообщение при преобразовании этого сообщения из TNEF в формат MIME или SMTP.</span><span class="sxs-lookup"><span data-stu-id="5decd-117">This property specifies whether TNEF should be included on a message when that message is converted from TNEF to MIME or SMTP format.</span></span> <span data-ttu-id="5decd-118">Это свойство может отсутствовать, и если это так, то TNEF не должен быть включен в сообщение.</span><span class="sxs-lookup"><span data-stu-id="5decd-118">This property may be absent, and if so, TNEF must not be included on the message.</span></span>
  
<span data-ttu-id="5decd-119">Это свойство применяется только тогда, когда сообщение отправляется из почтовой учетной записи POP3/SMTP и не применяется, когда сообщение отправляется другими поставщиками, например Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="5decd-119">This property only applies when the message is sent from a POP3/SMTP mail account and does not apply when the message is sent by other providers, such as Microsoft Exchange Server.</span></span>
  
<span data-ttu-id="5decd-120">При определенных обстоятельствах, например при включении кнопок голосования или присоединении встроенного объекта OLE к сообщению, Outlook может настроить это свойство, чтобы заставить использовать TNEF.</span><span class="sxs-lookup"><span data-stu-id="5decd-120">Under certain circumstances, such as when voting buttons are enabled or an OLE embedded object is attached to a message, Outlook can set this property to force the use of TNEF.</span></span>
  
<span data-ttu-id="5decd-121">Свойство **PR_MSG_EDITOR_FORMAT** [(PidTagMessageEditorFormat)](pidtagmessageeditorformat-canonical-property.md)может использоваться для применения только простого текста, а не TNEF при отправке сообщения.</span><span class="sxs-lookup"><span data-stu-id="5decd-121">The **PR_MSG_EDITOR_FORMAT** ([PidTagMessageEditorFormat](pidtagmessageeditorformat-canonical-property.md)) property can be used to enforce only plain text, and not TNEF, when sending a message.</span></span> <span data-ttu-id="5decd-122">Так как **PidLidUseTNEF** переопределяет параметр в **PR_MSG_EDITOR_FORMAT,** приложение, которое хочет задействовать простой текст в исходяном сообщении, также должно искать **PidLidUseTNEF** и сбросить его в FALSE.</span><span class="sxs-lookup"><span data-stu-id="5decd-122">Because **PidLidUseTNEF** overrides the setting in **PR_MSG_EDITOR_FORMAT**, an application that wants to force plain text on an outgoing message should also look for **PidLidUseTNEF** and reset it to FALSE.</span></span> <span data-ttu-id="5decd-123">Кроме того, надстройка должна удалить функции сообщения, которые требовали TNEF, чтобы избежать неиспользоваемых вложений в отправленное сообщение.</span><span class="sxs-lookup"><span data-stu-id="5decd-123">Additionally, the add-in must remove the message features that required TNEF to avoid unusable attachments on the message that is finally sent.</span></span> 
  
<span data-ttu-id="5decd-124">Использование **флага CCSF_USE_TNEF** при вызове [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) для преобразования исходячего сообщения MAPI в поток MIME также может применять TNEF.</span><span class="sxs-lookup"><span data-stu-id="5decd-124">Use the **CCSF_USE_TNEF** flag when calling [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) to convert an outgoing MAPI message to a MIME stream can also enforce TNEF.</span></span> <span data-ttu-id="5decd-125">Это применимо даже в том **случае, если набор PidLidUseTNEF** не установлен.</span><span class="sxs-lookup"><span data-stu-id="5decd-125">This applies even if **PidLidUseTNEF** is not set.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="5decd-126">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="5decd-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5decd-127">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="5decd-127">Protocol specifications</span></span>

<span data-ttu-id="5decd-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5decd-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5decd-129">Предоставляет определения набора свойств и ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="5decd-129">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5decd-130">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5decd-130">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5decd-131">Указывает свойства и операции, допустимые для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="5decd-131">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="5decd-132">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5decd-132">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5decd-133">Кодирует и декодирует объекты сообщений и вложений в эффективное представление потока.</span><span class="sxs-lookup"><span data-stu-id="5decd-133">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5decd-134">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="5decd-134">Header files</span></span>

<span data-ttu-id="5decd-135">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5decd-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="5decd-136">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="5decd-136">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5decd-137">См. также</span><span class="sxs-lookup"><span data-stu-id="5decd-137">See also</span></span>



[<span data-ttu-id="5decd-138">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="5decd-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5decd-139">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="5decd-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5decd-140">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="5decd-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5decd-141">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="5decd-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

