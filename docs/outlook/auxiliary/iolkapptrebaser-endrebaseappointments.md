---
title: IOlkApptRebaserEndRebaseAppointments
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e47d5a8d-6a13-f430-fbfd-00df04b4a006
description: Waits for appointment rebasing to complete and retrieves the results.
ms.openlocfilehash: a6e62cff9efea1fc7079d04bc9b032b5637f8847
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431003"
---
# <a name="iolkapptrebaserendrebaseappointments"></a>IOlkApptRebaser::EndRebaseAppointments

Waits for appointment rebasing to complete and retrieves the results.
  
## <a name="quick-info"></a>Краткие сведения

See [IOlkApptRebaser](iolkapptrebaser.md).
  
```cpp
HRESULT EndRebaseAppointments( 
    void *pContext, 
    HRESULT *phResult);
```

## <a name="parameters"></a>Parameters

_pContext_
  
> [in] Required. A pointer to the context obtained from a call to [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md).
    
_phResult_
  
> [out] Required. A pointer to an **HRESULT** to retrieve the result of the rebasing operation. 
    
## <a name="return-values"></a>Возвращаемые значения

S_OK if the call succeeded; otherwise, an error code.
  
## <a name="see-also"></a>См. также

- [About rebasing calendars programmatically for Daylight Saving Time](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

