---
title: Свойство QueryDefs.Count (DAO)
TOCTitle: Count Property
ms:assetid: 8caa01c5-692f-95e4-4b11-6e6c591f5872
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197340(v=office.15)
ms:contentKeyID: 48546240
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f5efc7479f69d379f406a9a7cda5d4c522df6325
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25930898"
---
# <a name="querydefscount-property-dao"></a>Свойство QueryDefs.Count (DAO)


**Применимо к**: Access 2013, Office 2013

Возвращает число объектов в указанном семействе сайтов. Только для чтения.

## <a name="syntax"></a>Синтаксис

*выражение* . Count

*выражение* Переменная, которая представляет собой объект- **QueryDefs** .

## <a name="remarks"></a>Примечания

Так как члены коллекции начинаются с 0, должны всегда кода циклов, начиная с элемента 0 и заканчивая значение свойства **Count** минус 1. Если вы хотите выполняют цикл по элементам коллекции без проверки свойство **Count** , можно использовать **For Each... Далее** команды.

Значение свойства **Count** никогда не имеет значение Null. Если значение равно 0, нет объектов в коллекции.

