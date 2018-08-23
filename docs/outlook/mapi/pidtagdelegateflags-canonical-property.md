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
ms.openlocfilehash: d43ec0bd2978c64e3a5ceb635f0dcda57de01cfd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590738"
---
# <a name="pidtagdelegateflags-canonical-property"></a><span data-ttu-id="77b5e-103">Каноническое свойство PidTagDelegateFlags</span><span class="sxs-lookup"><span data-stu-id="77b5e-103">PidTagDelegateFlags Canonical Property</span></span>

  
  
<span data-ttu-id="77b5e-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="77b5e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="77b5e-105">Указывает ли делегата можно просматривать объекты представитель личное сообщение.</span><span class="sxs-lookup"><span data-stu-id="77b5e-105">Specifies whether a delegate can view the delegator's private message objects.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="77b5e-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="77b5e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="77b5e-107">PR_DELEGATE_FLAGS</span><span class="sxs-lookup"><span data-stu-id="77b5e-107">PR_DELEGATE_FLAGS</span></span>  <br/> |
|<span data-ttu-id="77b5e-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="77b5e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="77b5e-109">0x686B</span><span class="sxs-lookup"><span data-stu-id="77b5e-109">0x686B</span></span>  <br/> |
|<span data-ttu-id="77b5e-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="77b5e-110">Data type:</span></span>  <br/> |<span data-ttu-id="77b5e-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="77b5e-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="77b5e-112">Область:</span><span class="sxs-lookup"><span data-stu-id="77b5e-112">Area:</span></span>  <br/> |<span data-ttu-id="77b5e-113">Сообщение, определенное класс передаваемого</span><span class="sxs-lookup"><span data-stu-id="77b5e-113">Message class-defined transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="77b5e-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="77b5e-114">Remarks</span></span>

<span data-ttu-id="77b5e-115">Каждая запись этого свойства необходимо установить одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="77b5e-115">Each entry of this property must be set to one of the following values.</span></span>
  
|<span data-ttu-id="77b5e-116">**Flag**</span><span class="sxs-lookup"><span data-stu-id="77b5e-116">**Flag**</span></span>|<span data-ttu-id="77b5e-117">**Значение**</span><span class="sxs-lookup"><span data-stu-id="77b5e-117">**Value**</span></span>|<span data-ttu-id="77b5e-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="77b5e-118">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="77b5e-119">HidePrivate</span><span class="sxs-lookup"><span data-stu-id="77b5e-119">HidePrivate</span></span>  <br/> |<span data-ttu-id="77b5e-120">0</span><span class="sxs-lookup"><span data-stu-id="77b5e-120">0</span></span>  <br/> |<span data-ttu-id="77b5e-121">Делегат не должны просматривать объекты личное сообщение.</span><span class="sxs-lookup"><span data-stu-id="77b5e-121">The delegate should not be allowed to view private message objects.</span></span>  <br/> |
|<span data-ttu-id="77b5e-122">ShowPrivate</span><span class="sxs-lookup"><span data-stu-id="77b5e-122">ShowPrivate</span></span>  <br/> |<span data-ttu-id="77b5e-123">1</span><span class="sxs-lookup"><span data-stu-id="77b5e-123">1</span></span>  <br/> |<span data-ttu-id="77b5e-124">Делегат должны просматривать объекты личное сообщение.</span><span class="sxs-lookup"><span data-stu-id="77b5e-124">The delegate should be allowed to view private message objects.</span></span>  <br/> |
   
<span data-ttu-id="77b5e-125">Это свойство необходимо установить в объекте сведения делегата.</span><span class="sxs-lookup"><span data-stu-id="77b5e-125">This property must be set in the delegate information object.</span></span> <span data-ttu-id="77b5e-126">Значение «ShowPrivate» указывает, что представитель сделайте видимым объекты личное сообщение.</span><span class="sxs-lookup"><span data-stu-id="77b5e-126">The value of "ShowPrivate" indicates that the delegator wants to make private message objects visible.</span></span> <span data-ttu-id="77b5e-127">Этот параметр применяется ко всем папкам, для которых делегат имеет роль проверяющего, автор или редактора.</span><span class="sxs-lookup"><span data-stu-id="77b5e-127">This preference is applicable to all folders for which the delegate has a role of reviewer, author, or editor.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="77b5e-128">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="77b5e-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="77b5e-129">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="77b5e-129">Protocol specifications</span></span>

<span data-ttu-id="77b5e-130">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="77b5e-130">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="77b5e-131">Указывает методы для подключений и настройки почтовых ящиков как делегаты и взаимодействия с объектами сообщений и календаря, когда они действовать от имени другого пользователя.</span><span class="sxs-lookup"><span data-stu-id="77b5e-131">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="77b5e-132">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="77b5e-132">Header files</span></span>

<span data-ttu-id="77b5e-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="77b5e-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="77b5e-134">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="77b5e-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="77b5e-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="77b5e-135">Mapitags.h</span></span>
  
> <span data-ttu-id="77b5e-136">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="77b5e-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="77b5e-137">См. также</span><span class="sxs-lookup"><span data-stu-id="77b5e-137">See also</span></span>



[<span data-ttu-id="77b5e-138">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="77b5e-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="77b5e-139">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="77b5e-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="77b5e-140">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="77b5e-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="77b5e-141">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="77b5e-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

