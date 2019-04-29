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
# <a name="pidtagresourcemethods-canonical-property"></a><span data-ttu-id="77ca8-103">Каноническое свойство PidTagResourceMethods</span><span class="sxs-lookup"><span data-stu-id="77ca8-103">PidTagResourceMethods Canonical Property</span></span>

  
  
<span data-ttu-id="77ca8-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="77ca8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="77ca8-105">Содержит битовую маску флагов, указывающих методы в интерфейсе **имапистатус** , поддерживаемые объектом Status.</span><span class="sxs-lookup"><span data-stu-id="77ca8-105">Contains a bitmask of flags that indicate the methods in the **IMAPIStatus** interface that are supported by the status object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="77ca8-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="77ca8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="77ca8-107">ПР_РЕСАУРЦЕ_МЕСОДС</span><span class="sxs-lookup"><span data-stu-id="77ca8-107">PR_RESOURCE_METHODS</span></span>  <br/> |
|<span data-ttu-id="77ca8-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="77ca8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="77ca8-109">0x3E02</span><span class="sxs-lookup"><span data-stu-id="77ca8-109">0x3E02</span></span>  <br/> |
|<span data-ttu-id="77ca8-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="77ca8-110">Data type:</span></span>  <br/> |<span data-ttu-id="77ca8-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="77ca8-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="77ca8-112">Область:</span><span class="sxs-lookup"><span data-stu-id="77ca8-112">Area:</span></span>  <br/> |<span data-ttu-id="77ca8-113">Состояние MAPI</span><span class="sxs-lookup"><span data-stu-id="77ca8-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="77ca8-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="77ca8-114">Remarks</span></span>

<span data-ttu-id="77ca8-115">Это свойство указывает, какие методы в реализации объекта Status поддерживаются в **имапистатус** .</span><span class="sxs-lookup"><span data-stu-id="77ca8-115">This property indicates which of the methods in a status object's implementation of **IMAPIStatus** are supported.</span></span> <span data-ttu-id="77ca8-116">Объектам состояния разрешено возвращать МАПИ_Е_НО_СУППОРТ из неподдерживаемых методов.</span><span class="sxs-lookup"><span data-stu-id="77ca8-116">Status objects are allowed to return MAPI_E_NO_SUPPORT from unsupported methods.</span></span> 
  
<span data-ttu-id="77ca8-117">Клиенты используют свойство **пр_ресаурце_месодс** объекта status, чтобы избежать вызовов неподдерживаемых методов.</span><span class="sxs-lookup"><span data-stu-id="77ca8-117">Clients use a status object's **PR_RESOURCE_METHODS** property to avoid making calls to unsupported methods.</span></span> <span data-ttu-id="77ca8-118">Если установлен флаг, соответствующий определенному методу, метод существует и может вызываться.</span><span class="sxs-lookup"><span data-stu-id="77ca8-118">If the flag that corresponds to a particular method is set, the method exists and can be called.</span></span> <span data-ttu-id="77ca8-119">Если этот флаг снят, метод не должен вызываться.</span><span class="sxs-lookup"><span data-stu-id="77ca8-119">If that flag is clear, the method should not be called.</span></span> 
  
<span data-ttu-id="77ca8-120">Объекты состояния, реализованные MAPI, поддерживают следующие методы:</span><span class="sxs-lookup"><span data-stu-id="77ca8-120">The status objects implemented by MAPI support the following methods:</span></span>
  
|<span data-ttu-id="77ca8-121">**Объект Status**</span><span class="sxs-lookup"><span data-stu-id="77ca8-121">**Status object**</span></span>|<span data-ttu-id="77ca8-122">**Поддерживаемые методы**</span><span class="sxs-lookup"><span data-stu-id="77ca8-122">**Supported methods**</span></span>|
|:-----|:-----|
|<span data-ttu-id="77ca8-123">Подсистема MAPI</span><span class="sxs-lookup"><span data-stu-id="77ca8-123">MAPI subsystem</span></span>  <br/> |<span data-ttu-id="77ca8-124">Только **валидатестате**</span><span class="sxs-lookup"><span data-stu-id="77ca8-124">**ValidateState** only</span></span>  <br/> |
|<span data-ttu-id="77ca8-125">Адресная книга MAPI</span><span class="sxs-lookup"><span data-stu-id="77ca8-125">MAPI address book</span></span>  <br/> |<span data-ttu-id="77ca8-126">Только **валидатестате**</span><span class="sxs-lookup"><span data-stu-id="77ca8-126">**ValidateState** only</span></span>  <br/> |
|<span data-ttu-id="77ca8-127">Диспетчер очереди MAPI</span><span class="sxs-lookup"><span data-stu-id="77ca8-127">MAPI spooler</span></span>  <br/> |<span data-ttu-id="77ca8-128">**Валидатестате** и **FlushQueues**</span><span class="sxs-lookup"><span data-stu-id="77ca8-128">**ValidateState** and **FlushQueues**</span></span> <br/> |
   
<span data-ttu-id="77ca8-129">В **пр_ресаурце_месодс**можно задать один или несколько из следующих флагов:</span><span class="sxs-lookup"><span data-stu-id="77ca8-129">One or more of the following flags can be set in **PR_RESOURCE_METHODS**:</span></span>
  
<span data-ttu-id="77ca8-130">СТАТУС_ЧАНЖЕ_ПАССВОРД</span><span class="sxs-lookup"><span data-stu-id="77ca8-130">STATUS_CHANGE_PASSWORD</span></span> 
  
> <span data-ttu-id="77ca8-131">Указывает на то, что метод [имапистатус:: ChangePassword](imapistatus-changepassword.md) поддерживается.</span><span class="sxs-lookup"><span data-stu-id="77ca8-131">Indicates that the [IMAPIStatus::ChangePassword](imapistatus-changepassword.md) method is supported.</span></span> 
    
<span data-ttu-id="77ca8-132">СТАТУС_ФЛУШ_КУЕУЕС</span><span class="sxs-lookup"><span data-stu-id="77ca8-132">STATUS_FLUSH_QUEUES</span></span> 
  
> <span data-ttu-id="77ca8-133">Указывает, что поддерживается метод [имапистатус:: FlushQueues](imapistatus-flushqueues.md) .</span><span class="sxs-lookup"><span data-stu-id="77ca8-133">Indicates that the [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) method is supported.</span></span> 
    
<span data-ttu-id="77ca8-134">СТАТУС_СЕТТИНГС_ДИАЛОГ</span><span class="sxs-lookup"><span data-stu-id="77ca8-134">STATUS_SETTINGS_DIALOG</span></span> 
  
> <span data-ttu-id="77ca8-135">Указывает, что поддерживается метод [имапистатус:: сеттингсдиалог](imapistatus-settingsdialog.md) .</span><span class="sxs-lookup"><span data-stu-id="77ca8-135">Indicates that the [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method is supported.</span></span> 
    
<span data-ttu-id="77ca8-136">СТАТУС_ВАЛИДАТЕ_СТАТЕ</span><span class="sxs-lookup"><span data-stu-id="77ca8-136">STATUS_VALIDATE_STATE</span></span> 
  
> <span data-ttu-id="77ca8-137">Указывает, что поддерживается метод [имапистатус:: валидатестате](imapistatus-validatestate.md) .</span><span class="sxs-lookup"><span data-stu-id="77ca8-137">Indicates that the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method is supported.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="77ca8-138">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="77ca8-138">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="77ca8-139">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="77ca8-139">Header files</span></span>

<span data-ttu-id="77ca8-140">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="77ca8-140">Mapidefs.h</span></span>
  
> <span data-ttu-id="77ca8-141">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="77ca8-141">Provides data type definitions.</span></span>
    
<span data-ttu-id="77ca8-142">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="77ca8-142">Mapitags.h</span></span>
  
> <span data-ttu-id="77ca8-143">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="77ca8-143">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="77ca8-144">См. также</span><span class="sxs-lookup"><span data-stu-id="77ca8-144">See also</span></span>



[<span data-ttu-id="77ca8-145">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="77ca8-145">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="77ca8-146">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="77ca8-146">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="77ca8-147">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="77ca8-147">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="77ca8-148">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="77ca8-148">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

