---
title: Каноническое свойство PidTagProviderOrdinal
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderOrdinal
api_type:
- COM
ms.assetid: d062b54d-7c32-4369-ab69-f7193773a1c0
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: fbeb63bbae23f8f7f78c92d3abed6bea1c3ac85d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438353"
---
# <a name="pidtagproviderordinal-canonical-property"></a><span data-ttu-id="dda87-103">Каноническое свойство PidTagProviderOrdinal</span><span class="sxs-lookup"><span data-stu-id="dda87-103">PidTagProviderOrdinal Canonical Property</span></span>

  
  
<span data-ttu-id="dda87-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dda87-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dda87-105">Содержит Отсчитываемый от нуля индекс положения поставщика услуг в таблице поставщика.</span><span class="sxs-lookup"><span data-stu-id="dda87-105">Contains the zero-based index of a service provider's position in the provider table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="dda87-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="dda87-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="dda87-107">PR_PROVIDER_ORDINAL</span><span class="sxs-lookup"><span data-stu-id="dda87-107">PR_PROVIDER_ORDINAL</span></span>  <br/> |
|<span data-ttu-id="dda87-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="dda87-108">Identifier:</span></span>  <br/> |<span data-ttu-id="dda87-109">0x300D</span><span class="sxs-lookup"><span data-stu-id="dda87-109">0x300D</span></span>  <br/> |
|<span data-ttu-id="dda87-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="dda87-110">Data type:</span></span>  <br/> |<span data-ttu-id="dda87-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="dda87-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="dda87-112">Область:</span><span class="sxs-lookup"><span data-stu-id="dda87-112">Area:</span></span>  <br/> |<span data-ttu-id="dda87-113">Общие протоколы MAPI</span><span class="sxs-lookup"><span data-stu-id="dda87-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dda87-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="dda87-114">Remarks</span></span>

<span data-ttu-id="dda87-115">Это свойство вычисляется MAPI.</span><span class="sxs-lookup"><span data-stu-id="dda87-115">This property is computed by MAPI.</span></span>
  
<span data-ttu-id="dda87-116">Получите таблицу поставщика, вызвав метод [имсгсервицеадмин:: жетпровидертабле](imsgserviceadmin-getprovidertable.md) .</span><span class="sxs-lookup"><span data-stu-id="dda87-116">Obtain the provider table by calling the [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) method.</span></span> <span data-ttu-id="dda87-117">В этом свойстве отсортируйте таблицу поставщика для отображения транспортного заказа.</span><span class="sxs-lookup"><span data-stu-id="dda87-117">Sort the provider table on this property to display the transport order.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="dda87-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="dda87-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="dda87-119">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="dda87-119">Header files</span></span>

<span data-ttu-id="dda87-120">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="dda87-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="dda87-121">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="dda87-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="dda87-122">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="dda87-122">Mapitags.h</span></span>
  
> <span data-ttu-id="dda87-123">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="dda87-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dda87-124">См. также</span><span class="sxs-lookup"><span data-stu-id="dda87-124">See also</span></span>



[<span data-ttu-id="dda87-125">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="dda87-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="dda87-126">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="dda87-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="dda87-127">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="dda87-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="dda87-128">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="dda87-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

