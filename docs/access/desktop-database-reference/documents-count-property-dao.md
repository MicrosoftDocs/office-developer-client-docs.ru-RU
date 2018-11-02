---
title: Свойство Documents.Count (DAO)
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
ms.openlocfilehash: b01ec200278095893214f10dc9e50c5266153d72
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25918935"
---
# <a name="documentscount-property-dao"></a>Свойство Documents.Count (DAO)


**Применимо к**: Access 2013, Office 2013

Возвращает число объектов в указанном семействе сайтов. Только для чтения.

## <a name="syntax"></a>Синтаксис

*выражение* . Count

*выражение* Переменная, которая представляет собой объект- **документы** .

## <a name="remarks"></a>Примечания

Так как члены коллекции начинаются с 0, должны всегда кода циклов, начиная с элемента 0 и заканчивая значение свойства **Count** минус 1. Если вы хотите выполняют цикл по элементам коллекции без проверки свойство **Count** , можно использовать **For Each... Далее** команды.

Значение свойства **Count** никогда не имеет значение Null. Если значение равно 0, нет объектов в коллекции.

