---
title: Вызов MAPI из Windows служб
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: debf7ec3-e9f9-4912-b9a2-fc0953a56a01
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: a606b8bf82ce4c06c8e55f6e4df94220bc67501d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318109"
---
# <a name="calling-mapi-from-windows-services"></a>Вызов MAPI из Windows служб

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Чтобы клиентские приложения MAPI, написанные как Windows, могли работать с поставщиками услуг, совместимыми с MAPI, MAPI накладывает несколько ограничений и требований.
  
Клиенты MAPI имеют следующие ограничения:
  
- Они не могут разрешить пользовательский интерфейс.
    
- Они могут отправлять сообщения только в тесном хранилище сообщений и поставщике транспорта. Кроме того, клиенты MAPI могут отправлять и получать сообщения, используя только Microsoft Exchange Server или другого поставщика транспорта на сервере. Из-за проблем с удостоверениями и безопасностью между клиентских приложений и пулером MAPI большинство поставщиков транспорта не поддерживаются в службе. 
    
Все клиентские приложения MAPI, вне зависимости от того, реализуются ли они в качестве Windows, должны вызвать функцию [MAPIInitialize](mapiinitialize.md) для инициализации библиотек MAPI. Вызов функции [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) также необходим для использования библиотек OLE. И [MAPIInitialize,](mapiinitialize.md) и [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) делают вызовы в [функцию CoInitialize](https://msdn.microsoft.com/library/ms678543%28VS.85%29.aspx) для инициализации библиотек компонентной объектной модели (COM). Клиенты, которые являются службами, должны установить специальный флаг MAPI_NT_SERVICE в члене **ulFlags** структуры [MAPIINIT_0,](mapiinit_0.md) которая передается [в MAPIInitialize,](mapiinitialize.md) и в  _параметре ulFlags,_ который передается функции [MAPILogonEx](mapilogonex.md) для информирования MAPI об их особой реализации. 
  
Клиенты MAPI, написанные как Windows службы и написанные с клиентского интерфейса MAPI, имеют дополнительное требование. Они должны установить флаг MAPI_NO_MAIL в [вызове MAPILogonEx](mapilogonex.md). Другим типам клиентов не нужно устанавливать флаг для logon, так как он автоматически задается MAPI.
  
Для обработки сообщений в потоке инициализации клиент MAPI, реализуемый в качестве службы, выполняет следующее:
  
1. Вызывает [функцию MsgWaitForMultipleObjects](https://msdn.microsoft.com/library/ms684242%28VS.85%29.aspx) при блоке основного потока. 
    
2. Вызывает последовательность функций [GetMessage,](https://msdn.microsoft.com/library/ms644936%28VS.85%29.aspx) [TranslateMessage](https://msdn.microsoft.com/library/ms644955%28VS.85%29.aspx)и [DispatchMessage](https://msdn.microsoft.com/library/ms644934%28VS.85%29.aspx) Windows для обработки сообщения, когда [MsgWaitForMultipleObjects](https://msdn.microsoft.com/library/ms684242%28VS.85%29.aspx) возвращает сумму значения параметра _nCount_ и значение **WAIT_OBJECT_0,** что указывает на то, что сообщение находится в очереди.
    
## <a name="see-also"></a>См. также



[MAPIInitialize](mapiinitialize.md)
  
[MAPIINIT_0](mapiinit_0.md)
  
[MAPILogonEx](mapilogonex.md)


[Проблемы с операционной средой](operating-environment-issues.md)

