---
title: Каноническое свойство PidLidValidFlagStringProof
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidValidFlagStringProof
api_type:
- COM
ms.assetid: e5a94968-7e84-4faf-8104-9ea36d35fa1a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: dfe3b57c246e247eda365bed46af2e0f35f0e54b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315388"
---
# <a name="pidlidvalidflagstringproof-canonical-property"></a><span data-ttu-id="3919e-103">Каноническое свойство PidLidValidFlagStringProof</span><span class="sxs-lookup"><span data-stu-id="3919e-103">PidLidValidFlagStringProof Canonical Property</span></span>

  
  
<span data-ttu-id="3919e-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3919e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3919e-105">Проверяет, было ли значение свойства **диспидрекуест** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) задано агентом, который знал значение свойства **пр_мессаже_деливери_тиме** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="3919e-105">Validates whether the **dispidRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) property's value was set by an agent who knew the value of the **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3919e-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="3919e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3919e-107">Диспидвалидфлагстрингпруф</span><span class="sxs-lookup"><span data-stu-id="3919e-107">dispidValidFlagStringProof</span></span>  <br/> |
|<span data-ttu-id="3919e-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="3919e-108">Property set:</span></span>  <br/> |<span data-ttu-id="3919e-109">Псетид_коммон</span><span class="sxs-lookup"><span data-stu-id="3919e-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="3919e-110">Длинный идентификатор (крышка):</span><span class="sxs-lookup"><span data-stu-id="3919e-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="3919e-111">0x000085BF</span><span class="sxs-lookup"><span data-stu-id="3919e-111">0x000085BF</span></span>  <br/> |
|<span data-ttu-id="3919e-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="3919e-112">Data type:</span></span>  <br/> |<span data-ttu-id="3919e-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="3919e-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="3919e-114">Область:</span><span class="sxs-lookup"><span data-stu-id="3919e-114">Area:</span></span>  <br/> |<span data-ttu-id="3919e-115">Задача</span><span class="sxs-lookup"><span data-stu-id="3919e-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3919e-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="3919e-116">Remarks</span></span>

<span data-ttu-id="3919e-117">Для объектов, не относящихся к отправке (получены почтовые сообщения и объекты, не являющиеся сообщениями), при изменении **диспидрекуест**клиенты должны задать для этого параметра значение **пр_мессаже_деливери_тиме** .</span><span class="sxs-lookup"><span data-stu-id="3919e-117">On non-sendable objects (received mail and non-mail objects), clients should set this value to the value of **PR_MESSAGE_DELIVERY_TIME** when modifying **dispidRequest**.</span></span>
  
<span data-ttu-id="3919e-118">Так как значение **пр_мессаже_деливери_тиме** не может быть предсказано отправителем, если значение этого свойства равно значению **пр_мессаже_деливери_тиме**, то разумно убедиться, что значение **диспидрекуест** не исходит от отправителя сообщения.</span><span class="sxs-lookup"><span data-stu-id="3919e-118">Since the value of **PR_MESSAGE_DELIVERY_TIME** cannot be predicted by the sender, if the value of this property is equal to the value of **PR_MESSAGE_DELIVERY_TIME**, it is reasonably certain that the value of **dispidRequest** did not originate from the sender of the message.</span></span> <span data-ttu-id="3919e-119">Клиент может принять решение о том, как предоставить конечному пользователю значение **диспидрекуест** на основании результатов этого сравнения в соответствии с определенной политикой безопасности клиента.</span><span class="sxs-lookup"><span data-stu-id="3919e-119">A client can decide how to present the value of **dispidRequest** to the end user based on the result of this comparison in accordance with the specific security policy of the client.</span></span> <span data-ttu-id="3919e-120">Если значение **диспидрекуест** игнорируется из-за наличия значения для **диспидфлагстринженум** ([PidLidFlagString](pidlidflagstring-canonical-property.md)), это свойство необходимо игнорировать.</span><span class="sxs-lookup"><span data-stu-id="3919e-120">If the value of **dispidRequest** is ignored due to the presence of a value for **dispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)), this property must be ignored.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3919e-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="3919e-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3919e-122">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="3919e-122">Protocol specifications</span></span>

<span data-ttu-id="3919e-123">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3919e-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3919e-124">Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="3919e-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3919e-125">[[MS — ОКСОФЛАГ]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3919e-125">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3919e-126">Задает свойства и операции, связанные с пометкой.</span><span class="sxs-lookup"><span data-stu-id="3919e-126">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3919e-127">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="3919e-127">Header files</span></span>

<span data-ttu-id="3919e-128">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="3919e-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="3919e-129">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="3919e-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3919e-130">См. также</span><span class="sxs-lookup"><span data-stu-id="3919e-130">See also</span></span>



[<span data-ttu-id="3919e-131">Каноническое свойство PidTagMessageDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="3919e-131">PidTagMessageDeliveryTime Canonical Property</span></span>](pidtagmessagedeliverytime-canonical-property.md)


[<span data-ttu-id="3919e-132">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="3919e-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3919e-133">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="3919e-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3919e-134">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="3919e-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3919e-135">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="3919e-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

