---
title: Метод - Read ActiveX Data Objects (ADO)
TOCTitle: Read method (ADO)
ms:assetid: 91c3ad34-f891-5be0-1fc1-c5c8a2ff07a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249641(v=office.15)
ms:contentKeyID: 48546357
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2bcee0de272a14825f978abb1f6dd2834a998f86
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949336"
---
# <a name="read-method-ado"></a>Метод Read (ADO)

**Применимо к**: Access 2013, Office 2013

Считывает указанное число байтов из двоичного объекта [потока](stream-object-ado.md) .

## <a name="syntax"></a>Синтаксис

*Variant* = *потока*. Чтение (*NumBytes* )

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*NumBytes* |Необязательно указывать. Значение типа **Long** , указывающее число байтов для чтения из файла или значение [StreamReadEnum](streamreadenum.md) **adReadAll**, который используется по умолчанию.|

## <a name="return-value"></a>Возвращаемое значение

Метод **Read** считывает указанное число байтов или потока всей из объекта **потока** и возвращает результирующую данных как **Variant**.

## <a name="remarks"></a>Примечания

Если *NumBytes* больше, чем количество байтов, оставшихся в **потоке**, возвращаются только остаток байтов. Данные, прочитанные не дополняется в соответствии с *NumBytes*заданной длины. Если нет байт для чтения, возвращается значение variant нулевое значение. **Чтение** не может использоваться для чтения в обратном направлении.

> [!NOTE]
> *NumBytes* всегда меры в байтах. Для текста **поток** объектов ([Тип](type-property-ado-stream.md) — **adTypeText**), используйте [ReadText](readtext-method-ado.md).


