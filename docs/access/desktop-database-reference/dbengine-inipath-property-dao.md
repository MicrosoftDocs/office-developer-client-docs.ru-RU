---
title: Свойство DBEngine. IniPath (DAO)
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
# <a name="dbengineinipath-property-dao"></a>Свойство DBEngine. IniPath (DAO)


**Область применения**: Access 2013, Office 2013

Задает или возвращает сведения о разделе реестра Windows, который содержит значения для ядра СУБД Microsoft Access (только для рабочих областей Microsoft Access).

## <a name="syntax"></a>Синтаксис

*Expression* . IniPath

*Expression (выражение* ) Переменная, представляющая объект **DBEngine** .

## <a name="remarks"></a>Замечания

Вы можете настроить ядро СУБД Microsoft Access с помощью реестра Windows. Вы можете использовать реестр для установки параметров, таких как устанавливаемые библиотеки ISAM DLL.

Чтобы этот параметр действовал, необходимо задать свойство **IniPath** , прежде чем приложение вызовет любой другой код DAO. Область этого параметра ограничена приложением и не может быть изменена без перезапуска приложения.

Вы также можете использовать реестр для предоставления параметров инициализации для некоторых устанавливаемых драйверов базы данных ISAM. Например, чтобы использовать Paradox версии 4,0, присвойте свойству **IniPath** часть реестра, содержащую соответствующие параметры.

Это свойство распознает либо\_\_локальный\_пользователь, либо\_локальный пользователь hKey. Если корневой ключ не указан, по умолчанию используется\_локальный\_компьютер hKey.

