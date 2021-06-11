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
# <a name="pidtagattachsize-canonical-property"></a><span data-ttu-id="c748a-103">Каноническое свойство PidTagAttachSize</span><span class="sxs-lookup"><span data-stu-id="c748a-103">PidTagAttachSize Canonical Property</span></span>

  
  
<span data-ttu-id="c748a-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c748a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c748a-105">Содержит сумму в bytes размеров всех свойств на вложении.</span><span class="sxs-lookup"><span data-stu-id="c748a-105">Contains the sum, in bytes, of the sizes of all properties on an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c748a-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="c748a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c748a-107">PR_ATTACH_SIZE</span><span class="sxs-lookup"><span data-stu-id="c748a-107">PR_ATTACH_SIZE</span></span>  <br/> |
|<span data-ttu-id="c748a-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="c748a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c748a-109">0x0E20</span><span class="sxs-lookup"><span data-stu-id="c748a-109">0x0E20</span></span>  <br/> |
|<span data-ttu-id="c748a-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="c748a-110">Data type:</span></span>  <br/> |<span data-ttu-id="c748a-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="c748a-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="c748a-112">Область:</span><span class="sxs-lookup"><span data-stu-id="c748a-112">Area:</span></span>  <br/> |<span data-ttu-id="c748a-113">Вложение в сообщение</span><span class="sxs-lookup"><span data-stu-id="c748a-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c748a-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="c748a-114">Remarks</span></span>

<span data-ttu-id="c748a-115">Рекомендуется, чтобы подобекты вложения подвергали **PR_ATTACH_SIZE** свойству.</span><span class="sxs-lookup"><span data-stu-id="c748a-115">It is recommended that attachment subobjects expose the **PR_ATTACH_SIZE** property.</span></span> <span data-ttu-id="c748a-116">В сумму,  PR_ATTACH_SIZE, входит размер свойства  [PR_ATTACH_DATA_BIN (PidTagAttachDataBinary)](pidtagattachdatabinary-canonical-property.md)или **PR_ATTACH_DATA_OBJ** [(PidTagAttachDataObject).](pidtagattachdataobject-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="c748a-116">The sum contained in **PR_ATTACH_SIZE** includes the size of the **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) or **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property.</span></span> <span data-ttu-id="c748a-117">Соответственно, **PR_ATTACH_SIZE** обычно больше, чем содержимое только вложения.</span><span class="sxs-lookup"><span data-stu-id="c748a-117">Accordingly, **PR_ATTACH_SIZE** is usually larger than the contents of the attachment alone.</span></span> 
  
<span data-ttu-id="c748a-118">Это свойство можно использовать для проверки приблизительного размера вложения перед выполнением удаленной передачи с помощью модема и отображения индикаторов прогресса при сохранении вложения на диске.</span><span class="sxs-lookup"><span data-stu-id="c748a-118">This property can be used to check the approximate size of the attachment before performing a remote transfer by modem and to display progress indicators when saving the attachment to disk.</span></span> <span data-ttu-id="c748a-119">Это особенно полезно с присоединенными объектами OLE.</span><span class="sxs-lookup"><span data-stu-id="c748a-119">It is particularly useful with attached OLE objects.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c748a-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c748a-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c748a-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="c748a-121">Protocol specifications</span></span>

<span data-ttu-id="c748a-122">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c748a-122">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c748a-123">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="c748a-123">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c748a-124">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="c748a-124">Header files</span></span>

<span data-ttu-id="c748a-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c748a-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="c748a-126">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="c748a-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="c748a-127">mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c748a-127">mapitags.h</span></span>
  
> <span data-ttu-id="c748a-128">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="c748a-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c748a-129">См. также</span><span class="sxs-lookup"><span data-stu-id="c748a-129">See also</span></span>



[<span data-ttu-id="c748a-130">Каноническое свойство PidTagMessageSize</span><span class="sxs-lookup"><span data-stu-id="c748a-130">PidTagMessageSize Canonical Property</span></span>](pidtagmessagesize-canonical-property.md)


[<span data-ttu-id="c748a-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c748a-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c748a-132">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c748a-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c748a-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="c748a-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c748a-134">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="c748a-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

