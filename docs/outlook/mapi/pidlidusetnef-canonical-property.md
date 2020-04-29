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
# <a name="pidlidusetnef-canonical-property"></a><span data-ttu-id="4a48f-103">Каноническое свойство PidLidUseTnef</span><span class="sxs-lookup"><span data-stu-id="4a48f-103">PidLidUseTnef Canonical Property</span></span>

  
  
<span data-ttu-id="4a48f-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4a48f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4a48f-105">Указывает, следует ли включать в сообщение формат TNEF, если сообщение преобразуется из формата MAPI в формат MIME или SMTP (Simple Mail Transfer Protocol).</span><span class="sxs-lookup"><span data-stu-id="4a48f-105">Specifies whether Transport Neutral Encapsulation Format (TNEF) should be included on a message when that message is converted from MAPI to Multipurpose Internet Mail Extensions (MIME) or Simple Mail Transfer Protocol (SMTP) format.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4a48f-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="4a48f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4a48f-107">диспидусетнеф</span><span class="sxs-lookup"><span data-stu-id="4a48f-107">dispidUseTNEF</span></span>  <br/> |
|<span data-ttu-id="4a48f-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="4a48f-108">Property set:</span></span>  <br/> |<span data-ttu-id="4a48f-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="4a48f-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="4a48f-110">Длинный идентификатор (крышка):</span><span class="sxs-lookup"><span data-stu-id="4a48f-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="4a48f-111">0x00008582</span><span class="sxs-lookup"><span data-stu-id="4a48f-111">0x00008582</span></span>  <br/> |
|<span data-ttu-id="4a48f-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="4a48f-112">Data type:</span></span>  <br/> |<span data-ttu-id="4a48f-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="4a48f-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="4a48f-114">Область:</span><span class="sxs-lookup"><span data-stu-id="4a48f-114">Area:</span></span>  <br/> |<span data-ttu-id="4a48f-115">Настройка времени выполнения</span><span class="sxs-lookup"><span data-stu-id="4a48f-115">Run-time configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4a48f-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="4a48f-116">Remarks</span></span>

<span data-ttu-id="4a48f-117">Данное свойство указывает, следует ли включать TNEF в сообщение при преобразовании сообщения из формата TNEF в формат MIME или SMTP.</span><span class="sxs-lookup"><span data-stu-id="4a48f-117">This property specifies whether TNEF should be included on a message when that message is converted from TNEF to MIME or SMTP format.</span></span> <span data-ttu-id="4a48f-118">Это свойство может отсутствовать, и если да, то не требуется включать в сообщение TNEF.</span><span class="sxs-lookup"><span data-stu-id="4a48f-118">This property may be absent, and if so, TNEF must not be included on the message.</span></span>
  
<span data-ttu-id="4a48f-119">Это свойство применяется только в том случае, если сообщение отправлено с учетной записи электронной почты POP3/SMTP и не применяется при отправке сообщения другими поставщиками, такими как Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="4a48f-119">This property only applies when the message is sent from a POP3/SMTP mail account and does not apply when the message is sent by other providers, such as Microsoft Exchange Server.</span></span>
  
<span data-ttu-id="4a48f-120">В определенных обстоятельствах, например при включении кнопок голосования или при присоединении к сообщению внедренного объекта OLE, Outlook может установить это свойство, чтобы принудительно использовать формат TNEF.</span><span class="sxs-lookup"><span data-stu-id="4a48f-120">Under certain circumstances, such as when voting buttons are enabled or an OLE embedded object is attached to a message, Outlook can set this property to force the use of TNEF.</span></span>
  
<span data-ttu-id="4a48f-121">Свойство **PR_MSG_EDITOR_FORMAT** ([PidTagMessageEditorFormat](pidtagmessageeditorformat-canonical-property.md)) можно использовать для принудительного применения только обычного текста, а не TNEF при отправке сообщения.</span><span class="sxs-lookup"><span data-stu-id="4a48f-121">The **PR_MSG_EDITOR_FORMAT** ([PidTagMessageEditorFormat](pidtagmessageeditorformat-canonical-property.md)) property can be used to enforce only plain text, and not TNEF, when sending a message.</span></span> <span data-ttu-id="4a48f-122">Так как **PidLidUseTNEF** переопределяет параметр в **PR_MSG_EDITOR_FORMAT**, то приложение, которое требуется принудительно использовать обычный текст в исходящих сообщениях, также должно искать **PidLidUseTNEF** и сбрасывать его в значение false.</span><span class="sxs-lookup"><span data-stu-id="4a48f-122">Because **PidLidUseTNEF** overrides the setting in **PR_MSG_EDITOR_FORMAT**, an application that wants to force plain text on an outgoing message should also look for **PidLidUseTNEF** and reset it to FALSE.</span></span> <span data-ttu-id="4a48f-123">Кроме того, надстройка должна удалить функции сообщений, которые требовали формат TNEF, чтобы избежать непригодных для отправки сообщений.</span><span class="sxs-lookup"><span data-stu-id="4a48f-123">Additionally, the add-in must remove the message features that required TNEF to avoid unusable attachments on the message that is finally sent.</span></span> 
  
<span data-ttu-id="4a48f-124">Используйте флаг **CCSF_USE_TNEF** при вызове [Иконвертерсессион:: мапитомиместм](iconvertersession-mapitomimestm.md) для преобразования исходящего сообщения MAPI в MIME поток также может применять TNEF.</span><span class="sxs-lookup"><span data-stu-id="4a48f-124">Use the **CCSF_USE_TNEF** flag when calling [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) to convert an outgoing MAPI message to a MIME stream can also enforce TNEF.</span></span> <span data-ttu-id="4a48f-125">Это свойство применяется, даже если **PidLidUseTNEF** не задано.</span><span class="sxs-lookup"><span data-stu-id="4a48f-125">This applies even if **PidLidUseTNEF** is not set.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="4a48f-126">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="4a48f-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4a48f-127">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="4a48f-127">Protocol specifications</span></span>

<span data-ttu-id="4a48f-128">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4a48f-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4a48f-129">Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="4a48f-129">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4a48f-130">[[MS — ОКСОМСГ]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4a48f-130">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4a48f-131">Задает свойства и операции, допустимые для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="4a48f-131">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="4a48f-132">[[MS — ОКСТНЕФ]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4a48f-132">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4a48f-133">Кодирует и декодирует объекты сообщений и вложений в эффективное потоковое представление.</span><span class="sxs-lookup"><span data-stu-id="4a48f-133">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4a48f-134">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="4a48f-134">Header files</span></span>

<span data-ttu-id="4a48f-135">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="4a48f-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="4a48f-136">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="4a48f-136">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4a48f-137">См. также</span><span class="sxs-lookup"><span data-stu-id="4a48f-137">See also</span></span>



[<span data-ttu-id="4a48f-138">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="4a48f-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4a48f-139">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="4a48f-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4a48f-140">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="4a48f-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4a48f-141">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="4a48f-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

