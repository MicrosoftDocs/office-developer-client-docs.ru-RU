---
title: Каноническое свойство PidTagTextAttachmentCharset
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagTextAttachmentCharset
api_type:
- COM
ms.assetid: d347c949-d0c3-4a36-8447-3fa01111cdc1
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 1db41bc5c7ea71d65d892da520d4258354eb53cf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358816"
---
# <a name="pidtagtextattachmentcharset-canonical-property"></a><span data-ttu-id="11896-103">Каноническое свойство PidTagTextAttachmentCharset</span><span class="sxs-lookup"><span data-stu-id="11896-103">PidTagTextAttachmentCharset Canonical Property</span></span>

  
  
<span data-ttu-id="11896-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="11896-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="11896-105">Содержит значение набора символов вложения сообщений.</span><span class="sxs-lookup"><span data-stu-id="11896-105">Contains a message attachment's character set value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="11896-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="11896-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="11896-107">Нет</span><span class="sxs-lookup"><span data-stu-id="11896-107">None</span></span>  <br/> |
|<span data-ttu-id="11896-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="11896-108">Identifier:</span></span>  <br/> |<span data-ttu-id="11896-109">0x371B</span><span class="sxs-lookup"><span data-stu-id="11896-109">0x371B</span></span>  <br/> |
|<span data-ttu-id="11896-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="11896-110">Data type:</span></span>  <br/> |<span data-ttu-id="11896-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="11896-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="11896-112">Область:</span><span class="sxs-lookup"><span data-stu-id="11896-112">Area:</span></span>  <br/> |<span data-ttu-id="11896-113">Вложение в сообщение</span><span class="sxs-lookup"><span data-stu-id="11896-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="11896-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="11896-114">Remarks</span></span>

<span data-ttu-id="11896-115">Данные этого свойства получены из поля заглавного поля MIME содержимого типа, которое начинается с параметра "text/", если присутствует параметр "charset".</span><span class="sxs-lookup"><span data-stu-id="11896-115">This property's data is derived from a Content-Type MIME header field that starts with "text/", if a "charset" parameter is present.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="11896-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="11896-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="11896-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="11896-117">Protocol specifications</span></span>

<span data-ttu-id="11896-118">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="11896-118">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="11896-119">Преобразуется из стандартных конвенций электронной почты в объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="11896-119">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="11896-120">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="11896-120">Header files</span></span>

<span data-ttu-id="11896-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="11896-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="11896-122">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="11896-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="11896-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="11896-123">Mapitags.h</span></span>
  
> <span data-ttu-id="11896-124">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="11896-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="11896-125">См. также</span><span class="sxs-lookup"><span data-stu-id="11896-125">See also</span></span>



[<span data-ttu-id="11896-126">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="11896-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="11896-127">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="11896-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="11896-128">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="11896-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="11896-129">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="11896-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

