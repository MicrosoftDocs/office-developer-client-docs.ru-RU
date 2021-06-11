---
title: Каноническое свойство PidTagListSubscribe
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagListSubscribe
api_type:
- HeaderDef
ms.assetid: 97387a82-8e40-4c76-818c-2229fac12e01
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: bee11c495d7f1ef21f9af70e6aa89f8c0d0f78b4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279659"
---
# <a name="pidtaglistsubscribe-canonical-property"></a><span data-ttu-id="c9d93-103">Каноническое свойство PidTagListSubscribe</span><span class="sxs-lookup"><span data-stu-id="c9d93-103">PidTagListSubscribe Canonical Property</span></span>

  
  
<span data-ttu-id="c9d93-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c9d93-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c9d93-105">Содержит значение поля многоцелевых расширений интернет-почты (MIME) List-Subscribe.</span><span class="sxs-lookup"><span data-stu-id="c9d93-105">Contains the value of a Multipurpose Internet Mail Extensions (MIME) message's List-Subscribe header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c9d93-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="c9d93-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c9d93-107">PR_LIST_SUBSCRIBE, PR_LIST_SUBSCRIBE_A, PR_LIST_SUBSCRIBE_W</span><span class="sxs-lookup"><span data-stu-id="c9d93-107">PR_LIST_SUBSCRIBE, PR_LIST_SUBSCRIBE_A, PR_LIST_SUBSCRIBE_W</span></span>  <br/> |
|<span data-ttu-id="c9d93-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="c9d93-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c9d93-109">0x1044</span><span class="sxs-lookup"><span data-stu-id="c9d93-109">0x1044</span></span>  <br/> |
|<span data-ttu-id="c9d93-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="c9d93-110">Data type:</span></span>  <br/> |<span data-ttu-id="c9d93-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c9d93-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="c9d93-112">Область:</span><span class="sxs-lookup"><span data-stu-id="c9d93-112">Area:</span></span>  <br/> |<span data-ttu-id="c9d93-113">Разное</span><span class="sxs-lookup"><span data-stu-id="c9d93-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c9d93-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="c9d93-114">Remarks</span></span>

<span data-ttu-id="c9d93-115">Чтобы создать поле List-Subscribe, клиенты должны задать значение этих свойств нужному значению.</span><span class="sxs-lookup"><span data-stu-id="c9d93-115">To generate a List-Subscribe header field, clients must set the value of these properties to the desired value.</span></span> <span data-ttu-id="c9d93-116">Авторы MIME должны скопировать значение этих свойств в поле List-Subscribe.</span><span class="sxs-lookup"><span data-stu-id="c9d93-116">MIME writers must copy the value of these properties to the List-Subscribe header field.</span></span>
  
<span data-ttu-id="c9d93-117">Чтобы установить значение таких свойств, связанных с сервером, клиенты MIME должны написать поля загона, указанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="c9d93-117">To set the value of server-related properties like these, MIME clients must write the header fields as specified in the following table.</span></span>
  
|<span data-ttu-id="c9d93-118">**Property**</span><span class="sxs-lookup"><span data-stu-id="c9d93-118">**Property**</span></span>|<span data-ttu-id="c9d93-119">**Предпочтительное имя поля загона**</span><span class="sxs-lookup"><span data-stu-id="c9d93-119">**Preferred header field name**</span></span>|<span data-ttu-id="c9d93-120">**Альтернативное имя поля загона**</span><span class="sxs-lookup"><span data-stu-id="c9d93-120">**Alternate header field name**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c9d93-121">**PidTagListSubscribe**</span><span class="sxs-lookup"><span data-stu-id="c9d93-121">**PidTagListSubscribe**</span></span> <br/> |<span data-ttu-id="c9d93-122">List-Subscribe</span><span class="sxs-lookup"><span data-stu-id="c9d93-122">List-Subscribe</span></span>  <br/> |<span data-ttu-id="c9d93-123">X-List-Subscribe</span><span class="sxs-lookup"><span data-stu-id="c9d93-123">X-List-Subscribe</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="c9d93-124">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c9d93-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c9d93-125">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="c9d93-125">Protocol specifications</span></span>

<span data-ttu-id="c9d93-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c9d93-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c9d93-127">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="c9d93-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c9d93-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c9d93-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c9d93-129">Преобразуется из стандартных конвенций электронной почты в объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="c9d93-129">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c9d93-130">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="c9d93-130">Header files</span></span>

<span data-ttu-id="c9d93-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c9d93-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="c9d93-132">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="c9d93-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="c9d93-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c9d93-133">Mapitags.h</span></span>
  
> <span data-ttu-id="c9d93-134">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="c9d93-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c9d93-135">См. также</span><span class="sxs-lookup"><span data-stu-id="c9d93-135">See also</span></span>



[<span data-ttu-id="c9d93-136">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c9d93-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c9d93-137">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c9d93-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c9d93-138">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="c9d93-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c9d93-139">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="c9d93-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

