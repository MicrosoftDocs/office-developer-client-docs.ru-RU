---
title: Объект подключения (DAO)
TOCTitle: Connection Object
ms:assetid: f469b04e-2539-6b53-31f2-85fe22fcc2fc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836694(v=office.15)
ms:contentKeyID: 48548690
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 73ede9cae5246db3d802125b0f7c4e6df5347930
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295865"
---
# <a name="connection-object-dao"></a>Объект подключения (DAO)

**Область применения**: Access 2013, Office 2013

> [!NOTE]
> Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013. Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.

Объект **Connection** представляет подключение к базе данных ODBC (только в рабочей области ODBCDirect).

## <a name="remarks"></a>Примечания

Подключение **—** это объект, который представляет собой подключение к удаленной базе данных. Объект **Connection** доступен только в рабочей области ODBCDirect (то есть объект **Workspace,** созданный с параметром типа **dbUseODBC).**

> [!NOTE]
> Код, написанный для более ранних версий DAO, может продолжать использовать объект **Database** для обратной совместимости, но при желании новых функций подключения следует пересмотреть код для использования объекта **Подключения.**  Чтобы помочь с преобразованием кода, вы можете  получить ссылку на объект **Подключения** из базы данных, прочитав свойство [Подключение](database-connection-property-dao.md) объекта **Database.** И наоборот, вы можете получить ссылку на объект **Базы** данных из свойства **Базы** данных объекта **Подключения.**


