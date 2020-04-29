---
title: Каноническое свойство PidTagDefCreateDl
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefCreateDl
api_type:
- HeaderDef
ms.assetid: 172dc15b-7bda-403f-a93a-446b2f9ff1d3
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ff5d35104e9effc27c405b716cb61cf4643677b3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417793"
---
# <a name="pidtagdefcreatedl-canonical-property"></a><span data-ttu-id="f177d-103">Каноническое свойство PidTagDefCreateDl</span><span class="sxs-lookup"><span data-stu-id="f177d-103">PidTagDefCreateDl Canonical Property</span></span>

  
  
<span data-ttu-id="f177d-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f177d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f177d-105">Содержит идентификатор элемента шаблона для списка рассылки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f177d-105">Contains the template entry identifier for a default distribution list.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f177d-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="f177d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f177d-107">PR_DEF_CREATE_DL</span><span class="sxs-lookup"><span data-stu-id="f177d-107">PR_DEF_CREATE_DL</span></span>  <br/> |
|<span data-ttu-id="f177d-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="f177d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f177d-109">0x3611</span><span class="sxs-lookup"><span data-stu-id="f177d-109">0x3611</span></span>  <br/> |
|<span data-ttu-id="f177d-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="f177d-110">Data type:</span></span>  <br/> |<span data-ttu-id="f177d-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="f177d-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="f177d-112">Область:</span><span class="sxs-lookup"><span data-stu-id="f177d-112">Area:</span></span>  <br/> |<span data-ttu-id="f177d-113">Адресная книга</span><span class="sxs-lookup"><span data-stu-id="f177d-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f177d-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="f177d-114">Remarks</span></span>

<span data-ttu-id="f177d-115">Клиентские приложения используют это свойство для создания списка рассылки в контейнере.</span><span class="sxs-lookup"><span data-stu-id="f177d-115">Client applications use this property to create a distribution list within a container.</span></span> <span data-ttu-id="f177d-116">Поддержка создания записей является необязательной для контейнеров адресных книг; те, которые не поддерживают эту возможность, не являются обязательными для предоставления этого свойства.</span><span class="sxs-lookup"><span data-stu-id="f177d-116">Support of entry creation is optional for address book containers; those that do not support it are not required to expose this property.</span></span> 
  
<span data-ttu-id="f177d-117">Это свойство указывает запись, которая может отображаться в свойстве **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) для списков рассылки.</span><span class="sxs-lookup"><span data-stu-id="f177d-117">This property specifies an entry that can appear in the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property for distribution lists.</span></span> <span data-ttu-id="f177d-118">После получения идентификатора клиент использует его в вызове метода [иабконтаинер:: креатинтри](iabcontainer-createentry.md) .</span><span class="sxs-lookup"><span data-stu-id="f177d-118">After obtaining the identifier, the client uses it in a call to the [IABContainer::CreateEntry](iabcontainer-createentry.md) method.</span></span> <span data-ttu-id="f177d-119">Запись представляет шаблон для списка рассылки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f177d-119">The entry represents the template for the default distribution list.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f177d-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f177d-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="f177d-121">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="f177d-121">Header files</span></span>

<span data-ttu-id="f177d-122">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="f177d-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="f177d-123">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="f177d-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="f177d-124">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="f177d-124">Mapitags.h</span></span>
  
> <span data-ttu-id="f177d-125">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="f177d-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f177d-126">См. также</span><span class="sxs-lookup"><span data-stu-id="f177d-126">See also</span></span>



[<span data-ttu-id="f177d-127">IABLogon::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="f177d-127">IABLogon::CompareEntryIDs</span></span>](iablogon-compareentryids.md)


[<span data-ttu-id="f177d-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f177d-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f177d-129">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="f177d-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f177d-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="f177d-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f177d-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="f177d-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

