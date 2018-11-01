---
title: DBEngine.LoginTimeout Property (DAO)
TOCTitle: LoginTimeout Property
ms:assetid: 81d14153-79c5-7860-b6a8-4079d2d7acf7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196648(v=office.15)
ms:contentKeyID: 48545964
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052923
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 8c6b7798419dc72dc28822741e2d038203ae257e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880721"
---
# <a name="dbenginelogintimeout-property-dao"></a>DBEngine.LoginTimeout Property (DAO)


**Применимо к**: Access 2013, Office 2013

Задает или возвращает число секунд, прежде чем возникает ошибка при попытке выполнить вход в базе данных ODBC.

## <a name="syntax"></a>Синтаксис

*выражение* . LoginTimeout

*выражение* Переменная, которая представляет собой объект- **DBEngine** .

## <a name="remarks"></a>Замечания

Свойство **LoginTimeout** по умолчанию установлено 20 секунд. Если свойство **LoginTimeout** имеет значение 0, происходит нет времени ожидания.

Когда вы при входе в систему в базе данных ODBC, например Microsoft SQL Server может возникнуть сбой подключения из-за ошибки сети, или сервер не будет запущен. Без необходимости по умолчанию 20 секунд для подключения, можно указать время до возникновения ошибки. Вход в систему на сервере происходит неявно, как часть из нескольких разных события, такие как выполнение запроса базы данных внешнего сервера.

