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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386441"
---
# <a name="pidtagsendrichinfo-canonical-property"></a><span data-ttu-id="d42a5-103">Каноническое свойство PidTagSendRichInfo</span><span class="sxs-lookup"><span data-stu-id="d42a5-103">PidTagSendRichInfo Canonical Property</span></span>

  
  
<span data-ttu-id="d42a5-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d42a5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d42a5-105">Содержит значение TRUE, если получатель может получать все содержимое сообщения, включая форматированный текст (RTF) и объектов внедрения (OLE).</span><span class="sxs-lookup"><span data-stu-id="d42a5-105">Contains TRUE if the recipient can receive all message content, including Rich Text Format (RTF) and Object Linking and Embedding (OLE) objects.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d42a5-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="d42a5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d42a5-107">PR_SEND_RICH_INFO</span><span class="sxs-lookup"><span data-stu-id="d42a5-107">PR_SEND_RICH_INFO</span></span>  <br/> |
|<span data-ttu-id="d42a5-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="d42a5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d42a5-109">0x3A40</span><span class="sxs-lookup"><span data-stu-id="d42a5-109">0x3A40</span></span>  <br/> |
|<span data-ttu-id="d42a5-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="d42a5-110">Data type:</span></span>  <br/> |<span data-ttu-id="d42a5-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="d42a5-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="d42a5-112">Область:</span><span class="sxs-lookup"><span data-stu-id="d42a5-112">Area:</span></span>  <br/> |<span data-ttu-id="d42a5-113">Address</span><span class="sxs-lookup"><span data-stu-id="d42a5-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d42a5-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="d42a5-114">Remarks</span></span>

<span data-ttu-id="d42a5-115">Список рассылки и системы обмена сообщениями объектов-пользователей предоставляют доступ к это свойство рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="d42a5-115">It is recommended that distribution list and messaging user objects expose this property.</span></span> 
  
<span data-ttu-id="d42a5-116">Это свойство указывает, учитывает ли отправителя получателю быть MAPI-совместимый.</span><span class="sxs-lookup"><span data-stu-id="d42a5-116">This property indicates whether the sender considers the recipient to be MAPI-enabled.</span></span> 
  
<span data-ttu-id="d42a5-117">Когда это свойство имеет значение TRUE, транспортный сервер и шлюз может передавать всего содержимого сообщения, включая объекты OLE и формат RTF.</span><span class="sxs-lookup"><span data-stu-id="d42a5-117">When this property is set to TRUE, the transport and gateway can transmit the full content of the message, including RTF and OLE objects.</span></span> <span data-ttu-id="d42a5-118">Поставщик транспорта и шлюза следует использовать транспорта Neutral Encapsulation формата TNEF для инкапсуляции любые свойства, которые не являются всех систем обмена сообщениями участвующих в определенном.</span><span class="sxs-lookup"><span data-stu-id="d42a5-118">The transport provider and gateway should use Transport Neutral Encapsulation Format (TNEF) to encapsulate any properties that are not native to all the messaging systems involved.</span></span> 
  
<span data-ttu-id="d42a5-119">Если это свойство установлено значение FALSE, поставщика транспорта и шлюза могут отменить содержимое сообщения, не могут использовать свои собственные клиентов.</span><span class="sxs-lookup"><span data-stu-id="d42a5-119">When this property is set to FALSE, the transport provider and gateway are free to discard message content that their native clients cannot use.</span></span> <span data-ttu-id="d42a5-120">Например если клиенты не поддерживают формат RTF, поставщика транспорта можно отправить только обычный текст.</span><span class="sxs-lookup"><span data-stu-id="d42a5-120">For example, when the clients do not support RTF, the transport provider can send only plain text.</span></span> 
  
<span data-ttu-id="d42a5-121">Если это свойство не задано, по умолчанию определяется реализации поставщика транспорта, передачи сообщений (агента) или шлюз.</span><span class="sxs-lookup"><span data-stu-id="d42a5-121">When this property is not set, default behavior is determined by the implementation of the transport provider, message transfer agent (MTA), or gateway.</span></span> <span data-ttu-id="d42a5-122">Поставщиками адресной книги не требуется для поддержки этого свойства.</span><span class="sxs-lookup"><span data-stu-id="d42a5-122">Address book providers are not required to support this property.</span></span> <span data-ttu-id="d42a5-123">Например тесно связанных адресной книги и транспорта поставщика можно отправить TNEF, но никогда не использовать формат RTF.</span><span class="sxs-lookup"><span data-stu-id="d42a5-123">For example, a tightly coupled address book and transport provider can choose to send TNEF but never use RTF.</span></span> 
  
<span data-ttu-id="d42a5-124">Клиент не должен принимать поставщика транспорта и шлюз будет использовать TNEF на собственные работ по проекту.</span><span class="sxs-lookup"><span data-stu-id="d42a5-124">The client should not assume the transport provider and gateway will use TNEF on their own initiative.</span></span> <span data-ttu-id="d42a5-125">Некоторые поставщики транспорта и шлюзов, которые поддерживают TNEF передачи его независимо от значения этого свойства, но другие пользователи отклонение для создания или отправки TNEF, если оно не установлено значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="d42a5-125">Some transport providers and gateways that support TNEF transmit it without regard to the value of this property, but others decline to construct or send TNEF if it is not set to TRUE.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="d42a5-126">Отдельно для каждого получателя, значения этого свойства и решения, основываясь на его значение.</span><span class="sxs-lookup"><span data-stu-id="d42a5-126">The setting of this property, and the decisions based on its value, are on a per-recipient basis.</span></span> 
  
<span data-ttu-id="d42a5-127">По умолчанию MAPI задается значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="d42a5-127">By default, MAPI sets the value to TRUE.</span></span> <span data-ttu-id="d42a5-128">Клиента, вызывающего [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) или поставщика, вызов [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md) можно установить бит **MAPI_SEND_NO_RICH_INFO** в параметре _ulFlags_ , что активирует MAPI к этому свойству присвоено значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="d42a5-128">A client calling [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) or a provider calling [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md) can set the **MAPI_SEND_NO_RICH_INFO** bit in the  _ulFlags_ parameter, which causes MAPI to set this property to FALSE.</span></span> <span data-ttu-id="d42a5-129">One-offs, созданных с помощью пользовательского интерфейса используйте значение, указанное для создания шаблона.</span><span class="sxs-lookup"><span data-stu-id="d42a5-129">One-offs created by the user interface use the value specified by the creating template.</span></span> 
  
<span data-ttu-id="d42a5-130">На вызовы метода [IAddrBook::ResolveName](iaddrbook-resolvename.md) при не удается разрешить имя, но могут обрабатываться как адрес Интернета (SMTP), это свойство задано значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="d42a5-130">On calls to the [IAddrBook::ResolveName](iaddrbook-resolvename.md) method when the name cannot be resolved but can be interpreted as an Internet address (SMTP), this property is set to FALSE.</span></span> <span data-ttu-id="d42a5-131">Чтобы рассматриваться как адрес в Интернете, отображаемое имя нерешенные записи должно быть в формате X@Y. Z, например «pete@pinecone.com».</span><span class="sxs-lookup"><span data-stu-id="d42a5-131">To be construed as an Internet address, the display name of the unresolved entry must be in the format X@Y.Z, such as "pete@pinecone.com".</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d42a5-132">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d42a5-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d42a5-133">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="d42a5-133">Protocol specifications</span></span>

<span data-ttu-id="d42a5-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d42a5-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d42a5-135">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="d42a5-135">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d42a5-136">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d42a5-136">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d42a5-137">Задает свойства и операции для списков пользователей, контактов, групп и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d42a5-137">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="d42a5-138">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d42a5-138">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d42a5-139">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="d42a5-139">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="d42a5-140">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d42a5-140">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d42a5-141">из соглашения о стандартных электронной почты Интернета для сообщения объектов.</span><span class="sxs-lookup"><span data-stu-id="d42a5-141">from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d42a5-142">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="d42a5-142">Header files</span></span>

<span data-ttu-id="d42a5-143">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d42a5-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="d42a5-144">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="d42a5-144">Provides data type definitions.</span></span>
    
<span data-ttu-id="d42a5-145">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d42a5-145">Mapitags.h</span></span>
  
> <span data-ttu-id="d42a5-146">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="d42a5-146">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d42a5-147">См. также</span><span class="sxs-lookup"><span data-stu-id="d42a5-147">See also</span></span>



[<span data-ttu-id="d42a5-148">Каноническое свойство PidTagAttachDataObject</span><span class="sxs-lookup"><span data-stu-id="d42a5-148">PidTagAttachDataObject Canonical Property</span></span>](pidtagattachdataobject-canonical-property.md)


[<span data-ttu-id="d42a5-149">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d42a5-149">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d42a5-150">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d42a5-150">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d42a5-151">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="d42a5-151">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d42a5-152">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="d42a5-152">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

