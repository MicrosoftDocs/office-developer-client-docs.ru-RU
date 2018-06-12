---
title: Каноническое свойство PidLidAppointmentMessageClass
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentMessageClass
api_type:
- COM
ms.assetid: 8b8c8484-0cb4-4842-8b11-de42d97e0140
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: 8777b2119e6beefc4d69dc0babfc8672df3a468b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810107"
---
# <a name="pidlidappointmentmessageclass-canonical-property"></a><span data-ttu-id="4718c-103">Каноническое свойство PidLidAppointmentMessageClass</span><span class="sxs-lookup"><span data-stu-id="4718c-103">PidLidAppointmentMessageClass Canonical Property</span></span>

  
  
<span data-ttu-id="4718c-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4718c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4718c-105">Указывает свойство **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) собрания, который будет создан из приглашения на собрание.</span><span class="sxs-lookup"><span data-stu-id="4718c-105">Indicates the **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property of the meeting that is to be generated from the meeting request.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4718c-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="4718c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4718c-107">dispidApptMessageClass</span><span class="sxs-lookup"><span data-stu-id="4718c-107">dispidApptMessageClass</span></span>  <br/> |
|<span data-ttu-id="4718c-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="4718c-108">Property set:</span></span>  <br/> |<span data-ttu-id="4718c-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="4718c-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="4718c-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="4718c-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="4718c-111">0x00000024</span><span class="sxs-lookup"><span data-stu-id="4718c-111">0x00000024</span></span>  <br/> |
|<span data-ttu-id="4718c-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="4718c-112">Data type:</span></span>  <br/> |<span data-ttu-id="4718c-113">PT_TSTRING</span><span class="sxs-lookup"><span data-stu-id="4718c-113">PT_TSTRING</span></span>  <br/> |
|<span data-ttu-id="4718c-114">Области:</span><span class="sxs-lookup"><span data-stu-id="4718c-114">Area:</span></span>  <br/> |<span data-ttu-id="4718c-115">Meetings (собрания);</span><span class="sxs-lookup"><span data-stu-id="4718c-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4718c-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="4718c-116">Remarks</span></span>

<span data-ttu-id="4718c-117">Значение этого свойства должны быть «IPM. Встреча» или иметь префикс «IPM. Встречи.».</span><span class="sxs-lookup"><span data-stu-id="4718c-117">The value of this property must either be "IPM.Appointment" or be prefixed with "IPM.Appointment.".</span></span> <span data-ttu-id="4718c-118">Это свойство не требуется.</span><span class="sxs-lookup"><span data-stu-id="4718c-118">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4718c-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="4718c-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4718c-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="4718c-120">Protocol specifications</span></span>

<span data-ttu-id="4718c-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4718c-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4718c-122">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="4718c-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4718c-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4718c-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4718c-124">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="4718c-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4718c-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="4718c-125">Header files</span></span>

<span data-ttu-id="4718c-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4718c-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="4718c-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="4718c-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4718c-128">См. также</span><span class="sxs-lookup"><span data-stu-id="4718c-128">See also</span></span>



[<span data-ttu-id="4718c-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="4718c-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4718c-130">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="4718c-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4718c-131">Каноническое свойство имена сопоставляемых именам MAPI</span><span class="sxs-lookup"><span data-stu-id="4718c-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4718c-132">Сопоставление имен MAPI имена каноническое свойств</span><span class="sxs-lookup"><span data-stu-id="4718c-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

