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
ms.openlocfilehash: 3bf6347102fc0865b081847a0b66763ba2654665
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589485"
---
# <a name="pidtagproviderdllname-canonical-property"></a><span data-ttu-id="3f9de-103">Каноническое свойство PidTagProviderDllName</span><span class="sxs-lookup"><span data-stu-id="3f9de-103">PidTagProviderDllName Canonical Property</span></span>

  
  
<span data-ttu-id="3f9de-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3f9de-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3f9de-105">Содержит имя базового файла библиотеки динамической компоновки поставщика служб MAPI (DLL).</span><span class="sxs-lookup"><span data-stu-id="3f9de-105">Contains the base file name of the MAPI service provider dynamic-link library (DLL).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3f9de-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="3f9de-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3f9de-107">PR_PROVIDER_DLL_NAME, PR_PROVIDER_DLL_NAME_A, PR_PROVIDER_DLL_NAME_W</span><span class="sxs-lookup"><span data-stu-id="3f9de-107">PR_PROVIDER_DLL_NAME, PR_PROVIDER_DLL_NAME_A, PR_PROVIDER_DLL_NAME_W</span></span>  <br/> |
|<span data-ttu-id="3f9de-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="3f9de-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3f9de-109">0x300A</span><span class="sxs-lookup"><span data-stu-id="3f9de-109">0x300A</span></span>  <br/> |
|<span data-ttu-id="3f9de-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="3f9de-110">Data type:</span></span>  <br/> |<span data-ttu-id="3f9de-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3f9de-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="3f9de-112">Область:</span><span class="sxs-lookup"><span data-stu-id="3f9de-112">Area:</span></span>  <br/> |<span data-ttu-id="3f9de-113">Распространенные MAPI</span><span class="sxs-lookup"><span data-stu-id="3f9de-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3f9de-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="3f9de-114">Remarks</span></span>

<span data-ttu-id="3f9de-115">MAPI использует соглашение об именовании файл DLL.</span><span class="sxs-lookup"><span data-stu-id="3f9de-115">MAPI uses a DLL file naming convention.</span></span> <span data-ttu-id="3f9de-116">Базовое имя файла содержит до шести символов, которые однозначно идентифицируют библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="3f9de-116">The base filename contains up to six characters that uniquely identify the DLL.</span></span> <span data-ttu-id="3f9de-117">MAPI добавляет строку 32 базовое имя DLL-Библиотеку для идентификации версии, на котором работает на 32-разрядных платформ.</span><span class="sxs-lookup"><span data-stu-id="3f9de-117">MAPI appends the string 32 to the base DLL name to identify the version that runs on 32-bit platforms.</span></span> <span data-ttu-id="3f9de-118">Например, если имя MAPI. Указан DLL-Библиотеку, MAPI создает имя MAPI32. DLL-Библиотеку для представления соответствующих 32-разрядная версия библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="3f9de-118">For example, when the name MAPI.DLL is specified, MAPI constructs the name MAPI32.DLL to represent the corresponding 32-bit version of the DLL.</span></span>
  
<span data-ttu-id="3f9de-119">Эти свойства следует указать базовое имя.</span><span class="sxs-lookup"><span data-stu-id="3f9de-119">These properties should specify the base name.</span></span> <span data-ttu-id="3f9de-120">MAPI добавляет строку 32 соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="3f9de-120">MAPI appends the string 32 as appropriate.</span></span> <span data-ttu-id="3f9de-121">Как часть этого свойства приводит к ошибке, включая строку 32.</span><span class="sxs-lookup"><span data-stu-id="3f9de-121">Including the string 32 as part of this property results in an error.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3f9de-122">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="3f9de-122">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="3f9de-123">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="3f9de-123">Header files</span></span>

<span data-ttu-id="3f9de-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3f9de-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="3f9de-125">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="3f9de-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="3f9de-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3f9de-126">Mapitags.h</span></span>
  
> <span data-ttu-id="3f9de-127">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="3f9de-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3f9de-128">См. также</span><span class="sxs-lookup"><span data-stu-id="3f9de-128">See also</span></span>



[<span data-ttu-id="3f9de-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="3f9de-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3f9de-130">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="3f9de-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3f9de-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="3f9de-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3f9de-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="3f9de-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

