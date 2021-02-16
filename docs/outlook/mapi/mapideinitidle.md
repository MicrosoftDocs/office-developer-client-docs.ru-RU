---
title: MAPIDeInitIdle
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIDeInitIdle
api_type:
- COM
ms.assetid: f7b04486-bc48-4ba4-9f35-f021e06124bf
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 74bba3ea9982838f0d010bbf106c1132df1c2c25
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408210"
---
# <a name="mapideinitidle"></a>MAPIDeInitIdle

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Выключает механизм бездействия MAPI для вызывающим приложением. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
void MAPIDeInitIdle( void );
```

## <a name="parameters"></a>Параметры

Нет. 
  
## <a name="return-value"></a>Возвращаемое значение

Нет.
  
## <a name="remarks"></a>Примечания

Клиентские приложения или поставщик службы должны вызывать **MAPIDeInitIdle,** когда ему больше не нужен механизм бездействия, например, когда он вот-вот остановит обработку. 
  
Каждый вызов [MAPIInitIdle](mapiinitidle.md) должен соответствовать последующим вызовом **MAPIDeInitIdle,** иначе для вызываемого приложения остается запущенный механизм бездействия. 
  
Следующие функции работают с механизмом бездействия MAPI и процедурами бездействия на основе прототипа функции [FNIDLE:](fnidle.md) 
  
|**Простаиваемая подпрограмма**|**Использование**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Изменяет характеристики зарегистрированной процедуры бездействия.  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Удаляет зарегистрированную процедуру бездействия из системы MAPI.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Отключает или повторно включает зарегистрированную процедуру бездействия, не удаляя ее из системы MAPI.  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Добавляет процедуру бездействия в систему MAPI с включением или без нее.  <br/> |
|**MAPIDeInitIdle** <br/> |Выключает механизм бездействия MAPI для вызывающим приложением.  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |Инициализирует механизм бездействия MAPI для вызывающим приложением.  <br/> |
   
Когда все задачи переднего плана для платформы простаивают, механизм бездействия MAPI вызывает процедуру простоя с наивысшим приоритетом, готовую к выполнению. Порядок вызовов между процедурами бездействия с одинаковым приоритетом не гарантируется. 
  

