---
title: Свойство Containers.Count (DAO)
TOCTitle: Count Property
ms:assetid: 3b0bf865-a4d5-82bb-c1a9-9957f110db4c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192657(v=office.15)
ms:contentKeyID: 48544276
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7553b0e7d64e059dfeed50f158f21f48455976d7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295592"
---
# <a name="containerscount-property-dao"></a>Свойство Containers.Count (DAO)


**Область применения**: Access 2013, Office 2013

Возвращает количество объектов **[Connection](connection-object-dao.md)** в коллекции **[Connections.](connections-collection-dao.md)**

## <a name="syntax"></a>Синтаксис

*выражение* . Count

*выражение* Переменная, представляюная объект **Connections.**

## <a name="remarks"></a>Заметки

Так как члены коллекции начинаются с 0, необходимо всегда кодировать циклы, начиная с 0 и заканчивая значением свойства **Count** минус 1. Если вы хотите обоймить члены коллекции, не проверяя свойство **Count,** можно использовать объект **For Each... Следующая** команда.

Параметр **свойства Count** никогда не имеет NULL. Если его значение 0, в коллекции нет объектов.

