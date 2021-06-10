---
title: Свойства Recordset, SourceRecordset (RDS)
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
# <a name="recordset-sourcerecordset-properties-rds"></a>Свойства Recordset, SourceRecordset (RDS)

**Область применения**: Access 2013, Office 2013

Указывает объект **Recordset,** возвращаемый из настраиваемой бизнес-объекта.

## <a name="syntax"></a>Синтаксис

*DataControl*. SourceRecordset = *Recordset*

*Recordset*  =  *DataControl*. Recordset

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*DataControl* |Переменная объекта, представляюая [RDS. Объект DataControl.](datacontrol-object-rds.md)|
|*Recordset* |Переменная объекта, представляют объект **Recordset.**|

## <a name="remarks"></a>Примечания

Свойство **SourceRecordset** можно настроить на [набор recordset,](recordset-object-ado.md) возвращаемый с пользовательского бизнес-объекта.

Эти свойства позволяют приложению обрабатывать процесс привязки с помощью настраиваемого процесса. Они получают набор строк, завернутый в **набор Recordset,** чтобы вы могли напрямую взаимодействовать с **Набором** записей, выполняя действия, такие как настройка свойств или итерации через **Набор записей.**

Вы можете задать **свойство SourceRecordset** или прочитать свойство **Recordset** во время запуска в коде скриптов.

**SourceRecordset** — это свойство только для записи, в отличие от свойства **Recordset,** которое является свойством только для чтения.

