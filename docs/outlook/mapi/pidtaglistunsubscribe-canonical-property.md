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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390600"
---
# <a name="pidtaglistunsubscribe-canonical-property"></a><span data-ttu-id="92898-103">Каноническое свойство PidTagListUnsubscribe</span><span class="sxs-lookup"><span data-stu-id="92898-103">PidTagListUnsubscribe Canonical Property</span></span>

  
  
<span data-ttu-id="92898-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="92898-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="92898-105">Содержит значение в поле Заголовок списка отписаться сообщение Multipurpose Internet Mail Extensions (MIME).</span><span class="sxs-lookup"><span data-stu-id="92898-105">Contains the value of a Multipurpose Internet Mail Extensions (MIME) message's List-Unsubscribe header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="92898-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="92898-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="92898-107">PR_LIST_UNSUBSCRIBE, PR_LIST_UNSUBSCRIBE_A, PR_LIST_UNSUBSCRIBE_W</span><span class="sxs-lookup"><span data-stu-id="92898-107">PR_LIST_UNSUBSCRIBE, PR_LIST_UNSUBSCRIBE_A, PR_LIST_UNSUBSCRIBE_W</span></span>  <br/> |
|<span data-ttu-id="92898-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="92898-108">Identifier:</span></span>  <br/> |<span data-ttu-id="92898-109">0x1045</span><span class="sxs-lookup"><span data-stu-id="92898-109">0x1045</span></span>  <br/> |
|<span data-ttu-id="92898-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="92898-110">Data type:</span></span>  <br/> |<span data-ttu-id="92898-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="92898-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="92898-112">Область:</span><span class="sxs-lookup"><span data-stu-id="92898-112">Area:</span></span>  <br/> |<span data-ttu-id="92898-113">Разное</span><span class="sxs-lookup"><span data-stu-id="92898-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="92898-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="92898-114">Remarks</span></span>

<span data-ttu-id="92898-115">Для создания списка отписаться поле заголовка, клиенты необходимо задать эти свойства нужное значение.</span><span class="sxs-lookup"><span data-stu-id="92898-115">To generate a List-Unsubscribe header field, clients must set these properties to the desired value.</span></span> <span data-ttu-id="92898-116">Записи MIME необходимо скопировать значения этих свойств поля заголовка отписаться списка.</span><span class="sxs-lookup"><span data-stu-id="92898-116">MIME writers must copy the value of these properties to the List-Unsubscribe header field.</span></span>
  
<span data-ttu-id="92898-117">Чтобы задать значение эти свойства списка, связанные с сервера, клиенты MIME необходимо создать поля заголовка, как указано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="92898-117">To set the value of these list server-related properties, MIME clients must write the header fields as specified in the following table.</span></span>
  
|<span data-ttu-id="92898-118">**Свойство**</span><span class="sxs-lookup"><span data-stu-id="92898-118">**Property**</span></span>|<span data-ttu-id="92898-119">**Имя поля Предпочитаемый заголовка**</span><span class="sxs-lookup"><span data-stu-id="92898-119">**Preferred header field name**</span></span>|<span data-ttu-id="92898-120">**Альтернативные заголовок поля имя**</span><span class="sxs-lookup"><span data-stu-id="92898-120">**Alternate header field name**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="92898-121">**PR_LIST_UNSUBSCRIBE**</span><span class="sxs-lookup"><span data-stu-id="92898-121">**PR_LIST_UNSUBSCRIBE**</span></span> <br/> |<span data-ttu-id="92898-122">Список отписаться</span><span class="sxs-lookup"><span data-stu-id="92898-122">List-Unsubscribe</span></span>  <br/> |<span data-ttu-id="92898-123">X список отписаться</span><span class="sxs-lookup"><span data-stu-id="92898-123">X-List-Unsubscribe</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="92898-124">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="92898-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="92898-125">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="92898-125">Protocol specifications</span></span>

<span data-ttu-id="92898-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="92898-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="92898-127">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="92898-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="92898-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="92898-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="92898-129">Преобразование conventions стандартных электронной почты Интернета объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="92898-129">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="92898-130">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="92898-130">Header files</span></span>

<span data-ttu-id="92898-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="92898-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="92898-132">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="92898-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="92898-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="92898-133">Mapitags.h</span></span>
  
> <span data-ttu-id="92898-134">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="92898-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="92898-135">См. также</span><span class="sxs-lookup"><span data-stu-id="92898-135">See also</span></span>



[<span data-ttu-id="92898-136">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="92898-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="92898-137">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="92898-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="92898-138">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="92898-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="92898-139">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="92898-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

