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
ms.openlocfilehash: 6e65311187ba96abde31a4779ebba371b3d02084
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576500"
---
# <a name="loading-a-message-into-a-form"></a>Загрузка сообщения в форму

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Чтобы загрузить существующее сообщение в форму с помощью сервера форм, используйте одну из следующих стратегий.
  
- Вызов [IMAPISession::PrepareForm](imapisession-prepareform.md) для создания маркера и затем [IMAPISession::ShowForm](imapisession-showform.md) для отображения формы. 
    
- Вызов [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md). 
    
С помощью стратегии **PrepareForm** и **ShowForm** сравнительно легко, но результаты в формах, которые являются модальными по отношению к вашей клиента. Это вызов **ShowForm** не возвращает пока выйдет из формы. Если вам требуется для обработки форм асинхронно, не используйте этой стратегии. 
  
С помощью стратегии **LoadForm** сложнее, так как метод требует несколько параметров. Эти параметры диспетчеру формы для запуска сервера соответствующую форму в контексте соответствующих прав и отображения соответствующее сообщение. Если на сервере формы уже выполняется, диспетчер форм загружает сообщения в сервера форм без запуска нового экземпляра сервера формы. 
  
Чтобы указать, какой сервер формы для запуска, передайте класс сообщения, обрабатываемых на целевой сервер в содержимое параметра _lpszMessageClass_ . Класс соответствующего сообщения можно определить извлекая свойство **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) сообщения для загрузки. В некоторых случаях нет ни одного сервера формы для указанного класса сообщений, только сервер формы, который обрабатывает сообщения, относящегося к суперкласса сообщения. Ниже приведена загрузку сообщений только с сервера форм, специально предназначенный для обработки сообщений этого класса, задайте флаг MAPIFORM_EXACTMATCH в вызове **LoadForm** . Для получения дополнительных сведений см [Классы сообщений MAPI](mapi-message-classes.md).
  
 **LoadForm** также требуется указатель сайта вашей средства просмотра сообщений и контекст представления и значение для сообщения целевой **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) и **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) свойства.
  

