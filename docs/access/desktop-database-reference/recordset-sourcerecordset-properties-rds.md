---
title: Свойства Recordset и SourceRecordset (RDS)
TOCTitle: Recordset, SourceRecordset properties (RDS)
ms:assetid: 5f4bb72d-ddfa-41c0-c353-b3a6632b4a91
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249345(v=office.15)
ms:contentKeyID: 48545160
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 21176e050c77b0f14fcb03b054e8a1ab692df7d5
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949259"
---
# <a name="recordset-sourcerecordset-properties-rds"></a>Свойства Recordset и SourceRecordset (RDS)

**Применимо к**: Access 2013, Office 2013

Указывает, возвращать пользовательский бизнес-объект объекта **набора записей** .

## <a name="syntax"></a>Синтаксис

*DataControl*. SourceRecordset = *набора записей*

*Набор записей* = *DataControl*. Набор записей

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*DataControl* |Объектную переменную, которая представляет [RDS. DataControl](datacontrol-object-rds.md) объекта.|
|*Набор записей* |Объектная переменная, представляющий объект **набора записей** .|

## <a name="remarks"></a>Примечания

Свойства **SourceRecordset** значение [набора записей](recordset-object-ado.md) , возвращаемых настраиваемых бизнес-объекта.

Эти свойства позволяют приложению обрабатывать процесс привязки с помощью настраиваемого процесса. Они получают набор строк, заключенное в **набор записей** , чтобы вы могли взаимодействовать непосредственно с **набора записей**, для выполнения действий, таких как установка свойств или итерации **записей**.

Можно задать свойство **SourceRecordset** или чтение свойства **набора записей** во время выполнения в код сценария.

**SourceRecordset** является свойством только для записи, в отличие от свойства **набора записей** , которое является свойством только для чтения.

