---
title: Создание метода - ActiveX Data Objects (ADO)
TOCTitle: Write method (ADO)
ms:assetid: cabe4581-409f-7f05-bd59-d495bfb2c6fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249986(v=office.15)
ms:contentKeyID: 48547697
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c6f4bba55ec3a32d206d3a7bfd001e96cd94923e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702518"
---
# <a name="write-method-ado"></a>Метод Write (ADO)

**Применимо к**: Access 2013, Office 2013

Записывает двоичные данные в объект [потока](stream-object-ado.md) .

## <a name="syntax"></a>Синтаксис

*Поток*. Запись*буфера*

## <a name="parameters"></a>Parameters

|Параметр|Описание|
|:--------|:----------|
|*Буфера* |**Variant** , содержащее массив байтов для записи.|

## <a name="remarks"></a>Замечания

Объект **потока** без пробелов промежуточных между каждый байт записывается указанный байт.

Текущей [позиции](position-property-ado.md) задано значение байт следующие записываемые данные. Метод **Write** не усекать остальную часть данных в поток. Если вы хотите усечение этих байт, вызовите [SetEOS](seteos-method-ado.md).

Если записать за текущую позицию [EOS](eos-property-ado.md) будет увеличить [размер](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream) **потока** , содержать любые новые байт и **EOS** будут перемещаться до нового получения последнего байта в **поток**.

> [!NOTE]
> Метод **Write** используется с двоичных потоков ([Тип](type-property-ado-stream.md) — **adTypeBinary**). Для текста потоков (**Тип** — **adTypeText**) используйте [WriteText](writetext-method-ado.md).

