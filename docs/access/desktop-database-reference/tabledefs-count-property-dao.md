---
title: Свойство TableDefs. Count (DAO)
TOCTitle: Count Property
ms:assetid: 6e2cf3e5-524f-a643-b1dc-99a4b2bb2e63
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195561(v=office.15)
ms:contentKeyID: 48545508
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6c997a437cc7a7ae1461e7308899c85dac44fbda
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314268"
---
# <a name="tabledefscount-property-dao"></a>Свойство TableDefs. Count (DAO)


**Область применения**: Access 2013, Office 2013

Возвращает число объектов в указанной коллекции. Только для чтения.

## <a name="syntax"></a>Синтаксис

*Expression* . Отсчет

*Expression (выражение* ) Переменная, представляющая объект **TableDefs** .

## <a name="remarks"></a>Примечания

Так как члены коллекции начинаются с 0, всегда следует всегда кодировать циклы, начиная с элемента 0 и заканчивая значением свойства **Count** минус 1. Если требуется перебрать элементы коллекции, не проверяя свойство **Count** , можно использовать оператор **For Each... Следующая** команда.

Значение свойства **Count** не может быть равно null. Если его значение равно 0, в коллекции отсутствуют объекты.

