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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339398"
---
# <a name="enableidleroutine"></a>EnableIdleRoutine

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Включает или отключает подпрограмму бездействия на основе [фнидле](fnidle.md) . 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Мапиутил. h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
VOID EnableIdleRoutine(
  FTG ftg,
  BOOL fEnable
);
```

## <a name="parameters"></a>Параметры

 _ФТГ_
  
> возврата Тег Function, определяющий подпрограмму, подлежащая включению или отключению. 
    
 _Фенабле_
  
> возврата Содержит значение TRUE, если антивирусная программа должна включить функцию Idle, или FALSE, если она должна быть отключена.
    
## <a name="return-value"></a>Возвращаемое значение

Нет.
  
## <a name="remarks"></a>Примечания

Следующие функции работают с модулем бездействия MAPI и с процедурами Idle, основанными на прототипе функции [фнидле](fnidle.md) : 
  
|**Функция неАктивности**|**Usage**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Изменяет характеристики зарегистрированной процедуры бездействия.  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Удаляет зарегистрированную процедуру бездействия из системы MAPI.  <br/> |
|**EnableIdleRoutine** <br/> |Отключает или повторно включает зарегистрированную подпрограмму бездействия, не удаляя ее из системы MAPI.  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Добавляет подпрограмму бездействия в систему MAPI с включением или без него.  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Завершает работу модуля бездействия MAPI для вызывающего приложения.  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |Инициализирует модуль бездействия MAPI для вызывающего приложения.  <br/> |
   
 **Чанжеидлераутине**, **дерегистеридлераутине**и **енаблеидлераутине** принимают в качестве входного параметра тег функции, возвращенный методом **фтгрегистеридлераутине**. 
  
Когда все фоновые задачи для платформы становятся неактивными, модуль бездействия MAPI вызывает подпрограмму самого высокого приоритета, готовую к выполнению. Не существует гарантии того, что вы звоните между процедурами неактивности и одинаковым приоритетом. 
  

