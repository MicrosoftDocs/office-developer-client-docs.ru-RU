---
title: Каноническое свойство PidTagReplyRecipientNames
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReplyRecipientNames
api_type:
- COM
ms.assetid: f5ae6124-3e44-400f-95c2-24b19f3085b5
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 02dcbcccd003fb0b53356da11a3b90b38e632c2a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355176"
---
# <a name="pidtagreplyrecipientnames-canonical-property"></a><span data-ttu-id="04d99-103">Каноническое свойство PidTagReplyRecipientNames</span><span class="sxs-lookup"><span data-stu-id="04d99-103">PidTagReplyRecipientNames Canonical Property</span></span>

  
  
<span data-ttu-id="04d99-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="04d99-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="04d99-105">Содержит список отображаемого имени получателей, которые должны получить ответ.</span><span class="sxs-lookup"><span data-stu-id="04d99-105">Contains a list of display names for recipients that are to get a reply.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="04d99-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="04d99-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="04d99-107">PR_REPLY_RECIPIENT_NAMES, PR_REPLY_RECIPIENT_NAMES_A, PR_REPLY_RECIPIENT_NAMES_W</span><span class="sxs-lookup"><span data-stu-id="04d99-107">PR_REPLY_RECIPIENT_NAMES, PR_REPLY_RECIPIENT_NAMES_A, PR_REPLY_RECIPIENT_NAMES_W</span></span>  <br/> |
|<span data-ttu-id="04d99-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="04d99-108">Identifier:</span></span>  <br/> |<span data-ttu-id="04d99-109">0x0050</span><span class="sxs-lookup"><span data-stu-id="04d99-109">0x0050</span></span>  <br/> |
|<span data-ttu-id="04d99-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="04d99-110">Data type:</span></span>  <br/> |<span data-ttu-id="04d99-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="04d99-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="04d99-112">Область:</span><span class="sxs-lookup"><span data-stu-id="04d99-112">Area:</span></span>  <br/> |<span data-ttu-id="04d99-113">Конверт MAPI</span><span class="sxs-lookup"><span data-stu-id="04d99-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="04d99-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="04d99-114">Remarks</span></span>

<span data-ttu-id="04d99-115">Эти свойства содержат отображаемую информацию, разделенную за 1000.</span><span class="sxs-lookup"><span data-stu-id="04d99-115">These properties contain the display names separated by semicolons.</span></span>
  
<span data-ttu-id="04d99-116">Если этого свойства нет, ответ отправляется только пользователю, который определен свойством **PR_SENDER_NAME** ([PidTagSenderName).](pidtagsendername-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="04d99-116">When this property is not present, a reply is sent only to the user identified by the **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) property.</span></span> <span data-ttu-id="04d99-117">Когда **PR_REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries)](pidtagreplyrecipiententries-canonical-property.md)и эти свойства определены, ответ отправляется всем получателям, определенным этими двумя свойствами.</span><span class="sxs-lookup"><span data-stu-id="04d99-117">When **PR_REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md)) and these properties are defined, the reply is sent to all of the recipients identified by these two properties.</span></span> <span data-ttu-id="04d99-118">Поставщик транспорта использует эти свойства для переопределения обычной логики ответа.</span><span class="sxs-lookup"><span data-stu-id="04d99-118">A transport provider uses these properties to override the usual reply logic.</span></span>
  
<span data-ttu-id="04d99-119">Если установлены **PR_REPLY_RECIPIENT_ENTRIES** или эти свойства, необходимо также установить другое свойство.</span><span class="sxs-lookup"><span data-stu-id="04d99-119">If either **PR_REPLY_RECIPIENT_ENTRIES** or these properties are set, the other property must be set also.</span></span> <span data-ttu-id="04d99-120">Эти свойства должны содержать одинаковое количество получателей, и они должны содержать их в одном порядке.</span><span class="sxs-lookup"><span data-stu-id="04d99-120">These properties must contain the same number of recipients, and they must contain them in the same order.</span></span> <span data-ttu-id="04d99-121">Несоблюдение этих требований может привести к непредсказуемым результатам.</span><span class="sxs-lookup"><span data-stu-id="04d99-121">Failure to observe these requirements can cause unpredictable results.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="04d99-122">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="04d99-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="04d99-123">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="04d99-123">Protocol specifications</span></span>

<span data-ttu-id="04d99-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="04d99-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="04d99-125">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="04d99-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="04d99-126">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="04d99-126">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="04d99-127">Указывает свойства и операции, которые разрешены для сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="04d99-127">Specifies the properties and operations that are permissible on email messages.</span></span>
    
<span data-ttu-id="04d99-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="04d99-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="04d99-129">Преобразуется из стандартных интернет-соглашений электронной почты в объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="04d99-129">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="04d99-130">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="04d99-130">Header files</span></span>

<span data-ttu-id="04d99-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="04d99-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="04d99-132">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="04d99-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="04d99-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="04d99-133">Mapitags.h</span></span>
  
> <span data-ttu-id="04d99-134">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="04d99-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="04d99-135">См. также</span><span class="sxs-lookup"><span data-stu-id="04d99-135">See also</span></span>



[<span data-ttu-id="04d99-136">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="04d99-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="04d99-137">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="04d99-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="04d99-138">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="04d99-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="04d99-139">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="04d99-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

