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
# <a name="ixplogonvalidatestate"></a><span data-ttu-id="0ef50-103">IXPLogon::ValidateState</span><span class="sxs-lookup"><span data-stu-id="0ef50-103">IXPLogon::ValidateState</span></span>

  
  
<span data-ttu-id="0ef50-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0ef50-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0ef50-105">Проверка внешнего состояния поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="0ef50-105">Checks the transport provider's external status.</span></span> 
  
```cpp
HRESULT ValidateState(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="0ef50-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="0ef50-106">Parameters</span></span>

 <span data-ttu-id="0ef50-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="0ef50-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="0ef50-108">[in] Ручка родительского окна любых диалогов или окон, отображаемого этим методом.</span><span class="sxs-lookup"><span data-stu-id="0ef50-108">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="0ef50-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0ef50-109">_ulFlags_</span></span>
  
> <span data-ttu-id="0ef50-110">[in] Битмаска флагов, которые контролируют, как выполняется проверка состояния и результаты проверки состояния.</span><span class="sxs-lookup"><span data-stu-id="0ef50-110">[in] A bitmask of flags that controls how the status check is performed and the results of the status check.</span></span> <span data-ttu-id="0ef50-111">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="0ef50-111">The following flags can be set:</span></span>
    
<span data-ttu-id="0ef50-112">ABORT_XP_HEADER_OPERATION</span><span class="sxs-lookup"><span data-stu-id="0ef50-112">ABORT_XP_HEADER_OPERATION</span></span> 
  
> <span data-ttu-id="0ef50-113">Пользователь отменил операцию, как правило, нажав кнопку **Отмена** в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="0ef50-113">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> <span data-ttu-id="0ef50-114">Поставщик транспорта может продолжить работу над операцией или прервать операцию и MAPI_E_USER_CANCELED.</span><span class="sxs-lookup"><span data-stu-id="0ef50-114">The transport provider has the option to continue working on the operation, or it can abort the operation and return MAPI_E_USER_CANCELED.</span></span> 
    
<span data-ttu-id="0ef50-115">CONFIG_CHANGED</span><span class="sxs-lookup"><span data-stu-id="0ef50-115">CONFIG_CHANGED</span></span> 
  
> <span data-ttu-id="0ef50-116">Проверяет состояние загруженных поставщиков транспорта, вызывая вызов spooler MAPI их [метода IXPLogon::AddressTypes.](ixplogon-addresstypes.md)</span><span class="sxs-lookup"><span data-stu-id="0ef50-116">Validates the state of currently loaded transport providers by causing the MAPI spooler to call their [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method.</span></span> <span data-ttu-id="0ef50-117">Этот флаг также предоставляет шпалеру MAPI возможность исправить критические сбои поставщика транспорта, не вынуждая клиентские приложения выйти из системы и снова войти в систему.</span><span class="sxs-lookup"><span data-stu-id="0ef50-117">This flag also provides the MAPI spooler an opportunity to correct critical transport-provider failures without forcing client applications to log off and then log on again.</span></span> 
    
<span data-ttu-id="0ef50-118">FORCE_XP_CONNECT</span><span class="sxs-lookup"><span data-stu-id="0ef50-118">FORCE_XP_CONNECT</span></span> 
  
> <span data-ttu-id="0ef50-119">Пользователь выбрал операцию подключения.</span><span class="sxs-lookup"><span data-stu-id="0ef50-119">The user selected a connect operation.</span></span> <span data-ttu-id="0ef50-120">Если этот флаг используется с REFRESH_XP_HEADER_CACHE или PROCESS_XP_HEADER_CACHE флагом, действие подключения происходит без кэшинга.</span><span class="sxs-lookup"><span data-stu-id="0ef50-120">When this flag is used with the REFRESH_XP_HEADER_CACHE or PROCESS_XP_HEADER_CACHE flag, the connect action occurs without caching.</span></span>
    
<span data-ttu-id="0ef50-121">FORCE_XP_DISCONNECT</span><span class="sxs-lookup"><span data-stu-id="0ef50-121">FORCE_XP_DISCONNECT</span></span> 
  
> <span data-ttu-id="0ef50-122">Пользователь выбрал операцию отключения.</span><span class="sxs-lookup"><span data-stu-id="0ef50-122">The user selected a disconnect operation.</span></span> <span data-ttu-id="0ef50-123">Если этот флаг используется с REFRESH_XP_HEADER_CACHE или PROCESS_XP_HEADER_CACHE, действие отключения происходит без кэшинга.</span><span class="sxs-lookup"><span data-stu-id="0ef50-123">When this flag is used with REFRESH_XP_HEADER_CACHE or PROCESS_XP_HEADER_CACHE, the disconnect action occurs without caching.</span></span>
    
<span data-ttu-id="0ef50-124">PROCESS_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="0ef50-124">PROCESS_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="0ef50-125">Записи в таблице кэша загона должны обрабатываться, все сообщения с флагом MSGSTATUS_REMOTE_DOWNLOAD должны быть загружены, а все сообщения, помеченные флагом MSGSTATUS_REMOTE_DELETE, должны быть удалены.</span><span class="sxs-lookup"><span data-stu-id="0ef50-125">Entries in the header cache table should be processed, all messages marked with the MSGSTATUS_REMOTE_DOWNLOAD flag should be downloaded, and all messages marked with the MSGSTATUS_REMOTE_DELETE flag should be deleted.</span></span> <span data-ttu-id="0ef50-126">Сообщения с набором MSGSTATUS_REMOTE_DOWNLOAD и MSGSTATUS_REMOTE_DELETE должны быть перемещены.</span><span class="sxs-lookup"><span data-stu-id="0ef50-126">Messages that have both MSGSTATUS_REMOTE_DOWNLOAD and MSGSTATUS_REMOTE_DELETE set should be moved.</span></span>
    
<span data-ttu-id="0ef50-127">REFRESH_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="0ef50-127">REFRESH_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="0ef50-128">Необходимо скачать новый список загона сообщений, а также очистить все флаги, помеченные состоянием сообщений.</span><span class="sxs-lookup"><span data-stu-id="0ef50-128">A new list of message headers should be downloaded, and all message status marking flags should be cleared.</span></span>
    
<span data-ttu-id="0ef50-129">SUPPRESS_UI</span><span class="sxs-lookup"><span data-stu-id="0ef50-129">SUPPRESS_UI</span></span> 
  
> <span data-ttu-id="0ef50-130">Не позволяет поставщику транспорта отображать пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="0ef50-130">Prevents the transport provider from displaying a user interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0ef50-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0ef50-131">Return value</span></span>

<span data-ttu-id="0ef50-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="0ef50-132">S_OK</span></span> 
  
> <span data-ttu-id="0ef50-133">Вызов удался и возвращает ожидаемое значение или значения.</span><span class="sxs-lookup"><span data-stu-id="0ef50-133">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="0ef50-134">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="0ef50-134">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="0ef50-135">В настоящее время продолжается другая операция; его следует разрешить завершить или остановить перед попыткой выполнения этой операции.</span><span class="sxs-lookup"><span data-stu-id="0ef50-135">Another operation is in progress; it should be allowed to complete, or it should be stopped before this operation is attempted.</span></span>
    
<span data-ttu-id="0ef50-136">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="0ef50-136">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="0ef50-137">Участвующий поставщик удаленного транспорта не поддерживает пользовательский интерфейс, а само клиентские приложения должны отображать диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="0ef50-137">The remote transport provider involved does not support a user interface, and the client application itself should display the dialog box.</span></span>
    
<span data-ttu-id="0ef50-138">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="0ef50-138">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="0ef50-139">Пользователь отменил операцию, как правило, нажав кнопку **Отмена** в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="0ef50-139">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="0ef50-140">Примечания</span><span class="sxs-lookup"><span data-stu-id="0ef50-140">Remarks</span></span>

<span data-ttu-id="0ef50-141">Spooler MAPI вызывает **метод IXPLogon::ValidateState** для поддержки вызовов для [метода IMAPIStatus::ValidateState](imapistatus-validatestate.md) для объекта состояния.</span><span class="sxs-lookup"><span data-stu-id="0ef50-141">The MAPI spooler calls the **IXPLogon::ValidateState** method to support calls to the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method for the status object.</span></span> <span data-ttu-id="0ef50-142">Поставщик транспорта должен отвечать на вызов **IXPLogon::ValidateState** так же, как если бы шпалер MAPI открыл объект состояния для текущего сеанса логотипа, а затем вызвал **IMAPIStatus::ValidateState** на этом объекте.</span><span class="sxs-lookup"><span data-stu-id="0ef50-142">The transport provider should respond to the **IXPLogon::ValidateState** call exactly as if the MAPI spooler had opened a status object for the current logon session and then called **IMAPIStatus::ValidateState** on that object.</span></span> 
  
<span data-ttu-id="0ef50-143">Чтобы поддержать реализацию **IMAPIStatus::ValidateState,** шпалер MAPI вызывает **IXPLogon::ValidateState** для всех объектов с логотипом для всех активных поставщиков транспорта, которые работают в сеансе профиля.</span><span class="sxs-lookup"><span data-stu-id="0ef50-143">To support its implementation of **IMAPIStatus::ValidateState**, the MAPI spooler calls **IXPLogon::ValidateState** on all logon objects for all active transport providers that are running in a profile session.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0ef50-144">См. также</span><span class="sxs-lookup"><span data-stu-id="0ef50-144">See also</span></span>



[<span data-ttu-id="0ef50-145">IMAPIStatus::ValidateState</span><span class="sxs-lookup"><span data-stu-id="0ef50-145">IMAPIStatus::ValidateState</span></span>](imapistatus-validatestate.md)
  
[<span data-ttu-id="0ef50-146">IXPLogon::AddressTypes</span><span class="sxs-lookup"><span data-stu-id="0ef50-146">IXPLogon::AddressTypes</span></span>](ixplogon-addresstypes.md)
  
[<span data-ttu-id="0ef50-147">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0ef50-147">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

