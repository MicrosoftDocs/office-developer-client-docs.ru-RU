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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401540"
---
# <a name="pidtagtextattachmentcharset-canonical-property"></a><span data-ttu-id="bd243-103">Каноническое свойство PidTagTextAttachmentCharset</span><span class="sxs-lookup"><span data-stu-id="bd243-103">PidTagTextAttachmentCharset Canonical Property</span></span>

  
  
<span data-ttu-id="bd243-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bd243-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bd243-105">Содержит значение набора символов вложения сообщения.</span><span class="sxs-lookup"><span data-stu-id="bd243-105">Contains a message attachment's character set value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bd243-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="bd243-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bd243-107">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="bd243-107">None</span></span>  <br/> |
|<span data-ttu-id="bd243-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="bd243-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bd243-109">0x371B</span><span class="sxs-lookup"><span data-stu-id="bd243-109">0x371B</span></span>  <br/> |
|<span data-ttu-id="bd243-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="bd243-110">Data type:</span></span>  <br/> |<span data-ttu-id="bd243-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="bd243-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="bd243-112">Область:</span><span class="sxs-lookup"><span data-stu-id="bd243-112">Area:</span></span>  <br/> |<span data-ttu-id="bd243-113">Вложение в сообщение</span><span class="sxs-lookup"><span data-stu-id="bd243-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bd243-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="bd243-114">Remarks</span></span>

<span data-ttu-id="bd243-115">Это свойство данные извлекаются из поля заголовка типа содержимого MIME, который начинается с «text /», при наличии параметра «charset».</span><span class="sxs-lookup"><span data-stu-id="bd243-115">This property's data is derived from a Content-Type MIME header field that starts with "text/", if a "charset" parameter is present.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bd243-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="bd243-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bd243-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="bd243-117">Protocol specifications</span></span>

<span data-ttu-id="bd243-118">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bd243-118">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bd243-119">Преобразование conventions стандартных электронной почты Интернета объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="bd243-119">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bd243-120">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="bd243-120">Header files</span></span>

<span data-ttu-id="bd243-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bd243-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="bd243-122">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="bd243-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="bd243-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="bd243-123">Mapitags.h</span></span>
  
> <span data-ttu-id="bd243-124">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="bd243-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bd243-125">См. также</span><span class="sxs-lookup"><span data-stu-id="bd243-125">See also</span></span>



[<span data-ttu-id="bd243-126">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="bd243-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bd243-127">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="bd243-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bd243-128">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="bd243-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bd243-129">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="bd243-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

