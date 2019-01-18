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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718905"
---
# <a name="append-method-adox-keys"></a>Метод Append (коллекция Keys в ADOX)

**Применимо к**: Access 2013, Office 2013

Добавляет новый объект [ключа](key-object-adox.md) в коллекцию [ключей](keys-collection-adox.md) .

## <a name="syntax"></a>Синтаксис

*Ключи*. Добавьте*ключ* \[,*KeyType* \] \[,*столбец* \] \[,*RelatedTable* \] \[,*RelatedColumn*\]

## <a name="parameters"></a>Parameters

|Параметр|Описание|
|:--------|:----------|
|*Key* |Объект **ключ** для добавления или имя раздела для создания и добавления.|
|*KeyType* |Необязательно. **Длинное** значение, задающее тип ключа. Параметр *ключ* соответствует свойство [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-keyadox) объекта **ключа** .|
|*Column* |Необязательно. **Строковое** значение, задающее имя столбца для индексирования. Параметр *столбцы* соответствует значению свойства [Name](name-property-adox.md) объекта [столбца](column-object-adox.md) .|
|*RelatedTable* |Необязательно. **Строковое** значение, задающее имя связанной таблице. Параметр *RelatedTable* соответствует значению свойства **Name** объекта [в таблице](table-object-adox.md) .|
|*RelatedColumn* |Необязательно. **Строковое** значение, задающее имя столбца, связанных с ними для внешнего ключа. Параметр RelatedColumn соответствует значению свойства **Name** объекта **столбца** .|

## <a name="remarks"></a>Замечания

Для *столбцов* параметра можно задать имя столбца, либо массив имена столбцов.

