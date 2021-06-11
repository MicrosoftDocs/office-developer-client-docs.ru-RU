---
title: Каноническое свойство PidTagServiceDllName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceDllName
api_type:
- COM
ms.assetid: a651af84-1711-449e-ba7e-5ce09cafa02b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: adf24bcd02d7efc303f911ee01a64325150339ce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330067"
---
# <a name="pidtagservicedllname-canonical-property"></a><span data-ttu-id="b0adb-103">Каноническое свойство PidTagServiceDllName</span><span class="sxs-lookup"><span data-stu-id="b0adb-103">PidTagServiceDllName Canonical Property</span></span>

  
  
<span data-ttu-id="b0adb-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b0adb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b0adb-105">Содержит имя файла DLL, содержащего функцию точки входа поставщика сообщений для вызова конфигурации.</span><span class="sxs-lookup"><span data-stu-id="b0adb-105">Contains the filename of the DLL containing the message service provider entry point function to call for configuration.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b0adb-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="b0adb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b0adb-107">PR_SERVICE_DLL_NAME, PR_SERVICE_DLL_NAME_A, PR_SERVICE_DLL_NAME_W</span><span class="sxs-lookup"><span data-stu-id="b0adb-107">PR_SERVICE_DLL_NAME, PR_SERVICE_DLL_NAME_A, PR_SERVICE_DLL_NAME_W</span></span>  <br/> |
|<span data-ttu-id="b0adb-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="b0adb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b0adb-109">0x3D0A</span><span class="sxs-lookup"><span data-stu-id="b0adb-109">0x3D0A</span></span>  <br/> |
|<span data-ttu-id="b0adb-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="b0adb-110">Data type:</span></span>  <br/> |<span data-ttu-id="b0adb-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b0adb-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="b0adb-112">Область:</span><span class="sxs-lookup"><span data-stu-id="b0adb-112">Area:</span></span>  <br/> |<span data-ttu-id="b0adb-113">Профиль MAPI</span><span class="sxs-lookup"><span data-stu-id="b0adb-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b0adb-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="b0adb-114">Remarks</span></span>

<span data-ttu-id="b0adb-115">Когда имя функции точки входа отображается в **методе PR_SERVICE_ENTRY_NAME** [(PidTagServiceEntryName),](pidtagserviceentryname-canonical-property.md)это указывает на существование точки входа.</span><span class="sxs-lookup"><span data-stu-id="b0adb-115">When the entry point function name appears in the **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) method, it indicates that the entry point exists.</span></span>
  
<span data-ttu-id="b0adb-116">MAPI использует конвенцию именования файлов DLL.</span><span class="sxs-lookup"><span data-stu-id="b0adb-116">MAPI uses a DLL file naming convention.</span></span> <span data-ttu-id="b0adb-117">Он применит строку 32 к базовому имени DLL, чтобы определить версию, которая выполняется на 32-битных платформах.</span><span class="sxs-lookup"><span data-stu-id="b0adb-117">It appends the string 32 to the base DLL name to identify the version that runs on 32-bit platforms.</span></span> <span data-ttu-id="b0adb-118">Например, когда MAPI.DLL имя, MAPI строит имя MAPI32.DLL для представления соответствующей 32-битной версии DLL.</span><span class="sxs-lookup"><span data-stu-id="b0adb-118">For example, when the name MAPI.DLL is specified, MAPI constructs the name MAPI32.DLL to represent the corresponding 32-bit version of the DLL.</span></span>
  
<span data-ttu-id="b0adb-119">Эти свойства должны указывать базовое имя.</span><span class="sxs-lookup"><span data-stu-id="b0adb-119">These properties should specify the base name.</span></span> <span data-ttu-id="b0adb-120">MAPI применит строку 32 по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="b0adb-120">MAPI appends the string 32 as appropriate.</span></span> <span data-ttu-id="b0adb-121">В том числе строка 32 в составе этих свойств приводит к ошибке.</span><span class="sxs-lookup"><span data-stu-id="b0adb-121">Including the string 32 as part of these properties result in an error.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b0adb-122">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b0adb-122">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="b0adb-123">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="b0adb-123">Header files</span></span>

<span data-ttu-id="b0adb-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b0adb-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="b0adb-125">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="b0adb-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="b0adb-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b0adb-126">Mapitags.h</span></span>
  
> <span data-ttu-id="b0adb-127">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="b0adb-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b0adb-128">См. также</span><span class="sxs-lookup"><span data-stu-id="b0adb-128">See also</span></span>



[<span data-ttu-id="b0adb-129">Каноническое свойство PidTagProviderDllName</span><span class="sxs-lookup"><span data-stu-id="b0adb-129">PidTagProviderDllName Canonical Property</span></span>](pidtagproviderdllname-canonical-property.md)


[<span data-ttu-id="b0adb-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b0adb-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b0adb-131">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b0adb-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b0adb-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="b0adb-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b0adb-133">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="b0adb-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

