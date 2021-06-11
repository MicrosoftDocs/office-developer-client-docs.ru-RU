---
title: Каноническое свойство PidTagListHelp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagListHelp
api_type:
- HeaderDef
ms.assetid: 403324b8-c992-4823-aa0f-0414b283debc
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 588747205ee3922fef7b107dc024f074a6ee527e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279631"
---
# <a name="pidtaglisthelp-canonical-property"></a><span data-ttu-id="0dfc0-103">Каноническое свойство PidTagListHelp</span><span class="sxs-lookup"><span data-stu-id="0dfc0-103">PidTagListHelp Canonical Property</span></span>

  
  
<span data-ttu-id="0dfc0-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0dfc0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0dfc0-105">Содержит значение поля многоцелевых расширений интернет-почты (MIME) List-Help.</span><span class="sxs-lookup"><span data-stu-id="0dfc0-105">Contains the value of a Multipurpose Internet Mail Extensions (MIME) message's List-Help header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0dfc0-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="0dfc0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0dfc0-107">PR_LIST_HELP, PR_LIST_HELP_A, PR_LIST_HELP_W</span><span class="sxs-lookup"><span data-stu-id="0dfc0-107">PR_LIST_HELP, PR_LIST_HELP_A, PR_LIST_HELP_W</span></span>  <br/> |
|<span data-ttu-id="0dfc0-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="0dfc0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0dfc0-109">0x1043</span><span class="sxs-lookup"><span data-stu-id="0dfc0-109">0x1043</span></span>  <br/> |
|<span data-ttu-id="0dfc0-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="0dfc0-110">Data type:</span></span>  <br/> |<span data-ttu-id="0dfc0-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0dfc0-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="0dfc0-112">Область:</span><span class="sxs-lookup"><span data-stu-id="0dfc0-112">Area:</span></span>  <br/> |<span data-ttu-id="0dfc0-113">Разное</span><span class="sxs-lookup"><span data-stu-id="0dfc0-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0dfc0-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="0dfc0-114">Remarks</span></span>

<span data-ttu-id="0dfc0-115">Чтобы создать поле List-Help, клиенты должны установить  значение PR_LIST_HELP или связанного свойства с нужным значением.</span><span class="sxs-lookup"><span data-stu-id="0dfc0-115">To generate a List-Help header field, clients must set the value of **PR_LIST_HELP** or an associated property to the desired value.</span></span> <span data-ttu-id="0dfc0-116">Авторы MIME должны скопировать это значение в поле List-Help загона.</span><span class="sxs-lookup"><span data-stu-id="0dfc0-116">MIME writers must copy this value to the List-Help header field.</span></span> 
  
<span data-ttu-id="0dfc0-117">Чтобы установить значение этих свойств сервера списка, клиенты MIME должны написать поля загона, указанные в следующей таблице:</span><span class="sxs-lookup"><span data-stu-id="0dfc0-117">To set the value of these list server-related properties, MIME clients must write the header fields as specified in the following table:</span></span>
  
|<span data-ttu-id="0dfc0-118">**Property**</span><span class="sxs-lookup"><span data-stu-id="0dfc0-118">**Property**</span></span>|<span data-ttu-id="0dfc0-119">**Предпочтительное имя поля загона**</span><span class="sxs-lookup"><span data-stu-id="0dfc0-119">**Preferred header field name**</span></span>|<span data-ttu-id="0dfc0-120">**Альтернативное имя поля загона**</span><span class="sxs-lookup"><span data-stu-id="0dfc0-120">**Alternate header field name**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0dfc0-121">**PR_LIST_HELP**</span><span class="sxs-lookup"><span data-stu-id="0dfc0-121">**PR_LIST_HELP**</span></span> <br/> |<span data-ttu-id="0dfc0-122">List-Help</span><span class="sxs-lookup"><span data-stu-id="0dfc0-122">List-Help</span></span>  <br/> |<span data-ttu-id="0dfc0-123">X-List-Help</span><span class="sxs-lookup"><span data-stu-id="0dfc0-123">X-List-Help</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="0dfc0-124">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="0dfc0-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0dfc0-125">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="0dfc0-125">Protocol specifications</span></span>

<span data-ttu-id="0dfc0-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0dfc0-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0dfc0-127">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="0dfc0-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0dfc0-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0dfc0-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0dfc0-129">Преобразуется из стандартных конвенций электронной почты в объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="0dfc0-129">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0dfc0-130">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="0dfc0-130">Header files</span></span>

<span data-ttu-id="0dfc0-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0dfc0-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="0dfc0-132">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="0dfc0-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="0dfc0-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0dfc0-133">Mapitags.h</span></span>
  
> <span data-ttu-id="0dfc0-134">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="0dfc0-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0dfc0-135">См. также</span><span class="sxs-lookup"><span data-stu-id="0dfc0-135">See also</span></span>



[<span data-ttu-id="0dfc0-136">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0dfc0-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0dfc0-137">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0dfc0-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0dfc0-138">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="0dfc0-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0dfc0-139">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="0dfc0-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

