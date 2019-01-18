---
title: Метод - Read ActiveX Data Objects (ADO)
TOCTitle: Read method (ADO)
ms:assetid: 91c3ad34-f891-5be0-1fc1-c5c8a2ff07a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249641(v=office.15)
ms:contentKeyID: 48546357
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7ce545b1a6b036cae9f92d7e1ab7ba7479e4e252
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710890"
---
# <a name="read-method-ado"></a>Метод Read (ADO)

**Применимо к**: Access 2013, Office 2013

Считывает указанное число байтов из двоичного объекта [потока](stream-object-ado.md) .

## <a name="syntax"></a>Синтаксис

*Variant* = *потока*. Чтение (*NumBytes* )

## <a name="parameters"></a>Parameters

|Параметр|Описание|
|:--------|:----------|
|*NumBytes* |Необязательно. Значение типа **Long** , указывающее число байтов для чтения из файла или значение [StreamReadEnum](streamreadenum.md) **adReadAll**, который используется по умолчанию.|

## <a name="return-value"></a>Возвращаемое значение

Метод **Read** считывает указанное число байтов или потока всей из объекта **потока** и возвращает результирующую данных как **Variant**.

## <a name="remarks"></a>Замечания

Если *NumBytes* больше, чем количество байтов, оставшихся в **потоке**, возвращаются только остаток байтов. Данные, прочитанные не дополняется в соответствии с *NumBytes*заданной длины. Если нет байт для чтения, возвращается значение variant нулевое значение. **Чтение** не может использоваться для чтения в обратном направлении.

> [!NOTE]
> *NumBytes* всегда меры в байтах. Для текста **поток** объектов ([Тип](type-property-ado-stream.md) — **adTypeText**), используйте [ReadText](readtext-method-ado.md).


