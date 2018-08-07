---
title: Каноническое свойство PidTagReceivedByEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceivedByEntryId
api_type:
- COM
ms.assetid: 737f8584-fc52-4324-ac40-2fc554a3095d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e7d457c898a1b8c733913de0fbb2fbfe9542dc9c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811626"
---
# <a name="pidtagreceivedbyentryid-canonical-property"></a><span data-ttu-id="630d7-103">Каноническое свойство PidTagReceivedByEntryId</span><span class="sxs-lookup"><span data-stu-id="630d7-103">PidTagReceivedByEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="630d7-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="630d7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="630d7-105">Содержит идентификатор записи обмена сообщениями пользователя, который получает сообщение.</span><span class="sxs-lookup"><span data-stu-id="630d7-105">Contains the entry identifier of the messaging user who actually receives the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="630d7-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="630d7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="630d7-107">PR_RECEIVED_BY_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="630d7-107">PR_RECEIVED_BY_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="630d7-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="630d7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="630d7-109">0x003F</span><span class="sxs-lookup"><span data-stu-id="630d7-109">0x003F</span></span>  <br/> |
|<span data-ttu-id="630d7-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="630d7-110">Data type:</span></span>  <br/> |<span data-ttu-id="630d7-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="630d7-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="630d7-112">Область:</span><span class="sxs-lookup"><span data-stu-id="630d7-112">Area:</span></span>  <br/> |<span data-ttu-id="630d7-113">Адресная книга</span><span class="sxs-lookup"><span data-stu-id="630d7-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="630d7-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="630d7-114">Remarks</span></span>

<span data-ttu-id="630d7-115">Это свойство является одним из свойств адреса для обмена мгновенными сообщениями пользователя, который получает сообщение.</span><span class="sxs-lookup"><span data-stu-id="630d7-115">This property is one of the address properties for the messaging user who receives the message.</span></span> <span data-ttu-id="630d7-116">Он должен иметь значение входящих поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="630d7-116">It must be set by the incoming transport provider.</span></span>
  
<span data-ttu-id="630d7-117">Это свойство соответствует атрибуту MH_T_ доставки конверт X.400-message.</span><span class="sxs-lookup"><span data-stu-id="630d7-117">This property corresponds to an X.400 delivery envelope per-message MH_T_ attribute.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="630d7-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="630d7-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="630d7-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="630d7-119">Protocol specifications</span></span>

<span data-ttu-id="630d7-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="630d7-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="630d7-121">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="630d7-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="630d7-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="630d7-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="630d7-123">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="630d7-123">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="630d7-124">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="630d7-124">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="630d7-125">Обрабатывает порядок и поток для передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="630d7-125">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="630d7-126">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="630d7-126">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="630d7-127">Преобразование между IETF RFC2445, RFC2446 и RFC2447 и встречи и собрания элементов.</span><span class="sxs-lookup"><span data-stu-id="630d7-127">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting items.</span></span>
    
<span data-ttu-id="630d7-128">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="630d7-128">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="630d7-129">Указывает методы для подключений и настройки почтовых ящиков как делегаты и взаимодействия с объектами сообщений и календаря, когда они действовать от имени другого пользователя.</span><span class="sxs-lookup"><span data-stu-id="630d7-129">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="630d7-130">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="630d7-130">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="630d7-131">Кодирует и декодирует объекты сообщения и вложения в представление эффективным потока.</span><span class="sxs-lookup"><span data-stu-id="630d7-131">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="630d7-132">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="630d7-132">Header files</span></span>

<span data-ttu-id="630d7-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="630d7-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="630d7-134">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="630d7-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="630d7-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="630d7-135">Mapitags.h</span></span>
  
> <span data-ttu-id="630d7-136">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="630d7-136">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="630d7-137">См. также</span><span class="sxs-lookup"><span data-stu-id="630d7-137">See also</span></span>



[<span data-ttu-id="630d7-138">Каноническое свойство PidTagEntryId</span><span class="sxs-lookup"><span data-stu-id="630d7-138">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)


[<span data-ttu-id="630d7-139">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="630d7-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="630d7-140">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="630d7-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="630d7-141">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="630d7-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="630d7-142">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="630d7-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

