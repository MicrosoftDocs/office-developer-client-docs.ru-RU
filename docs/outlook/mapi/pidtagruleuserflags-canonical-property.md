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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392727"
---
# <a name="pidtagruleuserflags-canonical-property"></a><span data-ttu-id="9ea22-103">Каноническое свойство PidTagRuleUserFlags</span><span class="sxs-lookup"><span data-stu-id="9ea22-103">PidTagRuleUserFlags Canonical Property</span></span>

  
  
<span data-ttu-id="9ea22-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9ea22-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9ea22-105">Это свойство имеет значение клиентом использовать только клиента.</span><span class="sxs-lookup"><span data-stu-id="9ea22-105">This property is set by the client for the exclusive use of the client.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9ea22-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="9ea22-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9ea22-107">PR_RULE_USER_FLAGS</span><span class="sxs-lookup"><span data-stu-id="9ea22-107">PR_RULE_USER_FLAGS</span></span>  <br/> |
|<span data-ttu-id="9ea22-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="9ea22-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9ea22-109">0x6678</span><span class="sxs-lookup"><span data-stu-id="9ea22-109">0x6678</span></span>  <br/> |
|<span data-ttu-id="9ea22-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="9ea22-110">Data type:</span></span>  <br/> |<span data-ttu-id="9ea22-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="9ea22-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="9ea22-112">Область:</span><span class="sxs-lookup"><span data-stu-id="9ea22-112">Area:</span></span>  <br/> |<span data-ttu-id="9ea22-113">Правила со стороны сервера</span><span class="sxs-lookup"><span data-stu-id="9ea22-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9ea22-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="9ea22-114">Remarks</span></span>

<span data-ttu-id="9ea22-115">Сервер должны сохранить значение этого свойства, если оно было задано клиентом.</span><span class="sxs-lookup"><span data-stu-id="9ea22-115">The server must preserve the value of this property if it was set by the client.</span></span> <span data-ttu-id="9ea22-116">Сервер должен пропустить во время оценки правил и обработки.</span><span class="sxs-lookup"><span data-stu-id="9ea22-116">The server must ignore it during rule evaluation and processing.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9ea22-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="9ea22-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9ea22-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="9ea22-118">Protocol specifications</span></span>

<span data-ttu-id="9ea22-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9ea22-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9ea22-120">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="9ea22-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9ea22-121">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9ea22-121">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9ea22-122">Управляет входящие сообщения электронной почты на сервере.</span><span class="sxs-lookup"><span data-stu-id="9ea22-122">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9ea22-123">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="9ea22-123">Header files</span></span>

<span data-ttu-id="9ea22-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9ea22-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="9ea22-125">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="9ea22-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="9ea22-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9ea22-126">Mapitags.h</span></span>
  
> <span data-ttu-id="9ea22-127">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="9ea22-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9ea22-128">См. также</span><span class="sxs-lookup"><span data-stu-id="9ea22-128">See also</span></span>



[<span data-ttu-id="9ea22-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="9ea22-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9ea22-130">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="9ea22-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9ea22-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="9ea22-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9ea22-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="9ea22-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

