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

Служба удаленных данных (RDS) позволяет легко выполнять доступ к данным в трехуровневой клиентской/серверной системе. Управление данными клиента указывает параметры строки подключения и команды для выполнения запроса на удаленном источнике данных или параметры объектов строки подключения и [Recordset](recordset-object-ado.md) для выполнения обновления.

Параметры передаются серверной программе, которая выполняет операцию доступа к данным на удаленном источнике данных. RDS предоставляет серверную программу по умолчанию под названием [объект RDSServer.DataFactory.](datafactory-object-rdsserver.md) Объект **RDSServer.DataFactory** возвращает клиенту любой объект **Recordset,** производимый запросом.

Однако **RDSServer.DataFactory** ограничивается выполнением запросов и обновлений. Он не может выполнять проверку или обработку в строках подключения или команд.

С помощью ADO можно указать, что **DataFactory** работает в сочетании с другим типом серверной программы, называемой *обработчиком.* Обработник может изменять клиентские подключения и строки команд, прежде чем они будут использоваться для доступа к источнику данных. Кроме того, обработник может применять права доступа, которые регулируют возможность клиента читать и записывать данные в источник данных.

Параметры, которые обработник использует для изменения параметров клиента и прав доступа, указаны в разделах файла настройки.

Дополнительные сведения о настройке объекта **DataFactory** см. в следующих разделах:

- [Understanding the Customization File](understanding-the-customization-file.md)
- [Раздел Connect в файле настройки](customization-file-connect-section.md)
- [Раздел SQL в файле настройки](customization-file-sql-section.md)
- [Раздел UserList в файле настройки](customization-file-userlist-section.md)
- [Раздел Logs в файле настройки](customization-file-logs-section.md)
- [Обязательные параметры клиента](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/required-client-settings)
- [Написание собственного настраиваемой обработки](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/writing-your-own-customized-handler)
