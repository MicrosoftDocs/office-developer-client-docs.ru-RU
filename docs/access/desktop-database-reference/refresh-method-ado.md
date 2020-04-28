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

Обновляет объекты в коллекции, чтобы отразить объекты, доступные поставщику и соответствующие объекты.

## <a name="syntax"></a>Синтаксис

*коллекция*. Обновление

## <a name="remarks"></a>Примечания

Метод **Refresh** выполняет различные задачи в зависимости от того, из какой коллекции он вызывается.

## <a name="parameters"></a>Параметры

При использовании метода **Refresh** в коллекции [Parameters](parameters-collection-ado.md) объекта [Command](command-object-ado.md) извлекаются сведения о параметрах на стороне поставщика для хранимой процедуры или запроса с параметрами, указанными в объекте **Command** . Коллекция будет пустой для поставщиков, которые не поддерживают вызовы хранимых процедур или параметризованные запросы.

Необходимо задать для свойства [ActiveConnection](activeconnection-property-ado.md) объекта **Command** допустимый объект [Connection](connection-object-ado.md) , свойство [CommandText](commandtext-property-ado.md) для допустимой команды, а свойство [CommandType](commandtype-property-ado.md) — **адкмдсторедпрок** перед вызовом метода **Refresh** .

Если вы обращаетесь к коллекции **Parameters** перед вызовом метода **Refresh** , ADO автоматически вызывает метод и заполняет коллекцию.

> [!NOTE]
> Если вы используете метод **Refresh** для получения сведений о параметрах от поставщика и возвращает один или несколько объектов [параметров](parameter-object-ado.md) типа данных переменной длины, ADO может выделить память для параметров на основе максимально возможного размера, что приведет к ошибке во время выполнения. Необходимо явно задать свойство [size](size-property-ado.md) для этих параметров перед вызовом метода [EXECUTE](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) для предотвращения ошибок.

### <a name="fields"></a>Fields

Использование метода **Refresh** в коллекции **Fields** не имеет видимого результата. Чтобы получить изменения из базовой структуры базы данных, необходимо использовать метод [Requery](requery-method-ado.md) либо, если объект [Recordset](recordset-object-ado.md) не поддерживает закладки, метод [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) .

### <a name="properties"></a>Свойства

Использование метода **Refresh** для коллекции **свойств** некоторых объектов заполняет коллекцию динамическими свойствами, предоставляемыми поставщиком. Эти свойства предоставляют сведения о функциональных возможностях, характерных для поставщика, Кроме встроенных свойств ADO.

