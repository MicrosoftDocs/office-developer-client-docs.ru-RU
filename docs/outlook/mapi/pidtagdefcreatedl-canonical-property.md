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
# <a name="pidtagdefcreatedl-canonical-property"></a><span data-ttu-id="ce204-103">Каноническое свойство PidTagDefCreateDl</span><span class="sxs-lookup"><span data-stu-id="ce204-103">PidTagDefCreateDl Canonical Property</span></span>

  
  
<span data-ttu-id="ce204-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ce204-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ce204-105">Содержит идентификатор записи шаблона для списка рассылки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ce204-105">Contains the template entry identifier for a default distribution list.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ce204-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="ce204-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ce204-107">PR_DEF_CREATE_DL</span><span class="sxs-lookup"><span data-stu-id="ce204-107">PR_DEF_CREATE_DL</span></span>  <br/> |
|<span data-ttu-id="ce204-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="ce204-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ce204-109">0x3611</span><span class="sxs-lookup"><span data-stu-id="ce204-109">0x3611</span></span>  <br/> |
|<span data-ttu-id="ce204-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="ce204-110">Data type:</span></span>  <br/> |<span data-ttu-id="ce204-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="ce204-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="ce204-112">Область:</span><span class="sxs-lookup"><span data-stu-id="ce204-112">Area:</span></span>  <br/> |<span data-ttu-id="ce204-113">Адресная книга</span><span class="sxs-lookup"><span data-stu-id="ce204-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ce204-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="ce204-114">Remarks</span></span>

<span data-ttu-id="ce204-115">Клиентские приложения используют это свойство для создания списка рассылки в контейнере.</span><span class="sxs-lookup"><span data-stu-id="ce204-115">Client applications use this property to create a distribution list within a container.</span></span> <span data-ttu-id="ce204-116">Поддержка создания записей необязательна для контейнеров адресной книги; те, кто не поддерживает его, не обязаны выставлять это свойство.</span><span class="sxs-lookup"><span data-stu-id="ce204-116">Support of entry creation is optional for address book containers; those that do not support it are not required to expose this property.</span></span> 
  
<span data-ttu-id="ce204-117">Это свойство указывает запись, которая может отображаться в **свойстве PR_CREATE_TEMPLATES** [(PidTagCreateTemplates)](pidtagcreatetemplates-canonical-property.md)для списков рассылки.</span><span class="sxs-lookup"><span data-stu-id="ce204-117">This property specifies an entry that can appear in the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property for distribution lists.</span></span> <span data-ttu-id="ce204-118">После получения идентификатора клиент использует его в вызове метода [IABContainer::CreateEntry.](iabcontainer-createentry.md)</span><span class="sxs-lookup"><span data-stu-id="ce204-118">After obtaining the identifier, the client uses it in a call to the [IABContainer::CreateEntry](iabcontainer-createentry.md) method.</span></span> <span data-ttu-id="ce204-119">Запись представляет шаблон для списка рассылки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ce204-119">The entry represents the template for the default distribution list.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ce204-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ce204-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="ce204-121">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="ce204-121">Header files</span></span>

<span data-ttu-id="ce204-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ce204-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="ce204-123">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="ce204-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="ce204-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ce204-124">Mapitags.h</span></span>
  
> <span data-ttu-id="ce204-125">Содержит определения свойств, перечисленных в качестве связанных свойств.</span><span class="sxs-lookup"><span data-stu-id="ce204-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ce204-126">См. также</span><span class="sxs-lookup"><span data-stu-id="ce204-126">See also</span></span>



[<span data-ttu-id="ce204-127">IABLogon::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="ce204-127">IABLogon::CompareEntryIDs</span></span>](iablogon-compareentryids.md)


[<span data-ttu-id="ce204-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ce204-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ce204-129">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ce204-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ce204-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="ce204-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ce204-131">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="ce204-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

