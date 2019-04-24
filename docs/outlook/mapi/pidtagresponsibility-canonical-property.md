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
# <a name="pidtagresponsibility-canonical-property"></a><span data-ttu-id="eeca5-103">Каноническое свойство PidTagResponsibility</span><span class="sxs-lookup"><span data-stu-id="eeca5-103">PidTagResponsibility Canonical Property</span></span>

  
  
<span data-ttu-id="eeca5-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eeca5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eeca5-105">Содержит значение TRUE, если некоторые поставщики транспорта уже приняли ответственность за доставку сообщения этому получателю, и FALSE, если диспетчер очереди MAPI считает, что этот поставщик транспорта должен принимать ответственность.</span><span class="sxs-lookup"><span data-stu-id="eeca5-105">Contains TRUE if some transport provider has already accepted responsibility for delivering the message to this recipient, and FALSE if the MAPI spooler considers that this transport provider should accept responsibility.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="eeca5-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="eeca5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="eeca5-107">ПР_РЕСПОНСИБИЛИТИ</span><span class="sxs-lookup"><span data-stu-id="eeca5-107">PR_RESPONSIBILITY</span></span>  <br/> |
|<span data-ttu-id="eeca5-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="eeca5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="eeca5-109">0x0E0F</span><span class="sxs-lookup"><span data-stu-id="eeca5-109">0x0E0F</span></span>  <br/> |
|<span data-ttu-id="eeca5-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="eeca5-110">Data type:</span></span>  <br/> |<span data-ttu-id="eeca5-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="eeca5-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="eeca5-112">Область:</span><span class="sxs-lookup"><span data-stu-id="eeca5-112">Area:</span></span>  <br/> |<span data-ttu-id="eeca5-113">Несъемный MAPI</span><span class="sxs-lookup"><span data-stu-id="eeca5-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="eeca5-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="eeca5-114">Remarks</span></span>

<span data-ttu-id="eeca5-115">Когда диспетчер очереди MAPI представляет исходящее сообщение для поставщика транспорта с помощью [иксплогон:: субмитмессаже](ixplogon-submitmessage.md), этому свойству ПРИСВАИВАЕТСЯ значение false для всех получателей, для которых диспетчер очереди MAPI считает его ответственным, и true для всех другие получатели.</span><span class="sxs-lookup"><span data-stu-id="eeca5-115">When the MAPI spooler presents an outbound message to a transport provider, through [IXPLogon::SubmitMessage](ixplogon-submitmessage.md), it sets this property to FALSE for all recipients for which the MAPI spooler considers that transport provider responsible, and TRUE for all other recipients.</span></span> <span data-ttu-id="eeca5-116">Поставщик транспорта должен попытаться обрабатывать всех получателей, у которых для **пр_респонсибилити** ЗАДАНО значение false.</span><span class="sxs-lookup"><span data-stu-id="eeca5-116">The transport provider should attempt to handle all recipients with **PR_RESPONSIBILITY** set to FALSE.</span></span> <span data-ttu-id="eeca5-117">После успешной отправки или неудачной ошибки отправки получателю, поставщик транспорта должен задать для этого свойства значение TRUE в исходном сообщении, чтобы указать, что он принял ответственность за этого получателя.</span><span class="sxs-lookup"><span data-stu-id="eeca5-117">After successfully sending, or conclusively failing to send, to a recipient, the transport provider should set this property to TRUE in the source message to indicate that it has accepted responsibility for that recipient.</span></span> 
  
<span data-ttu-id="eeca5-118">Если после проверки получателя поставщик транспорта решает, что он не может или не должен обрабатывать его, то поставщик транспорта должен оставить для параметра **пр_респонсибилити** значение false.</span><span class="sxs-lookup"><span data-stu-id="eeca5-118">If, after examining a recipient, a transport provider decides that it cannot or should not handle it, the transport provider should leave **PR_RESPONSIBILITY** set to FALSE.</span></span> <span data-ttu-id="eeca5-119">После этого диспетчер очереди MAPI будет искать другого поставщика транспорта, который может обработать этого получателя.</span><span class="sxs-lookup"><span data-stu-id="eeca5-119">The MAPI spooler will then look for another transport provider that can handle that recipient.</span></span> <span data-ttu-id="eeca5-120">В конечном счете, диспетчер очереди MAPI создает отчет о недоставке для всех получателей, для которых никакой поставщик транспорта не принимает ответственность.</span><span class="sxs-lookup"><span data-stu-id="eeca5-120">The MAPI spooler ultimately creates a nondelivery report for any recipients for which no transport provider accepts responsibility.</span></span> 
  
<span data-ttu-id="eeca5-121">Если поставщик транспорта пытается и не может доставить сообщение, он должен вызвать метод [имаписуппорт:: статусреЦипс](imapisupport-statusrecips.md) , чтобы указать MAPI причины сбоя, чтобы MAPI мог создать отчет о недоставке.</span><span class="sxs-lookup"><span data-stu-id="eeca5-121">If the transport provider attempts and fails to deliver the message, it should call the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method to indicate to MAPI the reasons for the failure, so that MAPI can generate a nondelivery report.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="eeca5-122">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="eeca5-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="eeca5-123">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="eeca5-123">Protocol specifications</span></span>

<span data-ttu-id="eeca5-124">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="eeca5-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="eeca5-125">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="eeca5-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="eeca5-126">[[MS — ОКСКФКСИКС]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="eeca5-126">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="eeca5-127">Обрабатывает порядок и потоки для передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="eeca5-127">Handles the order and flow for data transfers between a client and server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="eeca5-128">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="eeca5-128">Header files</span></span>

<span data-ttu-id="eeca5-129">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="eeca5-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="eeca5-130">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="eeca5-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="eeca5-131">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="eeca5-131">Mapitags.h</span></span>
  
> <span data-ttu-id="eeca5-132">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="eeca5-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="eeca5-133">См. также</span><span class="sxs-lookup"><span data-stu-id="eeca5-133">See also</span></span>



[<span data-ttu-id="eeca5-134">������������ �������� PidTagDeleteAfterSubmit</span><span class="sxs-lookup"><span data-stu-id="eeca5-134">PidTagDeleteAfterSubmit Canonical Property</span></span>](pidtagdeleteaftersubmit-canonical-property.md)


[<span data-ttu-id="eeca5-135">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="eeca5-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="eeca5-136">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="eeca5-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="eeca5-137">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="eeca5-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="eeca5-138">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="eeca5-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

