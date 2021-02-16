---
title: CallUDF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6421c9a2-07f7-4deb-aa43-c50d82cb0002
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 096f57335572c3788fdf129dd3bcf4a76cf62b01
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433013"
---
# <a name="calludf"></a>CallUDF

**Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Вызов пользовательской функции в высокоскоростной вычислительной среде.
  
```cpp
int CallUDF(int SessionId, WCHAR *XllName, WCHAR *UDFName, LPXLOPER12 pxAsyncHandle, int (*CallBackAddr)(), int ArgCount, LPXLOPER12 Parameter1, ...)
```

## <a name="parameters"></a>Параметры

_SessionId_
  
> ИД сеанса, в котором необходимо сделать вызов.
    
_XLLName_
  
> Имя XLL,который содержит определяемую пользователем функцию.
    
_UDFName_
  
> Имя пользовательской функции.
    
_CallBackAddr_
  
> Функция, которая должна вызываться соединитетелем после завершения пользовательской функции.
    
_pxAsyncHandle_
  
> Асинхронный окне, используемый Excel и соединитетелем для отслеживания ожидающих вызовов пользовательских функций. Соединитель использует его позже после завершения вызова, когда он возвращается в Excel с помощью указателя функции, переданного в _аргументе CallBackAddr._ 
    
_ArgCount_
  
> Количество аргументов, которые необходимо передать в определяемую пользователем функцию. Максимально допустимые значения — 255.
    
_Parameter1_
  
> Значение, передав его в определяемую пользователем функцию. Повторите этот аргумент для каждого параметра, на который указывает _ArgCount._
    
## <a name="return-value"></a>Возвращаемое значение

**xlHpcRetSuccess,** если вызов UDF успешно инициирован; **xlHpcRetInvalidSessionId,** если аргумент  _SessionId_ является недопустимым; **xlHpcRetCallFailed** при других сбоях, включая время простоя. Если вызов возвращает какой-либо код ошибки (за исключением **xlHpcRetSuccess),** То Excel считает вызов UDF неудачным, аннулирует  _pxAsyncHandle_ и не ожидает обратного вызова.
  
## <a name="remarks"></a>Примечания

Эта функция выполняется асинхронно.
  
## <a name="see-also"></a>См. также

- [Функции для работы с соединителями кластеров Excel](excel-cluster-connector-functions.md)

