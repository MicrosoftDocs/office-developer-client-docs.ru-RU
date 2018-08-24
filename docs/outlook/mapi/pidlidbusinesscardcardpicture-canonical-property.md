---
title: Каноническое свойство PidLidBusinessCardCardPicture
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidBusinessCardCardPicture
api_type:
- COM
ms.assetid: 2c7af147-f7eb-41ef-8403-93584a2041ba
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 1b83316b599ea9ee62bde78cbd734dfb6b2d8b80
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588498"
---
# <a name="pidlidbusinesscardcardpicture-canonical-property"></a><span data-ttu-id="d63fa-103">Каноническое свойство PidLidBusinessCardCardPicture</span><span class="sxs-lookup"><span data-stu-id="d63fa-103">PidLidBusinessCardCardPicture Canonical Property</span></span>

  
  
<span data-ttu-id="d63fa-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d63fa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d63fa-105">Содержит изображения, используемого на визитной карточки.</span><span class="sxs-lookup"><span data-stu-id="d63fa-105">Contains the image to use on a business card.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d63fa-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="d63fa-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d63fa-107">dispidBCCardPicture</span><span class="sxs-lookup"><span data-stu-id="d63fa-107">dispidBCCardPicture</span></span>  <br/> |
|<span data-ttu-id="d63fa-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="d63fa-108">Property set:</span></span>  <br/> |<span data-ttu-id="d63fa-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="d63fa-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="d63fa-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="d63fa-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="d63fa-111">0x00008041</span><span class="sxs-lookup"><span data-stu-id="d63fa-111">0x00008041</span></span>  <br/> |
|<span data-ttu-id="d63fa-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="d63fa-112">Data type:</span></span>  <br/> |<span data-ttu-id="d63fa-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="d63fa-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="d63fa-114">Область:</span><span class="sxs-lookup"><span data-stu-id="d63fa-114">Area:</span></span>  <br/> |<span data-ttu-id="d63fa-115">Contact</span><span class="sxs-lookup"><span data-stu-id="d63fa-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d63fa-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="d63fa-116">Remarks</span></span>

<span data-ttu-id="d63fa-117">Значение этого свойства должны быть потока JPEG или в формате PNG (PNG).</span><span class="sxs-lookup"><span data-stu-id="d63fa-117">The value of this property must be either a portable network graphics (PNG) or JPEG stream.</span></span> <span data-ttu-id="d63fa-118">Это свойство следует использовать в сочетании со свойством **dispidBCDisplayDefinition** ([PidLidBusinessCardDisplayDefinition](pidlidbusinesscarddisplaydefinition-canonical-property.md)) следующим образом: **dispidBCCardPicture** не должна быть установлена на контакта if ** dispidBCDisplayDefinition** не установлена.</span><span class="sxs-lookup"><span data-stu-id="d63fa-118">This property should be used in conjunction with the **dispidBCDisplayDefinition** ([PidLidBusinessCardDisplayDefinition](pidlidbusinesscarddisplaydefinition-canonical-property.md)) property as follows: **dispidBCCardPicture** should not be present on a contact if **dispidBCDisplayDefinition** is not present.</span></span> <span data-ttu-id="d63fa-119">Это свойство также не должна быть этот параметр указан, если данные в **dispidBCCardPicture** не требуется изображение карточки.</span><span class="sxs-lookup"><span data-stu-id="d63fa-119">This property also should not be present if the data in **dispidBCCardPicture** does not require a card image.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d63fa-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d63fa-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d63fa-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="d63fa-121">Protocol specifications</span></span>

<span data-ttu-id="d63fa-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d63fa-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d63fa-123">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="d63fa-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d63fa-124">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d63fa-124">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d63fa-125">Задает свойства и операции, допустимые для контакты и списки рассылки.</span><span class="sxs-lookup"><span data-stu-id="d63fa-125">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d63fa-126">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="d63fa-126">Header files</span></span>

<span data-ttu-id="d63fa-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d63fa-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="d63fa-128">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="d63fa-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d63fa-129">См. также</span><span class="sxs-lookup"><span data-stu-id="d63fa-129">See also</span></span>



[<span data-ttu-id="d63fa-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d63fa-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d63fa-131">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d63fa-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d63fa-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="d63fa-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d63fa-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="d63fa-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

