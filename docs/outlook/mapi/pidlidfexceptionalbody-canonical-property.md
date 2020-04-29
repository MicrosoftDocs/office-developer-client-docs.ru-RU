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
# <a name="pidlidfexceptionalbody-canonical-property"></a><span data-ttu-id="e851d-103">Каноническое свойство PidLidFExceptionalBody</span><span class="sxs-lookup"><span data-stu-id="e851d-103">PidLidFExceptionalBody Canonical Property</span></span>

  
  
<span data-ttu-id="e851d-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e851d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e851d-105">Указывает на то, что встроенный объект Message исключения имеет текст, отличающийся от объекта повторяющегося календаря.</span><span class="sxs-lookup"><span data-stu-id="e851d-105">Indicates that the exception embedded message object has a body that differs from the recurring calendar object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e851d-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="e851d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e851d-107">диспидфексцептионалбоди</span><span class="sxs-lookup"><span data-stu-id="e851d-107">dispidFExceptionalBody</span></span>  <br/> |
|<span data-ttu-id="e851d-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="e851d-108">Property set:</span></span>  <br/> |<span data-ttu-id="e851d-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="e851d-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="e851d-110">Длинный идентификатор (крышка):</span><span class="sxs-lookup"><span data-stu-id="e851d-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="e851d-111">0x00008206</span><span class="sxs-lookup"><span data-stu-id="e851d-111">0x00008206</span></span>  <br/> |
|<span data-ttu-id="e851d-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="e851d-112">Data type:</span></span>  <br/> |<span data-ttu-id="e851d-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="e851d-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="e851d-114">Область:</span><span class="sxs-lookup"><span data-stu-id="e851d-114">Area:</span></span>  <br/> |<span data-ttu-id="e851d-115">Собрания</span><span class="sxs-lookup"><span data-stu-id="e851d-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e851d-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="e851d-116">Remarks</span></span>

<span data-ttu-id="e851d-117">Если значение этого свойства равно TRUE, то внедренный объект Message исключения должен иметь текст Body.</span><span class="sxs-lookup"><span data-stu-id="e851d-117">If the value of this property is TRUE, then the exception embedded message object must have a body.</span></span> <span data-ttu-id="e851d-118">Если значение этого свойства равно FALSE или если свойство не существует, то клиент или сервер должен получить текст из повторяющегося объекта Calendar.</span><span class="sxs-lookup"><span data-stu-id="e851d-118">If the value of this property is FALSE, or if the property does not exist, then a client or server must obtain the body from the recurring calendar object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e851d-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="e851d-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e851d-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="e851d-120">Protocol specifications</span></span>

<span data-ttu-id="e851d-121">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e851d-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e851d-122">Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="e851d-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e851d-123">[[MS — ОКСОКАЛ]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e851d-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e851d-124">Задает свойства и операции для встречи, приглашения на собрание и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="e851d-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e851d-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="e851d-125">Header files</span></span>

<span data-ttu-id="e851d-126">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="e851d-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="e851d-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="e851d-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e851d-128">См. также</span><span class="sxs-lookup"><span data-stu-id="e851d-128">See also</span></span>



[<span data-ttu-id="e851d-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="e851d-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e851d-130">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="e851d-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e851d-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="e851d-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e851d-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="e851d-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

