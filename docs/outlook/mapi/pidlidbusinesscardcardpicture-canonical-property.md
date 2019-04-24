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
ms.openlocfilehash: fd1ad923acca5a75d06e6b15ae7ae7411edefb92
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342009"
---
# <a name="pidlidbusinesscardcardpicture-canonical-property"></a><span data-ttu-id="08b46-103">Каноническое свойство PidLidBusinessCardCardPicture</span><span class="sxs-lookup"><span data-stu-id="08b46-103">PidLidBusinessCardCardPicture Canonical Property</span></span>

  
  
<span data-ttu-id="08b46-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="08b46-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="08b46-105">Содержит изображение, которое будет использоваться для визитной карточки.</span><span class="sxs-lookup"><span data-stu-id="08b46-105">Contains the image to use on a business card.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="08b46-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="08b46-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="08b46-107">Диспидбккардпиктуре</span><span class="sxs-lookup"><span data-stu-id="08b46-107">dispidBCCardPicture</span></span>  <br/> |
|<span data-ttu-id="08b46-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="08b46-108">Property set:</span></span>  <br/> |<span data-ttu-id="08b46-109">Псетид_аддресс</span><span class="sxs-lookup"><span data-stu-id="08b46-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="08b46-110">Длинный идентификатор (крышка):</span><span class="sxs-lookup"><span data-stu-id="08b46-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="08b46-111">0x00008041</span><span class="sxs-lookup"><span data-stu-id="08b46-111">0x00008041</span></span>  <br/> |
|<span data-ttu-id="08b46-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="08b46-112">Data type:</span></span>  <br/> |<span data-ttu-id="08b46-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="08b46-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="08b46-114">Область:</span><span class="sxs-lookup"><span data-stu-id="08b46-114">Area:</span></span>  <br/> |<span data-ttu-id="08b46-115">Контакт</span><span class="sxs-lookup"><span data-stu-id="08b46-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="08b46-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="08b46-116">Remarks</span></span>

<span data-ttu-id="08b46-117">Значение этого свойства должно быть либо PNG-, либо JPEG-потоком.</span><span class="sxs-lookup"><span data-stu-id="08b46-117">The value of this property must be either a portable network graphics (PNG) or JPEG stream.</span></span> <span data-ttu-id="08b46-118">Это свойство следует использовать вместе со свойством **диспидбкдисплайдефинитион** ([PidLidBusinessCardDisplayDefinition](pidlidbusinesscarddisplaydefinition-canonical-property.md)) следующим образом: **диспидбккардпиктуре** не должно присутствовать в контакте, если \*\* Диспидбкдисплайдефинитион\*\* отсутствует.</span><span class="sxs-lookup"><span data-stu-id="08b46-118">This property should be used in conjunction with the **dispidBCDisplayDefinition** ([PidLidBusinessCardDisplayDefinition](pidlidbusinesscarddisplaydefinition-canonical-property.md)) property as follows: **dispidBCCardPicture** should not be present on a contact if **dispidBCDisplayDefinition** is not present.</span></span> <span data-ttu-id="08b46-119">Это свойство также должно отсутствовать, если для данных в **диспидбккардпиктуре** не требуется изображение карты.</span><span class="sxs-lookup"><span data-stu-id="08b46-119">This property also should not be present if the data in **dispidBCCardPicture** does not require a card image.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="08b46-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="08b46-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="08b46-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="08b46-121">Protocol specifications</span></span>

<span data-ttu-id="08b46-122">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="08b46-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="08b46-123">Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="08b46-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="08b46-124">[[MS — ОКСОКНТК]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="08b46-124">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="08b46-125">Задает свойства и операции, допустимые для контактов и личных списков рассылки.</span><span class="sxs-lookup"><span data-stu-id="08b46-125">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="08b46-126">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="08b46-126">Header files</span></span>

<span data-ttu-id="08b46-127">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="08b46-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="08b46-128">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="08b46-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="08b46-129">См. также</span><span class="sxs-lookup"><span data-stu-id="08b46-129">See also</span></span>



[<span data-ttu-id="08b46-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="08b46-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="08b46-131">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="08b46-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="08b46-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="08b46-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="08b46-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="08b46-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

