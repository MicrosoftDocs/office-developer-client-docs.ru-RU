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

Указывает источник данных для объекта [Recordset.](recordset-object-ado.md)

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает **строку значения** или [ссылку на объект](command-object-ado.md) Command; возвращает только **строку,** которая указывает источник **recordset.**

## <a name="remarks"></a>Заметки

Свойство **Source** используется для указания источника данных для объекта **Recordset** с помощью одной из следующих переменных: переменной объекта **Command,** SQL, хранимой процедуры или имени таблицы.

Если для свойства **Source** задан объект **Command,** свойство [ActiveConnection](activeconnection-property-ado.md) объекта **Recordset** наследует значение свойства **ActiveConnection** для указанного **объекта** Command. Однако чтение свойства **Source** не возвращает объект **Command;** вместо этого он возвращает свойство [CommandText](commandtext-property-ado.md) объекта **Command,** для которого занося **свойство Source.**

Если свойство **Source** является SQL, хранимой процедурой или именем таблицы, можно оптимизировать производительность, передав соответствующий аргумент *Options* с помощью вызова метода [Open.](open-method-ado-recordset.md)

Свойство **Source** — это свойство чтения и записи для закрытых объектов **Recordset** и только для чтения для открытых **объектов Recordset.**

