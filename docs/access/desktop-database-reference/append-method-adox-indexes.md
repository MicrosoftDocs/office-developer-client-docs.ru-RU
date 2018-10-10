---
title: Append Method (ADOX Indexes)
TOCTitle: Append Method (ADOX Indexes)
ms:assetid: 015ebab4-5e9d-8777-ac82-4d20e957c274
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248784(v=office.15)
ms:contentKeyID: 48542933
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5f91535075c2782861dc409a6c527f159cd5458a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480581"
---
# <a name="append-method-adox-indexes"></a>Append Method (ADOX Indexes)


**Применимо к**: Access 2013 | Office 2013



Добавляет новый объект [индекса](index-object-adox.md) в коллекцию [индексов](indexes-collection-adox.md) .

## <a name="syntax"></a>Синтаксис

*Индексы*. Добавление*индекса* \[,*столбцы*\]

## <a name="parameters"></a>Параметры

  - *Индекс*

  - Объект **индекса** для добавления или имя индекса для создания и добавления.

  - *Столбцы*

  - Необязательный параметр. Значение **типа Variant** , который указывает имена столбцов для индексации. Параметр *столбцы* соответствует значения свойства [Name](name-property-adox.md) [столбца](column-object-adox.md) объект или объекты.

## <a name="remarks"></a>Замечания

Для *столбцов* параметра можно задать имя столбца, либо массив имена столбцов.

Если поставщик не поддерживает создание индексов, произойдет ошибка.

