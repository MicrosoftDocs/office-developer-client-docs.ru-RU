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
ms.openlocfilehash: d8b4df2dbb0d7fd2edeb82222f333c11c5f71987
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811744"
---
# <a name="pidtagroamingdatatypes-canonical-property"></a><span data-ttu-id="791a1-103">Каноническое свойство PidTagRoamingDatatypes</span><span class="sxs-lookup"><span data-stu-id="791a1-103">PidTagRoamingDatatypes Canonical Property</span></span>

  
  
<span data-ttu-id="791a1-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="791a1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="791a1-105">Содержит битовую маску, которое указывает, какие свойства существуют на сообщение потока.</span><span class="sxs-lookup"><span data-stu-id="791a1-105">Contains a bitmask that indicates which stream properties exist on the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="791a1-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="791a1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="791a1-107">PR_ROAMING_DATATYPES</span><span class="sxs-lookup"><span data-stu-id="791a1-107">PR_ROAMING_DATATYPES</span></span>  <br/> |
|<span data-ttu-id="791a1-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="791a1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="791a1-109">0x7C06</span><span class="sxs-lookup"><span data-stu-id="791a1-109">0x7C06</span></span>  <br/> |
|<span data-ttu-id="791a1-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="791a1-110">Data type:</span></span>  <br/> |<span data-ttu-id="791a1-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="791a1-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="791a1-112">Область:</span><span class="sxs-lookup"><span data-stu-id="791a1-112">Area:</span></span>  <br/> |<span data-ttu-id="791a1-113">Конфигурация</span><span class="sxs-lookup"><span data-stu-id="791a1-113">Configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="791a1-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="791a1-114">Remarks</span></span>

<span data-ttu-id="791a1-115">Это свойство должно быть задано к одному или нескольким из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="791a1-115">This property must be set to one or more of the following values:</span></span>
  
|<span data-ttu-id="791a1-116">**Значение**</span><span class="sxs-lookup"><span data-stu-id="791a1-116">**Value**</span></span>|<span data-ttu-id="791a1-117">**Описание**</span><span class="sxs-lookup"><span data-stu-id="791a1-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="791a1-118">0x00000002</span><span class="sxs-lookup"><span data-stu-id="791a1-118">0x00000002</span></span>  <br/> |<span data-ttu-id="791a1-119">Указывает, что сообщение связанные сведения о папке (FAI) должен содержать потока словаря, сериализованным в основных XML-схеме и хранится в свойстве **PR_ROAMING_DICTIONARY** ([PidTagRoamingDictionary](pidtagroamingdictionary-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="791a1-119">Indicates that the Folder Associated Information (FAI) message should contain a Dictionary stream, serialized into a fixed XML schema and stored in the **PR_ROAMING_DICTIONARY** ([PidTagRoamingDictionary](pidtagroamingdictionary-canonical-property.md)) property.</span></span> <span data-ttu-id="791a1-120">Если сообщение FAI не содержит потока словаря, приложения должен обрабатывать словаря как необходимости нет записей.</span><span class="sxs-lookup"><span data-stu-id="791a1-120">If the FAI message does not contain a Dictionary stream, the application must treat the Dictionary as having no entries.</span></span>  <br/> |
|<span data-ttu-id="791a1-121">0x00000004</span><span class="sxs-lookup"><span data-stu-id="791a1-121">0x00000004</span></span>  <br/> |<span data-ttu-id="791a1-122">Указывает, что сообщение FAI должно содержать поток XML, хранящиеся в свойстве **PR_ROAMING_XMLSTREAM** ([PidTagRoamingXmlStream](pidtagroamingxmlstream-canonical-property.md)), который использует произвольных схемы XML.</span><span class="sxs-lookup"><span data-stu-id="791a1-122">Indicates that the FAI message must contain an XML stream stored in the **PR_ROAMING_XMLSTREAM** ([PidTagRoamingXmlStream](pidtagroamingxmlstream-canonical-property.md)) property that uses an arbitrary XML schema.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="791a1-123">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="791a1-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="791a1-124">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="791a1-124">Protocol specifications</span></span>

<span data-ttu-id="791a1-125">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="791a1-125">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="791a1-126">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="791a1-126">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="791a1-127">[[MS-OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="791a1-127">[[MS-OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="791a1-128">Указывает расположение и свойства клиентских и серверных данных конфигурации, такие как списки общие категории и рабочее время.</span><span class="sxs-lookup"><span data-stu-id="791a1-128">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="791a1-129">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="791a1-129">Header files</span></span>

<span data-ttu-id="791a1-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="791a1-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="791a1-131">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="791a1-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="791a1-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="791a1-132">Mapitags.h</span></span>
  
> <span data-ttu-id="791a1-133">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="791a1-133">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="791a1-134">См. также</span><span class="sxs-lookup"><span data-stu-id="791a1-134">See also</span></span>



[<span data-ttu-id="791a1-135">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="791a1-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="791a1-136">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="791a1-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="791a1-137">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="791a1-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="791a1-138">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="791a1-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

