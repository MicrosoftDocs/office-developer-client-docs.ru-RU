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
ms.openlocfilehash: cc4a8757586da8ec3a3d51f132fcc583ece748f6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588953"
---
# <a name="pidtagipmtaskentryid-canonical-property"></a><span data-ttu-id="73f3b-103">Каноническое свойство PidTagIpmTaskEntryId</span><span class="sxs-lookup"><span data-stu-id="73f3b-103">PidTagIpmTaskEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="73f3b-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="73f3b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="73f3b-105">Содержит **идентификатор записи** папки задач Outlook.</span><span class="sxs-lookup"><span data-stu-id="73f3b-105">Contains the **EntryID** of the Outlook Tasks folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="73f3b-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="73f3b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="73f3b-107">PR_IPM_TASK_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="73f3b-107">PR_IPM_TASK_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="73f3b-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="73f3b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="73f3b-109">0x36D4</span><span class="sxs-lookup"><span data-stu-id="73f3b-109">0x36D4</span></span>  <br/> |
|<span data-ttu-id="73f3b-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="73f3b-110">Data type:</span></span>  <br/> |<span data-ttu-id="73f3b-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="73f3b-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="73f3b-112">Область:</span><span class="sxs-lookup"><span data-stu-id="73f3b-112">Area:</span></span>  <br/> |<span data-ttu-id="73f3b-113">Folder</span><span class="sxs-lookup"><span data-stu-id="73f3b-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="73f3b-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="73f3b-114">Remarks</span></span>

<span data-ttu-id="73f3b-115">Это свойство чтения или записи с помощью протокола свойство и объект Stream.</span><span class="sxs-lookup"><span data-stu-id="73f3b-115">This property is read or written by using the Property and Stream Object protocol.</span></span> <span data-ttu-id="73f3b-116">Чтение из и в папке "Входящие" или корневой.</span><span class="sxs-lookup"><span data-stu-id="73f3b-116">It is read from and written to the Inbox or Root folder.</span></span> <span data-ttu-id="73f3b-117">Реализация необходимо использовать папку "Входящие" при хранилище, является основной пользователь обмена мгновенными сообщениями, и в ней должна использоваться в корневую папку, когда хранилище пользователя делегатом.</span><span class="sxs-lookup"><span data-stu-id="73f3b-117">The implementation must use the Inbox folder when the store is that of the primary messaging user, and it must use the Root folder when the store is that of a delegate user.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="73f3b-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="73f3b-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="73f3b-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="73f3b-119">Protocol specifications</span></span>

<span data-ttu-id="73f3b-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="73f3b-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="73f3b-121">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="73f3b-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="73f3b-122">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="73f3b-122">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="73f3b-123">Задает свойства и операции по созданию и поиск специальные папки в почтовом ящике.</span><span class="sxs-lookup"><span data-stu-id="73f3b-123">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="73f3b-124">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="73f3b-124">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="73f3b-125">Указывает методы для подключений и настройки почтовых ящиков как делегаты и взаимодействия с объектами сообщений и календаря, когда они действовать от имени другого пользователя.</span><span class="sxs-lookup"><span data-stu-id="73f3b-125">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="73f3b-126">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="73f3b-126">Header files</span></span>

<span data-ttu-id="73f3b-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="73f3b-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="73f3b-128">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="73f3b-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="73f3b-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="73f3b-129">Mapitags.h</span></span>
  
> <span data-ttu-id="73f3b-130">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="73f3b-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="73f3b-131">См. также</span><span class="sxs-lookup"><span data-stu-id="73f3b-131">See also</span></span>



[<span data-ttu-id="73f3b-132">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="73f3b-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="73f3b-133">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="73f3b-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="73f3b-134">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="73f3b-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="73f3b-135">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="73f3b-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

