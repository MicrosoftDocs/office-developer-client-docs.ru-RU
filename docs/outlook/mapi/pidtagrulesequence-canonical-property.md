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
# <a name="pidtagrulesequence-canonical-property"></a><span data-ttu-id="22c86-103">Каноническое свойство PidTagRuleSequence</span><span class="sxs-lookup"><span data-stu-id="22c86-103">PidTagRuleSequence Canonical Property</span></span>

  
  
<span data-ttu-id="22c86-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="22c86-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="22c86-105">Значение, используемее для определения порядка, в котором правила оцениваются и выполняются.</span><span class="sxs-lookup"><span data-stu-id="22c86-105">A value used to determine the order in which rules are evaluated and executed.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="22c86-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="22c86-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="22c86-107">PR_RULE_SEQUENCE</span><span class="sxs-lookup"><span data-stu-id="22c86-107">PR_RULE_SEQUENCE</span></span>  <br/> |
|<span data-ttu-id="22c86-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="22c86-108">Identifier:</span></span>  <br/> |<span data-ttu-id="22c86-109">0x6676</span><span class="sxs-lookup"><span data-stu-id="22c86-109">0x6676</span></span>  <br/> |
|<span data-ttu-id="22c86-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="22c86-110">Data type:</span></span>  <br/> |<span data-ttu-id="22c86-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="22c86-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="22c86-112">Область:</span><span class="sxs-lookup"><span data-stu-id="22c86-112">Area:</span></span>  <br/> |<span data-ttu-id="22c86-113">Правила на стороне сервера</span><span class="sxs-lookup"><span data-stu-id="22c86-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="22c86-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="22c86-114">Remarks</span></span>

<span data-ttu-id="22c86-115">Правила оцениваются по порядку в соответствии с порядком увеличения этого значения.</span><span class="sxs-lookup"><span data-stu-id="22c86-115">Rules are evaluated in sequence according to the increasing order of this value.</span></span> <span data-ttu-id="22c86-116">Порядок оценки правил, которые имеют одинаковое значение в этом свойстве, не заданной.</span><span class="sxs-lookup"><span data-stu-id="22c86-116">The evaluation order for rules that have the same value in this property is undefined.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="22c86-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="22c86-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="22c86-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="22c86-118">Protocol specifications</span></span>

<span data-ttu-id="22c86-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="22c86-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="22c86-120">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="22c86-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="22c86-121">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="22c86-121">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="22c86-122">Управляет входящие сообщения электронной почты на сервере.</span><span class="sxs-lookup"><span data-stu-id="22c86-122">Manipulates incoming email messages on a server.</span></span>
    
<span data-ttu-id="22c86-123">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="22c86-123">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="22c86-124">Указывает методы подключения и настройки почтовых ящиков в качестве делегатов, а также взаимодействия с элементами сообщений и календаря, когда они действуют от имени другого пользователя.</span><span class="sxs-lookup"><span data-stu-id="22c86-124">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar items when they act on behalf of another user.</span></span>
    
<span data-ttu-id="22c86-125">[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="22c86-125">[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="22c86-126">Включает допустимые операции для основных объектов таблицы.</span><span class="sxs-lookup"><span data-stu-id="22c86-126">Includes permissible operations for the core table objects.</span></span>
    
<span data-ttu-id="22c86-127">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="22c86-127">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="22c86-128">Указывает допустимые операции для основных объектов хранения сообщений.</span><span class="sxs-lookup"><span data-stu-id="22c86-128">Specifies permissible operations for the core message store objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="22c86-129">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="22c86-129">Header files</span></span>

<span data-ttu-id="22c86-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="22c86-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="22c86-131">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="22c86-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="22c86-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="22c86-132">Mapitags.h</span></span>
  
> <span data-ttu-id="22c86-133">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="22c86-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="22c86-134">См. также</span><span class="sxs-lookup"><span data-stu-id="22c86-134">See also</span></span>



[<span data-ttu-id="22c86-135">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="22c86-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="22c86-136">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="22c86-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="22c86-137">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="22c86-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="22c86-138">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="22c86-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

