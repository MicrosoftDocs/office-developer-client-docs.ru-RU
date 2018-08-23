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
ms.openlocfilehash: 2868533e0383309e013bb82aaa4300a0a40e335a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577515"
---
# <a name="pidtagcontrolid-canonical-property"></a><span data-ttu-id="2938b-103">Каноническое свойство PidTagControlId</span><span class="sxs-lookup"><span data-stu-id="2938b-103">PidTagControlId Canonical Property</span></span>

  
  
<span data-ttu-id="2938b-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2938b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2938b-105">Содержит уникальный идентификатор для элемента управления, используемый в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="2938b-105">Contains a unique identifier for a control used in a dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2938b-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="2938b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2938b-107">PR_CONTROL_ID</span><span class="sxs-lookup"><span data-stu-id="2938b-107">PR_CONTROL_ID</span></span>  <br/> |
|<span data-ttu-id="2938b-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="2938b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2938b-109">0x3F07</span><span class="sxs-lookup"><span data-stu-id="2938b-109">0x3F07</span></span>  <br/> |
|<span data-ttu-id="2938b-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="2938b-110">Data type:</span></span>  <br/> |<span data-ttu-id="2938b-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="2938b-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="2938b-112">Область:</span><span class="sxs-lookup"><span data-stu-id="2938b-112">Area:</span></span>  <br/> |<span data-ttu-id="2938b-113">Таблица отображения MAPI</span><span class="sxs-lookup"><span data-stu-id="2938b-113">MAPI display table</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2938b-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="2938b-114">Remarks</span></span>

<span data-ttu-id="2938b-115">Это свойство содержит уникальный идентификатор для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="2938b-115">This property contains a unique identifier for the control.</span></span> <span data-ttu-id="2938b-116">Этот идентификатор должен содержать структуры [GUID](guid.md) и двоичное значение типа **LONG**.</span><span class="sxs-lookup"><span data-stu-id="2938b-116">This identifier should contain a [GUID](guid.md) structure and a binary value of type **LONG**.</span></span> <span data-ttu-id="2938b-117">Все элементы управления в диалоговом окне должны использовать же **идентификатор GUID** для идентификации поставщика услуг, а все элементы управления, следует использовать уникальное значение **LONG** , чтобы убедиться, что элементы управления не перекрывались.</span><span class="sxs-lookup"><span data-stu-id="2938b-117">All controls in the dialog box should use the same **GUID** to identify the service provider, and each control should use a unique **LONG** value to ensure that the controls do not collide.</span></span> 
  
<span data-ttu-id="2938b-118">Это свойство используется в уведомления.</span><span class="sxs-lookup"><span data-stu-id="2938b-118">This property is used in notifications.</span></span> <span data-ttu-id="2938b-119">Например уведомлений, отправленных в таблице отображения необходимо установить это свойство для уникальной идентификации элемента управления для обновления.</span><span class="sxs-lookup"><span data-stu-id="2938b-119">For example, notifications sent on the display table must set this property to uniquely identify the control to update.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="2938b-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="2938b-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="2938b-121">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="2938b-121">Header files</span></span>

<span data-ttu-id="2938b-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2938b-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="2938b-123">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="2938b-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="2938b-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2938b-124">Mapitags.h</span></span>
  
> <span data-ttu-id="2938b-125">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="2938b-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2938b-126">См. также</span><span class="sxs-lookup"><span data-stu-id="2938b-126">See also</span></span>



[<span data-ttu-id="2938b-127">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="2938b-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2938b-128">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="2938b-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2938b-129">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="2938b-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2938b-130">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="2938b-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

