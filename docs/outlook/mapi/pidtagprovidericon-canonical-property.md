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
ms.openlocfilehash: 92407d56bd095135ac1c6c292aa4b1da4755e93c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811592"
---
# <a name="pidtagprovidericon-canonical-property"></a><span data-ttu-id="01ce9-103">Каноническое свойство PidTagProviderIcon</span><span class="sxs-lookup"><span data-stu-id="01ce9-103">PidTagProviderIcon Canonical Property</span></span>

  
  
<span data-ttu-id="01ce9-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="01ce9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="01ce9-105">Содержит строку Юникода, задает пользовательский значок или значки, отображаемые для поставщика MAPI в строке состояния Microsoft Office Outlook в США и в автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="01ce9-105">Contains a Unicode string that specifies a custom icon or icons to be displayed for a MAPI provider in the Microsoft Office Outlook status bar in both online and offline states.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="01ce9-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="01ce9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="01ce9-107">PR_PROVIDER_ICON PR_PROVIDER_ICON_W</span><span class="sxs-lookup"><span data-stu-id="01ce9-107">PR_PROVIDER_ICON, PR_PROVIDER_ICON_W</span></span>  <br/> |
|<span data-ttu-id="01ce9-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="01ce9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="01ce9-109">0x3417</span><span class="sxs-lookup"><span data-stu-id="01ce9-109">0x3417</span></span>  <br/> |
|<span data-ttu-id="01ce9-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="01ce9-110">Data type:</span></span>  <br/> |<span data-ttu-id="01ce9-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="01ce9-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="01ce9-112">Область:</span><span class="sxs-lookup"><span data-stu-id="01ce9-112">Area:</span></span>  <br/> |<span data-ttu-id="01ce9-113">Хранение сообщений MAPI</span><span class="sxs-lookup"><span data-stu-id="01ce9-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="01ce9-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="01ce9-114">Remarks</span></span>

<span data-ttu-id="01ce9-115">Эти свойства укажите файл ресурсов, содержащий пользовательский значок, представляющий поставщика MAPI в оперативном состоянии, и при необходимости другой пользовательский значок в автономный режим.</span><span class="sxs-lookup"><span data-stu-id="01ce9-115">These properties specify the resource file that contains a custom icon that represents a MAPI provider in an online state, and optionally, another custom icon in the offline state.</span></span> <span data-ttu-id="01ce9-116">Outlook всегда запрашивает этих свойств в Юникод.</span><span class="sxs-lookup"><span data-stu-id="01ce9-116">Outlook always requests these properties in Unicode representation.</span></span> 
  
<span data-ttu-id="01ce9-117">К примеру, следующее значение свойства указывает Outlook, чтобы загрузить значок ID 1001 из mymod32.dll модуль и использовать этот значок для состояние online: `mymod32.dll,#1001`.</span><span class="sxs-lookup"><span data-stu-id="01ce9-117">For example, the following property value instructs Outlook to load icon ID 1001 from the module mymod32.dll and use that icon for the online state:  `mymod32.dll,#1001`.</span></span> <span data-ttu-id="01ce9-118">Так как значок не зависящие от поставщика для автономный режим, в этом случае в строке состояния используется стандартный значок автономной Outlook.</span><span class="sxs-lookup"><span data-stu-id="01ce9-118">Since there is no provider-specific icon for the offline state, in this case, the standard Outlook offline icon is used in the status bar.</span></span> 
  
<span data-ttu-id="01ce9-119">Следующее значение свойства указывает Outlook можно загрузить значок ID 1001 из mymod32.dll модуль и используйте этот значок для состояние online, а также загрузить значок ID 1002 из этой же модуль для использования в автономный режим: `mymod32.dll,#1001,#1002`.</span><span class="sxs-lookup"><span data-stu-id="01ce9-119">The following property value instructs Outlook to load icon ID 1001 from the module mymod32.dll and use that icon for the online state, and to also load icon ID 1002 from this same module to be used for the offline state:  `mymod32.dll,#1001,#1002`.</span></span> <span data-ttu-id="01ce9-120">Значок Outlook не используется в строке состояния.</span><span class="sxs-lookup"><span data-stu-id="01ce9-120">No Outlook icon is used in the status bar.</span></span> 
  
<span data-ttu-id="01ce9-121">По умолчанию если нет настраиваемых значков не заданы, поставщик представлены значки Outlook по умолчанию состояние online и автономный режим.</span><span class="sxs-lookup"><span data-stu-id="01ce9-121">By default, if no custom icons are specified, the provider is represented by the Outlook default icons for the online state and the offline state.</span></span> <span data-ttu-id="01ce9-122">Поставщик при необходимости можно указать отображаемое имя, которое будет отображаться рядом со значком в строке состояния.</span><span class="sxs-lookup"><span data-stu-id="01ce9-122">The provider can optionally specify a display name to be shown adjacent to the icon in the status bar.</span></span> <span data-ttu-id="01ce9-123">Для получения дополнительных сведений см **PR_PROVIDER_DISPLAY_NAME_W** ([PidTagProviderDisplayName](pidtagproviderdisplayname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="01ce9-123">For more information, see **PR_PROVIDER_DISPLAY_NAME_W** ([PidTagProviderDisplayName](pidtagproviderdisplayname-canonical-property.md)).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="01ce9-124">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="01ce9-124">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="01ce9-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="01ce9-125">Header files</span></span>

<span data-ttu-id="01ce9-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="01ce9-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="01ce9-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="01ce9-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="01ce9-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="01ce9-128">Mapitags.h</span></span>
  
> <span data-ttu-id="01ce9-129">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="01ce9-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="01ce9-130">См. также</span><span class="sxs-lookup"><span data-stu-id="01ce9-130">See also</span></span>



[<span data-ttu-id="01ce9-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="01ce9-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="01ce9-132">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="01ce9-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="01ce9-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="01ce9-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="01ce9-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="01ce9-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

