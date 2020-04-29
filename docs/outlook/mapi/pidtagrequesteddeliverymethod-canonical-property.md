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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434076"
---
# <a name="pidtagrequesteddeliverymethod-canonical-property"></a><span data-ttu-id="ccac7-103">Каноническое свойство PidTagRequestedDeliveryMethod</span><span class="sxs-lookup"><span data-stu-id="ccac7-103">PidTagRequestedDeliveryMethod Canonical Property</span></span>

  
  
<span data-ttu-id="ccac7-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ccac7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ccac7-105">Данное свойство содержит двоичный массив методов доставки (поставщиков услуг) в порядке предпочтения отправителя сообщения.</span><span class="sxs-lookup"><span data-stu-id="ccac7-105">This property contains a binary array of delivery methods (service providers), in the order of a message sender's preference.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ccac7-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="ccac7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ccac7-107">PR_REQUESTED_DELIVERY_METHOD</span><span class="sxs-lookup"><span data-stu-id="ccac7-107">PR_REQUESTED_DELIVERY_METHOD</span></span>  <br/> |
|<span data-ttu-id="ccac7-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="ccac7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ccac7-109">0x0C18</span><span class="sxs-lookup"><span data-stu-id="ccac7-109">0x0C18</span></span>  <br/> |
|<span data-ttu-id="ccac7-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="ccac7-110">Data type:</span></span>  <br/> |<span data-ttu-id="ccac7-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="ccac7-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="ccac7-112">Область:</span><span class="sxs-lookup"><span data-stu-id="ccac7-112">Area:</span></span>  <br/> |<span data-ttu-id="ccac7-113">Получатель MAPI</span><span class="sxs-lookup"><span data-stu-id="ccac7-113">MAPI Recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ccac7-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="ccac7-114">Remarks</span></span>

<span data-ttu-id="ccac7-115">Массив, содержащийся в этом свойстве, состоит из идентификаторов ASN. 1 для каждого поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="ccac7-115">The array contained in the this property consists of ASN.1 identifiers for each of the service providers.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ccac7-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ccac7-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="ccac7-117">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="ccac7-117">Header files</span></span>

<span data-ttu-id="ccac7-118">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="ccac7-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="ccac7-119">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="ccac7-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="ccac7-120">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="ccac7-120">Mapitags.h</span></span>
  
> <span data-ttu-id="ccac7-121">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="ccac7-121">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ccac7-122">См. также</span><span class="sxs-lookup"><span data-stu-id="ccac7-122">See also</span></span>



[<span data-ttu-id="ccac7-123">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ccac7-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ccac7-124">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="ccac7-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ccac7-125">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="ccac7-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ccac7-126">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="ccac7-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

