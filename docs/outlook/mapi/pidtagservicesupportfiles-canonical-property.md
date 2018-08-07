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
ms.openlocfilehash: 2dc431d807bd74640e5b5a9c020f668b13530197
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811945"
---
# <a name="pidtagservicesupportfiles-canonical-property"></a><span data-ttu-id="0c1b1-103">Каноническое свойство PidTagServiceSupportFiles</span><span class="sxs-lookup"><span data-stu-id="0c1b1-103">PidTagServiceSupportFiles Canonical Property</span></span>

  
  
<span data-ttu-id="0c1b1-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0c1b1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0c1b1-105">Содержит список файлов, относящихся к службе сообщений.</span><span class="sxs-lookup"><span data-stu-id="0c1b1-105">Contains a list of the files that belong to the message service.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0c1b1-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="0c1b1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0c1b1-107">PR_SERVICE_SUPPORT_FILES, PR_SERVICE_SUPPORT_FILES_A, PR_SERVICE_SUPPORT_FILES_W</span><span class="sxs-lookup"><span data-stu-id="0c1b1-107">PR_SERVICE_SUPPORT_FILES, PR_SERVICE_SUPPORT_FILES_A, PR_SERVICE_SUPPORT_FILES_W</span></span>  <br/> |
|<span data-ttu-id="0c1b1-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="0c1b1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0c1b1-109">0x3D0F</span><span class="sxs-lookup"><span data-stu-id="0c1b1-109">0x3D0F</span></span>  <br/> |
|<span data-ttu-id="0c1b1-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="0c1b1-110">Data type:</span></span>  <br/> |<span data-ttu-id="0c1b1-111">PT_MV_STRING8 PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0c1b1-111">PT_MV_STRING8, PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="0c1b1-112">Область:</span><span class="sxs-lookup"><span data-stu-id="0c1b1-112">Area:</span></span>  <br/> |<span data-ttu-id="0c1b1-113">Профиль MAPI</span><span class="sxs-lookup"><span data-stu-id="0c1b1-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0c1b1-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="0c1b1-114">Remarks</span></span>

<span data-ttu-id="0c1b1-115">Используя диалоговое окно "" в панели управления, пользователь может получить список файлов, относящихся к службе сообщений.</span><span class="sxs-lookup"><span data-stu-id="0c1b1-115">Using a dialog box in the control panel applet, a user can obtain the list of files that belong to the message service.</span></span> <span data-ttu-id="0c1b1-116">Например пользователь может получить имена все библиотеки динамической компоновки (DLL), относящихся к службе.</span><span class="sxs-lookup"><span data-stu-id="0c1b1-116">For example, the user can obtain the names of all dynamic-link libraries (DLLs) that belong to the service.</span></span> <span data-ttu-id="0c1b1-117">Пользователь затем может выполнять поиск дополнительных сведений об указанных файлов, таких как имена и номера версий всех библиотек DLL.</span><span class="sxs-lookup"><span data-stu-id="0c1b1-117">The user can then seek additional details about the specified files, such as the names and version numbers of all the DLLs.</span></span> <span data-ttu-id="0c1b1-118">MAPI использует эти свойства, чтобы создать список файлов поддержки в диалоговом окне Выбор пользователей системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="0c1b1-118">MAPI uses the these properties to create a support file list in a dialog box for messaging user selection.</span></span>
  
<span data-ttu-id="0c1b1-119">MAPI для работы только с имена файлов и другие строки, переданным в него, в наборе символов интерфейсов службы Active Directory (ANSI).</span><span class="sxs-lookup"><span data-stu-id="0c1b1-119">MAPI works only with filenames, and other strings passed to it, in the Active Directory Service Interfaces (ANSI) character set.</span></span> <span data-ttu-id="0c1b1-120">Клиентские приложения, использующие имена файлов в набор символов (ПВТ) необходимо преобразовать их в формате ANSI перед вызовом MAPI.</span><span class="sxs-lookup"><span data-stu-id="0c1b1-120">Client applications that use filenames in an original equipment manufacturer (OEM) character set must convert them to ANSI before calling MAPI.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0c1b1-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="0c1b1-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="0c1b1-122">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="0c1b1-122">Header files</span></span>

<span data-ttu-id="0c1b1-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0c1b1-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="0c1b1-124">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="0c1b1-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="0c1b1-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0c1b1-125">Mapitags.h</span></span>
  
> <span data-ttu-id="0c1b1-126">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="0c1b1-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0c1b1-127">См. также</span><span class="sxs-lookup"><span data-stu-id="0c1b1-127">See also</span></span>



[<span data-ttu-id="0c1b1-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0c1b1-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0c1b1-129">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0c1b1-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0c1b1-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="0c1b1-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0c1b1-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="0c1b1-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

