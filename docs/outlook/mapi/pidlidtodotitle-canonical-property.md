---
title: Каноническое свойство PidLidToDoTitle
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidToDoTitle
api_type:
- COM
ms.assetid: 94cf031f-4c78-441d-9c01-55905b4974e0
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7ed69d9bab84a5c572026bb9480249c1212e3376
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339944"
---
# <a name="pidlidtodotitle-canonical-property"></a><span data-ttu-id="e6116-103">Каноническое свойство PidLidToDoTitle</span><span class="sxs-lookup"><span data-stu-id="e6116-103">PidLidToDoTitle Canonical Property</span></span>

  
  
<span data-ttu-id="e6116-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e6116-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e6116-105">Содержит указанный пользователем текст для идентификации этого объекта сообщения в консолидированном списке дел.</span><span class="sxs-lookup"><span data-stu-id="e6116-105">Contains user-specifiable text to identify this message object in a consolidated to-do list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e6116-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="e6116-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e6116-107">dispidToDoTitle</span><span class="sxs-lookup"><span data-stu-id="e6116-107">dispidToDoTitle</span></span>  <br/> |
|<span data-ttu-id="e6116-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="e6116-108">Property set:</span></span>  <br/> |<span data-ttu-id="e6116-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="e6116-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="e6116-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="e6116-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="e6116-111">0x000085A4</span><span class="sxs-lookup"><span data-stu-id="e6116-111">0x000085A4</span></span>  <br/> |
|<span data-ttu-id="e6116-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="e6116-112">Data type:</span></span>  <br/> |<span data-ttu-id="e6116-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e6116-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="e6116-114">Область:</span><span class="sxs-lookup"><span data-stu-id="e6116-114">Area:</span></span>  <br/> |<span data-ttu-id="e6116-115">Задача</span><span class="sxs-lookup"><span data-stu-id="e6116-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e6116-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="e6116-116">Remarks</span></span>

<span data-ttu-id="e6116-117">Это свойство не должно быть заданной задачей.</span><span class="sxs-lookup"><span data-stu-id="e6116-117">This property must not be set on a task.</span></span> <span data-ttu-id="e6116-118">Чтобы указать пустое свойство, не установите это свойство в строку нулевой длины, а удалите его.</span><span class="sxs-lookup"><span data-stu-id="e6116-118">To indicate an empty property, do not set this property to the zero-length string, but instead delete it.</span></span> 
  
<span data-ttu-id="e6116-119">При маркировке объекта сообщения, а свойства не существует, клиент должен написать значение **PR_NORMALIZED_SUBJECT** [(PidTagNormalizedSubject)](pidtagnormalizedsubject-canonical-property.md)в это свойство.</span><span class="sxs-lookup"><span data-stu-id="e6116-119">When flagging a message object, and the property does not exist, a client should write the value of **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) to this property.</span></span>
  
<span data-ttu-id="e6116-120">В консолидированном списке дел, если этого свойства не существует, клиент должен **заменить** значение свойства PR_NORMALIZED_SUBJECT при отобращении этого свойства в списке дел.</span><span class="sxs-lookup"><span data-stu-id="e6116-120">In a consolidated to-do list, if this property does not exist, a client should substitute the value of the **PR_NORMALIZED_SUBJECT** property when displaying this property in the to-do list.</span></span> 
  
<span data-ttu-id="e6116-121">На объекте черновика сообщения, если клиент реализует флаги отправитель, это свойство должно быть установлено в том же значении, что **и dispidRequest** [(PidLidFlagRequest).](pidlidflagrequest-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="e6116-121">On a draft message object, if the client implements sender flags, this property should be set to the same value as **dispidRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e6116-122">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="e6116-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e6116-123">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="e6116-123">Protocol specifications</span></span>

<span data-ttu-id="e6116-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e6116-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e6116-125">Предоставляет определения набора свойств и ссылки на спецификации Exchange Server протокола</span><span class="sxs-lookup"><span data-stu-id="e6116-125">Provides property set definitions and references to related Exchange Server protocol specifications</span></span>
    
<span data-ttu-id="e6116-126">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e6116-126">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e6116-127">Указывает свойства и операции, связанные с маркировкой.</span><span class="sxs-lookup"><span data-stu-id="e6116-127">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e6116-128">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="e6116-128">Header files</span></span>

<span data-ttu-id="e6116-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e6116-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="e6116-130">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="e6116-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e6116-131">См. также</span><span class="sxs-lookup"><span data-stu-id="e6116-131">See also</span></span>



[<span data-ttu-id="e6116-132">Каноническое свойство PidTagNormalizedSubject</span><span class="sxs-lookup"><span data-stu-id="e6116-132">PidTagNormalizedSubject Canonical Property</span></span>](pidtagnormalizedsubject-canonical-property.md)
  
[<span data-ttu-id="e6116-133">������������ �������� PidLidFlagRequest</span><span class="sxs-lookup"><span data-stu-id="e6116-133">PidLidFlagRequest Canonical Property</span></span>](pidlidflagrequest-canonical-property.md)


[<span data-ttu-id="e6116-134">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="e6116-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e6116-135">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="e6116-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e6116-136">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="e6116-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e6116-137">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="e6116-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

