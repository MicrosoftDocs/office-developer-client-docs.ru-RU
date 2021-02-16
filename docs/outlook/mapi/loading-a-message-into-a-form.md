---
title: Загрузка сообщения в форму
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4bdbe021-d694-4967-a105-4b24f1eebc44
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: afecd3b334dd2cf7b2953916872982e6459a8434
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412417"
---
# <a name="loading-a-message-into-a-form"></a>Загрузка сообщения в форму

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Чтобы загрузить существующее сообщение в форму с помощью сервера форм, используйте одну из следующих стратегий.
  
- Вызовите [IMAPISession::P repareForm](imapisession-prepareform.md) для создания маркера, а затем [IMAPISession::ShowForm](imapisession-showform.md) для отображения формы. 
    
- Вызов [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md). 
    
Использовать **стратегию PrepareForm** и **ShowForm** сравнительно просто, но это приводит к модальным формам по отношению к клиенту. Это происходит потому, что вызов **ShowForm** не возвращается до выхода формы. Если вам нужно обрабатывать формы асинхронно, не используйте эту стратегию. 
  
Использовать **стратегию LoadForm** сложнее, так как методу требуется несколько параметров. Эти параметры предписывают диспетчеру форм запустить соответствующий сервер форм в правильном контексте и отобразить соответствующее сообщение. Если сервер форм уже запущен, диспетчер форм загружает сообщение на сервер форм без запуска нового экземпляра сервера форм. 
  
Чтобы указать, какой сервер форм необходимо запустить, передав класс сообщения, обработанный целевым сервером, в содержимом параметра _lpszMessageClass._ Соответствующий класс сообщения можно определить, PR_MESSAGE_CLASS **(** [PidTagMessageClass)](pidtagmessageclass-canonical-property.md)загружаемого сообщения. Иногда для указанного класса сообщений не существует сервера форм, а только сервер форм, который обрабатывает сообщения, принадлежащие к суперклассу сообщения. Если вы хотите, чтобы сообщение загружалось только сервером форм, предназначенным специально для обработки сообщений этого класса, установите флаг MAPIFORM_EXACTMATCH в вызове **LoadForm.** Дополнительные сведения см. в сведениях о [классах сообщений MAPI.](mapi-message-classes.md)
  
 **Для LoadForm** также требуется указатель на сайт сообщения и контекст просмотра, а также значение свойств **PR_MSG_STATUS** ([PidTagMessageStatus)](pidtagmessagestatus-canonical-property.md)и **PR_MESSAGE_FLAGS** [(PidTagMessageFlags).](pidtagmessageflags-canonical-property.md)
  

