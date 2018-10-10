---
title: DBEngine.DefaultType Property (DAO)
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
ms.openlocfilehash: d32c0860f76aeeaa64a060a55579d05c1eb571ab
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481743"
---
# <a name="dbenginedefaulttype-property-dao"></a>DBEngine.DefaultType Property (DAO)


**Применимо к**: Access 2013 | Office 2013

Задает или возвращает значение, указывающее, какой тип рабочей области будет использоваться далее созданный объект **[рабочей области](workspace-object-dao.md)** .

## <a name="syntax"></a>Синтаксис

*выражение* . DefaultType

*выражение* Переменная, которая представляет собой объект- **DBEngine** .

## <a name="remarks"></a>Замечания

Параметр или возвращаемое значение может быть одним из **[WorkspaceTypeEnum](workspacetypeenum-enumeration-dao.md)** констант.


> [!NOTE]
> <P>Рабочие области технология ODBCDirect не поддерживаются в Microsoft Access 2013. Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.</P>



Параметр может быть переопределен для одной **рабочей области** путем установки для параметра метода **[CreateWorkspace](dbengine-createworkspace-method-dao.md)** аргумент типа.

