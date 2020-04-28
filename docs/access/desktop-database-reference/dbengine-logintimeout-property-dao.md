---
title: Свойство DBEngine. LoginTimeout (DAO)
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
localization_priority: Normal
ms.openlocfilehash: e3ff893a16e650fe7eb49b647ae8d67374375a0d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294311"
---
# <a name="dbenginelogintimeout-property-dao"></a>Свойство DBEngine. LoginTimeout (DAO)


**Область применения**: Access 2013, Office 2013

Задает или возвращает число секунд до возникновения ошибки при попытке входа в базу данных ODBC.

## <a name="syntax"></a>Синтаксис

*Expression* . LoginTimeout

*expression*: переменная, представляющая объект **DBEngine**.

## <a name="remarks"></a>Примечания

Значение свойства **LoginTimeOut** по умолчанию — 20 секунд. Если для свойства **LoginTimeOut** задано значение 0, время ожидания не возникает.

При попытке войти в базу данных ODBC, например Microsoft SQL Server, подключение может завершиться неудачей из-за ошибок сети или из-за того, что сервер не запущен. Вместо того чтобы ждать подключения по умолчанию (20 секунд), можно указать время ожидания перед возникновением ошибки. Вход на сервер неявно происходит в рамках ряда различных событий, например при выполнении запроса к базе данных внешнего сервера.

