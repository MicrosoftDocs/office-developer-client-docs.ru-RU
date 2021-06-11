---
title: Каноническое свойство PidTagCreationTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagCreationTime
api_type:
- HeaderDef
ms.assetid: 13122af2-06c8-4342-983d-e38178743d8f
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: de853c66f0ef4270f4c443881bfa163d4abfa3e0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357899"
---
# <a name="pidtagcreationtime-canonical-property"></a><span data-ttu-id="15109-103">Каноническое свойство PidTagCreationTime</span><span class="sxs-lookup"><span data-stu-id="15109-103">PidTagCreationTime Canonical Property</span></span>

  
  
<span data-ttu-id="15109-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="15109-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="15109-105">Содержит дату создания и время сообщения.</span><span class="sxs-lookup"><span data-stu-id="15109-105">Contains the creation date and time of a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="15109-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="15109-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="15109-107">PR_CREATION_TIME</span><span class="sxs-lookup"><span data-stu-id="15109-107">PR_CREATION_TIME</span></span>  <br/> |
|<span data-ttu-id="15109-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="15109-108">Identifier:</span></span>  <br/> |<span data-ttu-id="15109-109">0x3007</span><span class="sxs-lookup"><span data-stu-id="15109-109">0x3007</span></span>  <br/> |
|<span data-ttu-id="15109-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="15109-110">Data type:</span></span>  <br/> |<span data-ttu-id="15109-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="15109-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="15109-112">Область:</span><span class="sxs-lookup"><span data-stu-id="15109-112">Area:</span></span>  <br/> |<span data-ttu-id="15109-113">Время сообщения</span><span class="sxs-lookup"><span data-stu-id="15109-113">Message time</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="15109-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="15109-114">Remarks</span></span>

<span data-ttu-id="15109-115">Хранилище сообщений задает это свойство для каждого сообщения, которое оно создает.</span><span class="sxs-lookup"><span data-stu-id="15109-115">A message store sets this property for each message that it creates.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="15109-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="15109-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="15109-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="15109-117">Protocol specifications</span></span>

<span data-ttu-id="15109-118">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="15109-118">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="15109-119">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="15109-119">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="15109-120">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="15109-120">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="15109-121">Указывает свойства и операции для списков пользователей, контактов, групп и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="15109-121">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="15109-122">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="15109-122">Header files</span></span>

<span data-ttu-id="15109-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="15109-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="15109-124">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="15109-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="15109-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="15109-125">Mapitags.h</span></span>
  
> <span data-ttu-id="15109-126">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="15109-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="15109-127">См. также</span><span class="sxs-lookup"><span data-stu-id="15109-127">See also</span></span>



[<span data-ttu-id="15109-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="15109-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="15109-129">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="15109-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="15109-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="15109-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="15109-131">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="15109-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

