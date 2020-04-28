---
title: Свойство DBEngine. DefaultType (DAO)
TOCTitle: DefaultType Property
ms:assetid: b4371f3e-1ce0-1d0f-93a8-0c5329b510ab
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822060(v=office.15)
ms:contentKeyID: 48547217
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053580
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 23f6c87ede6da2cc5b2f3203bfa13cb17bf93e82
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294381"
---
# <a name="dbenginedefaulttype-property-dao"></a>Свойство DBEngine. DefaultType (DAO)


**Область применения**: Access 2013, Office 2013

Задает или возвращает значение, указывающее тип рабочей области, который будет использоваться при создании следующего объекта **[Workspace](workspace-object-dao.md)** .

## <a name="syntax"></a>Синтаксис

*Expression* . DefaultType

*expression*: переменная, представляющая объект **DBEngine**.

## <a name="remarks"></a>Примечания

Параметр или возвращаемое значение может быть одной из констант **[воркспацетипинум](workspacetypeenum-enumeration-dao.md)** .


> [!NOTE]
> Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013. Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.

Параметр можно переопределить для отдельной **рабочей области** , задав аргумент Type для метода **[CreateWorkspace](dbengine-createworkspace-method-dao.md)** .

