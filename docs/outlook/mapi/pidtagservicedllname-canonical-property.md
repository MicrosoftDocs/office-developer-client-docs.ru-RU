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
ms.openlocfilehash: 54fe624c98ddb631326853f387372468a61b2f70
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811912"
---
# <a name="pidtagservicedllname-canonical-property"></a><span data-ttu-id="4738e-103">Каноническое свойство PidTagServiceDllName</span><span class="sxs-lookup"><span data-stu-id="4738e-103">PidTagServiceDllName Canonical Property</span></span>

  
  
<span data-ttu-id="4738e-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4738e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4738e-105">Содержит имя файла библиотеки DLL, содержащей функцию точки входа поставщика службы сообщение будет вызываться для конфигурации.</span><span class="sxs-lookup"><span data-stu-id="4738e-105">Contains the filename of the DLL containing the message service provider entry point function to call for configuration.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4738e-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="4738e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4738e-107">PR_SERVICE_DLL_NAME, PR_SERVICE_DLL_NAME_A, PR_SERVICE_DLL_NAME_W</span><span class="sxs-lookup"><span data-stu-id="4738e-107">PR_SERVICE_DLL_NAME, PR_SERVICE_DLL_NAME_A, PR_SERVICE_DLL_NAME_W</span></span>  <br/> |
|<span data-ttu-id="4738e-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="4738e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4738e-109">0x3D0A</span><span class="sxs-lookup"><span data-stu-id="4738e-109">0x3D0A</span></span>  <br/> |
|<span data-ttu-id="4738e-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="4738e-110">Data type:</span></span>  <br/> |<span data-ttu-id="4738e-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4738e-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="4738e-112">Область:</span><span class="sxs-lookup"><span data-stu-id="4738e-112">Area:</span></span>  <br/> |<span data-ttu-id="4738e-113">Профиль MAPI</span><span class="sxs-lookup"><span data-stu-id="4738e-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4738e-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="4738e-114">Remarks</span></span>

<span data-ttu-id="4738e-115">Когда появится имя функции точки входа в метод **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)), указывает, что существует точка входа.</span><span class="sxs-lookup"><span data-stu-id="4738e-115">When the entry point function name appears in the **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) method, it indicates that the entry point exists.</span></span>
  
<span data-ttu-id="4738e-116">MAPI использует соглашение об именовании файл DLL.</span><span class="sxs-lookup"><span data-stu-id="4738e-116">MAPI uses a DLL file naming convention.</span></span> <span data-ttu-id="4738e-117">Базовое имя файла содержит до шести символов, которые однозначно идентифицируют библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="4738e-117">The base filename contains up to six characters that uniquely identify the DLL.</span></span> <span data-ttu-id="4738e-118">MAPI добавляет строку 32 базовое имя DLL-Библиотеку для идентификации версии, на котором работает на 32-разрядных платформ.</span><span class="sxs-lookup"><span data-stu-id="4738e-118">MAPI appends the string 32 to the base DLL name to identify the version that runs on 32-bit platforms.</span></span> <span data-ttu-id="4738e-119">Например, если имя MAPI. Указан DLL-Библиотеку, MAPI создает имя MAPI32. DLL-Библиотеку для представления соответствующих 32-разрядная версия библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="4738e-119">For example, when the name MAPI.DLL is specified, MAPI constructs the name MAPI32.DLL to represent the corresponding 32-bit version of the DLL.</span></span>
  
<span data-ttu-id="4738e-120">Эти свойства следует указать базовое имя.</span><span class="sxs-lookup"><span data-stu-id="4738e-120">These properties should specify the base name.</span></span> <span data-ttu-id="4738e-121">MAPI добавляет строку 32 соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="4738e-121">MAPI appends the string 32 as appropriate.</span></span> <span data-ttu-id="4738e-122">Строка 32, включая как часть этих свойств приводят к ошибке.</span><span class="sxs-lookup"><span data-stu-id="4738e-122">Including the string 32 as part of these properties result in an error.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4738e-123">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="4738e-123">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="4738e-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="4738e-124">Header files</span></span>

<span data-ttu-id="4738e-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4738e-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="4738e-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="4738e-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="4738e-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4738e-127">Mapitags.h</span></span>
  
> <span data-ttu-id="4738e-128">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="4738e-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4738e-129">См. также</span><span class="sxs-lookup"><span data-stu-id="4738e-129">See also</span></span>



[<span data-ttu-id="4738e-130">Каноническое свойство PidTagProviderDllName</span><span class="sxs-lookup"><span data-stu-id="4738e-130">PidTagProviderDllName Canonical Property</span></span>](pidtagproviderdllname-canonical-property.md)


[<span data-ttu-id="4738e-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="4738e-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4738e-132">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="4738e-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4738e-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="4738e-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4738e-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="4738e-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

