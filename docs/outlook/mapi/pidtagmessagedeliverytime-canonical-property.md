---
title: Каноническое свойство PidTagMessageDeliveryTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageDeliveryTime
api_type:
- HeaderDef
ms.assetid: 4f9d44f2-4faa-4f16-9e33-22f80c17db85
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 8ebaea7fb6888e51ee1ef658db53dcf3050644da
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397347"
---
# <a name="pidtagmessagedeliverytime-canonical-property"></a><span data-ttu-id="06e3b-103">Каноническое свойство PidTagMessageDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="06e3b-103">PidTagMessageDeliveryTime Canonical Property</span></span>

  
  
<span data-ttu-id="06e3b-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="06e3b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="06e3b-105">Содержит дату и время, когда сообщение было доставлено.</span><span class="sxs-lookup"><span data-stu-id="06e3b-105">Contains the date and time when a message was delivered.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="06e3b-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="06e3b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="06e3b-107">PR_MESSAGE_DELIVERY_TIME</span><span class="sxs-lookup"><span data-stu-id="06e3b-107">PR_MESSAGE_DELIVERY_TIME</span></span>  <br/> |
|<span data-ttu-id="06e3b-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="06e3b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="06e3b-109">0x0E06</span><span class="sxs-lookup"><span data-stu-id="06e3b-109">0x0E06</span></span>  <br/> |
|<span data-ttu-id="06e3b-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="06e3b-110">Data type:</span></span>  <br/> |<span data-ttu-id="06e3b-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="06e3b-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="06e3b-112">Область:</span><span class="sxs-lookup"><span data-stu-id="06e3b-112">Area:</span></span>  <br/> |<span data-ttu-id="06e3b-113">Время сообщения</span><span class="sxs-lookup"><span data-stu-id="06e3b-113">Message time</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="06e3b-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="06e3b-114">Remarks</span></span>

<span data-ttu-id="06e3b-115">Это свойство указывает время, когда сообщение было сохранено на сервере, а не время загрузки, когда поставщика транспорта копируются сообщения с сервера в локальном хранилище.</span><span class="sxs-lookup"><span data-stu-id="06e3b-115">This property describes the time the message was stored at the server, rather than the download time when the transport provider copied the message from the server to the local store.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="06e3b-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="06e3b-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="06e3b-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="06e3b-117">Protocol specifications</span></span>

<span data-ttu-id="06e3b-118">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="06e3b-118">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="06e3b-119">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="06e3b-119">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="06e3b-120">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="06e3b-120">Header files</span></span>

<span data-ttu-id="06e3b-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="06e3b-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="06e3b-122">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="06e3b-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="06e3b-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="06e3b-123">Mapitags.h</span></span>
  
> <span data-ttu-id="06e3b-124">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="06e3b-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="06e3b-125">См. также</span><span class="sxs-lookup"><span data-stu-id="06e3b-125">See also</span></span>



[<span data-ttu-id="06e3b-126">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="06e3b-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="06e3b-127">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="06e3b-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="06e3b-128">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="06e3b-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="06e3b-129">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="06e3b-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

