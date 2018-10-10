---
title: Recordset, SourceRecordset Properties (RDS)
TOCTitle: Recordset, SourceRecordset Properties (RDS)
ms:assetid: 5f4bb72d-ddfa-41c0-c353-b3a6632b4a91
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249345(v=office.15)
ms:contentKeyID: 48545160
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a66e803738c16d291817eb80e7f680ff9c3c71e9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481263"
---
# <a name="recordset-sourcerecordset-properties-rds"></a>Recordset, SourceRecordset Properties (RDS)


**Применимо к**: Access 2013 | Office 2013

Указывает, возвращать пользовательский бизнес-объект объекта **набора записей** .

## <a name="syntax"></a>Синтаксис

*DataControl*. SourceRecordset = *набора записей*

*Набор записей* = *DataControl*. Набор записей

## <a name="parameters"></a>Параметры

  - *DataControl*

  - Объектную переменную, которая представляет [RDS. DataControl](datacontrol-object-rds.md) объекта.

  - *Набор записей*

  - Объектная переменная, представляющий объект **набора записей** .

## <a name="remarks"></a>Замечания

Свойства **SourceRecordset** значение [набора записей](recordset-object-ado.md) , возвращаемых настраиваемых бизнес-объекта.

Эти свойства позволяют приложению обрабатывать процесс привязки с помощью настраиваемого процесса. Они получают набор строк, заключенное в **набор записей** , чтобы вы могли взаимодействовать непосредственно с **набора записей**, для выполнения действий, таких как установка свойств или итерации **записей**.

Можно задать свойство **SourceRecordset** или чтение свойства **набора записей** во время выполнения в код сценария.

**SourceRecordset** является свойством только для записи, в отличие от свойства **набора записей** , которое является свойством только для чтения.

