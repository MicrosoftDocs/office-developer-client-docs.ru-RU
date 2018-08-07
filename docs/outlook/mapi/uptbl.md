---
title: UPTBL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 39d9ad3b-ff4b-8378-a3ac-d5621c7ef7f1
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 70d23bebfda10339ffb05f573c8c309a44f09d7f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812591"
---
# <a name="uptbl"></a>UPTBL

**Относится к**: Outlook 
  
Информация для загрузки содержимого папки во время [загрузки состояния в таблице](upload-table-state.md).
  
## <a name="quick-info"></a>Краткие сведения

```cpp
struct UPTBL 
{ 
    ULONG ulFlags; 
    LPSTREAM pstmReserved; 
    LPSTR pszName; 
    FEID feid; 
    UINT uintReserved; 
    UPTBLE rgte[2]; 
    UINT iEnt; 
    UINT cEnt; 
    PUPMOV pupmovHead; 
    void* pReserved; 
};
```

## <a name="members"></a>Members

_ulFlags_
  
> [in] Флаги для определения соответствующего поведения во время загрузки.
    
  - UPT_OK
    
    - [in] Отправка прошла успешно. Клиент устанавливает это после отправки контента папки на сервере.
    
_pstmReserved_
  
> [out] Этот член зарезервирован для внутреннего использования Outlook и не поддерживается. 
    
_параметра pszName_
  
> [out] Имя папки.
    
_feid_
  
> [out] Идентификатор записи папки.
    
_uintReserved_
  
> [out] Этот член зарезервирован для внутреннего использования Outlook и не поддерживается. 
    
_rgte_
  
> [out] Структура для хранения следующие сведения для обычного (или не скрыты) элементы и связанные (или скрытых) элементы в папке: _rgte [0]_ — для обычных элементов, а _rgte [1]_ — для связанных элементов. 
    
   - число новые или измененные элементы
   - число чтения элементов 
   - Количество удаленных элементов
    
 _iEnt_
  
> [out] Индекс для отслеживания Отправка изменений, указанного идентификатором _централизованной_.
    
_централизованной_
  
> [out] Количество изменений в папку.
    
_pupmovHead_
  
> [out] Цепочка [UPMOV](upmov.md) структуры. 
    
_Сохраняются_
  
> [out] Этот член зарезервирован для внутреннего использования Outlook и не поддерживается.
    
## <a name="see-also"></a>См. также

- [Сведения об API репликации](about-the-replication-api.md)
- [Сведения о конечном автомате репликации](about-the-replication-state-machine.md)
- [��������� MAPI](mapi-constants.md)
- [UPTBLE](uptble.md)

