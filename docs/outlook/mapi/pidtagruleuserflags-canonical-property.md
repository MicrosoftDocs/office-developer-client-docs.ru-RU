---
title: Каноническое свойство PidTagRuleUserFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleUserFlags
api_type:
- COM
ms.assetid: c5dfb21f-b35e-4521-bf2b-e3d03d98d75d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 235efce341e1870f0c33917f1c6d42b021727308
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321345"
---
# <a name="pidtagruleuserflags-canonical-property"></a><span data-ttu-id="73b03-103">Каноническое свойство PidTagRuleUserFlags</span><span class="sxs-lookup"><span data-stu-id="73b03-103">PidTagRuleUserFlags Canonical Property</span></span>

  
  
<span data-ttu-id="73b03-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="73b03-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="73b03-105">Это свойство задается клиентом для эксклюзивного использования клиента.</span><span class="sxs-lookup"><span data-stu-id="73b03-105">This property is set by the client for the exclusive use of the client.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="73b03-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="73b03-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="73b03-107">ПР_РУЛЕ_УСЕР_ФЛАГС</span><span class="sxs-lookup"><span data-stu-id="73b03-107">PR_RULE_USER_FLAGS</span></span>  <br/> |
|<span data-ttu-id="73b03-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="73b03-108">Identifier:</span></span>  <br/> |<span data-ttu-id="73b03-109">0x6678</span><span class="sxs-lookup"><span data-stu-id="73b03-109">0x6678</span></span>  <br/> |
|<span data-ttu-id="73b03-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="73b03-110">Data type:</span></span>  <br/> |<span data-ttu-id="73b03-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="73b03-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="73b03-112">Область:</span><span class="sxs-lookup"><span data-stu-id="73b03-112">Area:</span></span>  <br/> |<span data-ttu-id="73b03-113">Правила на стороне сервера</span><span class="sxs-lookup"><span data-stu-id="73b03-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="73b03-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="73b03-114">Remarks</span></span>

<span data-ttu-id="73b03-115">Сервер должен сохранить значение этого свойства, если оно было задано клиентом.</span><span class="sxs-lookup"><span data-stu-id="73b03-115">The server must preserve the value of this property if it was set by the client.</span></span> <span data-ttu-id="73b03-116">Сервер должен игнорировать его во время оценки и обработки правила.</span><span class="sxs-lookup"><span data-stu-id="73b03-116">The server must ignore it during rule evaluation and processing.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="73b03-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="73b03-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="73b03-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="73b03-118">Protocol specifications</span></span>

<span data-ttu-id="73b03-119">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="73b03-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="73b03-120">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="73b03-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="73b03-121">[[MS — ОКСОРУЛЕ]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="73b03-121">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="73b03-122">Управляет входящими сообщениями электронной почты на сервере.</span><span class="sxs-lookup"><span data-stu-id="73b03-122">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="73b03-123">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="73b03-123">Header files</span></span>

<span data-ttu-id="73b03-124">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="73b03-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="73b03-125">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="73b03-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="73b03-126">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="73b03-126">Mapitags.h</span></span>
  
> <span data-ttu-id="73b03-127">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="73b03-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="73b03-128">См. также</span><span class="sxs-lookup"><span data-stu-id="73b03-128">See also</span></span>



[<span data-ttu-id="73b03-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="73b03-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="73b03-130">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="73b03-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="73b03-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="73b03-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="73b03-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="73b03-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

