---
title: Каноническое свойство PidTagResourceMethods
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResourceMethods
api_type:
- COM
ms.assetid: 60ebbcd5-b758-4c96-b8ec-089e0aae1a5f
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e9aee3280edbed60e97ef6e00e61f3086f6f07ce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436337"
---
# <a name="pidtagresourcemethods-canonical-property"></a><span data-ttu-id="5c27b-103">Каноническое свойство PidTagResourceMethods</span><span class="sxs-lookup"><span data-stu-id="5c27b-103">PidTagResourceMethods Canonical Property</span></span>

  
  
<span data-ttu-id="5c27b-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5c27b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5c27b-105">Содержит битмаску флагов, которые указывают методы в **интерфейсе IMAPIStatus,** поддерживаемые объектом состояния.</span><span class="sxs-lookup"><span data-stu-id="5c27b-105">Contains a bitmask of flags that indicate the methods in the **IMAPIStatus** interface that are supported by the status object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5c27b-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="5c27b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5c27b-107">PR_RESOURCE_METHODS</span><span class="sxs-lookup"><span data-stu-id="5c27b-107">PR_RESOURCE_METHODS</span></span>  <br/> |
|<span data-ttu-id="5c27b-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="5c27b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5c27b-109">0x3E02</span><span class="sxs-lookup"><span data-stu-id="5c27b-109">0x3E02</span></span>  <br/> |
|<span data-ttu-id="5c27b-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="5c27b-110">Data type:</span></span>  <br/> |<span data-ttu-id="5c27b-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="5c27b-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="5c27b-112">Область:</span><span class="sxs-lookup"><span data-stu-id="5c27b-112">Area:</span></span>  <br/> |<span data-ttu-id="5c27b-113">Состояние MAPI</span><span class="sxs-lookup"><span data-stu-id="5c27b-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5c27b-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="5c27b-114">Remarks</span></span>

<span data-ttu-id="5c27b-115">Это свойство указывает, какие из методов в реализации **объекта состояния IMAPIStatus** поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="5c27b-115">This property indicates which of the methods in a status object's implementation of **IMAPIStatus** are supported.</span></span> <span data-ttu-id="5c27b-116">Объектам status разрешено возвращать MAPI_E_NO_SUPPORT из неподтверченных методов.</span><span class="sxs-lookup"><span data-stu-id="5c27b-116">Status objects are allowed to return MAPI_E_NO_SUPPORT from unsupported methods.</span></span> 
  
<span data-ttu-id="5c27b-117">Клиенты используют свойство PR_RESOURCE_METHODS **объекта** состояния, чтобы не звонить на неподтверченные методы.</span><span class="sxs-lookup"><span data-stu-id="5c27b-117">Clients use a status object's **PR_RESOURCE_METHODS** property to avoid making calls to unsupported methods.</span></span> <span data-ttu-id="5c27b-118">Если заданной является флаг, соответствующий определенному методу, метод существует и может быть вызван.</span><span class="sxs-lookup"><span data-stu-id="5c27b-118">If the flag that corresponds to a particular method is set, the method exists and can be called.</span></span> <span data-ttu-id="5c27b-119">Если этот флаг понятен, метод не следует называть.</span><span class="sxs-lookup"><span data-stu-id="5c27b-119">If that flag is clear, the method should not be called.</span></span> 
  
<span data-ttu-id="5c27b-120">Объекты состояния, реализованные MAPI, поддерживают следующие методы:</span><span class="sxs-lookup"><span data-stu-id="5c27b-120">The status objects implemented by MAPI support the following methods:</span></span>
  
|<span data-ttu-id="5c27b-121">**Объект Status**</span><span class="sxs-lookup"><span data-stu-id="5c27b-121">**Status object**</span></span>|<span data-ttu-id="5c27b-122">**Поддерживаемые методы**</span><span class="sxs-lookup"><span data-stu-id="5c27b-122">**Supported methods**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5c27b-123">Подсистема MAPI</span><span class="sxs-lookup"><span data-stu-id="5c27b-123">MAPI subsystem</span></span>  <br/> |<span data-ttu-id="5c27b-124">**Только ValidateState**</span><span class="sxs-lookup"><span data-stu-id="5c27b-124">**ValidateState** only</span></span>  <br/> |
|<span data-ttu-id="5c27b-125">Адресная книга MAPI</span><span class="sxs-lookup"><span data-stu-id="5c27b-125">MAPI address book</span></span>  <br/> |<span data-ttu-id="5c27b-126">**Только ValidateState**</span><span class="sxs-lookup"><span data-stu-id="5c27b-126">**ValidateState** only</span></span>  <br/> |
|<span data-ttu-id="5c27b-127">Шпалер MAPI</span><span class="sxs-lookup"><span data-stu-id="5c27b-127">MAPI spooler</span></span>  <br/> |<span data-ttu-id="5c27b-128">**ValidateState** и **FlushQueues**</span><span class="sxs-lookup"><span data-stu-id="5c27b-128">**ValidateState** and **FlushQueues**</span></span> <br/> |
   
<span data-ttu-id="5c27b-129">Один или несколько из следующих флагов можно установить в **PR_RESOURCE_METHODS:**</span><span class="sxs-lookup"><span data-stu-id="5c27b-129">One or more of the following flags can be set in **PR_RESOURCE_METHODS**:</span></span>
  
<span data-ttu-id="5c27b-130">STATUS_CHANGE_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="5c27b-130">STATUS_CHANGE_PASSWORD</span></span> 
  
> <span data-ttu-id="5c27b-131">Указывает, что [метод IMAPIStatus::ChangePassword](imapistatus-changepassword.md) поддерживается.</span><span class="sxs-lookup"><span data-stu-id="5c27b-131">Indicates that the [IMAPIStatus::ChangePassword](imapistatus-changepassword.md) method is supported.</span></span> 
    
<span data-ttu-id="5c27b-132">STATUS_FLUSH_QUEUES</span><span class="sxs-lookup"><span data-stu-id="5c27b-132">STATUS_FLUSH_QUEUES</span></span> 
  
> <span data-ttu-id="5c27b-133">Указывает, что [метод IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) поддерживается.</span><span class="sxs-lookup"><span data-stu-id="5c27b-133">Indicates that the [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) method is supported.</span></span> 
    
<span data-ttu-id="5c27b-134">STATUS_SETTINGS_DIALOG</span><span class="sxs-lookup"><span data-stu-id="5c27b-134">STATUS_SETTINGS_DIALOG</span></span> 
  
> <span data-ttu-id="5c27b-135">Указывает, что [метод IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) поддерживается.</span><span class="sxs-lookup"><span data-stu-id="5c27b-135">Indicates that the [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method is supported.</span></span> 
    
<span data-ttu-id="5c27b-136">STATUS_VALIDATE_STATE</span><span class="sxs-lookup"><span data-stu-id="5c27b-136">STATUS_VALIDATE_STATE</span></span> 
  
> <span data-ttu-id="5c27b-137">Указывает, что [метод IMAPIStatus::ValidateState](imapistatus-validatestate.md) поддерживается.</span><span class="sxs-lookup"><span data-stu-id="5c27b-137">Indicates that the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method is supported.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="5c27b-138">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="5c27b-138">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="5c27b-139">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="5c27b-139">Header files</span></span>

<span data-ttu-id="5c27b-140">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5c27b-140">Mapidefs.h</span></span>
  
> <span data-ttu-id="5c27b-141">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="5c27b-141">Provides data type definitions.</span></span>
    
<span data-ttu-id="5c27b-142">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5c27b-142">Mapitags.h</span></span>
  
> <span data-ttu-id="5c27b-143">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="5c27b-143">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5c27b-144">См. также</span><span class="sxs-lookup"><span data-stu-id="5c27b-144">See also</span></span>



[<span data-ttu-id="5c27b-145">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="5c27b-145">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5c27b-146">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="5c27b-146">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5c27b-147">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="5c27b-147">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5c27b-148">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="5c27b-148">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

