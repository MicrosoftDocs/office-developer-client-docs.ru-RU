---
title: Каноническое свойство PidTagReceivedBySearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceivedBySearchKey
api_type:
- COM
ms.assetid: 4b37555a-1d07-4f42-95e3-b8fa37ed0c3b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: bace518784bf24807cfca09032a4f3912f4e98ed
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359208"
---
# <a name="pidtagreceivedbysearchkey-canonical-property"></a><span data-ttu-id="c8d01-103">Каноническое свойство PidTagReceivedBySearchKey</span><span class="sxs-lookup"><span data-stu-id="c8d01-103">PidTagReceivedBySearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="c8d01-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c8d01-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c8d01-105">Содержит ключ поиска пользователя обмена сообщениями, который получает сообщение.</span><span class="sxs-lookup"><span data-stu-id="c8d01-105">Contains the search key of the messaging user who receives the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c8d01-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="c8d01-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c8d01-107">PR_RECEIVED_BY_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="c8d01-107">PR_RECEIVED_BY_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="c8d01-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="c8d01-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c8d01-109">0x0051</span><span class="sxs-lookup"><span data-stu-id="c8d01-109">0x0051</span></span>  <br/> |
|<span data-ttu-id="c8d01-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="c8d01-110">Data type:</span></span>  <br/> |<span data-ttu-id="c8d01-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="c8d01-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="c8d01-112">Область:</span><span class="sxs-lookup"><span data-stu-id="c8d01-112">Area:</span></span>  <br/> |<span data-ttu-id="c8d01-113">Address</span><span class="sxs-lookup"><span data-stu-id="c8d01-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c8d01-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="c8d01-114">Remarks</span></span>

<span data-ttu-id="c8d01-115">Это свойство является одним из свойств адреса для пользователя сообщения, который получает сообщение.</span><span class="sxs-lookup"><span data-stu-id="c8d01-115">This property is one of the address properties for the messaging user who receives the message.</span></span> <span data-ttu-id="c8d01-116">Его должен установить поставщик входящих транспортных услуг.</span><span class="sxs-lookup"><span data-stu-id="c8d01-116">It must be set by the incoming transport provider.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c8d01-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c8d01-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c8d01-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="c8d01-118">Protocol specifications</span></span>

<span data-ttu-id="c8d01-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c8d01-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c8d01-120">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="c8d01-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c8d01-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c8d01-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c8d01-122">Указывает свойства и операции, допустимые для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="c8d01-122">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="c8d01-123">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c8d01-123">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c8d01-124">Обрабатывает порядок и поток передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="c8d01-124">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="c8d01-125">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c8d01-125">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c8d01-126">Преобразуется между IETF RFC2445, RFC2446 и RFC2447, а также объектами встреч и собраний.</span><span class="sxs-lookup"><span data-stu-id="c8d01-126">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="c8d01-127">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c8d01-127">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c8d01-128">Указывает методы подключения и настройки почтовых ящиков в качестве делегатов, а также взаимодействия с объектами сообщений и календаря, когда они действуют от имени другого пользователя.</span><span class="sxs-lookup"><span data-stu-id="c8d01-128">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="c8d01-129">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c8d01-129">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c8d01-130">Кодирует и декодирует объекты сообщений и вложений в эффективное представление потока.</span><span class="sxs-lookup"><span data-stu-id="c8d01-130">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c8d01-131">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="c8d01-131">Header files</span></span>

<span data-ttu-id="c8d01-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c8d01-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="c8d01-133">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="c8d01-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="c8d01-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c8d01-134">Mapitags.h</span></span>
  
> <span data-ttu-id="c8d01-135">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="c8d01-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c8d01-136">См. также</span><span class="sxs-lookup"><span data-stu-id="c8d01-136">See also</span></span>



[<span data-ttu-id="c8d01-137">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c8d01-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c8d01-138">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c8d01-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c8d01-139">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="c8d01-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c8d01-140">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="c8d01-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

