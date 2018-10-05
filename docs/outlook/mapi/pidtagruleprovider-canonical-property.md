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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385979"
---
# <a name="pidtagruleprovider-canonical-property"></a><span data-ttu-id="da141-103">Каноническое свойство PidTagRuleProvider</span><span class="sxs-lookup"><span data-stu-id="da141-103">PidTagRuleProvider Canonical Property</span></span>

  
  
<span data-ttu-id="da141-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="da141-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="da141-105">Содержит имя приложения, который задает правило.</span><span class="sxs-lookup"><span data-stu-id="da141-105">Contains the name of the application that sets a rule.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="da141-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="da141-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="da141-107">PR_RULE_PROVIDER, PR_RULE_PROVIDER_A, PR_RULE_PROVIDER_W</span><span class="sxs-lookup"><span data-stu-id="da141-107">PR_RULE_PROVIDER, PR_RULE_PROVIDER_A , PR_RULE_PROVIDER_W</span></span>  <br/> |
|<span data-ttu-id="da141-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="da141-108">Identifier:</span></span>  <br/> |<span data-ttu-id="da141-109">0x6681</span><span class="sxs-lookup"><span data-stu-id="da141-109">0x6681</span></span>  <br/> |
|<span data-ttu-id="da141-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="da141-110">Data type:</span></span>  <br/> |<span data-ttu-id="da141-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="da141-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="da141-112">Область:</span><span class="sxs-lookup"><span data-stu-id="da141-112">Area:</span></span>  <br/> |<span data-ttu-id="da141-113">Правила со стороны сервера</span><span class="sxs-lookup"><span data-stu-id="da141-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="da141-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="da141-114">Remarks</span></span>

<span data-ttu-id="da141-115">Отложенное необходимость действия для идентификации в коде эти свойства, которые необходимо интерпретировать и выполнить действие правила.</span><span class="sxs-lookup"><span data-stu-id="da141-115">Deferred actions need these properties to identify the code that must interpret and execute the rule action.</span></span>
  
<span data-ttu-id="da141-116">Правила, которые хранятся на почтовые ящики и папки связаны с приложением, который несет ответственность за их строкой поставщика правила.</span><span class="sxs-lookup"><span data-stu-id="da141-116">Rules stored on mailboxes and folders are associated with the application that owns them by a rule provider string.</span></span> <span data-ttu-id="da141-117">Поставщик правило задает и обрабатывает правила в таблице правил.</span><span class="sxs-lookup"><span data-stu-id="da141-117">A rule provider sets and handles rules in a rule table.</span></span> <span data-ttu-id="da141-118">Он также предоставляет средства обработки все отложенные действия, если значение таких правил.</span><span class="sxs-lookup"><span data-stu-id="da141-118">It also provides a means of handling any deferred actions if such rules are set.</span></span> <span data-ttu-id="da141-119">Отложенные действия создаются неявно с банка данных.</span><span class="sxs-lookup"><span data-stu-id="da141-119">Deferred actions are created implicitly by the information store.</span></span> <span data-ttu-id="da141-120">Для операций перемещения или копирования для различных хранилища Если поставщик задается отложенного действия, он должен предоставить обработчик для действий при срабатывании правила и создано отложенного действия.</span><span class="sxs-lookup"><span data-stu-id="da141-120">For move or copy operations to a different store, if a provider sets a deferred action rule, it must provide a handler to perform the action when the rule is fired and a deferred action is created.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="da141-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="da141-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="da141-122">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="da141-122">Protocol specifications</span></span>

<span data-ttu-id="da141-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="da141-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="da141-124">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="da141-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="da141-125">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="da141-125">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="da141-126">Управляет входящие сообщения электронной почты на сервере.</span><span class="sxs-lookup"><span data-stu-id="da141-126">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="da141-127">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="da141-127">Header files</span></span>

<span data-ttu-id="da141-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="da141-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="da141-129">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="da141-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="da141-130">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="da141-130">Mapitags.h</span></span>
  
> <span data-ttu-id="da141-131">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="da141-131">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="da141-132">См. также</span><span class="sxs-lookup"><span data-stu-id="da141-132">See also</span></span>



[<span data-ttu-id="da141-133">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="da141-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="da141-134">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="da141-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="da141-135">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="da141-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="da141-136">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="da141-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

