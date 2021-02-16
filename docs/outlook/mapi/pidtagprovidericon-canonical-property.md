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
# <a name="pidtagprovidericon-canonical-property"></a><span data-ttu-id="aea93-103">Каноническое свойство PidTagProviderIcon</span><span class="sxs-lookup"><span data-stu-id="aea93-103">PidTagProviderIcon Canonical Property</span></span>

  
  
<span data-ttu-id="aea93-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aea93-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aea93-105">Содержит строку Юникода, которая указывает настраиваемый значок или значки, отображаемые для поставщика MAPI в строке Microsoft Office Outlook состояния в интерактивном и автономном состояниях.</span><span class="sxs-lookup"><span data-stu-id="aea93-105">Contains a Unicode string that specifies a custom icon or icons to be displayed for a MAPI provider in the Microsoft Office Outlook status bar in both online and offline states.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="aea93-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="aea93-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="aea93-107">PR_PROVIDER_ICON, PR_PROVIDER_ICON_W</span><span class="sxs-lookup"><span data-stu-id="aea93-107">PR_PROVIDER_ICON, PR_PROVIDER_ICON_W</span></span>  <br/> |
|<span data-ttu-id="aea93-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="aea93-108">Identifier:</span></span>  <br/> |<span data-ttu-id="aea93-109">0x3417</span><span class="sxs-lookup"><span data-stu-id="aea93-109">0x3417</span></span>  <br/> |
|<span data-ttu-id="aea93-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="aea93-110">Data type:</span></span>  <br/> |<span data-ttu-id="aea93-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="aea93-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="aea93-112">Область:</span><span class="sxs-lookup"><span data-stu-id="aea93-112">Area:</span></span>  <br/> |<span data-ttu-id="aea93-113">Хранилище сообщений MAPI</span><span class="sxs-lookup"><span data-stu-id="aea93-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="aea93-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="aea93-114">Remarks</span></span>

<span data-ttu-id="aea93-115">Эти свойства указывают файл ресурсов, содержащий настраиваемый значок, который представляет поставщика MAPI в сетевом состоянии, и, при желании, другой пользовательский значок в автономном состоянии.</span><span class="sxs-lookup"><span data-stu-id="aea93-115">These properties specify the resource file that contains a custom icon that represents a MAPI provider in an online state, and optionally, another custom icon in the offline state.</span></span> <span data-ttu-id="aea93-116">Outlook всегда запрашивает эти свойства в представлении Юникод.</span><span class="sxs-lookup"><span data-stu-id="aea93-116">Outlook always requests these properties in Unicode representation.</span></span> 
  
<span data-ttu-id="aea93-117">Например, следующее значение свойства предписывает Outlook загрузить значок 1001 из модуля mymod32.dll и использовать этот значок для сетевого состояния:  `mymod32.dll,#1001` .</span><span class="sxs-lookup"><span data-stu-id="aea93-117">For example, the following property value instructs Outlook to load icon ID 1001 from the module mymod32.dll and use that icon for the online state:  `mymod32.dll,#1001`.</span></span> <span data-ttu-id="aea93-118">Так как для автономного состояния не существует специального значка поставщика, в данном случае стандартный значок автономного режима Outlook используется в панели состояния.</span><span class="sxs-lookup"><span data-stu-id="aea93-118">Since there is no provider-specific icon for the offline state, in this case, the standard Outlook offline icon is used in the status bar.</span></span> 
  
<span data-ttu-id="aea93-119">Следующее значение свойства предписывает Outlook загрузить значок 1001 из модуля mymod32.dll и использовать этот значок для сетевого состояния, а также загрузить значок 1002 из этого же модуля для использования в автономном  `mymod32.dll,#1001,#1002` состоянии:</span><span class="sxs-lookup"><span data-stu-id="aea93-119">The following property value instructs Outlook to load icon ID 1001 from the module mymod32.dll and use that icon for the online state, and to also load icon ID 1002 from this same module to be used for the offline state:  `mymod32.dll,#1001,#1002`.</span></span> <span data-ttu-id="aea93-120">Значок Outlook не используется в панели состояния.</span><span class="sxs-lookup"><span data-stu-id="aea93-120">No Outlook icon is used in the status bar.</span></span> 
  
<span data-ttu-id="aea93-121">По умолчанию, если пользовательские значки не указаны, поставщик представлен значками Outlook по умолчанию для состояния в сети и автономного состояния.</span><span class="sxs-lookup"><span data-stu-id="aea93-121">By default, if no custom icons are specified, the provider is represented by the Outlook default icons for the online state and the offline state.</span></span> <span data-ttu-id="aea93-122">При желании поставщик может указать отображаемую именем рядом со значком в панели состояния.</span><span class="sxs-lookup"><span data-stu-id="aea93-122">The provider can optionally specify a display name to be shown adjacent to the icon in the status bar.</span></span> <span data-ttu-id="aea93-123">Дополнительные сведения **см. в PR_PROVIDER_DISPLAY_NAME_W** ([PidTagProviderDisplayName).](pidtagproviderdisplayname-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="aea93-123">For more information, see **PR_PROVIDER_DISPLAY_NAME_W** ([PidTagProviderDisplayName](pidtagproviderdisplayname-canonical-property.md)).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="aea93-124">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="aea93-124">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="aea93-125">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="aea93-125">Header files</span></span>

<span data-ttu-id="aea93-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="aea93-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="aea93-127">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="aea93-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="aea93-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="aea93-128">Mapitags.h</span></span>
  
> <span data-ttu-id="aea93-129">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="aea93-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="aea93-130">См. также</span><span class="sxs-lookup"><span data-stu-id="aea93-130">See also</span></span>



[<span data-ttu-id="aea93-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="aea93-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="aea93-132">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="aea93-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="aea93-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="aea93-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="aea93-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="aea93-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

