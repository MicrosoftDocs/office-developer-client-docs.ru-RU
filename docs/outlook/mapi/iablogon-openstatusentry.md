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
ms.openlocfilehash: e693e1c3d6cb975a3a329e15c0b1a6d08817461a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808724"
---
# <a name="iablogonopenstatusentry"></a><span data-ttu-id="f83d2-103">IABLogon::OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="f83d2-103">IABLogon::OpenStatusEntry</span></span>

  
  
<span data-ttu-id="f83d2-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f83d2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f83d2-105">Открывает объект состояние поставщика.</span><span class="sxs-lookup"><span data-stu-id="f83d2-105">Opens the provider's status object.</span></span>
  
```cpp
HRESULT OpenStatusEntry(
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPMAPISTATUS FAR * lppEntry
);
```

## <a name="parameters"></a><span data-ttu-id="f83d2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f83d2-106">Parameters</span></span>

 <span data-ttu-id="f83d2-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="f83d2-107">_lpInterface_</span></span>
  
> <span data-ttu-id="f83d2-108">[in] Указатель на идентификатор интерфейса (ИД интерфейса), который представляет интерфейс, который должен использоваться для доступа к объекту состояния.</span><span class="sxs-lookup"><span data-stu-id="f83d2-108">[in] A pointer to the interface identifier (IID) that represents the interface that must be used to access the status object.</span></span> <span data-ttu-id="f83d2-109">Передача NULL возвращает объект стандартный интерфейс, [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="f83d2-109">Passing NULL returns the object's standard interface, [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md).</span></span>
    
 <span data-ttu-id="f83d2-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f83d2-110">_ulFlags_</span></span>
  
> <span data-ttu-id="f83d2-111">[in] Битовая маска флаги, который определяет способ открытия объекта состояния.</span><span class="sxs-lookup"><span data-stu-id="f83d2-111">[in] A bitmask of flags that controls how the status object is opened.</span></span> <span data-ttu-id="f83d2-112">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="f83d2-112">The following flag can be set:</span></span>
    
<span data-ttu-id="f83d2-113">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="f83d2-113">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="f83d2-114">Запросы на разрешение чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="f83d2-114">Requests read/write permission.</span></span> <span data-ttu-id="f83d2-115">По умолчанию объекты открываются с доступом только для чтения и абонентов не следует предполагать, что предоставлены разрешения на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="f83d2-115">By default, objects are opened with read-only access, and callers should not assume that read/write permission has been granted.</span></span>
    
 <span data-ttu-id="f83d2-116">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="f83d2-116">_lpulObjType_</span></span>
  
> <span data-ttu-id="f83d2-117">[out] Указатель на тип объекта открыт.</span><span class="sxs-lookup"><span data-stu-id="f83d2-117">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="f83d2-118">_lppEntry_</span><span class="sxs-lookup"><span data-stu-id="f83d2-118">_lppEntry_</span></span>
  
> <span data-ttu-id="f83d2-119">[out] Указатель на указатель на объект открыт.</span><span class="sxs-lookup"><span data-stu-id="f83d2-119">[out] A pointer to a pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f83d2-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0">Return value</span></span>

<span data-ttu-id="f83d2-121">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="f83d2-121">S_OK</span></span> 
  
> <span data-ttu-id="f83d2-122">Вызов завершился успешно и открытия объекта состояния.</span><span class="sxs-lookup"><span data-stu-id="f83d2-122">The call succeeded and the status object has been opened.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f83d2-123">Замечания</span><span class="sxs-lookup"><span data-stu-id="f83d2-123">Remarks</span></span>

<span data-ttu-id="f83d2-124">Метод **OpenStatusEntry** , чтобы предоставить доступ к их состояние объекта, реализуемые поставщиками адресных книг.</span><span class="sxs-lookup"><span data-stu-id="f83d2-124">Address book providers implement the **OpenStatusEntry** method to grant access to their status object.</span></span> <span data-ttu-id="f83d2-125">Все поставщиками адресной книги необходимы для реализации объект состояния, который поддерживает как минимум, метод [IMAPIStatus::ValidateState](imapistatus-validatestate.md) .</span><span class="sxs-lookup"><span data-stu-id="f83d2-125">All address book providers are required to implement a status object that supports, at a minimum, the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method.</span></span> <span data-ttu-id="f83d2-126">Для получения дополнительных сведений см [Реализация объекта состояния](status-object-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="f83d2-126">For more information, see [Status Object Implementation](status-object-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f83d2-127">См. также</span><span class="sxs-lookup"><span data-stu-id="f83d2-127">See also</span></span>



[<span data-ttu-id="f83d2-128">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="f83d2-128">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)
  
[<span data-ttu-id="f83d2-129">IMAPIStatus::SettingsDialog</span><span class="sxs-lookup"><span data-stu-id="f83d2-129">IMAPIStatus::SettingsDialog</span></span>](imapistatus-settingsdialog.md)
  
[<span data-ttu-id="f83d2-130">IMAPIStatus::ValidateState</span><span class="sxs-lookup"><span data-stu-id="f83d2-130">IMAPIStatus::ValidateState</span></span>](imapistatus-validatestate.md)
  
[<span data-ttu-id="f83d2-131">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f83d2-131">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

