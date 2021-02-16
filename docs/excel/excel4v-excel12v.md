---
title: Excel4v/Excel12v
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Excel12v
- Excel4v
keywords:
- Функция excel12v [excel 2007],Excel4v function [Excel 2007]
localization_priority: Normal
ms.assetid: e3e96b98-c5a7-4625-95b6-a1e2d09c6d3d
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 11ab86a95dde2ad52840822b28ce4d74dd05d148
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414993"
---
# <a name="excel4vexcel12v"></a>Excel4v/Excel12v

 **Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Вызывает внутреннюю функцию листа Microsoft Excel, функцию или команду листа макроса или специальную функцию или команду только для XLL из DLL, XLL или ресурса кода.
  
Все последние версии Excel поддерживают **Excel4v.** Начиная с Excel 2007, **excel12v** поддерживается. 
  
Эти функции могут быть вызваны только в том случае, если Excel передает управление DLL или XLL. Их также можно вызывать, когда Excel неявно передает управление через вызов Visual Basic для приложений (VBA). Они не могут быть вызваны в любое другое время. Например, они не могут быть вызваны во время вызовов функции DllMain или в других случаях, когда операционная система вызывает DLL, или из потока, созданного DLL. 
  
Функции Excel4 и [Excel12](excel4-excel12.md) принимают свои аргументы в качестве списка переменной длины в стеке, тогда как функции **Excel4v** и **Excel12v** принимают их аргументы в качестве массива. Во всех остальных отношениях **Excel4** ведет себя так же, как **Excel4v,** и **Excel12** ведет себя так же, как **Excel12v**.
  
```cs
int _cdecl Excel4v(int iFunction, LPXLOPER pxRes, int iCount, LPXLOPER rgx[]);
int _cdecl Excel12v(int iFunction, LPXLOPER12 pxRes, int iCount, LPXLOPER12 rgx[]);
```

## <a name="parameters"></a>Параметры

 _iFunction_ (**int**)
  
Номер, который указывает на команду, функцию или специальную функцию, которую вы хотите вызвать. Список допустимого значения  _iFunction_ см. в следующем разделе "Примечаний". 
  
 _pxRes_ (**LPXLOPER** или **LPXLOPER12)**
  
Указатель на **XLOPER** (в случае **Excel4v)** или **XLOPER12** (в случае **Excel12v),** который будет удерживать результат оцениваемой функции.
  
 _iCount_ (**int)**
  
Число последующих аргументов, которые будут переданы функции. В версиях Excel до 2003 это может быть любое число от 0 до 30. Начиная с Excel 2007, это может быть любое число от 0 до 255.
  
 _rgx_ (**LPXLOPER []** или **LPXLOPER12 []**)
  
Массив, содержащий аргументы функции. Все аргументы в массиве должны быть указателями на значения **XLOPER** или **XLOPER12.** 
  
## <a name="return-value"></a>Возвращаемое значение

Эти функции возвращают те же значения, что **и Excel4** и **Excel12.**
  
## <a name="remarks"></a>Примечания

Эти функции полезны, если число аргументов, переданных оператору, является переменным. Например, **Excel4v** и **Excel12v** полезны при регистрации функций с помощью [xlfRegister,](xlfregister-form-1.md) где общее число аргументов зависит от количества аргументов, принятых зарегистрированной функцией. **Excel4v** и **Excel12v** также полезны при написании функции-оболочки для **Excel4** **или Excel12.** В таких случаях необходимо преобразовать список аргументов переменных, как обычно предоставляется **в Excel4** или **Excel12,** в один аргумент массива переменного размера для обратного вызова в Excel с помощью **Excel4v** или **Excel12v**.
  
### <a name="example"></a>Пример

Примеры кода см. в коде функций **Excel** и **Excel12f** в XLL-SDK Excel 2010 в следующем расположении, где установлен SDK: 
  
Samples\Framewrk\Framewrk.c
  
## <a name="see-also"></a>См. также



[Excel4/Excel12](excel4-excel12.md)

