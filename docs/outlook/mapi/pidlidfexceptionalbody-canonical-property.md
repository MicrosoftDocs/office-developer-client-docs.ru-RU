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
ms.openlocfilehash: a2adbee409649f0268d96502a7dd3f658433052a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810346"
---
# <a name="pidlidfexceptionalbody-canonical-property"></a><span data-ttu-id="0b221-103">Каноническое свойство PidLidFExceptionalBody</span><span class="sxs-lookup"><span data-stu-id="0b221-103">PidLidFExceptionalBody Canonical Property</span></span>

  
  
<span data-ttu-id="0b221-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0b221-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0b221-105">Указывает, что исключение внедренное сообщение, что для объекта body, которые отличаются от повторяющихся объект календаря.</span><span class="sxs-lookup"><span data-stu-id="0b221-105">Indicates that the exception embedded message object has a body that differs from the recurring calendar object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0b221-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="0b221-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0b221-107">dispidFExceptionalBody</span><span class="sxs-lookup"><span data-stu-id="0b221-107">dispidFExceptionalBody</span></span>  <br/> |
|<span data-ttu-id="0b221-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="0b221-108">Property set:</span></span>  <br/> |<span data-ttu-id="0b221-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="0b221-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="0b221-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="0b221-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="0b221-111">0x00008206</span><span class="sxs-lookup"><span data-stu-id="0b221-111">0x00008206</span></span>  <br/> |
|<span data-ttu-id="0b221-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="0b221-112">Data type:</span></span>  <br/> |<span data-ttu-id="0b221-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="0b221-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="0b221-114">Область:</span><span class="sxs-lookup"><span data-stu-id="0b221-114">Area:</span></span>  <br/> |<span data-ttu-id="0b221-115">Meetings (собрания);</span><span class="sxs-lookup"><span data-stu-id="0b221-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0b221-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="0b221-116">Remarks</span></span>

<span data-ttu-id="0b221-117">Если значение этого свойства имеет значение TRUE, исключение внедренный объект должен иметь тело сообщения.</span><span class="sxs-lookup"><span data-stu-id="0b221-117">If the value of this property is TRUE, then the exception embedded message object must have a body.</span></span> <span data-ttu-id="0b221-118">Если значение этого свойства имеет значение FALSE, если свойство не существует, затем клиента или сервера необходимо получить текст из повторяющихся объекта календаря.</span><span class="sxs-lookup"><span data-stu-id="0b221-118">If the value of this property is FALSE, or if the property does not exist, then a client or server must obtain the body from the recurring calendar object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0b221-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="0b221-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0b221-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="0b221-120">Protocol specifications</span></span>

<span data-ttu-id="0b221-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0b221-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0b221-122">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="0b221-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0b221-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0b221-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0b221-124">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="0b221-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0b221-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="0b221-125">Header files</span></span>

<span data-ttu-id="0b221-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0b221-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="0b221-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="0b221-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0b221-128">См. также</span><span class="sxs-lookup"><span data-stu-id="0b221-128">See also</span></span>



[<span data-ttu-id="0b221-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0b221-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0b221-130">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0b221-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0b221-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="0b221-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0b221-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="0b221-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

