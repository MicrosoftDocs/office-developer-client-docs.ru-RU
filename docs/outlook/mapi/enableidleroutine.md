---
title: EnableIdleRoutine
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.EnableIdleRoutine
api_type:
- COM
ms.assetid: 332ea831-bdf9-4dbd-b9c7-a80f8ba11b3b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e04c872762665f4b3a22559dc2ed1504e7b8f9af
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410223"
---
# <a name="enableidleroutine"></a>EnableIdleRoutine

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Включает или отключает процедуру бездействия на основе [FNIDLE.](fnidle.md) 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
VOID EnableIdleRoutine(
  FTG ftg,
  BOOL fEnable
);
```

## <a name="parameters"></a>Параметры

 _ftg_
  
> [in] Тег функции, определяя процедуру простоя, которую необходимо включить или отключить. 
    
 _fEnable_
  
> [in] Содержит true, если механизм бездействия должен включить процедуру простоя, или FALSE, если он должен отключить его.
    
## <a name="return-value"></a>Возвращаемое значение

Нет.
  
## <a name="remarks"></a>Примечания

Следующие функции работают с механизмом бездействия MAPI и процедурами бездействия на основе прототипа функции [FNIDLE:](fnidle.md) 
  
|**Простаиваемая подпрограмма**|**Использование**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Изменяет характеристики зарегистрированной процедуры бездействия.  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Удаляет зарегистрированную процедуру бездействия из системы MAPI.  <br/> |
|**EnableIdleRoutine** <br/> |Отключает или повторно включает зарегистрированную процедуру бездействия, не удаляя ее из системы MAPI.  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Добавляет процедуру бездействия в систему MAPI с ее включением или без нее.  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Выключает механизм бездействия MAPI для вызывающим приложением.  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |Инициализирует механизм бездействия MAPI для вызывающим приложением.  <br/> |
   
 **ChangeIdleRoutine,** **DeregisterIdleRoutine** и **EnableIdleRoutine** принимают в качестве входного параметра тег функции, возвращенный **FtgRegisterIdleRoutine.** 
  
Когда все задачи переднего плана для платформы простаивают, механизм бездействия MAPI вызывает процедуру простоя с наивысшим приоритетом, готовую к выполнению. Порядок вызовов между процедурами бездействия с одинаковым приоритетом не гарантируется. 
  

