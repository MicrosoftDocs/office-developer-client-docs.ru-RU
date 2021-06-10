---
title: Метод обновления (ADO)
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
# <a name="refresh-method-ado"></a>Метод обновления (ADO)

**Область применения**: Access 2013, Office 2013

Обновляет объекты в коллекции, чтобы отражать объекты, доступные поставщику, и определенные для него.

## <a name="syntax"></a>Синтаксис

*коллекция*. Обновление

## <a name="remarks"></a>Примечания

Метод **Обновления** выполняет различные задачи в зависимости от коллекции, из которой он называется.

## <a name="parameters"></a>Parameters

С помощью метода [](command-object-ado.md) **Обновления** в [](parameters-collection-ado.md) коллекции Параметры объекта Command извлекает сведения о параметрах поставщика для сохраненной процедуры или параметризованного запроса, указанного в **объекте Command.** Коллекция будет пустой для поставщиков, которые не поддерживают сохраненные вызовы процедур или параметризированные запросы.

Перед вызовом метода Обновления необходимо  упредить [](connection-object-ado.md) свойство [ActiveConnection](activeconnection-property-ado.md) объекта Command допустимым объектом Подключения, свойство [CommandText](commandtext-property-ado.md) допустимой командой и свойство [CommandType](commandtype-property-ado.md) **adCmdStoredProc.** 

Если вы имеете доступ к коллекции **Параметры** перед вызовом метода **Обновления,** ADO автоматически вызывает метод и заполняет коллекцию для вас.

> [!NOTE]
> Если метод **Обновления** используется для получения сведений о параметрах от поставщика и [](parameter-object-ado.md) возвращает один или несколько объектов типа параметра переменной длины, ADO может выделять память для параметров в зависимости от их максимального потенциального размера, что приведет к ошибке во время выполнения. Прежде чем вызывать метод [Execute,](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) чтобы предотвратить ошибки, необходимо явно задано свойство [Size](size-property-ado.md) для этих параметров.

### <a name="fields"></a>Fields

Использование метода **Обновления** в коллекции **Fields** не оказывает видимого эффекта. Чтобы получить изменения из структуры баз данных, необходимо использовать метод [Requery](requery-method-ado.md) или, если объект [Recordset](recordset-object-ado.md) не поддерживает закладки, метод [MoveFirst.](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)

### <a name="properties"></a>Свойства

Использование метода **Обновления** в коллекции **свойств** некоторых объектов заполняет коллекцию динамическими свойствами, которые предоставляет поставщик. Эти свойства предоставляют сведения о функциональных возможностях, определенных поставщику, за пределами встроенных свойств, поддерживаемых ADO.

