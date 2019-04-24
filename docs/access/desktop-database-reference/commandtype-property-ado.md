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

Указывает тип объекта [Command](command-object-ado.md) .

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает одно или несколько значений [коммандтипинум](commandtypeenum.md) .

> [!NOTE]
> Не используйте значения **коммандтипинум** для **адкмдфиле** или **адкмдтабледирект** с **CommandType**. Эти значения можно использовать только в качестве параметров с помощью методов [Open](open-method-ado-recordset.md) и Requery объекта [Recordset](recordset-object-ado.md). [](requery-method-ado.md)


## <a name="remarks"></a>Замечания

Используйте свойство **CommandType** для оптимизации оценки свойства [CommandText](commandtext-property-ado.md) .

Если значение свойства **CommandType** равно **адкмдункновн** (значение по умолчанию), может наблюдаться снижение производительности, так как ADO должен вызывать поставщик, чтобы определить, является ли свойство **CommandText** оператором SQL, хранимая процедура или имя таблицы. Если вы знаете, какой тип команды вы используете, задание свойства **CommandType** указывает ADO перейти непосредственно к соответствующему коду. Если свойство **CommandType** не отвечает типу команды в свойстве **CommandText** , при вызове метода [EXECUTE](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) возникает ошибка.

