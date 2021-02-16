---
title: Каноническое свойство PidLidHasPicture
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidHasPicture
api_type:
- COM
ms.assetid: c3bea11c-3197-4060-8672-f1b4bf352112
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3aef2fc1038751c9ad6fb97cf347c2dcab114fda
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357752"
---
# <a name="pidlidhaspicture-canonical-property"></a><span data-ttu-id="f989e-103">Каноническое свойство PidLidHasPicture</span><span class="sxs-lookup"><span data-stu-id="f989e-103">PidLidHasPicture Canonical Property</span></span>

  
  
<span data-ttu-id="f989e-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f989e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f989e-105">Указывает, существует ли вложение фотографии для контакта.</span><span class="sxs-lookup"><span data-stu-id="f989e-105">Specifies whether a photo attachment exists for a contact.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f989e-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="f989e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f989e-107">dispidHasPicture</span><span class="sxs-lookup"><span data-stu-id="f989e-107">dispidHasPicture</span></span>  <br/> |
|<span data-ttu-id="f989e-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="f989e-108">Property set:</span></span>  <br/> |<span data-ttu-id="f989e-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="f989e-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="f989e-110">Длинный ИД (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="f989e-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="f989e-111">0x00008015</span><span class="sxs-lookup"><span data-stu-id="f989e-111">0x00008015</span></span>  <br/> |
|<span data-ttu-id="f989e-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="f989e-112">Data type:</span></span>  <br/> |<span data-ttu-id="f989e-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="f989e-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="f989e-114">Область:</span><span class="sxs-lookup"><span data-stu-id="f989e-114">Area:</span></span>  <br/> |<span data-ttu-id="f989e-115">Контакт</span><span class="sxs-lookup"><span data-stu-id="f989e-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f989e-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="f989e-116">Remarks</span></span>

<span data-ttu-id="f989e-117">Если это свойство существует и имеет свойство TRUE, таблица вложений контакта содержит **вложение** со свойством PR_ATTACHMENT_CONTACTPHOTO ([PidTagAttachmentContactPhoto),](pidtagattachmentcontactphoto-canonical-property.md)задаваемой true.</span><span class="sxs-lookup"><span data-stu-id="f989e-117">If this property exists and is set to TRUE, the contact's attachment table contains an attachment with the **PR_ATTACHMENT_CONTACTPHOTO** ([PidTagAttachmentContactPhoto](pidtagattachmentcontactphoto-canonical-property.md)) property set to TRUE.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f989e-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f989e-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f989e-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="f989e-119">Protocol specifications</span></span>

<span data-ttu-id="f989e-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f989e-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f989e-121">Предоставляет определения наборов свойств и ссылки на связанные Exchange Server спецификации протокола.</span><span class="sxs-lookup"><span data-stu-id="f989e-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f989e-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f989e-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f989e-123">Указывает свойства и операции, которые разрешены для контактов и личных списков рассылки.</span><span class="sxs-lookup"><span data-stu-id="f989e-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f989e-124">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="f989e-124">Header files</span></span>

<span data-ttu-id="f989e-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f989e-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="f989e-126">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="f989e-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f989e-127">См. также</span><span class="sxs-lookup"><span data-stu-id="f989e-127">See also</span></span>



[<span data-ttu-id="f989e-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f989e-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f989e-129">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f989e-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f989e-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="f989e-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f989e-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="f989e-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

