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
ms.openlocfilehash: 55cf41d251db4c84dad9f12d8f83d0b0dda63ff3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809420"
---
# <a name="imslogonopenstatusentry"></a><span data-ttu-id="bb4c3-103">IMSLogon::OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="bb4c3-103">IMSLogon::OpenStatusEntry</span></span>

  
  
<span data-ttu-id="bb4c3-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bb4c3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bb4c3-105">Открывает объект состояния.</span><span class="sxs-lookup"><span data-stu-id="bb4c3-105">Opens a status object.</span></span>
  
```cpp
HRESULT OpenStatusEntry(
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPVOID FAR * lppEntry
);
```

## <a name="parameters"></a><span data-ttu-id="bb4c3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bb4c3-106">Parameters</span></span>

 <span data-ttu-id="bb4c3-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="bb4c3-107">_lpInterface_</span></span>
  
> <span data-ttu-id="bb4c3-108">[in] Указатель на идентификатор интерфейса (ИД интерфейса) объект состояния, чтобы открыть.</span><span class="sxs-lookup"><span data-stu-id="bb4c3-108">[in] A pointer to the interface identifier (IID) for the status object to open.</span></span> <span data-ttu-id="bb4c3-109">Значение NULL указывает, что возвращаются стандартный интерфейс для объекта (в данном случае интерфейс [IMAPIStatus](imapistatusimapiprop.md) ).</span><span class="sxs-lookup"><span data-stu-id="bb4c3-109">Passing NULL indicates the standard interface for the object is returned (in this case, the [IMAPIStatus](imapistatusimapiprop.md) interface).</span></span> <span data-ttu-id="bb4c3-110">Параметр _lpInterface_ можно также назначается идентификатор соответствующий интерфейс для объекта.</span><span class="sxs-lookup"><span data-stu-id="bb4c3-110">The  _lpInterface_ parameter can also be set to an identifier for an appropriate interface for the object.</span></span> 
    
 <span data-ttu-id="bb4c3-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="bb4c3-111">_ulFlags_</span></span>
  
> <span data-ttu-id="bb4c3-112">[in] Битовая маска флаги, который определяет способ открытия объекта состояния.</span><span class="sxs-lookup"><span data-stu-id="bb4c3-112">[in] A bitmask of flags that controls how the status object is opened.</span></span> <span data-ttu-id="bb4c3-113">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="bb4c3-113">The following flag can be set:</span></span>
    
<span data-ttu-id="bb4c3-114">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="bb4c3-114">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="bb4c3-115">Запросы на разрешение чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="bb4c3-115">Requests read/write permission.</span></span> <span data-ttu-id="bb4c3-116">По умолчанию объекты создаются с разрешением только для чтения и клиентские приложения не должны работать предполагается, что что назначено разрешение чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="bb4c3-116">By default, objects are created with read-only permission, and client applications should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="bb4c3-117">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="bb4c3-117">_lpulObjType_</span></span>
  
> <span data-ttu-id="bb4c3-118">[out] Указатель на тип объекта открыт.</span><span class="sxs-lookup"><span data-stu-id="bb4c3-118">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="bb4c3-119">_lppEntry_</span><span class="sxs-lookup"><span data-stu-id="bb4c3-119">_lppEntry_</span></span>
  
> <span data-ttu-id="bb4c3-120">[out] Указатель на указатель на объект открыт.</span><span class="sxs-lookup"><span data-stu-id="bb4c3-120">[out] A pointer to the pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="bb4c3-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1">Return value</span></span>

<span data-ttu-id="bb4c3-122">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="bb4c3-122">S_OK</span></span> 
  
> <span data-ttu-id="bb4c3-123">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="bb4c3-123">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bb4c3-124">���������</span><span class="sxs-lookup"><span data-stu-id="bb4c3-124">Remarks</span></span>

<span data-ttu-id="bb4c3-125">Поставщики хранилища сообщений реализуйте метод **IMSLogon::OpenStatusEntry** открыть объект состояния.</span><span class="sxs-lookup"><span data-stu-id="bb4c3-125">Message store providers implement the **IMSLogon::OpenStatusEntry** method to open a status object.</span></span> <span data-ttu-id="bb4c3-126">Этот объект состояния затем используется для предоставления клиентам для вызова метода [IMAPIStatus](imapistatusimapiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="bb4c3-126">This status object is then used to enable clients to call [IMAPIStatus](imapistatusimapiprop.md) methods.</span></span> <span data-ttu-id="bb4c3-127">Например клиенты могут использовать метод [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) для изменения конфигурации сеанса входа в систему хранения сообщений либо метод [IMAPIStatus::ValidateState](imapistatus-validatestate.md) для проверки состояния сеанса входа в систему хранения сообщений.</span><span class="sxs-lookup"><span data-stu-id="bb4c3-127">For example, clients can use the [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method to reconfigure the message store logon session or the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method to validate the state of the message store logon session.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bb4c3-128">См. также</span><span class="sxs-lookup"><span data-stu-id="bb4c3-128">See also</span></span>



[<span data-ttu-id="bb4c3-129">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="bb4c3-129">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)
  
[<span data-ttu-id="bb4c3-130">IMAPIStatus::SettingsDialog</span><span class="sxs-lookup"><span data-stu-id="bb4c3-130">IMAPIStatus::SettingsDialog</span></span>](imapistatus-settingsdialog.md)
  
[<span data-ttu-id="bb4c3-131">IMAPIStatus::ValidateState</span><span class="sxs-lookup"><span data-stu-id="bb4c3-131">IMAPIStatus::ValidateState</span></span>](imapistatus-validatestate.md)
  
[<span data-ttu-id="bb4c3-132">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="bb4c3-132">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

