---
title: Item Property (ADO)
TOCTitle: Item Property (ADO)
ms:assetid: 793c305f-0e5b-a529-e21f-b7ab0843ed49
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249499(v=office.15)
ms:contentKeyID: 48545767
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 29453ac2801f606640fd6d9506a8ee1ee8625396
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480044"
---
# <a name="item-property-ado"></a>Item Property (ADO)

**Применимо к**: Access 2013 | Office 2013

Указывает конкретный элемент из коллекции по имени или номеру порядковый номер.

## <a name="syntax"></a>Синтаксис

Установить для*объекта* = *семейства сайтов*. Элемент (индекс)

## <a name="return-value"></a>Возвращаемое значение

Возвращает ссылку на объект.

## <a name="parameters"></a>Параметры

- *Индекс*

- Выражение **типа Variant** , которое оценивается как имя или порядковый номер объект в коллекцию.

## <a name="remarks"></a>Замечания

Используйте свойство **Item** для получения определенного объекта в коллекции. Если **элемент** не удается найти объект в коллекции, соответствующий аргумент *Index* , возникает ошибка. Кроме того некоторые коллекции не поддерживают именованные объекты; для этих семейств сайтов необходимо использовать ссылки на порядковый номер.

Свойство **Item** является свойством по умолчанию для всех семейств сайтов; Таким образом следующей формы синтаксиса являются взаимозаменяемыми.

```vb
    collection.Item (Index)
    collection (Index)
```
