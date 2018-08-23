---
title: Каноническое свойство PidTagSenderEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSenderEntryId
api_type:
- COM
ms.assetid: 9f311dd2-853e-46f7-966a-c2ab7a1fb6c5
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f2e8ecba7c92dcbcb719591464e10fb4af2d2344
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591767"
---
# <a name="pidtagsenderentryid-canonical-property"></a><span data-ttu-id="683db-103">Каноническое свойство PidTagSenderEntryId</span><span class="sxs-lookup"><span data-stu-id="683db-103">PidTagSenderEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="683db-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="683db-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="683db-105">Содержит идентификатор записи отправителя сообщения.</span><span class="sxs-lookup"><span data-stu-id="683db-105">Contains the message sender's entry identifier.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="683db-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="683db-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="683db-107">PR_SENDER_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="683db-107">PR_SENDER_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="683db-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="683db-108">Identifier:</span></span>  <br/> |<span data-ttu-id="683db-109">0x0C19</span><span class="sxs-lookup"><span data-stu-id="683db-109">0x0C19</span></span>  <br/> |
|<span data-ttu-id="683db-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="683db-110">Data type:</span></span>  <br/> |<span data-ttu-id="683db-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="683db-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="683db-112">Область:</span><span class="sxs-lookup"><span data-stu-id="683db-112">Area:</span></span>  <br/> |<span data-ttu-id="683db-113">Address</span><span class="sxs-lookup"><span data-stu-id="683db-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="683db-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="683db-114">Remarks</span></span>

<span data-ttu-id="683db-115">Это свойство является одним из свойств адреса отправителя сообщения.</span><span class="sxs-lookup"><span data-stu-id="683db-115">This property is one of the address properties for the message sender.</span></span> <span data-ttu-id="683db-116">Он должен иметь значение исходящей поставщика транспорта, никогда не следует передать все ранее существующие значения.</span><span class="sxs-lookup"><span data-stu-id="683db-116">It must be set by the outgoing transport provider, which should never propagate any previously existing values.</span></span>
  
<span data-ttu-id="683db-117">Если отсутствует транспорт не предоставил любые свойства адрес отправителя, диспетчер очереди MAPI пытается заполните их путем вызова метода [IMAPISession::QueryIdentity](imapisession-queryidentity.md) на идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="683db-117">If no transport provider has supplied any sender address properties, the MAPI spooler attempts to fill them in by calling the [IMAPISession::QueryIdentity](imapisession-queryidentity.md) method for an entry identifier.</span></span> <span data-ttu-id="683db-118">Если нет записи представили идентификаторы MAPI очереди идентификатор, соответствующий строка «Неизвестно» в этом свойстве.</span><span class="sxs-lookup"><span data-stu-id="683db-118">If no entry identifiers have been provided, the MAPI spooler an identifier corresponding to the string "Unknown" in this property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="683db-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="683db-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="683db-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="683db-120">Protocol specifications</span></span>

<span data-ttu-id="683db-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="683db-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="683db-122">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="683db-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="683db-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="683db-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="683db-124">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="683db-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="683db-125">[[MS-OXORSS]](http://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="683db-125">[[MS-OXORSS]](http://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="683db-126">Задает свойства и операции, которые представляют элементам RSS-Каналов.</span><span class="sxs-lookup"><span data-stu-id="683db-126">Specifies the properties and operations that represent RSS items.</span></span>
    
<span data-ttu-id="683db-127">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="683db-127">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="683db-128">Обрабатывает порядок и поток для передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="683db-128">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="683db-129">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="683db-129">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="683db-130">Преобразование между IETF RFC2445, RFC2446 и RFC2447 и встречи и собрания объекты.</span><span class="sxs-lookup"><span data-stu-id="683db-130">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="683db-131">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="683db-131">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="683db-132">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="683db-132">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="683db-133">[[MS-OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="683db-133">[[MS-OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="683db-134">Указывает, что свойства и операции, допустимые для учета объекты.</span><span class="sxs-lookup"><span data-stu-id="683db-134">Specifies the properties and operations that are permissible for post objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="683db-135">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="683db-135">Header files</span></span>

<span data-ttu-id="683db-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="683db-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="683db-137">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="683db-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="683db-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="683db-138">Mapitags.h</span></span>
  
> <span data-ttu-id="683db-139">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="683db-139">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="683db-140">См. также</span><span class="sxs-lookup"><span data-stu-id="683db-140">See also</span></span>



[<span data-ttu-id="683db-141">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="683db-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="683db-142">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="683db-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="683db-143">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="683db-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="683db-144">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="683db-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

