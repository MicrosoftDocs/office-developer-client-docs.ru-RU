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
ms.openlocfilehash: 33f4634623662b7bc09e0830e8bd0b51adc7799d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583500"
---
# <a name="mapideinitidle"></a>MAPIDeInitIdle

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Завершает работу обработчика бездействия MAPI для вызывающего приложения. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
```cpp
void MAPIDeInitIdle( void );
```

## <a name="parameters"></a>Параметры

Нет. 
  
## <a name="return-value"></a>Возвращаемое значение

Нет.
  
## <a name="remarks"></a>Замечания

Клиентское приложение или поставщик услуг должен вызывать **MAPIDeInitIdle** , когда больше нет необходимости простоя модуля, например, когда он должен остановить обработку. 
  
Каждый вызов [MAPIInitIdle](mapiinitidle.md) должна совпадать с следующий вызов **MAPIDeInitIdle**или простоя модуль остается для вызывающего приложения. 
  
Следующие функции работы с простоя подсистемы MAPI и на основании прототипа функции [FNIDLE](fnidle.md) простоя процедуры: 
  
|**Функция простоя процедуры**|**Использование**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Изменение характеристик зарегистрированных простоя процедуры.  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Удаляет зарегистрированные простоя процедуру из системы MAPI.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Отключает или повторно включает зарегистрированных простоя подпрограмму без его удаления из системы MAPI.  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Добавляет простоя подпрограммы система MAPI, независимо от его включение.  <br/> |
|**MAPIDeInitIdle** <br/> |Завершает работу обработчика бездействия MAPI для вызывающего приложения.  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |Инициализирует обработчик простоя MAPI для вызывающего приложения.  <br/> |
   
При бездействии все задачи переднего плана для платформы, механизм простоя MAPI вызывает наивысший приоритет простоя подпрограммы готов к выполнению. Нет никаких гарантий вызова порядок простоя процедуры одинаковый приоритет. 
  

