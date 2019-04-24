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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357325"
---
# <a name="mapideinitidle"></a>MAPIDeInitIdle

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Завершает работу модуля бездействия MAPI для вызывающего приложения. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Мапиутил. h  <br/> |
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

Клиентское приложение или поставщик услуг должен вызывать **мапидеинитидле** , когда больше не требуется модуль для бездействия, например, когда он собирается остановить обработку. 
  
Каждый вызов [мапиинитидле](mapiinitidle.md) должен быть сопоставлен последующему вызову **мапидеинитидле**, иначе для вызывающего приложения остается запущен модуль простоя. 
  
Следующие функции работают с модулем бездействия MAPI и с процедурами Idle, основанными на прототипе функции [фнидле](fnidle.md) : 
  
|**Функция неАктивности**|**Usage**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Изменяет характеристики зарегистрированной процедуры бездействия.  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Удаляет зарегистрированную процедуру бездействия из системы MAPI.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Отключает или повторно включает зарегистрированную подпрограмму бездействия, не удаляя ее из системы MAPI.  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Добавляет подпрограмму бездействия в систему MAPI с включением или без него.  <br/> |
|**MAPIDeInitIdle** <br/> |Завершает работу модуля бездействия MAPI для вызывающего приложения.  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |Инициализирует модуль бездействия MAPI для вызывающего приложения.  <br/> |
   
Когда все фоновые задачи для платформы становятся неактивными, модуль бездействия MAPI вызывает подпрограмму самого высокого приоритета, готовую к выполнению. Не существует гарантии того, что вы звоните между процедурами неактивности и одинаковым приоритетом. 
  

