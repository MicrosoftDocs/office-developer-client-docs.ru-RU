---
title: Каноническое свойство PidTagInConflict
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInConflict
api_type:
- HeaderDef
ms.assetid: e83c05c6-a7c0-486c-a112-58a39255767a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: fc2774efed1a15fe79e167149f2cb162bae7642c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358536"
---
# <a name="pidtaginconflict-canonical-property"></a><span data-ttu-id="cfdbb-103">Каноническое свойство PidTagInConflict</span><span class="sxs-lookup"><span data-stu-id="cfdbb-103">PidTagInConflict Canonical Property</span></span>

  
  
<span data-ttu-id="cfdbb-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cfdbb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cfdbb-105">Содержит TRUE, когда вложение представляет альтернативную реплику.</span><span class="sxs-lookup"><span data-stu-id="cfdbb-105">Contains TRUE when the attachment represents an alternate replica.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cfdbb-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="cfdbb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cfdbb-107">PR_IN_CONFLICT</span><span class="sxs-lookup"><span data-stu-id="cfdbb-107">PR_IN_CONFLICT</span></span>  <br/> |
|<span data-ttu-id="cfdbb-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="cfdbb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cfdbb-109">0x666C</span><span class="sxs-lookup"><span data-stu-id="cfdbb-109">0x666C</span></span>  <br/> |
|<span data-ttu-id="cfdbb-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="cfdbb-110">Data type:</span></span>  <br/> |<span data-ttu-id="cfdbb-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="cfdbb-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="cfdbb-112">Область:</span><span class="sxs-lookup"><span data-stu-id="cfdbb-112">Area:</span></span>  <br/> |<span data-ttu-id="cfdbb-113">Заметка о конфликте</span><span class="sxs-lookup"><span data-stu-id="cfdbb-113">Conflict note</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cfdbb-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="cfdbb-114">Remarks</span></span>

<span data-ttu-id="cfdbb-115">Клиент и сервер электронной почты должны создавать сообщение о разрешении конфликтов при обнаружении конфликта с текущей версией сообщения в реплике во время синхронизации.</span><span class="sxs-lookup"><span data-stu-id="cfdbb-115">The email client and server must generate a conflict resolve message when detecting a conflict against the current version of a message in the replica during synchronization.</span></span> <span data-ttu-id="cfdbb-116">Важно понимать, что вполне возможно, что текущая версия сообщения в локальной реплике была передана во время текущей операции синхронизации.</span><span class="sxs-lookup"><span data-stu-id="cfdbb-116">It is important to understand that it is possible that the current version of the message in the local replica was transmitted during the current synchronization operation.</span></span> <span data-ttu-id="cfdbb-117">Это произойдет, когда конфликт уже существует на сервере перед скачиванием конфликтующих сообщений в локализованную реплику.</span><span class="sxs-lookup"><span data-stu-id="cfdbb-117">This will happen when the conflict already exists on the server before any of the conflicting messages were downloaded to the local replica.</span></span> <span data-ttu-id="cfdbb-118">Сообщение о разрешении конфликтов должно синхронизироваться как независимые реплики с конфликтующие PCLs.</span><span class="sxs-lookup"><span data-stu-id="cfdbb-118">A conflict resolve message must be synchronized as independent replicas with conflicting PCLs.</span></span> <span data-ttu-id="cfdbb-119">Само сообщение по разрешению конфликтов не должно синхронизироваться между клиентом и сервером; следует обмениваться только независимыми репликами.</span><span class="sxs-lookup"><span data-stu-id="cfdbb-119">The conflict resolve message itself must not be synchronized between client and server; only the independent replicas should be exchanged.</span></span> <span data-ttu-id="cfdbb-120">Затем партнер синхронизации должен создать новое сообщение, которое соответствует структуре сообщения о конфликте.</span><span class="sxs-lookup"><span data-stu-id="cfdbb-120">The synchronization partner must then generate a new message that matches the structure of the conflict message.</span></span> <span data-ttu-id="cfdbb-121">Поэтому важно, чтобы клиент и сервер использовали тот же алгоритм для обнаружения элемента "победитель".</span><span class="sxs-lookup"><span data-stu-id="cfdbb-121">Therefore, it is important that client and server use the same algorithm to detect the "winner" item.</span></span> <span data-ttu-id="cfdbb-122">Для обнаружения "победителя" необходимо применить следующие правила:</span><span class="sxs-lookup"><span data-stu-id="cfdbb-122">The following rules must be applied to detect the "winner":</span></span>
  
1. <span data-ttu-id="cfdbb-123">Время последней модификации.</span><span class="sxs-lookup"><span data-stu-id="cfdbb-123">Last modification time.</span></span>
    
2. <span data-ttu-id="cfdbb-124">Higher CN GUID (using memory compare) to break tie.</span><span class="sxs-lookup"><span data-stu-id="cfdbb-124">Higher CN GUID (using memory compare) to break tie.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="cfdbb-125">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="cfdbb-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cfdbb-126">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="cfdbb-126">Protocol specifications</span></span>

<span data-ttu-id="cfdbb-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cfdbb-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cfdbb-128">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="cfdbb-128">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="cfdbb-129">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cfdbb-129">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cfdbb-130">Обрабатывает синхронизацию данных объектов обмена сообщениями между сервером и клиентом.</span><span class="sxs-lookup"><span data-stu-id="cfdbb-130">Handles synchronizing messaging object data between a server and a client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cfdbb-131">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="cfdbb-131">Header files</span></span>

<span data-ttu-id="cfdbb-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cfdbb-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="cfdbb-133">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="cfdbb-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="cfdbb-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="cfdbb-134">Mapitags.h</span></span>
  
> <span data-ttu-id="cfdbb-135">Содержит определения свойств, перечисленных в качестве связанных свойств.</span><span class="sxs-lookup"><span data-stu-id="cfdbb-135">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cfdbb-136">См. также</span><span class="sxs-lookup"><span data-stu-id="cfdbb-136">See also</span></span>



[<span data-ttu-id="cfdbb-137">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="cfdbb-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cfdbb-138">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="cfdbb-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cfdbb-139">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="cfdbb-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cfdbb-140">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="cfdbb-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

