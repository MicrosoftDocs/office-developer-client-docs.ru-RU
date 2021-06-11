---
title: Каноническое свойство PidTagRoamingXmlStream
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRoamingXmlStream
api_type:
- COM
ms.assetid: ce55b50e-3dbf-4690-9102-c08f35ada82e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3e7ce1f810a1dd37cd4370ceb423b664d75878a2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359544"
---
# <a name="pidtagroamingxmlstream-canonical-property"></a><span data-ttu-id="568d1-103">Каноническое свойство PidTagRoamingXmlStream</span><span class="sxs-lookup"><span data-stu-id="568d1-103">PidTagRoamingXmlStream Canonical Property</span></span>

  
  
<span data-ttu-id="568d1-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="568d1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="568d1-105">Содержит произвольный XML-поток.</span><span class="sxs-lookup"><span data-stu-id="568d1-105">Contains an arbitrary XML stream.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="568d1-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="568d1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="568d1-107">PR_ROAMING_XMLSTREAM</span><span class="sxs-lookup"><span data-stu-id="568d1-107">PR_ROAMING_XMLSTREAM</span></span>  <br/> |
|<span data-ttu-id="568d1-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="568d1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="568d1-109">0x7C08</span><span class="sxs-lookup"><span data-stu-id="568d1-109">0x7C08</span></span>  <br/> |
|<span data-ttu-id="568d1-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="568d1-110">Data type:</span></span>  <br/> |<span data-ttu-id="568d1-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="568d1-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="568d1-112">Область:</span><span class="sxs-lookup"><span data-stu-id="568d1-112">Area:</span></span>  <br/> |<span data-ttu-id="568d1-113">Конфигурация</span><span class="sxs-lookup"><span data-stu-id="568d1-113">Configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="568d1-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="568d1-114">Remarks</span></span>

<span data-ttu-id="568d1-115">Это свойство содержит произвольный поток XML-данных.</span><span class="sxs-lookup"><span data-stu-id="568d1-115">This property contains an arbitrary stream of XML data.</span></span> <span data-ttu-id="568d1-116">Другие свойства в сообщении могут подразумевать определенные схемы, которые следует использовать в этом свойстве.</span><span class="sxs-lookup"><span data-stu-id="568d1-116">Other properties in the message may imply specific schemas to use in this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="568d1-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="568d1-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="568d1-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="568d1-118">Protocol specifications</span></span>

<span data-ttu-id="568d1-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="568d1-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="568d1-120">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="568d1-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="568d1-121">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="568d1-121">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="568d1-122">Указывает расположение и свойства данных конфигурации клиента и сервера, например списки общих категорий и рабочие часы.</span><span class="sxs-lookup"><span data-stu-id="568d1-122">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="568d1-123">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="568d1-123">Header files</span></span>

<span data-ttu-id="568d1-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="568d1-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="568d1-125">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="568d1-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="568d1-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="568d1-126">Mapitags.h</span></span>
  
> <span data-ttu-id="568d1-127">Содержит определения свойств, перечисленных в качестве связанных свойств.</span><span class="sxs-lookup"><span data-stu-id="568d1-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="568d1-128">См. также</span><span class="sxs-lookup"><span data-stu-id="568d1-128">See also</span></span>



[<span data-ttu-id="568d1-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="568d1-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="568d1-130">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="568d1-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="568d1-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="568d1-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="568d1-132">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="568d1-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

