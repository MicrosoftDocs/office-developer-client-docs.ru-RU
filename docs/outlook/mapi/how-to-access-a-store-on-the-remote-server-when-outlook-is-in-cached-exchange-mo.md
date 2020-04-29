---
title: Доступ к хранилищу на удаленном сервере, если Outlook работает в режиме кэширования Exchange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5c6df156-4015-2d0f-26b7-07055a3f7810
description: 'Дата последнего изменения: 02 июля 2012 г.'
ms.openlocfilehash: cfc20c1a9ca4510ffec86bf16666f1fc50822321
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433866"
---
# <a name="access-a-store-on-the-remote-server-when-outlook-is-in-cached-exchange-mode"></a>Доступ к хранилищу на удаленном сервере, если Outlook работает в режиме кэширования Exchange
 
**Относится к**: Outlook 2013 | Outlook 2016 
  
В этом разделе приведен пример кода на языке C++, в котором показано, как использовать флаг **MAPI_NO_CACHE** , чтобы открыть папку или сообщение в хранилище сообщений на удаленном сервере, если Microsoft Office Outlook находится в режиме кэширования Exchange. 
  
Режим кэширования Exchange позволяет Outlook использовать локальную копию почтового ящика пользователя, в то время как Outlook поддерживает сетевое подключение к удаленной копии почтового ящика пользователя на удаленном сервере Exchange. Когда Outlook работает в режиме кэширования Exchange, по умолчанию все решения MAPI, которые выполняют вход в тот же сеанс, также подключаются к кэшированному хранилищу сообщений. Все данные, к которым обращается доступ, и все внесенные изменения вносятся в локальную копию почтового ящика.
  
Клиент или поставщик услуг может переопределить подключение к локальному хранилищу сообщений и открыть сообщение или папку в удаленном хранилище, установив бит для **MAPI_NO_CACHE** в параметре *ulFlags* при вызове **[IMsgStore:: OpenEntry](imsgstore-openentry.md)**. 
  
В приведенном ниже примере кода показано, как вызывать **IMsgStore:: OpenEntry** с флагом **MAPI_NO_CACHE** , установленным в параметре *ulFlags* , чтобы открыть корневую папку в удаленном хранилище сообщений. 
  
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

Если вы открыли хранилище сообщений с флагом **MDB_ONLINE** на удаленном сервере, не нужно использовать флаг **MAPI_NO_CACHE** . 
  
## <a name="see-also"></a>См. также

- [Сведения о дополнениях для MAPI](about-mapi-additions.md) 
- [Открытие хранилища на удаленном сервере, если Outlook работает в режиме кэширования Exchange](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)
- [Управление сообщением в OST без вызова синхронизации в режиме кэширования Exchange](how-to-manage-a-message-in-an-ost-without-invoking-a-synchronization.md)

