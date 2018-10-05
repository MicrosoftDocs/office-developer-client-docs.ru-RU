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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397368"
---
# <a name="pidlidflagrequest-canonical-property"></a><span data-ttu-id="b4d96-103">Каноническое свойство PidLidFlagRequest</span><span class="sxs-lookup"><span data-stu-id="b4d96-103">PidLidFlagRequest Canonical Property</span></span>

  
  
<span data-ttu-id="b4d96-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b4d96-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b4d96-105">Представляет состояние приглашения на собрание.</span><span class="sxs-lookup"><span data-stu-id="b4d96-105">Represents the status of a meeting request.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b4d96-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="b4d96-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b4d96-107">dispidRequest</span><span class="sxs-lookup"><span data-stu-id="b4d96-107">dispidRequest</span></span>  <br/> |
|<span data-ttu-id="b4d96-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="b4d96-108">Property set:</span></span>  <br/> |<span data-ttu-id="b4d96-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="b4d96-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="b4d96-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="b4d96-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="b4d96-111">0x00008530</span><span class="sxs-lookup"><span data-stu-id="b4d96-111">0x00008530</span></span>  <br/> |
|<span data-ttu-id="b4d96-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="b4d96-112">Data type:</span></span>  <br/> |<span data-ttu-id="b4d96-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b4d96-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="b4d96-114">Область:</span><span class="sxs-lookup"><span data-stu-id="b4d96-114">Area:</span></span>  <br/> |<span data-ttu-id="b4d96-115">Пометка</span><span class="sxs-lookup"><span data-stu-id="b4d96-115">Flagging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b4d96-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="b4d96-116">Remarks</span></span>

<span data-ttu-id="b4d96-117">В программе Microsoft Office Outlook приглашения на собрание — это элемента встречи.</span><span class="sxs-lookup"><span data-stu-id="b4d96-117">In Microsoft Office Outlook, a meeting request is an appointment item.</span></span>
  
<span data-ttu-id="b4d96-118">Это свойство содержит текст, при этом задаваемый пользователей связывались с флагом и должен быть задан, если объект message отмеченные или завершен, но не должна существовать для объекта, относящихся к собранию.</span><span class="sxs-lookup"><span data-stu-id="b4d96-118">This property contains user-specifiable text to be associated with the flag and should be set if the message object is flagged or completed, but should not exist for a meeting-related object.</span></span> <span data-ttu-id="b4d96-119">Клиенты, можно не поддерживают это свойство и всегда запись «Отслеживание» (переведенный на язык пользователя при необходимости) в качестве значения строку, когда необходимо задать это свойство.</span><span class="sxs-lookup"><span data-stu-id="b4d96-119">Clients may choose not to support this property, and always write "Follow up" (translated to the user's language if appropriate) as the value of the string when this property should be set.</span></span> <span data-ttu-id="b4d96-120">Это свойство условно игнорироваться на основании значения свойства **dispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)) и **dispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b4d96-120">This property should be conditionally ignored based on the values of the **dispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)) and **dispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)) properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b4d96-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b4d96-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b4d96-122">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="b4d96-122">Protocol specifications</span></span>

<span data-ttu-id="b4d96-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b4d96-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b4d96-124">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="b4d96-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b4d96-125">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b4d96-125">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b4d96-126">Задает свойства и операции, связанные с флагов.</span><span class="sxs-lookup"><span data-stu-id="b4d96-126">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b4d96-127">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="b4d96-127">Header files</span></span>

<span data-ttu-id="b4d96-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b4d96-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="b4d96-129">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="b4d96-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b4d96-130">См. также</span><span class="sxs-lookup"><span data-stu-id="b4d96-130">See also</span></span>



[<span data-ttu-id="b4d96-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b4d96-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b4d96-132">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b4d96-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b4d96-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="b4d96-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b4d96-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="b4d96-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

