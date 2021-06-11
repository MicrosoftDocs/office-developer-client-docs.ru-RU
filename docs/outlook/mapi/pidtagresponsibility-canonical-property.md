---
title: Каноническое свойство PidTagResponsibility
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResponsibility
api_type:
- COM
ms.assetid: 1e8ccef1-db0a-4230-9bd0-87540b53e890
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 15bf61e71a2c230f7891c738661f839ecddb52e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330123"
---
# <a name="pidtagresponsibility-canonical-property"></a><span data-ttu-id="676c7-103">Каноническое свойство PidTagResponsibility</span><span class="sxs-lookup"><span data-stu-id="676c7-103">PidTagResponsibility Canonical Property</span></span>

  
  
<span data-ttu-id="676c7-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="676c7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="676c7-105">Содержит TRUE, если какой-либо поставщик транспорта уже принял на себя ответственность за доставку сообщения этому получателю, и FALSE, если шпалер MAPI считает, что этот поставщик транспорта должен взять на себя ответственность.</span><span class="sxs-lookup"><span data-stu-id="676c7-105">Contains TRUE if some transport provider has already accepted responsibility for delivering the message to this recipient, and FALSE if the MAPI spooler considers that this transport provider should accept responsibility.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="676c7-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="676c7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="676c7-107">PR_RESPONSIBILITY</span><span class="sxs-lookup"><span data-stu-id="676c7-107">PR_RESPONSIBILITY</span></span>  <br/> |
|<span data-ttu-id="676c7-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="676c7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="676c7-109">0x0E0F</span><span class="sxs-lookup"><span data-stu-id="676c7-109">0x0E0F</span></span>  <br/> |
|<span data-ttu-id="676c7-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="676c7-110">Data type:</span></span>  <br/> |<span data-ttu-id="676c7-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="676c7-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="676c7-112">Область:</span><span class="sxs-lookup"><span data-stu-id="676c7-112">Area:</span></span>  <br/> |<span data-ttu-id="676c7-113">MAPI, не передаваемая</span><span class="sxs-lookup"><span data-stu-id="676c7-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="676c7-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="676c7-114">Remarks</span></span>

<span data-ttu-id="676c7-115">Когда spooler MAPI представляет исходящие сообщения поставщику транспорта, через [IXPLogon::SubmitMessage,](ixplogon-submitmessage.md)он задает это свойство FALSE для всех получателей, для которых spooler MAPI считает, что поставщик транспорта несет ответственность, и TRUE для всех других получателей.</span><span class="sxs-lookup"><span data-stu-id="676c7-115">When the MAPI spooler presents an outbound message to a transport provider, through [IXPLogon::SubmitMessage](ixplogon-submitmessage.md), it sets this property to FALSE for all recipients for which the MAPI spooler considers that transport provider responsible, and TRUE for all other recipients.</span></span> <span data-ttu-id="676c7-116">Поставщик транспорта должен попытаться обработать всех получателей с **PR_RESPONSIBILITY** для false.</span><span class="sxs-lookup"><span data-stu-id="676c7-116">The transport provider should attempt to handle all recipients with **PR_RESPONSIBILITY** set to FALSE.</span></span> <span data-ttu-id="676c7-117">После успешной отправки получателю или его неспособности, поставщик транспорта должен установить это свойство true в исходных сообщениях, чтобы указать, что он принял на себя ответственность за этого получателя.</span><span class="sxs-lookup"><span data-stu-id="676c7-117">After successfully sending, or conclusively failing to send, to a recipient, the transport provider should set this property to TRUE in the source message to indicate that it has accepted responsibility for that recipient.</span></span> 
  
<span data-ttu-id="676c7-118">Если после осмотра получателя поставщик транспорта решает, что он не может или  не должен с ним обращаться, поставщик транспорта должен оставить PR_RESPONSIBILITY установлено false.</span><span class="sxs-lookup"><span data-stu-id="676c7-118">If, after examining a recipient, a transport provider decides that it cannot or should not handle it, the transport provider should leave **PR_RESPONSIBILITY** set to FALSE.</span></span> <span data-ttu-id="676c7-119">Затем шпалер MAPI будет искать другого поставщика транспорта, который может обрабатывать этого получателя.</span><span class="sxs-lookup"><span data-stu-id="676c7-119">The MAPI spooler will then look for another transport provider that can handle that recipient.</span></span> <span data-ttu-id="676c7-120">Пульпер MAPI в конечном счете создает отчет о неделивости для всех получателей, за которые ни один поставщик транспорта не принимает на себя ответственность.</span><span class="sxs-lookup"><span data-stu-id="676c7-120">The MAPI spooler ultimately creates a nondelivery report for any recipients for which no transport provider accepts responsibility.</span></span> 
  
<span data-ttu-id="676c7-121">Если поставщик транспорта пытается и не доставляет сообщение, он должен вызвать метод [IMAPISupport::StatusRecips,](imapisupport-statusrecips.md) чтобы указать MAPI причины сбоя, чтобы MAPI могли создавать отчет о неделивости.</span><span class="sxs-lookup"><span data-stu-id="676c7-121">If the transport provider attempts and fails to deliver the message, it should call the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method to indicate to MAPI the reasons for the failure, so that MAPI can generate a nondelivery report.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="676c7-122">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="676c7-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="676c7-123">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="676c7-123">Protocol specifications</span></span>

<span data-ttu-id="676c7-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="676c7-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="676c7-125">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="676c7-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="676c7-126">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="676c7-126">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="676c7-127">Обрабатывает порядок и поток передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="676c7-127">Handles the order and flow for data transfers between a client and server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="676c7-128">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="676c7-128">Header files</span></span>

<span data-ttu-id="676c7-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="676c7-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="676c7-130">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="676c7-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="676c7-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="676c7-131">Mapitags.h</span></span>
  
> <span data-ttu-id="676c7-132">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="676c7-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="676c7-133">См. также</span><span class="sxs-lookup"><span data-stu-id="676c7-133">See also</span></span>



[<span data-ttu-id="676c7-134">������������ �������� PidTagDeleteAfterSubmit</span><span class="sxs-lookup"><span data-stu-id="676c7-134">PidTagDeleteAfterSubmit Canonical Property</span></span>](pidtagdeleteaftersubmit-canonical-property.md)


[<span data-ttu-id="676c7-135">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="676c7-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="676c7-136">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="676c7-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="676c7-137">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="676c7-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="676c7-138">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="676c7-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

