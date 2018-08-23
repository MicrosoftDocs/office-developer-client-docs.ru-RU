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
ms.openlocfilehash: 468cda97398bc393b1c0a65e2c13df5ba3ade3aa
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568912"
---
# <a name="pidtagcorrelatemtsid-canonical-property"></a><span data-ttu-id="f4d0b-103">Каноническое свойство PidTagCorrelateMtsid</span><span class="sxs-lookup"><span data-stu-id="f4d0b-103">PidTagCorrelateMtsid Canonical Property</span></span>

  
  
<span data-ttu-id="f4d0b-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f4d0b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f4d0b-105">Содержит идентификатор система передачи сообщений, используемый в сопоставление отчетов с отправленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="f4d0b-105">Contains the message transfer system (MTS) identifier used in correlating reports with sent messages.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f4d0b-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="f4d0b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f4d0b-107">PR_CORRELATE_MTSID</span><span class="sxs-lookup"><span data-stu-id="f4d0b-107">PR_CORRELATE_MTSID</span></span>  <br/> |
|<span data-ttu-id="f4d0b-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="f4d0b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f4d0b-109">0x0E0D</span><span class="sxs-lookup"><span data-stu-id="f4d0b-109">0x0E0D</span></span>  <br/> |
|<span data-ttu-id="f4d0b-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="f4d0b-110">Data type:</span></span>  <br/> |<span data-ttu-id="f4d0b-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="f4d0b-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="f4d0b-112">Область:</span><span class="sxs-lookup"><span data-stu-id="f4d0b-112">Area:</span></span>  <br/> |<span data-ttu-id="f4d0b-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="f4d0b-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f4d0b-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="f4d0b-114">Remarks</span></span>

<span data-ttu-id="f4d0b-115">Когда поставщика транспорта обнаруживает отправленное сообщение с набором свойств значение TRUE, это свойство присваивается идентификатор MTS для этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="f4d0b-115">When a transport provider encounters a submitted message with this property set to TRUE, it sets this property to the MTS identifier for that message.</span></span> <span data-ttu-id="f4d0b-116">После отправки это свойство хранится с сообщения в папке Отправленные сообщения электронной почты — это (IPM).</span><span class="sxs-lookup"><span data-stu-id="f4d0b-116">Following transmission, this property is stored with the message in the interpersonal message (IPM) Sent Items folder.</span></span>
  
<span data-ttu-id="f4d0b-117">Системы обмена сообщениями, которые поддерживают корреляции по идентификатору MTS, такие как X.400, сохранения идентификатора как часть конверт транспорта исходного сообщения, а также любые отчеты, созданные в ответ на него.</span><span class="sxs-lookup"><span data-stu-id="f4d0b-117">Messaging systems that support correlation by MTS identifier, such as X.400, retain the identifier as part of the transport envelope of the original message and also of any reports generated in response to it.</span></span> <span data-ttu-id="f4d0b-118">Когда отчет доставляется из таких систем обмена сообщениями, поставщика транспорта этому свойству в исходный идентификатор MTS из отчета транспорта конверт.</span><span class="sxs-lookup"><span data-stu-id="f4d0b-118">When a report is delivered from such a messaging system, the transport provider sets this property to the original MTS identifier from the report's transport envelope.</span></span> <span data-ttu-id="f4d0b-119">Это свойство будет храниться в отчете.</span><span class="sxs-lookup"><span data-stu-id="f4d0b-119">This property is then stored with the report.</span></span>
  
<span data-ttu-id="f4d0b-120">Клиентское приложение может поддерживать папка результатов поиска из всех сообщений, имеющих это свойство.</span><span class="sxs-lookup"><span data-stu-id="f4d0b-120">A client application can maintain a search-results folder of all messages having this property.</span></span> <span data-ttu-id="f4d0b-121">При поступлении отчет для такого сообщения клиента можно применяются ограничения в папку результатов поиска, найдите первоначальной версии сообщения и соотнесения исходного сообщения с новыми данными.</span><span class="sxs-lookup"><span data-stu-id="f4d0b-121">When a report comes in for such a message, the client can apply restrictions to the search-results folder, find the original version of the message, and correlate the original message information with the new information.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f4d0b-122">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f4d0b-122">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="f4d0b-123">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="f4d0b-123">Header files</span></span>

<span data-ttu-id="f4d0b-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f4d0b-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="f4d0b-125">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="f4d0b-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="f4d0b-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f4d0b-126">Mapitags.h</span></span>
  
> <span data-ttu-id="f4d0b-127">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="f4d0b-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f4d0b-128">См. также</span><span class="sxs-lookup"><span data-stu-id="f4d0b-128">See also</span></span>



[<span data-ttu-id="f4d0b-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f4d0b-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f4d0b-130">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f4d0b-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f4d0b-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="f4d0b-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f4d0b-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="f4d0b-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

