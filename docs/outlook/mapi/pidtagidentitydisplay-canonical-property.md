---
title: Каноническое свойство PidTagIdentityDisplay
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIdentityDisplay
api_type:
- HeaderDef
ms.assetid: ad9756c1-c1f9-4ab3-a58a-31e574dd9530
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6cfc4d6eab5b2f19bcfd4c7e2a8fc9fa1494afa4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585579"
---
# <a name="pidtagidentitydisplay-canonical-property"></a><span data-ttu-id="7eb3a-103">Каноническое свойство PidTagIdentityDisplay</span><span class="sxs-lookup"><span data-stu-id="7eb3a-103">PidTagIdentityDisplay Canonical Property</span></span>

  
  
<span data-ttu-id="7eb3a-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7eb3a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7eb3a-105">Содержит отображаемое имя для поставщика услуг удостоверения, как определено в системе обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="7eb3a-105">Contains the display name for a service provider's identity as defined within a messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7eb3a-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="7eb3a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7eb3a-107">PR_IDENTITY_DISPLAY, PR_IDENTITY_DISPLAY_A, PR_IDENTITY_DISPLAY_W</span><span class="sxs-lookup"><span data-stu-id="7eb3a-107">PR_IDENTITY_DISPLAY, PR_IDENTITY_DISPLAY_A, PR_IDENTITY_DISPLAY_W</span></span>  <br/> |
|<span data-ttu-id="7eb3a-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="7eb3a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7eb3a-109">0x3E00</span><span class="sxs-lookup"><span data-stu-id="7eb3a-109">0x3E00</span></span>  <br/> |
|<span data-ttu-id="7eb3a-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="7eb3a-110">Data type:</span></span>  <br/> |<span data-ttu-id="7eb3a-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7eb3a-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="7eb3a-112">Область:</span><span class="sxs-lookup"><span data-stu-id="7eb3a-112">Area:</span></span>  <br/> |<span data-ttu-id="7eb3a-113">Состояние MAPI</span><span class="sxs-lookup"><span data-stu-id="7eb3a-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7eb3a-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="7eb3a-114">Remarks</span></span>

<span data-ttu-id="7eb3a-115">Эти свойства не отображаются как свойства любого объекта, но только в виде столбцов в таблице состояния.</span><span class="sxs-lookup"><span data-stu-id="7eb3a-115">These properties do not appear as properties on any object but only as a column in a status table.</span></span> <span data-ttu-id="7eb3a-116">Он является частью идентификатор поставщика услуг, предоставление в строке состояния в таблице.</span><span class="sxs-lookup"><span data-stu-id="7eb3a-116">It is part of the identity of the service provider exposing the status table row.</span></span> <span data-ttu-id="7eb3a-117">Поставщик удостоверений обычно относится к его учетной записи на сервере, но можно ссылаться на любое представление, которое определяет поставщик в системе обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="7eb3a-117">The provider's identity typically refers to its account on the server, but can refer to any representation the provider defines within the messaging system.</span></span> 
  
<span data-ttu-id="7eb3a-118">Поставщик службы передачи Свойства identity должны предоставлять все из них.</span><span class="sxs-lookup"><span data-stu-id="7eb3a-118">A service provider furnishing any of the identity properties should furnish all of them.</span></span> <span data-ttu-id="7eb3a-119">Поставщики, относящихся к одной службы сообщения должны предоставлять те же значения для свойства identity.</span><span class="sxs-lookup"><span data-stu-id="7eb3a-119">Providers that belong to the same message service should expose the same values for the identity properties.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="7eb3a-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="7eb3a-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="7eb3a-121">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="7eb3a-121">Header files</span></span>

<span data-ttu-id="7eb3a-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7eb3a-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="7eb3a-123">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="7eb3a-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="7eb3a-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7eb3a-124">Mapitags.h</span></span>
  
> <span data-ttu-id="7eb3a-125">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="7eb3a-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7eb3a-126">См. также</span><span class="sxs-lookup"><span data-stu-id="7eb3a-126">See also</span></span>



[<span data-ttu-id="7eb3a-127">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="7eb3a-127">IMAPISession::QueryIdentity</span></span>](imapisession-queryidentity.md)


[<span data-ttu-id="7eb3a-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="7eb3a-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7eb3a-129">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="7eb3a-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7eb3a-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="7eb3a-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7eb3a-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="7eb3a-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

