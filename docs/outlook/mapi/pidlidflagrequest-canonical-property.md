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
ms.openlocfilehash: df2e474206559dadf250bdf9a078c69da61187c8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810351"
---
# <a name="pidlidflagrequest-canonical-property"></a><span data-ttu-id="f35ba-103">Каноническое свойство PidLidFlagRequest</span><span class="sxs-lookup"><span data-stu-id="f35ba-103">PidLidFlagRequest Canonical Property</span></span>

  
  
<span data-ttu-id="f35ba-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f35ba-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f35ba-105">Представляет состояние приглашения на собрание.</span><span class="sxs-lookup"><span data-stu-id="f35ba-105">Represents the status of a meeting request.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f35ba-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="f35ba-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f35ba-107">dispidRequest</span><span class="sxs-lookup"><span data-stu-id="f35ba-107">dispidRequest</span></span>  <br/> |
|<span data-ttu-id="f35ba-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="f35ba-108">Property set:</span></span>  <br/> |<span data-ttu-id="f35ba-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="f35ba-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="f35ba-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="f35ba-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="f35ba-111">0x00008530</span><span class="sxs-lookup"><span data-stu-id="f35ba-111">0x00008530</span></span>  <br/> |
|<span data-ttu-id="f35ba-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="f35ba-112">Data type:</span></span>  <br/> |<span data-ttu-id="f35ba-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f35ba-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="f35ba-114">Область:</span><span class="sxs-lookup"><span data-stu-id="f35ba-114">Area:</span></span>  <br/> |<span data-ttu-id="f35ba-115">Пометка</span><span class="sxs-lookup"><span data-stu-id="f35ba-115">Flagging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f35ba-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="f35ba-116">Remarks</span></span>

<span data-ttu-id="f35ba-117">В программе Microsoft Office Outlook приглашения на собрание — это элемента встречи.</span><span class="sxs-lookup"><span data-stu-id="f35ba-117">In Microsoft Office Outlook, a meeting request is an appointment item.</span></span>
  
<span data-ttu-id="f35ba-118">Это свойство содержит текст, при этом задаваемый пользователей связывались с флагом и должен быть задан, если объект message отмеченные или завершен, но не должна существовать для объекта, относящихся к собранию.</span><span class="sxs-lookup"><span data-stu-id="f35ba-118">This property contains user-specifiable text to be associated with the flag and should be set if the message object is flagged or completed, but should not exist for a meeting-related object.</span></span> <span data-ttu-id="f35ba-119">Клиенты, можно не поддерживают это свойство и всегда запись «Отслеживание» (переведенный на язык пользователя при необходимости) в качестве значения строку, когда необходимо задать это свойство.</span><span class="sxs-lookup"><span data-stu-id="f35ba-119">Clients may choose not to support this property, and always write "Follow up" (translated to the user's language if appropriate) as the value of the string when this property should be set.</span></span> <span data-ttu-id="f35ba-120">Это свойство условно игнорироваться на основании значения свойства **dispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)) и **dispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="f35ba-120">This property should be conditionally ignored based on the values of the **dispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)) and **dispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)) properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f35ba-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f35ba-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f35ba-122">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="f35ba-122">Protocol specifications</span></span>

<span data-ttu-id="f35ba-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f35ba-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f35ba-124">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="f35ba-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f35ba-125">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f35ba-125">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f35ba-126">Задает свойства и операции, связанные с флагов.</span><span class="sxs-lookup"><span data-stu-id="f35ba-126">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f35ba-127">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="f35ba-127">Header files</span></span>

<span data-ttu-id="f35ba-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f35ba-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="f35ba-129">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="f35ba-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f35ba-130">См. также</span><span class="sxs-lookup"><span data-stu-id="f35ba-130">See also</span></span>



[<span data-ttu-id="f35ba-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f35ba-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f35ba-132">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f35ba-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f35ba-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="f35ba-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f35ba-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="f35ba-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

