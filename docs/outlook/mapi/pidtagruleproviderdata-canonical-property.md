---
title: Каноническое свойство PidTagRuleProviderData
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleProviderData
api_type:
- COM
ms.assetid: b04a277c-b483-4f54-b360-311034b9a7ee
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f4f1070b89971c631fd855a6f84d56b699152421
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566847"
---
# <a name="pidtagruleproviderdata-canonical-property"></a><span data-ttu-id="f421e-103">Каноническое свойство PidTagRuleProviderData</span><span class="sxs-lookup"><span data-stu-id="f421e-103">PidTagRuleProviderData Canonical Property</span></span>

  
  
<span data-ttu-id="f421e-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f421e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f421e-105">Непрозрачный свойство, которое задает клиента использовать только клиента.</span><span class="sxs-lookup"><span data-stu-id="f421e-105">An opaque property that the client sets for the exclusive use of the client.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f421e-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="f421e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f421e-107">PR_RULE_PROVIDER_DATA</span><span class="sxs-lookup"><span data-stu-id="f421e-107">PR_RULE_PROVIDER_DATA</span></span>  <br/> |
|<span data-ttu-id="f421e-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="f421e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f421e-109">0x6684</span><span class="sxs-lookup"><span data-stu-id="f421e-109">0x6684</span></span>  <br/> |
|<span data-ttu-id="f421e-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="f421e-110">Data type:</span></span>  <br/> |<span data-ttu-id="f421e-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="f421e-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="f421e-112">Область:</span><span class="sxs-lookup"><span data-stu-id="f421e-112">Area:</span></span>  <br/> |<span data-ttu-id="f421e-113">Правила со стороны сервера</span><span class="sxs-lookup"><span data-stu-id="f421e-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f421e-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="f421e-114">Remarks</span></span>

<span data-ttu-id="f421e-115">Сервер должны сохранить значение этого свойства, если оно было задано клиентом, но необходимо игнорировать вместе с контентом во время оценки правил и обработки.</span><span class="sxs-lookup"><span data-stu-id="f421e-115">The server must preserve the value of this property if it was set by the client but must ignore its contents during rule evaluation and processing.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f421e-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f421e-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f421e-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="f421e-117">Protocol specifications</span></span>

<span data-ttu-id="f421e-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f421e-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f421e-119">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="f421e-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f421e-120">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f421e-120">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f421e-121">Управляет входящие сообщения электронной почты на сервере.</span><span class="sxs-lookup"><span data-stu-id="f421e-121">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f421e-122">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="f421e-122">Header files</span></span>

<span data-ttu-id="f421e-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f421e-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="f421e-124">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="f421e-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="f421e-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f421e-125">Mapitags.h</span></span>
  
> <span data-ttu-id="f421e-126">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="f421e-126">Contains definitions of properties listed as associated properties.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="f421e-127">См. также</span><span class="sxs-lookup"><span data-stu-id="f421e-127">See also</span></span>



[<span data-ttu-id="f421e-128">Каноническое свойство PidTagRuleProvider</span><span class="sxs-lookup"><span data-stu-id="f421e-128">PidTagRuleProvider Canonical Property</span></span>](pidtagruleprovider-canonical-property.md)


[<span data-ttu-id="f421e-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f421e-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f421e-130">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f421e-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f421e-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="f421e-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f421e-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="f421e-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

