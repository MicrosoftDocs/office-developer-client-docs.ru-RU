---
title: Свойство Databases.Count (DAO)
TOCTitle: Count Property
ms:assetid: 7c542b17-9806-e00e-8cbd-58d6d17e98c4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196364(v=office.15)
ms:contentKeyID: 48545831
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dbdaad343e1c149ea1f30b5c2d360cbd7bd6f1d8
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927650"
---
# <a name="databasescount-property-dao"></a>Свойство Databases.Count (DAO)


**Применимо к**: Access 2013, Office 2013

Возвращает число объектов в указанном семействе сайтов. Только для чтения.

## <a name="syntax"></a>Синтаксис

*выражение* . Count

*выражение* Переменная, которая представляет собой объект- **баз данных** .

## <a name="remarks"></a>Примечания

Так как члены коллекции начинаются с 0, должны всегда кода циклов, начиная с элемента 0 и заканчивая значение свойства **Count** минус 1. Если вы хотите выполняют цикл по элементам коллекции без проверки свойство **Count** , можно использовать **For Each... Далее** команды.

Значение свойства **Count** никогда не имеет значение Null. Если значение равно 0, нет объектов в коллекции.

