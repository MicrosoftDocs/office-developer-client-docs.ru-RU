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
ms.openlocfilehash: 5165867e46d3d86d65932e7ae432b446efbd8fff
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589128"
---
# <a name="pidtagservicesupportfiles-canonical-property"></a><span data-ttu-id="f5f03-103">Каноническое свойство PidTagServiceSupportFiles</span><span class="sxs-lookup"><span data-stu-id="f5f03-103">PidTagServiceSupportFiles Canonical Property</span></span>

  
  
<span data-ttu-id="f5f03-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f5f03-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f5f03-105">Содержит список файлов, относящихся к службе сообщений.</span><span class="sxs-lookup"><span data-stu-id="f5f03-105">Contains a list of the files that belong to the message service.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f5f03-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="f5f03-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f5f03-107">PR_SERVICE_SUPPORT_FILES, PR_SERVICE_SUPPORT_FILES_A, PR_SERVICE_SUPPORT_FILES_W</span><span class="sxs-lookup"><span data-stu-id="f5f03-107">PR_SERVICE_SUPPORT_FILES, PR_SERVICE_SUPPORT_FILES_A, PR_SERVICE_SUPPORT_FILES_W</span></span>  <br/> |
|<span data-ttu-id="f5f03-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="f5f03-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f5f03-109">0x3D0F</span><span class="sxs-lookup"><span data-stu-id="f5f03-109">0x3D0F</span></span>  <br/> |
|<span data-ttu-id="f5f03-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="f5f03-110">Data type:</span></span>  <br/> |<span data-ttu-id="f5f03-111">PT_MV_STRING8 PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f5f03-111">PT_MV_STRING8, PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="f5f03-112">Область:</span><span class="sxs-lookup"><span data-stu-id="f5f03-112">Area:</span></span>  <br/> |<span data-ttu-id="f5f03-113">Профиль MAPI</span><span class="sxs-lookup"><span data-stu-id="f5f03-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f5f03-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="f5f03-114">Remarks</span></span>

<span data-ttu-id="f5f03-115">Используя диалоговое окно "" в панели управления, пользователь может получить список файлов, относящихся к службе сообщений.</span><span class="sxs-lookup"><span data-stu-id="f5f03-115">Using a dialog box in the control panel applet, a user can obtain the list of files that belong to the message service.</span></span> <span data-ttu-id="f5f03-116">Например пользователь может получить имена все библиотеки динамической компоновки (DLL), относящихся к службе.</span><span class="sxs-lookup"><span data-stu-id="f5f03-116">For example, the user can obtain the names of all dynamic-link libraries (DLLs) that belong to the service.</span></span> <span data-ttu-id="f5f03-117">Пользователь затем может выполнять поиск дополнительных сведений об указанных файлов, таких как имена и номера версий всех библиотек DLL.</span><span class="sxs-lookup"><span data-stu-id="f5f03-117">The user can then seek additional details about the specified files, such as the names and version numbers of all the DLLs.</span></span> <span data-ttu-id="f5f03-118">MAPI использует эти свойства, чтобы создать список файлов поддержки в диалоговом окне Выбор пользователей системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="f5f03-118">MAPI uses the these properties to create a support file list in a dialog box for messaging user selection.</span></span>
  
<span data-ttu-id="f5f03-119">MAPI для работы только с имена файлов и другие строки, переданным в него, в наборе символов интерфейсов службы Active Directory (ANSI).</span><span class="sxs-lookup"><span data-stu-id="f5f03-119">MAPI works only with filenames, and other strings passed to it, in the Active Directory Service Interfaces (ANSI) character set.</span></span> <span data-ttu-id="f5f03-120">Клиентские приложения, использующие имена файлов в набор символов (ПВТ) необходимо преобразовать их в формате ANSI перед вызовом MAPI.</span><span class="sxs-lookup"><span data-stu-id="f5f03-120">Client applications that use filenames in an original equipment manufacturer (OEM) character set must convert them to ANSI before calling MAPI.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f5f03-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f5f03-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="f5f03-122">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="f5f03-122">Header files</span></span>

<span data-ttu-id="f5f03-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f5f03-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="f5f03-124">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="f5f03-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="f5f03-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f5f03-125">Mapitags.h</span></span>
  
> <span data-ttu-id="f5f03-126">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="f5f03-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f5f03-127">См. также</span><span class="sxs-lookup"><span data-stu-id="f5f03-127">See also</span></span>



[<span data-ttu-id="f5f03-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f5f03-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f5f03-129">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f5f03-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f5f03-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="f5f03-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f5f03-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="f5f03-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

