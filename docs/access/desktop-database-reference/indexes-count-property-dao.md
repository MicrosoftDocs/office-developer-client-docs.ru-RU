---
title: Свойство Indexes.Count (DAO)
TOCTitle: Count Property
ms:assetid: 195ede10-f91e-50c6-6af4-b318c476b9ea
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845647(v=office.15)
ms:contentKeyID: 48543499
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cffbf14e73e97113194eb25b8e0d5799d3578086
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291547"
---
# <a name="indexescount-property-dao"></a>Свойство Indexes.Count (DAO)


**Область применения**: Access 2013, Office 2013

Возвращает количество объектов в указанной коллекции. Только для чтения.

## <a name="syntax"></a>Синтаксис

*выражение .* Count

*выражение* Переменная, представляюная объект **Indexes.**

## <a name="remarks"></a>Заметки

Так как члены коллекции начинаются с 0, всегда следует кодировать циклы, начиная с 0 и заканчивая значением свойства **Count** минус 1. Если вы хотите обоймить члены коллекции, не проверяя свойство **Count,** можно использовать объект **For Each... Следующая** команда.

Параметр **свойства Count** никогда не имеет NULL. Если его значение 0, в коллекции нет объектов.

