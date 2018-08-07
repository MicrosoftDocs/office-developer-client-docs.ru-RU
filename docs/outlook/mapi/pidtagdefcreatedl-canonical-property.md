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
ms.openlocfilehash: 3fb86fba3b0ff8a79858fad59dca61069aff6db9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811051"
---
# <a name="pidtagdefcreatedl-canonical-property"></a><span data-ttu-id="06f88-103">Каноническое свойство PidTagDefCreateDl</span><span class="sxs-lookup"><span data-stu-id="06f88-103">PidTagDefCreateDl Canonical Property</span></span>

  
  
<span data-ttu-id="06f88-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="06f88-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="06f88-105">Содержит идентификатор записи шаблона для списка рассылки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="06f88-105">Contains the template entry identifier for a default distribution list.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="06f88-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="06f88-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="06f88-107">PR_DEF_CREATE_DL</span><span class="sxs-lookup"><span data-stu-id="06f88-107">PR_DEF_CREATE_DL</span></span>  <br/> |
|<span data-ttu-id="06f88-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="06f88-108">Identifier:</span></span>  <br/> |<span data-ttu-id="06f88-109">0x3611</span><span class="sxs-lookup"><span data-stu-id="06f88-109">0x3611</span></span>  <br/> |
|<span data-ttu-id="06f88-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="06f88-110">Data type:</span></span>  <br/> |<span data-ttu-id="06f88-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="06f88-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="06f88-112">Область:</span><span class="sxs-lookup"><span data-stu-id="06f88-112">Area:</span></span>  <br/> |<span data-ttu-id="06f88-113">Адресная книга</span><span class="sxs-lookup"><span data-stu-id="06f88-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="06f88-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="06f88-114">Remarks</span></span>

<span data-ttu-id="06f88-115">Клиентские приложения используйте это свойство для создания списка рассылки в контейнере.</span><span class="sxs-lookup"><span data-stu-id="06f88-115">Client applications use this property to create a distribution list within a container.</span></span> <span data-ttu-id="06f88-116">Поддержка создания записи является необязательным для контейнеров адресной книги; те, которые не поддерживают не требуется для предоставления этого свойства.</span><span class="sxs-lookup"><span data-stu-id="06f88-116">Support of entry creation is optional for address book containers; those that do not support it are not required to expose this property.</span></span> 
  
<span data-ttu-id="06f88-117">Это свойство определяет записи, которые отображаются в свойстве **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) для списков рассылки.</span><span class="sxs-lookup"><span data-stu-id="06f88-117">This property specifies an entry that can appear in the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property for distribution lists.</span></span> <span data-ttu-id="06f88-118">После получения идентификатора клиента используется в вызов метода [IABContainer::CreateEntry](iabcontainer-createentry.md) .</span><span class="sxs-lookup"><span data-stu-id="06f88-118">After obtaining the identifier, the client uses it in a call to the [IABContainer::CreateEntry](iabcontainer-createentry.md) method.</span></span> <span data-ttu-id="06f88-119">Операция представляет шаблона для списка рассылки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="06f88-119">The entry represents the template for the default distribution list.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="06f88-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="06f88-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="06f88-121">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="06f88-121">Header files</span></span>

<span data-ttu-id="06f88-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="06f88-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="06f88-123">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="06f88-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="06f88-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="06f88-124">Mapitags.h</span></span>
  
> <span data-ttu-id="06f88-125">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="06f88-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="06f88-126">См. также</span><span class="sxs-lookup"><span data-stu-id="06f88-126">See also</span></span>



[<span data-ttu-id="06f88-127">IABLogon::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="06f88-127">IABLogon::CompareEntryIDs</span></span>](iablogon-compareentryids.md)


[<span data-ttu-id="06f88-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="06f88-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="06f88-129">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="06f88-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="06f88-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="06f88-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="06f88-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="06f88-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

