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
  
Вызывает функцию, определяемую пользователем, в высокой производительности вычислительной среды.
  
```cpp
int CallUDF(int SessionId, WCHAR *XllName, WCHAR *UDFName, LPXLOPER12 pxAsyncHandle, int (*CallBackAddr)(), int ArgCount, LPXLOPER12 Parameter1, ...)
```

## <a name="parameters"></a>Parameters

_SessionId_
  
> ID сеанса, в котором необходимо сделать вызов.
    
_XLLName_
  
> Имя XLL, которое содержит функцию, определяемую пользователем.
    
_UDFName_
  
> Имя функции, определяемой пользователем.
    
_CallBackAddr_
  
> Функция, которую соединитатель должен вызывать после завершения функции, определенной пользователем.
    
_pxAsyncHandle_
  
> Асинхронная ручка, используемая Excel и соединитетелем для отслеживания ожидающих вызовов функций, определенных пользователем. Соединиттель использует его позже, когда вызов будет завершен, когда он возвращается в Excel с помощью указателя функции, переданного в _аргументе CallBackAddr._ 
    
_ArgCount_
  
> Количество аргументов, которые необходимо передать в функцию, определяемую пользователем. Максимальное допустимые значения — 255.
    
_Parameter1_
  
> Значение, передав его в функцию, определяемую пользователем. Повторите этот аргумент для каждого параметра, показанного  _ArgCount_.
    
## <a name="return-value"></a>Возвращаемое значение

**xlHpcRetSuccess,** если вызов UDF успешно инициировался; **xlHpcRetInvalidSessionId,** если аргумент _SessionId_ недействителен; **xlHpcRetCallFailed на** других сбоях, включая время. Если вызов возвращает код ошибки (все, кроме **xlHpcRetSuccess),** Excel считает вызов UDF недействительным, недействителен _pxAsyncHandle_ и не ожидает обратного вызова.
  
## <a name="remarks"></a>Примечания

Эта функция выполняется асинхронно.
  
## <a name="see-also"></a>См. также

- [Функции для работы с соединителями кластеров Excel](excel-cluster-connector-functions.md)

