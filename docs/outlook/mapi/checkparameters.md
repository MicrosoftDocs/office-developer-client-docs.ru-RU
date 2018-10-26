---
title: CheckParameters
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.CheckParameters
api_type:
- COM
ms.assetid: ba33866a-c9c4-454a-9549-72455c61ee97
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f01d0ad7e7e6b1ad7a5e4c4838bb46ca143e0968
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567057"
---
# <a name="checkparameters"></a>CheckParameters

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Вызывает внутренней функции для проверки параметров отладки на методы поставщика службы вызывается MAPI. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapival.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Поставщики услуг  <br/> |
   
```cpp
HRESULT CheckParameters(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a>Параметры

 _eMethod_
  
> [in] Указывает перечисление, метод для проверки. 
    
 _Первый_
  
> [in] Указатель на первый аргумент в стеке.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> The call succeeded.
    
## <a name="remarks"></a>Замечания

Макрос **CheckParameters** был заменен макрос [CheckParms](checkparms.md) . **CheckParms** рекомендуется для всех платформ. 
  

