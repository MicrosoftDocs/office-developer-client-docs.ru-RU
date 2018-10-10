---
title: Append Method (ADOX Keys)
TOCTitle: Append Method (ADOX Keys)
ms:assetid: 14d6e8d7-5c9e-a422-47d6-ebfd9dd7a120
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248913(v=office.15)
ms:contentKeyID: 48543396
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3d7e10e272155d2d0377810bf8aa1704a30bad39
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482661"
---
# <a name="append-method-adox-keys"></a>Append Method (ADOX Keys)


**Применимо к**: Access 2013 | Office 2013


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

