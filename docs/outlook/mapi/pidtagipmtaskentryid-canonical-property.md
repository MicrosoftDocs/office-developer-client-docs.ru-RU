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
ms.openlocfilehash: aa1c4979ce66a0e32aea7b04ef4412679545b3de
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811289"
---
# <a name="pidtagipmtaskentryid-canonical-property"></a><span data-ttu-id="6ad43-103">Каноническое свойство PidTagIpmTaskEntryId</span><span class="sxs-lookup"><span data-stu-id="6ad43-103">PidTagIpmTaskEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="6ad43-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6ad43-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6ad43-105">Содержит **идентификатор записи** папки задач Outlook.</span><span class="sxs-lookup"><span data-stu-id="6ad43-105">Contains the **EntryID** of the Outlook Tasks folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6ad43-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="6ad43-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6ad43-107">PR_IPM_TASK_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="6ad43-107">PR_IPM_TASK_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="6ad43-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="6ad43-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6ad43-109">0x36D4</span><span class="sxs-lookup"><span data-stu-id="6ad43-109">0x36D4</span></span>  <br/> |
|<span data-ttu-id="6ad43-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="6ad43-110">Data type:</span></span>  <br/> |<span data-ttu-id="6ad43-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="6ad43-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="6ad43-112">Область:</span><span class="sxs-lookup"><span data-stu-id="6ad43-112">Area:</span></span>  <br/> |<span data-ttu-id="6ad43-113">Folder</span><span class="sxs-lookup"><span data-stu-id="6ad43-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6ad43-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="6ad43-114">Remarks</span></span>

<span data-ttu-id="6ad43-115">Это свойство чтения или записи с помощью протокола свойство и объект Stream.</span><span class="sxs-lookup"><span data-stu-id="6ad43-115">This property is read or written by using the Property and Stream Object protocol.</span></span> <span data-ttu-id="6ad43-116">Чтение из и в папке "Входящие" или корневой.</span><span class="sxs-lookup"><span data-stu-id="6ad43-116">It is read from and written to the Inbox or Root folder.</span></span> <span data-ttu-id="6ad43-117">Реализация необходимо использовать папку "Входящие" при хранилище, является основной пользователь обмена мгновенными сообщениями, и в ней должна использоваться в корневую папку, когда хранилище пользователя делегатом.</span><span class="sxs-lookup"><span data-stu-id="6ad43-117">The implementation must use the Inbox folder when the store is that of the primary messaging user, and it must use the Root folder when the store is that of a delegate user.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6ad43-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="6ad43-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6ad43-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="6ad43-119">Protocol specifications</span></span>

<span data-ttu-id="6ad43-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6ad43-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6ad43-121">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="6ad43-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6ad43-122">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6ad43-122">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6ad43-123">Задает свойства и операции по созданию и поиск специальные папки в почтовом ящике.</span><span class="sxs-lookup"><span data-stu-id="6ad43-123">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="6ad43-124">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6ad43-124">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6ad43-125">Указывает методы для подключений и настройки почтовых ящиков как делегаты и взаимодействия с объектами сообщений и календаря, когда они действовать от имени другого пользователя.</span><span class="sxs-lookup"><span data-stu-id="6ad43-125">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6ad43-126">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="6ad43-126">Header files</span></span>

<span data-ttu-id="6ad43-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6ad43-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="6ad43-128">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="6ad43-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="6ad43-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6ad43-129">Mapitags.h</span></span>
  
> <span data-ttu-id="6ad43-130">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="6ad43-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6ad43-131">См. также</span><span class="sxs-lookup"><span data-stu-id="6ad43-131">See also</span></span>



[<span data-ttu-id="6ad43-132">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6ad43-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6ad43-133">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6ad43-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6ad43-134">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="6ad43-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6ad43-135">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="6ad43-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

