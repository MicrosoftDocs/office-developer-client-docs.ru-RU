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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391957"
---
# <a name="pidlidvalidflagstringproof-canonical-property"></a><span data-ttu-id="a5414-103">Каноническое свойство PidLidValidFlagStringProof</span><span class="sxs-lookup"><span data-stu-id="a5414-103">PidLidValidFlagStringProof Canonical Property</span></span>

  
  
<span data-ttu-id="a5414-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a5414-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a5414-105">Проверяет, является ли было задано значение свойства **dispidRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) по агенту, который знала, значение свойства **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a5414-105">Validates whether the **dispidRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) property's value was set by an agent who knew the value of the **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a5414-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="a5414-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a5414-107">dispidValidFlagStringProof</span><span class="sxs-lookup"><span data-stu-id="a5414-107">dispidValidFlagStringProof</span></span>  <br/> |
|<span data-ttu-id="a5414-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="a5414-108">Property set:</span></span>  <br/> |<span data-ttu-id="a5414-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="a5414-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="a5414-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="a5414-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="a5414-111">0x000085BF</span><span class="sxs-lookup"><span data-stu-id="a5414-111">0x000085BF</span></span>  <br/> |
|<span data-ttu-id="a5414-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="a5414-112">Data type:</span></span>  <br/> |<span data-ttu-id="a5414-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="a5414-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="a5414-114">Область:</span><span class="sxs-lookup"><span data-stu-id="a5414-114">Area:</span></span>  <br/> |<span data-ttu-id="a5414-115">Task</span><span class="sxs-lookup"><span data-stu-id="a5414-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a5414-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="a5414-116">Remarks</span></span>

<span data-ttu-id="a5414-117">Не отправляемого объектов (полученной почты и не содержащие почту объекты) клиенты должны присвойте этому параметру значение значение **PR_MESSAGE_DELIVERY_TIME** при изменении **dispidRequest**.</span><span class="sxs-lookup"><span data-stu-id="a5414-117">On non-sendable objects (received mail and non-mail objects), clients should set this value to the value of **PR_MESSAGE_DELIVERY_TIME** when modifying **dispidRequest**.</span></span>
  
<span data-ttu-id="a5414-118">Так как значение **PR_MESSAGE_DELIVERY_TIME** непредсказуемым образом отправителем, если значение этого свойства равно значению **PR_MESSAGE_DELIVERY_TIME**, это уверенность, что значение **dispidRequest** не поступают от отправителя сообщения.</span><span class="sxs-lookup"><span data-stu-id="a5414-118">Since the value of **PR_MESSAGE_DELIVERY_TIME** cannot be predicted by the sender, if the value of this property is equal to the value of **PR_MESSAGE_DELIVERY_TIME**, it is reasonably certain that the value of **dispidRequest** did not originate from the sender of the message.</span></span> <span data-ttu-id="a5414-119">Клиент может решить, как бы представить значение **dispidRequest** конечного пользователя, на основе результатов этого сравнения в соответствии с политикой безопасности клиента.</span><span class="sxs-lookup"><span data-stu-id="a5414-119">A client can decide how to present the value of **dispidRequest** to the end user based on the result of this comparison in accordance with the specific security policy of the client.</span></span> <span data-ttu-id="a5414-120">Если значение **dispidRequest** игнорируется из-за наличия значение для **dispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)), это свойство должны игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="a5414-120">If the value of **dispidRequest** is ignored due to the presence of a value for **dispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)), this property must be ignored.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a5414-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="a5414-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a5414-122">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="a5414-122">Protocol specifications</span></span>

<span data-ttu-id="a5414-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a5414-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a5414-124">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="a5414-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a5414-125">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a5414-125">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a5414-126">Задает свойства и операции, связанные с флагов.</span><span class="sxs-lookup"><span data-stu-id="a5414-126">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a5414-127">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="a5414-127">Header files</span></span>

<span data-ttu-id="a5414-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a5414-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="a5414-129">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="a5414-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a5414-130">См. также</span><span class="sxs-lookup"><span data-stu-id="a5414-130">See also</span></span>



[<span data-ttu-id="a5414-131">Каноническое свойство PidTagMessageDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="a5414-131">PidTagMessageDeliveryTime Canonical Property</span></span>](pidtagmessagedeliverytime-canonical-property.md)


[<span data-ttu-id="a5414-132">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a5414-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a5414-133">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a5414-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a5414-134">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="a5414-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a5414-135">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="a5414-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

