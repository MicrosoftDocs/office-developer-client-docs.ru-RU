---
title: Каноническое свойство PidTagMessageCodepage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageCodepage
api_type:
- HeaderDef
ms.assetid: eef73e34-470c-4c37-94ce-ea95fe83bc10
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f75a5e10a59d7c6db4e43d2552a38d523b537790
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580203"
---
# <a name="pidtagmessagecodepage-canonical-property"></a><span data-ttu-id="4dbd3-103">Каноническое свойство PidTagMessageCodepage</span><span class="sxs-lookup"><span data-stu-id="4dbd3-103">PidTagMessageCodepage Canonical Property</span></span>

  
  
<span data-ttu-id="4dbd3-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4dbd3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4dbd3-105">Содержит страницы код, используемый для сообщения.</span><span class="sxs-lookup"><span data-stu-id="4dbd3-105">Contains the code page that is used for the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4dbd3-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="4dbd3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4dbd3-107">PR_MESSAGE_CODEPAGE</span><span class="sxs-lookup"><span data-stu-id="4dbd3-107">PR_MESSAGE_CODEPAGE</span></span>  <br/> |
|<span data-ttu-id="4dbd3-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="4dbd3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4dbd3-109">0x3FFD</span><span class="sxs-lookup"><span data-stu-id="4dbd3-109">0x3FFD</span></span>  <br/> |
|<span data-ttu-id="4dbd3-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="4dbd3-110">Data type:</span></span>  <br/> |<span data-ttu-id="4dbd3-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="4dbd3-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="4dbd3-112">Область:</span><span class="sxs-lookup"><span data-stu-id="4dbd3-112">Area:</span></span>  <br/> |<span data-ttu-id="4dbd3-113">Common</span><span class="sxs-lookup"><span data-stu-id="4dbd3-113">Common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4dbd3-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="4dbd3-114">Remarks</span></span>

<span data-ttu-id="4dbd3-115">Кодовая страница папки объект используется в том случае, если это свойство имеет значение нуль (0).</span><span class="sxs-lookup"><span data-stu-id="4dbd3-115">The folder object code page is used if this property is set to zero (0).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4dbd3-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="4dbd3-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4dbd3-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="4dbd3-117">Protocol specifications</span></span>

<span data-ttu-id="4dbd3-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4dbd3-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4dbd3-119">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="4dbd3-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4dbd3-120">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4dbd3-120">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4dbd3-121">Обрабатывает объекты сообщения и вложения.</span><span class="sxs-lookup"><span data-stu-id="4dbd3-121">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="4dbd3-122">[[MS-OXPFOAB]](http://msdn.microsoft.com/library/258a07a7-34a7-4373-87c1-cddf51447d00%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4dbd3-122">[[MS-OXPFOAB]](http://msdn.microsoft.com/library/258a07a7-34a7-4373-87c1-cddf51447d00%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4dbd3-123">Задает метод доставки автономной адресной книги (OAB) данных от сервера к клиенту.</span><span class="sxs-lookup"><span data-stu-id="4dbd3-123">Specifies the method of delivering offline address book (OAB) data from server to client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4dbd3-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="4dbd3-124">Header files</span></span>

<span data-ttu-id="4dbd3-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4dbd3-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="4dbd3-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="4dbd3-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="4dbd3-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4dbd3-127">Mapitags.h</span></span>
  
> <span data-ttu-id="4dbd3-128">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="4dbd3-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4dbd3-129">См. также</span><span class="sxs-lookup"><span data-stu-id="4dbd3-129">See also</span></span>



[<span data-ttu-id="4dbd3-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="4dbd3-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4dbd3-131">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="4dbd3-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4dbd3-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="4dbd3-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4dbd3-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="4dbd3-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

