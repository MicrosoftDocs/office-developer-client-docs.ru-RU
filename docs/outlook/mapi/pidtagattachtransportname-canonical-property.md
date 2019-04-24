---
title: Каноническое свойство PidTagAttachTransportName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachTransportName
api_type:
- HeaderDef
ms.assetid: 701fca52-0f96-4019-80cd-c0ccd059ff9b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: bd3a22bf55d03f3a9f06bf5c19650407bcc5627d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361070"
---
# <a name="pidtagattachtransportname-canonical-property"></a><span data-ttu-id="42e93-103">Каноническое свойство PidTagAttachTransportName</span><span class="sxs-lookup"><span data-stu-id="42e93-103">PidTagAttachTransportName Canonical Property</span></span>

  
  
<span data-ttu-id="42e93-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="42e93-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="42e93-105">Содержит имя файла вложения, измененного таким образом, что его можно связать с сообщениями в формате TNEF.</span><span class="sxs-lookup"><span data-stu-id="42e93-105">Contains the name of an attachment file modified so that it can be associated with TNEF messages.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="42e93-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="42e93-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="42e93-107">ПР_АТТАЧ_ТРАНСПОРТ_НАМЕ, ПР_АТТАЧ_ТРАНСПОРТ_НАМЕ_А, ПР_АТТАЧ_ТРАНСПОРТ_НАМЕ_В</span><span class="sxs-lookup"><span data-stu-id="42e93-107">PR_ATTACH_TRANSPORT_NAME, PR_ATTACH_TRANSPORT_NAME_A, PR_ATTACH_TRANSPORT_NAME_W</span></span>  <br/> |
|<span data-ttu-id="42e93-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="42e93-108">Identifier:</span></span>  <br/> |<span data-ttu-id="42e93-109">0x370C</span><span class="sxs-lookup"><span data-stu-id="42e93-109">0x370C</span></span>  <br/> |
|<span data-ttu-id="42e93-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="42e93-110">Data type:</span></span>  <br/> |<span data-ttu-id="42e93-111">PT_STRING8, ПТ_УНИКОДЕ</span><span class="sxs-lookup"><span data-stu-id="42e93-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="42e93-112">Область:</span><span class="sxs-lookup"><span data-stu-id="42e93-112">Area:</span></span>  <br/> |<span data-ttu-id="42e93-113">Вложение в сообщение</span><span class="sxs-lookup"><span data-stu-id="42e93-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="42e93-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="42e93-114">Remarks</span></span>

<span data-ttu-id="42e93-115">В формате TNEF и транспортном поставщике используются эти свойства.</span><span class="sxs-lookup"><span data-stu-id="42e93-115">TNEF and the transport provider use these properties.</span></span> <span data-ttu-id="42e93-116">Они обычно недоступны для клиентских приложений.</span><span class="sxs-lookup"><span data-stu-id="42e93-116">They are usually not available to client applications.</span></span> 
  
<span data-ttu-id="42e93-117">Эти свойства обычно используются в формате TNEF, когда базовая система обмена сообщениями не поддерживает указанные имена файлов.</span><span class="sxs-lookup"><span data-stu-id="42e93-117">These properties are commonly used by TNEF when the underlying messaging system does not support the supplied filenames.</span></span> <span data-ttu-id="42e93-118">Например, они используются, когда пользователь присоединяет несколько файлов с одинаковыми именами, например, пять файлов с именем CONFIG. SYS.</span><span class="sxs-lookup"><span data-stu-id="42e93-118">For example, they are used when the user attaches multiple files with the same name, such as five files named CONFIG.SYS.</span></span> <span data-ttu-id="42e93-119">Поставщик транспорта должен изменить имена, чтобы убедиться, что они уникальны.</span><span class="sxs-lookup"><span data-stu-id="42e93-119">The transport provider must modify the names to make sure they are unique.</span></span> <span data-ttu-id="42e93-120">Каждое измененное имя отображается в **пр_аттач_транспорт_наме** вложения и связанных с ним свойствах.</span><span class="sxs-lookup"><span data-stu-id="42e93-120">Each modified name appears in its attachment's **PR_ATTACH_TRANSPORT_NAME** and associated properties.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="42e93-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="42e93-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="42e93-122">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="42e93-122">Protocol specifications</span></span>

<span data-ttu-id="42e93-123">[[MS — ОКСКМСГ]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="42e93-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="42e93-124">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="42e93-124">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="42e93-125">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="42e93-125">Header files</span></span>

<span data-ttu-id="42e93-126">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="42e93-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="42e93-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="42e93-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="42e93-128">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="42e93-128">Mapitags.h</span></span>
  
> <span data-ttu-id="42e93-129">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="42e93-129">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="42e93-130">См. также</span><span class="sxs-lookup"><span data-stu-id="42e93-130">See also</span></span>



[<span data-ttu-id="42e93-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="42e93-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="42e93-132">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="42e93-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="42e93-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="42e93-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="42e93-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="42e93-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

