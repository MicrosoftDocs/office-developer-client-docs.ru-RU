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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407482"
---
# <a name="pidtagdefcreatemailuser-canonical-property"></a><span data-ttu-id="cd12d-103">Каноническое свойство PidTagDefCreateMailuser</span><span class="sxs-lookup"><span data-stu-id="cd12d-103">PidTagDefCreateMailuser Canonical Property</span></span>

  
  
<span data-ttu-id="cd12d-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cd12d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cd12d-105">Содержит идентификатор записи шаблона для объекта пользователя обмена сообщениями по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="cd12d-105">Contains the template entry identifier for a default messaging user object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cd12d-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="cd12d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cd12d-107">PR_DEF_CREATE_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="cd12d-107">PR_DEF_CREATE_MAILUSER</span></span>  <br/> |
|<span data-ttu-id="cd12d-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="cd12d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cd12d-109">0x3612</span><span class="sxs-lookup"><span data-stu-id="cd12d-109">0x3612</span></span>  <br/> |
|<span data-ttu-id="cd12d-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="cd12d-110">Data type:</span></span>  <br/> |<span data-ttu-id="cd12d-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="cd12d-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="cd12d-112">Область:</span><span class="sxs-lookup"><span data-stu-id="cd12d-112">Area:</span></span>  <br/> |<span data-ttu-id="cd12d-113">Адресная книга</span><span class="sxs-lookup"><span data-stu-id="cd12d-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cd12d-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="cd12d-114">Remarks</span></span>

<span data-ttu-id="cd12d-115">Клиентские приложения используют это свойство для создания объекта пользователя обмена сообщениями в контейнере.</span><span class="sxs-lookup"><span data-stu-id="cd12d-115">Client applications use this property to create a messaging user object within a container.</span></span> <span data-ttu-id="cd12d-116">Поддержка создания записей не является обязательной для контейнеров адресной книги; те, которые не поддерживают его, не требуются для того, чтобы получить доступ к этому свойству.</span><span class="sxs-lookup"><span data-stu-id="cd12d-116">Support of entry creation is optional for address book containers; those that do not support it are not required to expose this property.</span></span> 
  
<span data-ttu-id="cd12d-117">Это свойство указывает запись, которая может отображаться в свойстве **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates)](pidtagcreatetemplates-canonical-property.md)для пользователей сообщений.</span><span class="sxs-lookup"><span data-stu-id="cd12d-117">This property specifies an entry that can appear in the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property for messaging users.</span></span> <span data-ttu-id="cd12d-118">После получения идентификатора клиент использует его в вызове метода [IABContainer::CreateEntry.](iabcontainer-createentry.md)</span><span class="sxs-lookup"><span data-stu-id="cd12d-118">After obtaining the identifier, the client uses it in a call to the [IABContainer::CreateEntry](iabcontainer-createentry.md) method.</span></span> <span data-ttu-id="cd12d-119">Запись представляет шаблон для пользователя обмена сообщениями по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="cd12d-119">The entry represents the template for the default messaging user.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="cd12d-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="cd12d-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="cd12d-121">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="cd12d-121">Header files</span></span>

<span data-ttu-id="cd12d-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cd12d-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="cd12d-123">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="cd12d-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="cd12d-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="cd12d-124">Mapitags.h</span></span>
  
> <span data-ttu-id="cd12d-125">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="cd12d-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cd12d-126">См. также</span><span class="sxs-lookup"><span data-stu-id="cd12d-126">See also</span></span>



[<span data-ttu-id="cd12d-127">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="cd12d-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cd12d-128">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="cd12d-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cd12d-129">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="cd12d-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cd12d-130">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="cd12d-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

