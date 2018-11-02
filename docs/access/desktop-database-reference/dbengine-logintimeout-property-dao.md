---
title: Свойство DBEngine.LoginTimeout (DAO)
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
ms.openlocfilehash: 91669b054cf9075375c4a5457086adc45ba43c70
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925907"
---
# <a name="dbenginelogintimeout-property-dao"></a>Свойство DBEngine.LoginTimeout (DAO)


**Применимо к**: Access 2013, Office 2013

Задает или возвращает число секунд, прежде чем возникает ошибка при попытке выполнить вход в базе данных ODBC.

## <a name="syntax"></a>Синтаксис

*выражение* . LoginTimeout

*выражение* Переменная, которая представляет собой объект- **DBEngine** .

## <a name="remarks"></a>Примечания

Свойство **LoginTimeout** по умолчанию установлено 20 секунд. Если свойство **LoginTimeout** имеет значение 0, происходит нет времени ожидания.

Когда вы при входе в систему в базе данных ODBC, например Microsoft SQL Server может возникнуть сбой подключения из-за ошибки сети, или сервер не будет запущен. Без необходимости по умолчанию 20 секунд для подключения, можно указать время до возникновения ошибки. Вход в систему на сервере происходит неявно, как часть из нескольких разных события, такие как выполнение запроса базы данных внешнего сервера.

