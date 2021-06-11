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
# <a name="imapisupportmodifyprofile"></a><span data-ttu-id="45efe-103">IMAPISupport::ModifyProfile</span><span class="sxs-lookup"><span data-stu-id="45efe-103">IMAPISupport::ModifyProfile</span></span>

  
  
<span data-ttu-id="45efe-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="45efe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="45efe-105">Вносит изменения в раздел профилей магазина сообщений навсегда.</span><span class="sxs-lookup"><span data-stu-id="45efe-105">Makes changes to a message store profile section permanent.</span></span>
  
```cpp
HRESULT ModifyProfile(
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="45efe-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="45efe-106">Parameters</span></span>

 <span data-ttu-id="45efe-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="45efe-107">_ulFlags_</span></span>
  
> <span data-ttu-id="45efe-108">[in] Битмашка флагов, которая указывает тип магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="45efe-108">[in] A bitmask of flags that indicates the type of message store.</span></span> <span data-ttu-id="45efe-109">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="45efe-109">The following flag can be set:</span></span>
    
<span data-ttu-id="45efe-110">MDB_TEMPORARY</span><span class="sxs-lookup"><span data-stu-id="45efe-110">MDB_TEMPORARY</span></span> 
  
> <span data-ttu-id="45efe-111">Хранилище сообщений является временным и не должно быть добавлено в таблицу хранения сообщений.</span><span class="sxs-lookup"><span data-stu-id="45efe-111">The message store is temporary and should not be added to the message store table.</span></span> <span data-ttu-id="45efe-112">Когда MDB_TEMPORARY установлено, **modifyProfile** возвращает S_OK.</span><span class="sxs-lookup"><span data-stu-id="45efe-112">When MDB_TEMPORARY is set, **ModifyProfile** returns S_OK immediately.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="45efe-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="45efe-113">Return value</span></span>

<span data-ttu-id="45efe-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="45efe-114">S_OK</span></span> 
  
> <span data-ttu-id="45efe-115">Изменения в разделе профилей были успешными.</span><span class="sxs-lookup"><span data-stu-id="45efe-115">The changes to the profile section were successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="45efe-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="45efe-116">Remarks</span></span>

<span data-ttu-id="45efe-117">Для объектов поддержки поставщика сообщений реализован метод **IMAPISupport::ModifyProfile.**</span><span class="sxs-lookup"><span data-stu-id="45efe-117">The **IMAPISupport::ModifyProfile** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="45efe-118">Поставщики магазинов сообщений **звонят в ModifyProfile,** чтобы побудить MAPI изменить сведения о профиле.</span><span class="sxs-lookup"><span data-stu-id="45efe-118">Message store providers call **ModifyProfile** to prompt MAPI to modify their profile information.</span></span> 
  
 <span data-ttu-id="45efe-119">**ModifyProfile** добавляет раздел профилей, связанный с поставщиком вызовов, в список ресурсов поставщика поставщиков установленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="45efe-119">**ModifyProfile** adds the profile section that is associated with the calling provider to the list of installed message store provider resources.</span></span> <span data-ttu-id="45efe-120">Это приводит к включению магазина сообщений в таблицу хранения сообщений, которая доступна клиентам с помощью метода [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) и открывается без отображения диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="45efe-120">This causes the message store to be listed in the message store table, which is available to clients through the [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) method, and to be opened without the display of a dialog box.</span></span> 
  
<span data-ttu-id="45efe-121">Если флаг MDB_TEMPORARY, MAPI ничего не делает и метод возвращается немедленно с S_OK.</span><span class="sxs-lookup"><span data-stu-id="45efe-121">If the MDB_TEMPORARY flag is set, MAPI does nothing and the method returns immediately with S_OK.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="45efe-122">См. также</span><span class="sxs-lookup"><span data-stu-id="45efe-122">See also</span></span>



[<span data-ttu-id="45efe-123">IMAPISession::GetMsgStoresTable</span><span class="sxs-lookup"><span data-stu-id="45efe-123">IMAPISession::GetMsgStoresTable</span></span>](imapisession-getmsgstorestable.md)
  
[<span data-ttu-id="45efe-124">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="45efe-124">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

