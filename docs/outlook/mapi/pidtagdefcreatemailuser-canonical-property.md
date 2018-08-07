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
ms.openlocfilehash: 33c62b81982aaac3659ad4d41ea2cf5298b42287
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811044"
---
# <a name="pidtagdefcreatemailuser-canonical-property"></a><span data-ttu-id="16993-103">Каноническое свойство PidTagDefCreateMailuser</span><span class="sxs-lookup"><span data-stu-id="16993-103">PidTagDefCreateMailuser Canonical Property</span></span>

  
  
<span data-ttu-id="16993-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="16993-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="16993-105">Содержит идентификатор записи шаблона для обмена сообщениями объекта пользователя по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="16993-105">Contains the template entry identifier for a default messaging user object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="16993-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="16993-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="16993-107">PR_DEF_CREATE_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="16993-107">PR_DEF_CREATE_MAILUSER</span></span>  <br/> |
|<span data-ttu-id="16993-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="16993-108">Identifier:</span></span>  <br/> |<span data-ttu-id="16993-109">0x3612</span><span class="sxs-lookup"><span data-stu-id="16993-109">0x3612</span></span>  <br/> |
|<span data-ttu-id="16993-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="16993-110">Data type:</span></span>  <br/> |<span data-ttu-id="16993-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="16993-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="16993-112">Область:</span><span class="sxs-lookup"><span data-stu-id="16993-112">Area:</span></span>  <br/> |<span data-ttu-id="16993-113">Адресная книга</span><span class="sxs-lookup"><span data-stu-id="16993-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="16993-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="16993-114">Remarks</span></span>

<span data-ttu-id="16993-115">Клиентские приложения используйте это свойство для создания объекта пользователя обмена сообщениями в контейнере.</span><span class="sxs-lookup"><span data-stu-id="16993-115">Client applications use this property to create a messaging user object within a container.</span></span> <span data-ttu-id="16993-116">Поддержка создания записи является необязательным для контейнеров адресной книги; те, которые не поддерживают не требуется для предоставления этого свойства.</span><span class="sxs-lookup"><span data-stu-id="16993-116">Support of entry creation is optional for address book containers; those that do not support it are not required to expose this property.</span></span> 
  
<span data-ttu-id="16993-117">Это свойство определяет записи, которые отображаются в свойстве **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) для обмена мгновенными сообщениями пользователей.</span><span class="sxs-lookup"><span data-stu-id="16993-117">This property specifies an entry that can appear in the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property for messaging users.</span></span> <span data-ttu-id="16993-118">После получения идентификатора клиента используется в вызов метода [IABContainer::CreateEntry](iabcontainer-createentry.md) .</span><span class="sxs-lookup"><span data-stu-id="16993-118">After obtaining the identifier, the client uses it in a call to the [IABContainer::CreateEntry](iabcontainer-createentry.md) method.</span></span> <span data-ttu-id="16993-119">Операция представляет шаблон для обмена сообщениями пользователя по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="16993-119">The entry represents the template for the default messaging user.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="16993-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="16993-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="16993-121">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="16993-121">Header files</span></span>

<span data-ttu-id="16993-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="16993-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="16993-123">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="16993-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="16993-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="16993-124">Mapitags.h</span></span>
  
> <span data-ttu-id="16993-125">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="16993-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="16993-126">См. также</span><span class="sxs-lookup"><span data-stu-id="16993-126">See also</span></span>



[<span data-ttu-id="16993-127">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="16993-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="16993-128">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="16993-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="16993-129">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="16993-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="16993-130">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="16993-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

