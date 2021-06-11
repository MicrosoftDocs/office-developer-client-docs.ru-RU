---
title: Каноническое свойство PidLidBusinessCardDisplayDefinition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidBusinessCardDisplayDefinition
api_type:
- COM
ms.assetid: c0b956dd-7139-49e3-a32a-d70bfb11e0b1
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f25f8a538ff61bc7e04c234efd7404b1c866d64d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342037"
---
# <a name="pidlidbusinesscarddisplaydefinition-canonical-property"></a><span data-ttu-id="6362f-103">Каноническое свойство PidLidBusinessCardDisplayDefinition</span><span class="sxs-lookup"><span data-stu-id="6362f-103">PidLidBusinessCardDisplayDefinition Canonical Property</span></span>

  
  
<span data-ttu-id="6362f-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6362f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6362f-105">Содержит сведения о настройке пользователя для отображения контакта в качестве визитной карточки.</span><span class="sxs-lookup"><span data-stu-id="6362f-105">Contains user-customization details for displaying a contact as a business card.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6362f-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="6362f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6362f-107">dispidBCDisplayDefinition</span><span class="sxs-lookup"><span data-stu-id="6362f-107">dispidBCDisplayDefinition</span></span>  <br/> |
|<span data-ttu-id="6362f-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="6362f-108">Property set:</span></span>  <br/> |<span data-ttu-id="6362f-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="6362f-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="6362f-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="6362f-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="6362f-111">0x00008040</span><span class="sxs-lookup"><span data-stu-id="6362f-111">0x00008040</span></span>  <br/> |
|<span data-ttu-id="6362f-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="6362f-112">Data type:</span></span>  <br/> |<span data-ttu-id="6362f-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="6362f-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="6362f-114">Область:</span><span class="sxs-lookup"><span data-stu-id="6362f-114">Area:</span></span>  <br/> |<span data-ttu-id="6362f-115">Contact</span><span class="sxs-lookup"><span data-stu-id="6362f-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6362f-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="6362f-116">Remarks</span></span>

<span data-ttu-id="6362f-117">Макет визитной карточки может быть представлен в виде изображения и ряда текстовых полей.</span><span class="sxs-lookup"><span data-stu-id="6362f-117">The layout of a business card can be represented as an image and a number of text fields.</span></span> <span data-ttu-id="6362f-118">Изображение может быть либо контактной фотографией, либо картой.</span><span class="sxs-lookup"><span data-stu-id="6362f-118">The image can be either a contact photo, or a card picture.</span></span> <span data-ttu-id="6362f-119">Текстовые поля состоят из значения из другого свойства, установленного на контакте, и необязательной настраиваемой строки метки, предоставляемой пользователем.</span><span class="sxs-lookup"><span data-stu-id="6362f-119">Text fields consist of a value from another property set on the contact and an optional customized label string provided by the user.</span></span> <span data-ttu-id="6362f-120">Обратите внимание, что многобетные значения хранятся в малоконфессийном формате в буфере.</span><span class="sxs-lookup"><span data-stu-id="6362f-120">Note that multi-byte values are stored in little-endian format in the buffer.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6362f-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="6362f-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6362f-122">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="6362f-122">Protocol specifications</span></span>

<span data-ttu-id="6362f-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6362f-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6362f-124">Предоставляет определения набора свойств и ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="6362f-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6362f-125">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6362f-125">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6362f-126">Указывает свойства и операции, допустимые для контактов и личных списков рассылки.</span><span class="sxs-lookup"><span data-stu-id="6362f-126">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6362f-127">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="6362f-127">Header files</span></span>

<span data-ttu-id="6362f-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6362f-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="6362f-129">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="6362f-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6362f-130">См. также</span><span class="sxs-lookup"><span data-stu-id="6362f-130">See also</span></span>



[<span data-ttu-id="6362f-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6362f-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6362f-132">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6362f-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6362f-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="6362f-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6362f-134">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="6362f-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

