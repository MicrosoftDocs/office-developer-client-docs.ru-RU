---
title: UPFLD
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6da9d6b6-a016-ccef-77da-3e037c30450d
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: c8f7bdc5864c049d8db6f38e92a69c97b6f9dc73
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431360"
---
# <a name="upfld"></a>UPFLD

**Относится к**: Outlook 2013 | Outlook 2016 
  
Сведения для отправки папки в [состояние папки отправки](upload-folder-state.md).
  
## <a name="quick-info"></a>Краткие сведения

```cpp
struct UPFLD 
{ 
    ULONG ulFlags; 
    LPMAPIFOLDER pfld; 
    FEID feid; 
}; 

```

## <a name="members"></a>Элементы

_ulFlags_
  
>  [out]/[in] флаги для определения подходящих действий для уплаод. 
    
  - UPF_NEW
    
    - вышли Папка является новой.
    
  - UPF_MOD_PARENT
    
    - вышли Папка была перемещена.
    
  - UPF_MOD_PROPS
    
    - вышли Свойства папки изменены.
    
  - UPF_DEL
    
    - вышли Удалена папка.
    
  - UPF_OK
    
    - возврата Отправка выполнена успешно. Клиент устанавливает это после отправки сведений о папке на сервер.
    
_пфлд_
  
> вышли Объект открываемой папки для отправки.
    
_feid_
  
> [out] Идентификатор записи папки.
    
## <a name="see-also"></a>См. также

- [Сведения об API репликации](about-the-replication-api.md) 
- [Сведения о конечном автомате репликации](about-the-replication-state-machine.md)
- [Константы MAPI](mapi-constants.md)

