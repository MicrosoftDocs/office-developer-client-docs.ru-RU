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
ms.openlocfilehash: 3ecae23d8631c818fb3d1c6786b2d180e9f32a2e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809329"
---
# <a name="implementing-the-iclassfactory-interface-for-form-servers"></a>Реализация интерфейса IClassFactory для серверов форм

  
  
**Относится к**: Outlook 
  
[IClassFactory](http://msdn.microsoft.com/en-us/library/ms694364%28VS.85%29.aspx) является интерфейса OLE, клиентские приложения для создания новой формы объектов класса сообщений сервера форм. В следующей таблице перечислены методы **IClassFactory** , которые необходимы. 
  
|**Способ**|**Описание**|
|:-----|:-----|
|[CreateInstance](http://msdn.microsoft.com/en-us/library/ms682215%28v=VS.85%29.aspx) <br/> |Создает новый объект формы.  <br/> |
|[LockServer](http://msdn.microsoft.com/en-us/library/ms682332%28v=VS.85%29.aspx) <br/> |Блокирует сервера форм в памяти, чтобы нагрузка на запуска можно избежать при создании нескольких объектов формы.  <br/> |
   
Все сведения, необходимые для реализации этих методов см в разделе COM и службы объект ActiveX в пакете SDK Windows.
  
## <a name="see-also"></a>См. также



[Написание серверного кода формы](writing-form-server-code.md)

