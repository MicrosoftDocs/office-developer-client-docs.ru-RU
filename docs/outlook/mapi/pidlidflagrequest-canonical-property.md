---
title: Каноническое свойство PidLidFlagRequest
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFlagRequest
api_type:
- COM
ms.assetid: 38981f07-14b8-47c2-93df-e6aed91896e4
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ddcf32df716fe2b0a02655278ff0cd8d821de1f4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357808"
---
# <a name="pidlidflagrequest-canonical-property"></a><span data-ttu-id="193a2-103">Каноническое свойство PidLidFlagRequest</span><span class="sxs-lookup"><span data-stu-id="193a2-103">PidLidFlagRequest Canonical Property</span></span>

  
  
<span data-ttu-id="193a2-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="193a2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="193a2-105">Представляет состояние приглашения на собрание.</span><span class="sxs-lookup"><span data-stu-id="193a2-105">Represents the status of a meeting request.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="193a2-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="193a2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="193a2-107">диспидрекуест</span><span class="sxs-lookup"><span data-stu-id="193a2-107">dispidRequest</span></span>  <br/> |
|<span data-ttu-id="193a2-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="193a2-108">Property set:</span></span>  <br/> |<span data-ttu-id="193a2-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="193a2-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="193a2-110">Длинный идентификатор (крышка):</span><span class="sxs-lookup"><span data-stu-id="193a2-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="193a2-111">0x00008530</span><span class="sxs-lookup"><span data-stu-id="193a2-111">0x00008530</span></span>  <br/> |
|<span data-ttu-id="193a2-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="193a2-112">Data type:</span></span>  <br/> |<span data-ttu-id="193a2-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="193a2-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="193a2-114">Область:</span><span class="sxs-lookup"><span data-stu-id="193a2-114">Area:</span></span>  <br/> |<span data-ttu-id="193a2-115">Пометка</span><span class="sxs-lookup"><span data-stu-id="193a2-115">Flagging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="193a2-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="193a2-116">Remarks</span></span>

<span data-ttu-id="193a2-117">В Microsoft Office Outlook приглашение на собрание является элементом встречи.</span><span class="sxs-lookup"><span data-stu-id="193a2-117">In Microsoft Office Outlook, a meeting request is an appointment item.</span></span>
  
<span data-ttu-id="193a2-118">Это свойство содержит определяемый пользователем текст, который необходимо связать с флагом и должен быть задан, если объект сообщения помечен или завершен, но не должен существовать для объекта, связанного с собранием.</span><span class="sxs-lookup"><span data-stu-id="193a2-118">This property contains user-specifiable text to be associated with the flag and should be set if the message object is flagged or completed, but should not exist for a meeting-related object.</span></span> <span data-ttu-id="193a2-119">Клиенты могут отказаться от поддержки этого свойства и всегда записывать "к исполнению" (при необходимости он преобразуется на язык пользователя) в качестве значения строки, когда это свойство должно быть задано.</span><span class="sxs-lookup"><span data-stu-id="193a2-119">Clients may choose not to support this property, and always write "Follow up" (translated to the user's language if appropriate) as the value of the string when this property should be set.</span></span> <span data-ttu-id="193a2-120">Это свойство должно игнорироваться условно в зависимости от значений свойств **диспидфлагстринженум** ([PidLidFlagString](pidlidflagstring-canonical-property.md)) и **диспидвалидфлагстрингпруф** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="193a2-120">This property should be conditionally ignored based on the values of the **dispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)) and **dispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)) properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="193a2-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="193a2-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="193a2-122">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="193a2-122">Protocol specifications</span></span>

<span data-ttu-id="193a2-123">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="193a2-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="193a2-124">Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="193a2-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="193a2-125">[[MS — ОКСОФЛАГ]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="193a2-125">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="193a2-126">Задает свойства и операции, связанные с пометкой.</span><span class="sxs-lookup"><span data-stu-id="193a2-126">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="193a2-127">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="193a2-127">Header files</span></span>

<span data-ttu-id="193a2-128">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="193a2-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="193a2-129">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="193a2-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="193a2-130">См. также</span><span class="sxs-lookup"><span data-stu-id="193a2-130">See also</span></span>



[<span data-ttu-id="193a2-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="193a2-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="193a2-132">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="193a2-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="193a2-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="193a2-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="193a2-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="193a2-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

