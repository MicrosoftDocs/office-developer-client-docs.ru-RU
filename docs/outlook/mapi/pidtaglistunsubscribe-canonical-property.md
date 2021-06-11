---
title: Каноническое свойство PidTagListUnsubscribe
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagListUnsubscribe
api_type:
- HeaderDef
ms.assetid: 4e6bfbc7-7586-43cc-9380-daa0fe3d85a5
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e057ab2ca0c75d5c0d749ebde8f1bdfb4f1ae66a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278881"
---
# <a name="pidtaglistunsubscribe-canonical-property"></a><span data-ttu-id="97dbf-103">Каноническое свойство PidTagListUnsubscribe</span><span class="sxs-lookup"><span data-stu-id="97dbf-103">PidTagListUnsubscribe Canonical Property</span></span>

  
  
<span data-ttu-id="97dbf-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="97dbf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="97dbf-105">Содержит значение поля многоцелевых расширений интернет-почты (MIME) List-Unsubscribe.</span><span class="sxs-lookup"><span data-stu-id="97dbf-105">Contains the value of a Multipurpose Internet Mail Extensions (MIME) message's List-Unsubscribe header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="97dbf-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="97dbf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="97dbf-107">PR_LIST_UNSUBSCRIBE, PR_LIST_UNSUBSCRIBE_A, PR_LIST_UNSUBSCRIBE_W</span><span class="sxs-lookup"><span data-stu-id="97dbf-107">PR_LIST_UNSUBSCRIBE, PR_LIST_UNSUBSCRIBE_A, PR_LIST_UNSUBSCRIBE_W</span></span>  <br/> |
|<span data-ttu-id="97dbf-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="97dbf-108">Identifier:</span></span>  <br/> |<span data-ttu-id="97dbf-109">0x1045</span><span class="sxs-lookup"><span data-stu-id="97dbf-109">0x1045</span></span>  <br/> |
|<span data-ttu-id="97dbf-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="97dbf-110">Data type:</span></span>  <br/> |<span data-ttu-id="97dbf-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="97dbf-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="97dbf-112">Область:</span><span class="sxs-lookup"><span data-stu-id="97dbf-112">Area:</span></span>  <br/> |<span data-ttu-id="97dbf-113">Разное</span><span class="sxs-lookup"><span data-stu-id="97dbf-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="97dbf-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="97dbf-114">Remarks</span></span>

<span data-ttu-id="97dbf-115">Чтобы создать поле List-Unsubscribe, клиенты должны установить эти свойства до нужного значения.</span><span class="sxs-lookup"><span data-stu-id="97dbf-115">To generate a List-Unsubscribe header field, clients must set these properties to the desired value.</span></span> <span data-ttu-id="97dbf-116">Авторы MIME должны скопировать значение этих свойств в поле List-Unsubscribe.</span><span class="sxs-lookup"><span data-stu-id="97dbf-116">MIME writers must copy the value of these properties to the List-Unsubscribe header field.</span></span>
  
<span data-ttu-id="97dbf-117">Чтобы установить значение этих свойств сервера списка, клиенты MIME должны написать поля загона, указанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="97dbf-117">To set the value of these list server-related properties, MIME clients must write the header fields as specified in the following table.</span></span>
  
|<span data-ttu-id="97dbf-118">**Property**</span><span class="sxs-lookup"><span data-stu-id="97dbf-118">**Property**</span></span>|<span data-ttu-id="97dbf-119">**Предпочтительное имя поля загона**</span><span class="sxs-lookup"><span data-stu-id="97dbf-119">**Preferred header field name**</span></span>|<span data-ttu-id="97dbf-120">**Альтернативное имя поля загона**</span><span class="sxs-lookup"><span data-stu-id="97dbf-120">**Alternate header field name**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="97dbf-121">**PR_LIST_UNSUBSCRIBE**</span><span class="sxs-lookup"><span data-stu-id="97dbf-121">**PR_LIST_UNSUBSCRIBE**</span></span> <br/> |<span data-ttu-id="97dbf-122">List-Unsubscribe</span><span class="sxs-lookup"><span data-stu-id="97dbf-122">List-Unsubscribe</span></span>  <br/> |<span data-ttu-id="97dbf-123">X-List-Unsubscribe</span><span class="sxs-lookup"><span data-stu-id="97dbf-123">X-List-Unsubscribe</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="97dbf-124">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="97dbf-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="97dbf-125">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="97dbf-125">Protocol specifications</span></span>

<span data-ttu-id="97dbf-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="97dbf-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="97dbf-127">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="97dbf-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="97dbf-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="97dbf-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="97dbf-129">Преобразуется из стандартных конвенций электронной почты в объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="97dbf-129">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="97dbf-130">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="97dbf-130">Header files</span></span>

<span data-ttu-id="97dbf-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="97dbf-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="97dbf-132">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="97dbf-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="97dbf-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="97dbf-133">Mapitags.h</span></span>
  
> <span data-ttu-id="97dbf-134">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="97dbf-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="97dbf-135">См. также</span><span class="sxs-lookup"><span data-stu-id="97dbf-135">See also</span></span>



[<span data-ttu-id="97dbf-136">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="97dbf-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="97dbf-137">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="97dbf-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="97dbf-138">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="97dbf-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="97dbf-139">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="97dbf-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

