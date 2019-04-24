---
title: Каноническое свойство PidTagInternetReferences
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInternetReferences
api_type:
- HeaderDef
ms.assetid: 645fe61d-414a-455e-b034-db3cfd003b9d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 431a212b6e024d695fe2de084080996d8b1054d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360412"
---
# <a name="pidtaginternetreferences-canonical-property"></a><span data-ttu-id="626db-103">Каноническое свойство PidTagInternetReferences</span><span class="sxs-lookup"><span data-stu-id="626db-103">PidTagInternetReferences Canonical Property</span></span>

  
  
<span data-ttu-id="626db-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="626db-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="626db-105">Содержит значение поля заголовка REFERENCES для многоцелевого почтового расширения Интернета (MIME).</span><span class="sxs-lookup"><span data-stu-id="626db-105">Contains the value of a Multipurpose Internet Mail Extensions (MIME) message's References header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="626db-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="626db-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="626db-107">ПР_ИНТЕРНЕТ_РЕФЕРЕНЦЕС, ПР_ИНТЕРНЕТ_РЕФЕРЕНЦЕС_А, ПР_ИНТЕРНЕТ_РЕФЕРЕНЦЕС_В</span><span class="sxs-lookup"><span data-stu-id="626db-107">PR_INTERNET_REFERENCES, PR_INTERNET_REFERENCES_A, PR_INTERNET_REFERENCES_W</span></span>  <br/> |
|<span data-ttu-id="626db-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="626db-108">Identifier:</span></span>  <br/> |<span data-ttu-id="626db-109">0x1039</span><span class="sxs-lookup"><span data-stu-id="626db-109">0x1039</span></span>  <br/> |
|<span data-ttu-id="626db-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="626db-110">Data type:</span></span>  <br/> |<span data-ttu-id="626db-111">PT_STRING8, ПТ_УНИКОДЕ</span><span class="sxs-lookup"><span data-stu-id="626db-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="626db-112">Область:</span><span class="sxs-lookup"><span data-stu-id="626db-112">Area:</span></span>  <br/> |<span data-ttu-id="626db-113">MIME</span><span class="sxs-lookup"><span data-stu-id="626db-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="626db-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="626db-114">Remarks</span></span>

<span data-ttu-id="626db-115">Чтобы создать поле заголовка References, клиенты должны задать для этих свойств нужное значение.</span><span class="sxs-lookup"><span data-stu-id="626db-115">To generate a References header field, clients must set these properties to the desired value.</span></span> <span data-ttu-id="626db-116">Записи MIME должны копировать значения этих свойств в поле заголовка References.</span><span class="sxs-lookup"><span data-stu-id="626db-116">MIME writers must copy the value of these properties to the References header field.</span></span>
  
<span data-ttu-id="626db-117">Чтобы задать значение этих свойств, клиенты MIME должны записать нужное значение в поле заголовка References.</span><span class="sxs-lookup"><span data-stu-id="626db-117">To set the value of these properties, MIME clients must write the desired value to a References header field.</span></span> <span data-ttu-id="626db-118">Устройства чтения MIME должны копировать значение поля заголовка References в эти свойства.</span><span class="sxs-lookup"><span data-stu-id="626db-118">MIME readers must copy the value of the References header field to these properties.</span></span> <span data-ttu-id="626db-119">Средства чтения MIME могут усечь значение этих свойств, если длина превышает 64 КБ.</span><span class="sxs-lookup"><span data-stu-id="626db-119">MIME readers may truncate the value of these properties if it exceeds 64KB in length.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="626db-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="626db-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="626db-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="626db-121">Protocol specifications</span></span>

<span data-ttu-id="626db-122">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="626db-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="626db-123">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="626db-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="626db-124">[[MS — ОКСКМАИЛ]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="626db-124">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="626db-125">Преобразует стандартные правила электронной почты из Интернета в объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="626db-125">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="626db-126">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="626db-126">Header files</span></span>

<span data-ttu-id="626db-127">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="626db-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="626db-128">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="626db-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="626db-129">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="626db-129">Mapitags.h</span></span>
  
> <span data-ttu-id="626db-130">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="626db-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="626db-131">См. также</span><span class="sxs-lookup"><span data-stu-id="626db-131">See also</span></span>



[<span data-ttu-id="626db-132">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="626db-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="626db-133">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="626db-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="626db-134">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="626db-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="626db-135">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="626db-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

