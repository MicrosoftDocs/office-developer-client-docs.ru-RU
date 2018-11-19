---
title: Создание метода - ActiveX Data Objects (ADO)
TOCTitle: Write method (ADO)
ms:assetid: cabe4581-409f-7f05-bd59-d495bfb2c6fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249986(v=office.15)
ms:contentKeyID: 48547697
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 227c7a3746d0c743c33f76362023d6d374269a81
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026283"
---
# <a name="write-method-ado"></a>Метод Write (ADO)

**Применимо к**: Access 2013, Office 2013

Записывает двоичные данные в объект [потока](stream-object-ado.md) .

## <a name="syntax"></a>Синтаксис

*Поток*. Запись*буфера*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*Буфера* |**Variant** , содержащее массив байтов для записи.|

## <a name="remarks"></a>Примечания

Объект **потока** без пробелов промежуточных между каждый байт записывается указанный байт.

Текущей [позиции](position-property-ado.md) задано значение байт следующие записываемые данные. Метод **Write** не усекать остальную часть данных в поток. Если вы хотите усечение этих байт, вызовите [SetEOS](seteos-method-ado.md).

Если записать за текущую позицию [EOS](eos-property-ado.md) будет увеличить [размер](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream) **потока** , содержать любые новые байт и **EOS** будут перемещаться до нового получения последнего байта в **поток**.

> [!NOTE]
> Метод **Write** используется с двоичных потоков ([Тип](type-property-ado-stream.md) — **adTypeBinary**). Для текста потоков (**Тип** — **adTypeText**) используйте [WriteText](writetext-method-ado.md).

