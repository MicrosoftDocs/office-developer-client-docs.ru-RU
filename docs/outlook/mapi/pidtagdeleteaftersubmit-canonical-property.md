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
ms.openlocfilehash: 2708d89e2572e8820de0b525b4f53ccd309ae2a0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359916"
---
# <a name="pidtagdeleteaftersubmit-canonical-property"></a><span data-ttu-id="8f53a-103">Каноническое свойство PidTagDeleteAfterSubmit</span><span class="sxs-lookup"><span data-stu-id="8f53a-103">PidTagDeleteAfterSubmit Canonical Property</span></span>

  
  
<span data-ttu-id="8f53a-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8f53a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8f53a-105">Содержит значение TRUE, если клиентскому приложению требуется MAPI удалить связанное сообщение после отправки.</span><span class="sxs-lookup"><span data-stu-id="8f53a-105">Contains TRUE if a client application wants MAPI to delete the associated message after submission.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8f53a-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="8f53a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8f53a-107">PR_DELETE_AFTER_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="8f53a-107">PR_DELETE_AFTER_SUBMIT</span></span>  <br/> |
|<span data-ttu-id="8f53a-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="8f53a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8f53a-109">0x0E01</span><span class="sxs-lookup"><span data-stu-id="8f53a-109">0x0E01</span></span>  <br/> |
|<span data-ttu-id="8f53a-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="8f53a-110">Data type:</span></span>  <br/> |<span data-ttu-id="8f53a-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="8f53a-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="8f53a-112">Область:</span><span class="sxs-lookup"><span data-stu-id="8f53a-112">Area:</span></span>  <br/> |<span data-ttu-id="8f53a-113">Несъемный MAPI</span><span class="sxs-lookup"><span data-stu-id="8f53a-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8f53a-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="8f53a-114">Remarks</span></span>

<span data-ttu-id="8f53a-115">Клиентское приложение использует это свойство со свойством **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)), чтобы контролировать, что происходит с сообщением после его отправки.</span><span class="sxs-lookup"><span data-stu-id="8f53a-115">A client application uses this property with the **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) property to control what happens to a message after it is submitted.</span></span> <span data-ttu-id="8f53a-116">Необходимо задать либо один, либо другой, но не оба варианта.</span><span class="sxs-lookup"><span data-stu-id="8f53a-116">Either one or the other should be set, but not both.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="8f53a-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="8f53a-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8f53a-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="8f53a-118">Protocol specifications</span></span>

<span data-ttu-id="8f53a-119">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8f53a-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8f53a-120">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="8f53a-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8f53a-121">[[MS — ОКСКСТОР]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8f53a-121">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8f53a-122">Указывает допустимые операции для основных объектов хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="8f53a-122">Specifies permissible operations for the core message store objects.</span></span>
    
<span data-ttu-id="8f53a-123">[[MS — ОКСОМСГ]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8f53a-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8f53a-124">Задает свойства и операции, допустимые для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="8f53a-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8f53a-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="8f53a-125">Header files</span></span>

<span data-ttu-id="8f53a-126">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="8f53a-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="8f53a-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="8f53a-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="8f53a-128">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="8f53a-128">Mapitags.h</span></span>
  
> <span data-ttu-id="8f53a-129">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="8f53a-129">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8f53a-130">См. также</span><span class="sxs-lookup"><span data-stu-id="8f53a-130">See also</span></span>



[<span data-ttu-id="8f53a-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8f53a-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8f53a-132">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="8f53a-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8f53a-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="8f53a-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8f53a-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="8f53a-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

