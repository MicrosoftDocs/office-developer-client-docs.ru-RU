---
title: Метод Append (коллекция Columns в ADOX)
TOCTitle: Append method (ADOX Columns)
ms:assetid: e256a478-abc0-f15b-fc29-1b52e354144a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250152(v=office.15)
ms:contentKeyID: 48548285
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 48bc100b7b56265a570ce963b80f569f1d827150
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711233"
---
# <a name="append-method-adox-columns"></a>Метод Append (коллекция Columns в ADOX)

**Применимо к**: Access 2013, Office 2013

Добавляет новый объект [столбца](column-object-adox.md) в коллекцию [столбцов](columns-collection-adox.md) .

## <a name="syntax"></a>Синтаксис

*Столбцы*. Добавление*столбца* \[,*Тип* \] \[,*DefinedSize*\]

## <a name="parameters"></a>Parameters

|Параметр|Описание|
|:--------|:----------|
|*Column* |Объект для добавления **столбца** или имя столбца для создания и добавления.|
|*Type* |Необязательно. Значение типа **Long** , определяющее тип данных столбца. Параметр *типа* соответствует свойство [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) объекта **столбца** .|
|*DefinedSize* |Необязательно. Значение типа **Long** , определяет размер столбца. Параметр *DefinedSize* соответствует свойству [DefinedSize](definedsize-property-adox.md) объекта **столбца** .|


> [!NOTE]
> После добавления **столбцов** в коллекцию **столбцов** [индекса](index-object-adox.md) , если **Столбец** не существует в [таблице](table-object-adox.md) , уже добавлен в коллекцию [таблиц](tables-collection-adox.md) , произойдет ошибка.


