---
title: Метод Append (коллекция Indexes в ADOX)
TOCTitle: Append method (ADOX Indexes)
ms:assetid: 015ebab4-5e9d-8777-ac82-4d20e957c274
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248784(v=office.15)
ms:contentKeyID: 48542933
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 00a02e74bbbc1b24939784a89965bf0757be0cfe
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949406"
---
# <a name="append-method-adox-indexes"></a>Метод Append (коллекция Indexes в ADOX)


**Применимо к**: Access 2013, Office 2013



Добавляет новый объект [индекса](index-object-adox.md) в коллекцию [индексов](indexes-collection-adox.md) .

## <a name="syntax"></a>Синтаксис

*Индексы*. Добавление*индекса* \[,*столбцы*\]

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*Индекс* |Объект **индекса** для добавления или имя индекса для создания и добавления.|
|*Столбцы* |Необязательно указывать. Значение **типа Variant** , который указывает имена столбцов для индексации. Параметр *столбцы* соответствует значения свойства [Name](name-property-adox.md) [столбца](column-object-adox.md) объект или объекты.|

## <a name="remarks"></a>Примечания

Для *столбцов* параметра можно задать имя столбца, либо массив имена столбцов.

Если поставщик не поддерживает создание индексов, произойдет ошибка.

