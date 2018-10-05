---
title: RebaseTaskComplete
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 2de5c77c-3fac-cfb6-3719-68df4013cf11
description: Отчеты о выполнении для повторного размещения en встреч.
ms.openlocfilehash: 9fab0d06bf0b9856b9a968f5c0db1bb15b0fe0bd
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388919"
---
# <a name="rebasetaskcomplete"></a>RebaseTaskComplete

Отчеты о выполнении для повторного размещения en встреч.
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Файл заголовка:  <br/> |tzmovelib.h  <br/> |
|Реализовано в:  <br/> |Клиентские приложения MAPI  <br/> |
|Вызывающая сторона:  <br/> |Объект сдвига Outlook  <br/> |
|Тип указателя:  <br/> |**PFNREBASETASKCOMPLETE** , определенных в tzmovelib.h  <br/> |
   
```cpp
void STDAPICALLTYPE RebaseTaskComplete(  
    ULONG ulRowIndex, 
    const SRow* pRowCur, 
    HRESULT hrResult, 
    BOOL fModified, 
    BOOL fSentUpdate, 
    const MAPIERROR* pError); 

```

## <a name="parameters"></a>Параметры

_ulRowIndex_
  
> [in] Строку, в которой было обработано. В этом индекс относится к **[SRowSet](https://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx)** структуры, переданной в [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md).
    
_pRowCur_
  
> входной параметр] указатель на структуру **[SRow](https://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** , описывающий элемент, который был обработан. 
    
_hrResult_
  
> [in] Значение **HRESULT** , указывающее, результат операции сдвига. 
    
_fModified_
  
> [in] Указывает, будет ли изменения элемента.
    
_fSentUpdate_
  
> [in] Указывает, было отправлено ли сообщение об обновлении собрания. 
    
_pError_
  
> [in] Указатель на структуру **MAPIERROR** с расширенные сведения об ошибке. 
    
## <a name="return-values"></a>Возвращаемые значения

S_OK if the call succeeded; otherwise, an error code.
  
## <a name="remarks"></a>Remarks

Клиентские приложения MAPI, использующие интерфейс [IOlkApptRebaser](iolkapptrebaser.md) реализовать эту функцию, чтобы отслеживать выполнение обновления элементов. 
  
## <a name="see-also"></a>См. также

- [About rebasing calendars programmatically for Daylight Saving Time](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

