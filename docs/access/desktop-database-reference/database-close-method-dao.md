---
title: Метод Database.Close (DAO)
TOCTitle: Close Method
ms:assetid: b777ee92-172a-3342-31fc-76e7361c47fd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822418(v=office.15)
ms:contentKeyID: 48547296
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 190b47b59bd9781553912f91156c74a3fd09c2d5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295025"
---
# <a name="databaseclose-method-dao"></a>Метод Database.Close (DAO)


**Область применения**: Access 2013, Office 2013

Закрывает открытую **базу данных.**

## <a name="syntax"></a>Синтаксис

*выражение*.Close

*выражение*: переменная, представляющая объект **Database**.

## <a name="remarks"></a>Примечания

Если объект **Database** уже закрыт при использовании **Close,** возникает ошибка времени запуска.

Альтернатива методу **Close** заключается в присвоении объектной переменной значения **Nothing** (Set dbsTemp = Nothing).

