---
title: DBEngine.IniПути (DAO)
TOCTitle: IniPath Property
ms:assetid: b18cace5-4e53-d011-6373-f4ac64556fd4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822009(v=office.15)
ms:contentKeyID: 48547151
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053070
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: f14f9f2d028bb8a9a8e71bc9d7b97ea5672466f1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294297"
---
# <a name="dbengineinipath-property-dao"></a>DBEngine.IniПути (DAO)


**Область применения**: Access 2013, Office 2013

Задает или возвращает сведения о ключе Windows реестра, который содержит значения для двигателя базы данных Microsoft Access (только в рабочей области Microsoft Access).

## <a name="syntax"></a>Синтаксис

*выражения* . IniPath

*expression*: переменная, представляющая объект **DBEngine**.

## <a name="remarks"></a>Примечания

Вы можете настроить движок базы данных Microsoft Access с помощью Windows реестра. Вы можете использовать реестр для установки параметров, таких как устанавливаемые DLLs ISAM.

Чтобы этот параметр мог иметь какой-либо эффект, необходимо установить свойство **IniPath,** прежде чем приложение вызывает любой другой код DAO. Область этого параметра ограничена вашим приложением и не может быть изменена без перезапуска приложения.

Вы также используете Реестр для предоставления параметров инициализации для некоторых установимых драйверов баз данных ISAM. Например, чтобы использовать версию Paradox 4.0, установите свойство **IniPath** в часть реестра, содержащую соответствующие параметры.

Это свойство распознает локального пользователя HKEY \_ \_ или локального пользователя HKEY. \_ \_ Если корневой ключ не поставляется, по умолчанию является локальной машиной \_ \_ HKEY.

