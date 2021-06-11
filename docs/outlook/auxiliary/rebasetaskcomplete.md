---
title: RebaseTaskComplete
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 2de5c77c-3fac-cfb6-3719-68df4013cf11
description: Отчеты о завершении повторного выполнения встреч.
ms.openlocfilehash: 9fab0d06bf0b9856b9a968f5c0db1bb15b0fe0bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328324"
---
# <a name="rebasetaskcomplete"></a>RebaseTaskComplete

Отчеты о завершении повторного выполнения встреч.
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Файл заголовка:  <br/> |tzmovelib.h  <br/> |
|Реализовано в:  <br/> |Клиентские приложения MAPI  <br/> |
|Вызывающая сторона:  <br/> |Outlook повторного повторного  <br/> |
|Тип указателя:  <br/> |**PFNREBASETASKCOMPLETE,** как определено в tzmovelib.h  <br/> |
   
```cpp
void STDAPICALLTYPE RebaseTaskComplete(  
    ULONG ulRowIndex, 
    const SRow* pRowCur, 
    HRESULT hrResult, 
    BOOL fModified, 
    BOOL fSentUpdate, 
    const MAPIERROR* pError); 

```

## <a name="parameters"></a>Parameters

_ulRowIndex_
  
> [in] Строка, которая была обработана. Этот индекс относится к **[структуре SRowSet,](https://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx)** переданной [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md).
    
_pRowCur_
  
> in] Указатель на структуру **[SRow,](https://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** описывающий обработанный элемент. 
    
_hrResult_
  
> [in] **HRESULT,** указывающее результат операции повторного повторного сбоя. 
    
_fModified_
  
> [in] Указывает, был ли элемент изменен.
    
_fSentUpdate_
  
> [in] Указывает, было ли отправлено сообщение об обновлении собрания. 
    
_pError_
  
> [in] Указатель на структуру **MAPIERROR** с расширенными сведениями об ошибках. 
    
## <a name="return-values"></a>Возвращаемые значения

S_OK if the call succeeded; otherwise, an error code.
  
## <a name="remarks"></a>Примечания

Клиентские приложения MAPI, которые используют [интерфейс IOlkApptRebaser,](iolkapptrebaser.md) реализуют эту функцию для отслеживания завершения обновлений элементов. 
  
## <a name="see-also"></a>См. также

- [About rebasing calendars programmatically for Daylight Saving Time](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

