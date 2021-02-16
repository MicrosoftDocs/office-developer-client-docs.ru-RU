---
title: Загрузка поставщиков store сообщений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 632d3ef9-43c5-429a-84d7-2dce543d49fb
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: fe3a76fa246cba9447db2f99562670973af183ab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307807"
---
# <a name="loading-message-store-providers"></a>Загрузка поставщиков store сообщений

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Когда клиентские приложения открывают хранилище сообщений, MAPI загружает DLL поставщика этого магазина сообщений в память. После того как MAPI загрузит DLL, между поставщиком и MAPI будет происходить определенная последовательность вызовов методов. Эта последовательность вызовов метода позволяет MAPI получать интерфейсы [ISProvider верхнего уровня : IUnknown](imsprovideriunknown.md), [IMSLogon : IUnknown](imslogoniunknown.md)и [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) интерфейсы и позволяет поставщику хранилищ сообщений получить объект поддержки MAPI. После последовательности вызовов поставщик store сообщений должен быть готов принять от клиентов данные для запуска. 
  
Последовательность вызовов при загрузке DLL поставщика сообщений:
  
1. Клиент вызывает [IMAPISession::OpenMsgStore.](imapisession-openmsgstore.md)
    
2. Если хранилище сообщений еще не открыто, MAPI загружает DLL поставщика магазина и вызывает точку входа [MSProviderInit](msproviderinit.md) DLL. Если хранилище сообщений уже открыто, MAPI пропускает шаги 2 и 3, а затем использует существующий интерфейс [IMSProvider : IUnknown](imsprovideriunknown.md) для выполнения шага 4. 
    
3. **MSProviderInit** создает и возвращает **объект IMSProvider.** 
    
4. MAPI вызывает [IMSProvider::Logon,](imsprovider-logon.md)передавая идентификатор записи в хранилище сообщений клиентского приложения.
    
5. **IMSProvider::Logon** создает и возвращает [интерфейс IMSLogon : IUnknown](imslogoniunknown.md) и [интерфейс IMsgStore : IMAPIProp,](imsgstoreimapiprop.md) а затем вызывает метод [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) в [интерфейсе IMAPISupport : IUnknown.](imapisupportiunknown.md) Если идентификатор записи в хранилище сообщений клиента ссылается на уже открытое хранилище сообщений, поставщик хранилищ сообщений может вернуть существующие интерфейсы **IMSLogon** и **IMsgStore** и не вызывать **AddRef** в объекте поддержки. 
    
6. Если клиент не установил флаг MAPI_NO_MAIL при входе в систему и не установил MDB_NO_MAIL на шаге 1, MAPI предоставляет идентификатор записи в хранилище сообщений для пула MAPI, чтобы пулер MAPI мог войти в хранилище сообщений.
    
7. MAPI возвращает интерфейс **IMsgStore** клиенту. 
    
8. Пулер MAPI вызывает [IMSProvider::SpoolerLogon.](imsprovider-spoolerlogon.md)
    
9. **IMSProvider::SpoolerLogon** возвращает те же интерфейсы **IMSLogon** и **IMsgStore** из шага 5. 
    
> [!NOTE]
> Если вызов для доступа к службе хранения сообщений не удается из-за неправильного пароля, и поставщик не может отобразить интерфейс для запроса правильного пароля, он должен вернуть MAPI_E_FAILONEPROVIDER из метода **IMSProvider::Logon.** Это позволит клиентам повторно отправить пользователю запрос на пароль, чтобы повторить вход в систему, вместо того чтобы вызывать сбой поставщика MAPI в течение всего сеанса. 
  
## <a name="see-also"></a>См. также



[Разработка поставщика хранилища сообщений MAPI](developing-a-mapi-message-store-provider.md)

