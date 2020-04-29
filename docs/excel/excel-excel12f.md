---
title: Excel/Excel12f
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Excel12f
keywords:
- функция Excel [Excel 2007], функция Excel12f [Excel 2007]
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
  
Функции библиотеки Framework. **Excel** — это оболочка для функции [Excel4](excel4-excel12.md) . **Excel12f** — это оболочка для функции [Excel12](excel4-excel12.md) . Каждый из них проверяет, не имеет ли ни одного из аргументов нулевого значения, что свидетельствует о том, что не удалось создать временную **XLOPER** или **XLOPER12** . При возникновении ошибки каждая печатает сообщение отладки. По завершении каждая освобождает всю временную память, которая могла быть создана **для временных и** **XLOPER12**s.
  
 **Excel12f** можно вызывать только из библиотеки DLL, начиная с библиотеки Excel 2007 C API C. Кроме того, она работает только при запуске с Excel 2007 и завершается с помощью **кслретфаилед** в противном случае. 
  
```cs
int Excel(int iFunction, LPXLOPER pxRes, int iCount, 
LPXLOPER argument1, ...);
int Excel12f(int iFunction, LPXLOPER12 pxRes, int iCount, 
LPXLOPER12 argument1, ...);
```

## <a name="parameters"></a>Параметры

 _ифунктион_ (**int**)
  
Число, обозначающее команду или функцию, которую необходимо вызвать. Дополнительные сведения см. в статье [Excel4/Excel12](excel4-excel12.md).
  
 _пксрес_
  
Указатель на результат вычисления функции. Все модули памяти, на которые указывает результат, будут выделены приложением Excel и должны быть освобождены в вызове [кслфри](xlfree.md) , когда он больше не нужен, или путем установки **кслбиткслфри** при его возврате в Excel. 
  
 _икаунт_ (**int**)
  
Число аргументов, которые будут переданы в функцию. Начиная с Excel 2007, предельное число аргументов равно 255. В более ранних версиях лимит равен 30.
  
 _argument1, ..._
  
Необязательные аргументы функции. Все аргументы должны быть указателями в **XLOPER**s в случае **Excel**или **XLOPER12**s в случае **Excel12f**.
  
## <a name="return-value"></a>Возвращаемое значение

Обе функции возвращают одни и те же коды ошибок и успешности, что и в **Excel4**, **Excel4v**, **Excel12**и **Excel12v**. Полное описание этих кодов приведено в статье [Excel4/Excel12](excel4-excel12.md) . Кроме того, эти функции платформы возвращают **кслретфаилед** без вызова API C, если обнаружен указатель NULL на параметр. 
  
## <a name="example"></a>Пример

В этом примере в функцию **Excel12f** передается неверный аргумент, который отправляет сообщение отладчику. 
  
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

