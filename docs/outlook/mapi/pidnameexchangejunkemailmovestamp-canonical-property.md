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
ms.openlocfilehash: 07acfd8715dccad8833ee14ac8e573fb995539ba
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399706"
---
# <a name="pidnameexchangejunkemailmovestamp-canonical-property"></a><span data-ttu-id="bf84d-103">Каноническое свойство PidNameExchangeJunkEmailMoveStamp</span><span class="sxs-lookup"><span data-stu-id="bf84d-103">PidNameExchangeJunkEmailMoveStamp Canonical Property</span></span>

  
  
<span data-ttu-id="bf84d-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bf84d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bf84d-105">Содержит значение постоянных сообщение, которое указывает, что сообщение не будет обработано фильтром нежелательной почты, так как сообщение уже обработки или безопасном.</span><span class="sxs-lookup"><span data-stu-id="bf84d-105">Contains the persisted message value that indicates that the message should not be processed by a spam filter because the message was either already processed or is safe.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bf84d-106">Понятные имена:</span><span class="sxs-lookup"><span data-stu-id="bf84d-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="bf84d-107">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="bf84d-107">None</span></span>  <br/> |
|<span data-ttu-id="bf84d-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="bf84d-108">Property set:</span></span>  <br/> |<span data-ttu-id="bf84d-109">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="bf84d-109">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="bf84d-110">Имя свойства:</span><span class="sxs-lookup"><span data-stu-id="bf84d-110">Property name:</span></span>  <br/> |https://schemas.microsoft.com/exchange/junkemailmovestamp  <br/> |
|<span data-ttu-id="bf84d-111">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="bf84d-111">Data type:</span></span>  <br/> |<span data-ttu-id="bf84d-112">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="bf84d-112">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="bf84d-113">Область:</span><span class="sxs-lookup"><span data-stu-id="bf84d-113">Area:</span></span>  <br/> |<span data-ttu-id="bf84d-114">Безопасный обмен сообщениями</span><span class="sxs-lookup"><span data-stu-id="bf84d-114">Secure messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bf84d-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="bf84d-115">Remarks</span></span>

<span data-ttu-id="bf84d-116">Это свойство будет указано на каждого сообщения, который перемещается правилом нежелательной электронной почты или в противном случае — надежного содержимого.</span><span class="sxs-lookup"><span data-stu-id="bf84d-116">This property is stamped on every message that is moved by the Junk E-Mail Rule or is otherwise trusted content.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bf84d-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="bf84d-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bf84d-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="bf84d-118">Protocol specifications</span></span>

<span data-ttu-id="bf84d-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bf84d-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bf84d-120">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="bf84d-120">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bf84d-121">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bf84d-121">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bf84d-122">Включает обработку списки разрешенных и запрещенных и определение нежелательных сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="bf84d-122">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
<span data-ttu-id="bf84d-123">[[MS-OXORSS]](https://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bf84d-123">[[MS-OXORSS]](https://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bf84d-124">Задает свойства и операции, которые представляют элементам RSS-Каналов.</span><span class="sxs-lookup"><span data-stu-id="bf84d-124">Specifies the properties and operations that represent RSS items.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bf84d-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="bf84d-125">Header files</span></span>

<span data-ttu-id="bf84d-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bf84d-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="bf84d-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="bf84d-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bf84d-128">См. также</span><span class="sxs-lookup"><span data-stu-id="bf84d-128">See also</span></span>



[<span data-ttu-id="bf84d-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="bf84d-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bf84d-130">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="bf84d-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bf84d-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="bf84d-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bf84d-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="bf84d-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

