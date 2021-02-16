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
# <a name="pidnamerightsmanagementlicense-canonical-property"></a><span data-ttu-id="af780-103">Каноническое свойство PidNameRightsManagementLicense</span><span class="sxs-lookup"><span data-stu-id="af780-103">PidNameRightsManagementLicense Canonical Property</span></span>

  
  
<span data-ttu-id="af780-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="af780-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="af780-105">Кэшрует лицензию на использование сообщения электронной почты, управляемого правами.</span><span class="sxs-lookup"><span data-stu-id="af780-105">Caches the use license for the rights-managed email message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="af780-106">Дружелюбные имена:</span><span class="sxs-lookup"><span data-stu-id="af780-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="af780-107">Нет</span><span class="sxs-lookup"><span data-stu-id="af780-107">None</span></span>  <br/> |
|<span data-ttu-id="af780-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="af780-108">Property set:</span></span>  <br/> |<span data-ttu-id="af780-109">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="af780-109">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="af780-110">Имя свойства:</span><span class="sxs-lookup"><span data-stu-id="af780-110">Property name:</span></span>  <br/> |<span data-ttu-id="af780-111">DRMLicense</span><span class="sxs-lookup"><span data-stu-id="af780-111">DRMLicense</span></span>  <br/> |
|<span data-ttu-id="af780-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="af780-112">Data type:</span></span>  <br/> |<span data-ttu-id="af780-113">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="af780-113">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="af780-114">Область:</span><span class="sxs-lookup"><span data-stu-id="af780-114">Area:</span></span>  <br/> |<span data-ttu-id="af780-115">Безопасный обмен сообщениями</span><span class="sxs-lookup"><span data-stu-id="af780-115">Secure messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="af780-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="af780-116">Remarks</span></span>

<span data-ttu-id="af780-117">Если свойство присутствует в сообщении электронной почты, управляемом правами, первое значение этого нескольких двоичных свойств должно содержать лицензию на сжатие ZLIB (как указано в [RFC1950]) для сообщения электронной почты, управляемого правами.</span><span class="sxs-lookup"><span data-stu-id="af780-117">If the property is present on a rights-managed email message, the first value of this multiple binary property must contain the ZLIB (as specified in [RFC1950]) compressed use license for the rights-managed email message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="af780-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="af780-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="af780-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="af780-119">Protocol specifications</span></span>

<span data-ttu-id="af780-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="af780-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="af780-121">Предоставляет определения наборов свойств и ссылки на связанные Exchange Server спецификации протокола.</span><span class="sxs-lookup"><span data-stu-id="af780-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="af780-122">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="af780-122">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="af780-123">Указывает свойства сообщений в кодированной кодировки с управлением правами.</span><span class="sxs-lookup"><span data-stu-id="af780-123">Specifies the properties of rights-managed encoded messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="af780-124">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="af780-124">Header files</span></span>

<span data-ttu-id="af780-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="af780-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="af780-126">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="af780-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="af780-127">См. также</span><span class="sxs-lookup"><span data-stu-id="af780-127">See also</span></span>



[<span data-ttu-id="af780-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="af780-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="af780-129">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="af780-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="af780-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="af780-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="af780-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="af780-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

