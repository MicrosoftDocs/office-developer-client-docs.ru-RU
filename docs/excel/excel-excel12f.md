---
title: Excel/Excel12f
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Excel12f
keywords:
- Функция Excel [Excel 2007], функция Excel12f [Excel 2007]
localization_priority: Normal
ms.assetid: 4e6a9ccc-988d-42a9-8874-01f2ee29b835
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f7ff6afac1737ee869e69fffd3dbed36a908b376
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431675"
---
# <a name="excelexcel12f"></a>Excel/Excel12f

 **Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Функции библиотеки Framework. **Excel** является оболочкой для [функции Excel4.](excel4-excel12.md) **Excel12f** — это оболочка для [функции Excel12.](excel4-excel12.md) Каждый проверяет, что ни один из аргументов не является нулевым, что указывает на сбой создания временного **XLOPER** или **XLOPER12.** В случае возникновения ошибки каждое сообщение отлаговка печатается. По завершению каждая из них освободит все временные памяти, которые могли быть созданы для временных **XLOPER** s и **XLOPER12** s.
  
 **Excel12f** можно назвать только из DLL, начиная с библиотеки API 2007 Excel C. Кроме того, он работает только при запуске Excel 2007 г. и не работает с **xlretFailed в** противном случае. 
  
```cs
int Excel(int iFunction, LPXLOPER pxRes, int iCount, 
LPXLOPER argument1, ...);
int Excel12f(int iFunction, LPXLOPER12 pxRes, int iCount, 
LPXLOPER12 argument1, ...);
```

## <a name="parameters"></a>Parameters

 _iFunction_ **(int)**
  
Номер с указанием команды или функции, которые необходимо вызвать. Дополнительные сведения см. в [excel4/Excel12](excel4-excel12.md).
  
 _pxRes_
  
Указатель на результат оцениваемой функции. Любая память, на которая указывается в результате, будет выделена Excel и должна быть освобождена при вызове [xlFree,](xlfree.md) когда она больше не потребуется, или путем установки **xlbitXLFree** при возвращении его в Excel. 
  
 _iCount_ **(int)**
  
Количество аргументов, которые будут переданы функции. Начиная с Excel 2007 г. ограничение составляет 255 аргументов. В предыдущих версиях ограничение составляет 30.
  
 _argument1, ..._
  
Необязательные аргументы для функции. Все аргументы должны быть указателями на **XLOPER** s в случае Excel **или XLOPER12** s в случае **Excel12f**. 
  
## <a name="return-value"></a>Возвращаемое значение

Обе функции возвращают те же коды ошибок и успехов, что **и Excel4,** **Excel4v,** **Excel12 и** **Excel12v.** Полное описание этих кодов см. в [excel4/Excel12.](excel4-excel12.md) Кроме того, эти функции Framework возвращают **xlretFailed** без вызова API C, если обнаружен указатель NULL на параметр. 
  
## <a name="example"></a>Пример

В этом примере плохой аргумент передается функции **Excel12f,** которая отправляет сообщение отладильщику. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI Excel12fExample(void)
{
    Excel12f(xlcDisplay, 0, 1, 0);
    return 1;
}
```

## <a name="see-also"></a>См. также



[Excel4/Excel12](excel4-excel12.md)


[Функции в библиотеке платформы](functions-in-the-framework-library.md)

