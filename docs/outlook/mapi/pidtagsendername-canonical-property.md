---
title: Каноническое свойство PidTagSenderName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSenderName
api_type:
- COM
ms.assetid: 33fb53a8-4c7b-4418-8849-b6f9a1580172
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 953e792b6d18f7da9ee7eb17e07e6e05557e98ae
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355071"
---
# <a name="pidtagsendername-canonical-property"></a><span data-ttu-id="81e05-103">Каноническое свойство PidTagSenderName</span><span class="sxs-lookup"><span data-stu-id="81e05-103">PidTagSenderName Canonical Property</span></span>

  
  
<span data-ttu-id="81e05-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="81e05-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="81e05-105">Содержит отображаемую имя отправитель сообщения.</span><span class="sxs-lookup"><span data-stu-id="81e05-105">Contains the message sender's display name.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="81e05-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="81e05-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="81e05-107">PR_SENDER_NAME, PR_SENDER_NAME_A, PR_SENDER_NAME_W</span><span class="sxs-lookup"><span data-stu-id="81e05-107">PR_SENDER_NAME, PR_SENDER_NAME_A, PR_SENDER_NAME_W</span></span>  <br/> |
|<span data-ttu-id="81e05-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="81e05-108">Identifier:</span></span>  <br/> |<span data-ttu-id="81e05-109">0x0C1A</span><span class="sxs-lookup"><span data-stu-id="81e05-109">0x0C1A</span></span>  <br/> |
|<span data-ttu-id="81e05-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="81e05-110">Data type:</span></span>  <br/> |<span data-ttu-id="81e05-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="81e05-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="81e05-112">Область:</span><span class="sxs-lookup"><span data-stu-id="81e05-112">Area:</span></span>  <br/> |<span data-ttu-id="81e05-113">Address</span><span class="sxs-lookup"><span data-stu-id="81e05-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="81e05-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="81e05-114">Remarks</span></span>

<span data-ttu-id="81e05-115">Эти свойства являются примерами свойств адреса для отправитель сообщения.</span><span class="sxs-lookup"><span data-stu-id="81e05-115">These properties are examples of the address properties for the message sender.</span></span> <span data-ttu-id="81e05-116">Он должен быть установлен поставщиком исходячих транспортных данных, который никогда не должен распространять ранее существовавших значений.</span><span class="sxs-lookup"><span data-stu-id="81e05-116">It must be set by the outgoing transport provider, which should never propagate any previously existing values.</span></span>
  
<span data-ttu-id="81e05-117">Если ни один поставщик транспорта не предоставил никаких свойств адресов отправитель, то пулер MAPI пытается заполнить их, вызывая метод [IMAPISession::QueryIdentity](imapisession-queryidentity.md) для идентификатора записи.</span><span class="sxs-lookup"><span data-stu-id="81e05-117">If no transport provider has supplied any sender address properties, the MAPI spooler attempts to fill them in by calling the [IMAPISession::QueryIdentity](imapisession-queryidentity.md) method for an entry identifier.</span></span> <span data-ttu-id="81e05-118">Если идентификаторы записей не указаны, то пулер MAPI сохраняет "Unknown" во всех свойствах адреса отправитель типа PT_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="81e05-118">If no entry identifiers have been provided, the MAPI spooler stores "Unknown" in all the sender address properties of type PT_TSTRING.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="81e05-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="81e05-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="81e05-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="81e05-120">Protocol specifications</span></span>

<span data-ttu-id="81e05-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="81e05-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="81e05-122">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="81e05-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="81e05-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="81e05-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="81e05-124">Описывает формат сообщений, используемых для отправки сведений, связанных с папками общего доступа на клиенте.</span><span class="sxs-lookup"><span data-stu-id="81e05-124">Describes the format of messages used to send information related to sharing folders on the client.</span></span>
    
<span data-ttu-id="81e05-125">[[MS-OXORSS]](https://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="81e05-125">[[MS-OXORSS]](https://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="81e05-126">Указывает свойства и операции, которые представляют элементы RSS.</span><span class="sxs-lookup"><span data-stu-id="81e05-126">Specifies the properties and operations that represent RSS items.</span></span>
    
<span data-ttu-id="81e05-127">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="81e05-127">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="81e05-128">Обрабатывает порядок и поток передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="81e05-128">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="81e05-129">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="81e05-129">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="81e05-130">Преобразуется между IETF RFC2445, RFC2446 и RFC2447, а также объектами встреч и собраний.</span><span class="sxs-lookup"><span data-stu-id="81e05-130">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="81e05-131">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="81e05-131">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="81e05-132">Указывает свойства и операции, допустимые для объектов post.</span><span class="sxs-lookup"><span data-stu-id="81e05-132">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="81e05-133">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="81e05-133">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="81e05-134">Указывает свойства и операции, которые разрешены для контактов и личных списков рассылки.</span><span class="sxs-lookup"><span data-stu-id="81e05-134">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="81e05-135">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="81e05-135">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="81e05-136">Кодирует и декодирует объекты сообщений и вложений в эффективное представление потока.</span><span class="sxs-lookup"><span data-stu-id="81e05-136">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="81e05-137">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="81e05-137">Header files</span></span>

<span data-ttu-id="81e05-138">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="81e05-138">Mapidefs.h</span></span>
  
> <span data-ttu-id="81e05-139">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="81e05-139">Provides data type definitions.</span></span>
    
<span data-ttu-id="81e05-140">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="81e05-140">Mapitags.h</span></span>
  
> <span data-ttu-id="81e05-141">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="81e05-141">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="81e05-142">См. также</span><span class="sxs-lookup"><span data-stu-id="81e05-142">See also</span></span>



[<span data-ttu-id="81e05-143">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="81e05-143">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="81e05-144">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="81e05-144">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="81e05-145">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="81e05-145">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="81e05-146">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="81e05-146">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

