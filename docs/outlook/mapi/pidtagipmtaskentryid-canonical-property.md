---
title: Каноническое свойство PidTagIpmTaskEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIpmTaskEntryId
api_type:
- HeaderDef
ms.assetid: ec8b7486-b547-4a4e-96e5-1fc825b23f3d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c3845c745dcd2c18525f147308233b94fbce70d4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327853"
---
# <a name="pidtagipmtaskentryid-canonical-property"></a><span data-ttu-id="32b2a-103">Каноническое свойство PidTagIpmTaskEntryId</span><span class="sxs-lookup"><span data-stu-id="32b2a-103">PidTagIpmTaskEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="32b2a-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="32b2a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="32b2a-105">Содержит **EntryID** для папки задач Outlook.</span><span class="sxs-lookup"><span data-stu-id="32b2a-105">Contains the **EntryID** of the Outlook Tasks folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="32b2a-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="32b2a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="32b2a-107">PR_IPM_TASK_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="32b2a-107">PR_IPM_TASK_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="32b2a-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="32b2a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="32b2a-109">0x36D4</span><span class="sxs-lookup"><span data-stu-id="32b2a-109">0x36D4</span></span>  <br/> |
|<span data-ttu-id="32b2a-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="32b2a-110">Data type:</span></span>  <br/> |<span data-ttu-id="32b2a-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="32b2a-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="32b2a-112">Область:</span><span class="sxs-lookup"><span data-stu-id="32b2a-112">Area:</span></span>  <br/> |<span data-ttu-id="32b2a-113">Folder</span><span class="sxs-lookup"><span data-stu-id="32b2a-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="32b2a-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="32b2a-114">Remarks</span></span>

<span data-ttu-id="32b2a-115">Это свойство считывается или записывается с помощью протокола объекта свойства и потока.</span><span class="sxs-lookup"><span data-stu-id="32b2a-115">This property is read or written by using the Property and Stream Object protocol.</span></span> <span data-ttu-id="32b2a-116">Он считывается и записывается в папку "Входящие" или в корневую папку.</span><span class="sxs-lookup"><span data-stu-id="32b2a-116">It is read from and written to the Inbox or Root folder.</span></span> <span data-ttu-id="32b2a-117">Реализация должна использовать папку "Входящие", когда хранилище является основным пользователем обмена сообщениями, и при наличии у пользователя делегирования он должен использовать корневую папку.</span><span class="sxs-lookup"><span data-stu-id="32b2a-117">The implementation must use the Inbox folder when the store is that of the primary messaging user, and it must use the Root folder when the store is that of a delegate user.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="32b2a-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="32b2a-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="32b2a-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="32b2a-119">Protocol specifications</span></span>

<span data-ttu-id="32b2a-120">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="32b2a-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="32b2a-121">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="32b2a-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="32b2a-122">[[MS — ОКСОСФЛД]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="32b2a-122">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="32b2a-123">Задает свойства и операции для создания и поиска специальных папок в почтовом ящике.</span><span class="sxs-lookup"><span data-stu-id="32b2a-123">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="32b2a-124">[[MS — ОКСОДЛГТ]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="32b2a-124">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="32b2a-125">Задает методы для подключения и настройки почтовых ящиков в качестве делегатов и взаимодействия с объектами Message и Calendar, когда они действуют от имени другого пользователя.</span><span class="sxs-lookup"><span data-stu-id="32b2a-125">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="32b2a-126">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="32b2a-126">Header files</span></span>

<span data-ttu-id="32b2a-127">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="32b2a-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="32b2a-128">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="32b2a-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="32b2a-129">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="32b2a-129">Mapitags.h</span></span>
  
> <span data-ttu-id="32b2a-130">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="32b2a-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="32b2a-131">См. также</span><span class="sxs-lookup"><span data-stu-id="32b2a-131">See also</span></span>



[<span data-ttu-id="32b2a-132">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="32b2a-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="32b2a-133">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="32b2a-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="32b2a-134">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="32b2a-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="32b2a-135">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="32b2a-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

