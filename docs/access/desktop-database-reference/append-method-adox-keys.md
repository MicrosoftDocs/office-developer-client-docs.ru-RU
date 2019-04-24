---
title: Метод Append (коллекция Keys в ADOX)
TOCTitle: Append method (ADOX Keys)
ms:assetid: 14d6e8d7-5c9e-a422-47d6-ebfd9dd7a120
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248913(v=office.15)
ms:contentKeyID: 48543396
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c301f6809ab7f785497637b12e0b5d7a0bb7772d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297090"
---
# <a name="append-method-adox-keys"></a>Метод Append (коллекция Keys в ADOX)

**Область применения**: Access 2013, Office 2013

Добавляет новый объект [Key](key-object-adox.md) в коллекцию [Keys](keys-collection-adox.md) .

## <a name="syntax"></a>Синтаксис

*Ключи*. Добавление*ключа* \[,*KeyType* \] \[,** \] Column \[,** RelatedTable\] ** , RelatedColumn \[\]

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*Key* |Объект **Key** , который необходимо добавить, или имя ключа для создания и добавления.|
|*Раздела* |Необязательный атрибут. **Длинное** значение, задающее тип ключа. Параметр *Key* соответствует свойству [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-keyadox) объекта **Key** .|
|*Column* |Необязательный атрибут. **Строковое** значение, задающее имя индексируемого столбца. Параметр *Columns* соответствует значению свойства [Name](name-property-adox.md) объекта [Column](column-object-adox.md) .|
|*RelatedTable* |Необязательный атрибут. **Строковое** значение, задающее имя связанной таблицы. Параметр *RelatedTable* соответствует значению свойства **Name** объекта [Table](table-object-adox.md) .|
|*RelatedColumn* |Необязательный атрибут. **Строковое** значение, задающее имя связанного столбца для внешнего ключа. Параметр RelatedColumn соответствует значению свойства **Name** объекта **Column** .|

## <a name="remarks"></a>Замечания

Параметр *Columns* может принимать либо имя столбца, либо массив имен столбцов.

