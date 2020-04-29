---
title: Каноническое свойство PidNameAcceptLanguage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameAcceptLanguage
api_type:
- COM
ms.assetid: 4b202bc1-f718-446a-950f-634ffee47baf
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 855610c43cfaa64fa69e6987743b137b188d84a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360944"
---
# <a name="pidnameacceptlanguage-canonical-property"></a><span data-ttu-id="0a30a-103">Каноническое свойство PidNameAcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="0a30a-103">PidNameAcceptLanguage Canonical Property</span></span>

  
  
<span data-ttu-id="0a30a-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0a30a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0a30a-105">Содержит значение поля заголовка [RFC3282] Accept. Language.</span><span class="sxs-lookup"><span data-stu-id="0a30a-105">Contains an [RFC3282] Accept-Language header field value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0a30a-106">Понятные имена:</span><span class="sxs-lookup"><span data-stu-id="0a30a-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="0a30a-107">акцептлангуаже</span><span class="sxs-lookup"><span data-stu-id="0a30a-107">AcceptLanguage</span></span>  <br/> |
|<span data-ttu-id="0a30a-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="0a30a-108">Property set:</span></span>  <br/> |<span data-ttu-id="0a30a-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="0a30a-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="0a30a-110">Имя свойства:</span><span class="sxs-lookup"><span data-stu-id="0a30a-110">Property name:</span></span>  <br/> |<span data-ttu-id="0a30a-111">Принять-Язык</span><span class="sxs-lookup"><span data-stu-id="0a30a-111">Accept-Language</span></span>  <br/> |
|<span data-ttu-id="0a30a-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="0a30a-112">Data type:</span></span>  <br/> |<span data-ttu-id="0a30a-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0a30a-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="0a30a-114">Область:</span><span class="sxs-lookup"><span data-stu-id="0a30a-114">Area:</span></span>  <br/> |<span data-ttu-id="0a30a-115">Электронная почта</span><span class="sxs-lookup"><span data-stu-id="0a30a-115">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0a30a-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="0a30a-116">Remarks</span></span>

<span data-ttu-id="0a30a-117">Чтобы задать значение этого свойства, клиенты с многоцелевыми расширениями Интернет-сообщений (MIME) должны записать поле заголовка Accept-Language с желаемым значением.</span><span class="sxs-lookup"><span data-stu-id="0a30a-117">To set the value of this property, Multipurpose Internet Message Extensions (MIME) clients should write an Accept-Language header field with the desired value.</span></span> <span data-ttu-id="0a30a-118">Клиенты MIME могут создавать вместо этого поле заголовка X — Accepting.</span><span class="sxs-lookup"><span data-stu-id="0a30a-118">MIME clients may write an X-Accept-Language header field instead.</span></span> <span data-ttu-id="0a30a-119">Считыватели MIME должны скопировать значение любого поля заголовка в значение этого свойства.</span><span class="sxs-lookup"><span data-stu-id="0a30a-119">MIME readers should copy the value of either header field to the value of this property.</span></span> <span data-ttu-id="0a30a-120">Если оба поля заголовков присутствуют, то для средств чтения MIME необходимо использовать поле заголовка Accept – Language.</span><span class="sxs-lookup"><span data-stu-id="0a30a-120">If both header fields are present, MIME readers should use the Accept-Language header field.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0a30a-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="0a30a-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0a30a-122">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="0a30a-122">Protocol specifications</span></span>

<span data-ttu-id="0a30a-123">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0a30a-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0a30a-124">Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="0a30a-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0a30a-125">[[MS — ОКСКМАИЛ]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0a30a-125">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0a30a-126">Преобразует стандартные правила электронной почты из Интернета в объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="0a30a-126">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0a30a-127">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="0a30a-127">Header files</span></span>

<span data-ttu-id="0a30a-128">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="0a30a-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="0a30a-129">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="0a30a-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0a30a-130">См. также</span><span class="sxs-lookup"><span data-stu-id="0a30a-130">See also</span></span>



[<span data-ttu-id="0a30a-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0a30a-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0a30a-132">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="0a30a-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0a30a-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="0a30a-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0a30a-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="0a30a-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

