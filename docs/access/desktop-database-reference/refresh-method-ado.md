---
title: Метод Refresh (ADO)
TOCTitle: Refresh method (ADO)
ms:assetid: f1c8829f-9c7d-12b6-7470-727ff38d663e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250227(v=office.15)
ms:contentKeyID: 48548631
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: bd7c47e7c3e41a7b42571043cfafc9e4e909a9f9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309259"
---
# <a name="refresh-method-ado"></a>Метод Refresh (ADO)

**Область применения**: Access 2013, Office 2013

Обновляет объекты в коллекции, чтобы отразить объекты, доступные поставщику и относяющиеся к конкретному поставщику.

## <a name="syntax"></a>Синтаксис

*collection*. Обновление

## <a name="remarks"></a>Заметки

Метод **Refresh** выполняет различные задачи в зависимости от коллекции, из которой он вызываем.

## <a name="parameters"></a>Параметры

Использование метода **Refresh** в коллекции [параметров](parameters-collection-ado.md) объекта [Command](command-object-ado.md) извлекает сведения о параметрах на стороне поставщика для хранимой процедуры или параметризованного запроса, указанного в **объекте Command.** Коллекция будет пустой для поставщиков, которые не поддерживают хранимые вызовы процедур или параметризованные запросы.

Перед вызовом метода **Refresh** необходимо установить для свойства [ActiveConnection](activeconnection-property-ado.md) объекта **Command** допустимый объект [Connection,](connection-object-ado.md) для свойства [CommandText](commandtext-property-ado.md) допустимую команду и свойство [CommandType](commandtype-property-ado.md) для **adCmdStoredProc.**

При доступе к коллекции **Parameters** перед вызовом метода **Refresh** ADO автоматически вызывает метод и заполняет коллекцию автоматически.

> [!NOTE]
> Если метод **Refresh** используется для получения сведений о параметрах от поставщика и [](parameter-object-ado.md) возвращает один или несколько объектов parameter типа данных переменной длины, ADO может выделить память для параметров в зависимости от их максимального потенциального размера, что приведет к ошибке во время выполнения. Перед вызовом метода [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) необходимо явно установить свойство [Size](size-property-ado.md) для этих параметров, чтобы предотвратить ошибки.

### <a name="fields"></a>Поля

Использование метода **Refresh** для коллекции **Fields** не оказывает видимого эффекта. Чтобы получить изменения из структуры баз данных, необходимо использовать либо метод [Requery,](requery-method-ado.md) либо, если объект [Recordset](recordset-object-ado.md) не поддерживает закладки, [метод MoveFirst.](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)

### <a name="properties"></a>Свойства

Использование метода **Refresh** для коллекции **свойств** некоторых объектов заполняет коллекцию динамическими свойствами, которые предоставляет поставщик. Эти свойства предоставляют сведения о функциях, характерных для поставщика, помимо встроенных свойств, поддерживаемых ADO.

