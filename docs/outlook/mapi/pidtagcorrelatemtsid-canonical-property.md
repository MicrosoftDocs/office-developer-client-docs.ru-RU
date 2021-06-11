---
title: Каноническое свойство PidTagCorrelateMtsid
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagCorrelateMtsid
api_type:
- HeaderDef
ms.assetid: d0fc4e91-ed90-4d27-bd23-f01e99728e2d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 96bfc184752b6a3e15434ad67ac8c2b4b26cac4b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426837"
---
# <a name="pidtagcorrelatemtsid-canonical-property"></a><span data-ttu-id="4010b-103">Каноническое свойство PidTagCorrelateMtsid</span><span class="sxs-lookup"><span data-stu-id="4010b-103">PidTagCorrelateMtsid Canonical Property</span></span>

  
  
<span data-ttu-id="4010b-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4010b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4010b-105">Содержит идентификатор системы передачи сообщений (MTS), используемый при сопоставлении отчетов с отправленными сообщениями.</span><span class="sxs-lookup"><span data-stu-id="4010b-105">Contains the message transfer system (MTS) identifier used in correlating reports with sent messages.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4010b-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="4010b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4010b-107">PR_CORRELATE_MTSID</span><span class="sxs-lookup"><span data-stu-id="4010b-107">PR_CORRELATE_MTSID</span></span>  <br/> |
|<span data-ttu-id="4010b-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="4010b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4010b-109">0x0E0D</span><span class="sxs-lookup"><span data-stu-id="4010b-109">0x0E0D</span></span>  <br/> |
|<span data-ttu-id="4010b-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="4010b-110">Data type:</span></span>  <br/> |<span data-ttu-id="4010b-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="4010b-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="4010b-112">Область:</span><span class="sxs-lookup"><span data-stu-id="4010b-112">Area:</span></span>  <br/> |<span data-ttu-id="4010b-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="4010b-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4010b-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="4010b-114">Remarks</span></span>

<span data-ttu-id="4010b-115">Когда поставщик транспорта сталкивается с отправленным сообщением с этим свойством, заданным true, он задает это свойство идентификатору МТС для этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="4010b-115">When a transport provider encounters a submitted message with this property set to TRUE, it sets this property to the MTS identifier for that message.</span></span> <span data-ttu-id="4010b-116">После передачи это свойство сохраняется с сообщением в папке отправленных элементов межличностного сообщения (IPM).</span><span class="sxs-lookup"><span data-stu-id="4010b-116">Following transmission, this property is stored with the message in the interpersonal message (IPM) Sent Items folder.</span></span>
  
<span data-ttu-id="4010b-117">Системы обмена сообщениями, поддерживаюющие корреляцию с идентификатором МТС, например X.400, сохраняют идентификатор как часть транспортного конверта исходного сообщения, а также любых отчетов, созданных в ответ на него.</span><span class="sxs-lookup"><span data-stu-id="4010b-117">Messaging systems that support correlation by MTS identifier, such as X.400, retain the identifier as part of the transport envelope of the original message and also of any reports generated in response to it.</span></span> <span data-ttu-id="4010b-118">При доставке отчета из такой системы обмена сообщениями поставщик транспорта задает это свойство исходному идентификатору МТС из транспортного конверта отчета.</span><span class="sxs-lookup"><span data-stu-id="4010b-118">When a report is delivered from such a messaging system, the transport provider sets this property to the original MTS identifier from the report's transport envelope.</span></span> <span data-ttu-id="4010b-119">Затем это свойство хранится в отчете.</span><span class="sxs-lookup"><span data-stu-id="4010b-119">This property is then stored with the report.</span></span>
  
<span data-ttu-id="4010b-120">Клиентские приложения могут поддерживать папку результатов поиска всех сообщений, имеющих это свойство.</span><span class="sxs-lookup"><span data-stu-id="4010b-120">A client application can maintain a search-results folder of all messages having this property.</span></span> <span data-ttu-id="4010b-121">Когда поступает отчет о таком сообщении, клиент может применить ограничения к папке результатов поиска, найти исходную версию сообщения и соотнести исходные сведения о сообщении с новыми сведениями.</span><span class="sxs-lookup"><span data-stu-id="4010b-121">When a report comes in for such a message, the client can apply restrictions to the search-results folder, find the original version of the message, and correlate the original message information with the new information.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4010b-122">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="4010b-122">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="4010b-123">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="4010b-123">Header files</span></span>

<span data-ttu-id="4010b-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4010b-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="4010b-125">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="4010b-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="4010b-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4010b-126">Mapitags.h</span></span>
  
> <span data-ttu-id="4010b-127">Содержит определения свойств, перечисленных в качестве связанных свойств.</span><span class="sxs-lookup"><span data-stu-id="4010b-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4010b-128">См. также</span><span class="sxs-lookup"><span data-stu-id="4010b-128">See also</span></span>



[<span data-ttu-id="4010b-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="4010b-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4010b-130">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="4010b-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4010b-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="4010b-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4010b-132">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="4010b-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

