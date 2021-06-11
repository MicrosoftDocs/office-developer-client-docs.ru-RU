---
title: Каноническое свойство PidTagServiceDeleteFiles
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceDeleteFiles
api_type:
- COM
ms.assetid: 9ec80a93-9e8f-46be-a1d4-7648aae47fec
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: da01385f83d9af9ad02eeb2fed08e3bc22d4df84
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436827"
---
# <a name="pidtagservicedeletefiles-canonical-property"></a><span data-ttu-id="e5198-103">Каноническое свойство PidTagServiceDeleteFiles</span><span class="sxs-lookup"><span data-stu-id="e5198-103">PidTagServiceDeleteFiles Canonical Property</span></span>

  
  
<span data-ttu-id="e5198-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e5198-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e5198-105">Содержит список имен файлов, которые должны быть удалены при удалении службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="e5198-105">Contains a list of filenames that are to be deleted when the message service is uninstalled.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e5198-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="e5198-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e5198-107">PR_SERVICE_DELETE_FILES, PR_SERVICE_DELETE_FILES_A, PR_SERVICE_DELETE_FILES_W</span><span class="sxs-lookup"><span data-stu-id="e5198-107">PR_SERVICE_DELETE_FILES, PR_SERVICE_DELETE_FILES_A, PR_SERVICE_DELETE_FILES_W</span></span>  <br/> |
|<span data-ttu-id="e5198-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="e5198-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e5198-109">0x3D10</span><span class="sxs-lookup"><span data-stu-id="e5198-109">0x3D10</span></span>  <br/> |
|<span data-ttu-id="e5198-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="e5198-110">Data type:</span></span>  <br/> |<span data-ttu-id="e5198-111">PT_MV_STRING8, PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e5198-111">PT_MV_STRING8, PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="e5198-112">Область:</span><span class="sxs-lookup"><span data-stu-id="e5198-112">Area:</span></span>  <br/> |<span data-ttu-id="e5198-113">Профиль MAPI</span><span class="sxs-lookup"><span data-stu-id="e5198-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e5198-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="e5198-114">Remarks</span></span>

<span data-ttu-id="e5198-115">Имена файлов в списке, содержащихся в этих свойствах, удаляются с компьютера при использовании панели управления для удаления службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="e5198-115">The filenames in the list contained in these properties are deleted from the computer when using the control panel to uninstall the message service.</span></span> <span data-ttu-id="e5198-116">Не включай в список ни один DLL, который поддерживает несколько служб сообщений, или дополнительные службы сообщений могут быть случайно удалены.</span><span class="sxs-lookup"><span data-stu-id="e5198-116">Do not include in the list any DLL that supports multiple message services, or additional message services could be inadvertently removed.</span></span>
  
<span data-ttu-id="e5198-117">MAPI работает только с именами файлов и другими строками, переданными ему, в наборе символов ANSI.</span><span class="sxs-lookup"><span data-stu-id="e5198-117">MAPI works only with filenames, and other strings passed to it, in the ANSI character set.</span></span> <span data-ttu-id="e5198-118">Приложения, которые используют имена файлов в наборе символов OEM, перед вызовом MAPI должны преобразовать их в ANSI.</span><span class="sxs-lookup"><span data-stu-id="e5198-118">Applications that use filenames in an OEM character set must convert them to ANSI before calling MAPI.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e5198-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="e5198-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="e5198-120">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="e5198-120">Header files</span></span>

<span data-ttu-id="e5198-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e5198-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="e5198-122">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="e5198-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="e5198-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e5198-123">Mapitags.h</span></span>
  
> <span data-ttu-id="e5198-124">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="e5198-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e5198-125">См. также</span><span class="sxs-lookup"><span data-stu-id="e5198-125">See also</span></span>



[<span data-ttu-id="e5198-126">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="e5198-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e5198-127">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="e5198-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e5198-128">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="e5198-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e5198-129">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="e5198-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

