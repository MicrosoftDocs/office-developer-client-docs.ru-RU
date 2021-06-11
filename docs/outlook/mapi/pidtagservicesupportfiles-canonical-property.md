---
title: Каноническое свойство PidTagServiceSupportFiles
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceSupportFiles
api_type:
- COM
ms.assetid: df4be986-62a8-49d6-8eca-25b55c74f830
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3753177552d45e32e53ae192a9dfae15b601afcc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417044"
---
# <a name="pidtagservicesupportfiles-canonical-property"></a><span data-ttu-id="53631-103">Каноническое свойство PidTagServiceSupportFiles</span><span class="sxs-lookup"><span data-stu-id="53631-103">PidTagServiceSupportFiles Canonical Property</span></span>

  
  
<span data-ttu-id="53631-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="53631-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="53631-105">Содержит список файлов, принадлежащих службе сообщений.</span><span class="sxs-lookup"><span data-stu-id="53631-105">Contains a list of the files that belong to the message service.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="53631-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="53631-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="53631-107">PR_SERVICE_SUPPORT_FILES, PR_SERVICE_SUPPORT_FILES_A, PR_SERVICE_SUPPORT_FILES_W</span><span class="sxs-lookup"><span data-stu-id="53631-107">PR_SERVICE_SUPPORT_FILES, PR_SERVICE_SUPPORT_FILES_A, PR_SERVICE_SUPPORT_FILES_W</span></span>  <br/> |
|<span data-ttu-id="53631-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="53631-108">Identifier:</span></span>  <br/> |<span data-ttu-id="53631-109">0x3D0F</span><span class="sxs-lookup"><span data-stu-id="53631-109">0x3D0F</span></span>  <br/> |
|<span data-ttu-id="53631-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="53631-110">Data type:</span></span>  <br/> |<span data-ttu-id="53631-111">PT_MV_STRING8, PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="53631-111">PT_MV_STRING8, PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="53631-112">Область:</span><span class="sxs-lookup"><span data-stu-id="53631-112">Area:</span></span>  <br/> |<span data-ttu-id="53631-113">Профиль MAPI</span><span class="sxs-lookup"><span data-stu-id="53631-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="53631-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="53631-114">Remarks</span></span>

<span data-ttu-id="53631-115">Используя диалоговое окно в applet панели управления, пользователь может получить список файлов, принадлежащих службе сообщений.</span><span class="sxs-lookup"><span data-stu-id="53631-115">Using a dialog box in the control panel applet, a user can obtain the list of files that belong to the message service.</span></span> <span data-ttu-id="53631-116">Например, пользователь может получить имена всех библиотек динамических ссылок (DLLs), принадлежащих службе.</span><span class="sxs-lookup"><span data-stu-id="53631-116">For example, the user can obtain the names of all dynamic-link libraries (DLLs) that belong to the service.</span></span> <span data-ttu-id="53631-117">Затем пользователь может получить дополнительные сведения о указанных файлах, например имена и номера версий всех DLLs.</span><span class="sxs-lookup"><span data-stu-id="53631-117">The user can then seek additional details about the specified files, such as the names and version numbers of all the DLLs.</span></span> <span data-ttu-id="53631-118">MAPI использует эти свойства для создания списка файлов поддержки в диалоговом окне для выбора пользователей сообщений.</span><span class="sxs-lookup"><span data-stu-id="53631-118">MAPI uses the these properties to create a support file list in a dialog box for messaging user selection.</span></span>
  
<span data-ttu-id="53631-119">MAPI работает только с именами файлов и другими строками, переданными ему, в наборе символов Active Directory Service Interfaces (ANSI).</span><span class="sxs-lookup"><span data-stu-id="53631-119">MAPI works only with filenames, and other strings passed to it, in the Active Directory Service Interfaces (ANSI) character set.</span></span> <span data-ttu-id="53631-120">Клиентские приложения, которые используют имена файлов в исходном наборе символов производителя оборудования (OEM), перед вызовом MAPI должны преобразовать их в ANSI.</span><span class="sxs-lookup"><span data-stu-id="53631-120">Client applications that use filenames in an original equipment manufacturer (OEM) character set must convert them to ANSI before calling MAPI.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="53631-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="53631-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="53631-122">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="53631-122">Header files</span></span>

<span data-ttu-id="53631-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="53631-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="53631-124">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="53631-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="53631-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="53631-125">Mapitags.h</span></span>
  
> <span data-ttu-id="53631-126">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="53631-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="53631-127">См. также</span><span class="sxs-lookup"><span data-stu-id="53631-127">See also</span></span>



[<span data-ttu-id="53631-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="53631-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="53631-129">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="53631-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="53631-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="53631-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="53631-131">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="53631-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

