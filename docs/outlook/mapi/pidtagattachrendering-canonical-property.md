---
title: Каноническое свойство PidTagAttachRendering
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachRendering
api_type:
- HeaderDef
ms.assetid: 1f31f7f4-fbda-4337-95e5-5474dd1bf84a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a1df3ba8e57f1e91894b88d7e8a72feb681e13dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810870"
---
# <a name="pidtagattachrendering-canonical-property"></a><span data-ttu-id="faf1f-103">Каноническое свойство PidTagAttachRendering</span><span class="sxs-lookup"><span data-stu-id="faf1f-103">PidTagAttachRendering Canonical Property</span></span>

  
  
<span data-ttu-id="faf1f-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="faf1f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="faf1f-105">Содержит метафайлов Microsoft Windows с сведения о визуализации для вложения.</span><span class="sxs-lookup"><span data-stu-id="faf1f-105">Contains a Microsoft Windows metafile with rendering information for an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="faf1f-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="faf1f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="faf1f-107">PR_ATTACH_RENDERING</span><span class="sxs-lookup"><span data-stu-id="faf1f-107">PR_ATTACH_RENDERING</span></span>  <br/> |
|<span data-ttu-id="faf1f-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="faf1f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="faf1f-109">0x3709</span><span class="sxs-lookup"><span data-stu-id="faf1f-109">0x3709</span></span>  <br/> |
|<span data-ttu-id="faf1f-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="faf1f-110">Data type:</span></span>  <br/> |<span data-ttu-id="faf1f-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="faf1f-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="faf1f-112">Область:</span><span class="sxs-lookup"><span data-stu-id="faf1f-112">Area:</span></span>  <br/> |<span data-ttu-id="faf1f-113">Вложение в сообщение</span><span class="sxs-lookup"><span data-stu-id="faf1f-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="faf1f-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="faf1f-114">Remarks</span></span>

<span data-ttu-id="faf1f-115">Это свойство предназначено для предоставления значок или другие графические представление, которое может отображаться в сообщении родительского точке вложения.</span><span class="sxs-lookup"><span data-stu-id="faf1f-115">The purpose of this property is to provide an icon or other pictorial representation that can be displayed within the parent message at the point of attachment.</span></span> <span data-ttu-id="faf1f-116">Такое представление обычно включает в себя, имя вложения, при их наличии и характер вложения, такие как документ Microsoft Office Word.</span><span class="sxs-lookup"><span data-stu-id="faf1f-116">Such representation typically includes the name of the attachment, if any, and the nature of the attachment, such as a Microsoft Office Word document.</span></span> <span data-ttu-id="faf1f-117">Клиентское приложение может использовать это представление в окне сообщения.</span><span class="sxs-lookup"><span data-stu-id="faf1f-117">A client application can use this representation in the display of the message.</span></span> 
  
<span data-ttu-id="faf1f-118">Для вложенного файла это свойство обычно показан переключатель, относящийся значка для файла.</span><span class="sxs-lookup"><span data-stu-id="faf1f-118">For an attached file, this property usually portrays an icon for the file.</span></span> 
  
<span data-ttu-id="faf1f-119">Вложенные сообщения это свойство обычно не задается.</span><span class="sxs-lookup"><span data-stu-id="faf1f-119">For an attached message, this property is typically not set.</span></span> <span data-ttu-id="faf1f-120">Клиентское приложение для отображения вложенное сообщение должны получить его свойство **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), вызовите [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) для указателя соответствующего объекта данные формы Откройте интерфейс [IMAPIFormInfo](imapiforminfoimapiprop.md) для этого объекта и используйте **GetProps** , чтобы получить **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) или свойство **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="faf1f-120">A client application needing to render an attached message should obtain its **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property, call [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) for a pointer to the corresponding form information object, open the [IMAPIFormInfo](imapiforminfoimapiprop.md) interface on that object, and use **GetProps** to retrieve the **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) or **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="faf1f-121">Для статических внедренный объект OLE это свойство содержит метафайл Microsoft Windows, который можно использовать для рисования представление вложения в окне.</span><span class="sxs-lookup"><span data-stu-id="faf1f-121">For an embedded static OLE object, this property contains a Microsoft Windows metafile that can be used to draw the attachment representation in a window.</span></span> 
  
<span data-ttu-id="faf1f-122">Для динамического внедренный объект OLE клиент должен использовать данные OLE для создания отображения сведений.</span><span class="sxs-lookup"><span data-stu-id="faf1f-122">For an embedded dynamic OLE object, the client should use the OLE data to generate the rendering information.</span></span> 
  
<span data-ttu-id="faf1f-123">Во всех случаях клиентское приложение следует иметь в виду, что это свойство обычно является нескольких сотен байтов по размеру и может быть усечения в таблице вложений.</span><span class="sxs-lookup"><span data-stu-id="faf1f-123">In all cases, the client application should be aware that this property is usually several hundred bytes in size and is subject to truncation in the attachment table.</span></span> <span data-ttu-id="faf1f-124">Если необходимо отображать вложения из этого свойства без открытия самого вложение клиента, работы в рамках правила усечения таблицы.</span><span class="sxs-lookup"><span data-stu-id="faf1f-124">If a client wishes to render the attachment from this property without opening the attachment itself, it must work within the table truncation rule.</span></span> <span data-ttu-id="faf1f-125">Для получения дополнительных сведений см [большой](working-with-large-columns.md).</span><span class="sxs-lookup"><span data-stu-id="faf1f-125">For more information, see [Working with Large Columns](working-with-large-columns.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="faf1f-126">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="faf1f-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="faf1f-127">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="faf1f-127">Protocol specifications</span></span>

<span data-ttu-id="faf1f-128">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="faf1f-128">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="faf1f-129">Обрабатывает объекты сообщения и вложения.</span><span class="sxs-lookup"><span data-stu-id="faf1f-129">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="faf1f-130">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="faf1f-130">Header files</span></span>

<span data-ttu-id="faf1f-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="faf1f-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="faf1f-132">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="faf1f-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="faf1f-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="faf1f-133">Mapitags.h</span></span>
  
> <span data-ttu-id="faf1f-134">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="faf1f-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="faf1f-135">См. также</span><span class="sxs-lookup"><span data-stu-id="faf1f-135">See also</span></span>



[<span data-ttu-id="faf1f-136">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="faf1f-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="faf1f-137">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="faf1f-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="faf1f-138">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="faf1f-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="faf1f-139">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="faf1f-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

