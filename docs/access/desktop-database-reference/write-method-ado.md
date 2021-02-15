---
title: Метод Write — ActiveX Data Objects (ADO)
TOCTitle: Write method (ADO)
ms:assetid: cabe4581-409f-7f05-bd59-d495bfb2c6fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249986(v=office.15)
ms:contentKeyID: 48547697
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c6f4bba55ec3a32d206d3a7bfd001e96cd94923e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302466"
---
# <a name="write-method-ado"></a>Метод Write (ADO)

**Область применения**: Access 2013, Office 2013

Записывает двоичные данные в [объект Stream.](stream-object-ado.md)

## <a name="syntax"></a>Синтаксис

*Stream*. Буфер *записи*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*Буфер* |**Вариант,** содержащий массив данных, которые необходимо написать.|

## <a name="remarks"></a>Заметки

Указанные bytes are written to the **Stream** object without any intervening spaces between each byte.

Текущее [положение](position-property-ado.md) устанавливается в соответствии с письменными данными в соответствии с данными. Метод **Write** не усечен остальных данных в потоке. Если вы хотите усечение этих данных, вызовите [SetEOS.](seteos-method-ado.md)

Если вы напишете после текущей [](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream) позиции  [EOS,](eos-property-ado.md) размер потока будет увеличен, чтобы содержать любые новые bytes, и **EOS** перейдет к новому последнему byte в **Stream**.

> [!NOTE]
> Метод **Write** используется с двоичными потоками [(тип](type-property-ado-stream.md) **adTypeBinary).** Для текстовых потоков **(тип** **adTypeText),** используйте [WriteText](writetext-method-ado.md).

