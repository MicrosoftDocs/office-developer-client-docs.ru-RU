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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Отключит простой движок MAPI для вызываемой программы. 
  
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

Клиентские приложения или поставщик услуг должны вызывать **MAPIDeInitIdle,** если он больше не нуждается в простое двигателя, например, когда он вот-вот прекратит обработку. 
  
Каждый звонок [в MAPIInitIdle](mapiinitidle.md) должен соответствовать последующему вызову **MAPIDeInitIdle,** иначе для вызываемого приложения остается запущен простой двигатель. 
  
Следующие функции выполняются с простаивающим двигателем MAPI и простаивающим режимом на основе прототипа [функции FNIDLE:](fnidle.md) 
  
|**Простаиваемая рутинная функция**|**Использование**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Изменяет характеристики зарегистрированного режима простоя.  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Удаляет зарегистрированную процедуру простоя из системы MAPI.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Отключает или повторно включает зарегистрированный режим простоя без удаления его из системы MAPI.  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Добавляет праздную рутину в систему MAPI с ее включением или без нее.  <br/> |
|**MAPIDeInitIdle** <br/> |Отключит простой движок MAPI для вызываемой программы.  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |Инициализирует простой двигатель MAPI для вызываемой заявки.  <br/> |
   
Когда все задачи переднего плана для платформы простаивают, простаивающим двигателем MAPI называются самые приоритетные режимы простоя, готовые к выполнению. Не гарантируется порядок вызова среди праздных режимов одного и того же приоритета. 
  

