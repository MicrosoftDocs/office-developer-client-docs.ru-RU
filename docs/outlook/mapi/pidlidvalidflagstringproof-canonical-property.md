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
ms.openlocfilehash: 90f16f33e7e116e124384f9988c0c7dddaad2da5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810667"
---
# <a name="pidlidvalidflagstringproof-canonical-property"></a><span data-ttu-id="d8542-103">Каноническое свойство PidLidValidFlagStringProof</span><span class="sxs-lookup"><span data-stu-id="d8542-103">PidLidValidFlagStringProof Canonical Property</span></span>

  
  
<span data-ttu-id="d8542-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d8542-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d8542-105">Проверяет, является ли было задано значение свойства **dispidRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) по агенту, который знала, значение свойства **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d8542-105">Validates whether the **dispidRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) property's value was set by an agent who knew the value of the **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d8542-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="d8542-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d8542-107">dispidValidFlagStringProof</span><span class="sxs-lookup"><span data-stu-id="d8542-107">dispidValidFlagStringProof</span></span>  <br/> |
|<span data-ttu-id="d8542-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="d8542-108">Property set:</span></span>  <br/> |<span data-ttu-id="d8542-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="d8542-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="d8542-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="d8542-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="d8542-111">0x000085BF</span><span class="sxs-lookup"><span data-stu-id="d8542-111">0x000085BF</span></span>  <br/> |
|<span data-ttu-id="d8542-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="d8542-112">Data type:</span></span>  <br/> |<span data-ttu-id="d8542-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="d8542-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="d8542-114">Область:</span><span class="sxs-lookup"><span data-stu-id="d8542-114">Area:</span></span>  <br/> |<span data-ttu-id="d8542-115">Task</span><span class="sxs-lookup"><span data-stu-id="d8542-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d8542-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="d8542-116">Remarks</span></span>

<span data-ttu-id="d8542-117">Не отправляемого объектов (полученной почты и не содержащие почту объекты) клиенты должны присвойте этому параметру значение значение **PR_MESSAGE_DELIVERY_TIME** при изменении **dispidRequest**.</span><span class="sxs-lookup"><span data-stu-id="d8542-117">On non-sendable objects (received mail and non-mail objects), clients should set this value to the value of **PR_MESSAGE_DELIVERY_TIME** when modifying **dispidRequest**.</span></span>
  
<span data-ttu-id="d8542-118">Так как значение **PR_MESSAGE_DELIVERY_TIME** непредсказуемым образом отправителем, если значение этого свойства равно значению **PR_MESSAGE_DELIVERY_TIME**, это уверенность, что значение **dispidRequest** не поступают от отправителя сообщения.</span><span class="sxs-lookup"><span data-stu-id="d8542-118">Since the value of **PR_MESSAGE_DELIVERY_TIME** cannot be predicted by the sender, if the value of this property is equal to the value of **PR_MESSAGE_DELIVERY_TIME**, it is reasonably certain that the value of **dispidRequest** did not originate from the sender of the message.</span></span> <span data-ttu-id="d8542-119">Клиент может решить, как бы представить значение **dispidRequest** конечного пользователя, на основе результатов этого сравнения в соответствии с политикой безопасности клиента.</span><span class="sxs-lookup"><span data-stu-id="d8542-119">A client can decide how to present the value of **dispidRequest** to the end user based on the result of this comparison in accordance with the specific security policy of the client.</span></span> <span data-ttu-id="d8542-120">Если значение **dispidRequest** игнорируется из-за наличия значение для **dispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)), это свойство должны игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="d8542-120">If the value of **dispidRequest** is ignored due to the presence of a value for **dispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)), this property must be ignored.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d8542-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d8542-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d8542-122">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="d8542-122">Protocol specifications</span></span>

<span data-ttu-id="d8542-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d8542-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d8542-124">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="d8542-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d8542-125">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d8542-125">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d8542-126">Задает свойства и операции, связанные с флагов.</span><span class="sxs-lookup"><span data-stu-id="d8542-126">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d8542-127">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="d8542-127">Header files</span></span>

<span data-ttu-id="d8542-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d8542-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="d8542-129">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="d8542-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d8542-130">См. также</span><span class="sxs-lookup"><span data-stu-id="d8542-130">See also</span></span>



[<span data-ttu-id="d8542-131">Каноническое свойство PidTagMessageDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="d8542-131">PidTagMessageDeliveryTime Canonical Property</span></span>](pidtagmessagedeliverytime-canonical-property.md)


[<span data-ttu-id="d8542-132">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d8542-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d8542-133">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d8542-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d8542-134">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="d8542-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d8542-135">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="d8542-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

