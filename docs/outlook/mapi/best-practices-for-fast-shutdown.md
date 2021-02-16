---
title: Best Practices for Fast Shutdown
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
# <a name="best-practices-for-fast-shutdown"></a>Best Practices for Fast Shutdown

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
В этом разделе советуем администраторам, клиентам MAPI и поставщикам MAPI использовать параметры реестра Windows и интерфейсы быстрого завершения работы, чтобы свести к минимуму потерю данных во время завершения работы клиента.
  
- Чтобы клиент MAPI мог успешно выполнить быстрое завершение работы, чтобы процессы поставщика не повлечали потери данных, клиент MAPI должен сначала вызвать метод [IMAPIClientShutdown::QueryFastShutdown.](imapiclientshutdown-queryfastshutdown.md) Клиент должен перейти к методам [IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) и [IMAPIClientShutdown::D oFastShutdown](imapiclientshutdown-dofastshutdown.md) на основе поддержки подсистемы MAPI быстрого завершения работы, как указано в возвращаемом значении **IMAPIClientShutdown::QueryFastShutdown**. Как клиент MAPI Microsoft Outlook не вызывает **IMAPIClientShutdown::NotifyProcessShutdown** или **IMAPIClientShutdown::D oFastShutdown,** если **IMAPIClientShutdown::QueryFastShutdown** возвращает ошибку. Если администратор отключил быстрое завершение работы в реестре Windows, подсистема MAPI вернет MAPI_E_NO_SUPPORT **IMAPIClientShutdown::QueryFastShutdown**. В этом случае подсистема MAPI не сообщит поставщикам MAPI о немедленном выходе клиентского процесса. Поэтому, если клиент MAPI игнорирует этот код возврата ошибки, переходит к быстрому отключению и отключает все внешние ссылки, все загруженные поставщики MAPI будут иметь потерю данных. 
    
- Поставщики MAPI должны реализовать интерфейс [IMAPIProviderShutdown : IUnknown,](imapiprovidershutdowniunknown.md) чтобы выполнить необходимые действия, чтобы избежать потери данных из-за отключения клиентом внешних ссылок до выхода клиента. Поставщик должен отложить все остальные нематериальные функции, чтобы сохранить данные в своем основном хранилище данных. Например, поставщик транспорта должен отложить ненужные фоновые операции, которые проверяют новую почту, поставщик адресной книги должен отложить скачивание последних изменений с сервера, а поставщик магазина должен отложить задачи обслуживания, такие как сжатие или индексация. 
    
- Пользователи, которым нужно закрыть клиенты MAPI, должны использовать параметр реестра по умолчанию, позволяющий быстрое завершение работы, если поставщик не отключит их.
    
- Когда клиент MAPI вызывает **IMAPIClientShutdown::D oFastShutdown,** он не должен делать дополнительные вызовы MAPI, включая функцию [MAPIUninitialize.](mapiuninitialize.md) Клиент не должен использовать MAPI в течение всего времени существования клиентского процесса. 
    
- Клиент MAPI никогда не должен напрямую вызывать интерфейс **IMAPIProviderShutdown** поставщика. Клиенты MAPI всегда должны использовать [интерфейс IMAPIClientShutdown : IUnknown.](imapiclientshutdowniunknown.md) 
    
- Если поставщик MAPI должен убедиться, что быстрое завершение работы не используется во время загрузки, он должен реализовать интерфейс **IMAPIProviderShutdown** и вернуть MAPI_E_NO_SUPPORT для метода **IMAPIProviderShutdown::QueryFastShutdown.** Однако для клиентов MAPI, таких как Outlook, это приведет к тому, что клиент отключится от быстрого завершения работы и займет больше времени. 
    
## <a name="see-also"></a>См. также



[Завершение работы клиента в MAPI](client-shutdown-in-mapi.md)
  
[Обзор быстрого завершения работы](fast-shutdown-overview.md)
  
[Параметры пользователей быстрого завершения работы](fast-shutdown-user-options.md)

