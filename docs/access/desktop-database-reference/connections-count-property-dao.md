---
title: Свойство Connections.Count (DAO)
TOCTitle: Count Property
ms:assetid: 9b2f0aaa-785a-7fe7-15c3-aea37fdacd12
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198023(v=office.15)
ms:contentKeyID: 48546563
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a286bf992116dc4ddfa71a9be8231e70b717aaa3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295760"
---
# <a name="connectionscount-property-dao"></a>Свойство Connections.Count (DAO)


**Область применения**: Access 2013, Office 2013

Возвращает количество объектов **[Подключения](connection-object-dao.md)** в коллекции **[Connections.](connections-collection-dao.md)**

## <a name="syntax"></a>Синтаксис

*выражения* . Count

*выражение* Переменная, представляюная объект **Connections.**

## <a name="remarks"></a>Примечания

Так как члены коллекции начинаются с 0, всегда следует использовать циклы кода, начиная с участника 0 и заканчивая значением свойства **Count** минус 1. Если вы хотите пройти цикл через членов коллекции без проверки свойства **Count,** вы можете использовать **для каждого... Следующая** команда.

Параметр **свойства Count** никогда не является Null. Если его значение 0, в коллекции нет объектов.

