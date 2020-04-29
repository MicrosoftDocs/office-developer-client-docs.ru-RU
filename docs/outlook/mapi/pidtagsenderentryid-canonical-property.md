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
ms.openlocfilehash: 0bc8b8bd76d553cc4e12e331e9fe7047ef7aaf4e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358914"
---
# <a name="pidtagsenderentryid-canonical-property"></a><span data-ttu-id="90675-103">Каноническое свойство PidTagSenderEntryId</span><span class="sxs-lookup"><span data-stu-id="90675-103">PidTagSenderEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="90675-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="90675-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="90675-105">Содержит идентификатор записи отправителя сообщения.</span><span class="sxs-lookup"><span data-stu-id="90675-105">Contains the message sender's entry identifier.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="90675-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="90675-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="90675-107">PR_SENDER_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="90675-107">PR_SENDER_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="90675-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="90675-108">Identifier:</span></span>  <br/> |<span data-ttu-id="90675-109">0x0C19</span><span class="sxs-lookup"><span data-stu-id="90675-109">0x0C19</span></span>  <br/> |
|<span data-ttu-id="90675-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="90675-110">Data type:</span></span>  <br/> |<span data-ttu-id="90675-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="90675-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="90675-112">Область:</span><span class="sxs-lookup"><span data-stu-id="90675-112">Area:</span></span>  <br/> |<span data-ttu-id="90675-113">Address</span><span class="sxs-lookup"><span data-stu-id="90675-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="90675-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="90675-114">Remarks</span></span>

<span data-ttu-id="90675-115">Это свойство является одним из свойств адреса отправителя сообщения.</span><span class="sxs-lookup"><span data-stu-id="90675-115">This property is one of the address properties for the message sender.</span></span> <span data-ttu-id="90675-116">Он должен быть задан поставщиком исходящей транспортировки, который никогда не должен распространять какие бы то ни было существующие значения.</span><span class="sxs-lookup"><span data-stu-id="90675-116">It must be set by the outgoing transport provider, which should never propagate any previously existing values.</span></span>
  
<span data-ttu-id="90675-117">Если поставщик транспорта не предоставил свойства адреса отправителя, то диспетчер очереди MAPI пытается заполнить их, вызвав метод [IMAPISession:: куеридентити](imapisession-queryidentity.md) для идентификатора записи.</span><span class="sxs-lookup"><span data-stu-id="90675-117">If no transport provider has supplied any sender address properties, the MAPI spooler attempts to fill them in by calling the [IMAPISession::QueryIdentity](imapisession-queryidentity.md) method for an entry identifier.</span></span> <span data-ttu-id="90675-118">Если не указаны никакие идентификаторы записей, диспетчер очереди MAPI имеет идентификатор, соответствующий строке "Unknown" в этом свойстве.</span><span class="sxs-lookup"><span data-stu-id="90675-118">If no entry identifiers have been provided, the MAPI spooler an identifier corresponding to the string "Unknown" in this property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="90675-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="90675-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="90675-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="90675-120">Protocol specifications</span></span>

<span data-ttu-id="90675-121">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="90675-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="90675-122">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="90675-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="90675-123">[[MS — ОКСОМСГ]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="90675-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="90675-124">Задает свойства и операции, допустимые для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="90675-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="90675-125">[[MS — ОКСОРСС]](https://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="90675-125">[[MS-OXORSS]](https://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="90675-126">Задает свойства и операции, представляющие элементы RSS.</span><span class="sxs-lookup"><span data-stu-id="90675-126">Specifies the properties and operations that represent RSS items.</span></span>
    
<span data-ttu-id="90675-127">[[MS — ОКСКФКСИКС]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="90675-127">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="90675-128">Обрабатывает порядок и потоки для передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="90675-128">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="90675-129">[[MS — ОКСЦИКАЛ]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="90675-129">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="90675-130">Преобразование между IETF RFC2445, RFC2446 и RFC2447, а объекты встреч и собраний.</span><span class="sxs-lookup"><span data-stu-id="90675-130">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="90675-131">[[MS — ОКСОКАЛ]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="90675-131">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="90675-132">Задает свойства и операции для встречи, приглашения на собрание и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="90675-132">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="90675-133">[[MS — ОКСОПОСТ]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="90675-133">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="90675-134">Задает свойства и операции, допустимые для объектов POST.</span><span class="sxs-lookup"><span data-stu-id="90675-134">Specifies the properties and operations that are permissible for post objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="90675-135">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="90675-135">Header files</span></span>

<span data-ttu-id="90675-136">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="90675-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="90675-137">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="90675-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="90675-138">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="90675-138">Mapitags.h</span></span>
  
> <span data-ttu-id="90675-139">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="90675-139">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="90675-140">См. также</span><span class="sxs-lookup"><span data-stu-id="90675-140">See also</span></span>



[<span data-ttu-id="90675-141">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="90675-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="90675-142">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="90675-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="90675-143">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="90675-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="90675-144">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="90675-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

