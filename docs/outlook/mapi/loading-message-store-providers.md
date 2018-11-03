---
title: Загрузка поставщиков хранилищ сообщений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 632d3ef9-43c5-429a-84d7-2dce543d49fb
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: fe3a76fa246cba9447db2f99562670973af183ab
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398397"
---
# <a name="loading-message-store-providers"></a>Загрузка поставщиков хранилищ сообщений

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
При открытии хранилища сообщений клиентского приложения MAPI загружает библиотеку DLL поставщика хранилища сообщений в память. После загрузки библиотеки DLL MAPI очень определенной последовательности вызовов методов происходит между поставщиком хранилища сообщений и MAPI. Последовательность вызовов этот метод позволяет MAPI для получения верхнего уровня [IMSProvider: IUnknown](imsprovideriunknown.md), [IMSLogon: IUnknown](imslogoniunknown.md), и [IMsgStore: IMAPIProp](imsgstoreimapiprop.md) интерфейсы и разрешает поставщика хранилища сообщений для получения объекта поддержки MAPI. После завершения последовательности вызовов поставщика хранилища сообщений должен быть готов принять входов в систему от клиентов. 
  
Последовательность вызовов, когда сообщение поставщика, который при загрузке библиотеки DLL выглядит следующим образом:
  
1. Клиент вызывает [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md).
    
2. Если хранилище сообщений еще не открыта, MAPI загружает библиотеку DLL поставщика хранилища и вызывает DLL-Библиотека [MSProviderInit](msproviderinit.md) Начальная точка. Если уже открыт хранилища сообщений, MAPI пропускает шаги 2 и 3, а затем использует существующий [IMSProvider: IUnknown](imsprovideriunknown.md) интерфейс для выполнения шага 4. 
    
3. **MSProviderInit** создает и возвращает объект **IMSProvider** . 
    
4. MAPI вызывает [IMSProvider::Logon](imsprovider-logon.md), передав идентификатор записи хранилища сообщений клиентского приложения.
    
5. **IMSProvider::Logon** создает и возвращает [IMSLogon: IUnknown](imslogoniunknown.md) интерфейс и [IMsgStore: IMAPIProp](imsgstoreimapiprop.md) интерфейс, а затем вызывается метод [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) его [IMAPISupport: IUnknown](imapisupportiunknown.md) интерфейса. Если сообщение клиента, хранения идентификатор входа ссылается на хранилища сообщений, которое уже открыт, поставщика хранилища сообщений можно вернуть существующие интерфейсы **IMSLogon** и **IMsgStore** и не нужно вызвать **метод AddRef** для объекта его поддержки. 
    
6. Если клиент не был указан флаг MAPI_NO_MAIL при его вход в систему, а не был указан MDB_NO_MAIL на шаге 1, MAPI предоставляет идентификатор записи хранилища сообщений очереди MAPI, диспетчер очереди MAPI может войти в хранилище сообщений.
    
7. MAPI возвращает интерфейс **IMsgStore** клиенту. 
    
8. Диспетчер очереди MAPI вызывает [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md).
    
9. **IMSProvider::SpoolerLogon** возвращает те же интерфейсы **IMSLogon** и **IMsgStore** из шага 5. 
    
> [!NOTE]
> Если звонок входа в систему с сообщением хранения возникает ошибка поставщика, поскольку предоставлен неверный пароль и поставщика хранилища сообщений не удается отобразить интерфейс для запрашивающих правильный пароль, он должен возвращать MAPI_E_FAILONEPROVIDER из **IMSProvider::Logon **метод. Это позволит клиентам возможности предложить пользователю пароль попробуйте войти на поставщика хранилища сообщений еще раз, а не вызывает ошибку MAPI могут быть поставщик для всего сеанса. 
  
## <a name="see-also"></a>См. также



[Разработка поставщика хранилища сообщений MAPI](developing-a-mapi-message-store-provider.md)

