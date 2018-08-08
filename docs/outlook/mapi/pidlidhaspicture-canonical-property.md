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
ms.openlocfilehash: 74a54db3ebb55c178fd5f8b7317bb27c83a47311
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810381"
---
# <a name="pidlidhaspicture-canonical-property"></a><span data-ttu-id="1d42a-103">Каноническое свойство PidLidHasPicture</span><span class="sxs-lookup"><span data-stu-id="1d42a-103">PidLidHasPicture Canonical Property</span></span>

  
  
<span data-ttu-id="1d42a-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1d42a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1d42a-105">Указывает, существует ли подключение к фотографии контакта.</span><span class="sxs-lookup"><span data-stu-id="1d42a-105">Specifies whether a photo attachment exists for a contact.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1d42a-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="1d42a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1d42a-107">dispidHasPicture</span><span class="sxs-lookup"><span data-stu-id="1d42a-107">dispidHasPicture</span></span>  <br/> |
|<span data-ttu-id="1d42a-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="1d42a-108">Property set:</span></span>  <br/> |<span data-ttu-id="1d42a-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="1d42a-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="1d42a-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="1d42a-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="1d42a-111">0x00008015</span><span class="sxs-lookup"><span data-stu-id="1d42a-111">0x00008015</span></span>  <br/> |
|<span data-ttu-id="1d42a-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="1d42a-112">Data type:</span></span>  <br/> |<span data-ttu-id="1d42a-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="1d42a-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="1d42a-114">Область:</span><span class="sxs-lookup"><span data-stu-id="1d42a-114">Area:</span></span>  <br/> |<span data-ttu-id="1d42a-115">Контакт</span><span class="sxs-lookup"><span data-stu-id="1d42a-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1d42a-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="1d42a-116">Remarks</span></span>

<span data-ttu-id="1d42a-117">Если это свойство существует и имеет значение TRUE, в таблице вложения контакта содержит вложение со свойством **PR_ATTACHMENT_CONTACTPHOTO** ([PidTagAttachmentContactPhoto](pidtagattachmentcontactphoto-canonical-property.md)), задайте значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="1d42a-117">If this property exists and is set to TRUE, the contact's attachment table contains an attachment with the **PR_ATTACHMENT_CONTACTPHOTO** ([PidTagAttachmentContactPhoto](pidtagattachmentcontactphoto-canonical-property.md)) property set to TRUE.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1d42a-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="1d42a-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1d42a-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="1d42a-119">Protocol specifications</span></span>

<span data-ttu-id="1d42a-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1d42a-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1d42a-121">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="1d42a-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1d42a-122">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1d42a-122">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1d42a-123">Задает свойства и операции, допустимые для контакты и списки рассылки.</span><span class="sxs-lookup"><span data-stu-id="1d42a-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1d42a-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="1d42a-124">Header files</span></span>

<span data-ttu-id="1d42a-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1d42a-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="1d42a-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="1d42a-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1d42a-127">См. также</span><span class="sxs-lookup"><span data-stu-id="1d42a-127">See also</span></span>



[<span data-ttu-id="1d42a-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="1d42a-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1d42a-129">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="1d42a-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1d42a-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="1d42a-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1d42a-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="1d42a-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

