---
title: xlEventRegister
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b98637d4-02e3-4dbd-8be5-6b46d32980c6
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 869122954ffe3928dfea72b8fc9fb432b9979e42
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438766"
---
# <a name="xleventregister"></a>xlEventRegister

 **Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Используется для регистрации обработчика событий. Представлены в Excel 2010.
  
```vb
Excel12(xlEventRegister, LPXLOPER12 pxRes, 2, LPXLOPER12 pxProcedure, LPXLOPER12 pxEvent);
```

## <a name="parameters"></a>Параметры

 _пкспроцедуре_ (**кслтипестр**)
  
Имя функции обработчика событий в том виде, в котором оно отображается в коде DLL.
  
 _пксевент_ (**кслтипеинт**)
  
Событие, обрабатываемое функцией, указанной в параметре _пкспроцедуре_ . 
  
Начиная с Excel 2010, Excel поддерживает следующие события:
  
|**Event**|**Описание**|
|:-----|:-----|
|**кслевенткалкулатионендед** <br/> |Создается, когда Excel завершает вычисление. После этого события можно освобождать ресурсы, выделенные в ходе вычисления.  <br/> |
|**кслевенткалкулатионканцелед** <br/> |Создается, когда пользователь прерывает вычисление. XLL должен остановить все асинхронные действия. Событие Калкулатионендед вызывается сразу после этого события.  <br/> |
   
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

В случае успеха возвращает **значение true** (**кслтипебул**). В случае неудачной попытки возвращает **значение false**.
  
## <a name="see-also"></a>См. также



[Асинхронные пользовательские функции](asynchronous-user-defined-functions.md)

