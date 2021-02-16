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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Инициализирует механизм бездействия MAPI для вызывающим приложением. 
  
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

## <a name="parameters"></a>Параметры

 _lpvReserved_
  
> [in] ���������������; ������ ���� ����� ����.
    
## <a name="return-value"></a>Возвращаемое значение

Функция **MAPIInitIdle** возвращает ноль при успешной инициализации, а 1 — в противном случае. Если **MAPIInitIdle** вызывается несколько раз, все дополнительные вызовы будут успешными, но будут игнорироваться, за исключением того, что добавит количество ссылок. 
  
## <a name="remarks"></a>Примечания

Клиентские приложения или поставщик службы должны вызвать **MAPIInitIdle перед** вызовом любой другой функции бездействия ядер. 
  
Каждый вызов **MAPIInitIdle** должен соответствовать последующим вызовом [MAPIDeInitIdle,](mapideinitidle.md)иначе механизм бездействия остается запущенным для вызываемого приложения. 
  
Следующие функции работают с механизмом бездействия MAPI и процедурами бездействия на основе прототипа функции [FNIDLE:](fnidle.md) 
  
|**Простаиваемая подпрограмма**|**Использование**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Изменяет характеристики зарегистрированной процедуры бездействия.  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Удаляет зарегистрированную процедуру бездействия из системы MAPI.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Отключает или повторно включает зарегистрированную процедуру бездействия, не удаляя ее из системы MAPI.  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Добавляет процедуру бездействия в систему MAPI с ее включением или без нее.  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Выключает механизм бездействия MAPI для вызывающим приложением.  <br/> |
|**MAPIInitIdle** <br/> |Инициализирует механизм бездействия MAPI для вызывающим приложением.  <br/> |
   
Когда все задачи переднего плана для платформы простаивают, механизм бездействия MAPI вызывает процедуру простоя с наивысшим приоритетом, готовую к выполнению. Порядок вызовов между процедурами бездействия с одинаковым приоритетом не гарантируется. 
  

