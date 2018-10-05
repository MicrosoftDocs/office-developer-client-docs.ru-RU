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
ms.openlocfilehash: ead7c9c33c92240ba5e458b68635b766caaa9760
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401673"
---
# <a name="pidtagroamingbinary-canonical-property"></a><span data-ttu-id="f8a8c-103">Каноническое свойство PidTagRoamingBinary</span><span class="sxs-lookup"><span data-stu-id="f8a8c-103">PidTagRoamingBinary Canonical Property</span></span>

  
  
<span data-ttu-id="f8a8c-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f8a8c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f8a8c-105">Содержит поток сообщений, связанных с подкласс **IPM. Конфигурация** класса.</span><span class="sxs-lookup"><span data-stu-id="f8a8c-105">Contains a message stream associated with a subclass of the **IPM.Configuration** class.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f8a8c-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="f8a8c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f8a8c-107">PR_ROAMING_BINARYSTREAM</span><span class="sxs-lookup"><span data-stu-id="f8a8c-107">PR_ROAMING_BINARYSTREAM</span></span>  <br/> |
|<span data-ttu-id="f8a8c-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="f8a8c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f8a8c-109">0x7C09</span><span class="sxs-lookup"><span data-stu-id="f8a8c-109">0x7C09</span></span>  <br/> |
|<span data-ttu-id="f8a8c-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="f8a8c-110">Data type:</span></span>  <br/> |<span data-ttu-id="f8a8c-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="f8a8c-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="f8a8c-112">Область:</span><span class="sxs-lookup"><span data-stu-id="f8a8c-112">Area:</span></span>  <br/> |<span data-ttu-id="f8a8c-113">Конфигурация</span><span class="sxs-lookup"><span data-stu-id="f8a8c-113">Configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f8a8c-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="f8a8c-114">Remarks</span></span>

<span data-ttu-id="f8a8c-115">Это свойство содержит поток данных, связанных с **IPM. Конфигурация** сообщение класс сообщения.</span><span class="sxs-lookup"><span data-stu-id="f8a8c-115">This property contains the data stream associated with an **IPM.Configuration** message class message.</span></span> <span data-ttu-id="f8a8c-116">Формат потока зависит от класса сообщения.</span><span class="sxs-lookup"><span data-stu-id="f8a8c-116">The format of the stream depends on the message class.</span></span> <span data-ttu-id="f8a8c-117">Например сообщение типа класса **IPM. Configuration.Autocomplete** может быть в формате [потока автозаполнения](autocomplete-stream.md).</span><span class="sxs-lookup"><span data-stu-id="f8a8c-117">For instance, a message of class type **IPM.Configuration.Autocomplete** would be formatted as an [Autocomplete Stream](autocomplete-stream.md).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f8a8c-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f8a8c-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f8a8c-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="f8a8c-119">Protocol specifications</span></span>

<span data-ttu-id="f8a8c-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f8a8c-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f8a8c-121">Содержит ссылки на связанные спецификаций протокола Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="f8a8c-121">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f8a8c-122">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f8a8c-122">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f8a8c-123">Указывает расположение и свойства клиентских и серверных данных конфигурации, такие как списки общие категории и рабочее время.</span><span class="sxs-lookup"><span data-stu-id="f8a8c-123">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f8a8c-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="f8a8c-124">Header files</span></span>

<span data-ttu-id="f8a8c-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f8a8c-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="f8a8c-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="f8a8c-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="f8a8c-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f8a8c-127">Mapitags.h</span></span>
  
> <span data-ttu-id="f8a8c-128">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="f8a8c-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f8a8c-129">См. также</span><span class="sxs-lookup"><span data-stu-id="f8a8c-129">See also</span></span>



[<span data-ttu-id="f8a8c-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f8a8c-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f8a8c-131">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f8a8c-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f8a8c-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="f8a8c-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f8a8c-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="f8a8c-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

