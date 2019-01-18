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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726248"
---
# <a name="writetext-method-ado"></a>Метод WriteText (ADO)

**Применимо к**: Access 2013, Office 2013

Записывает строку, указанный текст в объект [потока](stream-object-ado.md) .

## <a name="syntax"></a>Синтаксис

*Поток*. WriteText*данных*, *Параметры*

## <a name="parameters"></a>Parameters

|Параметр|Описание|
|:--------|:----------|
|*Данные* |**Строковое** значение, содержащее текст в символов для записи.|
|*Варианты* |Необязательно. [StreamWriteEnum](streamwriteenum.md) значение, указывающее, является ли знака разделителя строки должны быть записаны в конце указанной строки.|

## <a name="remarks"></a>Замечания

Объект **потока** без промежуточных пробелов и знаков между каждую строку, записывается заданных строк.

Символ, следующий записываемые данные имеет значение текущей [позиции](position-property-ado.md) . Метод **WriteText** не усекать остальную часть данных в поток. Если вы хотите усекать эти символы, вызовите [SetEOS](seteos-method-ado.md).

Если записать за текущую позицию [EOS](eos-property-ado.md) будет увеличить [размер](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream) **потока** , содержит новые символы и **EOS** будут перемещаться до нового получения последнего байта в **поток**.

> [!NOTE]
> Метод **WriteText** используется с потоками текст ([Тип](type-property-ado-stream.md) — **adTypeText**). Для двоичного файла потоков (**Тип** — **adTypeBinary**), используйте [запись](write-method-ado.md).


