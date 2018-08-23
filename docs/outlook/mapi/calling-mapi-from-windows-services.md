---
title: Вызов MAPI из служб Windows
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: debf7ec3-e9f9-4912-b9a2-fc0953a56a01
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: f77b3dd9ca8c977574aab337b0df572404061b4a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565867"
---
# <a name="calling-mapi-from-windows-services"></a>Вызов MAPI из служб Windows

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Чтобы включить клиентские приложения MAPI, которые записываются в виде служб Windows для работы с MAPI-совместимое поставщиков услуг, MAPI, задает некоторые ограничения и требования.
  
Клиенты MAPI имеют следующие ограничения:
  
- Они не могут разрешить пользовательского интерфейса.
    
- Они могут отправлять сообщения только с помощью хранилища тесно связанных сообщений и транспорта поставщика. Кроме того клиентов MAPI можно отправлять и получать сообщения с помощью Exchange Server корпорации Майкрософт или другого поставщика транспорта на стороне сервера. Из-за проблем удостоверения и безопасности между клиентскими приложениями и диспетчер очереди MAPI большинство поставщиков транспорта не поддерживаются в службе. 
    
Все клиентские приложения MAPI, ли они реализованы в качестве службы Windows, необходимо вызвать функцию [MAPIInitialize](mapiinitialize.md) для инициализации библиотеки MAPI. Вызов функции [OleInitialize](http://msdn.microsoft.com/en-us/library/ms690134%28v=VS.85%29.aspx) также возникает необходимость использования библиотек OLE. [MAPIInitialize](mapiinitialize.md) и [OleInitialize](http://msdn.microsoft.com/en-us/library/ms690134%28v=VS.85%29.aspx) вызывать функции [CoInitialize](http://msdn.microsoft.com/en-us/library/ms678543%28VS.85%29.aspx) при инициализации библиотек модели компонентных объектов (COM). Клиенты, которые являются службы необходимо установить специальные флаг MAPI_NT_SERVICE, в член **ulFlags** структуры [MAPIINIT_0](mapiinit_0.md) , который передается в [MAPIInitialize](mapiinitialize.md) и с помощью параметра _ulFlags_ , который передается в [MAPILogonEx](mapilogonex.md) функция для оповещения MAPI их специальных реализаций. 
  
Клиентов MAPI, которые записываются как службы Windows и записи с помощью клиентского интерфейса MAPI имеют дополнительные требования. Они должны установить флаг MAPI_NO_MAIL в вызове [MAPILogonEx](mapilogonex.md). Другие типы клиентов нет необходимости задан флаг для входа в систему, так как он автоматически устанавливается с MAPI.
  
Для обработки сообщений в поток инициализации, клиент MAPI, который реализован в виде службы выполняет следующее.
  
1. Функция [MsgWaitForMultipleObjects](http://msdn.microsoft.com/en-us/library/ms684242%28VS.85%29.aspx) вызывается при основной поток блокируется. 
    
2. Вызывает [GetMessage](http://msdn.microsoft.com/en-us/library/ms644936%28VS.85%29.aspx), [используемых](http://msdn.microsoft.com/en-us/library/ms644955%28VS.85%29.aspx)и [DispatchMessage](http://msdn.microsoft.com/en-us/library/ms644934%28VS.85%29.aspx) последовательность функции Windows для обработки сообщений при [MsgWaitForMultipleObjects](http://msdn.microsoft.com/en-us/library/ms684242%28VS.85%29.aspx) возвращает сумму значение параметра _nCount_ и значение **WAIT_OBJECT_0**, это означает, что сообщение находится в очереди.
    
## <a name="see-also"></a>См. также



[MAPIInitialize](mapiinitialize.md)
  
[MAPIINIT_0](mapiinit_0.md)
  
[MAPILogonEx](mapilogonex.md)


[Проблемы с операционной средой](operating-environment-issues.md)

