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
ms.openlocfilehash: 8f90d72e842df62c19c5aeeaf6c398c5db469560
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811921"
---
# <a name="pidtagservicedeletefiles-canonical-property"></a><span data-ttu-id="be7bb-103">Каноническое свойство PidTagServiceDeleteFiles</span><span class="sxs-lookup"><span data-stu-id="be7bb-103">PidTagServiceDeleteFiles Canonical Property</span></span>

  
  
<span data-ttu-id="be7bb-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="be7bb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="be7bb-105">Содержит список имен файлов, которые должны быть удалены при удалении службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="be7bb-105">Contains a list of filenames that are to be deleted when the message service is uninstalled.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="be7bb-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="be7bb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="be7bb-107">PR_SERVICE_DELETE_FILES, PR_SERVICE_DELETE_FILES_A, PR_SERVICE_DELETE_FILES_W</span><span class="sxs-lookup"><span data-stu-id="be7bb-107">PR_SERVICE_DELETE_FILES, PR_SERVICE_DELETE_FILES_A, PR_SERVICE_DELETE_FILES_W</span></span>  <br/> |
|<span data-ttu-id="be7bb-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="be7bb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="be7bb-109">0x3D10</span><span class="sxs-lookup"><span data-stu-id="be7bb-109">0x3D10</span></span>  <br/> |
|<span data-ttu-id="be7bb-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="be7bb-110">Data type:</span></span>  <br/> |<span data-ttu-id="be7bb-111">PT_MV_STRING8 PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="be7bb-111">PT_MV_STRING8, PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="be7bb-112">Область:</span><span class="sxs-lookup"><span data-stu-id="be7bb-112">Area:</span></span>  <br/> |<span data-ttu-id="be7bb-113">Профиль MAPI</span><span class="sxs-lookup"><span data-stu-id="be7bb-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="be7bb-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="be7bb-114">Remarks</span></span>

<span data-ttu-id="be7bb-115">Имена файлов в списке, содержащихся в эти свойства удаляются с компьютера при с помощью панели управления для удаления службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="be7bb-115">The filenames in the list contained in these properties are deleted from the computer when using the control panel to uninstall the message service.</span></span> <span data-ttu-id="be7bb-116">Не включайте в списке любой библиотеки DLL, которая поддерживает несколько служб сообщение или служб дополнительное сообщение случайно не может быть удален.</span><span class="sxs-lookup"><span data-stu-id="be7bb-116">Do not include in the list any DLL that supports multiple message services, or additional message services could be inadvertently removed.</span></span>
  
<span data-ttu-id="be7bb-117">MAPI для работы только с имена файлов и другие строки, переданным в него, в набор символов ANSI.</span><span class="sxs-lookup"><span data-stu-id="be7bb-117">MAPI works only with filenames, and other strings passed to it, in the ANSI character set.</span></span> <span data-ttu-id="be7bb-118">Приложения, использующие имена файлов в кодировке OEM необходимо преобразовать их в формате ANSI перед вызовом MAPI.</span><span class="sxs-lookup"><span data-stu-id="be7bb-118">Applications that use filenames in an OEM character set must convert them to ANSI before calling MAPI.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="be7bb-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="be7bb-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="be7bb-120">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="be7bb-120">Header files</span></span>

<span data-ttu-id="be7bb-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="be7bb-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="be7bb-122">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="be7bb-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="be7bb-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="be7bb-123">Mapitags.h</span></span>
  
> <span data-ttu-id="be7bb-124">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="be7bb-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="be7bb-125">См. также</span><span class="sxs-lookup"><span data-stu-id="be7bb-125">See also</span></span>



[<span data-ttu-id="be7bb-126">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="be7bb-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="be7bb-127">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="be7bb-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="be7bb-128">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="be7bb-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="be7bb-129">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="be7bb-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

