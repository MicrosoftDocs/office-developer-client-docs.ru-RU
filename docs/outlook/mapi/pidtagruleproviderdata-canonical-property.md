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
ms.openlocfilehash: e4d209c4f185ff253476beb04913e6a64884f9b6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335422"
---
# <a name="pidtagruleproviderdata-canonical-property"></a><span data-ttu-id="9f17f-103">Каноническое свойство PidTagRuleProviderData</span><span class="sxs-lookup"><span data-stu-id="9f17f-103">PidTagRuleProviderData Canonical Property</span></span>

  
  
<span data-ttu-id="9f17f-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9f17f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9f17f-105">Непрозрачное свойство, которое клиент задает для монопольного использования клиента.</span><span class="sxs-lookup"><span data-stu-id="9f17f-105">An opaque property that the client sets for the exclusive use of the client.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9f17f-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="9f17f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9f17f-107">PR_RULE_PROVIDER_DATA</span><span class="sxs-lookup"><span data-stu-id="9f17f-107">PR_RULE_PROVIDER_DATA</span></span>  <br/> |
|<span data-ttu-id="9f17f-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="9f17f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9f17f-109">0x6684</span><span class="sxs-lookup"><span data-stu-id="9f17f-109">0x6684</span></span>  <br/> |
|<span data-ttu-id="9f17f-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="9f17f-110">Data type:</span></span>  <br/> |<span data-ttu-id="9f17f-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="9f17f-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="9f17f-112">Область:</span><span class="sxs-lookup"><span data-stu-id="9f17f-112">Area:</span></span>  <br/> |<span data-ttu-id="9f17f-113">Правила на стороне сервера</span><span class="sxs-lookup"><span data-stu-id="9f17f-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9f17f-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="9f17f-114">Remarks</span></span>

<span data-ttu-id="9f17f-115">Сервер должен сохранить значение этого свойства, если оно было задано клиентом, но во время оценки и обработки правила необходимо проигнорировать его содержимое.</span><span class="sxs-lookup"><span data-stu-id="9f17f-115">The server must preserve the value of this property if it was set by the client but must ignore its contents during rule evaluation and processing.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9f17f-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="9f17f-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9f17f-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="9f17f-117">Protocol specifications</span></span>

<span data-ttu-id="9f17f-118">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9f17f-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9f17f-119">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="9f17f-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9f17f-120">[[MS — ОКСОРУЛЕ]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9f17f-120">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9f17f-121">Управляет входящими сообщениями электронной почты на сервере.</span><span class="sxs-lookup"><span data-stu-id="9f17f-121">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9f17f-122">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="9f17f-122">Header files</span></span>

<span data-ttu-id="9f17f-123">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="9f17f-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="9f17f-124">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="9f17f-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="9f17f-125">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="9f17f-125">Mapitags.h</span></span>
  
> <span data-ttu-id="9f17f-126">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="9f17f-126">Contains definitions of properties listed as associated properties.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="9f17f-127">См. также</span><span class="sxs-lookup"><span data-stu-id="9f17f-127">See also</span></span>



[<span data-ttu-id="9f17f-128">Каноническое свойство PidTagRuleProvider</span><span class="sxs-lookup"><span data-stu-id="9f17f-128">PidTagRuleProvider Canonical Property</span></span>](pidtagruleprovider-canonical-property.md)


[<span data-ttu-id="9f17f-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="9f17f-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9f17f-130">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="9f17f-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9f17f-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="9f17f-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9f17f-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="9f17f-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

