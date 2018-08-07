---
title: Доступ к хранилищу на удаленном сервере, когда Outlook находится в режиме кэширования данных Exchange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5c6df156-4015-2d0f-26b7-07055a3f7810
description: 'Последнее изменение: 2 июля 2012.'
ms.openlocfilehash: 8f1afd31f017b73fa5270d8fbf4c2a1c8fa08880
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808610"
---
# <a name="access-a-store-on-the-remote-server-when-outlook-is-in-cached-exchange-mode"></a>Доступ к хранилищу на удаленном сервере, когда Outlook находится в режиме кэширования данных Exchange
 
**Относится к**: Outlook 
  
В этом разделе содержится пример кода на C++, показано, как использовать флаг **MAPI_NO_CACHE** , чтобы открыть папку или сообщение для хранилища сообщений на удаленном сервере, когда Microsoft Office Outlook находится в режиме кэширования данных Exchange. 
  
Режим кэширования данных Exchange позволяет Outlook на использование локальной копии почтового ящика пользователя во время Outlook устанавливает соединение с удаленной копией почтового ящика пользователя на удаленном сервере Exchange. Когда Outlook работает в режиме кэширования данных Exchange по умолчанию всех решений MAPI, выполните вход на том же сеансе также подключены к хранилище кэшированных сообщений. Все данные, к которому осуществляется и все изменения, внесенные выполняются к локальной копии почтового ящика.
  
Клиент или служба поставщика можно переопределить подключения к хранилищу локального сообщения и откройте сообщение или папки для удаленного хранилища, установив бит для **MAPI_NO_CACHE** с помощью параметра *ulFlags* при вызове **[IMsgStore::OpenEntry](imsgstore-openentry.md)**. 
  
В следующем примере кода показано, как вызывать **IMsgStore::OpenEntry** с флагом **MAPI_NO_CACHE** значение с помощью параметра *ulFlags* откройте корневой папки хранилища удаленных сообщений. 
  
```cpp
HRESULT HrOpenRootFolder ( 
    LPMDB lpMDB, 
    LPMESSAGE* lpRootFolder) 
{ 
    ULONG ulObjType = NULL; 
    HRESULT hRes = lpMDB-&gt;OpenEntry( 
        0,// size of entry ID       
        NULL,                                   // Pointer to entry ID 
        NULL,                                   // Use default interface (IMAPIFolder) 
        MAPI_BEST_ACCESS | MAPI_NO_CACHE,       // Flags 
        &amp;ulObjType,
// Output parameter indicates the type of object returned 
        (LPUNKNOWN *) lpRootFolder));           // Pointer to put the opened folder in 
    return hRes; 
 
}
```

При открытии хранилища сообщений с флагом **MDB_ONLINE** на удаленном сервере, не нужно использовать флаг **MAPI_NO_CACHE** . 
  
## <a name="see-also"></a>См. также

- [Сведения о дополнениях для MAPI](about-mapi-additions.md)
- [Открытие хранилища на удаленном сервере, если Outlook работает в режиме кэширования Exchange](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)
- [Управление сообщением в OST без вызова синхронизации в режиме кэширования Exchange](how-to-manage-a-message-in-an-ost-without-invoking-a-synchronization.md)

