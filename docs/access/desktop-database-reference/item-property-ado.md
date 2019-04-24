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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32290795"
---
# <a name="item-property-ado"></a>Свойство Item (ADO)

**Область применения**: Access 2013, Office 2013

Указывает определенный элемент коллекции по имени или порядковому номеру.

## <a name="syntax"></a>Синтаксис

Задайте** = *коллекцию*объектов. Элемент (index)

## <a name="return-value"></a>Возвращаемое значение

Возвращает ссылку на объект.

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*Index* |Выражение **типа Variant** , которое оценивается как имя или порядковый номер объекта в коллекции.|

## <a name="remarks"></a>Замечания

Используйте свойство **Item** , чтобы возвратить определенный объект в коллекции. Если **элемент** не может найти объект в коллекции, соответствующем аргументу *index* , возникает ошибка. Кроме того, некоторые коллекции не поддерживают именованные объекты; для этих коллекций необходимо использовать ссылки на порядковые номера.

Свойство **Item** является свойством по умолчанию для всех коллекций; Таким образом, следующие синтаксические формы являются взаимозаменяемыми:

```vb
    collection.Item (Index)
    collection (Index)
```
