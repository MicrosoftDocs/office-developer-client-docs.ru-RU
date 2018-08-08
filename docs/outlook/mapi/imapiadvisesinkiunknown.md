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
ms.openlocfilehash: c6e352288f0bf5b0a3f284441bffc522bf00b9f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/15/2018
ms.locfileid: "19808809"
---
# <a name="imapiadvisesink--iunknown"></a>IMAPIAdviseSink : IUnknown

  
  
**Относится к**: Outlook 
  
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

