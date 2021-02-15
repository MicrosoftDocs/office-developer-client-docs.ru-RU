---
title: Свойство TableDefs.Count (DAO)
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
# <a name="tabledefscount-property-dao"></a>Свойство TableDefs.Count (DAO)


**Область применения**: Access 2013, Office 2013

Возвращает количество объектов в указанной коллекции. Только для чтения.

## <a name="syntax"></a>Синтаксис

*выражение .* Count

*выражение* Переменная, представляюная объект **TableDefs.**

## <a name="remarks"></a>Заметки

Так как члены коллекции начинаются с 0, всегда следует кодировать циклы, начиная с 0 и заканчивая значением свойства **Count** минус 1. Если вы хотите обоймить члены коллекции, не проверяя свойство **Count,** можно использовать объект **For Each... Следующая** команда.

Параметр **свойства Count** никогда не имеет NULL. Если его значение 0, в коллекции нет объектов.

