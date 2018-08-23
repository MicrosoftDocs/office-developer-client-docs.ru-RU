---
title: IMAPIAdviseSink IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIAdviseSink
api_type:
- COM
ms.assetid: f598fc57-75d3-473b-8eb0-9d8a3b92e9f2
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b9244e28337c74487562ec235f246559a49a390d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573805"
---
# <a name="imapiadvisesink--iunknown"></a>IMAPIAdviseSink : IUnknown

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Реализует объект приемника уведомлений для обработки уведомлений. В вызове метода **уведомлений** поставщика услуг, механизм, используемый для регистрации уведомления передается указатель на объект приемник уведомлений. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Предоставляемые:  <br/> |Уведомить объектов приемника  <br/> |
|Реализованный:  <br/> |Клиентские приложения и MAPI  <br/> |
|Вызывается:  <br/> |Поставщиков услуг и MAPI  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMAPIAdviseSink  <br/> |
|Тип указателя:  <br/> |LPMAPIADVISESINK  <br/> |
   
## <a name="vtable-order"></a>Порядке vtable

|||
|:-----|:-----|
|[OnNotify](imapiadvisesink-onnotify.md) <br/> |Отвечает на уведомление при выполнении одного или нескольких задач. Задачи, выполняемые зависят от типа события и объект, который создает уведомления.  <br/> |
   
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

