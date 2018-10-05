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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395548"
---
# <a name="pidnamerightsmanagementlicense-canonical-property"></a><span data-ttu-id="9ea5f-103">Каноническое свойство PidNameRightsManagementLicense</span><span class="sxs-lookup"><span data-stu-id="9ea5f-103">PidNameRightsManagementLicense Canonical Property</span></span>

  
  
<span data-ttu-id="9ea5f-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9ea5f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9ea5f-105">Кэширует лицензии на использование для сообщения электронной почты с управлением правами.</span><span class="sxs-lookup"><span data-stu-id="9ea5f-105">Caches the use license for the rights-managed email message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9ea5f-106">Понятные имена:</span><span class="sxs-lookup"><span data-stu-id="9ea5f-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="9ea5f-107">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="9ea5f-107">None</span></span>  <br/> |
|<span data-ttu-id="9ea5f-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="9ea5f-108">Property set:</span></span>  <br/> |<span data-ttu-id="9ea5f-109">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="9ea5f-109">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="9ea5f-110">Имя свойства:</span><span class="sxs-lookup"><span data-stu-id="9ea5f-110">Property name:</span></span>  <br/> |<span data-ttu-id="9ea5f-111">DRMLicense</span><span class="sxs-lookup"><span data-stu-id="9ea5f-111">DRMLicense</span></span>  <br/> |
|<span data-ttu-id="9ea5f-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="9ea5f-112">Data type:</span></span>  <br/> |<span data-ttu-id="9ea5f-113">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="9ea5f-113">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="9ea5f-114">Область:</span><span class="sxs-lookup"><span data-stu-id="9ea5f-114">Area:</span></span>  <br/> |<span data-ttu-id="9ea5f-115">Безопасный обмен сообщениями</span><span class="sxs-lookup"><span data-stu-id="9ea5f-115">Secure messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9ea5f-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="9ea5f-116">Remarks</span></span>

<span data-ttu-id="9ea5f-117">Если свойство присутствует в сообщении электронной почты с управлением правами, первое значение в этом нескольких двоичного свойства должно содержать ZLIB (как указано в [RFC1950]) сжатых лицензию для сообщения электронной почты с управлением правами.</span><span class="sxs-lookup"><span data-stu-id="9ea5f-117">If the property is present on a rights-managed email message, the first value of this multiple binary property must contain the ZLIB (as specified in [RFC1950]) compressed use license for the rights-managed email message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9ea5f-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="9ea5f-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9ea5f-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="9ea5f-119">Protocol specifications</span></span>

<span data-ttu-id="9ea5f-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9ea5f-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9ea5f-121">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="9ea5f-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9ea5f-122">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9ea5f-122">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9ea5f-123">Задает свойства управляемый правами закодированный сообщений.</span><span class="sxs-lookup"><span data-stu-id="9ea5f-123">Specifies the properties of rights-managed encoded messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9ea5f-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="9ea5f-124">Header files</span></span>

<span data-ttu-id="9ea5f-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9ea5f-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="9ea5f-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="9ea5f-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9ea5f-127">См. также</span><span class="sxs-lookup"><span data-stu-id="9ea5f-127">See also</span></span>



[<span data-ttu-id="9ea5f-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="9ea5f-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9ea5f-129">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="9ea5f-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9ea5f-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="9ea5f-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9ea5f-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="9ea5f-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

