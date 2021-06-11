---
title: Лучшие практики для быстрого отключения
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ae8a9214-e53f-4c57-8dbe-aa7cc6903aa8
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 8c7225427b80d89c6dd8adfa85f7d91885850365
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426970"
---
# <a name="best-practices-for-fast-shutdown"></a>Лучшие практики для быстрого отключения

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
В этом разделе рекомендуется передовая практика для администраторов, клиентов MAPI и поставщиков MAPI для использования параметров реестра Windows и интерфейсов быстрого отключения, чтобы свести к минимуму потерю данных во время остановки клиента.
  
- Чтобы клиент MAPI успешно выполнил быстрое отключение, чтобы процессы поставщика не повеяли потери данных, клиент MAPI должен сначала вызвать [метод IMAPIClientShutdown::QueryFastShutdown.](imapiclientshutdown-queryfastshutdown.md) Клиент должен продолжить работу с методами [IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) и [IMAPIClientShutdown::D FastShutdown,](imapiclientshutdown-dofastshutdown.md) основанными на поддержке подсистемы MAPI для быстрого отключения, о чем свидетельствует возвратное значение **IMAPIClientShutdown::QueryFastShutdown**. В качестве клиента MAPI корпорация Майкрософт Outlook не называет **IMAPIClientShutdown::NotifyProcessShutdown** или **IMAPIClientShutdown::D FastShutdown,** если **IMAPIClientShutdown::QueryFastShutdown** возвращает ошибку. Если администратор отключил быстрое отключение в реестре Windows, подсистема MAPI возвращает MAPI_E_NO_SUPPORT **в IMAPIClientShutdown::QueryFastShutdown**. В этом случае подсистема MAPI не будет информировать поставщиков MAPI о немедленном выходе клиентского процесса. Поэтому, если клиент MAPI игнорирует этот код возврата ошибок, приступить к быстрому отключению и отключит все внешние ссылки, все загруженные поставщики MAPI будут иметь потерю данных. 
    
- Поставщики MAPI должны реализовать [интерфейс IMAPIProviderShutdown : IUnknown,](imapiprovidershutdowniunknown.md) чтобы выполнить необходимые действия, чтобы избежать потери данных из-за отключения клиентом внешних ссылок перед выходом клиента. Поставщику следует отложить все остальное, не важное для сохранения данных в основном хранилище данных. Например, поставщик транспорта должен отложить ненужные фоновые операции, которые проверяют новую почту, поставщик адресных книг должен отложить скачивание недавних изменений с сервера, а поставщик магазина должен отложить выполнение задач обслуживания, таких как уплотнительная работа или индексация. 
    
- Пользователи, которые хотят, чтобы клиенты MAPI выходили сразу после их закрытия, должны использовать параметр реестра по умолчанию, который позволяет быстро закрыть работу, если поставщик не откажется.
    
- Если клиент MAPI вызывает **IMAPIClientShutdown::D oFastShutdown,** он не должен делать дополнительных вызовов в MAPI, включая функцию [MAPIUninitialize.](mapiuninitialize.md) Клиент не должен использовать MAPI до конца срока службы клиента. 
    
- Клиент MAPI никогда не должен напрямую вызывать интерфейс **IMAPIProviderShutdown** поставщика. Клиенты MAPI всегда должны использовать [интерфейс IMAPIClientShutdown: IUnknown.](imapiclientshutdowniunknown.md) 
    
- Если поставщику MAPI необходимо убедиться, что быстрое отключение не используется во время загрузки, он должен реализовать интерфейс **IMAPIProviderShutdown** и вернуть MAPI_E_NO_SUPPORT для метода **IMAPIProviderShutdown::QueryFastShutdown.** Однако для клиентов MAPI, таких как Outlook, это приведет к тому, что клиент откажется от быстрого отключения и закроется дольше. 
    
## <a name="see-also"></a>См. также



[Завершение работы клиента в MAPI](client-shutdown-in-mapi.md)
  
[Обзор быстрого завершения работы](fast-shutdown-overview.md)
  
[Параметры быстрого отключения пользователей](fast-shutdown-user-options.md)

