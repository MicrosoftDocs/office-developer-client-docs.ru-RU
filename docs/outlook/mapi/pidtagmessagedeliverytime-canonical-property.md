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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325615"
---
# <a name="pidtagmessagedeliverytime-canonical-property"></a><span data-ttu-id="dadf2-103">Каноническое свойство PidTagMessageDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="dadf2-103">PidTagMessageDeliveryTime Canonical Property</span></span>

  
  
<span data-ttu-id="dadf2-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dadf2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dadf2-105">Содержит дату и время доставки сообщения.</span><span class="sxs-lookup"><span data-stu-id="dadf2-105">Contains the date and time when a message was delivered.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dadf2-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="dadf2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="dadf2-107">ПР_МЕССАЖЕ_ДЕЛИВЕРИ_ТИМЕ</span><span class="sxs-lookup"><span data-stu-id="dadf2-107">PR_MESSAGE_DELIVERY_TIME</span></span>  <br/> |
|<span data-ttu-id="dadf2-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="dadf2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="dadf2-109">0x0E06</span><span class="sxs-lookup"><span data-stu-id="dadf2-109">0x0E06</span></span>  <br/> |
|<span data-ttu-id="dadf2-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="dadf2-110">Data type:</span></span>  <br/> |<span data-ttu-id="dadf2-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="dadf2-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="dadf2-112">Область:</span><span class="sxs-lookup"><span data-stu-id="dadf2-112">Area:</span></span>  <br/> |<span data-ttu-id="dadf2-113">Время сообщения</span><span class="sxs-lookup"><span data-stu-id="dadf2-113">Message time</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dadf2-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="dadf2-114">Remarks</span></span>

<span data-ttu-id="dadf2-115">Это свойство описывает время хранения сообщения на сервере, а не время загрузки, когда поставщик транспорта скопировал сообщение с сервера в локальное хранилище.</span><span class="sxs-lookup"><span data-stu-id="dadf2-115">This property describes the time the message was stored at the server, rather than the download time when the transport provider copied the message from the server to the local store.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="dadf2-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="dadf2-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="dadf2-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="dadf2-117">Protocol specifications</span></span>

<span data-ttu-id="dadf2-118">[[MS — ОКСОМСГ]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dadf2-118">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dadf2-119">Задает свойства и операции, допустимые для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="dadf2-119">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="dadf2-120">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="dadf2-120">Header files</span></span>

<span data-ttu-id="dadf2-121">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="dadf2-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="dadf2-122">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="dadf2-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="dadf2-123">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="dadf2-123">Mapitags.h</span></span>
  
> <span data-ttu-id="dadf2-124">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="dadf2-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dadf2-125">См. также</span><span class="sxs-lookup"><span data-stu-id="dadf2-125">See also</span></span>



[<span data-ttu-id="dadf2-126">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="dadf2-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="dadf2-127">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="dadf2-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="dadf2-128">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="dadf2-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="dadf2-129">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="dadf2-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

