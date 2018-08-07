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
ms.openlocfilehash: 9dba26ab6948d7190521ff31a8732c4b058ab7c9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811739"
---
# <a name="pidtagresponsibility-canonical-property"></a><span data-ttu-id="4e236-103">Каноническое свойство PidTagResponsibility</span><span class="sxs-lookup"><span data-stu-id="4e236-103">PidTagResponsibility Canonical Property</span></span>

  
  
<span data-ttu-id="4e236-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4e236-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4e236-105">Содержит значение TRUE, если некоторые поставщика транспорта уже принял ответственность за доставки сообщения для получателя и FALSE, если диспетчер очереди MAPI учитывает принятие данного поставщика транспорта ответственности.</span><span class="sxs-lookup"><span data-stu-id="4e236-105">Contains TRUE if some transport provider has already accepted responsibility for delivering the message to this recipient, and FALSE if the MAPI spooler considers that this transport provider should accept responsibility.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4e236-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="4e236-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4e236-107">PR_RESPONSIBILITY</span><span class="sxs-lookup"><span data-stu-id="4e236-107">PR_RESPONSIBILITY</span></span>  <br/> |
|<span data-ttu-id="4e236-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="4e236-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4e236-109">0x0E0F</span><span class="sxs-lookup"><span data-stu-id="4e236-109">0x0E0F</span></span>  <br/> |
|<span data-ttu-id="4e236-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="4e236-110">Data type:</span></span>  <br/> |<span data-ttu-id="4e236-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="4e236-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="4e236-112">Область:</span><span class="sxs-lookup"><span data-stu-id="4e236-112">Area:</span></span>  <br/> |<span data-ttu-id="4e236-113">MAPI передаваемого</span><span class="sxs-lookup"><span data-stu-id="4e236-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4e236-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="4e236-114">Remarks</span></span>

<span data-ttu-id="4e236-115">При диспетчер очереди MAPI представляет исходящее сообщение поставщика транспорта, через [IXPLogon::SubmitMessage](ixplogon-submitmessage.md)его этому свойству значение FALSE для всех получателей, для которых диспетчер очереди MAPI учитывает этого поставщика транспорта ответственность и значение TRUE для всех получатели.</span><span class="sxs-lookup"><span data-stu-id="4e236-115">When the MAPI spooler presents an outbound message to a transport provider, through [IXPLogon::SubmitMessage](ixplogon-submitmessage.md), it sets this property to FALSE for all recipients for which the MAPI spooler considers that transport provider responsible, and TRUE for all other recipients.</span></span> <span data-ttu-id="4e236-116">Поставщика транспорта производится попытка обработки всех получателей с **PR_RESPONSIBILITY** задано значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="4e236-116">The transport provider should attempt to handle all recipients with **PR_RESPONSIBILITY** set to FALSE.</span></span> <span data-ttu-id="4e236-117">После успешной отправки или conclusively восстановления после сбоя для отправки получателю, поставщика транспорта следует этому свойству присвоено значение TRUE в сообщении источник, чтобы указать, что ответственность за этот получатель принял.</span><span class="sxs-lookup"><span data-stu-id="4e236-117">After successfully sending, or conclusively failing to send, to a recipient, the transport provider should set this property to TRUE in the source message to indicate that it has accepted responsibility for that recipient.</span></span> 
  
<span data-ttu-id="4e236-118">Если после проверки получателя, поставщика транспорта решает, что не может или не должен обрабатывать, поставщика транспорта, следует оставить **PR_RESPONSIBILITY** set значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="4e236-118">If, after examining a recipient, a transport provider decides that it cannot or should not handle it, the transport provider should leave **PR_RESPONSIBILITY** set to FALSE.</span></span> <span data-ttu-id="4e236-119">Диспетчер очереди MAPI будет искать другого поставщика транспорта, который может обрабатывать получателя.</span><span class="sxs-lookup"><span data-stu-id="4e236-119">The MAPI spooler will then look for another transport provider that can handle that recipient.</span></span> <span data-ttu-id="4e236-120">Диспетчер очереди MAPI в конечном счете создает отчет о недоставке для получателей, для которых отсутствует транспорт принимает ответственности.</span><span class="sxs-lookup"><span data-stu-id="4e236-120">The MAPI spooler ultimately creates a nondelivery report for any recipients for which no transport provider accepts responsibility.</span></span> 
  
<span data-ttu-id="4e236-121">Если поставщика транспорта пытается и не удается доставить сообщение, он должен вызвать метод [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) для указания MAPI причины сбоя, чтобы MAPI можно создать отчет о недоставке.</span><span class="sxs-lookup"><span data-stu-id="4e236-121">If the transport provider attempts and fails to deliver the message, it should call the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method to indicate to MAPI the reasons for the failure, so that MAPI can generate a nondelivery report.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="4e236-122">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="4e236-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4e236-123">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="4e236-123">Protocol specifications</span></span>

<span data-ttu-id="4e236-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4e236-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4e236-125">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="4e236-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4e236-126">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4e236-126">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4e236-127">Обрабатывает порядок и поток для передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="4e236-127">Handles the order and flow for data transfers between a client and server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4e236-128">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="4e236-128">Header files</span></span>

<span data-ttu-id="4e236-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4e236-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="4e236-130">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="4e236-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="4e236-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4e236-131">Mapitags.h</span></span>
  
> <span data-ttu-id="4e236-132">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="4e236-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4e236-133">См. также</span><span class="sxs-lookup"><span data-stu-id="4e236-133">See also</span></span>



[<span data-ttu-id="4e236-134">������������ �������� PidTagDeleteAfterSubmit</span><span class="sxs-lookup"><span data-stu-id="4e236-134">PidTagDeleteAfterSubmit Canonical Property</span></span>](pidtagdeleteaftersubmit-canonical-property.md)


[<span data-ttu-id="4e236-135">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="4e236-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4e236-136">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="4e236-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4e236-137">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="4e236-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4e236-138">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="4e236-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

