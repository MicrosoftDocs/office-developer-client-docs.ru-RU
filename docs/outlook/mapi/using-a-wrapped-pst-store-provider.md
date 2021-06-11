---
title: Использование поставщика упакованного PST-хранилища
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 98f08432-e86c-cba6-45fd-5a6c94d50aaf
description: 'Последнее изменение: 03 июля 2012 г.'
ms.openlocfilehash: b7c651044ab7f4cad7032db69e157c9a3589bde9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420824"
---
# <a name="using-a-wrapped-pst-store-provider"></a>Использование поставщика упакованного PST-хранилища

**Область применения**: Outlook 2013 | Outlook 2016 
  
Прежде чем использовать поставщика хранения файлов персональных папок (PST), необходимо инициализировать и настроить поставщика магазина PST. После настройки поставщика магазина PST необходимо реализовать функции, чтобы MAPI и spooler MAPI могли войти в систему поставщика магазина сообщений. Дополнительные сведения о инициализации и входе в систему поставщика магазина PST см. в инициализации поставщика магазина [PST](initializing-a-wrapped-pst-store-provider.md) и ведения журнала в поставщике упакованных магазинов [PST.](logging-on-to-a-wrapped-pst-store-provider.md)
  
Интерфейс **[IMAPISupport::IUnknown](imapisupportiunknown.md)** обеспечивает реализацию задач, которые обычно выполняются поставщиками магазинов сообщений. Этот интерфейс должен быть завернут для работы поставщика магазина PST с пакетом образца. Функция **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** требует особой реализации. Все остальные функции могут передавать свои параметры в завернутый объект. 
  
В этом разделе функция **IMAPISupport::OpenProfileSection** демонстрируется с помощью примера кода поставщика магазина ПСД sample Wrapped. В примере реализован завернутый поставщик PST, который предназначен для использования в сочетании с API репликации. Дополнительные сведения о загрузке и установке поставщика магазинов PST sample wrapped см. в примере Установки поставщика упаковки [PST Store.](installing-the-sample-wrapped-pst-store-provider.md) Дополнительные сведения об API репликации см. в [иллюстрации API репликации.](about-the-replication-api.md)
  
Когда вы закончите использовать поставщика магазина PST, необходимо должным образом закрыть поставщика магазинов PST. Дополнительные сведения см. в [переключениях](shutting-down-a-wrapped-pst-store-provider.md)с поставщиком магазина PST.
  
## <a name="open-profile-section-routine"></a>Режим раздела "Открытый профиль"

Функция **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** открывает раздел текущего профиля. Функция требует специальной обработки в реализации поставщика магазина PST. При запросе функции возвращается кэшный раздел  `pgNSTGlobalProfileSectionGuid` профиля. 
  
### <a name="csupportopenprofilesection-example"></a>Пример CSupport::OpenProfileSection()

```cpp
STDMETHODIMP CSupport::OpenProfileSection( 
    LPMAPIUID lpUid,     
    ULONG ulFlags, 
    LPPROFSECT * lppProfileObj) 
{ 
    Log(true,"CSupport::OpenProfileSection\n"); 
    if (lpUid &&  
        IsEqualMAPIUID(lpUid, (void *)&pbNSTGlobalProfileSectionGuid) &&  
        m_lpProfSect) 
    {      
        // Allow the opening of the Global Section 
        if (m_lpProfSect) 
        { 
            *lppProfileObj = m_lpProfSect; 
            (*lppProfileObj)->AddRef(); 
            return S_OK; 
        } 
    } 
    return m_pMAPISup->OpenProfileSection(lpUid, ulFlags, lppProfileObj); 
}
```

## <a name="see-also"></a>См. также

- [О поставщике пакетных пакетов PST Store](about-the-sample-wrapped-pst-store-provider.md)
- [Установка поставщика пакетных пакетов PST](installing-the-sample-wrapped-pst-store-provider.md)
- [Инициализация поставщика упакованных магазинов PST](initializing-a-wrapped-pst-store-provider.md)
- [Ведение журнала в поставщике упакованных магазинов PST](logging-on-to-a-wrapped-pst-store-provider.md)
- [Отключение поставщика упакованных магазинов PST](shutting-down-a-wrapped-pst-store-provider.md)

