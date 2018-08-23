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
ms.openlocfilehash: 4fd0dd02c5cf6f6a49b782d06c02e373dcfc3327
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577487"
---
# <a name="ixplogonvalidatestate"></a><span data-ttu-id="be3d9-103">IXPLogon::ValidateState</span><span class="sxs-lookup"><span data-stu-id="be3d9-103">IXPLogon::ValidateState</span></span>

  
  
<span data-ttu-id="be3d9-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="be3d9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="be3d9-105">Проверяет состояние внешних поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="be3d9-105">Checks the transport provider's external status.</span></span> 
  
```cpp
HRESULT ValidateState(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="be3d9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="be3d9-106">Parameters</span></span>

 <span data-ttu-id="be3d9-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="be3d9-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="be3d9-108">[in] Дескриптор родительского окна все диалоговые окна или окна, которые отображаются этот метод.</span><span class="sxs-lookup"><span data-stu-id="be3d9-108">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="be3d9-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="be3d9-109">_ulFlags_</span></span>
  
> <span data-ttu-id="be3d9-110">[in] Битовая маска флаги, определяет, как выполняется проверка состояния и результатов Проверка состояния.</span><span class="sxs-lookup"><span data-stu-id="be3d9-110">[in] A bitmask of flags that controls how the status check is performed and the results of the status check.</span></span> <span data-ttu-id="be3d9-111">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="be3d9-111">The following flags can be set:</span></span>
    
<span data-ttu-id="be3d9-112">ABORT_XP_HEADER_OPERATION</span><span class="sxs-lookup"><span data-stu-id="be3d9-112">ABORT_XP_HEADER_OPERATION</span></span> 
  
> <span data-ttu-id="be3d9-113">Пользователь отменил операцию, как правило, нажмите кнопку **Отмена** в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="be3d9-113">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> <span data-ttu-id="be3d9-114">Поставщика транспорта имеет параметр, чтобы продолжить работу над операции или может прервать операцию и вернуть MAPI_E_USER_CANCELED.</span><span class="sxs-lookup"><span data-stu-id="be3d9-114">The transport provider has the option to continue working on the operation, or it can abort the operation and return MAPI_E_USER_CANCELED.</span></span> 
    
<span data-ttu-id="be3d9-115">CONFIG_CHANGED</span><span class="sxs-lookup"><span data-stu-id="be3d9-115">CONFIG_CHANGED</span></span> 
  
> <span data-ttu-id="be3d9-116">Проверяет состояние поставщиков в настоящее время загрузки транспорта, вызывающие диспетчер очереди MAPI для вызова метода их [IXPLogon::AddressTypes](ixplogon-addresstypes.md) .</span><span class="sxs-lookup"><span data-stu-id="be3d9-116">Validates the state of currently loaded transport providers by causing the MAPI spooler to call their [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method.</span></span> <span data-ttu-id="be3d9-117">Этот флаг также предоставляет диспетчер очереди MAPI для исправления ошибок критические поставщика транспорта без перезагрузки клиентских приложений, чтобы выйти и снова войти в систему.</span><span class="sxs-lookup"><span data-stu-id="be3d9-117">This flag also provides the MAPI spooler an opportunity to correct critical transport-provider failures without forcing client applications to log off and then log on again.</span></span> 
    
<span data-ttu-id="be3d9-118">FORCE_XP_CONNECT</span><span class="sxs-lookup"><span data-stu-id="be3d9-118">FORCE_XP_CONNECT</span></span> 
  
> <span data-ttu-id="be3d9-119">Пользователь выбрал операции подключения.</span><span class="sxs-lookup"><span data-stu-id="be3d9-119">The user selected a connect operation.</span></span> <span data-ttu-id="be3d9-120">Когда этот флаг используется с флагом REFRESH_XP_HEADER_CACHE или PROCESS_XP_HEADER_CACHE, действие подключения происходит без кэширования.</span><span class="sxs-lookup"><span data-stu-id="be3d9-120">When this flag is used with the REFRESH_XP_HEADER_CACHE or PROCESS_XP_HEADER_CACHE flag, the connect action occurs without caching.</span></span>
    
<span data-ttu-id="be3d9-121">FORCE_XP_DISCONNECT</span><span class="sxs-lookup"><span data-stu-id="be3d9-121">FORCE_XP_DISCONNECT</span></span> 
  
> <span data-ttu-id="be3d9-122">Пользователь выбрал операцию отключения.</span><span class="sxs-lookup"><span data-stu-id="be3d9-122">The user selected a disconnect operation.</span></span> <span data-ttu-id="be3d9-123">Когда этот флаг используется с REFRESH_XP_HEADER_CACHE или PROCESS_XP_HEADER_CACHE, действия отключения происходит без кэширования.</span><span class="sxs-lookup"><span data-stu-id="be3d9-123">When this flag is used with REFRESH_XP_HEADER_CACHE or PROCESS_XP_HEADER_CACHE, the disconnect action occurs without caching.</span></span>
    
<span data-ttu-id="be3d9-124">PROCESS_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="be3d9-124">PROCESS_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="be3d9-125">Будут обрабатываться записей в таблице кэша заголовок, необходимо загрузить все сообщения, помеченные с флагом MSGSTATUS_REMOTE_DOWNLOAD и все сообщения, помеченные с флагом MSGSTATUS_REMOTE_DELETE подлежащий удалению.</span><span class="sxs-lookup"><span data-stu-id="be3d9-125">Entries in the header cache table should be processed, all messages marked with the MSGSTATUS_REMOTE_DOWNLOAD flag should be downloaded, and all messages marked with the MSGSTATUS_REMOTE_DELETE flag should be deleted.</span></span> <span data-ttu-id="be3d9-126">Необходимо переместить сообщения, для которых MSGSTATUS_REMOTE_DOWNLOAD и задать MSGSTATUS_REMOTE_DELETE.</span><span class="sxs-lookup"><span data-stu-id="be3d9-126">Messages that have both MSGSTATUS_REMOTE_DOWNLOAD and MSGSTATUS_REMOTE_DELETE set should be moved.</span></span>
    
<span data-ttu-id="be3d9-127">REFRESH_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="be3d9-127">REFRESH_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="be3d9-128">Необходимо загрузить новый список заголовки сообщений, а все состояния сообщения Пометка флаги должна быть удалена.</span><span class="sxs-lookup"><span data-stu-id="be3d9-128">A new list of message headers should be downloaded, and all message status marking flags should be cleared.</span></span>
    
<span data-ttu-id="be3d9-129">SUPPRESS_UI</span><span class="sxs-lookup"><span data-stu-id="be3d9-129">SUPPRESS_UI</span></span> 
  
> <span data-ttu-id="be3d9-130">Запрещает отображение пользовательского интерфейса поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="be3d9-130">Prevents the transport provider from displaying a user interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="be3d9-131">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="be3d9-131">Return value</span></span>

<span data-ttu-id="be3d9-132">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="be3d9-132">S_OK</span></span> 
  
> <span data-ttu-id="be3d9-133">Вызов успешно и возвращается ожидаемым значением или значения.</span><span class="sxs-lookup"><span data-stu-id="be3d9-133">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="be3d9-134">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="be3d9-134">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="be3d9-135">Другой операции находится в стадии разработки; должны для выполнения или должна быть остановлена перед выполняется эта операция.</span><span class="sxs-lookup"><span data-stu-id="be3d9-135">Another operation is in progress; it should be allowed to complete, or it should be stopped before this operation is attempted.</span></span>
    
<span data-ttu-id="be3d9-136">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="be3d9-136">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="be3d9-137">Используемые поставщик удаленного транспорта не поддерживает пользовательский интерфейс и само приложение клиента должны отображать диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="be3d9-137">The remote transport provider involved does not support a user interface, and the client application itself should display the dialog box.</span></span>
    
<span data-ttu-id="be3d9-138">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="be3d9-138">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="be3d9-139">Пользователь отменил операцию, как правило, нажмите кнопку **Отмена** в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="be3d9-139">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="be3d9-140">Замечания</span><span class="sxs-lookup"><span data-stu-id="be3d9-140">Remarks</span></span>

<span data-ttu-id="be3d9-141">Диспетчер очереди MAPI вызывает метод **IXPLogon::ValidateState** для поддержки вызовы метода [IMAPIStatus::ValidateState](imapistatus-validatestate.md) для объекта состояния.</span><span class="sxs-lookup"><span data-stu-id="be3d9-141">The MAPI spooler calls the **IXPLogon::ValidateState** method to support calls to the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method for the status object.</span></span> <span data-ttu-id="be3d9-142">Поставщика транспорта должны ответить на звонок **IXPLogon::ValidateState** точно так же, если диспетчер очереди MAPI открыт объект состояния для текущего сеанса и затем вызвать **IMAPIStatus::ValidateState** для этого объекта.</span><span class="sxs-lookup"><span data-stu-id="be3d9-142">The transport provider should respond to the **IXPLogon::ValidateState** call exactly as if the MAPI spooler had opened a status object for the current logon session and then called **IMAPIStatus::ValidateState** on that object.</span></span> 
  
<span data-ttu-id="be3d9-143">Для поддержки его реализация **IMAPIStatus::ValidateState**, диспетчер очереди MAPI вызывает **IXPLogon::ValidateState** для всех объектов входа для всех поставщиков активный перенос, на которых выполняется в рамках сеанса профилей.</span><span class="sxs-lookup"><span data-stu-id="be3d9-143">To support its implementation of **IMAPIStatus::ValidateState**, the MAPI spooler calls **IXPLogon::ValidateState** on all logon objects for all active transport providers that are running in a profile session.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="be3d9-144">См. также</span><span class="sxs-lookup"><span data-stu-id="be3d9-144">See also</span></span>



[<span data-ttu-id="be3d9-145">IMAPIStatus::ValidateState</span><span class="sxs-lookup"><span data-stu-id="be3d9-145">IMAPIStatus::ValidateState</span></span>](imapistatus-validatestate.md)
  
[<span data-ttu-id="be3d9-146">IXPLogon::AddressTypes</span><span class="sxs-lookup"><span data-stu-id="be3d9-146">IXPLogon::AddressTypes</span></span>](ixplogon-addresstypes.md)
  
[<span data-ttu-id="be3d9-147">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="be3d9-147">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

