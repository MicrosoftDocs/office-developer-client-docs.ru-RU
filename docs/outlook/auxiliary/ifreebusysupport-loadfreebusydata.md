---
title: IFreeBusySupportLoadFreeBusyData
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f0baa310-7a53-07ee-0a7d-33dd1fb465c2
description: Возвращает для каждого указанного пользователя интерфейс для enumerating free/busy blocks of data within a time range.
ms.openlocfilehash: e55f902117a20bfefaa5d9a2f3a067cb78ec86cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411234"
---
# <a name="ifreebusysupportloadfreebusydata"></a>IFreeBusySupport::LoadFreeBusyData

Возвращает для каждого указанного пользователя интерфейс для enumerating free/busy blocks of data within a time range. 
  
## <a name="quick-info"></a>Краткие сведения

См. [IFreeBusySupport.](ifreebusysupport.md)
  
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

_cMax_
  
> [in] Количество [возвращаемого интерфейса IFreeBusyData.](ifreebusydata.md) 
    
_rgfbuser_
  
> [in] Массив пользователей со сведениями о занятости, для получения данных.
    
_prgfbdata_
  
> [in] [out] Массив интерфейсов **IFreeBusyData,** соответствующий _массиву rgfbuser_ структур [FBUser.](fbuser.md) 
    
   > [!NOTE]
   > Этот массив указателей выделяется вызываемой и освобожден вызываемой. Фактические интерфейсы, на которые указывает вызываемая, отпущены, когда вызываемая из них делает это. 
  
_phrStatus_
  
> [out] Массив результатов **HRESULT** для каждого соответствующего интерфейса **IFreeBusyData.** Значением может быть NULL. Результат будет иметь S_OK, если соответствующие  _prgfbdata_ допустимы. 
    
_pcRead_
  
>  [out] Фактическое количество пользователей, для которых найден интерфейс **IFreeBusyData.** 
    
## <a name="return-values"></a>Возвращаемые значения

S_OK if the call succeeded; otherwise, an error code.
  
## <a name="see-also"></a>См. также

- [Constants (Free/busy API)](constants-free-busy-api.md)

