---
title: DBEngine.IniPath Property (DAO)
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
ms.openlocfilehash: 1bb594ad9866785db3d12f114f6be0eccbbe2289
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481301"
---
# <a name="dbengineinipath-property-dao"></a>DBEngine.IniPath Property (DAO)


**Применимо к**: Access 2013 | Office 2013

Задает или возвращает сведения о раздел реестра Windows, который содержит значения для ядро базы данных Microsoft Access (только для рабочих областей Microsoft Access).

## <a name="syntax"></a>Синтаксис

*выражение* . IniPath

*выражение* Переменная, которая представляет собой объект- **DBEngine** .

## <a name="remarks"></a>Замечания

Ядро базы данных Microsoft Access можно настроить с помощью реестра Windows. Реестра можно использовать для установки параметров, таких как устанавливаемый драйвер ISAM библиотек DLL.

Для этого параметра не влияет на необходимо задать свойство **IniPath** перед приложение вызывает другой код DAO. Область этот параметр не может превышать приложения и не могут быть изменены без перезапуска приложения.

Можно также с помощью реестра предоставляют параметры инициализации для некоторых устанавливаемый драйвер ISAM драйверов базы данных. Например для использования Paradox версии 4.0, присвойте свойству **IniPath** часть реестра с соответствующими параметрами.

Это свойство определяет либо HKEY\_ЛОКАЛЬНОГО\_компьютера или HKEY\_ЛОКАЛЬНОГО\_пользователя. Если ключ не корневые предоставлен, значение по умолчанию — HKEY\_ЛОКАЛЬНОГО\_компьютера.

