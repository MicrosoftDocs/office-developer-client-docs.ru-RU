---
title: Каноническое свойство PidNameRightsManagementLicense
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameRightsManagementLicense
api_type:
- COM
ms.assetid: ca3c9317-7873-4f37-b78f-b35467c81c29
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 889b823a55c39ebc19e52c8cc9a1d078a5732a01
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315024"
---
# <a name="pidnamerightsmanagementlicense-canonical-property"></a><span data-ttu-id="3bcfb-103">Каноническое свойство PidNameRightsManagementLicense</span><span class="sxs-lookup"><span data-stu-id="3bcfb-103">PidNameRightsManagementLicense Canonical Property</span></span>

  
  
<span data-ttu-id="3bcfb-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3bcfb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3bcfb-105">Кэширует лицензию на использование для сообщения электронной почты с управляемыми правами.</span><span class="sxs-lookup"><span data-stu-id="3bcfb-105">Caches the use license for the rights-managed email message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3bcfb-106">Понятные имена:</span><span class="sxs-lookup"><span data-stu-id="3bcfb-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="3bcfb-107">Нет</span><span class="sxs-lookup"><span data-stu-id="3bcfb-107">None</span></span>  <br/> |
|<span data-ttu-id="3bcfb-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="3bcfb-108">Property set:</span></span>  <br/> |<span data-ttu-id="3bcfb-109">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="3bcfb-109">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="3bcfb-110">Имя свойства:</span><span class="sxs-lookup"><span data-stu-id="3bcfb-110">Property name:</span></span>  <br/> |<span data-ttu-id="3bcfb-111">дрмлиценсе</span><span class="sxs-lookup"><span data-stu-id="3bcfb-111">DRMLicense</span></span>  <br/> |
|<span data-ttu-id="3bcfb-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="3bcfb-112">Data type:</span></span>  <br/> |<span data-ttu-id="3bcfb-113">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="3bcfb-113">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="3bcfb-114">Область:</span><span class="sxs-lookup"><span data-stu-id="3bcfb-114">Area:</span></span>  <br/> |<span data-ttu-id="3bcfb-115">Защита обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="3bcfb-115">Secure messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3bcfb-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="3bcfb-116">Remarks</span></span>

<span data-ttu-id="3bcfb-117">Если свойство присутствует в сообщении электронной почты, управляемом правами, то первое значение этого нескольких двоичных свойств должно содержать ЗЛИБ (как указано в разделе [RFC1950]) сжатый лицензионный протокол для сообщения электронной почты, управляемого правами.</span><span class="sxs-lookup"><span data-stu-id="3bcfb-117">If the property is present on a rights-managed email message, the first value of this multiple binary property must contain the ZLIB (as specified in [RFC1950]) compressed use license for the rights-managed email message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3bcfb-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="3bcfb-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3bcfb-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="3bcfb-119">Protocol specifications</span></span>

<span data-ttu-id="3bcfb-120">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3bcfb-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3bcfb-121">Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="3bcfb-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3bcfb-122">[[MS — ОКСОРММС]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3bcfb-122">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3bcfb-123">Задает свойства сообщений, закодированных с помощью управления правами.</span><span class="sxs-lookup"><span data-stu-id="3bcfb-123">Specifies the properties of rights-managed encoded messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3bcfb-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="3bcfb-124">Header files</span></span>

<span data-ttu-id="3bcfb-125">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="3bcfb-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="3bcfb-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="3bcfb-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3bcfb-127">См. также</span><span class="sxs-lookup"><span data-stu-id="3bcfb-127">See also</span></span>



[<span data-ttu-id="3bcfb-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="3bcfb-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3bcfb-129">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="3bcfb-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3bcfb-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="3bcfb-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3bcfb-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="3bcfb-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

