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
localization_priority: Normal
ms.openlocfilehash: 7cbe8ad56e01249563f7b06c9018d923a96246e9
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707362"
---
# <a name="customizing-windows-registry-settings-for-the-microsoft-access-database-engine"></a>Настройка параметров реестра Windows для ядра СУБД Microsoft Access

**Применимо к**: Access 2013, Office 2013

Если приложение работает правильно с функциональными возможностями по умолчанию ядра базы данных Microsoft Access, может потребоваться изменить параметры в соответствии со своими потребностями реестра Microsoft Windows. Реестра Windows можно также использовать для настройки операции устанавливаемый драйвер ISAM и ODBC.

Можно настроить параметры реестра Windows четырьмя способами:

- [С помощью Regedit.exe для замены параметров по умолчанию](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/using-regedit-exe-to-overwrite-the-default-settings)
- [Создание компонента в дереве реестра приложения для управления параметрами](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/creating-a-portion-in-your-application-s-registry-tree-to-manage-the-settings)
- [С помощью метода SetOption от DAO](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/using-the-setoption-method-from-dao)
- [С помощью свойства подключения в поставщик Microsoft OLE DB для Access](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/using-the-connection-properties-in-the-microsoft-ole-db-provider-for-access)

