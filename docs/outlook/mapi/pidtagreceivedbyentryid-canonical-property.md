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
ms.openlocfilehash: ab3ffed8dd5b8d73d8024d27790f18397d615c2c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567470"
---
# <a name="pidtagreceivedbyentryid-canonical-property"></a><span data-ttu-id="5a148-103">Каноническое свойство PidTagReceivedByEntryId</span><span class="sxs-lookup"><span data-stu-id="5a148-103">PidTagReceivedByEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="5a148-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5a148-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5a148-105">Содержит идентификатор записи обмена сообщениями пользователя, который получает сообщение.</span><span class="sxs-lookup"><span data-stu-id="5a148-105">Contains the entry identifier of the messaging user who actually receives the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5a148-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="5a148-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5a148-107">PR_RECEIVED_BY_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="5a148-107">PR_RECEIVED_BY_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="5a148-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="5a148-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5a148-109">0x003F</span><span class="sxs-lookup"><span data-stu-id="5a148-109">0x003F</span></span>  <br/> |
|<span data-ttu-id="5a148-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="5a148-110">Data type:</span></span>  <br/> |<span data-ttu-id="5a148-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="5a148-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="5a148-112">Область:</span><span class="sxs-lookup"><span data-stu-id="5a148-112">Area:</span></span>  <br/> |<span data-ttu-id="5a148-113">Адресная книга</span><span class="sxs-lookup"><span data-stu-id="5a148-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5a148-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="5a148-114">Remarks</span></span>

<span data-ttu-id="5a148-115">Это свойство является одним из свойств адреса для обмена мгновенными сообщениями пользователя, который получает сообщение.</span><span class="sxs-lookup"><span data-stu-id="5a148-115">This property is one of the address properties for the messaging user who receives the message.</span></span> <span data-ttu-id="5a148-116">Он должен иметь значение входящих поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="5a148-116">It must be set by the incoming transport provider.</span></span>
  
<span data-ttu-id="5a148-117">Это свойство соответствует атрибуту MH_T_ доставки конверт X.400-message.</span><span class="sxs-lookup"><span data-stu-id="5a148-117">This property corresponds to an X.400 delivery envelope per-message MH_T_ attribute.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5a148-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="5a148-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5a148-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="5a148-119">Protocol specifications</span></span>

<span data-ttu-id="5a148-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5a148-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5a148-121">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="5a148-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5a148-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5a148-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5a148-123">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="5a148-123">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="5a148-124">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5a148-124">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5a148-125">Обрабатывает порядок и поток для передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="5a148-125">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="5a148-126">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5a148-126">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5a148-127">Преобразование между IETF RFC2445, RFC2446 и RFC2447 и встречи и собрания элементов.</span><span class="sxs-lookup"><span data-stu-id="5a148-127">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting items.</span></span>
    
<span data-ttu-id="5a148-128">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5a148-128">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5a148-129">Указывает методы для подключений и настройки почтовых ящиков как делегаты и взаимодействия с объектами сообщений и календаря, когда они действовать от имени другого пользователя.</span><span class="sxs-lookup"><span data-stu-id="5a148-129">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="5a148-130">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5a148-130">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5a148-131">Кодирует и декодирует объекты сообщения и вложения в представление эффективным потока.</span><span class="sxs-lookup"><span data-stu-id="5a148-131">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5a148-132">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="5a148-132">Header files</span></span>

<span data-ttu-id="5a148-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5a148-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="5a148-134">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="5a148-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="5a148-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5a148-135">Mapitags.h</span></span>
  
> <span data-ttu-id="5a148-136">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="5a148-136">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5a148-137">См. также</span><span class="sxs-lookup"><span data-stu-id="5a148-137">See also</span></span>



[<span data-ttu-id="5a148-138">Каноническое свойство PidTagEntryId</span><span class="sxs-lookup"><span data-stu-id="5a148-138">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)


[<span data-ttu-id="5a148-139">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="5a148-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5a148-140">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="5a148-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5a148-141">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="5a148-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5a148-142">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="5a148-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

