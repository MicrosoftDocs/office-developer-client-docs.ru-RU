---
title: Свойство Workspace.LoginTimeout (DAO)
TOCTitle: LoginTimeout Property
ms:assetid: 5f03b166-abbc-20de-1a01-3869a9f2907d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194743(v=office.15)
ms:contentKeyID: 48545151
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: dbc0ed4849e8c22bc7023bd4254fdee74a5d016c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306911"
---
# <a name="workspacelogintimeout-property-dao"></a>Свойство Workspace.LoginTimeout (DAO)


**Область применения**: Access 2013, Office 2013

Задает или возвращает количество секунд до возникновения ошибки при попытке войти в базу данных ODBC.

## <a name="syntax"></a>Синтаксис

*выражения* . LoginTimeout

*expression*: переменная, представляющая объект **Workspace**.

## <a name="remarks"></a>Примечания

Параметр **свойства LoginTimeout по** умолчанию — 20 секунд. Когда свойство **LoginTimeout** установлено на 0, время не происходит.

При попытке входа в базу данных ODBC, например Microsoft SQL Server, подключение может привести к сбойу из-за сетевых ошибок или из-за того, что сервер не запущен. Вместо того, чтобы ждать подключения по умолчанию 20 секунд, можно указать, как долго ждать, прежде чем поднимать ошибку. Вход на сервер происходит неявно в рамках ряда различных событий, таких как запуск запроса в базе данных внешнего сервера.

