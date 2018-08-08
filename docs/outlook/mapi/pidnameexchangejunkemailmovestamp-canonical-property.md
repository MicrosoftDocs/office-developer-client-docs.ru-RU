---
title: Каноническое свойство PidNameExchangeJunkEmailMoveStamp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameExchangeJunkEmailMoveStamp
api_type:
- COM
ms.assetid: 7a52f46c-371c-46d0-8d66-e154482e8269
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 41e1113faec18625f57b24f9fc165e2cb029724d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810711"
---
# <a name="pidnameexchangejunkemailmovestamp-canonical-property"></a><span data-ttu-id="c7b19-103">Каноническое свойство PidNameExchangeJunkEmailMoveStamp</span><span class="sxs-lookup"><span data-stu-id="c7b19-103">PidNameExchangeJunkEmailMoveStamp Canonical Property</span></span>

  
  
<span data-ttu-id="c7b19-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c7b19-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c7b19-105">Содержит значение постоянных сообщение, которое указывает, что сообщение не будет обработано фильтром нежелательной почты, так как сообщение уже обработки или безопасном.</span><span class="sxs-lookup"><span data-stu-id="c7b19-105">Contains the persisted message value that indicates that the message should not be processed by a spam filter because the message was either already processed or is safe.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c7b19-106">Понятные имена:</span><span class="sxs-lookup"><span data-stu-id="c7b19-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="c7b19-107">Нет</span><span class="sxs-lookup"><span data-stu-id="c7b19-107">None</span></span>  <br/> |
|<span data-ttu-id="c7b19-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="c7b19-108">Property set:</span></span>  <br/> |<span data-ttu-id="c7b19-109">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="c7b19-109">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="c7b19-110">Имя свойства:</span><span class="sxs-lookup"><span data-stu-id="c7b19-110">Property name:</span></span>  <br/> |http://schemas.microsoft.com/exchange/junkemailmovestamp  <br/> |
|<span data-ttu-id="c7b19-111">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="c7b19-111">Data type:</span></span>  <br/> |<span data-ttu-id="c7b19-112">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="c7b19-112">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="c7b19-113">Область:</span><span class="sxs-lookup"><span data-stu-id="c7b19-113">Area:</span></span>  <br/> |<span data-ttu-id="c7b19-114">Безопасный обмен сообщениями</span><span class="sxs-lookup"><span data-stu-id="c7b19-114">Secure messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c7b19-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="c7b19-115">Remarks</span></span>

<span data-ttu-id="c7b19-116">Это свойство будет указано на каждого сообщения, который перемещается правилом нежелательной электронной почты или в противном случае — надежного содержимого.</span><span class="sxs-lookup"><span data-stu-id="c7b19-116">This property is stamped on every message that is moved by the Junk E-Mail Rule or is otherwise trusted content.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c7b19-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c7b19-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c7b19-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="c7b19-118">Protocol specifications</span></span>

<span data-ttu-id="c7b19-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c7b19-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c7b19-120">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="c7b19-120">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c7b19-121">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c7b19-121">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c7b19-122">Включает обработку списки разрешенных и запрещенных и определение нежелательных сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="c7b19-122">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
<span data-ttu-id="c7b19-123">[[MS-OXORSS]](http://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c7b19-123">[[MS-OXORSS]](http://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c7b19-124">Задает свойства и операции, которые представляют элементам RSS-Каналов.</span><span class="sxs-lookup"><span data-stu-id="c7b19-124">Specifies the properties and operations that represent RSS items.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c7b19-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="c7b19-125">Header files</span></span>

<span data-ttu-id="c7b19-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c7b19-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="c7b19-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="c7b19-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c7b19-128">См. также</span><span class="sxs-lookup"><span data-stu-id="c7b19-128">See also</span></span>



[<span data-ttu-id="c7b19-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c7b19-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c7b19-130">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c7b19-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c7b19-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="c7b19-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c7b19-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="c7b19-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

