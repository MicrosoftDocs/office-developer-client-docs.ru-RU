---
title: DBEngine.IniPath (DAO)
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
# <a name="dbengineinipath-property-dao"></a>DBEngine.IniPath (DAO)


**Область применения**: Access 2013, Office 2013

Задает или возвращает сведения о ключе реестра Windows, который содержит значения для ядвижка базы данных Microsoft Access (только для рабочей области Microsoft Access).

## <a name="syntax"></a>Синтаксис

*выражение .* IniPath

*expression*: переменная, представляющая объект **DBEngine**.

## <a name="remarks"></a>Заметки

Вы можете настроить яд базы данных Microsoft Access с помощью реестра Windows. Реестр можно использовать для установки параметров, таких как устанавливаемые DLL ISAM.

Чтобы этот параметр вступил в силу, необходимо установить свойство **IniPath,** прежде чем приложение будет вызывать любой другой код DAO. Область действия этого параметра ограничена приложением и не может быть изменена без перезапуска приложения.

Реестр также используется для предоставления параметров инициализации для некоторых устанавливаемых драйверов базы данных ISAM. Например, чтобы использовать Paradox версии 4.0, установите для свойства **IniPath** часть реестра, содержащую соответствующие параметры.

Это свойство распознает HKEY \_ LOCAL \_ MACHINE или HKEY \_ LOCAL \_ USER. Если корневой ключ не задается, по умолчанию задается HKEY \_ LOCAL \_ MACHINE.

