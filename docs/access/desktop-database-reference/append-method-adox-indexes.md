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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707558"
---
# <a name="append-method-adox-indexes"></a>Метод Append (коллекция Indexes в ADOX)


**Применимо к**: Access 2013, Office 2013



Добавляет новый объект [индекса](index-object-adox.md) в коллекцию [индексов](indexes-collection-adox.md) .

## <a name="syntax"></a>Синтаксис

*Индексы*. Добавление*индекса* \[,*столбцы*\]

## <a name="parameters"></a>Parameters

|Параметр|Описание|
|:--------|:----------|
|*Index* |Объект **индекса** для добавления или имя индекса для создания и добавления.|
|*Columns* |Необязательно. Значение **типа Variant** , который указывает имена столбцов для индексации. Параметр *столбцы* соответствует значения свойства [Name](name-property-adox.md) [столбца](column-object-adox.md) объект или объекты.|

## <a name="remarks"></a>Замечания

Для *столбцов* параметра можно задать имя столбца, либо массив имена столбцов.

Если поставщик не поддерживает создание индексов, произойдет ошибка.

