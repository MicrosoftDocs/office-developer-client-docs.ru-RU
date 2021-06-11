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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Удаляет режим простоя на основе [FNIDLE](fnidle.md) из системы MAPI. 
  
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

## <a name="parameters"></a>Parameters

 _ftg_
  
> [in] Тег function, который определяет режим простоя, который необходимо удалить.
    
## <a name="return-value"></a>Возвращаемое значение

Нет.
  
## <a name="remarks"></a>Примечания

Любая задача в клиентских приложениях или поставщике услуг может отстранить любую праздную процедуру, для которой она имеет допустимый _параметр ftg._ В частности, простаивающим режимом может быть само зарегистриро- 
  
Следующие функции выполняются с простаивающим двигателем MAPI и простаивающим режимом на основе прототипа [функции FNIDLE:](fnidle.md) 
  
|**Простаиваемая рутинная функция**|**Использование**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Изменяет характеристики зарегистрированного режима простоя.  <br/> |
|**DeregisterIdleRoutine** <br/> |Удаляет зарегистрированную процедуру простоя из системы MAPI.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Отключает или повторно включает зарегистрированный режим простоя без удаления его из системы MAPI.  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Добавляет праздную рутину в систему MAPI с ее включением или без нее.  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Отключит простой движок MAPI для вызываемой программы.  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |Инициализирует простой двигатель MAPI для вызываемой заявки.  <br/> |
   
 **ChangeIdleRoutine,** **DeregisterIdleRoutine** и **EnableIdleRoutine** принимают в качестве параметра ввода тег функции, возвращенный **FtgRegisterIdleRoutine**. 
  
Когда все задачи переднего плана для платформы простаивают, простаивающим двигателем MAPI называются самые приоритетные режимы простоя, готовые к выполнению. Не гарантируется порядок вызова среди праздных режимов одного и того же приоритета. 
  
После того, как режим простоя будет отозвался, простой двигатель не будет вызывать его снова. Любая реализация, вызываемая **DeregisterIdleRoutine,** должна иметь дело с любыми блоками памяти, к которым он передал указатели для простоя двигателя для использования в первоначальном вызове функции **FtgRegisterIdleRoutine.** 
  

