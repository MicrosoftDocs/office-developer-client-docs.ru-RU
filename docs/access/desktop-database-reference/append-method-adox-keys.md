---
title: Добавьте метод (ADOX ключей)
TOCTitle: Append Method (ADOX Keys)
ms:assetid: 14d6e8d7-5c9e-a422-47d6-ebfd9dd7a120
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248913(v=office.15)
ms:contentKeyID: 48543396
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5ba46c922ff9fc27da0abc1908f6ffaff8e997ef
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879461"
---
# <a name="append-method-adox-keys"></a>Добавьте метод (ADOX ключей)


**Применимо к**: Access 2013, Office 2013


Добавляет новый объект [ключа](key-object-adox.md) в коллекцию [ключей](keys-collection-adox.md) .

## <a name="syntax"></a>Синтаксис

*Ключи*. Добавьте*ключ* \[,*KeyType* \] \[,*столбец* \] \[,*RelatedTable* \] \[,*RelatedColumn*\]

## <a name="parameters"></a>Параметры

  - *Key*

  - Объект **ключ** для добавления или имя раздела для создания и добавления.

  - *KeyType*

  - Необязательный параметр. **Длинное** значение, задающее тип ключа. Параметр *ключ* соответствует свойство [Type](https://msdn.microsoft.com/library/jj248879\(v=office.15\)) объекта **ключа** .

  - *Столбец*

  - Необязательный параметр. **Строковое** значение, задающее имя столбца для индексирования. Параметр *столбцы* соответствует значению свойства [Name](name-property-adox.md) объекта [столбца](column-object-adox.md) .

  - *RelatedTable*

  - Необязательный параметр. **Строковое** значение, задающее имя связанной таблице. Параметр *RelatedTable* соответствует значению свойства **Name** объекта [в таблице](table-object-adox.md) .

  - *RelatedColumn*

  - Необязательный параметр. **Строковое** значение, задающее имя столбца, связанных с ними для внешнего ключа. Параметр RelatedColumn соответствует значению свойства **Name** объекта **столбца** .

## <a name="remarks"></a>Замечания

Для *столбцов* параметра можно задать имя столбца, либо массив имена столбцов.

