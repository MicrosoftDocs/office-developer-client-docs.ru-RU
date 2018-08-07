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
ms.openlocfilehash: 8a2199ee2bba8b3b41af7bf26de6cdd3d8d0956e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811737"
---
# <a name="pidtagrequesteddeliverymethod-canonical-property"></a><span data-ttu-id="04c6c-103">Каноническое свойство PidTagRequestedDeliveryMethod</span><span class="sxs-lookup"><span data-stu-id="04c6c-103">PidTagRequestedDeliveryMethod Canonical Property</span></span>

  
  
<span data-ttu-id="04c6c-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="04c6c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="04c6c-105">Это свойство содержит двоичные массив методы доставки (поставщиков услуг) в порядке предпочтения отправителя сообщения.</span><span class="sxs-lookup"><span data-stu-id="04c6c-105">This property contains a binary array of delivery methods (service providers), in the order of a message sender's preference.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="04c6c-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="04c6c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="04c6c-107">PR_REQUESTED_DELIVERY_METHOD</span><span class="sxs-lookup"><span data-stu-id="04c6c-107">PR_REQUESTED_DELIVERY_METHOD</span></span>  <br/> |
|<span data-ttu-id="04c6c-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="04c6c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="04c6c-109">0x0C18</span><span class="sxs-lookup"><span data-stu-id="04c6c-109">0x0C18</span></span>  <br/> |
|<span data-ttu-id="04c6c-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="04c6c-110">Data type:</span></span>  <br/> |<span data-ttu-id="04c6c-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="04c6c-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="04c6c-112">Область:</span><span class="sxs-lookup"><span data-stu-id="04c6c-112">Area:</span></span>  <br/> |<span data-ttu-id="04c6c-113">Получатель MAPI</span><span class="sxs-lookup"><span data-stu-id="04c6c-113">MAPI Recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="04c6c-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="04c6c-114">Remarks</span></span>

<span data-ttu-id="04c6c-115">Массива, содержащихся в списке это свойство состоит из идентификаторы ASN.1 для каждого из поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="04c6c-115">The array contained in the this property consists of ASN.1 identifiers for each of the service providers.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="04c6c-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="04c6c-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="04c6c-117">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="04c6c-117">Header files</span></span>

<span data-ttu-id="04c6c-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="04c6c-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="04c6c-119">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="04c6c-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="04c6c-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="04c6c-120">Mapitags.h</span></span>
  
> <span data-ttu-id="04c6c-121">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="04c6c-121">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="04c6c-122">См. также</span><span class="sxs-lookup"><span data-stu-id="04c6c-122">See also</span></span>



[<span data-ttu-id="04c6c-123">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="04c6c-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="04c6c-124">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="04c6c-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="04c6c-125">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="04c6c-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="04c6c-126">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="04c6c-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

