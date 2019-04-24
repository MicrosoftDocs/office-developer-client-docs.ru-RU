---
title: UPHIER
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a75ca0dd-9c50-2a9f-6c59-1f8020833a01
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 45ef7ce9291376ac020035f0bde6172caf6cc01b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359425"
---
# <a name="uphier"></a>UPHIER
 
**Область применения**: Outlook 2013 | Outlook 2016 
  
Сведения для синхронизации иерархии папок во время [состояния иерархии отправки](upload-hierarchy-state.md).
  
## <a name="quick-info"></a>Краткие сведения

```cpp
struct UPHIER 
{ 
    ULONG ulFlags; 
    LPSTREAM pstmReserved; 
    UINT iEnt; 
    UINT cEnt; 
};
```

## <a name="members"></a>Элементы

_ulFlags_
  
> возврата Флаги для изменения поведения при синхронизации иерархии папок.
    
  - UPH_OK
    
    - возврата Отправка выполнена успешно. Клиент устанавливает это после успешной отправки информации на сервер. При просмотре этого флага в Outlook удаляются все внутренние сведения о регистрации, в которых указана иерархия папок, которую необходимо обновить. 
    
    - Клиент передает значение HRESULT в случае неудачной отправки.
    
_pstmReserved_
  
> вышли Этот член зарезервирован для внутреннего использования Outlook и не поддерживается.
    
_Иент_
  
> вышли Индекс, отслеживающий синхронизацию числа папок, заданных ** с помощью цента. 
    
_Центов_
  
> вышли Количество папок, которые не синхронизированы.
    
## <a name="see-also"></a>См. также

- [Сведения об API репликации](about-the-replication-api.md)
- [Сведения о конечном автомате репликации](about-the-replication-state-machine.md)
- [Константы MAPI](mapi-constants.md)

