---
title: Каноническое свойство PidTagRuleProvider
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleProvider
api_type:
- COM
ms.assetid: 64f80a03-9ba4-495a-9666-b3a909335cb6
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 19889a1f48a6088f0d5ad224f7e9189b112622fa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280607"
---
# <a name="pidtagruleprovider-canonical-property"></a><span data-ttu-id="bc62e-103">Каноническое свойство PidTagRuleProvider</span><span class="sxs-lookup"><span data-stu-id="bc62e-103">PidTagRuleProvider Canonical Property</span></span>

  
  
<span data-ttu-id="bc62e-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bc62e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bc62e-105">Содержит имя приложения, которое задает правило.</span><span class="sxs-lookup"><span data-stu-id="bc62e-105">Contains the name of the application that sets a rule.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bc62e-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="bc62e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bc62e-107">PR_RULE_PROVIDER, PR_RULE_PROVIDER_A , PR_RULE_PROVIDER_W</span><span class="sxs-lookup"><span data-stu-id="bc62e-107">PR_RULE_PROVIDER, PR_RULE_PROVIDER_A , PR_RULE_PROVIDER_W</span></span>  <br/> |
|<span data-ttu-id="bc62e-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="bc62e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bc62e-109">0x6681</span><span class="sxs-lookup"><span data-stu-id="bc62e-109">0x6681</span></span>  <br/> |
|<span data-ttu-id="bc62e-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="bc62e-110">Data type:</span></span>  <br/> |<span data-ttu-id="bc62e-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="bc62e-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="bc62e-112">Область:</span><span class="sxs-lookup"><span data-stu-id="bc62e-112">Area:</span></span>  <br/> |<span data-ttu-id="bc62e-113">Правила стороне сервера</span><span class="sxs-lookup"><span data-stu-id="bc62e-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bc62e-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="bc62e-114">Remarks</span></span>

<span data-ttu-id="bc62e-115">Отложенные действия требуют этих свойств для определения кода, который должен интерпретировать и выполнять действие правила.</span><span class="sxs-lookup"><span data-stu-id="bc62e-115">Deferred actions need these properties to identify the code that must interpret and execute the rule action.</span></span>
  
<span data-ttu-id="bc62e-116">Правила, хранимые в почтовых ящиках и папках, связаны с приложением, которое владеет ими строкой поставщика правил.</span><span class="sxs-lookup"><span data-stu-id="bc62e-116">Rules stored on mailboxes and folders are associated with the application that owns them by a rule provider string.</span></span> <span data-ttu-id="bc62e-117">Поставщик правил задает и обрабатывает правила в таблице правил.</span><span class="sxs-lookup"><span data-stu-id="bc62e-117">A rule provider sets and handles rules in a rule table.</span></span> <span data-ttu-id="bc62e-118">Он также предоставляет средство обработки любых отложенных действий, если такие правила установлены.</span><span class="sxs-lookup"><span data-stu-id="bc62e-118">It also provides a means of handling any deferred actions if such rules are set.</span></span> <span data-ttu-id="bc62e-119">Отложенные действия создаются неявным хранилищем сведений.</span><span class="sxs-lookup"><span data-stu-id="bc62e-119">Deferred actions are created implicitly by the information store.</span></span> <span data-ttu-id="bc62e-120">Для перемещения или копирования операций в другой магазин, если поставщик задает правило отложенных действий, он должен предоставить обработчиве для выполнения действия при увольнении правила и создания отложенного действия.</span><span class="sxs-lookup"><span data-stu-id="bc62e-120">For move or copy operations to a different store, if a provider sets a deferred action rule, it must provide a handler to perform the action when the rule is fired and a deferred action is created.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bc62e-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="bc62e-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bc62e-122">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="bc62e-122">Protocol specifications</span></span>

<span data-ttu-id="bc62e-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bc62e-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bc62e-124">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="bc62e-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bc62e-125">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bc62e-125">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bc62e-126">Манипулирует входящие сообщения электронной почты на сервере.</span><span class="sxs-lookup"><span data-stu-id="bc62e-126">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bc62e-127">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="bc62e-127">Header files</span></span>

<span data-ttu-id="bc62e-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bc62e-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="bc62e-129">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="bc62e-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="bc62e-130">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="bc62e-130">Mapitags.h</span></span>
  
> <span data-ttu-id="bc62e-131">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="bc62e-131">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bc62e-132">См. также</span><span class="sxs-lookup"><span data-stu-id="bc62e-132">See also</span></span>



[<span data-ttu-id="bc62e-133">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="bc62e-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bc62e-134">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="bc62e-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bc62e-135">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="bc62e-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bc62e-136">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="bc62e-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

