---
title: Excel/Excel12f
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Excel12f
keywords:
- функции Excel [excel 2007], функция Excel12f [Excel 2007]
localization_priority: Normal
ms.assetid: 4e6a9ccc-988d-42a9-8874-01f2ee29b835
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 56034984852713496465c3d1f79a9989fc47df1c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807186"
---
# <a name="excelexcel12f"></a>Excel/Excel12f

 **Относится к**: Excel 2013 | Office 2013 | Visual Studio 
  
Функции библиотеки Framework. **Excel** является оболочкой для функции [Excel4](excel4-excel12.md) . **Excel12f** является оболочкой для функции [Excel12](excel4-excel12.md) . Каждый проверяется, что ни один из аргументов равно нулю, что указывает, что не удалось создать временные **XLOPER** или **XLOPER12** . Если возникает ошибка, каждый печатает сообщение отладки. По завершении каждого освобождает все временные памяти, который мог быть создан для временного s **XLOPER**и **XLOPER12**.
  
 **Excel12f** могут вызываться только из DLL, начиная с Excel 2007 C API библиотеки. Кроме того его только работы при запуске, начиная с помощью Excel 2007 и в противном случае — ошибка в **xlretFailed** . 
  
```cs
int Excel(int iFunction, LPXLOPER pxRes, int iCount, 
LPXLOPER argument1, ...);
int Excel12f(int iFunction, LPXLOPER12 pxRes, int iCount, 
LPXLOPER12 argument1, ...);
```

## <a name="parameters"></a>Параметры

 _iFunction_ (**int**)
  
Число, указывающее команда или функция, которому нужно позвонить. Для получения дополнительных сведений см [Excel4/Excel12](excel4-excel12.md).
  
 _pxRes_
  
Указатель на результат вычисления функции. Память, на который указывает в результате будет выделено, Excel и нужно освободить в вызове [xlFree](xlfree.md) после больше не требуется, или задав **xlbitXLFree** Если возвращаясь в Excel. 
  
 _iCount_ (**int**)
  
Число аргументов, передаваемых в функцию. Начиная с версии Excel 2007, ограничение составляет 255 аргументов. В более ранних версиях ограничение: 30.
  
 _аргумент1..._
  
Необязательные аргументы для функции. Все аргументы должны быть указатели на **XLOPER**в случае **Excel**, или **XLOPER12**в случае **Excel12f**.
  
## <a name="return-value"></a>������������ ��������

Обе функции возвращают же об ошибках и коды при успешном выполнении как **Excel4**, **Excel4v**, **Excel12**и **Excel12v**. В разделе [Excel4/Excel12](excel4-excel12.md) полное описание этих кодов. Кроме того эти функции Framework возвращают обнаружил **xlretFailed** без вызова интерфейса API C, если указатель на параметр NULL. 
  
## <a name="example"></a>Пример

В этом примере функция **Excel12f** , которая отправляет сообщение в отладчике передает недопустимый аргумент. 
  
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

