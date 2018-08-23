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
ms.openlocfilehash: e1d9a8bce2207529d1062f50a86547379c6255e4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569414"
---
# <a name="pidtagroamingxmlstream-canonical-property"></a><span data-ttu-id="08bb3-103">Каноническое свойство PidTagRoamingXmlStream</span><span class="sxs-lookup"><span data-stu-id="08bb3-103">PidTagRoamingXmlStream Canonical Property</span></span>

  
  
<span data-ttu-id="08bb3-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="08bb3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="08bb3-105">Содержит произвольных XML-потока.</span><span class="sxs-lookup"><span data-stu-id="08bb3-105">Contains an arbitrary XML stream.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="08bb3-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="08bb3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="08bb3-107">PR_ROAMING_XMLSTREAM</span><span class="sxs-lookup"><span data-stu-id="08bb3-107">PR_ROAMING_XMLSTREAM</span></span>  <br/> |
|<span data-ttu-id="08bb3-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="08bb3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="08bb3-109">0x7C08</span><span class="sxs-lookup"><span data-stu-id="08bb3-109">0x7C08</span></span>  <br/> |
|<span data-ttu-id="08bb3-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="08bb3-110">Data type:</span></span>  <br/> |<span data-ttu-id="08bb3-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="08bb3-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="08bb3-112">Область:</span><span class="sxs-lookup"><span data-stu-id="08bb3-112">Area:</span></span>  <br/> |<span data-ttu-id="08bb3-113">Конфигурация</span><span class="sxs-lookup"><span data-stu-id="08bb3-113">Configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="08bb3-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="08bb3-114">Remarks</span></span>

<span data-ttu-id="08bb3-115">Это свойство содержит произвольных потока XML-данных.</span><span class="sxs-lookup"><span data-stu-id="08bb3-115">This property contains an arbitrary stream of XML data.</span></span> <span data-ttu-id="08bb3-116">Другие свойства в сообщении может означать определенных схем для использования в этом свойстве.</span><span class="sxs-lookup"><span data-stu-id="08bb3-116">Other properties in the message may imply specific schemas to use in this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="08bb3-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="08bb3-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="08bb3-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="08bb3-118">Protocol specifications</span></span>

<span data-ttu-id="08bb3-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="08bb3-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="08bb3-120">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="08bb3-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="08bb3-121">[[MS-OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="08bb3-121">[[MS-OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="08bb3-122">Указывает расположение и свойства клиентских и серверных данных конфигурации, такие как списки общие категории и рабочее время.</span><span class="sxs-lookup"><span data-stu-id="08bb3-122">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="08bb3-123">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="08bb3-123">Header files</span></span>

<span data-ttu-id="08bb3-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="08bb3-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="08bb3-125">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="08bb3-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="08bb3-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="08bb3-126">Mapitags.h</span></span>
  
> <span data-ttu-id="08bb3-127">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="08bb3-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="08bb3-128">См. также</span><span class="sxs-lookup"><span data-stu-id="08bb3-128">See also</span></span>



[<span data-ttu-id="08bb3-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="08bb3-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="08bb3-130">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="08bb3-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="08bb3-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="08bb3-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="08bb3-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="08bb3-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

