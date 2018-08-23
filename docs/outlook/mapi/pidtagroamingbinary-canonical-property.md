---
title: Каноническое свойство PidTagRoamingBinary
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f06bf063-fc95-46f9-b5fa-3f127a59ebda
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 717c456024dd98495550f1377edc6a53f82ee042
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572412"
---
# <a name="pidtagroamingbinary-canonical-property"></a><span data-ttu-id="204a1-103">Каноническое свойство PidTagRoamingBinary</span><span class="sxs-lookup"><span data-stu-id="204a1-103">PidTagRoamingBinary Canonical Property</span></span>

  
  
<span data-ttu-id="204a1-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="204a1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="204a1-105">Содержит поток сообщений, связанных с подкласс **IPM. Конфигурация** класса.</span><span class="sxs-lookup"><span data-stu-id="204a1-105">Contains a message stream associated with a subclass of the **IPM.Configuration** class.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="204a1-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="204a1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="204a1-107">PR_ROAMING_BINARYSTREAM</span><span class="sxs-lookup"><span data-stu-id="204a1-107">PR_ROAMING_BINARYSTREAM</span></span>  <br/> |
|<span data-ttu-id="204a1-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="204a1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="204a1-109">0x7C09</span><span class="sxs-lookup"><span data-stu-id="204a1-109">0x7C09</span></span>  <br/> |
|<span data-ttu-id="204a1-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="204a1-110">Data type:</span></span>  <br/> |<span data-ttu-id="204a1-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="204a1-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="204a1-112">Область:</span><span class="sxs-lookup"><span data-stu-id="204a1-112">Area:</span></span>  <br/> |<span data-ttu-id="204a1-113">Конфигурация</span><span class="sxs-lookup"><span data-stu-id="204a1-113">Configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="204a1-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="204a1-114">Remarks</span></span>

<span data-ttu-id="204a1-115">Это свойство содержит поток данных, связанных с **IPM. Конфигурация** сообщение класс сообщения.</span><span class="sxs-lookup"><span data-stu-id="204a1-115">This property contains the data stream associated with an **IPM.Configuration** message class message.</span></span> <span data-ttu-id="204a1-116">Формат потока зависит от класса сообщения.</span><span class="sxs-lookup"><span data-stu-id="204a1-116">The format of the stream depends on the message class.</span></span> <span data-ttu-id="204a1-117">Например сообщение типа класса **IPM. Configuration.Autocomplete** может быть в формате [потока автозаполнения](autocomplete-stream.md).</span><span class="sxs-lookup"><span data-stu-id="204a1-117">For instance, a message of class type **IPM.Configuration.Autocomplete** would be formatted as an [Autocomplete Stream](autocomplete-stream.md).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="204a1-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="204a1-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="204a1-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="204a1-119">Protocol specifications</span></span>

<span data-ttu-id="204a1-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="204a1-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="204a1-121">Содержит ссылки на связанные спецификаций протокола Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="204a1-121">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="204a1-122">[[MS-OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="204a1-122">[[MS-OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="204a1-123">Указывает расположение и свойства клиентских и серверных данных конфигурации, такие как списки общие категории и рабочее время.</span><span class="sxs-lookup"><span data-stu-id="204a1-123">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="204a1-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="204a1-124">Header files</span></span>

<span data-ttu-id="204a1-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="204a1-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="204a1-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="204a1-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="204a1-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="204a1-127">Mapitags.h</span></span>
  
> <span data-ttu-id="204a1-128">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="204a1-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="204a1-129">См. также</span><span class="sxs-lookup"><span data-stu-id="204a1-129">See also</span></span>



[<span data-ttu-id="204a1-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="204a1-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="204a1-131">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="204a1-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="204a1-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="204a1-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="204a1-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="204a1-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

