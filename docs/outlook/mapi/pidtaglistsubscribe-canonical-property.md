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
ms.openlocfilehash: 5030e48ac87408f983696a365d3234c3362346c0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811327"
---
# <a name="pidtaglistsubscribe-canonical-property"></a><span data-ttu-id="fb727-103">Каноническое свойство PidTagListSubscribe</span><span class="sxs-lookup"><span data-stu-id="fb727-103">PidTagListSubscribe Canonical Property</span></span>

  
  
<span data-ttu-id="fb727-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fb727-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fb727-105">Содержит значение в поле Заголовок списка подписка сообщение Multipurpose Internet Mail Extensions (MIME).</span><span class="sxs-lookup"><span data-stu-id="fb727-105">Contains the value of a Multipurpose Internet Mail Extensions (MIME) message's List-Subscribe header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fb727-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="fb727-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fb727-107">PR_LIST_SUBSCRIBE, PR_LIST_SUBSCRIBE_A, PR_LIST_SUBSCRIBE_W</span><span class="sxs-lookup"><span data-stu-id="fb727-107">PR_LIST_SUBSCRIBE, PR_LIST_SUBSCRIBE_A, PR_LIST_SUBSCRIBE_W</span></span>  <br/> |
|<span data-ttu-id="fb727-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="fb727-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fb727-109">0x1044</span><span class="sxs-lookup"><span data-stu-id="fb727-109">0x1044</span></span>  <br/> |
|<span data-ttu-id="fb727-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="fb727-110">Data type:</span></span>  <br/> |<span data-ttu-id="fb727-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="fb727-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="fb727-112">Область:</span><span class="sxs-lookup"><span data-stu-id="fb727-112">Area:</span></span>  <br/> |<span data-ttu-id="fb727-113">Разное</span><span class="sxs-lookup"><span data-stu-id="fb727-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fb727-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="fb727-114">Remarks</span></span>

<span data-ttu-id="fb727-115">Для создания поля заголовка подписка списка клиентов необходимо установить значение этих свойств нужное значение.</span><span class="sxs-lookup"><span data-stu-id="fb727-115">To generate a List-Subscribe header field, clients must set the value of these properties to the desired value.</span></span> <span data-ttu-id="fb727-116">Записи MIME необходимо скопировать значения этих свойств поля заголовка подписка списка.</span><span class="sxs-lookup"><span data-stu-id="fb727-116">MIME writers must copy the value of these properties to the List-Subscribe header field.</span></span>
  
<span data-ttu-id="fb727-117">Чтобы задать значение свойства, связанные с сервера эти клиенты MIME необходимо создать поля заголовка, как указано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="fb727-117">To set the value of server-related properties like these, MIME clients must write the header fields as specified in the following table.</span></span>
  
|<span data-ttu-id="fb727-118">**Свойство**</span><span class="sxs-lookup"><span data-stu-id="fb727-118">**Property**</span></span>|<span data-ttu-id="fb727-119">**Имя поля Предпочитаемый заголовка**</span><span class="sxs-lookup"><span data-stu-id="fb727-119">**Preferred header field name**</span></span>|<span data-ttu-id="fb727-120">**Альтернативные заголовок поля имя**</span><span class="sxs-lookup"><span data-stu-id="fb727-120">**Alternate header field name**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fb727-121">**PidTagListSubscribe**</span><span class="sxs-lookup"><span data-stu-id="fb727-121">**PidTagListSubscribe**</span></span> <br/> |<span data-ttu-id="fb727-122">Подписка списка</span><span class="sxs-lookup"><span data-stu-id="fb727-122">List-Subscribe</span></span>  <br/> |<span data-ttu-id="fb727-123">X список подписки</span><span class="sxs-lookup"><span data-stu-id="fb727-123">X-List-Subscribe</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="fb727-124">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="fb727-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fb727-125">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="fb727-125">Protocol specifications</span></span>

<span data-ttu-id="fb727-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fb727-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fb727-127">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="fb727-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fb727-128">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fb727-128">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fb727-129">Преобразование conventions стандартных электронной почты Интернета объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="fb727-129">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fb727-130">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="fb727-130">Header files</span></span>

<span data-ttu-id="fb727-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fb727-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="fb727-132">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="fb727-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="fb727-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="fb727-133">Mapitags.h</span></span>
  
> <span data-ttu-id="fb727-134">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="fb727-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fb727-135">См. также</span><span class="sxs-lookup"><span data-stu-id="fb727-135">See also</span></span>



[<span data-ttu-id="fb727-136">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="fb727-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fb727-137">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="fb727-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fb727-138">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="fb727-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fb727-139">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="fb727-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

