---
title: MAPIInitIdle
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIInitIdle
api_type:
- COM
ms.assetid: b6de7c6a-f2e7-4248-adea-d354924a8bbf
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: fd9a91b089bb06e6dfe34a1a144245d404adb270
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569227"
---
# <a name="mapiinitidle"></a>MAPIInitIdle

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Инициализирует обработчик простоя MAPI для вызывающего приложения. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
```cpp
LONG MAPIInitIdle(
  LPVOID lpvReserved
);
```

## <a name="parameters"></a>Параметры

 _lpvReserved_
  
> [in] ���������������; ������ ���� ����� ����.
    
## <a name="return-value"></a>������������ ��������

Функция **MAPIInitIdle** возвращает ноль при инициализации успешные и 1 в противном случае. Если **MAPIInitIdle** вызван несколько раз, все дополнительные звонки выполняются успешно, но игнорируется за исключением чтобы увеличивают счетчик ссылок. 
  
## <a name="remarks"></a>Замечания

Клиентское приложение или поставщик услуг необходимо вызвать **MAPIInitIdle** перед вызовом других функции простоя модуль. 
  
Каждый вызов **MAPIInitIdle** должна совпадать с следующий вызов [MAPIDeInitIdle](mapideinitidle.md)или простоя модуль остается для вызывающего приложения. 
  
Следующие функции работы с простоя подсистемы MAPI и на основании прототипа функции [FNIDLE](fnidle.md) простоя процедуры: 
  
|**Функция простоя процедуры**|**Использование**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Изменение характеристик зарегистрированных простоя процедуры.  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Удаляет зарегистрированные простоя процедуру из системы MAPI.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Отключает или повторно включает зарегистрированных простоя подпрограмму без его удаления из системы MAPI.  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Добавляет простоя подпрограммы система MAPI, независимо от его включение.  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Завершает работу обработчика бездействия MAPI для вызывающего приложения.  <br/> |
|**MAPIInitIdle** <br/> |Инициализирует обработчик простоя MAPI для вызывающего приложения.  <br/> |
   
При бездействии все задачи переднего плана для платформы, механизм простоя MAPI вызывает наивысший приоритет простоя подпрограммы готов к выполнению. Нет никаких гарантий вызова порядок простоя процедуры одинаковый приоритет. 
  

