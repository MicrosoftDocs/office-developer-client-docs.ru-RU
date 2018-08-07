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
ms.openlocfilehash: b88fc54f1db26277d8a8d5e54fcff0ae164b0eac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811223"
---
# <a name="pidtagidentitydisplay-canonical-property"></a><span data-ttu-id="eeaa9-103">Каноническое свойство PidTagIdentityDisplay</span><span class="sxs-lookup"><span data-stu-id="eeaa9-103">PidTagIdentityDisplay Canonical Property</span></span>

  
  
<span data-ttu-id="eeaa9-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="eeaa9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="eeaa9-105">Содержит отображаемое имя для поставщика услуг удостоверения, как определено в системе обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="eeaa9-105">Contains the display name for a service provider's identity as defined within a messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="eeaa9-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="eeaa9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="eeaa9-107">PR_IDENTITY_DISPLAY, PR_IDENTITY_DISPLAY_A, PR_IDENTITY_DISPLAY_W</span><span class="sxs-lookup"><span data-stu-id="eeaa9-107">PR_IDENTITY_DISPLAY, PR_IDENTITY_DISPLAY_A, PR_IDENTITY_DISPLAY_W</span></span>  <br/> |
|<span data-ttu-id="eeaa9-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="eeaa9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="eeaa9-109">0x3E00</span><span class="sxs-lookup"><span data-stu-id="eeaa9-109">0x3E00</span></span>  <br/> |
|<span data-ttu-id="eeaa9-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="eeaa9-110">Data type:</span></span>  <br/> |<span data-ttu-id="eeaa9-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="eeaa9-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="eeaa9-112">Область:</span><span class="sxs-lookup"><span data-stu-id="eeaa9-112">Area:</span></span>  <br/> |<span data-ttu-id="eeaa9-113">Состояние MAPI</span><span class="sxs-lookup"><span data-stu-id="eeaa9-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="eeaa9-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="eeaa9-114">Remarks</span></span>

<span data-ttu-id="eeaa9-115">Эти свойства не отображаются как свойства любого объекта, но только в виде столбцов в таблице состояния.</span><span class="sxs-lookup"><span data-stu-id="eeaa9-115">These properties do not appear as properties on any object but only as a column in a status table.</span></span> <span data-ttu-id="eeaa9-116">Он является частью идентификатор поставщика услуг, предоставление в строке состояния в таблице.</span><span class="sxs-lookup"><span data-stu-id="eeaa9-116">It is part of the identity of the service provider exposing the status table row.</span></span> <span data-ttu-id="eeaa9-117">Поставщик удостоверений обычно относится к его учетной записи на сервере, но можно ссылаться на любое представление, которое определяет поставщик в системе обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="eeaa9-117">The provider's identity typically refers to its account on the server, but can refer to any representation the provider defines within the messaging system.</span></span> 
  
<span data-ttu-id="eeaa9-118">Поставщик службы передачи Свойства identity должны предоставлять все из них.</span><span class="sxs-lookup"><span data-stu-id="eeaa9-118">A service provider furnishing any of the identity properties should furnish all of them.</span></span> <span data-ttu-id="eeaa9-119">Поставщики, относящихся к одной службы сообщения должны предоставлять те же значения для свойства identity.</span><span class="sxs-lookup"><span data-stu-id="eeaa9-119">Providers that belong to the same message service should expose the same values for the identity properties.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="eeaa9-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="eeaa9-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="eeaa9-121">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="eeaa9-121">Header files</span></span>

<span data-ttu-id="eeaa9-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="eeaa9-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="eeaa9-123">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="eeaa9-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="eeaa9-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="eeaa9-124">Mapitags.h</span></span>
  
> <span data-ttu-id="eeaa9-125">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="eeaa9-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="eeaa9-126">См. также</span><span class="sxs-lookup"><span data-stu-id="eeaa9-126">See also</span></span>



[<span data-ttu-id="eeaa9-127">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="eeaa9-127">IMAPISession::QueryIdentity</span></span>](imapisession-queryidentity.md)


[<span data-ttu-id="eeaa9-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="eeaa9-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="eeaa9-129">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="eeaa9-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="eeaa9-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="eeaa9-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="eeaa9-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="eeaa9-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

