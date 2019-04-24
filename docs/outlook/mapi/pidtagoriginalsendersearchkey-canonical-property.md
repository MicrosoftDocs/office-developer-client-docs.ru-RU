---
title: Каноническое свойство PidTagOriginalSenderSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSenderSearchKey
api_type:
- COM
ms.assetid: 164eb9dd-e553-459e-99c1-3da0284bb01f
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 97ab08d3da3725187ef2d5c70bec80e9142bdd21
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342604"
---
# <a name="pidtagoriginalsendersearchkey-canonical-property"></a><span data-ttu-id="f9270-103">Каноническое свойство PidTagOriginalSenderSearchKey</span><span class="sxs-lookup"><span data-stu-id="f9270-103">PidTagOriginalSenderSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="f9270-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f9270-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f9270-105">Содержит ключ поиска для отправителя первой версии сообщения, то есть сообщение перед пересылкой или ответом.</span><span class="sxs-lookup"><span data-stu-id="f9270-105">Contains the search key for the sender of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f9270-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="f9270-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f9270-107">ПР_ОРИГИНАЛ_СЕНДЕР_СЕАРЧ_КЭЙ</span><span class="sxs-lookup"><span data-stu-id="f9270-107">PR_ORIGINAL_SENDER_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="f9270-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="f9270-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f9270-109">0x005C</span><span class="sxs-lookup"><span data-stu-id="f9270-109">0x005C</span></span>  <br/> |
|<span data-ttu-id="f9270-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="f9270-110">Data type:</span></span>  <br/> |<span data-ttu-id="f9270-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="f9270-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="f9270-112">Область:</span><span class="sxs-lookup"><span data-stu-id="f9270-112">Area:</span></span>  <br/> |<span data-ttu-id="f9270-113">Общий обмен сообщениями</span><span class="sxs-lookup"><span data-stu-id="f9270-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f9270-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f9270-114">Remarks</span></span>

<span data-ttu-id="f9270-115">Это свойство является одним из свойств адреса исходного отправителя сообщения.</span><span class="sxs-lookup"><span data-stu-id="f9270-115">This property is one of the address properties for the original sender of a message.</span></span> <span data-ttu-id="f9270-116">При первой отправке сообщения клиентскому приложению следует задать для этого свойства значение свойства **пр_сендер_сеарч_кэй** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="f9270-116">At first submission of the message, the client application should set this property to the value of the **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)) property.</span></span> <span data-ttu-id="f9270-117">Он никогда не изменяется при пересылке сообщения или ответе на него.</span><span class="sxs-lookup"><span data-stu-id="f9270-117">It is never changed when the message is forwarded or replied to.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f9270-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f9270-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f9270-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="f9270-119">Protocol specifications</span></span>

<span data-ttu-id="f9270-120">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f9270-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f9270-121">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="f9270-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f9270-122">[[MS — ОКСОМСГ]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f9270-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f9270-123">Задает свойства и операции, допустимые для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="f9270-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f9270-124">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="f9270-124">Header files</span></span>

<span data-ttu-id="f9270-125">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="f9270-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="f9270-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="f9270-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="f9270-127">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="f9270-127">Mapitags.h</span></span>
  
> <span data-ttu-id="f9270-128">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="f9270-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f9270-129">См. также</span><span class="sxs-lookup"><span data-stu-id="f9270-129">See also</span></span>



[<span data-ttu-id="f9270-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f9270-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f9270-131">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="f9270-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f9270-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="f9270-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f9270-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="f9270-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

