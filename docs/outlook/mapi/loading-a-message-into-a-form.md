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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Чтобы загрузить существующее сообщение в форму с помощью сервера форм, используйте одну из следующих стратегий.
  
- Вызов [IMAPISession::P repareForm](imapisession-prepareform.md) для создания маркера, а затем [IMAPISession::ShowForm](imapisession-showform.md) для отображения формы. 
    
- Вызов [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md). 
    
Использование **стратегии PrepareForm** и **ShowForm** сравнительно просто, но она приводит к формам, которые являются модальными по отношению к вашему клиенту. Это происходит из-за того, что вызов **в ShowForm** не возвращается до тех пор, пока форма не выйдет. Если вам нужно обрабатывать формы асинхронно, не используйте эту стратегию. 
  
Использование **стратегии LoadForm** сложнее, так как метод требует нескольких параметров. Эти параметры предписывают руководителю форм запустить соответствующий сервер формы в надлежащем контексте и отобразить соответствующее сообщение. Если сервер формы уже запущен, диспетчер форм загружает сообщение на сервер формы, не запуская новый экземпляр сервера форм. 
  
Чтобы указать, какой сервер формы необходимо запустить, передай класс сообщений, обрабатываемый целевым сервером, в содержимое параметра _lpszMessageClass._ Соответствующий класс сообщений можно определить путем PR_MESSAGE_CLASS **свойства** [PR_MESSAGE_CLASS (PidTagMessageClass)](pidtagmessageclass-canonical-property.md)загружаемого сообщения. Иногда для указанного класса сообщений нет сервера форм, а только сервера форм, который обрабатывает сообщения, принадлежащие суперклассу сообщения. Если вы предпочитаете, чтобы сообщение загружалось только сервером форм, специально предназначенным для обработки сообщений этого класса, установите флаг MAPIFORM_EXACTMATCH в **вызове LoadForm.** Дополнительные сведения см. в [нескольких классах сообщений MAPI.](mapi-message-classes.md)
  
 **LoadForm** также требует указателя на сайт сообщения и контекст просмотра, а также значение  свойств PR_MSG_STATUS [(PidTagMessageStatus)](pidtagmessagestatus-canonical-property.md)и **PR_MESSAGE_FLAGS** [(PidTagMessageFlags).](pidtagmessageflags-canonical-property.md)
  

