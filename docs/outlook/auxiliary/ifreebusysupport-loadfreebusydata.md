---
title: IFreeBusySupportLoadFreeBusyData
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f0baa310-7a53-07ee-0a7d-33dd1fb465c2
description: Возвращает для каждого указанного пользователя интерфейс для записи бесплатных и загруженных блоков данных в диапазоне времени.
ms.openlocfilehash: e55f902117a20bfefaa5d9a2f3a067cb78ec86cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411234"
---
# <a name="ifreebusysupportloadfreebusydata"></a>IFreeBusySupport::LoadFreeBusyData

Возвращает для каждого указанного пользователя интерфейс для записи бесплатных и загруженных блоков данных в диапазоне времени. 
  
## <a name="quick-info"></a>Краткие сведения

См. [в программе IFreeBusySupport](ifreebusysupport.md).
  
```cpp
HRESULT LoadFreeBusyData( 
    ULONG cMax,  
    FBUser *rgfbuser, 
    IFreeBusyData **prgfbdata,  
    HRESULT *phrStatus, 
    ULONG *pcRead 
);
```

## <a name="parameters"></a>Parameters

_cMax_
  
> [in] Количество возвращаемого [интерфейса IFreeBusyData.](ifreebusydata.md) 
    
_rgfbuser_
  
> [in] Массив бесплатных и занятых пользователей для получения данных.
    
_prgfbdata_
  
> [in] [вышел] Массив интерфейсов **IFreeBusyData,** соответствующих массиву _rgfbuser_ структур [FBUser.](fbuser.md) 
    
   > [!NOTE]
   > Этот массив указателей выделяется вызываемой и освобожден вызываемой. Фактические интерфейсы, на которые указывается, выпускаются, когда вызываемая с ними работа. 
  
_phrStatus_
  
> [вышел] Массив результатов **HRESULT** для поиска каждого соответствующего **интерфейса IFreeBusyData.** Значение может быть NULL. Результат задан для S_OK, если  _соответствующая prgfbdata_ действительна. 
    
_pcRead_
  
>  [вышел] Фактическое число пользователей, для которых найден **интерфейс IFreeBusyData.** 
    
## <a name="return-values"></a>Возвращаемые значения

S_OK if the call succeeded; otherwise, an error code.
  
## <a name="see-also"></a>См. также

- [Константы (API free/busy)](constants-free-busy-api.md)

