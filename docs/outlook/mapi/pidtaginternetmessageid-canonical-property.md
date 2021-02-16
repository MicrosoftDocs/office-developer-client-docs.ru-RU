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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358572"
---
# <a name="pidtaginternetmessageid-canonical-property"></a><span data-ttu-id="6c9d3-103">Каноническое свойство PidTagInternetMessageId</span><span class="sxs-lookup"><span data-stu-id="6c9d3-103">PidTagInternetMessageId Canonical Property</span></span>

  
  
<span data-ttu-id="6c9d3-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6c9d3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6c9d3-105">Соответствует полю "ИД сообщения", как указано в [RFC2822].</span><span class="sxs-lookup"><span data-stu-id="6c9d3-105">Corresponds to the message ID field as specified in [RFC2822].</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6c9d3-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="6c9d3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6c9d3-107">PR_INTERNET_MESSAGE_ID, PR_INTERNET_MESSAGE_ID_A, PR_INTERNET_MESSAGE_ID_W</span><span class="sxs-lookup"><span data-stu-id="6c9d3-107">PR_INTERNET_MESSAGE_ID, PR_INTERNET_MESSAGE_ID_A, PR_INTERNET_MESSAGE_ID_W</span></span>  <br/> |
|<span data-ttu-id="6c9d3-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="6c9d3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6c9d3-109">0x1035</span><span class="sxs-lookup"><span data-stu-id="6c9d3-109">0x1035</span></span>  <br/> |
|<span data-ttu-id="6c9d3-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="6c9d3-110">Data type:</span></span>  <br/> |<span data-ttu-id="6c9d3-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6c9d3-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="6c9d3-112">Область:</span><span class="sxs-lookup"><span data-stu-id="6c9d3-112">Area:</span></span>  <br/> |<span data-ttu-id="6c9d3-113">MIME</span><span class="sxs-lookup"><span data-stu-id="6c9d3-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6c9d3-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="6c9d3-114">Remarks</span></span>

<span data-ttu-id="6c9d3-115">Эти свойства должны присутствовать во всех сообщениях электронной почты.</span><span class="sxs-lookup"><span data-stu-id="6c9d3-115">These properties should be present on all email messages.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6c9d3-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="6c9d3-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6c9d3-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="6c9d3-117">Protocol specifications</span></span>

<span data-ttu-id="6c9d3-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6c9d3-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6c9d3-119">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="6c9d3-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6c9d3-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6c9d3-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6c9d3-121">Указывает свойства и операции, которые разрешены для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="6c9d3-121">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6c9d3-122">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="6c9d3-122">Header files</span></span>

<span data-ttu-id="6c9d3-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6c9d3-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="6c9d3-124">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="6c9d3-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="6c9d3-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6c9d3-125">Mapitags.h</span></span>
  
> <span data-ttu-id="6c9d3-126">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="6c9d3-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6c9d3-127">См. также</span><span class="sxs-lookup"><span data-stu-id="6c9d3-127">See also</span></span>



[<span data-ttu-id="6c9d3-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6c9d3-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6c9d3-129">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6c9d3-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6c9d3-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="6c9d3-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6c9d3-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="6c9d3-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

