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
- функция Excel12v [excel 2007], функция Excel4v [Excel 2007]
localization_priority: Normal
ms.assetid: e3e96b98-c5a7-4625-95b6-a1e2d09c6d3d
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 7ffa0bc3ae6222af1ecd7f65de66d026ea178c87
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807259"
---
# <a name="excel4vexcel12v"></a>Excel4v/Excel12v

 **Относится к**: Excel 2013 | Office 2013 | Visual Studio 
  
Вызывает внутренней функции Microsoft Excel, функцию листа макросов или команды, или только для XLL специальные функции или команды, из в DLL-Библиотеку, XLL или ресурс кода.
  
Все последние версии Excel поддерживают **Excel4v**. Начиная с версии Excel 2007, **Excel12v** поддерживается. 
  
Эти функции могут вызываться только в том случае, когда Excel истекло управления DLL или XLL. Они также могут вызываться, когда Excel истекло управления косвенно через вызов Visual Basic для приложений (VBA). Они не могут вызывать в любое время. Например они не может вызываться при выполнении вызова функции DllMain или в других случаях, когда операционная система называется библиотеки DLL или из потока, созданные в библиотеку DLL. 
  
Функции [Excel4 и Excel12](excel4-excel12.md) примите их аргументах как список переменной длины в стеке, тогда как функции **Excel4v** и **Excel12v** примите их аргументах как массив. Во всех других отношениях **Excel4** происходит так же, как **Excel4v**и **Excel12** происходит так же, как **Excel12v**.
  
```cs
int _cdecl Excel4v(int iFunction, LPXLOPER pxRes, int iCount, LPXLOPER rgx[]);
int _cdecl Excel12v(int iFunction, LPXLOPER12 pxRes, int iCount, LPXLOPER12 rgx[]);
```

## <a name="parameters"></a>Параметры

 _iFunction_ (**int**)
  
Число, указывающее команды, функции или специальные функции, которому нужно позвонить. Список значений допустимый _iFunction_ в следующем разделе Примечания. 
  
 _pxRes_ (**LPXLOPER** или **LPXLOPER12**)
  
Указатель на **XLOPER** (в случае **Excel4v**) или **XLOPER12** (в случае **Excel12v**), который будет содержать результат вычисления функции.
  
 _iCount_ (**int**)
  
Число последующих аргументов, передаваемых в функцию. В версиях Excel 2003 до это может быть любое число от 0 до 30. Начиная с версии Excel 2007, это может быть любое число от 0 до 255.
  
 _rgx_ (**LPXLOPER []** или **[LPXLOPER12]**)
  
Массив, содержащий аргументы для функции. Все аргументы в массиве должны быть указатели на **XLOPER** или **XLOPER12** значения. 
  
## <a name="return-value"></a>������������ ��������

Эти функции возвращают те же значения, как **Excel4** и **Excel12**.
  
## <a name="remarks"></a>Замечания

Эти функции полезны, где число аргументов, передаваемых в оператор — это переменная. Например **Excel4v** и **Excel12v** полезны при регистрации функции с помощью [xlfRegister](xlfregister-form-1.md) , где число аргументов, общее зависит от числа аргументов, занимаемых функцию регистрации. **Excel4v** и **Excel12v** также используются при записи функции программы-оболочки для **Excel4** или **Excel12**. В таких случаях необходимо преобразовать список аргументов переменных, как бы обычно **Excel4** или **Excel12**, чтобы указать аргумент один массив переменного размера для обратного вызова Excel с помощью **Excel4v** или **Excel12v**.
  
### <a name="example"></a>Пример

Примеры кода просмотрите код для функции **Excel** и **Excel12f** в Excel 2010 XLL SDK, в следующем расположении, где установлен пакет SDK: 
  
Samples\Framewrk\Framewrk.c
  
## <a name="see-also"></a>См. также



[Excel4/Excel12](excel4-excel12.md)

