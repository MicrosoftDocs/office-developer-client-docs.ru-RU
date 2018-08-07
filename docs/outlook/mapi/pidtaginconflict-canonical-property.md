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
ms.openlocfilehash: 573e0ba37d4117d85193933a3a5045b5060fbd3d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811235"
---
# <a name="pidtaginconflict-canonical-property"></a><span data-ttu-id="6cf09-103">Каноническое свойство PidTagInConflict</span><span class="sxs-lookup"><span data-stu-id="6cf09-103">PidTagInConflict Canonical Property</span></span>

  
  
<span data-ttu-id="6cf09-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6cf09-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6cf09-105">Содержит значение TRUE, когда вложение представляет альтернативного реплики.</span><span class="sxs-lookup"><span data-stu-id="6cf09-105">Contains TRUE when the attachment represents an alternate replica.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6cf09-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="6cf09-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6cf09-107">PR_IN_CONFLICT</span><span class="sxs-lookup"><span data-stu-id="6cf09-107">PR_IN_CONFLICT</span></span>  <br/> |
|<span data-ttu-id="6cf09-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="6cf09-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6cf09-109">0x666C</span><span class="sxs-lookup"><span data-stu-id="6cf09-109">0x666C</span></span>  <br/> |
|<span data-ttu-id="6cf09-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="6cf09-110">Data type:</span></span>  <br/> |<span data-ttu-id="6cf09-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="6cf09-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="6cf09-112">Область:</span><span class="sxs-lookup"><span data-stu-id="6cf09-112">Area:</span></span>  <br/> |<span data-ttu-id="6cf09-113">Примечание конфликта</span><span class="sxs-lookup"><span data-stu-id="6cf09-113">Conflict note</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6cf09-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="6cf09-114">Remarks</span></span>

<span data-ttu-id="6cf09-115">Сервером и клиентом электронной почты необходимо создать сообщение устранением конфликтов при обнаружении конфликта с текущей версией сообщение в реплике во время синхронизации.</span><span class="sxs-lookup"><span data-stu-id="6cf09-115">The email client and server must generate a conflict resolve message when detecting a conflict against the current version of a message in the replica during synchronization.</span></span> <span data-ttu-id="6cf09-116">Важно понимать, что это и возможно, что текущая версия сообщения в локальной реплики передавался во время текущей операции синхронизации.</span><span class="sxs-lookup"><span data-stu-id="6cf09-116">It is important to understand that it is possible that the current version of the message in the local replica was transmitted during the current synchronization operation.</span></span> <span data-ttu-id="6cf09-117">Это происходит конфликт уже существует на сервере перед конфликтующие сообщения были загружены для локальной реплики.</span><span class="sxs-lookup"><span data-stu-id="6cf09-117">This will happen when the conflict already exists on the server before any of the conflicting messages were downloaded to the local replica.</span></span> <span data-ttu-id="6cf09-118">Устраните конфликт сообщения должны быть синхронизированы как независимые реплики с конфликтующие PCLs.</span><span class="sxs-lookup"><span data-stu-id="6cf09-118">A conflict resolve message must be synchronized as independent replicas with conflicting PCLs.</span></span> <span data-ttu-id="6cf09-119">Конфликт устранить сообщения не должны быть синхронизированы между клиентом и сервером; только независимой реплик обмена.</span><span class="sxs-lookup"><span data-stu-id="6cf09-119">The conflict resolve message itself must not be synchronized between client and server; only the independent replicas should be exchanged.</span></span> <span data-ttu-id="6cf09-120">Партнер синхронизации необходимо создать новое сообщение, которое совпадает со структурой сообщение о конфликте.</span><span class="sxs-lookup"><span data-stu-id="6cf09-120">The synchronization partner must then generate a new message that matches the structure of the conflict message.</span></span> <span data-ttu-id="6cf09-121">Таким образом важно, что клиент и сервер используют тот же алгоритм для обнаружения элемента «по результатам».</span><span class="sxs-lookup"><span data-stu-id="6cf09-121">Therefore, it is important that client and server use the same algorithm to detect the "winner" item.</span></span> <span data-ttu-id="6cf09-122">Для обнаружения «результатам» должны применяться следующие правила:</span><span class="sxs-lookup"><span data-stu-id="6cf09-122">The following rules must be applied to detect the "winner":</span></span>
  
1. <span data-ttu-id="6cf09-123">Время последнего изменения.</span><span class="sxs-lookup"><span data-stu-id="6cf09-123">Last modification time.</span></span>
    
2. <span data-ttu-id="6cf09-124">Выше CN идентификатор GUID (compare памяти) чтобы разорвать связи.</span><span class="sxs-lookup"><span data-stu-id="6cf09-124">Higher CN GUID (using memory compare) to break tie.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="6cf09-125">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="6cf09-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6cf09-126">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="6cf09-126">Protocol specifications</span></span>

<span data-ttu-id="6cf09-127">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6cf09-127">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6cf09-128">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="6cf09-128">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6cf09-129">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6cf09-129">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6cf09-130">Обрабатывает синхронизации обмена сообщениями объект данных между сервером и клиентом.</span><span class="sxs-lookup"><span data-stu-id="6cf09-130">Handles synchronizing messaging object data between a server and a client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6cf09-131">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="6cf09-131">Header files</span></span>

<span data-ttu-id="6cf09-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6cf09-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="6cf09-133">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="6cf09-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="6cf09-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6cf09-134">Mapitags.h</span></span>
  
> <span data-ttu-id="6cf09-135">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="6cf09-135">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6cf09-136">См. также</span><span class="sxs-lookup"><span data-stu-id="6cf09-136">See also</span></span>



[<span data-ttu-id="6cf09-137">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6cf09-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6cf09-138">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6cf09-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6cf09-139">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="6cf09-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6cf09-140">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="6cf09-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

