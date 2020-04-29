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
ms.openlocfilehash: 098261cd71631e4816d22272e1b1bef1d5932a94
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540947"
---
# <a name="pidnameexchangejunkemailmovestamp-canonical-property"></a><span data-ttu-id="cc353-103">Каноническое свойство PidNameExchangeJunkEmailMoveStamp</span><span class="sxs-lookup"><span data-stu-id="cc353-103">PidNameExchangeJunkEmailMoveStamp Canonical Property</span></span>

  
  
<span data-ttu-id="cc353-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cc353-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cc353-105">Содержит постоянное значение сообщения, которое указывает на то, что сообщение не должно обрабатываться фильтром нежелательной почты, так как сообщение уже было обработано или является безопасным.</span><span class="sxs-lookup"><span data-stu-id="cc353-105">Contains the persisted message value that indicates that the message should not be processed by a spam filter because the message was either already processed or is safe.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cc353-106">Понятные имена:</span><span class="sxs-lookup"><span data-stu-id="cc353-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="cc353-107">Нет</span><span class="sxs-lookup"><span data-stu-id="cc353-107">None</span></span>  <br/> |
|<span data-ttu-id="cc353-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="cc353-108">Property set:</span></span>  <br/> |<span data-ttu-id="cc353-109">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="cc353-109">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="cc353-110">Имя свойства:</span><span class="sxs-lookup"><span data-stu-id="cc353-110">Property name:</span></span>  <br/> |http://schemas.microsoft.com/exchange/junkemailmovestamp  <br/> |
|<span data-ttu-id="cc353-111">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="cc353-111">Data type:</span></span>  <br/> |<span data-ttu-id="cc353-112">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="cc353-112">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="cc353-113">Область:</span><span class="sxs-lookup"><span data-stu-id="cc353-113">Area:</span></span>  <br/> |<span data-ttu-id="cc353-114">Защита обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="cc353-114">Secure messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cc353-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="cc353-115">Remarks</span></span>

<span data-ttu-id="cc353-116">Это свойство отмечено для каждого сообщения, которое перемещается с помощью правила нежелательной почты или является надежным контентом.</span><span class="sxs-lookup"><span data-stu-id="cc353-116">This property is stamped on every message that is moved by the Junk E-Mail Rule or is otherwise trusted content.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="cc353-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="cc353-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cc353-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="cc353-118">Protocol specifications</span></span>

<span data-ttu-id="cc353-119">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cc353-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cc353-120">Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="cc353-120">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="cc353-121">[[MS — ОКСКСПАМ]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cc353-121">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cc353-122">Разрешает обработку списков разрешений и блокировок, а также определение нежелательных сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="cc353-122">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
<span data-ttu-id="cc353-123">[[MS — ОКСОРСС]](https://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cc353-123">[[MS-OXORSS]](https://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cc353-124">Задает свойства и операции, представляющие элементы RSS.</span><span class="sxs-lookup"><span data-stu-id="cc353-124">Specifies the properties and operations that represent RSS items.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cc353-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="cc353-125">Header files</span></span>

<span data-ttu-id="cc353-126">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="cc353-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="cc353-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="cc353-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cc353-128">См. также</span><span class="sxs-lookup"><span data-stu-id="cc353-128">See also</span></span>



[<span data-ttu-id="cc353-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="cc353-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cc353-130">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="cc353-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cc353-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="cc353-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cc353-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="cc353-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

