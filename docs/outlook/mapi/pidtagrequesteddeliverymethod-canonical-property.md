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
ms.openlocfilehash: f18d726c1b06a6fb7f79964165bbdb9074a6d4d7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571369"
---
# <a name="pidtagrequesteddeliverymethod-canonical-property"></a><span data-ttu-id="16668-103">Каноническое свойство PidTagRequestedDeliveryMethod</span><span class="sxs-lookup"><span data-stu-id="16668-103">PidTagRequestedDeliveryMethod Canonical Property</span></span>

  
  
<span data-ttu-id="16668-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="16668-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="16668-105">Это свойство содержит двоичные массив методы доставки (поставщиков услуг) в порядке предпочтения отправителя сообщения.</span><span class="sxs-lookup"><span data-stu-id="16668-105">This property contains a binary array of delivery methods (service providers), in the order of a message sender's preference.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="16668-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="16668-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="16668-107">PR_REQUESTED_DELIVERY_METHOD</span><span class="sxs-lookup"><span data-stu-id="16668-107">PR_REQUESTED_DELIVERY_METHOD</span></span>  <br/> |
|<span data-ttu-id="16668-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="16668-108">Identifier:</span></span>  <br/> |<span data-ttu-id="16668-109">0x0C18</span><span class="sxs-lookup"><span data-stu-id="16668-109">0x0C18</span></span>  <br/> |
|<span data-ttu-id="16668-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="16668-110">Data type:</span></span>  <br/> |<span data-ttu-id="16668-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="16668-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="16668-112">Область:</span><span class="sxs-lookup"><span data-stu-id="16668-112">Area:</span></span>  <br/> |<span data-ttu-id="16668-113">Получатель MAPI</span><span class="sxs-lookup"><span data-stu-id="16668-113">MAPI Recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="16668-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="16668-114">Remarks</span></span>

<span data-ttu-id="16668-115">Массива, содержащихся в списке это свойство состоит из идентификаторы ASN.1 для каждого из поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="16668-115">The array contained in the this property consists of ASN.1 identifiers for each of the service providers.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="16668-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="16668-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="16668-117">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="16668-117">Header files</span></span>

<span data-ttu-id="16668-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="16668-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="16668-119">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="16668-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="16668-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="16668-120">Mapitags.h</span></span>
  
> <span data-ttu-id="16668-121">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="16668-121">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="16668-122">См. также</span><span class="sxs-lookup"><span data-stu-id="16668-122">See also</span></span>



[<span data-ttu-id="16668-123">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="16668-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="16668-124">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="16668-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="16668-125">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="16668-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="16668-126">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="16668-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

