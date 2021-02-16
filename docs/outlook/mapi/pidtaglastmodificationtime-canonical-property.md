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
# <a name="pidtaglastmodificationtime-canonical-property"></a><span data-ttu-id="641c2-103">Каноническое свойство PidTagLastModificationTime</span><span class="sxs-lookup"><span data-stu-id="641c2-103">PidTagLastModificationTime Canonical Property</span></span>

  
  
<span data-ttu-id="641c2-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="641c2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="641c2-105">Содержит дату и время последнего изменения объекта или подпроекта.</span><span class="sxs-lookup"><span data-stu-id="641c2-105">Contains the date and time when the object or subobject was last modified.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="641c2-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="641c2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="641c2-107">PR_LAST_MODIFICATION_TIME</span><span class="sxs-lookup"><span data-stu-id="641c2-107">PR_LAST_MODIFICATION_TIME</span></span>  <br/> |
|<span data-ttu-id="641c2-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="641c2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="641c2-109">0x3008</span><span class="sxs-lookup"><span data-stu-id="641c2-109">0x3008</span></span>  <br/> |
|<span data-ttu-id="641c2-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="641c2-110">Data type:</span></span>  <br/> |<span data-ttu-id="641c2-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="641c2-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="641c2-112">Область:</span><span class="sxs-lookup"><span data-stu-id="641c2-112">Area:</span></span>  <br/> |<span data-ttu-id="641c2-113">Время сообщения</span><span class="sxs-lookup"><span data-stu-id="641c2-113">Message time</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="641c2-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="641c2-114">Remarks</span></span>

<span data-ttu-id="641c2-115">Изначально этому свойству задается то же **значение, что** и для свойства PR_CREATION_TIME ([PidTagCreationTime).](pidtagcreationtime-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="641c2-115">This property is initially set to the same value as the **PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md)) property.</span></span> <span data-ttu-id="641c2-116">Вложенные вложения могут обновлять его по мере необходимости, копируя время последнего изменения, поддерживаемые файловой системой.</span><span class="sxs-lookup"><span data-stu-id="641c2-116">Attachment subobjects can update it as necessary by copying the last modification time maintained by the native file system.</span></span> <span data-ttu-id="641c2-117">Клиентские приложения могут установить это свойство до первого вызова метода [IMAPIProp::SaveChanges.](imapiprop-savechanges.md)</span><span class="sxs-lookup"><span data-stu-id="641c2-117">A client application can set this property until the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="641c2-118">С этого времени поставщик должен обновлять **PR_LAST_MODIFICATION_TIME** во время каждого вызова **IMAPIProp::SaveChanges.**</span><span class="sxs-lookup"><span data-stu-id="641c2-118">From then on the provider should update **PR_LAST_MODIFICATION_TIME** during every **IMAPIProp::SaveChanges** call.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="641c2-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="641c2-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="641c2-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="641c2-120">Protocol specifications</span></span>

<span data-ttu-id="641c2-121">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="641c2-121">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="641c2-122">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="641c2-122">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="641c2-123">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="641c2-123">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="641c2-124">Обрабатывает синхронизацию данных объектов обмена сообщениями между сервером и клиентом.</span><span class="sxs-lookup"><span data-stu-id="641c2-124">Handles synchronizing messaging object data between a server and a client.</span></span>
    
<span data-ttu-id="641c2-125">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="641c2-125">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="641c2-126">Указывает свойства и операции для списков пользователей, контактов, групп и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="641c2-126">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="641c2-127">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="641c2-127">Header files</span></span>

<span data-ttu-id="641c2-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="641c2-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="641c2-129">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="641c2-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="641c2-130">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="641c2-130">Mapitags.h</span></span>
  
> <span data-ttu-id="641c2-131">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="641c2-131">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="641c2-132">См. также</span><span class="sxs-lookup"><span data-stu-id="641c2-132">See also</span></span>



[<span data-ttu-id="641c2-133">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="641c2-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="641c2-134">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="641c2-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="641c2-135">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="641c2-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="641c2-136">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="641c2-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

