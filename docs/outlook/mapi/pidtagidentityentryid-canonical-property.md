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
ms.openlocfilehash: a8810b6c39b909ebaa612496824150499cd15165
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584844"
---
# <a name="pidtagidentityentryid-canonical-property"></a><span data-ttu-id="e6034-103">Каноническое свойство PidTagIdentityEntryId</span><span class="sxs-lookup"><span data-stu-id="e6034-103">PidTagIdentityEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="e6034-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e6034-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e6034-105">Содержит идентификатор записи для поставщика услуг удостоверения, как определено в системе обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="e6034-105">Contains the entry identifier for a service provider's identity as defined within a messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e6034-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="e6034-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e6034-107">PR_IDENTITY_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="e6034-107">PR_IDENTITY_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="e6034-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="e6034-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e6034-109">0x3E01</span><span class="sxs-lookup"><span data-stu-id="e6034-109">0x3E01</span></span>  <br/> |
|<span data-ttu-id="e6034-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="e6034-110">Data type:</span></span>  <br/> |<span data-ttu-id="e6034-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="e6034-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="e6034-112">Область:</span><span class="sxs-lookup"><span data-stu-id="e6034-112">Area:</span></span>  <br/> |<span data-ttu-id="e6034-113">Состояние MAPI</span><span class="sxs-lookup"><span data-stu-id="e6034-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e6034-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="e6034-114">Remarks</span></span>

<span data-ttu-id="e6034-115">Это свойство не отображается как свойство для любого объекта, но только в виде столбцов в таблице состояния.</span><span class="sxs-lookup"><span data-stu-id="e6034-115">This property does not appear as a property on any object but only as a column in a status table.</span></span> <span data-ttu-id="e6034-116">Он является частью идентификатор поставщика услуг, предоставление в строке состояния в таблице.</span><span class="sxs-lookup"><span data-stu-id="e6034-116">It is part of the identity of the service provider exposing the status table row.</span></span> <span data-ttu-id="e6034-117">Поставщик удостоверений обычно относится к его учетной записи на сервере, но можно ссылаться на любое представление, которое определяет поставщик в системе обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="e6034-117">The provider's identity typically refers to its account on the server, but can refer to any representation the provider defines within the messaging system.</span></span> 
  
<span data-ttu-id="e6034-118">В этом proprerty обычно имеет значение идентификатор записи соответствующие адресной книги.</span><span class="sxs-lookup"><span data-stu-id="e6034-118">This proprerty is commonly set to the appropriate address book entry identifier.</span></span> 
  
<span data-ttu-id="e6034-119">Поставщик службы передачи Свойства identity должны предоставлять все из них.</span><span class="sxs-lookup"><span data-stu-id="e6034-119">A service provider furnishing any of the identity properties should furnish all of them.</span></span> <span data-ttu-id="e6034-120">Поставщики, относящихся к одной службы сообщения должны предоставлять те же значения для свойства identity.</span><span class="sxs-lookup"><span data-stu-id="e6034-120">Providers that belong to the same message service should expose the same values for the identity properties.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e6034-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="e6034-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="e6034-122">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="e6034-122">Header files</span></span>

<span data-ttu-id="e6034-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e6034-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="e6034-124">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="e6034-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="e6034-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e6034-125">Mapitags.h</span></span>
  
> <span data-ttu-id="e6034-126">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="e6034-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e6034-127">См. также</span><span class="sxs-lookup"><span data-stu-id="e6034-127">See also</span></span>



[<span data-ttu-id="e6034-128">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="e6034-128">IMAPISession::QueryIdentity</span></span>](imapisession-queryidentity.md)


[<span data-ttu-id="e6034-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="e6034-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e6034-130">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="e6034-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e6034-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="e6034-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e6034-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="e6034-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

