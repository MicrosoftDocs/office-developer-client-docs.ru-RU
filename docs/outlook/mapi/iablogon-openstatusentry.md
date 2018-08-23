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
ms.openlocfilehash: cb9a2ba72ee9fd9c45aefe9d0797930a4871404a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579286"
---
# <a name="iablogonopenstatusentry"></a><span data-ttu-id="2f1ff-103">IABLogon::OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="2f1ff-103">IABLogon::OpenStatusEntry</span></span>

  
  
<span data-ttu-id="2f1ff-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2f1ff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2f1ff-105">Открывает объект состояние поставщика.</span><span class="sxs-lookup"><span data-stu-id="2f1ff-105">Opens the provider's status object.</span></span>
  
```cpp
HRESULT OpenStatusEntry(
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPMAPISTATUS FAR * lppEntry
);
```

## <a name="parameters"></a><span data-ttu-id="2f1ff-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2f1ff-106">Parameters</span></span>

 <span data-ttu-id="2f1ff-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="2f1ff-107">_lpInterface_</span></span>
  
> <span data-ttu-id="2f1ff-108">[in] Указатель на идентификатор интерфейса (ИД интерфейса), который представляет интерфейс, который должен использоваться для доступа к объекту состояния.</span><span class="sxs-lookup"><span data-stu-id="2f1ff-108">[in] A pointer to the interface identifier (IID) that represents the interface that must be used to access the status object.</span></span> <span data-ttu-id="2f1ff-109">Передача NULL возвращает объект стандартный интерфейс, [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="2f1ff-109">Passing NULL returns the object's standard interface, [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md).</span></span>
    
 <span data-ttu-id="2f1ff-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2f1ff-110">_ulFlags_</span></span>
  
> <span data-ttu-id="2f1ff-111">[in] Битовая маска флаги, который определяет способ открытия объекта состояния.</span><span class="sxs-lookup"><span data-stu-id="2f1ff-111">[in] A bitmask of flags that controls how the status object is opened.</span></span> <span data-ttu-id="2f1ff-112">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="2f1ff-112">The following flag can be set:</span></span>
    
<span data-ttu-id="2f1ff-113">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="2f1ff-113">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="2f1ff-114">Запросы на разрешение чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="2f1ff-114">Requests read/write permission.</span></span> <span data-ttu-id="2f1ff-115">По умолчанию объекты открываются с доступом только для чтения и абонентов не следует предполагать, что предоставлены разрешения на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="2f1ff-115">By default, objects are opened with read-only access, and callers should not assume that read/write permission has been granted.</span></span>
    
 <span data-ttu-id="2f1ff-116">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="2f1ff-116">_lpulObjType_</span></span>
  
> <span data-ttu-id="2f1ff-117">[out] Указатель на тип объекта открыт.</span><span class="sxs-lookup"><span data-stu-id="2f1ff-117">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="2f1ff-118">_lppEntry_</span><span class="sxs-lookup"><span data-stu-id="2f1ff-118">_lppEntry_</span></span>
  
> <span data-ttu-id="2f1ff-119">[out] Указатель на указатель на объект открыт.</span><span class="sxs-lookup"><span data-stu-id="2f1ff-119">[out] A pointer to a pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2f1ff-120">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="2f1ff-120">Return value</span></span>

<span data-ttu-id="2f1ff-121">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="2f1ff-121">S_OK</span></span> 
  
> <span data-ttu-id="2f1ff-122">Вызов завершился успешно и открытия объекта состояния.</span><span class="sxs-lookup"><span data-stu-id="2f1ff-122">The call succeeded and the status object has been opened.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2f1ff-123">Замечания</span><span class="sxs-lookup"><span data-stu-id="2f1ff-123">Remarks</span></span>

<span data-ttu-id="2f1ff-124">Метод **OpenStatusEntry** , чтобы предоставить доступ к их состояние объекта, реализуемые поставщиками адресных книг.</span><span class="sxs-lookup"><span data-stu-id="2f1ff-124">Address book providers implement the **OpenStatusEntry** method to grant access to their status object.</span></span> <span data-ttu-id="2f1ff-125">Все поставщиками адресной книги необходимы для реализации объект состояния, который поддерживает как минимум, метод [IMAPIStatus::ValidateState](imapistatus-validatestate.md) .</span><span class="sxs-lookup"><span data-stu-id="2f1ff-125">All address book providers are required to implement a status object that supports, at a minimum, the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method.</span></span> <span data-ttu-id="2f1ff-126">Для получения дополнительных сведений см [Реализация объекта состояния](status-object-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="2f1ff-126">For more information, see [Status Object Implementation](status-object-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2f1ff-127">См. также</span><span class="sxs-lookup"><span data-stu-id="2f1ff-127">See also</span></span>



[<span data-ttu-id="2f1ff-128">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="2f1ff-128">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)
  
[<span data-ttu-id="2f1ff-129">IMAPIStatus::SettingsDialog</span><span class="sxs-lookup"><span data-stu-id="2f1ff-129">IMAPIStatus::SettingsDialog</span></span>](imapistatus-settingsdialog.md)
  
[<span data-ttu-id="2f1ff-130">IMAPIStatus::ValidateState</span><span class="sxs-lookup"><span data-stu-id="2f1ff-130">IMAPIStatus::ValidateState</span></span>](imapistatus-validatestate.md)
  
[<span data-ttu-id="2f1ff-131">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2f1ff-131">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

