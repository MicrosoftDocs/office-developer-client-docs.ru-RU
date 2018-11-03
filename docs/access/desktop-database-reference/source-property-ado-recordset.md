---
title: Свойство Source (объект Recordset в ADO)
TOCTitle: Source property (ADO Recordset)
ms:assetid: 523ea81e-d011-8d87-436e-084b6eba0908
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249269(v=office.15)
ms:contentKeyID: 48544843
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a58ac3c5315daef040ba6a999753a19f76504087
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947574"
---
# <a name="source-property-ado-recordset"></a>Свойство Source (объект Recordset в ADO)


**Применимо к**: Access 2013, Office 2013

Указывает источник данных для объекта [набора записей](recordset-object-ado.md) .

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает **строковое** значение или ссылку на объект [Command](command-object-ado.md) ; Возвращает только **строковое** значение, указывающее источник **набора записей**.

## <a name="remarks"></a>Примечания

Используйте свойство **Source** , чтобы указать источник данных для объекта **набора записей** с помощью одного из следующих действий: переменной объекта **команды** , инструкции SQL, хранимую процедуру или имя таблицы.

Если задать свойство **Source** для объекта **команды** , свойство [ActiveConnection](activeconnection-property-ado.md) объекта **набора записей** наследует значение свойства **ActiveConnection** для указанного объекта **команды** . Тем не менее чтение свойство **Source** не возвращает объект **команды** ; Вместо этого он возвращает свойство [CommandText](commandtext-property-ado.md) объекта **команды** , к которому задать свойство **источника** .

Если свойство **Source** инструкции SQL, хранимую процедуру или имя таблицы, можно оптимизировать производительность, передав соответствующий аргумент *параметров* с помощью вызова метода [Open](open-method-ado-recordset.md) .

Свойство **Source** — чтение и запись для закрытой объектов **наборов записей** и доступны только для чтения, для открытия объектов **набора записей** .

