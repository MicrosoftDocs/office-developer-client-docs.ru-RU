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
ms.openlocfilehash: b401f54df020fb6553cbdcc5b85206ee422a8429
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438115"
---
# <a name="uptbl"></a>UPTBL

**Относится к**: Outlook 2013 | Outlook 2016 
  
Сведения о загрузке содержимого папки во время состояния [отправки таблицы.](upload-table-state.md)
  
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

## <a name="members"></a>Элементы

_ulFlags_
  
> [in] Флаги для определения соответствующего поведения во время отправки.
    
  - UPT_OK
    
    - [in] Отправка прошла успешно. Клиент устанавливает это после отправки содержимого папки на сервер.
    
_pstmReserved_
  
> [] Данный элемент резервируется для внутреннего использования в Outlook и не поддерживается. 
    
_pszName_
  
> [out] Имя папки.
    
_feid_
  
> [out] Идентификатор записи папки.
    
_uintReserved_
  
> [out] Данный элемент резервируется для внутреннего использования в Outlook и не поддерживается. 
    
_rgte_
  
> [out] Структура для удержания следующих сведений для обычных (или не скрытых) элементов и связанных (или скрытых) элементов в папке:  _rgte[0]_ — для обычных элементов, а  _rgte[1]_ — для связанных элементов. 
    
   - количество новых или измененных элементов
   - количество прочитаных элементов 
   - количество удаленных элементов
    
 _iEnt_
  
> [out] Индекс для отслеживания отправки количества изменений, указанных  _в cEnt_.
    
_cEnt_
  
> [out] Количество изменений в папке.
    
_pupmovHead_
  
> [out] Цепочка [структур UPMOV.](upmov.md) 
    
_pReserved_
  
> [out] Данный элемент резервируется для внутреннего использования в Outlook и не поддерживается.
    
## <a name="see-also"></a>См. также

- [Сведения об API репликации](about-the-replication-api.md)
- [Сведения о конечном автомате репликации](about-the-replication-state-machine.md)
- [Константы MAPI](mapi-constants.md)
- [UPTBLE](uptble.md)

