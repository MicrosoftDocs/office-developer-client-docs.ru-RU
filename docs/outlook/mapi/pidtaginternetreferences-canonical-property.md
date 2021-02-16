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
# <a name="pidtaginternetreferences-canonical-property"></a><span data-ttu-id="c95b1-103">Каноническое свойство PidTagInternetReferences</span><span class="sxs-lookup"><span data-stu-id="c95b1-103">PidTagInternetReferences Canonical Property</span></span>

  
  
<span data-ttu-id="c95b1-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c95b1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c95b1-105">Содержит значение поля "Ссылки" сообщения MIME.</span><span class="sxs-lookup"><span data-stu-id="c95b1-105">Contains the value of a Multipurpose Internet Mail Extensions (MIME) message's References header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c95b1-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="c95b1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c95b1-107">PR_INTERNET_REFERENCES, PR_INTERNET_REFERENCES_A, PR_INTERNET_REFERENCES_W</span><span class="sxs-lookup"><span data-stu-id="c95b1-107">PR_INTERNET_REFERENCES, PR_INTERNET_REFERENCES_A, PR_INTERNET_REFERENCES_W</span></span>  <br/> |
|<span data-ttu-id="c95b1-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="c95b1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c95b1-109">0x1039</span><span class="sxs-lookup"><span data-stu-id="c95b1-109">0x1039</span></span>  <br/> |
|<span data-ttu-id="c95b1-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="c95b1-110">Data type:</span></span>  <br/> |<span data-ttu-id="c95b1-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c95b1-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="c95b1-112">Область:</span><span class="sxs-lookup"><span data-stu-id="c95b1-112">Area:</span></span>  <br/> |<span data-ttu-id="c95b1-113">MIME</span><span class="sxs-lookup"><span data-stu-id="c95b1-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c95b1-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="c95b1-114">Remarks</span></span>

<span data-ttu-id="c95b1-115">Чтобы создать поле "Ссылки", клиенты должны установить для этих свойств нужное значение.</span><span class="sxs-lookup"><span data-stu-id="c95b1-115">To generate a References header field, clients must set these properties to the desired value.</span></span> <span data-ttu-id="c95b1-116">Авторы MIME должны скопировать значение этих свойств в поле "Ссылки".</span><span class="sxs-lookup"><span data-stu-id="c95b1-116">MIME writers must copy the value of these properties to the References header field.</span></span>
  
<span data-ttu-id="c95b1-117">Чтобы установить значение этих свойств, клиенты MIME должны записать нужное значение в поле загона ссылок.</span><span class="sxs-lookup"><span data-stu-id="c95b1-117">To set the value of these properties, MIME clients must write the desired value to a References header field.</span></span> <span data-ttu-id="c95b1-118">Читатели MIME должны скопировать значение поля "Ссылки" в эти свойства.</span><span class="sxs-lookup"><span data-stu-id="c95b1-118">MIME readers must copy the value of the References header field to these properties.</span></span> <span data-ttu-id="c95b1-119">Считыватели MIME могут обсечены значения этих свойств, если их длина превышает 64 КБ.</span><span class="sxs-lookup"><span data-stu-id="c95b1-119">MIME readers may truncate the value of these properties if it exceeds 64KB in length.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c95b1-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c95b1-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c95b1-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="c95b1-121">Protocol specifications</span></span>

<span data-ttu-id="c95b1-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c95b1-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c95b1-123">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="c95b1-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c95b1-124">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c95b1-124">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c95b1-125">Преобразуется из стандартных интернет-соглашений электронной почты в объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="c95b1-125">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c95b1-126">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="c95b1-126">Header files</span></span>

<span data-ttu-id="c95b1-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c95b1-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="c95b1-128">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="c95b1-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="c95b1-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c95b1-129">Mapitags.h</span></span>
  
> <span data-ttu-id="c95b1-130">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="c95b1-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c95b1-131">См. также</span><span class="sxs-lookup"><span data-stu-id="c95b1-131">See also</span></span>



[<span data-ttu-id="c95b1-132">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c95b1-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c95b1-133">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c95b1-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c95b1-134">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="c95b1-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c95b1-135">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="c95b1-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

