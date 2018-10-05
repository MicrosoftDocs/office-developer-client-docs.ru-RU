---
title: Каноническое свойство PidTagInternetMessageId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInternetMessageId
api_type:
- HeaderDef
ms.assetid: 5c93d00c-a199-4d45-9bf6-87bd2ffe4784
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c2cc0eabd9c329953d9b0d252418549ea1c588a1
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391929"
---
# <a name="pidtaginternetmessageid-canonical-property"></a><span data-ttu-id="f3863-103">Каноническое свойство PidTagInternetMessageId</span><span class="sxs-lookup"><span data-stu-id="f3863-103">PidTagInternetMessageId Canonical Property</span></span>

  
  
<span data-ttu-id="f3863-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f3863-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f3863-105">Соответствует поле идентификатор сообщения, как указано в [RFC2822].</span><span class="sxs-lookup"><span data-stu-id="f3863-105">Corresponds to the message ID field as specified in [RFC2822].</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f3863-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="f3863-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f3863-107">PR_INTERNET_MESSAGE_ID, PR_INTERNET_MESSAGE_ID_A, PR_INTERNET_MESSAGE_ID_W</span><span class="sxs-lookup"><span data-stu-id="f3863-107">PR_INTERNET_MESSAGE_ID, PR_INTERNET_MESSAGE_ID_A, PR_INTERNET_MESSAGE_ID_W</span></span>  <br/> |
|<span data-ttu-id="f3863-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="f3863-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f3863-109">0x1035</span><span class="sxs-lookup"><span data-stu-id="f3863-109">0x1035</span></span>  <br/> |
|<span data-ttu-id="f3863-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="f3863-110">Data type:</span></span>  <br/> |<span data-ttu-id="f3863-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f3863-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="f3863-112">Область:</span><span class="sxs-lookup"><span data-stu-id="f3863-112">Area:</span></span>  <br/> |<span data-ttu-id="f3863-113">MIME</span><span class="sxs-lookup"><span data-stu-id="f3863-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f3863-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="f3863-114">Remarks</span></span>

<span data-ttu-id="f3863-115">Эти свойства должны быть настроены на все сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="f3863-115">These properties should be present on all email messages.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f3863-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f3863-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f3863-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="f3863-117">Protocol specifications</span></span>

<span data-ttu-id="f3863-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f3863-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f3863-119">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="f3863-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f3863-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f3863-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f3863-121">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="f3863-121">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f3863-122">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="f3863-122">Header files</span></span>

<span data-ttu-id="f3863-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f3863-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="f3863-124">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="f3863-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="f3863-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f3863-125">Mapitags.h</span></span>
  
> <span data-ttu-id="f3863-126">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="f3863-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f3863-127">См. также</span><span class="sxs-lookup"><span data-stu-id="f3863-127">See also</span></span>



[<span data-ttu-id="f3863-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f3863-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f3863-129">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f3863-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f3863-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="f3863-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f3863-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="f3863-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

