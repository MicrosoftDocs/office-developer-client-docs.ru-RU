---
title: Свойство Parameters.Count (DAO)
TOCTitle: Count Property
ms:assetid: bc8c814b-da55-22b7-431f-a0f7e6cac994
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822720(v=office.15)
ms:contentKeyID: 48547415
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 536e058a0485479cabd1cc2a0aae09f2396bfbcc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287876"
---
# <a name="parameterscount-property-dao"></a>Свойство Parameters.Count (DAO)


**Область применения**: Access 2013, Office 2013

Возвращает количество объектов в указанной коллекции. Только для чтения.

## <a name="syntax"></a>Синтаксис

*выражения* . Count

*выражение* Переменная, представляюная **объект Параметры.**

## <a name="remarks"></a>Примечания

Так как члены коллекции начинаются с 0, всегда следует использовать циклы кода, начиная с участника 0 и заканчивая значением свойства **Count** минус 1. Если вы хотите пройти цикл через членов коллекции без проверки свойства **Count,** вы можете использовать **для каждого... Следующая** команда.

Параметр **свойства Count** никогда не является Null. Если его значение 0, в коллекции нет объектов.

