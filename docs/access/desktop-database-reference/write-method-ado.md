---
title: Создание метода - ActiveX Data Objects (ADO)
TOCTitle: Write Method (ADO)
ms:assetid: cabe4581-409f-7f05-bd59-d495bfb2c6fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249986(v=office.15)
ms:contentKeyID: 48547697
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 98af810c9a24d38a6b2b32db31f9a650c2d6f70a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482525"
---
# <a name="write-method-ado"></a>Write Method (ADO)


**Применимо к**: Access 2013 | Office 2013


Записывает двоичные данные в объект [потока](stream-object-ado.md) .

## <a name="syntax"></a>Синтаксис

*Поток*. Запись*буфера*

## <a name="parameters"></a>Параметры

  - *Буфера*

  - **Variant** , содержащее массив байтов для записи.

## <a name="remarks"></a>Замечания

Объект **потока** без пробелов промежуточных между каждый байт записывается указанный байт.

Текущей [позиции](position-property-ado.md) задано значение байт следующие записываемые данные. Метод **Write** не усекать остальную часть данных в поток. Если вы хотите усечение этих байт, вызовите [SetEOS](seteos-method-ado.md).

Если записать за текущую позицию [EOS](eos-property-ado.md) будет увеличить [размер](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) **потока** , содержать любые новые байт и **EOS** будут перемещаться до нового получения последнего байта в **поток**.


> [!NOTE]
> <P>Метод <STRONG>Write</STRONG> используется с двоичных потоков (<A href="type-property-ado-stream.md">Тип</A> — <STRONG>adTypeBinary</STRONG>). Для текста потоков (<STRONG>Тип</STRONG> — <STRONG>adTypeText</STRONG>) используйте <A href="writetext-method-ado.md">WriteText</A>.</P>


