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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Включает или отключает режим простоя на основе [FNIDLE.](fnidle.md) 
  
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

## <a name="parameters"></a>Parameters

 _ftg_
  
> [in] Тег function, который определяет режим простоя, который необходимо включить или отключить. 
    
 _fEnable_
  
> [in] Содержит TRUE, если простой двигатель должен включить режим простоя, или FALSE, если он должен отключить его.
    
## <a name="return-value"></a>Возвращаемое значение

Нет.
  
## <a name="remarks"></a>Примечания

Следующие функции выполняются с простаивающим двигателем MAPI и простаивающим режимом на основе прототипа [функции FNIDLE:](fnidle.md) 
  
|**Простаиваемая рутинная функция**|**Использование**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Изменяет характеристики зарегистрированного режима простоя.  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Удаляет зарегистрированную процедуру простоя из системы MAPI.  <br/> |
|**EnableIdleRoutine** <br/> |Отключает или повторно включает зарегистрированный режим простоя без удаления его из системы MAPI.  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Добавляет праздную рутину в систему MAPI с ее включением или без нее.  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Отключит простой движок MAPI для вызываемой программы.  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |Инициализирует простой двигатель MAPI для вызываемой заявки.  <br/> |
   
 **ChangeIdleRoutine,** **DeregisterIdleRoutine** и **EnableIdleRoutine** принимают в качестве параметра ввода тег функции, возвращенный **FtgRegisterIdleRoutine**. 
  
Когда все задачи переднего плана для платформы простаивают, простаивающим двигателем MAPI называются самые приоритетные режимы простоя, готовые к выполнению. Не гарантируется порядок вызова среди праздных режимов одного и того же приоритета. 
  

