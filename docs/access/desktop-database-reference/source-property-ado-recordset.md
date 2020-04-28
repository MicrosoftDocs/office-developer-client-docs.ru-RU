---
title: Свойство Source (Recordset в ADO)
TOCTitle: Source property (ADO Recordset)
ms:assetid: 523ea81e-d011-8d87-436e-084b6eba0908
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249269(v=office.15)
ms:contentKeyID: 48544843
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 26f41181f1233931f24ff091b3009dfa7a5d6ff3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306414"
---
# <a name="source-property-ado-recordset"></a>Свойство Source (Recordset в ADO)


**Область применения**: Access 2013, Office 2013

Указывает источник данных для объекта [Recordset](recordset-object-ado.md) .

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает **строковое** значение или ссылку на объект [команды](command-object-ado.md) ; Возвращает только **строковое** значение, указывающее источник объекта **Recordset**.

## <a name="remarks"></a>Примечания

Используйте свойство **Source** , чтобы указать источник данных для объекта **Recordset** с помощью одного из следующих элементов: объектная ПЕРЕМЕННАЯ **команды** , инструкция SQL, хранимая процедура или имя таблицы.

Если свойству **Source** присвоено значение **Command** , свойство [ActiveConnection](activeconnection-property-ado.md) объекта **Recordset** будет наследовать значение свойства **ActiveConnection** для указанного объекта **Command** . Однако чтение свойства **Source** не возвращает объект **Command** ; Вместо этого возвращается свойство [CommandText](commandtext-property-ado.md) объекта **Command** , для которого задается свойство **Source** .

Если свойство **Source** имеет инструкцию SQL, хранимую процедуру или имя таблицы, можно оптимизировать производительность, передав соответствующий аргумент *Options* с помощью вызова метода [Open](open-method-ado-recordset.md) .

Свойство **Source** доступно для чтения и записи для закрытых объектов **Recordset** и только для чтения для объектов Open **Recordset** .

