---
title: Каноническое свойство PidTagIdentitySearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIdentitySearchKey
api_type:
- HeaderDef
ms.assetid: 5fe55ba7-4ecd-4a43-ab5b-2ef595c2cdd9
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 5f5f5eaa41d6256bed69b2cd9a91208181d5bda1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346636"
---
# <a name="pidtagidentitysearchkey-canonical-property"></a><span data-ttu-id="5e5b3-103">Каноническое свойство PidTagIdentitySearchKey</span><span class="sxs-lookup"><span data-stu-id="5e5b3-103">PidTagIdentitySearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="5e5b3-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5e5b3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5e5b3-105">Содержит ключ поиска для удостоверения поставщика услуг в соответствии с определением в системе обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="5e5b3-105">Contains the search key for a service provider's identity as defined within a messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5e5b3-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="5e5b3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5e5b3-107">ПР_ИДЕНТИТИ_СЕАРЧ_КЭЙ</span><span class="sxs-lookup"><span data-stu-id="5e5b3-107">PR_IDENTITY_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="5e5b3-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="5e5b3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5e5b3-109">0x3E05</span><span class="sxs-lookup"><span data-stu-id="5e5b3-109">0x3E05</span></span>  <br/> |
|<span data-ttu-id="5e5b3-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="5e5b3-110">Data type:</span></span>  <br/> |<span data-ttu-id="5e5b3-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="5e5b3-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="5e5b3-112">Область:</span><span class="sxs-lookup"><span data-stu-id="5e5b3-112">Area:</span></span>  <br/> |<span data-ttu-id="5e5b3-113">Состояние MAPI</span><span class="sxs-lookup"><span data-stu-id="5e5b3-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5e5b3-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="5e5b3-114">Remarks</span></span>

<span data-ttu-id="5e5b3-115">Это свойство не отображается как свойство ни для одного объекта, но только как столбец в таблице "состояние".</span><span class="sxs-lookup"><span data-stu-id="5e5b3-115">This property does not appear as a property on any object but only as a column in a status table.</span></span> <span data-ttu-id="5e5b3-116">Он является частью удостоверения поставщика услуг, предоставляющего строку таблицы состояния.</span><span class="sxs-lookup"><span data-stu-id="5e5b3-116">It is part of the identity of the service provider exposing the status table row.</span></span> <span data-ttu-id="5e5b3-117">Удостоверение поставщика обычно относится к его учетной записи на сервере, но может ссылаться на любое представление, которое определяет поставщик в системе обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="5e5b3-117">The provider's identity typically refers to its account on the server, but can refer to any representation the provider defines within the messaging system.</span></span> 
  
<span data-ttu-id="5e5b3-118">Поставщик услуг, представляя любое из свойств Identity, должен отказаться от всех этих свойств.</span><span class="sxs-lookup"><span data-stu-id="5e5b3-118">A service provider furnishing any of the identity properties should furnish all of them.</span></span> <span data-ttu-id="5e5b3-119">Поставщики одной и той же службы сообщений должны предоставлять одни и те же значения для свойств Identity.</span><span class="sxs-lookup"><span data-stu-id="5e5b3-119">Providers that belong to the same message service should expose the same values for the identity properties.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="5e5b3-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="5e5b3-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="5e5b3-121">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="5e5b3-121">Header files</span></span>

<span data-ttu-id="5e5b3-122">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="5e5b3-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="5e5b3-123">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="5e5b3-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="5e5b3-124">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="5e5b3-124">Mapitags.h</span></span>
  
> <span data-ttu-id="5e5b3-125">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="5e5b3-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5e5b3-126">См. также</span><span class="sxs-lookup"><span data-stu-id="5e5b3-126">See also</span></span>



[<span data-ttu-id="5e5b3-127">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="5e5b3-127">IMAPISession::QueryIdentity</span></span>](imapisession-queryidentity.md)


[<span data-ttu-id="5e5b3-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="5e5b3-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5e5b3-129">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="5e5b3-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5e5b3-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="5e5b3-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5e5b3-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="5e5b3-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

