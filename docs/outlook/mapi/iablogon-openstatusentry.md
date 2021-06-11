---
title: IABLogonOpenStatusEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.OpenStatusEntry
api_type:
- COM
ms.assetid: 66f1e246-a67a-4f8a-ae3a-6a8ec8c2b367
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 22f98e52444b17c383737bffd1685df0fb7ba8bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410786"
---
# <a name="iablogonopenstatusentry"></a><span data-ttu-id="f515e-103">IABLogon::OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="f515e-103">IABLogon::OpenStatusEntry</span></span>

  
  
<span data-ttu-id="f515e-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f515e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f515e-105">Открывает объект состояния поставщика.</span><span class="sxs-lookup"><span data-stu-id="f515e-105">Opens the provider's status object.</span></span>
  
```cpp
HRESULT OpenStatusEntry(
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPMAPISTATUS FAR * lppEntry
);
```

## <a name="parameters"></a><span data-ttu-id="f515e-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="f515e-106">Parameters</span></span>

 <span data-ttu-id="f515e-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="f515e-107">_lpInterface_</span></span>
  
> <span data-ttu-id="f515e-108">[in] Указатель на идентификатор интерфейса (IID), который представляет интерфейс, который должен использоваться для доступа к объекту состояния.</span><span class="sxs-lookup"><span data-stu-id="f515e-108">[in] A pointer to the interface identifier (IID) that represents the interface that must be used to access the status object.</span></span> <span data-ttu-id="f515e-109">Передача NULL возвращает стандартный интерфейс [объекта IMAPIStatus : IMAPIProp](imapistatusimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="f515e-109">Passing NULL returns the object's standard interface, [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md).</span></span>
    
 <span data-ttu-id="f515e-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f515e-110">_ulFlags_</span></span>
  
> <span data-ttu-id="f515e-111">[in] Битмашка флагов, контролируемая тем, как открывается объект состояния.</span><span class="sxs-lookup"><span data-stu-id="f515e-111">[in] A bitmask of flags that controls how the status object is opened.</span></span> <span data-ttu-id="f515e-112">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="f515e-112">The following flag can be set:</span></span>
    
<span data-ttu-id="f515e-113">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="f515e-113">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="f515e-114">Запросы на чтение и написание разрешений.</span><span class="sxs-lookup"><span data-stu-id="f515e-114">Requests read/write permission.</span></span> <span data-ttu-id="f515e-115">По умолчанию объекты открываются с доступом только для чтения, и звонителям не следует предполагать, что разрешение на чтение и записи было предоставлено.</span><span class="sxs-lookup"><span data-stu-id="f515e-115">By default, objects are opened with read-only access, and callers should not assume that read/write permission has been granted.</span></span>
    
 <span data-ttu-id="f515e-116">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="f515e-116">_lpulObjType_</span></span>
  
> <span data-ttu-id="f515e-117">[вышел] Указатель на тип открываемого объекта.</span><span class="sxs-lookup"><span data-stu-id="f515e-117">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="f515e-118">_lppEntry_</span><span class="sxs-lookup"><span data-stu-id="f515e-118">_lppEntry_</span></span>
  
> <span data-ttu-id="f515e-119">[вышел] Указатель на указатель на открытый объект.</span><span class="sxs-lookup"><span data-stu-id="f515e-119">[out] A pointer to a pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f515e-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f515e-120">Return value</span></span>

<span data-ttu-id="f515e-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="f515e-121">S_OK</span></span> 
  
> <span data-ttu-id="f515e-122">Вызов удался, и объект состояния был открыт.</span><span class="sxs-lookup"><span data-stu-id="f515e-122">The call succeeded and the status object has been opened.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f515e-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="f515e-123">Remarks</span></span>

<span data-ttu-id="f515e-124">Поставщики адресных книг реализуют **метод OpenStatusEntry** для предоставления доступа к объекту состояния.</span><span class="sxs-lookup"><span data-stu-id="f515e-124">Address book providers implement the **OpenStatusEntry** method to grant access to their status object.</span></span> <span data-ttu-id="f515e-125">Все поставщики адресных книг должны реализовать объект состояния, который поддерживает как минимум метод [IMAPIStatus::ValidateState.](imapistatus-validatestate.md)</span><span class="sxs-lookup"><span data-stu-id="f515e-125">All address book providers are required to implement a status object that supports, at a minimum, the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method.</span></span> <span data-ttu-id="f515e-126">Дополнительные сведения см. в [дополнительных сведениях о реализации объектов status.](status-object-implementation.md)</span><span class="sxs-lookup"><span data-stu-id="f515e-126">For more information, see [Status Object Implementation](status-object-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f515e-127">См. также</span><span class="sxs-lookup"><span data-stu-id="f515e-127">See also</span></span>



[<span data-ttu-id="f515e-128">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="f515e-128">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)
  
[<span data-ttu-id="f515e-129">IMAPIStatus::SettingsDialog</span><span class="sxs-lookup"><span data-stu-id="f515e-129">IMAPIStatus::SettingsDialog</span></span>](imapistatus-settingsdialog.md)
  
[<span data-ttu-id="f515e-130">IMAPIStatus::ValidateState</span><span class="sxs-lookup"><span data-stu-id="f515e-130">IMAPIStatus::ValidateState</span></span>](imapistatus-validatestate.md)
  
[<span data-ttu-id="f515e-131">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f515e-131">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

