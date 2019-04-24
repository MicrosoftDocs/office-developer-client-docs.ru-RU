---
title: Каноническое свойство PidTagLastModificationTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagLastModificationTime
api_type:
- HeaderDef
ms.assetid: a64e5300-6865-4588-8e1b-158cfd9c60c2
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: dea709b457e28efef62718fc388621e01c4eb5bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279711"
---
# <a name="pidtaglastmodificationtime-canonical-property"></a><span data-ttu-id="4c8bf-103">Каноническое свойство PidTagLastModificationTime</span><span class="sxs-lookup"><span data-stu-id="4c8bf-103">PidTagLastModificationTime Canonical Property</span></span>

  
  
<span data-ttu-id="4c8bf-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4c8bf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4c8bf-105">Содержит дату и время последнего изменения объекта или подобъекта.</span><span class="sxs-lookup"><span data-stu-id="4c8bf-105">Contains the date and time when the object or subobject was last modified.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4c8bf-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="4c8bf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4c8bf-107">ПР_ЛАСТ_МОДИФИКАТИОН_ТИМЕ</span><span class="sxs-lookup"><span data-stu-id="4c8bf-107">PR_LAST_MODIFICATION_TIME</span></span>  <br/> |
|<span data-ttu-id="4c8bf-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="4c8bf-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4c8bf-109">0x3008</span><span class="sxs-lookup"><span data-stu-id="4c8bf-109">0x3008</span></span>  <br/> |
|<span data-ttu-id="4c8bf-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="4c8bf-110">Data type:</span></span>  <br/> |<span data-ttu-id="4c8bf-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="4c8bf-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="4c8bf-112">Область:</span><span class="sxs-lookup"><span data-stu-id="4c8bf-112">Area:</span></span>  <br/> |<span data-ttu-id="4c8bf-113">Время сообщения</span><span class="sxs-lookup"><span data-stu-id="4c8bf-113">Message time</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4c8bf-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="4c8bf-114">Remarks</span></span>

<span data-ttu-id="4c8bf-115">Для этого свойства изначально задается то же значение, что и в свойстве **пр_креатион_тиме** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="4c8bf-115">This property is initially set to the same value as the **PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md)) property.</span></span> <span data-ttu-id="4c8bf-116">Вложенные объекты вложений могут обновлять их по мере необходимости путем копирования времени последнего изменения, поддерживаемого собственной файловой системой.</span><span class="sxs-lookup"><span data-stu-id="4c8bf-116">Attachment subobjects can update it as necessary by copying the last modification time maintained by the native file system.</span></span> <span data-ttu-id="4c8bf-117">Клиентское приложение может установить это свойство до первого вызова метода [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="4c8bf-117">A client application can set this property until the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="4c8bf-118">После этого поставщик должен обновить **пр_ласт_модификатион_тиме** во время каждого вызова **IMAPIProp: SaveChanges** .</span><span class="sxs-lookup"><span data-stu-id="4c8bf-118">From then on the provider should update **PR_LAST_MODIFICATION_TIME** during every **IMAPIProp::SaveChanges** call.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="4c8bf-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="4c8bf-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4c8bf-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="4c8bf-120">Protocol specifications</span></span>

<span data-ttu-id="4c8bf-121">[[MS — ОКСКМСГ]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4c8bf-121">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4c8bf-122">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="4c8bf-122">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="4c8bf-123">[[MS — ОКСКФКСИКС]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4c8bf-123">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4c8bf-124">Обрабатывает синхронизацию данных объекта обмена данными между сервером и клиентом.</span><span class="sxs-lookup"><span data-stu-id="4c8bf-124">Handles synchronizing messaging object data between a server and a client.</span></span>
    
<span data-ttu-id="4c8bf-125">[[MS — ОКСОАБК]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4c8bf-125">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4c8bf-126">Задает свойства и операции для списков пользователей, контактов, групп и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4c8bf-126">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4c8bf-127">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="4c8bf-127">Header files</span></span>

<span data-ttu-id="4c8bf-128">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="4c8bf-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="4c8bf-129">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="4c8bf-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="4c8bf-130">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="4c8bf-130">Mapitags.h</span></span>
  
> <span data-ttu-id="4c8bf-131">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="4c8bf-131">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4c8bf-132">См. также</span><span class="sxs-lookup"><span data-stu-id="4c8bf-132">See also</span></span>



[<span data-ttu-id="4c8bf-133">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="4c8bf-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4c8bf-134">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="4c8bf-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4c8bf-135">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="4c8bf-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4c8bf-136">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="4c8bf-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

