---
title: Отключение надстройки, позволяющей управлять автономным состоянием
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 6922cb38-a9e3-e4a9-d4a3-e11b81fc77e2
description: 'Дата последнего изменения: 7 декабря 2015 года'
ms.openlocfilehash: ce25c6777c8a71da0fe11e0bbf34eefafe2ca50d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564138"
---
# <a name="disconnecting-an-offline-state-add-in"></a><span data-ttu-id="40188-103">Отключение надстройки, позволяющей управлять автономным состоянием</span><span class="sxs-lookup"><span data-stu-id="40188-103">Disconnecting an Offline State Add-in</span></span>

<span data-ttu-id="40188-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="40188-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="40188-105">Если отключить надстройку, позволяющую управлять автономном состоянии, необходимо реализовать ряд функций для корректного прекращения работы и удаления надстройки.</span><span class="sxs-lookup"><span data-stu-id="40188-105">When the offline state add-in is disconnected, you must implement functions to properly terminate and clean up the add-in.</span></span> <span data-ttu-id="40188-106">Дополнительные сведения о настройке и использовании надстройки, позволяющей управлять автономным состоянием, для отслеживания изменений состояния подключения см. в статье [Конфигурация надстройки, позволяющей управлять автономным состоянием,](setting-up-an-offline-state-add-in.md) и [Мониторинг изменений состояния подключения изменения с помощью надстройки, позволяющей управлять автономным состоянием](monitoring-connection-state-changes-using-an-offline-state-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="40188-106">For more information on setting up and using the offline state add-in to monitor connection state changes, see [Setting Up an Offline State Add-in](setting-up-an-offline-state-add-in.md) and [Monitoring Connection State Changes Using an Offline State Add-in](monitoring-connection-state-changes-using-an-offline-state-add-in.md).</span></span>
  
<span data-ttu-id="40188-107">В этой статье работа функций отключения, прекращения работы и очистки будет продемонстрирована с помощью примеров кода из примера надстройки, позволяющей управлять автономным состоянием.</span><span class="sxs-lookup"><span data-stu-id="40188-107">In this topic, these disconnection, terminate, and clean-up functions are demonstrated by using code examples from the Sample Offline State Add-in.</span></span> <span data-ttu-id="40188-108">Пример надстройки, позволяющей управлять автономным состоянием, — это надстройка COM, добавляющее \*\*автономное состояние \*\* в меню Outlook и использует API автономного режима.</span><span class="sxs-lookup"><span data-stu-id="40188-108">The Sample Offline State Add-in is a COM add-in that adds an **Offline State** menu to Outlook and uses the Offline State API.</span></span> <span data-ttu-id="40188-109">С помощью меню автономного состояния вы можете включать или отключать отслеживание состояния, проверять текущее состояние и изменять текущее состояние.</span><span class="sxs-lookup"><span data-stu-id="40188-109">Through the Offline State menu, you can enable or disable state monitoring, check the current state, and change the current state.</span></span> <span data-ttu-id="40188-110">Дополнительные сведения о скачивании и установке надстройки, позволяющей управлять автономным состоянием, см. в статье [Установка надстройки, позволяющей управлять автономным состоянием](installing-the-sample-offline-state-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="40188-110">For more information about downloading and installing the Sample Offline State Add-in, see [Installing the Sample Offline State Add-in](installing-the-sample-offline-state-add-in.md).</span></span> <span data-ttu-id="40188-111">Дополнительные сведения об API автономного режима см. в статье [Об API автономного режима](about-the-offline-state-api.md).</span><span class="sxs-lookup"><span data-stu-id="40188-111">For more information about the Offline State API, see [About the Offline State API](about-the-offline-state-api.md).</span></span>
  
## <a name="on-disconnection-routine"></a><span data-ttu-id="40188-112">Процесс отключения</span><span class="sxs-lookup"><span data-stu-id="40188-112">On Disconnection Routine</span></span>

<span data-ttu-id="40188-113">Функция **IDTExtensibility2.OnDisconnection** вызывается при выгрузке надстройки, позволяющей управлять автономным состоянием.</span><span class="sxs-lookup"><span data-stu-id="40188-113">The **IDTExtensibility2.OnDisconnection** method is called when the Offline State Add-in is unloaded.</span></span> <span data-ttu-id="40188-114">Вам необходимо добавить код очистки в эту функцию.</span><span class="sxs-lookup"><span data-stu-id="40188-114">You should implement clean up code in this function.</span></span> <span data-ttu-id="40188-115">В приведенном ниже примере функция  **IDTExtensibility2.OnDisconnection** вызывает `HrTermAddin`функцию</span><span class="sxs-lookup"><span data-stu-id="40188-115">In the following example, the **IDTExtensibility2.OnDisconnection** function calls the  `HrTermAddin` function.</span></span> 
  
### <a name="cmyaddinondisconnection-example"></a><span data-ttu-id="40188-116">CMyAddin::OnDisconnection() пример</span><span class="sxs-lookup"><span data-stu-id="40188-116">CMyAddin::OnDisconnection() example</span></span>

```cpp
STDMETHODIMP CMyAddin::OnDisconnection(ext_DisconnectMode /*RemoveMode*/, SAFEARRAY * * /*custom*/) 
{ 
    Log(true,"OnDisconnection\n"); 
    HRESULT hRes = S_OK; 
    hRes = HrTermAddin(); 
     return hRes; 
}
```

## <a name="terminate-add-in-function"></a><span data-ttu-id="40188-117">Удаление функции надстройки</span><span class="sxs-lookup"><span data-stu-id="40188-117">Terminate Add-in Function</span></span>

<span data-ttu-id="40188-118">`HrTermAddin`Функция вызывает функции `inDeInitMonitor`, `HrRemoveMenuItems` и `UnloadLibraries` для завершения удаления надстройки, позволяющей управлять автономным состоянием.</span><span class="sxs-lookup"><span data-stu-id="40188-118">The  `HrTermAddin` function calls the  `inDeInitMonitor`,  `HrRemoveMenuItems`, and  `UnloadLibraries` functions to finish cleaning up the Offline State Add-in.</span></span> 
  
### <a name="cmyaddinhrtermaddin-example"></a><span data-ttu-id="40188-119">CMyAddin::HrTermAddin() пример</span><span class="sxs-lookup"><span data-stu-id="40188-119">CMyAddin::HrTermAddin() example</span></span>

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

## <a name="deinitialize-monitor-routine"></a><span data-ttu-id="40188-120">Деинициализация мониторинга</span><span class="sxs-lookup"><span data-stu-id="40188-120">Deinitialize Monitor Routine</span></span>

<span data-ttu-id="40188-121">`inDeInitMonitor`Функция вызывает функцию [IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md) для прекращения повторных вызовов для автономного объекта.</span><span class="sxs-lookup"><span data-stu-id="40188-121">The  `inDeInitMonitor` function calls the [IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md) function to cancel the callbacks for the offline object.</span></span> 
  
### <a name="deinitmonitor-example"></a><span data-ttu-id="40188-122">DeInitMonitor() пример</span><span class="sxs-lookup"><span data-stu-id="40188-122">DeInitMonitor() example</span></span>

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

## <a name="remove-menu-items-routine"></a><span data-ttu-id="40188-123">Процесс удаления элементов меню</span><span class="sxs-lookup"><span data-stu-id="40188-123">Remove Menu Items Routine</span></span>

<span data-ttu-id="40188-124">`HrRemoveMenuItems` Функция вызывает `DispEventUnadvise` для каждого элемента меню **Автономное состояние**, а затем удаляет меню **Автономное состояние**.</span><span class="sxs-lookup"><span data-stu-id="40188-124">The  `HrRemoveMenuItems` function calls  `DispEventUnadvise` for each menu item under the **Offline State** menu, and then deletes the **Offline State** menu.</span></span> 
  
### <a name="cmyaddinhrremovemenuitems-example"></a><span data-ttu-id="40188-125">CMyAddin::HrRemoveMenuItems() пример</span><span class="sxs-lookup"><span data-stu-id="40188-125">CMyAddin::HrRemoveMenuItems() example</span></span>

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

## <a name="unload-libraries-routine"></a><span data-ttu-id="40188-126">Процесс выгрузки библиотек</span><span class="sxs-lookup"><span data-stu-id="40188-126">Unload Libraries Routine</span></span>

<span data-ttu-id="40188-127">Когда надстройка будет выгружена из Outlook, функция `UnloadLibraries` выгружает динамически загружаемые библиотеки (DLL), которые использует надстройка.</span><span class="sxs-lookup"><span data-stu-id="40188-127">When the add-in is unloaded from Outlook, the  `UnloadLibraries` function unloads the dynamic-link libraries (DLLs) that the add-in required.</span></span> 
  
### <a name="unloadlibraries-example"></a><span data-ttu-id="40188-128">UnloadLibraries() пример</span><span class="sxs-lookup"><span data-stu-id="40188-128">UnloadLibraries() example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="40188-129">См. также</span><span class="sxs-lookup"><span data-stu-id="40188-129">See also</span></span>

- [<span data-ttu-id="40188-130">Об API автономного режима</span><span class="sxs-lookup"><span data-stu-id="40188-130">About the Offline State API</span></span>](about-the-offline-state-api.md)
- [<span data-ttu-id="40188-131">Установка примера надстройки, позволяющей управлять автономным состоянием</span><span class="sxs-lookup"><span data-stu-id="40188-131">Installing the sample Offline State add-in</span></span>](installing-the-sample-offline-state-add-in.md)
- [<span data-ttu-id="40188-132">О примере надстройки, позволяющей управлять автономным состоянием</span><span class="sxs-lookup"><span data-stu-id="40188-132">About the sample Offline State add-in</span></span>](about-the-sample-offline-state-add-in.md)
- [<span data-ttu-id="40188-133">Конфигурация надстройки, позволяющей управлять автономным состоянием</span><span class="sxs-lookup"><span data-stu-id="40188-133">Setting up an Offline State add-in</span></span>](setting-up-an-offline-state-add-in.md)
- [<span data-ttu-id="40188-134">Отслеживание изменений состояния подключения с помощью надстройки, позволяющей управлять автономным состоянием</span><span class="sxs-lookup"><span data-stu-id="40188-134">Monitoring connection state changes using an Offline State add-in</span></span>](monitoring-connection-state-changes-using-an-offline-state-add-in.md)

