---
title: Каноническое свойство PidTagProviderDllName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderDllName
api_type:
- COM
ms.assetid: 9ddb38eb-9a32-4dbe-b42c-6ea9db98acd2
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 57fdc754ed4be29dbdd50a198707d8f39a14b3d4
ms.sourcegitcommit: 18f3d9462048859fe040e12136ff66f19066764b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2019
ms.locfileid: "31980462"
---
# <a name="pidtagproviderdllname-canonical-property"></a><span data-ttu-id="ed198-103">Каноническое свойство PidTagProviderDllName</span><span class="sxs-lookup"><span data-stu-id="ed198-103">PidTagProviderDllName Canonical Property</span></span>

  
  
<span data-ttu-id="ed198-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ed198-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ed198-105">Содержит базовое имя файла библиотеки динамической компоновки (DLL) поставщика службы MAPI.</span><span class="sxs-lookup"><span data-stu-id="ed198-105">Contains the base file name of the MAPI service provider dynamic-link library (DLL).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ed198-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="ed198-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ed198-107">ПР_ПРОВИДЕР_ДЛЛ_НАМЕ, ПР_ПРОВИДЕР_ДЛЛ_НАМЕ_А, ПР_ПРОВИДЕР_ДЛЛ_НАМЕ_В</span><span class="sxs-lookup"><span data-stu-id="ed198-107">PR_PROVIDER_DLL_NAME, PR_PROVIDER_DLL_NAME_A, PR_PROVIDER_DLL_NAME_W</span></span>  <br/> |
|<span data-ttu-id="ed198-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="ed198-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ed198-109">0x300A</span><span class="sxs-lookup"><span data-stu-id="ed198-109">0x300A</span></span>  <br/> |
|<span data-ttu-id="ed198-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="ed198-110">Data type:</span></span>  <br/> |<span data-ttu-id="ed198-111">PT_STRING8, ПТ_УНИКОДЕ</span><span class="sxs-lookup"><span data-stu-id="ed198-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="ed198-112">Область:</span><span class="sxs-lookup"><span data-stu-id="ed198-112">Area:</span></span>  <br/> |<span data-ttu-id="ed198-113">Общие протоколы MAPI</span><span class="sxs-lookup"><span data-stu-id="ed198-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ed198-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="ed198-114">Remarks</span></span>

<span data-ttu-id="ed198-115">MAPI использует соглашение об именовании файлов DLL.</span><span class="sxs-lookup"><span data-stu-id="ed198-115">MAPI uses a DLL file naming convention.</span></span> <span data-ttu-id="ed198-116">Он добавляет к имени базового DLL строку 32, чтобы определить версию, работающую на 32 разрядных платформах.</span><span class="sxs-lookup"><span data-stu-id="ed198-116">It appends the string 32 to the base DLL name to identify the version that runs on 32-bit platforms.</span></span> <span data-ttu-id="ed198-117">Например, если имя MAPI. DLL, то MAPI создает имя MAPI32. DLL для представления соответствующей 32 разрядной версии DLL.</span><span class="sxs-lookup"><span data-stu-id="ed198-117">For example, when the name MAPI.DLL is specified, MAPI constructs the name MAPI32.DLL to represent the corresponding 32-bit version of the DLL.</span></span>
  
<span data-ttu-id="ed198-118">Эти свойства должны указывать базовое имя.</span><span class="sxs-lookup"><span data-stu-id="ed198-118">These properties should specify the base name.</span></span> <span data-ttu-id="ed198-119">MAPI добавляет строку 32 в соответствии с требованиями.</span><span class="sxs-lookup"><span data-stu-id="ed198-119">MAPI appends the string 32 as appropriate.</span></span> <span data-ttu-id="ed198-120">Включение строки 32 в качестве части этого свойства приводит к ошибке.</span><span class="sxs-lookup"><span data-stu-id="ed198-120">Including the string 32 as part of this property results in an error.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ed198-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ed198-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="ed198-122">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="ed198-122">Header files</span></span>

<span data-ttu-id="ed198-123">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="ed198-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="ed198-124">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="ed198-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="ed198-125">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="ed198-125">Mapitags.h</span></span>
  
> <span data-ttu-id="ed198-126">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="ed198-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ed198-127">См. также</span><span class="sxs-lookup"><span data-stu-id="ed198-127">See also</span></span>



[<span data-ttu-id="ed198-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ed198-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ed198-129">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="ed198-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ed198-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="ed198-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ed198-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="ed198-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

