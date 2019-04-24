---
title: Каноническое свойство PidTagDefCreateMailuser
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefCreateMailuser
api_type:
- HeaderDef
ms.assetid: e8293dc9-f2f1-4065-89f4-e734a8db63df
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: cd09c85e4f44bbea29807d72a273ccf6980ca6df
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32269988"
---
# <a name="pidtagdefcreatemailuser-canonical-property"></a><span data-ttu-id="8c7fc-103">Каноническое свойство PidTagDefCreateMailuser</span><span class="sxs-lookup"><span data-stu-id="8c7fc-103">PidTagDefCreateMailuser Canonical Property</span></span>

  
  
<span data-ttu-id="8c7fc-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8c7fc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8c7fc-105">Содержит идентификатор элемента шаблона для объекта пользователя, используемого по умолчанию для обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="8c7fc-105">Contains the template entry identifier for a default messaging user object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8c7fc-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="8c7fc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8c7fc-107">ПР_ДЕФ_КРЕАТЕ_МАИЛУСЕР</span><span class="sxs-lookup"><span data-stu-id="8c7fc-107">PR_DEF_CREATE_MAILUSER</span></span>  <br/> |
|<span data-ttu-id="8c7fc-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="8c7fc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8c7fc-109">0x3612</span><span class="sxs-lookup"><span data-stu-id="8c7fc-109">0x3612</span></span>  <br/> |
|<span data-ttu-id="8c7fc-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="8c7fc-110">Data type:</span></span>  <br/> |<span data-ttu-id="8c7fc-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="8c7fc-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="8c7fc-112">Область:</span><span class="sxs-lookup"><span data-stu-id="8c7fc-112">Area:</span></span>  <br/> |<span data-ttu-id="8c7fc-113">Адресная книга</span><span class="sxs-lookup"><span data-stu-id="8c7fc-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8c7fc-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="8c7fc-114">Remarks</span></span>

<span data-ttu-id="8c7fc-115">Клиентские приложения используют это свойство, чтобы создать объект пользователя для обмена сообщениями в контейнере.</span><span class="sxs-lookup"><span data-stu-id="8c7fc-115">Client applications use this property to create a messaging user object within a container.</span></span> <span data-ttu-id="8c7fc-116">Поддержка создания записей является необязательной для контейнеров адресных книг; те, которые не поддерживают эту возможность, не являются обязательными для предоставления этого свойства.</span><span class="sxs-lookup"><span data-stu-id="8c7fc-116">Support of entry creation is optional for address book containers; those that do not support it are not required to expose this property.</span></span> 
  
<span data-ttu-id="8c7fc-117">Это свойство указывает запись, которая может отображаться в свойстве **пр_креате_темплатес** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) для пользователей системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="8c7fc-117">This property specifies an entry that can appear in the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property for messaging users.</span></span> <span data-ttu-id="8c7fc-118">После получения идентификатора клиент использует его в вызове метода [иабконтаинер:: креатинтри](iabcontainer-createentry.md) .</span><span class="sxs-lookup"><span data-stu-id="8c7fc-118">After obtaining the identifier, the client uses it in a call to the [IABContainer::CreateEntry](iabcontainer-createentry.md) method.</span></span> <span data-ttu-id="8c7fc-119">Запись представляет шаблон для пользователя обмена сообщениями по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8c7fc-119">The entry represents the template for the default messaging user.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="8c7fc-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="8c7fc-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="8c7fc-121">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="8c7fc-121">Header files</span></span>

<span data-ttu-id="8c7fc-122">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="8c7fc-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="8c7fc-123">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="8c7fc-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="8c7fc-124">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="8c7fc-124">Mapitags.h</span></span>
  
> <span data-ttu-id="8c7fc-125">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="8c7fc-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8c7fc-126">См. также</span><span class="sxs-lookup"><span data-stu-id="8c7fc-126">See also</span></span>



[<span data-ttu-id="8c7fc-127">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8c7fc-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8c7fc-128">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="8c7fc-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8c7fc-129">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="8c7fc-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8c7fc-130">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="8c7fc-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

