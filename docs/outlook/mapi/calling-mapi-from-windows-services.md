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
ms.openlocfilehash: a606b8bf82ce4c06c8e55f6e4df94220bc67501d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385580"
---
# <a name="calling-mapi-from-windows-services"></a>Вызов MAPI из служб Windows

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Чтобы включить клиентские приложения MAPI, которые записываются в виде служб Windows для работы с MAPI-совместимое поставщиков услуг, MAPI, задает некоторые ограничения и требования.
  
Клиенты MAPI имеют следующие ограничения:
  
- Они не могут разрешить пользовательского интерфейса.
    
- Они могут отправлять сообщения только с помощью хранилища тесно связанных сообщений и транспорта поставщика. Кроме того клиентов MAPI можно отправлять и получать сообщения с помощью Exchange Server корпорации Майкрософт или другого поставщика транспорта на стороне сервера. Из-за проблем удостоверения и безопасности между клиентскими приложениями и диспетчер очереди MAPI большинство поставщиков транспорта не поддерживаются в службе. 
    
Все клиентские приложения MAPI, ли они реализованы в качестве службы Windows, необходимо вызвать функцию [MAPIInitialize](mapiinitialize.md) для инициализации библиотеки MAPI. Вызов функции [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) также возникает необходимость использования библиотек OLE. [MAPIInitialize](mapiinitialize.md) и [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) вызывать функции [CoInitialize](https://msdn.microsoft.com/library/ms678543%28VS.85%29.aspx) при инициализации библиотек модели компонентных объектов (COM). Клиенты, которые являются службы необходимо установить специальные флаг MAPI_NT_SERVICE, в член **ulFlags** структуры [MAPIINIT_0](mapiinit_0.md) , который передается в [MAPIInitialize](mapiinitialize.md) и с помощью параметра _ulFlags_ , который передается в [MAPILogonEx](mapilogonex.md) функция для оповещения MAPI их специальных реализаций. 
  
Клиентов MAPI, которые записываются как службы Windows и записи с помощью клиентского интерфейса MAPI имеют дополнительные требования. Они должны установить флаг MAPI_NO_MAIL в вызове [MAPILogonEx](mapilogonex.md). Другие типы клиентов нет необходимости задан флаг для входа в систему, так как он автоматически устанавливается с MAPI.
  
Для обработки сообщений в поток инициализации, клиент MAPI, который реализован в виде службы выполняет следующее.
  
1. Функция [MsgWaitForMultipleObjects](https://msdn.microsoft.com/library/ms684242%28VS.85%29.aspx) вызывается при основной поток блокируется. 
    
2. Вызывает [GetMessage](https://msdn.microsoft.com/library/ms644936%28VS.85%29.aspx), [используемых](https://msdn.microsoft.com/library/ms644955%28VS.85%29.aspx)и [DispatchMessage](https://msdn.microsoft.com/library/ms644934%28VS.85%29.aspx) последовательность функции Windows для обработки сообщений при [MsgWaitForMultipleObjects](https://msdn.microsoft.com/library/ms684242%28VS.85%29.aspx) возвращает сумму значение параметра _nCount_ и значение **WAIT_OBJECT_0**, это означает, что сообщение находится в очереди.
    
## <a name="see-also"></a>См. также



[MAPIInitialize](mapiinitialize.md)
  
[MAPIINIT_0](mapiinit_0.md)
  
[MAPILogonEx](mapilogonex.md)


[Проблемы с операционной средой](operating-environment-issues.md)

