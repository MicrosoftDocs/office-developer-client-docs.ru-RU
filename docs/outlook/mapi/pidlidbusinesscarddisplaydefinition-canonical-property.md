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
ms.openlocfilehash: df9b880739215a681986670926b843fec6cc3969
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584193"
---
# <a name="pidlidbusinesscarddisplaydefinition-canonical-property"></a><span data-ttu-id="fd026-103">Каноническое свойство PidLidBusinessCardDisplayDefinition</span><span class="sxs-lookup"><span data-stu-id="fd026-103">PidLidBusinessCardDisplayDefinition Canonical Property</span></span>

  
  
<span data-ttu-id="fd026-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fd026-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fd026-105">Содержит сведения о пользовательские настройки для отображения в виде визитной карточки контакта.</span><span class="sxs-lookup"><span data-stu-id="fd026-105">Contains user-customization details for displaying a contact as a business card.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fd026-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="fd026-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fd026-107">dispidBCDisplayDefinition</span><span class="sxs-lookup"><span data-stu-id="fd026-107">dispidBCDisplayDefinition</span></span>  <br/> |
|<span data-ttu-id="fd026-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="fd026-108">Property set:</span></span>  <br/> |<span data-ttu-id="fd026-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="fd026-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="fd026-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="fd026-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="fd026-111">0x00008040</span><span class="sxs-lookup"><span data-stu-id="fd026-111">0x00008040</span></span>  <br/> |
|<span data-ttu-id="fd026-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="fd026-112">Data type:</span></span>  <br/> |<span data-ttu-id="fd026-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="fd026-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="fd026-114">Область:</span><span class="sxs-lookup"><span data-stu-id="fd026-114">Area:</span></span>  <br/> |<span data-ttu-id="fd026-115">Contact</span><span class="sxs-lookup"><span data-stu-id="fd026-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fd026-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="fd026-116">Remarks</span></span>

<span data-ttu-id="fd026-117">Макет визитной карточки может быть представлена как изображения и количество полей текст.</span><span class="sxs-lookup"><span data-stu-id="fd026-117">The layout of a business card can be represented as an image and a number of text fields.</span></span> <span data-ttu-id="fd026-118">Изображение может быть фотографий контактов или изображение карточки.</span><span class="sxs-lookup"><span data-stu-id="fd026-118">The image can be either a contact photo, or a card picture.</span></span> <span data-ttu-id="fd026-119">Текстовые поля состоят из значения из другого свойства на контакт и строку необязательные настраиваемые метки, заданное пользователем.</span><span class="sxs-lookup"><span data-stu-id="fd026-119">Text fields consist of a value from another property set on the contact and an optional customized label string provided by the user.</span></span> <span data-ttu-id="fd026-120">Обратите внимание, что значения несколькими byte хранятся в формате с прямым в буфере.</span><span class="sxs-lookup"><span data-stu-id="fd026-120">Note that multi-byte values are stored in little-endian format in the buffer.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="fd026-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="fd026-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fd026-122">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="fd026-122">Protocol specifications</span></span>

<span data-ttu-id="fd026-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fd026-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fd026-124">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="fd026-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fd026-125">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fd026-125">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fd026-126">Задает свойства и операции, допустимые для контакты и списки рассылки.</span><span class="sxs-lookup"><span data-stu-id="fd026-126">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fd026-127">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="fd026-127">Header files</span></span>

<span data-ttu-id="fd026-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fd026-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="fd026-129">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="fd026-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fd026-130">См. также</span><span class="sxs-lookup"><span data-stu-id="fd026-130">See also</span></span>



[<span data-ttu-id="fd026-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="fd026-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fd026-132">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="fd026-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fd026-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="fd026-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fd026-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="fd026-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

