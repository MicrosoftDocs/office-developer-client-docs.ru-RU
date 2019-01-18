---
title: Свойство Item (ADO)
TOCTitle: Item property (ADO)
ms:assetid: 793c305f-0e5b-a529-e21f-b7ab0843ed49
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249499(v=office.15)
ms:contentKeyID: 48545767
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9cc38101cb17c52bf2c8c08c08c14163c3772b2f
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718562"
---
# <a name="item-property-ado"></a>Свойство Item (ADO)

**Применимо к**: Access 2013, Office 2013

Указывает конкретный элемент из коллекции по имени или номеру порядковый номер.

## <a name="syntax"></a>Синтаксис

Установить для*объекта* = *семейства сайтов*. Элемент (индекс)

## <a name="return-value"></a>Возвращаемое значение

Возвращает ссылку на объект.

## <a name="parameters"></a>Parameters

|Параметр|Описание|
|:--------|:----------|
|*Index* |Выражение **типа Variant** , которое оценивается как имя или порядковый номер объект в коллекцию.|

## <a name="remarks"></a>Замечания

Используйте свойство **Item** для получения определенного объекта в коллекции. Если **элемент** не удается найти объект в коллекции, соответствующий аргумент *Index* , возникает ошибка. Кроме того некоторые коллекции не поддерживают именованные объекты; для этих семейств сайтов необходимо использовать ссылки на порядковый номер.

Свойство **Item** является свойством по умолчанию для всех семейств сайтов; Таким образом следующей формы синтаксиса являются взаимозаменяемыми.

```vb
    collection.Item (Index)
    collection (Index)
```
