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
ms.openlocfilehash: 7653d7a56302deaad75443746ff7e83834af260f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571362"
---
# <a name="pidlidfexceptionalbody-canonical-property"></a><span data-ttu-id="2c48c-103">Каноническое свойство PidLidFExceptionalBody</span><span class="sxs-lookup"><span data-stu-id="2c48c-103">PidLidFExceptionalBody Canonical Property</span></span>

  
  
<span data-ttu-id="2c48c-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2c48c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2c48c-105">Указывает, что исключение внедренное сообщение, что для объекта body, которые отличаются от повторяющихся объект календаря.</span><span class="sxs-lookup"><span data-stu-id="2c48c-105">Indicates that the exception embedded message object has a body that differs from the recurring calendar object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2c48c-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="2c48c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2c48c-107">dispidFExceptionalBody</span><span class="sxs-lookup"><span data-stu-id="2c48c-107">dispidFExceptionalBody</span></span>  <br/> |
|<span data-ttu-id="2c48c-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="2c48c-108">Property set:</span></span>  <br/> |<span data-ttu-id="2c48c-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="2c48c-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="2c48c-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="2c48c-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="2c48c-111">0x00008206</span><span class="sxs-lookup"><span data-stu-id="2c48c-111">0x00008206</span></span>  <br/> |
|<span data-ttu-id="2c48c-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="2c48c-112">Data type:</span></span>  <br/> |<span data-ttu-id="2c48c-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="2c48c-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="2c48c-114">Область:</span><span class="sxs-lookup"><span data-stu-id="2c48c-114">Area:</span></span>  <br/> |<span data-ttu-id="2c48c-115">Meetings (собрания);</span><span class="sxs-lookup"><span data-stu-id="2c48c-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2c48c-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="2c48c-116">Remarks</span></span>

<span data-ttu-id="2c48c-117">Если значение этого свойства имеет значение TRUE, исключение внедренный объект должен иметь тело сообщения.</span><span class="sxs-lookup"><span data-stu-id="2c48c-117">If the value of this property is TRUE, then the exception embedded message object must have a body.</span></span> <span data-ttu-id="2c48c-118">Если значение этого свойства имеет значение FALSE, если свойство не существует, затем клиента или сервера необходимо получить текст из повторяющихся объекта календаря.</span><span class="sxs-lookup"><span data-stu-id="2c48c-118">If the value of this property is FALSE, or if the property does not exist, then a client or server must obtain the body from the recurring calendar object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2c48c-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="2c48c-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2c48c-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="2c48c-120">Protocol specifications</span></span>

<span data-ttu-id="2c48c-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2c48c-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2c48c-122">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="2c48c-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2c48c-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2c48c-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2c48c-124">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="2c48c-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2c48c-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="2c48c-125">Header files</span></span>

<span data-ttu-id="2c48c-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2c48c-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="2c48c-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="2c48c-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2c48c-128">См. также</span><span class="sxs-lookup"><span data-stu-id="2c48c-128">See also</span></span>



[<span data-ttu-id="2c48c-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="2c48c-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2c48c-130">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="2c48c-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2c48c-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="2c48c-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2c48c-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="2c48c-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

