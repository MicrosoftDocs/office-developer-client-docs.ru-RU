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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297125"
---
# <a name="append-method-adox-columns"></a>Метод Append (коллекция Columns в ADOX)

**Область применения**: Access 2013, Office 2013

Добавляет новый [объект Column](column-object-adox.md) в коллекцию [Columns.](columns-collection-adox.md)

## <a name="syntax"></a>Синтаксис

*Столбцы*. Append *Column,* \[ *Type* , \] \[ *DefinedSize*\]

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*Столбец* |Объект **Column,** который необходимо к приложению, или имя столбца, который необходимо создать и к приложению.|
|*Тип* |Необязательный параметр. **Длинное** значение, которое указывает тип данных столбца. Параметр *Type* соответствует свойству [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) объекта **Column.**|
|*DefinedSize* |Необязательный параметр. **Длинное** значение, которое указывает размер столбца. Параметр *DefinedSize соответствует* свойству [DefinedSize](definedsize-property-adox.md) объекта **Column.**|


> [!NOTE]
> Ошибка будет возникать при  приложении столбца к [](index-object-adox.md) коллекции **Columns** индекса, [](table-object-adox.md) если столбец не существует в таблице, которая уже была сдана в коллекцию [Tables.](tables-collection-adox.md) 


