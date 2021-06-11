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
ms.openlocfilehash: 723affa054cb35a9cc7a2ee28e051e3b9a6d04e0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329402"
---
# <a name="pidtagmessagesubmissionid-canonical-property"></a><span data-ttu-id="a44cb-103">Каноническое свойство PidTagMessageSubmissionId</span><span class="sxs-lookup"><span data-stu-id="a44cb-103">PidTagMessageSubmissionId Canonical Property</span></span>

  
  
<span data-ttu-id="a44cb-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a44cb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a44cb-105">Содержит идентификатор системы передачи сообщений (MTS) для агента передачи сообщений (MTA).</span><span class="sxs-lookup"><span data-stu-id="a44cb-105">Contains a message transfer system (MTS) identifier for the message transfer agent (MTA).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a44cb-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="a44cb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a44cb-107">PR_MESSAGE_SUBMISSION_ID</span><span class="sxs-lookup"><span data-stu-id="a44cb-107">PR_MESSAGE_SUBMISSION_ID</span></span>  <br/> |
|<span data-ttu-id="a44cb-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="a44cb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a44cb-109">0x0047</span><span class="sxs-lookup"><span data-stu-id="a44cb-109">0x0047</span></span>  <br/> |
|<span data-ttu-id="a44cb-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="a44cb-110">Data type:</span></span>  <br/> |<span data-ttu-id="a44cb-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="a44cb-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="a44cb-112">Область:</span><span class="sxs-lookup"><span data-stu-id="a44cb-112">Area:</span></span>  <br/> |<span data-ttu-id="a44cb-113">Электронная почта</span><span class="sxs-lookup"><span data-stu-id="a44cb-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a44cb-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="a44cb-114">Remarks</span></span>

<span data-ttu-id="a44cb-115">Это свойство возвращается MTA после успешного завершения отправки сообщений.</span><span class="sxs-lookup"><span data-stu-id="a44cb-115">This property is returned by the MTA upon successful completion of message submission.</span></span> <span data-ttu-id="a44cb-116">Любой будущий контакт с MTA по этому сообщению, например запрос отмены, использует идентификатор МТС в этом свойстве.</span><span class="sxs-lookup"><span data-stu-id="a44cb-116">Any future contact with the MTA regarding this message, such as requesting cancellation, uses the MTS identifier in this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a44cb-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="a44cb-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a44cb-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="a44cb-118">Protocol specifications</span></span>

<span data-ttu-id="a44cb-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a44cb-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a44cb-120">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="a44cb-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a44cb-121">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a44cb-121">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a44cb-122">Кодирует и декодирует объекты сообщений и вложений в эффективное представление потока.</span><span class="sxs-lookup"><span data-stu-id="a44cb-122">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a44cb-123">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="a44cb-123">Header files</span></span>

<span data-ttu-id="a44cb-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a44cb-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="a44cb-125">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="a44cb-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="a44cb-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a44cb-126">Mapitags.h</span></span>
  
> <span data-ttu-id="a44cb-127">Содержит определения свойств, перечисленных в качестве связанных свойств.</span><span class="sxs-lookup"><span data-stu-id="a44cb-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a44cb-128">См. также</span><span class="sxs-lookup"><span data-stu-id="a44cb-128">See also</span></span>



[<span data-ttu-id="a44cb-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a44cb-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a44cb-130">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a44cb-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a44cb-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="a44cb-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a44cb-132">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="a44cb-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

