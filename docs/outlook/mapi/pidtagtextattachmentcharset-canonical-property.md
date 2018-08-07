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
ms.openlocfilehash: c728799832b10ad2d4533a9a040582b67054baad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812019"
---
# <a name="pidtagtextattachmentcharset-canonical-property"></a><span data-ttu-id="40498-103">Каноническое свойство PidTagTextAttachmentCharset</span><span class="sxs-lookup"><span data-stu-id="40498-103">PidTagTextAttachmentCharset Canonical Property</span></span>

  
  
<span data-ttu-id="40498-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="40498-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="40498-105">Содержит значение набора символов вложения сообщения.</span><span class="sxs-lookup"><span data-stu-id="40498-105">Contains a message attachment's character set value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="40498-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="40498-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="40498-107">Нет</span><span class="sxs-lookup"><span data-stu-id="40498-107">None</span></span>  <br/> |
|<span data-ttu-id="40498-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="40498-108">Identifier:</span></span>  <br/> |<span data-ttu-id="40498-109">0x371B</span><span class="sxs-lookup"><span data-stu-id="40498-109">0x371B</span></span>  <br/> |
|<span data-ttu-id="40498-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="40498-110">Data type:</span></span>  <br/> |<span data-ttu-id="40498-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="40498-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="40498-112">Область:</span><span class="sxs-lookup"><span data-stu-id="40498-112">Area:</span></span>  <br/> |<span data-ttu-id="40498-113">Вложение в сообщение</span><span class="sxs-lookup"><span data-stu-id="40498-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="40498-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="40498-114">Remarks</span></span>

<span data-ttu-id="40498-115">Это свойство данные извлекаются из поля заголовка типа содержимого MIME, который начинается с «text /», при наличии параметра «charset».</span><span class="sxs-lookup"><span data-stu-id="40498-115">This property's data is derived from a Content-Type MIME header field that starts with "text/", if a "charset" parameter is present.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="40498-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="40498-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="40498-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="40498-117">Protocol specifications</span></span>

<span data-ttu-id="40498-118">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="40498-118">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="40498-119">Преобразование conventions стандартных электронной почты Интернета объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="40498-119">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="40498-120">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="40498-120">Header files</span></span>

<span data-ttu-id="40498-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="40498-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="40498-122">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="40498-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="40498-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="40498-123">Mapitags.h</span></span>
  
> <span data-ttu-id="40498-124">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="40498-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="40498-125">См. также</span><span class="sxs-lookup"><span data-stu-id="40498-125">See also</span></span>



[<span data-ttu-id="40498-126">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="40498-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="40498-127">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="40498-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="40498-128">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="40498-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="40498-129">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="40498-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

