---
title: Реализация интерфейса IClassFactory для серверов форм
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22402261-c0fc-49bd-a222-e31989d6ff30
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 12d854b72632653d9e1081c9e726c0fe7087bc27
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310033"
---
# <a name="implementing-the-iclassfactory-interface-for-form-servers"></a>Реализация интерфейса IClassFactory для серверов форм

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
[IClassFactory](https://msdn.microsoft.com/library/ms694364%28VS.85%29.aspx) — это интерфейс OLE, который клиентские приложения используют для создания новых объектов форм класса сообщений сервера форм. В следующей таблице перечислены необходимые методы **IClassFactory.** 
  
|**Способ**|**Описание**|
|:-----|:-----|
|[CreateInstance](https://msdn.microsoft.com/library/ms682215%28v=VS.85%29.aspx) <br/> |Создает новый объект формы.  <br/> |
|[LockServer](https://msdn.microsoft.com/library/ms682332%28v=VS.85%29.aspx) <br/> |Блокирует сервер форм в памяти, чтобы избежать накладных расходов при запуске нескольких объектов форм.  <br/> |
   
Все сведения, необходимые для реализации этих методов, см. в разделе com и ActiveX Object Services в Windows SDK.
  
## <a name="see-also"></a>См. также



[Написание кода сервера форм](writing-form-server-code.md)

