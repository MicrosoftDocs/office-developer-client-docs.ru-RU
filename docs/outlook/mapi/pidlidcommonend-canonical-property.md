---
title: Каноническое свойство PidLidCommonEnd
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCommonEnd
api_type:
- COM
ms.assetid: c89f388a-1585-4bed-91b4-1b0c268292f3
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 97d6ef6343cedb6fbed93cccda9f65476bb73f4f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345502"
---
# <a name="pidlidcommonend-canonical-property"></a><span data-ttu-id="2c491-103">Каноническое свойство PidLidCommonEnd</span><span class="sxs-lookup"><span data-stu-id="2c491-103">PidLidCommonEnd Canonical Property</span></span>

  
  
<span data-ttu-id="2c491-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2c491-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2c491-105">Представляет дату и время окончания сообщения.</span><span class="sxs-lookup"><span data-stu-id="2c491-105">Represents the end date and time of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2c491-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="2c491-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2c491-107">Диспидкоммоненд</span><span class="sxs-lookup"><span data-stu-id="2c491-107">dispidCommonEnd</span></span>  <br/> |
|<span data-ttu-id="2c491-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="2c491-108">Property set:</span></span>  <br/> |<span data-ttu-id="2c491-109">Псетид_коммон</span><span class="sxs-lookup"><span data-stu-id="2c491-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="2c491-110">Длинный идентификатор (крышка):</span><span class="sxs-lookup"><span data-stu-id="2c491-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="2c491-111">0x00008517</span><span class="sxs-lookup"><span data-stu-id="2c491-111">0x00008517</span></span>  <br/> |
|<span data-ttu-id="2c491-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="2c491-112">Data type:</span></span>  <br/> |<span data-ttu-id="2c491-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="2c491-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="2c491-114">Область:</span><span class="sxs-lookup"><span data-stu-id="2c491-114">Area:</span></span>  <br/> |<span data-ttu-id="2c491-115">Общий обмен сообщениями</span><span class="sxs-lookup"><span data-stu-id="2c491-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2c491-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2c491-116">Remarks</span></span>

<span data-ttu-id="2c491-117">Это свойство указывает время окончания для элемента.</span><span class="sxs-lookup"><span data-stu-id="2c491-117">This property indicates the end time for an item.</span></span> <span data-ttu-id="2c491-118">Оно должно быть больше или равно значению свойства **диспидкоммонстарт** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="2c491-118">It must be greater than or equal to the value of the **dispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="2c491-119">Это значение должно быть эквивалентом свойства **диспидтаскдуедате** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) в формате всемирного координированного времени (UTC).</span><span class="sxs-lookup"><span data-stu-id="2c491-119">This value must be the Coordinated Universal Time (UTC) equivalent of the **dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2c491-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="2c491-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2c491-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="2c491-121">Protocol specifications</span></span>

<span data-ttu-id="2c491-122">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2c491-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2c491-123">Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="2c491-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2c491-124">[[MS — ОКСКМСГ]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2c491-124">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2c491-125">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="2c491-125">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="2c491-126">[[MS — ОКСОТАСК]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2c491-126">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2c491-127">Задает свойства и операции, допустимые для контактов и личных списков рассылки.</span><span class="sxs-lookup"><span data-stu-id="2c491-127">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2c491-128">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="2c491-128">Header files</span></span>

<span data-ttu-id="2c491-129">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="2c491-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="2c491-130">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="2c491-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2c491-131">См. также</span><span class="sxs-lookup"><span data-stu-id="2c491-131">See also</span></span>



[<span data-ttu-id="2c491-132">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="2c491-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2c491-133">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="2c491-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2c491-134">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="2c491-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2c491-135">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="2c491-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

