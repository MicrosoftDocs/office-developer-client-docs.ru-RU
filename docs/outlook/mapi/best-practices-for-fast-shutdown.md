---
title: Рекомендации по быстрому завершению работы
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ae8a9214-e53f-4c57-8dbe-aa7cc6903aa8
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 0d9e7caf43bcee654aa92652e94bc8c2ebba18e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808129"
---
# <a name="best-practices-for-fast-shutdown"></a>Рекомендации по быстрому завершению работы

  
  
**Относится к**: Outlook 
  
В данном разделе содержатся советы и рекомендации для администраторов, клиентов MAPI и поставщики MAPI для использования интерфейсов быстрое завершение работы и параметры реестра Windows для сведения к минимуму потерю данных во время отключения клиента.
  
- Клиент MAPI успешно выполнить быстрое завершение работы, поэтому процессы поставщика не приводят к потере данных клиент MAPI сначала необходимо вызвать метод [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) . Клиент должен приступите к методы [IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) и [IMAPIClientShutdown::DoFastShutdown](imapiclientshutdown-dofastshutdown.md) , основанные на подсистемы MAPI поддержка быстрое завершение работы, как указано в возвращаемое значение ** IMAPIClientShutdown::QueryFastShutdown**. Как клиент MAPI Microsoft Outlook не вызывает **IMAPIClientShutdown::NotifyProcessShutdown** или **IMAPIClientShutdown::DoFastShutdown** **IMAPIClientShutdown::QueryFastShutdown** возвращает ошибку. Если администратор отключил быстрое завершение работы в реестре Windows, подсистемы MAPI вернет MAPI_E_NO_SUPPORT **IMAPIClientShutdown::QueryFastShutdown**. В этом случае подсистемы MAPI не будет сообщение, выйдите из поставщики MAPI процесса интерпретации клиента. Таким образом Если клиент MAPI игнорирует этот код возврата ошибки, переходит к быстрое завершение работы и отключение всех внешних ссылок, все поставщики MAPI загруженных будут иметь потери данных. 
    
- Поставщики MAPI следует реализовать [IMAPIProviderShutdown: IUnknown](imapiprovidershutdowniunknown.md) интерфейс для выполнения своевременного и необходимые действия, чтобы избежать потери данных из-за клиента, отключение внешних ссылок перед выходом из клиента. Поставщик должен отложить все, что несущественные для сохранения данных в хранилище данных. Например поставщика транспорта следует отложить ненужных фоновых операций, которые проверять новые сообщения поставщика адресных книг должны откладывать загрузки последних изменений с сервера и поставщика хранилища таких как следует отложить задач по обслуживанию сжатие или индексирования. 
    
- Пользователи, которым необходим клиентов MAPI, чтобы выйти из сразу после их закрытия следует использовать параметр реестра по умолчанию, которая позволяет быстрое завершение работы, если не отключает поставщика.
    
- Если клиент MAPI вызывает **IMAPIClientShutdown::DoFastShutdown**, не рекомендуется создавать любые дополнительные вызовы MAPI, включая функцию [MAPIUninitialize](mapiuninitialize.md) . Клиент не следует использовать MAPI для остальных существования процесса клиента. 
    
- Клиент MAPI должен никогда не прямой звонок интерфейс **IMAPIProviderShutdown** поставщика. Всегда использовать клиентов MAPI [IMAPIClientShutdown: IUnknown](imapiclientshutdowniunknown.md) интерфейса. 
    
- Если поставщика MAPI должен убедиться, что при его загрузке, быстрое завершение работы не используется, его следует реализовать интерфейс **IMAPIProviderShutdown** и возврата MAPI_E_NO_SUPPORT для метода **IMAPIProviderShutdown::QueryFastShutdown** . Тем не менее для клиентов MAPI, такие как Outlook, это приведет к клиенту отменить быстрое завершение работы и дольше, чтобы завершить работу. 
    
## <a name="see-also"></a>См. также



[Завершение работы клиента в MAPI](client-shutdown-in-mapi.md)
  
[Обзор быстрого завершения работы](fast-shutdown-overview.md)
  
[Пользовательские параметры быстрого завершения работы](fast-shutdown-user-options.md)

