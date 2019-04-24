---
title: Свойство Documents. Count (DAO)
TOCTitle: Count Property
ms:assetid: 3fc0b1e6-f7be-cd43-711f-5cf5763fe7f6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192858(v=office.15)
ms:contentKeyID: 48544407
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053325
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: dd9cc563ecc885fca4fa0ef5829d82aa2f8bfef6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293744"
---
# <a name="documentscount-property-dao"></a>Свойство Documents. Count (DAO)


**Область применения**: Access 2013, Office 2013

Возвращает число объектов в указанной коллекции. Только для чтения.

## <a name="syntax"></a>Синтаксис

*Expression* . Отсчет

*Expression (выражение* ) Переменная, представляющая объект **Documents** .

## <a name="remarks"></a>Замечания

Так как члены коллекции начинаются с 0, всегда следует всегда кодировать циклы, начиная с элемента 0 и заканчивая значением свойства **Count** минус 1. Если требуется перебрать элементы коллекции, не проверяя свойство **Count** , можно использовать оператор **For Each... Следующая** команда.

Значение свойства **Count** не может быть равно null. Если его значение равно 0, в коллекции отсутствуют объекты.

