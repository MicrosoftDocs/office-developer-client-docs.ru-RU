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
ms.openlocfilehash: 73fa4311a61be9259d8c45aca79d719785c213a6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810660"
---
# <a name="pidlidusetnef-canonical-property"></a><span data-ttu-id="112a5-103">Каноническое свойство PidLidUseTnef</span><span class="sxs-lookup"><span data-stu-id="112a5-103">PidLidUseTnef Canonical Property</span></span>

  
  
<span data-ttu-id="112a5-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="112a5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="112a5-105">Указывает, следует ли включать транспорта Neutral Encapsulation формата TNEF на сообщение при преобразовании этого сообщения из MAPI в формат Multipurpose Internet Mail Extensions (MIME) или Simple Mail Transfer Protocol (SMTP).</span><span class="sxs-lookup"><span data-stu-id="112a5-105">Specifies whether Transport Neutral Encapsulation Format (TNEF) should be included on a message when that message is converted from MAPI to Multipurpose Internet Mail Extensions (MIME) or Simple Mail Transfer Protocol (SMTP) format.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="112a5-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="112a5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="112a5-107">dispidUseTNEF</span><span class="sxs-lookup"><span data-stu-id="112a5-107">dispidUseTNEF</span></span>  <br/> |
|<span data-ttu-id="112a5-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="112a5-108">Property set:</span></span>  <br/> |<span data-ttu-id="112a5-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="112a5-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="112a5-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="112a5-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="112a5-111">0x00008582</span><span class="sxs-lookup"><span data-stu-id="112a5-111">0x00008582</span></span>  <br/> |
|<span data-ttu-id="112a5-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="112a5-112">Data type:</span></span>  <br/> |<span data-ttu-id="112a5-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="112a5-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="112a5-114">Область:</span><span class="sxs-lookup"><span data-stu-id="112a5-114">Area:</span></span>  <br/> |<span data-ttu-id="112a5-115">Конфигурация во время выполнения</span><span class="sxs-lookup"><span data-stu-id="112a5-115">Run-time configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="112a5-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="112a5-116">Remarks</span></span>

<span data-ttu-id="112a5-117">Это свойство определяет, следует ли включать TNEF на сообщение при преобразовании этого сообщения из формата TNEF в формате MIME или SMTP.</span><span class="sxs-lookup"><span data-stu-id="112a5-117">This property specifies whether TNEF should be included on a message when that message is converted from TNEF to MIME or SMTP format.</span></span> <span data-ttu-id="112a5-118">Это свойство может отсутствовать, и если да, TNEF не должны быть включены в окне сообщения.</span><span class="sxs-lookup"><span data-stu-id="112a5-118">This property may be absent, and if so, TNEF must not be included on the message.</span></span>
  
<span data-ttu-id="112a5-119">Это свойство применяется только в том случае, когда сообщение отправляется с учетной записью электронной почты POP3/SMTP и не применяется, если сообщение отправляется с другими поставщиками, такими как Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="112a5-119">This property only applies when the message is sent from a POP3/SMTP mail account and does not apply when the message is sent by other providers, such as Microsoft Exchange Server.</span></span>
  
<span data-ttu-id="112a5-120">При определенных условиях, например, при голосования активируются кнопки или внедренные OLE объекта присоединены к сообщению Outlook этому свойству можно задать для принудительного использования формата TNEF.</span><span class="sxs-lookup"><span data-stu-id="112a5-120">Under certain circumstances, such as when voting buttons are enabled or an OLE embedded object is attached to a message, Outlook can set this property to force the use of TNEF.</span></span>
  
<span data-ttu-id="112a5-121">Свойство **PR_MSG_EDITOR_FORMAT** ([PidTagMessageEditorFormat](pidtagmessageeditorformat-canonical-property.md)) можно использовать для применения параметров только обычный текст и не TNEF при отправке сообщения.</span><span class="sxs-lookup"><span data-stu-id="112a5-121">The **PR_MSG_EDITOR_FORMAT** ([PidTagMessageEditorFormat](pidtagmessageeditorformat-canonical-property.md)) property can be used to enforce only plain text, and not TNEF, when sending a message.</span></span> <span data-ttu-id="112a5-122">Так как **PidLidUseTNEF** переопределяет параметр **PR_MSG_EDITOR_FORMAT**, приложение, которое хочет принудительное обычного текста на исходящие сообщения следует искать **PidLidUseTNEF** и сбросить значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="112a5-122">Because **PidLidUseTNEF** overrides the setting in **PR_MSG_EDITOR_FORMAT**, an application that wants to force plain text on an outgoing message should also look for **PidLidUseTNEF** and reset it to FALSE.</span></span> <span data-ttu-id="112a5-123">Кроме того надстройки необходимо удалить функции сообщения, которые требуется TNEF во избежание могут использовать вложения в сообщение, которое отправляется и, наконец.</span><span class="sxs-lookup"><span data-stu-id="112a5-123">Additionally, the add-in must remove the message features that required TNEF to avoid unusable attachments on the message that is finally sent.</span></span> 
  
<span data-ttu-id="112a5-124">Использование флаг **CCSF_USE_TNEF** при вызове [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) для преобразования исходящих сообщений MAPI в MIME-поток также обеспечивают TNEF.</span><span class="sxs-lookup"><span data-stu-id="112a5-124">Use the **CCSF_USE_TNEF** flag when calling [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) to convert an outgoing MAPI message to a MIME stream can also enforce TNEF.</span></span> <span data-ttu-id="112a5-125">Это относится даже в том случае, если не указано **PidLidUseTNEF** .</span><span class="sxs-lookup"><span data-stu-id="112a5-125">This applies even if **PidLidUseTNEF** is not set.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="112a5-126">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="112a5-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="112a5-127">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="112a5-127">Protocol specifications</span></span>

<span data-ttu-id="112a5-128">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="112a5-128">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="112a5-129">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="112a5-129">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="112a5-130">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="112a5-130">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="112a5-131">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="112a5-131">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="112a5-132">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="112a5-132">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="112a5-133">Кодирует и декодирует объекты сообщения и вложения в представление эффективным потока.</span><span class="sxs-lookup"><span data-stu-id="112a5-133">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="112a5-134">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="112a5-134">Header files</span></span>

<span data-ttu-id="112a5-135">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="112a5-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="112a5-136">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="112a5-136">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="112a5-137">См. также</span><span class="sxs-lookup"><span data-stu-id="112a5-137">See also</span></span>



[<span data-ttu-id="112a5-138">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="112a5-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="112a5-139">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="112a5-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="112a5-140">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="112a5-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="112a5-141">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="112a5-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

