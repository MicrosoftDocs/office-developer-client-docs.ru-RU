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
- функция excel12v [Excel 2007], функция Excel4v [Excel 2007]
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
  
Вызывает внутреннюю Microsoft Excel лист, функцию или команду макроса или специальную функцию или команду только для XLL из ресурса DLL, XLL или кода.
  
Все последние версии Excel поддерживают **Excel4v.** Начиная с Excel 2007 года **поддерживается Excel12v.** 
  
Эти функции могут быть вызваны только Excel, когда управление передано DLL или XLL. Их также можно вызвать, Excel, которые косвенно передали управление с помощью вызова Visual Basic для приложений (VBA). Они не могут быть вызваны в любое другое время. Например, они не могут быть вызваны во время вызовов на функцию DllMain или в другое время, когда операционная система вызывает DLL, или из потока, созданного DLL. 
  
Функции Excel4 и [Excel12](excel4-excel12.md) принимают их аргументы в качестве списка переменной длины в стеке, в то время как функции **Excel4v** и **Excel12v** принимают их аргументы в качестве массива. Во всех остальных отношениях **Excel4** ведет себя так же, как **и Excel4v,** **а Excel12** ведет себя так же, как **и Excel12v.**
  
```cs
int _cdecl Excel4v(int iFunction, LPXLOPER pxRes, int iCount, LPXLOPER rgx[]);
int _cdecl Excel12v(int iFunction, LPXLOPER12 pxRes, int iCount, LPXLOPER12 rgx[]);
```

## <a name="parameters"></a>Parameters

 _iFunction_ **(int)**
  
Номер, который указывает команду, функцию или специальную функцию, которую необходимо вызвать. Список допустимого  _значения iFunction_ см. в следующем разделе Примечание. 
  
 _pxRes_ **(LPXLOPER** или **LPXLOPER12)**
  
Указатель на **XLOPER** (в случае **Excel4v)** или **XLOPER12** (в случае **Excel12v),** которые будут удерживать результат оцениваемой функции.
  
 _iCount_ **(int)**
  
Количество последующих аргументов, которые будут переданы функции. В версиях Excel до 2003 года это может быть любое число от 0 до 30. Начиная с Excel 2007 г. это может быть любое число от 0 до 255.
  
 _rgx_ **(LPXLOPER []** или **LPXLOPER12 []**)
  
Массив, содержащий аргументы для функции. Все аргументы в массиве должны быть указателями на **значения XLOPER** или **XLOPER12.** 
  
## <a name="return-value"></a>Возвращаемое значение

Эти функции возвращают те же значения, что **и Excel4** и **Excel12.**
  
## <a name="remarks"></a>Примечания

Эти функции полезны, если количество аргументов, переданных оператору, переменно. Например, **Excel4v** и **Excel12v** полезны при регистрации функций с помощью [xlfRegister,](xlfregister-form-1.md) где количество аргументов зависит от количества аргументов, принятых зарегистрированной функцией. **Excel4v** и **Excel12v** также полезны при записи функции оболочки **для Excel4** или **Excel12.** В этих случаях необходимо преобразовать список переменных аргументов, как это обычно предоставляется **в Excel4** или **Excel12,** в один аргумент массива переменного размера, чтобы вызвать обратно в Excel с помощью **Excel4v** или **Excel12v**.
  
### <a name="example"></a>Пример

В примерах кода см. код для **функций Excel** **и Excel12f** в Excel XLL SDK 2010 г., в следующем расположении, где установлен SDK: 
  
Samples\Framewrk\Framewrk.c
  
## <a name="see-also"></a>См. также



[Excel4/Excel12](excel4-excel12.md)

