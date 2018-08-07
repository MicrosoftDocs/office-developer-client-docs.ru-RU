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
ms.openlocfilehash: 8e241022504291ad70f45a3318a7901bbbba213f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810212"
---
# <a name="pidlidbusinesscardcardpicture-canonical-property"></a><span data-ttu-id="633ba-103">Каноническое свойство PidLidBusinessCardCardPicture</span><span class="sxs-lookup"><span data-stu-id="633ba-103">PidLidBusinessCardCardPicture Canonical Property</span></span>

  
  
<span data-ttu-id="633ba-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="633ba-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="633ba-105">Содержит изображения, используемого на визитной карточки.</span><span class="sxs-lookup"><span data-stu-id="633ba-105">Contains the image to use on a business card.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="633ba-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="633ba-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="633ba-107">dispidBCCardPicture</span><span class="sxs-lookup"><span data-stu-id="633ba-107">dispidBCCardPicture</span></span>  <br/> |
|<span data-ttu-id="633ba-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="633ba-108">Property set:</span></span>  <br/> |<span data-ttu-id="633ba-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="633ba-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="633ba-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="633ba-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="633ba-111">0x00008041</span><span class="sxs-lookup"><span data-stu-id="633ba-111">0x00008041</span></span>  <br/> |
|<span data-ttu-id="633ba-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="633ba-112">Data type:</span></span>  <br/> |<span data-ttu-id="633ba-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="633ba-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="633ba-114">Область:</span><span class="sxs-lookup"><span data-stu-id="633ba-114">Area:</span></span>  <br/> |<span data-ttu-id="633ba-115">Контакт</span><span class="sxs-lookup"><span data-stu-id="633ba-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="633ba-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="633ba-116">Remarks</span></span>

<span data-ttu-id="633ba-117">Значение этого свойства должны быть потока JPEG или в формате PNG (PNG).</span><span class="sxs-lookup"><span data-stu-id="633ba-117">The value of this property must be either a portable network graphics (PNG) or JPEG stream.</span></span> <span data-ttu-id="633ba-118">Это свойство следует использовать в сочетании со свойством **dispidBCDisplayDefinition** ([PidLidBusinessCardDisplayDefinition](pidlidbusinesscarddisplaydefinition-canonical-property.md)) следующим образом: **dispidBCCardPicture** не должна быть установлена на контакта if ** dispidBCDisplayDefinition** не установлена.</span><span class="sxs-lookup"><span data-stu-id="633ba-118">This property should be used in conjunction with the **dispidBCDisplayDefinition** ([PidLidBusinessCardDisplayDefinition](pidlidbusinesscarddisplaydefinition-canonical-property.md)) property as follows: **dispidBCCardPicture** should not be present on a contact if **dispidBCDisplayDefinition** is not present.</span></span> <span data-ttu-id="633ba-119">Это свойство также не должна быть этот параметр указан, если данные в **dispidBCCardPicture** не требуется изображение карточки.</span><span class="sxs-lookup"><span data-stu-id="633ba-119">This property also should not be present if the data in **dispidBCCardPicture** does not require a card image.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="633ba-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="633ba-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="633ba-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="633ba-121">Protocol specifications</span></span>

<span data-ttu-id="633ba-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="633ba-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="633ba-123">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="633ba-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="633ba-124">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="633ba-124">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="633ba-125">Задает свойства и операции, допустимые для контакты и списки рассылки.</span><span class="sxs-lookup"><span data-stu-id="633ba-125">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="633ba-126">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="633ba-126">Header files</span></span>

<span data-ttu-id="633ba-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="633ba-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="633ba-128">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="633ba-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="633ba-129">См. также</span><span class="sxs-lookup"><span data-stu-id="633ba-129">See also</span></span>



[<span data-ttu-id="633ba-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="633ba-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="633ba-131">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="633ba-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="633ba-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="633ba-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="633ba-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="633ba-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

