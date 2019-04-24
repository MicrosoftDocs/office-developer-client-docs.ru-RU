---
title: Настройка DataFactory
TOCTitle: DataFactory customization
ms:assetid: 43cd7416-1f05-87ee-22f0-6cf0d2d1b39f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249205(v=office.15)
ms:contentKeyID: 48544511
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a5fc1c284ee7aae77c4fb067ad57d50200119594
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294507"
---
# <a name="datafactory-customization"></a>Настройка DataFactory


**Область применения**: Access 2013, Office 2013

Удаленная служба данных (RDS) позволяет легко осуществлять доступ к данным в трехуровневой клиент-серверной системе. Клиентский элемент управления данными определяет параметры подключения и командной строки для выполнения запроса на удаленном источнике данных, строки подключения и параметры объекта [Recordset](recordset-object-ado.md) для выполнения обновления.

Параметры передаются в серверную программу, которая выполняет операцию доступа к данным на удаленном источнике данных. RDS предоставляет программу сервера по умолчанию с именем [рдссервер.](datafactory-object-rdsserver.md) DataObject. Объект **рдссервер.** DataObject возвращает любой объект **Recordset** , созданный запросом к клиенту.

Тем не менее, **рдссервер.** для фактов ограничено выполнение запросов и обновлений. Она не может выполнять проверку или обработку для подключения или командных строк.

С помощью ADO вы можете указать, что данные в **самом деле** работают совместно с другими типами серверных программ, которые ** называют обработчиком. Обработчик может изменить клиентское соединение и строки команд, прежде чем они будут использоваться для доступа к источнику данных. Кроме того, обработчик может применять права доступа, которые определяют способность клиента считывать и записывать данные в источник данных.

Параметры, используемые обработчиком для изменения параметров клиента и прав доступа, указаны в разделах файла настройки.

В следующих разделах приВодятся дополнительные сведения о настройке объекта **факты** данных:

- [Understanding the Customization File](understanding-the-customization-file.md)
- [Раздел Connect в файле настройки](customization-file-connect-section.md)
- [Раздел SQL в файле настройки](customization-file-sql-section.md)
- [Раздел UserList в файле настройки](customization-file-userlist-section.md)
- [Раздел Logs в файле настройки](customization-file-logs-section.md)
- [Обязательные параметры клиента](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/required-client-settings)
- [Создание собственного пользовательского обработчика](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/writing-your-own-customized-handler)
