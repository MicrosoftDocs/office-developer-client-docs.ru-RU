---
title: Создание метода - ActiveX Data Objects (ADO)
TOCTitle: Write Method (ADO)
ms:assetid: cabe4581-409f-7f05-bd59-d495bfb2c6fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249986(v=office.15)
ms:contentKeyID: 48547697
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5987b16c033b13be145e60317cdfdc821851be38
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867414"
---
# <a name="write-method-ado"></a>Создание метода (ADO)


**Применимо к**: Access 2013, Office 2013


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


