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
ms.sourcegitcommit: 18f3d9462048859fe040e12136ff66f19066764b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2019
ms.locfileid: "31980457"
---
# <a name="pidtagservicedllname-canonical-property"></a><span data-ttu-id="d27ac-103">Каноническое свойство PidTagServiceDllName</span><span class="sxs-lookup"><span data-stu-id="d27ac-103">PidTagServiceDllName Canonical Property</span></span>

  
  
<span data-ttu-id="d27ac-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d27ac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d27ac-105">Содержит имя библиотеки DLL, содержащей функцию точки входа поставщика службы сообщений, которую необходимо вызвать для настройки.</span><span class="sxs-lookup"><span data-stu-id="d27ac-105">Contains the filename of the DLL containing the message service provider entry point function to call for configuration.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d27ac-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="d27ac-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d27ac-107">ПР_СЕРВИЦЕ_ДЛЛ_НАМЕ, ПР_СЕРВИЦЕ_ДЛЛ_НАМЕ_А, ПР_СЕРВИЦЕ_ДЛЛ_НАМЕ_В</span><span class="sxs-lookup"><span data-stu-id="d27ac-107">PR_SERVICE_DLL_NAME, PR_SERVICE_DLL_NAME_A, PR_SERVICE_DLL_NAME_W</span></span>  <br/> |
|<span data-ttu-id="d27ac-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="d27ac-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d27ac-109">0x3D0A</span><span class="sxs-lookup"><span data-stu-id="d27ac-109">0x3D0A</span></span>  <br/> |
|<span data-ttu-id="d27ac-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="d27ac-110">Data type:</span></span>  <br/> |<span data-ttu-id="d27ac-111">PT_STRING8, ПТ_УНИКОДЕ</span><span class="sxs-lookup"><span data-stu-id="d27ac-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="d27ac-112">Область:</span><span class="sxs-lookup"><span data-stu-id="d27ac-112">Area:</span></span>  <br/> |<span data-ttu-id="d27ac-113">Профиль MAPI</span><span class="sxs-lookup"><span data-stu-id="d27ac-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d27ac-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="d27ac-114">Remarks</span></span>

<span data-ttu-id="d27ac-115">Если имя функции в точке входа присутствует в методе **пр_сервице_ентри_наме** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)), оно указывает, что точка входа существует.</span><span class="sxs-lookup"><span data-stu-id="d27ac-115">When the entry point function name appears in the **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) method, it indicates that the entry point exists.</span></span>
  
<span data-ttu-id="d27ac-116">MAPI использует соглашение об именовании файлов DLL.</span><span class="sxs-lookup"><span data-stu-id="d27ac-116">MAPI uses a DLL file naming convention.</span></span> <span data-ttu-id="d27ac-117">Он добавляет к имени базового DLL строку 32, чтобы определить версию, работающую на 32 разрядных платформах.</span><span class="sxs-lookup"><span data-stu-id="d27ac-117">It appends the string 32 to the base DLL name to identify the version that runs on 32-bit platforms.</span></span> <span data-ttu-id="d27ac-118">Например, если имя MAPI. DLL, то MAPI создает имя MAPI32. DLL для представления соответствующей 32 разрядной версии DLL.</span><span class="sxs-lookup"><span data-stu-id="d27ac-118">For example, when the name MAPI.DLL is specified, MAPI constructs the name MAPI32.DLL to represent the corresponding 32-bit version of the DLL.</span></span>
  
<span data-ttu-id="d27ac-119">Эти свойства должны указывать базовое имя.</span><span class="sxs-lookup"><span data-stu-id="d27ac-119">These properties should specify the base name.</span></span> <span data-ttu-id="d27ac-120">MAPI добавляет строку 32 в соответствии с требованиями.</span><span class="sxs-lookup"><span data-stu-id="d27ac-120">MAPI appends the string 32 as appropriate.</span></span> <span data-ttu-id="d27ac-121">Включение строки 32 в состав этих свойств приводит к ошибке.</span><span class="sxs-lookup"><span data-stu-id="d27ac-121">Including the string 32 as part of these properties result in an error.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d27ac-122">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d27ac-122">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="d27ac-123">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="d27ac-123">Header files</span></span>

<span data-ttu-id="d27ac-124">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="d27ac-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="d27ac-125">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="d27ac-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="d27ac-126">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="d27ac-126">Mapitags.h</span></span>
  
> <span data-ttu-id="d27ac-127">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="d27ac-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d27ac-128">См. также</span><span class="sxs-lookup"><span data-stu-id="d27ac-128">See also</span></span>



[<span data-ttu-id="d27ac-129">Каноническое свойство PidTagProviderDllName</span><span class="sxs-lookup"><span data-stu-id="d27ac-129">PidTagProviderDllName Canonical Property</span></span>](pidtagproviderdllname-canonical-property.md)


[<span data-ttu-id="d27ac-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d27ac-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d27ac-131">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="d27ac-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d27ac-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="d27ac-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d27ac-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="d27ac-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

