---
title: RebaseTaskProgress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8b8368d2-b04b-42a5-fdc3-955fc873c2f5
description: Отчеты о ходе выполнения для перечисления и повторного размещения en встреч.
ms.openlocfilehash: 4219ab1d59b596bebbe3ced03651716b04b51f81
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807962"
---
# <a name="rebasetaskprogress"></a>RebaseTaskProgress

Отчеты о ходе выполнения для перечисления и повторного размещения en встреч.
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Файл заголовка:  <br/> |tzmovelib.h  <br/> |
|Реализованный:  <br/> |Клиентские приложения MAPI  <br/> |
|Вызывается:  <br/> |Объект сдвига Outlook  <br/> |
|Тип указателя:  <br/> |**PFNREBASETASKPROGRESS** , определенных в tzmovelib.h  <br/> |
   
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
  
> [in] Низкая конец диапазона, обрабатываемых встреч. Обычно равно нулю.
    
_ulMax_
  
> [in] Высокая конец диапазона, обрабатываемых встреч. Обычно это количество элементов в папке календаря, обрабатываемых.
    
_ulCur_
  
> [in] Текущий элемент, обрабатываемых.
    
_Состояние_
  
> [in] Значение, указывающее состояние обрабатываемый элемент. Перечисление **REBASE_APPT_STATE** определен в tzmovelib.h.  _Состояние_ — это один из следующих значений: 
    
   - **REBASE_APPT_STATE_SCANNING_EXAMINING** — сканирования и проверки элемента. 
    
   - **REBASE_APPT_STATE_SCANNING_FOUND** — сканирование и найти элемент. 
    
   - **REBASE_APPT_STATE_BEGIN** — устранению и запуск элемента. 
    
   - **REBASE_APPT_STATE_REBASING** — устранению и изменяет значения элемента. 
    
   - **REBASE_APPT_STATE_SENDING** — устранению и отправка обновления собрания. 
    
   - **REBASE_APPT_STATE_DONE** — исправление и Готово с элементом. 
    
_pRowCur_
  
> [in] Указатель на структуру **[SRow](http://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** с описанием элемента выполняется поиск вирусов или фиксированной. 
    
## <a name="return-values"></a>Возвращаемые значения

S_OK if the call succeeded; otherwise, an error code.
  
## <a name="remarks"></a>Remarks

Клиентские приложения MAPI, использующие интерфейс [IOlkApptRebaser](iolkapptrebaser.md) реализовать эту функцию для отслеживания обработки элементов. 
  
## <a name="see-also"></a>См. также

- [About rebasing calendars programmatically for Daylight Saving Time](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

