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
# <a name="pidtagproviderordinal-canonical-property"></a><span data-ttu-id="56a1f-103">Каноническое свойство PidTagProviderOrdinal</span><span class="sxs-lookup"><span data-stu-id="56a1f-103">PidTagProviderOrdinal Canonical Property</span></span>

  
  
<span data-ttu-id="56a1f-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="56a1f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="56a1f-105">Содержит нулевой индекс позиции поставщика услуг в таблице поставщика.</span><span class="sxs-lookup"><span data-stu-id="56a1f-105">Contains the zero-based index of a service provider's position in the provider table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="56a1f-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="56a1f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="56a1f-107">PR_PROVIDER_ORDINAL</span><span class="sxs-lookup"><span data-stu-id="56a1f-107">PR_PROVIDER_ORDINAL</span></span>  <br/> |
|<span data-ttu-id="56a1f-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="56a1f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="56a1f-109">0x300D</span><span class="sxs-lookup"><span data-stu-id="56a1f-109">0x300D</span></span>  <br/> |
|<span data-ttu-id="56a1f-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="56a1f-110">Data type:</span></span>  <br/> |<span data-ttu-id="56a1f-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="56a1f-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="56a1f-112">Область:</span><span class="sxs-lookup"><span data-stu-id="56a1f-112">Area:</span></span>  <br/> |<span data-ttu-id="56a1f-113">MAPI общие</span><span class="sxs-lookup"><span data-stu-id="56a1f-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="56a1f-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="56a1f-114">Remarks</span></span>

<span data-ttu-id="56a1f-115">Это свойство вычисляется MAPI.</span><span class="sxs-lookup"><span data-stu-id="56a1f-115">This property is computed by MAPI.</span></span>
  
<span data-ttu-id="56a1f-116">Получение таблицы поставщика с помощью метода [IMsgServiceAdmin::GetProviderTable.](imsgserviceadmin-getprovidertable.md)</span><span class="sxs-lookup"><span data-stu-id="56a1f-116">Obtain the provider table by calling the [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) method.</span></span> <span data-ttu-id="56a1f-117">Сортировка таблицы поставщика в этом свойстве для отображения порядка транспортировки.</span><span class="sxs-lookup"><span data-stu-id="56a1f-117">Sort the provider table on this property to display the transport order.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="56a1f-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="56a1f-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="56a1f-119">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="56a1f-119">Header files</span></span>

<span data-ttu-id="56a1f-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="56a1f-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="56a1f-121">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="56a1f-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="56a1f-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="56a1f-122">Mapitags.h</span></span>
  
> <span data-ttu-id="56a1f-123">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="56a1f-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="56a1f-124">См. также</span><span class="sxs-lookup"><span data-stu-id="56a1f-124">See also</span></span>



[<span data-ttu-id="56a1f-125">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="56a1f-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="56a1f-126">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="56a1f-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="56a1f-127">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="56a1f-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="56a1f-128">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="56a1f-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

