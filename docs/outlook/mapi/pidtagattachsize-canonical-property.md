---
title: Каноническое свойство PidTagAttachSize
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachSize
api_type:
- HeaderDef
ms.assetid: 768b3215-dd9f-4aa0-b52c-178ca81a7b07
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f3e4f19ab43a3da7c4840d762d5131813c83d996
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361091"
---
# <a name="pidtagattachsize-canonical-property"></a><span data-ttu-id="76c7d-103">Каноническое свойство PidTagAttachSize</span><span class="sxs-lookup"><span data-stu-id="76c7d-103">PidTagAttachSize Canonical Property</span></span>

  
  
<span data-ttu-id="76c7d-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="76c7d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="76c7d-105">Содержит сумму (в байтах) всех размеров всех свойств вложения.</span><span class="sxs-lookup"><span data-stu-id="76c7d-105">Contains the sum, in bytes, of the sizes of all properties on an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="76c7d-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="76c7d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="76c7d-107">PR_ATTACH_SIZE</span><span class="sxs-lookup"><span data-stu-id="76c7d-107">PR_ATTACH_SIZE</span></span>  <br/> |
|<span data-ttu-id="76c7d-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="76c7d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="76c7d-109">0x0E20</span><span class="sxs-lookup"><span data-stu-id="76c7d-109">0x0E20</span></span>  <br/> |
|<span data-ttu-id="76c7d-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="76c7d-110">Data type:</span></span>  <br/> |<span data-ttu-id="76c7d-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="76c7d-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="76c7d-112">Область:</span><span class="sxs-lookup"><span data-stu-id="76c7d-112">Area:</span></span>  <br/> |<span data-ttu-id="76c7d-113">Вложение в сообщение</span><span class="sxs-lookup"><span data-stu-id="76c7d-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="76c7d-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="76c7d-114">Remarks</span></span>

<span data-ttu-id="76c7d-115">Рекомендуется, чтобы вложенные объекты вложения предоставляли свойство **PR_ATTACH_SIZE** .</span><span class="sxs-lookup"><span data-stu-id="76c7d-115">It is recommended that attachment subobjects expose the **PR_ATTACH_SIZE** property.</span></span> <span data-ttu-id="76c7d-116">Сумма, содержащаяся в **PR_ATTACH_SIZE** , включает размер свойства **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) или **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="76c7d-116">The sum contained in **PR_ATTACH_SIZE** includes the size of the **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) or **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property.</span></span> <span data-ttu-id="76c7d-117">Соответственно, **PR_ATTACH_SIZE** обычно превышает содержимое вложения.</span><span class="sxs-lookup"><span data-stu-id="76c7d-117">Accordingly, **PR_ATTACH_SIZE** is usually larger than the contents of the attachment alone.</span></span> 
  
<span data-ttu-id="76c7d-118">Это свойство можно использовать для проверки приблизительного размера вложения перед выполнением удаленной передачи по модему и отображения индикаторов хода выполнения при сохранении вложения на диск.</span><span class="sxs-lookup"><span data-stu-id="76c7d-118">This property can be used to check the approximate size of the attachment before performing a remote transfer by modem and to display progress indicators when saving the attachment to disk.</span></span> <span data-ttu-id="76c7d-119">Он особенно полезен с присоединенными объектами OLE.</span><span class="sxs-lookup"><span data-stu-id="76c7d-119">It is particularly useful with attached OLE objects.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="76c7d-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="76c7d-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="76c7d-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="76c7d-121">Protocol specifications</span></span>

<span data-ttu-id="76c7d-122">[[MS — ОКСКМСГ]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="76c7d-122">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="76c7d-123">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="76c7d-123">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="76c7d-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="76c7d-124">Header files</span></span>

<span data-ttu-id="76c7d-125">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="76c7d-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="76c7d-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="76c7d-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="76c7d-127">мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="76c7d-127">mapitags.h</span></span>
  
> <span data-ttu-id="76c7d-128">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="76c7d-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="76c7d-129">См. также</span><span class="sxs-lookup"><span data-stu-id="76c7d-129">See also</span></span>



[<span data-ttu-id="76c7d-130">Каноническое свойство PidTagMessageSize</span><span class="sxs-lookup"><span data-stu-id="76c7d-130">PidTagMessageSize Canonical Property</span></span>](pidtagmessagesize-canonical-property.md)


[<span data-ttu-id="76c7d-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="76c7d-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="76c7d-132">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="76c7d-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="76c7d-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="76c7d-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="76c7d-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="76c7d-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

