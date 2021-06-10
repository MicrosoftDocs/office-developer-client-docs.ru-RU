---
title: Поиск метода — ActiveX объектов данных (ADO)
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
# <a name="seek-method-ado"></a>Поиск метода (ADO)

**Область применения**: Access 2013, Office 2013

Выполняется поиск индекса [наборов записей,](recordset-object-ado.md) чтобы быстро найти строку, которая соответствует указанным значениям, и изменить текущее положение строки в этой строке.

## <a name="syntax"></a>Синтаксис

*набор записей.* Seek *KeyValues*, *SeekOption*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*KeyValues* |Массив **значений Variant.** Индекс состоит из одного или нескольких столбцов, а массив содержит значение для сравнения с каждым соответствующим столбцом.|
|*SeekOption* |Значение [SeekEnum,](seekenum.md) которое указывает тип сравнения между столбцами индекса и *соответствующими KeyValues.*|

## <a name="remarks"></a>Примечания

Используйте метод **Seek** совместно с свойством [Index,](index-property-ado.md) если поставщик поддерживает индексы на **объекте Recordset.** Используйте метод Supports **(adSeek),** чтобы определить, поддерживает ли поставщик seek **и** метод [Supports](supports-method-ado.md) **(adIndex),** чтобы определить, поддерживает ли поставщик индексы. (Например, поставщик [OLE DB для Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md) поддерживает **Seek** and **Index.)**

Если **Seek** не находит нужную строку, ошибки не возникает, и строка находится в конце **recordset.** Установите свойство **Index** в нужный индекс перед выполнением этого метода.

Этот метод поддерживается только с помощью курсоров на стороне сервера. Поиск не поддерживается, когда значение [свойства CursorLocation](cursorlocation-property-ado.md) объекта **Recordset** **является adUseClient.**

Этот метод можно использовать только в том случае, если объект **Recordset** открыт со значением [CommandTypeEnum](commandtypeenum.md) **adCmdTableDirect.**

