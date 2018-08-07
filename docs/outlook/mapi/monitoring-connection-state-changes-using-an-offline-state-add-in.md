---
title: Мониторинг изменения состояния подключения с помощью надстройки автономный режим
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: c482ddce-f2b6-222b-aa30-824b1c6f3b14
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 9f7f3bc0e305fb5aa7d6ae1e1909b573b3376ef8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810020"
---
# <a name="monitoring-connection-state-changes-using-an-offline-state-add-in"></a><span data-ttu-id="8c299-103">Мониторинг изменения состояния подключения с помощью надстройки автономный режим</span><span class="sxs-lookup"><span data-stu-id="8c299-103">Monitoring connection state changes using an offline state add-in</span></span>

<span data-ttu-id="8c299-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8c299-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8c299-105">Прежде чем использовать автономное состояние add-in для отслеживания изменений состояния подключения, необходимо реализовать функции для установки и инициализации надстройки.</span><span class="sxs-lookup"><span data-stu-id="8c299-105">Before you can use an offline state add-in to monitor connection state changes, you must implement functions to set up and initialize the add-in.</span></span> <span data-ttu-id="8c299-106">Для получения дополнительных сведений см [параметр копирование автономно состояние надстройки](setting-up-an-offline-state-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="8c299-106">For more information, see [Setting Up an Offline State Add-in](setting-up-an-offline-state-add-in.md).</span></span>
  
<span data-ttu-id="8c299-107">После настройки надстройки автономное состояние, необходимо использовать функцию **[HrOpenOfflineObj](hropenofflineobj.md)** для получения автономного объекта.</span><span class="sxs-lookup"><span data-stu-id="8c299-107">After you set up the offline state add-in, you must use the **[HrOpenOfflineObj](hropenofflineobj.md)** function to obtain an offline object.</span></span> <span data-ttu-id="8c299-108">С помощью этой автономной объекта, можно инициализировать мониторе состояния и получить и установить для текущего состояния.</span><span class="sxs-lookup"><span data-stu-id="8c299-108">Using this offline object, you can initialize your state monitor, and then get and set the current state.</span></span> 
  
<span data-ttu-id="8c299-109">В этом разделе демонстрируются эти функции мониторинга состояния с помощью примеры кода из надстройки пример состояние не в сети.</span><span class="sxs-lookup"><span data-stu-id="8c299-109">In this topic, these state monitoring functions are demonstrated by using code examples from the Sample Offline State Add-in.</span></span> <span data-ttu-id="8c299-110">Надстройки пример состояние не в сети — это надстройка COM, который добавляет меню **Состояния не в сети** в Outlook и использует автономный режим состояния API.</span><span class="sxs-lookup"><span data-stu-id="8c299-110">The Sample Offline State Add-in is a COM add-in that adds an **Offline State** menu to Outlook and utilizes the Offline State API.</span></span> <span data-ttu-id="8c299-111">Через меню **Состояния не в сети** можно включить или отключить мониторинг состояния, проверьте текущее состояние и изменения текущего состояния.</span><span class="sxs-lookup"><span data-stu-id="8c299-111">Through the **Offline State** menu, you can enable or disable state monitoring, check the current state, and change the current state.</span></span> <span data-ttu-id="8c299-112">Дополнительные сведения о загрузке и установке надстройки пример состояние не в сети содержатся в разделе [Установка надстройки пример состояние не в сети](installing-the-sample-offline-state-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="8c299-112">For more information about downloading and installing the Sample Offline State Add-in, see [Installing the Sample Offline State Add-in](installing-the-sample-offline-state-add-in.md).</span></span> <span data-ttu-id="8c299-113">Дополнительные сведения об автономном режиме состояние API [Об автономном режиме состояние API](about-the-offline-state-api.md)см.</span><span class="sxs-lookup"><span data-stu-id="8c299-113">For more information about the Offline State API, see [About the Offline State API](about-the-offline-state-api.md).</span></span>
  
<span data-ttu-id="8c299-114">При отключении добавить в автономном режиме, необходимо реализовать функции для правильного прерывания и очистка надстройки.</span><span class="sxs-lookup"><span data-stu-id="8c299-114">When the offline state add-in is disconnected, you must implement functions to properly terminate and clean up the add-in.</span></span> <span data-ttu-id="8c299-115">Для получения дополнительных сведений см [отключение надстройки состояние не в сети](disconnecting-an-offline-state-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="8c299-115">For more information, see [Disconnecting an Offline State Add-in](disconnecting-an-offline-state-add-in.md).</span></span>
  
## <a name="open-offline-object-routine"></a><span data-ttu-id="8c299-116">Открыть автономный режим объекта общей процедуры</span><span class="sxs-lookup"><span data-stu-id="8c299-116">Open Offline Object routine</span></span>

<span data-ttu-id="8c299-117">Для клиента для получения уведомлений об изменении состояния подключения необходимо вызвать функцию **[HrOpenOfflineObj](hropenofflineobj.md)** .</span><span class="sxs-lookup"><span data-stu-id="8c299-117">For the client to be notified when a connection state change occurs, you must call the **[HrOpenOfflineObj](hropenofflineobj.md)** function.</span></span> <span data-ttu-id="8c299-118">Эта функция открывает автономного объекта, который поддерживает **[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**.</span><span class="sxs-lookup"><span data-stu-id="8c299-118">This function opens an offline object that supports **[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**.</span></span> <span data-ttu-id="8c299-119">Функция **HrOpenOfflineObj** определяется в файле заголовка ConnectionState.h.</span><span class="sxs-lookup"><span data-stu-id="8c299-119">The **HrOpenOfflineObj** function is defined in the ConnectionState.h header file.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="8c299-120">Функция **HrOpenOfflineObj** объявляется в файле заголовка ImportProcs.h следующим образом: `extern HROPENOFFLINEOBJ* pfnHrOpenOfflineObj;`.</span><span class="sxs-lookup"><span data-stu-id="8c299-120">The **HrOpenOfflineObj** function is declared in the ImportProcs.h header file as follows:  `extern HROPENOFFLINEOBJ* pfnHrOpenOfflineObj;`.</span></span> 
  
### <a name="hropenofflineobj-example"></a><span data-ttu-id="8c299-121">Пример HrOpenOfflineObj</span><span class="sxs-lookup"><span data-stu-id="8c299-121">HrOpenOfflineObj example</span></span>

```cpp
typedef HRESULT (STDMETHODCALLTYPE HROPENOFFLINEOBJ)( 
    ULONG ulFlags, 
    LPCWSTR pwszProfileName, 
    const GUID* pGUID, 
    const GUID* pInstance, 
    IMAPIOfflineMgr** ppOffline 
);
```

## <a name="initialize-monitor-routine"></a><span data-ttu-id="8c299-122">Инициализация подпрограммы монитор</span><span class="sxs-lookup"><span data-stu-id="8c299-122">Initialize Monitor routine</span></span>

<span data-ttu-id="8c299-123">`InitMonitor` Функция вызывает функцию **HrOpenOfflineObj** .</span><span class="sxs-lookup"><span data-stu-id="8c299-123">The  `InitMonitor` function calls the **HrOpenOfflineObj** function.</span></span> <span data-ttu-id="8c299-124">`InitMonitor` Функция вызывает **CMyOfflineNotify** , поэтому Outlook можно отправлять уведомления обратного вызова для клиента и регистрирует обратного вызова через переменную **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** `AdviseInfo`.</span><span class="sxs-lookup"><span data-stu-id="8c299-124">The  `InitMonitor` function calls **CMyOfflineNotify** so that Outlook can send callback notifications to the client, and registers the callback through the **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** variable  `AdviseInfo`.</span></span>
  
### <a name="initmonitor-example"></a><span data-ttu-id="8c299-125">Пример InitMonitor()</span><span class="sxs-lookup"><span data-stu-id="8c299-125">InitMonitor() example</span></span>

```cpp
void InitMonitor(LPCWSTR szProfile) 
{ 
    if (!szProfile) return; 
    Log(true,_T("Initializing Outlook Offline State Monitor\n")); 
    HRESULT hRes = S_OK; 
 
    if (g_lpOfflineMgr) 
    { 
        Log(true,_T("Already initialized\n")); 
        return; 
    } 
     
    if (pfnHrOpenOfflineObj) 
    { 
        if (g_lpOfflineMgr) DeInitMonitor(); 
        Log(true,_T("Calling HrOpenOfflineObj for \"%ws\"\n"),szProfile); 
        hRes = pfnHrOpenOfflineObj( 
            NULL, 
            szProfile, 
            &GUID_GlobalState, 
            NULL, 
            &g_lpOfflineMgr); 
        if (FAILED(hRes))  
        { 
            Log(true,_T("HrOpenOfflineObj failed: 0x%08X\n"),hRes); 
        } 
        if (g_lpOfflineMgr) 
        { 
            IMAPIOffline* lpOffline = NULL; 
            hRes = g_lpOfflineMgr->QueryInterface(IID_IMAPIOffline,(LPVOID*)&lpOffline); 
             
            if (lpOffline) 
            { 
                ULONG ulCap = NULL; 
                hRes = lpOffline->GetCapabilities(&ulCap); 
                 
                if (ulCap & MAPIOFFLINE_CAPABILITY_OFFLINE) Log(true,_T("MAPIOFFLINE_CAPABILITY_OFFLINE supported\n")); 
                if (ulCap & MAPIOFFLINE_CAPABILITY_ONLINE) Log(true,_T("MAPIOFFLINE_CAPABILITY_ONLINE supported\n")); 
                 
                if (ulCap & (MAPIOFFLINE_CAPABILITY_OFFLINE | MAPIOFFLINE_CAPABILITY_ONLINE)) 
                { 
                    CMyOfflineNotify* lpImplNotify = new CMyOfflineNotify(); 
                     
                    if (lpImplNotify) 
                    { 
                        MAPIOFFLINE_ADVISEINFO AdviseInfo = {0}; 
                        AdviseInfo.ulSize = sizeof(MAPIOFFLINE_ADVISEINFO); 
                        AdviseInfo.ulClientToken = 0;// something you want to get handed back when you get the notification 
                        AdviseInfo.CallbackType = MAPIOFFLINE_CALLBACK_TYPE_NOTIFY; 
                        AdviseInfo.pCallback = lpImplNotify; 
                        AdviseInfo.ulAdviseTypes = MAPIOFFLINE_ADVISE_TYPE_STATECHANGE; 
                        AdviseInfo.ulStateMask = MAPIOFFLINE_STATE_ALL; 
                         
                        hRes = g_lpOfflineMgr->Advise(MAPIOFFLINE_ADVISE_DEFAULT, &AdviseInfo, &g_ulAdviseToken); 
                        Log(true,"ulAdviseToken = 0x%08X\n",g_ulAdviseToken); 
                    } 
                } 
                lpOffline->Release(); 
            }                 
        } 
    } 
}
```

## <a name="get-current-state-routine"></a><span data-ttu-id="8c299-126">Процедура Get текущее состояние</span><span class="sxs-lookup"><span data-stu-id="8c299-126">Get Current State routine</span></span>

<span data-ttu-id="8c299-127">`GetCurrentState` Функция вызывает функцию **HrOpenOfflineObj** , а затем использует объект автономной для получения текущего состояния подключения.</span><span class="sxs-lookup"><span data-stu-id="8c299-127">The  `GetCurrentState` function calls the **HrOpenOfflineObj** function, and then uses the offline object to get the current connection state.</span></span> <span data-ttu-id="8c299-128">Текущее состояние возвращается в `ulCurState` переменной, которая используется в `CButtonEventHandler::Click` функцию, чтобы отобразить текущее состояние для пользователя.</span><span class="sxs-lookup"><span data-stu-id="8c299-128">The current state is returned in the  `ulCurState` variable, which is used in the  `CButtonEventHandler::Click` function to display the current state to the user.</span></span> 
  
### <a name="getcurrentstate-example"></a><span data-ttu-id="8c299-129">Пример GetCurrentState()</span><span class="sxs-lookup"><span data-stu-id="8c299-129">GetCurrentState() example</span></span>

```cpp
ULONG (LPCWSTR szProfile) 
{ 
    if (!szProfile) return 0; 
    Log(true,_T("Getting Current Offline State\n")); 
    HRESULT hRes = S_OK; 
    ULONG ulCurState = NULL; 
 
    if (pfnHrOpenOfflineObj) 
    { 
        if (g_lpOfflineMgr) DeInitMonitor(); 
        Log(true,_T("Calling HrOpenOfflineObj for \"%ws\"\n"),szProfile); 
        hRes = pfnHrOpenOfflineObj( 
            NULL, 
            szProfile, 
            &GUID_GlobalState, 
            NULL, 
            &g_lpOfflineMgr); 
        if (FAILED(hRes))  
        { 
            Log(true,_T("HrOpenOfflineObj failed: 0x%08X\n"),hRes); 
        } 
        if (g_lpOfflineMgr) 
        { 
            IMAPIOffline* lpOffline = NULL; 
            hRes = g_lpOfflineMgr->QueryInterface(IID_IMAPIOffline,(LPVOID*)&lpOffline); 
             
            if (lpOffline) 
            { 
                hRes = lpOffline->GetCurrentState(&ulCurState); 
                Log(true,_T("GetCurrentState returned 0x%08X\n"),hRes); 
 
                switch(ulCurState) 
                { 
                case MAPIOFFLINE_STATE_ONLINE: 
                    Log(true,_T("Current state is MAPIOFFLINE_STATE_ONLINE\n")); 
                    break; 
                case MAPIOFFLINE_STATE_OFFLINE: 
                    Log(true,_T("Current state is MAPIOFFLINE_STATE_OFFLINE\n")); 
                    break; 
                default: 
                    Log(true,_T("Current state is 0x%0X\n"),ulCurState); 
                } 
                lpOffline->Release(); 
            } 
        } 
    } 
    return ulCurState; 
}
```

## <a name="set-current-state-routine"></a><span data-ttu-id="8c299-130">Процедура Set текущее состояние</span><span class="sxs-lookup"><span data-stu-id="8c299-130">Set Current State routine</span></span>

<span data-ttu-id="8c299-131">`SetCurrentState` Функция вызывает функцию **HrOpenOfflineObj** , а затем использует объект автономной Установка текущего состояния подключения.</span><span class="sxs-lookup"><span data-stu-id="8c299-131">The  `SetCurrentState` function calls the **HrOpenOfflineObj** function, and then uses the offline object to set the current connection state.</span></span> <span data-ttu-id="8c299-132">`CButtonEventHandler::Click` Вызовы функций `SetCurrentState` функции и новое состояние передается в `ulState` переменной.</span><span class="sxs-lookup"><span data-stu-id="8c299-132">The  `CButtonEventHandler::Click` function calls the  `SetCurrentState` function and the new state is passed in through the  `ulState` variable.</span></span> 
  
### <a name="setcurrentstate-example"></a><span data-ttu-id="8c299-133">Пример SetCurrentState()</span><span class="sxs-lookup"><span data-stu-id="8c299-133">SetCurrentState() example</span></span>

```cpp
HRESULT SetCurrentState(LPCWSTR szProfile, ULONG ulFlags, ULONG ulState) 
{ 
    if (!szProfile) return 0; 
    Log(true,_T("Setting Current Offline State\n")); 
    HRESULT hRes = S_OK; 
 
    if (pfnHrOpenOfflineObj) 
    { 
        if (g_lpOfflineMgr) DeInitMonitor(); 
        Log(true,_T("Calling HrOpenOfflineObj for \"%ws\"\n"),szProfile); 
        hRes = pfnHrOpenOfflineObj( 
            NULL, 
            szProfile, 
            &GUID_GlobalState, 
            NULL, 
            &g_lpOfflineMgr); 
        if (FAILED(hRes))  
        { 
            Log(true,_T("HrOpenOfflineObj failed: 0x%08X\n"),hRes); 
        } 
        if (g_lpOfflineMgr) 
        { 
            IMAPIOffline* lpOffline = NULL; 
            hRes = g_lpOfflineMgr->QueryInterface(IID_IMAPIOffline,(LPVOID*)&lpOffline); 
             
            if (lpOffline) 
            { 
                switch(ulFlags) 
                { 
                case MAPIOFFLINE_FLAG_BLOCK: 
                    Log(true,_T("Flag used: MAPIOFFLINE_FLAG_BLOCK\n")); 
                    break; 
                case MAPIOFFLINE_FLAG_DEFAULT: 
                    Log(true,_T("Flag used: MAPIOFFLINE_FLAG_DEFAULT\n")); 
                    break; 
                default: 
                    Log(true,_T("Flag used: 0x%0X\n"),ulFlags); 
                } 
                switch(ulState) 
                { 
                case MAPIOFFLINE_STATE_ONLINE: 
                    Log(true,_T("New state will be MAPIOFFLINE_STATE_ONLINE\n")); 
                    break; 
                case MAPIOFFLINE_STATE_OFFLINE: 
                    Log(true,_T("New state will be MAPIOFFLINE_STATE_OFFLINE\n")); 
                    break; 
                default: 
                    Log(true,_T("New state will be 0x%0X\n"),ulState); 
                } 
                hRes = lpOffline->SetCurrentState(ulFlags, MAPIOFFLINE_STATE_OFFLINE_MASK,ulState,NULL); 
                Log(true,_T("SetCurrentState returned 0x%08X\n"),hRes); 
                 
                lpOffline->Release(); 
            } 
        } 
    } 
    return hRes; 
}
```

## <a name="notification-routine"></a><span data-ttu-id="8c299-134">Процедура уведомлений</span><span class="sxs-lookup"><span data-stu-id="8c299-134">Notification routine</span></span>

<span data-ttu-id="8c299-135">Функция **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)** используется Outlook для отправки уведомлений в клиент при внесении изменений в состоянии подключения.</span><span class="sxs-lookup"><span data-stu-id="8c299-135">The **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)** function is used by Outlook to send notifications to a client when there are changes in the connection state.</span></span> 
  
### <a name="cmyofflinenotifynotify-example"></a><span data-ttu-id="8c299-136">Пример CMyOfflineNotify::Notify()</span><span class="sxs-lookup"><span data-stu-id="8c299-136">CMyOfflineNotify::Notify() example</span></span>

```cpp
void CMyOfflineNotify::Notify(const MAPIOFFLINE_NOTIFY *pNotifyInfo) 
{ 
    Log(true,_T("CMyOfflineNotify::Notify\n")); 
    if    (pNotifyInfo == NULL) 
    {     
        Log(true,_T("pNotifyInfo is NULL\n")); 
    } 
    else 
    { 
        Log(true,_T("pNotifyInfo->ulSize == 0x%0X\n"),pNotifyInfo->ulSize); 
        switch(pNotifyInfo->NotifyType) 
        { 
            case    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE: 
                Log(true,_T("pNotifyInfo->NotifyType == MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE\n")); 
                break; 
            case    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START: 
                Log(true,_T("pNotifyInfo->NotifyType == MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START\n")); 
                break; 
            case    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE: 
                Log(true,_T("pNotifyInfo->NotifyType == MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE\n")); 
                break; 
            default: 
                Log(true,_T("pNotifyInfo->NotifyType == 0x%08X\n"),pNotifyInfo->NotifyType); 
        } 
        Log(true,_T("pNotifyInfo->ulClientToken == 0x%0X\n"),pNotifyInfo->ulClientToken); 
        switch(pNotifyInfo->Info.StateChange.ulMask) 
        { 
            case    MAPIOFFLINE_STATE_OFFLINE_MASK: 
                Log(true,_T("pNotifyInfo->Info.StateChange.ulMask == MAPIOFFLINE_STATE_OFFLINE_MASK\n")); 
                break; 
            default: 
                Log(true,_T("pNotifyInfo->Info.StateChange.ulMask == 0x%0X\n"),pNotifyInfo->Info.StateChange.ulMask); 
        } 
        switch(pNotifyInfo->Info.StateChange.ulStateOld) 
        { 
            case    MAPIOFFLINE_STATE_ONLINE: 
                Log(true,_T("pNotifyInfo->Info.StateChange.ulStateOld == MAPIOFFLINE_STATE_ONLINE\n")); 
                break; 
            case    MAPIOFFLINE_STATE_OFFLINE: 
                Log(true,_T("pNotifyInfo->Info.StateChange.ulStateOld == MAPIOFFLINE_STATE_OFFLINE\n")); 
                break; 
            default: 
                Log(true,_T("pNotifyInfo->Info.StateChange.ulStateOld == 0x%0X\n"),pNotifyInfo->Info.StateChange.ulStateOld); 
        } 
        switch(pNotifyInfo->Info.StateChange.ulStateNew) 
        { 
            case    MAPIOFFLINE_STATE_ONLINE: 
                Log(true,_T("pNotifyInfo->Info.StateChange.ulStateNew == MAPIOFFLINE_STATE_ONLINE\n")); 
                break; 
            case    MAPIOFFLINE_STATE_OFFLINE: 
                Log(true,_T("pNotifyInfo->Info.StateChange.ulStateNew == MAPIOFFLINE_STATE_OFFLINE\n")); 
                break; 
            default: 
                Log(true,_T("pNotifyInfo->Info.StateChange.ulStateNew == 0x%0X\n"),pNotifyInfo->Info.StateChange.ulStateNew); 
        } 
    } 
    return; 
}
```

## <a name="see-also"></a><span data-ttu-id="8c299-137">См. также</span><span class="sxs-lookup"><span data-stu-id="8c299-137">See also</span></span>

- [<span data-ttu-id="8c299-138">Сведения об API автономного состояния</span><span class="sxs-lookup"><span data-stu-id="8c299-138">About the Offline State API</span></span>](about-the-offline-state-api.md)
- [<span data-ttu-id="8c299-139">Установка примера надстройки, позволяющей управлять автономным состоянием</span><span class="sxs-lookup"><span data-stu-id="8c299-139">Installing the Sample Offline State Add-in</span></span>](installing-the-sample-offline-state-add-in.md)
- [<span data-ttu-id="8c299-140">Сведения о примере надстройки с автономным состоянием</span><span class="sxs-lookup"><span data-stu-id="8c299-140">About the Sample Offline State Add-in</span></span>](about-the-sample-offline-state-add-in.md)
- [<span data-ttu-id="8c299-141">Конфигурация надстройки, позволяющей управлять автономным состоянием</span><span class="sxs-lookup"><span data-stu-id="8c299-141">Setting Up an Offline State Add-in</span></span>](setting-up-an-offline-state-add-in.md)
- [<span data-ttu-id="8c299-142">Отсоединение надстройки, позволяющей управлять автономным состоянием</span><span class="sxs-lookup"><span data-stu-id="8c299-142">Disconnecting an Offline State Add-in</span></span>](disconnecting-an-offline-state-add-in.md)

