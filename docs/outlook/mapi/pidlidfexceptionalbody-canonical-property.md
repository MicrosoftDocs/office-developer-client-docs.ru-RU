---
title: Каноническое свойство PidLidFExceptionalBody
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFExceptionalBody
api_type:
- COM
ms.assetid: 327516e8-ed3f-40fc-9604-03a70aecef5a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 93eb98aee19ea3f46a4e01e2c80150c3efe893a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327463"
---
# <a name="pidlidfexceptionalbody-canonical-property"></a><span data-ttu-id="b54b4-103">Каноническое свойство PidLidFExceptionalBody</span><span class="sxs-lookup"><span data-stu-id="b54b4-103">PidLidFExceptionalBody Canonical Property</span></span>

  
  
<span data-ttu-id="b54b4-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b54b4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b54b4-105">Указывает, что объект встроенного сообщения исключения имеет тело, отличащееся от повторяющегося объекта календаря.</span><span class="sxs-lookup"><span data-stu-id="b54b4-105">Indicates that the exception embedded message object has a body that differs from the recurring calendar object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b54b4-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="b54b4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b54b4-107">dispidFExceptionalBody</span><span class="sxs-lookup"><span data-stu-id="b54b4-107">dispidFExceptionalBody</span></span>  <br/> |
|<span data-ttu-id="b54b4-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="b54b4-108">Property set:</span></span>  <br/> |<span data-ttu-id="b54b4-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="b54b4-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="b54b4-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="b54b4-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="b54b4-111">0x00008206</span><span class="sxs-lookup"><span data-stu-id="b54b4-111">0x00008206</span></span>  <br/> |
|<span data-ttu-id="b54b4-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="b54b4-112">Data type:</span></span>  <br/> |<span data-ttu-id="b54b4-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="b54b4-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="b54b4-114">Область:</span><span class="sxs-lookup"><span data-stu-id="b54b4-114">Area:</span></span>  <br/> |<span data-ttu-id="b54b4-115">Собрания</span><span class="sxs-lookup"><span data-stu-id="b54b4-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b54b4-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="b54b4-116">Remarks</span></span>

<span data-ttu-id="b54b4-117">Если значение этого свойства true, то объект встроенного сообщения исключения должен иметь тело.</span><span class="sxs-lookup"><span data-stu-id="b54b4-117">If the value of this property is TRUE, then the exception embedded message object must have a body.</span></span> <span data-ttu-id="b54b4-118">Если значение этого свойства false или если свойство не существует, клиент или сервер должны получить тело из повторяющегося объекта календаря.</span><span class="sxs-lookup"><span data-stu-id="b54b4-118">If the value of this property is FALSE, or if the property does not exist, then a client or server must obtain the body from the recurring calendar object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b54b4-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b54b4-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b54b4-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="b54b4-120">Protocol specifications</span></span>

<span data-ttu-id="b54b4-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b54b4-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b54b4-122">Предоставляет определения набора свойств и ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="b54b4-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b54b4-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b54b4-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b54b4-124">Указывает свойства и операции для встреч, запросов на собрания и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="b54b4-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b54b4-125">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="b54b4-125">Header files</span></span>

<span data-ttu-id="b54b4-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b54b4-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="b54b4-127">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="b54b4-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b54b4-128">См. также</span><span class="sxs-lookup"><span data-stu-id="b54b4-128">See also</span></span>



[<span data-ttu-id="b54b4-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b54b4-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b54b4-130">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b54b4-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b54b4-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="b54b4-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b54b4-132">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="b54b4-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

