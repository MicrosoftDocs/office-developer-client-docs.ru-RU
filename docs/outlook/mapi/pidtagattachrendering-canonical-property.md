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
# <a name="pidtagattachrendering-canonical-property"></a><span data-ttu-id="9db4f-103">Каноническое свойство PidTagAttachRendering</span><span class="sxs-lookup"><span data-stu-id="9db4f-103">PidTagAttachRendering Canonical Property</span></span>

  
  
<span data-ttu-id="9db4f-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9db4f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9db4f-105">Содержит метафайл Microsoft Windows с отображением сведений о вложении.</span><span class="sxs-lookup"><span data-stu-id="9db4f-105">Contains a Microsoft Windows metafile with rendering information for an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9db4f-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="9db4f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9db4f-107">PR_ATTACH_RENDERING</span><span class="sxs-lookup"><span data-stu-id="9db4f-107">PR_ATTACH_RENDERING</span></span>  <br/> |
|<span data-ttu-id="9db4f-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="9db4f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9db4f-109">0x3709</span><span class="sxs-lookup"><span data-stu-id="9db4f-109">0x3709</span></span>  <br/> |
|<span data-ttu-id="9db4f-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="9db4f-110">Data type:</span></span>  <br/> |<span data-ttu-id="9db4f-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="9db4f-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="9db4f-112">Область:</span><span class="sxs-lookup"><span data-stu-id="9db4f-112">Area:</span></span>  <br/> |<span data-ttu-id="9db4f-113">Вложение в сообщение</span><span class="sxs-lookup"><span data-stu-id="9db4f-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9db4f-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="9db4f-114">Remarks</span></span>

<span data-ttu-id="9db4f-115">Это свойство предназначено для предоставления значка или другого представления пикториал, которое может отображаться в родительском сообщении в точке вложения.</span><span class="sxs-lookup"><span data-stu-id="9db4f-115">The purpose of this property is to provide an icon or other pictorial representation that can be displayed within the parent message at the point of attachment.</span></span> <span data-ttu-id="9db4f-116">Как правило, такое представление включает имя вложения, если оно есть, и характер вложения, например документ Microsoft Office Word.</span><span class="sxs-lookup"><span data-stu-id="9db4f-116">Such representation typically includes the name of the attachment, if any, and the nature of the attachment, such as a Microsoft Office Word document.</span></span> <span data-ttu-id="9db4f-117">Клиентское приложение может использовать это представление в отображении сообщения.</span><span class="sxs-lookup"><span data-stu-id="9db4f-117">A client application can use this representation in the display of the message.</span></span> 
  
<span data-ttu-id="9db4f-118">Для вложенного файла это свойство обычно портрайс значок для файла.</span><span class="sxs-lookup"><span data-stu-id="9db4f-118">For an attached file, this property usually portrays an icon for the file.</span></span> 
  
<span data-ttu-id="9db4f-119">Для вложенного сообщения это свойство обычно не задается.</span><span class="sxs-lookup"><span data-stu-id="9db4f-119">For an attached message, this property is typically not set.</span></span> <span data-ttu-id="9db4f-120">Клиентскому приложению, необходимому для отображения вложенного сообщения, необходимо получить его свойство **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), вызвать [имапиформмгр:: ресолвемессажекласс](imapiformmgr-resolvemessageclass.md) для указателя на соответствующий объект сведений о форме, открыть интерфейс [имапиформинфо](imapiforminfoimapiprop.md) для этого объекта и использовать свойства- **PROPS** для получения свойства **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) или **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="9db4f-120">A client application needing to render an attached message should obtain its **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property, call [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) for a pointer to the corresponding form information object, open the [IMAPIFormInfo](imapiforminfoimapiprop.md) interface on that object, and use **GetProps** to retrieve the **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) or **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="9db4f-121">Для внедренного статического объекта OLE это свойство содержит метафайл Microsoft Windows, который можно использовать для рисования представления вложений в окне.</span><span class="sxs-lookup"><span data-stu-id="9db4f-121">For an embedded static OLE object, this property contains a Microsoft Windows metafile that can be used to draw the attachment representation in a window.</span></span> 
  
<span data-ttu-id="9db4f-122">Для внедренного динамического объекта OLE клиент должен использовать данные OLE для создания данных отображения.</span><span class="sxs-lookup"><span data-stu-id="9db4f-122">For an embedded dynamic OLE object, the client should use the OLE data to generate the rendering information.</span></span> 
  
<span data-ttu-id="9db4f-123">Во всех случаях клиентское приложение должно знать о том, что это свойство обычно имеет размер не более ста байт и может быть усечено в таблице вложений.</span><span class="sxs-lookup"><span data-stu-id="9db4f-123">In all cases, the client application should be aware that this property is usually several hundred bytes in size and is subject to truncation in the attachment table.</span></span> <span data-ttu-id="9db4f-124">Если клиент хочет отобразить вложение из этого свойства, не открывая само вложение, оно должно работать в рамках правила усечения таблицы.</span><span class="sxs-lookup"><span data-stu-id="9db4f-124">If a client wishes to render the attachment from this property without opening the attachment itself, it must work within the table truncation rule.</span></span> <span data-ttu-id="9db4f-125">Более подробную информацию можно узнать [в статье работа с большими столбцами](working-with-large-columns.md).</span><span class="sxs-lookup"><span data-stu-id="9db4f-125">For more information, see [Working with Large Columns](working-with-large-columns.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="9db4f-126">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="9db4f-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9db4f-127">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="9db4f-127">Protocol specifications</span></span>

<span data-ttu-id="9db4f-128">[[MS — ОКСКМСГ]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9db4f-128">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9db4f-129">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="9db4f-129">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9db4f-130">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="9db4f-130">Header files</span></span>

<span data-ttu-id="9db4f-131">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="9db4f-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="9db4f-132">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="9db4f-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="9db4f-133">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="9db4f-133">Mapitags.h</span></span>
  
> <span data-ttu-id="9db4f-134">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="9db4f-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9db4f-135">См. также</span><span class="sxs-lookup"><span data-stu-id="9db4f-135">See also</span></span>



[<span data-ttu-id="9db4f-136">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="9db4f-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9db4f-137">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="9db4f-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9db4f-138">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="9db4f-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9db4f-139">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="9db4f-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

