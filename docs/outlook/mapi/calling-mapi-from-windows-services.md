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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318109"
---
# <a name="calling-mapi-from-windows-services"></a>Вызов MAPI из служб Windows

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Чтобы включить клиентские приложения MAPI, которые создаются как службы Windows для работы с поставщиками услуг, совместимыми с MAPI, MAPI накладывает несколько ограничений и требований.
  
Клиенты MAPI имеют следующие ограничения:
  
- Они не могут разрешить пользовательскому интерфейсу.
    
- Они могут отправлять сообщения только через тесно связанное хранилище сообщений и поставщик транспорта. Кроме того, клиенты MAPI могут отправлять и получать сообщения с помощью только сервера Microsoft Exchange Server или другого поставщика транспорта на основе сервера. Из-за проблем с идентификацией и безопасностью между клиентскими приложениями и диспетчером очереди MAPI большинство поставщиков транспорта не поддерживаются в службе. 
    
Все клиентские приложения MAPI независимо от того, реализуются ли они как службы Windows, должны вызвать функцию [мапиинитиализе](mapiinitialize.md) для инициализации библиотек MAPI. Вызов функции [олеинитиализе](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) также необходимо для использования библиотек OLE. Как [мапиинитиализе](mapiinitialize.md) , так и [олеинитиализе](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) выполняют вызовы функции [CoInitialize](https://msdn.microsoft.com/library/ms678543%28VS.85%29.aspx) для инициализации библиотек COM (Component Object Model). Клиенты, которые являются службами, должны задать специальный флаг, MAPI_NT_SERVICE, в элементе **ulFlags** структуры [MAPIINIT_0](mapiinit_0.md) , который передается в [мапиинитиализе](mapiinitialize.md) , и в параметре _ulFlags_ , который передается в функцию [мапилогонекс](mapilogonex.md) для информирования MAPI о их особой реализации. 
  
Клиенты MAPI, написанные как службы Windows и записанные с помощью клиентского интерфейса MAPI, имеют дополнительные требования. Необходимо установить флаг MAPI_NO_MAIL в вызове [мапилогонекс](mapilogonex.md). Другим типам клиентов не требуется устанавливать флаг для входа в систему, так как он автоматически задается MAPI.
  
Для обработки сообщений в потоке инициализации клиент MAPI, реализованный как служба, выполняет следующие действия:
  
1. Вызывает функцию [мсгваитформултиплеобжектс](https://msdn.microsoft.com/library/ms684242%28VS.85%29.aspx) , когда блокируется главный поток. 
    
2. Вызывает последовательность функций [транслатемессаже](https://msdn.microsoft.com/library/ms644955%28VS.85%29.aspx), а также [диспатчмессаже](https://msdn.microsoft.com/library/ms644934%28VS.85%29.aspx) для обработки [сообщения, когда](https://msdn.microsoft.com/library/ms644936%28VS.85%29.aspx) [мсгваитформултиплеобжектс](https://msdn.microsoft.com/library/ms684242%28VS.85%29.aspx) возвращает сумму значения параметра _нкаунт_ и значение **WAIT_OBJECT_0**, что указывает на то, что сообщение находится в очереди.
    
## <a name="see-also"></a>См. также



[MAPIInitialize](mapiinitialize.md)
  
[MAPIINIT_0](mapiinit_0.md)
  
[MAPILogonEx](mapilogonex.md)


[Проблемы с операционной средой](operating-environment-issues.md)

