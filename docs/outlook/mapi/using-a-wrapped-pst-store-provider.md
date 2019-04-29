---
title: Использование поставщика упакованного PST-хранилища
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 98f08432-e86c-cba6-45fd-5a6c94d50aaf
description: 'Дата последнего изменения: 03 июля, 2012'
ms.openlocfilehash: b7c651044ab7f4cad7032db69e157c9a3589bde9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420824"
---
# <a name="using-a-wrapped-pst-store-provider"></a>Использование поставщика упакованного PST-хранилища

**Относится к**: Outlook 2013 | Outlook 2016 
  
Перед использованием упакованного поставщика хранилища файлов личных папок (PST) необходимо инициализировать и настроить поставщик упакованного PST-хранилища. После настройки поставщика упакованного PST-хранилища необходимо реализовать функции, чтобы MAPI и Диспетчер очереди MAPI могли входить в систему поставщика хранилища сообщений. Дополнительные сведения об инициализации и входе в систему поставщика упакованного PST-хранилища можно найти в статье инициализация поставщика упакованного [PST-](initializing-a-wrapped-pst-store-provider.md) хранилища и вход в систему [поставщика упакованного PST-хранилища](logging-on-to-a-wrapped-pst-store-provider.md).
  
Интерфейс **[имаписуппорт:: IUnknown](imapisupportiunknown.md)** предоставляет реализации для задач, которые обычно выполняются поставщиками хранилища сообщений. Чтобы работать с примером поставщика упакованного PST-хранилища, необходимо обернуть этот интерфейс в оболочку. Для функции **[имаписуппорт:: опенпрофилесектион](imapisupport-openprofilesection.md)** требуется специальная реализация. Все остальные функции могут передавать свои параметры базовому объекту, упакованному в оболочку. 
  
В этой статье функция **имаписуппорт:: опенпрофилесектион** демонстрируется с помощью примера кода из примера поставщика УПАКОВАНного PST-хранилища. В примере реализуется упакованный поставщик PST, предназначенный для использования вместе с API репликации. Дополнительные сведения о загрузке и установке примера поставщика упакованного PST-хранилища можно найти в статье [Установка примера поставщика упакованНОГО PST-хранилища](installing-the-sample-wrapped-pst-store-provider.md). Более подробную информацию об API репликации можно узнать [в статье о API репликации](about-the-replication-api.md).
  
По завершении работы с поставщиком упакованного PST-хранилища необходимо надлежащим образом завершить работу поставщика упакованного PST-хранилища. Дополнительные сведения см. [в разделе Завершение работы поставщика упакованНОГО PST-хранилища](shutting-down-a-wrapped-pst-store-provider.md).
  
## <a name="open-profile-section-routine"></a>Процедура открытия раздела профиля

Функция **[имаписуппорт:: опенпрофилесектион](imapisupport-openprofilesection.md)** открывает раздел текущего профиля. Для функции требуется специальная обработка в реализации поставщика упакованного PST-хранилища. `pgNSTGlobalProfileSectionGuid` Когда запрашивается запрос, функция возвращает раздел профиля, который кэшируется. 
  
### <a name="csupportopenprofilesection-example"></a>Ксуппорт:: Опенпрофилесектион () пример

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

- [О примере поставщика упакованного PST-хранилища](about-the-sample-wrapped-pst-store-provider.md)
- [Установка примера поставщика упакованного PST-хранилища](installing-the-sample-wrapped-pst-store-provider.md)
- [Инициализация поставщика упакованного PST-хранилища](initializing-a-wrapped-pst-store-provider.md)
- [Вход в систему поставщика упакованного PST-хранилища](logging-on-to-a-wrapped-pst-store-provider.md)
- [Завершение работы поставщика упакованного PST-хранилища](shutting-down-a-wrapped-pst-store-provider.md)

