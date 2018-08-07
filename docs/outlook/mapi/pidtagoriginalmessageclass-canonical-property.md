---
title: Каноническое свойство PidTagOriginalMessageClass
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalMessageClass
api_type:
- COM
ms.assetid: 49deb153-03c6-4be2-a3a5-53cca01accba
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7167b7b51698cda5610356779a8e8342b34a6082
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811473"
---
# <a name="pidtagoriginalmessageclass-canonical-property"></a><span data-ttu-id="0639d-103">Каноническое свойство PidTagOriginalMessageClass</span><span class="sxs-lookup"><span data-stu-id="0639d-103">PidTagOriginalMessageClass Canonical Property</span></span>

  
  
<span data-ttu-id="0639d-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0639d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0639d-105">Содержит класс исходного сообщения для использования в отчете.</span><span class="sxs-lookup"><span data-stu-id="0639d-105">Contains the class of the original message for use in a report.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0639d-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="0639d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0639d-107">PR_ORIG_MESSAGE_CLASS, PR_ORIG_MESSAGE_CLASS_A, PR_ORIG_MESSAGE_CLASS_W</span><span class="sxs-lookup"><span data-stu-id="0639d-107">PR_ORIG_MESSAGE_CLASS, PR_ORIG_MESSAGE_CLASS_A, PR_ORIG_MESSAGE_CLASS_W</span></span>  <br/> |
|<span data-ttu-id="0639d-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="0639d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0639d-109">0x004B</span><span class="sxs-lookup"><span data-stu-id="0639d-109">0x004B</span></span>  <br/> |
|<span data-ttu-id="0639d-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="0639d-110">Data type:</span></span>  <br/> |<span data-ttu-id="0639d-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0639d-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="0639d-112">Область:</span><span class="sxs-lookup"><span data-stu-id="0639d-112">Area:</span></span>  <br/> |<span data-ttu-id="0639d-113">Безопасного обмена сообщениями свойства</span><span class="sxs-lookup"><span data-stu-id="0639d-113">Secure Messaging Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0639d-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="0639d-114">Remarks</span></span>

<span data-ttu-id="0639d-115">Эти свойства содержит копию свойство **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) сообщения, для которого создается отчет.</span><span class="sxs-lookup"><span data-stu-id="0639d-115">These properties contain a copy of the **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property of the message for which the report is being generated.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0639d-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="0639d-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0639d-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="0639d-117">Protocol specifications</span></span>

<span data-ttu-id="0639d-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0639d-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0639d-119">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="0639d-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0639d-120">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0639d-120">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0639d-121">Кодирует и декодирует объекты сообщения и вложения в представление эффективным потока.</span><span class="sxs-lookup"><span data-stu-id="0639d-121">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0639d-122">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="0639d-122">Header files</span></span>

<span data-ttu-id="0639d-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0639d-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="0639d-124">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="0639d-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="0639d-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0639d-125">Mapitags.h</span></span>
  
> <span data-ttu-id="0639d-126">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="0639d-126">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0639d-127">См. также</span><span class="sxs-lookup"><span data-stu-id="0639d-127">See also</span></span>



[<span data-ttu-id="0639d-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0639d-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0639d-129">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0639d-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0639d-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="0639d-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0639d-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="0639d-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

