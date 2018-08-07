---
title: Каноническое свойство PidTagOriginalSenderAddressType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSenderAddressType
api_type:
- COM
ms.assetid: bd777f19-cbb1-4497-8a0b-e05b491c6957
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 5cac96287db9638f699b75e0c387e003beb5e197
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811461"
---
# <a name="pidtagoriginalsenderaddresstype-canonical-property"></a><span data-ttu-id="9e047-103">Каноническое свойство PidTagOriginalSenderAddressType</span><span class="sxs-lookup"><span data-stu-id="9e047-103">PidTagOriginalSenderAddressType Canonical Property</span></span>

  
  
<span data-ttu-id="9e047-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9e047-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9e047-105">Содержит тип адреса отправителя первая версия сообщения, то есть, сообщение перед пересылку и ответ.</span><span class="sxs-lookup"><span data-stu-id="9e047-105">Contains the address type of the sender of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9e047-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="9e047-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9e047-107">PR_ORIGINAL_SENDER_ADDRTYPE, PR_ORIGINAL_SENDER_ADDRTYPE_A, PR_ORIGINAL_SENDER_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="9e047-107">PR_ORIGINAL_SENDER_ADDRTYPE, PR_ORIGINAL_SENDER_ADDRTYPE_A, PR_ORIGINAL_SENDER_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="9e047-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="9e047-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9e047-109">0x0066</span><span class="sxs-lookup"><span data-stu-id="9e047-109">0x0066</span></span>  <br/> |
|<span data-ttu-id="9e047-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="9e047-110">Data type:</span></span>  <br/> |<span data-ttu-id="9e047-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9e047-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="9e047-112">Область:</span><span class="sxs-lookup"><span data-stu-id="9e047-112">Area:</span></span>  <br/> |<span data-ttu-id="9e047-113">Общие системы обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="9e047-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9e047-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="9e047-114">Remarks</span></span>

<span data-ttu-id="9e047-115">Эти свойства являются примерами свойства адреса для исходного отправителя сообщения.</span><span class="sxs-lookup"><span data-stu-id="9e047-115">These properties are examples of the address properties for the original sender of a message.</span></span> <span data-ttu-id="9e047-116">В первой отправки сообщения в клиентском приложении необходимо задать эти свойства значение **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="9e047-116">At first submission of the message, the client application should set these properties to the value of **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)).</span></span> <span data-ttu-id="9e047-117">Никогда не изменяется при сообщение будет переслано или ответ.</span><span class="sxs-lookup"><span data-stu-id="9e047-117">It is never changed when the message is forwarded or replied to.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9e047-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="9e047-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9e047-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="9e047-119">Protocol specifications</span></span>

<span data-ttu-id="9e047-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9e047-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9e047-121">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="9e047-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9e047-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9e047-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9e047-123">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="9e047-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9e047-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="9e047-124">Header files</span></span>

<span data-ttu-id="9e047-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9e047-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="9e047-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="9e047-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="9e047-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9e047-127">Mapitags.h</span></span>
  
> <span data-ttu-id="9e047-128">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="9e047-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9e047-129">См. также</span><span class="sxs-lookup"><span data-stu-id="9e047-129">See also</span></span>



[<span data-ttu-id="9e047-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="9e047-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9e047-131">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="9e047-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9e047-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="9e047-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9e047-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="9e047-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

