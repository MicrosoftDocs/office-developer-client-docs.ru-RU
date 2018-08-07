---
title: Каноническое свойство PidTagReceivedByName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceivedByName
api_type:
- COM
ms.assetid: edd29217-74bb-4321-82fd-65f0fbfd05f8
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7b564b1dda1d72a28e16fad40f0ef90451aaaf0f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811631"
---
# <a name="pidtagreceivedbyname-canonical-property"></a><span data-ttu-id="a53f1-103">Каноническое свойство PidTagReceivedByName</span><span class="sxs-lookup"><span data-stu-id="a53f1-103">PidTagReceivedByName Canonical Property</span></span>

  
  
<span data-ttu-id="a53f1-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a53f1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a53f1-105">Содержит отображаемое имя пользователя системы обмена сообщениями, который получает сообщение.</span><span class="sxs-lookup"><span data-stu-id="a53f1-105">Contains the display name of the messaging user who receives the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a53f1-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="a53f1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a53f1-107">PR_RECEIVED_BY_NAME, PR_RECEIVED_BY_NAME_A, PR_RECEIVED_BY_NAME_W</span><span class="sxs-lookup"><span data-stu-id="a53f1-107">PR_RECEIVED_BY_NAME, PR_RECEIVED_BY_NAME_A, PR_RECEIVED_BY_NAME_W</span></span>  <br/> |
|<span data-ttu-id="a53f1-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="a53f1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a53f1-109">0x0040</span><span class="sxs-lookup"><span data-stu-id="a53f1-109">0x0040</span></span>  <br/> |
|<span data-ttu-id="a53f1-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="a53f1-110">Data type:</span></span>  <br/> |<span data-ttu-id="a53f1-111">PT_UNICODE PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="a53f1-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="a53f1-112">Область:</span><span class="sxs-lookup"><span data-stu-id="a53f1-112">Area:</span></span>  <br/> |<span data-ttu-id="a53f1-113">Address</span><span class="sxs-lookup"><span data-stu-id="a53f1-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a53f1-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="a53f1-114">Remarks</span></span>

<span data-ttu-id="a53f1-115">Эти свойства — это пример свойств адрес для обмена мгновенными сообщениями пользователя, который получает сообщение.</span><span class="sxs-lookup"><span data-stu-id="a53f1-115">These properties are an example of the address properties for the messaging user who receives the message.</span></span> <span data-ttu-id="a53f1-116">Им должен иметь значение входящих поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="a53f1-116">They must be set by the incoming transport provider.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a53f1-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="a53f1-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a53f1-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="a53f1-118">Protocol specifications</span></span>

<span data-ttu-id="a53f1-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a53f1-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a53f1-120">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="a53f1-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a53f1-121">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a53f1-121">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a53f1-122">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="a53f1-122">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="a53f1-123">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a53f1-123">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a53f1-124">Обрабатывает порядок и поток для передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="a53f1-124">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="a53f1-125">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a53f1-125">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a53f1-126">Преобразование между IETF RFC2445, RFC2446 и RFC2447 и встречи и собрания объекты.</span><span class="sxs-lookup"><span data-stu-id="a53f1-126">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="a53f1-127">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a53f1-127">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a53f1-128">Указывает методы для подключений и настройки почтовых ящиков как делегаты и взаимодействия с объектами сообщений и календаря, когда они действовать от имени другого пользователя.</span><span class="sxs-lookup"><span data-stu-id="a53f1-128">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="a53f1-129">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a53f1-129">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a53f1-130">Кодирует и декодирует объекты сообщения и вложения в представление эффективным потока.</span><span class="sxs-lookup"><span data-stu-id="a53f1-130">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a53f1-131">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="a53f1-131">Header files</span></span>

<span data-ttu-id="a53f1-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a53f1-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="a53f1-133">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="a53f1-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="a53f1-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a53f1-134">Mapitags.h</span></span>
  
> <span data-ttu-id="a53f1-135">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="a53f1-135">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a53f1-136">См. также</span><span class="sxs-lookup"><span data-stu-id="a53f1-136">See also</span></span>



[<span data-ttu-id="a53f1-137">Каноническое свойство PidTagDisplayName</span><span class="sxs-lookup"><span data-stu-id="a53f1-137">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)


[<span data-ttu-id="a53f1-138">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a53f1-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a53f1-139">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a53f1-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a53f1-140">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="a53f1-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a53f1-141">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="a53f1-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

