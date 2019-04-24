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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342618"
---
# <a name="pidtagoriginalsenderentryid-canonical-property"></a><span data-ttu-id="5b380-103">Каноническое свойство PidTagOriginalSenderEntryId</span><span class="sxs-lookup"><span data-stu-id="5b380-103">PidTagOriginalSenderEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="5b380-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5b380-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5b380-105">Содержит идентификатор отправителя первой версии сообщения, то есть сообщение перед пересылкой или ответом.</span><span class="sxs-lookup"><span data-stu-id="5b380-105">Contains the entry identifier of the sender of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5b380-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="5b380-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5b380-107">ПР_ОРИГИНАЛ_СЕНДЕР_ЕНТРИД</span><span class="sxs-lookup"><span data-stu-id="5b380-107">PR_ORIGINAL_SENDER_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="5b380-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="5b380-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5b380-109">0x005B</span><span class="sxs-lookup"><span data-stu-id="5b380-109">0x005B</span></span>  <br/> |
|<span data-ttu-id="5b380-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="5b380-110">Data type:</span></span>  <br/> |<span data-ttu-id="5b380-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="5b380-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="5b380-112">Область:</span><span class="sxs-lookup"><span data-stu-id="5b380-112">Area:</span></span>  <br/> |<span data-ttu-id="5b380-113">Общий обмен сообщениями</span><span class="sxs-lookup"><span data-stu-id="5b380-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5b380-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5b380-114">Remarks</span></span>

<span data-ttu-id="5b380-115">Это свойство является одним из свойств адреса исходного отправителя сообщения.</span><span class="sxs-lookup"><span data-stu-id="5b380-115">This property is one of the address properties for the original sender of a message.</span></span> <span data-ttu-id="5b380-116">При первой отправке сообщения клиентскому приложению следует задать для этого свойства значение свойства **пр_сендер_ентрид** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="5b380-116">At first submission of the message, a client application should set this property to the value of the **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="5b380-117">Он никогда не изменяется при пересылке сообщения или ответе на него.</span><span class="sxs-lookup"><span data-stu-id="5b380-117">It is never changed when the message is forwarded or replied to.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5b380-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="5b380-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5b380-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="5b380-119">Protocol specifications</span></span>

<span data-ttu-id="5b380-120">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5b380-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5b380-121">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="5b380-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5b380-122">[[MS — ОКСОМСГ]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5b380-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5b380-123">Задает свойства и операции, допустимые для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="5b380-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5b380-124">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="5b380-124">Header files</span></span>

<span data-ttu-id="5b380-125">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="5b380-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="5b380-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="5b380-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="5b380-127">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="5b380-127">Mapitags.h</span></span>
  
> <span data-ttu-id="5b380-128">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="5b380-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5b380-129">См. также</span><span class="sxs-lookup"><span data-stu-id="5b380-129">See also</span></span>



[<span data-ttu-id="5b380-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="5b380-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5b380-131">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="5b380-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5b380-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="5b380-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5b380-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="5b380-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

