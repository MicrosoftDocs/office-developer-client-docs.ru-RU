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
ms.openlocfilehash: bf58e0598af6eb833b003b824be95f8fb82bd8bf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/21/2018
ms.locfileid: "19811316"
---
# <a name="pidtaglastmodificationtime-canonical-property"></a><span data-ttu-id="8a5c0-103">Каноническое свойство PidTagLastModificationTime</span><span class="sxs-lookup"><span data-stu-id="8a5c0-103">PidTagLastModificationTime Canonical Property</span></span>

  
  
<span data-ttu-id="8a5c0-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8a5c0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8a5c0-105">Содержит дату и время последнего изменения объекта или вложенные объекты.</span><span class="sxs-lookup"><span data-stu-id="8a5c0-105">Contains the date and time when the object or subobject was last modified.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8a5c0-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="8a5c0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8a5c0-107">PR_LAST_MODIFICATION_TIME</span><span class="sxs-lookup"><span data-stu-id="8a5c0-107">PR_LAST_MODIFICATION_TIME</span></span>  <br/> |
|<span data-ttu-id="8a5c0-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="8a5c0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8a5c0-109">0x3008</span><span class="sxs-lookup"><span data-stu-id="8a5c0-109">0x3008</span></span>  <br/> |
|<span data-ttu-id="8a5c0-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="8a5c0-110">Data type:</span></span>  <br/> |<span data-ttu-id="8a5c0-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="8a5c0-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="8a5c0-112">Область:</span><span class="sxs-lookup"><span data-stu-id="8a5c0-112">Area:</span></span>  <br/> |<span data-ttu-id="8a5c0-113">Время сообщения</span><span class="sxs-lookup"><span data-stu-id="8a5c0-113">Message time</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8a5c0-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="8a5c0-114">Remarks</span></span>

<span data-ttu-id="8a5c0-115">Это свойство изначально установлено значение совпадает со значением свойства **PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="8a5c0-115">This property is initially set to the same value as the **PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md)) property.</span></span> <span data-ttu-id="8a5c0-116">Вложения вложенных можно обновить при необходимости, скопировав времени последнего изменения, задаваемые с помощью собственного файловой системы.</span><span class="sxs-lookup"><span data-stu-id="8a5c0-116">Attachment subobjects can update it as necessary by copying the last modification time maintained by the native file system.</span></span> <span data-ttu-id="8a5c0-117">Клиентское приложение можно задать это свойство до первого вызова метода [IMAPIProp::SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="8a5c0-117">A client application can set this property until the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="8a5c0-118">В дальнейшем поставщика следует обновить **PR_LAST_MODIFICATION_TIME** во время каждого вызова **IMAPIProp::SaveChanges** .</span><span class="sxs-lookup"><span data-stu-id="8a5c0-118">From then on the provider should update **PR_LAST_MODIFICATION_TIME** during every **IMAPIProp::SaveChanges** call.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="8a5c0-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="8a5c0-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8a5c0-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="8a5c0-120">Protocol specifications</span></span>

<span data-ttu-id="8a5c0-121">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8a5c0-121">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8a5c0-122">Обрабатывает объекты сообщения и вложения.</span><span class="sxs-lookup"><span data-stu-id="8a5c0-122">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="8a5c0-123">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8a5c0-123">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8a5c0-124">Обрабатывает синхронизации обмена сообщениями объект данных между сервером и клиентом.</span><span class="sxs-lookup"><span data-stu-id="8a5c0-124">Handles synchronizing messaging object data between a server and a client.</span></span>
    
<span data-ttu-id="8a5c0-125">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8a5c0-125">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8a5c0-126">Задает свойства и операции для списков пользователей, контактов, групп и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8a5c0-126">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8a5c0-127">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="8a5c0-127">Header files</span></span>

<span data-ttu-id="8a5c0-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8a5c0-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="8a5c0-129">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="8a5c0-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="8a5c0-130">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8a5c0-130">Mapitags.h</span></span>
  
> <span data-ttu-id="8a5c0-131">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="8a5c0-131">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8a5c0-132">См. также</span><span class="sxs-lookup"><span data-stu-id="8a5c0-132">See also</span></span>



[<span data-ttu-id="8a5c0-133">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8a5c0-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8a5c0-134">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8a5c0-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8a5c0-135">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="8a5c0-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8a5c0-136">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="8a5c0-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

