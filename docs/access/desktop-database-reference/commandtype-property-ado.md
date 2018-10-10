---
title: CommandType Property (ADO)
TOCTitle: CommandType Property (ADO)
ms:assetid: c8d4fc1c-502b-11f3-af9d-605a03b6f056
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249976(v=office.15)
ms:contentKeyID: 48547663
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231125
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 3cff3c3540208b142fc13cd79eb83bd218814873
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483237"
---
# <a name="commandtype-property-ado"></a>CommandType Property (ADO)


**Применимо к**: Access 2013 | Office 2013

Указывает тип объекта [команды](command-object-ado.md) .

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает одно или несколько значений [CommandTypeEnum](commandtypeenum.md) .


> [!NOTE]
> <P>Не используйте значения <STRONG>CommandTypeEnum</STRONG> <STRONG>adCmdFile</STRONG> или <STRONG>adCmdTableDirect</STRONG> с <STRONG>CommandType</STRONG>. Эти значения может использоваться только как параметры методов <A href="open-method-ado-recordset.md">Open</A> и <A href="requery-method-ado.md">повторный запрос</A> набора <A href="recordset-object-ado.md">записей</A>.</P>



## <a name="remarks"></a>Замечания

Используйте свойство **CommandType** для оптимизации оценки свойства [CommandText](commandtext-property-ado.md) .

Если значение свойства **CommandType** равно **adCmdUnknown** (значение по умолчанию), так как ADO необходимо выполнять вызовы к поставщику, чтобы определить свойство **CommandText** инструкции SQL, сохраненного могут возникнуть снижение производительности процедуры, или имя таблицы. Если вы знаете, какой тип используется, задав свойство **CommandType** команда указывает ADO для перехода в соответствующий код. Если свойство **CommandType** не соответствует типу команды в свойстве **CommandText** , возникает ошибка при вызове метода [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)) .

