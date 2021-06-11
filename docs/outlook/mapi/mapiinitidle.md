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
ms.openlocfilehash: b07c40882c0b9974c71eeb03123e7025b948a75e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432445"
---
# <a name="mapiinitidle"></a>MAPIInitIdle

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Инициализирует простой двигатель MAPI для вызываемой заявки. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
LONG MAPIInitIdle(
  LPVOID lpvReserved
);
```

## <a name="parameters"></a>Parameters

 _lpvReserved_
  
> [in] ���������������; ������ ���� ����� ����.
    
## <a name="return-value"></a>Возвращаемое значение

Функция **MAPIInitIdle** возвращает ноль при успешной инициализации и 1 в противном случае. Если **MAPIInitIdle** вызывается несколько раз, все дополнительные вызовы успешно, но игнорируются, за исключением прибавления отсчета ссылок. 
  
## <a name="remarks"></a>Примечания

Клиентские приложения или поставщик услуг должны вызвать **MAPIInitIdle** перед вызовом любой другой функции простоя двигателя. 
  
Каждый звонок **в MAPIInitIdle** должен соответствовать последующему вызову [MAPIDeInitIdle,](mapideinitidle.md)иначе для вызываемого приложения остается запущен простой двигатель. 
  
Следующие функции выполняются с простаивающим двигателем MAPI и простаивающим режимом на основе прототипа [функции FNIDLE:](fnidle.md) 
  
|**Простаиваемая рутинная функция**|**Использование**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Изменяет характеристики зарегистрированного режима простоя.  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Удаляет зарегистрированную процедуру простоя из системы MAPI.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Отключает или повторно включает зарегистрированный режим простоя без удаления его из системы MAPI.  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Добавляет праздную рутину в систему MAPI с ее включением или без нее.  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Отключит простой движок MAPI для вызываемой программы.  <br/> |
|**MAPIInitIdle** <br/> |Инициализирует простой двигатель MAPI для вызываемой заявки.  <br/> |
   
Когда все задачи переднего плана для платформы простаивают, простаивающим двигателем MAPI называются самые приоритетные режимы простоя, готовые к выполнению. Не гарантируется порядок вызова среди праздных режимов одного и того же приоритета. 
  

