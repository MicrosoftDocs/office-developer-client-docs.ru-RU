---
title: RebaseTaskProgress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8b8368d2-b04b-42a5-fdc3-955fc873c2f5
description: Отчеты о ходе переомирия и повторного выполнения встреч.
ms.openlocfilehash: e5df0cd6df10ab86b1a125b9807637438976726f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326455"
---
# <a name="rebasetaskprogress"></a>RebaseTaskProgress

Отчеты о ходе переомирия и повторного выполнения встреч.
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Файл заголовка:  <br/> |tzmovelib.h  <br/> |
|Реализовано в:  <br/> |Клиентские приложения MAPI  <br/> |
|Вызывающая сторона:  <br/> |Outlook повторного повторного  <br/> |
|Тип указателя:  <br/> |**PFNREBASETASKPROGRESS,** как определено в tzmovelib.h  <br/> |
   
```cpp
void STDAPICALLTYPE RebaseTaskProgress(  
    ULONG ulMin, 
    ULONG ulMax, 
    ULONG ulCur, 
    REBASE_APPT_STATE State, 
    const SRow* pRowCur); 

```

## <a name="parameters"></a>Parameters

_ulMin_
  
> [in] Низкий конец диапазона обрабатываемых назначений. Обычно это ноль.
    
_ulMax_
  
> [in] Высокий конец диапазона обрабатываемых назначений. Обычно это число элементов в обрабатываемой папке календаря.
    
_ulCur_
  
> [in] Текущий обрабатываемый элемент.
    
_Состояние_
  
> [in] Значение, которое указывает состояние обрабатываемого элемента. Код REBASE_APPT_STATE **определяется** в tzmovelib.h.  _State_  одно из следующих значений: 
    
   - **REBASE_APPT_STATE_SCANNING_EXAMINING** — сканирование и изучение элемента. 
    
   - **REBASE_APPT_STATE_SCANNING_FOUND** — сканирование и найти элемент. 
    
   - **REBASE_APPT_STATE_BEGIN** — исправление и запуск элемента. 
    
   - **REBASE_APPT_STATE_REBASING** — исправление и настройка элемента. 
    
   - **REBASE_APPT_STATE_SENDING** — исправление и отправка обновления собрания. 
    
   - **REBASE_APPT_STATE_DONE** — исправление и исправление элемента. 
    
_pRowCur_
  
> [in] Указатель на структуру **[SRow,](https://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** которая описывает отсканированный или исправленный элемент. 
    
## <a name="return-values"></a>Возвращаемые значения

S_OK if the call succeeded; otherwise, an error code.
  
## <a name="remarks"></a>Примечания

Клиентские приложения MAPI, которые используют [интерфейс IOlkApptRebaser,](iolkapptrebaser.md) реализуют эту функцию для отслеживания обработки элементов. 
  
## <a name="see-also"></a>См. также

- [About rebasing calendars programmatically for Daylight Saving Time](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

