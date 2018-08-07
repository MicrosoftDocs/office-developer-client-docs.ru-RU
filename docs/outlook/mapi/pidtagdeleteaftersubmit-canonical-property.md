---
title: Каноническое свойство PidTagDeleteAfterSubmit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeleteAfterSubmit
api_type:
- HeaderDef
ms.assetid: ba69a557-120c-4b1e-bbb7-0e901e7d1ebf
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7a63b3ad3c45790e043e1ea8e7d996c4847ef8d4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811041"
---
# <a name="pidtagdeleteaftersubmit-canonical-property"></a><span data-ttu-id="11858-103">Каноническое свойство PidTagDeleteAfterSubmit</span><span class="sxs-lookup"><span data-stu-id="11858-103">PidTagDeleteAfterSubmit Canonical Property</span></span>

  
  
<span data-ttu-id="11858-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="11858-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="11858-105">Содержит значение TRUE, если клиентское приложение, где требуется реализовать MAPI для удаления связанного сообщения после отправки.</span><span class="sxs-lookup"><span data-stu-id="11858-105">Contains TRUE if a client application wants MAPI to delete the associated message after submission.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="11858-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="11858-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="11858-107">PR_DELETE_AFTER_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="11858-107">PR_DELETE_AFTER_SUBMIT</span></span>  <br/> |
|<span data-ttu-id="11858-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="11858-108">Identifier:</span></span>  <br/> |<span data-ttu-id="11858-109">0x0E01</span><span class="sxs-lookup"><span data-stu-id="11858-109">0x0E01</span></span>  <br/> |
|<span data-ttu-id="11858-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="11858-110">Data type:</span></span>  <br/> |<span data-ttu-id="11858-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="11858-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="11858-112">Область:</span><span class="sxs-lookup"><span data-stu-id="11858-112">Area:</span></span>  <br/> |<span data-ttu-id="11858-113">MAPI передаваемого</span><span class="sxs-lookup"><span data-stu-id="11858-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="11858-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="11858-114">Remarks</span></span>

<span data-ttu-id="11858-115">Клиентское приложение использует это свойство со свойством **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) для управления, что происходит после ее отправки сообщения.</span><span class="sxs-lookup"><span data-stu-id="11858-115">A client application uses this property with the **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) property to control what happens to a message after it is submitted.</span></span> <span data-ttu-id="11858-116">Одно или другое должен быть набор, но не оба.</span><span class="sxs-lookup"><span data-stu-id="11858-116">Either one or the other should be set, but not both.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="11858-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="11858-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="11858-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="11858-118">Protocol specifications</span></span>

<span data-ttu-id="11858-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="11858-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="11858-120">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="11858-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="11858-121">[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="11858-121">[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="11858-122">Указывает допустимые операции для базовых объектов хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="11858-122">Specifies permissible operations for the core message store objects.</span></span>
    
<span data-ttu-id="11858-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="11858-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="11858-124">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="11858-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="11858-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="11858-125">Header files</span></span>

<span data-ttu-id="11858-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="11858-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="11858-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="11858-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="11858-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="11858-128">Mapitags.h</span></span>
  
> <span data-ttu-id="11858-129">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="11858-129">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="11858-130">См. также</span><span class="sxs-lookup"><span data-stu-id="11858-130">See also</span></span>



[<span data-ttu-id="11858-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="11858-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="11858-132">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="11858-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="11858-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="11858-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="11858-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="11858-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

