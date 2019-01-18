---
title: Свойства Recordset и SourceRecordset (RDS)
TOCTitle: Recordset, SourceRecordset properties (RDS)
ms:assetid: 5f4bb72d-ddfa-41c0-c353-b3a6632b4a91
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249345(v=office.15)
ms:contentKeyID: 48545160
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f83ab385b1fab511ab71ea9ff3456fe466efa17c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703526"
---
# <a name="recordset-sourcerecordset-properties-rds"></a>Свойства Recordset и SourceRecordset (RDS)

**Применимо к**: Access 2013, Office 2013

Указывает, возвращать пользовательский бизнес-объект объекта **набора записей** .

## <a name="syntax"></a>Синтаксис

*DataControl*. SourceRecordset = *набора записей*

*Набор записей* = *DataControl*. Набор записей

## <a name="parameters"></a>Parameters

|Параметр|Описание|
|:--------|:----------|
|*DataControl* |Объектную переменную, которая представляет [RDS. DataControl](datacontrol-object-rds.md) объекта.|
|*Recordset* |Объектная переменная, представляющий объект **набора записей** .|

## <a name="remarks"></a>Замечания

Свойства **SourceRecordset** значение [набора записей](recordset-object-ado.md) , возвращаемых настраиваемых бизнес-объекта.

Эти свойства позволяют приложению обрабатывать процесс привязки с помощью настраиваемого процесса. Они получают набор строк, заключенное в **набор записей** , чтобы вы могли взаимодействовать непосредственно с **набора записей**, для выполнения действий, таких как установка свойств или итерации **записей**.

Можно задать свойство **SourceRecordset** или чтение свойства **набора записей** во время выполнения в код сценария.

**SourceRecordset** является свойством только для записи, в отличие от свойства **набора записей** , которое является свойством только для чтения.

