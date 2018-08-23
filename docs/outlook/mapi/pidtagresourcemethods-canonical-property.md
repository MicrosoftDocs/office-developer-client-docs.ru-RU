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
ms.openlocfilehash: 2e1cff8148815c3e03b92e4d57d1c6a303943c9c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578166"
---
# <a name="pidtagresourcemethods-canonical-property"></a><span data-ttu-id="8d653-103">Каноническое свойство PidTagResourceMethods</span><span class="sxs-lookup"><span data-stu-id="8d653-103">PidTagResourceMethods Canonical Property</span></span>

  
  
<span data-ttu-id="8d653-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8d653-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8d653-105">Содержит битовую маску флагов, которые указывают методы в интерфейсе **IMAPIStatus** , поддерживаемых приложением объект состояния.</span><span class="sxs-lookup"><span data-stu-id="8d653-105">Contains a bitmask of flags that indicate the methods in the **IMAPIStatus** interface that are supported by the status object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8d653-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="8d653-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8d653-107">PR_RESOURCE_METHODS</span><span class="sxs-lookup"><span data-stu-id="8d653-107">PR_RESOURCE_METHODS</span></span>  <br/> |
|<span data-ttu-id="8d653-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="8d653-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8d653-109">0x3E02</span><span class="sxs-lookup"><span data-stu-id="8d653-109">0x3E02</span></span>  <br/> |
|<span data-ttu-id="8d653-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="8d653-110">Data type:</span></span>  <br/> |<span data-ttu-id="8d653-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="8d653-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="8d653-112">Область:</span><span class="sxs-lookup"><span data-stu-id="8d653-112">Area:</span></span>  <br/> |<span data-ttu-id="8d653-113">Состояние MAPI</span><span class="sxs-lookup"><span data-stu-id="8d653-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8d653-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="8d653-114">Remarks</span></span>

<span data-ttu-id="8d653-115">Это свойство указывает, какой из методов в реализации объектом состояние **IMAPIStatus** поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="8d653-115">This property indicates which of the methods in a status object's implementation of **IMAPIStatus** are supported.</span></span> <span data-ttu-id="8d653-116">Объекты состояния могут возвращать MAPI_E_NO_SUPPORT из методов не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8d653-116">Status objects are allowed to return MAPI_E_NO_SUPPORT from unsupported methods.</span></span> 
  
<span data-ttu-id="8d653-117">Клиенты используют свойство **PR_RESOURCE_METHODS** объекта состояния во избежание вызов методов не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8d653-117">Clients use a status object's **PR_RESOURCE_METHODS** property to avoid making calls to unsupported methods.</span></span> <span data-ttu-id="8d653-118">Если установлен флаг, соответствующий определенного метода, метод существует и могут вызываться.</span><span class="sxs-lookup"><span data-stu-id="8d653-118">If the flag that corresponds to a particular method is set, the method exists and can be called.</span></span> <span data-ttu-id="8d653-119">Если этот флажок снят, метод не должен вызываться.</span><span class="sxs-lookup"><span data-stu-id="8d653-119">If that flag is clear, the method should not be called.</span></span> 
  
<span data-ttu-id="8d653-120">Объекты состояния реализован MAPI поддержки следующих методов:</span><span class="sxs-lookup"><span data-stu-id="8d653-120">The status objects implemented by MAPI support the following methods:</span></span>
  
|<span data-ttu-id="8d653-121">**Состояние объекта**</span><span class="sxs-lookup"><span data-stu-id="8d653-121">**Status object**</span></span>|<span data-ttu-id="8d653-122">**Поддерживаемые методы**</span><span class="sxs-lookup"><span data-stu-id="8d653-122">**Supported methods**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8d653-123">Подсистема MAPI</span><span class="sxs-lookup"><span data-stu-id="8d653-123">MAPI subsystem</span></span>  <br/> |<span data-ttu-id="8d653-124">Только **ValidateState**</span><span class="sxs-lookup"><span data-stu-id="8d653-124">**ValidateState** only</span></span>  <br/> |
|<span data-ttu-id="8d653-125">Адресная книга MAPI</span><span class="sxs-lookup"><span data-stu-id="8d653-125">MAPI address book</span></span>  <br/> |<span data-ttu-id="8d653-126">Только **ValidateState**</span><span class="sxs-lookup"><span data-stu-id="8d653-126">**ValidateState** only</span></span>  <br/> |
|<span data-ttu-id="8d653-127">Диспетчер очереди MAPI</span><span class="sxs-lookup"><span data-stu-id="8d653-127">MAPI spooler</span></span>  <br/> |<span data-ttu-id="8d653-128">**ValidateState** и **FlushQueues**</span><span class="sxs-lookup"><span data-stu-id="8d653-128">**ValidateState** and **FlushQueues**</span></span> <br/> |
   
<span data-ttu-id="8d653-129">Один или несколько из следующих флагов может быть установлено в **PR_RESOURCE_METHODS**:</span><span class="sxs-lookup"><span data-stu-id="8d653-129">One or more of the following flags can be set in **PR_RESOURCE_METHODS**:</span></span>
  
<span data-ttu-id="8d653-130">STATUS_CHANGE_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="8d653-130">STATUS_CHANGE_PASSWORD</span></span> 
  
> <span data-ttu-id="8d653-131">Указывает, что поддерживается метод [IMAPIStatus::ChangePassword](imapistatus-changepassword.md) .</span><span class="sxs-lookup"><span data-stu-id="8d653-131">Indicates that the [IMAPIStatus::ChangePassword](imapistatus-changepassword.md) method is supported.</span></span> 
    
<span data-ttu-id="8d653-132">STATUS_FLUSH_QUEUES</span><span class="sxs-lookup"><span data-stu-id="8d653-132">STATUS_FLUSH_QUEUES</span></span> 
  
> <span data-ttu-id="8d653-133">Указывает, что поддерживается метод [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) .</span><span class="sxs-lookup"><span data-stu-id="8d653-133">Indicates that the [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) method is supported.</span></span> 
    
<span data-ttu-id="8d653-134">STATUS_SETTINGS_DIALOG</span><span class="sxs-lookup"><span data-stu-id="8d653-134">STATUS_SETTINGS_DIALOG</span></span> 
  
> <span data-ttu-id="8d653-135">Указывает, что поддерживается метод [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) .</span><span class="sxs-lookup"><span data-stu-id="8d653-135">Indicates that the [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method is supported.</span></span> 
    
<span data-ttu-id="8d653-136">STATUS_VALIDATE_STATE</span><span class="sxs-lookup"><span data-stu-id="8d653-136">STATUS_VALIDATE_STATE</span></span> 
  
> <span data-ttu-id="8d653-137">Указывает, что поддерживается метод [IMAPIStatus::ValidateState](imapistatus-validatestate.md) .</span><span class="sxs-lookup"><span data-stu-id="8d653-137">Indicates that the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method is supported.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="8d653-138">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="8d653-138">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="8d653-139">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="8d653-139">Header files</span></span>

<span data-ttu-id="8d653-140">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8d653-140">Mapidefs.h</span></span>
  
> <span data-ttu-id="8d653-141">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="8d653-141">Provides data type definitions.</span></span>
    
<span data-ttu-id="8d653-142">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8d653-142">Mapitags.h</span></span>
  
> <span data-ttu-id="8d653-143">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="8d653-143">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8d653-144">См. также</span><span class="sxs-lookup"><span data-stu-id="8d653-144">See also</span></span>



[<span data-ttu-id="8d653-145">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8d653-145">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8d653-146">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8d653-146">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8d653-147">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="8d653-147">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8d653-148">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="8d653-148">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

