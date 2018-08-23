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
ms.openlocfilehash: 236349a6b53eeb2f5c18c841c05cfb80a3fce824
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580224"
---
# <a name="pidtagservicedeletefiles-canonical-property"></a><span data-ttu-id="5a2fd-103">Каноническое свойство PidTagServiceDeleteFiles</span><span class="sxs-lookup"><span data-stu-id="5a2fd-103">PidTagServiceDeleteFiles Canonical Property</span></span>

  
  
<span data-ttu-id="5a2fd-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5a2fd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5a2fd-105">Содержит список имен файлов, которые должны быть удалены при удалении службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="5a2fd-105">Contains a list of filenames that are to be deleted when the message service is uninstalled.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5a2fd-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="5a2fd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5a2fd-107">PR_SERVICE_DELETE_FILES, PR_SERVICE_DELETE_FILES_A, PR_SERVICE_DELETE_FILES_W</span><span class="sxs-lookup"><span data-stu-id="5a2fd-107">PR_SERVICE_DELETE_FILES, PR_SERVICE_DELETE_FILES_A, PR_SERVICE_DELETE_FILES_W</span></span>  <br/> |
|<span data-ttu-id="5a2fd-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="5a2fd-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5a2fd-109">0x3D10</span><span class="sxs-lookup"><span data-stu-id="5a2fd-109">0x3D10</span></span>  <br/> |
|<span data-ttu-id="5a2fd-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="5a2fd-110">Data type:</span></span>  <br/> |<span data-ttu-id="5a2fd-111">PT_MV_STRING8 PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5a2fd-111">PT_MV_STRING8, PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="5a2fd-112">Область:</span><span class="sxs-lookup"><span data-stu-id="5a2fd-112">Area:</span></span>  <br/> |<span data-ttu-id="5a2fd-113">Профиль MAPI</span><span class="sxs-lookup"><span data-stu-id="5a2fd-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5a2fd-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="5a2fd-114">Remarks</span></span>

<span data-ttu-id="5a2fd-115">Имена файлов в списке, содержащихся в эти свойства удаляются с компьютера при с помощью панели управления для удаления службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="5a2fd-115">The filenames in the list contained in these properties are deleted from the computer when using the control panel to uninstall the message service.</span></span> <span data-ttu-id="5a2fd-116">Не включайте в списке любой библиотеки DLL, которая поддерживает несколько служб сообщение или служб дополнительное сообщение случайно не может быть удален.</span><span class="sxs-lookup"><span data-stu-id="5a2fd-116">Do not include in the list any DLL that supports multiple message services, or additional message services could be inadvertently removed.</span></span>
  
<span data-ttu-id="5a2fd-117">MAPI для работы только с имена файлов и другие строки, переданным в него, в набор символов ANSI.</span><span class="sxs-lookup"><span data-stu-id="5a2fd-117">MAPI works only with filenames, and other strings passed to it, in the ANSI character set.</span></span> <span data-ttu-id="5a2fd-118">Приложения, использующие имена файлов в кодировке OEM необходимо преобразовать их в формате ANSI перед вызовом MAPI.</span><span class="sxs-lookup"><span data-stu-id="5a2fd-118">Applications that use filenames in an OEM character set must convert them to ANSI before calling MAPI.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5a2fd-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="5a2fd-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="5a2fd-120">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="5a2fd-120">Header files</span></span>

<span data-ttu-id="5a2fd-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5a2fd-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="5a2fd-122">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="5a2fd-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="5a2fd-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5a2fd-123">Mapitags.h</span></span>
  
> <span data-ttu-id="5a2fd-124">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="5a2fd-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5a2fd-125">См. также</span><span class="sxs-lookup"><span data-stu-id="5a2fd-125">See also</span></span>



[<span data-ttu-id="5a2fd-126">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="5a2fd-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5a2fd-127">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="5a2fd-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5a2fd-128">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="5a2fd-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5a2fd-129">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="5a2fd-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

