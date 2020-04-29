---
title: RebaseTaskProgress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8b8368d2-b04b-42a5-fdc3-955fc873c2f5
description: Сообщает о ходе перечислений и перепланировании встреч.
ms.openlocfilehash: e5df0cd6df10ab86b1a125b9807637438976726f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326455"
---
# <a name="rebasetaskprogress"></a>RebaseTaskProgress

Сообщает о ходе перечислений и перепланировании встреч.
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Файл заголовка:  <br/> |тзмовелиб. h  <br/> |
|Реализовано в:  <br/> |Клиентские приложения MAPI  <br/> |
|Вызывающая сторона:  <br/> |Объект перебазового объекта Outlook  <br/> |
|Тип указателя:  <br/> |**Пфнребасетаскпрогресс** в соответствии с определением в тзмовелиб. h  <br/> |
   
```cpp
void STDAPICALLTYPE RebaseTaskProgress(  
    ULONG ulMin, 
    ULONG ulMax, 
    ULONG ulCur, 
    REBASE_APPT_STATE State, 
    const SRow* pRowCur); 

```

## <a name="parameters"></a>Параметры

_улмин_
  
> возврата Нижний конец диапазона обрабатываемых встреч. Обычно это ноль.
    
_улмакс_
  
> возврата Максимальный конец диапазона обрабатываемых встреч. Обычно это количество обрабатываемых элементов в папке календаря.
    
_улкур_
  
> возврата Обрабатываемый текущий элемент.
    
_State_
  
> возврата Значение, указывающее состояние обрабатываемого элемента. **REBASE_APPT_STATE** перечисления задается в тзмовелиб. h.  _State_  одно из следующих значений: 
    
   - **REBASE_APPT_STATE_SCANNING_EXAMINING** — сканирование и проверка элемента. 
    
   - **REBASE_APPT_STATE_SCANNING_FOUND** — сканирование и поиск элемента. 
    
   - **REBASE_APPT_STATE_BEGIN** — исправление и запуск элемента. 
    
   - **REBASE_APPT_STATE_REBASING** — исправление и корректировка элемента. 
    
   - **REBASE_APPT_STATE_SENDING** — исправление и отправка обновления собрания. 
    
   - **REBASE_APPT_STATE_DONE** — исправление и выполнение элемента. 
    
_провкур_
  
> возврата Указатель на структуру **[сров](https://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** , которая описывает проверяемый или фиксированный элемент. 
    
## <a name="return-values"></a>Возвращаемые значения

S_OK if the call succeeded; otherwise, an error code.
  
## <a name="remarks"></a>Примечания

Клиентские приложения MAPI, использующие интерфейс [иолкапптребасер](iolkapptrebaser.md) , реализуют эту функцию для отслеживания обработки элементов. 
  
## <a name="see-also"></a>См. также

- [About rebasing calendars programmatically for Daylight Saving Time](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

