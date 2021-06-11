---
title: Каноническое свойство PidTagProviderIcon
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderIcon
api_type:
- COM
ms.assetid: 59c84b1f-13b5-484b-b703-2fb9fcc6c7eb
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 55e6c8fb013e544ae04740aeaeb23ac23949cffb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425640"
---
# <a name="pidtagprovidericon-canonical-property"></a><span data-ttu-id="ee121-103">Каноническое свойство PidTagProviderIcon</span><span class="sxs-lookup"><span data-stu-id="ee121-103">PidTagProviderIcon Canonical Property</span></span>

  
  
<span data-ttu-id="ee121-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ee121-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ee121-105">Содержит строку Unicode, которая указывает настраиваемый значок или значки, отображаемые для поставщика MAPI в панели Microsoft Office Outlook состояния как в интернете, так и в автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="ee121-105">Contains a Unicode string that specifies a custom icon or icons to be displayed for a MAPI provider in the Microsoft Office Outlook status bar in both online and offline states.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ee121-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="ee121-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ee121-107">PR_PROVIDER_ICON, PR_PROVIDER_ICON_W</span><span class="sxs-lookup"><span data-stu-id="ee121-107">PR_PROVIDER_ICON, PR_PROVIDER_ICON_W</span></span>  <br/> |
|<span data-ttu-id="ee121-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="ee121-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ee121-109">0x3417</span><span class="sxs-lookup"><span data-stu-id="ee121-109">0x3417</span></span>  <br/> |
|<span data-ttu-id="ee121-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="ee121-110">Data type:</span></span>  <br/> |<span data-ttu-id="ee121-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ee121-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="ee121-112">Область:</span><span class="sxs-lookup"><span data-stu-id="ee121-112">Area:</span></span>  <br/> |<span data-ttu-id="ee121-113">Хранилище сообщений MAPI</span><span class="sxs-lookup"><span data-stu-id="ee121-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ee121-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="ee121-114">Remarks</span></span>

<span data-ttu-id="ee121-115">В этих свойствах указывается файл ресурса, содержащий настраиваемый значок, который представляет поставщика MAPI в онлайновом состоянии, и необязательно другой настраиваемый значок в автономном состоянии.</span><span class="sxs-lookup"><span data-stu-id="ee121-115">These properties specify the resource file that contains a custom icon that represents a MAPI provider in an online state, and optionally, another custom icon in the offline state.</span></span> <span data-ttu-id="ee121-116">Outlook всегда запрашивает эти свойства в представлении Юникод.</span><span class="sxs-lookup"><span data-stu-id="ee121-116">Outlook always requests these properties in Unicode representation.</span></span> 
  
<span data-ttu-id="ee121-117">Например, следующее значение свойства Outlook загрузить значок ID 1001 из модуля mymod32.dll и использовать этот значок для состояния online: `mymod32.dll,#1001` .</span><span class="sxs-lookup"><span data-stu-id="ee121-117">For example, the following property value instructs Outlook to load icon ID 1001 from the module mymod32.dll and use that icon for the online state:  `mymod32.dll,#1001`.</span></span> <span data-ttu-id="ee121-118">Так как для автономного состояния нет значка, определенного для поставщика, в этом случае в панели состояния используется стандартный значок Outlook автономного режима.</span><span class="sxs-lookup"><span data-stu-id="ee121-118">Since there is no provider-specific icon for the offline state, in this case, the standard Outlook offline icon is used in the status bar.</span></span> 
  
<span data-ttu-id="ee121-119">Следующее значение свойства Outlook загрузить значок ID 1001 из модуля mymod32.dll и использовать этот значок для состояния online, а также загрузить значок ID 1002 из этого же модуля, который будет использоваться для автономного состояния: `mymod32.dll,#1001,#1002` .</span><span class="sxs-lookup"><span data-stu-id="ee121-119">The following property value instructs Outlook to load icon ID 1001 from the module mymod32.dll and use that icon for the online state, and to also load icon ID 1002 from this same module to be used for the offline state:  `mymod32.dll,#1001,#1002`.</span></span> <span data-ttu-id="ee121-120">В Outlook не используется значок состояния.</span><span class="sxs-lookup"><span data-stu-id="ee121-120">No Outlook icon is used in the status bar.</span></span> 
  
<span data-ttu-id="ee121-121">По умолчанию, если не указаны настраиваемые значки, поставщик представлен значками Outlook по умолчанию для состояния online и автономного состояния.</span><span class="sxs-lookup"><span data-stu-id="ee121-121">By default, if no custom icons are specified, the provider is represented by the Outlook default icons for the online state and the offline state.</span></span> <span data-ttu-id="ee121-122">Поставщик может дополнительно указать имя отображения, которое будет отображаться рядом с значком в панели состояния.</span><span class="sxs-lookup"><span data-stu-id="ee121-122">The provider can optionally specify a display name to be shown adjacent to the icon in the status bar.</span></span> <span data-ttu-id="ee121-123">Дополнительные сведения см. **в PR_PROVIDER_DISPLAY_NAME_W** [(PidTagProviderDisplayName).](pidtagproviderdisplayname-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="ee121-123">For more information, see **PR_PROVIDER_DISPLAY_NAME_W** ([PidTagProviderDisplayName](pidtagproviderdisplayname-canonical-property.md)).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ee121-124">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ee121-124">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="ee121-125">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="ee121-125">Header files</span></span>

<span data-ttu-id="ee121-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ee121-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="ee121-127">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="ee121-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="ee121-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ee121-128">Mapitags.h</span></span>
  
> <span data-ttu-id="ee121-129">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="ee121-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ee121-130">См. также</span><span class="sxs-lookup"><span data-stu-id="ee121-130">See also</span></span>



[<span data-ttu-id="ee121-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ee121-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ee121-132">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ee121-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ee121-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="ee121-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ee121-134">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="ee121-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

