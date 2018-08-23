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
ms.openlocfilehash: 34d6eb0653c3eb550bf03242a2c1b2acc3330a13
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572293"
---
# <a name="upfld"></a>UPFLD

**Применимо к**: Outlook 2013 | Outlook 2016 
  
Сведения для передачи в папку во время [загрузки состояние папки](upload-folder-state.md).
  
## <a name="quick-info"></a>Краткие сведения

```cpp
struct UPFLD 
{ 
    ULONG ulFlags; 
    LPMAPIFOLDER pfld; 
    FEID feid; 
}; 

```

## <a name="members"></a>Members

_ulFlags_
  
>  [out] и [in] флаги для определения соответствующих действий для uplaod. 
    
  - UPF_NEW
    
    - [out] Папка является новым.
    
  - UPF_MOD_PARENT
    
    - [out] Папка была перемещена.
    
  - UPF_MOD_PROPS
    
    - [out] Свойства папки были изменены.
    
  - UPF_DEL
    
    - [out] Папка была удалена.
    
  - UPF_OK
    
    - [in] Отправка прошла успешно. Клиент устанавливает это после отправки сведений о папке на сервере.
    
_pfld_
  
> [out] Объект открыть папку для загрузки.
    
_feid_
  
> [out] Идентификатор записи папки.
    
## <a name="see-also"></a>См. также

- [Сведения об API репликации](about-the-replication-api.md) 
- [Сведения о конечном автомате репликации](about-the-replication-state-machine.md)
- [��������� MAPI](mapi-constants.md)

