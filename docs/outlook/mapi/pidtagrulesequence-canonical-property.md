---
title: Каноническое свойство PidTagRuleSequence
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleSequence
api_type:
- COM
ms.assetid: c42f2539-f7d6-464a-a82c-f0ac51823168
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 70e7a20a69b7467c1d8c31469273dcc28ce219ae
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321247"
---
# <a name="pidtagrulesequence-canonical-property"></a><span data-ttu-id="bbe18-103">Каноническое свойство PidTagRuleSequence</span><span class="sxs-lookup"><span data-stu-id="bbe18-103">PidTagRuleSequence Canonical Property</span></span>

  
  
<span data-ttu-id="bbe18-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bbe18-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bbe18-105">Значение, используемее для определения порядка оценки и выполнения правил.</span><span class="sxs-lookup"><span data-stu-id="bbe18-105">A value used to determine the order in which rules are evaluated and executed.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bbe18-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="bbe18-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bbe18-107">PR_RULE_SEQUENCE</span><span class="sxs-lookup"><span data-stu-id="bbe18-107">PR_RULE_SEQUENCE</span></span>  <br/> |
|<span data-ttu-id="bbe18-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="bbe18-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bbe18-109">0x6676</span><span class="sxs-lookup"><span data-stu-id="bbe18-109">0x6676</span></span>  <br/> |
|<span data-ttu-id="bbe18-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="bbe18-110">Data type:</span></span>  <br/> |<span data-ttu-id="bbe18-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="bbe18-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="bbe18-112">Область:</span><span class="sxs-lookup"><span data-stu-id="bbe18-112">Area:</span></span>  <br/> |<span data-ttu-id="bbe18-113">Правила стороне сервера</span><span class="sxs-lookup"><span data-stu-id="bbe18-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bbe18-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="bbe18-114">Remarks</span></span>

<span data-ttu-id="bbe18-115">Правила оцениваются последовательно в соответствии с растущим порядком этого значения.</span><span class="sxs-lookup"><span data-stu-id="bbe18-115">Rules are evaluated in sequence according to the increasing order of this value.</span></span> <span data-ttu-id="bbe18-116">Порядок оценки для правил, которые имеют одинаковое значение в этом свойстве, неопределяется.</span><span class="sxs-lookup"><span data-stu-id="bbe18-116">The evaluation order for rules that have the same value in this property is undefined.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bbe18-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="bbe18-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bbe18-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="bbe18-118">Protocol specifications</span></span>

<span data-ttu-id="bbe18-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bbe18-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bbe18-120">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="bbe18-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bbe18-121">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bbe18-121">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bbe18-122">Манипулирует входящие сообщения электронной почты на сервере.</span><span class="sxs-lookup"><span data-stu-id="bbe18-122">Manipulates incoming email messages on a server.</span></span>
    
<span data-ttu-id="bbe18-123">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bbe18-123">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bbe18-124">Указывает методы подключения и настройки почтовых ящиков в качестве делегатов, а также взаимодействия с элементами сообщения и календаря, когда они действуют от имени другого пользователя.</span><span class="sxs-lookup"><span data-stu-id="bbe18-124">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar items when they act on behalf of another user.</span></span>
    
<span data-ttu-id="bbe18-125">[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bbe18-125">[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bbe18-126">Включает допустимые операции для основных объектов таблицы.</span><span class="sxs-lookup"><span data-stu-id="bbe18-126">Includes permissible operations for the core table objects.</span></span>
    
<span data-ttu-id="bbe18-127">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bbe18-127">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bbe18-128">Указывает допустимые операции для основных объектов хранения сообщений.</span><span class="sxs-lookup"><span data-stu-id="bbe18-128">Specifies permissible operations for the core message store objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bbe18-129">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="bbe18-129">Header files</span></span>

<span data-ttu-id="bbe18-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bbe18-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="bbe18-131">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="bbe18-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="bbe18-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="bbe18-132">Mapitags.h</span></span>
  
> <span data-ttu-id="bbe18-133">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="bbe18-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bbe18-134">См. также</span><span class="sxs-lookup"><span data-stu-id="bbe18-134">See also</span></span>



[<span data-ttu-id="bbe18-135">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="bbe18-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bbe18-136">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="bbe18-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bbe18-137">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="bbe18-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bbe18-138">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="bbe18-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

