---
title: Каноническое свойство PidTagDelegateFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDelegateFlags
api_type:
- HeaderDef
ms.assetid: 3a504594-204c-472c-8be7-dca154c94ea2
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 20ffc6f7f4d21f980e5f0f387464430ba187192a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359901"
---
# <a name="pidtagdelegateflags-canonical-property"></a><span data-ttu-id="6f116-103">Каноническое свойство PidTagDelegateFlags</span><span class="sxs-lookup"><span data-stu-id="6f116-103">PidTagDelegateFlags Canonical Property</span></span>

  
  
<span data-ttu-id="6f116-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6f116-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6f116-105">Указывает, может ли представитель просматривать частные объекты сообщений этого представителя.</span><span class="sxs-lookup"><span data-stu-id="6f116-105">Specifies whether a delegate can view the delegator's private message objects.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6f116-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="6f116-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6f116-107">ПР_ДЕЛЕГАТЕ_ФЛАГС</span><span class="sxs-lookup"><span data-stu-id="6f116-107">PR_DELEGATE_FLAGS</span></span>  <br/> |
|<span data-ttu-id="6f116-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="6f116-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6f116-109">0x686B</span><span class="sxs-lookup"><span data-stu-id="6f116-109">0x686B</span></span>  <br/> |
|<span data-ttu-id="6f116-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="6f116-110">Data type:</span></span>  <br/> |<span data-ttu-id="6f116-111">ПТ_МВ_ЛОНГ</span><span class="sxs-lookup"><span data-stu-id="6f116-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="6f116-112">Область:</span><span class="sxs-lookup"><span data-stu-id="6f116-112">Area:</span></span>  <br/> |<span data-ttu-id="6f116-113">Определяемый классом Message передающей</span><span class="sxs-lookup"><span data-stu-id="6f116-113">Message class-defined transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6f116-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="6f116-114">Remarks</span></span>

<span data-ttu-id="6f116-115">Каждой записи этого свойства должно быть присвоено одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="6f116-115">Each entry of this property must be set to one of the following values.</span></span>
  
|<span data-ttu-id="6f116-116">**Флаг**</span><span class="sxs-lookup"><span data-stu-id="6f116-116">**Flag**</span></span>|<span data-ttu-id="6f116-117">**Value**</span><span class="sxs-lookup"><span data-stu-id="6f116-117">**Value**</span></span>|<span data-ttu-id="6f116-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6f116-118">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6f116-119">Хидепривате</span><span class="sxs-lookup"><span data-stu-id="6f116-119">HidePrivate</span></span>  <br/> |<span data-ttu-id="6f116-120">нуль</span><span class="sxs-lookup"><span data-stu-id="6f116-120">0</span></span>  <br/> |<span data-ttu-id="6f116-121">Представителю не следует разрешено просматривать объекты частных сообщений.</span><span class="sxs-lookup"><span data-stu-id="6f116-121">The delegate should not be allowed to view private message objects.</span></span>  <br/> |
|<span data-ttu-id="6f116-122">Шовпривате</span><span class="sxs-lookup"><span data-stu-id="6f116-122">ShowPrivate</span></span>  <br/> |<span data-ttu-id="6f116-123">1,1</span><span class="sxs-lookup"><span data-stu-id="6f116-123">1</span></span>  <br/> |<span data-ttu-id="6f116-124">Представителю следует разрешить просмотр частных объектов сообщений.</span><span class="sxs-lookup"><span data-stu-id="6f116-124">The delegate should be allowed to view private message objects.</span></span>  <br/> |
   
<span data-ttu-id="6f116-125">Это свойство должно быть задано в объекте сведений о делегате.</span><span class="sxs-lookup"><span data-stu-id="6f116-125">This property must be set in the delegate information object.</span></span> <span data-ttu-id="6f116-126">Значение "Шовпривате" указывает на то, что делегирование хочет отобразить частные объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="6f116-126">The value of "ShowPrivate" indicates that the delegator wants to make private message objects visible.</span></span> <span data-ttu-id="6f116-127">Этот параметр применяется ко всем папкам, для которых представитель имеет роль рецензента, автора или редактора.</span><span class="sxs-lookup"><span data-stu-id="6f116-127">This preference is applicable to all folders for which the delegate has a role of reviewer, author, or editor.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6f116-128">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="6f116-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6f116-129">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="6f116-129">Protocol specifications</span></span>

<span data-ttu-id="6f116-130">[[MS — ОКСОДЛГТ]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6f116-130">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6f116-131">Задает методы для подключения и настройки почтовых ящиков в качестве делегатов и взаимодействия с объектами Message и Calendar, когда они действуют от имени другого пользователя.</span><span class="sxs-lookup"><span data-stu-id="6f116-131">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6f116-132">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="6f116-132">Header files</span></span>

<span data-ttu-id="6f116-133">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="6f116-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="6f116-134">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="6f116-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="6f116-135">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="6f116-135">Mapitags.h</span></span>
  
> <span data-ttu-id="6f116-136">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="6f116-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6f116-137">См. также</span><span class="sxs-lookup"><span data-stu-id="6f116-137">See also</span></span>



[<span data-ttu-id="6f116-138">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6f116-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6f116-139">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="6f116-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6f116-140">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="6f116-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6f116-141">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="6f116-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

