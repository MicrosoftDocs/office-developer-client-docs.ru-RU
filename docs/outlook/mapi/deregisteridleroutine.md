---
title: DeregisterIdleRoutine
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DeregisterIdleRoutine
api_type:
- COM
ms.assetid: a8ada6fe-9963-4c25-b4b4-db77f9517368
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 62231a900dbe01ebe1e848355226c0589072cd42
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404563"
---
# <a name="deregisteridleroutine"></a>DeregisterIdleRoutine

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Удаляет процедуру бездействия на основе [FNIDLE](fnidle.md) из системы MAPI. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
VOID DeregisterIdleRoutine(
  FTG ftg
);
```

## <a name="parameters"></a>Параметры

 _ftg_
  
> [in] Тег функции, определяя процедуру простоя, которую необходимо удалить.
    
## <a name="return-value"></a>Возвращаемое значение

Нет.
  
## <a name="remarks"></a>Примечания

Любая задача в клиентских приложениях или поставщиках служб может отоздать регистрацию любой процедуры бездействия, для которой она имеет допустимый _параметр ftg._ В частности, простаиваемая процедура может отоздать регистрацию. 
  
Следующие функции работают с механизмом бездействия MAPI и процедурами бездействия на основе прототипа функции [FNIDLE:](fnidle.md) 
  
|**Простаиваемая подпрограмма**|**Использование**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Изменяет характеристики зарегистрированной процедуры бездействия.  <br/> |
|**DeregisterIdleRoutine** <br/> |Удаляет зарегистрированную процедуру бездействия из системы MAPI.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Отключает или повторно включает зарегистрированную процедуру бездействия, не удаляя ее из системы MAPI.  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Добавляет процедуру бездействия в систему MAPI с включением или без нее.  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Выключает механизм бездействия MAPI для вызывающим приложением.  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |Инициализирует механизм бездействия MAPI для вызывающим приложением.  <br/> |
   
 **ChangeIdleRoutine,** **DeregisterIdleRoutine** и **EnableIdleRoutine** принимают в качестве входного параметра тег функции, возвращенный **FtgRegisterIdleRoutine.** 
  
Когда все задачи переднего плана для платформы простаивают, механизм бездействия MAPI вызывает процедуру простоя с наивысшим приоритетом, готовую к выполнению. Порядок вызовов между процедурами бездействия с одинаковым приоритетом не гарантируется. 
  
После того как процедура простоя будет отознана, механизм простоя не будет вызывать ее снова. Любая реализация, вызываемая **DeregisterIdleRoutine,** должна иметь дело с блоками памяти, в которые он передал указатели, чтобы механизм бездействия использовали его при первоначальном вызове функции **FtgRegisterIdleRoutine.** 
  

