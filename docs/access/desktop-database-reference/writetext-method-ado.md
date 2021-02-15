---
title: Метод WriteText (ADO)
TOCTitle: WriteText method (ADO)
ms:assetid: 1ca2d9d5-11f4-d088-6fc3-53240208bb09
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248963(v=office.15)
ms:contentKeyID: 48543574
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 92983163a909e72c3da142ebcf63b7e0723e96af
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308269"
---
# <a name="writetext-method-ado"></a>Метод WriteText (ADO)

**Область применения**: Access 2013, Office 2013

Записывает указанную текстовую строку в [объект Stream.](stream-object-ado.md)

## <a name="syntax"></a>Синтаксис

*Stream*. WriteText *Data*, *Options*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*Data* |**Строковое** значение, которое содержит текст в символах, которые необходимо написать.|
|*Options* |Необязательный параметр. Значение [StreamWriteEnum,](streamwriteenum.md) которое указывает, должен ли знак в конце указанной строки быть записан в знаке разметки строки.|

## <a name="remarks"></a>Заметки

Указанные строки пишутся в объект **Stream** без пробелов или символов между каждой строкой.

В текущем [положении](position-property-ado.md) замеется символ, следующий за письменными данными. Метод **WriteText** не усечен остальных данных в потоке. Если вы хотите усеть эти символы, вызовите [SetEOS.](seteos-method-ado.md)

Если вы напишите после текущей [](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream) позиции [EOS,](eos-property-ado.md) размер потока будет увеличен, чтобы содержать любые новые символы, и  **EOS** перейдет к новому последнему byte в **Stream.**

> [!NOTE]
> Метод **WriteText** используется с текстовыми потоками [(type](type-property-ado-stream.md) is **adTypeText).** Для двоичных потоков **(type** is **adTypeBinary),** используйте [write](write-method-ado.md).


