---
title: Метод WriteText (ADO)
TOCTitle: WriteText method (ADO)
ms:assetid: 1ca2d9d5-11f4-d088-6fc3-53240208bb09
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248963(v=office.15)
ms:contentKeyID: 48543574
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5c0c4668141c0da6e5faddee009d2548f1ee2c53
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926999"
---
# <a name="writetext-method-ado"></a>Метод WriteText (ADO)


**Применимо к**: Access 2013, Office 2013

Записывает строку, указанный текст в объект [потока](stream-object-ado.md) .

## <a name="syntax"></a>Синтаксис

*Поток*. WriteText*данных*, *Параметры*

## <a name="parameters"></a>Параметры

  - *Данные*

  - **Строковое** значение, содержащее текст в символов для записи.

  - *Варианты*

  - Необязательно указывать. [StreamWriteEnum](streamwriteenum.md) значение, указывающее, является ли знака разделителя строки должны быть записаны в конце указанной строки.

## <a name="remarks"></a>Примечания

Объект **потока** без промежуточных пробелов и знаков между каждую строку, записывается заданных строк.

Символ, следующий записываемые данные имеет значение текущей [позиции](position-property-ado.md) . Метод **WriteText** не усекать остальную часть данных в поток. Если вы хотите усекать эти символы, вызовите [SetEOS](seteos-method-ado.md).

Если записать за текущую позицию [EOS](eos-property-ado.md) будет увеличить [размер](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) **потока** , содержит новые символы и **EOS** будут перемещаться до нового получения последнего байта в **поток**.


> [!NOTE]
> <P>Метод <STRONG>WriteText</STRONG> используется с потоками текст (<A href="type-property-ado-stream.md">Тип</A> — <STRONG>adTypeText</STRONG>). Для двоичного файла потоков (<STRONG>Тип</STRONG> — <STRONG>adTypeBinary</STRONG>), используйте <A href="write-method-ado.md">запись</A>.</P>


