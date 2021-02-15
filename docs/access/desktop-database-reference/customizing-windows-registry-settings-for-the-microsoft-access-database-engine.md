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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295123"
---
# <a name="customizing-windows-registry-settings-for-the-microsoft-access-database-engine"></a>Настройка параметров реестра Windows для ядра СУБД Microsoft Access

**Область применения**: Access 2013, Office 2013

Если приложение не может правильно работать с функциями якоря базы данных Microsoft Access по умолчанию, может потребоваться изменить параметры реестра Microsoft Windows в соответствии со своими потребностями. Реестр Windows также можно использовать для настройки работы устанавливаемого драйвера ISAM и ODBC.

Параметры в реестре Windows можно настроить четырьмя способами:

- [Использование Regedit.exe для переоценки параметров по умолчанию](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/using-regedit-exe-to-overwrite-the-default-settings)
- [Создание части в дереве реестра приложения для управления настройками](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/creating-a-portion-in-your-application-s-registry-tree-to-manage-the-settings)
- [Использование метода SetOption из DAO](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/using-the-setoption-method-from-dao)
- [Использование свойств подключения в поставщике Microsoft OLE DB для Access](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/using-the-connection-properties-in-the-microsoft-ole-db-provider-for-access)

