---
title: Каноническое свойство PidTagMessageSubmissionId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageSubmissionId
api_type:
- HeaderDef
ms.assetid: 0a799fe5-04e2-4e1d-b0cd-9bdd2577d299
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3a26a8483e584ccc5cf9f33e0dbd75f379c01633
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569668"
---
# <a name="pidtagmessagesubmissionid-canonical-property"></a><span data-ttu-id="4a99c-103">Каноническое свойство PidTagMessageSubmissionId</span><span class="sxs-lookup"><span data-stu-id="4a99c-103">PidTagMessageSubmissionId Canonical Property</span></span>

  
  
<span data-ttu-id="4a99c-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4a99c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4a99c-105">Содержит идентификатор система передачи сообщений для передачи сообщений (агента).</span><span class="sxs-lookup"><span data-stu-id="4a99c-105">Contains a message transfer system (MTS) identifier for the message transfer agent (MTA).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4a99c-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="4a99c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4a99c-107">PR_MESSAGE_SUBMISSION_ID</span><span class="sxs-lookup"><span data-stu-id="4a99c-107">PR_MESSAGE_SUBMISSION_ID</span></span>  <br/> |
|<span data-ttu-id="4a99c-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="4a99c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4a99c-109">0x0047</span><span class="sxs-lookup"><span data-stu-id="4a99c-109">0x0047</span></span>  <br/> |
|<span data-ttu-id="4a99c-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="4a99c-110">Data type:</span></span>  <br/> |<span data-ttu-id="4a99c-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="4a99c-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="4a99c-112">Область:</span><span class="sxs-lookup"><span data-stu-id="4a99c-112">Area:</span></span>  <br/> |<span data-ttu-id="4a99c-113">Электронная почта</span><span class="sxs-lookup"><span data-stu-id="4a99c-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4a99c-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="4a99c-114">Remarks</span></span>

<span data-ttu-id="4a99c-115">Данное свойство возвращает агента передачи сообщений при успешном выполнении отправки сообщений.</span><span class="sxs-lookup"><span data-stu-id="4a99c-115">This property is returned by the MTA upon successful completion of message submission.</span></span> <span data-ttu-id="4a99c-116">Дальнейших контактов с помощью агента передачи сообщений о сообщении, например запрашивающая отмены используется идентификатор MTS в этом свойстве.</span><span class="sxs-lookup"><span data-stu-id="4a99c-116">Any future contact with the MTA regarding this message, such as requesting cancellation, uses the MTS identifier in this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4a99c-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="4a99c-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4a99c-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="4a99c-118">Protocol specifications</span></span>

<span data-ttu-id="4a99c-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4a99c-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4a99c-120">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="4a99c-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4a99c-121">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4a99c-121">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4a99c-122">Кодирует и декодирует объекты сообщения и вложения в представление эффективным потока.</span><span class="sxs-lookup"><span data-stu-id="4a99c-122">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4a99c-123">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="4a99c-123">Header files</span></span>

<span data-ttu-id="4a99c-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4a99c-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="4a99c-125">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="4a99c-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="4a99c-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4a99c-126">Mapitags.h</span></span>
  
> <span data-ttu-id="4a99c-127">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="4a99c-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4a99c-128">См. также</span><span class="sxs-lookup"><span data-stu-id="4a99c-128">See also</span></span>



[<span data-ttu-id="4a99c-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="4a99c-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4a99c-130">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="4a99c-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4a99c-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="4a99c-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4a99c-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="4a99c-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

