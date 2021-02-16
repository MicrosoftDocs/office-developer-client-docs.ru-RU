---
title: Каноническое свойство PidTagLocation
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagLocation
api_type:
- HeaderDef
ms.assetid: 99dffcd9-83dc-462e-b0ce-e2101e546cc6
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 558db0d89103d02f37297c058384cac96ea9ca26
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278787"
---
# <a name="pidtaglocation-canonical-property"></a><span data-ttu-id="dbbdc-103">Каноническое свойство PidTagLocation</span><span class="sxs-lookup"><span data-stu-id="dbbdc-103">PidTagLocation Canonical Property</span></span>

  
  
<span data-ttu-id="dbbdc-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dbbdc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dbbdc-105">Содержит расположение получателя в формате, удобном для организации получателя.</span><span class="sxs-lookup"><span data-stu-id="dbbdc-105">Contains the location of the recipient in a format that is useful to the recipient's organization.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dbbdc-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="dbbdc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="dbbdc-107">PR_LOCATION, PR_LOCATION_A, PR_LOCATION_W</span><span class="sxs-lookup"><span data-stu-id="dbbdc-107">PR_LOCATION, PR_LOCATION_A, PR_LOCATION_W</span></span>  <br/> |
|<span data-ttu-id="dbbdc-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="dbbdc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="dbbdc-109">0x3A0D</span><span class="sxs-lookup"><span data-stu-id="dbbdc-109">0x3A0D</span></span>  <br/> |
|<span data-ttu-id="dbbdc-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="dbbdc-110">Data type:</span></span>  <br/> |<span data-ttu-id="dbbdc-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="dbbdc-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="dbbdc-112">Область:</span><span class="sxs-lookup"><span data-stu-id="dbbdc-112">Area:</span></span>  <br/> |<span data-ttu-id="dbbdc-113">Address</span><span class="sxs-lookup"><span data-stu-id="dbbdc-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dbbdc-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="dbbdc-114">Remarks</span></span>

<span data-ttu-id="dbbdc-115">Эти свойства предоставляют сведения об идентификации и доступе для получателя.</span><span class="sxs-lookup"><span data-stu-id="dbbdc-115">These properties provide identification and access information for a recipient.</span></span> <span data-ttu-id="dbbdc-116">Они определяются получателем и его организацией.</span><span class="sxs-lookup"><span data-stu-id="dbbdc-116">They are defined by the recipient and their organization.</span></span> 
  
<span data-ttu-id="dbbdc-117">Содержимое определяется потребностями организации получателя.</span><span class="sxs-lookup"><span data-stu-id="dbbdc-117">The contents are defined by the needs of the recipient's organization.</span></span> <span data-ttu-id="dbbdc-118">Например, некоторые организации могут определить пользователей сообщений, указав номер здания и номер офиса.</span><span class="sxs-lookup"><span data-stu-id="dbbdc-118">For example, some organizations might identify messaging users by specifying the building number and office number.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="dbbdc-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="dbbdc-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="dbbdc-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="dbbdc-120">Protocol specifications</span></span>

<span data-ttu-id="dbbdc-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dbbdc-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dbbdc-122">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="dbbdc-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="dbbdc-123">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dbbdc-123">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dbbdc-124">Указывает свойства и операции, которые разрешены для контактов и личных списков рассылки.</span><span class="sxs-lookup"><span data-stu-id="dbbdc-124">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="dbbdc-125">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dbbdc-125">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dbbdc-126">Указывает свойства и операции для списков пользователей, контактов, групп и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dbbdc-126">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="dbbdc-127">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="dbbdc-127">Header files</span></span>

<span data-ttu-id="dbbdc-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="dbbdc-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="dbbdc-129">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="dbbdc-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="dbbdc-130">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="dbbdc-130">Mapitags.h</span></span>
  
> <span data-ttu-id="dbbdc-131">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="dbbdc-131">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dbbdc-132">См. также</span><span class="sxs-lookup"><span data-stu-id="dbbdc-132">See also</span></span>



[<span data-ttu-id="dbbdc-133">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="dbbdc-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="dbbdc-134">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="dbbdc-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="dbbdc-135">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="dbbdc-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="dbbdc-136">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="dbbdc-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

