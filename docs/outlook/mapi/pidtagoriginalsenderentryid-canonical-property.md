---
title: Каноническое свойство PidTagOriginalSenderEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSenderEntryId
api_type:
- COM
ms.assetid: bd182589-afea-4967-92f5-ba1914e4db3f
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: bd32ef6540e0deec1b793bd49bab651d864754c6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393833"
---
# <a name="pidtagoriginalsenderentryid-canonical-property"></a><span data-ttu-id="3046e-103">Каноническое свойство PidTagOriginalSenderEntryId</span><span class="sxs-lookup"><span data-stu-id="3046e-103">PidTagOriginalSenderEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="3046e-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3046e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3046e-105">Содержит запись идентификатор отправителя первая версия сообщения, то есть, сообщение перед пересылку и ответ.</span><span class="sxs-lookup"><span data-stu-id="3046e-105">Contains the entry identifier of the sender of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3046e-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="3046e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3046e-107">PR_ORIGINAL_SENDER_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="3046e-107">PR_ORIGINAL_SENDER_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="3046e-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="3046e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3046e-109">0x005B</span><span class="sxs-lookup"><span data-stu-id="3046e-109">0x005B</span></span>  <br/> |
|<span data-ttu-id="3046e-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="3046e-110">Data type:</span></span>  <br/> |<span data-ttu-id="3046e-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="3046e-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="3046e-112">Область:</span><span class="sxs-lookup"><span data-stu-id="3046e-112">Area:</span></span>  <br/> |<span data-ttu-id="3046e-113">Общие системы обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="3046e-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3046e-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="3046e-114">Remarks</span></span>

<span data-ttu-id="3046e-115">Это свойство является одним из свойств адреса для исходного отправителя сообщения.</span><span class="sxs-lookup"><span data-stu-id="3046e-115">This property is one of the address properties for the original sender of a message.</span></span> <span data-ttu-id="3046e-116">В первой отправки сообщения клиентское приложение следует этому свойству присвоено значение свойства **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="3046e-116">At first submission of the message, a client application should set this property to the value of the **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="3046e-117">Никогда не изменяется при сообщение будет переслано или ответ.</span><span class="sxs-lookup"><span data-stu-id="3046e-117">It is never changed when the message is forwarded or replied to.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3046e-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="3046e-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3046e-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="3046e-119">Protocol specifications</span></span>

<span data-ttu-id="3046e-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3046e-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3046e-121">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="3046e-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3046e-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3046e-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3046e-123">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="3046e-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3046e-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="3046e-124">Header files</span></span>

<span data-ttu-id="3046e-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3046e-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="3046e-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="3046e-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="3046e-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3046e-127">Mapitags.h</span></span>
  
> <span data-ttu-id="3046e-128">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="3046e-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3046e-129">См. также</span><span class="sxs-lookup"><span data-stu-id="3046e-129">See also</span></span>



[<span data-ttu-id="3046e-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="3046e-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3046e-131">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="3046e-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3046e-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="3046e-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3046e-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="3046e-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

