---
title: Метод записи — ActiveX объектов данных (ADO)
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
# <a name="write-method-ado"></a>Метод записи (ADO)

**Область применения**: Access 2013, Office 2013

Записывает двоичные данные на [объект Stream.](stream-object-ado.md)

## <a name="syntax"></a>Синтаксис

*Stream*. Write *Buffer*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*Буфер* |**Вариант,** содержащий массив написанных bytes.|

## <a name="remarks"></a>Примечания

Указанные bytes пишутся в объект **Stream** без каких-либо пересекающихся пробелов между каждым byte.

Текущая [позиция](position-property-ado.md) за набором byte после письменных данных. Метод **Write** не усечен остальных данных в потоке. Если вы хотите усечение этих bytes, позвоните [SetEOS](seteos-method-ado.md).

Если вы записывете текущую [](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream) позицию  [EOS,](eos-property-ado.md) размер потока будет увеличен, чтобы содержать все новые bytes, и **EOS** будет перейти к новой последней byte в **потоке**.

> [!NOTE]
> Метод **Write** используется с двоичными потоками [(Type](type-property-ado-stream.md) **is adTypeBinary).** Для текстовых потоков **(Тип** **adTypeText),** используйте [WriteText](writetext-method-ado.md).

