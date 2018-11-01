---
title: Метод - Read ActiveX Data Objects (ADO)
TOCTitle: Read Method (ADO)
ms:assetid: 91c3ad34-f891-5be0-1fc1-c5c8a2ff07a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249641(v=office.15)
ms:contentKeyID: 48546357
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b47b557fcb3e3c9ed26af29ce910c95262e4fe13
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884949"
---
# <a name="read-method-ado"></a>Метод Read (ADO)


**Применимо к**: Access 2013, Office 2013

Считывает указанное число байтов из двоичного объекта [потока](stream-object-ado.md) .

## <a name="syntax"></a>Синтаксис

*Variant* = *потока*. Чтение (*NumBytes* )

## <a name="parameters"></a>Параметры

  - *NumBytes*

  - Необязательный параметр. Значение типа **Long** , указывающее число байтов для чтения из файла или значение [StreamReadEnum](streamreadenum.md) **adReadAll**, который используется по умолчанию.

## <a name="return-value"></a>Возвращаемое значение

Метод **Read** считывает указанное число байтов или потока всей из объекта **потока** и возвращает результирующую данных как **Variant**.

## <a name="remarks"></a>Замечания

Если *NumBytes* больше, чем количество байтов, оставшихся в **потоке**, возвращаются только остаток байтов. Данные, прочитанные не дополняется в соответствии с *NumBytes*заданной длины. Если нет байт для чтения, возвращается значение variant нулевое значение. **Чтение** не может использоваться для чтения в обратном направлении.


> [!NOTE]
> <P><EM>NumBytes</EM> всегда меры в байтах. Для текста <STRONG>поток</STRONG> объектов (<A href="type-property-ado-stream.md">Тип</A> — <STRONG>adTypeText</STRONG>), используйте <A href="readtext-method-ado.md">ReadText</A>.</P>


