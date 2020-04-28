---
title: Свойство databases. Count (DAO)
TOCTitle: Count Property
ms:assetid: 7c542b17-9806-e00e-8cbd-58d6d17e98c4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196364(v=office.15)
ms:contentKeyID: 48545831
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cd8908492721315202c5bdf26109753c88905a07
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294626"
---
# <a name="databasescount-property-dao"></a>Свойство databases. Count (DAO)


**Область применения**: Access 2013, Office 2013

Возвращает число объектов в указанной коллекции. Только для чтения.

## <a name="syntax"></a>Синтаксис

*Expression* . Отсчет

*Expression (выражение* ) Переменная, представляющая объект **databases** .

## <a name="remarks"></a>Примечания

Так как члены коллекции начинаются с 0, всегда следует всегда кодировать циклы, начиная с элемента 0 и заканчивая значением свойства **Count** минус 1. Если требуется перебрать элементы коллекции, не проверяя свойство **Count** , можно использовать оператор **For Each... Следующая** команда.

Значение свойства **Count** не может быть равно null. Если его значение равно 0, в коллекции отсутствуют объекты.

