---
title: Свойство DBEngine.IniPath (DAO)
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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717631"
---
# <a name="dbengineinipath-property-dao"></a>Свойство DBEngine.IniPath (DAO)


**Применимо к**: Access 2013, Office 2013

Задает или возвращает сведения о раздел реестра Windows, который содержит значения для ядро базы данных Microsoft Access (только для рабочих областей Microsoft Access).

## <a name="syntax"></a>Синтаксис

*выражение* . IniPath

*выражение* Переменная, которая представляет собой объект- **DBEngine** .

## <a name="remarks"></a>Замечания

Ядро базы данных Microsoft Access можно настроить с помощью реестра Windows. Реестра можно использовать для установки параметров, таких как устанавливаемый драйвер ISAM библиотек DLL.

Для этого параметра не влияет на необходимо задать свойство **IniPath** перед приложение вызывает другой код DAO. Область этот параметр не может превышать приложения и не могут быть изменены без перезапуска приложения.

Можно также с помощью реестра предоставляют параметры инициализации для некоторых устанавливаемый драйвер ISAM драйверов базы данных. Например для использования Paradox версии 4.0, присвойте свойству **IniPath** часть реестра с соответствующими параметрами.

Это свойство определяет либо HKEY\_ЛОКАЛЬНОГО\_компьютера или HKEY\_ЛОКАЛЬНОГО\_пользователя. Если ключ не корневые предоставлен, значение по умолчанию — HKEY\_ЛОКАЛЬНОГО\_компьютера.

