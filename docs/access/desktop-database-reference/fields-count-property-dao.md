---
title: Свойство Fields.Count (DAO)
TOCTitle: Count Property
ms:assetid: 574de1db-2640-159b-7756-28c37acc9f83
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194261(v=office.15)
ms:contentKeyID: 48544969
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 99eb21ba4f4ef13c902fc0d029dba59c30066853
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292547"
---
# <a name="fieldscount-property-dao"></a>Свойство Fields.Count (DAO)


**Область применения**: Access 2013, Office 2013

Возвращает количество объектов в указанной коллекции. Только для чтения, **Integer**.

## <a name="syntax"></a>Синтаксис

*выражение .* Count

*выражение*: переменная, представляющая объект **Fields**.

## <a name="remarks"></a>Заметки

Так как члены коллекции начинаются с 0, всегда следует кодировать циклы, начиная с 0 и заканчивая значением свойства **Count** минус 1. Если вы хотите обоймить члены коллекции, не проверяя свойство **Count,** можно использовать объект **For Each... Следующая** команда.

Параметр **свойства Count** никогда не имеет NULL. Если его значение 0, в коллекции нет объектов.

