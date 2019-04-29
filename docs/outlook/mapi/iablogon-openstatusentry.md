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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410786"
---
# <a name="iablogonopenstatusentry"></a><span data-ttu-id="cf191-103">IABLogon::OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="cf191-103">IABLogon::OpenStatusEntry</span></span>

  
  
<span data-ttu-id="cf191-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cf191-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cf191-105">Открывает объект Status поставщика.</span><span class="sxs-lookup"><span data-stu-id="cf191-105">Opens the provider's status object.</span></span>
  
```cpp
HRESULT OpenStatusEntry(
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPMAPISTATUS FAR * lppEntry
);
```

## <a name="parameters"></a><span data-ttu-id="cf191-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cf191-106">Parameters</span></span>

 <span data-ttu-id="cf191-107">_Лпинтерфаце_</span><span class="sxs-lookup"><span data-stu-id="cf191-107">_lpInterface_</span></span>
  
> <span data-ttu-id="cf191-108">возврата Указатель на идентификатор интерфейса (IID), представляющий интерфейс, который должен использоваться для доступа к объекту Status.</span><span class="sxs-lookup"><span data-stu-id="cf191-108">[in] A pointer to the interface identifier (IID) that represents the interface that must be used to access the status object.</span></span> <span data-ttu-id="cf191-109">При передаче значения NULL возвращается стандартный интерфейс объекта [имапистатус: IMAPIProp](imapistatusimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="cf191-109">Passing NULL returns the object's standard interface, [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md).</span></span>
    
 <span data-ttu-id="cf191-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="cf191-110">_ulFlags_</span></span>
  
> <span data-ttu-id="cf191-111">возврата Битовая маска флагов, которые управляют способом открытия объекта Status.</span><span class="sxs-lookup"><span data-stu-id="cf191-111">[in] A bitmask of flags that controls how the status object is opened.</span></span> <span data-ttu-id="cf191-112">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="cf191-112">The following flag can be set:</span></span>
    
<span data-ttu-id="cf191-113">МАПИ_МОДИФИ</span><span class="sxs-lookup"><span data-stu-id="cf191-113">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="cf191-114">ЗаПрашивает разрешение на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="cf191-114">Requests read/write permission.</span></span> <span data-ttu-id="cf191-115">По умолчанию объекты открываются с доступом только для чтения, а абоненты не должны предполагать, что предоставлено разрешение на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="cf191-115">By default, objects are opened with read-only access, and callers should not assume that read/write permission has been granted.</span></span>
    
 <span data-ttu-id="cf191-116">_Лпулобжтипе_</span><span class="sxs-lookup"><span data-stu-id="cf191-116">_lpulObjType_</span></span>
  
> <span data-ttu-id="cf191-117">вышли Указатель на тип открытого объекта.</span><span class="sxs-lookup"><span data-stu-id="cf191-117">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="cf191-118">_Лппентри_</span><span class="sxs-lookup"><span data-stu-id="cf191-118">_lppEntry_</span></span>
  
> <span data-ttu-id="cf191-119">вышли Указатель на указатель на открытый объект.</span><span class="sxs-lookup"><span data-stu-id="cf191-119">[out] A pointer to a pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="cf191-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cf191-120">Return value</span></span>

<span data-ttu-id="cf191-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="cf191-121">S_OK</span></span> 
  
> <span data-ttu-id="cf191-122">Вызов выполнен успешно и открыт объект Status.</span><span class="sxs-lookup"><span data-stu-id="cf191-122">The call succeeded and the status object has been opened.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cf191-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="cf191-123">Remarks</span></span>

<span data-ttu-id="cf191-124">Поставщики адресных книг реализуют метод **опенстатусентри** , чтобы предоставить доступ к объекту своего состояния.</span><span class="sxs-lookup"><span data-stu-id="cf191-124">Address book providers implement the **OpenStatusEntry** method to grant access to their status object.</span></span> <span data-ttu-id="cf191-125">Все поставщики адресных книг необходимы для реализации объекта status, который поддерживает, по крайней мере, метод [имапистатус:: валидатестате](imapistatus-validatestate.md) .</span><span class="sxs-lookup"><span data-stu-id="cf191-125">All address book providers are required to implement a status object that supports, at a minimum, the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method.</span></span> <span data-ttu-id="cf191-126">Дополнительные сведения: [Реализация объекта Status](status-object-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="cf191-126">For more information, see [Status Object Implementation](status-object-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cf191-127">См. также</span><span class="sxs-lookup"><span data-stu-id="cf191-127">See also</span></span>



[<span data-ttu-id="cf191-128">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="cf191-128">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)
  
[<span data-ttu-id="cf191-129">IMAPIStatus::SettingsDialog</span><span class="sxs-lookup"><span data-stu-id="cf191-129">IMAPIStatus::SettingsDialog</span></span>](imapistatus-settingsdialog.md)
  
[<span data-ttu-id="cf191-130">IMAPIStatus::ValidateState</span><span class="sxs-lookup"><span data-stu-id="cf191-130">IMAPIStatus::ValidateState</span></span>](imapistatus-validatestate.md)
  
[<span data-ttu-id="cf191-131">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cf191-131">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

