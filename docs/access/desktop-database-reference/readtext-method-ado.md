---
title: ReadText Method (ADO)
TOCTitle: ReadText Method (ADO)
ms:assetid: 08f5bac4-dccd-696c-09a7-e1ba0cb38d79
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248826(v=office.15)
ms:contentKeyID: 48543108
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5083dccd2c1d328e825a198008fd773bc3a592f6
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25605214"
---
# <a name="readtext-method-ado"></a>ReadText Method (ADO)


**Применимо к**: Access 2013 | Office 2013

Число операций чтения указанное число символов из объекта [потока](stream-object-ado.md) текста.

## <a name="syntax"></a>Синтаксис

*Строка* = *потока*. ReadText (*NumChars*)

## <a name="parameters"></a>Параметры

  - *NumChars*

  - Необязательный параметр. **Длинное целое** значение, задающее число символов для чтения из файла, или значение [StreamReadEnum](streamreadenum.md) . Значение по умолчанию — **adReadAll**.

<<<<<<< HEAD
## <a name="return-value"></a>Возвращаемое значение
=======
## <a name="return-value"></a>Возвращаемое значение
>>>>>>> master

Метод **ReadText** считывает указанное число символов, строку целиком или всей потока из объекта **потока** и возвращает результирующую строку.

## <a name="remarks"></a>Замечания

Если *NumChar* больше, чем количество символов в потоке, возвращаются только оставшиеся символы. Чтение строки не дополняется в соответствии с *NumChar*заданной длины. Если не используются никакие символы для чтения, возвращается значение типа variant, значение которого равно null. **ReadText** не может использоваться для чтения в обратном направлении.


> [!NOTE]
> <P>Метод <STRONG>ReadText</STRONG> используется с потоками текст (<A href="type-property-ado-stream.md">Тип</A> — <STRONG>adTypeText</STRONG>). Для двоичного файла потоков (<STRONG>Тип</STRONG> — <STRONG>adTypeBinary</STRONG>), используйте <A href="read-method-ado.md">чтения</A>.</P>


