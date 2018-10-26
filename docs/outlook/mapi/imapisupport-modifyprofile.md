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
ms.openlocfilehash: b16730681b5414f28ae45be7195b4fa551bf0e82
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591991"
---
# <a name="imapisupportmodifyprofile"></a><span data-ttu-id="5bf40-103">IMAPISupport::ModifyProfile</span><span class="sxs-lookup"><span data-stu-id="5bf40-103">IMAPISupport::ModifyProfile</span></span>

  
  
<span data-ttu-id="5bf40-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5bf40-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5bf40-105">Вносятся изменения в сообщение хранения основного раздела профиля.</span><span class="sxs-lookup"><span data-stu-id="5bf40-105">Makes changes to a message store profile section permanent.</span></span>
  
```cpp
HRESULT ModifyProfile(
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="5bf40-106">���������</span><span class="sxs-lookup"><span data-stu-id="5bf40-106">Parameters</span></span>

 <span data-ttu-id="5bf40-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5bf40-107">_ulFlags_</span></span>
  
> <span data-ttu-id="5bf40-108">[in] Хранить битовую маску флагов, указывающую тип сообщений.</span><span class="sxs-lookup"><span data-stu-id="5bf40-108">[in] A bitmask of flags that indicates the type of message store.</span></span> <span data-ttu-id="5bf40-109">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="5bf40-109">The following flag can be set:</span></span>
    
<span data-ttu-id="5bf40-110">MDB_TEMPORARY</span><span class="sxs-lookup"><span data-stu-id="5bf40-110">MDB_TEMPORARY</span></span> 
  
> <span data-ttu-id="5bf40-111">Хранилище сообщений временно и не следует добавлять к таблице хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="5bf40-111">The message store is temporary and should not be added to the message store table.</span></span> <span data-ttu-id="5bf40-112">Если для MDB_TEMPORARY, **ModifyProfile** возвращает значение S_OK немедленно.</span><span class="sxs-lookup"><span data-stu-id="5bf40-112">When MDB_TEMPORARY is set, **ModifyProfile** returns S_OK immediately.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="5bf40-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5bf40-113">Return value</span></span>

<span data-ttu-id="5bf40-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="5bf40-114">S_OK</span></span> 
  
> <span data-ttu-id="5bf40-115">Изменения в раздел профиля было выполнено успешно.</span><span class="sxs-lookup"><span data-stu-id="5bf40-115">The changes to the profile section were successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5bf40-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="5bf40-116">Remarks</span></span>

<span data-ttu-id="5bf40-117">Метод **IMAPISupport::ModifyProfile** реализуется для объектов поддержки поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="5bf40-117">The **IMAPISupport::ModifyProfile** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="5bf40-118">Сообщение вызова поставщиков хранилища **ModifyProfile** запроса MAPI для изменения сведения о своих профилях.</span><span class="sxs-lookup"><span data-stu-id="5bf40-118">Message store providers call **ModifyProfile** to prompt MAPI to modify their profile information.</span></span> 
  
 <span data-ttu-id="5bf40-119">**ModifyProfile** Добавление раздела профиля, который связан с вызова поставщика в список установленных сообщение ресурсов поставщика хранилища.</span><span class="sxs-lookup"><span data-stu-id="5bf40-119">**ModifyProfile** adds the profile section that is associated with the calling provider to the list of installed message store provider resources.</span></span> <span data-ttu-id="5bf40-120">В этом случае хранилища сообщений и будет включено в таблицу хранилища сообщений, в которой доступен для клиентов, метод [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) и открывать без отображения диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="5bf40-120">This causes the message store to be listed in the message store table, which is available to clients through the [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) method, and to be opened without the display of a dialog box.</span></span> 
  
<span data-ttu-id="5bf40-121">Если установлен флаг MDB_TEMPORARY, MAPI не выполняет никаких действий и метод немедленно возвращает значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="5bf40-121">If the MDB_TEMPORARY flag is set, MAPI does nothing and the method returns immediately with S_OK.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5bf40-122">См. также</span><span class="sxs-lookup"><span data-stu-id="5bf40-122">See also</span></span>



[<span data-ttu-id="5bf40-123">IMAPISession::GetMsgStoresTable</span><span class="sxs-lookup"><span data-stu-id="5bf40-123">IMAPISession::GetMsgStoresTable</span></span>](imapisession-getmsgstorestable.md)
  
[<span data-ttu-id="5bf40-124">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="5bf40-124">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

