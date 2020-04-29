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
ms.openlocfilehash: d6e189f78dec2fc92f1804be93e7885b61734b03
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431423"
---
# <a name="pidtagidentitydisplay-canonical-property"></a><span data-ttu-id="667ac-103">Каноническое свойство PidTagIdentityDisplay</span><span class="sxs-lookup"><span data-stu-id="667ac-103">PidTagIdentityDisplay Canonical Property</span></span>

  
  
<span data-ttu-id="667ac-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="667ac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="667ac-105">Содержит отображаемое имя для удостоверения поставщика услуг в соответствии с определением в системе обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="667ac-105">Contains the display name for a service provider's identity as defined within a messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="667ac-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="667ac-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="667ac-107">PR_IDENTITY_DISPLAY, PR_IDENTITY_DISPLAY_A PR_IDENTITY_DISPLAY_W</span><span class="sxs-lookup"><span data-stu-id="667ac-107">PR_IDENTITY_DISPLAY, PR_IDENTITY_DISPLAY_A, PR_IDENTITY_DISPLAY_W</span></span>  <br/> |
|<span data-ttu-id="667ac-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="667ac-108">Identifier:</span></span>  <br/> |<span data-ttu-id="667ac-109">0x3E00</span><span class="sxs-lookup"><span data-stu-id="667ac-109">0x3E00</span></span>  <br/> |
|<span data-ttu-id="667ac-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="667ac-110">Data type:</span></span>  <br/> |<span data-ttu-id="667ac-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="667ac-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="667ac-112">Область:</span><span class="sxs-lookup"><span data-stu-id="667ac-112">Area:</span></span>  <br/> |<span data-ttu-id="667ac-113">Состояние MAPI</span><span class="sxs-lookup"><span data-stu-id="667ac-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="667ac-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="667ac-114">Remarks</span></span>

<span data-ttu-id="667ac-115">Эти свойства не отображаются как свойства ни в одном объекте, но только в виде столбца в таблице состояния.</span><span class="sxs-lookup"><span data-stu-id="667ac-115">These properties do not appear as properties on any object but only as a column in a status table.</span></span> <span data-ttu-id="667ac-116">Он является частью удостоверения поставщика услуг, предоставляющего строку таблицы состояния.</span><span class="sxs-lookup"><span data-stu-id="667ac-116">It is part of the identity of the service provider exposing the status table row.</span></span> <span data-ttu-id="667ac-117">Удостоверение поставщика обычно относится к его учетной записи на сервере, но может ссылаться на любое представление, которое определяет поставщик в системе обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="667ac-117">The provider's identity typically refers to its account on the server, but can refer to any representation the provider defines within the messaging system.</span></span> 
  
<span data-ttu-id="667ac-118">Поставщик услуг, представляя любое из свойств Identity, должен отказаться от всех этих свойств.</span><span class="sxs-lookup"><span data-stu-id="667ac-118">A service provider furnishing any of the identity properties should furnish all of them.</span></span> <span data-ttu-id="667ac-119">Поставщики одной и той же службы сообщений должны предоставлять одни и те же значения для свойств Identity.</span><span class="sxs-lookup"><span data-stu-id="667ac-119">Providers that belong to the same message service should expose the same values for the identity properties.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="667ac-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="667ac-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="667ac-121">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="667ac-121">Header files</span></span>

<span data-ttu-id="667ac-122">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="667ac-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="667ac-123">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="667ac-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="667ac-124">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="667ac-124">Mapitags.h</span></span>
  
> <span data-ttu-id="667ac-125">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="667ac-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="667ac-126">См. также</span><span class="sxs-lookup"><span data-stu-id="667ac-126">See also</span></span>



[<span data-ttu-id="667ac-127">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="667ac-127">IMAPISession::QueryIdentity</span></span>](imapisession-queryidentity.md)


[<span data-ttu-id="667ac-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="667ac-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="667ac-129">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="667ac-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="667ac-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="667ac-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="667ac-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="667ac-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

