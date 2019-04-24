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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359474"
---
# <a name="pidtagservicesupportfiles-canonical-property"></a><span data-ttu-id="0d58e-103">Каноническое свойство PidTagServiceSupportFiles</span><span class="sxs-lookup"><span data-stu-id="0d58e-103">PidTagServiceSupportFiles Canonical Property</span></span>

  
  
<span data-ttu-id="0d58e-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0d58e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0d58e-105">Содержит список файлов, принадлежащих службе сообщений.</span><span class="sxs-lookup"><span data-stu-id="0d58e-105">Contains a list of the files that belong to the message service.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0d58e-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="0d58e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0d58e-107">ПР_СЕРВИЦЕ_СУППОРТ_ФИЛЕС, ПР_СЕРВИЦЕ_СУППОРТ_ФИЛЕС_А, ПР_СЕРВИЦЕ_СУППОРТ_ФИЛЕС_В</span><span class="sxs-lookup"><span data-stu-id="0d58e-107">PR_SERVICE_SUPPORT_FILES, PR_SERVICE_SUPPORT_FILES_A, PR_SERVICE_SUPPORT_FILES_W</span></span>  <br/> |
|<span data-ttu-id="0d58e-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="0d58e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0d58e-109">0x3D0F</span><span class="sxs-lookup"><span data-stu-id="0d58e-109">0x3D0F</span></span>  <br/> |
|<span data-ttu-id="0d58e-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="0d58e-110">Data type:</span></span>  <br/> |<span data-ttu-id="0d58e-111">PT_MV_STRING8, ПТ_МВ_УНИКОДЕ</span><span class="sxs-lookup"><span data-stu-id="0d58e-111">PT_MV_STRING8, PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="0d58e-112">Область:</span><span class="sxs-lookup"><span data-stu-id="0d58e-112">Area:</span></span>  <br/> |<span data-ttu-id="0d58e-113">Профиль MAPI</span><span class="sxs-lookup"><span data-stu-id="0d58e-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0d58e-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="0d58e-114">Remarks</span></span>

<span data-ttu-id="0d58e-115">С помощью диалогового окна в приложении панели управления пользователь может получить список файлов, принадлежащих службе сообщений.</span><span class="sxs-lookup"><span data-stu-id="0d58e-115">Using a dialog box in the control panel applet, a user can obtain the list of files that belong to the message service.</span></span> <span data-ttu-id="0d58e-116">Например, пользователь может получить имена всех библиотек динамической компоновки (DLL), принадлежащих службе.</span><span class="sxs-lookup"><span data-stu-id="0d58e-116">For example, the user can obtain the names of all dynamic-link libraries (DLLs) that belong to the service.</span></span> <span data-ttu-id="0d58e-117">Затем пользователь может найти дополнительные сведения о указанных файлах, такие как имена и номера версий всех библиотек DLL.</span><span class="sxs-lookup"><span data-stu-id="0d58e-117">The user can then seek additional details about the specified files, such as the names and version numbers of all the DLLs.</span></span> <span data-ttu-id="0d58e-118">MAPI использует эти свойства для создания списка файлов поддержки в диалоговом окне для выбора пользователя в обмене сообщениями.</span><span class="sxs-lookup"><span data-stu-id="0d58e-118">MAPI uses the these properties to create a support file list in a dialog box for messaging user selection.</span></span>
  
<span data-ttu-id="0d58e-119">MAPI работает только с именами файлов и другими строками, передаваемыми в нее, в наборе символов ANSI (интерфейсы службы Active Directory).</span><span class="sxs-lookup"><span data-stu-id="0d58e-119">MAPI works only with filenames, and other strings passed to it, in the Active Directory Service Interfaces (ANSI) character set.</span></span> <span data-ttu-id="0d58e-120">Клиентские приложения, использующие имена файлов в наборе символов ПВТ, должны преобразовать их в ANSI перед вызовом функции MAPI.</span><span class="sxs-lookup"><span data-stu-id="0d58e-120">Client applications that use filenames in an original equipment manufacturer (OEM) character set must convert them to ANSI before calling MAPI.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0d58e-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="0d58e-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="0d58e-122">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="0d58e-122">Header files</span></span>

<span data-ttu-id="0d58e-123">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="0d58e-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="0d58e-124">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="0d58e-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="0d58e-125">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="0d58e-125">Mapitags.h</span></span>
  
> <span data-ttu-id="0d58e-126">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="0d58e-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0d58e-127">См. также</span><span class="sxs-lookup"><span data-stu-id="0d58e-127">See also</span></span>



[<span data-ttu-id="0d58e-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0d58e-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0d58e-129">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="0d58e-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0d58e-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="0d58e-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0d58e-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="0d58e-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

