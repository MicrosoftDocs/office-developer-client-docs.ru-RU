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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286490"
---
# <a name="pidtagproviderdllname-canonical-property"></a><span data-ttu-id="8bba8-103">Каноническое свойство PidTagProviderDllName</span><span class="sxs-lookup"><span data-stu-id="8bba8-103">PidTagProviderDllName Canonical Property</span></span>

  
  
<span data-ttu-id="8bba8-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8bba8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8bba8-105">Содержит базовое имя файла библиотеки динамической ссылки поставщика служб MAPI (DLL).</span><span class="sxs-lookup"><span data-stu-id="8bba8-105">Contains the base file name of the MAPI service provider dynamic-link library (DLL).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8bba8-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="8bba8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8bba8-107">PR_PROVIDER_DLL_NAME, PR_PROVIDER_DLL_NAME_A, PR_PROVIDER_DLL_NAME_W</span><span class="sxs-lookup"><span data-stu-id="8bba8-107">PR_PROVIDER_DLL_NAME, PR_PROVIDER_DLL_NAME_A, PR_PROVIDER_DLL_NAME_W</span></span>  <br/> |
|<span data-ttu-id="8bba8-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="8bba8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8bba8-109">0x300A</span><span class="sxs-lookup"><span data-stu-id="8bba8-109">0x300A</span></span>  <br/> |
|<span data-ttu-id="8bba8-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="8bba8-110">Data type:</span></span>  <br/> |<span data-ttu-id="8bba8-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="8bba8-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="8bba8-112">Область:</span><span class="sxs-lookup"><span data-stu-id="8bba8-112">Area:</span></span>  <br/> |<span data-ttu-id="8bba8-113">Общие mapI</span><span class="sxs-lookup"><span data-stu-id="8bba8-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8bba8-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="8bba8-114">Remarks</span></span>

<span data-ttu-id="8bba8-115">MAPI использует соглашение об именовостей файлов DLL.</span><span class="sxs-lookup"><span data-stu-id="8bba8-115">MAPI uses a DLL file naming convention.</span></span> <span data-ttu-id="8bba8-116">Он применит строку 32 к базовому имени DLL, чтобы определить версию, которая выполняется на 32-битных платформах.</span><span class="sxs-lookup"><span data-stu-id="8bba8-116">It appends the string 32 to the base DLL name to identify the version that runs on 32-bit platforms.</span></span> <span data-ttu-id="8bba8-117">Например, если задан MAPI.DLL имя, MAPI MAPI32.DLL имя для представления соответствующей 32-битной версии DLL.</span><span class="sxs-lookup"><span data-stu-id="8bba8-117">For example, when the name MAPI.DLL is specified, MAPI constructs the name MAPI32.DLL to represent the corresponding 32-bit version of the DLL.</span></span>
  
<span data-ttu-id="8bba8-118">Эти свойства должны указывать базовое имя.</span><span class="sxs-lookup"><span data-stu-id="8bba8-118">These properties should specify the base name.</span></span> <span data-ttu-id="8bba8-119">MAPI при необходимости применит строку 32.</span><span class="sxs-lookup"><span data-stu-id="8bba8-119">MAPI appends the string 32 as appropriate.</span></span> <span data-ttu-id="8bba8-120">Если строка 32 будет частью этого свойства, будет выявить ошибку.</span><span class="sxs-lookup"><span data-stu-id="8bba8-120">Including the string 32 as part of this property results in an error.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8bba8-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="8bba8-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="8bba8-122">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="8bba8-122">Header files</span></span>

<span data-ttu-id="8bba8-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8bba8-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="8bba8-124">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="8bba8-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="8bba8-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8bba8-125">Mapitags.h</span></span>
  
> <span data-ttu-id="8bba8-126">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="8bba8-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8bba8-127">См. также</span><span class="sxs-lookup"><span data-stu-id="8bba8-127">See also</span></span>



[<span data-ttu-id="8bba8-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8bba8-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8bba8-129">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8bba8-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8bba8-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="8bba8-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8bba8-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="8bba8-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

