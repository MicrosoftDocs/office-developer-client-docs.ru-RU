---
title: Workspace.LoginTimeout Property (DAO)
TOCTitle: LoginTimeout Property
ms:assetid: 5f03b166-abbc-20de-1a01-3869a9f2907d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194743(v=office.15)
ms:contentKeyID: 48545151
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6427b99fd212fa358b70fb20a5ecf0c9180209fb
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479816"
---
# <a name="workspacelogintimeout-property-dao"></a>Workspace.LoginTimeout Property (DAO)


**Применимо к**: Access 2013 | Office 2013

Задает или возвращает число секунд, прежде чем возникает ошибка при попытке выполнить вход в базе данных ODBC.

## <a name="syntax"></a>Синтаксис

*выражение* . LoginTimeout

*выражение* Переменная, которая представляет собой объект- **рабочей области** .

## <a name="remarks"></a>Замечания

Свойство **LoginTimeout** по умолчанию установлено 20 секунд. Если свойство **LoginTimeout** имеет значение 0, происходит нет времени ожидания.

Когда вы при входе в систему в базе данных ODBC, например Microsoft SQL Server может возникнуть сбой подключения из-за ошибки сети, или сервер не будет запущен. Без необходимости по умолчанию 20 секунд для подключения, можно указать время до возникновения ошибки. Вход в систему на сервере происходит неявно, как часть из нескольких разных события, такие как выполнение запроса базы данных внешнего сервера.
