---
title: Ифрибусисуппортлоадфрибусидата
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f0baa310-7a53-07ee-0a7d-33dd1fb465c2
description: Возвращает для каждого указанного пользователя интерфейс для перечисления блоков сведений о занятости в пределах диапазона времени.
ms.openlocfilehash: e55f902117a20bfefaa5d9a2f3a067cb78ec86cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319406"
---
# <a name="ifreebusysupportloadfreebusydata"></a>IFreeBusySupport::LoadFreeBusyData

Возвращает для каждого указанного пользователя интерфейс для перечисления блоков сведений о занятости в пределах диапазона времени. 
  
## <a name="quick-info"></a>Краткие сведения

Обратитесь к разделу [ифрибусисуппорт](ifreebusysupport.md).
  
```cpp
HRESULT LoadFreeBusyData( 
    ULONG cMax,  
    FBUser *rgfbuser, 
    IFreeBusyData **prgfbdata,  
    HRESULT *phrStatus, 
    ULONG *pcRead 
);
```

## <a name="parameters"></a>Параметры

_Кмакс_
  
> возврата Число возвращаемых интерфейсов [ифрибусидата](ifreebusydata.md) . 
    
_ргфбусер_
  
> возврата Массив пользователей сведений о занятости для получения данных.
    
_пргфбдата_
  
> возврата вышли Массив интерфейсов **ифрибусидата** , соответствующих массиву _ргфбусер_ структуры [фбусер](fbuser.md) . 
    
   > [!NOTE]
   > Этот массив указателей выделяется вызывающим и освобождается вызывающим абонентом. Фактические интерфейсы, на которые указывает, освобождаются, когда вызывающая сторона выполнила их. 
  
_Фрстатус_
  
> вышли Массив результатов **HRESULT** для получения каждого соответствующего интерфейса **ифрибусидата** . Значение может быть равно NULL. Если соответствующий _пргфбдата_ является допустимым, в результате получается значение S_OK. 
    
_Пкреад_
  
>  вышли Фактическое количество пользователей, для которых был найден интерфейс **ифрибусидата** . 
    
## <a name="return-values"></a>Возвращаемые значения

S_OK if the call succeeded; otherwise, an error code.
  
## <a name="see-also"></a>См. также

- [Константы (API сведений о доступности)](constants-free-busy-api.md)

