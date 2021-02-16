---
title: IXPLogonOpenStatusEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.OpenStatusEntry
api_type:
- COM
ms.assetid: 261d5f7c-bb61-4e1d-aa41-cca224c63f8e
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: d9e09de1064a0ae034bb3618f0e5b3719a82c163
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435903"
---
# <a name="ixplogonopenstatusentry"></a><span data-ttu-id="fd78d-103">IXPLogon::OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="fd78d-103">IXPLogon::OpenStatusEntry</span></span>

  
  
<span data-ttu-id="fd78d-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fd78d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fd78d-105">Открывает объект состояния поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="fd78d-105">Opens the transport provider's status object.</span></span>
  
```cpp
HRESULT OpenStatusEntry(
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPMAPISTATUS FAR * lppEntry
);
```

## <a name="parameters"></a><span data-ttu-id="fd78d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fd78d-106">Parameters</span></span>

 <span data-ttu-id="fd78d-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="fd78d-107">_lpInterface_</span></span>
  
> <span data-ttu-id="fd78d-108">[in] Указатель на идентификатор интерфейса (IID) для объекта транспортного логотипа.</span><span class="sxs-lookup"><span data-stu-id="fd78d-108">[in] A pointer to an interface identifier (IID) for the transport logon object.</span></span> <span data-ttu-id="fd78d-109">Передача NULL возвращает [интерфейс IMAPIStatus.](imapistatusimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="fd78d-109">Passing NULL returns the [IMAPIStatus](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="fd78d-110">Параметр  _lpInterface_ также может быть задан в качестве идентификатора интерфейса для объекта.</span><span class="sxs-lookup"><span data-stu-id="fd78d-110">The  _lpInterface_ parameter can also be set to an identifier for an interface for the object.</span></span> 
    
 <span data-ttu-id="fd78d-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="fd78d-111">_ulFlags_</span></span>
  
> <span data-ttu-id="fd78d-112">[in] Битоваяmas флагов, которая управляет открытием объекта состояния.</span><span class="sxs-lookup"><span data-stu-id="fd78d-112">[in] A bitmask of flags that controls how the status object is opened.</span></span> <span data-ttu-id="fd78d-113">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="fd78d-113">The following flag can be set:</span></span>
    
<span data-ttu-id="fd78d-114">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="fd78d-114">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="fd78d-115">Запрашивает разрешение на чтение и записи.</span><span class="sxs-lookup"><span data-stu-id="fd78d-115">Requests read/write permission.</span></span> <span data-ttu-id="fd78d-116">Интерфейс по умолчанию является только для чтения.</span><span class="sxs-lookup"><span data-stu-id="fd78d-116">The default interface is read-only.</span></span> 
    
 <span data-ttu-id="fd78d-117">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="fd78d-117">_lpulObjType_</span></span>
  
> <span data-ttu-id="fd78d-118">[out] Указатель на тип открытого объекта.</span><span class="sxs-lookup"><span data-stu-id="fd78d-118">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="fd78d-119">_lppEntry_</span><span class="sxs-lookup"><span data-stu-id="fd78d-119">_lppEntry_</span></span>
  
> <span data-ttu-id="fd78d-120">[out] Указатель на указатель на открытый объект состояния.</span><span class="sxs-lookup"><span data-stu-id="fd78d-120">[out] A pointer to the pointer to the opened status object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fd78d-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fd78d-121">Return value</span></span>

<span data-ttu-id="fd78d-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="fd78d-122">S_OK</span></span> 
  
> <span data-ttu-id="fd78d-123">Вызов был успешным и возвратил ожидаемое значение или значения.</span><span class="sxs-lookup"><span data-stu-id="fd78d-123">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fd78d-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="fd78d-124">Remarks</span></span>

<span data-ttu-id="fd78d-125">Пулер MAPI вызывает метод **IXPLogon::OpenStatusEntry,** когда клиентский приложение вызывает метод **OpenEntry** для идентификатора записи в строке таблицы состояния поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="fd78d-125">The MAPI spooler calls the **IXPLogon::OpenStatusEntry** method when a client application calls an **OpenEntry** method for the entry identifier in the transport provider's status table row.</span></span> <span data-ttu-id="fd78d-126">**OpenStatusEntry** открывает объект с интерфейсом **IMAPIStatus,** связанным с этим конкретным поставщиком транспорта.</span><span class="sxs-lookup"><span data-stu-id="fd78d-126">**OpenStatusEntry** opens an object with the **IMAPIStatus** interface associated with this particular transport provider logon.</span></span> <span data-ttu-id="fd78d-127">Этот объект затем используется для того, чтобы клиентские приложения могли вызывать методы **IMAPIStatus** (например, для перенастройки сеанса logon с помощью метода [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) или для проверки состояния сеанса logon с помощью метода [IMAPIStatus::ValidateState).](imapistatus-validatestate.md)</span><span class="sxs-lookup"><span data-stu-id="fd78d-127">This object is then used to enable client applications to call **IMAPIStatus** methods (for example, to reconfigure the logon session by using the [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method, or to validate the state of the logon session by using the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fd78d-128">См. также</span><span class="sxs-lookup"><span data-stu-id="fd78d-128">See also</span></span>



[<span data-ttu-id="fd78d-129">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="fd78d-129">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)
  
[<span data-ttu-id="fd78d-130">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fd78d-130">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

