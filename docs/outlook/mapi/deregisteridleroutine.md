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
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: 85161fb87e798bbb03b267f9760870da1246e48d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808286"
---
# <a name="deregisteridleroutine"></a>DeregisterIdleRoutine

  
  
**Применимо к**: Outlook 
  
Удаляет [FNIDLE](fnidle.md) на основе простоя общей процедуры из системы MAPI. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
```cpp
VOID DeregisterIdleRoutine(
  FTG ftg
);
```

## <a name="parameters"></a>Parameters

 _ftg_
  
> [in] Функция тег, идентифицирующий простоя процедуры требуется удалить.
    
## <a name="return-value"></a>Возвращаемое значение

Нет.
  
## <a name="remarks"></a>Замечания

Любой из задач в клиентском приложении или поставщик услуг можно отменить регистрацию любой простоя подпрограммы, для которого он имеет допустимый _ftg_ параметр. В частности простоя процедуры можно отменить регистрацию самого. 
  
Следующие функции работы с простоя подсистемы MAPI и на основании прототипа функции [FNIDLE](fnidle.md) простоя процедуры: 
  
|**Функция простоя процедуры**|**Использование**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Изменение характеристик зарегистрированных простоя процедуры.  <br/> |
|**DeregisterIdleRoutine** <br/> |Удаляет зарегистрированные простоя процедуру из системы MAPI.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Отключает или повторно включает зарегистрированных простоя подпрограмму без его удаления из системы MAPI.  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Добавляет простоя подпрограммы система MAPI, независимо от его включение.  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Завершает работу обработчика бездействия MAPI для вызывающего приложения.  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |Инициализирует обработчик простоя MAPI для вызывающего приложения.  <br/> |
   
 **ChangeIdleRoutine**, **DeregisterIdleRoutine**и **EnableIdleRoutine** принимают в качестве входного параметра, функция тег возвращаемых **FtgRegisterIdleRoutine**. 
  
При бездействии все задачи переднего плана для платформы, механизм простоя MAPI вызывает наивысший приоритет простоя подпрограммы готов к выполнению. Нет никаких гарантий вызова порядок простоя процедуры одинаковый приоритет. 
  
После простоя подпрограммы отменяется, простоя модуль не вызывает его еще раз. Любой реализации, который вызывает **DeregisterIdleRoutine** необходимо отменить любые блоки памяти, к которым он передается указатели простоя системы в его исходное вызове функции **FtgRegisterIdleRoutine** . 
  

