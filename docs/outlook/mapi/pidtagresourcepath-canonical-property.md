---
title: Каноническое свойство PidTagResourcePath
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResourcePath
api_type:
- COM
ms.assetid: ac49538e-6ee8-4ab4-9d79-88a83c7d0149
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a00abec7627eb12e23e7b76f5d0900514d710ffb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593097"
---
# <a name="pidtagresourcepath-canonical-property"></a><span data-ttu-id="44cd3-103">Каноническое свойство PidTagResourcePath</span><span class="sxs-lookup"><span data-stu-id="44cd3-103">PidTagResourcePath Canonical Property</span></span>

  
  
<span data-ttu-id="44cd3-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="44cd3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="44cd3-105">Содержит путь к серверу поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="44cd3-105">Contains a path to the service provider's server.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="44cd3-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="44cd3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="44cd3-107">PR_RESOURCE_PATH, PR_RESOURCE_PATH_A, PR_RESOURCE_PATH_W</span><span class="sxs-lookup"><span data-stu-id="44cd3-107">PR_RESOURCE_PATH, PR_RESOURCE_PATH_A, PR_RESOURCE_PATH_W</span></span>  <br/> |
|<span data-ttu-id="44cd3-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="44cd3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="44cd3-109">0x3E07</span><span class="sxs-lookup"><span data-stu-id="44cd3-109">0x3E07</span></span>  <br/> |
|<span data-ttu-id="44cd3-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="44cd3-110">Data type:</span></span>  <br/> |<span data-ttu-id="44cd3-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="44cd3-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="44cd3-112">Область:</span><span class="sxs-lookup"><span data-stu-id="44cd3-112">Area:</span></span>  <br/> |<span data-ttu-id="44cd3-113">Состояние MAPI</span><span class="sxs-lookup"><span data-stu-id="44cd3-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="44cd3-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="44cd3-114">Remarks</span></span>

<span data-ttu-id="44cd3-115">Путь, содержащийся в эти свойства представляет предложенный путь, где пользователь может найти ресурсы.</span><span class="sxs-lookup"><span data-stu-id="44cd3-115">The path contained in these properties represents the suggested path where the user can find resources.</span></span> <span data-ttu-id="44cd3-116">Определение этих свойств зависит от поставщика.</span><span class="sxs-lookup"><span data-stu-id="44cd3-116">The definition of these properties is provider specific.</span></span> <span data-ttu-id="44cd3-117">Например планирования приложение использует эти свойства для указания предложенного расположения для ее планирования файлы приложения.</span><span class="sxs-lookup"><span data-stu-id="44cd3-117">For example, a scheduling application uses these properties to specify the suggested location for its scheduling application files.</span></span>
  
<span data-ttu-id="44cd3-118">Эти свойства предоставляющей обмена сообщениями профилей пользователей для удобства, чтобы клиентского приложения не нужно запрашивать обмена сообщениями для сетевой путь или сетевого диска.</span><span class="sxs-lookup"><span data-stu-id="44cd3-118">The messaging user profile furnishes these properties as a convenience so that a client application does not have to prompt the messaging user for a network path or network drive letter.</span></span>
  
<span data-ttu-id="44cd3-119">MAPI работает только с именами файлов в набор знаков American National стандартов института (ANSI).</span><span class="sxs-lookup"><span data-stu-id="44cd3-119">MAPI works only with filenames in the American National Standards Institute (ANSI) character set.</span></span> <span data-ttu-id="44cd3-120">Приложения, использующие имена файлов в набор символов (ПВТ) необходимо преобразовать их в формате ANSI перед вызовом MAPI.</span><span class="sxs-lookup"><span data-stu-id="44cd3-120">Applications that use filenames in an original equipment manufacturer (OEM) character set must convert them to ANSI before calling MAPI.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="44cd3-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="44cd3-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="44cd3-122">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="44cd3-122">Header files</span></span>

<span data-ttu-id="44cd3-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="44cd3-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="44cd3-124">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="44cd3-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="44cd3-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="44cd3-125">Mapitags.h</span></span>
  
> <span data-ttu-id="44cd3-126">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="44cd3-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="44cd3-127">См. также</span><span class="sxs-lookup"><span data-stu-id="44cd3-127">See also</span></span>



[<span data-ttu-id="44cd3-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="44cd3-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="44cd3-129">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="44cd3-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="44cd3-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="44cd3-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="44cd3-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="44cd3-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

