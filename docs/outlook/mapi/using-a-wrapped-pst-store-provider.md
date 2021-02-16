---
title: Использование поставщика упакованного PST-хранилища
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 98f08432-e86c-cba6-45fd-5a6c94d50aaf
description: 'Last modified: July 03, 2012'
ms.openlocfilehash: b7c651044ab7f4cad7032db69e157c9a3589bde9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420824"
---
# <a name="using-a-wrapped-pst-store-provider"></a>Использование поставщика упакованного PST-хранилища

**Относится к**: Outlook 2013 | Outlook 2016 
  
Перед использованием поставщика упакованного PST-файла необходимо инициализировать и настроить поставщика упакованного PST-магазина. После настройки поставщика упакованного PST-магазина необходимо реализовать функции, чтобы MAPI и пулер MAPI могли войти в систему поставщика store сообщений. Дополнительные сведения об инициализации и входе в систему для поставщика упакованного PST-магазина см. в инициализации поставщика упакованного [PST-магазина](initializing-a-wrapped-pst-store-provider.md) и входе в систему для поставщика упакованного [PST-магазина.](logging-on-to-a-wrapped-pst-store-provider.md)
  
Интерфейс **[IMAPISupport::IUnknown](imapisupportiunknown.md)** предоставляет реализации задач, которые обычно выполняются поставщиками store сообщений. Этот интерфейс должен быть оболочкой для работы примера поставщика упакованного PST-магазина. Функция **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** требует особой реализации. Все остальные функции могут передавать свои параметры в объект-оболочку. 
  
В этом разделе функция **IMAPISupport::OpenProfileSection** демонстрируется с помощью примера кода из примера поставщика упакованного PST-магазина. В примере реализован упакованный поставщик PST,который предназначен для использования в сочетании с API репликации. Дополнительные сведения о загрузке и установке примера поставщика упакованного PST-магазина см. в установке примера поставщика упакованного [PST-магазина.](installing-the-sample-wrapped-pst-store-provider.md) Дополнительные сведения об API репликации см. в сведениях [об API репликации.](about-the-replication-api.md)
  
После завершения работы с поставщиком упакованного PST-магазина необходимо завершить работу поставщика упакованного PST-магазина. Дополнительные сведения см. в подстроке "Завершение работы поставщика упакованного [PST-магазина".](shutting-down-a-wrapped-pst-store-provider.md)
  
## <a name="open-profile-section-routine"></a>Процедура открытия раздела профилей

Функция **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** открывает раздел текущего профиля. Функция требует специальной обработки в реализации поставщика упакованного PST-магазина. При запросе функция возвращает кэшный раздел  `pgNSTGlobalProfileSectionGuid` профиля. 
  
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

- [Пример поставщика упакованного PST-магазина](about-the-sample-wrapped-pst-store-provider.md)
- [Установка примера поставщика упакованного PST-магазина](installing-the-sample-wrapped-pst-store-provider.md)
- [Инициализация поставщика упакованного PST-магазина](initializing-a-wrapped-pst-store-provider.md)
- [Вход в систему поставщика упакованного PST-магазина](logging-on-to-a-wrapped-pst-store-provider.md)
- [Завершение работы поставщика упакованного PST-магазина](shutting-down-a-wrapped-pst-store-provider.md)

