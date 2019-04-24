---
title: Иаблогонопенстатусентри
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349023"
---
# <a name="iablogonopenstatusentry"></a><span data-ttu-id="9c532-103">IABLogon::OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="9c532-103">IABLogon::OpenStatusEntry</span></span>

  
  
<span data-ttu-id="9c532-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9c532-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9c532-105">Открывает объект Status поставщика.</span><span class="sxs-lookup"><span data-stu-id="9c532-105">Opens the provider's status object.</span></span>
  
```cpp
HRESULT OpenStatusEntry(
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPMAPISTATUS FAR * lppEntry
);
```

## <a name="parameters"></a><span data-ttu-id="9c532-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9c532-106">Parameters</span></span>

 <span data-ttu-id="9c532-107">_Лпинтерфаце_</span><span class="sxs-lookup"><span data-stu-id="9c532-107">_lpInterface_</span></span>
  
> <span data-ttu-id="9c532-108">возврата Указатель на идентификатор интерфейса (IID), представляющий интерфейс, который должен использоваться для доступа к объекту Status.</span><span class="sxs-lookup"><span data-stu-id="9c532-108">[in] A pointer to the interface identifier (IID) that represents the interface that must be used to access the status object.</span></span> <span data-ttu-id="9c532-109">При передаче значения NULL возвращается стандартный интерфейс объекта [имапистатус: IMAPIProp](imapistatusimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="9c532-109">Passing NULL returns the object's standard interface, [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md).</span></span>
    
 <span data-ttu-id="9c532-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9c532-110">_ulFlags_</span></span>
  
> <span data-ttu-id="9c532-111">возврата Битовая маска флагов, которые управляют способом открытия объекта Status.</span><span class="sxs-lookup"><span data-stu-id="9c532-111">[in] A bitmask of flags that controls how the status object is opened.</span></span> <span data-ttu-id="9c532-112">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="9c532-112">The following flag can be set:</span></span>
    
<span data-ttu-id="9c532-113">МАПИ_МОДИФИ</span><span class="sxs-lookup"><span data-stu-id="9c532-113">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="9c532-114">ЗаПрашивает разрешение на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="9c532-114">Requests read/write permission.</span></span> <span data-ttu-id="9c532-115">По умолчанию объекты открываются с доступом только для чтения, а абоненты не должны предполагать, что предоставлено разрешение на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="9c532-115">By default, objects are opened with read-only access, and callers should not assume that read/write permission has been granted.</span></span>
    
 <span data-ttu-id="9c532-116">_Лпулобжтипе_</span><span class="sxs-lookup"><span data-stu-id="9c532-116">_lpulObjType_</span></span>
  
> <span data-ttu-id="9c532-117">вышли Указатель на тип открытого объекта.</span><span class="sxs-lookup"><span data-stu-id="9c532-117">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="9c532-118">_Лппентри_</span><span class="sxs-lookup"><span data-stu-id="9c532-118">_lppEntry_</span></span>
  
> <span data-ttu-id="9c532-119">вышли Указатель на указатель на открытый объект.</span><span class="sxs-lookup"><span data-stu-id="9c532-119">[out] A pointer to a pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9c532-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9c532-120">Return value</span></span>

<span data-ttu-id="9c532-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="9c532-121">S_OK</span></span> 
  
> <span data-ttu-id="9c532-122">Вызов выполнен успешно и открыт объект Status.</span><span class="sxs-lookup"><span data-stu-id="9c532-122">The call succeeded and the status object has been opened.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9c532-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="9c532-123">Remarks</span></span>

<span data-ttu-id="9c532-124">Поставщики адресных книг реализуют метод **опенстатусентри** , чтобы предоставить доступ к объекту своего состояния.</span><span class="sxs-lookup"><span data-stu-id="9c532-124">Address book providers implement the **OpenStatusEntry** method to grant access to their status object.</span></span> <span data-ttu-id="9c532-125">Все поставщики адресных книг необходимы для реализации объекта status, который поддерживает, по крайней мере, метод [имапистатус:: валидатестате](imapistatus-validatestate.md) .</span><span class="sxs-lookup"><span data-stu-id="9c532-125">All address book providers are required to implement a status object that supports, at a minimum, the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method.</span></span> <span data-ttu-id="9c532-126">Дополнительные сведения: [Реализация объекта Status](status-object-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="9c532-126">For more information, see [Status Object Implementation](status-object-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9c532-127">См. также</span><span class="sxs-lookup"><span data-stu-id="9c532-127">See also</span></span>



[<span data-ttu-id="9c532-128">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="9c532-128">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)
  
[<span data-ttu-id="9c532-129">IMAPIStatus::SettingsDialog</span><span class="sxs-lookup"><span data-stu-id="9c532-129">IMAPIStatus::SettingsDialog</span></span>](imapistatus-settingsdialog.md)
  
[<span data-ttu-id="9c532-130">IMAPIStatus::ValidateState</span><span class="sxs-lookup"><span data-stu-id="9c532-130">IMAPIStatus::ValidateState</span></span>](imapistatus-validatestate.md)
  
[<span data-ttu-id="9c532-131">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9c532-131">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

