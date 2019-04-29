---
title: UPDELE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c38aa8be-ae77-0c40-9843-42e07b80db6b
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 9bd61739b14d0ec382a9d582689c1049fe89429b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424884"
---
# <a name="updele"></a>UPDELE

**Относится к**: Outlook 2013 | Outlook 2016 
  
Расширенные сведения об элементах, удаленных в локальном хранилище. Эти сведения используются в состоянии состояния [отправки для удаления](upload-delete-status-state.md).
  
## <a name="quick-info"></a>Краткие сведения

```cpp
struct UPDELE 
{ 
    ULONG ulFlags; 
    SKEY skey; 
    DWORD   dwReserved; 
    SBinary binChg; 
    SBinary binPcl; 
    SKEY skeyDst; 
    PUPMOV pupmov; 
};
```

## <a name="members"></a>Элементы

_ulFlags_
  
> [out]/[in] флаги для определения надлежащего поведения при отправке.
    
  - UPD_ASSOC
    
    - вышли Связан элемент.
    
  - UPD_MOV
    
    - вышли Элемент был перемещен.
    
  - UPD_OK 
    
    - возврата Отправка выполнена успешно. Клиент устанавливает это после отправки информации на сервер.
    
  - UPD_MOVED
    
    - возврата Элемент успешно перемещен.
    
  - UPD_UPDATE
    
    - возврата ПоМетить исходный элемент как измененный.
    
  - UPD_COMMIT
    
    - возврата ЗаФиксировать состояние отправки сейчас (запись 0).
    
_скэй_
  
> вышли Ключ источника элемента.
    
_Двресервед_
  
> [out] Данный элемент резервируется для внутреннего использования в Outlook и не поддерживается.
    
_Бинчг_
  
> вышли Изменение ключа целевого элемента, если элемент был перемещен.
    
_Бинпкл_
  
> вышли Изменение списка элементов назначения, если элемент был перемещен.
    
_Скэйдст_
  
> вышли Исходный ключ целевого элемента, если элемент был перемещен.
    
_пупмов_
  
> вышли Сведения о папке назначения, если элемент был перемещен.
    
## <a name="see-also"></a>См. также

- [Сведения об API репликации](about-the-replication-api.md) 
- [Сведения о конечном автомате репликации](about-the-replication-state-machine.md)
- [Константы MAPI](mapi-constants.md)
- [SKEY](skey.md)
- [UPDEL](updel.md)
- [UPMOV](upmov.md)

