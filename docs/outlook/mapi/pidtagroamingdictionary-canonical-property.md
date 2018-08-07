---
title: Каноническое свойство PidTagRoamingDictionary
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRoamingDictionary
api_type:
- COM
ms.assetid: 40b50181-f88c-40ee-b3d0-a36dd36c158e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 41d1a4abe79892fa1c9c8789e159a19645318497
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811757"
---
# <a name="pidtagroamingdictionary-canonical-property"></a><span data-ttu-id="f3df8-103">Каноническое свойство PidTagRoamingDictionary</span><span class="sxs-lookup"><span data-stu-id="f3df8-103">PidTagRoamingDictionary Canonical Property</span></span>

<span data-ttu-id="f3df8-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f3df8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f3df8-105">Содержит XML-документ, описывающий перемещения словаря.</span><span class="sxs-lookup"><span data-stu-id="f3df8-105">Contains an XML document that describes the roaming dictionary.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f3df8-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="f3df8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f3df8-107">PR_ROAMING_DICTIONARY</span><span class="sxs-lookup"><span data-stu-id="f3df8-107">PR_ROAMING_DICTIONARY</span></span>  <br/> |
|<span data-ttu-id="f3df8-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="f3df8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f3df8-109">0x7C07</span><span class="sxs-lookup"><span data-stu-id="f3df8-109">0x7C07</span></span>  <br/> |
|<span data-ttu-id="f3df8-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="f3df8-110">Data type:</span></span>  <br/> |<span data-ttu-id="f3df8-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="f3df8-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="f3df8-112">Область:</span><span class="sxs-lookup"><span data-stu-id="f3df8-112">Area:</span></span>  <br/> |<span data-ttu-id="f3df8-113">Конфигурация</span><span class="sxs-lookup"><span data-stu-id="f3df8-113">Configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f3df8-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="f3df8-114">Remarks</span></span>

<span data-ttu-id="f3df8-115">Это свойство содержит Юникод XML-документ, с использованием кодировки UTF8.</span><span class="sxs-lookup"><span data-stu-id="f3df8-115">This property contains a UNICODE XML document that is using UTF8 encoding.</span></span> <span data-ttu-id="f3df8-116">Сообщение с потоком словаря необходимо установить это свойство со следующей схемой:</span><span class="sxs-lookup"><span data-stu-id="f3df8-116">A message with a dictionary stream must set this property with the following schema:</span></span>
  
```xml
<?xml version="1.0" encoding="utf-8"?> 
<xs:schema targetNamespace="Dictionary.xsd" xmlns="Dictionary.xsd" xmlns:xs="http://www.w3.org/2001/XMLSchema"> 
   <xs:element name="UserConfiguration"> 
   <xs:complexType> 
   <xs:sequence> 
   <xs:element name="Info"> 
   <xs:complexType> 
   <xs:sequence /> 
   <xs:attribute name="version" type="VersionString"> 
   </xs:attribute> 
   </xs:complexType>
```

<span data-ttu-id="f3df8-117">Ниже приведен пример документа XML, хранящиеся в этом свойстве на сообщение данные конфигурации:</span><span class="sxs-lookup"><span data-stu-id="f3df8-117">The following is a sample XML document stored in this property on a Configuration Data message:</span></span> 
  
```xml
<?xml version="1.0"?> 
<UserConfiguration> 
<Info version="Outlook.12"/> 
<Data> <e k="18-piAutoProcess" v="3-True"/> 
<e k="18-piRemindDefault" v="9-15"/> 
<e k="18-piReminderUpgradeTime" v="9-212864507"/> 
<e k="18-OLPrefsVersion" v="9-1"/> 
</Data> 
</UserConfiguration>
```

## <a name="related-resources"></a><span data-ttu-id="f3df8-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f3df8-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f3df8-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="f3df8-119">Protocol specifications</span></span>

<span data-ttu-id="f3df8-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f3df8-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f3df8-121">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="f3df8-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f3df8-122">[[MS-OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f3df8-122">[[MS-OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f3df8-123">Указывает расположение и свойства клиентских и серверных данных конфигурации, такие как списки общие категории и рабочее время.</span><span class="sxs-lookup"><span data-stu-id="f3df8-123">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f3df8-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="f3df8-124">Header files</span></span>

<span data-ttu-id="f3df8-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f3df8-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="f3df8-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="f3df8-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="f3df8-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f3df8-127">Mapitags.h</span></span>
  
> <span data-ttu-id="f3df8-128">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="f3df8-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f3df8-129">См. также</span><span class="sxs-lookup"><span data-stu-id="f3df8-129">See also</span></span>



[<span data-ttu-id="f3df8-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f3df8-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f3df8-131">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f3df8-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f3df8-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="f3df8-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f3df8-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="f3df8-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

