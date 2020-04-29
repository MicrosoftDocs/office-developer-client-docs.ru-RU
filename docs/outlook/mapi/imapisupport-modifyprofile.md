---
title: имаписуппортмодифипрофиле
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.ModifyProfile
api_type:
- COM
ms.assetid: 33bef4ea-d6c0-4455-b95d-4b29edb9c0bc
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 4c296b12d2dc98c4ff8d94349298e9dda0fb9409
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419991"
---
# <a name="imapisupportmodifyprofile"></a><span data-ttu-id="9552f-103">IMAPISupport::ModifyProfile</span><span class="sxs-lookup"><span data-stu-id="9552f-103">IMAPISupport::ModifyProfile</span></span>

  
  
<span data-ttu-id="9552f-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9552f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9552f-105">Вносит изменения в раздел профиля хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="9552f-105">Makes changes to a message store profile section permanent.</span></span>
  
```cpp
HRESULT ModifyProfile(
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="9552f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9552f-106">Parameters</span></span>

 <span data-ttu-id="9552f-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9552f-107">_ulFlags_</span></span>
  
> <span data-ttu-id="9552f-108">возврата Битовая маска флагов, указывающая тип хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="9552f-108">[in] A bitmask of flags that indicates the type of message store.</span></span> <span data-ttu-id="9552f-109">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="9552f-109">The following flag can be set:</span></span>
    
<span data-ttu-id="9552f-110">MDB_TEMPORARY</span><span class="sxs-lookup"><span data-stu-id="9552f-110">MDB_TEMPORARY</span></span> 
  
> <span data-ttu-id="9552f-111">Хранилище сообщений является временным и не должно добавляться в таблицу хранения сообщений.</span><span class="sxs-lookup"><span data-stu-id="9552f-111">The message store is temporary and should not be added to the message store table.</span></span> <span data-ttu-id="9552f-112">Когда MDB_TEMPORARY задается, **модифипрофиле** немедленно возвращает S_OK.</span><span class="sxs-lookup"><span data-stu-id="9552f-112">When MDB_TEMPORARY is set, **ModifyProfile** returns S_OK immediately.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="9552f-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9552f-113">Return value</span></span>

<span data-ttu-id="9552f-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="9552f-114">S_OK</span></span> 
  
> <span data-ttu-id="9552f-115">Изменения в разделе профиля выполнены успешно.</span><span class="sxs-lookup"><span data-stu-id="9552f-115">The changes to the profile section were successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9552f-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="9552f-116">Remarks</span></span>

<span data-ttu-id="9552f-117">Метод **имаписуппорт:: модифипрофиле** реализован для объектов поддержки поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="9552f-117">The **IMAPISupport::ModifyProfile** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="9552f-118">Поставщики хранилищ сообщений вызывают **модифипрофиле** для запроса MAPI для изменения сведений о профиле.</span><span class="sxs-lookup"><span data-stu-id="9552f-118">Message store providers call **ModifyProfile** to prompt MAPI to modify their profile information.</span></span> 
  
 <span data-ttu-id="9552f-119">**Модифипрофиле** добавляет раздел профиля, связанный с поставщиком вызовов, в список установленных ресурсов поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="9552f-119">**ModifyProfile** adds the profile section that is associated with the calling provider to the list of installed message store provider resources.</span></span> <span data-ttu-id="9552f-120">Это приводит к тому, что хранилище сообщений отображается в таблице хранилища сообщений, которое доступно клиентам через метод [IMAPISession:: жетмсгсторестабле](imapisession-getmsgstorestable.md) , и его можно открыть без отображения диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="9552f-120">This causes the message store to be listed in the message store table, which is available to clients through the [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) method, and to be opened without the display of a dialog box.</span></span> 
  
<span data-ttu-id="9552f-121">Если установлен флаг MDB_TEMPORARY, MAPI не выполняет никаких действий, а метод немедленно возвращает с S_OK.</span><span class="sxs-lookup"><span data-stu-id="9552f-121">If the MDB_TEMPORARY flag is set, MAPI does nothing and the method returns immediately with S_OK.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9552f-122">См. также</span><span class="sxs-lookup"><span data-stu-id="9552f-122">See also</span></span>



[<span data-ttu-id="9552f-123">IMAPISession::GetMsgStoresTable</span><span class="sxs-lookup"><span data-stu-id="9552f-123">IMAPISession::GetMsgStoresTable</span></span>](imapisession-getmsgstorestable.md)
  
[<span data-ttu-id="9552f-124">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="9552f-124">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

