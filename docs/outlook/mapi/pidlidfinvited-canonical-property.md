---
title: Каноническое свойство PidLidFInvited
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFInvited
api_type:
- COM
ms.assetid: ca1ea5ec-20d5-4b70-95de-c2246a10beae
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: efedeb54decf1feae7b31f8af299a154606d7afc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582905"
---
# <a name="pidlidfinvited-canonical-property"></a><span data-ttu-id="28ead-103">Каноническое свойство PidLidFInvited</span><span class="sxs-lookup"><span data-stu-id="28ead-103">PidLidFInvited Canonical Property</span></span>

  
  
<span data-ttu-id="28ead-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="28ead-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="28ead-105">Указывает ли отправки приглашения на собрания, представляющий этого собрания.</span><span class="sxs-lookup"><span data-stu-id="28ead-105">Indicates whether or not invitations have been sent for the meeting that this meeting represents.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="28ead-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="28ead-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="28ead-107">dispidFInvited</span><span class="sxs-lookup"><span data-stu-id="28ead-107">dispidFInvited</span></span>  <br/> |
|<span data-ttu-id="28ead-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="28ead-108">Property set:</span></span>  <br/> |<span data-ttu-id="28ead-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="28ead-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="28ead-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="28ead-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="28ead-111">0x00008229</span><span class="sxs-lookup"><span data-stu-id="28ead-111">0x00008229</span></span>  <br/> |
|<span data-ttu-id="28ead-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="28ead-112">Data type:</span></span>  <br/> |<span data-ttu-id="28ead-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="28ead-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="28ead-114">Область:</span><span class="sxs-lookup"><span data-stu-id="28ead-114">Area:</span></span>  <br/> |<span data-ttu-id="28ead-115">Meetings (собрания);</span><span class="sxs-lookup"><span data-stu-id="28ead-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="28ead-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="28ead-116">Remarks</span></span>

<span data-ttu-id="28ead-117">Значение FALSE или отсутствие этого свойства указывает, что приглашения на собрание никогда не отправляются.</span><span class="sxs-lookup"><span data-stu-id="28ead-117">A value of FALSE, or the absence of this property, indicates that a meeting request has never been sent.</span></span> <span data-ttu-id="28ead-118">Значение TRUE указывает отправку приглашения на собрание.</span><span class="sxs-lookup"><span data-stu-id="28ead-118">A value of TRUE indicates that a meeting request has been sent.</span></span> <span data-ttu-id="28ead-119">Если это значение задано значение TRUE на собрание, его нельзя изменять.</span><span class="sxs-lookup"><span data-stu-id="28ead-119">Once this value is set to TRUE on a meeting, it must not be changed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="28ead-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="28ead-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="28ead-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="28ead-121">Protocol specifications</span></span>

<span data-ttu-id="28ead-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="28ead-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="28ead-123">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="28ead-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="28ead-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="28ead-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="28ead-125">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="28ead-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="28ead-126">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="28ead-126">Header files</span></span>

<span data-ttu-id="28ead-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="28ead-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="28ead-128">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="28ead-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="28ead-129">См. также</span><span class="sxs-lookup"><span data-stu-id="28ead-129">See also</span></span>



[<span data-ttu-id="28ead-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="28ead-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="28ead-131">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="28ead-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="28ead-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="28ead-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="28ead-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="28ead-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

