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
# <a name="iablogonopenstatusentry"></a><span data-ttu-id="cf5f4-103">IABLogon::OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="cf5f4-103">IABLogon::OpenStatusEntry</span></span>

  
  
<span data-ttu-id="cf5f4-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cf5f4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cf5f4-105">Открывает объект состояния поставщика.</span><span class="sxs-lookup"><span data-stu-id="cf5f4-105">Opens the provider's status object.</span></span>
  
```cpp
HRESULT OpenStatusEntry(
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPMAPISTATUS FAR * lppEntry
);
```

## <a name="parameters"></a><span data-ttu-id="cf5f4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cf5f4-106">Parameters</span></span>

 <span data-ttu-id="cf5f4-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="cf5f4-107">_lpInterface_</span></span>
  
> <span data-ttu-id="cf5f4-108">[in] Указатель на идентификатор интерфейса ( IID), который представляет интерфейс, который должен использоваться для доступа к объекту состояния.</span><span class="sxs-lookup"><span data-stu-id="cf5f4-108">[in] A pointer to the interface identifier (IID) that represents the interface that must be used to access the status object.</span></span> <span data-ttu-id="cf5f4-109">Передача NULL возвращает стандартный интерфейс [объекта, IMAPIStatus : IMAPIProp](imapistatusimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="cf5f4-109">Passing NULL returns the object's standard interface, [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md).</span></span>
    
 <span data-ttu-id="cf5f4-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="cf5f4-110">_ulFlags_</span></span>
  
> <span data-ttu-id="cf5f4-111">[in] Битоваяmas флагов, которая управляет открытием объекта состояния.</span><span class="sxs-lookup"><span data-stu-id="cf5f4-111">[in] A bitmask of flags that controls how the status object is opened.</span></span> <span data-ttu-id="cf5f4-112">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="cf5f4-112">The following flag can be set:</span></span>
    
<span data-ttu-id="cf5f4-113">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="cf5f4-113">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="cf5f4-114">Запрашивает разрешение на чтение и записи.</span><span class="sxs-lookup"><span data-stu-id="cf5f4-114">Requests read/write permission.</span></span> <span data-ttu-id="cf5f4-115">По умолчанию объекты открываются с доступом только для чтения, и вызывающим не следует предполагать, что разрешение на чтение и записи предоставлено.</span><span class="sxs-lookup"><span data-stu-id="cf5f4-115">By default, objects are opened with read-only access, and callers should not assume that read/write permission has been granted.</span></span>
    
 <span data-ttu-id="cf5f4-116">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="cf5f4-116">_lpulObjType_</span></span>
  
> <span data-ttu-id="cf5f4-117">[out] Указатель на тип открытого объекта.</span><span class="sxs-lookup"><span data-stu-id="cf5f4-117">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="cf5f4-118">_lppEntry_</span><span class="sxs-lookup"><span data-stu-id="cf5f4-118">_lppEntry_</span></span>
  
> <span data-ttu-id="cf5f4-119">[out] Указатель на указатель на открытый объект.</span><span class="sxs-lookup"><span data-stu-id="cf5f4-119">[out] A pointer to a pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="cf5f4-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cf5f4-120">Return value</span></span>

<span data-ttu-id="cf5f4-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="cf5f4-121">S_OK</span></span> 
  
> <span data-ttu-id="cf5f4-122">Вызов был успешным, и был открыт объект status.</span><span class="sxs-lookup"><span data-stu-id="cf5f4-122">The call succeeded and the status object has been opened.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cf5f4-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="cf5f4-123">Remarks</span></span>

<span data-ttu-id="cf5f4-124">Поставщики адресных книг реализуют метод **OpenStatusEntry,** чтобы предоставить доступ к их объекту состояния.</span><span class="sxs-lookup"><span data-stu-id="cf5f4-124">Address book providers implement the **OpenStatusEntry** method to grant access to their status object.</span></span> <span data-ttu-id="cf5f4-125">Все поставщики адресных книг необходимы для реализации объекта состояния, который поддерживает как минимум метод [IMAPIStatus::ValidateState.](imapistatus-validatestate.md)</span><span class="sxs-lookup"><span data-stu-id="cf5f4-125">All address book providers are required to implement a status object that supports, at a minimum, the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method.</span></span> <span data-ttu-id="cf5f4-126">Дополнительные сведения см. в [реализации объекта status.](status-object-implementation.md)</span><span class="sxs-lookup"><span data-stu-id="cf5f4-126">For more information, see [Status Object Implementation](status-object-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cf5f4-127">См. также</span><span class="sxs-lookup"><span data-stu-id="cf5f4-127">See also</span></span>



[<span data-ttu-id="cf5f4-128">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="cf5f4-128">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)
  
[<span data-ttu-id="cf5f4-129">IMAPIStatus::SettingsDialog</span><span class="sxs-lookup"><span data-stu-id="cf5f4-129">IMAPIStatus::SettingsDialog</span></span>](imapistatus-settingsdialog.md)
  
[<span data-ttu-id="cf5f4-130">IMAPIStatus::ValidateState</span><span class="sxs-lookup"><span data-stu-id="cf5f4-130">IMAPIStatus::ValidateState</span></span>](imapistatus-validatestate.md)
  
[<span data-ttu-id="cf5f4-131">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cf5f4-131">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

