---
title: Свойство QueryDefs.Count (DAO)
TOCTitle: Count Property
ms:assetid: 8caa01c5-692f-95e4-4b11-6e6c591f5872
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197340(v=office.15)
ms:contentKeyID: 48546240
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 95624c82ee9ab322eec5455759cf4ec2e9708dba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300961"
---
# <a name="querydefscount-property-dao"></a>Свойство QueryDefs.Count (DAO)


**Область применения**: Access 2013, Office 2013

Возвращает количество объектов в указанной коллекции. Только для чтения.

## <a name="syntax"></a>Синтаксис

*выражение .* Count

*выражение* Переменная, представляюная объект **QueryDefs.**

## <a name="remarks"></a>Заметки

Так как члены коллекции начинаются с 0, всегда следует кодировать циклы, начиная с 0 и заканчивая значением свойства **Count** минус 1. Если вы хотите обоймить члены коллекции, не проверяя свойство **Count,** можно использовать объект **For Each... Следующая** команда.

Параметр **свойства Count** никогда не имеет NULL. Если его значение 0, в коллекции нет объектов.

