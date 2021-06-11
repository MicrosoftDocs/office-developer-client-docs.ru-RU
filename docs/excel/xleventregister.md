---
title: xlEventRegister
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b98637d4-02e3-4dbd-8be5-6b46d32980c6
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 00c222efce6925c3f691eb2b799adf687c22082c
ms.sourcegitcommit: 41f2ee16badd6009bab642d68a61eaaccb91c3ec
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/17/2020
ms.locfileid: "45160281"
---
# <a name="xleventregister"></a>xlEventRegister

 **Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Используется для регистрации обработка событий. Представлен в Excel 2010 г.
  
```vb
Excel12(xlEventRegister, LPXLOPER12 pxRes, 2, LPXLOPER12 pxProcedure, LPXLOPER12 pxEvent);
```

## <a name="parameters"></a>Parameters

 _pxProcedure_ **(xltypeStr)**
  
Имя функции обработера событий в коде DLL.
  
 _pxEvent_ **(xltypeInt)**
  
Событие обрабатывается функцией, указанной в параметре _pxProcedure._ 
  
Начиная с Excel 2010 Excel поддерживает следующие события:
  
|**Event**|**Описание**|
|:-----|:-----|
|**xleventCalculationEnded** <br/> |Поднято после Excel выполнения вычисления. Вы можете освободить все ресурсы, выделенные во время вычисления после этого события.  <br/> |
|**xleventCalculationCanceled** <br/> |Повышается, когда пользователь прерывает вычисление. XLL должен остановить любые асинхронные действия. Событие CalculationEnded вызывается сразу после этого события.  <br/> |
   
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

В случае успешной работы **pxRes (xltypeInt)** имеет значение > 0. Если не удалось, pxRes ==0.
  
## <a name="see-also"></a>См. также



[Асинхронные пользовательские функции](asynchronous-user-defined-functions.md)

