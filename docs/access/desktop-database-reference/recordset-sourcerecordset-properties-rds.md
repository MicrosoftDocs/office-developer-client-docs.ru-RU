---
title: Recordset, свойства SourceRecordset (RDS)
TOCTitle: Recordset, SourceRecordset properties (RDS)
ms:assetid: 5f4bb72d-ddfa-41c0-c353-b3a6632b4a91
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249345(v=office.15)
ms:contentKeyID: 48545160
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f83ab385b1fab511ab71ea9ff3456fe466efa17c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307590"
---
# <a name="recordset-sourcerecordset-properties-rds"></a>Recordset, свойства SourceRecordset (RDS)

**Область применения**: Access 2013, Office 2013

Указывает объект **Recordset** , возвращенный из настраиваемого бизнес-объекта.

## <a name="syntax"></a>Синтаксис

*Элемент управления*. SourceRecordset = *Recordset*

*Recordset* = *Элемент управления*"набор данных". Recordset

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*DataControl* |Объектная переменная, представляющая [RDS. Объект управления](datacontrol-object-rds.md) DataObject.|
|*Recordset* |Объектная переменная, представляющая объект **Recordset** .|

## <a name="remarks"></a>Примечания

Вы можете задать для свойства **SourceRecordset** [набор записей](recordset-object-ado.md) , возвращенный из настраиваемого бизнес-объекта.

Эти свойства позволяют приложению обрабатывать процесс привязки с помощью настраиваемого процесса. Они получают набор строк, заключенный в **набор записей** и позволяющий напрямую взаимодействовать с **набором записей**, выполняя такие действия, как Настройка свойств или итерация по **набору записей**.

Вы можете задать свойство **SourceRecordset** или прочитать свойство **Recordset** во время выполнения в коде сценария.

**SourceRecordset** — это свойство, доступное только для записи, в отличие от свойства **Recordset** , которое является свойством, предназначенным только для чтения.

