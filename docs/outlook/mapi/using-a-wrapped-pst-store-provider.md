---
title: С помощью оболочку поставщика хранилища PST-файлов
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 98f08432-e86c-cba6-45fd-5a6c94d50aaf
description: 'Последнее изменение: 03 июля 2012 г.'
ms.openlocfilehash: e74ccd44797bb5629bfe4f390b099771c6932a9b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566469"
---
# <a name="using-a-wrapped-pst-store-provider"></a>С помощью оболочку поставщика хранилища PST-файлов

**Применимо к**: Outlook 2013 | Outlook 2016 
  
Прежде чем использовать оболочку поставщика хранилища личных папок (PST) файла, необходимо инициализировать и настроить оболочку поставщика хранилища PST-файлов. После настройки оболочку поставщика хранилища PST-файлов, необходимо реализовать функции, чтобы MAPI и диспетчер очереди MAPI могут войти на поставщика хранилища сообщений. Дополнительные сведения об инициализации и вход в систему на оболочку поставщик хранилища PST-файлов можно [инициализации поставщика оболочку хранения PST -файлов](initializing-a-wrapped-pst-store-provider.md) и [Ведение журнала на к поставщику хранения оболочку PST -файлов](logging-on-to-a-wrapped-pst-store-provider.md).
  
Интерфейс **[IMAPISupport::IUnknown](imapisupportiunknown.md)** включает сведения о реализации для задач, которые обычно выполняются с сообщение хранения поставщиков. Этот интерфейс должен оболочку для оболочку PST поставщик хранилища для работы. Функция **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** требует специальных реализаций. Другие функции можно передать свои параметры базового объекта оболочку. 
  
В этом разделе демонстрируется функция **IMAPISupport::OpenProfileSection** с помощью пример кода из оболочку PST поставщик хранилища. В примере реализуется оболочку поставщика PST-файлов, который предназначен для использования совместно с использованием интерфейса API репликации. Дополнительные сведения о загрузке и установке оболочку PST поставщик хранилища [Оболочку PST поставщик хранилища](installing-the-sample-wrapped-pst-store-provider.md)см. Дополнительные сведения об API репликации можно [О репликации API](about-the-replication-api.md).
  
После завершения работы с оболочкой поставщика хранилища PST-файлов, необходимо правильно выключить оболочку поставщика хранилища PST-файлов. Для получения дополнительных сведений см [Завершает работу оболочку PST поставщика хранилища](shutting-down-a-wrapped-pst-store-provider.md).
  
## <a name="open-profile-section-routine"></a>Открытие раздела профиля общей процедуры

Функция **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** откроется раздел текущего профиля. Функции требуется особая обработка выполняется в оболочку реализации поставщика хранилища PST-файлов. При `pgNSTGlobalProfileSectionGuid` запрашивается, функция возвращает раздела профиля кэширования. 
  
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

- [Сведения о примере поставщика упакованного PST-хранилища](about-the-sample-wrapped-pst-store-provider.md)
- [Установка примера поставщика упакованного PST-хранилища](installing-the-sample-wrapped-pst-store-provider.md)
- [Инициализация поставщика упакованного PST-хранилища](initializing-a-wrapped-pst-store-provider.md)
- [Вход в систему поставщика упакованного PST-хранилища](logging-on-to-a-wrapped-pst-store-provider.md)
- [Завершение работы поставщика упакованного PST-хранилища](shutting-down-a-wrapped-pst-store-provider.md)

