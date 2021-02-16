---
title: Каноническое свойство PidTagAttachmentContactPhoto
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachmentContactPhoto
api_type:
- HeaderDef
ms.assetid: ea5b77b7-8440-4e54-abd2-c475138c8f63
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 5d61289349306b763d13a9a2111c2cd02ff3937e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345768"
---
# <a name="pidtagattachmentcontactphoto-canonical-property"></a><span data-ttu-id="48c88-103">Каноническое свойство PidTagAttachmentContactPhoto</span><span class="sxs-lookup"><span data-stu-id="48c88-103">PidTagAttachmentContactPhoto Canonical Property</span></span>

  
  
<span data-ttu-id="48c88-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="48c88-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="48c88-105">Указывает на наличие вложения фотографии для контакта.</span><span class="sxs-lookup"><span data-stu-id="48c88-105">Indicates the existence of a photo attachment for a contact.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="48c88-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="48c88-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="48c88-107">PR_ATTACHMENT_CONTACTPHOTO</span><span class="sxs-lookup"><span data-stu-id="48c88-107">PR_ATTACHMENT_CONTACTPHOTO</span></span>  <br/> |
|<span data-ttu-id="48c88-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="48c88-108">Identifier:</span></span>  <br/> |<span data-ttu-id="48c88-109">0x7FFF</span><span class="sxs-lookup"><span data-stu-id="48c88-109">0x7FFF</span></span>  <br/> |
|<span data-ttu-id="48c88-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="48c88-110">Data type:</span></span>  <br/> |<span data-ttu-id="48c88-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="48c88-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="48c88-112">Область:</span><span class="sxs-lookup"><span data-stu-id="48c88-112">Area:</span></span>  <br/> |<span data-ttu-id="48c88-113">Вложение в сообщение</span><span class="sxs-lookup"><span data-stu-id="48c88-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="48c88-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="48c88-114">Remarks</span></span>

<span data-ttu-id="48c88-115">Для этого свойства должно быть задано значение TRUE, и для данного объекта Contact должно быть только одно вложение.</span><span class="sxs-lookup"><span data-stu-id="48c88-115">This property's value must be set to TRUE, and there should only be one attachment on a given Contact object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="48c88-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="48c88-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="48c88-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="48c88-117">Protocol specifications</span></span>

<span data-ttu-id="48c88-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="48c88-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="48c88-119">Предоставляет определения наборов свойств и ссылки на связанные Exchange Server спецификации протокола.</span><span class="sxs-lookup"><span data-stu-id="48c88-119">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="48c88-120">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="48c88-120">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="48c88-121">Указывает свойства и операции, которые разрешены для контактов и личных списков рассылки.</span><span class="sxs-lookup"><span data-stu-id="48c88-121">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="48c88-122">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="48c88-122">Header files</span></span>

<span data-ttu-id="48c88-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="48c88-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="48c88-124">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="48c88-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="48c88-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="48c88-125">Mapitags.h</span></span>
  
> <span data-ttu-id="48c88-126">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="48c88-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="48c88-127">См. также</span><span class="sxs-lookup"><span data-stu-id="48c88-127">See also</span></span>



[<span data-ttu-id="48c88-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="48c88-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="48c88-129">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="48c88-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="48c88-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="48c88-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="48c88-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="48c88-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

