---
title: Отключение автономного состояния надстройке
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
# <a name="disconnecting-an-offline-state-add-in"></a>Отключение автономного состояния надстройке

**Применимо к**: Outlook 
  
При отключении добавить в автономном режиме, необходимо реализовать функции для правильного прерывания и очистка надстройки. Дополнительные сведения о настройке и использованию автономной состояний надстройки для отслеживания изменений состояния подключения см [параметр копирование автономное состояние надстройки](setting-up-an-offline-state-add-in.md) и [Мониторинг подключения состояние изменений с помощью надстройки состояние не в сети](monitoring-connection-state-changes-using-an-offline-state-add-in.md).
  
В этом разделе, эти отключение прерывания и демонстрируются функции очистки с помощью примеры кода из надстройки пример состояние не в сети. Добавить пример состояние не в сети в является надстройки COM, которая добавляет в меню **Состояния не в сети** в Outlook и использует автономный режим состояния API-Интерфейс. Через меню состояния не в сети можно включить или отключить мониторинг состояния, проверьте текущее состояние и изменения текущего состояния. Дополнительные сведения о загрузке и установке надстройки пример состояние не в сети содержатся в разделе [Установка надстройки пример состояние не в сети](installing-the-sample-offline-state-add-in.md). Дополнительные сведения об автономном режиме состояние API [Об автономном режиме состояние API](about-the-offline-state-api.md)см.
  
## <a name="on-disconnection-routine"></a>Для отключения подпрограммы

Метод **IDTExtensibility2.OnDisconnection** вызывается при выгрузке надстройки состояние не в сети. Необходимо реализовать Очистка кода в этой функции. В следующем примере, вызывает функцию **IDTExtensibility2.OnDisconnection** `HrTermAddin` функции. 
  
### <a name="cmyaddinondisconnection-example"></a>Пример CMyAddin::OnDisconnection()

```cpp
STDMETHODIMP CMyAddin::OnDisconnection(ext_DisconnectMode /*RemoveMode*/, SAFEARRAY * * /*custom*/) 
{ 
    Log(true,"OnDisconnection\n"); 
    HRESULT hRes = S_OK; 
    hRes = HrTermAddin(); 
     return hRes; 
}
```

## <a name="terminate-add-in-function"></a>Завершение функция надстройки

`HrTermAddin` Вызовы функций `inDeInitMonitor`, `HrRemoveMenuItems`, и `UnloadLibraries` выполнение Очистка надстройки автономный функций. 
  
### <a name="cmyaddinhrtermaddin-example"></a>Пример CMyAddin::HrTermAddin()

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

## <a name="deinitialize-monitor-routine"></a>Deinitialize подпрограммы монитор

`inDeInitMonitor` Функция вызывает функцию [IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md) для отмены обратных вызовов для автономного объекта. 
  
### <a name="deinitmonitor-example"></a>Пример DeInitMonitor()

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

## <a name="remove-menu-items-routine"></a>Удаление подпрограммы элементы меню

`HrRemoveMenuItems` Вызовы функций `DispEventUnadvise` для каждого элемента меню в группе меню **Состояния не в сети** , а затем удаляет меню **Состояния не в сети** . 
  
### <a name="cmyaddinhrremovemenuitems-example"></a>Пример CMyAddin::HrRemoveMenuItems()

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

## <a name="unload-libraries-routine"></a>Процедуры Unload библиотек

При выгрузке из Outlook, надстройка `UnloadLibraries` функция выгружает библиотеки динамической компоновки (DLL), которые требуется добавить в. 
  
### <a name="unloadlibraries-example"></a>Пример UnloadLibraries()

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

- [Об автономных состояний API](about-the-offline-state-api.md)
- [Установка примера автономного состояния надстройки](installing-the-sample-offline-state-add-in.md)
- [О примера в автономном режиме состояние надстройки](about-the-sample-offline-state-add-in.md)
- [Настройка автономной состояний надстройке](setting-up-an-offline-state-add-in.md)
- [Мониторинга состояния подключения изменяется с помощью автономного состояния надстройке](monitoring-connection-state-changes-using-an-offline-state-add-in.md)

