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
ms.openlocfilehash: 33e41343e0c159be20ed1499fc24223947975e1d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359096"
---
# <a name="pidtagreceivedrepresentingentryid-canonical-property"></a><span data-ttu-id="f4385-103">Каноническое свойство PidTagReceivedRepresentingEntryId</span><span class="sxs-lookup"><span data-stu-id="f4385-103">PidTagReceivedRepresentingEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="f4385-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f4385-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f4385-105">Содержит идентификатор записи для пользователя обмена сообщениями, представленного пользователем-получателем.</span><span class="sxs-lookup"><span data-stu-id="f4385-105">Contains the entry identifier for the messaging user who is represented by the receiving user.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f4385-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="f4385-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f4385-107">ПР_РКВД_РЕПРЕСЕНТИНГ_ЕНТРИД</span><span class="sxs-lookup"><span data-stu-id="f4385-107">PR_RCVD_REPRESENTING_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="f4385-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="f4385-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f4385-109">0x0043</span><span class="sxs-lookup"><span data-stu-id="f4385-109">0x0043</span></span>  <br/> |
|<span data-ttu-id="f4385-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="f4385-110">Data type:</span></span>  <br/> |<span data-ttu-id="f4385-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="f4385-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="f4385-112">Область:</span><span class="sxs-lookup"><span data-stu-id="f4385-112">Area:</span></span>  <br/> |<span data-ttu-id="f4385-113">Address</span><span class="sxs-lookup"><span data-stu-id="f4385-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f4385-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="f4385-114">Remarks</span></span>

<span data-ttu-id="f4385-115">Это свойство является одним из свойств адреса пользователя обмена сообщениями, представленного принимающим пользователем.</span><span class="sxs-lookup"><span data-stu-id="f4385-115">This property is one of the address properties for the messaging user who is being represented by the receiving user.</span></span> <span data-ttu-id="f4385-116">Он должен быть задан входящим поставщиком транспорта, который также отвечает за авторизацию или проверку делегата.</span><span class="sxs-lookup"><span data-stu-id="f4385-116">It must be set by the incoming transport provider, which is also responsible for authorization or verification of the delegate.</span></span> <span data-ttu-id="f4385-117">Если пользователь обмена сообщениями не представлен, для этого свойства необходимо задать идентификатор записи, содержащийся в свойстве **пр_рецеивед_би_ентрид** ([PidTagReceivedByEntryId](pidtagreceivedbyentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="f4385-117">If no messaging user is being represented, this property should be set to the entry identifier contained in the **PR_RECEIVED_BY_ENTRYID** ([PidTagReceivedByEntryId](pidtagreceivedbyentryid-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="f4385-118">Клиентское приложение, отвечающее на сообщение, полученное от имени другого клиента, должно копировать это свойство из полученного сообщения в свойство **пр_сент_репресентинг_ентрид** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md)) для ответа.</span><span class="sxs-lookup"><span data-stu-id="f4385-118">A client application replying to a message received on behalf of another client should copy this property from the received message into the **PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md)) property for the reply.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f4385-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f4385-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f4385-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="f4385-120">Protocol specifications</span></span>

<span data-ttu-id="f4385-121">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f4385-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f4385-122">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="f4385-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f4385-123">[[MS — ОКСОМСГ]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f4385-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f4385-124">Задает свойства и операции, допустимые для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="f4385-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="f4385-125">[[MS — ОКСКФКСИКС]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f4385-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f4385-126">Обрабатывает порядок и потоки для передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="f4385-126">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="f4385-127">[[MS — ОКСОДЛГТ]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f4385-127">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f4385-128">Задает методы для подключения и настройки почтовых ящиков в качестве делегатов и взаимодействия с объектами Message и Calendar, когда они действуют от имени другого пользователя.</span><span class="sxs-lookup"><span data-stu-id="f4385-128">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f4385-129">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="f4385-129">Header files</span></span>

<span data-ttu-id="f4385-130">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="f4385-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="f4385-131">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="f4385-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="f4385-132">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="f4385-132">Mapitags.h</span></span>
  
> <span data-ttu-id="f4385-133">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="f4385-133">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f4385-134">См. также</span><span class="sxs-lookup"><span data-stu-id="f4385-134">See also</span></span>



[<span data-ttu-id="f4385-135">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f4385-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f4385-136">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="f4385-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f4385-137">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="f4385-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f4385-138">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="f4385-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

