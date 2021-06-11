---
title: Каноническое свойство PidTagControlId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagControlId
api_type:
- HeaderDef
ms.assetid: 281bc3e0-7c69-461b-bf09-4281abbb5e1b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b27f59e0bfdcac8eca1751af2f07139f12e2b3a7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416022"
---
# <a name="pidtagcontrolid-canonical-property"></a><span data-ttu-id="6d8c8-103">Каноническое свойство PidTagControlId</span><span class="sxs-lookup"><span data-stu-id="6d8c8-103">PidTagControlId Canonical Property</span></span>

  
  
<span data-ttu-id="6d8c8-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6d8c8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6d8c8-105">Содержит уникальный идентификатор для управления, используемого в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="6d8c8-105">Contains a unique identifier for a control used in a dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6d8c8-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="6d8c8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6d8c8-107">PR_CONTROL_ID</span><span class="sxs-lookup"><span data-stu-id="6d8c8-107">PR_CONTROL_ID</span></span>  <br/> |
|<span data-ttu-id="6d8c8-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="6d8c8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6d8c8-109">0x3F07</span><span class="sxs-lookup"><span data-stu-id="6d8c8-109">0x3F07</span></span>  <br/> |
|<span data-ttu-id="6d8c8-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="6d8c8-110">Data type:</span></span>  <br/> |<span data-ttu-id="6d8c8-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="6d8c8-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="6d8c8-112">Область:</span><span class="sxs-lookup"><span data-stu-id="6d8c8-112">Area:</span></span>  <br/> |<span data-ttu-id="6d8c8-113">Таблица отображения MAPI</span><span class="sxs-lookup"><span data-stu-id="6d8c8-113">MAPI display table</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6d8c8-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="6d8c8-114">Remarks</span></span>

<span data-ttu-id="6d8c8-115">Это свойство содержит уникальный идентификатор для управления.</span><span class="sxs-lookup"><span data-stu-id="6d8c8-115">This property contains a unique identifier for the control.</span></span> <span data-ttu-id="6d8c8-116">Этот идентификатор должен содержать структуру [GUID](guid.md) и двоичное значение типа **LONG**.</span><span class="sxs-lookup"><span data-stu-id="6d8c8-116">This identifier should contain a [GUID](guid.md) structure and a binary value of type **LONG**.</span></span> <span data-ttu-id="6d8c8-117">Все элементы управления в диалоговом окне должны использовать один и тот же **GUID** для идентификации поставщика услуг, и каждый элемент управления должен использовать уникальное значение **LONG** для обеспечения того, чтобы элементы управления не сталкивались.</span><span class="sxs-lookup"><span data-stu-id="6d8c8-117">All controls in the dialog box should use the same **GUID** to identify the service provider, and each control should use a unique **LONG** value to ensure that the controls do not collide.</span></span> 
  
<span data-ttu-id="6d8c8-118">Это свойство используется в уведомлениях.</span><span class="sxs-lookup"><span data-stu-id="6d8c8-118">This property is used in notifications.</span></span> <span data-ttu-id="6d8c8-119">Например, уведомления, отправленные на таблице отображения, должны установить это свойство для уникальной идентификации управления для обновления.</span><span class="sxs-lookup"><span data-stu-id="6d8c8-119">For example, notifications sent on the display table must set this property to uniquely identify the control to update.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="6d8c8-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="6d8c8-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="6d8c8-121">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="6d8c8-121">Header files</span></span>

<span data-ttu-id="6d8c8-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6d8c8-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="6d8c8-123">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="6d8c8-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="6d8c8-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6d8c8-124">Mapitags.h</span></span>
  
> <span data-ttu-id="6d8c8-125">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="6d8c8-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6d8c8-126">См. также</span><span class="sxs-lookup"><span data-stu-id="6d8c8-126">See also</span></span>



[<span data-ttu-id="6d8c8-127">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6d8c8-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6d8c8-128">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6d8c8-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6d8c8-129">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="6d8c8-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6d8c8-130">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="6d8c8-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

