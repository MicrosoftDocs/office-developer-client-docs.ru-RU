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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296124"
---
# <a name="commandtype-property-ado"></a>Свойство CommandType (ADO)


**Область применения**: Access 2013, Office 2013

Указывает тип объекта [Command.](command-object-ado.md)

## <a name="settings-and-return-values"></a>Параметры и значения возврата

Задает или возвращает одно или несколько [значений CommandTypeEnum.](commandtypeenum.md)

> [!NOTE]
> Не используйте **значения CommandTypeEnum** **adCmdFile** или **adCmdTableDirect** с **командным типом.** Эти значения можно использовать только в качестве параметров с помощью методов [Open](open-method-ado-recordset.md) и [Requery](requery-method-ado.md) [recordset.](recordset-object-ado.md)


## <a name="remarks"></a>Примечания

Используйте свойство **CommandType** для оптимизации оценки свойства [CommandText.](commandtext-property-ado.md)

Если значение **свойства CommandType** равно **adCmdUnknown** (значение по умолчанию), производительность может снизиться, так как ADO должна звонить поставщику, чтобы определить, является ли свойство **CommandText** оператором SQL, сохраненной процедурой или именем таблицы. Если вы знаете, какой тип команды вы используете, задав свойство **CommandType** указание ADO перейти непосредственно к соответствующему коду. Если свойство **CommandType** не соответствует типу команды в свойстве **CommandText,** при вызове метода [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) возникает ошибка.

