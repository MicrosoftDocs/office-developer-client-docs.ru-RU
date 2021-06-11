---
title: FNIDLE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FNIDLE
api_type:
- COM
ms.assetid: f6b31bb4-69dd-43de-b62b-abfa99557641
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 534f4da15bba5f38bec4cde91206694f8691cbc6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412382"
---
# <a name="fnidle"></a>FNIDLE
 
**Область применения**: Outlook 2013 | Outlook 2016 
  
Определяет режим простоя, который периодически вызывает холостый двигатель MAPI в соответствии с приоритетом. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Определенные функции, реализованные в:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
|Определенная функция, вызванная:  <br/> |MAPI  <br/> |
|Соответствующий тип указателя:  <br/> |PFNIDLE  <br/> |
   
```cpp
BOOL (STDAPICALLTYPE FNIDLE)(
  LPVOID lpvContext
);
```

## <a name="parameters"></a>Parameters

 _lpvContext_
  
> [in] Указатель на блок памяти, который MAPI передает в режим простоя при каждом вызове. Этот указатель передается в простой двигатель MAPI в _параметре pvIdleParam_ [ftgRegisterIdleRoutine.](ftgregisteridleroutine.md) Данные в блоке памяти могут обеспечить контекст для вызова к режиму простоя, например к объекту, на котором необходимо работать, или текущему состоянии длительной операции.
    
## <a name="return-value"></a>Возвращаемое значение

FALSE 
  
> Простаиваемая процедура с прототипом **FNIDLE** всегда должна возвращать FALSE. 
    
## <a name="remarks"></a>Примечания

Конкретные функции обычного простоя определяются реализующим клиентом или поставщиком услуг. 
  
Клиент или поставщик должны ограничить время выполнения каждого состояния обычного простоя. Каждое состояние должно выполнять минимальный объем обработки, обновлять текущее состояние в контекстных данных, на которые указывает  _lpvContext,_ и возвращаться в простой двигатель MAPI. 
  
Клиент или поставщик должны вызвать функцию [MAPI MAPIInitIdle,](mapiinitidle.md) прежде чем он сможет зарегистрировать свою собственную процедуру простоя с вызовом на функцию [FtgRegisterIdleRoutine.](ftgregisteridleroutine.md) 
  
Следующие функции выполняются с простаивающим двигателем MAPI и простаивающим режимом на основе прототипа функции FNIDLE: 
  
|**Простаиваемая рутинная функция**|**Использование**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Изменяет характеристики зарегистрированного режима простоя.  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Удаляет зарегистрированную процедуру простоя из системы MAPI.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Отключает или повторно включает зарегистрированный режим простоя без удаления его из системы MAPI.  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Добавляет праздную рутину в систему MAPI с ее включением или без нее.  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Отключит простой движок MAPI для вызываемой программы.  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |Инициализирует простой двигатель MAPI для вызываемой заявки.  <br/> |
   
**ChangeIdleRoutine,** **DeregisterIdleRoutine** и **EnableIdleRoutine** принимают в качестве параметра ввода тег функции, возвращенный **FtgRegisterIdleRoutine**. 
  
Когда все задачи переднего плана для платформы простаивают, простаивающим двигателем MAPI называются самые приоритетные режимы простоя, готовые к выполнению. Не гарантируется порядок вызова среди праздных режимов одного и того же приоритета. 
  

