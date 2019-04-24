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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359936"
---
# <a name="pidtagcorrelatemtsid-canonical-property"></a><span data-ttu-id="95733-103">Каноническое свойство PidTagCorrelateMtsid</span><span class="sxs-lookup"><span data-stu-id="95733-103">PidTagCorrelateMtsid Canonical Property</span></span>

  
  
<span data-ttu-id="95733-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="95733-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="95733-105">Содержит идентификатор системы передачи сообщений (MTS), используемый при согласовании отчетов с отправленными сообщениями.</span><span class="sxs-lookup"><span data-stu-id="95733-105">Contains the message transfer system (MTS) identifier used in correlating reports with sent messages.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="95733-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="95733-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="95733-107">ПР_КОРРЕЛАТЕ_МТСИД</span><span class="sxs-lookup"><span data-stu-id="95733-107">PR_CORRELATE_MTSID</span></span>  <br/> |
|<span data-ttu-id="95733-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="95733-108">Identifier:</span></span>  <br/> |<span data-ttu-id="95733-109">0x0E0D</span><span class="sxs-lookup"><span data-stu-id="95733-109">0x0E0D</span></span>  <br/> |
|<span data-ttu-id="95733-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="95733-110">Data type:</span></span>  <br/> |<span data-ttu-id="95733-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="95733-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="95733-112">Область:</span><span class="sxs-lookup"><span data-stu-id="95733-112">Area:</span></span>  <br/> |<span data-ttu-id="95733-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="95733-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="95733-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="95733-114">Remarks</span></span>

<span data-ttu-id="95733-115">Когда поставщик транспорта обнаруживает отправленное сообщение, у которого для этого свойства установлено значение TRUE, этому свойству присваивается идентификатор MTS для этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="95733-115">When a transport provider encounters a submitted message with this property set to TRUE, it sets this property to the MTS identifier for that message.</span></span> <span data-ttu-id="95733-116">После передачи это свойство хранится вместе с сообщением в папке "сообщения с взаимосвязанными сообщениями (IPM)".</span><span class="sxs-lookup"><span data-stu-id="95733-116">Following transmission, this property is stored with the message in the interpersonal message (IPM) Sent Items folder.</span></span>
  
<span data-ttu-id="95733-117">Системы обмена сообщениями, поддерживающие корреляцию по идентификатору MTS, например X. 400, сохраняют идентификатор как часть транспортного конверта исходного сообщения, а также любые отчеты, созданные в ответ на него.</span><span class="sxs-lookup"><span data-stu-id="95733-117">Messaging systems that support correlation by MTS identifier, such as X.400, retain the identifier as part of the transport envelope of the original message and also of any reports generated in response to it.</span></span> <span data-ttu-id="95733-118">Когда отчет доставляется из такой системы обмена сообщениями, поставщик транспорта присваивает этому свойству исходный идентификатор MTS из транспортного конверта отчета.</span><span class="sxs-lookup"><span data-stu-id="95733-118">When a report is delivered from such a messaging system, the transport provider sets this property to the original MTS identifier from the report's transport envelope.</span></span> <span data-ttu-id="95733-119">Затем это свойство сохраняется вместе с отчетом.</span><span class="sxs-lookup"><span data-stu-id="95733-119">This property is then stored with the report.</span></span>
  
<span data-ttu-id="95733-120">Клиентское приложение может хранить папку результатов поиска для всех сообщений, имеющих данное свойство.</span><span class="sxs-lookup"><span data-stu-id="95733-120">A client application can maintain a search-results folder of all messages having this property.</span></span> <span data-ttu-id="95733-121">Когда отчет поступает в таком сообщении, клиент может применить ограничения к папке результатов поиска, найти исходную версию сообщения и сопоставить сведения об исходном сообщении с новыми данными.</span><span class="sxs-lookup"><span data-stu-id="95733-121">When a report comes in for such a message, the client can apply restrictions to the search-results folder, find the original version of the message, and correlate the original message information with the new information.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="95733-122">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="95733-122">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="95733-123">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="95733-123">Header files</span></span>

<span data-ttu-id="95733-124">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="95733-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="95733-125">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="95733-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="95733-126">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="95733-126">Mapitags.h</span></span>
  
> <span data-ttu-id="95733-127">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="95733-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="95733-128">См. также</span><span class="sxs-lookup"><span data-stu-id="95733-128">See also</span></span>



[<span data-ttu-id="95733-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="95733-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="95733-130">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="95733-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="95733-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="95733-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="95733-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="95733-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

