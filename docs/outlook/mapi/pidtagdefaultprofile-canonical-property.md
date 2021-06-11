---
title: Каноническое свойство PidTagDefaultProfile
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefaultProfile
api_type:
- HeaderDef
ms.assetid: 47f745a4-5a9c-42af-b076-a72548ef4d31
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 8295ae6904f503ca831a00c1f35ac08596b5358c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428776"
---
# <a name="pidtagdefaultprofile-canonical-property"></a><span data-ttu-id="3ed92-103">Каноническое свойство PidTagDefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ed92-103">PidTagDefaultProfile Canonical Property</span></span>

  
  
<span data-ttu-id="3ed92-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3ed92-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3ed92-105">Содержит TRUE, если профиль пользователя обмена сообщениями — это профиль по умолчанию MAPI.</span><span class="sxs-lookup"><span data-stu-id="3ed92-105">Contains TRUE if a messaging user profile is the MAPI default profile.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3ed92-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="3ed92-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3ed92-107">PR_DEFAULT_PROFILE</span><span class="sxs-lookup"><span data-stu-id="3ed92-107">PR_DEFAULT_PROFILE</span></span>  <br/> |
|<span data-ttu-id="3ed92-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="3ed92-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3ed92-109">0x3D04</span><span class="sxs-lookup"><span data-stu-id="3ed92-109">0x3D04</span></span>  <br/> |
|<span data-ttu-id="3ed92-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="3ed92-110">Data type:</span></span>  <br/> |<span data-ttu-id="3ed92-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="3ed92-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="3ed92-112">Область:</span><span class="sxs-lookup"><span data-stu-id="3ed92-112">Area:</span></span>  <br/> |<span data-ttu-id="3ed92-113">Профиль MAPI</span><span class="sxs-lookup"><span data-stu-id="3ed92-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3ed92-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="3ed92-114">Remarks</span></span>

<span data-ttu-id="3ed92-115">Это свойство не появляется как свойство любого объекта, а только как столбец в таблице профилей.</span><span class="sxs-lookup"><span data-stu-id="3ed92-115">This property does not appear as a property of any object but only as a column in a profile table.</span></span> <span data-ttu-id="3ed92-116">Клиентские приложения могут использовать [метод IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md) для назначить профиль по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3ed92-116">A client application can use the [IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md) method to designate the default profile.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="3ed92-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="3ed92-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="3ed92-118">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="3ed92-118">Header files</span></span>

<span data-ttu-id="3ed92-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3ed92-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="3ed92-120">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="3ed92-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="3ed92-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3ed92-121">Mapitags.h</span></span>
  
> <span data-ttu-id="3ed92-122">Содержит определения свойств, перечисленных в качестве связанных свойств.</span><span class="sxs-lookup"><span data-stu-id="3ed92-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3ed92-123">См. также</span><span class="sxs-lookup"><span data-stu-id="3ed92-123">See also</span></span>



[<span data-ttu-id="3ed92-124">Каноническое свойство PidTagDefaultStore</span><span class="sxs-lookup"><span data-stu-id="3ed92-124">PidTagDefaultStore Canonical Property</span></span>](pidtagdefaultstore-canonical-property.md)


[<span data-ttu-id="3ed92-125">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="3ed92-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3ed92-126">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="3ed92-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3ed92-127">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="3ed92-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3ed92-128">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="3ed92-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

