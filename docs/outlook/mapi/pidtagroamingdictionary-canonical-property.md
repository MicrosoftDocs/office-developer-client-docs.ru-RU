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
ms.openlocfilehash: 4b2aa12b1b81dfd218781a839f5f84881763ef06
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359551"
---
# <a name="pidtagroamingdictionary-canonical-property"></a><span data-ttu-id="a6920-103">Каноническое свойство PidTagRoamingDictionary</span><span class="sxs-lookup"><span data-stu-id="a6920-103">PidTagRoamingDictionary Canonical Property</span></span>

<span data-ttu-id="a6920-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a6920-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a6920-105">Содержит XML-документ, описывающий перемещающийся словарь.</span><span class="sxs-lookup"><span data-stu-id="a6920-105">Contains an XML document that describes the roaming dictionary.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a6920-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="a6920-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a6920-107">PR_ROAMING_DICTIONARY</span><span class="sxs-lookup"><span data-stu-id="a6920-107">PR_ROAMING_DICTIONARY</span></span>  <br/> |
|<span data-ttu-id="a6920-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="a6920-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a6920-109">0x7C07</span><span class="sxs-lookup"><span data-stu-id="a6920-109">0x7C07</span></span>  <br/> |
|<span data-ttu-id="a6920-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="a6920-110">Data type:</span></span>  <br/> |<span data-ttu-id="a6920-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="a6920-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="a6920-112">Область:</span><span class="sxs-lookup"><span data-stu-id="a6920-112">Area:</span></span>  <br/> |<span data-ttu-id="a6920-113">Конфигурация</span><span class="sxs-lookup"><span data-stu-id="a6920-113">Configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a6920-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="a6920-114">Remarks</span></span>

<span data-ttu-id="a6920-115">Это свойство содержит XML-документ Юникод, использующий кодировки UTF8.</span><span class="sxs-lookup"><span data-stu-id="a6920-115">This property contains a UNICODE XML document that is using UTF8 encoding.</span></span> <span data-ttu-id="a6920-116">Сообщение с потоком словаря должно устанавливать это свойство со следующей схемой:</span><span class="sxs-lookup"><span data-stu-id="a6920-116">A message with a dictionary stream must set this property with the following schema:</span></span>
  
```xml
<?xml version="1.0" encoding="utf-8"?> 
<xs:schema targetNamespace="Dictionary.xsd" xmlns="Dictionary.xsd" xmlns:xs="https://www.w3.org/2001/XMLSchema"> 
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

<span data-ttu-id="a6920-117">Ниже приводится пример XML-документа, хранимый в этом свойстве в сообщении configuration Data:</span><span class="sxs-lookup"><span data-stu-id="a6920-117">The following is a sample XML document stored in this property on a Configuration Data message:</span></span> 
  
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

## <a name="related-resources"></a><span data-ttu-id="a6920-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="a6920-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a6920-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="a6920-119">Protocol specifications</span></span>

<span data-ttu-id="a6920-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a6920-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a6920-121">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="a6920-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a6920-122">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a6920-122">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a6920-123">Указывает расположение и свойства данных конфигурации клиента и сервера, например списки общих категорий и рабочие часы.</span><span class="sxs-lookup"><span data-stu-id="a6920-123">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a6920-124">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="a6920-124">Header files</span></span>

<span data-ttu-id="a6920-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a6920-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="a6920-126">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="a6920-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="a6920-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a6920-127">Mapitags.h</span></span>
  
> <span data-ttu-id="a6920-128">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="a6920-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a6920-129">См. также</span><span class="sxs-lookup"><span data-stu-id="a6920-129">See also</span></span>



[<span data-ttu-id="a6920-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a6920-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a6920-131">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a6920-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a6920-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="a6920-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a6920-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="a6920-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

