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
ms.openlocfilehash: f66a570273d78f63ced110a4bdc8a12a49c531b6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595246"
---
# <a name="pidnameacceptlanguage-canonical-property"></a><span data-ttu-id="cfb92-103">Каноническое свойство PidNameAcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="cfb92-103">PidNameAcceptLanguage Canonical Property</span></span>

  
  
<span data-ttu-id="cfb92-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cfb92-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cfb92-105">Содержит значение поля заголовка [RFC3282] Accept-Language.</span><span class="sxs-lookup"><span data-stu-id="cfb92-105">Contains an [RFC3282] Accept-Language header field value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cfb92-106">Понятные имена:</span><span class="sxs-lookup"><span data-stu-id="cfb92-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="cfb92-107">AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="cfb92-107">AcceptLanguage</span></span>  <br/> |
|<span data-ttu-id="cfb92-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="cfb92-108">Property set:</span></span>  <br/> |<span data-ttu-id="cfb92-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="cfb92-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="cfb92-110">Имя свойства:</span><span class="sxs-lookup"><span data-stu-id="cfb92-110">Property name:</span></span>  <br/> |<span data-ttu-id="cfb92-111">Примите языка</span><span class="sxs-lookup"><span data-stu-id="cfb92-111">Accept-Language</span></span>  <br/> |
|<span data-ttu-id="cfb92-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="cfb92-112">Data type:</span></span>  <br/> |<span data-ttu-id="cfb92-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="cfb92-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="cfb92-114">Область:</span><span class="sxs-lookup"><span data-stu-id="cfb92-114">Area:</span></span>  <br/> |<span data-ttu-id="cfb92-115">Электронная почта</span><span class="sxs-lookup"><span data-stu-id="cfb92-115">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cfb92-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="cfb92-116">Remarks</span></span>

<span data-ttu-id="cfb92-117">Чтобы задать значение этого свойства, клиенты сообщение расширения MIME (Multipurpose Internet) указывайте полем заголовок Accept-Language с нужное значение.</span><span class="sxs-lookup"><span data-stu-id="cfb92-117">To set the value of this property, Multipurpose Internet Message Extensions (MIME) clients should write an Accept-Language header field with the desired value.</span></span> <span data-ttu-id="cfb92-118">Клиенты MIME может вместо этого использовать поле заголовка принять языка X.</span><span class="sxs-lookup"><span data-stu-id="cfb92-118">MIME clients may write an X-Accept-Language header field instead.</span></span> <span data-ttu-id="cfb92-119">Читатели MIME следует скопировать значение любого из поля заголовка значение этого свойства.</span><span class="sxs-lookup"><span data-stu-id="cfb92-119">MIME readers should copy the value of either header field to the value of this property.</span></span> <span data-ttu-id="cfb92-120">Если оба поля заголовков, читатели MIME следует использовать поле Заголовок Accept-Language.</span><span class="sxs-lookup"><span data-stu-id="cfb92-120">If both header fields are present, MIME readers should use the Accept-Language header field.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="cfb92-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="cfb92-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cfb92-122">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="cfb92-122">Protocol specifications</span></span>

<span data-ttu-id="cfb92-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cfb92-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cfb92-124">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="cfb92-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="cfb92-125">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cfb92-125">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cfb92-126">Преобразование conventions стандартных электронной почты Интернета объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="cfb92-126">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cfb92-127">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="cfb92-127">Header files</span></span>

<span data-ttu-id="cfb92-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cfb92-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="cfb92-129">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="cfb92-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cfb92-130">См. также</span><span class="sxs-lookup"><span data-stu-id="cfb92-130">See also</span></span>



[<span data-ttu-id="cfb92-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="cfb92-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cfb92-132">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="cfb92-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cfb92-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="cfb92-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cfb92-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="cfb92-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

