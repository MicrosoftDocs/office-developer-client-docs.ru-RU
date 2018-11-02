---
title: IMSLogonOpenStatusEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.OpenStatusEntry
api_type:
- COM
ms.assetid: 850e256b-6b50-428c-aede-287edaf7b005
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: a48d8248878c64de827bb09030073e6becba3024
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571201"
---
# <a name="imslogonopenstatusentry"></a><span data-ttu-id="88c5a-103">IMSLogon::OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="88c5a-103">IMSLogon::OpenStatusEntry</span></span>

  
  
<span data-ttu-id="88c5a-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="88c5a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="88c5a-105">Открывает объект состояния.</span><span class="sxs-lookup"><span data-stu-id="88c5a-105">Opens a status object.</span></span>
  
```cpp
HRESULT OpenStatusEntry(
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPVOID FAR * lppEntry
);
```

## <a name="parameters"></a><span data-ttu-id="88c5a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="88c5a-106">Parameters</span></span>

 <span data-ttu-id="88c5a-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="88c5a-107">_lpInterface_</span></span>
  
> <span data-ttu-id="88c5a-108">[in] Указатель на идентификатор интерфейса (ИД интерфейса) объект состояния, чтобы открыть.</span><span class="sxs-lookup"><span data-stu-id="88c5a-108">[in] A pointer to the interface identifier (IID) for the status object to open.</span></span> <span data-ttu-id="88c5a-109">Значение NULL указывает, что возвращаются стандартный интерфейс для объекта (в данном случае интерфейс [IMAPIStatus](imapistatusimapiprop.md) ).</span><span class="sxs-lookup"><span data-stu-id="88c5a-109">Passing NULL indicates the standard interface for the object is returned (in this case, the [IMAPIStatus](imapistatusimapiprop.md) interface).</span></span> <span data-ttu-id="88c5a-110">Параметр _lpInterface_ можно также назначается идентификатор соответствующий интерфейс для объекта.</span><span class="sxs-lookup"><span data-stu-id="88c5a-110">The  _lpInterface_ parameter can also be set to an identifier for an appropriate interface for the object.</span></span> 
    
 <span data-ttu-id="88c5a-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="88c5a-111">_ulFlags_</span></span>
  
> <span data-ttu-id="88c5a-112">[in] Битовая маска флаги, который определяет способ открытия объекта состояния.</span><span class="sxs-lookup"><span data-stu-id="88c5a-112">[in] A bitmask of flags that controls how the status object is opened.</span></span> <span data-ttu-id="88c5a-113">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="88c5a-113">The following flag can be set:</span></span>
    
<span data-ttu-id="88c5a-114">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="88c5a-114">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="88c5a-115">Запросы на разрешение чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="88c5a-115">Requests read/write permission.</span></span> <span data-ttu-id="88c5a-116">По умолчанию объекты создаются с разрешением только для чтения и клиентские приложения не должны работать предполагается, что что назначено разрешение чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="88c5a-116">By default, objects are created with read-only permission, and client applications should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="88c5a-117">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="88c5a-117">_lpulObjType_</span></span>
  
> <span data-ttu-id="88c5a-118">[out] Указатель на тип объекта открыт.</span><span class="sxs-lookup"><span data-stu-id="88c5a-118">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="88c5a-119">_lppEntry_</span><span class="sxs-lookup"><span data-stu-id="88c5a-119">_lppEntry_</span></span>
  
> <span data-ttu-id="88c5a-120">[out] Указатель на указатель на объект открыт.</span><span class="sxs-lookup"><span data-stu-id="88c5a-120">[out] A pointer to the pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="88c5a-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="88c5a-121">Return value</span></span>

<span data-ttu-id="88c5a-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="88c5a-122">S_OK</span></span> 
  
> <span data-ttu-id="88c5a-123">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="88c5a-123">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="88c5a-124">���������</span><span class="sxs-lookup"><span data-stu-id="88c5a-124">Remarks</span></span>

<span data-ttu-id="88c5a-125">Поставщики хранилища сообщений реализуйте метод **IMSLogon::OpenStatusEntry** открыть объект состояния.</span><span class="sxs-lookup"><span data-stu-id="88c5a-125">Message store providers implement the **IMSLogon::OpenStatusEntry** method to open a status object.</span></span> <span data-ttu-id="88c5a-126">Этот объект состояния затем используется для предоставления клиентам для вызова метода [IMAPIStatus](imapistatusimapiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="88c5a-126">This status object is then used to enable clients to call [IMAPIStatus](imapistatusimapiprop.md) methods.</span></span> <span data-ttu-id="88c5a-127">Например клиенты могут использовать метод [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) для изменения конфигурации сеанса входа в систему хранения сообщений либо метод [IMAPIStatus::ValidateState](imapistatus-validatestate.md) для проверки состояния сеанса входа в систему хранения сообщений.</span><span class="sxs-lookup"><span data-stu-id="88c5a-127">For example, clients can use the [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method to reconfigure the message store logon session or the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method to validate the state of the message store logon session.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="88c5a-128">См. также</span><span class="sxs-lookup"><span data-stu-id="88c5a-128">See also</span></span>



[<span data-ttu-id="88c5a-129">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="88c5a-129">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)
  
[<span data-ttu-id="88c5a-130">IMAPIStatus::SettingsDialog</span><span class="sxs-lookup"><span data-stu-id="88c5a-130">IMAPIStatus::SettingsDialog</span></span>](imapistatus-settingsdialog.md)
  
[<span data-ttu-id="88c5a-131">IMAPIStatus::ValidateState</span><span class="sxs-lookup"><span data-stu-id="88c5a-131">IMAPIStatus::ValidateState</span></span>](imapistatus-validatestate.md)
  
[<span data-ttu-id="88c5a-132">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="88c5a-132">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

