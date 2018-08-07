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
ms.openlocfilehash: b3286e9e666d59997693df636263cb04f7b767d8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811389"
---
# <a name="pidtagmessagesubmissionid-canonical-property"></a><span data-ttu-id="621ee-103">Каноническое свойство PidTagMessageSubmissionId</span><span class="sxs-lookup"><span data-stu-id="621ee-103">PidTagMessageSubmissionId Canonical Property</span></span>

  
  
<span data-ttu-id="621ee-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="621ee-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="621ee-105">Содержит идентификатор система передачи сообщений для передачи сообщений (агента).</span><span class="sxs-lookup"><span data-stu-id="621ee-105">Contains a message transfer system (MTS) identifier for the message transfer agent (MTA).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="621ee-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="621ee-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="621ee-107">PR_MESSAGE_SUBMISSION_ID</span><span class="sxs-lookup"><span data-stu-id="621ee-107">PR_MESSAGE_SUBMISSION_ID</span></span>  <br/> |
|<span data-ttu-id="621ee-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="621ee-108">Identifier:</span></span>  <br/> |<span data-ttu-id="621ee-109">0x0047</span><span class="sxs-lookup"><span data-stu-id="621ee-109">0x0047</span></span>  <br/> |
|<span data-ttu-id="621ee-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="621ee-110">Data type:</span></span>  <br/> |<span data-ttu-id="621ee-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="621ee-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="621ee-112">Область:</span><span class="sxs-lookup"><span data-stu-id="621ee-112">Area:</span></span>  <br/> |<span data-ttu-id="621ee-113">Электронная почта</span><span class="sxs-lookup"><span data-stu-id="621ee-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="621ee-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="621ee-114">Remarks</span></span>

<span data-ttu-id="621ee-115">Данное свойство возвращает агента передачи сообщений при успешном выполнении отправки сообщений.</span><span class="sxs-lookup"><span data-stu-id="621ee-115">This property is returned by the MTA upon successful completion of message submission.</span></span> <span data-ttu-id="621ee-116">Дальнейших контактов с помощью агента передачи сообщений о сообщении, например запрашивающая отмены используется идентификатор MTS в этом свойстве.</span><span class="sxs-lookup"><span data-stu-id="621ee-116">Any future contact with the MTA regarding this message, such as requesting cancellation, uses the MTS identifier in this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="621ee-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="621ee-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="621ee-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="621ee-118">Protocol specifications</span></span>

<span data-ttu-id="621ee-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="621ee-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="621ee-120">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="621ee-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="621ee-121">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="621ee-121">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="621ee-122">Кодирует и декодирует объекты сообщения и вложения в представление эффективным потока.</span><span class="sxs-lookup"><span data-stu-id="621ee-122">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="621ee-123">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="621ee-123">Header files</span></span>

<span data-ttu-id="621ee-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="621ee-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="621ee-125">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="621ee-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="621ee-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="621ee-126">Mapitags.h</span></span>
  
> <span data-ttu-id="621ee-127">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="621ee-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="621ee-128">См. также</span><span class="sxs-lookup"><span data-stu-id="621ee-128">See also</span></span>



[<span data-ttu-id="621ee-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="621ee-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="621ee-130">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="621ee-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="621ee-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="621ee-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="621ee-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="621ee-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

