---
title: Каноническое свойство PidTagRoamingDatatypes
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRoamingDatatypes
api_type:
- COM
ms.assetid: a3336b61-01b6-47a7-9498-0a03878e91cb
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: fe5528f7605412d0cfd4b4b914e9b221c715e1b1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359558"
---
# <a name="pidtagroamingdatatypes-canonical-property"></a><span data-ttu-id="e34b1-103">Каноническое свойство PidTagRoamingDatatypes</span><span class="sxs-lookup"><span data-stu-id="e34b1-103">PidTagRoamingDatatypes Canonical Property</span></span>

  
  
<span data-ttu-id="e34b1-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e34b1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e34b1-105">Содержит битовую маску, указывающую, какие свойства потока существуют для сообщения.</span><span class="sxs-lookup"><span data-stu-id="e34b1-105">Contains a bitmask that indicates which stream properties exist on the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e34b1-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="e34b1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e34b1-107">ПР_РОАМИНГ_ДАТАТИПЕС</span><span class="sxs-lookup"><span data-stu-id="e34b1-107">PR_ROAMING_DATATYPES</span></span>  <br/> |
|<span data-ttu-id="e34b1-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="e34b1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e34b1-109">0x7C06</span><span class="sxs-lookup"><span data-stu-id="e34b1-109">0x7C06</span></span>  <br/> |
|<span data-ttu-id="e34b1-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="e34b1-110">Data type:</span></span>  <br/> |<span data-ttu-id="e34b1-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="e34b1-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="e34b1-112">Область:</span><span class="sxs-lookup"><span data-stu-id="e34b1-112">Area:</span></span>  <br/> |<span data-ttu-id="e34b1-113">Конфигурация</span><span class="sxs-lookup"><span data-stu-id="e34b1-113">Configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e34b1-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="e34b1-114">Remarks</span></span>

<span data-ttu-id="e34b1-115">Для этого свойства необходимо задать одно или несколько из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="e34b1-115">This property must be set to one or more of the following values:</span></span>
  
|<span data-ttu-id="e34b1-116">**Value**</span><span class="sxs-lookup"><span data-stu-id="e34b1-116">**Value**</span></span>|<span data-ttu-id="e34b1-117">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e34b1-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e34b1-118">0x00000002</span><span class="sxs-lookup"><span data-stu-id="e34b1-118">0x00000002</span></span>  <br/> |<span data-ttu-id="e34b1-119">Указывает, что сообщение связанной информации о папке (ФАИ) должно содержать поток словаря, сериализованный в фиксированную схему XML и хранящийся в свойстве **пр_роаминг_диктионари** ([PidTagRoamingDictionary](pidtagroamingdictionary-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="e34b1-119">Indicates that the Folder Associated Information (FAI) message should contain a Dictionary stream, serialized into a fixed XML schema and stored in the **PR_ROAMING_DICTIONARY** ([PidTagRoamingDictionary](pidtagroamingdictionary-canonical-property.md)) property.</span></span> <span data-ttu-id="e34b1-120">Если сообщение ФАИ не содержит поток словаря, приложение должно считать словарь без записей.</span><span class="sxs-lookup"><span data-stu-id="e34b1-120">If the FAI message does not contain a Dictionary stream, the application must treat the Dictionary as having no entries.</span></span>  <br/> |
|<span data-ttu-id="e34b1-121">0x00000004</span><span class="sxs-lookup"><span data-stu-id="e34b1-121">0x00000004</span></span>  <br/> |<span data-ttu-id="e34b1-122">Указывает, что сообщение ФАИ должно содержать XML-поток, хранящийся в свойстве **пр_роаминг_ксмлстреам** ([PidTagRoamingXmlStream](pidtagroamingxmlstream-canonical-property.md)), использующем произвольную XML-схему.</span><span class="sxs-lookup"><span data-stu-id="e34b1-122">Indicates that the FAI message must contain an XML stream stored in the **PR_ROAMING_XMLSTREAM** ([PidTagRoamingXmlStream](pidtagroamingxmlstream-canonical-property.md)) property that uses an arbitrary XML schema.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="e34b1-123">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="e34b1-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e34b1-124">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="e34b1-124">Protocol specifications</span></span>

<span data-ttu-id="e34b1-125">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e34b1-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e34b1-126">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="e34b1-126">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e34b1-127">[[MS — ОКСОКФГ]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e34b1-127">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e34b1-128">Задает расположение и свойства данных конфигурации клиента и сервера, например списки общих категорий и рабочие часы.</span><span class="sxs-lookup"><span data-stu-id="e34b1-128">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e34b1-129">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="e34b1-129">Header files</span></span>

<span data-ttu-id="e34b1-130">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="e34b1-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="e34b1-131">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="e34b1-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="e34b1-132">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="e34b1-132">Mapitags.h</span></span>
  
> <span data-ttu-id="e34b1-133">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="e34b1-133">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e34b1-134">См. также</span><span class="sxs-lookup"><span data-stu-id="e34b1-134">See also</span></span>



[<span data-ttu-id="e34b1-135">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="e34b1-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e34b1-136">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="e34b1-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e34b1-137">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="e34b1-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e34b1-138">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="e34b1-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

