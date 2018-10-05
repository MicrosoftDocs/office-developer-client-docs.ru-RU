---
title: Каноническое свойство PidTagTransportMessageHeaders
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagTransportMessageHeaders
api_type:
- COM
ms.assetid: 9f8e3f20-6454-4dfd-9b35-e0401abac6b3
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7ad9048a19123b94c10afaddcbedb7f54e8fe477
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392351"
---
# <a name="pidtagtransportmessageheaders-canonical-property"></a><span data-ttu-id="51af5-103">Каноническое свойство PidTagTransportMessageHeaders</span><span class="sxs-lookup"><span data-stu-id="51af5-103">PidTagTransportMessageHeaders Canonical Property</span></span>

  
  
<span data-ttu-id="51af5-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="51af5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="51af5-105">Содержит сведения о конверт сообщения транспорта.</span><span class="sxs-lookup"><span data-stu-id="51af5-105">Contains transport-specific message envelope information.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="51af5-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="51af5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="51af5-107">PR_TRANSPORT_MESSAGE_HEADERS, PR_TRANSPORT_MESSAGE_HEADERS_A, PR_TRANSPORT_MESSAGE_HEADERS_W</span><span class="sxs-lookup"><span data-stu-id="51af5-107">PR_TRANSPORT_MESSAGE_HEADERS, PR_TRANSPORT_MESSAGE_HEADERS_A, PR_TRANSPORT_MESSAGE_HEADERS_W</span></span>  <br/> |
|<span data-ttu-id="51af5-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="51af5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="51af5-109">0x007D</span><span class="sxs-lookup"><span data-stu-id="51af5-109">0x007D</span></span>  <br/> |
|<span data-ttu-id="51af5-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="51af5-110">Data type:</span></span>  <br/> |<span data-ttu-id="51af5-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="51af5-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="51af5-112">Область:</span><span class="sxs-lookup"><span data-stu-id="51af5-112">Area:</span></span>  <br/> |<span data-ttu-id="51af5-113">Электронная почта</span><span class="sxs-lookup"><span data-stu-id="51af5-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="51af5-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="51af5-114">Remarks</span></span>

<span data-ttu-id="51af5-115">Поставщика транспорта можно создать заголовок сообщения для входящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="51af5-115">The transport provider can generate the message header information for inbound messages.</span></span>
  
<span data-ttu-id="51af5-116">Эти свойства предоставляют альтернативой пропуск данные заголовка сообщения транспорта или ее добавления текста сообщения.</span><span class="sxs-lookup"><span data-stu-id="51af5-116">These properties offer an alternative to either discarding the transport message header information or prepending it to the message text.</span></span> <span data-ttu-id="51af5-117">Клиент можно ли отобразить сведения.</span><span class="sxs-lookup"><span data-stu-id="51af5-117">The client can choose whether or not to display the information.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="51af5-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="51af5-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="51af5-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="51af5-119">Protocol specifications</span></span>

<span data-ttu-id="51af5-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="51af5-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="51af5-121">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="51af5-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="51af5-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="51af5-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="51af5-123">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="51af5-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
<span data-ttu-id="51af5-124">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="51af5-124">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="51af5-125">Преобразование conventions стандартных электронной почты Интернета объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="51af5-125">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="51af5-126">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="51af5-126">Header files</span></span>

<span data-ttu-id="51af5-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="51af5-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="51af5-128">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="51af5-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="51af5-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="51af5-129">Mapitags.h</span></span>
  
> <span data-ttu-id="51af5-130">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="51af5-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="51af5-131">См. также</span><span class="sxs-lookup"><span data-stu-id="51af5-131">See also</span></span>



[<span data-ttu-id="51af5-132">Каноническое свойство PidTagBody</span><span class="sxs-lookup"><span data-stu-id="51af5-132">PidTagBody Canonical Property</span></span>](pidtagbody-canonical-property.md)


[<span data-ttu-id="51af5-133">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="51af5-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="51af5-134">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="51af5-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="51af5-135">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="51af5-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="51af5-136">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="51af5-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

