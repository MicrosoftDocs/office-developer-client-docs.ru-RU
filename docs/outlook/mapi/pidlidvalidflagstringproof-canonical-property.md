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
# <a name="pidlidvalidflagstringproof-canonical-property"></a><span data-ttu-id="aa168-103">Каноническое свойство PidLidValidFlagStringProof</span><span class="sxs-lookup"><span data-stu-id="aa168-103">PidLidValidFlagStringProof Canonical Property</span></span>

  
  
<span data-ttu-id="aa168-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aa168-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aa168-105">Проверяет, задавало ли значение свойства **dispidRequest** ([PidLidFlagRequest)](pidlidflagrequest-canonical-property.md)агентом, который знал значение свойства **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime).](pidtagmessagedeliverytime-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="aa168-105">Validates whether the **dispidRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) property's value was set by an agent who knew the value of the **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="aa168-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="aa168-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="aa168-107">dispidValidFlagStringProof</span><span class="sxs-lookup"><span data-stu-id="aa168-107">dispidValidFlagStringProof</span></span>  <br/> |
|<span data-ttu-id="aa168-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="aa168-108">Property set:</span></span>  <br/> |<span data-ttu-id="aa168-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="aa168-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="aa168-110">Длинный ИД (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="aa168-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="aa168-111">0x000085BF</span><span class="sxs-lookup"><span data-stu-id="aa168-111">0x000085BF</span></span>  <br/> |
|<span data-ttu-id="aa168-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="aa168-112">Data type:</span></span>  <br/> |<span data-ttu-id="aa168-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="aa168-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="aa168-114">Область:</span><span class="sxs-lookup"><span data-stu-id="aa168-114">Area:</span></span>  <br/> |<span data-ttu-id="aa168-115">Task</span><span class="sxs-lookup"><span data-stu-id="aa168-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="aa168-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="aa168-116">Remarks</span></span>

<span data-ttu-id="aa168-117">Для объектов, не отправляемых (полученных и не отправляемых объектов), клиенты должны установить для этого значения значение **PR_MESSAGE_DELIVERY_TIME** при изменении **dispidRequest.**</span><span class="sxs-lookup"><span data-stu-id="aa168-117">On non-sendable objects (received mail and non-mail objects), clients should set this value to the value of **PR_MESSAGE_DELIVERY_TIME** when modifying **dispidRequest**.</span></span>
  
<span data-ttu-id="aa168-118">Так как  значение PR_MESSAGE_DELIVERY_TIME не может быть предугадать отправитель, если значение этого свойства равно значению **PR_MESSAGE_DELIVERY_TIME,** то вполне возможно, что значение **dispidRequest** не было исходят от отправитель сообщения.</span><span class="sxs-lookup"><span data-stu-id="aa168-118">Since the value of **PR_MESSAGE_DELIVERY_TIME** cannot be predicted by the sender, if the value of this property is equal to the value of **PR_MESSAGE_DELIVERY_TIME**, it is reasonably certain that the value of **dispidRequest** did not originate from the sender of the message.</span></span> <span data-ttu-id="aa168-119">Клиент может решить, как представить значение **dispidRequest** конечному пользователю на основе результатов этого сравнения в соответствии с определенной политикой безопасности клиента.</span><span class="sxs-lookup"><span data-stu-id="aa168-119">A client can decide how to present the value of **dispidRequest** to the end user based on the result of this comparison in accordance with the specific security policy of the client.</span></span> <span data-ttu-id="aa168-120">Если значение **dispidRequest** игнорируется из-за наличия значения **для dispidFlagStringEnum** ([PidLidFlagString),](pidlidflagstring-canonical-property.md)это свойство должно быть проигнорировано.</span><span class="sxs-lookup"><span data-stu-id="aa168-120">If the value of **dispidRequest** is ignored due to the presence of a value for **dispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)), this property must be ignored.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="aa168-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="aa168-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="aa168-122">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="aa168-122">Protocol specifications</span></span>

<span data-ttu-id="aa168-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aa168-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="aa168-124">Предоставляет определения набора свойств и ссылки на связанные Exchange Server спецификации протокола.</span><span class="sxs-lookup"><span data-stu-id="aa168-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="aa168-125">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aa168-125">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="aa168-126">Указывает свойства и операции, связанные с помезданием.</span><span class="sxs-lookup"><span data-stu-id="aa168-126">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="aa168-127">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="aa168-127">Header files</span></span>

<span data-ttu-id="aa168-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="aa168-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="aa168-129">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="aa168-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="aa168-130">См. также</span><span class="sxs-lookup"><span data-stu-id="aa168-130">See also</span></span>



[<span data-ttu-id="aa168-131">Каноническое свойство PidTagMessageDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="aa168-131">PidTagMessageDeliveryTime Canonical Property</span></span>](pidtagmessagedeliverytime-canonical-property.md)


[<span data-ttu-id="aa168-132">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="aa168-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="aa168-133">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="aa168-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="aa168-134">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="aa168-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="aa168-135">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="aa168-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

