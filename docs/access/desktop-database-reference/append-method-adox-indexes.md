---
title: Метод Append (коллекция Indexes в ADOX)
TOCTitle: Append method (ADOX Indexes)
ms:assetid: 015ebab4-5e9d-8777-ac82-4d20e957c274
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248784(v=office.15)
ms:contentKeyID: 48542933
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 41eb1cc67dd5a2058f9c5673db381f0bc9067454
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921483"
---
# <a name="append-method-adox-indexes"></a>Метод Append (коллекция Indexes в ADOX)


**Применимо к**: Access 2013, Office 2013



Добавляет новый объект [индекса](index-object-adox.md) в коллекцию [индексов](indexes-collection-adox.md) .

## <a name="syntax"></a>Синтаксис

*Индексы*. Добавление*индекса* \[,*столбцы*\]

## <a name="parameters"></a>Параметры

  - *Индекс*

  - Объект **индекса** для добавления или имя индекса для создания и добавления.

  - *Столбцы*

  - Необязательно указывать. Значение **типа Variant** , который указывает имена столбцов для индексации. Параметр *столбцы* соответствует значения свойства [Name](name-property-adox.md) [столбца](column-object-adox.md) объект или объекты.

## <a name="remarks"></a>Примечания

Для *столбцов* параметра можно задать имя столбца, либо массив имена столбцов.

Если поставщик не поддерживает создание индексов, произойдет ошибка.

