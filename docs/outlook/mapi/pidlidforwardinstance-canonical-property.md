---
title: Каноническое свойство PidLidForwardInstance
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidForwardInstance
api_type:
- COM
ms.assetid: 055bdcaf-5002-44a6-b2b6-87244b2bea93
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 585e1a5400965288aa4a4c321888a570270021c8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357773"
---
# <a name="pidlidforwardinstance-canonical-property"></a><span data-ttu-id="71944-103">Каноническое свойство PidLidForwardInstance</span><span class="sxs-lookup"><span data-stu-id="71944-103">PidLidForwardInstance Canonical Property</span></span>

  
  
<span data-ttu-id="71944-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="71944-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="71944-105">Указывает на то, что приглашение на собрание представляет исключение из повторяющегося ряда и Переадресовано (даже при переадресации организатором), а не приглашение, отправленное организатором.</span><span class="sxs-lookup"><span data-stu-id="71944-105">Indicates that the meeting request represents an exception to a recurring series, and it was forwarded (even when forwarded by the organizer) rather than being an invitation sent by the organizer.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="71944-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="71944-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="71944-107">Диспидфврдинстанце</span><span class="sxs-lookup"><span data-stu-id="71944-107">dispidFwrdInstance</span></span>  <br/> |
|<span data-ttu-id="71944-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="71944-108">Property set:</span></span>  <br/> |<span data-ttu-id="71944-109">Псетид_аппоинтмент</span><span class="sxs-lookup"><span data-stu-id="71944-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="71944-110">Длинный идентификатор (крышка):</span><span class="sxs-lookup"><span data-stu-id="71944-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="71944-111">0x0000820A</span><span class="sxs-lookup"><span data-stu-id="71944-111">0x0000820A</span></span>  <br/> |
|<span data-ttu-id="71944-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="71944-112">Data type:</span></span>  <br/> |<span data-ttu-id="71944-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="71944-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="71944-114">Область:</span><span class="sxs-lookup"><span data-stu-id="71944-114">Area:</span></span>  <br/> |<span data-ttu-id="71944-115">Meetings</span><span class="sxs-lookup"><span data-stu-id="71944-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="71944-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="71944-116">Remarks</span></span>

<span data-ttu-id="71944-117">Значение FALSE для этого свойства указывает на то, что приглашение на собрание не является переадресованным экземпляром.</span><span class="sxs-lookup"><span data-stu-id="71944-117">A value of FALSE for this property indicates that the meeting request is not a forwarded instance.</span></span> <span data-ttu-id="71944-118">Это свойство не является обязательным.</span><span class="sxs-lookup"><span data-stu-id="71944-118">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="71944-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="71944-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="71944-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="71944-120">Protocol specifications</span></span>

<span data-ttu-id="71944-121">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="71944-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="71944-122">Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="71944-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="71944-123">[[MS — ОКСОКАЛ]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="71944-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="71944-124">Задает свойства и операции для встречи, приглашения на собрание и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="71944-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="71944-125">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="71944-125">Header files</span></span>

<span data-ttu-id="71944-126">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="71944-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="71944-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="71944-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="71944-128">См. также</span><span class="sxs-lookup"><span data-stu-id="71944-128">See also</span></span>



[<span data-ttu-id="71944-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="71944-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="71944-130">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="71944-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="71944-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="71944-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="71944-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="71944-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

