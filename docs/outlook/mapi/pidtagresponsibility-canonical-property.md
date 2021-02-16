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
# <a name="pidtagresponsibility-canonical-property"></a><span data-ttu-id="2b850-103">Каноническое свойство PidTagResponsibility</span><span class="sxs-lookup"><span data-stu-id="2b850-103">PidTagResponsibility Canonical Property</span></span>

  
  
<span data-ttu-id="2b850-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2b850-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2b850-105">Содержит true, если какой-либо поставщик транспорта уже принял на себя ответственность за доставку сообщения этому получателю, и FALSE, если пулер MAPI считает, что этот поставщик транспорта должен взять на себя ответственность.</span><span class="sxs-lookup"><span data-stu-id="2b850-105">Contains TRUE if some transport provider has already accepted responsibility for delivering the message to this recipient, and FALSE if the MAPI spooler considers that this transport provider should accept responsibility.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2b850-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="2b850-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2b850-107">PR_RESPONSIBILITY</span><span class="sxs-lookup"><span data-stu-id="2b850-107">PR_RESPONSIBILITY</span></span>  <br/> |
|<span data-ttu-id="2b850-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="2b850-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2b850-109">0x0E0F</span><span class="sxs-lookup"><span data-stu-id="2b850-109">0x0E0F</span></span>  <br/> |
|<span data-ttu-id="2b850-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="2b850-110">Data type:</span></span>  <br/> |<span data-ttu-id="2b850-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="2b850-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="2b850-112">Область:</span><span class="sxs-lookup"><span data-stu-id="2b850-112">Area:</span></span>  <br/> |<span data-ttu-id="2b850-113">MAPI, не передаваемый</span><span class="sxs-lookup"><span data-stu-id="2b850-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2b850-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="2b850-114">Remarks</span></span>

<span data-ttu-id="2b850-115">Когда пулер MAPI представляет исходящие сообщения поставщику транспорта через [IXPLogon::SubmitMessage,](ixplogon-submitmessage.md)он устанавливает для этого свойства false для всех получателей, для которых пулер MAPI считает, что этот поставщик транспорта отвечает, и TRUE для всех остальных получателей.</span><span class="sxs-lookup"><span data-stu-id="2b850-115">When the MAPI spooler presents an outbound message to a transport provider, through [IXPLogon::SubmitMessage](ixplogon-submitmessage.md), it sets this property to FALSE for all recipients for which the MAPI spooler considers that transport provider responsible, and TRUE for all other recipients.</span></span> <span data-ttu-id="2b850-116">Поставщик транспорта должен попытаться обработать всех получателей с PR_RESPONSIBILITY **false.**</span><span class="sxs-lookup"><span data-stu-id="2b850-116">The transport provider should attempt to handle all recipients with **PR_RESPONSIBILITY** set to FALSE.</span></span> <span data-ttu-id="2b850-117">После успешной отправки или неудачной отправки получателю поставщик транспорта должен установить для этого свойства в текстовом сообщении true, чтобы указать, что он несет ответственность за этого получателя.</span><span class="sxs-lookup"><span data-stu-id="2b850-117">After successfully sending, or conclusively failing to send, to a recipient, the transport provider should set this property to TRUE in the source message to indicate that it has accepted responsibility for that recipient.</span></span> 
  
<span data-ttu-id="2b850-118">Если после проверки получателя поставщик транспорта решает, что не может или не  должен обработать его, поставщик транспорта должен оставить PR_RESPONSIBILITY false.</span><span class="sxs-lookup"><span data-stu-id="2b850-118">If, after examining a recipient, a transport provider decides that it cannot or should not handle it, the transport provider should leave **PR_RESPONSIBILITY** set to FALSE.</span></span> <span data-ttu-id="2b850-119">Затем пулер MAPI будет искать другого поставщика транспорта, который может обработать этого получателя.</span><span class="sxs-lookup"><span data-stu-id="2b850-119">The MAPI spooler will then look for another transport provider that can handle that recipient.</span></span> <span data-ttu-id="2b850-120">Пулер MAPI создает отчет о ненастройке для всех получателей, ответственность за которые не несет ни один поставщик транспорта.</span><span class="sxs-lookup"><span data-stu-id="2b850-120">The MAPI spooler ultimately creates a nondelivery report for any recipients for which no transport provider accepts responsibility.</span></span> 
  
<span data-ttu-id="2b850-121">Если поставщик транспорта пытается доставить сообщение, он должен вызвать метод [IMAPISupport::StatusRecips,](imapisupport-statusrecips.md) чтобы указать MAPI причины сбоя, чтобы MAPI смог создать отчет о ненастройстве.</span><span class="sxs-lookup"><span data-stu-id="2b850-121">If the transport provider attempts and fails to deliver the message, it should call the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method to indicate to MAPI the reasons for the failure, so that MAPI can generate a nondelivery report.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="2b850-122">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="2b850-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2b850-123">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="2b850-123">Protocol specifications</span></span>

<span data-ttu-id="2b850-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2b850-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2b850-125">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="2b850-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2b850-126">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2b850-126">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2b850-127">Обрабатывает порядок и поток передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="2b850-127">Handles the order and flow for data transfers between a client and server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2b850-128">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="2b850-128">Header files</span></span>

<span data-ttu-id="2b850-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2b850-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="2b850-130">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="2b850-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="2b850-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2b850-131">Mapitags.h</span></span>
  
> <span data-ttu-id="2b850-132">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="2b850-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2b850-133">См. также</span><span class="sxs-lookup"><span data-stu-id="2b850-133">See also</span></span>



[<span data-ttu-id="2b850-134">������������ �������� PidTagDeleteAfterSubmit</span><span class="sxs-lookup"><span data-stu-id="2b850-134">PidTagDeleteAfterSubmit Canonical Property</span></span>](pidtagdeleteaftersubmit-canonical-property.md)


[<span data-ttu-id="2b850-135">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="2b850-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2b850-136">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="2b850-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2b850-137">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="2b850-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2b850-138">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="2b850-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

