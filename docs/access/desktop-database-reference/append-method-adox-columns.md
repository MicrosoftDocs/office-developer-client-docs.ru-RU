---
title: Метод Append (коллекция Columns в ADOX)
TOCTitle: Append method (ADOX Columns)
ms:assetid: e256a478-abc0-f15b-fc29-1b52e354144a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250152(v=office.15)
ms:contentKeyID: 48548285
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: aa7042f34f4b125c9cd34d31baae538ea3637801
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928539"
---
# <a name="append-method-adox-columns"></a>Метод Append (коллекция Columns в ADOX)


**Применимо к**: Access 2013, Office 2013

Добавляет новый объект [столбца](column-object-adox.md) в коллекцию [столбцов](columns-collection-adox.md) .

## <a name="syntax"></a>Синтаксис

*Столбцы*. Добавление*столбца* \[,*Тип* \] \[,*DefinedSize*\]

## <a name="parameters"></a>Параметры

  - *Столбец*

  - Объект для добавления **столбца** или имя столбца для создания и добавления.

  - *Тип*

  - Необязательно указывать. Значение типа **Long** , определяющее тип данных столбца. Параметр *типа* соответствует свойство [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) объекта **столбца** .

  - *DefinedSize*

  - Необязательно указывать. Значение типа **Long** , определяет размер столбца. Параметр *DefinedSize* соответствует свойству [DefinedSize](definedsize-property-adox.md) объекта **столбца** .


> [!NOTE]
> После добавления **столбцов** в коллекцию **столбцов** [индекса](index-object-adox.md) , если **Столбец** не существует в [таблице](table-object-adox.md) , уже добавлен в коллекцию [таблиц](tables-collection-adox.md) , произойдет ошибка.


