---
title: Загрузка поставщиков магазина сообщений
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
# <a name="loading-message-store-providers"></a>Загрузка поставщиков магазина сообщений

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
При открываемом клиентском приложении хранилище сообщений MAPI загружает DLL поставщика сообщений в память. После загрузки MAPI DLL между поставщиком хранения сообщений и MAPI возникает очень специфическая последовательность вызовов методов. Эта последовательность вызовов метода позволяет MAPI получать интерфейсы [IMSProvider верхнего уровня: IUnknown](imsprovideriunknown.md), [IMSLogon : IUnknown](imslogoniunknown.md)и [IMsgStore: интерфейсы IMAPIProp](imsgstoreimapiprop.md) и позволяет поставщику магазина сообщений получить объект поддержки MAPI. После последовательности вызовов поставщик магазина сообщений должен быть готов принимать логотипы от клиентов. 
  
Последовательность вызовов при загрузке DLL поставщика сообщений следующим образом:
  
1. Клиент вызывает [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md).
    
2. Если хранилище сообщений еще не открыто, MAPI загружает DLL поставщика магазина и вызывает точку входа [MSProviderInit DLL.](msproviderinit.md) Если хранилище сообщений уже открыто, MAPI пропускает шаги 2 и 3, а затем использует существующий [интерфейс IMSProvider: IUnknown](imsprovideriunknown.md) для выполнения шага 4. 
    
3. **MSProviderInit** создает и возвращает **объект IMSProvider.** 
    
4. MAPI вызывает [IMSProvider:::Logon,](imsprovider-logon.md)передав идентификатор входа в хранилище сообщений клиента.
    
5. **IMSProvider::Logon** создает и возвращает [интерфейс IMSLogon : IUnknown](imslogoniunknown.md) и [интерфейс IMsgStore : IMAPIProp,](imsgstoreimapiprop.md) а затем вызывает метод [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) в [интерфейсе IMAPISupport : IUnknown.](imapisupportiunknown.md) Если идентификатор входа в хранилище сообщений клиента ссылается на уже открытый магазин сообщений, поставщик магазина сообщений может вернуть существующие интерфейсы **IMSLogon** и **IMsgStore** и не вызывать **AddRef** на объекте поддержки. 
    
6. Если клиент не установил флаг MAPI_NO_MAIL при входе в систему и не задаёт MDB_NO_MAIL на шаге 1, MAPI предоставляет идентификатор входа в хранилище сообщений в пулер MAPI, чтобы пульпер MAPI мог войти в хранилище сообщений.
    
7. MAPI возвращает интерфейс **IMsgStore** клиенту. 
    
8. Spooler MAPI вызывает [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md).
    
9. **ИНТЕРФЕЙСЫ IMSProvider::SpoolerLogon** возвращают те же интерфейсы **IMSLogon** и **IMsgStore** с 5-го шага. 
    
> [!NOTE]
> Если вызов логона поставщику магазина сообщений не удается, так как был поставлен неправильный пароль, а поставщик магазина сообщений не может отображать интерфейс для запроса правильного пароля, он должен MAPI_E_FAILONEPROVIDER из метода **IMSProvider::Logon.** Это позволит клиентам снова подсказыть пользователю пароль, чтобы попытаться войти в поставщик магазина сообщений, а не вызывать сбой MAPI для поставщика на протяжении всего сеанса. 
  
## <a name="see-also"></a>См. также



[Разработка поставщика хранилища сообщений MAPI](developing-a-mapi-message-store-provider.md)

