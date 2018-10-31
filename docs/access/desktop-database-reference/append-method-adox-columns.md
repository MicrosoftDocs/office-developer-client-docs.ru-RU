---
title: Добавьте метод (ADOX столбцов)
TOCTitle: Append Method (ADOX Columns)
ms:assetid: e256a478-abc0-f15b-fc29-1b52e354144a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250152(v=office.15)
ms:contentKeyID: 48548285
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 727634356a08646b1e2757996cc6bf071de07353
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861577"
---
# <a name="append-method-adox-columns"></a>Добавьте метод (ADOX столбцов)


**Применимо к**: Access 2013 | Office 2013

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


