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

Отправка ожидающих изменений локально кэшируемых и updatable [Recordset](recordset-object-ado.md) источнику данных, указанному в свойстве Подключение или [свойстве](url-property-rds.md) [URL-адреса.](connect-property-rds.md)

## <a name="syntax"></a>Синтаксис

*DataControl*. SubmitChanges

*DataFactory*. SubmitChanges *Connection*, *Recordset*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*DataControl* |Переменная объекта, представляюая [RDS. Объект DataControl.](datacontrol-object-rds.md)|
|*DataFactory* |Переменная объекта, представляют [объект RDSServer.DataFactory.](datafactory-object-rdsserver.md)|
|*Connection* |Значение **String,** представляю которое представляет соединение, созданное с **RDS. Свойство Подключение объекта DataControl.** |
|*Recordset* |Переменная объекта, представляют объект **Recordset.**|

## <a name="remarks"></a>Примечания

Свойства [Подключение,](connect-property-rds.md) [server](server-property-rds.md)и [SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) должны быть заданы, прежде чем использовать метод **SubmitChanges** с **помощью RDS. Объект DataControl.**

При вызове метода [CancelUpdate](cancelupdate-method-rds.md) после вызова **SubmitChanges** для того же объекта **Recordset** вызов **CancelUpdate** не удается, так как изменения уже были совершены.

Только измененные записи отправляются для изменения, и либо все изменения успешно, либо все они сбой вместе.

Можно использовать **SubmitChanges** только с *объектом* **RDSServer.DataFactory** по умолчанию. Настраиваемые бизнес-объекты не могут использовать этот метод.

Если свойство **URL-адреса** задано, **SubmitChanges** будет отправлять изменения в указанное URL-адресом расположение.

