---
title: Append Method (ADOX Columns)
TOCTitle: Append Method (ADOX Columns)
ms:assetid: e256a478-abc0-f15b-fc29-1b52e354144a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250152(v=office.15)
ms:contentKeyID: 48548285
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1f64f3b04df989348173ad2fc975dcefbd1114b2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480236"
---
# <a name="append-method-adox-columns"></a>Append Method (ADOX Columns)


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
> <P>После добавления <STRONG>столбцов</STRONG> в коллекцию <STRONG>столбцов</STRONG> <A href="index-object-adox.md">индекса</A> , если <STRONG>Столбец</STRONG> не существует в <A href="table-object-adox.md">таблице</A> , уже добавлен в коллекцию <A href="tables-collection-adox.md">таблиц</A> , произойдет ошибка.</P>


