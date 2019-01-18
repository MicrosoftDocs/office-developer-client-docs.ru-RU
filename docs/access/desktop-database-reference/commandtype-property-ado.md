---
title: Свойство CommandType (ADO)
TOCTitle: CommandType property (ADO)
ms:assetid: c8d4fc1c-502b-11f3-af9d-605a03b6f056
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249976(v=office.15)
ms:contentKeyID: 48547663
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231125
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: c978a6a227266fa43c1102fc109be2b81262de8e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717148"
---
# <a name="commandtype-property-ado"></a>Свойство CommandType (ADO)


**Применимо к**: Access 2013, Office 2013

Указывает тип объекта [команды](command-object-ado.md) .

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает одно или несколько значений [CommandTypeEnum](commandtypeenum.md) .

> [!NOTE]
> Не используйте значения **CommandTypeEnum** **adCmdFile** или **adCmdTableDirect** с **CommandType**. Эти значения может использоваться только как параметры методов [Open](open-method-ado-recordset.md) и [повторный запрос](requery-method-ado.md) набора [записей](recordset-object-ado.md).


## <a name="remarks"></a>Замечания

Используйте свойство **CommandType** для оптимизации оценки свойства [CommandText](commandtext-property-ado.md) .

Если значение свойства **CommandType** равно **adCmdUnknown** (значение по умолчанию), так как ADO необходимо выполнять вызовы к поставщику, чтобы определить свойство **CommandText** инструкции SQL, сохраненного могут возникнуть снижение производительности процедуры, или имя таблицы. Если вы знаете, какой тип используется, задав свойство **CommandType** команда указывает ADO для перехода в соответствующий код. Если свойство **CommandType** не соответствует типу команды в свойстве **CommandText** , возникает ошибка при вызове метода [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) .

