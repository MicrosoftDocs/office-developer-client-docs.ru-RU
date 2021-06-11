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
ms.openlocfilehash: 22d3e649641dbe688912ecece7fde73a555f4a88
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361098"
---
# <a name="pidtagattachrendering-canonical-property"></a><span data-ttu-id="e9109-103">Каноническое свойство PidTagAttachRendering</span><span class="sxs-lookup"><span data-stu-id="e9109-103">PidTagAttachRendering Canonical Property</span></span>

  
  
<span data-ttu-id="e9109-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e9109-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e9109-105">Содержит метафиль microsoft Windows с отрисовкой сведений для вложения.</span><span class="sxs-lookup"><span data-stu-id="e9109-105">Contains a Microsoft Windows metafile with rendering information for an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e9109-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="e9109-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e9109-107">PR_ATTACH_RENDERING</span><span class="sxs-lookup"><span data-stu-id="e9109-107">PR_ATTACH_RENDERING</span></span>  <br/> |
|<span data-ttu-id="e9109-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="e9109-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e9109-109">0x3709</span><span class="sxs-lookup"><span data-stu-id="e9109-109">0x3709</span></span>  <br/> |
|<span data-ttu-id="e9109-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="e9109-110">Data type:</span></span>  <br/> |<span data-ttu-id="e9109-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="e9109-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="e9109-112">Область:</span><span class="sxs-lookup"><span data-stu-id="e9109-112">Area:</span></span>  <br/> |<span data-ttu-id="e9109-113">Вложение в сообщение</span><span class="sxs-lookup"><span data-stu-id="e9109-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e9109-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="e9109-114">Remarks</span></span>

<span data-ttu-id="e9109-115">Целью этого свойства является предоставление значка или другого изображения, которое может отображаться в родительском сообщении в точке вложения.</span><span class="sxs-lookup"><span data-stu-id="e9109-115">The purpose of this property is to provide an icon or other pictorial representation that can be displayed within the parent message at the point of attachment.</span></span> <span data-ttu-id="e9109-116">Такое представление обычно включает имя вложения, если таковые имеются, и характер вложения, например документ Microsoft Office Word.</span><span class="sxs-lookup"><span data-stu-id="e9109-116">Such representation typically includes the name of the attachment, if any, and the nature of the attachment, such as a Microsoft Office Word document.</span></span> <span data-ttu-id="e9109-117">Клиентская заявка может использовать это представление на дисплее сообщения.</span><span class="sxs-lookup"><span data-stu-id="e9109-117">A client application can use this representation in the display of the message.</span></span> 
  
<span data-ttu-id="e9109-118">Для присоединенного файла это свойство обычно отображает значок для файла.</span><span class="sxs-lookup"><span data-stu-id="e9109-118">For an attached file, this property usually portrays an icon for the file.</span></span> 
  
<span data-ttu-id="e9109-119">Для прикрепленного сообщения это свойство обычно не заданной.</span><span class="sxs-lookup"><span data-stu-id="e9109-119">For an attached message, this property is typically not set.</span></span> <span data-ttu-id="e9109-120">Клиентский приложение, нуждающийся в отрисовке прикрепленного **сообщения,** должно получить свойство PR_MESSAGE_CLASS [(PidTagMessageClass),](pidtagmessageclass-canonical-property.md)вызвать [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) для указателя на соответствующий информационный объект формы, открыть интерфейс [IMAPIFormInfo](imapiforminfoimapiprop.md) на этом объекте и использовать **GetProps** для получения свойства **PR_ICON** [(PidTagIcon)](pidtagicon-canonical-property.md)или PR_MINI_ICON [(PidTagMiniIcon).](pidtagminiicon-canonical-property.md) </span><span class="sxs-lookup"><span data-stu-id="e9109-120">A client application needing to render an attached message should obtain its **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property, call [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) for a pointer to the corresponding form information object, open the [IMAPIFormInfo](imapiforminfoimapiprop.md) interface on that object, and use **GetProps** to retrieve the **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) or **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="e9109-121">Для встроенного статического объекта OLE это свойство содержит метафиль microsoft Windows, который можно использовать для нарисовки представления вложений в окне.</span><span class="sxs-lookup"><span data-stu-id="e9109-121">For an embedded static OLE object, this property contains a Microsoft Windows metafile that can be used to draw the attachment representation in a window.</span></span> 
  
<span data-ttu-id="e9109-122">Для встроенного динамического объекта OLE клиент должен использовать данные OLE для создания данных отрисовки.</span><span class="sxs-lookup"><span data-stu-id="e9109-122">For an embedded dynamic OLE object, the client should use the OLE data to generate the rendering information.</span></span> 
  
<span data-ttu-id="e9109-123">Во всех случаях клиентские приложения должны знать, что это свойство обычно имеет размер в несколько сотен bytes и подлежит truncation в таблице вложений.</span><span class="sxs-lookup"><span data-stu-id="e9109-123">In all cases, the client application should be aware that this property is usually several hundred bytes in size and is subject to truncation in the attachment table.</span></span> <span data-ttu-id="e9109-124">Если клиент хочет отрисовки вложения из этого свойства, не открывая само вложение, он должен работать в правиле обрезки таблицы.</span><span class="sxs-lookup"><span data-stu-id="e9109-124">If a client wishes to render the attachment from this property without opening the attachment itself, it must work within the table truncation rule.</span></span> <span data-ttu-id="e9109-125">Дополнительные сведения см. в [статье Работа с большими столбцами.](working-with-large-columns.md)</span><span class="sxs-lookup"><span data-stu-id="e9109-125">For more information, see [Working with Large Columns](working-with-large-columns.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e9109-126">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="e9109-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e9109-127">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="e9109-127">Protocol specifications</span></span>

<span data-ttu-id="e9109-128">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e9109-128">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e9109-129">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="e9109-129">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e9109-130">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="e9109-130">Header files</span></span>

<span data-ttu-id="e9109-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e9109-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="e9109-132">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="e9109-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="e9109-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e9109-133">Mapitags.h</span></span>
  
> <span data-ttu-id="e9109-134">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="e9109-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e9109-135">См. также</span><span class="sxs-lookup"><span data-stu-id="e9109-135">See also</span></span>



[<span data-ttu-id="e9109-136">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="e9109-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e9109-137">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="e9109-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e9109-138">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="e9109-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e9109-139">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="e9109-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

