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
ms.openlocfilehash: 03c4c0810c69f8dd8f22ce84212200d3ccad1dab
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563242"
---
# <a name="pidtagcreationtime-canonical-property"></a><span data-ttu-id="b05a4-103">Каноническое свойство PidTagCreationTime</span><span class="sxs-lookup"><span data-stu-id="b05a4-103">PidTagCreationTime Canonical Property</span></span>

  
  
<span data-ttu-id="b05a4-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b05a4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b05a4-105">Содержит дату и время создания сообщения.</span><span class="sxs-lookup"><span data-stu-id="b05a4-105">Contains the creation date and time of a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b05a4-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="b05a4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b05a4-107">PR_CREATION_TIME</span><span class="sxs-lookup"><span data-stu-id="b05a4-107">PR_CREATION_TIME</span></span>  <br/> |
|<span data-ttu-id="b05a4-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="b05a4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b05a4-109">0x3007</span><span class="sxs-lookup"><span data-stu-id="b05a4-109">0x3007</span></span>  <br/> |
|<span data-ttu-id="b05a4-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="b05a4-110">Data type:</span></span>  <br/> |<span data-ttu-id="b05a4-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="b05a4-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="b05a4-112">Область:</span><span class="sxs-lookup"><span data-stu-id="b05a4-112">Area:</span></span>  <br/> |<span data-ttu-id="b05a4-113">Время сообщения</span><span class="sxs-lookup"><span data-stu-id="b05a4-113">Message time</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b05a4-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="b05a4-114">Remarks</span></span>

<span data-ttu-id="b05a4-115">Хранилище сообщений этому свойству для каждого сообщения, он создает.</span><span class="sxs-lookup"><span data-stu-id="b05a4-115">A message store sets this property for each message that it creates.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b05a4-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b05a4-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b05a4-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="b05a4-117">Protocol specifications</span></span>

<span data-ttu-id="b05a4-118">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b05a4-118">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b05a4-119">Обрабатывает объекты сообщения и вложения.</span><span class="sxs-lookup"><span data-stu-id="b05a4-119">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="b05a4-120">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b05a4-120">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b05a4-121">Задает свойства и операции для списков пользователей, контактов, групп и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b05a4-121">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b05a4-122">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="b05a4-122">Header files</span></span>

<span data-ttu-id="b05a4-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b05a4-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="b05a4-124">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="b05a4-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="b05a4-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b05a4-125">Mapitags.h</span></span>
  
> <span data-ttu-id="b05a4-126">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="b05a4-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b05a4-127">См. также</span><span class="sxs-lookup"><span data-stu-id="b05a4-127">See also</span></span>



[<span data-ttu-id="b05a4-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b05a4-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b05a4-129">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b05a4-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b05a4-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="b05a4-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b05a4-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="b05a4-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

