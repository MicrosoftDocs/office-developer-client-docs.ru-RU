---
title: Каноническое свойство PidTagServiceExtraUids
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceExtraUids
api_type:
- COM
ms.assetid: 4838a9af-7818-49aa-ace8-cb94dda8471f
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 0fb688e2a845186224c1802f9df2ac537d5bb4d9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422308"
---
# <a name="pidtagserviceextrauids-canonical-property"></a><span data-ttu-id="c8ed6-103">Каноническое свойство PidTagServiceExtraUids</span><span class="sxs-lookup"><span data-stu-id="c8ed6-103">PidTagServiceExtraUids Canonical Property</span></span>

  
  
<span data-ttu-id="c8ed6-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c8ed6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c8ed6-105">Содержит список структур [мапиуид](mapiuid.md) , которые определяют дополнительные разделы профиля для службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="c8ed6-105">Contains a list of [MAPIUID](mapiuid.md) structures that identify additional profile sections for the message service.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c8ed6-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="c8ed6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c8ed6-107">PR_SERVICE_EXTRA_UIDS</span><span class="sxs-lookup"><span data-stu-id="c8ed6-107">PR_SERVICE_EXTRA_UIDS</span></span>  <br/> |
|<span data-ttu-id="c8ed6-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="c8ed6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c8ed6-109">0x3D0D</span><span class="sxs-lookup"><span data-stu-id="c8ed6-109">0x3D0D</span></span>  <br/> |
|<span data-ttu-id="c8ed6-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="c8ed6-110">Data type:</span></span>  <br/> |<span data-ttu-id="c8ed6-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="c8ed6-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="c8ed6-112">Область:</span><span class="sxs-lookup"><span data-stu-id="c8ed6-112">Area:</span></span>  <br/> |<span data-ttu-id="c8ed6-113">Профиль MAPI</span><span class="sxs-lookup"><span data-stu-id="c8ed6-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c8ed6-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="c8ed6-114">Remarks</span></span>

<span data-ttu-id="c8ed6-115">Для каждого фильтра сообщений можно создавать новые разделы профилей.</span><span class="sxs-lookup"><span data-stu-id="c8ed6-115">New profile sections can be created for each message filter.</span></span> <span data-ttu-id="c8ed6-116">Когда информация о службе сообщений копируется в другой профиль, важно также скопировать дополнительные разделы профиля для этих фильтров.</span><span class="sxs-lookup"><span data-stu-id="c8ed6-116">When the information about the message service is to be copied to another profile, it is important to copy the additional profile sections for the filters as well.</span></span> <span data-ttu-id="c8ed6-117">Поставщик услуг, использующий дополнительные разделы профилей, может хранить структуры **мапиуид** в разделах профилей в **PR_SERVICE_EXTRA_UIDS**, что позволяет MAPI копировать дополнительные сведения о службе сообщений.</span><span class="sxs-lookup"><span data-stu-id="c8ed6-117">A service provider that uses additional profile sections can store the **MAPIUID** structures of those profile sections in **PR_SERVICE_EXTRA_UIDS**, which allows MAPI to copy the additional message service information.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c8ed6-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c8ed6-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="c8ed6-119">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="c8ed6-119">Header files</span></span>

<span data-ttu-id="c8ed6-120">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="c8ed6-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="c8ed6-121">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="c8ed6-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="c8ed6-122">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="c8ed6-122">Mapitags.h</span></span>
  
> <span data-ttu-id="c8ed6-123">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="c8ed6-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c8ed6-124">См. также</span><span class="sxs-lookup"><span data-stu-id="c8ed6-124">See also</span></span>



[<span data-ttu-id="c8ed6-125">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c8ed6-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c8ed6-126">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="c8ed6-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c8ed6-127">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="c8ed6-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c8ed6-128">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="c8ed6-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

