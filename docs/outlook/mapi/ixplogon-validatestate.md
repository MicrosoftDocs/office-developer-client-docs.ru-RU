---
title: IXPLogonValidateState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.ValidateState
api_type:
- COM
ms.assetid: c3649daa-cba1-48e3-9ffb-069c1bcf8228
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: a3469e6baacb52938b870ca87d824bf640a8a88f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439487"
---
# <a name="ixplogonvalidatestate"></a><span data-ttu-id="4741e-103">IXPLogon::ValidateState</span><span class="sxs-lookup"><span data-stu-id="4741e-103">IXPLogon::ValidateState</span></span>

  
  
<span data-ttu-id="4741e-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4741e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4741e-105">Проверяет внешнее состояние поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="4741e-105">Checks the transport provider's external status.</span></span> 
  
```cpp
HRESULT ValidateState(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="4741e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4741e-106">Parameters</span></span>

 <span data-ttu-id="4741e-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="4741e-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="4741e-108">[in] Handle to the parent window of any dialog boxes or windows that this method displays.</span><span class="sxs-lookup"><span data-stu-id="4741e-108">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="4741e-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4741e-109">_ulFlags_</span></span>
  
> <span data-ttu-id="4741e-110">[in] Битоваяmas флагов, которая управляет выполнением проверки состояния и результатами проверки состояния.</span><span class="sxs-lookup"><span data-stu-id="4741e-110">[in] A bitmask of flags that controls how the status check is performed and the results of the status check.</span></span> <span data-ttu-id="4741e-111">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="4741e-111">The following flags can be set:</span></span>
    
<span data-ttu-id="4741e-112">ABORT_XP_HEADER_OPERATION</span><span class="sxs-lookup"><span data-stu-id="4741e-112">ABORT_XP_HEADER_OPERATION</span></span> 
  
> <span data-ttu-id="4741e-113">Пользователь отменил операцию, обычно нажав  кнопку "Отмена" в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="4741e-113">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> <span data-ttu-id="4741e-114">Поставщик транспорта может продолжить работу над операцией или отменить операцию и вернуть MAPI_E_USER_CANCELED.</span><span class="sxs-lookup"><span data-stu-id="4741e-114">The transport provider has the option to continue working on the operation, or it can abort the operation and return MAPI_E_USER_CANCELED.</span></span> 
    
<span data-ttu-id="4741e-115">CONFIG_CHANGED</span><span class="sxs-lookup"><span data-stu-id="4741e-115">CONFIG_CHANGED</span></span> 
  
> <span data-ttu-id="4741e-116">Проверяет состояние загруженных поставщиков транспорта, вызывая метод [IXPLogon::AddressTypes](ixplogon-addresstypes.md) пулом MAPI.</span><span class="sxs-lookup"><span data-stu-id="4741e-116">Validates the state of currently loaded transport providers by causing the MAPI spooler to call their [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method.</span></span> <span data-ttu-id="4741e-117">Этот флаг также предоставляет пулу MAPI возможность исправить критические сбои поставщика транспорта без принудительного отключения клиентских приложений и повторного входа в систему.</span><span class="sxs-lookup"><span data-stu-id="4741e-117">This flag also provides the MAPI spooler an opportunity to correct critical transport-provider failures without forcing client applications to log off and then log on again.</span></span> 
    
<span data-ttu-id="4741e-118">FORCE_XP_CONNECT</span><span class="sxs-lookup"><span data-stu-id="4741e-118">FORCE_XP_CONNECT</span></span> 
  
> <span data-ttu-id="4741e-119">Пользователь выбрал операцию подключения.</span><span class="sxs-lookup"><span data-stu-id="4741e-119">The user selected a connect operation.</span></span> <span data-ttu-id="4741e-120">Если этот флаг используется с флагом REFRESH_XP_HEADER_CACHE или PROCESS_XP_HEADER_CACHE, действие подключения происходит без кэшинга.</span><span class="sxs-lookup"><span data-stu-id="4741e-120">When this flag is used with the REFRESH_XP_HEADER_CACHE or PROCESS_XP_HEADER_CACHE flag, the connect action occurs without caching.</span></span>
    
<span data-ttu-id="4741e-121">FORCE_XP_DISCONNECT</span><span class="sxs-lookup"><span data-stu-id="4741e-121">FORCE_XP_DISCONNECT</span></span> 
  
> <span data-ttu-id="4741e-122">Пользователь выбрал операцию отключения.</span><span class="sxs-lookup"><span data-stu-id="4741e-122">The user selected a disconnect operation.</span></span> <span data-ttu-id="4741e-123">Если этот флаг используется с REFRESH_XP_HEADER_CACHE или PROCESS_XP_HEADER_CACHE, действие отключения происходит без кэшинга.</span><span class="sxs-lookup"><span data-stu-id="4741e-123">When this flag is used with REFRESH_XP_HEADER_CACHE or PROCESS_XP_HEADER_CACHE, the disconnect action occurs without caching.</span></span>
    
<span data-ttu-id="4741e-124">PROCESS_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="4741e-124">PROCESS_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="4741e-125">Записи в таблице кэша загона должны быть обработаны, все сообщения, помеченные флагом MSGSTATUS_REMOTE_DOWNLOAD, должны быть загружены, а все сообщения с флагом MSGSTATUS_REMOTE_DELETE должны быть удалены.</span><span class="sxs-lookup"><span data-stu-id="4741e-125">Entries in the header cache table should be processed, all messages marked with the MSGSTATUS_REMOTE_DOWNLOAD flag should be downloaded, and all messages marked with the MSGSTATUS_REMOTE_DELETE flag should be deleted.</span></span> <span data-ttu-id="4741e-126">Сообщения, для MSGSTATUS_REMOTE_DOWNLOAD и MSGSTATUS_REMOTE_DELETE, должны быть перемещены.</span><span class="sxs-lookup"><span data-stu-id="4741e-126">Messages that have both MSGSTATUS_REMOTE_DOWNLOAD and MSGSTATUS_REMOTE_DELETE set should be moved.</span></span>
    
<span data-ttu-id="4741e-127">REFRESH_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="4741e-127">REFRESH_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="4741e-128">Необходимо скачать новый список заглавных сообщений, а также очистить все флаги пометки состояния сообщения.</span><span class="sxs-lookup"><span data-stu-id="4741e-128">A new list of message headers should be downloaded, and all message status marking flags should be cleared.</span></span>
    
<span data-ttu-id="4741e-129">SUPPRESS_UI</span><span class="sxs-lookup"><span data-stu-id="4741e-129">SUPPRESS_UI</span></span> 
  
> <span data-ttu-id="4741e-130">Не позволяет поставщику транспорта отображать пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="4741e-130">Prevents the transport provider from displaying a user interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4741e-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4741e-131">Return value</span></span>

<span data-ttu-id="4741e-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="4741e-132">S_OK</span></span> 
  
> <span data-ttu-id="4741e-133">Вызов был успешным и возвратил ожидаемое значение или значения.</span><span class="sxs-lookup"><span data-stu-id="4741e-133">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="4741e-134">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="4741e-134">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="4741e-135">В настоящее время идет другая операция; его следует разрешить завершить или остановить перед попыткой выполнения этой операции.</span><span class="sxs-lookup"><span data-stu-id="4741e-135">Another operation is in progress; it should be allowed to complete, or it should be stopped before this operation is attempted.</span></span>
    
<span data-ttu-id="4741e-136">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="4741e-136">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="4741e-137">Задействованный удаленный поставщик транспорта не поддерживает пользовательский интерфейс, а в самом клиенте должно отобразиться диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="4741e-137">The remote transport provider involved does not support a user interface, and the client application itself should display the dialog box.</span></span>
    
<span data-ttu-id="4741e-138">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="4741e-138">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="4741e-139">Пользователь отменил операцию, обычно нажав  кнопку "Отмена" в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="4741e-139">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="4741e-140">Примечания</span><span class="sxs-lookup"><span data-stu-id="4741e-140">Remarks</span></span>

<span data-ttu-id="4741e-141">Пулер MAPI вызывает метод **IXPLogon::ValidateState** для поддержки вызовов метода [IMAPIStatus::ValidateState](imapistatus-validatestate.md) для объекта состояния.</span><span class="sxs-lookup"><span data-stu-id="4741e-141">The MAPI spooler calls the **IXPLogon::ValidateState** method to support calls to the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method for the status object.</span></span> <span data-ttu-id="4741e-142">Поставщик транспорта должен отвечать на вызов **IXPLogon::ValidateState** точно так же, как если бы пулер MAPI открыл объект состояния для текущего сеанса и затем вызвал **IMAPIStatus::ValidateState** для этого объекта.</span><span class="sxs-lookup"><span data-stu-id="4741e-142">The transport provider should respond to the **IXPLogon::ValidateState** call exactly as if the MAPI spooler had opened a status object for the current logon session and then called **IMAPIStatus::ValidateState** on that object.</span></span> 
  
<span data-ttu-id="4741e-143">Чтобы поддерживать реализацию **IMAPIStatus::ValidateState,** пулер MAPI вызывает **IXPLogon::ValidateState** для всех объектов для запуска всех активных поставщиков транспорта, работающих в сеансе профиля.</span><span class="sxs-lookup"><span data-stu-id="4741e-143">To support its implementation of **IMAPIStatus::ValidateState**, the MAPI spooler calls **IXPLogon::ValidateState** on all logon objects for all active transport providers that are running in a profile session.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4741e-144">См. также</span><span class="sxs-lookup"><span data-stu-id="4741e-144">See also</span></span>



[<span data-ttu-id="4741e-145">IMAPIStatus::ValidateState</span><span class="sxs-lookup"><span data-stu-id="4741e-145">IMAPIStatus::ValidateState</span></span>](imapistatus-validatestate.md)
  
[<span data-ttu-id="4741e-146">IXPLogon::AddressTypes</span><span class="sxs-lookup"><span data-stu-id="4741e-146">IXPLogon::AddressTypes</span></span>](ixplogon-addresstypes.md)
  
[<span data-ttu-id="4741e-147">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4741e-147">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

