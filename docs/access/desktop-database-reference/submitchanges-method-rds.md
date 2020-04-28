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

Передает ожидающие изменения локального кэшированного и обновляемого [набора записей](recordset-object-ado.md) в источник данных, указанный в свойстве [Connect](connect-property-rds.md) или [URL-адрес](url-property-rds.md) .

## <a name="syntax"></a>Синтаксис

*Элемент управления*. SubmitChanges

*Фактическое*. *Подключение*SubmitChanges, *набор записей*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*DataControl* |Объектная переменная, представляющая [RDS. Объект управления](datacontrol-object-rds.md) DataObject.|
|*DataFactory* |Объектная переменная, представляющая объект [фактов рдссервер.](datafactory-object-rdsserver.md) DataObject.|
|*Connection* |**Строковое** значение, представляющее подключение, созданное с помощью **RDS. **Свойство **Connect** объекта DataObject.|
|*Recordset* |Объектная переменная, представляющая объект **Recordset** .|

## <a name="remarks"></a>Примечания

Необходимо задать свойства [Connect](connect-property-rds.md), [Server](server-property-rds.md)и [SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) , прежде чем можно будет использовать метод **SubmitChanges** с помощью **RDS. Объект управления** DataObject.

Если метод [CancelUpdate](cancelupdate-method-rds.md) вызывается после вызова **SubmitChanges** для того же объекта **Recordset** , вызов **CancelUpdate** завершится с ошибкой, так как изменения уже были зафиксированы.

Только измененные записи отправляются для изменения и либо все изменения успешно выполнены, либо все они работают вместе.

Параметр **SubmitChanges** можно использовать только с объектом **рдссервер.** DataObject, *используемым по умолчанию* . Пользовательские бизнес-объекты не могут использовать этот метод.

Если задано свойство **URL** , **SubmitChanges** отправит изменения в расположении, указанном с помощью URL-адреса.

