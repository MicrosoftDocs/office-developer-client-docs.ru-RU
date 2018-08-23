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
ms.openlocfilehash: 7f36562ba189cd8f547056b93c0f0373ee9a3360
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563494"
---
# <a name="pidtagrulesequence-canonical-property"></a><span data-ttu-id="b32c3-103">Каноническое свойство PidTagRuleSequence</span><span class="sxs-lookup"><span data-stu-id="b32c3-103">PidTagRuleSequence Canonical Property</span></span>

  
  
<span data-ttu-id="b32c3-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b32c3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b32c3-105">Значение, используемое для определения порядка, в котором правила проверяются и выполняются.</span><span class="sxs-lookup"><span data-stu-id="b32c3-105">A value used to determine the order in which rules are evaluated and executed.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b32c3-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="b32c3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b32c3-107">PR_RULE_SEQUENCE</span><span class="sxs-lookup"><span data-stu-id="b32c3-107">PR_RULE_SEQUENCE</span></span>  <br/> |
|<span data-ttu-id="b32c3-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="b32c3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b32c3-109">0x6676</span><span class="sxs-lookup"><span data-stu-id="b32c3-109">0x6676</span></span>  <br/> |
|<span data-ttu-id="b32c3-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="b32c3-110">Data type:</span></span>  <br/> |<span data-ttu-id="b32c3-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="b32c3-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="b32c3-112">Область:</span><span class="sxs-lookup"><span data-stu-id="b32c3-112">Area:</span></span>  <br/> |<span data-ttu-id="b32c3-113">Правила со стороны сервера</span><span class="sxs-lookup"><span data-stu-id="b32c3-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b32c3-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="b32c3-114">Remarks</span></span>

<span data-ttu-id="b32c3-115">Правила оцениваются в последовательности в порядке возрастания это значение.</span><span class="sxs-lookup"><span data-stu-id="b32c3-115">Rules are evaluated in sequence according to the increasing order of this value.</span></span> <span data-ttu-id="b32c3-116">Порядок вычисления для правил, которые имеют одинаковые значения в этом свойстве не определен.</span><span class="sxs-lookup"><span data-stu-id="b32c3-116">The evaluation order for rules that have the same value in this property is undefined.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b32c3-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b32c3-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b32c3-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="b32c3-118">Protocol specifications</span></span>

<span data-ttu-id="b32c3-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b32c3-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b32c3-120">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="b32c3-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b32c3-121">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b32c3-121">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b32c3-122">Управляет входящие сообщения электронной почты на сервере.</span><span class="sxs-lookup"><span data-stu-id="b32c3-122">Manipulates incoming email messages on a server.</span></span>
    
<span data-ttu-id="b32c3-123">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b32c3-123">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b32c3-124">Указывает методы для подключений и настройки почтовых ящиков как делегаты и взаимодействия с элементами календаря и сообщения, когда они действовать от имени другого пользователя.</span><span class="sxs-lookup"><span data-stu-id="b32c3-124">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar items when they act on behalf of another user.</span></span>
    
<span data-ttu-id="b32c3-125">[[MS-OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b32c3-125">[[MS-OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b32c3-126">Включает в себя разрешенных операций для базовых объектов в таблице.</span><span class="sxs-lookup"><span data-stu-id="b32c3-126">Includes permissible operations for the core table objects.</span></span>
    
<span data-ttu-id="b32c3-127">[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b32c3-127">[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b32c3-128">Указывает допустимые операции для базовых объектов хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="b32c3-128">Specifies permissible operations for the core message store objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b32c3-129">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="b32c3-129">Header files</span></span>

<span data-ttu-id="b32c3-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b32c3-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="b32c3-131">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="b32c3-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="b32c3-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b32c3-132">Mapitags.h</span></span>
  
> <span data-ttu-id="b32c3-133">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="b32c3-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b32c3-134">См. также</span><span class="sxs-lookup"><span data-stu-id="b32c3-134">See also</span></span>



[<span data-ttu-id="b32c3-135">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b32c3-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b32c3-136">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b32c3-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b32c3-137">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="b32c3-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b32c3-138">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="b32c3-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

