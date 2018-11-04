---
title: Создание метода - ActiveX Data Objects (ADO)
TOCTitle: Write method (ADO)
ms:assetid: cabe4581-409f-7f05-bd59-d495bfb2c6fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249986(v=office.15)
ms:contentKeyID: 48547697
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 93336294380ffa207f47adbcad630be3fdd1a8b8
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25950218"
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

Если записать за текущую позицию [EOS](eos-property-ado.md) будет увеличить [размер](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) **потока** , содержать любые новые байт и **EOS** будут перемещаться до нового получения последнего байта в **поток**.

> [!NOTE]
> Метод **Write** используется с двоичных потоков ([Тип](type-property-ado-stream.md) — **adTypeBinary**). Для текста потоков (**Тип** — **adTypeText**) используйте [WriteText](writetext-method-ado.md).

