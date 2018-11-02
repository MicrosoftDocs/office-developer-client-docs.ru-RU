---
title: Метод Append (коллекция Keys в ADOX)
TOCTitle: Append method (ADOX Keys)
ms:assetid: 14d6e8d7-5c9e-a422-47d6-ebfd9dd7a120
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248913(v=office.15)
ms:contentKeyID: 48543396
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: cc1d03fe68093959406a444419128b161f3b5be4
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921477"
---
# <a name="append-method-adox-keys"></a>Метод Append (коллекция Keys в ADOX)


**Применимо к**: Access 2013, Office 2013


Добавляет новый объект [ключа](key-object-adox.md) в коллекцию [ключей](keys-collection-adox.md) .

## <a name="syntax"></a>Синтаксис

*Ключи*. Добавьте*ключ* \[,*KeyType* \] \[,*столбец* \] \[,*RelatedTable* \] \[,*RelatedColumn*\]

## <a name="parameters"></a>Параметры

  - *Key*

  - Объект **ключ** для добавления или имя раздела для создания и добавления.

  - *KeyType*

  - Необязательно указывать. **Длинное** значение, задающее тип ключа. Параметр *ключ* соответствует свойство [Type](https://msdn.microsoft.com/library/jj248879\(v=office.15\)) объекта **ключа** .

  - *Столбец*

  - Необязательно указывать. **Строковое** значение, задающее имя столбца для индексирования. Параметр *столбцы* соответствует значению свойства [Name](name-property-adox.md) объекта [столбца](column-object-adox.md) .

  - *RelatedTable*

  - Необязательно указывать. **Строковое** значение, задающее имя связанной таблице. Параметр *RelatedTable* соответствует значению свойства **Name** объекта [в таблице](table-object-adox.md) .

  - *RelatedColumn*

  - Необязательно указывать. **Строковое** значение, задающее имя столбца, связанных с ними для внешнего ключа. Параметр RelatedColumn соответствует значению свойства **Name** объекта **столбца** .

## <a name="remarks"></a>Примечания

Для *столбцов* параметра можно задать имя столбца, либо массив имена столбцов.

