---
title: Способа - ActiveX Data Objects (ADO)
TOCTitle: Seek Method (ADO)
ms:assetid: cf0f133b-31f2-a2df-6cf3-1b5fa73b516c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250027(v=office.15)
ms:contentKeyID: 48547802
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fb6a5a72474b8d19efe1dd155950fa9e3ecd8714
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889520"
---
# <a name="seek-method-ado"></a>Способ (ADO)


**Применимо к**: Access 2013, Office 2013



Выполняет поиск индекса [набора записей](recordset-object-ado.md) для быстрого поиска строку, в которой совпадает с указанными значениями и изменяет текущее положение строки на эту строку.

## <a name="syntax"></a>Синтаксис

*набор записей*. Поиск*KeyValues*, *SeekOption*

## <a name="parameters"></a>Параметры

  - *KeyValues*

  - Массив значений **Variant** . Индекс состоит из одного или нескольких столбцов и массив содержит значение, которое будет сравниваться с все соответствующие столбцы.

  - *SeekOption*

  - [SeekEnum](seekenum.md) значение, задающее тип сравнения между столбцов индекса и соответствующие *KeyValues*.

## <a name="remarks"></a>Замечания

Используйте метод **Seek** в сочетании со свойством [индекса](index-property-ado.md) , если базовый поставщик поддерживает индексы в объекте **набора записей** . Используйте метод [поддерживает](supports-method-ado.md)**(adSeek)** , чтобы определить, поддерживает ли основного поставщика **поиска**и метод **Supports(adIndex)** , чтобы определить, поддерживает ли поставщик индексов. (Например, [Поставщик OLE DB для Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md) поддерживает **поиска** и **индекса**).

Если **Поиск** не удается найти нужную строку, ошибка не происходит и размещенный строку в конец **набора записей**. Значение свойства **Index** желаемую индекса перед выполнением этого метода.

Этот метод поддерживается только записей на стороне сервера. Поиск не поддерживается, если значение свойства [CursorLocation](cursorlocation-property-ado.md) объекта **набора записей** является **adUseClient**.

Этот метод можно использовать, только когда со значением [CommandTypeEnum](commandtypeenum.md) **adCmdTableDirect**был открыт в объект **набора записей** .

