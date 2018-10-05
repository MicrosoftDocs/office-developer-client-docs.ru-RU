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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399104"
---
# <a name="pidlidbusinesscarddisplaydefinition-canonical-property"></a><span data-ttu-id="76769-103">Каноническое свойство PidLidBusinessCardDisplayDefinition</span><span class="sxs-lookup"><span data-stu-id="76769-103">PidLidBusinessCardDisplayDefinition Canonical Property</span></span>

  
  
<span data-ttu-id="76769-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="76769-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="76769-105">Содержит сведения о пользовательские настройки для отображения в виде визитной карточки контакта.</span><span class="sxs-lookup"><span data-stu-id="76769-105">Contains user-customization details for displaying a contact as a business card.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="76769-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="76769-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="76769-107">dispidBCDisplayDefinition</span><span class="sxs-lookup"><span data-stu-id="76769-107">dispidBCDisplayDefinition</span></span>  <br/> |
|<span data-ttu-id="76769-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="76769-108">Property set:</span></span>  <br/> |<span data-ttu-id="76769-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="76769-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="76769-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="76769-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="76769-111">0x00008040</span><span class="sxs-lookup"><span data-stu-id="76769-111">0x00008040</span></span>  <br/> |
|<span data-ttu-id="76769-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="76769-112">Data type:</span></span>  <br/> |<span data-ttu-id="76769-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="76769-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="76769-114">Область:</span><span class="sxs-lookup"><span data-stu-id="76769-114">Area:</span></span>  <br/> |<span data-ttu-id="76769-115">Contact</span><span class="sxs-lookup"><span data-stu-id="76769-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="76769-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="76769-116">Remarks</span></span>

<span data-ttu-id="76769-117">Макет визитной карточки может быть представлена как изображения и количество полей текст.</span><span class="sxs-lookup"><span data-stu-id="76769-117">The layout of a business card can be represented as an image and a number of text fields.</span></span> <span data-ttu-id="76769-118">Изображение может быть фотографий контактов или изображение карточки.</span><span class="sxs-lookup"><span data-stu-id="76769-118">The image can be either a contact photo, or a card picture.</span></span> <span data-ttu-id="76769-119">Текстовые поля состоят из значения из другого свойства на контакт и строку необязательные настраиваемые метки, заданное пользователем.</span><span class="sxs-lookup"><span data-stu-id="76769-119">Text fields consist of a value from another property set on the contact and an optional customized label string provided by the user.</span></span> <span data-ttu-id="76769-120">Обратите внимание, что значения несколькими byte хранятся в формате с прямым в буфере.</span><span class="sxs-lookup"><span data-stu-id="76769-120">Note that multi-byte values are stored in little-endian format in the buffer.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="76769-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="76769-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="76769-122">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="76769-122">Protocol specifications</span></span>

<span data-ttu-id="76769-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="76769-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="76769-124">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="76769-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="76769-125">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="76769-125">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="76769-126">Задает свойства и операции, допустимые для контакты и списки рассылки.</span><span class="sxs-lookup"><span data-stu-id="76769-126">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="76769-127">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="76769-127">Header files</span></span>

<span data-ttu-id="76769-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="76769-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="76769-129">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="76769-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="76769-130">См. также</span><span class="sxs-lookup"><span data-stu-id="76769-130">See also</span></span>



[<span data-ttu-id="76769-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="76769-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="76769-132">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="76769-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="76769-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="76769-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="76769-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="76769-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

