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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395702"
---
# <a name="pidtaginternetreferences-canonical-property"></a><span data-ttu-id="af890-103">Каноническое свойство PidTagInternetReferences</span><span class="sxs-lookup"><span data-stu-id="af890-103">PidTagInternetReferences Canonical Property</span></span>

  
  
<span data-ttu-id="af890-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="af890-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="af890-105">Содержит значение поля заголовка сообщения Multipurpose Internet Mail Extensions (MIME) ссылки.</span><span class="sxs-lookup"><span data-stu-id="af890-105">Contains the value of a Multipurpose Internet Mail Extensions (MIME) message's References header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="af890-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="af890-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="af890-107">PR_INTERNET_REFERENCES, PR_INTERNET_REFERENCES_A, PR_INTERNET_REFERENCES_W</span><span class="sxs-lookup"><span data-stu-id="af890-107">PR_INTERNET_REFERENCES, PR_INTERNET_REFERENCES_A, PR_INTERNET_REFERENCES_W</span></span>  <br/> |
|<span data-ttu-id="af890-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="af890-108">Identifier:</span></span>  <br/> |<span data-ttu-id="af890-109">0x1039</span><span class="sxs-lookup"><span data-stu-id="af890-109">0x1039</span></span>  <br/> |
|<span data-ttu-id="af890-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="af890-110">Data type:</span></span>  <br/> |<span data-ttu-id="af890-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="af890-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="af890-112">Область:</span><span class="sxs-lookup"><span data-stu-id="af890-112">Area:</span></span>  <br/> |<span data-ttu-id="af890-113">MIME</span><span class="sxs-lookup"><span data-stu-id="af890-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="af890-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="af890-114">Remarks</span></span>

<span data-ttu-id="af890-115">Для создания ссылки на поля заголовка, клиенты необходимо задать эти свойства нужное значение.</span><span class="sxs-lookup"><span data-stu-id="af890-115">To generate a References header field, clients must set these properties to the desired value.</span></span> <span data-ttu-id="af890-116">Записи MIME необходимо скопировать значения этих свойств поля заголовка ссылки.</span><span class="sxs-lookup"><span data-stu-id="af890-116">MIME writers must copy the value of these properties to the References header field.</span></span>
  
<span data-ttu-id="af890-117">Для установки значения этих свойств, клиенты MIME должен записи нужное значение в поле Заголовок справочные материалы.</span><span class="sxs-lookup"><span data-stu-id="af890-117">To set the value of these properties, MIME clients must write the desired value to a References header field.</span></span> <span data-ttu-id="af890-118">Читатели MIME, должен скопировать значение поля заголовка ссылки на эти свойства.</span><span class="sxs-lookup"><span data-stu-id="af890-118">MIME readers must copy the value of the References header field to these properties.</span></span> <span data-ttu-id="af890-119">Читатели MIME усекать значение эти свойства, если оно превышает 64 КБ в длину.</span><span class="sxs-lookup"><span data-stu-id="af890-119">MIME readers may truncate the value of these properties if it exceeds 64KB in length.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="af890-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="af890-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="af890-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="af890-121">Protocol specifications</span></span>

<span data-ttu-id="af890-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="af890-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="af890-123">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="af890-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="af890-124">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="af890-124">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="af890-125">Преобразование conventions стандартных электронной почты Интернета объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="af890-125">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="af890-126">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="af890-126">Header files</span></span>

<span data-ttu-id="af890-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="af890-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="af890-128">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="af890-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="af890-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="af890-129">Mapitags.h</span></span>
  
> <span data-ttu-id="af890-130">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="af890-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="af890-131">См. также</span><span class="sxs-lookup"><span data-stu-id="af890-131">See also</span></span>



[<span data-ttu-id="af890-132">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="af890-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="af890-133">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="af890-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="af890-134">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="af890-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="af890-135">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="af890-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

