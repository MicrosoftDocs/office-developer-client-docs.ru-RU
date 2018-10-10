---
title: Recordsets.Count Property (DAO)
TOCTitle: Count Property
ms:assetid: 4362aa16-c8e9-e517-887e-c4532bd1eef9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192940(v=office.15)
ms:contentKeyID: 48544500
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3351c1bb2099072622b7f18d7eba23674b398807
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480748"
---
# <a name="recordsetscount-property-dao"></a>Recordsets.Count Property (DAO)


**Применимо к**: Access 2013 | Office 2013

Возвращает число объектов в указанном семействе сайтов. Только для чтения **целое число**.

## <a name="syntax"></a>Синтаксис

*выражение* . Count

*выражение* Переменная, которая представляет собой объект- **наборов записей** .

## <a name="remarks"></a>Замечания

Так как члены коллекции начинаются с 0, должны всегда кода циклов, начиная с элемента 0 и заканчивая значение свойства **Count** минус 1. Если вы хотите выполняют цикл по элементам коллекции без проверки свойство **Count** , можно использовать **For Each... Далее** команды.

Значение свойства **Count** никогда не имеет значение Null. Если значение равно 0, нет объектов в коллекции.

