---
title: Каноническое свойство PidTagRequestedDeliveryMethod
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRequestedDeliveryMethod
api_type:
- COM
ms.assetid: cc55089b-e389-405e-8174-f5b5ec352f78
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ecfed5684ba2166c1c00c1fd07fa074b4ce9fd79
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331418"
---
# <a name="pidtagrequesteddeliverymethod-canonical-property"></a><span data-ttu-id="921c3-103">Каноническое свойство PidTagRequestedDeliveryMethod</span><span class="sxs-lookup"><span data-stu-id="921c3-103">PidTagRequestedDeliveryMethod Canonical Property</span></span>

  
  
<span data-ttu-id="921c3-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="921c3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="921c3-105">Данное свойство содержит двоичный массив методов доставки (поставщиков услуг) в порядке предпочтения отправителя сообщения.</span><span class="sxs-lookup"><span data-stu-id="921c3-105">This property contains a binary array of delivery methods (service providers), in the order of a message sender's preference.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="921c3-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="921c3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="921c3-107">ПР_РЕКУЕСТЕД_ДЕЛИВЕРИ_МЕСОД</span><span class="sxs-lookup"><span data-stu-id="921c3-107">PR_REQUESTED_DELIVERY_METHOD</span></span>  <br/> |
|<span data-ttu-id="921c3-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="921c3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="921c3-109">0x0C18</span><span class="sxs-lookup"><span data-stu-id="921c3-109">0x0C18</span></span>  <br/> |
|<span data-ttu-id="921c3-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="921c3-110">Data type:</span></span>  <br/> |<span data-ttu-id="921c3-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="921c3-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="921c3-112">Область:</span><span class="sxs-lookup"><span data-stu-id="921c3-112">Area:</span></span>  <br/> |<span data-ttu-id="921c3-113">Получатель MAPI</span><span class="sxs-lookup"><span data-stu-id="921c3-113">MAPI Recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="921c3-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="921c3-114">Remarks</span></span>

<span data-ttu-id="921c3-115">Массив, содержащийся в этом свойстве, состоит из идентификаторов ASN. 1 для каждого поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="921c3-115">The array contained in the this property consists of ASN.1 identifiers for each of the service providers.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="921c3-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="921c3-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="921c3-117">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="921c3-117">Header files</span></span>

<span data-ttu-id="921c3-118">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="921c3-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="921c3-119">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="921c3-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="921c3-120">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="921c3-120">Mapitags.h</span></span>
  
> <span data-ttu-id="921c3-121">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="921c3-121">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="921c3-122">См. также</span><span class="sxs-lookup"><span data-stu-id="921c3-122">See also</span></span>



[<span data-ttu-id="921c3-123">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="921c3-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="921c3-124">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="921c3-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="921c3-125">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="921c3-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="921c3-126">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="921c3-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

