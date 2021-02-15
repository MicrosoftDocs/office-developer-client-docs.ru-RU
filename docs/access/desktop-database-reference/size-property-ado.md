---
title: Свойство Size (ADO)
TOCTitle: Size property (ADO)
ms:assetid: 24596b5c-b1cc-e97e-68b6-8ff53baf150b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249017(v=office.15)
ms:contentKeyID: 48543753
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2a1bed3454d081b9d5de3a01e9b326130b40baa4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306932"
---
# <a name="size-property-ado"></a>Свойство Size (ADO)


**Область применения**: Access 2013, Office 2013

Указывает максимальный размер объекта [Parameter](parameter-object-ado.md) (в ветвях или символах).

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает **длинное** значение, которое указывает максимальный размер значения в параметров (в ветвях или **символах).**

## <a name="remarks"></a>Заметки

Используйте свойство **Size,** чтобы определить максимальный размер значений, в которые записано или прочитано свойство [Value](value-property-ado.md) объекта **Parameter.**

При указании типа данных переменной длины для объекта **Parameter** (например, любого типа **String,** например **adVarChar),** необходимо задать свойство **Size** объекта перед его приложением в коллекцию [Parameters;](parameters-collection-ado.md) в противном случае возникает ошибка.

Если вы уже применили объект **Parameter** к коллекции **Parameters** объекта [Command](command-object-ado.md) и измените его тип на тип данных переменной длины, перед выполнением объекта **Command** необходимо установить свойство Size объекта **Parameter;**  в противном случае возникает ошибка.

Если метод [Refresh](refresh-method-ado.md) используется для получения сведений о параметрах от поставщика и  возвращает один или несколько объектов parameter типа данных переменной длины, ADO может выделить память для параметров в зависимости от их максимального потенциального размера, что может привести к ошибке во время выполнения. Чтобы избежать ошибки, перед выполнением команды необходимо явно установить свойство **Size** для этих параметров.

Свойство **Size** имеет свойство read/write.

