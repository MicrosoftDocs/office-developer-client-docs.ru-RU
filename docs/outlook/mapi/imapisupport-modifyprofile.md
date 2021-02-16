---
title: IMAPISupportModifyProfile
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
# <a name="imapisupportmodifyprofile"></a><span data-ttu-id="470ef-103">IMAPISupport::ModifyProfile</span><span class="sxs-lookup"><span data-stu-id="470ef-103">IMAPISupport::ModifyProfile</span></span>

  
  
<span data-ttu-id="470ef-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="470ef-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="470ef-105">Вносит изменения в раздел профиля хранения сообщений без изменений.</span><span class="sxs-lookup"><span data-stu-id="470ef-105">Makes changes to a message store profile section permanent.</span></span>
  
```cpp
HRESULT ModifyProfile(
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="470ef-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="470ef-106">Parameters</span></span>

 <span data-ttu-id="470ef-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="470ef-107">_ulFlags_</span></span>
  
> <span data-ttu-id="470ef-108">[in] Битоваяmas флагов, которая указывает тип хранения сообщений.</span><span class="sxs-lookup"><span data-stu-id="470ef-108">[in] A bitmask of flags that indicates the type of message store.</span></span> <span data-ttu-id="470ef-109">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="470ef-109">The following flag can be set:</span></span>
    
<span data-ttu-id="470ef-110">MDB_TEMPORARY</span><span class="sxs-lookup"><span data-stu-id="470ef-110">MDB_TEMPORARY</span></span> 
  
> <span data-ttu-id="470ef-111">Хранилище сообщений является временным и не должно быть добавлено в таблицу хранения сообщений.</span><span class="sxs-lookup"><span data-stu-id="470ef-111">The message store is temporary and should not be added to the message store table.</span></span> <span data-ttu-id="470ef-112">Если MDB_TEMPORARY, **ModifyProfile** возвращает S_OK немедленно.</span><span class="sxs-lookup"><span data-stu-id="470ef-112">When MDB_TEMPORARY is set, **ModifyProfile** returns S_OK immediately.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="470ef-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="470ef-113">Return value</span></span>

<span data-ttu-id="470ef-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="470ef-114">S_OK</span></span> 
  
> <span data-ttu-id="470ef-115">Изменения раздела профиля были успешно внесены.</span><span class="sxs-lookup"><span data-stu-id="470ef-115">The changes to the profile section were successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="470ef-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="470ef-116">Remarks</span></span>

<span data-ttu-id="470ef-117">Метод **IMAPISupport::ModifyProfile реализован** для объектов поддержки поставщика store сообщений.</span><span class="sxs-lookup"><span data-stu-id="470ef-117">The **IMAPISupport::ModifyProfile** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="470ef-118">Поставщики store сообщений **звонят modifyProfile,** чтобы упредить MAPI изменить данные своего профиля.</span><span class="sxs-lookup"><span data-stu-id="470ef-118">Message store providers call **ModifyProfile** to prompt MAPI to modify their profile information.</span></span> 
  
 <span data-ttu-id="470ef-119">**ModifyProfile** добавляет раздел профиля, связанный с поставщиком вызовов, в список ресурсов поставщика установленного магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="470ef-119">**ModifyProfile** adds the profile section that is associated with the calling provider to the list of installed message store provider resources.</span></span> <span data-ttu-id="470ef-120">В результате хранилище сообщений отображается в таблице банка сообщений, доступной клиентам с помощью метода [IMAPISession::GetMsgStoresTable,](imapisession-getmsgstorestable.md) и открывается без отображения диалоговых окно.</span><span class="sxs-lookup"><span data-stu-id="470ef-120">This causes the message store to be listed in the message store table, which is available to clients through the [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) method, and to be opened without the display of a dialog box.</span></span> 
  
<span data-ttu-id="470ef-121">Если флаг MDB_TEMPORARY установлен, MAPI ничего не делает, и метод немедленно возвращается с S_OK.</span><span class="sxs-lookup"><span data-stu-id="470ef-121">If the MDB_TEMPORARY flag is set, MAPI does nothing and the method returns immediately with S_OK.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="470ef-122">См. также</span><span class="sxs-lookup"><span data-stu-id="470ef-122">See also</span></span>



[<span data-ttu-id="470ef-123">IMAPISession::GetMsgStoresTable</span><span class="sxs-lookup"><span data-stu-id="470ef-123">IMAPISession::GetMsgStoresTable</span></span>](imapisession-getmsgstorestable.md)
  
[<span data-ttu-id="470ef-124">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="470ef-124">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

