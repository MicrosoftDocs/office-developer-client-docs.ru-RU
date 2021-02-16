---
title: Каноническое свойство PidTagSenderEmailAddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSenderEmailAddress
api_type:
- COM
ms.assetid: 6e1531ac-489b-4224-921a-8fd13ace9497
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 82c0e386ab9231d1066dbdc4456c31031d2409c1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359166"
---
# <a name="pidtagsenderemailaddress-canonical-property"></a><span data-ttu-id="75bfa-103">Каноническое свойство PidTagSenderEmailAddress</span><span class="sxs-lookup"><span data-stu-id="75bfa-103">PidTagSenderEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="75bfa-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="75bfa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="75bfa-105">Содержит адрес электронной почты отправитель сообщения.</span><span class="sxs-lookup"><span data-stu-id="75bfa-105">Contains the message sender's email address.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="75bfa-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="75bfa-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="75bfa-107">PR_SENDER_EMAIL_ADDRESS, PR_SENDER_EMAIL_ADDRESS_A, PR_SENDER_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="75bfa-107">PR_SENDER_EMAIL_ADDRESS, PR_SENDER_EMAIL_ADDRESS_A, PR_SENDER_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="75bfa-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="75bfa-108">Identifier:</span></span>  <br/> |<span data-ttu-id="75bfa-109">0x0C1F</span><span class="sxs-lookup"><span data-stu-id="75bfa-109">0x0C1F</span></span>  <br/> |
|<span data-ttu-id="75bfa-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="75bfa-110">Data type:</span></span>  <br/> |<span data-ttu-id="75bfa-111">PT_UNICOIDE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="75bfa-111">PT_UNICOIDE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="75bfa-112">Область:</span><span class="sxs-lookup"><span data-stu-id="75bfa-112">Area:</span></span>  <br/> |<span data-ttu-id="75bfa-113">Address</span><span class="sxs-lookup"><span data-stu-id="75bfa-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="75bfa-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="75bfa-114">Remarks</span></span>

<span data-ttu-id="75bfa-115">Эти свойства являются примерами свойств адреса для отправитель сообщения.</span><span class="sxs-lookup"><span data-stu-id="75bfa-115">These properties are examples of the address properties for the message sender.</span></span> <span data-ttu-id="75bfa-116">Они должны быть установлены поставщиком исходятго транспорта, который никогда не должен распространять ранее существующие значения.</span><span class="sxs-lookup"><span data-stu-id="75bfa-116">They must be set by the outgoing transport provider, which should never propagate any previously existing values.</span></span>
  
<span data-ttu-id="75bfa-117">Если ни один поставщик транспорта не предоставил никаких свойств адресов отправитель, то пулер MAPI пытается заполнить их, вызывая метод [IMAPISession::QueryIdentity](imapisession-queryidentity.md) для идентификатора записи.</span><span class="sxs-lookup"><span data-stu-id="75bfa-117">If no transport provider has supplied any sender address properties, the MAPI spooler attempts to fill them in by calling the [IMAPISession::QueryIdentity](imapisession-queryidentity.md) method for an entry identifier.</span></span> <span data-ttu-id="75bfa-118">Если идентификаторы записей не указаны, то пульщик MAPI сохраняет "Unknown" во всех свойствах адреса отправитель типа PT_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="75bfa-118">If no entry identifiers have been provided, the MAPI spooler stores "Unknown" in all the sender address properties of type PT_TSTRING.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="75bfa-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="75bfa-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="75bfa-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="75bfa-120">Protocol specifications</span></span>

<span data-ttu-id="75bfa-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="75bfa-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="75bfa-122">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="75bfa-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="75bfa-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="75bfa-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="75bfa-124">Указывает свойства и операции, которые разрешены для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="75bfa-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="75bfa-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="75bfa-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="75bfa-126">Обрабатывает порядок и поток передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="75bfa-126">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="75bfa-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="75bfa-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="75bfa-128">Преобразуется между IETF RFC2445, RFC2446 и RFC2447, а также объектами встреч и собраний.</span><span class="sxs-lookup"><span data-stu-id="75bfa-128">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="75bfa-129">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="75bfa-129">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="75bfa-130">Указывает свойства и операции, которые разрешены для объектов post.</span><span class="sxs-lookup"><span data-stu-id="75bfa-130">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="75bfa-131">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="75bfa-131">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="75bfa-132">Указывает свойства и операции, которые разрешены для объектов контактов и личных списков рассылки.</span><span class="sxs-lookup"><span data-stu-id="75bfa-132">Specifies the properties and operations that are permissible for contact and personal distribution list objects.</span></span>
    
<span data-ttu-id="75bfa-133">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="75bfa-133">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="75bfa-134">Кодирует и декодирует объекты сообщений и вложений в эффективное представление потока.</span><span class="sxs-lookup"><span data-stu-id="75bfa-134">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="75bfa-135">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="75bfa-135">Header files</span></span>

<span data-ttu-id="75bfa-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="75bfa-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="75bfa-137">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="75bfa-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="75bfa-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="75bfa-138">Mapitags.h</span></span>
  
> <span data-ttu-id="75bfa-139">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="75bfa-139">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="75bfa-140">См. также</span><span class="sxs-lookup"><span data-stu-id="75bfa-140">See also</span></span>



[<span data-ttu-id="75bfa-141">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="75bfa-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="75bfa-142">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="75bfa-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="75bfa-143">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="75bfa-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="75bfa-144">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="75bfa-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

