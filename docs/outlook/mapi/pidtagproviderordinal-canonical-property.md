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
ms.openlocfilehash: 4cd865fbc443a20ebf4b4cd9722fe52c44d5eddc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573812"
---
# <a name="pidtagproviderordinal-canonical-property"></a><span data-ttu-id="9e286-103">Каноническое свойство PidTagProviderOrdinal</span><span class="sxs-lookup"><span data-stu-id="9e286-103">PidTagProviderOrdinal Canonical Property</span></span>

  
  
<span data-ttu-id="9e286-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9e286-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9e286-105">Содержит начинающийся с нуля индекс положения поставщика услуг в таблице поставщика.</span><span class="sxs-lookup"><span data-stu-id="9e286-105">Contains the zero-based index of a service provider's position in the provider table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9e286-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="9e286-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9e286-107">PR_PROVIDER_ORDINAL</span><span class="sxs-lookup"><span data-stu-id="9e286-107">PR_PROVIDER_ORDINAL</span></span>  <br/> |
|<span data-ttu-id="9e286-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="9e286-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9e286-109">0x300D</span><span class="sxs-lookup"><span data-stu-id="9e286-109">0x300D</span></span>  <br/> |
|<span data-ttu-id="9e286-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="9e286-110">Data type:</span></span>  <br/> |<span data-ttu-id="9e286-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="9e286-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="9e286-112">Область:</span><span class="sxs-lookup"><span data-stu-id="9e286-112">Area:</span></span>  <br/> |<span data-ttu-id="9e286-113">Распространенные MAPI</span><span class="sxs-lookup"><span data-stu-id="9e286-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9e286-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="9e286-114">Remarks</span></span>

<span data-ttu-id="9e286-115">Это свойство вычисляется путем MAPI.</span><span class="sxs-lookup"><span data-stu-id="9e286-115">This property is computed by MAPI.</span></span>
  
<span data-ttu-id="9e286-116">В таблице поставщика получите путем вызова метода [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) .</span><span class="sxs-lookup"><span data-stu-id="9e286-116">Obtain the provider table by calling the [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) method.</span></span> <span data-ttu-id="9e286-117">Сортировка в таблице поставщика для данного свойства для отображения порядка транспорта.</span><span class="sxs-lookup"><span data-stu-id="9e286-117">Sort the provider table on this property to display the transport order.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="9e286-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="9e286-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="9e286-119">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="9e286-119">Header files</span></span>

<span data-ttu-id="9e286-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9e286-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="9e286-121">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="9e286-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="9e286-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9e286-122">Mapitags.h</span></span>
  
> <span data-ttu-id="9e286-123">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="9e286-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9e286-124">См. также</span><span class="sxs-lookup"><span data-stu-id="9e286-124">See also</span></span>



[<span data-ttu-id="9e286-125">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="9e286-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9e286-126">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="9e286-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9e286-127">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="9e286-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9e286-128">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="9e286-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

