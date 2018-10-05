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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388051"
---
# <a name="implementing-the-iclassfactory-interface-for-form-servers"></a>Реализация интерфейса IClassFactory для серверов форм

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
[IClassFactory](https://msdn.microsoft.com/library/ms694364%28VS.85%29.aspx) является интерфейса OLE, клиентские приложения для создания новой формы объектов класса сообщений сервера форм. В следующей таблице перечислены методы **IClassFactory** , которые необходимы. 
  
|**Способ**|**Описание**|
|:-----|:-----|
|[CreateInstance](https://msdn.microsoft.com/library/ms682215%28v=VS.85%29.aspx) <br/> |Создает новый объект формы.  <br/> |
|[LockServer](https://msdn.microsoft.com/library/ms682332%28v=VS.85%29.aspx) <br/> |Блокирует сервера форм в памяти, чтобы нагрузка на запуска можно избежать при создании нескольких объектов формы.  <br/> |
   
Все сведения, необходимые для реализации этих методов см в разделе COM и службы объект ActiveX в пакете SDK Windows.
  
## <a name="see-also"></a>См. также



[Написание серверного кода формы](writing-form-server-code.md)

