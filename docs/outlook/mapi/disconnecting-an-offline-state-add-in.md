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
# <a name="disconnecting-an-offline-state-add-in"></a>Отключение надстройки, позволяющей управлять автономным состоянием

**Область применения**: Outlook 2013 | Outlook 2016 
  
Если отключить надстройку, позволяющую управлять автономном состоянии, необходимо реализовать ряд функций для корректного прекращения работы и удаления надстройки. Дополнительные сведения о настройке и использовании надстройки, позволяющей управлять автономным состоянием, для отслеживания изменений состояния подключения см. в статье [Конфигурация надстройки, позволяющей управлять автономным состоянием,](setting-up-an-offline-state-add-in.md) и [Мониторинг изменений состояния подключения изменения с помощью надстройки, позволяющей управлять автономным состоянием](monitoring-connection-state-changes-using-an-offline-state-add-in.md).
  
В этой статье работа функций отключения, прекращения работы и очистки будет продемонстрирована с помощью примеров кода из примера надстройки, позволяющей управлять автономным состоянием. Пример надстройки, позволяющей управлять автономным состоянием, — это надстройка COM, добавляющее **автономное состояние ** в меню Outlook и использует API автономного режима. С помощью меню автономного состояния вы можете включать или отключать отслеживание состояния, проверять текущее состояние и изменять текущее состояние. Дополнительные сведения о скачивании и установке надстройки, позволяющей управлять автономным состоянием, см. в статье [Установка надстройки, позволяющей управлять автономным состоянием](installing-the-sample-offline-state-add-in.md). Дополнительные сведения об API автономного режима см. в статье [Об API автономного режима](about-the-offline-state-api.md).
  
## <a name="on-disconnection-routine"></a>Процесс отключения

Функция **IDTExtensibility2.OnDisconnection** вызывается при выгрузке надстройки, позволяющей управлять автономным состоянием. Вам необходимо добавить код очистки в эту функцию. В приведенном ниже примере функция  **IDTExtensibility2.OnDisconnection** вызывает `HrTermAddin`функцию 
  
### <a name="cmyaddinondisconnection-example"></a>CMyAddin::OnDisconnection() пример

```cpp
STDMETHODIMP CMyAddin::OnDisconnection(ext_DisconnectMode /*RemoveMode*/, SAFEARRAY * * /*custom*/) 
{ 
    Log(true,"OnDisconnection\n"); 
    HRESULT hRes = S_OK; 
    hRes = HrTermAddin(); 
     return hRes; 
}
```

## <a name="terminate-add-in-function"></a>Удаление функции надстройки

`HrTermAddin`Функция вызывает функции `inDeInitMonitor`, `HrRemoveMenuItems` и `UnloadLibraries` для завершения удаления надстройки, позволяющей управлять автономным состоянием. 
  
### <a name="cmyaddinhrtermaddin-example"></a>CMyAddin::HrTermAddin() пример

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

## <a name="deinitialize-monitor-routine"></a>Деинициализация мониторинга

`inDeInitMonitor`Функция вызывает функцию [IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md) для прекращения повторных вызовов для автономного объекта. 
  
### <a name="deinitmonitor-example"></a>DeInitMonitor() пример

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

## <a name="remove-menu-items-routine"></a>Процесс удаления элементов меню

`HrRemoveMenuItems` Функция вызывает `DispEventUnadvise` для каждого элемента меню **Автономное состояние**, а затем удаляет меню **Автономное состояние**. 
  
### <a name="cmyaddinhrremovemenuitems-example"></a>CMyAddin::HrRemoveMenuItems() пример

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

## <a name="unload-libraries-routine"></a>Процесс выгрузки библиотек

Когда надстройка будет выгружена из Outlook, функция `UnloadLibraries` выгружает динамически загружаемые библиотеки (DLL), которые использует надстройка. 
  
### <a name="unloadlibraries-example"></a>UnloadLibraries() пример

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

## <a name="see-also"></a>См. также

- [Об API автономного режима](about-the-offline-state-api.md)
- [Установка примера надстройки, позволяющей управлять автономным состоянием](installing-the-sample-offline-state-add-in.md)
- [О примере надстройки, позволяющей управлять автономным состоянием](about-the-sample-offline-state-add-in.md)
- [Конфигурация надстройки, позволяющей управлять автономным состоянием](setting-up-an-offline-state-add-in.md)
- [Отслеживание изменений состояния подключения с помощью надстройки, позволяющей управлять автономным состоянием](monitoring-connection-state-changes-using-an-offline-state-add-in.md)

