---
title: Каноническое свойство PidTagReceivedRepresentingEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceivedRepresentingEntryId
api_type:
- COM
ms.assetid: 2ae2266c-f093-41e5-b4d0-e12aa0f03190
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 12e4c97947cfe579f550cc6d48ca0b64750b9ab6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811637"
---
# <a name="pidtagreceivedrepresentingentryid-canonical-property"></a><span data-ttu-id="d0871-103">Каноническое свойство PidTagReceivedRepresentingEntryId</span><span class="sxs-lookup"><span data-stu-id="d0871-103">PidTagReceivedRepresentingEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="d0871-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d0871-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d0871-105">Содержит идентификатор записи для обмена сообщениями пользователя, представленного получателя.</span><span class="sxs-lookup"><span data-stu-id="d0871-105">Contains the entry identifier for the messaging user who is represented by the receiving user.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d0871-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="d0871-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d0871-107">PR_RCVD_REPRESENTING_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="d0871-107">PR_RCVD_REPRESENTING_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="d0871-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="d0871-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d0871-109">0x0043</span><span class="sxs-lookup"><span data-stu-id="d0871-109">0x0043</span></span>  <br/> |
|<span data-ttu-id="d0871-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="d0871-110">Data type:</span></span>  <br/> |<span data-ttu-id="d0871-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="d0871-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="d0871-112">Область:</span><span class="sxs-lookup"><span data-stu-id="d0871-112">Area:</span></span>  <br/> |<span data-ttu-id="d0871-113">Address</span><span class="sxs-lookup"><span data-stu-id="d0871-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d0871-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="d0871-114">Remarks</span></span>

<span data-ttu-id="d0871-115">Это свойство является одним из свойств адреса для обмена мгновенными сообщениями пользователя, который представляется получателя.</span><span class="sxs-lookup"><span data-stu-id="d0871-115">This property is one of the address properties for the messaging user who is being represented by the receiving user.</span></span> <span data-ttu-id="d0871-116">Он должен иметь значение входящих поставщика транспорта, также несет ответственность за авторизации или проверки делегата.</span><span class="sxs-lookup"><span data-stu-id="d0871-116">It must be set by the incoming transport provider, which is also responsible for authorization or verification of the delegate.</span></span> <span data-ttu-id="d0871-117">Если пользователь не обмена сообщениями представлен, это свойство должно быть присвоено идентификатор записи, содержащиеся в свойстве **PR_RECEIVED_BY_ENTRYID** ([PidTagReceivedByEntryId](pidtagreceivedbyentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d0871-117">If no messaging user is being represented, this property should be set to the entry identifier contained in the **PR_RECEIVED_BY_ENTRYID** ([PidTagReceivedByEntryId](pidtagreceivedbyentryid-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="d0871-118">Клиентского приложения ответ на сообщение получено от имени другого клиента должны скопируйте это свойство из полученного сообщения в свойство **PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md)) для ответа.</span><span class="sxs-lookup"><span data-stu-id="d0871-118">A client application replying to a message received on behalf of another client should copy this property from the received message into the **PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md)) property for the reply.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d0871-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d0871-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d0871-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="d0871-120">Protocol specifications</span></span>

<span data-ttu-id="d0871-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d0871-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d0871-122">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="d0871-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d0871-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d0871-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d0871-124">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="d0871-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="d0871-125">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d0871-125">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d0871-126">Обрабатывает порядок и поток для передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="d0871-126">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="d0871-127">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d0871-127">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d0871-128">Указывает методы для подключений и настройки почтовых ящиков как делегаты и взаимодействия с объектами сообщений и календаря, когда они действовать от имени другого пользователя.</span><span class="sxs-lookup"><span data-stu-id="d0871-128">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d0871-129">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="d0871-129">Header files</span></span>

<span data-ttu-id="d0871-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d0871-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="d0871-131">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="d0871-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="d0871-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d0871-132">Mapitags.h</span></span>
  
> <span data-ttu-id="d0871-133">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="d0871-133">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d0871-134">См. также</span><span class="sxs-lookup"><span data-stu-id="d0871-134">See also</span></span>



[<span data-ttu-id="d0871-135">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d0871-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d0871-136">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d0871-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d0871-137">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="d0871-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d0871-138">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="d0871-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

