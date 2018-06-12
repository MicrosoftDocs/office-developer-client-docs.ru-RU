---
title: xlEventRegister
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b98637d4-02e3-4dbd-8be5-6b46d32980c6
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: d837d87c479f70f0184a7cf1612dea5ab8c99e6d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807352"
---
# <a name="xleventregister"></a>xlEventRegister

 **Применимо к**: Excel 2013 | Office 2013 | Visual Studio 
  
Используется для регистрации обработчика событий. Появился в Excel 2010.
  
```vb
Excel12(xlEventRegister, LPXLOPER12 pxRes, 2, LPXLOPER12 pxProcedure, LPXLOPER12 pxEvent);
```

## <a name="parameters"></a>Parameters

 _pxProcedure_ (**xltypeStr**)
  
Имя функции обработчика событий как оно отображается в коде DLL.
  
 _pxEvent_ (**xltypeInt**)
  
Событие обрабатывается с помощью функции, указанный в параметре _pxProcedure_ . 
  
Начиная с версии Excel 2010, Excel поддерживает следующие события:
  
|**Событие**|**Описание**|
|:-----|:-----|
|**xleventCalculationEnded** <br/> |Возникает после завершения вычислений Excel. Можно освободить все ресурсы, выделенные при расчете после этого события.  <br/> |
|**xleventCalculationCanceled** <br/> |Возникает, когда пользователь прерывает вычисления. XLL необходимо остановить любые асинхронной операции. Событие CalculationEnded вызывается сразу после этого события.  <br/> |
   
## <a name="property-valuereturn-value"></a>Значение свойства или возвращаемое значение

В случае успешного выполнения возвращает **значение TRUE** (**xltypeBool**). В случае неудачи возвращает **значение FALSE**.
  
## <a name="see-also"></a>См. также



[Асинхронные пользовательские функции](asynchronous-user-defined-functions.md)

