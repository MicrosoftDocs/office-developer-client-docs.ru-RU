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
# <a name="pidtagroamingdatatypes-canonical-property"></a><span data-ttu-id="63bcf-103">Каноническое свойство PidTagRoamingDatatypes</span><span class="sxs-lookup"><span data-stu-id="63bcf-103">PidTagRoamingDatatypes Canonical Property</span></span>

  
  
<span data-ttu-id="63bcf-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="63bcf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="63bcf-105">Содержит битмаску, которая указывает, какие свойства потока существуют в сообщении.</span><span class="sxs-lookup"><span data-stu-id="63bcf-105">Contains a bitmask that indicates which stream properties exist on the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="63bcf-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="63bcf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="63bcf-107">PR_ROAMING_DATATYPES</span><span class="sxs-lookup"><span data-stu-id="63bcf-107">PR_ROAMING_DATATYPES</span></span>  <br/> |
|<span data-ttu-id="63bcf-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="63bcf-108">Identifier:</span></span>  <br/> |<span data-ttu-id="63bcf-109">0x7C06</span><span class="sxs-lookup"><span data-stu-id="63bcf-109">0x7C06</span></span>  <br/> |
|<span data-ttu-id="63bcf-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="63bcf-110">Data type:</span></span>  <br/> |<span data-ttu-id="63bcf-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="63bcf-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="63bcf-112">Область:</span><span class="sxs-lookup"><span data-stu-id="63bcf-112">Area:</span></span>  <br/> |<span data-ttu-id="63bcf-113">Конфигурация</span><span class="sxs-lookup"><span data-stu-id="63bcf-113">Configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="63bcf-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="63bcf-114">Remarks</span></span>

<span data-ttu-id="63bcf-115">Это свойство должно быть заданной для одного или более из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="63bcf-115">This property must be set to one or more of the following values:</span></span>
  
|<span data-ttu-id="63bcf-116">**Значение**</span><span class="sxs-lookup"><span data-stu-id="63bcf-116">**Value**</span></span>|<span data-ttu-id="63bcf-117">**Описание**</span><span class="sxs-lookup"><span data-stu-id="63bcf-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="63bcf-118">0x00000002</span><span class="sxs-lookup"><span data-stu-id="63bcf-118">0x00000002</span></span>  <br/> |<span data-ttu-id="63bcf-119">Указывает на то, что сообщение о связанной с папкой информации (FAI) должно содержать поток  словарей, сериализованный в фиксированную схему XML и хранимый в свойстве[PR_ROAMING_DICTIONARY (PidTagRoamingDictionary).](pidtagroamingdictionary-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="63bcf-119">Indicates that the Folder Associated Information (FAI) message should contain a Dictionary stream, serialized into a fixed XML schema and stored in the **PR_ROAMING_DICTIONARY** ([PidTagRoamingDictionary](pidtagroamingdictionary-canonical-property.md)) property.</span></span> <span data-ttu-id="63bcf-120">Если сообщение FAI не содержит потока Словарь, приложение должно рассматривать словарь как не имеющий записей.</span><span class="sxs-lookup"><span data-stu-id="63bcf-120">If the FAI message does not contain a Dictionary stream, the application must treat the Dictionary as having no entries.</span></span>  <br/> |
|<span data-ttu-id="63bcf-121">0x00000004</span><span class="sxs-lookup"><span data-stu-id="63bcf-121">0x00000004</span></span>  <br/> |<span data-ttu-id="63bcf-122">Указывает, что сообщение FAI должно содержать поток **XML,** хранимый в свойстве [PR_ROAMING_XMLSTREAM (PidTagRoamingXmlStream),](pidtagroamingxmlstream-canonical-property.md)который использует произвольную схему XML.</span><span class="sxs-lookup"><span data-stu-id="63bcf-122">Indicates that the FAI message must contain an XML stream stored in the **PR_ROAMING_XMLSTREAM** ([PidTagRoamingXmlStream](pidtagroamingxmlstream-canonical-property.md)) property that uses an arbitrary XML schema.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="63bcf-123">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="63bcf-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="63bcf-124">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="63bcf-124">Protocol specifications</span></span>

<span data-ttu-id="63bcf-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="63bcf-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="63bcf-126">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="63bcf-126">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="63bcf-127">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="63bcf-127">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="63bcf-128">Указывает расположение и свойства данных конфигурации клиента и сервера, например списки общих категорий и рабочие часы.</span><span class="sxs-lookup"><span data-stu-id="63bcf-128">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="63bcf-129">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="63bcf-129">Header files</span></span>

<span data-ttu-id="63bcf-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="63bcf-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="63bcf-131">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="63bcf-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="63bcf-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="63bcf-132">Mapitags.h</span></span>
  
> <span data-ttu-id="63bcf-133">Содержит определения свойств, перечисленных в качестве связанных свойств.</span><span class="sxs-lookup"><span data-stu-id="63bcf-133">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="63bcf-134">См. также</span><span class="sxs-lookup"><span data-stu-id="63bcf-134">See also</span></span>



[<span data-ttu-id="63bcf-135">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="63bcf-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="63bcf-136">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="63bcf-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="63bcf-137">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="63bcf-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="63bcf-138">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="63bcf-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

