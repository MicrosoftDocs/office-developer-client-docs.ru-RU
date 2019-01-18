---
title: Способ - ActiveX Data Objects (ADO)
TOCTitle: Seek method (ADO)
ms:assetid: cf0f133b-31f2-a2df-6cf3-1b5fa73b516c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250027(v=office.15)
ms:contentKeyID: 48547802
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 321040a39b02f31f0265df6e91748df13c05032c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726304"
---
# <a name="seek-method-ado"></a>Метод Seek (ADO)

**Применимо к**: Access 2013, Office 2013

Выполняет поиск индекса [набора записей](recordset-object-ado.md) для быстрого поиска строку, в которой совпадает с указанными значениями и изменяет текущее положение строки на эту строку.

## <a name="syntax"></a>Синтаксис

*набор записей*. Поиск*KeyValues*, *SeekOption*

## <a name="parameters"></a>Parameters

|Параметр|Описание|
|:--------|:----------|
|*KeyValues* |Массив значений **Variant** . Индекс состоит из одного или нескольких столбцов и массив содержит значение, которое будет сравниваться с все соответствующие столбцы.|
|*SeekOption* |[SeekEnum](seekenum.md) значение, задающее тип сравнения между столбцов индекса и соответствующие *KeyValues*.|

## <a name="remarks"></a>Замечания

Используйте метод **Seek** в сочетании со свойством [индекса](index-property-ado.md) , если базовый поставщик поддерживает индексы в объекте **набора записей** . Используйте метод [поддерживает](supports-method-ado.md)**(adSeek)** , чтобы определить, поддерживает ли основного поставщика **поиска**и метод **Supports(adIndex)** , чтобы определить, поддерживает ли поставщик индексов. (Например, [Поставщик OLE DB для Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md) поддерживает **поиска** и **индекса**).

Если **Поиск** не удается найти нужную строку, ошибка не происходит и размещенный строку в конец **набора записей**. Значение свойства **Index** желаемую индекса перед выполнением этого метода.

Этот метод поддерживается только записей на стороне сервера. Поиск не поддерживается, если значение свойства [CursorLocation](cursorlocation-property-ado.md) объекта **набора записей** является **adUseClient**.

Этот метод можно использовать, только когда со значением [CommandTypeEnum](commandtypeenum.md) **adCmdTableDirect**был открыт в объект **набора записей** .

