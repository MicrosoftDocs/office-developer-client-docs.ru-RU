---
title: Каноническое свойство PidLidAttendeeCriticalChange
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAttendeeCriticalChange
api_type:
- COM
ms.assetid: 2b46966d-c63d-4241-92d4-001d6a674e97
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d6464a346d8543a128ec1af9f605667c6a51ca3c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342044"
---
# <a name="pidlidattendeecriticalchange-canonical-property"></a><span data-ttu-id="88119-103">Каноническое свойство PidLidAttendeeCriticalChange</span><span class="sxs-lookup"><span data-stu-id="88119-103">PidLidAttendeeCriticalChange Canonical Property</span></span>

  
  
<span data-ttu-id="88119-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="88119-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="88119-105">Указывает дату и время, когда был отправлен объект, связанный с собранием.</span><span class="sxs-lookup"><span data-stu-id="88119-105">Specifies the date and time when the meeting-related object was sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="88119-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="88119-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="88119-107">LID_ATTENDEE_CRITICAL_CHANGE</span><span class="sxs-lookup"><span data-stu-id="88119-107">LID_ATTENDEE_CRITICAL_CHANGE</span></span>  <br/> |
|<span data-ttu-id="88119-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="88119-108">Property set:</span></span>  <br/> |<span data-ttu-id="88119-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="88119-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="88119-110">Длинный ИД (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="88119-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="88119-111">0x00000001</span><span class="sxs-lookup"><span data-stu-id="88119-111">0x00000001</span></span>  <br/> |
|<span data-ttu-id="88119-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="88119-112">Data type:</span></span>  <br/> |<span data-ttu-id="88119-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="88119-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="88119-114">Область:</span><span class="sxs-lookup"><span data-stu-id="88119-114">Area:</span></span>  <br/> |<span data-ttu-id="88119-115">Собрания</span><span class="sxs-lookup"><span data-stu-id="88119-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="88119-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="88119-116">Remarks</span></span>

<span data-ttu-id="88119-117">Значение должно быть указано в UTC.</span><span class="sxs-lookup"><span data-stu-id="88119-117">The value must be specified in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="88119-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="88119-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="88119-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="88119-119">Protocol specifications</span></span>

<span data-ttu-id="88119-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="88119-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="88119-121">Предоставляет определения набора свойств и ссылки на связанные Exchange Server спецификации протокола.</span><span class="sxs-lookup"><span data-stu-id="88119-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="88119-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="88119-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="88119-123">Указывает свойства и операции для встреч, запросов на собрание и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="88119-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="88119-124">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="88119-124">Header files</span></span>

<span data-ttu-id="88119-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="88119-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="88119-126">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="88119-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="88119-127">См. также</span><span class="sxs-lookup"><span data-stu-id="88119-127">See also</span></span>



[<span data-ttu-id="88119-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="88119-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="88119-129">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="88119-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="88119-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="88119-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="88119-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="88119-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

