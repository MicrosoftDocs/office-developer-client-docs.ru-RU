---
title: Каноническое свойство PidTagRuleLevel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleLevel
api_type:
- COM
ms.assetid: b1a30543-250d-4afb-87f2-448d90ee7cf9
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3de5093f1fa395b1fba061f88a9b67b5dedf4740
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385853"
---
# <a name="pidtagrulelevel-canonical-property"></a><span data-ttu-id="12bc2-103">Каноническое свойство PidTagRuleLevel</span><span class="sxs-lookup"><span data-stu-id="12bc2-103">PidTagRuleLevel Canonical Property</span></span>

  
  
<span data-ttu-id="12bc2-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="12bc2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="12bc2-105">Содержит уровень exit правила.</span><span class="sxs-lookup"><span data-stu-id="12bc2-105">Contains the exit level of a rule.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="12bc2-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="12bc2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="12bc2-107">PR_RULE_LEVEL</span><span class="sxs-lookup"><span data-stu-id="12bc2-107">PR_RULE_LEVEL</span></span>  <br/> |
|<span data-ttu-id="12bc2-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="12bc2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="12bc2-109">0x6683</span><span class="sxs-lookup"><span data-stu-id="12bc2-109">0x6683</span></span>  <br/> |
|<span data-ttu-id="12bc2-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="12bc2-110">Data type:</span></span>  <br/> |<span data-ttu-id="12bc2-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="12bc2-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="12bc2-112">Область:</span><span class="sxs-lookup"><span data-stu-id="12bc2-112">Area:</span></span>  <br/> |<span data-ttu-id="12bc2-113">Правила со стороны сервера</span><span class="sxs-lookup"><span data-stu-id="12bc2-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="12bc2-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="12bc2-114">Remarks</span></span>

<span data-ttu-id="12bc2-115">Если назначить этому свойству, клиент должен проходить в 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="12bc2-115">If setting this property, the client must pass in 0x00000000.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="12bc2-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="12bc2-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="12bc2-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="12bc2-117">Protocol specifications</span></span>

<span data-ttu-id="12bc2-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="12bc2-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="12bc2-119">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="12bc2-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="12bc2-120">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="12bc2-120">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="12bc2-121">Указывает методы для подключений и настройки почтовых ящиков как делегаты и взаимодействия с элементами календаря и сообщения, когда они действовать от имени другого пользователя.</span><span class="sxs-lookup"><span data-stu-id="12bc2-121">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar items when they act on behalf of another user.</span></span>
    
<span data-ttu-id="12bc2-122">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="12bc2-122">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="12bc2-123">Управляет входящие сообщения электронной почты на сервере.</span><span class="sxs-lookup"><span data-stu-id="12bc2-123">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="12bc2-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="12bc2-124">Header files</span></span>

<span data-ttu-id="12bc2-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="12bc2-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="12bc2-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="12bc2-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="12bc2-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="12bc2-127">Mapitags.h</span></span>
  
> <span data-ttu-id="12bc2-128">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="12bc2-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="12bc2-129">См. также</span><span class="sxs-lookup"><span data-stu-id="12bc2-129">See also</span></span>



[<span data-ttu-id="12bc2-130">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="12bc2-130">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)


[<span data-ttu-id="12bc2-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="12bc2-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="12bc2-132">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="12bc2-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="12bc2-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="12bc2-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="12bc2-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="12bc2-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

