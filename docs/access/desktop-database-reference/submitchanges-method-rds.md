---
title: Метод SubmitChanges (RDS)
TOCTitle: SubmitChanges method (RDS)
ms:assetid: ecaea12d-7e1a-095d-17e7-d631ef230b90
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250201(v=office.15)
ms:contentKeyID: 48548521
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ea7f3e27a75b4483cb8cf46e27d4492f831cff33
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314401"
---
# <a name="submitchanges-method-rds"></a>Метод SubmitChanges (RDS)

**Область применения**: Access 2013, Office 2013

Отправка ожидающих изменений локально кэшируемых и updatable [recordset](recordset-object-ado.md) в источник данных, указанный в свойстве [Connect](connect-property-rds.md) или [URL-адресе.](url-property-rds.md)

## <a name="syntax"></a>Синтаксис

*DataControl*. SubmitChanges

*DataFactory*. Подключение SubmitChanges, *Recordset*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*DataControl* |Объектная переменная, представляюная [RDS. Объект DataControl.](datacontrol-object-rds.md)|
|*DataFactory* |Объектная переменная, представляюная [объект RDSServer.DataFactory.](datafactory-object-rdsserver.md)|
|*Connection* |**Строка,** представляютив подключение, созданное с **помощью RDS. Свойство Connect объекта DataControl.** |
|*Recordset* |Объектная переменная, представляюная объект **Recordset.**|

## <a name="remarks"></a>Заметки

Свойства [Connect,](connect-property-rds.md) [Server](server-property-rds.md) [и SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) должны быть заданы перед использованием метода **SubmitChanges** с **RDS. Объект DataControl.**

Если вызвать метод [CancelUpdate](cancelupdate-method-rds.md) после вызова **SubmitChanges** для того же объекта **Recordset,** вызов **CancelUpdate** не удастся, так как изменения уже были зафиксированы.

Для изменения отправляются только измененные записи, и либо все изменения будут успешными, либо все они будут сбой вместе.

**SubmitChanges можно использовать** только с *объектом* **RDSServer.DataFactory** по умолчанию. Настраиваемые бизнес-объекты не могут использовать этот метод.

Если свойство **URL-адреса** задано, **SubmitChanges** будет отправлять изменения в расположение, указанное URL-адресом.

