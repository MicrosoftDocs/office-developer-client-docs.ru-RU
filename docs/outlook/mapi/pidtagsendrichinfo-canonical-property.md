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
# <a name="pidtagsendrichinfo-canonical-property"></a><span data-ttu-id="ad8ba-103">Каноническое свойство PidTagSendRichInfo</span><span class="sxs-lookup"><span data-stu-id="ad8ba-103">PidTagSendRichInfo Canonical Property</span></span>

  
  
<span data-ttu-id="ad8ba-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ad8ba-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ad8ba-105">Содержит true, если получатель может получить все содержимое сообщения, в том числе объекты RTF и объекты OLE.</span><span class="sxs-lookup"><span data-stu-id="ad8ba-105">Contains TRUE if the recipient can receive all message content, including Rich Text Format (RTF) and Object Linking and Embedding (OLE) objects.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ad8ba-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="ad8ba-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ad8ba-107">PR_SEND_RICH_INFO</span><span class="sxs-lookup"><span data-stu-id="ad8ba-107">PR_SEND_RICH_INFO</span></span>  <br/> |
|<span data-ttu-id="ad8ba-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="ad8ba-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ad8ba-109">0x3A40</span><span class="sxs-lookup"><span data-stu-id="ad8ba-109">0x3A40</span></span>  <br/> |
|<span data-ttu-id="ad8ba-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="ad8ba-110">Data type:</span></span>  <br/> |<span data-ttu-id="ad8ba-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="ad8ba-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="ad8ba-112">Область:</span><span class="sxs-lookup"><span data-stu-id="ad8ba-112">Area:</span></span>  <br/> |<span data-ttu-id="ad8ba-113">Address</span><span class="sxs-lookup"><span data-stu-id="ad8ba-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ad8ba-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="ad8ba-114">Remarks</span></span>

<span data-ttu-id="ad8ba-115">Рекомендуется, чтобы список рассылки и объекты пользователей сообщений выдали это свойство.</span><span class="sxs-lookup"><span data-stu-id="ad8ba-115">It is recommended that distribution list and messaging user objects expose this property.</span></span> 
  
<span data-ttu-id="ad8ba-116">Это свойство указывает, считает ли отправитель получателя включенным MAPI.</span><span class="sxs-lookup"><span data-stu-id="ad8ba-116">This property indicates whether the sender considers the recipient to be MAPI-enabled.</span></span> 
  
<span data-ttu-id="ad8ba-117">Если для этого свойства установлено true, транспорт и шлюз могут передавать все содержимое сообщения, включая объекты RTF и OLE.</span><span class="sxs-lookup"><span data-stu-id="ad8ba-117">When this property is set to TRUE, the transport and gateway can transmit the full content of the message, including RTF and OLE objects.</span></span> <span data-ttu-id="ad8ba-118">Поставщик транспорта и шлюз должны использовать формат TNEF для инкапсуляции всех свойств, которые не являются входными для всех систем обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="ad8ba-118">The transport provider and gateway should use Transport Neutral Encapsulation Format (TNEF) to encapsulate any properties that are not native to all the messaging systems involved.</span></span> 
  
<span data-ttu-id="ad8ba-119">Если для этого свойства установлено false, поставщик транспорта и шлюз могут отменить содержимое сообщений, которое их собственные клиенты не могут использовать.</span><span class="sxs-lookup"><span data-stu-id="ad8ba-119">When this property is set to FALSE, the transport provider and gateway are free to discard message content that their native clients cannot use.</span></span> <span data-ttu-id="ad8ba-120">Например, если клиенты не поддерживают RTF, поставщик транспорта может отправлять только обычный текст.</span><span class="sxs-lookup"><span data-stu-id="ad8ba-120">For example, when the clients do not support RTF, the transport provider can send only plain text.</span></span> 
  
<span data-ttu-id="ad8ba-121">Если это свойство не установлено, поведение по умолчанию определяется реализацией поставщика транспорта, агента передачи сообщений (MTA) или шлюза.</span><span class="sxs-lookup"><span data-stu-id="ad8ba-121">When this property is not set, default behavior is determined by the implementation of the transport provider, message transfer agent (MTA), or gateway.</span></span> <span data-ttu-id="ad8ba-122">Поставщики адресных книг не требуются для поддержки этого свойства.</span><span class="sxs-lookup"><span data-stu-id="ad8ba-122">Address book providers are not required to support this property.</span></span> <span data-ttu-id="ad8ba-123">Например, тесно тесная адресная книга и поставщик транспорта могут выбрать отправку TNEF, но никогда не использовать RTF.</span><span class="sxs-lookup"><span data-stu-id="ad8ba-123">For example, a tightly coupled address book and transport provider can choose to send TNEF but never use RTF.</span></span> 
  
<span data-ttu-id="ad8ba-124">Клиент не должен предполагать, что поставщик транспорта и шлюз будут использовать TNEF по собственной инициативе.</span><span class="sxs-lookup"><span data-stu-id="ad8ba-124">The client should not assume the transport provider and gateway will use TNEF on their own initiative.</span></span> <span data-ttu-id="ad8ba-125">Некоторые поставщики транспорта и шлюзы, которые поддерживают TNEF, передают его безототно в отношении значения этого свойства, но другие отклоают создание или отправку TNEF, если для него не установлено значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="ad8ba-125">Some transport providers and gateways that support TNEF transmit it without regard to the value of this property, but others decline to construct or send TNEF if it is not set to TRUE.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="ad8ba-126">Параметр этого свойства и решения, основанные на его значении, настраиваются для каждого получателя.</span><span class="sxs-lookup"><span data-stu-id="ad8ba-126">The setting of this property, and the decisions based on its value, are on a per-recipient basis.</span></span> 
  
<span data-ttu-id="ad8ba-127">По умолчанию MAPI устанавливает значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="ad8ba-127">By default, MAPI sets the value to TRUE.</span></span> <span data-ttu-id="ad8ba-128">Клиент, вызывающий [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) или поставщик, вызывающий [IMAPISupport::CreateOneOff,](imapisupport-createoneoff.md) может установить бит **MAPI_SEND_NO_RICH_INFO** в параметре  _ulFlags,_ в результате чего MAPI задает для этого свойства false.</span><span class="sxs-lookup"><span data-stu-id="ad8ba-128">A client calling [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) or a provider calling [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md) can set the **MAPI_SEND_NO_RICH_INFO** bit in the  _ulFlags_ parameter, which causes MAPI to set this property to FALSE.</span></span> <span data-ttu-id="ad8ba-129">Одновключицы, созданные пользовательским интерфейсом, используют значение, указанное в шаблоне создания.</span><span class="sxs-lookup"><span data-stu-id="ad8ba-129">One-offs created by the user interface use the value specified by the creating template.</span></span> 
  
<span data-ttu-id="ad8ba-130">При вызове метода [IAddrBook::ResolveName,](iaddrbook-resolvename.md) когда имя не может быть разрешено, но может интерпретироваться как АДРЕС Интернета (SMTP), этому свойству задается false.</span><span class="sxs-lookup"><span data-stu-id="ad8ba-130">On calls to the [IAddrBook::ResolveName](iaddrbook-resolvename.md) method when the name cannot be resolved but can be interpreted as an Internet address (SMTP), this property is set to FALSE.</span></span> <span data-ttu-id="ad8ba-131">Чтобы его можно было рассматривать как адрес Интернета, отображаемая запись должна иметь формат X@Y. Z, например "pete@pinecone.com".</span><span class="sxs-lookup"><span data-stu-id="ad8ba-131">To be construed as an Internet address, the display name of the unresolved entry must be in the format X@Y.Z, such as "pete@pinecone.com".</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ad8ba-132">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ad8ba-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ad8ba-133">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="ad8ba-133">Protocol specifications</span></span>

<span data-ttu-id="ad8ba-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ad8ba-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ad8ba-135">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="ad8ba-135">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ad8ba-136">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ad8ba-136">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ad8ba-137">Указывает свойства и операции для списков пользователей, контактов, групп и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ad8ba-137">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="ad8ba-138">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ad8ba-138">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ad8ba-139">Указывает свойства и операции, которые разрешены для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="ad8ba-139">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="ad8ba-140">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ad8ba-140">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ad8ba-141">от стандартных интернет-соглашений по электронной почте до объектов сообщений.</span><span class="sxs-lookup"><span data-stu-id="ad8ba-141">from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ad8ba-142">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="ad8ba-142">Header files</span></span>

<span data-ttu-id="ad8ba-143">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ad8ba-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="ad8ba-144">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="ad8ba-144">Provides data type definitions.</span></span>
    
<span data-ttu-id="ad8ba-145">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ad8ba-145">Mapitags.h</span></span>
  
> <span data-ttu-id="ad8ba-146">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="ad8ba-146">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ad8ba-147">См. также</span><span class="sxs-lookup"><span data-stu-id="ad8ba-147">See also</span></span>



[<span data-ttu-id="ad8ba-148">Каноническое свойство PidTagAttachDataObject</span><span class="sxs-lookup"><span data-stu-id="ad8ba-148">PidTagAttachDataObject Canonical Property</span></span>](pidtagattachdataobject-canonical-property.md)


[<span data-ttu-id="ad8ba-149">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ad8ba-149">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ad8ba-150">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ad8ba-150">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ad8ba-151">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="ad8ba-151">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ad8ba-152">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="ad8ba-152">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

