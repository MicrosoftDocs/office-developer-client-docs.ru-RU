---
title: Метод Workspace. Close (DAO)
TOCTitle: Close Method
ms:assetid: 9b3d28f9-5cde-0dd9-8a4a-d2efaec5fe5d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198027(v=office.15)
ms:contentKeyID: 48546565
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0049fb335c869a050a2c20d5740c487413c76786
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32305959"
---
# <a name="workspaceclose-method-dao"></a>Метод Workspace. Close (DAO)


**Область применения**: Access 2013, Office 2013

Закрывает открытую **рабочую область**.

## <a name="syntax"></a>Синтаксис

*выражение*.Close

*expression*: переменная, представляющая объект **Workspace**.

## <a name="remarks"></a>Примечания

Если объект **Workspace** уже закрыт при использовании **Close**, возникает ошибка времени выполнения.

Альтернатива методу **Close** заключается в присвоении объектной переменной значения **Nothing** (Set dbsTemp = Nothing).

