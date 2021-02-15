---
title: Метод Append (коллекция Indexes в ADOX)
TOCTitle: Append method (ADOX Indexes)
ms:assetid: 015ebab4-5e9d-8777-ac82-4d20e957c274
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248784(v=office.15)
ms:contentKeyID: 48542933
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0b541512de9748e94d033bb56f27dd0941c7f5a7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297097"
---
# <a name="append-method-adox-indexes"></a>Метод Append (коллекция Indexes в ADOX)


**Область применения**: Access 2013, Office 2013



Добавляет новый [объект Index](index-object-adox.md) в [коллекцию Indexes.](indexes-collection-adox.md)

## <a name="syntax"></a>Синтаксис

*Индексы.* Append *Index* \[ ,*Columns*\]

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*Индекс* |Объект **Index,** который необходимо к приложению, или имя индекса, который необходимо создать и к приложению.|
|*Columns* |Необязательный параметр. Значение **Variant,** которое указывает имена столбцов для индексации. Параметр *Columns* соответствует значениям свойства [Name](name-property-adox.md) объекта или объектов [Column.](column-object-adox.md)|

## <a name="remarks"></a>Заметки

Параметр *Columns* может принимать имя столбца или массив имен столбцов.

Если поставщик не поддерживает создание индексов, произойдет ошибка.

