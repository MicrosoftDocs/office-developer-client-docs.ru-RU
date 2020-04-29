---
title: RebaseTaskComplete
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 2de5c77c-3fac-cfb6-3719-68df4013cf11
description: Создает отчет о завершении для ребазового использования встреч.
ms.openlocfilehash: 9fab0d06bf0b9856b9a968f5c0db1bb15b0fe0bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328324"
---
# <a name="rebasetaskcomplete"></a>RebaseTaskComplete

Создает отчет о завершении для ребазового использования встреч.
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Файл заголовка:  <br/> |тзмовелиб. h  <br/> |
|Реализовано в:  <br/> |Клиентские приложения MAPI  <br/> |
|Вызывающая сторона:  <br/> |Объект перебазового объекта Outlook  <br/> |
|Тип указателя:  <br/> |**Пфнребасетасккомплете** в соответствии с определением в тзмовелиб. h  <br/> |
   
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

_улровиндекс_
  
> возврата Строка, которая была обработана. Этот индекс ссылается на структуру **[SRowSet](https://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx)** , переданную в [Иолкапптребасер:: бегинребасеаппоинтментс](iolkapptrebaser-beginrebaseappointments.md).
    
_провкур_
  
> in] указатель на структуру **[сров](https://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** , описывающий обработанный элемент. 
    
_хрресулт_
  
> возврата **Значение HRESULT** , указывающее результат операции перезаписи. 
    
_фмодифиед_
  
> возврата Указывает, был ли изменен элемент.
    
_фсентупдате_
  
> возврата Указывает, было ли отправлено сообщение обновления собрания. 
    
_перрор_
  
> возврата Указатель на структуру **мапиеррор** с расширенными сведениями об ошибке. 
    
## <a name="return-values"></a>Возвращаемые значения

S_OK if the call succeeded; otherwise, an error code.
  
## <a name="remarks"></a>Примечания

Клиентские приложения MAPI, использующие интерфейс [иолкапптребасер](iolkapptrebaser.md) , реализуют эту функцию для отслеживания завершения обновления элемента. 
  
## <a name="see-also"></a>См. также

- [About rebasing calendars programmatically for Daylight Saving Time](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

