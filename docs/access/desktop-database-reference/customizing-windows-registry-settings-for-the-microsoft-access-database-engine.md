---
title: Настройка параметров реестра Windows для ядра СУБД Microsoft Access
TOCTitle: Customizing Windows registry settings for the Microsoft Access database engine
ms:assetid: ca7e958a-ea26-d67d-45b9-10aeb1eac96b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834346(v=office.15)
ms:contentKeyID: 48547690
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- acmain11.chm1032168
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 99e2b31cf686895a56e9d70b177314355c1aff3c
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945148"
---
# <a name="customizing-windows-registry-settings-for-the-microsoft-access-database-engine"></a>Настройка параметров реестра Windows для ядра СУБД Microsoft Access

**Применимо к**: Access 2013, Office 2013

Если приложение работает правильно с функциональными возможностями по умолчанию ядра базы данных Microsoft Access, может потребоваться изменить параметры в соответствии со своими потребностями реестра Microsoft Windows. Реестра Windows можно также использовать для настройки операции устанавливаемый драйвер ISAM и ODBC.

Можно настроить параметры реестра Windows четырьмя способами:

- [С помощью Regedit.exe для замены параметров по умолчанию](https://msdn.microsoft.com/library/ff193205\(v=office.15\))
- [Создание компонента в дереве реестра приложения для управления параметрами](https://msdn.microsoft.com/library/ff836342\(v=office.15\))
- [С помощью метода SetOption от DAO](https://msdn.microsoft.com/library/ff194471\(v=office.15\))
- [С помощью свойства подключения в поставщик Microsoft OLE DB для Access](https://msdn.microsoft.com/library/ff196356\(v=office.15\))

