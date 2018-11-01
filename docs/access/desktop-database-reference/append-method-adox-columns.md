---
title: Добавьте метод (ADOX столбцов)
TOCTitle: Append Method (ADOX Columns)
ms:assetid: e256a478-abc0-f15b-fc29-1b52e354144a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250152(v=office.15)
ms:contentKeyID: 48548285
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ec64241bf63719fe4f5c547d60a93f7804f181ca
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25877662"
---
# <a name="append-method-adox-columns"></a>Добавьте метод (ADOX столбцов)


**Применимо к**: Access 2013, Office 2013

Добавляет новый объект [столбца](column-object-adox.md) в коллекцию [столбцов](columns-collection-adox.md) .

## <a name="syntax"></a>Синтаксис

*Столбцы*. Добавление*столбца* \[,*Тип* \] \[,*DefinedSize*\]

## <a name="parameters"></a>Параметры

  - *Столбец*

  - Объект для добавления **столбца** или имя столбца для создания и добавления.

  - *Тип*

  - Необязательный параметр. Значение типа **Long** , определяющее тип данных столбца. Параметр *типа* соответствует свойство [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) объекта **столбца** .

  - *DefinedSize*

  - Необязательный параметр. Значение типа **Long** , определяет размер столбца. Параметр *DefinedSize* соответствует свойству [DefinedSize](definedsize-property-adox.md) объекта **столбца** .


> [!NOTE]
> После добавления **столбцов** в коллекцию **столбцов** [индекса](index-object-adox.md) , если **Столбец** не существует в [таблице](table-object-adox.md) , уже добавлен в коллекцию [таблиц](tables-collection-adox.md) , произойдет ошибка.


