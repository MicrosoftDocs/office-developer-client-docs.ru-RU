---
title: Метод Seek — ActiveX Data Objects (ADO)
TOCTitle: Seek method (ADO)
ms:assetid: cf0f133b-31f2-a2df-6cf3-1b5fa73b516c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250027(v=office.15)
ms:contentKeyID: 48547802
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 321040a39b02f31f0265df6e91748df13c05032c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308794"
---
# <a name="seek-method-ado"></a>Метод Seek (ADO)

**Область применения**: Access 2013, Office 2013

Выполняет поиск в индексе наборов [записей,](recordset-object-ado.md) чтобы быстро найти строку, которая соответствует указанным значениям, и изменяет текущую позицию строки на эту строку.

## <a name="syntax"></a>Синтаксис

*recordset*. Seek *KeyValues*, *SeekOption*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*KeyValues* |Массив значений **Variant.** Индекс состоит из одного или нескольких столбцов, а массив содержит значение для сравнения с каждым соответствующим столбцом.|
|*SeekOption* |Значение [SeekEnum,](seekenum.md) которое указывает тип сравнения между столбцами индекса и *соответствующими значениями KeyValues.*|

## <a name="remarks"></a>Заметки

Используйте метод **Seek** в сочетании со свойством [Index,](index-property-ado.md) если поставщик поддерживает индексы объекта **Recordset.** Используйте метод [Supports](supports-method-ado.md)**(adSeek),** чтобы определить, поддерживает ли поставщик **поиск,** и метод **Supports(adIndex),** чтобы определить, поддерживает ли поставщик индексы. (Например, поставщик [OLE DB для Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md) поддерживает **Seek** и **Index.)**

Если **Seek** не находит нужную строку, ошибка не возникает, а строка находится в конце **recordset.** Перед **выполнением** этого метода установите для свойства Index нужный индекс.

Этот метод поддерживается только с помощью курсоров на стороне сервера. Seek не поддерживается, если свойство [CursorLocation](cursorlocation-property-ado.md) объекта **Recordset** имеет значение **adUseClient.**

Этот метод можно использовать, только если объект **Recordset** открыт со значением [CommandTypeEnum](commandtypeenum.md) **adCmdTableDirect.**

