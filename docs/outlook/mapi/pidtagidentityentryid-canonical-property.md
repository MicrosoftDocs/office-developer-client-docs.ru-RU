---
title: Каноническое свойство PidTagIdentityEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIdentityEntryId
api_type:
- HeaderDef
ms.assetid: 61a9d403-e0e5-45c3-8d18-4d53207ab927
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e724cc727292158fab26495e5d627b42dfe00daa
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811204"
---
# <a name="pidtagidentityentryid-canonical-property"></a><span data-ttu-id="172d8-103">Каноническое свойство PidTagIdentityEntryId</span><span class="sxs-lookup"><span data-stu-id="172d8-103">PidTagIdentityEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="172d8-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="172d8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="172d8-105">Содержит идентификатор записи для поставщика услуг удостоверения, как определено в системе обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="172d8-105">Contains the entry identifier for a service provider's identity as defined within a messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="172d8-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="172d8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="172d8-107">PR_IDENTITY_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="172d8-107">PR_IDENTITY_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="172d8-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="172d8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="172d8-109">0x3E01</span><span class="sxs-lookup"><span data-stu-id="172d8-109">0x3E01</span></span>  <br/> |
|<span data-ttu-id="172d8-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="172d8-110">Data type:</span></span>  <br/> |<span data-ttu-id="172d8-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="172d8-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="172d8-112">Область:</span><span class="sxs-lookup"><span data-stu-id="172d8-112">Area:</span></span>  <br/> |<span data-ttu-id="172d8-113">Состояние MAPI</span><span class="sxs-lookup"><span data-stu-id="172d8-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="172d8-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="172d8-114">Remarks</span></span>

<span data-ttu-id="172d8-115">Это свойство не отображается как свойство для любого объекта, но только в виде столбцов в таблице состояния.</span><span class="sxs-lookup"><span data-stu-id="172d8-115">This property does not appear as a property on any object but only as a column in a status table.</span></span> <span data-ttu-id="172d8-116">Он является частью идентификатор поставщика услуг, предоставление в строке состояния в таблице.</span><span class="sxs-lookup"><span data-stu-id="172d8-116">It is part of the identity of the service provider exposing the status table row.</span></span> <span data-ttu-id="172d8-117">Поставщик удостоверений обычно относится к его учетной записи на сервере, но можно ссылаться на любое представление, которое определяет поставщик в системе обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="172d8-117">The provider's identity typically refers to its account on the server, but can refer to any representation the provider defines within the messaging system.</span></span> 
  
<span data-ttu-id="172d8-118">В этом proprerty обычно имеет значение идентификатор записи соответствующие адресной книги.</span><span class="sxs-lookup"><span data-stu-id="172d8-118">This proprerty is commonly set to the appropriate address book entry identifier.</span></span> 
  
<span data-ttu-id="172d8-119">Поставщик службы передачи Свойства identity должны предоставлять все из них.</span><span class="sxs-lookup"><span data-stu-id="172d8-119">A service provider furnishing any of the identity properties should furnish all of them.</span></span> <span data-ttu-id="172d8-120">Поставщики, относящихся к одной службы сообщения должны предоставлять те же значения для свойства identity.</span><span class="sxs-lookup"><span data-stu-id="172d8-120">Providers that belong to the same message service should expose the same values for the identity properties.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="172d8-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="172d8-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="172d8-122">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="172d8-122">Header files</span></span>

<span data-ttu-id="172d8-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="172d8-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="172d8-124">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="172d8-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="172d8-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="172d8-125">Mapitags.h</span></span>
  
> <span data-ttu-id="172d8-126">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="172d8-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="172d8-127">См. также</span><span class="sxs-lookup"><span data-stu-id="172d8-127">See also</span></span>



[<span data-ttu-id="172d8-128">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="172d8-128">IMAPISession::QueryIdentity</span></span>](imapisession-queryidentity.md)


[<span data-ttu-id="172d8-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="172d8-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="172d8-130">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="172d8-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="172d8-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="172d8-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="172d8-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="172d8-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

