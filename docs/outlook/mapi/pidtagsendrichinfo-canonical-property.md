---
title: Каноническое свойство PidTagSendRichInfo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSendRichInfo
api_type:
- COM
ms.assetid: e85fc766-197a-484f-b600-68cd28a052a2
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a7ad27d757d4ed6df58c597bf17d9e5412f83457
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342520"
---
# <a name="pidtagsendrichinfo-canonical-property"></a><span data-ttu-id="986ba-103">Каноническое свойство PidTagSendRichInfo</span><span class="sxs-lookup"><span data-stu-id="986ba-103">PidTagSendRichInfo Canonical Property</span></span>

  
  
<span data-ttu-id="986ba-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="986ba-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="986ba-105">Содержит значение TRUE, если получатель может получать все содержимое сообщений, в том числе объекты в формате RTF и объект OLE.</span><span class="sxs-lookup"><span data-stu-id="986ba-105">Contains TRUE if the recipient can receive all message content, including Rich Text Format (RTF) and Object Linking and Embedding (OLE) objects.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="986ba-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="986ba-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="986ba-107">ПР_СЕНД_РИЧ_ИНФО</span><span class="sxs-lookup"><span data-stu-id="986ba-107">PR_SEND_RICH_INFO</span></span>  <br/> |
|<span data-ttu-id="986ba-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="986ba-108">Identifier:</span></span>  <br/> |<span data-ttu-id="986ba-109">0x3A40</span><span class="sxs-lookup"><span data-stu-id="986ba-109">0x3A40</span></span>  <br/> |
|<span data-ttu-id="986ba-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="986ba-110">Data type:</span></span>  <br/> |<span data-ttu-id="986ba-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="986ba-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="986ba-112">Область:</span><span class="sxs-lookup"><span data-stu-id="986ba-112">Area:</span></span>  <br/> |<span data-ttu-id="986ba-113">Address</span><span class="sxs-lookup"><span data-stu-id="986ba-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="986ba-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="986ba-114">Remarks</span></span>

<span data-ttu-id="986ba-115">Рекомендуется, чтобы объекты пользователей списка рассылки и обмена сообщениями раскрывают это свойство.</span><span class="sxs-lookup"><span data-stu-id="986ba-115">It is recommended that distribution list and messaging user objects expose this property.</span></span> 
  
<span data-ttu-id="986ba-116">Это свойство указывает, считает ли отправитель, что для получателя включена поддержка MAPI.</span><span class="sxs-lookup"><span data-stu-id="986ba-116">This property indicates whether the sender considers the recipient to be MAPI-enabled.</span></span> 
  
<span data-ttu-id="986ba-117">Если для этого свойства задано значение TRUE, транспортный шлюз и шлюз могут передавать все содержимое сообщения, включая объекты RTF и OLE.</span><span class="sxs-lookup"><span data-stu-id="986ba-117">When this property is set to TRUE, the transport and gateway can transmit the full content of the message, including RTF and OLE objects.</span></span> <span data-ttu-id="986ba-118">Поставщик транспорта и шлюз должен использовать формат TNEF для инкапсуляции любых свойств, которые не являются собственными для всех используемых систем обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="986ba-118">The transport provider and gateway should use Transport Neutral Encapsulation Format (TNEF) to encapsulate any properties that are not native to all the messaging systems involved.</span></span> 
  
<span data-ttu-id="986ba-119">Если для этого свойства задано значение FALSE, поставщик транспорта и шлюз не могут удалять содержимое сообщений, которые не могут использоваться собственными клиентами.</span><span class="sxs-lookup"><span data-stu-id="986ba-119">When this property is set to FALSE, the transport provider and gateway are free to discard message content that their native clients cannot use.</span></span> <span data-ttu-id="986ba-120">Например, если клиенты не поддерживают формат RTF, поставщик транспорта может отправлять только обычный текст.</span><span class="sxs-lookup"><span data-stu-id="986ba-120">For example, when the clients do not support RTF, the transport provider can send only plain text.</span></span> 
  
<span data-ttu-id="986ba-121">Если это свойство не задано, поведение по умолчанию определяется реализацией поставщика транспорта, агента передачи сообщений (MTA) или шлюза.</span><span class="sxs-lookup"><span data-stu-id="986ba-121">When this property is not set, default behavior is determined by the implementation of the transport provider, message transfer agent (MTA), or gateway.</span></span> <span data-ttu-id="986ba-122">Для поддержки этого свойства поставщики адресных книг не требуются.</span><span class="sxs-lookup"><span data-stu-id="986ba-122">Address book providers are not required to support this property.</span></span> <span data-ttu-id="986ba-123">Например, жестко связанная адресная книга и поставщик транспорта могут отправить TNEF, но никогда не использовать формат RTF.</span><span class="sxs-lookup"><span data-stu-id="986ba-123">For example, a tightly coupled address book and transport provider can choose to send TNEF but never use RTF.</span></span> 
  
<span data-ttu-id="986ba-124">Клиент не должен предполагать, что поставщик транспорта и шлюз будут использовать TNEF в собственной инициативе.</span><span class="sxs-lookup"><span data-stu-id="986ba-124">The client should not assume the transport provider and gateway will use TNEF on their own initiative.</span></span> <span data-ttu-id="986ba-125">Некоторые поставщики транспорта и шлюзы, поддерживающие TNEF, передают их без учета значения этого свойства, но другие отклоняются для создания или отправки TNEF, если для него не задано значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="986ba-125">Some transport providers and gateways that support TNEF transmit it without regard to the value of this property, but others decline to construct or send TNEF if it is not set to TRUE.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="986ba-126">Параметр этого свойства и решения, основанные на его значении, относятся к отдельному получателю.</span><span class="sxs-lookup"><span data-stu-id="986ba-126">The setting of this property, and the decisions based on its value, are on a per-recipient basis.</span></span> 
  
<span data-ttu-id="986ba-127">По умолчанию MAPI устанавливает значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="986ba-127">By default, MAPI sets the value to TRUE.</span></span> <span data-ttu-id="986ba-128">Клиент вызывает [IAddrBook:: креатеонеофф](iaddrbook-createoneoff.md) или поставщик, вызывающий [Имаписуппорт:: креатеонеофф](imapisupport-createoneoff.md) может установить бит **мапи_сенд_но_рич_инфо** в параметре _ulFlags_ , что приводит к тому, что MAPI устанавливает для этого свойства значение false.</span><span class="sxs-lookup"><span data-stu-id="986ba-128">A client calling [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) or a provider calling [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md) can set the **MAPI_SEND_NO_RICH_INFO** bit in the  _ulFlags_ parameter, which causes MAPI to set this property to FALSE.</span></span> <span data-ttu-id="986ba-129">Односторонние свойства, созданные в пользовательском интерфейсе, используют значение, заданное при создании шаблона.</span><span class="sxs-lookup"><span data-stu-id="986ba-129">One-offs created by the user interface use the value specified by the creating template.</span></span> 
  
<span data-ttu-id="986ba-130">При вызове метода [IAddrBook:: ресолвенаме](iaddrbook-resolvename.md) , когда имя не удается разрешить, но может интерпретироваться как адрес в Интернете (SMTP), этому свойству присваиваетСЯ значение false.</span><span class="sxs-lookup"><span data-stu-id="986ba-130">On calls to the [IAddrBook::ResolveName](iaddrbook-resolvename.md) method when the name cannot be resolved but can be interpreted as an Internet address (SMTP), this property is set to FALSE.</span></span> <span data-ttu-id="986ba-131">Если вы хотите использовать адрес в Интернете, отображаемое имя неразрешенной записи должно быть в формате X @ Y. Z, например "pete@pinecone.com".</span><span class="sxs-lookup"><span data-stu-id="986ba-131">To be construed as an Internet address, the display name of the unresolved entry must be in the format X@Y.Z, such as "pete@pinecone.com".</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="986ba-132">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="986ba-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="986ba-133">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="986ba-133">Protocol specifications</span></span>

<span data-ttu-id="986ba-134">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="986ba-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="986ba-135">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="986ba-135">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="986ba-136">[[MS — ОКСОАБК]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="986ba-136">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="986ba-137">Задает свойства и операции для списков пользователей, контактов, групп и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="986ba-137">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="986ba-138">[[MS — ОКСОМСГ]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="986ba-138">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="986ba-139">Задает свойства и операции, допустимые для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="986ba-139">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="986ba-140">[[MS — ОКСКМАИЛ]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="986ba-140">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="986ba-141">из Интернета стандартные правила электронной почты для объектов сообщений.</span><span class="sxs-lookup"><span data-stu-id="986ba-141">from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="986ba-142">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="986ba-142">Header files</span></span>

<span data-ttu-id="986ba-143">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="986ba-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="986ba-144">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="986ba-144">Provides data type definitions.</span></span>
    
<span data-ttu-id="986ba-145">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="986ba-145">Mapitags.h</span></span>
  
> <span data-ttu-id="986ba-146">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="986ba-146">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="986ba-147">См. также</span><span class="sxs-lookup"><span data-stu-id="986ba-147">See also</span></span>



[<span data-ttu-id="986ba-148">Каноническое свойство PidTagAttachDataObject</span><span class="sxs-lookup"><span data-stu-id="986ba-148">PidTagAttachDataObject Canonical Property</span></span>](pidtagattachdataobject-canonical-property.md)


[<span data-ttu-id="986ba-149">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="986ba-149">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="986ba-150">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="986ba-150">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="986ba-151">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="986ba-151">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="986ba-152">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="986ba-152">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

