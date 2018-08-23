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
ms.openlocfilehash: 4408bbc9461d11859292c1d4c356c2323598eb7b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584228"
---
# <a name="pidtaglistsubscribe-canonical-property"></a><span data-ttu-id="aed8c-103">Каноническое свойство PidTagListSubscribe</span><span class="sxs-lookup"><span data-stu-id="aed8c-103">PidTagListSubscribe Canonical Property</span></span>

  
  
<span data-ttu-id="aed8c-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aed8c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aed8c-105">Содержит значение в поле Заголовок списка подписка сообщение Multipurpose Internet Mail Extensions (MIME).</span><span class="sxs-lookup"><span data-stu-id="aed8c-105">Contains the value of a Multipurpose Internet Mail Extensions (MIME) message's List-Subscribe header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="aed8c-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="aed8c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="aed8c-107">PR_LIST_SUBSCRIBE, PR_LIST_SUBSCRIBE_A, PR_LIST_SUBSCRIBE_W</span><span class="sxs-lookup"><span data-stu-id="aed8c-107">PR_LIST_SUBSCRIBE, PR_LIST_SUBSCRIBE_A, PR_LIST_SUBSCRIBE_W</span></span>  <br/> |
|<span data-ttu-id="aed8c-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="aed8c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="aed8c-109">0x1044</span><span class="sxs-lookup"><span data-stu-id="aed8c-109">0x1044</span></span>  <br/> |
|<span data-ttu-id="aed8c-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="aed8c-110">Data type:</span></span>  <br/> |<span data-ttu-id="aed8c-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="aed8c-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="aed8c-112">Область:</span><span class="sxs-lookup"><span data-stu-id="aed8c-112">Area:</span></span>  <br/> |<span data-ttu-id="aed8c-113">Разное</span><span class="sxs-lookup"><span data-stu-id="aed8c-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="aed8c-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="aed8c-114">Remarks</span></span>

<span data-ttu-id="aed8c-115">Для создания поля заголовка подписка списка клиентов необходимо установить значение этих свойств нужное значение.</span><span class="sxs-lookup"><span data-stu-id="aed8c-115">To generate a List-Subscribe header field, clients must set the value of these properties to the desired value.</span></span> <span data-ttu-id="aed8c-116">Записи MIME необходимо скопировать значения этих свойств поля заголовка подписка списка.</span><span class="sxs-lookup"><span data-stu-id="aed8c-116">MIME writers must copy the value of these properties to the List-Subscribe header field.</span></span>
  
<span data-ttu-id="aed8c-117">Чтобы задать значение свойства, связанные с сервера эти клиенты MIME необходимо создать поля заголовка, как указано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="aed8c-117">To set the value of server-related properties like these, MIME clients must write the header fields as specified in the following table.</span></span>
  
|<span data-ttu-id="aed8c-118">**Свойство**</span><span class="sxs-lookup"><span data-stu-id="aed8c-118">**Property**</span></span>|<span data-ttu-id="aed8c-119">**Имя поля Предпочитаемый заголовка**</span><span class="sxs-lookup"><span data-stu-id="aed8c-119">**Preferred header field name**</span></span>|<span data-ttu-id="aed8c-120">**Альтернативные заголовок поля имя**</span><span class="sxs-lookup"><span data-stu-id="aed8c-120">**Alternate header field name**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="aed8c-121">**PidTagListSubscribe**</span><span class="sxs-lookup"><span data-stu-id="aed8c-121">**PidTagListSubscribe**</span></span> <br/> |<span data-ttu-id="aed8c-122">Подписка списка</span><span class="sxs-lookup"><span data-stu-id="aed8c-122">List-Subscribe</span></span>  <br/> |<span data-ttu-id="aed8c-123">X список подписки</span><span class="sxs-lookup"><span data-stu-id="aed8c-123">X-List-Subscribe</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="aed8c-124">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="aed8c-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="aed8c-125">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="aed8c-125">Protocol specifications</span></span>

<span data-ttu-id="aed8c-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aed8c-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="aed8c-127">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="aed8c-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="aed8c-128">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aed8c-128">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="aed8c-129">Преобразование conventions стандартных электронной почты Интернета объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="aed8c-129">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="aed8c-130">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="aed8c-130">Header files</span></span>

<span data-ttu-id="aed8c-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="aed8c-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="aed8c-132">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="aed8c-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="aed8c-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="aed8c-133">Mapitags.h</span></span>
  
> <span data-ttu-id="aed8c-134">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="aed8c-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="aed8c-135">См. также</span><span class="sxs-lookup"><span data-stu-id="aed8c-135">See also</span></span>



[<span data-ttu-id="aed8c-136">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="aed8c-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="aed8c-137">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="aed8c-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="aed8c-138">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="aed8c-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="aed8c-139">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="aed8c-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

