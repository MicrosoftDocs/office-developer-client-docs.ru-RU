---
title: Метод Write — объекты данных ActiveX (ADO)
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

Записывает двоичные данные в объект [Stream](stream-object-ado.md) .

## <a name="syntax"></a>Синтаксис

*Stream*. *Буфер* записи

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*Буферизовать* |**Переменная типа Variant** , содержащая массив байтов для записи.|

## <a name="remarks"></a>Примечания

Указанные байты записываются в объект **Stream** без промежуточных пробелов между ними.

Текущая [позиция](position-property-ado.md) равна байту после записанных данных. Метод **Write** не усекает остальные данные в потоке. Если вы хотите усечь эти байты, вызовите [SetEOS](seteos-method-ado.md).

Если вы пишете за пределами текущей позиции [Size](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream) [EOS](eos-property-ado.md) , размер **потока** увеличится до того, как будут содержаться новые байты, а **EOS** перейдет к новому последнему байту в **потоке**.

> [!NOTE]
> Метод **Write** используется с двоичными потоками ([Type](type-property-ado-stream.md) — **адтипебинари**). Для текстовых потоков (**Type** — **Адтипетекст**) используйте [WriteText](writetext-method-ado.md).

