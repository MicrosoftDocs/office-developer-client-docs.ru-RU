---
title: Отсоединение надстройки, позволяющей управлять автономным состоянием
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 6922cb38-a9e3-e4a9-d4a3-e11b81fc77e2
description: '���� ���������� ���������: 7 ������� 2015 �.'
ms.openlocfilehash: 82f529f58a62f412ed8b25d1ceaf508463491612
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/15/2018
ms.locfileid: "19808296"
---
# <a name="disconnecting-an-offline-state-add-in"></a><span data-ttu-id="3ea3e-103">Отсоединение надстройки, позволяющей управлять автономным состоянием</span><span class="sxs-lookup"><span data-stu-id="3ea3e-103">Disconnecting an Offline State Add-in</span></span>

<span data-ttu-id="3ea3e-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3ea3e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3ea3e-105">При отключении добавить в автономном режиме, необходимо реализовать функции для правильного прерывания и очистка надстройки.</span><span class="sxs-lookup"><span data-stu-id="3ea3e-105">When the offline state add-in is disconnected, you must implement functions to properly terminate and clean up the add-in.</span></span> <span data-ttu-id="3ea3e-106">Дополнительные сведения о настройке и использованию автономной состояний надстройки для отслеживания изменений состояния подключения см [параметр копирование автономное состояние надстройки](setting-up-an-offline-state-add-in.md) и [Мониторинг подключения состояние изменений с помощью надстройки состояние не в сети](monitoring-connection-state-changes-using-an-offline-state-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="3ea3e-106">For more information on setting up and using the offline state add-in to monitor connection state changes, see [Setting Up an Offline State Add-in](setting-up-an-offline-state-add-in.md) and [Monitoring Connection State Changes Using an Offline State Add-in](monitoring-connection-state-changes-using-an-offline-state-add-in.md).</span></span>
  
<span data-ttu-id="3ea3e-107">В этом разделе, эти отключение прерывания и демонстрируются функции очистки с помощью примеры кода из надстройки пример состояние не в сети.</span><span class="sxs-lookup"><span data-stu-id="3ea3e-107">In this topic, these disconnection, terminate, and clean-up functions are demonstrated by using code examples from the Sample Offline State Add-in.</span></span> <span data-ttu-id="3ea3e-108">Добавить пример состояние не в сети в является надстройки COM, которая добавляет в меню **Состояния не в сети** в Outlook и использует автономный режим состояния API-Интерфейс.</span><span class="sxs-lookup"><span data-stu-id="3ea3e-108">The Sample Offline State Add-in is a COM add-in that adds an **Offline State** menu to Outlook and uses the Offline State API.</span></span> <span data-ttu-id="3ea3e-109">Через меню состояния не в сети можно включить или отключить мониторинг состояния, проверьте текущее состояние и изменения текущего состояния.</span><span class="sxs-lookup"><span data-stu-id="3ea3e-109">Through the Offline State menu, you can enable or disable state monitoring, check the current state, and change the current state.</span></span> <span data-ttu-id="3ea3e-110">Дополнительные сведения о загрузке и установке надстройки пример состояние не в сети содержатся в разделе [Установка надстройки пример состояние не в сети](installing-the-sample-offline-state-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="3ea3e-110">For more information about downloading and installing the Sample Offline State Add-in, see [Installing the Sample Offline State Add-in](installing-the-sample-offline-state-add-in.md).</span></span> <span data-ttu-id="3ea3e-111">Дополнительные сведения об автономном режиме состояние API [Об автономном режиме состояние API](about-the-offline-state-api.md)см.</span><span class="sxs-lookup"><span data-stu-id="3ea3e-111">For more information about the Offline State API, see [About the Offline State API](about-the-offline-state-api.md).</span></span>
  
## <a name="on-disconnection-routine"></a><span data-ttu-id="3ea3e-112">Для отключения подпрограммы</span><span class="sxs-lookup"><span data-stu-id="3ea3e-112">On Disconnection Routine</span></span>

<span data-ttu-id="3ea3e-113">Метод **IDTExtensibility2.OnDisconnection** вызывается при выгрузке надстройки состояние не в сети.</span><span class="sxs-lookup"><span data-stu-id="3ea3e-113">The **IDTExtensibility2.OnDisconnection** method is called when the Offline State Add-in is unloaded.</span></span> <span data-ttu-id="3ea3e-114">Необходимо реализовать Очистка кода в этой функции.</span><span class="sxs-lookup"><span data-stu-id="3ea3e-114">You should implement clean up code in this function.</span></span> <span data-ttu-id="3ea3e-115">В следующем примере, вызывает функцию **IDTExtensibility2.OnDisconnection** `HrTermAddin` функции.</span><span class="sxs-lookup"><span data-stu-id="3ea3e-115">In the following example, the **IDTExtensibility2.OnDisconnection** function calls the  `HrTermAddin` function.</span></span> 
  
### <a name="cmyaddinondisconnection-example"></a><span data-ttu-id="3ea3e-116">Пример CMyAddin::OnDisconnection()</span><span class="sxs-lookup"><span data-stu-id="3ea3e-116">CMyAddin::OnDisconnection() example</span></span>

```cpp
STDMETHODIMP CMyAddin::OnDisconnection(ext_DisconnectMode /*RemoveMode*/, SAFEARRAY * * /*custom*/) 
{ 
    Log(true,"OnDisconnection\n"); 
    HRESULT hRes = S_OK; 
    hRes = HrTermAddin(); 
     return hRes; 
}
```

## <a name="terminate-add-in-function"></a><span data-ttu-id="3ea3e-117">Завершение функция надстройки</span><span class="sxs-lookup"><span data-stu-id="3ea3e-117">Terminate Add-in Function</span></span>

<span data-ttu-id="3ea3e-118">`HrTermAddin` Вызовы функций `inDeInitMonitor`, `HrRemoveMenuItems`, и `UnloadLibraries` выполнение Очистка надстройки автономный функций.</span><span class="sxs-lookup"><span data-stu-id="3ea3e-118">The  `HrTermAddin` function calls the  `inDeInitMonitor`,  `HrRemoveMenuItems`, and  `UnloadLibraries` functions to finish cleaning up the Offline State Add-in.</span></span> 
  
### <a name="cmyaddinhrtermaddin-example"></a><span data-ttu-id="3ea3e-119">Пример CMyAddin::HrTermAddin()</span><span class="sxs-lookup"><span data-stu-id="3ea3e-119">CMyAddin::HrTermAddin() example</span></span>

```cpp
HRESULT CMyAddin::HrTermAddin() 
{ 
    HRESULT hRes = S_OK; 
    DeInitMonitor(); 
    hRes =  HrRemoveMenuItems(); 
    UnloadLibraries(); 
    return hRes; 
}
```

## <a name="deinitialize-monitor-routine"></a><span data-ttu-id="3ea3e-120">Deinitialize подпрограммы монитор</span><span class="sxs-lookup"><span data-stu-id="3ea3e-120">Deinitialize Monitor Routine</span></span>

<span data-ttu-id="3ea3e-121">`inDeInitMonitor` Функция вызывает функцию [IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md) для отмены обратных вызовов для автономного объекта.</span><span class="sxs-lookup"><span data-stu-id="3ea3e-121">The  `inDeInitMonitor` function calls the [IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md) function to cancel the callbacks for the offline object.</span></span> 
  
### <a name="deinitmonitor-example"></a><span data-ttu-id="3ea3e-122">Пример DeInitMonitor()</span><span class="sxs-lookup"><span data-stu-id="3ea3e-122">DeInitMonitor() example</span></span>

```cpp
void DeInitMonitor() 
{ 
Log(true,_T("Deinitializing Outlook Offline State Monitor\n")); 
HRESULT hRes = S_OK; 
if (g_lpOfflineMgr) 
{ 
hRes = g_lpOfflineMgr->Unadvise(MAPIOFFLINE_UNADVISE_DEFAULT, g_ulAdviseToken); 
g_lpOfflineMgr->Release(); 
g_lpOfflineMgr = NULL; 
g_ulAdviseToken = NULL; 
} 
}
```

## <a name="remove-menu-items-routine"></a><span data-ttu-id="3ea3e-123">Удаление подпрограммы элементы меню</span><span class="sxs-lookup"><span data-stu-id="3ea3e-123">Remove Menu Items Routine</span></span>

<span data-ttu-id="3ea3e-124">`HrRemoveMenuItems` Вызовы функций `DispEventUnadvise` для каждого элемента меню в группе меню **Состояния не в сети** , а затем удаляет меню **Состояния не в сети** .</span><span class="sxs-lookup"><span data-stu-id="3ea3e-124">The  `HrRemoveMenuItems` function calls  `DispEventUnadvise` for each menu item under the **Offline State** menu, and then deletes the **Offline State** menu.</span></span> 
  
### <a name="cmyaddinhrremovemenuitems-example"></a><span data-ttu-id="3ea3e-125">Пример CMyAddin::HrRemoveMenuItems()</span><span class="sxs-lookup"><span data-stu-id="3ea3e-125">CMyAddin::HrRemoveMenuItems() example</span></span>

```cpp
HRESULT CMyAddin::HrRemoveMenuItems() 
{     
    Log(true,"HrRemoveMenuItems\n"); 
    HRESULT hRes = S_OK; 
    if (m_fMenuItemsAdded) 
    { 
        try 
        { 
            if (m_spInitButton) 
            { 
                m_InitButtonHandler.DispEventUnadvise(m_spInitButton); 
            } 
            if (m_spDeinitButton) 
            { 
                m_DeinitButtonHandler.DispEventUnadvise(m_spDeinitButton); 
            } 
            if (m_spGetStateButton) 
            { 
                m_GetStateButtonHandler.DispEventUnadvise(m_spGetStateButton); 
            } 
            if (m_spSetStateButton) 
            { 
                m_SetStateButtonHandler.DispEventUnadvise(m_spSetStateButton); 
            } 
 
            m_spMyMenu->Delete(); 
        } 
        catch(_com_error) 
        { 
            hRes = E_FAIL; 
        } 
        if (SUCCEEDED(hRes)) 
        { 
            m_fMenuItemsAdded = false; 
        } 
    } 
    return hRes; 
}
```

## <a name="unload-libraries-routine"></a><span data-ttu-id="3ea3e-126">Процедуры Unload библиотек</span><span class="sxs-lookup"><span data-stu-id="3ea3e-126">Unload Libraries Routine</span></span>

<span data-ttu-id="3ea3e-127">При выгрузке из Outlook, надстройка `UnloadLibraries` функция выгружает библиотеки динамической компоновки (DLL), которые требуется добавить в.</span><span class="sxs-lookup"><span data-stu-id="3ea3e-127">When the add-in is unloaded from Outlook, the  `UnloadLibraries` function unloads the dynamic-link libraries (DLLs) that the add-in required.</span></span> 
  
### <a name="unloadlibraries-example"></a><span data-ttu-id="3ea3e-128">Пример UnloadLibraries()</span><span class="sxs-lookup"><span data-stu-id="3ea3e-128">UnloadLibraries() example</span></span>

```cpp
void UnloadLibraries() 
{ 
    Log(true,_T("UnloadLibraries - freeing modules\n")); 
    pfnHrOpenOfflineObj = NULL; 
    pfnMAPIFreeBuffer = NULL; 
    if (hModMSMAPI) FreeLibrary(hModMSMAPI); 
    hModMSMAPI = NULL; 
    if (hModMAPI) FreeLibrary(hModMAPI); 
    hModMAPI = NULL; 
    if (hModMAPIStub) FreeLibrary(hModMAPIStub); 
    hModMAPIStub = NULL; 
}
```

## <a name="see-also"></a><span data-ttu-id="3ea3e-129">См. также</span><span class="sxs-lookup"><span data-stu-id="3ea3e-129">See also</span></span>

- [<span data-ttu-id="3ea3e-130">Сведения об API автономного состояния</span><span class="sxs-lookup"><span data-stu-id="3ea3e-130">About the Offline State API</span></span>](about-the-offline-state-api.md)
- [<span data-ttu-id="3ea3e-131">Установка примера надстройки, позволяющей управлять автономным состоянием</span><span class="sxs-lookup"><span data-stu-id="3ea3e-131">Installing the Sample Offline State Add-in</span></span>](installing-the-sample-offline-state-add-in.md)
- [<span data-ttu-id="3ea3e-132">Сведения о примере надстройки с автономным состоянием</span><span class="sxs-lookup"><span data-stu-id="3ea3e-132">About the Sample Offline State Add-in</span></span>](about-the-sample-offline-state-add-in.md)
- [<span data-ttu-id="3ea3e-133">Конфигурация надстройки, позволяющей управлять автономным состоянием</span><span class="sxs-lookup"><span data-stu-id="3ea3e-133">Setting Up an Offline State Add-in</span></span>](setting-up-an-offline-state-add-in.md)
- [<span data-ttu-id="3ea3e-134">Отслеживание изменений состояния подключения с помощью надстройки, позволяющей управлять автономным состоянием</span><span class="sxs-lookup"><span data-stu-id="3ea3e-134">Monitoring Connection State Changes Using an Offline State Add-in</span></span>](monitoring-connection-state-changes-using-an-offline-state-add-in.md)

